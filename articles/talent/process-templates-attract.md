---
title: Opprette en prosessmal i Attract
description: Dette emnet gir informasjon om hvordan du oppretter en prosessmal i Attract.
author: andreabichsel
manager: AnnBe
ms.date: 10/15/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-10-01
ms.dyn365.ops.version: AX 8.1
ms.openlocfilehash: ca04bb623b9ddd19f02efbf99289461a78ddd7f1
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "856629"
---
# <a name="create-a-process-template-in-attract"></a><span data-ttu-id="019e2-103">Opprette en prosessmal i Attract</span><span class="sxs-lookup"><span data-stu-id="019e2-103">Create a process template in Attract</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="019e2-104">En *mal for ansettelsesprosess* inneholder alle aktivitetene som bør tas med som en del av ansettelsesprosessen for en jobb.</span><span class="sxs-lookup"><span data-stu-id="019e2-104">A *hiring process template* contains all the activities that should be included as part of the hiring process for a job.</span></span> <span data-ttu-id="019e2-105">Dette emnet beskriver elementene i en prosessmal i Microsoft Dynamics 365 for Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="019e2-105">This topic describes the elements of a process template in Microsoft Dynamics 365 for Talent: Attract.</span></span> <span data-ttu-id="019e2-106">Det forklarer også hvordan du oppretter en mal.</span><span class="sxs-lookup"><span data-stu-id="019e2-106">It also explains how to create a template.</span></span>

> [!NOTE]
> <span data-ttu-id="019e2-107">Maloppretting av er en del av tillegget for omfattende ansettelse for Attract.</span><span class="sxs-lookup"><span data-stu-id="019e2-107">Template creation is part of the Comprehensive Hiring Add-on for Attract.</span></span>

## <a name="template-management"></a><span data-ttu-id="019e2-108">Malbehandling</span><span class="sxs-lookup"><span data-stu-id="019e2-108">Template management</span></span>

<span data-ttu-id="019e2-109">Organisasjoner kan bestemme om gruppemedlemmer eller bare administratorer kan opprette prosessmaler i Attract.</span><span class="sxs-lookup"><span data-stu-id="019e2-109">Organizations can decide whether team members or only admins can create process templates in Attract.</span></span> <span data-ttu-id="019e2-110">Hvis du vil konfigurere malbehandling, kan du gå til **Administrasjonssenter** \> **Malbehandling**.</span><span class="sxs-lookup"><span data-stu-id="019e2-110">To configure template management, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="019e2-111">Hvis du vil at gruppemedlemmer skal opprette sine egne maler, kan du aktivere malbehandling.</span><span class="sxs-lookup"><span data-stu-id="019e2-111">To let team members create their own templates, turn on template management.</span></span> <span data-ttu-id="019e2-112">Hvis du ikke aktiverer malbehandling, kan bare administratorer opprette maler.</span><span class="sxs-lookup"><span data-stu-id="019e2-112">If you don't turn on template management, only admins can create templates.</span></span>

## <a name="default-template"></a><span data-ttu-id="019e2-113">Standardmal</span><span class="sxs-lookup"><span data-stu-id="019e2-113">Default template</span></span>

<span data-ttu-id="019e2-114">Bare administratorer kan angi standardmalen.</span><span class="sxs-lookup"><span data-stu-id="019e2-114">Only admins can set the default template.</span></span> <span data-ttu-id="019e2-115">Standardmalen blir brukt hvis det ikke er valgt en mal når det opprettes en jobb.</span><span class="sxs-lookup"><span data-stu-id="019e2-115">The default template is used if a template isn't selected when a job is created.</span></span> <span data-ttu-id="019e2-116">For å angi standardmalen kan du gå til **Administrasjonssenter** \> **Malbehandling**.</span><span class="sxs-lookup"><span data-stu-id="019e2-116">To set the default template, go to **Admin Center** \> **Template management**.</span></span> <span data-ttu-id="019e2-117">På kortet for malen som skal være standardmalen, velg ellipseknappen (**...**), og velg deretter **Bruk som standard**.</span><span class="sxs-lookup"><span data-stu-id="019e2-117">On the card for the template that should be the default template, select the ellipsis button (**...**), and then select **Set as default**.</span></span>

## <a name="create-a-process-template"></a><span data-ttu-id="019e2-118">Opprette en prosessmal</span><span class="sxs-lookup"><span data-stu-id="019e2-118">Create a process template</span></span>

