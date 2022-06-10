---
title: Lagerpostering
description: Dette emnet forklarer kategorien Lagerpostering på siden Lagerposteringsprofil.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: 464ffccd658003271b517038f430914fd5d8d50e
ms.sourcegitcommit: 6744cc2971047e3e568100eae338885104c38294
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/20/2022
ms.locfileid: "8783373"
---
# <a name="inventory-posting"></a>Lagerpostering

**Lager**-fanen på siden **Lagerposteringsprofiler** brukes til å styre hvordan lagertransaksjoner skal posteres i økonomimodulen. Lagertransaksjoner er transaksjoner som ikke er opprettet fra salgsordrer, bestillinger eller produksjonsordrer. De posterer automatisk de fysiske og finansielle oppdateringene til lageret samtidig. Ett unntak er overføringsordrer som skiller fysiske og finansielle oppdateringer når du sender og mottar lageret.

Tabellen nedenfor viser noen eksempler på lagertransaksjoner.

| Transaksjonstype | Mottak eller avgang | Fysisk postering, økonomisk postering eller begge deler | Beskrivelse |
|---|---|---|---|
| Bevegelse | Begge | Begge | <p>En bevegelsesjournal er en lagerjournal som du kan bruke til å legge til eller fjerne lager. Den fungerer som en beholdningsjusteringsjournal. Én hovedforskjell er imidlertid at hovedkontoen som motposterer oppføringen, er angitt.</p><p>Bevegelsesjournalen angir startsaldoer og engangsjusteringer som må utgiftsføres. Den brukes for eksempel når lager fjernes for en salgsprøve.</p><p>Når journalen posteres, skjer de fysiske og finansielle oppdateringene samtidig.</p><p>Positive antall på journallinjene representerer mottak, og negative antall representerer avganger.</p> |
| Lagerjustering | Begge | Begge | En lagerjusteringsjournal brukes til å legge til eller fjerne lager. Den lar deg ikke velge en motkonto. Bare kontoene som er angitt på siden **Lagerposteringsprofil** brukes til å oppdatere økonomimoduloppføringen. |
| Overføring (journal) | Begge | Begge | <p>En overføringsjournal brukes til å flytte lageret fra én lokasjon til en annen (ved hjelp av lagringsdimensjoner). Den oppdaterer produktinformasjonen på en lagertransaksjon med nye produkt- eller sporingsdimensjoner.</p><p>En overføringsjournal oppretter én linje for flyttingen av en vare. Denne linjen har "fra"- og "til"-felt for lagerdimensjonene. Hver linje i en overføringsjournal oppretter to lagertransaksjoner. Én transaksjon opprettes for "fra"-lagerdimensjonene. Den representerer avgangen, og har et negativt antall. Den andre transaksjonen opprettes for "til"-lagerdimensjonene. Den representerer mottaket og har et positivt antall.</p><p>Overføringsjournaler oppretter kanskje ikke et bilag hvis varebevegelsen av lageret regnes som en ikke-finansiell overføring. Lagerdimensjoner som er forskjellige for verdiene "fra" og "til", merkes ikke med alternativet **Økonomisk lager** på siden **Lagringsdimensjonsgruppe** eller **Sporingsdimensjonsgruppe**. Hvis for eksempel alternativet **Økonomisk lager** ikke er merket på **Lokasjon**-dimensjonen, og du flytter lageret fra ett sted til et annet sted i samme område og lager, opprettes det ingen bilag.</p><p>Overføringsjournaler er forskjellige fra overføringsordrer i og med at det ikke finnes dokumenter for flyttingen. Oppdateringen gjøres i én transaksjon ved å postere journalen. I kontrast til dette kan en overføringsordre generere plukk- og forsendelsesdokumenter, og det kreves to oppdateringer for å behandle transaksjonen.</p> |
| Sending av overføringsordre | Problem | Begge | <p>Når du oppretter en ny overføringsordre, har hver kombinasjon av en linje og en lagerdimensjon to lagertransaksjoner: én for overføringsordreforsendelsen og én for overføringsordremottaket. Når du sender overføringsordren, oppdateres to lagertransaksjoner, og ytterligere to lagertransaksjoner blir opprettet for varetransporten, totalt fire lagertransaksjoner.</p><ol><li>Den første lagertransaksjonen brukes til å fjerne varen fra kildelageret og lokasjonen. Avgangsstatusen for denne transaksjonen er **Solgt** for å angi at varen ikke lenger er tilgjengelig på lageret.</li><li>Den andre lagertransaksjonen brukes til å legge til varen i transittlageret som er valgt for lageret som varen overføres fra. Mottaksstatusen for denne transaksjonen er **Kjøpt**.</li><li>Den tredje lagertransaksjonen er for overføringen fra transittlageret til mållageret. Denne transaksjonens avgangsstatus er **Fysisk reservert**. Denne statusen sikrer at varen ikke kan forbrukes av en annen prosess mens den fremdeles er i transitt.</li><li>Den fjerde lagertransaksjonen er for mottak av varer i mållageret. Mottaksstatusen for denne transaksjonen er **Bestilt**.</li></ol> |
| Mottak av overføringsordre | Tilgang | Begge | Når en overføringsordre mottas i mållageret, oppdateres lagerstatusen for lagertransaksjonen som er i transittlageret (nummer 3 i det forrige eksemplet) til **Solgt**, og lagerstatusen for lagertransaksjonen for mållageret oppdateres til **Kjøpt**. |
| Stykklister | Begge | Begge | Du kan bruke en stykklistejournal til å ferdigmelde et produkt og forbruke råvarene som ble forbrukt under prosessen uten å bruke en produksjonsordre. En stykklistejournal inneholder vanligvis minst én positiv linje for ferdigvaren, og én eller flere negative linjer for råvarene som forbrukes. Linjen for ferdigvare er et mottak til lageret, mens de negative linjene er avganger fra lageret for råvarene. Når du oppretter en stykklistejournal, er den første linjen stykklistehodet, og etterfølgende linjer som blir lagt til, er stykklistelinjene. |
| Endring av lagereierskap | Begge | Begge | Journal for endring av lagereierskap brukes til å endre eierskapet til forsendelseslageret fra leverandøren til organisasjonen din. Endringsjournaler for lagereierskap ligner lageroverføringsjournaler ved at to lagertransaksjoner er relatert til hver kombinasjon av en linje og en lagerdimensjon. Én lagertransaksjon fjerner lageret fra leverandøren **Eierskap**-dimensjonen, og den andre legger til varen i den juridiske enheten i **Eierskap**-dimensjonen. |
| Vareankomst | Tilgang | Fysisk | En vareankomstjournal brukes til å oppdatere mottaksstatusen for lageret til **Registrert**. Den brukes vanligvis til bestillingsmottak av varer og salgsordrereturer. |
| Produksjonsinnlevering | Tilgang | Fysisk | En produksjonsinnleveringsjournal ligner en vareankomstjournal. Produksjonsinnlevering brukes til å motta ferdige varer fra en produksjonsordre i lageret. Når journalen blir postert, oppdateres statusen for lagertransaksjonen til **Registrert**. |
| Opptelling | Begge | Begge | En opptellingsjournal brukes til å registrere antall varer som ble talt opp for en bestemt kombinasjon av lagerdimensjoner. Det opprettes lagertransaksjoner når linjen i journalen har en opptellingsdifferanse. En linje som har et høyere opptellingsantall, fører til et mottak i lageret. En linje som har et lavere opptellingsantall, fører til en avgang fra lageret. Linjer der det opplistede antallet samsvarer med det forventede antallet, har ingen lagertransaksjoner. |
| Brikkeopptelling | Gjelder ikke her | Gjelder ikke her | En brikkeopptellingsjournal brukes til å spore lagerbrikker som er tilordnet og brukt i en fullstendig lageropptelling. Du kan bruke journalen til å tilordne et brikkenummer til en bestemt kombinasjon av en vare og en lagerdimensjon, og til å spore statusen til brikken under et fullstendig lager. Brikketellingsjournaler oppretter ikke lagertransaksjoner. |
| Kvalitetsordrer | Problem | Fysisk | <p>En kvalitetsordre brukes til å registrere testresultater for et angitt parti på lager. Hver kvalitetsordre er knyttet til en eksisterende lagertransaksjon eller en del av en lagertransaksjon.</p><p>En kvalitetsordre genererer en ny lagertransaksjon i to situasjoner:</p><ul><li>Kvalitetsordren er merket som **Destruktiv test** i kategorien **Generelt**.</li><li>Kvalitetsordren merkes som **Sett i karantene ved valideringsfeil** i kategorien **Generelt**, og testen mislykkes i valideringen. I dette tilfellet opprettes to lagertransaksjoner. Én lagertransaksjon fjerner varen fra den opprinnelige lagerdimensjonskombinasjonen og -lokasjonen, og den andre legger til varen i karantenelageret.</li></ul> |
| Karanteneordrer | Begge | Begge | <p>Lagertransaksjoner for en karanteneordre er som en overføringsordre. Det brukes et karantenelager til å spore lageret. Det finnes to mottakstransaksjoner og to avgangstransaksjoner.</p><p>Når du først oppretter ordren, opprettes det to transaksjoner. Mottakstransaksjonen har statusen **Bestilt** for karantenelageret som er knyttet til lageret der varen finnes. Avgangstransaksjonen har statusen **I ordre** for lageret der varen er lagret.</p><p>Når du starter karanteneordren, opprettes det to ekstra transaksjoner, og de eksisterende transaksjonene oppdateres. Statusen for mottakstransaksjonen for karantenelageret oppdateres til **Mottatt**, og statusen for avgangstransaksjonen for lageret oppdateres til **Fratrukket**.</p><p>De to nye transaksjonene brukes til å angi eventuell flytting tilbake til lageret. Mottakstransaksjonen har statusen **Bestilt** for lageret, og avgangstransaksjonen har statusen **Fysisk reservert** for karantenelageret.</p><p>Når du rapporterer en karanteneordre som ferdig, representerer denne operasjonen den fysiske oppdateringen av karanteneordren. Tilgangsstatusen i lageret oppdateres til **Mottatt**.</p><p>Når du avslutter karanteneordren, representerer denne operasjonen den økonomiske oppdateringen av karanteneordren. Statusen for avgangstransaksjonene oppdateres til **Solgt**, og statusen for mottakstransaksjonene oppdateres til **Kjøpt**.</p><p>Du kan også kassere karanteneordren. Denne operasjonen fjerner varen fra lageret. Når du kasserer en karanteneordre, blir det bare tre transaksjoner igjen. Mottakstransaksjonen for lageret fjernes, og statusen for den gjenværende mottakstransaksjonen oppdateres til **Kjøpt**. Statusen for de to avgangstransaksjonene oppdateres til **Solgt**. Denne operasjonen er en fysisk og økonomisk oppdatering for ordren.</p> |

