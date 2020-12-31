---
title: Kontantstrømprognose (forhåndsversjon)
description: Dette emnet beskriver funksjonen for kontantstrømprognoser.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-19
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: f97b8fc0896f0f7b95bf5609f94367b3a8230ca7
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645254"
---
# <a name="cash-flow-forecast-preview"></a><span data-ttu-id="14fac-103">Kontantstrømprognose (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="14fac-103">Cash flow forecast (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="14fac-104">Kontantstrøm er avgjørende for alle bedrifter.</span><span class="sxs-lookup"><span data-stu-id="14fac-104">Cash flow is critical to any business.</span></span> <span data-ttu-id="14fac-105">Selv lønnsomme firmaer kan stå i fare for å gå konkurs hvis de ikke opprettholder kontantstrømmen for å dekke umiddelbare behov.</span><span class="sxs-lookup"><span data-stu-id="14fac-105">Even profitable companies can face insolvency if they don't maintain the cash flow to meet immediate needs.</span></span> <span data-ttu-id="14fac-106">Muligheten for kontantstrømprognoser i Finance Insights kan hjelpe firmaer med å overvåke og behandle kontantsaldoene effektivt.</span><span class="sxs-lookup"><span data-stu-id="14fac-106">The cash flow forecasting capability in Finance insights can help companies monitor and manage their cash balances effectively.</span></span> <span data-ttu-id="14fac-107">Denne funksjonen bruker maskinlæring til å hjelpe bedrifter med å lage en mer presis prognose for kontantstrømmer enn tidligere.</span><span class="sxs-lookup"><span data-stu-id="14fac-107">This feature uses machine learning to help businesses forecast cash flows more accurately than they have previously.</span></span> <span data-ttu-id="14fac-108">Den kan også hjelpe ledere å ta beslutninger som optimaliserer salgsmuligheter i konteksten til den gjeldende likviditetsbeholdningen.</span><span class="sxs-lookup"><span data-stu-id="14fac-108">It can also help managers make decisions that optimize opportunities in the context of their current cash position.</span></span> 

<span data-ttu-id="14fac-109">For de fleste firmaer er det en kjedelig, repeterende og manuell prosess å behandle kontantstrøm og kjøre kontantstrømprognoser.</span><span class="sxs-lookup"><span data-stu-id="14fac-109">For most companies, managing cash flow and running cash flow forecasting is a tedious, repetitive, and manual process.</span></span> <span data-ttu-id="14fac-110">De fleste firmaer er avhengige av Microsoft Excel-løsninger som har varierende grad av kompleksitet.</span><span class="sxs-lookup"><span data-stu-id="14fac-110">Most companies rely on Microsoft Excel solutions that have varying degrees of complexity.</span></span> <span data-ttu-id="14fac-111">Utfordringene ved å lage nøyaktige prognoser for kontantstrøm omfatter følgende:</span><span class="sxs-lookup"><span data-stu-id="14fac-111">The challenges of accurately forecasting cash flow include the following:</span></span>

- <span data-ttu-id="14fac-112">Data er ikke tilgjengelige for beslutningstakere fordi de er spredt over flere steder, inkludert følgende:</span><span class="sxs-lookup"><span data-stu-id="14fac-112">Data isn't available to decision makers because it's scattered in multiple places, including:</span></span> 
  - <span data-ttu-id="14fac-113">Regnskaps- eller ressursplanleggingssystemet</span><span class="sxs-lookup"><span data-stu-id="14fac-113">The accounting or enterprise resource planning system</span></span>
  - <span data-ttu-id="14fac-114">Programvare for økonomisk planlegging</span><span class="sxs-lookup"><span data-stu-id="14fac-114">Financial planning software</span></span>
  - <span data-ttu-id="14fac-115">Excel</span><span class="sxs-lookup"><span data-stu-id="14fac-115">Excel</span></span>
  - <span data-ttu-id="14fac-116">Andre programmer</span><span class="sxs-lookup"><span data-stu-id="14fac-116">Additional software applications</span></span> 
