---
visibility: restricted
---
# SIDN fonds Pioniers 2026 — aanvraag (concept)

Concept voor FundPro-aanvraag 141866. Veldspecificatie: `sidn-fundpro-form.md`. Bronnen: `sidn-webform-v2.md`, `sidn-antwoorden-jet-veldhuis.md`, `brains/docs/atproto-lexicons.md`, `brains/docs/plans/atproto-integration.md`.

Scope (besloten 2026-09-15): zelfstandig uitvoeren, geen partner en geen bron van een ander; de tweede bron is van mij op gescheiden infrastructuur. Eigen lexicon, zoals aan Jet beloofd: onderwerpen, eenheden, verwijzingen, peers, en zichtbaarheid per record met drie waarden. Levering aan alleen-peers wordt in dit project gebouwd als proof of concept. Standard.site krijgt één alinea in de contextanalyse, als aangrenzend protocol met een ander doel.

Registerregels: Nederlands, geen em-dashes, platte tekst, geen partners die niet zijn toegezegd (één keer gemeld, in Team), geen node-aantallen, geen titelclaims, Rizom als open-source project. Velden max 2000 tekens tenzij anders vermeld.

Besloten 2026-09-15: specificatie en lexiconbestanden onder Apache 2.0, gelijk aan de bestaande lexicons; start 2026-11-16, einde 2027-05-15; budget 246 uur à €60, 166 uur aangevraagd (€9.960), 80 uur eigen bijdrage.

Besloten 2026-09-15: geen partner in de aanvraag en geen afhankelijkheid van anderen. Concept-vragen aan INC (`inc-ask-second-source.md`) en Niels/GGF (`ggf-ask-niels-second-source.md`) worden niet verstuurd.

---

## Titel project

Een open lexicon voor verwijzen en delen tussen zelfgehoste kennisbronnen

## Startdatum / Einddatum

2026-11-16 / 2027-05-15

## Korte beschrijving project (max 200)

Een open lexicon op het AT Protocol waarmee zelfgehoste kennisbronnen elkaar vinden, stabiel naar elkaar verwijzen en per record bepalen wat zij delen. Specificatie plus referentiecode onder AGPL.

## Aanleiding

Zelfgehoste kennisbronnen bestaan al: onderzoekers en praktijkmensen met een eigen kennisbank, onderzoeksgroepen, archieven en maatschappelijke organisaties die in eigen beheer publiceren. Wat ontbreekt is de laag waarmee zulke bronnen elkaar vinden en naar elkaar verwijzen zonder tussenpartij. Er is geen afgesproken vorm waarin een bron zegt: dit houd ik bij, zo verwijs je ernaar, en dit deel ik met wie.

Dat levert drie problemen op. Onzichtbaarheid: zelfgehoste kennis bestaat praktisch niet buiten de kring die het adres al kent; wie vindbaar wil zijn, moet terug naar een platform dat de verbinding als bezit behandelt. Brekende verwijzingen: verwijzen gebeurt met kale URL's naar hele pagina's, zonder semantiek en zonder stabiele sleutel, en breekt zodra een bron haar structuur wijzigt. Alles of niets: een bron publiceert een record of niet; delen met een beperkte kring, per record, bestaat nergens als afgesproken vorm. Dat laatste leeft breder: het AT Protocol heeft er sinds augustus 2026 met Spaces een eerste vorm voor, in alfa, maar nog geen schema dat zegt wat een bron deelt en met wie.

Ik ken de behoefte uit praktijk, niet uit marktonderzoek. Door mijn werk voor PublicSpaces, de coalitie van Nederlandse publieke organisaties voor een internet op publieke waarden, heb ik gezien hoe leden platformonafhankelijke infrastructuur zoeken en hoe juist deze laag ontbreekt. Met Offcourse, het open-source platform voor kennisdeling tussen praktijkmensen dat ik in 2013 oprichtte, heb ik zeven jaar gezien dat mensen die elkaar hadden moeten vinden, elkaar niet vonden. En met Rizom, het open-source project waarin ik zelfgehoste kennisbronnen op open protocollen bouw, publiceer ik al records op het AT Protocol en loop ik tegen precies deze drie gaten aan.