## <a name="fixed-receipt-price-posting"></a>Postering for fast mottakspris

Med fast mottakspris kan du bruke standard kostpris for et produkt. Det er et alternativ til å velge alternativet **Standard** på siden **Varemodellgruppe** for en vare. Den viktigste forskjellen når du bruker en fast mottakspris, er at kostprisen som er konfigurert for øyeblikket, vil bli brukt for varen når mottak til lager posteres. Det er ingen kostnadsrevalueringsprosess for en fast mottakspris. Når en økonomisk oppdatering posteres, brukes den gjeldende kostprisen ved postering. Hvis kostprisen som brukes ved mottak, og fakturaen er forskjellig, blir avviket postert til de faste resultatkontoene for mottakspris.

Hvis du vil bruke en fast mottakspris for et produkt, må du fullføre følgende konfigurasjon:

- Merk av for **Poster aktuell beholdning** på siden **Varemodellgruppe** for varen som er valgt på lagertransaksjonslinjen.
- Merk av for **Fast mottakspris** på siden **Varemodellgruppe**.
- Angi hovedkontoene for følgende posteringstyper på siden **Lagerposteringsprofil**:

    - Fortjeneste på fast mottakspris
    - Tap på fast mottakspris

Hvis du vil ha mer informasjon, se [Fast mottakspris](/supply-chain/cost-management/fixed-receipt-price.md).

