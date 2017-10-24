---
title: Konfigurere en parallell aktivitet i en arbeidsflyt
description: "Hvis du vil konfigurere en parallell aktivitet, kan du fullføre fremgangsmåtene nedenfor i redigeringsprogrammet for arbeidsflyt."
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 5473327c0665c9183746eb8125c7a368fbedc21e
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="configure-a-parallel-activity-in-a-workflow"></a><span data-ttu-id="05915-103">Konfigurere en parallell aktivitet i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="05915-103">Configure a parallel activity in a workflow</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="05915-104">Hvis du vil konfigurere en parallell aktivitet, kan du fullføre fremgangsmåtene nedenfor i redigeringsprogrammet for arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="05915-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="05915-105">En parallell aktivitet består av grener i arbeidsflyten som kjører samtidig.</span><span class="sxs-lookup"><span data-stu-id="05915-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="05915-106">Navngi en parallell aktivitet</span><span class="sxs-lookup"><span data-stu-id="05915-106">Name a parallel activity</span></span>
<span data-ttu-id="05915-107">Følg denne fremgangsmåten for å angi et navn for en parallell aktivitet.</span><span class="sxs-lookup"><span data-stu-id="05915-107">Follow these steps to enter a name for a parallel activity.</span></span>
1.  <span data-ttu-id="05915-108">Høyreklikk den parallelle aktiviteten, og klikk deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="05915-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2.  <span data-ttu-id="05915-109">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="05915-109">In the left pane, click **Basic Settings**.</span></span>
3.  <span data-ttu-id="05915-110">I feltet **Navn** angir du et unikt navn på den parallelle aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="05915-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4.  <span data-ttu-id="05915-111">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="05915-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="05915-112">Konfigurere grenene til en parallell aktivitet</span><span class="sxs-lookup"><span data-stu-id="05915-112">Configure the branches of a parallel activity</span></span>
<span data-ttu-id="05915-113">Følg denne fremgangsmåten for å legge til og konfigurere grenene til denne parallelle aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="05915-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>
1.  <span data-ttu-id="05915-114">Dobbeltklikk den parallelle aktiviteten for å vise grenene til den parallelle aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="05915-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2.  <span data-ttu-id="05915-115">Hvis du vil legge til en gren, kan du dra **Gren**-elementet fra **Arbeidsflytelementer**-området til et innsettingspunkt på lerretet.</span><span class="sxs-lookup"><span data-stu-id="05915-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="05915-116">Den følgende illustrasjonen viser et innsettingspunkt. ![Innsettingspunkt](./media/workflow_insertionpoint.gif)</span><span class="sxs-lookup"><span data-stu-id="05915-116">The following figure shows an insertion point.![Insertion point](./media/workflow_insertionpoint.gif)</span></span>
    | <span data-ttu-id="05915-117">**Obs!**</span><span class="sxs-lookup"><span data-stu-id="05915-117">**Note**</span></span>                                                                                                         |
    |------------------------------------------------------------------------------------------------------------------|
    | <span data-ttu-id="05915-118">Rekkefølgen på grenene er ikke viktig fordi alle grenene til en parallell aktivitet kjøres samtidig.</span><span class="sxs-lookup"><span data-stu-id="05915-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span> |

3.  <span data-ttu-id="05915-119">Hvis du vil konfigurere hver gren, kan du se [Konfigurere en parallell gren](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="05915-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>






