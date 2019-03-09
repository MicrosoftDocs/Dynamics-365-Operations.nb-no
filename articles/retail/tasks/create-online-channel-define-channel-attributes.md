---
title: Opprette Internett-kanal og definere kanalattributter
description: Denne prosedyren hjelper med å opprette en ny Internett-kanal og legge den til i organisasjonshierarkiet.
author: jashanno
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailSPOnlineStoreDetailPage, SysLookupMultiSelectGrid, DimensionLookup, OMHierarchyManager, HierarchyDesigner, OMNodeSelection, HierarchyPublishAndCloseForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e066e9901a97bd5b72815a7af472247ef519ecb9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "312376"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="2a8c4-103">Opprette Internett-kanal og definere kanalattributter</span><span class="sxs-lookup"><span data-stu-id="2a8c4-103">Create online channel and define channel attributes</span></span>

[!include[task guide banner](../includes/task-guide-banner.md)]

<span data-ttu-id="2a8c4-104">Denne prosedyren hjelper med å opprette en ny Internett-kanal og legge den til i organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="2a8c4-105">Før du kan opprette en ny Internett-kanal, må du opprette organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="2a8c4-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="2a8c4-107">Opprette en ny Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="2a8c4-107">Create a new online channel</span></span>
1. <span data-ttu-id="2a8c4-108">Gå til Detaljhandel og handel > Kanaler > Nettbutikker.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-108">Go to Retail and commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="2a8c4-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-109">Click New.</span></span>
3. <span data-ttu-id="2a8c4-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2a8c4-111">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="2a8c4-112">Velg et alternativ i feltet Tidssone for butikk.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="2a8c4-113">Angi eller velg en verdi i Standardkunde-feltet.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="2a8c4-114">Angi eller velg en verdi i feltet Adressebok for kunde.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="2a8c4-115">Angi eller velg en verdi i Betalingsbetingelser-feltet.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="2a8c4-116">Angi eller velg en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="2a8c4-117">Angi eller velg en verdi i feltet Profil for e-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="2a8c4-118">Vis delen Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="2a8c4-119">Angi eller velg en verdi i BusinessUnit-feltet.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="2a8c4-120">Angi verdien for alle andre standarddimensjoner på samme måte.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="2a8c4-121">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="2a8c4-122">Legge til Internett-kanalen i organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="2a8c4-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="2a8c4-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-123">Close the page.</span></span>
2. <span data-ttu-id="2a8c4-124">Gå til Organisasjonsstyring > Organisasjoner > Organisasjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="2a8c4-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="2a8c4-126">Klikk Vis.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-126">Click View.</span></span>
5. <span data-ttu-id="2a8c4-127">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-127">Click Edit.</span></span>
    * <span data-ttu-id="2a8c4-128">Du kan velge en hierarkinode der du vil sette inn den nye kanalen.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="2a8c4-129">Klikk Sett inn.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-129">Click Insert.</span></span>
7. <span data-ttu-id="2a8c4-130">Klikk Detaljhandelskanal.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-130">Click Retail channel.</span></span>
8. <span data-ttu-id="2a8c4-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-131">Click OK.</span></span>
9. <span data-ttu-id="2a8c4-132">Klikk Publiser for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="2a8c4-133">Angi dato og klokkeslett i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="2a8c4-134">Klikk Publiser.</span><span class="sxs-lookup"><span data-stu-id="2a8c4-134">Click Publish.</span></span>