## <a name="catch-weight-posting"></a>Faktisk vekt-postering

Faktisk vekt-produkter brukes ofte i industrier som næringsmiddelindustrien, der produkter kan variere litt i vekt, størrelse eller begge deler. Faktisk vekt-produkter bruker to måleenheter: en lagerenhet og en faktisk vekt-enhet. Vekten på lagerbeholdningen når den kommer inn på et lager, kan være forskjellig fra vekten når lageret utstedes fra lageret. Produktbehandling for faktisk vekt justerer lageret.

Hvis det er et avvik i den faktiske vekten, posteres forskjellene til kontoene som er angitt i feltene **Tap for faktisk vekt** og **Overskuddskonto for faktisk vekt** på siden **Lagerposteringsprofil**. Vanligvis angis samme hovedkonto i begge felt.

Følgende tabell viser eksempler på standard posteringstyper og inkluderer eksempelhovedkontoer og beskrivelser.

- Kolonnen «Debet/kredit?» angir om transaksjonen vanligvis posterer et debet eller kredit. I noen tilfeller kan transaksjonen postere enten et debet- eller en kreditbeløp.
- "Avregningskonto"-kolonnen angir at posteringstypen er en avregningskonto. Beløpet er med andre ord postert i denne kontoen, blir automatisk tilbakeført når en senere transaksjon posteres.
- Kolonnen "P/F" angir posteringstypen. "P" representerer fysisk postering, og "F" representerer økonomisk postering.
- "Følg"-kolonnen angir om hovedkontoen for en posteringstype vanligvis er den samme som hovedkontoen for en annen posteringstype. Mer bestemt angir det posteringstypen som vanligvis brukes for posteringen.

