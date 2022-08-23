---
title: Mva-deklarering (Tyskland)
description: Denne artikkelen beskriver hvordan du definerer og genererer en mva-deklarering for forskudd for Tyskland i det offisielle XML-formatet.
author: AdamTrukawka
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 8ee288a1ec7ae950bdff9da7d373e29daef74d3c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9269412"
---
# <a name="vat-declaration-germany"></a>Mva-deklarering (Tyskland)

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du definerer og genererer en mva-deklarering for forskudd for Tyskland i det offisielle XML-formatet. Denne artikkelen beskriver også hvordan du forhåndsviser mva-deklareringen i Microsoft Excel.

Hvis du vil generere rapporten automatisk, oppretter du nok mva-koder til å beholde en egen mva-regnskap for hver boks i forskuddsvis mva-deklarering. I programspesifikke parametere i ER-formatet (Elektronisk rapportering) for forskuddsvis mva-deklarering knytter du dessuten mva-koder til oppslagsresultatet til oppslagene for boksene i mva-deklareringen.

For Tyskland må du konfigurere **rapportfeltoppslag**. Hvis du vil ha mer informasjon om hvordan du definerer programspesifikke parametere, kan du se delen [Definere programspesifikke parametere for mva-deklareringsfelt](#set-up-application-specific-parameters-for-vat-declaration-fields) senere i denne artikkelen.

Kolonnen "Oppslagsresultat" i tabellen nedenfor viser oppslagsresultatet som er forhåndskonfigurert for en bestemt mva-deklareringsrad i mva-deklareringsformatet. Bruk denne informasjonen til å knytte mva-koder til oppslagsresultatet på riktig måte, og deretter til raden i mva-deklareringen.

### <a name="vat-declaration-overview"></a><a name="vat-declaration-overview"></a>Oversikt over mva-deklarering

Mva-deklarering for forskudd i Tyskland inneholder følgende informasjon.

**DEL – LEVERINGER OG ANDRE TJENESTER**

**Avgiftspliktig salg**

| Rad | Boks – avgiftsgrunnlag | Boks – avgiftsbeløp | Beskrivelse                                                                                                                                      | Oppslagsresultat                                                                             |
|-----|----------------|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------|
| 20  | 81             | Uten kode     | Avgiftspliktig salg med en mva-sats på 19 prosent.                                                                                                       | 20-TaxableSalesStandard</br>73-BadDebtsWriteOffStandard (81/50) – med minustegn             |
| 21  | 86             | Uten kode     | Avgiftspliktig salg med en mva-sats på 7 prosent.                                                                                                        | 21-TaxableSalesReduced</br>73-BadDebtsWriteOffReduced (86/50) – med minustegn               |
| 22  | 35             | 36               | Avgiftspliktig salg til andre mva-satser.                                                                                                                | 22-TaxableSalesOtherRates</br>73-BadDebtsWriteOffOtherRates (35/36/50) – med minustegn      |
| 23  | 77             | *Intet avgiftsbeløp*  | Leveringer fra jordbruks- og skogdrift i henhold til § 24 i den tyske mva-loven (UStG) gjelder kunder som har mva-id-nummer. | 23-EUSalesAverageRate24</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50) – med minustegn |
| 24  | 76             | 80               | Salg som det må betales skatt for, i henhold til §24 i UStG (sagbruksprodukter, drikkvarer og alkoholholdige væsker).                                | 24-SalesAverageRate24</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50)                    |

**Avgiftsfrie salg med inngående avgiftsfradrag**

| Rad | Boks – avgiftsgrunnlag | Boks – avgiftsbeløp | Beskrivelse                                                                       | Oppslagsresultat                       |
|-----|----------------|------------------|-----------------------------------------------------------------------------------|-------------------------------------|
| 26  | 41             | *Intet avgiftsbeløp*  | Fellesskapsleveringer til kunder som har en mva-ID.                       | 26-EUSales                          |
| 27  | 44             | *Intet avgiftsbeløp*  | Fellesskapsleveringer av nye kjøretøy til kjøpere som ikke har mva-ID.    | 27-EUSalesNewVehicles               |
| 28  | 49             | *Intet avgiftsbeløp*  | Fellesskapsleveringer av nye kjøretøy utenfor et firma.                     | 28-EUSalesNewVehiclesOutsideCompany |
| 29  | 43             | *Intet avgiftsbeløp*  | Annet avgiftsfritt salg som har inngående skattefradrag, for eksempel eksportleveringer. | 29-ExportOtherTaxFreeSales          |

**Avgiftsfrie salg uten inngående avgiftsfradrag**

