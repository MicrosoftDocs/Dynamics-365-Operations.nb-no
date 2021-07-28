---
title: Generere konsoliderte regnskapsoppgjør
description: Dette emnet beskriver de forskjellige scenariene der du kan generere konsoliderte regnskapsoppgjør.
author: aprilolson
ms.date: 07/09/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2018-5-31
ms.dyn365.ops.version: 8.0.1
ms.openlocfilehash: dce0dd216d552d956ba7fdbcb4eebb6ed85b7115
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6348968"
---
# <a name="generate-consolidated-financial-statements"></a>Generere konsoliderte regnskapsoppgjør

[!include [banner](../includes/banner.md)]

Dette emnet beskriver de forskjellige scenariene der du kan generere konsoliderte regnskapsoppgjør.

## <a name="single-level-and-multilevel-consolidations-across-legal-entities"></a>Enkeltnivå- og flernivåkonsolideringer på tvers av juridiske enheter
Den enkleste metoden for å konsolidere ved hjelp av Finansrapportering er å bruke rapporteringstrær for å samle data på tvers av firmaer som har samme kontoplan og regnskapsperioder. Her er fremgangsmåten på høyt nivå for å konsolidere ved å bruke et rapporteringstre.

1. Opprett en raddefinisjon, og kontroller at alle de aktuelle kontoene i alle firmaer er inkludert i radene.
2. Opprett en kolonnedefinisjon som inneholder alle kolonnene som er nødvendig for rapporten som du oppretter.
3. Opprett et rapporteringstre som inkluderer en rapporteringsnode for hvert firma som du bruker i konsoliderte rapporter.

> [!TIP]
> Hvis du vil ha mer informasjon om hvordan du oppretter og behandler raddefinisjoner, kolonnedefinisjoner og rapporteringstrær, se [Komponenter for finansrapport](../../fin-ops-core/dev-itpro/analytics/financial-report-components.md).

Illustrasjonen nedenfor viser hvordan du kan bruke en definisjon for rapporteringstre i Finansrapport til å identifisere hvert enkelt firma som du vil konsolidere.

![Rapporteringstredefinisjon.](./media/reporting-tree-definition.png "Rapporteringstredefinisjon")

Som den konsoliderte rapporten i illustrasjonen nedenfor viser, når du bruker rapporteringstreet sammen med en rapportdefinisjon, kan du vise hvert firma separat. De konsoliderte beløpene vises på sammendragsnivå.

![Konsoliderte beløp på sammendragsnivå.](./media/consolidate-amount-summary-level.png "Konsoliderte beløp på sammendragsnivå")

Du kan også opprette et rapporteringstre med en liste med flere nivåer som har så mange nivåer du trenger. Illustrasjonen nedenfor viser en liste med flere nivåer rapporteringstredefinisjon med fremhevinger ved globalt område.

![Definsjon av rapporteringstre for flere nivåer med opprullinger etter region.](./media/multilevel-reporting-tree-definition-roll-ups-worldwide-region.png "Definsjon av rapporteringstre for flere nivåer med opprullinger etter region")

Illustrasjonen nedenfor viser en liste med flere nivåer rapporteringstredefinisjon med fremhevinger etter funksjon.

![Definsjon av rapporteringstre for flere nivåer med opprullinger etter funksjon.](./media/multilevel-reporting-tree-definition-roll-ups-by-function.png "Definsjon av rapporteringstre for flere nivåer med opprullinger etter funksjon")

### <a name="viewing-companies-side-by-side"></a>Vise firmaer side ved side
Mange kunder foretrekker rapporter der firmaene vises side ved side, og der en kolonne viser den konsoliderte totalsummen. Dette formatet er enkelt å oppnå når du har opprettet rapporteringstreet. Her er trinnene på høyt nivå for å vise firmaer side ved side i konsoliderte regnskapsoppgjør.

1. Opprett en kolonnedefinisjon som inkluderer en **Finansdimensjon** -kolonne for hvert firma.
2. Bruk feltet **Rapporteringsenhet** til å velge treet og rapporteringsenheten for hver kolonne.
3. Valgfritt: Legg til overskrifter og totalsumkolonner.

