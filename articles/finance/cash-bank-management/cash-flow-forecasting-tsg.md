---
title: Feilsøke konfigurasjon av kontantstrømprognose
description: Dette emnet inneholder svar på spørsmål du kan ha når du konfigurerer kontantstrømprognoser. Den omhandler ofte stilte spørsmål om oppsettet for kontantstrøm, oppdateringer for kontantstrøm og Power BI-kontantstrøm.
author: panolte
manager: AnnBe
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerCovParameters
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2020-12-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d1cde9321259753bd0cacab3706c7f8455598ff3
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232495"
---
# <a name="troubleshoot-cash-flow-forecasting-setup"></a><span data-ttu-id="ea0c5-104">Feilsøke konfigurasjon av kontantstrømprognose</span><span class="sxs-lookup"><span data-stu-id="ea0c5-104">Troubleshoot cash flow forecasting setup</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ea0c5-105">Dette emnet inneholder svar på spørsmål du kan ha når du konfigurerer kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-105">This topic provides answers to questions that you might have when you configure cash flow forecasting.</span></span> <span data-ttu-id="ea0c5-106">Den omhandler ofte stilte spørsmål om oppsettet for kontantstrøm, oppdateringer for kontantstrøm og Power BI-kontantstrøm.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-106">It addresses frequently asked questions (FAQ) about the setup for cash flow, updates to cash flow, and cash flow Power BI.</span></span>

## <a name="why-is-cash-flow-shown-for-only-one-legal-entity"></a><span data-ttu-id="ea0c5-107">Hvorfor vises kontantstrøm bare for én juridisk enhet?</span><span class="sxs-lookup"><span data-stu-id="ea0c5-107">Why is cash flow shown for only one legal entity?</span></span>

<span data-ttu-id="ea0c5-108">Kontantstrømprognoser konfigureres og beregnes per juridisk enhet.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-108">Cash flow forecasting is configured and calculated per legal entity.</span></span> <span data-ttu-id="ea0c5-109">Power BI-rapporter og kontantstrømprognosefunksjonene i Finance Insights viser resultatene.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-109">Power BI reports and the cash flow forecasts capability in Finance insights show the results.</span></span>

<span data-ttu-id="ea0c5-110">Kontantstrømprognoser må defineres for hver juridiske enhet du vil se en prognose for.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-110">Cash flow forecasting must be set up for each legal entity that you want to see a forecast for.</span></span> <span data-ttu-id="ea0c5-111">Gå gjennom konfigurasjonen av kontantstrømprognoser i alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-111">Review the configuration of cash flow forecasting in all your legal entities.</span></span> <span data-ttu-id="ea0c5-112">Du kan også se gjennom konfigurasjonen til alle juridiske enheter for kontantstrømprognoser, og kontrollere at de er angitt slik du ønsker.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-112">Alternatively, review the configuration of all the legal entities for cash flow forecasting, and make sure that they are set as you intended.</span></span>

## <a name="why-doesnt-power-bi-show-all-the-cash-flow-data"></a><span data-ttu-id="ea0c5-113">Hvorfor vises ikke Power BI alle kontantstrømdataene?</span><span class="sxs-lookup"><span data-stu-id="ea0c5-113">Why doesn't Power BI show all the cash flow data?</span></span>

<span data-ttu-id="ea0c5-114">Flere trinn må fullføres før kontantstrømprognoser kan vises i Power BI-visninger.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-114">Several steps must be completed before cash flow forecasts can appear in Power BI views.</span></span> <span data-ttu-id="ea0c5-115">Gå gjennom følgende kontrolliste, og kontroller at hvert trinn er fullført:</span><span class="sxs-lookup"><span data-stu-id="ea0c5-115">Review the following checklist, and make sure that every step has been completed:</span></span>

