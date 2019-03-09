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
ms.openlocfilehash: 73626ad21dfe2be7400f321a3eee272c896276f3
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "367346"
---
# <a name="configure-parallel-branches-in-a-workflow"></a><span data-ttu-id="b91db-103">Konfigurere parallelle avdelinger i en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="b91db-103">Configure parallel branches in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b91db-104">Hvis du vil konfigurere en parallell avdeling, kan du fullføre fremgangsmåtene nedenfor i redigeringsprogrammet for arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="b91db-104">To configure a parallel branch, complete the following procedures in the workflow editor.</span></span>

<span data-ttu-id="b91db-105">En parallell avdeling er egentlig en arbeidsflyt som kjøres i konteksten til en overordnet arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="b91db-105">A parallel branch is essentially a workflow that runs in the context of a parent workflow.</span></span>

## <a name="name-a-branch"></a><span data-ttu-id="b91db-106">Navn på en avdeling</span><span class="sxs-lookup"><span data-stu-id="b91db-106">Name a branch</span></span>

<span data-ttu-id="b91db-107">Følg denne fremgangsmåten for å angi et navn for en parallell avdeling.</span><span class="sxs-lookup"><span data-stu-id="b91db-107">Follow these steps to enter a name for a parallel branch.</span></span>

1. <span data-ttu-id="b91db-108">Høyreklikk den parallelle avdelingen, og klikk deretter **Egenskaper**.</span><span class="sxs-lookup"><span data-stu-id="b91db-108">Right-click the parallel branch, and then click **Properties**.</span></span> <span data-ttu-id="b91db-109">**Egenskaper**-skjemaet vises.</span><span class="sxs-lookup"><span data-stu-id="b91db-109">The **Properties** form is displayed.</span></span>
2. <span data-ttu-id="b91db-110">Klikk **Grunnleggende innstillinger** i ruten til venstre.</span><span class="sxs-lookup"><span data-stu-id="b91db-110">In the left pane, click **Basic Settings**.</span></span>
3. <span data-ttu-id="b91db-111">I feltet **Navn** angir du et unikt navn på den parallelle avdelingen.</span><span class="sxs-lookup"><span data-stu-id="b91db-111">In the **Name** field, enter a unique name for the parallel branch.</span></span>
4. <span data-ttu-id="b91db-112">Klikk **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="b91db-112">Click **Close**.</span></span>

## <a name="design-and-configure-the-elements-of-a-branch"></a><span data-ttu-id="b91db-113">Utforme og konfigurere elementene for en avdeling</span><span class="sxs-lookup"><span data-stu-id="b91db-113">Design and configure the elements of a branch</span></span>

<span data-ttu-id="b91db-114">Følg denne fremgangsmåten for å utforme og konfigurere elementene for en parallell avdeling.</span><span class="sxs-lookup"><span data-stu-id="b91db-114">Follow these steps to design and configure the elements of a parallel branch.</span></span>

1. <span data-ttu-id="b91db-115">Dobbeltklikk den parallelle avdelingen.</span><span class="sxs-lookup"><span data-stu-id="b91db-115">Double-click the parallel branch.</span></span>
2. <span data-ttu-id="b91db-116">Dra arbeidsflytelementer til arbeidsområdet, og konfigurer deretter elementene, akkurat som når du skal opprette en ny arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="b91db-116">Drag workflow elements onto the canvas, and then configure the elements, just as you would to create any other workflow.</span></span> <span data-ttu-id="b91db-117">Hvis du vil ha mer informasjon, kan du se [Opprette en arbeidsflyt](create-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="b91db-117">For more information, see [Create a workflow](create-workflow.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b91db-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b91db-118">Additional resources</span></span>

[<span data-ttu-id="b91db-119">Opprette en arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="b91db-119">Create a workflow</span></span>](create-workflow.md)
