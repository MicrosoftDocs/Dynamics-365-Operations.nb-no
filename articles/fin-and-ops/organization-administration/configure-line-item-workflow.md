---
title: Konfigurere arbeidsflyter for linjeelement
description: Dette emnet forklarer hvordan du konfigurerer et arbeidsflytelement for linjeelement.
author: sericks007
manager: AnnBe
ms.date: 11/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 764d4c9049d94ebcd55c61654aa2f4133b35bae6
ms.openlocfilehash: 0a57baa3ecae727721f62477cfc5fa41f60ad06d
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---

# <a name="configure-line-item-workflows"></a><span data-ttu-id="4dcae-103">Konfigurere arbeidsflyter for linjeelement</span><span class="sxs-lookup"><span data-stu-id="4dcae-103">Configure line-item workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4dcae-104">Dette emnet forklarer hvordan du konfigurerer et arbeidsflytelement for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="4dcae-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="4dcae-105">Når du skal konfigurere en arbeidsflyt for linjeelement i redigeringsprogrammet for arbeidsflyt, høyreklikker du elementet og klikker deretter **Egenskaper** for å åpne **Egenskaper**-siden.</span><span class="sxs-lookup"><span data-stu-id="4dcae-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="4dcae-106">Du kan deretter bruke fremgangsmåten nedenfor for å konfigurere egenskapene for arbeidsflyten for linjeelementet.</span><span class="sxs-lookup"><span data-stu-id="4dcae-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="4dcae-107">Navnet på arbeidsflyten for linjeelement</span><span class="sxs-lookup"><span data-stu-id="4dcae-107">Name the line-item workflow element</span></span>
<span data-ttu-id="4dcae-108">Følg denne fremgangsmåten for å sette et navn på arbeidsflyten for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="4dcae-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1.  <span data-ttu-id="4dcae-109">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="4dcae-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="4dcae-110">I **Navn**-feltet angir du et unikt navn på arbeidsflyten for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="4dcae-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="4dcae-111">Angi om den samme arbeidsflyten skal brukes til å behandle alle linjeelementer</span><span class="sxs-lookup"><span data-stu-id="4dcae-111">Specify whether the same workflow is used to process all line items</span></span>
<span data-ttu-id="4dcae-112">Følg denne fremgangsmåten for å angi om den samme arbeidsflyten skal brukes til å behandle alle linjeelementene på et dokument.</span><span class="sxs-lookup"><span data-stu-id="4dcae-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1.  <span data-ttu-id="4dcae-113">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="4dcae-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="4dcae-114">Hvis den samme arbeidsflyten skal behandle alle linjeelementene på et dokument, klikker du **Aktiver én arbeidsflyt for alle linjeelementer**.</span><span class="sxs-lookup"><span data-stu-id="4dcae-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="4dcae-115">Velg deretter arbeidsflyten som skal brukes til å behandle linjeelementene.</span><span class="sxs-lookup"><span data-stu-id="4dcae-115">Then select the workflow to use to process the line items.</span></span>
3.  <span data-ttu-id="4dcae-116">Hvis en bestemt arbeidsflyt skal behandle linjeelementer som oppfyller et bestemt sett med betingelser, klikker du **Aktiver en arbeidsflyt for hvert linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="4dcae-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="4dcae-117">Følg denne fremgangsmåten for å definere settet med betingelser:</span><span class="sxs-lookup"><span data-stu-id="4dcae-117">Then follow these steps to define the set of conditions:</span></span>
    1.  <span data-ttu-id="4dcae-118">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="4dcae-118">Click **Add**.</span></span>
    2.  <span data-ttu-id="4dcae-119">Velg betingelsen i tabellen.</span><span class="sxs-lookup"><span data-stu-id="4dcae-119">Select the condition in the table.</span></span>
    3.  <span data-ttu-id="4dcae-120">I kategorien **Betingelsesnavn** skriver du inn et navn for settet med betingelser som du definerer.</span><span class="sxs-lookup"><span data-stu-id="4dcae-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4.  <span data-ttu-id="4dcae-121">Klikk **Legg til betingelse** for å angi en betingelse.</span><span class="sxs-lookup"><span data-stu-id="4dcae-121">Click **Add condition** to enter a condition.</span></span>
    5.  <span data-ttu-id="4dcae-122">Angi eventuelle ekstra betingelser som kreves.</span><span class="sxs-lookup"><span data-stu-id="4dcae-122">Enter any additional conditions that are required.</span></span>
    6.  <span data-ttu-id="4dcae-123">Hvis du vil kontrollere om settet med betingelsene du har skrevet inn, er riktig konfigurert, klikker du **Test**.</span><span class="sxs-lookup"><span data-stu-id="4dcae-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="4dcae-124">På **Test arbeidsflytbetingelse**-siden i **Valider betingelse**-området velger du en post, og deretter klikker du **Test**.</span><span class="sxs-lookup"><span data-stu-id="4dcae-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="4dcae-125">Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.</span><span class="sxs-lookup"><span data-stu-id="4dcae-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="4dcae-126">Klikk **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-siden.</span><span class="sxs-lookup"><span data-stu-id="4dcae-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="4dcae-127">I kategorien **Arbeidsflyt** velger du arbeidsflyten som skal brukes til å behandle linjeelementer som oppfyller settet med betingelser som du har definert.</span><span class="sxs-lookup"><span data-stu-id="4dcae-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>





