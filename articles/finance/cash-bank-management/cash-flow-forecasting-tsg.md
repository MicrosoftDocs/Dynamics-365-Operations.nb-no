---
title: Feilsøke konfigurasjon av kontantstrømprognose
description: Dette emnet inneholder svar på spørsmål du kan ha når du konfigurerer kontantstrømprognoser. Den omhandler ofte stilte spørsmål om oppsettet for kontantstrøm, oppdateringer for kontantstrøm og Power BI-kontantstrøm.
author: panolte
ms.date: 03/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7b4760d7a0d0c14e2df8df20c2f81ec41e077cc0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5827320"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="99441-104">Feilsøke konfigurasjon av kontantstrømprognose</span><span class="sxs-lookup"><span data-stu-id="99441-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="99441-105">Dette emnet inneholder svar på spørsmål du kan ha når du konfigurerer kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="99441-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="99441-106">Den omhandler ofte stilte spørsmål om oppsettet for kontantstrøm, oppdateringer for kontantstrøm og Power BI-kontantstrøm.</span><span class="sxs-lookup"><span data-stu-id="99441-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="99441-107">Hvorfor vises kontantstrøm bare for én juridisk enhet?</span><span class="sxs-lookup"><span data-stu-id="99441-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="99441-108">Kontantstrømprognoser konfigureres og beregnes per juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="99441-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="99441-109">Power BI-rapporter og kontantstrømprognosefunksjonene i Finance Insights viser resultatene.</span><span class="sxs-lookup"><span data-stu-id="99441-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="99441-110">Kontantstrømprognoser må defineres for hver juridiske enhet du vil se en prognose for.</span><span class="sxs-lookup"><span data-stu-id="99441-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="99441-111">Gå gjennom konfigurasjonen av kontantstrømprognoser i alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="99441-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="99441-112">Du kan også se gjennom konfigurasjonen til alle juridiske enheter for kontantstrømprognoser, og kontrollere at de er angitt slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="99441-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="99441-113">Hvorfor vises ikke Power BI alle kontantstrømdataene?</span><span class="sxs-lookup"><span data-stu-id="99441-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="99441-114">Flere trinn må fullføres før kontantstrømprognoser kan vises i Power BI-visninger.</span><span class="sxs-lookup"><span data-stu-id="99441-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="99441-115">Gå gjennom følgende kontrolliste, og kontroller at hvert trinn er fullført:</span><span class="sxs-lookup"><span data-stu-id="99441-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="99441-116">Definere kontantstrøm for hver juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="99441-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="99441-117">Angi systemvalutaen og systemvalutakurstypen i parametere for økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="99441-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="99441-118">Angi finansregnskapsvalutaen og valutakurstypen.</span><span class="sxs-lookup"><span data-stu-id="99441-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="99441-119">Angi valutakursen mellom transaksjonsvalutaen og regnskapsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="99441-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="99441-120">Angi valutakursen mellom regnskapsvalutaen og systemvalutaen.</span><span class="sxs-lookup"><span data-stu-id="99441-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="99441-121">Angi valutakursen mellom regnskapsvalutaen og hver bankvaluta.</span><span class="sxs-lookup"><span data-stu-id="99441-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="99441-122">Hvorfor fungerte Power BI-kontantstrøm i tidligere versjoner, men er nå tom?</span><span class="sxs-lookup"><span data-stu-id="99441-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="99441-123">Kontroller at målingene for "kontantstrømmåling V2" og "LedgerCovLiquidityMeasurement" fra enhetslager er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="99441-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="99441-124">Hvis du vil ha mer informasjon om hvordan du arbeider med data i enhetsbutikk, kan du se [Power BI-integrering med enhetslager](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span><span class="sxs-lookup"><span data-stu-id="99441-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md).</span></span> <span data-ttu-id="99441-125">Kontroller at alle trinnene som kreves for å vise Power BI-innhold, er fullført.</span><span class="sxs-lookup"><span data-stu-id="99441-125">Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="99441-126">Hvis du vil ha mer informasjon, kan du se [Power BI-innholdet Kontantstrømoversikt](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="99441-126">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="99441-127">Er enhetslagerenhetene oppdatert?</span><span class="sxs-lookup"><span data-stu-id="99441-127">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="99441-128">Du må oppdatere enhetene regelmessig for å sikre at dataene er oppdatert og nøyaktige.</span><span class="sxs-lookup"><span data-stu-id="99441-128">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="99441-129">Hvis du vil oppdatere en bestemt enhet manuelt, kan du gå til **Systemadministrasjon \> Oppsett \> Enhetslager**, velge enheten og deretter velge **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="99441-129">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="99441-130">Dataene kan også oppdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="99441-130">The data can also be updated automatically.</span></span> <span data-ttu-id="99441-131">Sett alternativet **Automatisk oppdatering aktivert** til **Ja** på siden **Enhetslager**.</span><span class="sxs-lookup"><span data-stu-id="99441-131">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>

## <a name="which-calculation-method-should-be-used-when-calculating-cash-flow-forecasts"></a><span data-ttu-id="99441-132">Hvilken beregningsmetode skal brukes når kontantstrømprognoser beregnes?</span><span class="sxs-lookup"><span data-stu-id="99441-132">Which calculation method should be used when calculating cash flow forecasts?</span></span>

<span data-ttu-id="99441-133">Beregningsmetoden for kontantstrømprognose har to viktige valgalternativer.</span><span class="sxs-lookup"><span data-stu-id="99441-133">The Cash flow forecast calculation method has two important selection options.</span></span> <span data-ttu-id="99441-134">Alternativet **Ny** vil beregne kontantstrømprognoser for nye dokumenter og dokumenter som er endret siden den siste satsvise jobben ble kjørt.</span><span class="sxs-lookup"><span data-stu-id="99441-134">The **New** option will calculate cash flow forecasts for new documents and documents that have changed since the last batch job ran.</span></span> <span data-ttu-id="99441-135">Dette alternativet går raskere, fordi det behandler et mindre delsett med dokumenter.</span><span class="sxs-lookup"><span data-stu-id="99441-135">This option tends to run faster because it processes a smaller subset of documents.</span></span> <span data-ttu-id="99441-136">Alternativet **Totalt** beregner kontantstrømprognoser på nytt for hvert dokument i systemet.</span><span class="sxs-lookup"><span data-stu-id="99441-136">The **Total** option will recalculate cash flow forecasts for every document in the system.</span></span> <span data-ttu-id="99441-137">Dette alternativet tar mer tid, fordi det har mer arbeid å fullføre.</span><span class="sxs-lookup"><span data-stu-id="99441-137">This option takes more time because it has more work to complete.</span></span>

### <a name="how-do-i-improve-the-performance-of-the-cash-flow-forecasting-recurring-batch-job"></a><span data-ttu-id="99441-138">Hvordan forbedrer jeg ytelsen til kontantstrømprognosene for gjentakende satsvis jobb?</span><span class="sxs-lookup"><span data-stu-id="99441-138">How do I improve the performance of the cash flow forecasting recurring batch job?</span></span>

<span data-ttu-id="99441-139">Vi anbefaler at du kjører kontantstrømprognosen én gang hver dag i perioder med mindre trafikk ved hjelp av **Ny beregning**-metoden.</span><span class="sxs-lookup"><span data-stu-id="99441-139">We recommend running your cash flow forecast once each day during the off-peak hours using the **New** calculation method.</span></span> <span data-ttu-id="99441-140">Vi anbefaler at du bruker denne fremgangsmåten seks dager i uken.</span><span class="sxs-lookup"><span data-stu-id="99441-140">We recommend using this approach six days per week.</span></span> <span data-ttu-id="99441-141">Deretter kjører du en kontantstrømprognose én gang i uken med beregningsmetoden **Totalt** på dagen med minst aktivitet.</span><span class="sxs-lookup"><span data-stu-id="99441-141">Then run a cash flow forecast once each week using the **Total** calculation method on the day with the least amount of activity.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]

