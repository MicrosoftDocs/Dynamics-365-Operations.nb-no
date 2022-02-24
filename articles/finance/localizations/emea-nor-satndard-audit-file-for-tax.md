---
title: Standard revisjonsfil for avgift (SAF-T) for Norge
description: Dette emnet forklarer hvordan du setter opp og generere standard revisjonsfil for avgift (SAF-T) for juridiske enheter som har en primær postadresse i Norge.
author: liza-golub
ms.author: elgolu
ms.date: 04/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
manager: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Norway
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: f26d3d49af8ddf2d5f10c516e81a4d21727a9f72
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4408309"
---
# <a name="standard-audit-file-for-tax-saf-t-for-norway"></a>Standard revisjonsfil for avgift (SAF-T) for Norge

[!include [banner](../includes/banner.md)]

Dette emnet inneholder landsspesifikk informasjon om hvordan du setter opp standard revisjonsfil for avgift (SAF-T) for juridiske enheter som har en primæradresse i Norge.

## <a name="introduction"></a>Innledning

Fra og med januar 2020 er alle selskaper i Norge pålagt av Skatteetaten å gi SAF-T finansielle data. Dette kravet er i samsvar med versjon 1.4 av dokumentasjonen, som ble publisert den 8. juli 2019, og versjon 1.3 av den tekniske dokumentasjonen, som ble publisert den 23. mars 2018, i form av en XML-rapport. Publiseringen av disse delene av dokumentasjonen sammenfaller med versjon 1.1 av "norsk SAF-T økonomiske data" XML Schema Definition (XSD)-skjema som ble utviklet av SAF-T-arbeidsgruppen, Skatteetaten, og basert på "OECD-standard revisjonsfil - Avgifter 2.00,"som ble modifisert 2. februar 2018.

## <a name="overview"></a>Oversikt

For å støtte rapporten **Norsk SAF-T økonomiske data** må Microsoft Dynamics 365 Finance-programmet være en av følgende versjoner eller senere.

| Versjon av Finance | Build-nummer       |
|--------------------|--------------------|
| 10.0.6             | 10.0.234.**20020** |
| 10.0.7             | 10.0.283.**10012** |
| 10.0.8             | 10.0.319.**12**    |
| 10.0.9             | 10.0.328.**20020** |

Når Finance-programversjonen er egnet, importerer du følgende versjoner eller senere av disse konfigurasjonene for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS).

| ER-konfigurasjonsnavn              | Konfigurasjonstype | Versjon |
|------------------------------------|--------------------|---------|
| Standard revisjonsfil (SAF-T)        | Modell              | 32      |
| SAF-T økonomiske datamodelltilordning | Modelltilordning      | 32.30   |
| SAF-T-format (NO)                  | Format (eksport) | 32.41   |

Importer de nyeste versjonene av konfigurasjonene. Versjonsbeskrivelsen inneholder vanligvis nummeret til Microsoft Knowledge Base-artikkelen (KB) som forklarer endringene som konfigurasjonsversjonen introduserte.

> [!NOTE]
> Når du er ferdig med å importere alle ER-konfigurasjoner fra tabellen ovenfor, kan du angi alternativet **Standard for modelltilordning** til **Ja** for konfigurasjonen **SAF-T økonomiske datamodelltilordning**.
>
> ![Standardalternativ for modelltilordning er satt til Ja](media/nor-saf-default-model-mapping.jpg)


![Last opp og legg til-knappen](media/nor-saf-default-model-mapping.jpg)

Hvis du vil ha mer informasjon om hvordan du laster ned ER-konfigurasjoner fra Microsoft Dynamics Lifecycle Services (LCS), kan du se [Laste ned konfigurasjoner for elektronisk rapportering fra Lifecycle Services](../../dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).


## <a name="setup"></a>Oppsett

Hvis du vil begynne å bruke rapporten **Norsk SAF-T økonomiske data** i Finance, må du fullføre følgende oppsett:

- **Parametere for økonomimodul:** Definer ER-formatet på siden **Parametere for økonomimodul**.
- **Mva-koder:** Knytt mva-koder til norske standard mva-koder for merverdiavgift (mva.).
- **Hovedkontoer:** Knytt hovedkontoer til norske standardkontoer.

Delene nedenfor forklarer hvordan du gjør hver del av dette oppsettet.

### <a name="general-ledger-parameters"></a>Parametere for økonomimodul

1. I Finance går du til **Økonomimodul** \> **Finansoppsett** \> **Parametere for økonomimodul**.
2. På siden **Parametere for økonomimodul**, i kategorien **Standard revisjonsfil for avgift (SAF-T)** i feltet **Standard revisjonsfil for avgift (SAF-T)**, velger du **SAF-T-format (NO)**.

![Feltet Standard revisjonsfil for avgift (SAF-T) på siden parametere for økonomimodul](media/nor-saf-gl-parameters.jpg)