Illustrasjonen nedenfor viser en kolonnedefinisjon i et side-ved-side-format.

![Kolonnedefinisjon i et side-ved-side-format.](./media/column-definition-side-by-side-format.png "Kolonnedefinisjon i et side-ved-side-format")

## <a name="consolidations-that-use-organization-structures-that-are-created-from-legal-entities"></a>Konsolideringer som bruker organisasjonsstrukturer som opprettes fra juridiske enheter
Organisasjonshierarkier med dimensjoner eller juridiske enheter oppretter dynamisk rapporteringstredefinisjonene i Finansirapportering. En enkel måte å strømlinjeforme konsolideringer på er å legge til et organisasjonshierarki i rapporten i Finansirapportering. Basert på rapportdatoen, velger Financial reporting organisasjonshierarkiet på eller før den effektive datoen, som vist i illustrasjonen nedenfor.

![Dynamisk oppretting av rapporteringstredefinisjon.](./media/dynamically-create-reporting-tree-definitions.png "Dynamisk oppretting av rapporteringstredefinisjon")

## <a name="consolidations-that-involve-eliminations"></a>Konsolideringer som involverer elimineringer
Elimineringstransaksjoner er en vanlig del av konsolideringsprosessen. I dette eksemplet elimineres fem kontoer i løpet av konsolideringen: 142600, 211400, 401420, 401180 og 510820. Firmaer kan definere de konserninterne kontoene på en annen måte. Enkelte firmaer kan for eksempel angi det siste sifferet til 9 hvis kontoen brukes i konserninterne transaksjoner. Uansett metode, hvis du kjenner de konserninterne kontoene, kan du vise elimineringer på de konsoliderte regnskapsoppgjørene.

Illustrasjonen nedenfor viser en kolonnedefinisjon for et konsolidert resultatregnskap. Tre konserninterne resultatkontoer for fortjeneste og tap defineres for hvert firma ved hjelp av dimensjonsfilteret. Kolonnene F, G og H inkluderer elimineringskontoene bare for firmaene USCOR, USRT og DEMF. Disse kolonnene er satt opp slik at de **ikke** skrives ut i regnskapsoppgjøret.

![Kolonnedefinisjon for konsolidert resultatregnskap.](./media/column-definition-consolidated-income-statement.png "Kolonnedefinisjon for konsolidert resultatregnskap")

Når rapporten genereres, beregnes elimineringsbeløpene i kolonnene F, G og H, og de summeres i kolonne I. Kolonne J viser de konsoliderte beløpene. Disse konsolideringsbeløpene utelukker elimineringer for USMF-, USRT- og DEMF-firmaene.

> [!TIP]
> Opprett en annen rapport som viser bare elimineringsoppføringer, og bruk den i en rapportgruppe som inneholder den konsoliderte rapporten. På denne måten kan du ha all nødvendig informasjon for å opprette alle journaloppføringer som er nødvendig.

Følgende illustrasjon viser den konsoliderte rapporten.

![Konsolidert rapport, resultatregnskap.](./media/consolidated-report-income-statement.png "Konsolidert rapport, resultatregnskap")

Enten du bruker kontoer, dimensjoner eller begge deler, lar Finansrapportering deg filtrere ut elimineringspostene ved hjelp av dimensjonsfiltreringsfunksjonene.

## <a name="minority-interest"></a>Minoritetsrente
Et firma eier kanskje bare en prosent av et annet firma. I så fall, når du produserer en konsolidert rapport, er det viktig at du tar hensyn til bare prosentdelen som firmaet eier. Finansrapportering har flere måter å vise minoritetsrente på, avhengig av brukerinnstillingen. Én måte er å bruke en beregnet prosent i definisjonen av rapporteringstreet. En annen måte er å vise minoritetseierskapet som en egen linje i en rapport.

### <a name="using-the-reporting-tree-definition"></a>Bruke definisjonen av rapporteringstre
I rapporteringstredefinisjonen kan du angi prosenten av eierskap i kolonnen **Opprullings-%** (kolonne H), som vist i illustrasjonen nedenfor. Når rapporten er generert, brukes denne prosenten til å regne ut det konsoliderte beløpet. I dette eksemplet eier Contoso bare 80 prosent av Contoso Tyskland. Du kan angi enten **80** eller **.8** i kolonnen **Opprullings-%**, og 80 prosent blir rullet opp til det konsoliderte nivået.

