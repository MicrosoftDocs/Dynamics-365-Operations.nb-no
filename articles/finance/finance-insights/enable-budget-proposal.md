---
title: Aktivere budsjettforslag (forhåndsversjon)
description: Dette emnet forklarer hvordan du aktiverer funksjonen for budsjettforslag i Finance Insights.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
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
ms.openlocfilehash: 59cf40e8bf69734c5f3645997ff0b07c29d4f40e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4995146"
---
# <a name="enable-budget-proposals-preview"></a><span data-ttu-id="3a33e-103">Aktivere budsjettforslag (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="3a33e-103">Enable budget proposals (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="3a33e-104">Dette emnet forklarer hvordan du aktiverer funksjonen for budsjettforslag i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="3a33e-104">This topic explains how to turn on the Budget proposal feature in Finance Insights.</span></span>

1. <span data-ttu-id="3a33e-105">Bruk informasjon fra miljøsiden i Microsoft Dynamics Lifecycle Services (LCS) til å koble til den primære forekomsten av Azure SQL for dette miljøet.</span><span class="sxs-lookup"><span data-stu-id="3a33e-105">Use information from the environment page in Microsoft Dynamics Lifecycle Services (LCS) to connect to the primary instance of Azure SQL for that environment.</span></span> <span data-ttu-id="3a33e-106">Kjør følgende Transact-SQL-kommando (T-SQL) for å aktivere testversjoner for sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="3a33e-106">Run the following Transact-SQL (T-SQL) command to turn on flights for the sandbox environment.</span></span> <span data-ttu-id="3a33e-107">(Det kan hende at du må aktivere tilgang for IP-adressen din i LCS før du kan koble til Application Object Server \[AOS\] eksternt.)</span><span class="sxs-lookup"><span data-stu-id="3a33e-107">(You might have to turn on access for your IP address in LCS before you can connect remotely to Application Object Server \[AOS\].)</span></span>

    `INSERT INTO SYSFLIGHTING (FLIGHTNAME, ENABLED) VALUES ('BudgetIntelligentBudgetRegisterProposalFeature', 1)`

    > [!NOTE]
    > <span data-ttu-id="3a33e-108">Hvis distribusjonen av Microsoft Dynamics 365 Finance er en Service Fabric-distribusjon, kan du hoppe over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="3a33e-108">If your deployment of Microsoft Dynamics 365 Finance is a Service Fabric deployment, you can skip this step.</span></span> <span data-ttu-id="3a33e-109">Finance Insights-teamet skal allerede ha aktivert testversjonen for deg.</span><span class="sxs-lookup"><span data-stu-id="3a33e-109">The Finance Insights team should already have turned on the flight for you.</span></span> <span data-ttu-id="3a33e-110">Hvis du ikke ser funksjonen i arbeidsområdet **Funksjonsbehandling** eller får problemer når du prøver å aktivere den, kan du sende e-post til [teamet for forhåndsversjon av appen Finance Insights](mailto:fiap@microsoft.com).</span><span class="sxs-lookup"><span data-stu-id="3a33e-110">If you don't see the feature in the **Feature management** workspace, or if you experience issues when you try to turn it on, send email to the [Finance Insights App Preview team](mailto:fiap@microsoft.com).</span></span>

2. <span data-ttu-id="3a33e-111">Åpne arbeidsområdet **Funksjonsbehandling**, og følg denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="3a33e-111">Open the **Feature management** workspace, and follow these steps:</span></span>

    1. <span data-ttu-id="3a33e-112">Velg **Se etter oppdateringer**.</span><span class="sxs-lookup"><span data-stu-id="3a33e-112">Select **Check for updates**.</span></span>
    2. <span data-ttu-id="3a33e-113">Søk etter **Budsjettforslag**, og aktiver denne funksjonen.</span><span class="sxs-lookup"><span data-stu-id="3a33e-113">Search for **Budget proposal**, and turn on that feature.</span></span>

3. <span data-ttu-id="3a33e-114">Gå til **Budsjettering \> Oppsett \> Grunnleggende budsjettering \> Budsjettforslag (forhåndsversjon)**, og velg **Aktiver funksjon**.</span><span class="sxs-lookup"><span data-stu-id="3a33e-114">Go to **Budgeting \> Setup \> basic Budgeting \> Budget proposal (preview)**, and select **Enable feature**.</span></span>

#### <a name="privacy-notice"></a><span data-ttu-id="3a33e-115">Personvernerklæring</span><span class="sxs-lookup"><span data-stu-id="3a33e-115">Privacy notice</span></span>
<span data-ttu-id="3a33e-116">Forhåndsversjoner (1) kan ha redusert personvern og færre sikkerhetstiltak enn Dynamics 365 Finance and Operations-tjenesten, (2) er ikke inkludert i serviceavtalen (SLA) for denne tjenesten, (3) må ikke brukes til å behandle personlige data eller andre data som er underlagt juridiske eller forskriftsmessige krav, og (4) har begrenset støtte.</span><span class="sxs-lookup"><span data-stu-id="3a33e-116">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
