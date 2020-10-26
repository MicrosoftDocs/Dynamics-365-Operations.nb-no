---
title: Registrere varer for en vare for grunnleggende lageraktiviteter ved hjelp av en journal for vareankomst
description: Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker "grunnleggende lageraktiviteter" i lagerstyringsmodulen.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1745642dd270e62557b8624cc9daf85d13da044e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3982582"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="51bf7-103">Registrere varer for en vare for grunnleggende lageraktiviteter ved hjelp av en journal for vareankomst</span><span class="sxs-lookup"><span data-stu-id="51bf7-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="51bf7-104">Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker "grunnleggende lageraktiviteter" i lagerstyringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="51bf7-104">This procedure shows you how to register items using the item arrival journal when you are using "basic warehousing" in the Inventory management module.</span></span> <span data-ttu-id="51bf7-105">Dette gjøres vanligvis av en mottaksassistent.</span><span class="sxs-lookup"><span data-stu-id="51bf7-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="51bf7-106">Du kan kjøre denne prosedyren i demonstrasjonsdatafirmaet USMF med eksempelverdiene som vises.</span><span class="sxs-lookup"><span data-stu-id="51bf7-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="51bf7-107">Hvis du ikke bruker USMF, må du ha en bekreftet bestilling med en åpen bestillingslinje før du starter denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="51bf7-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="51bf7-108">Varen på linjen må være lagerført.</span><span class="sxs-lookup"><span data-stu-id="51bf7-108">The item on the line must be stocked.</span></span> <span data-ttu-id="51bf7-109">Og varene må være tilknyttet en lagringsdimensjonsgruppe der område og lager er aktive.</span><span class="sxs-lookup"><span data-stu-id="51bf7-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="51bf7-110">Opprette et hode for vareankomstjournal</span><span class="sxs-lookup"><span data-stu-id="51bf7-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="51bf7-111">Gå til Lagerstyring > Loggoppføringer > Vareankomst > Vareankomst.</span><span class="sxs-lookup"><span data-stu-id="51bf7-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="51bf7-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="51bf7-112">Click New.</span></span>
3. <span data-ttu-id="51bf7-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="51bf7-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="51bf7-114">Hvis du bruker USMF, kan du velge WHS.</span><span class="sxs-lookup"><span data-stu-id="51bf7-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="51bf7-115">Hvis du bruker andre data, må journalen med det valgte navnet ha følgende egenskaper: Kontroller plukklokasjon plukklokasjon må settes til Nei og Karantenestyring må settes til Nei.</span><span class="sxs-lookup"><span data-stu-id="51bf7-115">If you're using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="51bf7-116">Skriv inn en verdi i Følgeseddel-feltet.</span><span class="sxs-lookup"><span data-stu-id="51bf7-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="51bf7-117">Dette er følgeseddel-IDen fra følgeseddelen som er utstedt av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="51bf7-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="51bf7-118">Legg til et unikt nummer.</span><span class="sxs-lookup"><span data-stu-id="51bf7-118">Add a unique number.</span></span>  
5. <span data-ttu-id="51bf7-119">Velg bestillingen i Nummer-feltet i Nummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="51bf7-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="51bf7-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="51bf7-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="51bf7-121">Legge til linjer i journal for vareankomst</span><span class="sxs-lookup"><span data-stu-id="51bf7-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="51bf7-122">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="51bf7-122">Click Functions.</span></span>
2. <span data-ttu-id="51bf7-123">Klikk Opprett linjer.</span><span class="sxs-lookup"><span data-stu-id="51bf7-123">Click Create lines.</span></span>
    * <span data-ttu-id="51bf7-124">Linjene kan angis manuelt i denne journalen, eller opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="51bf7-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="51bf7-125">Dette viser hvordan du oppretter dette automatisk.</span><span class="sxs-lookup"><span data-stu-id="51bf7-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="51bf7-126">Merk av eller fjern merket i boksen Initialiser antall.</span><span class="sxs-lookup"><span data-stu-id="51bf7-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="51bf7-127">Dette vil initialisere antallet på journallinjene med antallet som ikke er registrert fra bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="51bf7-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="51bf7-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="51bf7-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="51bf7-129">Poster journalen</span><span class="sxs-lookup"><span data-stu-id="51bf7-129">Post the journal</span></span>
1. <span data-ttu-id="51bf7-130">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="51bf7-130">Click Post.</span></span>
2. <span data-ttu-id="51bf7-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="51bf7-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="51bf7-132">Generere produktkvitteringen</span><span class="sxs-lookup"><span data-stu-id="51bf7-132">Generate the product receipt</span></span>
1. <span data-ttu-id="51bf7-133">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="51bf7-133">Click Functions.</span></span>
2. <span data-ttu-id="51bf7-134">Klikk Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="51bf7-134">Click Product receipt.</span></span>
3. <span data-ttu-id="51bf7-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="51bf7-135">Click OK.</span></span>

