---
title: Importere og eksportere avgiftsberegninger
description: Denne artikkelen inneholder informasjon om import- og eksportfunksjonaliteten til avgiftsberegningstjenesten.
author: Kai-Cloud
ms.date: 10/17/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kfend
ms.custom: ''
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-11-15
ms.dyn365.ops.version: 10.0.23
ms.openlocfilehash: 8666d4971e36279ebd2b1396de7cab37680980e6
ms.sourcegitcommit: 40c80a617b903c2b26e44b41147e0021c5cb680d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/18/2022
ms.locfileid: "9690240"
---
# <a name="import-and-export-tax-calculations"></a>Importere og eksportere avgiftsberegninger

Denne artikkelen inneholder informasjon om import- og eksportfunksjonaliteten til avgiftsberegningstjenesten. Denne funksjonaliteten sikrer en fleksibel og effektiv konfigurasjonsopplevelse.

## <a name="import-and-export-tax-codes"></a>Importere og eksportere avgiftskoder

### <a name="export-templates"></a>Eksportmaler

1. Logg på [Regulatory Configuration Service (RCS)](https://marketing.configure.global.dynamics.com/).
2. I arbeidsområdet **Globaliseringsfunksjoner** velger du **Funksjoner**, og velg deretter flisen **Avgiftsberegning**.
3. Opprett en eksisterende funksjon eller [opprett en ny funksjon](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Velg **Rediger** i rutenettet **Versjoner**.
5. På funksjonssiden **Avgiftsberegning** angir du [konfigurasjonsversjonen](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Velg **Importer** i fanen **Avgiftskoder**.
7. Velg **Eksporter en mva-kodemal** for å laste ned filen **TaxCodesTemplate.zip**.
8. Pakk ut **TaxCodesTemplate.zip**. Avgiftskodemalene komprimeres separat i henhold til verdien for **Beregningsgrunnlag**.
9. Pakke ut **Etter nettobeløp.zip** for å hente følgende filer med kommaseparerte verdier (CSV):

    - **TaxCode.csv** – Angi avgiftskodene.
    - **TaxLimit.csv** – Angi mva-grensene for hver avgiftskode.
    - **TaxRate.csv** – Angi mva-satsene for hver avgiftskode.

> [!NOTE]
> Som standard er oppføringer for **Eksempel**-avgiftskoden tilgjengelig i malene. Hvis **Eksempel**-avgiftskode ikke fjernes fra CSV-filene, importeres den til funksjonen.

### <a name="import-tax-codes"></a>Importere mva-koder

Følg denne fremgangsmåten for å importere **Eksempel**-avgiftskoden i malen til avgiftsberegningsfunksjonen.

1. I RCS, på funksjonssiden for **Avgiftsberegning** i fanen **Avgiftskoder**, velger du **Importer**.
2. Velg **Bla gjennom**, finn og velg **TaxCode.csv**-filen, og velg deretter **Mva-kode** i feltet **Måltabell**.
3. Velg **OK** for å importere avgiftskoden.
4. Finn og velg **TaxCode.csv**-filen, og velg deretter **Mva-sats** i feltet **Måltabell**.
5. Velg **OK** for å importere avgiftssatsen.
6. Finn og velg **TaxLimit.csv**-filen, og velg deretter **Avgiftsgrense** i feltet **Måltabell**.
7. Velg **OK** for å importere avgiftsgrensen.

Du kan også importere zip-filen direkte som inneholder alle de tre CSV-filene. På denne måten kan du raskt og enkelt fullføre importen.

1. I RCS, på funksjonssiden for **Avgiftsberegning** i fanen **Avgiftskoder**, velger du **Importer**.
2. Velg **Bla gjennom**, finn og velg filen **Etter nettobeløp.zip**, og velg deretter **OK**.

### <a name="export-tax-codes"></a>Eksportere mva-koder

1. I RCS, på funksjonssiden for **Avgiftsberegning** i fanen **Avgiftskoder**, velger du **Eksporter**.

    **Eksporter**-knappen er tilgjengelig når det finnes minst én avgiftskode i rutenettet **Mva-koder**.

2. Velg **OK** for å eksportere alle avgiftskodene til funksjonen i en zip-fil.

> [!NOTE]
> Bruk den eksporterte filen som en mal for å importere avgiftskoder til tilsvarende funksjon.

## <a name="import-and-export-applicability-rules"></a>Importere og eksportere gjeldende regler

### <a name="export-applicability-rules"></a>Eksportere relevansregler

1. Logg på [RCS](https://marketing.configure.global.dynamics.com/).
2. I arbeidsområdet **Globaliseringsfunksjoner** velger du **Funksjoner**, og velg deretter flisen **Avgiftsberegning**.
3. Opprett en eksisterende funksjon eller [opprett en ny funksjon](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
4. Velg **Rediger** i rutenettet **Versjoner**.
5. På funksjonssiden **Avgiftsberegning** angir du [konfigurasjonsversjonen](global-get-started-with-tax-calculation-service.md#set-up-tax-calculation-in-rcs).
6. Merk radene i rutenettet for **Konfigurere avgiftsgrupperelevans** i fanen **Anvendelse av avgiftsgruppe**.
7. Velg knappen **Åpne i Microsoft Office**, og velg deretter valget for **Dynamisk relevansmatrise for avgiftstjeneste**.

    [![Eksportere gjeldende regler til Microsoft Excel på siden for avgiftsberegningsfunksjonen.](./media/tax-cal-import-export-1.png)](./media/tax-cal-import-export-1.png)

8. Velg **Last ned** for å eksportere de valgte radene til et Microsoft Excel-regneark.

### <a name="import-applicability-rules"></a>Importere relevansregler

Excel-regnearket du lastet ned, inneholder strukturen for rutenettet **Konfigurere avgiftsgrupperelevans**. Du kan legge til nye regler direkte i regnearket. Når du er ferdig, følger du denne fremgangsmåten for å importere de nye reglene tilbake til rutenettet for **Konfigurere avgiftsgrupperelevans**.

1. Merk og kopier radene som skal importeres, i Excel-regnearket.
2. I RCS, på funksjonssiden for **Avgiftsberegning** i fanen **Relevans for avgiftsgruppe**, velger du **Legg til** for å sette inn en tom post nederst i rutenettet **Konfigurere avgiftsgrupperelevans**.
3. Velg **Ctrl+V** for å lime inn de kopierte radene i rutenettet.
4. Velg **Lagre**.

## <a name="import-feature-demo-data"></a>Importere demodata for funksjoner

Følg denne fremgangsmåten for å importere demodata for funksjoner.

1. Logg på [RCS](https://marketing.configure.global.dynamics.com/).
2. I arbeidsområdet **Globaliseringsfunksjoner** velger du **Funksjoner**, og velg deretter flisen **Avgiftsberegning**.
3. Velg **Importer**, og deretter på siden **Importer funksjon fra globalt repositorium** velger du **Synkroniser**. 
4. I tabellen velger du funksjonen for **avgiftsberegning-funksjon-demodata**, og deretter velger du **Importer**.
5. Velg **Vis** for å se gjennom avgiftskodene, gruppene og reglene for bruk som er definert i den importerte funksjonen.
6. I Finance bytter du til den juridiske enheten **DEMF**, og deretter går du til **Avgift** \> **Oppsett** \> **Avgiftskonfigurasjon** \> **Parametere for avgiftsberegning**.
7. I **Generelt**-fanen velger du **Aktiver tjeneste for avgiftsberegning**.
8. I feltet **Navn på funksjonsoppsett** velger du **avgiftsberegning-funksjon-demodata**.
9. Velg en **Utligningsperiode** og **Finansposteringsgruppe** for de nye demoavgiftskodene, og velg deretter **Bekreft**.
10. Velg **Lagre**.

> [!NOTE]
> Demofunksjonen for **avgiftsberegning-funksjon-demodata** er basert på funksjonsversjonsversjon **40.54.234** og er utformet for den juridiske enheter i **DEMF**-demoen. Kontroller at Finance og RCS oppgraderes til versjon 10.0.26 eller senere.
