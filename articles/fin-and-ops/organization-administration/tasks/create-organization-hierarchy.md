---
title: Opprette et organisasjonshierarki
description: Bruk følgende fremgangsmåte for å opprette et organisasjonshierarki.
author: sericks007
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 203a586b06a13a7c67f246384152d17627e22041
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545551"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="05e9c-103">Opprette et organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="05e9c-103">Create an organization hierarchy</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="05e9c-104">Bruk følgende fremgangsmåte for å opprette et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="05e9c-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="05e9c-105">Du kan bruke organisasjonshierarkier for å vise og rapportere for bedriften fra ulike perspektiver.</span><span class="sxs-lookup"><span data-stu-id="05e9c-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="05e9c-106">Du kan for eksempel definere ett hierarki for avgiftsrapportering, juridisk eller lovpålagt rapportering.</span><span class="sxs-lookup"><span data-stu-id="05e9c-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="05e9c-107">Du kan deretter definere et annet hierarki for å rapportere finansinformasjon som ikke er lovpålagt, men som brukes til intern rapportering.</span><span class="sxs-lookup"><span data-stu-id="05e9c-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 



<span data-ttu-id="05e9c-108">Før du oppretter et organisasjonshierarki, må du opprette organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="05e9c-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="05e9c-109">Hvis du vil ha mer informasjon, kan du se oppgavene "Opprette en juridisk enhet" eller "Opprette en driftsenhet".</span><span class="sxs-lookup"><span data-stu-id="05e9c-109">For more information, see the “Create a legal entity” or “Create an operating unit” tasks.</span></span> <span data-ttu-id="05e9c-110">Du kan også opprette avdelinger og team.</span><span class="sxs-lookup"><span data-stu-id="05e9c-110">You can also create departments and teams.</span></span> 



<span data-ttu-id="05e9c-111">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="05e9c-111">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-hierarchy"></a><span data-ttu-id="05e9c-112">Opprett et hierarki</span><span class="sxs-lookup"><span data-stu-id="05e9c-112">Create a hierarchy</span></span>
1. <span data-ttu-id="05e9c-113">Gå til Organisasjonsstyring > Organisasjoner > Organisasjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="05e9c-113">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
2. <span data-ttu-id="05e9c-114">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="05e9c-114">Click New.</span></span>
3. <span data-ttu-id="05e9c-115">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="05e9c-115">In the Name field, type a value.</span></span>
4. <span data-ttu-id="05e9c-116">Klikk Tilordne formål.</span><span class="sxs-lookup"><span data-stu-id="05e9c-116">Click Assign purpose.</span></span>
5. <span data-ttu-id="05e9c-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="05e9c-117">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="05e9c-118">Velg et formål som skal tilordnes til organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="05e9c-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="05e9c-119">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="05e9c-119">Click Add.</span></span>
7. <span data-ttu-id="05e9c-120">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="05e9c-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="05e9c-121">Finn hierarkiet du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="05e9c-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="05e9c-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="05e9c-122">Click OK.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="05e9c-123">Legge til organisasjoner i hierarkiet</span><span class="sxs-lookup"><span data-stu-id="05e9c-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="05e9c-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="05e9c-124">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="05e9c-125">Velg hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="05e9c-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="05e9c-126">Klikk Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="05e9c-126">Click View hierarchy.</span></span>
    * <span data-ttu-id="05e9c-127">Legg til organisasjoner etter behov.</span><span class="sxs-lookup"><span data-stu-id="05e9c-127">Add organizations, as necessary.</span></span>  
    * <span data-ttu-id="05e9c-128">Hvis du vil legge til en organisasjon, klikker du Rediger og deretter Sett inn for å legge til organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="05e9c-128">To add an organization, click Edit and then Insert to add the organization.</span></span>     <span data-ttu-id="05e9c-129">Når du er ferdig med endringene, kan du lagre en kladd og/eller publisere endringene.</span><span class="sxs-lookup"><span data-stu-id="05e9c-129">When you are done making changes you can save a draft and/or publish the changes.</span></span>  