| Rad | Boks – avgiftsgrunnlag | Boks – avgiftsbeløp | Beskrivelse                                            | Oppslagsresultat                           |
|-----|----------------|------------------|--------------------------------------------------------|-----------------------------------------|
| 30  | 48             | *Intet avgiftsbeløp*  | Skattefritt salg som ikke har inngående skattefradrag. | 30-TaxFreeSalesWithoutInputTaxDeduction |

**Fellesskapsoppkjøp**

| Rad | Boks – avgiftsgrunnlag | Boks – avgiftsbeløp | Beskrivelse                                                                                                                   | Oppslagsresultat                                                    |
|-----|----------------|------------------|-------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| 33  | 91             | *Intet avgiftsbeløp*  | Skattefrie fellesskapsanskaffelse av noen objekter og investeringsgull.                                                    | 33-TaxFreeEUPurchase                                             |
| 34  | 89             | Uten kode     | Avgiftspliktige fellesskapsanskaffelse med en mva-sats på 19 prosent.                                                             | 34-EUPurchaseStandard</br>34-UseTaxEUPurchaseStandard (89/61)        |
| 35  | 93             | Uten kode     | Avgiftspliktige fellesskapsanskaffelse med en mva-sats på 7 prosent.                                                              | 35-EUPurchaseReduced</br>35-UseTaxEUPurchaseReduced (93/61)          |
| 36  | 95             | 98               | Avgiftspliktige fellesskapsanskaffelse med andre mva-satser.                                                                      | 36-EUPurchaseOtherRates</br>36-UseTaxEUPurchaseOtherRates (95/98/61) |
| 37  | 94             | 96               | Avgiftspliktige fellesskapsanskaffelse av nye kjøretøy fra leverandører som ikke har et MVA-ID-nummer, til den generelle avgiftssatsen. | 37-EUPurchaseVehicles</br>37-UseTaxEUPurchaseVehicles (94/96/61)     |

**DEL – MOTTAKER SOM SKATTEDEBITOR**

| Rad | Boks – avgiftsgrunnlag | Boks – avgiftsbeløp | Beskrivelse                                                                        | Oppslagsresultat                                                                                        |
|-----|----------------|------------------|------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 40  | 46             | 47               | Andre tjenester til en entreprenør, basert på resten av Fellesskapsområdet.        | 40-BeneficiaryTaxDebtor</br>40-UseTaxBeneficiaryTaxDebtor (46/47/66)                                                                              |
| 41  | 73             | 74               | Salg som faller under seksjon 13b (2) nr. 3 av UStG.                               | 41-BeneficiaryTaxDebtorRealEstateTransfer</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67) |
| 42  | 84             | 85               | Annet salg som faller under seksjon 13b (2) nr. 1, 2 og 4 til og med 12 av UStG. | 42-BeneficiaryTaxDebtorOther</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                           |

**DEL – TILLEGGSINFORMASJON OM SALG**

| Rad | Boks – avgiftsgrunnlag  | Boks – avgiftsbeløp | Beskrivelse                                                                                                | Oppslagsresultat                                                                                    |
|-----|-----------------|------------------|------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| 48  | 42              | *Intet avgiftsbeløp*  | Leveringer av den første kunden når det gjelder trekanttransaksjoner i fellesskapet.                   | 48-DeliveriesFirstCustomerEUTriangular                                                           |
| 49  | 60              | *Intet avgiftsbeløp*  | Avgiftspliktig salg av utførende entreprenør som mottakeren av tjenesten skylder mva i henhold til. | 49-SalesServicesReverseCharge                                                                    |
| 50  | 21              | *Intet avgiftsbeløp*  | Andre ikke-avgiftspliktige tjenester.                                                                                | 50-OtherServicesNonTaxable                                                                       |
| 51  | 45              | *Intet avgiftsbeløp*  | Annet ikke-avgiftspliktig salg når det aktuelle stedet ikke er i Tyskland.                                    | 51-OtherSalesNonTaxable                                                                          |
| 52  | *Intet avgiftsbeløp* | *Intet avgiftsbeløp*  | Mva.                                                                                                       | Rad 20 + Rad 21 + Rad 22 + Rad 24 + Rad 34 + Rad 35 + Rad 36 + Rad 37 + Rad 40 + Rad 41 + Rad 42 |

**DEL – FRADRAGSBERETTIGET INNGÅENDE AVGIFT**

