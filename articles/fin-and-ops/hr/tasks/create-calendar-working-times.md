--- 
title: Opprette en kalender og generere arbeidstider
description: Kalendere beskriver kapasitet og arbeidstid for operasjonsressurser.
author: kherr75
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Operations
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: d65fe0363e418f9c2e78bd78e802a4b0ea98599c
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-calendar-and-generate-working-times"></a><span data-ttu-id="74c9b-103">Opprette en kalender og generere arbeidstider</span><span class="sxs-lookup"><span data-stu-id="74c9b-103">Create a calendar and generate working times</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="74c9b-104">Kalendere beskriver kapasitet og arbeidstid for operasjonsressurser.</span><span class="sxs-lookup"><span data-stu-id="74c9b-104">Calendars describe the capacity and working times of operations resources.</span></span> <span data-ttu-id="74c9b-105">Denne fremgangsmåten vil hjelpe deg med å definere en arbeidskalender basert på en arbeidstidsmal.</span><span class="sxs-lookup"><span data-stu-id="74c9b-105">This procedure will help you define a work calendar based on a working time template.</span></span> <span data-ttu-id="74c9b-106">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="74c9b-106">You can walk through this procedure in demo data company USMF, or using your own data.</span></span>

1. <span data-ttu-id="74c9b-107">Gå til Alle arbeidsområder > Administrasjon av livssyklus for ressurs.</span><span class="sxs-lookup"><span data-stu-id="74c9b-107">Go to All workspaces > Resource lifecycle management.</span></span>
2. <span data-ttu-id="74c9b-108">Klikk Kalendere.</span><span class="sxs-lookup"><span data-stu-id="74c9b-108">Click Calendars.</span></span>
3. <span data-ttu-id="74c9b-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="74c9b-109">Click New.</span></span>
4. <span data-ttu-id="74c9b-110">Skriv inn en verdi i feltet Kalender.</span><span class="sxs-lookup"><span data-stu-id="74c9b-110">In the Calendar field, type a value.</span></span>
    * <span data-ttu-id="74c9b-111">Dette er ID-en for kalenderen som brukes som referanse når du tilordner kalendere, for eksempel til en operasjonsressurs eller en ressursgruppe.</span><span class="sxs-lookup"><span data-stu-id="74c9b-111">This is the ID of the calendar, which is used as a reference when assigning calendars, such as to an operations resource or a resource group.</span></span>  
5. <span data-ttu-id="74c9b-112">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="74c9b-112">In the Name field, type a value.</span></span>
6. <span data-ttu-id="74c9b-113">I feltet Standard arbeidsdag i timer angir du et tall.</span><span class="sxs-lookup"><span data-stu-id="74c9b-113">In the Standard work day in hours field, enter a number.</span></span>
7. <span data-ttu-id="74c9b-114">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="74c9b-114">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="74c9b-115">Klikk Driftstider.</span><span class="sxs-lookup"><span data-stu-id="74c9b-115">Click Working times.</span></span>
9. <span data-ttu-id="74c9b-116">Klikk Definer driftstid.</span><span class="sxs-lookup"><span data-stu-id="74c9b-116">Click Compose working times.</span></span>
    * <span data-ttu-id="74c9b-117">Generer arbeidstimer for hver dag i perioden der du vil kunne planlegge arbeidet.</span><span class="sxs-lookup"><span data-stu-id="74c9b-117">Generate working hours for each day in the period where you want to be able to schedule work.</span></span> <span data-ttu-id="74c9b-118">Som tiden går kan du generere arbeidstider for flere perioder.</span><span class="sxs-lookup"><span data-stu-id="74c9b-118">As time goes by, you can generate working times for additional periods.</span></span>  
10. <span data-ttu-id="74c9b-119">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="74c9b-119">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="74c9b-120">Dette er den første dagen denne kalenderen må være åpen.</span><span class="sxs-lookup"><span data-stu-id="74c9b-120">This is the first day that this calendar must be open.</span></span>  
11. <span data-ttu-id="74c9b-121">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="74c9b-121">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="74c9b-122">Dette er den siste dagen denne kalenderen er åpen.</span><span class="sxs-lookup"><span data-stu-id="74c9b-122">This is the last day that this calendar is open.</span></span>  
12. <span data-ttu-id="74c9b-123">I feltet Driftstidsmal angir eller velger du en verdi.</span><span class="sxs-lookup"><span data-stu-id="74c9b-123">In the Working time template field, enter or select a value.</span></span>
    * <span data-ttu-id="74c9b-124">Arbeidstidsmalen definerer arbeidstiden for hver dag i uken.</span><span class="sxs-lookup"><span data-stu-id="74c9b-124">The working time template defines the working hours for each day of the week.</span></span>  
13. <span data-ttu-id="74c9b-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="74c9b-125">Click OK.</span></span>
14. <span data-ttu-id="74c9b-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="74c9b-126">Close the page.</span></span>


