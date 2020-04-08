---
title: Opprette Internett-kanal og definere kanalattributter
description: Denne prosedyren hjelper med å opprette en ny Internett-kanal og legge den til i organisasjonshierarkiet.
author: jashanno
manager: AnnBe
ms.date: 06/04/2019
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
ms.openlocfilehash: f15b035c01801041d637a2d315d8a3ddcc9d6540
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3140959"
---
# <a name="create-online-channel-and-define-channel-attributes"></a><span data-ttu-id="4613c-103">Opprette Internett-kanal og definere kanalattributter</span><span class="sxs-lookup"><span data-stu-id="4613c-103">Create online channel and define channel attributes</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4613c-104">Denne prosedyren hjelper med å opprette en ny Internett-kanal og legge den til i organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="4613c-104">This procedure walks through creating a new online channel and adding it to the organization hierarchy.</span></span> <span data-ttu-id="4613c-105">Før du kan opprette en ny Internett-kanal, må du opprette organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="4613c-105">You must create the organization hierarchy before you can create a new online channel.</span></span> <span data-ttu-id="4613c-106">Denne prosedyren bruker demonstrasjonsdatafirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="4613c-106">This procedure uses the USRT demo data company.</span></span>


## <a name="create-a-new-online-channel"></a><span data-ttu-id="4613c-107">Opprette en ny Internett-kanal</span><span class="sxs-lookup"><span data-stu-id="4613c-107">Create a new online channel</span></span>
1. <span data-ttu-id="4613c-108">Gå til Detaljhandel og handel > Kanaler > Nettbutikker.</span><span class="sxs-lookup"><span data-stu-id="4613c-108">Go to Retail and Commerce > Channels > Online stores.</span></span>
2. <span data-ttu-id="4613c-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4613c-109">Click New.</span></span>
3. <span data-ttu-id="4613c-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4613c-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="4613c-111">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="4613c-111">In the Warehouse field, enter or select a value.</span></span>
5. <span data-ttu-id="4613c-112">Velg et alternativ i feltet Tidssone for butikk.</span><span class="sxs-lookup"><span data-stu-id="4613c-112">In the Store time zone field, select an option.</span></span>
6. <span data-ttu-id="4613c-113">Angi eller velg en verdi i Standardkunde-feltet.</span><span class="sxs-lookup"><span data-stu-id="4613c-113">In the Default customer field, enter or select a value.</span></span>
7. <span data-ttu-id="4613c-114">Angi eller velg en verdi i feltet Adressebok for kunde.</span><span class="sxs-lookup"><span data-stu-id="4613c-114">In the Customer address book field, enter or select a value.</span></span>
8. <span data-ttu-id="4613c-115">Angi eller velg en verdi i Betalingsbetingelser-feltet.</span><span class="sxs-lookup"><span data-stu-id="4613c-115">In the Terms of payment field, enter or select a value.</span></span>
9. <span data-ttu-id="4613c-116">Angi eller velg en verdi i Betalingsmåte-feltet.</span><span class="sxs-lookup"><span data-stu-id="4613c-116">In the Method of payment field, enter or select a value.</span></span>
10. <span data-ttu-id="4613c-117">Angi eller velg en verdi i feltet Profil for e-postvarsling.</span><span class="sxs-lookup"><span data-stu-id="4613c-117">In the Email notification profile field, enter or select a value.</span></span>
11. <span data-ttu-id="4613c-118">Vis delen Finansdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="4613c-118">Expand the Financial dimensions section.</span></span>
12. <span data-ttu-id="4613c-119">Angi eller velg en verdi i BusinessUnit-feltet.</span><span class="sxs-lookup"><span data-stu-id="4613c-119">In the BusinessUnit field, enter or select a value.</span></span>
    * <span data-ttu-id="4613c-120">Angi verdien for alle andre standarddimensjoner på samme måte.</span><span class="sxs-lookup"><span data-stu-id="4613c-120">Similarly set the value for all the other default dimensions.</span></span>  
13. <span data-ttu-id="4613c-121">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4613c-121">Click Save.</span></span>

## <a name="add-the-online-channel-to-organization-hierarchy"></a><span data-ttu-id="4613c-122">Legge til Internett-kanalen i organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="4613c-122">Add the online channel to organization hierarchy</span></span>
1. <span data-ttu-id="4613c-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4613c-123">Close the page.</span></span>
2. <span data-ttu-id="4613c-124">Gå til Organisasjonsstyring > Organisasjoner > Organisasjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="4613c-124">Go to Organization administration > Organizations > Organization hierarchies.</span></span>
3. <span data-ttu-id="4613c-125">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4613c-125">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="4613c-126">Klikk Vis.</span><span class="sxs-lookup"><span data-stu-id="4613c-126">Click View.</span></span>
5. <span data-ttu-id="4613c-127">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="4613c-127">Click Edit.</span></span>
    * <span data-ttu-id="4613c-128">Du kan velge en hierarkinode der du vil sette inn den nye kanalen.</span><span class="sxs-lookup"><span data-stu-id="4613c-128">You can select any hierarchy node under which you want to insert the new channel.</span></span>  
6. <span data-ttu-id="4613c-129">Klikk Sett inn.</span><span class="sxs-lookup"><span data-stu-id="4613c-129">Click Insert.</span></span>
7. <span data-ttu-id="4613c-130">Klikk på Handelskanal.</span><span class="sxs-lookup"><span data-stu-id="4613c-130">Click Commerce channel.</span></span>
8. <span data-ttu-id="4613c-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4613c-131">Click OK.</span></span>
9. <span data-ttu-id="4613c-132">Klikk Publiser for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4613c-132">Click Publish to open the drop dialog.</span></span>
10. <span data-ttu-id="4613c-133">Angi dato og klokkeslett i feltet Gyldighetsdato.</span><span class="sxs-lookup"><span data-stu-id="4613c-133">In the Effective date field, enter a date and time.</span></span>
11. <span data-ttu-id="4613c-134">Klikk Publiser.</span><span class="sxs-lookup"><span data-stu-id="4613c-134">Click Publish.</span></span>

## <a name="configure-orders-for-near-real-time-notification"></a><span data-ttu-id="4613c-135">Konfigurere ordrer for varsling i nær sanntid</span><span class="sxs-lookup"><span data-stu-id="4613c-135">Configure orders for near real-time notification</span></span>
1. <span data-ttu-id="4613c-136">Gå til Detaljhandel og handel > Hovedkvarteroppsett > Parametere > Handelsparametere.</span><span class="sxs-lookup"><span data-stu-id="4613c-136">Go to Retail and Commerce  > Headquarters setup > Parameters > Commerce parameters.</span></span>
2. <span data-ttu-id="4613c-137">Sett bruk sanntid-tjenesten for eCommerce-ordreoppretting til "Ja".</span><span class="sxs-lookup"><span data-stu-id="4613c-137">Set Use realtime service for eCommerce order creation to "Yes".</span></span>
3. <span data-ttu-id="4613c-138">Kjør distribusjonsplanen 1070 for å synkronisere endringer i kanaldatabasen.</span><span class="sxs-lookup"><span data-stu-id="4613c-138">Run the 1070 distribution schedule to sync changes to the channel database.</span></span> 


