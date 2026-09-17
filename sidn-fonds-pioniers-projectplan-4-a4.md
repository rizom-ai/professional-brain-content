---
visibility: restricted
---
# Een open lexicon voor verwijzen en delen tussen zelfgehoste kennisbronnen

*Projectplan bij de Pioniers-aanvraag, SIDN fonds. Jan Hein Hoogstad, september 2026. Bron: `~/Documents/sidn-pioniers-projectplan.md`, gerenderd als vier pagina's A4 (`sidn-pioniers-projectplan.pdf`).*

## 1. Wat het project bouwt

Een zelfgehoste kennisbron is een website of archief dat iemand op eigen infrastructuur publiceert: een onderzoeker met een kennisbank, een lectoraat, een instituut met een eigen archief. Zulke bronnen kunnen elkaar nu niet vinden zonder tussenpartij, kunnen niet stabiel naar een deel van elkaars inhoud verwijzen, en kunnen niet per record bepalen wie iets te zien krijgt.

Dit project levert een lexicon op het AT Protocol dat die drie dingen mogelijk maakt, een referentie-implementatie onder AGPL, een demonstratie tussen twee bronnen zonder gedeelde infrastructuur, en een conformiteitstestset waarmee anderen hun eigen implementatie kunnen toetsen. De specificatie en de lexiconbestanden verschijnen onder Apache 2.0.

Het AT Protocol levert de fundering: een identiteit per bron, een ondertekend repository per identiteit, en lexicons als afdwingbaar schema dat protocol-natief wordt gepubliceerd. Op die fundering bestaan lexicons voor sociale objecten en, met standard.site, voor het uitzenden van publicaties naar leesfeeds. Er bestaat geen schema voor wat een bron bijhoudt, hoe je naar een deel ervan verwijst, en met wie zij dat deelt. Dat schema is de opbrengst.

## 2. Identiteit en repository

Elke bron heeft een identiteit op haar eigen domein: `did:web:<domein>`. Het DID-document staat op `https://<domein>/.well-known/did.json` en is zonder register op te lossen; wie het domein kent, kent de bron. Het document wijst naar het repository van de bron en naar de sleutel waarmee de bron zich als peer bij anderen legitimeert. Het repository is een ondertekende recordverzameling op een host die de bron zelf beheert of kiest.

De binding wordt in twee richtingen gecontroleerd: het domein moet naar de identiteit wijzen en de identiteit terug naar het domein. Zonder die dubbele binding erkent de referentie-implementatie een bron niet.

## 3. De recordtypen

Vier recordtypen, gepubliceerd onder een naamruimte die ik beheer en die via DNS aan mijn identiteit is gedelegeerd, zoals de negen lexicons die daar al staan. Elk record draagt een veld `visibility` met de waarden `public`, `peers` of `private`.

**Onderwerp** (`topic`). Wat de bron bijhoudt: een naam, een korte omschrijving, en optioneel een verwijzing naar een breder onderwerp bij een andere bron. Dit is de ingang voor vinden op onderwerp. Bouwt voort op het bestaande topic-record in mijn naamruimte, dat nu alleen een projectie van een lokaal onderwerp is.

**Eenheid** (`unit`). Een verwijsbaar deel van de inhoud: een alinea, een sectie, een tabel, een bestand. De bron kiest de sleutel en houdt die stabiel, los van het pad waarop de inhoud op het web staat. Het record bevat de sleutel, een titel, de onderwerpen waar het onder valt, het huidige webadres, en een hash van de inhoud zodat een verwijzer kan zien of de eenheid sinds de verwijzing is veranderd.

**Verwijzing** (`reference`). Een getypt record van de ene bron naar een eenheid in een andere: de identiteit van die bron plus de sleutel van de eenheid, de aard van de relatie uit een kleine vaste set (bouwt op, citeert, spreekt tegen, vervangt), en optioneel de eigen eenheid waaruit de verwijzing komt. De verwijzing hangt aan identiteit plus sleutel, niet aan een URL, en blijft dus werken zolang de bron bestaat.

**Peer** (`peer`). Welke andere bron deze bron erkent, en sinds wanneer. Erkenning is lokaal en eenzijdig: een bron erkent wie zij wil, en alleen een erkende peer krijgt de records met zichtbaarheid `peers`.

## 4. Hoe vinden werkt zonder centrale partij

Drie wegen, alle drie zonder register of centrale index.

**Op onderwerp, rechtstreeks.** Wie een domein kent, lost het DID-document op, vindt het repository en leest de onderwerpen en eenheden. Dat is één HTTPS-verzoek naar het domein en één naar de host van het repository. Geen tussenpartij ziet dat verzoek.