De toets van die praktijkkennis zit in het project: in de eerste maand voer ik tien gestructureerde gesprekken met mensen en organisaties die hun kennis al zelf hosten, en de uitkomst bepaalt de vorm van de recordtypen.

## Aanpak

Hoe het werkt. Elke bron heeft een identiteit op haar eigen domein (did:web), zonder register op te lossen, en een eigen repository met vier soorten records. Onderwerp: wat de bron bijhoudt. Eenheid: een verwijsbaar deel van de inhoud met een stabiele sleutel die de bron zelf beheert. Verwijzing: een getypt record naar een eenheid in andermans bron, via identiteit plus sleutel, dat blijft werken zolang die bron bestaat, ook als paden wijzigen. Peer: welke bronnen deze bron erkent. Elk record draagt een zichtbaarheid: publiek, alleen voor peers, of verlaat de bron nooit.

Vinden zonder centrale partij gaat langs drie wegen. Op onderwerp: wie een domein kent, leest de onderwerpen en eenheden rechtstreeks. Via verwijzingen: elke verwijzing en elk peer-record wijst naar een andere bron, dus je loopt van bron naar bron zoals via hyperlinks, maar getypt en machine-leesbaar. Via indexen: iedereen kan er een bouwen over de publieke records, geen enkele is vereist. Elke bron beslist zelf wie zij als peer erkent.

Delen op eigen voorwaarden. Records voor alleen-peers gaan niet in het publieke repository. Zij staan in een afgeschermd repository op de eigen host van de bron, volgens het Spaces-model dat het AT Protocol sinds augustus 2026 in alfa heeft: de bron bepaalt welke identiteiten mogen lezen, er is geen relay, en een erkende peer leest rechtstreeks bij de bron, geauthenticeerd op zijn DID. Omdat Spaces alfa is, werkt de leveringsweg ook als de bron die records zelf serveert. Records die de bron nooit verlaten, komen in geen repository.

Vijf stappen.
1. Maand 1 en 2: tien ontwerpgesprekken, ontwerp, specificatie.
2. Maand 2 tot 4: referentie-implementatie, publiceren, lezen en levering aan peers vanaf de eigen host, AGPL in github.com/rizom-ai/brains.
3. Maand 4 en 5: demonstratie tussen yeehaa.io en rizom.ai, zeven stappen (zie Projectresultaten).
4. Maand 5: conformiteitstestset en handleiding.
5. Maand 6: publicatie van specificatie en verslag.

## Innovatie

Bestaande protocollen lossen aangrenzende problemen op. ActivityPub regelt berichtenverkeer voor sociale objecten; ontdekking loopt via volgrelaties en er is geen schema voor wat een bron als geheel bevat. OAI-PMH oogst metadata voor formele publicaties via centrale harvesters, veronderstelt institutionele infrastructuur en kent geen voorwaarden per record. RSS en sitemaps kondigen aan maar verwijzen niet. Schema.org levert vocabulaire zonder identiteits- en transportlaag en dient centrale crawlers. Solid biedt pods met toegangscontrole, maar hoe pods elkaar vinden is er niet opgelost.

Het AT Protocol levert de fundering: verplaatsbare identiteit, een repository per actor, lexicons als afdwingbaar schema. Op die fundering staan inmiddels lexicons voor sociale objecten en, sinds 2026 met standard.site, voor publiceren: een publicatie, een document, een abonnement, een aanbeveling, bedoeld om essays in leesfeeds te brengen. Dat is een uitzendlaag voor lezers. Wat er niet is, is een laag tussen bronnen: een record dat zegt welk stuk van mij op welk stuk van jou bouwt, en wie dat mag zien. Het gat is geen ontbrekend protocol maar een ontbrekend schema, en ATProto heeft precies het mechanisme om dat schema te publiceren.

Dit project vult dat schema in, met drie dingen die nu nergens bestaan als afgesproken vorm. Een bron vinden op onderwerp, rechtstreeks, zonder index ertussen. Stabiel verwijzen naar een eenheid in andermans bron, onafhankelijk van paden en platforms. En per record bepalen wat publiek is, wat alleen peers zien en wat de bron nooit verlaat, met een werkende leveringsweg voor het middelste geval vanaf de eigen host van de bron, aansluitend op het Spaces-model van het protocol.

