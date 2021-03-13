---
title: Opprette kalendere og generere arbeidstider
description: Kalendere beskriver kapasitet og arbeidstid for operasjonsressurser. Denne artikkelen forklarer hvordan du definerer en arbeidskalender basert på en arbeidstidsmal.
author: andreabichsel
manager: tfehr
ms.date: 07/09/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OpResLifeCycleManagementWorkspace, WorkCalendarTable, WorkCalendarDate, HcmPersonnelManagementWorkspace, WrkCtrGroupDateCalendar, WrkCtrDateCalendar
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2fd297d9368472138fbe2db5a2133719cb1a9f18
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130307"
---
# <a name="create-calendars-and-generate-working-times"></a><span data-ttu-id="69bc7-104">Opprette kalendere og generere arbeidstider</span><span class="sxs-lookup"><span data-stu-id="69bc7-104">Create calendars and generate working times</span></span>



<span data-ttu-id="69bc7-105">Kalendere beskriver kapasitet og arbeidstid for operasjonsressurser.</span><span class="sxs-lookup"><span data-stu-id="69bc7-105">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="69bc7-106">Denne artikkelen forklarer hvordan du definerer en arbeidskalender basert på en arbeidstidsmal.</span><span class="sxs-lookup"><span data-stu-id="69bc7-106">This article explains how to define a work calendar based on a working time template.</span></span> <span data-ttu-id="69bc7-107">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="69bc7-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="69bc7-108">På startsiden velger du **Administrasjon av livssyklus for ressurs**.</span><span class="sxs-lookup"><span data-stu-id="69bc7-108">On the home page, select **Resource lifecycle management**.</span></span>
2. <span data-ttu-id="69bc7-109">Velg **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="69bc7-109">Select **Calendars**.</span></span>
3. <span data-ttu-id="69bc7-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="69bc7-110">Select **New**.</span></span>
4. <span data-ttu-id="69bc7-111">I **Kalender**-feltet klassifiserer du kalenderen.</span><span class="sxs-lookup"><span data-stu-id="69bc7-111">In the **Calendar** field, classify your calendar.</span></span> <span data-ttu-id="69bc7-112">Dette er ID-en for kalenderen som brukes som referanse når du tilordner kalendere, for eksempel til en operasjonsressurs eller en ressursgruppe.</span><span class="sxs-lookup"><span data-stu-id="69bc7-112">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="69bc7-113">Angi deretter et navn på kalenderen i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="69bc7-113">In the **Name** field, name your calendar.</span></span>
6. <span data-ttu-id="69bc7-114">I feltet **Standard arbeidsdag i timer** angir du et tall.</span><span class="sxs-lookup"><span data-stu-id="69bc7-114">In the **Standard work day in hours** field, enter a number.</span></span>
7. <span data-ttu-id="69bc7-115">Kontroller at raden er merket, og velg deretter **Driftstider** fra handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="69bc7-115">Make sure the row is selected, then select **Working times** from the Action Pane.</span></span>
8. <span data-ttu-id="69bc7-116">Velg **Definer driftstid**.</span><span class="sxs-lookup"><span data-stu-id="69bc7-116">Select **Compose working times**.</span></span> <span data-ttu-id="69bc7-117">Generer arbeidstimer for hver dag i perioden der du vil kunne planlegge arbeidet.</span><span class="sxs-lookup"><span data-stu-id="69bc7-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="69bc7-118">Som tiden går kan du generere arbeidstider for flere perioder.</span><span class="sxs-lookup"><span data-stu-id="69bc7-118">As time goes by, you can generate working times for additional periods.</span></span>  
9. <span data-ttu-id="69bc7-119">Angi en dato i **Fra dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="69bc7-119">In the **From date** field, enter a date.</span></span> <span data-ttu-id="69bc7-120">Dette er den første dagen denne kalenderen må være åpen.</span><span class="sxs-lookup"><span data-stu-id="69bc7-120">This is the first day that this calendar must be open.</span></span>  
10. <span data-ttu-id="69bc7-121">Angi en dato i **Til dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="69bc7-121">In the **To date field**, enter a date.</span></span> <span data-ttu-id="69bc7-122">Dette er den siste dagen denne kalenderen er åpen.</span><span class="sxs-lookup"><span data-stu-id="69bc7-122">This is the last day that this calendar is open.</span></span>  
11. <span data-ttu-id="69bc7-123">I feltet **Driftstidsmal** angir eller velger du en verdi.</span><span class="sxs-lookup"><span data-stu-id="69bc7-123">In the **Working time template** field, enter or select a value.</span></span> <span data-ttu-id="69bc7-124">Arbeidstidsmalen definerer arbeidstiden for hver dag i uken.</span><span class="sxs-lookup"><span data-stu-id="69bc7-124">The working time template defines the working hours for each day of the week.</span></span>  
12. <span data-ttu-id="69bc7-125">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="69bc7-125">Select **OK**.</span></span>
13. <span data-ttu-id="69bc7-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="69bc7-126">Close the page.</span></span>