> [!NOTE]
> Hovedkontoene og hovedkontonavnene i tabellen er forslag. Vi anbefaler at du samarbeider med regnskapsføreren for å fastsette den beste konfigurasjonen for forretningsbehovet ditt.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | F/Ø | Følg | Beskrivelse |
|---|---|---|---|---|---|---|---|---|
| Tapskonto for faktisk vekt | 510520 | Lagerjustering | Utgift | | Nei | Begge | Overskuddskonto for faktisk vekt | Denne kontoen brukes når du posterer en lagertransaksjon der faktisk vekt-mengden er lavere. |
| Overskuddskonto for faktisk vekt | 510520 | Lagerjustering | Utgift | | Nei | Begge | Tapskonto for faktisk vekt | Denne kontoen brukes når du posterer en lagertransaksjon der faktisk vekt-mengden er høyere. |

Hvis du vil ha mer informasjon om faktisk vekt-produkter, kan du se [Om faktisk vekt-elementer](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.md) og videoen [Produktbehandling for faktisk vekt med lagerstyring](/supply-chain/warehousing/catch-weight-processing.md).

## <a name="inventory-to-fixed-asset-transfer-posting"></a>Lager til overføringspostering for anleggsmiddel

Beholdning til anleggsmiddeljournal (**Anleggsmiddel** \> **Journaler** \> **Beholdning til anleggsmiddeljournal**) brukes til å flytte varer ut av lageret og konvertere dem til anleggsmidler. Hvis du vil ha mer informasjon, se [Integrering av anleggsmidler](/fixed-assets/fixed-asset-integration.md).

Følgende tabell viser eksempler på standard posteringstyper og inkluderer eksempelhovedkontoer og beskrivelser.

- Kolonnen «Debet/kredit?» angir om transaksjonen vanligvis posterer et debet eller kredit. I noen tilfeller kan transaksjonen postere enten et debet- eller en kreditbeløp.
- "Avregningskonto"-kolonnen angir at posteringstypen er en avregningskonto. Beløpet er med andre ord postert i denne kontoen, blir automatisk tilbakeført når en senere transaksjon posteres.
- Kolonnen "P/F" angir posteringstypen. "P" representerer fysisk postering, og "F" representerer økonomisk postering.
- "Følg"-kolonnen angir om hovedkontoen for en posteringstype vanligvis er den samme som hovedkontoen for en annen posteringstype. Mer bestemt angir det posteringstypen som vanligvis brukes for posteringen.

> [!NOTE]
> Hovedkontoene og hovedkontonavnene i tabellen er forslag. Vi anbefaler at du samarbeider med regnskapsføreren for å fastsette den beste konfigurasjonen for forretningsbehovet ditt.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | F/Ø | Følg | Beskrivelse |
|---|---|---|---|---|---|---|---|---|
| Anleggsmiddelfrigivelse | 180100 | Materielle anleggsmidler | Objekt | Kreditt | Nei | Begge | Gjelder ikke her | Denne kontoen brukes når du posterer et lager til anleggsmiddeljournal for å fjerne en vare fra lageret og konvertere det til et anleggsmiddel. |

## <a name="moving-average-posting"></a>Postering for glidende gjennomsnitt

Glidende gjennomsnitt er en permanent etterkalkuleringsmetode som er basert på gjennomsnittsprinsippet. Kostnadene på lageravganger endres ikke når innkjøpskostnaden gjør det. Forskjellen kapitaliseres og baseres på en proporsjonal beregning. Beløpet som gjenstår utgiftsføres.

