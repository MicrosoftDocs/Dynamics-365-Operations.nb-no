---
title: Produksjonsordrepostering
description: Dette emnet inneholder informasjon om ulike typer posteringer i produksjonsordrer.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup, ProdGroup, WrkCtrTable, WrkCtrResourceGroup, ProjCategory, CostSheetDesigner
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: cd1b6c49e59f9480fd831ad5ff143033ca09792c
ms.sourcegitcommit: 5b55f2913e736d12e40c227bf3ce3a9abec815bd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/24/2022
ms.locfileid: "8803021"
---
# <a name="production-postings"></a>Produksjonsposteringer

Dette emnet inneholder informasjon om ulike typer posteringer i produksjonsordreprosessen.


## <a name="material-consumption"></a>Materialforbruk

Materialer registreres som forbruk under produksjon når produksjonsplukklistejournalen posteres. Dette oppretter transaksjoner som trekkes fra i lagerbeholdningen. I **Produksjonsparametere** kan du angi om verdien av råvarer som pågår (kalt VIA) skal posteres i finans.

Verdien av råvarer som pågår (VIA) posteres til kontoene **Estimert kost for materialer brukt** og **Estimert kost for materialer brukt, VIA**. Plukklisteprosessen for produksjonsordren er en fysisk oppdatering av lagertransaksjonene som er knyttet til produksjonsordren. Når en produksjonsordre registreres som avsluttet, tilbakeføres de fysiske transaksjonene, og de relaterte lagertransaksjonene oppdateres finansielt. Når sluttjournalen posteres, brukes posteringstypene **Kostnad for materialer brukt** og **Kostnad for materialer brukt, VIA**.

**Produksjon**-fanen på siden **Lagerposteringsprofiler** styrer hvordan produksjonsordrer posteres til økonomimodulen. Dette brukes når feltet **Finanspostering** er satt til enten **Vare og ressurs** eller **Vare og kategori** på siden **Parametere for produksjonskontroll**. 

For at en plukklistejournal skal kunne posteres i økonomimodulen for en produksjonsordre, må følgende betingelser oppfylles:

-   Det må være merket av for **Poster plukkliste i finans** på siden **Parametere for produksjonskontroll**. Denne innstillingen kan overstyres for et bestemt område på siden **Parametere for produksjonskontroll etter område**.
-   Det må være merket av for **Poster aktuell beholdning** på siden **Varemodellgrupper** for varen som er valgt på bestillingslinjen.
-   Hovedkontoene må være angitt på siden **Lagerposteringsprofil** for følgende posteringstyper:
    -   **Estimert kost for materialer brukt**
    -   **Estimert kost for materialer brukt, VIA**

## <a name="time-consumption"></a>Tidsforbruk

Tiden som arbeidere bruker på produksjonsjobber registreres i **Rutekortjournal** eller **Jobbkortjournal**. Når disse journalene posteres, behandles finansposteringen til en egen konto for ressurser som er i arbeid (VIA). Denne posteringen representerer verdien av tiden som er brukt på produksjonsordren. Etter at produksjonsordren er registrert som avsluttet, utlignes via-kontoene.

Det finnes tre mulige måter å postere tidsforbruk på, avhengig av alternativet som er valgt i feltet **Finanspostering** på siden **Parametere for produksjonskontroll**.

## <a name="reporting-finished-goods-and-error-quantities"></a>Rapportere ferdige varer og antall feil

Når en produksjonsordre **Ferdigmeldes**, oppdateres ferdigvarene som er fullført, i lageret via **Ferdigmeld**-journalen. Hvis du bruker VIA-regnskap, posteres en finansjournal for å redusere VIA-kontoene og øke beholdningen av ferdigvarene. Journalen bruker standardkostnaden som er definert for produktet. Hvis alternativet **Bruk estimert kostpris** er valgt på siden **Parametere for produksjonskontroll**, brukes den estimerte kostnaden fra produksjonsordren.

