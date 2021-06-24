---
title: Aktivere kundebetalingsprognoser (forhåndsversjon)
description: Dette emnet forklarer hvordan du aktiverer og konfigurerer funksjonen for kundebetalingsprognoser i Finance Insights.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-05-29
ms.dyn365.ops.version: AX 10.0.12
ms.openlocfilehash: ae957f592ad9a1237817fec5d4172295f9a53020
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222592"
---
# <a name="enable-customer-payment-predictions-preview"></a><span data-ttu-id="e38a7-103">Aktivere kundebetalingsprognoser (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="e38a7-103">Enable customer payment predictions (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="e38a7-104">Dette emnet forklarer hvordan du aktiverer og konfigurerer funksjonen for kundebetalingsprognoser i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="e38a7-104">This topic explains how to turn on and configure the Customer payment predictions feature in Finance insights.</span></span> <span data-ttu-id="e38a7-105">Du aktiverer funksjonen i arbeidsområdet **Funksjonsbehandling** og angir konfigurasjonsinnstillinger på siden **Parametere for økonomisk innsikt**.</span><span class="sxs-lookup"><span data-stu-id="e38a7-105">You turn on the feature in the **Feature management** workspace and enter configuration settings on the **Financial insights parameters** page.</span></span> <span data-ttu-id="e38a7-106">Dette emnet inneholder også informasjon som kan hjelpe deg å bruke funksjonen på en effektiv måte.</span><span class="sxs-lookup"><span data-stu-id="e38a7-106">This topic also includes information that can help you effectively use the feature.</span></span>