> [!NOTE]
> Du kan bruke denne eierskapsprosenten på en hvilken som helst rapporteringsenhet, ikke bare på firmanivå. 

![Bruke prosentverdi i rapporteringstredefinisjonen.](./media/Using-reporting-tree-definition-percentage.png "Bruke prosentverdi i rapporteringstredefinisjonen")

Når rapporten er generert, viser Contoso Tyskland-rapporten 100 prosent av salgsbeløpet, og 80 prosent av beløpet blir fordelt og rullet opp til det konsoliderte salgsnivået.

Hvis du eier mindre enn 1 prosent av et firma, kan du merke av for **Tillat opprullering på mindre enn 1 %** i kategorien **Tilleggsalternativer** på **Innstillinger**-siden, som vist i illustrasjonen nedenfor. I så fall blir verdier i kolonnen **Opprullings-%** i rapporteringstreet behandlet som mindre enn 1 prosent. Hvis du angir for eksempel **.8**, blir 0,8 prosent rullet opp til det konsoliderte nivået, ikke 80 prosent. Alternativt kan du oppnå samme resultat ved å la **Tillat opprulling på mindre enn 1%** stå tomt og angi **.008** i kolonnen **Opprullings-%**.

![Alternativer for rapportinnstillinger.](./media/reporting-setting-options.png "Alternativer for rapportinnstillinger")

### <a name="showing-ownership-as-a-separate-row-on-the-consolidated-report"></a>Vise eierskap som en separat rad i den konsoliderte rapporten
Et annet alternativ for minoritetsrente er å vise 100 prosent av datterselskapet for hver linje i rapporten, men trekke den ikke-kontrollerte renten fra nettoinntekten.

Som eksemplet nedenfor viser, kan et **IF THEN ELSE**-uttrykk og kolonnenbegrensningen i raddefinisjonen brukes til å beregne minoritetsrenter i finansrapporter.

![Vise eierskap som en separat rad i den konsoliderte rapporten.](./media/Showing-ownership-separate-row-consolidated-report.png "Vise eierskap som en separat rad i den konsoliderte rapporten")

## <a name="multiple-charts-of-accounts-across-legal-entities"></a>Flere kontoplaner på tvers av juridiske enheter
Ofte har andre juridiske enheter forskjellige kontoplaner, men ønsker likevel å produsere konsoliderte regnskapsoppgjør. I så fall kan Finansrapportering brukes til å konsolidere dataene, slik at du kan generere konsoliderte finansrapporter. Her er fremgangsmåten på høyt nivå for å konsolidere når det finnes ulike kontoplaner på tvers av juridiske enheter.

1. Opprett en raddefinisjon med flere koblinger til finansdimensjoner. Det skal være én kobling for hver kontoplan.
2. Bruk rapporteringsenhetsbegrensningen i kolonnedefinisjonen til å tilordne hvert firma til rett kolonne.


Flere koblinger til finansdimensjoner kan legges til i hver rad i raddefinisjonen for hvert unike firmas kontoplan. I illustrasjonen nedenfor bruker USMF-firmaet kontosettet i den første **Kobling til finansdimensjoner**-kolonnen (kolonne J), og DEMF-firmaet bruker kontoene i den andre **Kobling til finansdimensjoner**-kolonnen (kolonne K).

> [!TIP]
> Hvis du vil ha mer informasjon om cellen **Kobling til finansdimensjoner**, kan du se Angi cellen Kobling til finansdimensjoner.

![Angi den første koblingen for kontoer til finansdimensjoner.](./media/set-accounts-first-Link-to-Financial-Dimensions.png "Angi den første koblingen for kontoer til finansdimensjoner")

Du kan bruke en rapporteringstrestruktur til å definere hvilken kobling til finansdimensjoner fra raddefinisjonen som skal brukes med hvert firma. Velg raddefinisjonen i kolonne E, og klikk deretter koblingen for riktig rad i kolonne F, som vist i illustrasjonen nedenfor.

