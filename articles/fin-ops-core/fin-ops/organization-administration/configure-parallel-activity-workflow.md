---
title: Konfigurere parallelle aktiviter i en arbeidsflyt
description: Hvis du vil konfigurere en parallell aktivitet, kan du fullføre fremgangsmåtene nedenfor i redigeringsprogrammet for arbeidsflyt.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 195753
ms.assetid: 6d0656df-b5af-4001-96e6-6f0fcc44d022
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 11b541c3e159b2c38e4dd2fa9f2ad08e4c1e4500
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179310"
---
# <a name="configure-parallel-activities-in-a-workflow"></a><span data-ttu-id="43ab1-103">Konfigurere parallelle aktiviter i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="43ab1-103">Configure parallel activities in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="43ab1-104">Hvis du vil konfigurere en parallell aktivitet, kan du fullføre fremgangsmåtene nedenfor i redigeringsprogrammet for arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="43ab1-104">To configure a parallel activity, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="43ab1-105">En parallell aktivitet består av grener i arbeidsflyten som kjører samtidig.</span><span class="sxs-lookup"><span data-stu-id="43ab1-105">A parallel activity consists of workflow branches that run at the same time.</span></span>

## <a name="name-a-parallel-activity"></a><span data-ttu-id="43ab1-106">Navngi en parallell aktivitet</span><span class="sxs-lookup"><span data-stu-id="43ab1-106">Name a parallel activity</span></span>

<span data-ttu-id="43ab1-107">Følg denne fremgangsmåten for å angi et navn for en parallell aktivitet.</span><span class="sxs-lookup"><span data-stu-id="43ab1-107">Follow these steps to enter a name for a parallel activity.</span></span>

1. <span data-ttu-id="43ab1-108">Høyreklikk den parallelle aktiviteten, og klikk deretter **Egenskaper** for å åpne **Egenskaper**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="43ab1-108">Right-click the parallel activity, and then click **Properties** to open the **Properties** form.</span></span>
2. <span data-ttu-id="43ab1-109">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="43ab1-109">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="43ab1-110">I feltet **Navn** angir du et unikt navn på den parallelle aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="43ab1-110">In the **Name** field, enter a unique name for the parallel activity.</span></span>
4. <span data-ttu-id="43ab1-111">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="43ab1-111">Click **Close**.</span></span>

## <a name="configure-the-branches-of-a-parallel-activity"></a><span data-ttu-id="43ab1-112">Konfigurere grenene til en parallell aktivitet</span><span class="sxs-lookup"><span data-stu-id="43ab1-112">Configure the branches of a parallel activity</span></span>

<span data-ttu-id="43ab1-113">Følg denne fremgangsmåten for å legge til og konfigurere grenene til denne parallelle aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="43ab1-113">Follow these steps to add and configure the branches of this parallel activity.</span></span>

1. <span data-ttu-id="43ab1-114">Dobbeltklikk den parallelle aktiviteten for å vise grenene til den parallelle aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="43ab1-114">Double-click the parallel activity to display the branches of the parallel activity.</span></span>
2. <span data-ttu-id="43ab1-115">Hvis du vil legge til en gren, kan du dra **Gren**-elementet fra **Arbeidsflytelementer**-området til et innsettingspunkt på lerretet.</span><span class="sxs-lookup"><span data-stu-id="43ab1-115">To add a branch, drag the **Branch** element from the **Workflow elements** area to an insertion point on the canvas.</span></span> <span data-ttu-id="43ab1-116">Den følgende illustrasjonen viser et innsettingspunkt.</span><span class="sxs-lookup"><span data-stu-id="43ab1-116">The following figure shows an insertion point.</span></span>

    ![Innsettingspunkt](./media/workflow_insertionpoint.gif)

    > [!NOTE]
    > <span data-ttu-id="43ab1-118">Rekkefølgen på grenene er ikke viktig fordi alle grenene til en parallell aktivitet kjøres samtidig.</span><span class="sxs-lookup"><span data-stu-id="43ab1-118">The order of the branches is not important because all the branches of a parallel activity run at the same time.</span></span>

3. <span data-ttu-id="43ab1-119">Hvis du vil konfigurere hver gren, kan du se [Konfigurere en parallell gren](configure-parallel-branch-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="43ab1-119">To configure each branch, see [Configure a parallel branch](configure-parallel-branch-workflow.md).</span></span>