Het bouwt op Rizom, waar al negen lexicons protocol-natief gepubliceerd staan onder een via DNS gedelegeerde naamruimte en twee bronnen live draaien. Het mechanisme om een schema te publiceren en te valideren is er; dit project gebruikt het voor de laag die ontbreekt.

## Projectresultaten

Na zes maanden ligt er:

1. Een gepubliceerde specificatie van vier recordtypen (onderwerp, eenheid, verwijzing, peer) en een zichtbaarheidsveld met drie waarden, onder Apache 2.0, protocol-natief gepubliceerd en implementeerbaar zonder mijn code.

2. Een referentie-implementatie onder AGPL in een publieke repository, die alle recordtypen publiceert en leest en records voor alleen-peers rechtstreeks aan erkende peers levert.

3. Een demonstratie tussen yeehaa.io en rizom.ai, twee bronnen die al live op het protocol staan en niets delen: verschillende domeinen, verschillende servers, eigen repository en eigen sleutels. Beide beheer ik zelf; de onafhankelijkheid die de demonstratie toetst, is technisch. Een gedocumenteerde reeks van zeven stappen die alle slagen: A publiceert onderwerpen en eenheden; B vindt A op onderwerp; B verwijst naar een eenheid in A; A wijzigt haar paden en de verwijzing blijft oplossen; A markeert een record als alleen-peers en erkent B; B haalt het op; een derde bron zonder erkenning krijgt het niet.

4. Een conformiteitstestset van ten minste twintig testgevallen, geldige en ongeldige records per type, plus een implementatiehandleiding van hooguit tien pagina's.

5. Specificatie en testset voorgelegd aan ten minste vijf bouwers van tools voor zelfgehoste sites en projecten met eigen lexicons op het AT Protocol, met schriftelijke reactie van ten minste drie. Een onafhankelijke tweede implementatie binnen de looptijd is het streven.

6. Een openbaar verslag van methode en bevindingen, inclusief wat niet werkte en wat de ontwerpgesprekken hebben veranderd.

Meetbaar op de dag van oplevering: de zeven demonstratiestappen slagen, de testset draait groen tegen de referentie-implementatie, en de specificatie is op haar protocol-natieve adres op te halen.

## Aansluiting doelstellingen fonds

Dit project rust op het domeinnaamsysteem. De identiteit van een bron is haar domein (did:web), dus een .nl-domein wordt de identiteit van een kennisbron; de naamruimte van het lexicon is via DNS gedelegeerd; en de demonstratiebronnen worden op internet.nl getoetst, inclusief DNSSEC. Dat is rechtstreeks relevant voor de Nederlandse internetinfrastructuur, en het schema is daarbuiten net zo bruikbaar, omdat het op een open protocol staat en door wie dan ook te implementeren is.

Het levert de vier waarden die het fonds noemt. Veiligheid: ondertekende records, dubbele domeinbinding, geen automatische toelating. Autonomie: elke bron beheert haar eigen identiteit, sleutels en peer-lijst. Privacy: zichtbaarheid per record, met een leveringsweg die het publieke repository omzeilt. Openheid: specificatie onder Apache 2.0, code onder AGPL, alles zonder toestemming te gebruiken.

Ontdekking en verwijzing zijn nog grotendeels gecentraliseerde functies: wie wat vindt, en of een verwijzing blijft werken, bepalen een handvol zoekmachines en platforms. Dit project maakt van vinden en verwijzen een protocolfunctie, en van delen een keuze die de bron zelf maakt. Het mechanisme heeft alleen waarde tussen onafhankelijke partijen, dus het kan niet worden dichtgetrokken, ook niet door mij.

Het verlaagt de drempel om kennis zelf te hosten. Zelf hosten betekent nu isolement; met deze laag betekent het volwaardig meedoen. Elke bron die daardoor buiten een platform blijft bestaan, maakt het internet een stukje gedecentraliseerder.