![Brukt kobling til raddefinisjon for finansdimensjoner.](./media/link-financial-dimensions-row-definition-used.png "Brukt kobling til raddefinisjon for finansdimensjoner")

> [!TIP]
> Når du oppretter koblinger til finansdimensjoner, kan du bruke beskrivelsen til å identifisere firmaer som hver kobling gjelder for. På denne måten kan du enklere velge det riktige firmaet når du oppretter et rapporteringstre. I kolonnedefinisjonen lar feltet **Rapporteringsenhet** deg begrense hver kolonne til en enhet i rapporteringstreet, slik at du kan vise dataene side ved side. Hvis du ikke angir et bestemt firma for en kolonne, vises konsoliderte data for alle firmaer.

## <a name="different-fiscal-calendars-across-multiple-legal-entities"></a>Ulike regnskapskalendere på tvers av flere juridiske enheter
Ulike juridiske enheter kan ha ulike økonomiske kalendere, men må likevel produsere konsoliderte regnskapsoppgjør. Det er to måter å konsolidere på når det finnes ulike regnskapsperioder på tvers av juridiske enheter:

- Opprett en kolonnedefinisjon, og bruk periode og år for å tilordne de riktige periodene for hvert firma.
- Under **Innstillinger** \> **Annet** \> **Tilleggsalternativer** velger du om du vil konsolidere ved hjelp av periodens sluttdato eller periodenummeret.

Når du utformer kolonnedefinisjonen for flere firmaer som har forskjellige regnskapsperioder, er det viktig at du vurderer hvilket firma som skal tilordnes til feltet **Firmanavn** i rapportdefinisjonen. Firmaets regnskapskalender vil bli brukt som basis regnskapskalender for rapportdefinisjonen. Tabellen nedenfor viser for eksempel regnskapsperiodeoppsettet som ble konfigurert for USMF- og INMF-firmaene. For konsoliderte rapporter kan du bruke den økonomiske kalenderen som USMF bruker. Kolonnen "Tilordning" viser tilsvarende periode og år for hvert firma hvis det opprettes en rapport for 30. juni 2018.

| Bedrift   | Regnskapsår                                  | Tildeling                     |
|-----------|----------------------------------------------|-----------------------------|
| USMF      | Regnskapsår, 1. juli til 30. juni          | Periode 12, regnskapsåret 2018 | 
| INMF      | Kalenderår, 1. januartil 31. desember | Periode 6, regnskapsåret 2018  |

I illustrasjonen nedenfor er USMF-firmaet angitt i feltet **Firmanavn** i rapportdefinisjonen. USMF-firmaets regnskapskalender vil derfor bli brukt som basis regnskapskalender. Når det genereres en rapport for 30. juni 2018, bruker i dette eksemplet USMF-firmaet BASE-perioden, som er definert som periode 12 i rapportdefinisjonen. INMF-firmaet bruker BASE -6, som er periode 6. Begge kolonnene inkluderer data for juni 2018.

![BASE-periode for rapport.](./media/report-base-period.png "BASE-periode for rapport")

Illustrasjonen nedenfor viser alternativene i rapportdefinisjonen som du kan bruke til å velge om periodenummeret eller periodens sluttdato skal brukes til konsolideringen.

![Alternativer for periodenummer for rapporterdefinisjon.](./media/options-report-definition-period-number.png "Alternativer for periodenummer for rapporterdefinisjon")

## <a name="business-unit-consolidations"></a>Forretningsenhetskonsolideringer
Dette emnet har fokus på bruk av rapporteringstredefinisjoner og organisasjonshierarkier Finansrapportering til konsolideringsformål. Du kan også bruke rapporteringstreet til å opprette konsolideringsrapporter for forretningsenheten, for eksempel rapporter om globalt salg eller global drift. Disse rapportene er et vanlig krav. Du kan opprette dem ved å velge et firma og en dimensjon for hver enhet du vil konsolidere i. I illustrasjonen nedenfor oppnås for eksempel opprulling av forretningsenheten ved å gjenta hvert firma i **Firma**-kolonnen (kolonne A) og identifisere en gruppe med avdelingsdimensjonsverdier per firma i **Dimensjoner**-kolonnen (kolonne D).

