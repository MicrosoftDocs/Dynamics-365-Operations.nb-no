---
title: Konfigurere parallelle avdelinger i en arbeidsflyt
description: Hvis du vil konfigurere en parallell avdeling, kan du fullføre fremgangsmåtene nedenfor i redigeringsprogrammet for arbeidsflyt.
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
ms.custom: 196043
ms.assetid: dfdae2b8-6a4f-4760-b339-b755c66f3f89
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2058eaac77282946559cae11fcec8152658fc96b
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2019
ms.locfileid: "2811363"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="287d2-103">Konfigurere parallelle avdelinger i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="287d2-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="287d2-104">Hvis du vil konfigurere en parallell avdeling, kan du fullføre fremgangsmåtene nedenfor i redigeringsprogrammet for arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="287d2-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="287d2-105">En parallell avdeling er egentlig en arbeidsflyt som kjøres i konteksten til en overordnet arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="287d2-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="287d2-106">Navn på en avdeling</span><span class="sxs-lookup"><span data-stu-id="287d2-106">Name a branch</span></span>

<span data-ttu-id="287d2-107">Følg denne fremgangsmåten for å angi et navn for en parallell avdeling.</span><span class="sxs-lookup"><span data-stu-id="287d2-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="287d2-108">Høyreklikk den parallelle avdelingen, og klikk deretter **Egenskaper**.</span><span class="sxs-lookup"><span data-stu-id="287d2-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="287d2-109">**Egenskaper**-skjemaet vises.</span><span class="sxs-lookup"><span data-stu-id="287d2-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="287d2-110">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="287d2-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="287d2-111">I feltet **Navn** angir du et unikt navn på den parallelle avdelingen.</span><span class="sxs-lookup"><span data-stu-id="287d2-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="287d2-112">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="287d2-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="287d2-113">Utforme og konfigurere elementene for en avdeling</span><span class="sxs-lookup"><span data-stu-id="287d2-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="287d2-114">Følg denne fremgangsmåten for å utforme og konfigurere elementene for en parallell avdeling.</span><span class="sxs-lookup"><span data-stu-id="287d2-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="287d2-115">Dobbeltklikk den parallelle avdelingen.</span><span class="sxs-lookup"><span data-stu-id="287d2-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="287d2-116">Dra arbeidsflytelementer til arbeidsområdet, og konfigurer deretter elementene, akkurat som når du skal opprette en ny arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="287d2-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="287d2-117">Hvis du vil ha mer informasjon, kan du se [Oversikt over å opprette arbeidsflyter](create-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="287d2-117">For more information, see [Create workflows overview](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="287d2-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="287d2-118">Additional resources</span></span>

[<span data-ttu-id="287d2-119">Oversikt over å opprette arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="287d2-119">Create workflows overview</span></span>](create-workflow.md)
