---
title: Importere ISO20022-filer
description: Dette emnet forklarer hvordan du importerer betalingsfiler i formatene ISO 20022 camt.054 og pain.002 i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
author: neserovleo
manager: AnnBe
ms.date: 05/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations, UnifiedOperations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Italy, Latvia, Lithuania, Norway, Poland, Spain, Sweden, Switzerland, United Kingdom
ms.author: v-lenest
ms.search.validFrom: 2017-06-01T00:00:00.000Z
ms.dyn365.ops.version: Enterprise edition, July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 48e280bf0a6c5db237bd389fe448c9d698d3ae12
ms.openlocfilehash: acf6ed5f503d77f372d802a51a71cec062c2b24b
ms.contentlocale: nb-no
ms.lasthandoff: 07/25/2017

---

# <a name="import-iso20022-files"></a>Importere ISO20022-filer

## <a name="overview"></a>Oversikt
Du kan importere betalingsfiler i følgende formater:

 - **ISO20022 camt.054 credit advice** – Importer innkommende betalinger fra en fil i dette formatet i kundebetalingsjournalen.
 - **ISO20022 pain.002 status return** og **ISO20022 camt.054 debit advice** – Importer returfiler i disse formatene i AP-betalingsoverføringsjournalen.

## <a name="prerequisites-for-importing-the-camt054-credit-advice-file"></a>Forutsetninger for å importere camt.054 credit advice-filen
Du må oppfylle følgende forutsetninger for å importere bank varselmeldinger i formatet camt.054.001.002 i kundebetalingsjournalen.

1. Import av **ISO20022 camt.054** Konfigurasjonsnøkkel for elektronisk rapportering (ER) fra Microsoft Dynamics Lifecycle Services (LCS). Deretter, på siden **Kundens betalingsmåte** i feltet **Importer konfigurasjon av format**, velger du denne konfigurasjonen. Hvis du vil ha mer informasjon, se [Filformater for betalingsmåter](emea-select-file-formats-for-the-method-of-payments.md).
2. På siden **Alle kunder** skriver du inn et navn og organisasjonsnummer for hver kunde.
3. På siden **Kundebankkonto** kan du definere en kundebankkontopost ved å angi følgende informasjon: IBAN-nummeret eller bankkontonummeret, og SWIFT-koden eller rutingnummeret.
4. På siden **Bankkontoer** kan du definere en bankkontoer for juridiske enheter ved å angi følgende informasjon: IBAN-nummeret eller bankkontonummeret, og SWIFT-koden eller rutingnummeret, valuta og adresse.

    > [!NOTE]
    > Hvis du planlegger å bruke avansert bankavstemming, på den **Avstemming** hurtigfanen angir du **Avansert bankavstemming** til **Ja**. Hvis du vil avstemme uposterte importerte betalinger, kan du angi **Bruk bankkontoutdrag som bekreftelse av elektroniske betalinger** til **Ja**.

5. Valgfritt: På siden **Transaksjonskodetilordning** kan du definere koblingen mellom banktransaksjonskoder i fil- og banktransaksjonstypene.
6. Hvis filen inneholder avgifter på transaksjonen som du vil postere sammen med den innkommende betalingen, oppretter du et betalingsgebyr på siden **Kundebetalingsgebyr**. Deretter, på siden **Betalingsmåter**, knytte du betalingsgebyret til bankkontoen i betalingsgebyroppsettet.
7. Hvis ESR-betalingene blir importert og inneholder ISR-referanser (aktuelt for juridiske enheter i Sveits), kan du utføre følgende oppsett:

    - I feltet **Kundebetaling, kontolengde** angir du lengden på kundekoden for som skal brukes i-ISR referanser, eller til å identifisere kunden automatisk.
    - Pass på at kundenummeret og fakturanummeret (nummerserier) inneholder bare sifre. De må ikke inneholde andre tegn. Fakturanummeret kan ikke ha innledende nuller.
    - Angi ESR, BESR og rutingnummeret for bankkontoen til den juridiske enheten. Hvis du vil ha mer informasjon, se [Eldre ESR-funksjon](emea-che-esr-customer-payments-import.md), fordi lignende innstillinger er nødvendig.
    