![Konsolideringsrapporter for forretningsenhet.](./media/business-unit-consolidation-reports.png "Konsolideringsrapporter for forretningsenhet")

## <a name="consolidations-that-involve-multiple-reporting-currencies"></a>Konsolideringer som omfatter flere rapporteringsvalutaer
Finansrapportering gir økt fleksibilitet når du viser faktiske data, budsjetterte data, budsjettkontrolldata og budsjettplanleggingsdata i flere valutaer. Ved å ta over viktige oppsettdata, trenger du ikke gjøre noe mer oppsett i Finansrapportering for å vise enhver, i hvilken som helst valuta når som helst for alle brukere.

### <a name="prerequisites"></a>Nødvendig programvare
Hvis du vil beregne oversatte saldoer på riktig måte, krever Finansrapporter at kategorien **Konto for opptjente midler** tilordnes til kontoen for opptjente midler i listen **Hovedkonto**. Finansrapportering støtter ikke postering til kontoen for opptjente midler. Hvis transaksjoner posteres til kontoen for opptjente midler, beregnes ikke de omregnede saldoene på riktig måte. Vi anbefaler at brukere angir en ekstra opptjente midler-konto for å postere justeringer i kontoen for opptjente midler.

I hovedkontoen må fletene **Valutakurstype for finansrapportering** og **Type valutaveksling** i hurtigkategorien **Finansrapportering** angis for hver konto, som vist i følgende illustrasjon. Du kan fullføre denne oppgaven på konto-til-konto-basis, eller du kan bruke kontomalene til enkelt å rulle ned endringer.

- I feltet **Valutakurstype for finansrapportering** velger du valutakurstypen som inneholder valutaene og valutakursene som skal brukes på kontoen. Denne tabellen over valutaer og valutakurser brukes på faktiske data i Finansirapportering.
- I feltet **Type valutaveksling** velger du metoden som skal brukes til å beregne valutakursen for kontoen. Denne valutametoden brukes til både faktiske og budsjetterte data i Finansirapportering.

![Hovedkontoer i Finansrapportering.](./media/Financial-reporting-main-accounts.png "Hovedkontoer i Finansrapportering")

For budsjett, budsjettkontroll og budsjettplanleggingsdata er valutakurtypen definert på **Finans**-siden. Denne tabellen brukes til å hente valutakursene, og valutaomregningstypen som er tilordnet til kontoen, brukes.

### <a name="currency-translation-methods"></a>Metoder for valutaveksling
Det finnes fire alternativer for å beregne valutakurser i Finansirapportering:

- **Avveid gjennomsnitt** – denne metoden brukes oftest for fortjeneste og tap-kontoer. Følgende formel brukes:

    (Valutakurs × dager i effekt) ÷ dager i perioden

- **Gjennomsnitt** – denne metoden er en alternativ metode for fortjeneste og tap-kontoer. Følgende formel brukes:

    Totalt antall valutakurser ÷ antall valutakurser

- **Gjeldende** – denne metoden brukes oftest for balansekontoer. Valutakursen som brukes, er kursen på eller før datoen for rapporten eller kolonnen i Finansirapportering.
- **Transaksjonsdato** – denne metoden brukes til kontoer for anleggsmidler. Valutakursen som brukes, er kursen på dagen da anleggsmidlet ble anskaffet. Hvis en kurs ikke er angitt for den aktuelle datoen, brukes den tidligere kursen som ble lagt inn nærmest anskaffelsesdatoen for aktivumet.

### <a name="report-designer-options-for-currency-translation"></a>Rapportutformingsalternativer for valutaomveksling
I Finansrapport kan en hvilken som helst rapport vises i et hvilket som helst antall rapportvalutaer. Følgende felt i rapportdefinisjonen støtter denne funksjonen:

