---
title: Konfigurere en betingede beslutninger i en arbeidsflyt
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
ms.sourcegitcommit: 3ee5334c87b2b0acae2afa6882feca63e3b9cc8e
ms.openlocfilehash: a01290b3e2810aa1762f2230e8d01d219d6b10bf
ms.contentlocale: nb-no
ms.lasthandoff: 12/18/2018

---

# <a name="configure-conditional-decisions-in-a-workflow"></a><span data-ttu-id="8f228-103">Konfigurere en betingede beslutninger i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="8f228-103">Configure conditional decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f228-104">Bruk deretter fremgangsmåten nedenfor for å konfigurere egenskapene for en betinget beslutning.</span><span class="sxs-lookup"><span data-stu-id="8f228-104">Use the following procedure to configure the properties of a conditional decision.</span></span>

<span data-ttu-id="8f228-105">En betinget beslutning er et punkt der en arbeidsflyt deles opp i to grener.</span><span class="sxs-lookup"><span data-stu-id="8f228-105">A conditional decision is a point at which a workflow divides into two branches.</span></span> <span data-ttu-id="8f228-106">Når du skal konfigurere en betinget beslutning i redigeringsprogrammet for arbeidsflyt, høyreklikker du den betingede beslutningen og klikker deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="8f228-106">To configure a conditional decision, in the workflow editor, right-click the conditional decision, and then click **Properties** to open the **Properties** form.</span></span>

## <a name="name-a-decision"></a><span data-ttu-id="8f228-107">Navngi en beslutning</span><span class="sxs-lookup"><span data-stu-id="8f228-107">Name a decision</span></span>

<span data-ttu-id="8f228-108">Følg denne fremgangsmåten for å angi et navn for en betinget beslutning.</span><span class="sxs-lookup"><span data-stu-id="8f228-108">Follow these steps to enter a name for a conditional decision.</span></span>

1. <span data-ttu-id="8f228-109">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="8f228-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8f228-110">I feltet **Navn** angir du et unikt navn på den betingede beslutningen.</span><span class="sxs-lookup"><span data-stu-id="8f228-110">In the **Name** field, enter a unique name for the conditional decision.</span></span>

## <a name="set-conditions"></a><span data-ttu-id="8f228-111"> Angi betingelser</span><span class="sxs-lookup"><span data-stu-id="8f228-111">Set conditions</span></span>

<span data-ttu-id="8f228-112">Systemet avgjør hvilken gren som skal brukes ved evaluering av det sendte dokumentet for å fastslå om det oppfyller angitte betingelser.</span><span class="sxs-lookup"><span data-stu-id="8f228-112">The system determines which branch is used by evaluating the submitted document to determine whether it meets specific conditions.</span></span>

1. <span data-ttu-id="8f228-113">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="8f228-113">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="8f228-114">Klikk **Legg til betingelse**.</span><span class="sxs-lookup"><span data-stu-id="8f228-114">Click **Add condition**.</span></span>
3. <span data-ttu-id="8f228-115">Angi en betingelse.</span><span class="sxs-lookup"><span data-stu-id="8f228-115">Enter a condition.</span></span>
4. <span data-ttu-id="8f228-116">Angi eventuelle ekstra betingelser som kreves.</span><span class="sxs-lookup"><span data-stu-id="8f228-116">Enter additional conditions, if they are required.</span></span>
5. <span data-ttu-id="8f228-117">Hvis du vil kontrollere om betingelsene du har skrevet inn, er riktig konfigurert, følger du denne fremgangsmåten:</span><span class="sxs-lookup"><span data-stu-id="8f228-117">To verify that the conditions that you entered are configured correctly, complete the following steps:</span></span>

    1. <span data-ttu-id="8f228-118">Klikk **Test** for å åpne skjemaet **Test arbeidsflytbetingelse**.</span><span class="sxs-lookup"><span data-stu-id="8f228-118">Click **Test** to open the **Test workflow condition** form.</span></span>
    2. <span data-ttu-id="8f228-119">Velg en post i **Valider betingelse**-området i skjemaet.</span><span class="sxs-lookup"><span data-stu-id="8f228-119">Select a record in the **Validate condition** area of the form.</span></span>
    3. <span data-ttu-id="8f228-120">Klikk **Test**.</span><span class="sxs-lookup"><span data-stu-id="8f228-120">Click **Test**.</span></span> <span data-ttu-id="8f228-121">Systemet evaluerer posten for å finne ut om den oppfyller betingelsene du definerte.</span><span class="sxs-lookup"><span data-stu-id="8f228-121">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="8f228-122">Klikk **OK** eller **Avbryt** for å gå tilbake til **Egenskaper**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="8f228-122">Click **OK** or **Cancel** to return to the **Properties** form.</span></span>