<span data-ttu-id="019e2-119">Administratorer, rekrutterere og ansettelsesansvarlige kan opprette prosessmaler.</span><span class="sxs-lookup"><span data-stu-id="019e2-119">Admins, recruiters, and hiring managers can create process templates.</span></span> <span data-ttu-id="019e2-120">En prosessmal består av *stadier* og *aktiviteter*.</span><span class="sxs-lookup"><span data-stu-id="019e2-120">A process template consists of *stages* and *activities*.</span></span> <span data-ttu-id="019e2-121">Stadier gruppere sammen én eller flere aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="019e2-121">Stages group together one or more activities.</span></span> <span data-ttu-id="019e2-122">Som standard har hver prosessmal kundeemne-, søknads- og tilbudsaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="019e2-122">By default, every process template has Prospect, Application, and Offer activities.</span></span> <span data-ttu-id="019e2-123">Stadiene som inneholder disse aktivitetene, kan gis nytt navn.</span><span class="sxs-lookup"><span data-stu-id="019e2-123">The stages that contain these activities can be renamed.</span></span> <span data-ttu-id="019e2-124">Du kan legge til flere faser ved å velge **+ Nytt stadium**.</span><span class="sxs-lookup"><span data-stu-id="019e2-124">You can add more stages by selecting **+ New Stage**.</span></span> <span data-ttu-id="019e2-125">Aktiviteter kan legges til et stadium ved å dra dem til det aktuelle stadiet, eller ved å dobbeltklikke dem i aktivitetslisten.</span><span class="sxs-lookup"><span data-stu-id="019e2-125">You can activities to a stage either by dragging them to the appropriate stage or by double-clicking them in the activity list.</span></span>

> [!NOTE]
> <span data-ttu-id="019e2-126">Navn på stadium er synlig for kandidater på siden **Søknadsstatus**.</span><span class="sxs-lookup"><span data-stu-id="019e2-126">Stage names are visible to candidates on the **Application status** page.</span></span> <span data-ttu-id="019e2-127">Dette bør du tenke over når du velger navn for stadier.</span><span class="sxs-lookup"><span data-stu-id="019e2-127">You should consider this fact when you choose names for stages.</span></span>

<span data-ttu-id="019e2-128">Hvis du vil ha mer informasjon om aktiviteter, kan du se [Aktiviteter i ansettelsesprosess i Attract](./activities-attract.md).</span><span class="sxs-lookup"><span data-stu-id="019e2-128">To learn more about activities, see [Hiring process activities in Attract](./activities-attract.md).</span></span>

<span data-ttu-id="019e2-129">Følg denne fremgangsmåten for å opprette en mal for ansettelsesprosess.</span><span class="sxs-lookup"><span data-stu-id="019e2-129">Follow these steps to create a hiring process template.</span></span>

1. <span data-ttu-id="019e2-130">Gå til **Maler**.</span><span class="sxs-lookup"><span data-stu-id="019e2-130">Go to **Templates**.</span></span>
2. <span data-ttu-id="019e2-131">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="019e2-131">Select **New**.</span></span>
3. <span data-ttu-id="019e2-132">I feltet **Malnavn** angir du et navn for malen, og deretter velger du **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="019e2-132">In the **Template name** field, enter a name for the template, and then select **Create**.</span></span>
4. <span data-ttu-id="019e2-133">I listen **Velg godkjenningsprosessen** velger du **Standard** for å kreve godkjenning for en jobb.</span><span class="sxs-lookup"><span data-stu-id="019e2-133">In the **Choose the approval process** list, select **Default** to require approval for a job.</span></span>
5. <span data-ttu-id="019e2-134">Velg for å aktivere eller deaktivere kundeemner.</span><span class="sxs-lookup"><span data-stu-id="019e2-134">Select to enable or disable prospects.</span></span>
6. <span data-ttu-id="019e2-135">Valgfritt: Legge til eller fjerne stadier.</span><span class="sxs-lookup"><span data-stu-id="019e2-135">Optional: Add or remove stages.</span></span>

    - <span data-ttu-id="019e2-136">Hvis du vil legge til et stadium, kan du velge **+ Nytt stadium**.</span><span class="sxs-lookup"><span data-stu-id="019e2-136">To add a stage, select **+ New Stage**.</span></span>
    - <span data-ttu-id="019e2-137">Hvis du vil fjerne et stadium, hold pekeren over det stadiet, og velg deretter papirkurv-knappen som vises.</span><span class="sxs-lookup"><span data-stu-id="019e2-137">To remove a stage, hover the pointer over the stage, and then select the trash can button that appears.</span></span>

        > [!NOTE]
        > <span data-ttu-id="019e2-138">Stadiene kundemne, søknad og tilbud kan ikke fjernes, men kan gis nytt navn.</span><span class="sxs-lookup"><span data-stu-id="019e2-138">Prospect, Application, and Offer stages can't be removed, but they can be renamed.</span></span>

7. <span data-ttu-id="019e2-139">Valgfritt: Legge til eller fjerne aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="019e2-139">Optional: Add or remove activities.</span></span>

    - <span data-ttu-id="019e2-140">Hvis du vil legge til en aktivitet, drar du den fra aktivitetslisten til høyre til det aktuelle stadiet.</span><span class="sxs-lookup"><span data-stu-id="019e2-140">To add an activity, drag it from the activity list on the right to the appropriate stage.</span></span> <span data-ttu-id="019e2-141">Du kan også dobbeltklikke aktiviteten, og deretter velge stadiet du vil legge den til.</span><span class="sxs-lookup"><span data-stu-id="019e2-141">Alternatively, double-click the activity, and then select the stage to add it to.</span></span>
    - <span data-ttu-id="019e2-142">Hvis du vil fjerne en aktivitet, utvider du den og velger deretter papirkurv-knappen på overskriften for aktiviteten.</span><span class="sxs-lookup"><span data-stu-id="019e2-142">To remove an activity, expand it, and then select the trash can button on the activity header.</span></span>

8. <span data-ttu-id="019e2-143">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="019e2-143">Select **Save**.</span></span>