| Rad | Boks – avgiftsbeløp | Beskrivelse                                                                                                | Oppslagsresultat                                                                                                                                                                |
|-----|------------------|------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 55  | 66               | Angi fakturaavgiftsbeløp fra andre firmaer, tjenester og triangulære transaksjoner innen fellesskap.     | 55-InputTax 40-UseTaxBeneficiaryTaxDebtor (46/47/66)</br>74-BadDebtsWriteOffInputTax (66/37) – med minustegn                                                                   |
| 56  | 61               | Inngående avgiftsbeløp fra fellesskapsoppkjøp av varer.                                           | 56-InputTaxEUPurchase 34-UseTaxEUPurchaseStandard (89/61)</br>35-UseTaxEUPurchaseReduced (93/61)</br>36-UseTaxEUPurchaseOtherRates (95/98/61)</br>37-UseTaxEUPurchaseVehicles (94/96/61) |
| 57  | 62               | Påløpt merverdiavgift for import.                                                                                 | 57-InputTaxImport                                                                                                                                                            |
| 58  | 67               | Avgiftsbeløp som angis fra tjenester som tilsvarer § 13b av UStG.                                        | 58-InputTaxServices</br>41-UseTaxBeneficiaryTaxDebtorRealEstateTransfer (73/74/67)</br>42-UseTaxBeneficiaryTaxDebtorOther (84/85/67)                                                 |
| 59  | 63               | Inngående avgiftsbeløp som beregnes i henhold til generelle gjennomsnittssatser.                                  | 59-InputTaxAverageRates</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37) – med minustegn                                                                                    |
| 60  | 59               | Inngående skattetrekk for fellesskapsleveranser av nye kjøretøy utenfor et firma og små bedrifter. | 60-InputTaxEUPurchaseNewVehicles</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37) – med minustegn                                                                  |
| 61  | 64               | Rettelse av det inngående avgiftstrekket.                                                                     | 61-InputTaxCorrection                                                                                                                                                        |
| 62  | \-               | Gjenstående beløp.                                                                                      | Rad 52 – Rad 55 – Rad 56 – Rad 57 – Rad 58 – Rad 50 – Rad 60 – Rad 61                                                                                                        |

**DEL – ANDRE MVA-BELØP**

| Rad | Boks – avgiftsbeløp | Beskrivelse                                                                                                                                                                                                                                                         | Oppslagsresultat                                 |
|-----|------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| 64  | 65               | Skatt på grunn av en endring i form av avgift og tilleggsavgift på beskattede betalinger på grunn av endring i avgiftssatsen.                                                                                                                                        | 64-AdditionalTaxDueChangeTaxRate              |
| 65  | 69               | Feil eller ujusterte mva-beløp som vises på fakturaer, og avgiftsbeløp som skyldes i henhold til seksjon 6a (4) setning 2, seksjon 17 (1) setning 7 eller seksjon 25b (2) i UStG, eller som skyldes et utsettingsfirma eller en lagerregistrerer. | 65-TaxDecreaseCorrection                      |
| 67  | 39               | Fratrekk av fast, spesiell forskuddsbetaling for permanent utvidelse. Denne raden fylles vanligvis ut med det siste forskuddsvarselet for mva-perioden.                                                                                                  | Brukerinndataparameter i rapportdialogboksen |
| 68  | 83               | Den gjenværende forskuddsbetalingen for merverdiavgift og gjenværende tillegg. Inkluder et minustegn foran beløpet.                                                                                                                                                          | Rad 62 + Rad 64 – Rad 65 – Rad 66             |

**DEL – TILLEGGSINFORMASJON OM REDUKSJONER**

| Rad | Boks – avgiftsgrunnlag | Boks – avgiftsbeløp | Beskrivelse                                                            | Oppslagsresultat                                                                                                                                                                                                    |
|-----|----------------|------------------|------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 73  | 50             | \-               | Reduksjon av avgiftsgrunnlaget på linje 20 til og med 24.                      | 73-BadDebtsWriteOffStandard (81/50)</br>73-BadDebtsWriteOffReduced (86/50)</br>73-BadDebtsWriteOffOtherRates (35/36/50)</br>73-BadDebtsWriteOffEUSalesAverageRate24 (77/50)</br>73-BadDebtsWriteOffSalesAverageRate24 (76/80/50) |
| 74  | \-             | 37               | Reduksjon av de fradragsberettigede inngående avgiftsbeløpene på linje 55, 59 og 60. | 74-BadDebtsWriteOffInputTax (66/37)</br>74-BadDebtsWriteOffInputTaxAverageRates (63/37)</br>74-BadDebtsWriteOffInputTaxEUPurchaseNewVehicles (59/37)                                                                     |

#### <a name="purchase-reverse-charge-vat"></a>Inngående mva, snudd avregning