Verdien av råvarer som pågår (VIA), posteres til kontoene **Estimert produksjonskostnad** og **Estimert produksjonskostnad, VIA**. **Ferdigmeld**-prosessen for produksjonsordren er en fysisk oppdatering av lagertransaksjonene som er knyttet til produksjonsordren. Når en produksjonsordre avsluttes, tilbakeføres de fysiske transaksjonene, og de relaterte lagertransaksjonene oppdateres finansielt. Når sluttjournalen posteres, brukes posteringstypene **Produksjonskostnad** og **Produksjonskostnad, VIA**.

**Produksjon**-fanen på siden **Lagerposteringsprofiler** brukes til å styre hvordan produksjonsordrer skal posteres i økonomimodulen. Dette brukes når feltet **Finanspostering** er satt til enten **Vare og ressurs** eller **Vare og kategori** på siden **Parametere for produksjonskontroll**. Hurtigkategorien **Finans - varer** på siden **Produksjonsgrupper** kan også brukes til å styre postering for produksjonsordrer når feltet er satt til **Produksjonsgrupper**.

For at en **Ferdigmeld**-journal skal kunne posteres i økonomimodulen for en produksjonsordre, må følgende betingelser oppfylles:
-   Det må være merket av for **Poster ferdigmelding i finans** på siden **Parametere for produksjonskontroll**. Denne innstillingen kan overstyres for et bestemt område på siden **Parametere for produksjonskontroll etter område**.
-   Det må være merket av for **Poster aktuell beholdning** på siden **Varemodellgrupper** for varen som er valgt på bestillingslinjen.
-   Hovedkontoene må være angitt på siden **Lagerposteringsprofil** for følgende posteringstyper:
    -   **Estimert produksjonskostnad**
    -   **Estimert produksjonskostnad, VIA**

## <a name="ending-the-production-order"></a>Avslutte produksjonsordren

Før avslutning av en produksjonsordre beregnes faktiske kostnader for antallet som ble produsert. Alle estimerte kostnader i forbindelse med materialer, arbeid og administrasjonskostnader tilbakeføres og erstattes med faktiske kostnader. Hele kostnaden på ferdigvaren debiteres fra **Produksjonskostnad**-kontoen og krediteres til **Produksjonskostnad, VIA**. Materialene som ble forbrukt i løpet av produksjonsordren, krediteres til **Kostnad for materialer brukt** og debiteres til kontoen **Kostnad for materialer brukt, VIA**.

Hvis du merker av for **Avslutt jobb** når du kjører kostnadsberegningen, endres status for produksjonsordren til **Avsluttet**. Denne statusen hindrer at det posteres tilleggskostnader til en fullført produksjonsordre ved en feiltakelse. Du kan angi at verdien for antall feil som ferdigmeldes, skal tilordnes til de gode antallene som er rapportert som ferdige. Du kan også angi at verdien for antall feil skal posteres til en dedikert svinnkonto. 

Følg denne fremgangsmåten for å angi en spesifikk svinnkonto:
1.  Gå til **Produksjonskontroll** > **Oppsett** > **Parametere for produksjonskontroll**.
2.  Velg fanen **Standardoppdatering**.
3.  I feltet **Svinnmetode** velger du **Svinnkonto**.
4.  I **Svinnkonto**-feltet velger du hovedkontoen der svinn for feilantall skal posteres når produksjonsordren er avsluttet. Velg for eksempel en utgiftskonto, for eksempel 510380: Produksjonssvinn.

For at sluttjournalen skal posteres til økonomimodulen for en produksjonsordre, må følgende betingelser oppfylles:
-   Hovedkontoene må være angitt på siden **Lagerposteringsprofil** eller **Produksjonsgrupper** for følgende posteringstyper:
    -   **Kostnad for materialer brukt**
    -   **Kostnad for materialer brukt, VIA**
    -   **Produksjonskostnad**
    -   **Produksjonskostnad, VIA**
