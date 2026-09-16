---
visibility: restricted
---
# Videopitch SIDN fonds Pioniers — script (concept v3)

Max 3 minuten. Gesproken, niet voorgelezen. Webcam of telefoon, landschap. Circa 305 woorden. Korte zinnen; elke regel is één gedachte. Geen slides. Schermdeling: yeehaa.io bij blok 1, één record in JSON bij blok 3, verder niets.

Frame: de domeinnaam als identiteit (SIDN's terrein), het probleem als internetprobleem (de hyperlink-belofte, voor zelfgehoste kennis weer gecentraliseerd), en Jets twee punten uit de uitnodiging van 2026-09-10 in haar volgorde: vinden zonder tussenpartij (blok 3), breedte van adoptie (blok 4).

---

## 1. Wie (0:00 tot 0:15)

Ik ben Jan Hein Hoogstad. Ik bouw al ruim tien jaar open-source infrastructuur voor kennisdeling.

Een voorbeeld hiervan is yeehaa.io. Mijn eigen kennisbron. Eigen server, eigen domein, platte tekst. Ik ben niet de enige. Onderzoekers, lectoraten, instituten met een archief hosten hun kennis ook zelf.

## 2. Het probleem (0:15 tot 0:50)

Het web had één belofte: onafhankelijke sites die elkaar vinden en naar elkaar verwijzen, zonder iemand ertussen. De hyperlink.

Voor kennis is die belofte weg. Wie zelf host, is onzichtbaar. Vindbaar worden betekent: terug naar een platform. Een verwijzing is een kale URL, en die breekt zodra je iets verplaatst. En iets delen met een kleine kring, per stuk? Bestaat niet.

Vinden, verwijzen, delen. Drie basisfuncties van het internet. Voor zelfgehoste kennis zijn ze alle drie weer gecentraliseerd.

## 3. Wat ik bouw (0:50 tot 1:40)

Ik bouw de laag die dat terugdraait. Een open lexicon op het AT Protocol.

Het begint bij het domein. Een domeinnaam is al een identiteit. Hier ook, van een kennisbron. Geen register, geen aanmelding.

Onder dat domein regelt een bron drie dingen. Vinden: ze zegt waar ze over gaat. Verwijzen: elk stuk krijgt een vaste sleutel. Delen: bij elk stuk staat wie het mag zien. Iedereen, alleen erkende peers, of niemand.

Een voorbeeld. Een instituut citeert een alinea van mijn site. Later verhuis ik die alinea. Een gewone link is dan dood. Deze verwijzing werkt nog, want hij wijst naar de alinea zelf, niet naar het adres.

Tweede voorbeeld. Een stuk dat alleen dat instituut mag zien, markeer ik: alleen peers. Het instituut is mijn peer. Zij halen het rechtstreeks op bij mijn server. Vraagt iemand anders het op, dan krijgt die niets. Geen platform ertussen. Mijn server beslist.

## 4. Wat er al is, wie meedoet (1:40 tot 2:15)

Dit begint niet bij nul. Mijn lexicons staan al op het protocol. Mijn eigen bronnen draaien erop, en die van mensen uit mijn netwerk. Het mechanisme is er. Het schema voor vinden, verwijzen en delen niet. Dat is dit project. Zes maanden, één persoon.

De eerste gebruikers hosten hun kennis al zelf. Zij hoeven niets te vervangen. Meedoen is een dag werk: vier kleine recordtypen. Het werkt al bij twee bronnen, dus dat is de demonstratie. Daarna de bouwers van hun tools. Eén plugin, en al hun gebruikers doen mee.

## 5. Slot (2:15 tot 2:35)

Na zes maanden is alles openbaar. De specificatie, apart gepubliceerd, zodat je het kunt bouwen zonder mijn code. Mijn code zelf, als referentie. En een testset om je eigen bouw te controleren.

En één ding dat een platform niet kan nabouwen: dit werkt alleen tussen onafhankelijke partijen. Binnen één aanbieder is het niets waard. Daarom kan niemand het dichttrekken. Ik ook niet.

---

## Aantekeningen (niet opnemen)

- 2026-09-16: gemeten op 10 seconden te lang; 25 woorden geschrapt verspreid over blok 3 tot 5, geen gedachte weg. Opnieuw meten.
- Blok 3: "drie dingen" zijn de drie functies uit blok 2 (vinden, verwijzen, delen), niet de vier recordtypen. Zo blijft de telling kloppen; de recordtypen komen pas in blok 4 als "vier kleine recordtypen".
- Blok 3: de twee voorbeelden zijn bewust "stel", geen anekdote. Niets verzinnen. Eerste: stabiel verwijzen (verhuizen, link houdt). Tweede: delen op voorwaarden (peers-record, instituut erkend, ophalen bij mijn server, een niet-erkende bron krijgt niets). "Mijn server beslist" is de kern: geen tussenpartij.
- Blok 4: "die van mensen uit mijn netwerk" is jouw toevoeging van 2026-09-16. Geen aantallen noemen; als Jet doorvraagt, zijn dat bronnen op dezelfde software, niet onafhankelijke implementaties van het lexicon.
- Blok 5: drie opbrengsten, elk met zijn functie: specificatie (bouwen zonder mijn code), referentiecode, conformiteitstestset (eigen implementatie controleren). Licenties niet hardop.
- Geen partners, geen titels, geen NLnet, geen licentienamen hardop, Rizom niet genoemd.
- Elke claim staat al in `sidn-fonds-pioniers-2026-fundpro-aanvraag-concept`; de video voegt geen feiten toe.
- Nog te lang? Volgende kandidaat: "Binnen één aanbieder is het niets waard." in blok 5 (6 woorden). Niet snijden in blok 2.

## Geschiedenis

- v1 (2026-09-16 ochtend): opende op een gebroken link, las de aanvraag voor, stelde de spreker pas op 2:45 voor, noemde het internet niet en beantwoordde Jets adoptievraag niet. Vervangen.
- v2 (2026-09-16): huidig frame, 390 woorden. Te wollig voor spreektaal. Ingekort tot v3 in eigen stem.
