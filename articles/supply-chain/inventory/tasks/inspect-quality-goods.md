---
title: Kontrollere varekvaliteten
description: Denne prosedyren viser hvordan du behandler en kvalitetsordre.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventQualityOrderTable, InventQualityOrderLineResults, HcmWorkerLookUp
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f9e9d750f116db62519ac7148f19bf62050430e9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "315435"
---
# <a name="inspect-the-quality-of-goods"></a><span data-ttu-id="9278a-103">Kontrollere varekvaliteten</span><span class="sxs-lookup"><span data-stu-id="9278a-103">Inspect the quality of goods</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="9278a-104">Denne prosedyren viser hvordan du behandler en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="9278a-104">This procedure shows you how to process a quality order.</span></span> <span data-ttu-id="9278a-105">Du kan bruke denne veiledningen i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="9278a-105">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="9278a-106">Før du starter denne eksempelprosedyren, må du bekrefte bestillingen "000016" og postere en produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="9278a-106">Before you start this example procedure, you need to confirm purchase order “000016” and post a product receipt.</span></span> <span data-ttu-id="9278a-107">Dermed opprettes automatisk en kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="9278a-107">This will automatically create a quality order.</span></span> <span data-ttu-id="9278a-108">Kvalitetsinspeksjoner utføres vanligvis av en kvalitetsassistent.</span><span class="sxs-lookup"><span data-stu-id="9278a-108">Quality inspections are typically carried out by a quality clerk.</span></span>


## <a name="select-a-quality-order"></a><span data-ttu-id="9278a-109">Velge en kvalitetsordre</span><span class="sxs-lookup"><span data-stu-id="9278a-109">Select a quality order</span></span>
1. <span data-ttu-id="9278a-110">Gå til Lagerstyring > Periodiske oppgaver > Kvalitetsstyring > Kvalitetsordrer.</span><span class="sxs-lookup"><span data-stu-id="9278a-110">Go to Inventory management > Periodic tasks > Quality management > Quality orders.</span></span>
2. <span data-ttu-id="9278a-111">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9278a-111">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="9278a-112">Velg kvalitetsordren som ble opprettet før du startet denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="9278a-112">Select the quality order that was created before you started this procedure.</span></span>  

## <a name="record-test-results"></a><span data-ttu-id="9278a-113">Registere testresultater</span><span class="sxs-lookup"><span data-stu-id="9278a-113">Record test results</span></span>
1. <span data-ttu-id="9278a-114">Klikk Resultater.</span><span class="sxs-lookup"><span data-stu-id="9278a-114">Click Results.</span></span>
2. <span data-ttu-id="9278a-115">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="9278a-115">Click Edit.</span></span>
3. <span data-ttu-id="9278a-116">Angi et tall i Resultatantall-feltet.</span><span class="sxs-lookup"><span data-stu-id="9278a-116">In the Result quantity field, enter a number.</span></span>
4. <span data-ttu-id="9278a-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9278a-117">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="9278a-118">Klikk rullegardinknappen i Resultat-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="9278a-118">In the Outcome field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="9278a-119">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9278a-119">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="9278a-120">I dette eksemplet er resultatet basert på et forhåndsdefinert resultat.</span><span class="sxs-lookup"><span data-stu-id="9278a-120">In this example the result is based on a pre-defined outcome.</span></span> <span data-ttu-id="9278a-121">Vanligvis vil du registrere et mer spesifikt testresultat, for eksempel en størrelse eller annen dimensjon.</span><span class="sxs-lookup"><span data-stu-id="9278a-121">Normally you would record a more specific test result, for example a size or other dimension.</span></span>  
7. <span data-ttu-id="9278a-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9278a-122">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="9278a-123">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="9278a-123">Click Save.</span></span>
9. <span data-ttu-id="9278a-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9278a-124">Close the page.</span></span>

## <a name="validate-the-quality-order"></a><span data-ttu-id="9278a-125">Valider kvalitetsordren</span><span class="sxs-lookup"><span data-stu-id="9278a-125">Validate the quality order</span></span>
1. <span data-ttu-id="9278a-126">Klikk Valider.</span><span class="sxs-lookup"><span data-stu-id="9278a-126">Click Validate.</span></span>
2. <span data-ttu-id="9278a-127">Klikk rullegardinknappen i feltet Valider av for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="9278a-127">In the Validated by field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="9278a-128">Velg brukeren som utfører inspeksjonen.</span><span class="sxs-lookup"><span data-stu-id="9278a-128">Select the user performing the inspection.</span></span>  
3. <span data-ttu-id="9278a-129">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9278a-129">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9278a-130">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="9278a-130">Click Select.</span></span>
5. <span data-ttu-id="9278a-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="9278a-131">Click OK.</span></span>
6. <span data-ttu-id="9278a-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9278a-132">Close the page.</span></span>