- <span data-ttu-id="14fac-117">Prognoser er basert på intern kunnskap som er i «siloer» i hvert domene eller hver avdeling.</span><span class="sxs-lookup"><span data-stu-id="14fac-117">Forecasting is based on internal knowledge that resides in "silos" within each domain or department.</span></span>
- <span data-ttu-id="14fac-118">Det er usikkert og vanskelig å måle nøyaktigheten til kontantstrømprognoser etter at finansen er realisert.</span><span class="sxs-lookup"><span data-stu-id="14fac-118">Measuring the accuracy of cash flow forecasting after the financials have been realized is uncertain and difficult.</span></span>
    
## <a name="details-of-the-cash-flow-forecasts-capability"></a><span data-ttu-id="14fac-119">Detaljer om funksjonen for kontantstrømprognoser</span><span class="sxs-lookup"><span data-stu-id="14fac-119">Details of the Cash flow forecasts capability</span></span>
<span data-ttu-id="14fac-120">Funksjonen for kontantstrømprognoser omfatter følgende funksjonalitet.</span><span class="sxs-lookup"><span data-stu-id="14fac-120">The Cash flow forecasts feature includes the following functionality.</span></span> 

- <span data-ttu-id="14fac-121">Gjør det enkelt å integrere kontantstrømdata fra eksterne systemer i Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="14fac-121">Makes it easy to integrate cash flow data from external systems to Dynamics 365 Finance.</span></span> <span data-ttu-id="14fac-122">Kontantstrømprognoser kan også bruke rammeverket for import/eksport av data.</span><span class="sxs-lookup"><span data-stu-id="14fac-122">Cash flow forecasts can also use the data import-export framework.</span></span> <span data-ttu-id="14fac-123">Dette rammeverket gjør det enkelt å integrere med Excel OData.</span><span class="sxs-lookup"><span data-stu-id="14fac-123">This framework makes it easy to integrate with Excel OData.</span></span> <span data-ttu-id="14fac-124">Du kan også kombinere data fra flere kilder for å opprette en omfattende kontantstrømløsning.</span><span class="sxs-lookup"><span data-stu-id="14fac-124">You can also combine data from multiple sources to create a comprehensive cash flow solution.</span></span> 

- <span data-ttu-id="14fac-125">Innfører intelligent likviditetsbeholdning.</span><span class="sxs-lookup"><span data-stu-id="14fac-125">Introduces intelligent cash position.</span></span> <span data-ttu-id="14fac-126">Likviditetsbeholdning opprettes på grunnlag av kundens betalingsatferd for å forutsi når et firma kan forvente kontanter på kontoene.</span><span class="sxs-lookup"><span data-stu-id="14fac-126">Cash position is created  based on customer’s payment behavior to predict when a company can expect cash to arrive in their accounts.</span></span> <span data-ttu-id="14fac-127">Den analyserer også de historiske mønstrene til betalende leverandører, for å forutsi når fremtidige fakturaer og ordrer sannsynligvis blir betalt.</span><span class="sxs-lookup"><span data-stu-id="14fac-127">It also analyzes the historical patterns of paying vendors, to predict when future invoices and orders are likely to be paid.</span></span> 

- <span data-ttu-id="14fac-128">Innfører intelligente kontantstrømprognoser for langsiktige prognoser ved hjelp av tidsserieprognoser gjennom automatisert integrasjon med AI Builder.</span><span class="sxs-lookup"><span data-stu-id="14fac-128">Introduces intelligent cash flow forecasting for long-term forecasting, using time series forecasting through automated integration with AI Builder.</span></span>

- <span data-ttu-id="14fac-129">Gir mulighet til å lagre bestemt kontantstrømbeholdning eller -prognoser, redigere dem og deretter enkelt sammenligne og måle prognosens ytelse i forhold til den faktiske finansen.</span><span class="sxs-lookup"><span data-stu-id="14fac-129">Provides the ability to save specific cash flow position or forecasts, edit them, and then easily compare and measure the forecast performance to the actual financials.</span></span>