Følgende tabell viser eksempler på standard posteringstyper med eksempelhovedkontoer og -beskrivelser.

- Kolonnen «Debet/kredit?» angir om transaksjonen vanligvis posterer et debet eller kredit. I noen tilfeller kan transaksjonen postere enten et debet- eller en kreditbeløp.
- "Avregningskonto"-kolonnen angir at posteringstypen er en avregningskonto. Beløpet er med andre ord postert i denne kontoen, blir automatisk tilbakeført når en senere transaksjon posteres.
- Kolonnen "P/F" angir posteringstypen. "P" representerer fysisk postering, og "F" representerer økonomisk postering.
- "Følg"-kolonnen angir om hovedkontoen for en posteringstype vanligvis er den samme som hovedkontoen for en annen posteringstype. Mer bestemt angir det posteringstypen som vanligvis brukes for posteringen.

> [!NOTE]
> Hovedkontoene og hovedkontonavnene i tabellen er forslag. Vi anbefaler at du samarbeider med regnskapsføreren for å fastsette den beste konfigurasjonen for forretningsbehovet ditt.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | F/Ø | Følg | Beskrivelse |
|---|---|---|---|---|---|---|---|---|
| Prisdifferanse for glidende gjennomsnitt | 510600 | Prisdifferanse for glidende gjennomsnitt | Utgift | Begge | Nei | Begge | Gjelder ikke her | Denne kontoen brukes når det er en forskjell i kostnaden mellom mottaket og fakturaen. |
| Revaluering for glidende gjennomsnitt | 510610 | Revaluering for glidende gjennomsnitt | Utgift | Begge | Nei | Begge | Gjelder ikke her | Denne kontoen brukes når du justerer kostnaden for glidende gjennomsnitt til et produkt |

## <a name="sample-posting-profile-configuration"></a>Eksempel på konfigurasjon av posteringsprofil

Følgende tabell viser eksempler på standard posteringstyper med eksempelhovedkontoer og -beskrivelser.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | F/Ø | Følg | Beskrivelse |
|---|---|---|---|---|---|---|---|---|
| Beholdningsutstedelse | 140100 | Materiallager | Objekt | Kreditt | Nei | Begge | Beholdningsmottak | Denne kontoen brukes når en lagertransaksjon som er postert, er en avgang (negativt antall) og ikke er knyttet til salg, innkjøp eller produksjon. Motkontoen til denne kontoen er lagerutgift, tapskonto. Denne kontoen representerer vanligvis lageret i balansen. |
| Lagerutgift, tap | 510100 | Resultat for lager | Utgift | Debet | Nei | Begge | Lagerutgift, fortjeneste | Denne kontoen brukes når en lagertransaksjon som er postert, er en avgang (negativt antall) og ikke er knyttet til salg, innkjøp eller produksjon. Motkontoen til denne kontoen er lageravgangskontoen. |
| Beholdningsmottak | 140100 | Materiallager | Objekt | Debet | Nei | Begge | Beholdningsutstedelse | Denne kontoen brukes når en lagertransaksjon som er postert, er et mottak (positivt antall) og ikke er knyttet til salg, innkjøp eller produksjon. Motkontoen til denne kontoen er lagerutgift, overskuddskonto. Denne kontoen representerer vanligvis lageret i balansen. |
| Lagerutgift, fortjeneste | 510100 | Resultat for lager | Utgift | Kreditt | Nei | Begge | Lagerutgift, tap | Denne kontoen brukes når en lagertransaksjon som er postert, er et mottak (positivt antall) og ikke er knyttet til salg, innkjøp eller produksjon. Motkontoen til denne kontoen er lagermottakskontoen. |
| Overføring, skyldig | 231500 | Enhetsintern utgående | Gjeld | Debet | Nei | Begge | | Denne kontoen brukes når lager overføres mellom lagerdimensjoner, for eksempel områder, og varekostnaden er forskjellig ved de forskjellige områdene. |
| Overføring, tilgode | 131500 | Enhetsintern innkommende | Objekt | Kreditt | Nei | Begge | | Denne kontoen brukes når lager overføres mellom lagerdimensjoner, for eksempel områder, og varekostnaden er forskjellig ved de forskjellige områdene. |