Samenwerking in de Nederlandse internetsector: de host voor levering aan peers van de tweede demonstratiebron, een nieuw onderdeel uit dit project, zet ik bij een Nederlandse hostingpartij die op publieke waarden werkt; daarnaast benader ik organisaties die ik door mijn werk voor PublicSpaces ken en de gemeenschap rond ISOC Nederland als gesprekspartners voor het ontwerp.

## Doelgroep

Vijf groepen, in volgorde van verwachte adoptie.

1. Mensen met een eigen publieke kennisbank die hun notities al als website publiceren, meestal vanuit Obsidian via Quartz, of met Hugo, Eleventy of Zola. De bron bestaat; de laag waarmee anderen haar vinden niet.

2. Onderzoeksgroepen en lectoraten die buiten de formele repository om in eigen beheer publiceren en naar elkaar willen verwijzen zonder uitgever of platform ertussen.

3. Instituten en archieven die hun eigen publicaties uitgeven en hosten, zoals het Instituut voor Netwerkcultuur, en maatschappelijke organisaties met een eigen kennisbank. Voor hen is zichtbaarheid per record de doorslag: delen met een beperkte kring is nu onmogelijk zonder platform.

4. Bouwers van de tools uit groep 1. Een Quartz-plugin of Hugo-module die de records en een DID-document uitschrijft, brengt het lexicon naar iedereen die die tool gebruikt.

5. Projecten met eigen lexicons op het AT Protocol voor niet-sociale inhoud, zoals Leaflet, WhiteWind, Frontpage en Smoke Signal. Zij gebruiken het schema-mechanisme al en zijn de eerste kandidaten voor een onafhankelijke implementatie.

Wat bredere toepassing bepaalt, en welke keuze daarop antwoordt:
- Meedoen moet een dag werk zijn: daarom vier kleine recordtypen en een DID-document; alleen wie aan peers levert, draait een klein servercomponent.
- Waarde al bij twee bronnen: daarom is de demonstratie tussen precies twee bronnen het kernresultaat.
- Niemand mag de toegang beheren: daarom did:web op het eigen domein, geen register, geen aanmelding.
- Een implementator moet zichzelf kunnen controleren: daarom de conformiteitstestset.
- Specificatie los van mijn code: daarom apart, protocol-natief, onder open licentie.

Betrokkenheid: uit groep 1 tot 3 tien ontwerpgesprekken in maand 1 (drie, drie en vier). Groep 4 en 5 krijgen in maand 5 en 6 specificatie, testset en handleiding, met de vraag om een onafhankelijke implementatie.

## Communicatie

De specificatie, de testset en de handleiding worden gepubliceerd waar implementatoren ze verwachten: protocol-natief op het AT Protocol, in de publieke repository op GitHub, en op het lexiconregister van rizom.ai. Methode en bevindingen verschijnen als openbare tekst op yeehaa.io, mijn eigen zelfgehoste bron, die zelf een van de twee demonstratiebronnen is.

Zelfhosters en kleinere instellingen bereik ik rechtstreeks: via de organisaties die ik door mijn werk voor PublicSpaces ken, via het netwerk rond Offcourse, en via de gemeenschap rond ISOC Nederland.

Bouwers en het AT Protocol-ecosysteem bereik ik via de ontwikkelaarskanalen van het protocol en via de projecten die er al eigen lexicons op publiceren. De aanleiding is steeds de specificatie en de testset zelf, niet een aankondiging.

## Toegankelijkheid

Het lexicon zelf is een machine-leesbare laag zonder gebruikersinterface. De onderdelen die mensen lezen, zijn de specificatie, de handleiding, het verslag en de twee demonstratiebronnen. Die worden gepubliceerd als semantische HTML met platte tekst als bron, zonder afhankelijkheid van kleur of beeld voor betekenis, met voldoende contrast en volledig te bedienen met toetsenbord en schermlezer. Mijn demonstratiebron draait op dezelfde software als yeehaa.io, dat op deze punten al is ingericht; ik toets beide bronnen en het lexiconregister na oplevering.

## Delen kennis & resultaten