Hvis du konfigurerer mva-koder til å postere innkommende merverdiavgift for snudd avregning ved hjelp av use tax, knytter du mva-kodene til **rapportfeltoppslaget** som inneholder "UseTax" i navnet.

Du kan også konfigurere to separate mva-koder: én for skyldig mva, og én for mva-fradrag. Deretter knytter du hver kode til de tilsvarende oppslagsresultatene for **rapportfeltoppslag**.

For avgiftspliktige fellesskapsanskaffeelser til en standardsats, konfigurerer du for eksempel **UT_S_EU** med use tax, og knytter den til **34-UseTaxEUPurchaseStandard**-oppslagsresultatet for **Rapportfeltoppslag**. I dette tilfellet gjenspeiles beløp som bruker avgiftskoden **UT_S_EU**, i boksene 089 og 061 (rad 34 og 56).

Du kan også konfigurere to mva-koder:

  - **VAT_S_EU**, som har en mva-satsverdi på -19 prosent
  - **InVAT_S_EU**, som har en mva-satsverdi på 19 prosent

Deretter knytter du kodene til oppslagsresultatene for **rapportfeltoppslag** slik:

  - Knytt **VAT_S_EU** med oppslagsresultatet **34-EUPurchaseStandard**.
  - Knytt **InVAT_S_EU** med oppslagsresultatet **56-InputTaxEUPurchase**.

I dette tilfellet gjenspeiles beløp som bruker avgiftskoden **UT_S_EU**, i boksen 089 (rad 34). Beløpene som bruker avgiftskoden **InVAT_S_EU**, i boksen 061 (rad 56).

