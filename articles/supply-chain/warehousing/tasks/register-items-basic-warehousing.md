---
title: Registrere varer for en vare for grunnleggende lageraktiviteter ved hjelp av en journal for vareankomst
description: Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker "grunnleggende lageraktiviteter" i lagerstyringsmodulen.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, WMSJournalTable, WMSJournalCreate, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4e64a6df41e43c1b97243a6f7291393982575636
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847237"
---
# <a name="register-items-for-a-basic-warehousing-enabled-item-using-an-item-an-item-arrival-journal"></a><span data-ttu-id="b798c-103">Registrere varer for en vare for grunnleggende lageraktiviteter ved hjelp av en journal for vareankomst</span><span class="sxs-lookup"><span data-stu-id="b798c-103">Register items for a basic warehousing enabled item using an item an item arrival journal</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b798c-104">Denne fremgangsmåten viser hvordan du registrerer varer ved hjelp av vareankomstjournalen når du bruker "grunnleggende lageraktiviteter" i lagerstyringsmodulen.</span><span class="sxs-lookup"><span data-stu-id="b798c-104">This procedure shows you how to register items using the item arrival journal when you are using “basic warehousing” in the Inventory management module.</span></span> <span data-ttu-id="b798c-105">Dette gjøres vanligvis av en mottaksassistent.</span><span class="sxs-lookup"><span data-stu-id="b798c-105">This would usually be done by a receiving clerk.</span></span> <span data-ttu-id="b798c-106">Du kan kjøre denne prosedyren i demonstrasjonsdatafirmaet USMF med eksempelverdiene som vises.</span><span class="sxs-lookup"><span data-stu-id="b798c-106">You can run this procedure in demo data company USMF with the example values that are shown.</span></span>  <span data-ttu-id="b798c-107">Hvis du ikke bruker USMF, må du ha en bekreftet bestilling med en åpen bestillingslinje før du starter denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="b798c-107">If you are not using USMF, you need to have a confirmed purchase order with an open purchase order line before you start this guide.</span></span> <span data-ttu-id="b798c-108">Varen på linjen må være lagerført.</span><span class="sxs-lookup"><span data-stu-id="b798c-108">The item on the line must be stocked.</span></span> <span data-ttu-id="b798c-109">Og varene må være tilknyttet en lagringsdimensjonsgruppe der område og lager er aktive.</span><span class="sxs-lookup"><span data-stu-id="b798c-109">And the item needs to be associated with a storage dimension group, where site and warehouse are active.</span></span>


## <a name="create-item-arrival-journal-header"></a><span data-ttu-id="b798c-110">Opprette et hode for vareankomstjournal</span><span class="sxs-lookup"><span data-stu-id="b798c-110">Create item arrival journal header</span></span>
1. <span data-ttu-id="b798c-111">Gå til Lagerstyring > Loggoppføringer > Vareankomst > Vareankomst.</span><span class="sxs-lookup"><span data-stu-id="b798c-111">Go to Inventory management > Journal entries > Item arrival > Item arrival.</span></span>
2. <span data-ttu-id="b798c-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b798c-112">Click New.</span></span>
3. <span data-ttu-id="b798c-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="b798c-113">In the Name field, type a value.</span></span>
    * <span data-ttu-id="b798c-114">Hvis du bruker USMF, kan du velge WHS.</span><span class="sxs-lookup"><span data-stu-id="b798c-114">If you are using USMF, you can type WHS.</span></span> <span data-ttu-id="b798c-115">Hvis du bruker andre data, må journalen med det valgte navnet ha følgende egenskaper: Kontroller plukklokasjon plukklokasjon må settes til Nei og Karantenestyring må settes til Nei.</span><span class="sxs-lookup"><span data-stu-id="b798c-115">If you’re using other data, the journal whose name you choose has to have the following properties: cheque picking location must be set to No, and Quarantine management must be set to No.</span></span>  
4. <span data-ttu-id="b798c-116">Skriv inn en verdi i Følgeseddel-feltet.</span><span class="sxs-lookup"><span data-stu-id="b798c-116">In the Packing slip field, type a value.</span></span>
    * <span data-ttu-id="b798c-117">Dette er følgeseddel-IDen fra følgeseddelen som er utstedt av leverandøren.</span><span class="sxs-lookup"><span data-stu-id="b798c-117">This is the packing slip ID from the packing slip issued by the vendor.</span></span> <span data-ttu-id="b798c-118">Legg til et unikt nummer.</span><span class="sxs-lookup"><span data-stu-id="b798c-118">Add a unique number.</span></span>  
5. <span data-ttu-id="b798c-119">Velg bestillingen i Nummer-feltet i Nummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="b798c-119">In the Number field, In the Number field, select the purchase order..</span></span>
6. <span data-ttu-id="b798c-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b798c-120">Click OK.</span></span>

## <a name="add-lines-to-item-arrival-journal"></a><span data-ttu-id="b798c-121">Legge til linjer i journal for vareankomst</span><span class="sxs-lookup"><span data-stu-id="b798c-121">Add lines to item arrival journal</span></span>
1. <span data-ttu-id="b798c-122">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="b798c-122">Click Functions.</span></span>
2. <span data-ttu-id="b798c-123">Klikk Opprett linjer.</span><span class="sxs-lookup"><span data-stu-id="b798c-123">Click Create lines.</span></span>
    * <span data-ttu-id="b798c-124">Linjene kan angis manuelt i denne journalen, eller opprettes automatisk.</span><span class="sxs-lookup"><span data-stu-id="b798c-124">The lines can be entered manually into this journal or created automatically.</span></span> <span data-ttu-id="b798c-125">Dette viser hvordan du oppretter dette automatisk.</span><span class="sxs-lookup"><span data-stu-id="b798c-125">This will show you how to create this automatically.</span></span>  
3. <span data-ttu-id="b798c-126">Merk av eller fjern merket i boksen Initialiser antall.</span><span class="sxs-lookup"><span data-stu-id="b798c-126">Check or uncheck the Initialize quantity checkbox.</span></span>
    * <span data-ttu-id="b798c-127">Dette vil initialisere antallet på journallinjene med antallet som ikke er registrert fra bestillingslinjen.</span><span class="sxs-lookup"><span data-stu-id="b798c-127">This will initialize the quantity on the journal lines with the quantity not registered from the purchase order line.</span></span>  
4. <span data-ttu-id="b798c-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b798c-128">Click OK.</span></span>

## <a name="post-the-journal"></a><span data-ttu-id="b798c-129">Poster journalen</span><span class="sxs-lookup"><span data-stu-id="b798c-129">Post the journal</span></span>
1. <span data-ttu-id="b798c-130">Klikk Poster.</span><span class="sxs-lookup"><span data-stu-id="b798c-130">Click Post.</span></span>
2. <span data-ttu-id="b798c-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b798c-131">Click OK.</span></span>

## <a name="generate-the-product-receipt"></a><span data-ttu-id="b798c-132">Generere produktkvitteringen</span><span class="sxs-lookup"><span data-stu-id="b798c-132">Generate the product receipt</span></span>
1. <span data-ttu-id="b798c-133">Klikk Funksjoner.</span><span class="sxs-lookup"><span data-stu-id="b798c-133">Click Functions.</span></span>
2. <span data-ttu-id="b798c-134">Klikk Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="b798c-134">Click Product receipt.</span></span>
3. <span data-ttu-id="b798c-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b798c-135">Click OK.</span></span>

