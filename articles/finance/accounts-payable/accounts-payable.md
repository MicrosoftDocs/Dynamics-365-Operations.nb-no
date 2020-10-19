---
title: Startside for leverandører
description: Dette emnet gir en oversikt over leverandører.
author: ShylaThompson
manager: AnnBe
ms.date: 02/15/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendInvoiceWorkspace
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 21901
ms.assetid: 1e4c2ac4-077b-4678-8733-5cec8f6ff659
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 6a6f53007f8bd04724c43c518c5a9b10856b68d7
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976725"
---
# <a name="accounts-payable-home-page"></a>Startside for leverandører

[!include [banner](../includes/banner.md)]

Dette emnet gir en oversikt over leverandører. 

Du kan registrere leverandørfakturaer manuelt eller motta dem elektronisk via en dataenhet. Når fakturaene er registrert eller mottatt, kan du se gjennom og godkjenne fakturaene ved hjelp av en fakturagodkjenningsjournal eller siden **Leverandørfaktura**. Du kan bruke fakturasamsvar, leverandørfakturapolicyer og arbeidsflyt til å automatisere kontrollprosessen slik at fakturaer som oppfyller bestemte kriterier, godkjennes automatisk, og de gjenværende fakturaene flagges for gjennomgang av en autorisert bruker.

**Forretningsprosesser**

[![Diagram med forretningsprosesser](./media/AP-process.PNG)](./media/AP-process.PNG)

## <a name="set-up-accounts-payable"></a>Definere Leverandør

Definer leverandørgrupper, leverandører, posteringsprofiler, ulike betalingsalternativer og parametere i forbindelse med leverandører, tillegg, leveranser og mål, egenveksler, og annen type informasjon om leverandører. 

[Oversikt over å konfigurere leverandør](accounts-payable-overview.md)

[Regnskapsdistribusjoner og underfinansjournaloppføringer for leverandørfakturaer](accounting-distributions-subledger-journal-entries-vendor-invoices.md) 

[Revaluering av utenlandsk valuta for leverandører og kunder](../cash-bank-management/foreign-currency-revaluation-accounts-payable-accounts-receivable.md)

## <a name="configure-vendor-invoices"></a>Konfigurere leverandørfakturaer

Bruk leverandører til å spore fakturaer og utgående utgifter til leverandører.

[Oversikt over samsvar for leverandørfaktura](accounts-payable-invoice-matching.md)

[Leverandørposteringsprofiler](vendor-posting-profiles.md)

[Definere validering av leverandørfakturakontroll](tasks/set-up-accounts-payable-invoice-matching-validation.md)

[Treveis kontrollpolicyer](three-way-matching-policies.md)

[Fakturasamsvar og konserninterne bestillinger](invoice-matching-intercompany-purchase-orders.md)

[Oversikt over å løse avvik under kontroll for fakturatotaler](resolve-invoice-totals-invoice-matching-discrepancies.md)

[Standard motkontoer for leverandørfakturajournaler og fakturagodkjenningsjournaler](default-offset-accounts-vendor-invoice-journals.md)

[Mobile fakturagodkjenninger](mobile-invoice-approvals.md)

[Arbeidsområde for leverandørsamarbeidsfakturering](vendor-portal-invoicing-workspace.md)

[Automatisering av leverandørfaktura](vendor-invoice-automation.md)

## <a name="configure-vendor-payments"></a>Konfigurere leverandørbetalinger 

Tilordne en systemdefinert betalingstype, for eksempel sjekk, elektronisk betaling eller egenveksel, til en hvilken som helst brukerdefinert betalingsmåte. Betalingstyper er valgfrie, men de er nyttige når du validerer elektroniske betalinger, og når du vil ha muligheten til raskt å finne ut hvilken betalingstype en betaling skal bruke. 

[Arbeidsområde for leverandørbetalinger](vendor-payments-workspace.md)

[Definere leverandørbetalingsgebyrer](tasks/define-vendor-payment-fees.md)

