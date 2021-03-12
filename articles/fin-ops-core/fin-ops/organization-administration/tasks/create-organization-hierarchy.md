---
title: Opprette et organisasjonshierarki
description: Bruk følgende fremgangsmåte for å opprette et organisasjonshierarki.
author: sericks007
manager: AnnBe
ms.date: 12/15/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: OMHierarchyManager, OMHierarchyPurposeAssociation, OMHierarchySelection, HierarchyDesigner
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8627c1aa0ce9ec011b568224040b1143f0f54c31
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/19/2020
ms.locfileid: "4796928"
---
# <a name="create-an-organization-hierarchy"></a><span data-ttu-id="e33ea-103">Opprette et organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="e33ea-103">Create an organization hierarchy</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e33ea-104">Bruk følgende fremgangsmåte for å opprette et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="e33ea-104">Use the following procedure to create an organizational hierarchy.</span></span> <span data-ttu-id="e33ea-105">Du kan bruke organisasjonshierarkier for å vise og rapportere for bedriften fra ulike perspektiver.</span><span class="sxs-lookup"><span data-stu-id="e33ea-105">You can use organizational hierarchies to view and report on your business from various perspectives.</span></span> <span data-ttu-id="e33ea-106">Du kan for eksempel definere ett hierarki for avgiftsrapportering, juridisk eller lovpålagt rapportering.</span><span class="sxs-lookup"><span data-stu-id="e33ea-106">For example, you can set up one hierarchy for tax, legal, or statutory reporting.</span></span> <span data-ttu-id="e33ea-107">Du kan deretter definere et annet hierarki for å rapportere finansinformasjon som ikke er lovpålagt, men som brukes til intern rapportering.</span><span class="sxs-lookup"><span data-stu-id="e33ea-107">You can then set up another hierarchy to report financial information that is not legally required, but that is used for internal reporting.</span></span> 

<span data-ttu-id="e33ea-108">Før du oppretter et organisasjonshierarki, må du opprette organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="e33ea-108">Before you create an organizational hierarchy, you must create organizations.</span></span> <span data-ttu-id="e33ea-109">Hvis du vil ha mer informasjon, kan du se oppgavene "Opprette en juridisk enhet" eller "Opprette en driftsenhet".</span><span class="sxs-lookup"><span data-stu-id="e33ea-109">For more information, see the "Create a legal entity" or "Create an operating unit" tasks.</span></span> <span data-ttu-id="e33ea-110">Du kan også opprette avdelinger og team.</span><span class="sxs-lookup"><span data-stu-id="e33ea-110">You can also create departments and teams.</span></span> 

<span data-ttu-id="e33ea-111">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="e33ea-111">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-hierarchy"></a><span data-ttu-id="e33ea-112">Opprett et hierarki</span><span class="sxs-lookup"><span data-stu-id="e33ea-112">Create a hierarchy</span></span>
1. <span data-ttu-id="e33ea-113">Gå til **Navigasjonsrute > Moduler > Organisasjonsstyring > Organisasjoner > Organisasjonshierarkier**.</span><span class="sxs-lookup"><span data-stu-id="e33ea-113">Go to **Navigation pane > Modules > Organization administration > Organizations > Organization hierarchies**.</span></span>
2. <span data-ttu-id="e33ea-114">Klikk på **Ny** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="e33ea-114">On the **Action pane**, click **New**.</span></span>
3. <span data-ttu-id="e33ea-115">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e33ea-115">In the **Name** field, type a value.</span></span>
4. <span data-ttu-id="e33ea-116">I **Formål**-delen klikker du **Tilordne formål**.</span><span class="sxs-lookup"><span data-stu-id="e33ea-116">In the **Purpose** section, click **Assign purpose**.</span></span>
5. <span data-ttu-id="e33ea-117">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e33ea-117">In the list, find and select the desired record.</span></span> <span data-ttu-id="e33ea-118">Velg et formål som skal tilordnes til organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="e33ea-118">Select a purpose to assign to your organization hierarchy.</span></span>  
6. <span data-ttu-id="e33ea-119">I delen **Tilordnede hierarkier** klikker du på **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="e33ea-119">In the **Assigned hierarchies** section, click **Add**.</span></span>
7. <span data-ttu-id="e33ea-120">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e33ea-120">In the list, mark the selected row.</span></span> <span data-ttu-id="e33ea-121">Finn hierarkiet du nettopp opprettet.</span><span class="sxs-lookup"><span data-stu-id="e33ea-121">Find the hierarchy you just created.</span></span>  
8. <span data-ttu-id="e33ea-122">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="e33ea-122">Click **OK**.</span></span>

## <a name="add-organizations-to-the-hierarchy"></a><span data-ttu-id="e33ea-123">Legge til organisasjoner i hierarkiet</span><span class="sxs-lookup"><span data-stu-id="e33ea-123">Add organizations to the hierarchy</span></span>
1. <span data-ttu-id="e33ea-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e33ea-124">In the list, find and select the desired record.</span></span> <span data-ttu-id="e33ea-125">Velg hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="e33ea-125">Select your hierarchy.</span></span>  
2. <span data-ttu-id="e33ea-126">I delen **Tilordnede hierarkier** klikker du **Vis hierarki**.</span><span class="sxs-lookup"><span data-stu-id="e33ea-126">In the **Assigned hierarchies** section, click **View hierarchy**.</span></span>
    - <span data-ttu-id="e33ea-127">Legg til organisasjoner etter behov.</span><span class="sxs-lookup"><span data-stu-id="e33ea-127">Add organizations, as necessary.</span></span>  
    - <span data-ttu-id="e33ea-128">Hvis du vil legge til en organisasjon, klikker du **Rediger** og deretter **Sett inn** for å legge til organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="e33ea-128">To add an organization, click **Edit** and then **Insert** to add the organization.</span></span> <span data-ttu-id="e33ea-129">Når du er ferdig med endringene, kan du **lagre** en kladd og/eller **publisere** endringene.</span><span class="sxs-lookup"><span data-stu-id="e33ea-129">When you are done making changes you can **Save** a draft and/or **Publish** the changes.</span></span>  

