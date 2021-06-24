---
title: Aktivere budsjettforslag (forhåndsversjon)
description: Dette emnet forklarer hvordan du aktiverer funksjonen for budsjettforslag i Finance Insights.
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
ms.openlocfilehash: 948a3e051e5964c5c773cefd90c8587cf833a450
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222540"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="93171-103">Aktivere budsjettforslag (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="93171-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="93171-104">Dette emnet forklarer hvordan du aktiverer funksjonen for budsjettforslag i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="93171-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="93171-105">Bruk informasjon fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til å koble til den primære forekomsten av Azure SQL for dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="93171-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="93171-106">Kjør følgende Transact-SQL-kommando (T-SQL) for å aktivere testversjoner for sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="93171-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="93171-107">(Det kan hende at du må aktivere tilgang for IP-adressen din i LCS før du kan koble til Application Object Server \[AOS\] eksternt.)</span><span class="sxs-lookup"><span data-stu-id="93171-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="93171-108">Hopp over dette trinnet hvis du bruker versjon 10.0.20 eller nyere, eller hvis du bruker en Service Fabric-distribusjon.</span><span class="sxs-lookup"><span data-stu-id="93171-108">Skip this step if you're using version 10.0.20 or later, or if you're using a Service Fabric deployment.</span></span> <span data-ttu-id="93171-109">Finance Insights-teamet skal allerede ha aktivert testversjonen for deg.</span><span class="sxs-lookup"><span data-stu-id="93171-109">The Finance insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="93171-110">Hvis du ikke ser funksjonen i arbeidsområdet **Funksjonsbehandling** eller får problemer når du prøver å aktivere den, kontakter du <fiap@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="93171-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, contact <fiap@microsoft.com>.</span></span>

2. <span data-ttu-id="93171-111">Åpne arbeidsområdet **Funksjonsbehandling**, og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="93171-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="93171-112">Velg **Se etter oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="93171-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="93171-113">Søk etter **Budsjettforslag**, og aktiver denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="93171-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="93171-114">Gå til **Budsjettering \> Oppsett \> Grunnleggende budsjettering \> Budsjettforslag (forhåndsversjon)**, og velg **Aktiver funksjon**.</span><span class="sxs-lookup"><span data-stu-id="93171-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
