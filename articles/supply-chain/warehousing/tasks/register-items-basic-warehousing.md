---
title: Registrere varer for en vare for grunnleggende lageraktiviteter ved hjelp av en journal for vareankomst
description: Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker "grunnleggende lageraktiviteter" i lagerstyringsmodulen.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchTablePart, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 61ce76c5aac82ec95b7113066b47b85a9c944307
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5830864"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="f4c6e-103">Registrere varer for en vare for grunnleggende lageraktiviteter ved hjelp av en journal for vareankomst</span><span class="sxs-lookup"><span data-stu-id="f4c6e-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f4c6e-104">Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker "grunnleggende lageraktiviteter" i lagerstyringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-104">This procedure shows you how to register items using the item arrival journal when you are using "basic warehousing" in the Inventory management module.</span></span> <span data-ttu-id="f4c6e-105">Dette gjøres vanligvis av en mottaksassistent.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="f4c6e-106">Du kan kjøre denne prosedyren i demonstrasjonsdatafirmaet USMF med eksempelverdiene som vises.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="f4c6e-107">Hvis du ikke bruker USMF, må du ha en bekreftet bestilling med en åpen bestillingslinje før du starter denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="f4c6e-108">Varen på linjen må være lagerført.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-108">The item on the line must be stocked.</span></span> <span data-ttu-id="f4c6e-109">Og varene må være tilknyttet en lagringsdimensjonsgruppe der område og lager er aktive.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="f4c6e-110">Opprette et hode for vareankomstjournal</span><span class="sxs-lookup"><span data-stu-id="f4c6e-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="f4c6e-111">Gå til Lagerstyring > Loggoppføringer > Vareankomst > Vareankomst.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="f4c6e-112">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-112">Click New.</span></span>
3. <span data-ttu-id="f4c6e-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f4c6e-114">Hvis du bruker USMF, kan du velge WHS.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="f4c6e-115">Hvis du bruker andre data, må journalen med det valgte navnet ha følgende egenskaper: Kontroller plukklokasjon plukklokasjon må settes til Nei og Karantenestyring må settes til Nei.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-115">If you're using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="f4c6e-116">Skriv inn en verdi i Følgeseddel-feltet.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="f4c6e-117">Dette er følgeseddel-IDen fra følgeseddelen som er utstedt av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="f4c6e-118">Legg til et unikt nummer.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-118">Add a unique number.</span></span>  
5. <span data-ttu-id="f4c6e-119">Velg bestillingen i Nummer-feltet i Nummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="f4c6e-120">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="f4c6e-121">Legge til linjer i journal for vareankomst</span><span class="sxs-lookup"><span data-stu-id="f4c6e-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="f4c6e-122">Klikk på Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-122">Click Functions.</span></span>
2. <span data-ttu-id="f4c6e-123">Klikk på Opprett linjer.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-123">Click Create lines.</span></span>
    * <span data-ttu-id="f4c6e-124">Linjene kan angis manuelt i denne journalen, eller opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="f4c6e-125">Dette viser hvordan du oppretter dette automatisk.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="f4c6e-126">Merk av eller fjern merket i boksen Initialiser antall.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="f4c6e-127">Dette vil initialisere antallet på journallinjene med antallet som ikke er registrert fra bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="f4c6e-128">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="f4c6e-129">Poster journalen</span><span class="sxs-lookup"><span data-stu-id="f4c6e-129">Post the journal</span></span>
1. <span data-ttu-id="f4c6e-130">Klikk på Poster.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-130">Click Post.</span></span>
2. <span data-ttu-id="f4c6e-131">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="f4c6e-132">Generere produktkvitteringen</span><span class="sxs-lookup"><span data-stu-id="f4c6e-132">Generate the product receipt</span></span>
1. <span data-ttu-id="f4c6e-133">Klikk på Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-133">Click Functions.</span></span>
2. <span data-ttu-id="f4c6e-134">Klikk på Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-134">Click Product receipt.</span></span>
3. <span data-ttu-id="f4c6e-135">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="f4c6e-135">Click OK.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]