---
title: Aktivere kontantstrømprognose (forhåndsversjon)
description: Dette emnet forklarer hvordan du aktiverer funksjonen for kontantstrømprognoser i Finance Insights.
author: ShivamPandey-msft
ms.date: 07/24/2020
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
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: f7c06eaeb79c1a2aa319cfa3d2ad8255bf716cd0
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5818734"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="09479-103">Aktivere kontantstrømprognose (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="09479-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="09479-104">Dette emnet forklarer hvordan du aktiverer funksjonen for kontantstrømprognoser i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="09479-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="09479-105">For å kunne bruke betalingsprognoser i kontantstrømmen må du konfigurere funksjonen for kundebetalingsprognoser som beskrevet i [Aktivere kundebetalingsprognoser](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="09479-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="09479-106">Bruk informasjon fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til å koble til den primære forekomsten av Azure SQL for dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="09479-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="09479-107">Kjør følgende Transact-SQL-kommando (T-SQL) for å aktivere testversjoner for sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="09479-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="09479-108">(Det kan hende at du må aktivere tilgang for IP-adressen din i LCS før du kan koble til Application Object Server \[AOS\] eksternt.)</span><span class="sxs-lookup"><span data-stu-id="09479-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="09479-109">Hvis distribusjonen av Microsoft Dynamics 365 Finance er en Service Fabric-distribusjon, kan du hoppe over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="09479-109">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="09479-110">Finance Insights-teamet skal allerede ha aktivert testversjonen for deg.</span><span class="sxs-lookup"><span data-stu-id="09479-110">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="09479-111">Hvis du ikke ser funksjonene i arbeidsområdet **Funksjonsbehandling**, eller hvis du får problemer når du prøver å aktivere dem, kontakter du <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="09479-111">If you don't see the features in the **Feature management** workspace, or if experience issues when you try to turn them on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="09479-112">Åpne arbeidsområdet **Funksjonsbehandling**, og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="09479-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="09479-113">Velg **Se etter oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="09479-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="09479-114">Aktiver følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="09479-114">Turn on the following features:</span></span>

        - <span data-ttu-id="09479-115">Ny rutenettkontroll</span><span class="sxs-lookup"><span data-stu-id="09479-115">New grid control</span></span>
        - <span data-ttu-id="09479-116">Gruppering i rutenett (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="09479-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="09479-117">Kundebetalingsforutsigelser (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="09479-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="09479-118">Kontantstrømprognoser (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="09479-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="09479-119">Gå til **Kontant- og bankbehandling \> Oppsett for kontantstrømprognose**, og legg til likviditetskontoene som skal tas med i prognosene.</span><span class="sxs-lookup"><span data-stu-id="09479-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="09479-120">Hvis likviditetskontoer ikke er opprettet, kan ikke kontantstrømmen genereres.</span><span class="sxs-lookup"><span data-stu-id="09479-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="09479-121">Gå til **Kontant- og bankbehandling \> Oppsett \> Finance Insights (forhåndsversjon) \> Kontantstrømprognoser (forhåndsversjon)**, og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="09479-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="09479-122">Velg **Aktiver funksjon** i fanen **Kontantstrømprognose**.</span><span class="sxs-lookup"><span data-stu-id="09479-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="09479-123">Velg **Opprett prognosemodell**.</span><span class="sxs-lookup"><span data-stu-id="09479-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="09479-124">Hvis du vil ha mer informasjon om funksjonen for kontantstrømprognose, kan du se [Kontantstrømprognose](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="09479-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="09479-125">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="09479-125">Privacy notice</span></span>

<span data-ttu-id="09479-126">Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.</span><span class="sxs-lookup"><span data-stu-id="09479-126">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]