-   Hovedkontoene må angis på siden **Kostnadskategorier**, **Ressurser** eller **Ressursgrupper** for følgende typer:
    -   **Produksjonskostnad absorbert**
    -   **Kostnad for produksjon brukt, VIA**

## <a name="indirect-costs-for-production-orders"></a>Indirekte kostnader for produksjonsordrer

Når du behandler transaksjoner for en produksjonsordre, kan du konfigurere indirekte kostnader for å registrere indirekte kostnader eller tilleggsgebyrer i økonomimodulen. Fysiske transaksjoner for indirekte kostnader gjenkjennes på lager når du posterer en plukklistejournal eller ferdigmeldingsjournal. Økonomiske transaksjoner for indirekte kostnader gjenkjennes på lager når du posterer sluttjournalen.

Du kan gjenkjenne indirekte kostnader på tidsforbruket ditt relatert til **Rutekort**-journaler eller **jobbkort**-journaler. Disse transaksjonene tilbakeføres og posteres til finanskontoene når du avslutter produksjonsordren. For mer informasjon, se [Kostark](/supply-chain/cost-management/costing-sheets.md).

## <a name="controlling-the-level-of-ledger-posting"></a>Kontrollere nivået for finanspostering

På siden **Parametere for produksjonskontroll** kan du bruke feltet **Finanspostering** for å angi nivået for finanspostering for produksjonsprosesser. 

Følgende felt er tilgjengelige:

### <a name="item-and-resource"></a>Vare og ressurs

Når du velger alternativet **Vare og ressurs** i feltet **Finanspostering**, kommer posteringskontoene fra ressursen eller ressursgruppen som er i drift i ruten. Kontoer for den bestemte ressursen blir det første posteringsalternativet. Hvis kontoen som er angitt i ressursgruppen, ikke er angitt, vil kontoene som er angitt i ressursgruppen, bli brukt. Hver operasjonslinje i en rute kan ha én ressurs angitt som **Kostnadsressurs**. Denne ressursen brukes til å fastslå kontoen som skal brukes. Dette alternativet brukes vanligvis når en organisasjon tilordner driftskostnadene til ressursene. Kostnadene er ofte høyere for ressursene, og brukes til å treffe valg om produksjon eller kjøp. Dette er den mest detaljerte posteringskonfigurasjonen, og gir den mest detaljerte kontrollen over posteringene og svært detaljert analyse av produksjonsprosessen.

### <a name="item-and-category"></a>Vare og kategori

Når du velger alternativet **Vare og kategori** i feltet **Finanspostering**, vil posteringskontoene komme fra siden **Kostnadskategori** som er knyttet til hver linje i ruten. Hver operasjonslinje i ruten kan ha tre kostnadskategorier: **Oppstillingstid**, **Kjøretid** og **Antall**. Dette alternativet brukes vanligvis når organisasjonens hovedfokus er på prosesseffektivitet og aktivitetsvarighet. Dette alternativet er en mer summert metode for postering, og gir likevel en metode for å gruppere kostnader i kategorier.

### <a name="production-group"></a>Produksjonsgruppe

Når du velger alternativet **Produksjonsgrupper** i **Finanspostering**-feltet, kommer posteringskontoene fra **Produksjonsgrupper**-siden. **Produksjonsgrupper** brukes vanligvis når mer enn én produksjonslinje kjører like produkter eller har lignende utstyr. Du kan bruke dette alternativet til å sammenligne kostnadene mellom to forskjellige produksjonsgrupper.  
  
> [!NOTE]
> Hvis standardmetoden for beregning av kostnaden på ferdigvaren brukes, vil de siste transaksjonene reflektere dette. Hvis faktiske kostnader og kostnadene som beregnes ved hjelp av standardmetoden er forskjellige, posteres differansene til kontoen som viser resultat.

### <a name="route-groups-and-ledger-posting"></a>Rutegrupper og finanspostering

