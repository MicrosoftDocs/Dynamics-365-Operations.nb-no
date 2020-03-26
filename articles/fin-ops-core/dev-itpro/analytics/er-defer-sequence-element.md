---
title: Utsette kjøringen av sekvenselementer i ER-formater
description: Dette emnet forklarer hvordan du kan utsette kjøringen av et sekvenselement i et elektronisk rapporteringsformat (ER).
author: NickSelin
manager: kfend
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: EROperationDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-07-01
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 6efa4466dbf7f5ca1d3945acf15fac65d628d691
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124549"
---
# <a name="defer-the-execution-of-sequence-elements-in-er-formats"></a>Utsette kjøringen av sekvenselementer i ER-formater

[!include [banner](../includes/banner.md)]

[!include [banner](../includes/preview-banner.md)]

## <a name="overview"></a>Oversikt

Du kan bruke operasjonsutformingen i [Elektronisk rapportering (ER)](general-electronic-reporting.md)-rammeverket til å [konfigurere](tasks/er-format-configuration-2016-11.md) [formatkomponenten](general-electronic-reporting.md#FormatComponentOutbound) av en ER-løsning som brukes til å generere utgående dokumenter i et tekstformat. Den hierarkiske strukturen til den konfigurerte formatkomponenten består av formateringselementer av forskjellige typer. Disse formatelementene brukes til å fylle genererte dokumenter med påkrevd informasjon ved kjøretid. Når du kjører et ER-format, kjøres formatelementene som standard i samme rekkefølge som de presenteres i i formathierarkiet: ett etter ett, fra øverst til nederst. På utformingstidspunktet kan du imidlertid endre kjøringsrekkefølgen for alle sekvenselementer i den konfigurerte formatkomponenten.

Ved å aktivere <a name="DeferredSequenceExecution"></a>**Utsatt kjøring**-alternativet for et sekvensformatelement i det konfigurerte formatet kan du utsette (skyve frem i tid) kjøringen av dette elementet. I dette tilfellet kjøres ikke elementet før alle andre elementer i det overordnede utvalget er kjørt.

Hvis du vil vite mer om denne funksjonen, kan du fullføre eksemplet i dette emnet.

## <a name="limitations"></a>Begrensninger

**Utsatt kjøring**-alternativet støttes bare for sekvenselementer som er konfigurert for et ER-format som brukes til å generere **utgående** dokumenter i tekstformat.

**Utsatt kjøring**-alternativet er ikke aktuelt for sekvenser som er konfigurert som trimmede sekvenser der maksimal lengde er begrenset.

## <a name="example-defer-the-execution-of-a-sequence-element-in-an-er-format"></a><a name="Example"></a>Eksempel: Utsette kjøringen av et sekvenselement i et ER-format

Følgende trinn forklarer hvordan en bruker med [rollen](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/tasks/assign-users-security-roles) systemadministrator eller funksjonell konsulent for elektronisk rapportering kan konfigurere et ER-format som inneholder et sekvenselement der kjøringsrekkefølgen er forskjellig fra rekkefølgen i formathierarkiet.

Disse trinnene kan utføres i **USMF**-selskapet i Microsoft Dynamics 365 Finance.

### <a name="prerequisites"></a>Forutsetninger

For å fullføre dette eksempelet må du ha tilgang til **USMF**-selskapet i Finans for en av følgende roller:

- Funksjonell konsulent for elektronisk rapportering
- Systemansvarlig

Hvis du enda ikke har utført eksempelet i emnet [Utsette kjøringen av XML-elementer i ER-formater](er-defer-xml-element.md#Example), laster du ned følgende [konfigurasjoner](general-electronic-reporting.md#Configuration) av ER-eksempelløsningen.

| Innholdsbeskrivelse            | Filnavn |
|--------------------------------|-----------|
| ER-datamodellkonfigurasjon    | [Modell for å lære utsatte elementer.versjon.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |
| Konfigurasjon for ER-modellkartlegging | [Kartlegge for å lære utsatte elementer.versjon.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

Før du begynner, må du også laste ned og lagre følgende konfigurasjon av ER-eksempelløsningen.

| Innholdsbeskrivelse     |Filnavn |
|-------------------------|----------|
| ER-formatkonfigurasjon | [Formatere for å lære utsatte sekvenser.versjon.1.1.xml](https://mbs.microsoft.com/customersource/Global/AX/downloads/hot-fixes/365optelecrepeg) |

### <a name="import-the-sample-er-configurations"></a>Importere ER-eksempelkonfigurasjonene

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. Velg **Rapporteringskonfigurasjoner**.
3. På **Konfigurasjoner**-siden gjelder følgende: Hvis **Modell for å lære utsatte elementer**-konfigurasjonen er ikke tilgjengelig i konfigurasjonstreet, importerer du ER-datamodellkonfigurasjonen:

    1. Velg **Veksle**, og velg deretter **Last inn fra XML-fil**.
    2. Velg **Bla gjennom**, finn og velg **Modell for å lære utsatte elementer.1.xml**-filen og velg deretter **OK**.

4. Hvis **Kartlegg for å lære utsatte elementer**-konfigurasjonen er ikke tilgjengelig i konfigurasjonstreet, importerer du ER-modellkartleggingskonfigurasjonen:

    1. Velg **Veksle**, og velg deretter **Last inn fra XML-fil**.
    2. Velg **Bla gjennom**, finn og velg **Kartlegge for å lære utsatte elementer.1.xml**-filen og velg deretter **OK**.

5. Importer ER-formatkonfigurasjonen:

    1. Velg **Veksle**, og velg deretter **Last inn fra XML-fil**.
    2. Velg **Bla gjennom**, finn og velg **Format for å lære utsatte sekvenser.1.xml**-filen og velg deretter **OK**.

6. I konfigurasjonstreet utvider du **Modell for å lære utsatte elementer**.
7. Gjennomgå listen over importerte ER-konfigurasjoner i konfigurasjonstreet.

    ![Importerte ER-konfigurasjoner på konfigurasjonssiden](./media/ER-DeferredSequence-Configurations.png)

### <a name="activate-a-configurations-provider"></a>Aktivere en konfigurasjonsleverandør

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På **Lokaliseringskonfigurasjoner**-siden i **Konfigurasjonsleverandører**-delen må du sørge for at [konfigurasjonsleverandør](general-electronic-reporting.md#Provider) for eksempelselskapet Litware, Inc. (`http://www.litware.com`) er oppført, og at den er merket som aktiv. Hvis denne konfigurasjonsleverandøren ikke er oppført, eller hvis den ikke er merket som aktiv, følger du trinnene i emnet [Opprette en konfigurasjonsleverandør og merke den som aktiv](./tasks/er-configuration-provider-mark-it-active-2016-11.md).

    ![Eksempelselskapet Litware, Inc. på Lokaliseringskonfigurasjoner-siden](./media/ER-DeferredSequence-ElectronicReportingWorkspace.png)

### <a name="review-the-imported-model-mapping"></a>Gjennomgå den importerte modellkartleggingen

Gjennomgå innstillingene for ER-modellkartleggingskomponenten som er konfigurert til å få tilgang til avgiftstransaksjoner, og som viser åpnede data på forespørsel.

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. Velg **Rapporteringskonfigurasjoner**.
3. På **Konfigurasjoner**-siden, i konfigurasjonstreet, utvider du **Modell for å lære utsatte elementer**.
4. Velg **Kartlegge for å lære utsatte elementer**-konfigurasjonen.
5. Velg **Utforming** for å åpne listen over tilordninger.
6. Velg **Utforming** for å se gjennom tilordningensdetaljer.
7. Velg **Vis detaljer**.
8. Gjennomgå datakildene som er konfigurert for å få tilgang til avgiftstransaksjoner:

    - **Transaksjoner**-datakilden til *Tabelloppføring*-typen er konfigurert til å få tilgang til oppføringer i **TaxTrans**-applikasjonstabellen.
    - **Bilag**-datakilden til *Beregnet felt*-typen er konfigurert til å returnere de påkrevde bilagskodene (**INV-10000349** og **INV-10000350**) som en liste over oppføringer.
    - **Filtrert**-datakilden til *Beregnet felt*-typen er konfigurert til å velge, fra **Transaksjoner**-datakilden, bare avgiftstransaksjoner med de påkrevde bilagene.
    - **\$TaxAmount**-feltet i *Beregnet felt*-typen legges til for **Filtrert**-datakilden for å eksponere avgiftsverdien som har det motsatte tegnet.
    - **Gruppert**-datakilden til *Grupper etter*-typen er konfigurert til å gruppere filtrerte avgiftstransaksjoner av **Filtrert**-datakilden.
    - **TotalSum**-aggregeringsfeltet i **Gruppert**-datakilden er konfigurert til å summere verdiene i **\$TaxAmount**-feltet i **Filtrert**-datakilden for alle filtrerte avgiftstransaksjoner med denne datakilden.

        ![TotalSum-aggregeringsfeltet på siden Rediger GroupBy-parametere](./media/ER-DeferredSequence-GroupByParameters.png)

9. Gjennomgå hvordan de konfigurerte datakildene er bundet til datamodellen, og hvordan de viser tilgjengelige data for å gjøre dem tilgjengelige i et ER-format:

    - **Filtrert**-datakilden er bundet til **Data.List**-feltet for datamodellen.
    - **\$TaxAmount**-feltet for **Filtrert**-datakilden er bundet til **Data.List.Value**-feltet for datamodellen.
    - **TotalSum**-feltet for **Gruppert**-datakilden er bundet til **Data.Summary.Total**-feltet for datamodellen.

    ![Modellkartleggingsutforming-siden](./media/ER-DeferredSequence-ModelMapping.png)

10. Lukk sidene **Modellkartleggingsutforming** og **Modellkartlegginger**.

### <a name="review-the-imported-format"></a>Gå gjennom det importerte formatet

1. På **Konfigurasjoner**-siden, i konfigurasjonstreet, velger du **Formater for å lære utsatte sekvenser**-konfigurasjonen.
2. Velg **Utforming** for å se gjennom formatdetaljer.
3. Velg **Vis detaljer**.
4. Gjennomgå innstillingene for ER-formatkomponentene som er konfigurert til å generere et utgående dokument i tekstformat, som inneholder detaljer om avgiftstransaksjonene:

    - **Rapport\\Linjer**-sekvensformatelementet er konfigurert til å fylle det utgående dokumentet med én enkelt linje som genereres fra de nestede sekvenselementene (**Topptekst**, **Oppføring** og **Sammendrag**).

        ![Linjer-sekvensformatelementet og nestede elementer på Formatutforming-siden](./media/ER-DeferredSequence-Format.png)

    - **Rapport\\Linjer\\Topptekst**-sekvensformatelementet er konfigurert til å fylle det utgående dokumentet med én enkelt topptekstlinje som viser dato og klokkeslett for når behandlingen starter.
    - **Rapport \\Linjer\\Oppføring**-sekvensformatelementet er konfigurert til å fylle det utgående dokumentet med én enkelt linje som viser detaljene for individuelle avgiftstransaksjoner. Disse avgiftstransaksjonene er atskilt med semikolon.

        ![Oppføringssekvens-formatelement som bruker et semikolon som skilletegn](./media/ER-DeferredSequence-Format1.png)

    - **Rapport\\Linjer\\Sammendrag**-sekvensformatelementet er konfigurert til å fylle det utgående dokumentet med én enkelt sammendragslinje som inkluderer summen av avgiftsverdiene fra de behandlede avgiftstransaksjonene.

4. På **Kartlegging**-fanen gjennomgår du følgende detaljer.

    - **Rapport\\Linjer\\Topptekst**-elementet trenger ikke å være bundet til en datakilde for å generere én enkelt linje i et utgående dokument.
    - **Prefix1**-elementet genererer **P1**-symboler for å indikere at linjen som legges til, er rapporttopptekstlinjen.
    - **ExecutionDateTime**-elementet genererer datoen og klokkeslettet (inkludert millisekunder) topptekstlinjen legges til på.
    - **Rapport\\Linjer\\Oppføring**-elementet er bundet til **model.Data.List**-listen for å generere én enkelt linje for hver oppføring fra den bundne listen.
    - **Prefix2**-elementet genererer **P2**-symboler for å indikere at linjen som legges til, er for avgiftstransaksjonsdetaljene.
    - **TaxAmount**-elementet er bundet til **model.Data.List.Value** (som vises som **\@.Value** i den relative banevisningen) for å generere avgiftsverdien for den gjeldende avgiftstransaksjonen.
    - **RunningTotal**-elementet er en plassholder for den løpende summen av avgiftsverdier. Dette elementet har for øyeblikket ingen utdata, fordi verken en binding eller en standardverdi er konfigurert for det.
    - **ExecutionDateTime**-elementet genererer datoen og klokkeslettet (inkludert millisekunder) som den gjeldende transaksjonen behandles i denne rapporten på.
    - **Rapport\\Linjer\\Sammendrag**-elementet trenger ikke å være bundet til en datakilde for å generere én enkelt linje i et utgående dokument.
    - **Prefix3**-elementet genererer **P3**-symboler for å indikere at linjen som legges til, inneholder den totale avgiftsverdien.
    - **TotalTaxAmount**-elementet er bundet til **model.Data.Summary.Total** for å generere summen av avgiftsverdiene for de behandlede avgiftstransaksjonene.
    - **ExecutionDateTime**-elementet genererer datoen og klokkeslettet (inkludert millisekunder) sammendragslinjen legges til på.

    ![Kartlegging-fanen på Formatutforming-siden](./media/ER-DeferredSequence-Format2.png)

### <a name="run-the-imported-format"></a>Kjør det importerte formatet

1. På **Formatutforming**-siden velger du **Kjør**.
2. Last ned filen som nettleseren tilbyr, og åpne den for gjennomgang.

    ![Nedlastet fil](./media/ER-DeferredSequence-Run.png)

Vær oppmerksom på at sammendragslinje 22 representerer summen av avgiftsverdiene for de behandlede transaksjonene. Fordi formatet er konfigurert til å bruke **model.Data.Summary.Total**-bindingen til å returnere denne summen, beregnes summen ved å kalle til **TotalSum**-aggregeringen av **Gruppert**-datakilden til *GroupBy*-typen som bruker modellkartleggingen. For å beregne denne aggregeringen itererer modellkartlegging over alle transaksjoner som er valgt i **Filtrert**-datakilden. Ved å sammenligne kjøringstidene for linje 21 og 22 kan du bestemme at beregningen av summen tok 10 millisekunder (ms). Ved å sammenligne kjøringstidene for linje 2 og 21 kan du bestemme at genereringen av alle transaksjonslinjer tok 7 ms. Derfor var totalt 17 ms påkrevd.

### <a name="modify-the-format-so-that-the-summing-is-based-on-generated-output"></a>Endre formatet slik at summeringen baseres på genererte utdata

Hvis transaksjonsvolumet er mye større enn volumet i det gjeldende eksemplet, kan det hende at summeringstiden øker og forårsaker ytelsesproblemer. Hvis du endrer innstillingen for formatet, kan du bidra til å forhindre disse ytelsesproblemene. Fordi du får tilgang til avgiftsverdier for å inkludere dem i den genererte rapporten, kan du bruke denne informasjonen til å summere avgiftsverdier. Hvis du vil ha mer informasjon, kan du se [Konfigurere format for å utføre telling og summering](./tasks/er-format-counting-summing-1.md).

1. På **Formatutforming**-siden i **Format**-fanen velger du **Rapport**-filelementet i formattreet.
2. Sett **Samle inn utdatadetaljer**-alternativet til **Ja**. Du kan nå konfigurere dette formatet ved å bruke innholdet i en eksisterende rapport som en datakilde, som du kan få tilgang til ved å bruke de innebygde ER-funksjonene i [Datainnsamling](er-functions-category-data-collection.md)-kategorien.
3. På **Kartlegging**-fanen velger du **Rapport\\Linjer**-sekvenselementet.
4. Konfigurer **Nøkkelnavn på innsamlede data**-uttrykket som `WsColumn`.
5. Konfigurer **Nøkkelverdi for innsamlede data**-uttrykket som `WsRow`.

    ![Linjesekvenselement på Formatutforming-siden](./media/ER-DeferredSequence-Format3.png)

6. Velg det numeriske elementet **Rapport\\Linjer\\Oppføring\\TaxAmount**.
7. Konfigurer **Nøkkelnavn på innsamlede data**-uttrykket som `SummingAmountKey`.

    ![Det numeriske elementet TaxAmount på Formatutforming-siden](./media/ER-DeferredSequence-Format4.png)

    Du kan anse denne innstillingen som oppfyllelsen av et virtuelt arbeidsark, der verdien av celle A1 tilføyes med verdien på avgiftsbeløpet fra hver behandlet avgiftstransaksjon.

8. Velg det numeriske elementet **Rapport\\Linjer\\Oppføring\\RunningTotal**, og velg deretter **Rediger formel**.
9. Konfigurer `SUMIF(SummingAmountKey, WsColumn, WsRow)`-uttrykket ved å bruke den innebygde ER-funksjonen [SUMIF](er-functions-datacollection-sumif.md).
10. Velg **Lagre**.

    ![SUMIF-uttrykk](./media/ER-DeferredSequence-FormulaDesigner.png)

11. Lukk siden **Formelutforming**.
12. Velg **Lagre**, og velg deretter **Kjør**.
13. Last ned og gjennomgå filen som nettleseren tilbyr.

    ![Nedlastet fil](./media/ER-DeferredSequence-Run1.png)

    Linje 21 inneholder den løpende summen av avgiftsverdiene, som er beregnet for alle behandlede transaksjoner ved å benytte de genererte utdataene som en datakilde. Denne datakilden starter fra begynnelsen av rapporten og fortsetter til den siste avgiftstransaksjonen. Linje 22 inneholder summen av avgiftsverdiene for alle behandlede transaksjoner som er beregnet i modellkartleggingen ved å benytte datakilden av *GroupBy*-typen. Vær oppmerksom på at disse verdiene er like. Derfor kan den utdatabaserte summeringen brukes i stedet for **GroupBy**. Ved å sammenligne kjøringstidene for linje 2 og 21 kan du bestemme at genereringen av alle transaksjonslinjene og summeringen tok 9 ms. Når det gjelder genereringen av detaljerte linjer og summeringen av avgiftsverdier, er det endrede formatet derfor omtrent to ganger raskere enn det opprinnelige formatet.

14. Velg det numeriske elementet **Rapport\\Linjer\\Sammendrag\\TotalTaxAmount**, og velg deretter **Rediger formel**.
15. Angi `SUMIF(SummingAmountKey, WsColumn, WsRow)`-uttrykket i stedet for det eksisterende uttrykket.
16. Velg **Lagre**, og velg deretter **Kjør**.
17. Last ned og gjennomgå filen som nettleseren tilbyr.

    ![Nedlastet fil](./media/ER-DeferredSequence-Run2.png)

    Vær oppmerksom på at den løpende summen av avgiftsverdier på den siste linjen over transaksjonsdetaljer nå er lik summen på sammendragslinjen.

### <a name="put-values-of-output-based-summing-in-the-report-header"></a>Sett verdier av utdatabasert summering i rapporttoppteksten

Hvis du for eksempel må presentere summen av avgiftsverdier i rapportens topptekst, kan du endre formatet.

1. På **Formatutforming**-siden, i **Format**-fanen velger du **Rapport\\Linjer\\Sammendrag**-sekvenselementet.
2. Velg **Flytt opp**.
3. Velg **Lagre**, og velg deretter **Kjør**.
4. Last ned og gjennomgå filen som nettleseren tilbyr.

    ![Nedlastet fil](./media/ER-DeferredSequence-Run3.png)

    Legg merke til at summen av avgiftsverdier på sammendragslinje 2 nå er lik 0 (null), fordi denne summen nå beregnes på grunnlag av de genererte utdataene. Når linje 2 genereres, inneholder ikke de genererte utdataene linjer med transaksjonsdetaljer enda. Du kan konfigurere dette formatet til å utsette kjøringen av **Rapport\\Linjer\\Sammendrag**-sekvenselementet til **Rapport\\Linjer\\Oppføring**-sekvenselementet er kjørt for alle avgiftstransaksjoner.

### <a name="defer-the-execution-of-the-summary-sequence-so-that-the-calculated-total-is-used"></a>Utsett kjøringen av sammendragssekvensen slik at beregnet sum brukes

1. På **Formatutforming**-siden, i **Format**-fanen velger du **Rapport\\Linjer\\Sammendrag**-sekvenselementet.
2. Sett **Utsatt kjøring**-alternativet til **Ja**.

    ![Utsatt kjøring-alternativet for Sammendragssekvens-elementet på Formatutforming-siden](./media/ER-DeferredSequence-Format5.png)

3. Velg **Lagre**, og velg deretter **Kjør**.
4. Last ned og gjennomgå filen som nettleseren tilbyr.

    ![Nedlastet fil](./media/ER-DeferredSequence-Run4.png)

    **Rapport\\Linjer\\Sammendrag**-sekvenselementet kjøres nå bare etter alle andre elementer som er nestet under det overordnede elementet, **Rapport\\Linjer**, har blitt kjørt. Derfor kjøres det etter at **Rapport\\Linjer\\Oppføring**-sekvenselementet har blitt kjørt for alle avgiftstransaksjoner med **model.Data.List**-datakilden. Kjøringstidene for linje 1, 2 og 3, og for den siste linjen, 22, avslører dette faktumet.

## <a name="additional-resources"></a>Tilleggsressurser

- [Konfigurere format for å utføre telling og summering](./tasks/er-format-counting-summing-1.md)
- [Spore utførelse av ER-format for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md)
- [Utsette kjøringen av XML-elementer i ER-formater](er-defer-xml-element.md#Example)