De specificatie verschijnt onder Apache 2.0, protocol-natief op het AT Protocol en als leesbare tekst. De referentie-implementatie staat onder AGPL in github.com/rizom-ai/brains; de SDK is Apache-gelicentieerd. Testset en handleiding staan in dezelfde repository. Alles is zonder toestemming of afname te gebruiken.

Voor wie bruikbaar: bouwers van tools voor zelfgehoste sites implementeren de recordtypen; beheerders van bestaande bronnen doen mee zonder hun software te vervangen; wie aan Spaces of aan niet-publieke gegevens in het AT Protocol werkt, krijgt een uitgewerkt en getest schema voor delen op eigen voorwaarden om op te bouwen of tegen af te zetten.

Het verslag beschrijft methode, ontwerpkeuzes en bevindingen, inclusief wat niet werkte: waar verwijzingen op het verkeerde kenmerk ontstaan, waar het signaal te dun is om iets te dragen, welke onderdelen in de ontwerpgesprekken sneuvelden, en wat de levering aan peers in de praktijk kost. Dat is de kennis die het meest waard is voor wie na mij iets soortgelijks bouwt.

## Team

Ik voer het project zelf uit. Ik bouw sinds 2013 open-source infrastructuur voor kennisdeling: Offcourse, het platform voor kennisdeling tussen praktijkmensen; werk voor PublicSpaces, de coalitie van Nederlandse publieke organisaties voor een internet op publieke waarden; en Rizom, het open-source project waarin ik zelfgehoste kennisbronnen op open protocollen bouw. De software waarop dit project voortbouwt, inclusief de al gepubliceerde lexicons en de identiteitslaag, is van mijn hand. De software wordt ook door anderen gebruikt om eigen bronnen op te zetten, zodat de referentie-implementatie niet alleen door mij wordt getest. Het project vraagt 246 uur in zes maanden, ruim tien uur per week naast mijn overige werk; de planning is daarop gemaakt en de volgorde van de stappen is zo gekozen dat het publieke deel af is voordat de levering aan peers begint.

Buiten mijzelf kent het project twee rollen: de tien gesprekspartners in het ontwerp en meelezers op de specificatie uit de AT Protocol-gemeenschap. Die zijn nog niet toegezegd; zodra dat wel zo is, meld ik het. Het project is zo opgezet dat het niet van hen afhangt.

## Duurzaamheid

De opbrengst hangt niet van mij af. De specificatie staat los van de implementatie, is protocol-natief gepubliceerd onder een via DNS gedelegeerde naamruimte, en blijft opvraagbaar zolang het AT Protocol bestaat. De code is publiek onder AGPL. Wie het lexicon implementeert, heeft mij daarna niet nodig.

Onderhoud: het lexicon volgt een gepubliceerd compatibiliteitsbeleid (compatibele wijzigingen zonder versiesprong, onverenigbare alleen via een nieuwe versie), en wijzigingen lopen via de publieke repository. Ik onderhoud het als onderdeel van Rizom, mijn doorlopende werk, waar het in productie draait.

Dit project heeft geen eerdere steun ontvangen. Vervolg: dit project levert de specificatie en de eerste werkende implementatie, inclusief de levering aan peers als proof of concept. Het uitharden tot productiefederatie tussen zelfgehoste bronnen, met portabiliteit en verpakking voor zelfhosting, is aangrenzend werk waarvoor ik een aanvraag voorbereid bij NLnet in het NGI Zero-programma Open Internet Stack. Dat bouwt voort op dit project en overlapt er niet mee; ik meld de relatie in beide aanvragen.

Financieel vraagt het lexicon na oplevering geen geld: het is een schema, geen dienst. Het lexiconregister op rizom.ai en mijn eigen bron draaien al en blijven draaien als onderdeel van Rizom.

## Privacy

Het project verwerkt geen persoonsgegevens van derden en bevat geen algoritmische besluitvorming of AI. De enige gegevens die het lexicon draagt, zijn wat een bronhouder zelf besluit te publiceren over de eigen bron. Beide demonstratiebronnen beheer ik zelf.

