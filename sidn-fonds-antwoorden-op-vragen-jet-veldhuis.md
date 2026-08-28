# SIDN fonds — antwoorden op de vragen van Jet Veldhuis (na v2-toets)

**VERSTUURD 2026-08-28 aan Jet Veldhuis.**

**Context.** Jet Veldhuis reageerde 2026-08-27 op de v2-toets (`sidn-webform-v2.md`, ingediend 2026-08-23) met vijf aanvullende vragen. Alle vijf zijn vraagzijde-vragen (gebruikers, behoefte, positionering, meerwaarde); de techniek is geland. De antwoorden hieronder volgen haar volgorde exact, zodat ze direct in haar interne beoordeling passen.

Registerregels uit de de-AI pass aangehouden: Nederlands, geen em-dashes, geen markdown in de mailtekst, geen credentials-afsluiting, geen gesprek gevraagd. Geen partners genoemd die niet zijn toegezegd; geen node-aantallen geclaimd.

Lokale kopie: `~/Documents/sidn-antwoorden-jet-veldhuis.md`. Zie ook `sidn-fonds-pioniers-application-draft`.

---

Beste Jet,

Dank voor je vragen. Ik beantwoord ze in dezelfde volgorde.

Wie zijn de belangrijkste gebruikers?

Twee groepen. De eerste bestaat uit mensen en kleine organisaties die hun kennis al zelf hosten: onderzoekers en praktijkmensen met een eigen publieke kennisbank, en kleinere instellingen zoals onderzoeksgroepen, archieven en maatschappelijke organisaties die hun materiaal in eigen beheer publiceren. Zij hebben de bron al. Wat ze missen is de laag waarmee anderen die bron kunnen vinden en ernaar kunnen verwijzen. De tweede groep zijn bouwers van kennistools. Omdat de specificatie los van mijn code wordt gepubliceerd, kunnen zij deze laag in hun eigen software implementeren zonder iets van mij af te nemen.

Wat kunnen gebruikers dankzij het lexicon dat vandaag niet kan?

Vandaag is een zelfgehoste kennisbron alleen vindbaar voor wie het adres al kent, of via een zoekmachine of platform dat de verbinding bemiddelt en als bezit behandelt. Met het lexicon publiceert een bron machine-leesbaar wat zij bijhoudt, hoe je ernaar verwijst en onder welke voorwaarden. Drie dingen worden daarmee mogelijk die nu niet bestaan:

1. Een bron vinden op onderwerp, rechtstreeks, zonder centrale tussenpartij.
2. Stabiel citeren naar een specifieke eenheid in andermans bron, met een verwijzing die blijft werken zolang de bron bestaat, onafhankelijk van welk platform ertussenuit valt.
3. Per record bepalen wat publiek is, wat alleen voor peers beschikbaar is en wat de bron nooit verlaat. Publiceren is vandaag alles of niets; deelbaarheid op eigen voorwaarden bestaat op dit moment nergens als afgesproken vorm.

Hoe groot is de behoefte, en tegen welke concrete problemen lopen partijen aan?

Een eerlijk antwoord vooraf: dit is een Pioniersvraag, dus ik onderbouw de behoefte structureel en met eigen praktijkervaring, niet met marktcijfers.

De concrete problemen zijn er drie. Ten eerste onzichtbaarheid: zelfgehoste kennis bestaat praktisch niet buiten de kring die het adres al kent, terwijl het aantal zelfgehoste bronnen groeit, van persoonlijke kennisbanken tot institutionele repositories. Ten tweede brekende verwijzingen: verwijzen gebeurt nu met kale URL's zonder semantiek, en zodra een bron haar structuur wijzigt of een bemiddelend platform verdwijnt, breekt de verwijzing. Ten derde platformafhankelijkheid als enige uitweg: wie vindbaar wil zijn, moet terug naar een gecentraliseerde dienst en levert daarmee de verbinding in.

Ik ken dit probleem van meerdere kanten uit eigen praktijk. Door mijn werk voor PublicSpaces, de coalitie van Nederlandse publieke organisaties die werkt aan een internet op basis van publieke waarden, heb ik van dichtbij gezien hoe de leden, van omroepen tot culturele instellingen, expliciet op zoek zijn naar platformonafhankelijke infrastructuur, en hoe juist de laag ontbreekt waarmee hun eigen bronnen elkaar kunnen vinden en naar elkaar kunnen verwijzen. Met Offcourse, het open-source platform voor kennisdeling tussen praktijkmensen dat ik in 2013 oprichtte, heb ik er zeven jaar aan gebouwd; één probleem is nooit opgelost: mensen die elkaar hadden moeten vinden, vonden elkaar niet, omdat matching op titels en bekendheid liep. En met Rizom, het open-source project waarin ik nu zelfgehoste kennisbronnen op open protocollen bouw, verken ik hetzelfde probleem van de bouwkant: elke bron kan zelfstandig bestaan, maar er is geen afgesproken vorm waarin de ene de andere vindt. Drie routes, steeds dezelfde ontbrekende laag. Dit project bouwt die laag.

Waarom zijn bestaande protocollen en platforms onvoldoende?

Elk bestaand protocol lost een aangrenzend probleem op; geen ervan levert een afgesproken, afdwingbare vorm waarin onafhankelijk gehoste bronnen elkaar vinden en citeren.