Hvis du vil ha mer informasjon om hvordan du konfigurerer merverdiavgift for snudd avregning, kan du se [Snudde avregninger](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Konfigurere systemparametere

Hvis du vil generere en mva-deklarering, må du konfigurere avgiftsnummeret (Steuernummer) for organisasjonen.

1. Gå til **Organisasjonsstyring** > **Organisasjoner** > **Juridiske enheter**.
2. Velg den juridiske enheten, og velg deretter **Registrerings-ID-er**.
3. Velg eller opprett adressen i Tyskland, og velg deretter **Legg til** i hurtigfanen **Registrerings-ID**.
4. I **Registreringstype**-feltet velger du registreringstypen som er dedikert til Tyskland, og som bruker registreringskategorien **Foretaks-ID (COID)**.
5. Angi avgiftsnummeret i **Registreringsnummer**-feltet.
6. I **Generelt**-fanen i **Effektiv**-feltet angir du datoen når nummeret blir gjeldende.

Hvis du vil ha mer informasjon om hvordan du definerer registreringskategorier og registreringstyper, kan du se [Registrerings-ID-er](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-for-germany"></a>Konfigurere Mva-deklarering for Tyskland

### <a name="import-er-configurations"></a>Importere ER-konfigurasjoner

Åpne arbeidsområdet **Elektronisk rapportering**, og importer følgende versjoner eller senere av disse ER-formatene:

   - MVA-deklarering Excel (DE).version.101.16.12.xml
   - MVA-deklarering XML (DE).version.101.16.xml

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a>Definere programspesifikke parametere for mva-deklareringsfelt

Hvis du vil generere en mva-deklarering automatisk, knytter du mva-koder i programmet og oppslagsresultater i ER-konfigurasjonen.

> [!NOTE]
> Vi anbefaler at du aktiverer funksjonen, **Bruk programspesifikke parametere fra tidligere versjoner av ER-formater** i arbeidsområdet **Funksjonsbehandling**. Når denne funksjonen er aktivert, blir parametere som er konfigurert for den tidligere versjonen av et ER-format, automatisk gjeldende for den senere versjonen av samme format. Hvis denne funksjonen ikke er aktivert, må du konfigurere programspesifikke parametere eksplisitt for hver formatversjon. Funksjonen **Bruk programspesifikke parametere fra tidligere versjoner av ER-formater** er tilgjangelig i arbeidsområdet **Funksjonsbehandling** fra og med Finance-versjon 10.0.23. Hvis du vil ha mer informasjon om hvordan du definerer parameterne for et ER-format for hver juridiske enhet, kan du se [Definere parameterne for et ER-format per juridisk enhet](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Følg denne fremgangsmåten for å definere hvilke mva-koder som genererer hvilke bokser i mva-deklareringen.

1. Gå til **Arbeidsområder** > **Elektronisk rapportering**, og velg **Rapporteringskonfigurasjoner**.
2. Velg konfigurasjonen **VAT-deklarasjon XML (DE)**, og velg deretter **Konfigurasjoner \> Oppsett for programspesifikke parametere**.
3. På siden **Programspesifikke parametere** i hurtigfanen **Oppslag** velger du **Rapportfeltoppslag**.
4. I hurtigfanen **Betingelser** angir du følgende felt for å tilknytte mva-kodene og rapportfeltene.

    | Felt                  | Beskrivelse                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Oppslagsresultat          | Velg verdien for rapportfeltet. Hvis du vil ha mer informasjon om verdiene og tilordningen til mva-deklareringsrader, kan du se delen [Oversikt for mva-deklarering](#vat-declaration-overview) tidligere i denne artikkelen.                                                                                               |
    | Avgiftskode               | Velg avgiftskoden som skal knyttes til rapportfeltet. Posterte avgiftstransaksjoner som bruker den valgte avgiftskoden, blir samlet inn i den riktige deklareringsboksen. Vi anbefaler at du skiller avgiftskoder på en slik måte at én avgiftskode genererer beløp i bare én deklareringsboks. |
    | Transaksjonsklassifikator | Hvis du har opprettet nok mva-koder til å bestemme en deklareringsboks, velger du **\*Ikke tom\***. Hvis du ikke opprettet nok mva-koder slik at én mva-kode genererer beløp i bare én deklareringsboks, kan du definere en transaksjonsklassifikator. Følgende transaksjonsklassifikatorer er tilgjengelige:</br>-   **Kjøp**</br>-   **PurchaseExempt** (avgiftsfritt kjøp)</br>-   **PurchaseReverseCharge** (inngående merverdiavgift fra et innkjøp med snudd avskriving)</br>-   **Salg**</br>-   **SalesExempt** (avgiftsfritt salg)</br>-   **SalesReverseCharge** (skyldig mva fra snudd avregning for innkjøp eller snudd avregning for salg)</br>-   **Use tax**. </br>For hver transaksjonsklassifikator er også en klassifikator for kreditnotaen tilgjengelig. Én av disse klassifikatorene er for eksempel **PurchaseCreditNote** (innkjøpskreditnota).</br>Pass på at du oppretter to linjer for hver mva-kode: en som har transaksjonsklassifikatorverdien, og en som har transaksjonsklassifikatoren for kreditnotaverdi. |

    > [!NOTE]
    > Knytt alle mva-koder til oppslagsresultater. Hvis noen mva-koder ikke skal generere verdier i mva-deklareringen, knytter du dem til resultatet av **Annet**-oppslaget.

    ![Siden Programspesifikke parametere](media/69ecb881f12819259ca166b9b98b8303.jpg)

5. I **Tilstand**-feltet endrer du verdien til **Fullført**.
6. Velg **Eksporter** i handlingsruten for å eksportere innstillingene for de programspesifikke parameterne.
7. Velg konfigurasjonen **VAT-deklarering Excel (DE)**, og velg deretter **Importer** i handlingsruten for å importere parameterne du konfigurerte for **VAT-deklarering XML (DE)**.
8. Velg **Fullført** i **Status**-feltet.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Definere mva-rapporteringsformat for forhåndsvisningsbeløp i Excel

1. I arbeidsområdet **Funksjonsbehandling** finner og aktiverer du funksjonen **Rapporter i mva-oppgaveformat**.
2. Gå gil **Økonomimodul** > **Oppsett** > **Parametere for økonomimodul**.
3. Velg **Mva-deklarering Excel (DE)** i feltet **Tilordning av format for mva-oppgave** i hurtigfanen **Mva-alternativer** i fanen **Mva**.

   Dette formatet blir skrevet ut når du kjører rapporten **Rapporter merverdiavgift for utligningsperiode**. Den blir også skrevet ut når du velger **Skriv ut** på siden **Mva-betalinger**.

4. Velg skattemyndigheten på siden **Skattemyndigheter** og velg deretter **Standard** i feltet **Rapportoppsett**.

Følg denne fremgangsmåten hvis du konfigurerer mva-deklareringen i en juridisk enhet som har [flere mva-registreringer](emea-reporting-for-multiple-vat-registrations.md):

1. Gå gil **Økonomimodul** > **Oppsett** > **Parametere for økonomimodul**.
2. I kategorien **Mva** i hurtigfanen **Elektronisk rapportering for land/områder** i linjen for **DEU** velger du **Mva-deklarering Excel (DE)**-ER-format.

## <a name="set-up-electronic-messages"></a>Definere elektroniske meldinger

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Laste ned og importere datapakken som har eksempelinnstillinger for elektroniske meldinger

Datapakken inneholder innstillinger for elektroniske meldinger som brukes til å generere mva-deklareringen i XML-format, og forhåndsvise den i Excel. Du kan utvide disse innstillingene eller opprette dine egne. Hvis du vil ha mer informasjon om hvordan du arbeider med elektroniske meldinger og oppretter dine egne innstillinger, kan du se [Elektroniske meldinger](../general-ledger/electronic-messaging.md).

1. I [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2), i Delt aktivabibliotek, velger du **Datapakke** som ressurstype, og laster ned **DE mva-deklarering EM-pakken**. Filnavnet som lastes ned, er **DE VAT declaration EM package.zip**.
2. I Dynamics 365 Finance, i arbeidsområdet **Databehandling** velger du **Importer**.
3. Skriv inn en navn for jobben i hurtigfanen **Import** i feltet **Gruppenavn**.
4. På **Valgte enheter**-hurtigfanen velger du **Legg til fil**.
5. I dialogboksen **Legg til fil** kontrollerer du at feltet **Kildedataformat** er satt til **Pakke**, velger **Last opp og legg til**, og deretter velger du zipfilen du lastet ned tidligere.
6. Velg **Lukk**.
7. Når dataenhetene er lastet opp, velger du **Importer** i handlingsruten.
8. Gå til **Avgift** > **Forespørsler og rapporter** > **Elektroniske meldinger** > **Elektroniske meldinger**, og valider den elektroniske meldingsbehandlingen du importerte.

### <a name="configure-electronic-messages"></a>Konfigurere elektroniske meldinger

1. Gå til **Mva** > **Oppsett** > **Elektroniske meldinger** > **Handlinger for Fyll ut poster**.
2. Velg linjen for **DE Fyll ut mva-returposter**, og velg deretter **Rediger spørring**.
3. Bruk filteret til å angi utligningsperiodene som skal tas med i rapporten.
4. Hvis du må rapportere avgiftstransaksjoner fra andre utligningsperioder i en annen deklarering, oppretter du en ny **Fyll ut poster**-handling og velger de riktige utligningsperiodene.

## <a name="preview-the-vat-declaration-in-excel"></a>Forhåndsvise mva-deklareringen i Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a>Forhåndsvise mva-deklareringen i Excel fra oppgaven Rapportere merverdiavgift for en utligningsperiode

1. Gå til **Avgift** > **Periodiske oppgaver** > **Deklareringer** > **Merverdiavgift** > **Rapportere merverdiavgift for en utligningsperiode**.
2. Angi en verdi i feltet **Utligningsperiode**.
3. I feltet **Mva-betalingsversjon** velger du en av følgende verdier:

    - **Original**: Generer en rapport for mva-transaksjoner for den opprinnelige mva-betalingen eller før mva-betalingen genereres.
    - **Rettelser**: Generer en rapport for mva-transaksjonene for alle de etterfølgende mva-betalingene for perioden.
    - **Total liste**: Generer en rapport for alle mva-transaksjoner for perioden, inkludert den opprinnelige og alle rettelsene.

4. Velg startdatoen for rapporteringsperioden i **Fra dato**-feltet.
5. Velg **OK**, og se over Excel-rapporten.

### <a name="settle-and-post-sales-tax"></a><a name="settle-and-post-sales-tax"></a>Utlign og poster merverdiavgift

1. Gå til **Avgift** > **Periodiske oppgaver** > **Deklareringer** > **Merverdiavgift** > **Utlign og poster merverdiavgift**.
2. Angi en verdi i feltet **Utligningsperiode**.
3. I feltet **Mva-betalingsversjon** velger du en av følgende verdier:

    - **Original**: Generer den opprinnelige mva-betalingen for utligningsperioden.
    - **Siste rettelser**: Generer en rettelse av mva-betaling etter at den opprinnelige mva-betalingen for utligningsperioden ble opprettet.

4. Velg startdatoen for rapporteringsperioden i **Fra dato**-feltet.
5. Velg **OK**.

### <a name="preview-the-vat-declaration-in-excel-from-a-sales-tax-payment"></a>Forhåndsvis mva-deklareringen i Excel fra en mva-betaling

1. Gå til **Avgift** > **Forespørsler og rapporter** > **Merverdiavgiftforespørsler** > **Mva-betalinger**, og velg en betalingslinje for merverdiavgift.
2. Velg **Skriv ut rapport**, og velg deretter **OK**.
3. Gå gjennom Excel-filen som er generert for den valgte mva-betalingslinjen.

    > [!NOTE]
    > Denne rapporten genereres bare for den valgte mva-betalingslinjen. Hvis du for eksempel vil generere en korrigerende deklarering som inneholder alle rettelsene for perioden, eller en erstatningsdeklarering som inneholder de opprinnelige dataene og alle rettelsene, bruker du rapporten **Rapporter merverdiavgift for utligningsperioden**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Generere en mva-deklarering fra elektroniske meldinger

Når du bruker elektroniske meldinger til å generere rapporten, kan du samle inn avgiftsdata fra flere juridiske enheter. Hvis du vil ha mer informasjon, kan du se delen [Kjøre en mva-deklarering for flere juridiske enheter](#run-a-vat-declaration-for-multiple-legal-entities) senere i denne artikkelen.

Følgende fremgangsmåte gjelder for eksempel for behandling av elektroniske meldinger som du importerte fra LCS delt aktivabibliotek.

1. Gå til **Mva** > **Forespørsler og rapporter** > **Elektroniske meldinger** > **Elektroniske meldinger**.
2. Velg **DE-mva-deklarering** i den venstre ruten.
3. I hurtigfanen **Meldinger** velger du **Ny**, og deretter, i dialogboksen **Kjør behandling**, velger du **OK**.
4. Velg meldingslinjen som er opprettet, skriv inn en beskrivelse, og angi deretter start- og sluttdatoene for deklareringen.

    > [!NOTE]
    > Trinn 5 til og med 7 er valgfrie.

5. Valgfritt: I hurtigfanen **Meldinger** velger du **Samle inn data**, og deretter velger du **OK**. Mva-betalingene som ble generert tidligere, blir lagt til i meldingen. Hvis du vil ha mer informasjon, kan du se delen [Utlign og poster merverdiavgift](#settle-and-post-sales-tax) tidligere i denne artikkelen. Hvis du hopper over dette trinnet, kan du likevel generere en mva-deklarering ved å bruke feltet **Avgiftsdeklareringsversjon** i dialogboksen **Deklarering**.
6. Valgfritt: Gå gjennom mva-betalingene som er overført for behandling, i hurtigfanen **Meldingselementer**. Alle mva-betalinger for den valgte perioden som ikke var inkludert i andre meldinger av samme behandling, er som standard inkludert.
7. Valgfritt: Velg **Opprinnelig dokument** for å gå gjennom mva-betalingene, eller velg **Slett** for å utelate mva-betalinger fra behandling. Hvis du hopper over dette trinnet, kan du likevel generere en mva-deklarering ved å bruke feltet **Avgiftsdeklareringsversjon** i dialogboksen **Deklarering**.
8. På hurtigfanen **Meldinger** velger du **Oppdater status**. I dialogboksen **Oppdater status** velger du **Klar til å generere**, og deretter velger du **OK**. Kontroller at meldingens status er endret til **Klar til å generere**.
9. Velg **Generer rapport**. Hvis du vil forhåndsvise mva-deklareringsbeløpene, velger du **Forhåndsvis rapport** i dialogboksen **Kjør behandling** og velger deretter **OK**.
10. I dialogboksen **Parametere for elektronisk rapportering** angir du følgende felt og velger **OK**.

    | **Felt**                                   | **Beskrivelse**                                                                                                                                                                                                              |
    |---------------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Utligningsperiode                           | Velg utligningsperioden. Hvis du valgte **Samle inn data** i trinn 5, kan du la dette feltet stå tomt. Rapporten genereres for mva-transaksjoner som er inkludert i de innsamlede mva-betalingene. |
    | Avgiftsdeklareringsversjon                     | Velg én av følgende verdier:</br>-   **Original** – Generer en rapport for mva-transaksjoner for den opprinnelige mva-betalingen eller før mva-betalingen genereres.</br>-   **Rettelser** – Generer en rapport for mva-transaksjonene for alle de etterfølgende mva-betalingene for perioden.</br>-   **Total liste** – Generer en rapport for alle mva-transaksjoner for perioden, inkludert den opprinnelige og alle rettelsene.|
    | Avgiftsrepresentant | Velg parten som er skatterepresentant for mva-deklarering, om nødvendig. Informasjon om den valgte parten eksporteres til XML-elementet **DatenLieferant**. |
    | Kontaktperson | Velg en person i organisasjonen som er dataleverandør. Informasjon om den valgte personen eksporteres til XML-elementet **DatenLieferant**. |
    | Korrigerende retur | Velg **Ja** hvis dette er korrigerende mva-deklarering. I dette tilfellet vil XML-elementet KZ10 ha verdien **1**.|
    | Støttedokumenter | Velg **Ja** hvis du også sender støttedokumenter. I dette tilfellet vil XML-elementet KZ22 ha verdien **1**.|
    | Mandatet for SEPA-avtalegiro blir opphevet som et unntak| Velg **Ja** hvis obligatorisk for SEPA-avtalegiro skal oppheves som et unntak for denne forhåndsregistreringsperioden. For eksempel på grunn av å motpostere forespørsler. Eventuell gjenstående saldo skal betales separat. I dette tilfellet vil XML-elementet KZ26 ha verdien **1**. |
    | Motpostering av det ønskede refusjonsbeløpet | Velg **Ja** hvis du vil motpostere refusjonsbeløpet, eller hvis refusjonsbeløpet er tilordnet. I dette tilfellet vil XML-elementet KZ29 ha verdien **1**. |
    | Permanent utvidelse for spesialforskudd | Angi fratrekksbeløpet for den faste forskuddsbetaling for permanent utvidelse. Dette fratrekksbeløpet fullføres vanligvis bare i den siste forhåndsregistreringen av skatteperioden. Beløpet eksporteres i rad 67 (boks 39) og XML-element KZ39 i mva-deklareringen. |

11. Velg **Vedlegg** øverst til høyre på siden, og velg deretter **Åpne**.
12. Gå gjennom beløpene i Excel-dokumentet, og velg deretter **Generer rapport**.
13. Hvis du vil generere en mva-deklarering i XML-format, velger du **Generer rapport** i dialogboksen **Kjør behandling** og velger deretter **OK**.
14. I dialogboksen **Parametere for elektronisk rapportering** definerer du feltene slik som beskrevet i trinn 10.
15. Velg **Vedlegg** i øverste høyre hjørne på siden, last ned filen og bruk den til innsendingen til skattemyndighetene.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-a-vat-declaration-for-multiple-legal-entities"></a>Kjøre en mva-deklarering for flere juridiske enheter

Hvis du vil bruke formatene til å rapportere mva-deklareringen for en gruppe juridiske enheter, må du først definere programspesifikke parametere for ER-formatene for mva-koder fra alle nødvendige juridiske enheter.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Definere elektroniske meldinger for å samle inn avgiftsdata fra flere juridiske enheter

Følg denne fremgangsmåten for å definere elektroniske meldinger som samler inn data fra flere juridiske enheter.

1. Gå til **Arbeidsområder** > **Funksjonsbehandling**.
2. Søk etter og velg funksjonen **Spørringer på tvers av firmaer for Handlinger for fyll ut poster** i listen, og velg deretter **Aktiver nå**.
3. Gå til **Mva** > **Oppsett** > **Elektroniske meldinger \> Handlinger for Fyll ut poster**.
4. På siden **Handlinger for Fyll ut poster** merker du linjen for **DE Fylle ut mva-returposter**.

   I **Oppsett av datakilder**-rutenettet er et nytt **Firma** tilgjengelig. For eksisterende poster viser dette feltet IDen til den gjeldende juridiske enheten.

5. I rutenettet **Oppsett av datakilder** legger du til en linje for hver ekstra juridiske enhet som må inkluderes i rapportering. For hver nye linje angir du feltene nedenfor.

    | Felt                  | Beskrivelse                                                                                                                   |
    |------------------------|-------------------------------------------------------------------------------------------------------------------------------|
    | Navn                   | Angi en verdi som vil hjelpe deg med å forstå hvor denne posten kommer fra. Du kan for eksempel angi **Mva-betaling for datterselskap 1**. |
    | Type meldingselement      | Velg **Mva-retur**. Denne verdien er den eneste verdien som er tilgjengelig for alle postene.                                    |
    | Kontotype           | Velg **Alle**.                                                                                                               |
    | Navn på hovedtabell      | Angi **TaxReportVoucher** for alle postene.                                                                             |
    | Feltet Dokumentnummer  | Angi **Bilag** for alle postene.                                                                                      |
    | Feltet Dokumentdato    | Angi **TransDate** for alle postene.                                                                                    |
    | Feltet Dokumentkonto | Angi **TaxPeriod** for alle postene.                                                                                    |
    | Selskap                | Velg IDen for den juridiske enheten.                                                                                            |
    | Brukerspørring             | Denne boksen blir automatisk merket når du definerer kriterier ved å velge **Rediger spørring**.                                 |

6. For hver nye linje velger du **Rediger spørring** og angir en tilknyttet utligningsperiode for den juridiske enheten som er angitt i **Firma**-feltet i linjen.

Når oppsettet er fullført, vil funksjonen **Samle inn data** på siden **Elektroniske meldinger** samle inn mva-betalinger fra alle juridiske enheter som du har definert.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
