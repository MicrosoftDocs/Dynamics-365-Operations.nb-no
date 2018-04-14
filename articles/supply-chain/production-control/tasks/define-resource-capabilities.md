--- 
title: Definere ressursfunksjoner
description: "Ressursfunksjoner beskriver hva operasjonsressursene kan utføre."
author: sorenva
manager: AnnBe
ms.date: 10/27/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: sorenand
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6cd8b8e409348b4df1144ad58700882879012766
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="define-resource-capabilities"></a><span data-ttu-id="bbdca-103">Definere ressursfunksjoner</span><span class="sxs-lookup"><span data-stu-id="bbdca-103">Define resource capabilities</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bbdca-104">Ressursfunksjoner beskriver hva operasjonsressursene kan utføre.</span><span class="sxs-lookup"><span data-stu-id="bbdca-104">Resource capabilities describe what operations resources can do.</span></span> <span data-ttu-id="bbdca-105">Under planlegging sammenlignes kravene for hver jobb og en operasjon mot mulighetene i de tilgjengelige ressursene.</span><span class="sxs-lookup"><span data-stu-id="bbdca-105">During scheduling, the requirements of each job and operation are matched against the capabilities of the available resources.</span></span> <span data-ttu-id="bbdca-106">Denne oppgaveveiledning hjelper deg med å opprette en ressursfunksjon og tilordne den til en ressurs.</span><span class="sxs-lookup"><span data-stu-id="bbdca-106">This task guide will help you create a resource capability and assign it to a resource.</span></span> <span data-ttu-id="bbdca-107">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="bbdca-107">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-resource-capability"></a><span data-ttu-id="bbdca-108">Opprett en ressursfunksjon</span><span class="sxs-lookup"><span data-stu-id="bbdca-108">Create a resource capability</span></span>
1. <span data-ttu-id="bbdca-109">Gå til Ressursfunksjoner.</span><span class="sxs-lookup"><span data-stu-id="bbdca-109">Go to Resource capabilities.</span></span>
2. <span data-ttu-id="bbdca-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="bbdca-110">Click New.</span></span>
3. <span data-ttu-id="bbdca-111">Skriv inn IDen til ressursfunksjonen i Funksjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="bbdca-111">In the Capability field, type the ID of the resource capability.</span></span>
    * <span data-ttu-id="bbdca-112">For en bestemt operasjon kan du bruke funksjons-IDen til å angi at ressurser må ha denne muligheten til å utføre operasjonen.</span><span class="sxs-lookup"><span data-stu-id="bbdca-112">For a given operation, you use the capability ID to specify that resources must have this capability to perform the operation.</span></span>  
4. <span data-ttu-id="bbdca-113">Angi en kort beskrivelse av funksjonen i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="bbdca-113">In the Description field, enter a description of the capability.</span></span>

## <a name="assign-capability-to-a-resource"></a><span data-ttu-id="bbdca-114">Tilordne funksjon til en ressurs</span><span class="sxs-lookup"><span data-stu-id="bbdca-114">Assign capability to a resource</span></span>
1. <span data-ttu-id="bbdca-115">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="bbdca-115">Click Add.</span></span>
2. <span data-ttu-id="bbdca-116">Skriv inn IDen til ressursen i Ressurs-feltet.</span><span class="sxs-lookup"><span data-stu-id="bbdca-116">In the Resource field, type the ID of the resource.</span></span>
    * <span data-ttu-id="bbdca-117">En ressursfunksjon kan tilordnes til én eller flere ressurser.</span><span class="sxs-lookup"><span data-stu-id="bbdca-117">A resource capability can be assigned to one or more resources.</span></span>  
3. <span data-ttu-id="bbdca-118">Angi en dato i Utløp-feltet.</span><span class="sxs-lookup"><span data-stu-id="bbdca-118">In the Expiration field, enter a date.</span></span>
    * <span data-ttu-id="bbdca-119">Du kan bruke dette feltet til å angi at en ressurs har funksjonen i en begrenset periode.</span><span class="sxs-lookup"><span data-stu-id="bbdca-119">You can use this field to specify that a resource has the capability for only a limited time.</span></span>  
4. <span data-ttu-id="bbdca-120">Angi et tall i Prioritet-feltet.</span><span class="sxs-lookup"><span data-stu-id="bbdca-120">In the Priority field, enter a number.</span></span>
    * <span data-ttu-id="bbdca-121">Når du planlegger jobber og operasjoner, kan du angi om du velger ressursene etter prioritet.</span><span class="sxs-lookup"><span data-stu-id="bbdca-121">When you schedule jobs and operations, you can specify whether to select resources by priority.</span></span> <span data-ttu-id="bbdca-122">Hvis du vil gjøre dette, og mer enn én ressurs kan utføre jobben eller operasjonen etter ønsket dato, velges ressursen som har lavest prioritet i forhold til den nødvendige kapasiteten.</span><span class="sxs-lookup"><span data-stu-id="bbdca-122">If you choose to do this, and more than one resource can perform the job or operation by the requested date, the resource that has the lowest priority with respect to the required capability is selected.</span></span>  
5. <span data-ttu-id="bbdca-123">Angi et nummer i Nivå-feltet.</span><span class="sxs-lookup"><span data-stu-id="bbdca-123">In the Level field, enter a number.</span></span>
    * <span data-ttu-id="bbdca-124">Når du angir at en jobb eller operasjon krever en bestemt funksjon, kan du også angi det minste tillatelsesnivå som kreves.</span><span class="sxs-lookup"><span data-stu-id="bbdca-124">When you specify that a job or operation requires a particular capability, you can also specify the minimum level that is required.</span></span> <span data-ttu-id="bbdca-125">Bruk ressursnivået til å skille mellom ressurser som kan utføre den samme jobben, men med forskjellige hastigheter, styrker, størrelser og så videre.</span><span class="sxs-lookup"><span data-stu-id="bbdca-125">Use the capability level to differentiate resources that can perform the same job, but at different speeds, strengths, sizes, and so on.</span></span>  