## <a name="import-the-camt054-credit-advice-file-into-the-customer-payment-journal"></a>Importer camt.054 credit advice-filen i kundebetalingsjournalen.
1. På siden **Kundebetalingsjournallinjer** klikker du **Funksjoner** > **importerer betalinger**.
2. Velg betalingsmåten som har de nødvendige innstillingene for formatet ISO20022 camt.054.
3. Angi de nødvendige parametrene og banen til filen, og klikk deretter **OK**.

Filen importeres.

## <a name="prerequisites-for-importing-files-in-the-pain002-status-return-and-camt054-debit-advice-formats-into-the-ap-payment-transfer-journal"></a>Forutsetninger for å importere filer i formatene pain.002 statusretur og camt.054 debetadvis i AP-betalingsoverføringsjournalen.
Du må oppfylle følgende forutsetninger for å importere bankmeldinger i følgende ISO20022-formater til siden **Leverandørbetalingsoverføring**: pain.002.001.003 statusreturmeldinger og camt.054.001.002 debetadvis.

1. Importer ER-konfigurasjonene **ISO20022 camt.054** og **ISO20022 pain.002** fra LCS.
2. På siden **Betalingsmåte for leverandør** i feltene **juridisk enhet** og **Sekundær konfigurasjon av returformat** velger du ER-konfigurasjonene du importerte. Du må aktivere det genrelle elektroniske returformatet for den valgte betalingsmåten.
3. På siden **Tilordning av status for rapportformat**, definerer du tilordning av statuskoder mellom statusene for pain.002 statusene for Leverandørbetalingsjournal.

    Her er et eksempel på et statusoppsett.

    Returstatus | Betalingsstatus
    --------------|---------------
    RJCT          | Avslått
    ACCP          | Godtatt
    ACSP          | Mottatt

4. På siden **Feilkoder for returformat** definere feilkoder for pain.002 og beskrivelser i samsvar med eksterne koder for ISO20022 status.

    Her er et eksempel på en del av et oppsett av feilkode.

    Kode | Navn
    -----|-----
    AC01 | IncorrectAccountNumber
    AC02 | InvalidDebtorAccountNumber
    AC03 | InvalidCreditorAccountNumber
    AC04 | ClosedAccountNumber
    AC05 | ClosedDebtorAccountNumber
    AC06 | BlockedAccount

5. Hvis camt.054-filen inneholder avgifter på transaksjonen som du vil postere sammen med den innkommende betalingen, oppretter du et betalingsgebyr på siden **Leverandørbetalingsgebyr**. Deretter, på siden **Betalingsmåter**, knytte du betalingsgebyret til bankkontoen i betalingsgebyroppsettet.

## <a name="import-the-pain002-status-return-or-camt054-debit-advice-files-into-the-vendor-payment-journal"></a>Importer filene pain.002 statusretur eller camt.054 debetadvis til leverandørbetalingsjournalen
1. Åpne siden **Betalingsoverføringer** på Leverandører-menyen.
2. På siden **Betalingsoverføringer** klikker du **Returfil - leverandør**.
3. Velg betalingsmåten som har de nødvendige innstillingene for ISO20022-filene, og klikk deretter **OK**.
4. Velg filformatet du vil importere, og klikk deretter **OK**.
5. Angi de nødvendige parametrene og banen til filen, og klikk deretter **OK**.

Hvis du importerer filen pain.002, statusen for leverandørbetalingslinjer oppdateres, basert på informasjonen i den importerte filen.

Hvis du importerer filen camt.054, bør du angi følgende tilleggsparametere:

- **Gebyr-ID** – angi en gebyr-ID som definerer nye betalingsgebyrlinjer, som vil bli opprettet på leverandørbetalingsjournallinjen hvis det finnes en tilleggsbeløp i camt.054-filen.
- **Nytt journalnavn** og **Ny journalbeskrivelse** – angi navnet og beskrivelsen av journalen som behandlede transaksjoner vil bli overført til. Etter overføringen må nye bilagsnumre tilordnes i den nye journalen.
- **Importer avtalegirotransaksjoner** – Sett dette alternativet til **Ja** hvis utgående avtalegiroer må importeres til leverandørbetalingsjournalen.
- **Journalnavn** – Definer et nytt navn for de importerte avtalegirotransaksjonene.
- **Utlign transaksjoner** – Sett dette alternativet til **Ja** hvis importerte leverandørbetalinger må utlignes med fakturaer som blir funnet i systemet.

Du kan vise den importerte informasjonen på siden **Betalingsoverføringer**. 

