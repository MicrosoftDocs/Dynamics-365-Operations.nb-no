--- 
title: "Endre eierskap for forsendelseslager basert på produksjonsbehov"
description: "Denne fremgangsmåten viser hvordan du endrer eieren av forsendelseslageret fra leverandøren til den juridiske enheten når det er behov for beholdningen i produksjonen."
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventJournalOwnershipChange, InventJournalCreate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: d1324da6996230eb383e2f37d3a133ec35cb0f41
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="change-the-ownership-of-consignment-inventory-based-on-production-demand"></a><span data-ttu-id="48cff-103">Endre eierskap for forsendelseslager basert på produksjonsbehov</span><span class="sxs-lookup"><span data-stu-id="48cff-103">Change the ownership of consignment inventory based on production demand</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="48cff-104">Denne fremgangsmåten viser hvordan du endrer eieren av forsendelseslageret fra leverandøren til den juridiske enheten når det er behov for beholdningen i produksjonen.</span><span class="sxs-lookup"><span data-stu-id="48cff-104">This procedure shows how to change the owner of consignment inventory from the vendor to your legal entity when there is demand for the inventory in production.</span></span> <span data-ttu-id="48cff-105">Denne endringen av eierskap gjøres ved å opprette og postere en endringsjournal for lagereierskap.</span><span class="sxs-lookup"><span data-stu-id="48cff-105">This change of ownership is done by creating and posting an inventory ownership change journal.</span></span> <span data-ttu-id="48cff-106">Endringsjournallinjene for lagereierskap kan opprettes manuelt eller, som vist her, basert på eksisterende produksjonsbehov.</span><span class="sxs-lookup"><span data-stu-id="48cff-106">The ownership change journal lines can be created manually or, as shown in this recording, based on existing production demand.</span></span> <span data-ttu-id="48cff-107">Vanligvis utfører en arbeidsleder denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="48cff-107">Typically, a shop floor supervisor performs this task.</span></span> <span data-ttu-id="48cff-108">Du kan bruke denne fremgangsmåten i USMF-demodatafirmaet eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="48cff-108">You can use this procedure in the USMF demo data company or on your own data.</span></span> <span data-ttu-id="48cff-109">Hvis du bruker dine egne data, må du kontrollere at følgende forutsetninger er tilstede: et lagerjournalnavn som har blitt definert for lagereierskapsendringen, fysisk registrerte leverandøreide varer på lager og én eller flere produksjonsordrelinjer for materialet.</span><span class="sxs-lookup"><span data-stu-id="48cff-109">If you're using your own data, make sure that you have the following prerequisites: an inventory journal name that has been set up for inventory ownership change, physically recorded vendor-owned on-hand items, and one or more production order lines for the material.</span></span> <span data-ttu-id="48cff-110">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="48cff-110">This procedure is for a feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-an-inventory-ownership-journal"></a><span data-ttu-id="48cff-111">Opprette en lagereierskapsjournal</span><span class="sxs-lookup"><span data-stu-id="48cff-111">Create an inventory ownership journal</span></span>
1. <span data-ttu-id="48cff-112">Gå til Lagerstyring > Journaloppføringer > Varer > Endring av lagereierskap.</span><span class="sxs-lookup"><span data-stu-id="48cff-112">Go to Inventory management > Journal entries > Items > Inventory ownership change.</span></span>
2. <span data-ttu-id="48cff-113">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="48cff-113">Click New.</span></span>
    * <span data-ttu-id="48cff-114">Endringsjournalen for lagereierskap brukes til å endre eieren av forsendelseslageret fra leverandøren til gjeldende juridiske enhet.</span><span class="sxs-lookup"><span data-stu-id="48cff-114">The inventory ownership change journal is used to change the owner of consignment inventory from the vendor to the current legal entity.</span></span> <span data-ttu-id="48cff-115">Denne endringen av eierskap gjøres ved å frigi lagerbeholdningen som eies av leverandøren. og deretter motta dette lageret i den gjeldende juridiske enheten.</span><span class="sxs-lookup"><span data-stu-id="48cff-115">This change of ownership is done by releasing the on-hand inventory that is owned by the vendor and then receiving that inventory in the current legal entity.</span></span>  
