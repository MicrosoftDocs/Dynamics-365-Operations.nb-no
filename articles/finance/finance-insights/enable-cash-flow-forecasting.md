---
title: Aktivere kontantstrømprognose (forhåndsversjon)
description: Dette emnet forklarer hvordan du aktiverer funksjonen for kontantstrømprognoser i Finance Insights.
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
ms.search.validFrom: 2020-07-24
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: ba8acb2191291e2abed5cabf234c19fe09e6c8ff
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222564"
---
# <a name="enable-cash-flow-forecasting-preview"></a><span data-ttu-id="5785a-103">Aktivere kontantstrømprognose (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="5785a-103">Enable cash flow forecasting (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="5785a-104">Dette emnet forklarer hvordan du aktiverer funksjonen for kontantstrømprognoser i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="5785a-104">This topic explains how to turn on the Cash flow forecasts feature in Finance Insights.</span></span>

> [!NOTE]
> <span data-ttu-id="5785a-105">For å kunne bruke betalingsprognoser i kontantstrømmen må du konfigurere funksjonen for kundebetalingsprognoser som beskrevet i [Aktivere kundebetalingsprognoser](enable-cust-paymnt-prediction.md).</span><span class="sxs-lookup"><span data-stu-id="5785a-105">To use payment predictions in the cash flow, you must set up the Customer payment predictions feature as described in [Enable customer payment predictions](enable-cust-paymnt-prediction.md).</span></span>

1. <span data-ttu-id="5785a-106">Bruk informasjon fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til å koble til den primære forekomsten av Azure SQL for dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="5785a-106">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="5785a-107">Kjør følgende Transact-SQL-kommando (T-SQL) for å aktivere testversjoner for sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="5785a-107">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="5785a-108">(Det kan hende at du må aktivere tilgang for IP-adressen din i LCS før du kan koble til Application Object Server \[AOS\] eksternt.)</span><span class="sxs-lookup"><span data-stu-id="5785a-108">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('CashflowInsightsFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="5785a-109">Hopp over dette trinnet hvis du bruker versjon 10.0.20 eller nyere, eller hvis du bruker en Service Fabric-distribusjon.</span><span class="sxs-lookup"><span data-stu-id="5785a-109">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="5785a-110">Finance Insights-teamet skal allerede ha aktivert testversjonen for deg.</span><span class="sxs-lookup"><span data-stu-id="5785a-110">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="5785a-111">Hvis du ikke ser funksjonen i arbeidsområdet **Funksjonsbehandling** eller får problemer når du prøver å aktivere den, kontakter du <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="5785a-111">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>
  
2. <span data-ttu-id="5785a-112">Åpne arbeidsområdet **Funksjonsbehandling**, og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="5785a-112">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="5785a-113">Velg **Se etter oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="5785a-113">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="5785a-114">Aktiver følgende funksjoner:</span><span class="sxs-lookup"><span data-stu-id="5785a-114">Turn on the following features:</span></span>

        - <span data-ttu-id="5785a-115">Ny rutenettkontroll</span><span class="sxs-lookup"><span data-stu-id="5785a-115">New grid control</span></span>
        - <span data-ttu-id="5785a-116">Gruppering i rutenett (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="5785a-116">Grouping in grids (preview)</span></span> 
        - <span data-ttu-id="5785a-117">Kundebetalingsforutsigelser (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="5785a-117">Customer payment predictions (preview)</span></span>
        - <span data-ttu-id="5785a-118">Kontantstrømprognoser (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="5785a-118">Cash flow forecasts (preview)</span></span>

3. <span data-ttu-id="5785a-119">Gå til **Kontant- og bankbehandling \> Oppsett for kontantstrømprognose**, og legg til likviditetskontoene som skal tas med i prognosene.</span><span class="sxs-lookup"><span data-stu-id="5785a-119">Go to **Cash and bank management \> Cash flow forecast setup**, and add the liquidity accounts that should be included in the forecasts.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5785a-120">Hvis likviditetskontoer ikke er opprettet, kan ikke kontantstrømmen genereres.</span><span class="sxs-lookup"><span data-stu-id="5785a-120">If liquidity accounts aren't set up, the cash flow can't be generated.</span></span>

4. <span data-ttu-id="5785a-121">Gå til **Kontant- og bankbehandling \> Oppsett \> Finance Insights (forhåndsversjon) \> Kontantstrømprognoser (forhåndsversjon)**, og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="5785a-121">Go to **Cash and bank management \> Setup \> Finance Insights (preview) \> Cash flow forecasts (preview)**, and follow these steps:</span></span>

    1. <span data-ttu-id="5785a-122">Velg **Aktiver funksjon** i fanen **Kontantstrømprognose**.</span><span class="sxs-lookup"><span data-stu-id="5785a-122">On the **Cash flow forecast** tab, select **Enable feature**.</span></span>
    2. <span data-ttu-id="5785a-123">Velg **Opprett prognosemodell**.</span><span class="sxs-lookup"><span data-stu-id="5785a-123">Select **Create prediction model**.</span></span>

<span data-ttu-id="5785a-124">Hvis du vil ha mer informasjon om funksjonen for kontantstrømprognose, kan du se [Kontantstrømprognose](cash-flow-forecast-intro.md).</span><span class="sxs-lookup"><span data-stu-id="5785a-124">For more information about the cash flow forecasting capability, see [Cash flow forecasting](cash-flow-forecast-intro.md).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
