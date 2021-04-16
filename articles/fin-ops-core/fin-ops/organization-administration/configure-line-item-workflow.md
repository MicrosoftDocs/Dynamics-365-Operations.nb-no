---
title: Konfigurere arbeidsflyter for linjeelement
description: Dette emnet forklarer hvordan du konfigurerer et arbeidsflytelement for linjeelement.
author: ChrisGarty
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 195833
ms.assetid: 3237347e-71d5-4569-bc9a-0d0fc9410b78
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 84da7080542b4cc2ecc487b0a1331482fb69b998
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747911"
---
# <a name="configure-line-item-workflows"></a><span data-ttu-id="cc4c3-103">Konfigurere arbeidsflyter for linjeelement</span><span class="sxs-lookup"><span data-stu-id="cc4c3-103">Configure line-item workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc4c3-104">Dette emnet forklarer hvordan du konfigurerer et arbeidsflytelement for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-104">This topic explains how to configure a line-item workflow element.</span></span>

<span data-ttu-id="cc4c3-105">Når du skal konfigurere en arbeidsflyt for linjeelement i redigeringsprogrammet for arbeidsflyt, høyreklikker du elementet og klikker deretter **Egenskaper** for å åpne **Egenskaper**-siden.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-105">To configure a line-item workflow element, in the workflow editor, right-click the element, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="cc4c3-106">Du kan deretter bruke fremgangsmåten nedenfor for å konfigurere egenskapene for arbeidsflyten for linjeelementet.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-106">Then use the following procedures to configure the properties of the line-item workflow element.</span></span>

## <a name="name-the-line-item-workflow-element"></a><span data-ttu-id="cc4c3-107">Navnet på arbeidsflyten for linjeelement</span><span class="sxs-lookup"><span data-stu-id="cc4c3-107">Name the line-item workflow element</span></span>

<span data-ttu-id="cc4c3-108">Følg denne fremgangsmåten for å sette et navn på arbeidsflyten for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-108">Follow these steps to enter a name for the line-item workflow element.</span></span>

1. <span data-ttu-id="cc4c3-109">Klikk på **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="cc4c3-110">I **Navn**-feltet angir du et unikt navn på arbeidsflyten for linjeelement.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-110">In the **Name** field, enter a unique name for the line-item workflow element.</span></span>

## <a name="specify-whether-the-same-workflow-is-used-to-process-all-line-items"></a><span data-ttu-id="cc4c3-111">Angi om den samme arbeidsflyten skal brukes til å behandle alle linjeelementer</span><span class="sxs-lookup"><span data-stu-id="cc4c3-111">Specify whether the same workflow is used to process all line items</span></span>

<span data-ttu-id="cc4c3-112">Følg denne fremgangsmåten for å angi om den samme arbeidsflyten skal brukes til å behandle alle linjeelementene på et dokument.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-112">Follow these steps to specify whether the same workflow is used to process all the line items on a document.</span></span>

1. <span data-ttu-id="cc4c3-113">Klikk på **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="cc4c3-114">Hvis den samme arbeidsflyten skal behandle alle linjeelementene på et dokument, klikker du **Aktiver én arbeidsflyt for alle linjeelementer**.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-114">If the same workflow should process all the line items on a document, click **Invoke a single workflow for all line-items**.</span></span> <span data-ttu-id="cc4c3-115">Velg deretter arbeidsflyten som skal brukes til å behandle linjeelementene.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-115">Then select the workflow to use to process the line items.</span></span>
3. <span data-ttu-id="cc4c3-116">Hvis en bestemt arbeidsflyt skal behandle linjeelementer som oppfyller et bestemt sett med betingelser, klikker du **Aktiver en arbeidsflyt for hvert linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-116">If a specific workflow should process line items that meet a specific set of conditions, click **Invoke a workflow for each line-item**.</span></span> <span data-ttu-id="cc4c3-117">Følg denne fremgangsmåten for å definere settet med betingelser:</span><span class="sxs-lookup"><span data-stu-id="cc4c3-117">Then follow these steps to define the set of conditions:</span></span>

    1. <span data-ttu-id="cc4c3-118">Klikk på **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-118">Click **Add**.</span></span>
    2. <span data-ttu-id="cc4c3-119">Velg betingelsen i tabellen.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-119">Select the condition in the table.</span></span>
    3. <span data-ttu-id="cc4c3-120">I fanen **Betingelsesnavn** skriver du inn et navn for settet med betingelser som du definerer.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-120">On the **Condition name** tab, enter a name for the set of conditions that you're defining.</span></span>
    4. <span data-ttu-id="cc4c3-121">Klikk på **Legg til betingelse** for å angi en betingelse.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-121">Click **Add condition** to enter a condition.</span></span>
    5. <span data-ttu-id="cc4c3-122">Angi eventuelle ekstra betingelser som kreves.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-122">Enter any additional conditions that are required.</span></span>
    6. <span data-ttu-id="cc4c3-123">Hvis du vil kontrollere om settet med betingelsene du har skrevet inn, er riktig konfigurert, klikker du **Test**.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-123">To verify that the set of conditions that you entered is configured correctly, click **Test**.</span></span> <span data-ttu-id="cc4c3-124">På **Test arbeidsflytbetingelse**-siden i **Valider betingelse**-området velger du en post, og deretter klikker du **Test**.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-124">On the **Test workflow condition** page, in the **Validate condition** area, select a record, and then click **Test**.</span></span> <span data-ttu-id="cc4c3-125">Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-125">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span> <span data-ttu-id="cc4c3-126">Klikk på **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-siden.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-126">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

    <span data-ttu-id="cc4c3-127">I fanen **Arbeidsflyt** velger du arbeidsflyten som skal brukes til å behandle linjeelementer som oppfyller settet med betingelser som du har definert.</span><span class="sxs-lookup"><span data-stu-id="cc4c3-127">On the **Workflow** tab, select the workflow select the workflow to use to process line items that meet the set of conditions that you defined.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]