3. <span data-ttu-id="48cff-116">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="48cff-116">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="48cff-117">Du kan bare velge lagerjournalnavn som har journaltypen Endring av eierskap.</span><span class="sxs-lookup"><span data-stu-id="48cff-117">You can select only inventory journal names that have a journal type of Ownership change.</span></span>  
4. <span data-ttu-id="48cff-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="48cff-118">Click OK.</span></span>
5. <span data-ttu-id="48cff-119">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="48cff-119">Click Functions.</span></span>
6. <span data-ttu-id="48cff-120">Klikk Opprett journallinjer fra produksjonsordrer.</span><span class="sxs-lookup"><span data-stu-id="48cff-120">Click Create journal lines from production orders.</span></span>
    * <span data-ttu-id="48cff-121">Du kan starte endringen av eierskapsprosessen ved å spørre alle produksjonslinjer som har behov for forbruk av råvarer.</span><span class="sxs-lookup"><span data-stu-id="48cff-121">You can start the change of ownership process by querying all the production lines that have demand for consumption of raw material.</span></span>  
7. <span data-ttu-id="48cff-122">Velg et alternativ i feltet Lageravgangsstatus som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="48cff-122">In the Inventory issue statuses to include field, select an option.</span></span>
    * <span data-ttu-id="48cff-123">Dette alternativet gjør at du kan filtrere etter avgangsstatus for lagertransaksjonene.</span><span class="sxs-lookup"><span data-stu-id="48cff-123">This option lets you filter by the issue status of the inventory transactions.</span></span> <span data-ttu-id="48cff-124">Du kan for eksempel opprette journallinjer for lager som har statusen Plukket og Fysisk reservert.</span><span class="sxs-lookup"><span data-stu-id="48cff-124">For example, you can create journal lines for inventory that has the Picked and Reserved physical statuses.</span></span>  
8. <span data-ttu-id="48cff-125">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="48cff-125">Expand the Records to include section.</span></span>
    * <span data-ttu-id="48cff-126">Denne delen lar deg bruke ekstra filtrering.</span><span class="sxs-lookup"><span data-stu-id="48cff-126">This section lets you apply additional filtering.</span></span> <span data-ttu-id="48cff-127">Du kan for eksempel velge en bestemt råvaredato.</span><span class="sxs-lookup"><span data-stu-id="48cff-127">For example, you can select a specific raw material date.</span></span>  
9. <span data-ttu-id="48cff-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="48cff-128">Click OK.</span></span>

## <a name="post-the-inventory-ownership-change-journal"></a><span data-ttu-id="48cff-129">Postere endringsjournalen for lagereierskap</span><span class="sxs-lookup"><span data-stu-id="48cff-129">Post the inventory ownership change journal</span></span>
1. <span data-ttu-id="48cff-130">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="48cff-130">Click Post.</span></span>
    * <span data-ttu-id="48cff-131">Når journalen posteres, frigis det leverandøreide lageret ved hjelp referansen Endring av eierskap.</span><span class="sxs-lookup"><span data-stu-id="48cff-131">When the journal is posted, the vendor-owned inventory is released by using an "Ownership change" reference.</span></span> <span data-ttu-id="48cff-132">Lageret blir deretter mottatt som på lager ved hjelp av en lagertransaksjon som oppdateres med en bestillingsmottaksseddel.</span><span class="sxs-lookup"><span data-stu-id="48cff-132">The inventory is then received as on-hand by using an inventory transaction that is updated with a purchase order product receipt.</span></span> <span data-ttu-id="48cff-133">Vær oppmerksom på at bare transaksjoner som er knyttet til den posterte journalen, opprettes.</span><span class="sxs-lookup"><span data-stu-id="48cff-133">Note that only transactions that are related to the posted journal are created.</span></span> <span data-ttu-id="48cff-134">Ingen forventede lagertransaksjoner opprettes.</span><span class="sxs-lookup"><span data-stu-id="48cff-134">No expected inventory transactions are created.</span></span>  
2. <span data-ttu-id="48cff-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="48cff-135">Click OK.</span></span>
3. <span data-ttu-id="48cff-136">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="48cff-136">Close the page.</span></span>