### <a name="sales-tax-codes"></a>Mva-koder

Som dokumentasjonen forklarer, må mva-koder i norsk SAF-T Financial-data som brukes i Finance, være knyttet til norske standard mva-koder (\<StandardTaxCode\>) for SAF-T-rapportering. Norske standard mva-koder er tilgjengelige på <https://github.com/Skatteetaten/saf-t>.

Hvis du vil knytte mva-koder som brukes i Finance, med norske standard mva-koder, følger du denne fremgangsmåten.

1. I Finance går du til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Mva-koder**.
2. På siden **Mva-kode** velger du **Mva-kode**-posten, og deretter, i handlingsruten i kategorien **Mva-kode** i gruppen **Mva-kode**, velger du **Eksterne koder**.

    ![Eksterne koder-knappen i handlingsruten på siden for mva-kode](media/nor-saf-standard-tax-codes.jpg)

3. På **Eksterne koder**-siden angir du norske standard mva-koder som skal brukes for den valgte posten for mva-koden, for SAF-T-rapportering.

### <a name="main-accounts"></a>Hovedkontoer

Som dokumentasjonen forklarer, i Norsk SAF-T økonomiske data, må hovedkontoer som brukes i Finance, være knyttet til norske standardkontoer for SAF-T-rapportering. Norske standardkontoer er tilgjengelige på <https://github.com/Skatteetaten/saf-t>.


Fra og med **versjon 54.61** støtter det elektroniske rapporteringsformatet **“SAF-T-format (NO)”** oppsettet av **Standardkontoer** for selskapets **Hovedkontoer** ved å benytte **Applikasjonsspesifikke parametere**.

Hvis du vil knytte **Hovedkontoer** som brukes i Finans, til norske standardkontoer via **Applikasjonsspesifikke parametere**, følger du trinnene nedenfor:

1. Åpne **Elektronisk rapportering**-arbeidsområdet, gå til konfigurasjonstreet og velg det elektroniske rapporteringsformatet **“SAF-T-format (NO)”**. 
2. Kontroller at selskapet du arbeider med, er selskapet du vil definere **Applikasjonsspesifikke parametere** for.
3. På Handling-panelet, i kategorien **Konfigurasjoner**, i gruppen **Programspesifikke parametere**, velg **Oppsett**.
4. Velg versjonen av formatet som du vil bruke på venstre side av siden **Applikasjonsspesifikke parametere**.
5. I **Oppslag**-hurtigfanen velger du **StandardMainAccount_Lookup** og spesifiserer deretter kriteriene på **Betingelser**-hurtigfanen ved å legge til linjer for hver **Resultat**-verdi som må brukes i det valgte selskapet. Hvis flere **Hovedkontoer** i det valgte selskapet må resultere i samme **Standardkonto**, legger du til en separat linje for hver **Hovedkonto** og spesifiserer samme **Standardkonto** for hver.
6. Velg verdien **Ikke aktuelt** som den siste betingelsen i listen. Den må være satt til **\*Ikke tom\*** i **Hovedkonto**-kolonnen. Verifiser verdien i **Linje**-kolonnen for at **"Ikke aktuelt"** er den siste betingelsen i tabellen.
7. Når du er ferdig med å sette opp betingelser, endrer du verdien i **Tilstand**-feltet til **Fullført**, lagrer endringene og lukker siden.

![Standardkonto-feltet på siden Hovedkontoer](media/nor-saf-standard-main-accounts-appsppar.jpg)

Du kan enkelt eksportere oppsettet av applikasjonsspesifikke parametere fra én versjon av en rapport og importere det til en annen versjon ved å velge **Eksporter** eller **Importer** i handlingsruten. Du kan også eksportere oppsettet fra én rapport og importere det til samme rapport i et annet selskap hvis hovedkontoene er de samme i begge selskapene.

## <a name="generate-the-norwegian-saf-t-financial-data-report"></a>Generer rapporten Norsk SAF-T økonomiske data

Hvis du vil generere rapporten **Norsk SAF-T økonomiske data**, følger du denne fremgangsmåten.

1. I Finance går du til **Økonomimodul** \> **Forespørsler og rapporter** \> **Standard revisjonsfil for avgift (SAF-T)** \> **Standard revisjonsfil for avgift (SAF-T)**.
2. Angi start- og sluttdatoene for perioden du vil generere rapporten for, i **Fra dato**- og **Til dato**-feltene i dialogboksen for rapporten.
3. Merk av for **Kunder**, **Leverandører** og **Finansdimensjoner** for å ta med alle postene fra de relaterte tabellene i rapporten.

    Hvis det ikke er merket av for **Kunder** og **Leverandører**, vil rapporten bare inkludere kunder og leverandører i firmaet som det var transaksjoner for i rapporteringsperioden, og kunder og leverandører som har en saldo som ikke er null.
    
    Hvis det ikke er merket av for **Finansdimensjoner**, vil bare finansdimensjonene som ble brukt i transaksjoner i løpet av rapporteringsperioden, rapporteres i **\<MasterFiles\>**-noden i rapporten.

