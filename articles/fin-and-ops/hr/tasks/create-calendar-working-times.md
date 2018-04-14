--- 
title: Opprette en kalender og generere arbeidstider
description: Kalendere beskriver kapasitet og arbeidstid for operasjonsressurser.
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations, Talent
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: a8dcef8d8ba6f6d41a997b5b0623cb9577ce00d3
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="create-a-calendar-and-generate-working-times"></a><span data-ttu-id="2823d-103">Opprette en kalender og generere arbeidstider</span><span class="sxs-lookup"><span data-stu-id="2823d-103">Create a calendar and generate working times</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2823d-104">Kalendere beskriver kapasitet og arbeidstid for operasjonsressurser.</span><span class="sxs-lookup"><span data-stu-id="2823d-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="2823d-105">Denne fremgangsmåten vil hjelpe deg med å definere en arbeidskalender basert på en arbeidstidsmal.</span><span class="sxs-lookup"><span data-stu-id="2823d-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="2823d-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="2823d-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="2823d-107">Gå til Alle arbeidsområder > Administrasjon av livssyklus for ressurs.</span><span class="sxs-lookup"><span data-stu-id="2823d-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="2823d-108">Klikk Kalendere.</span><span class="sxs-lookup"><span data-stu-id="2823d-108">Click Calendars.</span></span>
3. <span data-ttu-id="2823d-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2823d-109">Click New.</span></span>
4. <span data-ttu-id="2823d-110">Skriv inn en verdi i feltet Kalender.</span><span class="sxs-lookup"><span data-stu-id="2823d-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="2823d-111">Dette er ID-en for kalenderen som brukes som referanse når du tilordner kalendere, for eksempel til en operasjonsressurs eller en ressursgruppe.</span><span class="sxs-lookup"><span data-stu-id="2823d-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="2823d-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2823d-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="2823d-113">I feltet Standard arbeidsdag i timer angir du et tall.</span><span class="sxs-lookup"><span data-stu-id="2823d-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="2823d-114">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2823d-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="2823d-115">Klikk Driftstider.</span><span class="sxs-lookup"><span data-stu-id="2823d-115">Click Working times.</span></span>
9. <span data-ttu-id="2823d-116">Klikk Definer driftstid.</span><span class="sxs-lookup"><span data-stu-id="2823d-116">Click Compose working times.</span></span>
    * <span data-ttu-id="2823d-117">Generer arbeidstimer for hver dag i perioden der du vil kunne planlegge arbeidet.</span><span class="sxs-lookup"><span data-stu-id="2823d-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="2823d-118">Som tiden går kan du generere arbeidstider for flere perioder.</span><span class="sxs-lookup"><span data-stu-id="2823d-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="2823d-119">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="2823d-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="2823d-120">Dette er den første dagen denne kalenderen må være åpen.</span><span class="sxs-lookup"><span data-stu-id="2823d-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="2823d-121">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="2823d-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="2823d-122">Dette er den siste dagen denne kalenderen er åpen.</span><span class="sxs-lookup"><span data-stu-id="2823d-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="2823d-123">I feltet Driftstidsmal angir eller velger du en verdi.</span><span class="sxs-lookup"><span data-stu-id="2823d-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="2823d-124">Arbeidstidsmalen definerer arbeidstiden for hver dag i uken.</span><span class="sxs-lookup"><span data-stu-id="2823d-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="2823d-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2823d-125">Click OK.</span></span>
14. <span data-ttu-id="2823d-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2823d-126">Close the page.</span></span>