- <span data-ttu-id="14fac-130">Gjør at det kan foretas hva-skjer-hvis-analyse gjennom sammenligning av øyeblikksbilder.</span><span class="sxs-lookup"><span data-stu-id="14fac-130">Enables what-if analysis through snapshot comparison.</span></span> <span data-ttu-id="14fac-131">Du kan for eksempel opprette flere øyeblikksbilder som representerer et optimistisk, et pessimistisk og det mest realistiske perspektivet på kontantstrømmen, og deretter sammenligne og vise forskjellene.</span><span class="sxs-lookup"><span data-stu-id="14fac-131">For example, you can create multiple snapshots that represent optimistic, pessimistic, and the most realistic views of your cash flow, and then compare and view the differences.</span></span>

- <span data-ttu-id="14fac-132">Du kan vise kontantstrømprognosen i flere valutaer, på tvers av juridiske enheter, og filtrere og vise kontantstrøm som er knyttet til en bankkonto.</span><span class="sxs-lookup"><span data-stu-id="14fac-132">Provides the ability to view the cash flow forecast in multiple currencies, across legal entities, and filter and view cash flow related to a bank account.</span></span> 

- <span data-ttu-id="14fac-133">Lar deg filtrere og vise bankkontoer som er knyttet til finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="14fac-133">Lets you filter and view bank accounts that are related to financial dimensions.</span></span>

<span data-ttu-id="14fac-134">Funksjonaliteten for kontantstrømprognose i Dynamics 365 Finance gjør det enklere for organisasjonen å transformere kjedelig, kompleks og repeterende kontantstrømprognose til en enkel, automatisert prosess.</span><span class="sxs-lookup"><span data-stu-id="14fac-134">The cash flow forecasting functionality in Dynamics 365 Finance will empower your organization to transform tedious, complex, yet repetitive cash flow projection to a simple, automated process.</span></span> <span data-ttu-id="14fac-135">Når du automatiserer de kjedeligste aspektene ved kontantstrømprognoser, kan du fokusere på avgjørende beslutningstaking for å oppnå ønskede forretningsresultater.</span><span class="sxs-lookup"><span data-stu-id="14fac-135">Automating the most tedious aspects of cash flow forecasting lets you focus on critical decision making to drive desired business outcomes.</span></span>

## <a name="setting-up-dimensions-for-cash-flow-forecasting"></a><span data-ttu-id="14fac-136">Definere dimensjoner for kontantstrømprognoser</span><span class="sxs-lookup"><span data-stu-id="14fac-136">Setting up Dimensions for Cash flow forecasting</span></span>
<span data-ttu-id="14fac-137">En ny fane på siden **Oppsett for kontantstrømprognose** lar deg styre hvilke finansdimensjoner du vil bruke i arbeidsområdet **Kontantstrømprognose**.</span><span class="sxs-lookup"><span data-stu-id="14fac-137">A new tab on the **Cash flow forecasting setup** page lets you control what financial dimensions to use for filtering in the **Cash flow forecasting** workspace.</span></span> <span data-ttu-id="14fac-138">Denne fanen vises bare når funksjonen for kontantstrømprognose er aktivert.</span><span class="sxs-lookup"><span data-stu-id="14fac-138">This tab will only appear when the Cash flow forecasts feature is enabled.</span></span> 

<span data-ttu-id="14fac-139">I fanen **Dimensjoner** velger du dimensjoner som skal brukes til filtrering, fra listen over dimensjoner, og bruker piltastene til å flytte dem til høyre kolonne.</span><span class="sxs-lookup"><span data-stu-id="14fac-139">On the **Dimensions** tab, choose from the list of dimensions to use for filtering, and use the arrow keys to move them to the right-hand column.</span></span> <span data-ttu-id="14fac-140">Du kan bare velge to dimensjoner til filtrering av data for kontantstrømprognose.</span><span class="sxs-lookup"><span data-stu-id="14fac-140">Only two dimensions can be selected for filtering cash flow forecast data.</span></span> 

#### <a name="privacy-notice"></a><span data-ttu-id="14fac-141">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="14fac-141">Privacy notice</span></span>
<span data-ttu-id="14fac-142">Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.</span><span class="sxs-lookup"><span data-stu-id="14fac-142">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