- Delen **Valutainformasjon** på siden **Rapportdefinisjon**. Denne delen viser valutaen som verdiene skal vises i, når det genereres en rapport.
- En ny **Inkluder alle rapporteringsvalutaer**-avmerkingsboks. Når denne avmerkingsboksen er valgt, legges det til en rapport for hver rapporteringsvaluta i rapportkøen etter at rapporten som bruker firmaets funksjonelle valuta, er generert. Hvis merket er fjernet, kan du fremdeles velge en rapporteringsvaluta i nettvisningsprogrammet. I så fall behandles rapporteringsvalutaen bare når du velger den.

Alternativene i rapportdefinisjonen gjør det mulig å oversette en rapport til alle rapporteringsvalutaer. Du kan derfor kanskje eliminere duplikate rapportdefinisjoner som er forskjellige, bare i valutaene som brukes. Hvis du trenger en rapport som viser flere valutaer ved siden av hverandre, kan du fortsette å bruke feltet **Valutavisning** på siden **Kolonnedefinisjon** til bare å regne om denne kolonnen i rapporten til en alternativ rapporteringsvaluta.

### <a name="currency-translation-adjustment"></a>Justering av valutaomveksling
Justering av valutaomveksling (CTA) er forskjellen mellom kursene som brukes til å beregne balansekontoer og kursen som brukes for resultatkontoene. Denne forskjellen får balansen til å bli ubalansert. Du kan bruke Finansrapportering til å beregne CTA på to måter:

- Bruk siden **Avrundingsjusteringer** i raddefinisjonen, som vist i illustrasjonen nedenfor.

    ![Avrundingsjusteringer ved valutaomregning.](./media/Currency-translation-adjustment-rounding-adjustments.png "Avrundingsjusteringer ved valutaomregning")

    Når du angir raden som skal vise avrundingsjusteringen (CTA), raden for samlede aktiva, samlet gjeld og egenkapital og terskelen som du er vant til, beregner Finansrapportering forskjellen og legger den inn på den aktuelle raden. En linje som heter **Avrundingsjustering** opprettes og vises ved neddrilling, som vist i illustrasjonen nedenfor.

    ![Avrundingsjustering, neddrilling.](./media/rounding-adjustment-drill-down.png "Avrundingsjustering, neddrilling")

- Plasser alle kontoene i et område, fra anleggsmidler til utgifter. Som vist i illustrasjonen nedenfor, blir forskjellen det samme beløpet som avrundingsjusteringen (CTA). Derfor kan du bruke det som en totalsumkontroll for å være sikker på at avrundingsjusteringssiden ikke inneholder noen kontosaldoer som ble hoppet over.

    ![Sjekk av avrundingsjusteringsskjemaet.](./media/rounding-adjustment-form-check.png "Sjekk av avrundingsjusteringsskjemaet")

### <a name="balance-calculation-approach"></a>Saldoberegningsmetode
For korrekt omregnede beløp når valutaer brukes, bruker Finansrapportering følgende beregningsmetoder for saldoene:

- **Avveid gjennomsnitt og gjennomsnitt** – hver periode blir beregnet ved dens avveide gjennomsnitt, og legges sammen for kolonner som kvartalsvis og hittil i år.
- **Historisk** – alle kontoer som bruker den historiske omregningsmetoden, alltid går tilbake til transaksjonsdatoen. Hvis det er knyttet en anskaffelsesdato til transaksjonen, brukes denne datoen til å få valutakursen. Hver periode totalsummeres deretter og lagres for å forbedre beregningstiden.
- **Gjeldende** – kolonner for beregnet beløp og totalsum, for eksempel for kvartalsvis og hittil i år, blir beregnet etter spotkursen som angis i kolonnen eller i rapporten. Kolonnen **kvartal 1** bruker for eksempel kursen 31. mars hvis et kalenderår brukes.

## <a name="additional-resources"></a>Tilleggsressurser

Hvis du vil ha mer informasjon om konsolidering og valutavekslinger, kan du se det overordnede emnet i dette emnet, [Oversikt over finanskonsolideringer og valutaomveksling](./financial-consolidations-currency-translation.md).

Hvis du vil ha mer informasjon om hvordan du registrerer detaljer om konsolideringer på nettet, kan du se [Elektroniske finanskonsolideringer](./consolidate-online.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]