> [!NOTE]
> <span data-ttu-id="e38a7-107">Før du fullfører trinnene nedenfor, må du fullføre de nødvendige trinnene i emnet [Konfigurere for Finance Insights](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="e38a7-107">Before you complete the following steps, be sure to complete the prerequisite steps in the [Configure for Finance insights](configure-for-fin-insites.md) topic.</span></span>

1. <span data-ttu-id="e38a7-108">Bruk informasjon fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til å koble til den primære forekomsten av Azure SQL for dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="e38a7-108">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="e38a7-109">Kjør følgende Transact-SQL-kommando (T-SQL) for å aktivere testversjoner for sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="e38a7-109">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="e38a7-110">(Det kan hende at du må aktivere tilgang for IP-adressen din i LCS før du kan koble til Application Object Server \[AOS\] eksternt.)</span><span class="sxs-lookup"><span data-stu-id="e38a7-110">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('PayPredEnableFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="e38a7-111">Hopp over dette trinnet hvis du bruker versjon 10.0.20 eller nyere, eller hvis du bruker en Service Fabric-distribusjon.</span><span class="sxs-lookup"><span data-stu-id="e38a7-111">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="e38a7-112">Finance Insights-teamet skal allerede ha aktivert testversjonen for deg.</span><span class="sxs-lookup"><span data-stu-id="e38a7-112">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="e38a7-113">Hvis du ikke ser funksjonen i arbeidsområdet **Funksjonsbehandling** eller får problemer når du prøver å aktivere den, kontakter du <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="e38a7-113">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span> 

2. <span data-ttu-id="e38a7-114">Slik aktiverer du funksjonen for innsikt i kundebetaling:</span><span class="sxs-lookup"><span data-stu-id="e38a7-114">Turn on the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="e38a7-115">Gå til **Systemadministrasjon \> Arbeidsområder \> Funksjonsbehandling**.</span><span class="sxs-lookup"><span data-stu-id="e38a7-115">Go to **System administration \> Workspaces \> Feature management**.</span></span>
    2. <span data-ttu-id="e38a7-116">Finn funksjonen kalt **Innsikt i kundebetaling (forhåndsversjon)**.</span><span class="sxs-lookup"><span data-stu-id="e38a7-116">Find the feature that is named **Customer payment insights (preview)**.</span></span>
    3. <span data-ttu-id="e38a7-117">Velg **Aktiver nå**.</span><span class="sxs-lookup"><span data-stu-id="e38a7-117">Select **Enable now**.</span></span>

    <span data-ttu-id="e38a7-118">Funksjonen for innsikt i kundebetaling er nå aktivert og klar til å konfigureres.</span><span class="sxs-lookup"><span data-stu-id="e38a7-118">The Customer payment insights feature is now turned on and ready to be configured.</span></span>

3. <span data-ttu-id="e38a7-119">Slik konfigurerer du funksjonen for innsikt i kundebetaling:</span><span class="sxs-lookup"><span data-stu-id="e38a7-119">Configure the Customer payment insights feature:</span></span>

    1. <span data-ttu-id="e38a7-120">Gå til **Kreditt og innkreving \> Oppsett \> Finance Insights \> Parametere for økonomisk innsikt**.</span><span class="sxs-lookup"><span data-stu-id="e38a7-120">Go to **Credit and collections \> Setup \> Finance insights \> Finance insights parameters**.</span></span>

        <span data-ttu-id="e38a7-121">[![Siden Parametere for økonomisk innsikt før funksjonen er konfigurert](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span><span class="sxs-lookup"><span data-stu-id="e38a7-121">[![Financial insights parameters page before the feature is configured](./media/finance-insights-parameters.png)](./media/finance-insights-parameters.png)</span></span>

    2. <span data-ttu-id="e38a7-122">Velg koblingen **Vis datafeltene som brukes i prognosemodellen** i fanen **Innsikt i kundebetaling** på siden **Parametere for økonomisk innsikt** for å åpne siden **Datafelter for prognosemodell**.</span><span class="sxs-lookup"><span data-stu-id="e38a7-122">On the **Financial insights parameters** page, on the **Customer payment insights** tab, select the **View the data fields used in the prediction model** link to open the **Data fields for prediction model** page.</span></span> <span data-ttu-id="e38a7-123">Der kan du vise standardlisten over felt som brukes til å opprette en prognosemodell basert på kunstig intelligens (AI) for kundebetalingsprognoser.</span><span class="sxs-lookup"><span data-stu-id="e38a7-123">There, you can view the default list of fields that are used to create the artificial intelligence (AI) prediction model for customer payment predictions.</span></span>

        <span data-ttu-id="e38a7-124">Hvis du vil bruke standardlisten over felt til å opprette en prognosemodell, lukker du siden **Datafelter for prognosemodell**, og deretter setter du alternativet **Aktiver funksjon** til **Ja** på siden **Parametere for økonomisk innsikt**.</span><span class="sxs-lookup"><span data-stu-id="e38a7-124">To use the default list of fields to create the prediction model, close the **Data fields for prediction model** page, and then, on the **Financial insights parameters** page, set the **Enable feature** option to **Yes**.</span></span>

    3. <span data-ttu-id="e38a7-125">Angi transaksjonsperioden «svært sent» for å definere hva prognosesamlingen **Svært sent** betyr for firmaet.</span><span class="sxs-lookup"><span data-stu-id="e38a7-125">Specify the "very late" transaction period to define what the **Very late** prediction bucket means for your business.</span></span>

        <span data-ttu-id="e38a7-126">For hver åpne faktura forutsier systemet sannsynligheten for betaling i tre samlinger: **Til planlagt tid**, **For sent** og **Svært sent**.</span><span class="sxs-lookup"><span data-stu-id="e38a7-126">For each open invoice, the system predicts the probability of payment in three buckets: **On time**, **Late**, and **Very late**.</span></span>

        - <span data-ttu-id="e38a7-127">**Til planlagt tid** – Denne samlingen inneholder betalinger som forutsies å bli betalt på eller før forfallsdatoen for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="e38a7-127">**On time** – This bucket includes payments that are predicted to be paid on or before the transaction due date.</span></span>
        - <span data-ttu-id="e38a7-128">**For sent** – Denne samlingen inneholder betalinger som forutsies å bli betalt etter forfallsdatoen for transaksjonen, men før starten på transaksjonsperioden Svært sent.</span><span class="sxs-lookup"><span data-stu-id="e38a7-128">**Late** – This bucket includes payments that are predicted to be paid after the transaction due date but before the start of the "very late" transaction period.</span></span>
        - <span data-ttu-id="e38a7-129">**Svært sent** – Denne samlingen inneholder betalinger som forutsies å bli betalt etter starten på transaksjonsperioden Svært sent.</span><span class="sxs-lookup"><span data-stu-id="e38a7-129">**Very late** – This bucket includes payments that are predicted to be paid after the start of the "very late" transaction period.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e38a7-130">Hvis du endrer transaksjonsperioden Svært sent og velger **Endre terskel for For sent** etter at AI-prognosemodellen for kundebetalinger er opprettet, slettes den eksisterende prognosemodellen, og det opprettes en ny modell.</span><span class="sxs-lookup"><span data-stu-id="e38a7-130">If you change the "very late" transaction period and select **Change late threshold** after the AI prediction model for customer payments has been created, the existing prediction model is deleted, and a new model is created.</span></span> <span data-ttu-id="e38a7-131">Den nye prognosemodellen flytter transaksjoner til Svært sent-perioden, basert på innstillingene som ble angitt for å definere den.</span><span class="sxs-lookup"><span data-stu-id="e38a7-131">The new prediction model will move transactions into the "very late" period, based on the settings that were entered to define it.</span></span>

    4. <span data-ttu-id="e38a7-132">Når du er ferdig å definere transaksjonsperioden Svært sent, velger du **Opprett prognosemodell** for å opprette en prognosemodell.</span><span class="sxs-lookup"><span data-stu-id="e38a7-132">After you've finished defining the "very late" transaction period, select **Create prediction model** to create the prediction model.</span></span> <span data-ttu-id="e38a7-133">**Prognosemodell**-delen på siden **Parametere for økonomisk innsikt** viser statusen for prognosemodellen.</span><span class="sxs-lookup"><span data-stu-id="e38a7-133">The **Prediction model** section on the **Financial insights parameters** page shows the status of the prediction model.</span></span>

        > [!NOTE]
        > <span data-ttu-id="e38a7-134">Når du oppretter en prognosemodell, kan du når som helst velge **Tilbakestill modellopprettelse** for å starte prosessen på nytt.</span><span class="sxs-lookup"><span data-stu-id="e38a7-134">At any time while the prediction model is being created, you can select **Reset model creation** to restart the process.</span></span>

    <span data-ttu-id="e38a7-135">Funksjonen er nå konfigurert og klar til bruk.</span><span class="sxs-lookup"><span data-stu-id="e38a7-135">The feature has now been configured and is ready to be used.</span></span>

<span data-ttu-id="e38a7-136">Etter at funksjonen er aktivert og konfigurert, og prognosemodellen er opprettet og fungerer, viser **Prognosemodell**-delen på siden **Parametere for økonomisk innsikt** nøyaktigheten til modellen, som vist i illustrasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="e38a7-136">After the feature has been turned on and configured, and the prediction model has been created and is working, the **Prediction model** section of the **Financial insights parameters** page shows the accuracy of the model, as shown in the following illustration.</span></span>

<span data-ttu-id="e38a7-137">[![Nøyaktigheten til prognosemodellen på siden Parametere for økonomisk innsikt](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span><span class="sxs-lookup"><span data-stu-id="e38a7-137">[![Accuracy of the prediction model on the Financial insights parameters page](./media/finance-insights-parameters-accuracy.png)](./media/finance-insights-parameters-accuracy.png)</span></span>

## <a name="release-details"></a><span data-ttu-id="e38a7-138">Frigivelsesdetaljer</span><span class="sxs-lookup"><span data-stu-id="e38a7-138">Release details</span></span>

<span data-ttu-id="e38a7-139">Den offentlige forhåndsversjonen av Finance Insights er tilgjengelig for prøvedistribusjoner i USA, Europa og Storbritannia.</span><span class="sxs-lookup"><span data-stu-id="e38a7-139">Finance insights public preview is available for trial deployments in the United States of America, Europe, and the United Kingdom.</span></span> <span data-ttu-id="e38a7-140">Microsoft legger gradvis til støtte for flere områder.</span><span class="sxs-lookup"><span data-stu-id="e38a7-140">Microsoft is incrementally adding support for more regions.</span></span>

<span data-ttu-id="e38a7-141">Funksjoner i offentlige forhåndsversjoner kan og bør bare aktiveres i sandkassemiljøer på lag 2.</span><span class="sxs-lookup"><span data-stu-id="e38a7-141">Public preview features can and should be turned on only in Tier-2 sandbox environments.</span></span> <span data-ttu-id="e38a7-142">Oppsett og modeller for kunstig intelligens som er opprettet i et sandkassemiljø, kan ikke overføres til et produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="e38a7-142">Setup and AI models that are created in a sandbox environment can't be migrated to a production environment.</span></span> <span data-ttu-id="e38a7-143">Hvis du vil ha mer informasjon, kan du se [Ekstra vilkår for bruk for Microsoft Dynamics 365-forhåndsversjoner](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span><span class="sxs-lookup"><span data-stu-id="e38a7-143">For more information, see [Supplemental Terms of Use for Microsoft Dynamics 365 Previews](../../fin-ops-core/fin-ops/get-started/public-preview-terms.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