Det er angitt en **Rutegruppe** for hver operasjonslinje i en rute. Feltene **Oppstillingstid**, **Kjøretid** og **Antall** i **Rutegruppe** i gruppen **Estimering og etterkalkulering**-gruppen brukes til å styre om tiden skal brukes til etterkalkulering ved postering av et **Jobbkort** eller en **Rutekortjournal** på produksjonsordren. Hvis alternativene deaktiveres, blir det ikke opprettet et bilag i økonomimodulen for tidsforbruket.

For at **Rutekort** eller **Jobbkortjournal** skal kunne posteres i økonomimodulen for en produksjonsordre, må følgende betingelser oppfylles:

-   **Oppstillingstid**, **Kjøretid** eller **Antall**-feltet må være valgt i **Estimering og etterkalkulering**-gruppen på siden **Rutegruppe**.
-   Hovedkontoene må være angitt på siden **Kostnadskategori**, **Rute**, **Rutegruppe** eller **Produksjonsgrupper** for følgende posteringstyper:
    -   Estimert produksjonskostnad absorbert
    -   Estimert kost for produksjon brukt, VIA

Diagrammet nedenfor viser rutegruppens relasjon til beregningen av total kostnad for hver operasjon (rutelinje) i en angitt rute. Hver rutelinje har én rutegruppe. Rutegruppen styrer parametere for oppstillingstid, kjøretid og antall. Kategorien **Kostnadskategori** har tre alternativer for **Oppsett**, **Kjøring** og **Antall** som er aktivert basert på rutegruppeinnstillingen. Hurtigkategorien **Tidsmåling** har tre felt som er basert på rutegruppen.

Formelen som brukes, er basert på om alternativet er aktivert i rutegruppen. Kostnaden fra den valgte kostnadskategorien multipliseres med antallet som ble angitt i tidsberegningene for å beregne totalkostnaden.

:::image type="complex" source="media/RouteGroupRelationship.png" alt-text="Forholdet mellom rutegrupper og den totale beregnede kostnaden.":::
Forholdet mellom rutegrupper og den totale beregnede kostnaden. Hver rutelinje har én rutegruppe. Rutegruppen styrer parametere for oppstillingstid, kjøretid og antall. Kategorien Kostnadskategori har tre alternativer for Oppsett, Kjøring og Antall som er aktivert basert på rutegruppeinnstillingen. Hurtigkategorien Tidsmåling har tre felt som er aktivert og kostnadsbasert på rutegruppen. Formelen som brukes, er basert på om alternativet er aktivert i rutegruppen. Kostnaden fra den valgte kostnadskategorien multipliseres med antallet som ble angitt i tidsberegningene for å beregne totalkostnaden.
:::image-end:::

## <a name="sample-posting-profile-configuration"></a>Eksempel på konfigurasjon av posteringsprofil

Følgende tabell viser eksempler på standard posteringstyper med eksempelhovedkontoer og -beskrivelser. 

 - Kolonnen **Debet/kredit** angir om transaksjonen vanligvis debiterer eller krediterer, eller i noen tilfeller kan postere begge. 
 - **Avregningskonto**-kolonnen angir om posteringstypen er en avregningskonto. Beløpet som er postert på denne kontoen, tilbakeføres automatisk når en senere transaksjon posteres. 
 - **F/Ø**-kolonnen inneholder **F** for fysisk postering og **Ø** for økonomisk postering. 
 - **Følg**-kolonnen angir om hovedkontoen for en bestemt posteringstype vanligvis er den samme som en annen posteringstype. Verdien i kolonnen angir posteringstypen som vanligvis følges.

> [!NOTE]
> De foreslåtte hovedkontoene og hovedkontonavnene er bare forslag. Vi anbefaler at du samarbeider med regnskapsføreren for å fastsette den beste konfigurasjonen for forretningsbehovet ditt.