**Via verwijzingen.** Elke verwijzing en elk peer-record bevat de identiteit van een andere bron. Vanuit één bekende bron loopt een lezer dus naar elke bron waar die naar verwijst, en van daar verder. Dat is het web-mechanisme van de hyperlink, maar getypt: een verwijzing zegt welk stuk op welk stuk bouwt, en is machine-leesbaar.

**Via indexen, als iemand die wil.** Publieke records lopen door de gewone relay van het protocol. Iedereen kan daarover een index bouwen, op onderwerp of op verwijzingsgraaf. Zulke indexen zijn meervoudig en vervangbaar: valt er een weg, dan verandert er niets aan de bronnen of aan de eerste twee wegen. Het project bouwt geen index; het laat zien dat er geen nodig is.

Organisatorisch: er is niets om je bij aan te melden. Een bron doet mee door records te publiceren. Wie iets ziet, bepaalt de bron per record; wie als peer geldt, bepaalt de bron per peer-record.

## 5. Delen op eigen voorwaarden

Het publieke repository van een bron is publiek, en de relay verspreidt het. Records met `visibility: public` gaan daarin. De twee andere waarden vragen iets anders.

`private`: het record verlaat de bron nooit. De publicatiestap van de referentie-implementatie weigert het, ook per ongeluk; het bestaat alleen in de lokale opslag van de bron.

`peers`: het record gaat in een afgeschermd repository op de eigen host van de bron, volgens het Spaces-model dat het AT Protocol sinds augustus 2026 in alfa heeft. De bron bepaalt welke identiteiten dat repository mogen lezen; die lijst is haar peer-lijst. Er is geen relay: een erkende peer leest rechtstreeks bij de host van de bron, en legitimeert zich met een verzoek dat is ondertekend met de sleutel uit zijn DID-document. De host controleert die handtekening tegen het DID-document en tegen de peer-lijst. Een niet-erkende bron krijgt hetzelfde antwoord als voor een record dat niet bestaat.

Omdat Spaces alfa is en breaking changes aankondigt, bouwt het project de leveringsweg zo dat zij ook werkt als de bron de peers-records zelf serveert vanaf een eigen endpoint met dezelfde authenticatie. De specificatie beschrijft beide; de demonstratie gebruikt wat op dat moment stabiel is. Spaces biedt toegangscontrole, geen versleuteling. Dat staat als grens in de specificatie: `peers` betekent leesbaar voor erkende peers en voor de host van de bron, niet meer.

Consequentie voor wie meedoet: een bron die alleen publiceert, heeft geen eigen server nodig, alleen een domein en een repository bij een host naar keuze. Een bron die aan peers levert, draait of beheert een eigen host. De referentie-implementatie levert die host.

## 6. De demonstratie als testprotocol

Twee bronnen die al live op het protocol staan en niets delen. A is yeehaa.io, B is rizom.ai: verschillende domeinen, verschillende servers, eigen repository en eigen sleutels. Beide beheer ik zelf; de onafhankelijkheid die de reeks toetst, is technisch: geen gedeelde infrastructuur, identiteit of sleutel. B is tevens de naamruimte-autoriteit van het lexicon; A laat daarmee zien dat een bron die de autoriteit niet is, het schema gewoon gebruikt. De host voor levering aan peers van B, een nieuw onderdeel uit dit project, komt bij een Nederlandse hostingpartij op publieke waarden. Een derde bron C, zonder erkenning, dient in de laatste stap. Elke stap heeft een controleerbaar slagingscriterium.

| Stap | Handeling | Slaagt als |
|---|---|---|
| 1 | A publiceert onderwerpen en eenheden | De records zijn via het DID-document van A en het repository op te halen, zonder andere ingang |
| 2 | B vindt A op onderwerp | B, met alleen het domein van A, toont de eenheden van A onder één opgegeven onderwerp |
| 3 | B verwijst naar een eenheid in A | Het verwijzingsrecord in het repository van B lost op naar de eenheid in A, met kloppende inhoudshash |
| 4 | A wijzigt haar paden | Het webadres van de eenheid verandert; de verwijzing van B lost nog steeds op en toont het nieuwe adres |
| 5 | A markeert een record `peers` en erkent B | Het record staat niet in het publieke repository van A en niet in de relay |
| 6 | B haalt het record op | B leest het record bij de host van A na ondertekend verzoek |
| 7 | C probeert hetzelfde | C, zonder erkenning, krijgt het antwoord voor een niet-bestaand record |

De reeks wordt uitgevoerd als geautomatiseerde test tegen de twee live bronnen en als handmatige demonstratie, opgenomen en gepubliceerd.