4. I feltet **Personalnummer** velger du en ansatt for å legge til den ansatte i **\<AuditFileSender\>**-noden i rapporten. Denne noden rapporterer informasjon om kontaktpersonen for revisjonsfilen (fornavn og etternavn).

5. Merk av for **Rapporter skatteinformasjon i merverdiavgiftsvaluta** hvis du vil rapportere skatteinformasjon i merverdiavgiftsvaluta.

    Hvis det er merket av for **Rapporter skatteinformasjon i merverdiavgiftsvaluta**, rapporterer elementet **\<TaxInformation\>** følgende beløp i avgiftskodevalutaen:

    - *GeneralLedgerEntries/Journal/Transaction/Line/TaxInformation/TaxBase*
    - *GeneralLedgerEntries/Journal/Transaction/Line/TaxInformation/TaxAmount/Amount*


    Hvis det ikke er merket av for **Rapporter skatteinformasjon i merverdiavgiftsvaluta**, rapporteres beløpene i elementet **\<TaxInformation\>** og alle beløpene i rapportene i regnskapsvalutaen.

    Følgende beløp rapporteres alltid i dokumentvaluta:

    - *GeneralLedgerEntries/Journal/Transaction/Line/TaxInformation/TaxAmount/CurrencyAmount*

    Der *GeneralLedgerEntries/Journal/Transaction/Line/TaxInformation/TaxAmount/Currency* representerer dokumentvalutaen.

Du kan også bruke filtre for feltene **Hovedkontoer** og **Oppføring i økonomijournal** ved hjelp av hurtigfanen **Poster som skal inkluderes** i dialogboksen for rapporten.

## <a name="report-naming-and-splitting"></a>Navngivning og oppdeling av rapporter

Dokumentasjonen for norske SAF-T økonomiske data krever følgende navngivingsstruktur for XML-rapportene som genereres:

\<SAF-T export type\>\_\<organization number of the vendor that the data represents\>\_\<date and time(yyyymmddhh24hmise\>\_\<file number of total files\>.xml 

Her er et eksempel:

SAF-T Financial\_999999999\_20160401235911\_1\_12.xml

Her er en forklaring på delene av dette filnavnet:

- **SAF-T Financial** angir SAF-T-typen fil.
- **999999999** representerer organisasjonsnummeret som tilhører eieren av dataene.
- **20160401235911** representerer datoen og klokkeslettet da filen ble opprettet. (En 24-timers klokke brukes for klokkeslettet.)
- **1\_12** representerer fil 1 av 12 totalt antall filer i eksporten (det vil si i samme valg).

Volumet til en enkelt XML-fil må være mindre enn 2 gigabyte (GB). Hver enkelt XML-fil som sendes, må valideres mot skjemaet. Alle \<MasterFiles\>-noder må være i den første filen, og de tilknyttede transaksjonene må være i de påfølgende filene (antallet av disse filene er fleksibelt).

Tabellen nedenfor viser et eksempelutvalg av ett regnskapsår som har 12 perioder. For hver periode er det én fil som inneholder transaksjoner.

| Filnummer | Innhold i revisjonsfilen                     |
|-------------|------------------------------------------------|
| 1           | \<Header\>- og \<MasterFiles\>-noder           |
| 2–13        | \<Header\>- og \<GeneralLedgerEntries\>-noder  |

Det kan være maksimalt 10 XML-filer i samme zip-arkiv.

I samsvar med disse kravene er ER-formatet **SAF-T-format (NO)** implementert for å automatisk dele den resulterende rapporten i XML-format, basert på følgende forutsetninger:

- Det maksimale volumet for den resulterende XML-rapporten er 2 000 000 kilobyte (kB) (det vil si 2 GB).
- Alle XML-filene bruker følgende navngivningsstruktur:

    \<SAF-T export type\>\_\<organization number of the vendor that the data represents\>\_\<date and time(yyyymmddhh24hmise\>

- Alle XML-filer er inkludert i ett zip-arkiv.
- Hver enkelt XML-fil valideres mot skjemaet.

Når rapporten er generert, hvis det genereres mer enn én XML-fil, må brukeren manuelt nummerere de genererte filene i zip-arkivet ved å legge til **\_\<file number of total files\>** i filnavnene. Brukeren må likeledes sikre at det ikke mer enn 10 XML-filer i det samme zip-arkivet. Hvis det er mer enn 10 XML-filer i et arkiv, må brukeren manuelt dele det opp i flere arkiver, som hver har maksimalt 10 XML-filer.
