---
title: Opprette et masseansettelsesprosjekt
description: Dette hjelper med å definere et masseansettelsesprosjekt.
author: andreabichsel
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: HRMMassHireProject,  HRMMassHireLineCreate, HcmJobLookup, HcmPersonnelManagementWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d6d553c5762dcb456bd7178858c09129bc154349
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5467055"
---
# <a name="create-a-mass-hire-project"></a><span data-ttu-id="e3ada-103">Opprette et masseansettelsesprosjekt</span><span class="sxs-lookup"><span data-stu-id="e3ada-103">Create a mass hire project</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



<span data-ttu-id="e3ada-104">Dette hjelper med å definere et masseansettelsesprosjekt.</span><span class="sxs-lookup"><span data-stu-id="e3ada-104">This procedure walks through the process of setting up a mass hire project.</span></span> <span data-ttu-id="e3ada-105">En bemanningskonsulent kan bruke masseansettelsesprosjekter til å opprette flere stillinger og ansette en rekke arbeidere i disse stillingene.</span><span class="sxs-lookup"><span data-stu-id="e3ada-105">A recruiter can use mass hire projects to easily create multiple positions and hire a number of workers into those positions.</span></span> <span data-ttu-id="e3ada-106">Hvis du vil gjør dette, kan du gå til Personale > Rekruttering > Masseansettelsesprosjekter.</span><span class="sxs-lookup"><span data-stu-id="e3ada-106">To begin this procedure, go to Human resources > Recruitment > Mass hire projects.</span></span> <span data-ttu-id="e3ada-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="e3ada-107">The demo data company used to create this procedure is USMF.</span></span>

1. <span data-ttu-id="e3ada-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="e3ada-108">Click New.</span></span>
2. <span data-ttu-id="e3ada-109">Skriv inn en verdi i feltet Masseansettelsesprosjekt.</span><span class="sxs-lookup"><span data-stu-id="e3ada-109">In the Mass hire project field, type a value.</span></span>
3. <span data-ttu-id="e3ada-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e3ada-110">In the Description field, type a value.</span></span>
4. <span data-ttu-id="e3ada-111">Angi en dato i Prosjektstart-feltet.</span><span class="sxs-lookup"><span data-stu-id="e3ada-111">In the Project start field, enter a date.</span></span>
5. <span data-ttu-id="e3ada-112">Angi en dato i Prosjektavslutning-feltet.</span><span class="sxs-lookup"><span data-stu-id="e3ada-112">In the Project end field, enter a date.</span></span>
6. <span data-ttu-id="e3ada-113">Klikk Åpne prosjekt.</span><span class="sxs-lookup"><span data-stu-id="e3ada-113">Click Open project.</span></span>
7. <span data-ttu-id="e3ada-114">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="e3ada-114">Click Yes.</span></span>
8. <span data-ttu-id="e3ada-115">Klikk Opprett stillinger.</span><span class="sxs-lookup"><span data-stu-id="e3ada-115">Click Create positions.</span></span>
9. <span data-ttu-id="e3ada-116">I Antall-feltet angir du antallet stillinger du vil opprette.</span><span class="sxs-lookup"><span data-stu-id="e3ada-116">In the Quantity field, enter the number of positions that you want to create</span></span>
    * <span data-ttu-id="e3ada-117">Startdatoen blir ansettelsesdatoen for de nye arbeiderne.</span><span class="sxs-lookup"><span data-stu-id="e3ada-117">The Start date will become the Hire date for the new workers.</span></span>  
    * <span data-ttu-id="e3ada-118">Sluttdatoen blir avslutningsdatoen for de nye arbeiderne.</span><span class="sxs-lookup"><span data-stu-id="e3ada-118">The End date will be the Termination date for the new workers.</span></span>  
    * <span data-ttu-id="e3ada-119">Angi om de nye arbeiderne skal være ansatte eller oppdragstakere.</span><span class="sxs-lookup"><span data-stu-id="e3ada-119">Specify whether the new workers will be Employees or Contractors.</span></span>  
10. <span data-ttu-id="e3ada-120">I Jobb-feltet klikker du rullegardinlisten for å velge jobben du vil opprette stillinger for.</span><span class="sxs-lookup"><span data-stu-id="e3ada-120">In the Job field, click the drop-down button to select the job to create the positions for.</span></span>
11. <span data-ttu-id="e3ada-121">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e3ada-121">In the list, find and select the desired record.</span></span>
12. <span data-ttu-id="e3ada-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e3ada-122">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="e3ada-123">Standard verdi for fulltidsansatte kommer fra den valgte jobben.</span><span class="sxs-lookup"><span data-stu-id="e3ada-123">The default full-time equivalent value will come from the selected job.</span></span> <span data-ttu-id="e3ada-124">Du kan endre verdien ved behov.</span><span class="sxs-lookup"><span data-stu-id="e3ada-124">You can change this if needed.</span></span>  
    * <span data-ttu-id="e3ada-125">Velg eventuelt avdelingen for de nye stillingene.</span><span class="sxs-lookup"><span data-stu-id="e3ada-125">Optionally, select the Department for the new positions.</span></span>  
13. <span data-ttu-id="e3ada-126">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e3ada-126">Click OK.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]