Het zichtbaarheidsveld is zelf een privacymechanisme. Per record staat vast of het de bron mag verlaten en voor wie. De publicatiestap zet alleen publieke records in het repository en weigert de rest; records voor alleen-peers staan in een afgeschermd repository op de eigen host van de bron, zijn alleen leesbaar voor peers die de beheerder zelf heeft erkend, gaan niet door een relay, en worden nergens anders opgeslagen dan bij de bron en de ontvangende peer. Spaces biedt toegangscontrole, geen versleuteling; dat staat als grens in de specificatie en het verslag.

De referentie-implementatie en de demonstratiebronnen verzamelen geen bezoekersgegevens, gebruiken geen tracking en plaatsen geen cookies. Van de gesprekspartners leg ik alleen naam en contactgegevens vast, met instemming, voor de duur van het project.

## Security

Het lexicon rust op de beveiligingslaag van het AT Protocol: publieke records worden ondertekend in de repository van de bron, en de identiteit van een bron is aan haar domein gebonden via did:web. De referentie-implementatie controleert die binding in beide richtingen (het domein moet naar de identiteit wijzen en de identiteit naar het domein) voordat zij een bron als peer erkent.

Levering aan peers gebruikt de authenticatie van het protocol zelf: de peer ondertekent zijn verzoek met de sleutel uit zijn DID-document, en de host van de bron controleert de handtekening tegen dat document en tegen de peer-lijst voordat zij iets teruggeeft. Een niet-erkende bron krijgt hetzelfde antwoord als voor een record dat niet bestaat. Een bron die aan peers levert, draait of beheert daarvoor een eigen host; de referentie-implementatie levert die.

Alle records worden lokaal tegen het lexicon gevalideerd voordat zij worden gepubliceerd of verwerkt; ongeldige of onoplosbare records worden geweigerd, niet genegeerd. Onbekende bronnen worden niet automatisch toegelaten.

Al het verkeer loopt over HTTPS. De demonstratiebronnen en het lexiconregister worden na oplevering getoetst op internet.nl, inclusief DNSSEC en de moderne TLS- en mailstandaarden; yeehaa.io wordt op die punten al bijgehouden. De conformiteitstestset bevat bewust ongeldige en kwaadwillige records en verzoeken (verkeerde binding, vervalste handtekening, verwijzingen naar niet-bestaande eenheden, te grote velden), zodat implementatoren hun invoercontrole kunnen toetsen.

## SIDN fonds (max 500)

Via de website van SIDN fonds. In augustus 2026 diende ik een eerste projecttoets in, die op aansluiting werd afgewezen; na een opnieuw afgebakende tweede toets en aanvullende vragen van Jet Veldhuis ben ik uitgenodigd deze aanvraag in te dienen.

---

## Budget

Uurtarief €60 (intern, richtlijn SIDN). Project 246 uur; aangevraagd 166 uur = €9.960; eigen bijdrage 80 uur = €4.800.

| Kostensoort | Uren totaal | Totale kosten | Aangevraagd |
|---|---|---|---|
| Ontwerpgesprekken (10) en verwerking | 30 | €1.800 | €1.200 |
| Ontwerp lexicon en specificatie | 46 | €2.760 | €2.760 |
| Referentie-implementatie incl. levering aan peers | 90 | €5.400 | €3.600 |
| Demonstratie tussen twee bronnen | 30 | €1.800 | €1.200 |
| Conformiteitstestset en handleiding | 30 | €1.800 | €960 |
| Verslag en publicatie | 20 | €1.200 | €240 |
| **Totaal** | **246** | **€14.760** | **€9.960** |

Cofinanciering: geen. Eigen bijdrage: 80 uur (€4.800) plus hosting van mijn demonstratiebron en het lexiconregister.

## Bijlagen

- Projectplan (optioneel, max 4 A4): geschreven, zie `sidn-pioniers-projectplan` (PDF lokaal in ~/Documents).
- Begroting (optioneel, max 2 A4): de tabel hierboven volstaat in het formulier.
- Videopitch (verplicht, max 3 min): script geschreven, zie `sidn-pioniers-videopitch`; nog op te nemen.