| Posteringstype  | Eksempel på hovedkonto | Eksempel på hovedkontonavn| Kontotype | Debet/kredit? | Avregningskonto | Fysisk eller økonomisk | Følg | Beskrivelse |
|---------------|----------------------|--------------------------|--------------|----------------|------------------|-----------------------|--------|------------|
| Estimert kost for materialer brukt      | 140100               | Materiallager        | Objekt        | Kreditt         | Y                | Ø                     | Kostnad for materialer brukt                | Denne kontoen brukes når du posterer en plukklistejournal for en produksjonsordre. Motkontoen for denne kontoen er Estimert kost for materialer brukt, VIA. Beløpet i denne kontoen tilbakeføres automatisk når produksjonsordren avsluttes. Denne kontoen representerer lagerkontoen i balansen.       |
| Estimert kost for materialer brukt, VIA | 150150               | Produksjons-VIA – Materialer | Objekt        | Debet          | Y                | Ø                     | Estimert produksjonskostnad, VIA          | Denne kontoen brukes når du posterer en plukklistejournal for en produksjonsordre. Motkontoen for denne kontoen er Estimert kost for materialer brukt. Beløpet i denne kontoen tilbakeføres automatisk når en produksjonsordre avsluttes. Denne kontoen representerer VIA i balansen.                  |
| Estimert produksjonskostnad               | 140200               | Ferdigvarelager   | Objekt        | Debet          | Y                | Ø                     | Produksjonskostnad                         | Denne kontoen brukes når du posterer en ferdigmeldingingsjournal for en produksjonsordre. Motkontoen for denne kontoen er Estimert produksjonskostnad, VIA. Beløpet i denne kontoen tilbakeføres automatisk når produksjonsordren avsluttes. Denne kontoen representerer lagerkontoen i balansen. |
| Estimert produksjonskostnad, VIA          | 150150               | Produksjons-VIA – Materialer | Objekt        | Kreditt         | Y                | Ø                     | Produksjonskostnad, VIA                    | Denne kontoen brukes når du posterer en ferdigmeldingingsjournal for en produksjonsordre. Motkontoen for denne kontoen er Estimert produksjonskostnad. Beløpet i denne kontoen tilbakeføres automatisk når en produksjonsordre avsluttes. Denne kontoen representerer VIA i balansen.                     |
| Kostnad for materialer brukt                | 140100               | Materiallager        | Objekt        | Kreditt         | N                 | F                     | Estimert kost for materialer brukt      | Denne kontoen brukes til å gjenkjenne materialene som forbrukes i produksjonsordren under avslutningsprosessen. Motkontoen for denne kontoen er Kostnad for materialer brukt, VIA.                                                                                                    |
| Kostnad for materialer brukt, VIA           | 150150               | Produksjons-VIA – Materialer | Objekt        | Debet          | N                 | F                     | Estimert kost for materialer brukt, VIA | Denne kontoen brukes til å gjenkjenne materialene i VIA som forbrukes i produksjonsordren under avslutningsprosessen. Motkontoen for denne kontoen er Kostnad for materialer brukt.                                                |
| Produksjonskostnad                         | 140200               | Ferdigvarelager   | Objekt        | Debet          | N                 | F                     | Estimert produksjonskostnad               | Denne kontoen brukes til å gjenkjenne kostnadene for den ferdigvaren som produseres av en produksjonsordre når du avslutter produksjonsordren. Motkontoen for denne kontoen er Produksjonskostnad, VIA.                                                                  |
| Produksjonskostnad, VIA                    | 150150               | Produksjons-VIA – Materialer | Objekt        | Kreditt         | N                 | F                     | Estimert produksjonskostnad, VIA          | Denne kontoen brukes til å gjenkjenne kostnadene for den ferdigvaren i VIA som produseres av en produksjonsordre når du avslutter produksjonsordren. Motkontoen for denne kontoen er Produksjonskostnad.                                     |

> [!NOTE]
> **VIA-kvittering for enkel tjeneste** og **VIA-clearingkonto for enkel tjeneste** brukes med backflush-etterkalkulering for lean manufacturing. For mer informasjon, se [Backflush-etterkalkulering](/supply-chain/cost-management/backflush-costing.md).