## 7. Conformiteitstestset en handleiding

De testset bestaat uit ten minste twintig gevallen: per recordtype geldige en ongeldige records, plus verzoeken met een verkeerde binding tussen domein en identiteit, een vervalste handtekening, een verwijzing naar een niet-bestaande eenheid, en te grote velden. Elk geval is een bestand met de verwachte uitkomst. Een kleine opdrachtregeltool leest de gevallen en toetst een implementatie via haar publieke endpoints, zodat iemand zijn eigen implementatie kan controleren zonder mijn code te draaien.

De handleiding, hooguit tien pagina's, beschrijft wat een implementator minimaal moet doen om mee te doen (DID-document, vier recordtypen, publicatie) en wat erbij komt voor levering aan peers.

## 8. Planning

| Maand | Werk | Resultaat |
|---|---|---|
| 1 | Tien ontwerpgesprekken met zelfhosters, onderzoeksgroepen en instituten; eerste ontwerp | Gespreksverslagen; ontwerpnotitie |
| 2 | Specificatie; DID-document uitgebreid met peer-sleutel; recordtypen gepubliceerd in alfa | Specificatie v0.1, protocol-natief gepubliceerd |
| 3 | Referentie-implementatie: publiceren en lezen op beide bronnen | Publieke records live op yeehaa.io en rizom.ai |
| 4 | Levering aan peers | Peers-records leesbaar tussen A en B |
| 5 | Demonstratie stap 1 tot 7; conformiteitstestset; handleiding | Testprotocol groen; testset en handleiding gepubliceerd |
| 6 | Specificatie v1.0; verslag; voorleggen aan implementatoren | Alles gepubliceerd; reacties verzameld |

Start 16 november 2026, einde 15 mei 2027.

## 9. Begroting

Uurtarief 60 euro. Project 246 uur; aangevraagd 166 uur; eigen bijdrage 80 uur plus hosting van mijn bron en het lexiconregister.

| Kostensoort | Uren | Kosten | Aangevraagd |
|---|---|---|---|
| Ontwerpgesprekken en verwerking | 30 | 1.800 | 1.200 |
| Ontwerp lexicon en specificatie | 46 | 2.760 | 2.760 |
| Referentie-implementatie incl. levering aan peers | 90 | 5.400 | 3.600 |
| Demonstratie tussen twee bronnen | 30 | 1.800 | 1.200 |
| Conformiteitstestset en handleiding | 30 | 1.800 | 960 |
| Verslag en publicatie | 20 | 1.200 | 240 |
| Totaal | 246 | 14.760 | 9.960 |

## 10. Risico's en wat ik dan doe

**Spaces verandert of valt weg tijdens het project.** De leveringsweg werkt ook vanaf een eigen endpoint van de bron met dezelfde authenticatie. De specificatie beschrijft beide vanaf het begin.

**Beide bronnen zijn van mij.** De demonstratie toetst het mechanisme, niet de adoptie. Dat is een grens van dit project en geen risico dat ik kan afdekken: of anderen het lexicon gaan gebruiken, blijkt pas na afloop. Wat het project wel geeft, zijn twee signalen. De tien gesprekken vooraf laten zien of de recordtypen aansluiten bij wat zelfhosters werkelijk bijhouden. De schriftelijke reacties achteraf laten zien of implementatoren de specificatie bruikbaar vinden. Meldt zich tijdens het project een externe beheerder voor B, dan neem ik die; het plan hangt er niet van af.

**De ontwerpgesprekken sneuvelen een recordtype.** Dan verandert de specificatie en meld ik in het verslag wat en waarom. De gesprekken zijn er om dat vóór de bouw te ontdekken.

**Tijd.** Het project is voor één persoon in zes maanden strak, en het is bewust zo opgezet dat geen stap op een ander wacht. De volgorde is daarop gekozen: publiek publiceren en verwijzen eerst, levering aan peers daarna. Valt het laatste deel uit de tijd, dan is de specificatie ervan af en de demonstratie tot stap 4 compleet; dat meld ik.

## 11. Wat er na afloop is

Een specificatie die los van mijn code bestaat en protocol-natief opvraagbaar blijft; code onder AGPL in een publieke repository; een testset waarmee een ander zichzelf kan toetsen; twee bronnen die elkaar vinden, citeren en op voorwaarden delen; en een verslag dat ook zegt wat niet werkte. Het uitharden tot productiefederatie en de vertrouwenslaag per record zijn aangrenzend werk, waarvoor ik bij NLnet (Restack) een aanvraag voorbereid die op dit resultaat voortbouwt.
