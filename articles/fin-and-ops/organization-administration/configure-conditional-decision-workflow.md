---
title: Konfigurere en betinget beslutning i en arbeidsflyt
description: "Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for en betinget beslutning."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195703
ms.assetid: cd5554a4-210c-4c20-a7d3-4b1563c2b5df
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 597a6a254dcd623f9e7c59a0309eeedee1b5adee
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="configure-a-conditional-decision-in-a-workflow"></a><span data-ttu-id="f619d-103">Konfigurere en betinget beslutning i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="f619d-103">Configure a conditional decision in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="f619d-104">Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for en betinget beslutning.</span><span class="sxs-lookup"><span data-stu-id="f619d-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="f619d-105">En betinget beslutning er et punkt der en arbeidsflyt deles opp i to grener.</span><span class="sxs-lookup"><span data-stu-id="f619d-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="f619d-106">Når du skal konfigurere en betinget beslutning i redigeringsprogrammet for arbeidsflyt, høyreklikker du den betingede beslutningen og klikker deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="f619d-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="f619d-107">Navngi en beslutning</span><span class="sxs-lookup"><span data-stu-id="f619d-107">Name a decision</span></span>
<span data-ttu-id="f619d-108">Følg denne fremgangsmåten for å angi et navn for en betinget beslutning.</span><span class="sxs-lookup"><span data-stu-id="f619d-108">Follow these steps to enter a name for a conditional decision.</span></span>
1.  <span data-ttu-id="f619d-109">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="f619d-109">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="f619d-110">I feltet **Navn** angir du et unikt navn på den betingede beslutningen.</span><span class="sxs-lookup"><span data-stu-id="f619d-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="f619d-111"> Angi betingelser</span><span class="sxs-lookup"><span data-stu-id="f619d-111">Set conditions</span></span>
<span data-ttu-id="f619d-112">Systemet avgjør hvilken gren som skal brukes ved evaluering av det sendte dokumentet for å fastslå om det oppfyller angitte betingelser.</span><span class="sxs-lookup"><span data-stu-id="f619d-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>
1.  <span data-ttu-id="f619d-113">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="f619d-113">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="f619d-114">Klikk **Legg til betingelse**.</span><span class="sxs-lookup"><span data-stu-id="f619d-114">Click **Add condition**.</span></span>
3.  <span data-ttu-id="f619d-115">Angi en betingelse.</span><span class="sxs-lookup"><span data-stu-id="f619d-115">Enter a condition.</span></span>
4.  <span data-ttu-id="f619d-116">Angi eventuelle ekstra betingelser som kreves.</span><span class="sxs-lookup"><span data-stu-id="f619d-116">Enter additional conditions, if they are required.</span></span>
5.  <span data-ttu-id="f619d-117">Hvis du vil kontrollere om betingelsene du har skrevet inn, er riktig konfigurert, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="f619d-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>
    1.  <span data-ttu-id="f619d-118">Klikk **Test** for å åpne skjemaet **Test arbeidsflytbetingelse**.</span><span class="sxs-lookup"><span data-stu-id="f619d-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2.  <span data-ttu-id="f619d-119">Velg en post i **Valider betingelse**-området i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="f619d-119">Select a record in the **Validate condition** area of the form.</span></span>
    3.  <span data-ttu-id="f619d-120">Klikk **Test**.</span><span class="sxs-lookup"><span data-stu-id="f619d-120">Click **Test**.</span></span> <span data-ttu-id="f619d-121">Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.</span><span class="sxs-lookup"><span data-stu-id="f619d-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4.  <span data-ttu-id="f619d-122">Klikk **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="f619d-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>