[Definere leverandørbetalingsbetingelser](tasks/define-vendor-payment-terms.md)

[Oversikt over positiv betaling](positive-pay-overview.md)

[Definere og generere positive betalingsfiler](set-up-generate-positive-pay-files.md)

[Opprette leverandørbetalinger ved hjelp av et betalingsforslag](create-vendor-payments-payment-proposal.md)

[Leverandørbetalinger for et delbeløp](vendor-payments-partial-amount.md)

[Bruke en rabatt som er større enn beregnet rabatt for en leverandørbetaling](take-discount-more-calculated-discount-vendor-payment.md)

[Bruke en kontantrabatt utenfor kontantrabattperioden](take-cash-discount-outside-cash-discount-timeframe.md)

[Eksempel på leverandørsjekker for elektronisk rapportering](electronic-reporting-sample-vendor-checks.md)

[Tilbakeføre en leverandørbetaling](reverse-vendor-payment.md)

[Forskuddsbetalte fakturaer i forhold til forskuddsbetalinger](prepayments-invoices-vs-prepayments.md)

[Sentraliserte betalinger leverandører](centralized-payments-accounts-payable.md)

## <a name="settlements"></a>Utligninger

Emnene nedenfor gir informasjon om utligninger. Utligning er prosessen med å utligne betalinger med fakturaer. 

[Konfigurere utligning](../cash-bank-management/configure-settlement.md)

[Utligne en delvis leverandørbetaling før rabattdatoen med en endelige betaling etter rabattdatoen](settle-partial-vendor-payment-before-discount-or-final-payment-after.md)

[Utligne en delvis leverandørbetaling som har rabatter på leverandørkreditnotaer](settle-partial-vendor-payment-discounts-vendor-credit-notes.md)

[Utligne en delvis leverandørbetaling som har flere rabattperioder](settle-partial-vendor-payment-multiple-discount-periods.md)

[Utligne en delvis leverandørbetaling og den endelige betalingen i sin helhet før rabattdatoen](settle-partial-vendor-payment-or-final-payment-before-discount.md)

[Enkelt bilag med flere poster for kunde eller leverandør](single-voucher-multiple-customer-vendor-records.md)



### <a name="additional-resources"></a>Tilleggsressurser

#### <a name="whats-new-and-in-development"></a>Hva er nytt og hva er under utvikling?

Gå til [Lanseringsplaner for Microsoft Dynamics 365](https://go.microsoft.com/fwlink/?linkid=2010158) for å se hvilke nye funksjoner som er planlagt. 

#### <a name="blogs"></a>Blogger

Du kan finne meninger, nyheter og annen informasjon om Leverandører og andre løsninger i bloggen for [Microsoft Dynamics 365](https://community.dynamics.com/b/msftdynamicsblog?c=Enterprise) og bloggen for [Microsoft Dynamics 365 Finance - Financials](https://community.dynamics.com/365/financeandoperations/b/financials).

[Microsoft Dynamics Operations Partner Community-bloggen](https://community.dynamics.com/partner/b/operationspartnercommunityblog) gir Microsoft Dynamics-partnere én ressurs der de kan finne ut mer om hva som er nytt og populært i Dynamics 365.

#### <a name="community-blogs"></a>Fellesskapsblogger

[Administrere leverandører i Dynamics 365 Finance](https://financefunction.tech/2019/02/15/how-to-manage-payables-in-dynamics-365-for-finance-and-operations)

#### <a name="task-guides"></a>Oppgaveveiledninger
Mer hjelp er tilgjengelig som oppgaveveiledninger i programmet. For å få tilgang til oppgaveveiledninger klikker du på Hjelp-knappen på en side.

#### <a name="videos"></a>Videoer

Se instruksjonsvideoene som nå er tilgjengelige på [Microsoft Dynamics 365 YouTube-kanalen](https://www.youtube.com/channel/UCJGCg4rB3QSs8y_1FquelBQ).




