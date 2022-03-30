---
title: Mva-deklarering (Danmark)
description: Dette emnet beskriver hvordan du definerer og genererer en mva-deklarering for forskudd for Danmark.
author: anasyash
ms.date: 03/10/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: ''
ms.openlocfilehash: 4d4a1185fa3c3b059744018b6e4e195de07126c9
ms.sourcegitcommit: 9c19898e1f41495f804c7f07e2636b53a098c4c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/10/2022
ms.locfileid: "8402986"
---
# <a name="vat-declaration-denmark"></a>Mva-deklarering (Danmark)

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du definerer mva-deklareringen for Danmark og forhåndsviser den i Microsoft Excel.

Hvis du vil generere rapporten automatisk, oppretter du først nok mva-koder til å beholde en egen mva-regnskap for hver boks i forskuddsvis mva-deklarering. I programspesifikke parametere i ER-formatet (Elektronisk rapportering) for forskuddsvis mva-deklarering knytter du dessuten mva-koder til oppslagsresultatet til oppslagene for boksene i mva-deklareringen.

For Danmark må du konfigurere **rapportfeltoppslag**. Hvis du vil ha mer informasjon om hvordan du definerer programspesifikke parametere, kan du se delen [Definere programspesifikke parametere for mva-deklareringsfelt](#set-up-application-specific-parameters) senere i dette emnet.

Kolonnen "Oppslagsresultat" i tabellen nedenfor viser oppslagsresultatet som er forhåndskonfigurert for en bestemt mva-deklareringsrad i mva-deklareringsformatet. Bruk denne informasjonen til å knytte mva-koder til oppslagsresultatet på riktig måte, og deretter til raden i mva-deklareringen.

### <a name="vat-declaration-overview"></a>Oversikt over mva-deklarering

Mva-deklareringen i Danmark inneholder følgende informasjon.

**VAT skyldig**

| Beskrivelse                                                  | Avgiftsgrunnlag/Avgiftsbeløp | Oppslagsresultat/Total                                                                                                                                                                                                                                                                                                                          |
|--------------------------------------------------------------|---------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Utgående mva.                                                   | Avgiftsbeløp          | **OutputVAT**</br> **DomesticVATUseTax** (også rapportert i boksen "Inngående mva")                                                                                                                                                                                                                                                                       |
| Mva på varer osv. kjøpt i utlandet                           | Avgiftsbeløp          | **PurchaseGoodsAbroad**</br>**PurchaseGoodsAbroadUseTax** (også rapportert i boksen "Inngående mva")</br>**PurchaseGoodsEU** (Avgiftsgrunnlaget rapporteres i "Boks A - anskaffelse av varer".)</br>**PurchaseGoodsEUUseTax** (Avgiftsbeløpet rapporteres i boksen "Inngående mva". Avgiftsgrunnlaget rapporteres i "Boks A - anskaffelse av varer".)                   |
| Mva. på tjenester kjøpt utenlands underlagt snudd avregning | Avgiftsbeløp          | **PurchaseServicesAbroad**</br> **PurchaseServicesAbroadUseTax** (også rapportert i boksen "Inngående mva")</br>**PurchaseServicesEU** (Avgiftsgrunnlaget rapporteres i "Boks A - anskaffelse av tjenester".)</br>**PurchaseServicesEUUseTax** (Avgiftsbeløpet rapporteres i boksen "Inngående mva". Avgiftsgrunnlaget rapporteres i "Boks A - anskaffelse av tjenester".) |
| Skyldig totalt                                                | Avgiftsbeløp          | Totalsummen av de tre forrige boksene                                                                                                                                                                                                                                                                                                            |

**Fradrag**

| Beskrivelse                                                                               | Avgiftsgrunnlag/Avgiftsbeløp | Oppslagsresultat/Total                                                                                                                                                                                                                                                                                                                                                                                                                                                                                              |
|-------------------------------------------------------------------------------------------|---------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Inngående mva.                                                                                 | Avgiftsbeløp          | **InputVAT**</br> **DomesticVATUseTax** (også rapportert i boksen "Utgående mva")</br>**PurchaseGoodsAbroadUseTax** (også rapportert i boksen "Mva på varer osv. kjøpt i utlandet")</br>**PurchaseServicesAbroadUseTax** (også rapportert i boksen "Mva for tjenester kjøpt i utlandet underlagt snudd avregning")</br>**PurchaseGoodsEUUseTax** (også rapportert i boksen "Mva på varer osv. kjøpt i utlandet")</br> **PurchaseServicesEUUseTax** (også rapportert i boksen "Mva for tjenester kjøpt i utlandet underlagt snudd avregning") |
| Olje- og gassflaskeavgift                                                                  | Avgiftsbeløp          | **OilGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| Naturgass- og byforurensningsavgift                                                             | Avgiftsbeløp          | **NaturalTownGasDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                           |
| Karbonavgift                                                                               | Avgiftsbeløp          | **CarbonDuty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                   |
| CO2Duty                                                                                   | Avgiftsbeløp          | **CO2Duty**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                      |
| Vannavgift                                                                              | Avgiftsbeløp          | **WaterCharge**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Fradrag totalt                                                                          | Avgiftsbeløp          | Totalsummen av de seks forrige boksene                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
| Totalbeløp for avgifter (positivt beløp = foreta betaling, negativt beløp = motta refundering) | Avgiftsbeløp          | "Skyldig totalt" – "Totale fradrag"                                                                                                                                                                                                                                                                                                                                                                                                                                                                                 |

**Tilleggsinformasjon**

| Beskrivelse                                                                                                                                                                                                                                | Avgiftsgrunnlag/Avgiftsbeløp | Oppslagsresultat/Total                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------|-------------------------------------------------|
| Boks A - anskaffelse av varer. Verdien uten mva for anskaffelse av varer internt i unionen.                                                                                                                                                   | Grunnlag            | **PurchaseGoodsEU PurchaseGoodsEUUseTax**       |
| Boks A - anskaffelse av tjenester. Verdien uten mva for anskaffelse av tjenester internt i unionen.                                                                                                                                             | Grunnlag            | **PurchaseServicesEU PurchaseServicesEUUseTax** |
| Boks B – forsyning av varer – som skal rapporteres til "EU-salg uten mva"/DK VIES. Verdien uten mva for forsyning av varer internt i unionen                                                                                                           | Grunnlag            | **SalesGoodsEU**                                |
| Boks B – forsyninger – som ikke skal rapporteres til "EU-salg uten mva"/DK VIES. Verdien uten mva for bestemte forsyninger internt i unionen, for eksempel installasjon, montering, fjernsalg og nye transportmåter til personer som ikke er avgiftspliktige. | Grunnlag            | **SalesInstallationAssemblyEtcEU**              |
| Boks B - forsyning av tjenester. Verdien uten mva for forsyning av tjenester innen unionen som kjøperen er ansvarlig for å betale merverdiavgift som snudd avregning for, må også rapporteres til "EU-salg uten mva"/DK VIES.                          | Grunnlag            | **SalesServicesEU**                             |
| Boks C - andre forsyninger. Verdien av forsyning av andre varer og tjenester som leveres uten mva i Danmark, til andre EU-medlemsland og til tredjeland eller tredjeterritorier.                                     | Grunnlag            | **OtherSuppliesWithoutVAT**                     |

#### <a name="purchase-reverse-charge-vat"></a>Inngående mva, snudd avregning

Hvis du konfigurerer mva-koder til å postere innkommende merverdiavgift for snudd avregning ved hjelp av use tax, knytter du mva-kodene til **rapportfeltoppslaget** som inneholder "UseTax" i navnet.

Du kan også konfigurere to separate mva-koder: én for skyldig mva, og én for mva-fradrag. Deretter knytter du hver kode til de tilsvarende oppslagsresultatene for **rapportfeltoppslag**.

For avgiftspliktige fellesskapsanskaffeelser konfigurerer du for eksempel **UT_S_EU** med use tax, og knytter den til **PurchaseGoodsEUUseTax**-oppslagsresultatet for **Rapportfeltoppslag**. I dette tilfellet gjenspeiles avgiftsbeløp som bruker avgiftskoden **UT_S_EU**, i boksene "Mva på varer osv. kjøpt i utlandet" og "Inngående mva". Avgiftsgrunnlagene gjenspeiles i "Boks A - anskaffelse av varer".

Du kan også konfigurere to mva-koder:

- **VAT_S_EU**, som har en mva-satsverdi på -25 prosent
- **InVAT_S_EU**, som har en mva-satsverdi på 25 prosent

Deretter knytter du kodene til oppslagsresultatene for **rapportfeltoppslag** slik:

- Knytt **VAT_S_EU** med oppslagsresultatet **PurchaseGoodsEU**.
- Knytt **InVAT_S_EU** med oppslagsresultatet **InputVAT**.

I dette tilfellet gjenspeiles beløp som bruker avgiftskoden **VAT_S_EU**, i boksen "Mva på varer osv. kjøpt i utlandet" og "Boks A - anskaffelse av varer." Beløpene som bruker avgiftskoden **InVAT_S_EU**, i boksen "Inngående mva".

Hvis du vil ha mer informasjon om hvordan du konfigurerer merverdiavgift for snudd avregning, kan du se [Snudde avregninger](emea-reverse-charge.md).

## <a name="configure-system-parameters"></a>Konfigurere systemparametere

Hvis du vil generere en mva-deklarering, må du konfigurere mva-nummeret.

1. Gå til **Organisasjonsstyring** > **Organisasjoner** > **Juridiske enheter**.
2. Velg den juridiske enheten, og velg deretter **Registrerings-ID-er**.
3. Velg eller opprett adressen i Danmark, og velg deretter **Legg til** i hurtigfanen **Registrerings-ID**.
4. I **Registreringstype**-feltet velger du registreringstypen som er dedikert til Danmark, og som bruker registreringskategorien **Mva-ID**.
5. Angi avgiftsnummeret i **Registreringsnummer**-feltet.
6. I **Generelt**-fanen i **Effektiv**-feltet angir du datoen når nummeret blir gjeldende.

Hvis du vil ha mer informasjon om hvordan du definerer registreringskategorier og registreringstyper, kan du se [Registrerings-ID-er](emea-registration-ids.md).

## <a name="set-up-a-vat-declaration-preview-for-denmark"></a>Konfigurer en forhåndsvisning av mva-deklarering for Danmark

### <a name="import-er-configurations"></a>Importere ER-konfigurasjoner

Åpne arbeidsområdet **Elektronisk rapportering**, og importer ER-formatet **Mva-deklarasjon Excel (DK)**.

For mer informasjon, se [Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

### <a name="set-up-application-specific-parameters-for-vat-declaration-fields"></a><a name="set-up-application-specific-parameters"></a>Definere programspesifikke parametere for mva-deklareringsfelt

> [!NOTE]
> Vi anbefaler at du aktiverer funksjonen, **Bruk programspesifikke parametere fra tidligere versjoner av ER-formater** i arbeidsområdet **Funksjonsbehandling**. Når denne funksjonen er aktivert, blir parametere som er konfigurert for den tidligere versjonen av et ER-format, automatisk gjeldende for den senere versjonen av samme format. Hvis denne funksjonen ikke er aktivert, må du konfigurere programspesifikke parametere uttrykkelig for hver formatversjon. Funksjonen **Bruk programspesifikke parametere fra tidligere versjoner av ER-formater** er tilgjangelig i arbeidsområdet **Funksjonsbehandling** fra og med Finance-versjon 10.0.23. Hvis du vil ha mer informasjon om hvordan du definerer parameterne for et ER-format for hver juridiske enhet, kan du se [Definere parameterne for et ER-format per juridisk enhet](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Hvis du vil generere en mva-deklarering automatisk, knytter du mva-koder i programmet og oppslagsresultater i ER-konfigurasjonen.

Følg denne fremgangsmåten for å definere hvilke mva-koder som genererer hvilke bokser i mva-deklareringen.

1. Gå til **Arbeidsområder** > **Elektronisk rapportering**, og velg **Rapporteringskonfigurasjoner**.
2. Velg konfigurasjonen **Mva-deklarasjon Excel (DK)**, og velg deretter **Konfigurasjoner \> Oppsett for programspesifikke parametere**.
3. På siden **Programspesifikke parametere** i hurtigfanen **Oppslag** velger du **Rapportfeltoppslag**.
4. I hurtigfanen **Betingelser** angir du følgende felt for å tilknytte mva-kodene og rapportfeltene.

    | Felt                  | Beskrivelse                                                                                                                                                                                                                                                                                                          |
    |------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
    | Oppslagsresultat          | Velg verdien for rapportfeltet. Hvis du vil ha mer informasjon om verdiene og tilordningen til mva-deklareringsrader, kan du se delen [Oversikt for mva-deklarering](#vat-declaration-overview) tidligere i dette emnet.                                                                                               |
    | Avgiftskode               | Velg avgiftskoden som skal knyttes til rapportfeltet. Posterte avgiftstransaksjoner som bruker den valgte avgiftskoden, blir samlet inn i den riktige deklareringsboksen. Vi anbefaler at du skiller avgiftskoder på en slik måte at én avgiftskode genererer beløp i bare én deklareringsboks. |
    | Transaksjonsklassifikator | Hvis du har opprettet nok mva-koder til å bestemme en deklareringsboks, velger du **\*Ikke tom\***. Hvis du ikke opprettet nok mva-koder slik at én mva-kode genererer beløp i bare én deklareringsboks, kan du definere en transaksjonsklassifikator. Følgende transaksjonsklassifikatorer er tilgjengelige:</br>-   **Kjøp**</br>-   **PurchaseExempt** (avgiftsfritt kjøp)</br>-   **PurchaseReverseCharge** (inngående merverdiavgift fra et innkjøp med snudd avskriving)</br>-   **Salg**</br>-   **SalesExempt** (avgiftsfritt salg)</br>-   **SalesReverseCharge** (skyldig mva fra snudd avregning for innkjøp eller snudd avregning for salg)</br>-   **Use tax**. </br>For hver transaksjonsklassifikator er også en klassifikator for kreditnotaen tilgjengelig. Én av disse klassifikatorene er for eksempel **PurchaseCreditNote** (innkjøpskreditnota).</br>Pass på at du oppretter to linjer for hver mva-kode: en som har transaksjonsklassifikatorverdien, og en som har transaksjonsklassifikatoren for kreditnotaverdi. |


    > [!NOTE]
    > Knytt alle mva-koder til oppslagsresultater. Hvis noen mva-koder ikke skal generere verdier i mva-deklareringen, knytter du dem til resultatet av **Annet**-oppslaget.

    ![Siden Programspesifikke parametere.](media/7db74920fad66a0db7fad60758698cc0.png)


5. I **Tilstand**-feltet endrer du verdien til **Fullført**.

### <a name="set-up-the-vat-reporting-format-for-preview-amounts-in-excel"></a>Definere mva-rapporteringsformat for forhåndsvisningsbeløp i Excel

1. I arbeidsområdet **Funksjonsbehandling** finner og velger du funksjonen **Rapporter i mva-oppgaveformat** i listen og velger deretter **Aktiver nå**.
2. Gå gil **Økonomimodul** > **Oppsett** > **Parametere for økonomimodul**.
3. Velg ER-formatet **Mva-deklarering Excel (DK)** i feltet **Tilordning av format for mva-oppgave** i hurtigfanen **Mva-alternativer** i fanen **Mva**.

   Dette formatet blir skrevet ut når du kjører rapporten **Rapporter merverdiavgift for utligningsperiode**. Den blir også skrevet ut når du velger **Skriv ut** på siden **Mva-betalinger**.

4. Velg skattemyndigheten på siden **Skattemyndigheter** og velg deretter **Standard** i feltet **Rapportoppsett**.

Følg denne fremgangsmåten hvis du konfigurerer mva-deklareringen i en juridisk enhet som har [flere mva-registreringer](emea-reporting-for-multiple-vat-registrations.md).

1. Gå til **Økonomimodul** \> **Oppsett** \> **Parametere for økonomimodul**.
2. I kategorien **Mva** i hurtigfanen **Elektronisk rapportering for land/områder** i linjen for **DNK** velger du ER-formatet **Mva-deklarering Excel (DK)**.

## <a name="set-up-electronic-messages"></a>Definere elektroniske meldinger

### <a name="download-and-import-the-data-package-that-has-example-settings-for-electronic-messages"></a>Laste ned og importere datapakken som har eksempelinnstillinger for elektroniske meldinger

Datapakken inneholder innstillinger for elektroniske meldinger som brukes til å forhåndsvise mva-deklareringen i Excel. Du kan utvide disse innstillingene eller opprette dine egne. Hvis du vil ha mer informasjon om hvordan du arbeider med elektroniske meldinger og oppretter dine egne innstillinger, kan du se [Elektroniske meldinger](../general-ledger/electronic-messaging.md).

1. I [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/v2), i Delt aktivabibliotek, velger du **Datapakke** som ressurstype, og laster ned **pakken DK mva-deklarering**. Navnet på den nedlastede filen er **DK VAT declaration package.zip**.
2. I Finance, i arbeidsområdet **Databehandling** velger du **Importer**.
3. Skriv inn en navn for jobben i hurtigfanen **Import** i feltet **Gruppenavn**.
4. På **Valgte enheter**-hurtigfanen velger du **Legg til fil**.
5. I dialogboksen **Legg til fil** kontrollerer du at feltet **Kildedataformat** er satt til **Pakke**, velger **Last opp og legg til**, og deretter velger du zipfilen du lastet ned tidligere.
6. Velg **Lukk**.
7. Når dataenhetene er lastet opp, velger du **Importer** i handlingsruten.
8. Gå til **Avgift** > **Forespørsler og rapporter** > **Elektroniske meldinger** > **Elektroniske meldinger**, og valider den elektroniske meldingsbehandlingen du importerte (**DK mva-erklæring**).

### <a name="configure-electronic-messages"></a>Konfigurere elektroniske meldinger

1. Gå til **Mva** > **Oppsett** > **Elektroniske meldinger** > **Handlinger for Fyll ut poster**.
2. Velg linjen for **DK Fyll ut mva-returposter**, og velg deretter **Rediger spørring**.
3. Bruk filteret til å angi utligningsperiodene som skal tas med i rapporten.
4. Hvis du må rapportere avgiftstransaksjoner fra andre utligningsperioder i en annen deklarering, oppretter du en ny **Fyll ut poster**-handling og velger de riktige utligningsperiodene.

## <a name="preview-the-vat-declaration-in-excel"></a>Forhåndsvise mva-deklareringen i Excel

### <a name="preview-the-vat-declaration-in-excel-from-the-report-sales-tax-for-settlement-period-periodic-task"></a><a name="preview-vat-excel"></a>Forhåndsvise mva-deklareringen i Excel fra oppgaven Rapportere merverdiavgift for en utligningsperiode

1. Gå til **Avgift** > **Periodiske oppgaver** > **Deklareringer** > **Merverdiavgift** > **Rapportere merverdiavgift for en utligningsperiode**.
2. Angi en verdi i feltet **Utligningsperiode**.
3. I feltet **Mva-betalingsversjon** velger du en av følgende verdier:

    - **Original**: Generer en rapport for mva-transaksjoner for den opprinnelige mva-betalingen eller før mva-betalingen genereres.
    - **Rettelser**: Generer en rapport for mva-transaksjonene for alle de etterfølgende mva-betalingene for perioden.
    - **Total liste**: Generer en rapport for alle mva-transaksjoner for perioden, inkludert den opprinnelige og alle rettelsene.

4. Velg startdatoen for rapporteringsperioden i **Fra dato**-feltet.
5. Velg **OK**, og se over Excel-rapporten.

### <a name="settle-and-post-sales-tax"></a>Utlign og poster merverdiavgift

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
> Denne rapporten genereres bare for den valgte mva-betalingslinjen. Hvis du for eksempel må generere en korrigerende deklarering som inneholder alle rettelsene for perioden, eller en erstatningsdeklarering som inneholder de opprinnelige dataene og alle rettelsene, bruker du rapporten **Rapporter merverdiavgift for utligningsperioden**.

## <a name="generate-a-vat-declaration-from-electronic-messages"></a>Generere en mva-deklarering fra elektroniske meldinger

Når du bruker elektroniske meldinger til å generere rapporten, kan du samle inn avgiftsdata fra flere juridiske enheter. Hvis du vil ha mer informasjon, kan du se delen [Kjøre en mva-deklarering for flere juridiske enheter](#run-vat-declaration) senere i dette emnet.

Følgende fremgangsmåte gjelder for eksempel for behandling av elektroniske meldinger som du importerte tidligere fra LCS delt aktivabibliotek.

1. Gå til **Mva \> Forespørsler og rapporter \> Elektroniske meldinger \> Elektroniske meldinger**.
2. Velg **DK-mva-deklarering** i den venstre ruten.
3. I hurtigfanen **Meldinger** velger du **Ny**, og deretter, i dialogboksen **Kjør behandling**, velger du **OK**.
4. Velg meldingslinjen som er opprettet, skriv inn en beskrivelse, og angi deretter start- og sluttdatoene for deklareringen.

   > [!NOTE]
   > Trinn 5 til og med 7 er valgfrie.

5. Valgfritt: I hurtigfanen **Meldinger** velger du **Samle inn data**, og deretter velger du **OK**. Mva-betalingene som ble generert tidligere, blir lagt til i meldingen. Hvis du vil ha mer informasjon, kan du se delen [Utlign og poster merverdiavgift](#settle-and-post-sales-tax) tidligere i dette emnet. Hvis du hopper over dette trinnet, kan du likevel generere en mva-deklarering ved å bruke feltet **Avgiftsdeklareringsversjon** i dialogboksen **Deklarering**.
6. Valgfritt: Gå gjennom mva-betalingene som er overført for behandling, i hurtigfanen **Meldingselementer**. Alle mva-betalinger for den valgte perioden som ikke var inkludert i andre meldinger av samme behandling, er som standard inkludert.
7. Valgfritt: Velg **Opprinnelig dokument** for å gå gjennom mva-betalingene, eller velg **Slett** for å utelate mva-betalinger fra behandling. Hvis du hopper over dette trinnet, kan du likevel generere en mva-deklarering ved å bruke feltet **Avgiftsdeklareringsversjon** i dialogboksen **Deklarering**.
8. På hurtigfanen **Meldinger** velger du **Oppdater status**. I dialogboksen **Oppdater status** velger du **Klar til å generere**, og deretter velger du **OK**. Kontroller at meldingens status er endret til **Klar til å generere**.
9. Velg **Generer rapport**. Hvis du vil forhåndsvise mva-deklareringsbeløpene, velger du **Forhåndsvis rapport** i dialogboksen **Kjør behandling** og velger deretter **OK**.
10. I dialogboksen **Parametere for elektronisk rapportering** definerer du feltene som er beskrevet i delen [Forhåndsvise mva-deklareringen i Excel fra oppgaven Rapportere merverdiavgift for en utligningsperiode](#preview-vat-excel) tidligere i dette emnet, og deretter velger du **OK**.
11. Velg **Vedlegg**-knappen (binderssymbol) i øvre høyre hjørne på siden, og velg deretter **Åpne** for å åpne filen. Gå gjennom beløpene i Excel-dokumentet.

## <a name="run-a-vat-declaration-for-multiple-legal-entities"></a><a name="run-vat-declaration"></a>Kjøre en mva-deklarering for flere juridiske enheter

Hvis du vil bruke formatene til å rapportere mva-deklareringen for en gruppe juridiske enheter, må du først definere programspesifikke parametere for ER-formatene for mva-koder fra alle nødvendige juridiske enheter.

### <a name="set-up-electronic-messages-to-collect-tax-data-from-several-legal-entities"></a>Definere elektroniske meldinger for å samle inn avgiftsdata fra flere juridiske enheter

Følg denne fremgangsmåten for å definere elektroniske meldinger som samler inn data fra flere juridiske enheter.

1. Gå til **Arbeidsområder** > **Funksjonsbehandling**.
2. Søk etter og velg funksjonen **Spørringer på tvers av firmaer for Handlinger for fyll ut poster** i listen, og velg deretter **Aktiver nå**.
3. Gå til **Mva** > **Oppsett** > **Elektroniske meldinger** > **Handlinger for Fyll ut poster**.
4. På siden **Handlinger for Fyll ut poster** merker du linjen for **DK Fylle ut mva-returposter**.

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