- <span data-ttu-id="ea0c5-116">Definere kontantstrøm for hver juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-116">Set up cash flow for each legal entity.</span></span>
- <span data-ttu-id="ea0c5-117">Angi systemvalutaen og systemvalutakurstypen i parametere for økonomimodul.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-117">In General ledger parameters, set the system currency and the system exchange rate type.</span></span>
- <span data-ttu-id="ea0c5-118">Angi finansregnskapsvalutaen og valutakurstypen.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-118">Set the ledger accounting currency and the exchange rate type.</span></span>
- <span data-ttu-id="ea0c5-119">Angi valutakursen mellom transaksjonsvalutaen og regnskapsvalutaen.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-119">Enter exchange rates between the transaction currency and the accounting currency.</span></span>
- <span data-ttu-id="ea0c5-120">Angi valutakursen mellom regnskapsvalutaen og systemvalutaen.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-120">Enter exchange rates between the accounting currency and the system currency.</span></span>
- <span data-ttu-id="ea0c5-121">Angi valutakursen mellom regnskapsvalutaen og hver bankvaluta.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-121">Enter exchange rates between the accounting currency and each bank currency.</span></span>

## <a name="why-did-cash-flow-power-bi-work-in-previous-versions-but-is-now-blank"></a><span data-ttu-id="ea0c5-122">Hvorfor fungerte Power BI-kontantstrøm i tidligere versjoner, men er nå tom?</span><span class="sxs-lookup"><span data-stu-id="ea0c5-122">Why did cash flow Power BI work in previous versions but is now blank?</span></span>

<span data-ttu-id="ea0c5-123">Kontroller at målingene for "kontantstrømmåling V2" og "LedgerCovLiquidityMeasurement" fra enhetslager er konfigurert.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-123">Verify that the "Cash flow measure V2" and "LedgerCovLiquidityMeasurement" measurements from Entity store have been configured.</span></span> <span data-ttu-id="ea0c5-124">Hvis du vil ha mer informasjon om hvordan du arbeider med enhetslager, kan du se [Power BI-integrering med enhetslager](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md). Kontroller at alle trinnene som er nødvendige for å vise Power BI-innhold, er fullført.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-124">For more information about how to work with data in Entity store, see [Power BI integration with Entity store](../../fin-ops-core/dev-itpro/analytics/power-bi-integration-entity-store.md) Verify that all the steps that are required to view Power BI content have been completed.</span></span> <span data-ttu-id="ea0c5-125">Hvis du vil ha mer informasjon, kan du se [Power BI-innholdet Kontantstrømoversikt](Cash-Overview-Power-BI-content.md).</span><span class="sxs-lookup"><span data-stu-id="ea0c5-125">For more information, see [Cash overview Power BI content](Cash-Overview-Power-BI-content.md).</span></span>

## <a name="have-the-entity-store-entities-been-refreshed"></a><span data-ttu-id="ea0c5-126">Er enhetslagerenhetene oppdatert?</span><span class="sxs-lookup"><span data-stu-id="ea0c5-126">Have the Entity store entities been refreshed?</span></span>

<span data-ttu-id="ea0c5-127">Du må oppdatere enhetene regelmessig for å sikre at dataene er oppdatert og nøyaktige.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-127">You must periodically refresh your entities to ensure that the data is current and accurate.</span></span> <span data-ttu-id="ea0c5-128">Hvis du vil oppdatere en bestemt enhet manuelt, kan du gå til **Systemadministrasjon \> Oppsett \> Enhetslager**, velge enheten og deretter velge **Oppdater**.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-128">To manually refresh a specific entity, go to **System administration \> Setup \> Entity store**, select the entity, and then select **Refresh**.</span></span> <span data-ttu-id="ea0c5-129">Dataene kan også oppdateres automatisk.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-129">The data can also be updated automatically.</span></span> <span data-ttu-id="ea0c5-130">Sett alternativet **Automatisk oppdatering aktivert** til **Ja** på siden **Enhetslager**.</span><span class="sxs-lookup"><span data-stu-id="ea0c5-130">On the **Entity store** page, set the **Automatic refresh enabled** option to **Yes**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]