ActivityPub regelt berichtenverkeer voor sociale objecten. Ontdekking loopt er via volgrelaties en instance-tijdlijnen, en er is geen afdwingbaar schema voor wat een bron als geheel bevat.

Het AT Protocol zelf levert de fundering: verplaatsbare identiteit via DID's, een repository per actor, en lexicons als afdwingbaar schema-mechanisme. Maar de bestaande lexicons beschrijven sociale objecten zoals posts, volgrelaties en likes. Daarom bouw ik hierop voort: het gat is geen ontbrekend protocol maar een ontbrekend schema, en ATProto heeft precies het mechanisme om dat schema te publiceren.

OAI-PMH, de standaard uit de bibliotheek- en repositorywereld, is metadata-oogst voor formele publicaties via centrale harvesters. Het veronderstelt institutionele infrastructuur, kent geen voorwaarden per record en geen verwijzing tussen peers.

RSS en sitemaps kondigen nieuwe items aan, maar zeggen niets over wat een bron bijhoudt en kennen geen verwijs- of zichtbaarheidssemantiek.

Schema.org en de linked-data-stapel leveren vocabulaire zonder identiteits- en transportlaag; in de praktijk dienen ze centrale crawlers. Solid biedt persoonlijke datapods met toegangscontrole, maar hoe pods elkaar vinden is er niet opgelost.

Samenwerkingsplatforms als Notion of ResearchGate bieden de verbinding wel, maar binnen het platform en als eigendom van het platform. Dat is de situatie die dit project wil doorbreken, geen alternatief ervoor.

Welke bredere meerwaarde heeft het lexicon voor het internet als geheel?

Ontdekking is een van de laatste kernfuncties van het internet die vrijwel volledig gecentraliseerd is gebleven. E-mail en het web zelf zijn gedecentraliseerd; wie wat vindt, bepalen een handvol zoekmachines en platforms. Dit lexicon maakt van vinden en verwijzen een protocolfunctie in plaats van een platformdienst.

Drie eigenschappen maken dat duurzaam. Het mechanisme heeft per constructie alleen waarde tussen onafhankelijke partijen, dus het kan niet worden dichtgetrokken, ook niet door mij. De specificatie staat los van de implementatie en blijft bruikbaar onafhankelijk van mijn voortbestaan; de referentiecode is AGPL en publiek. En het laat zien dat het AT Protocol algemene internetinfrastructuur kan dragen, voorbij sociale media, wat het hele open ecosysteem eromheen versterkt.

Daarnaast verlaagt het de drempel om kennis zelf te hosten. Zelf hosten betekent nu isolement; met deze laag betekent het volwaardig meedoen. Elke bron die daardoor buiten een platform blijft bestaan, maakt het internet als geheel een stukje gedecentraliseerder.

Als er nog iets ontbreekt, hoor ik het graag. Wat er al staat, is publiek te zien: github.com/rizom-ai/brains is de code voor zelfgehoste kennisbronnen, en yeehaa.io draait daarop als zo'n bron. Het lexicon waarmee zulke bronnen elkaar vinden, bestaat nog niet; dat is wat dit voorstel bouwt.

Met vriendelijke groet,

Jan Hein Hoogstad

---

## Aantekeningen bij het concept (niet meesturen)

- **Vraag 3** steunt op de structurele analyse plus drie eigen praktijkroutes: PublicSpaces (vraagzijde bij publieke organisaties, zonder titelclaim), Offcourse (zeven jaar, consistent met de v2-tekst) en Rizom (de bouwkant, als verkenning en niet als bedrijf). INC en de ISOC-cohort zijn niet toegezegd en worden dus niet genoemd; zodra een partij zich wél committeert, is dit de eerste plek om die te noemen.
- **Vraag 4 is de dragende.** Elke genoemde oplossing krijgt een concrete tekortkoming, geen abstracte differentiatie. OAI-PMH is bewust opgenomen: herkenbaar voor een Nederlandse beoordelaar (SURF/DANS-wereld).
- **Consistent gehouden met v2:** geen communityframing, geen node-claims, geen partners, geen gespreksverzoek, afsluiting op repo plus draaiende bron.
- **Geen CV meegestuurd, bewust.** Er is nooit een CV bij SIDN geweest (beide toetsen waren kale webformulieren), dus elke verwijzing draagt zijn eigen context als korte bijstelling in de zin: PublicSpaces (coalitie), Offcourse (platform, 2013), Rizom (open-source project). Het CV hoort pas bij stap 3 in FundPro.
- **rizom.ai bewust niet gelinkt.** De productsite haalt het bedrijfsframe terug, en de netwerkkaart (centraal geïndexeerde agents) zou de bestaat-al/bestaat-nog-niet-lijn van de afsluiting vertroebelen. Repo plus yeehaa.io zijn de twee bewijsstukken.
- **Afsluiting expliciet gesplitst in bestaat al / bestaat nog niet.** "yeehaa.io draait op deze basis" kon gelezen worden alsof het lexicon al bestaat, wat de financieringsvraag ondergraaft. Nu: substrate (code, yeehaa.io als bron) bestaat, het lexicon niet; dat is het voorstel.
- **Veld-3-vraag (interoperabiliteit) bewust niet herhaald** in dit antwoord; haar vragen tonen dat de beoordeling loopt, en de vraag staat al in de toets.