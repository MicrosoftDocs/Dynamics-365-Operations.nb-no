--- 
title: "Opprette og eksportere leverandørbetalinger ved hjelp av ISO20022-betalingsformat"
description: "Denne prosedyren viser hvordan du oppretter betalingslinjer i leverandørbetalingsjournalen og genererer en leverandørbetalingsfil ved hjelp av eksemplet med ISO2022-kredittoverføring."
author: mrolecki
manager: AnnBe
ms.date: 10/24/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 5787edc4a041e4b571c7ab6f056f4bd0a17cf2d7
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="create-and-export-vendor-payments-using-iso20022-payment-format"></a><span data-ttu-id="8810e-103">Opprette og eksportere leverandørbetalinger ved hjelp av ISO20022-betalingsformat</span><span class="sxs-lookup"><span data-stu-id="8810e-103">Create and export vendor payments using ISO20022 payment format</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8810e-104">Denne prosedyren viser hvordan du oppretter betalingslinjer i leverandørbetalingsjournalen og genererer en leverandørbetalingsfil ved hjelp av eksemplet med ISO2022-kredittoverføring.</span><span class="sxs-lookup"><span data-stu-id="8810e-104">This procedure shows how to create payment lines in the vendor payment journal and generate a vendor payment file using ISO2022 Credit transfer example.</span></span> 

<span data-ttu-id="8810e-105">Demonstrasjonsdatafirmaet DEMF brukes til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="8810e-105">The demo data company used to create this procedure is DEMF.</span></span>

<span data-ttu-id="8810e-106">Dette er den femte prosedyren av fem, som illustrerer leverandørbetalingsprosessen ved hjelp av konfigurasjoner for elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="8810e-106">This is the fifth procedure, out of five, that illustrates the vendor payment process using electronic reporting configurations.</span></span> <span data-ttu-id="8810e-107">Denne fremgangsmåten gjelder for en funksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="8810e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-payment-lines"></a><span data-ttu-id="8810e-108">Opprette betalingslinjer</span><span class="sxs-lookup"><span data-stu-id="8810e-108">Create payment lines</span></span>
1. <span data-ttu-id="8810e-109">Gå til Leverandører > Betalinger > Betalingsjournal.</span><span class="sxs-lookup"><span data-stu-id="8810e-109">Go to Accounts payable > Payments > Payment journal.</span></span>
2. <span data-ttu-id="8810e-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8810e-110">Click New.</span></span>
3. <span data-ttu-id="8810e-111">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8810e-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="8810e-112">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="8810e-112">In the Name field, enter or select a value.</span></span>
5. <span data-ttu-id="8810e-113">Klikk Linjer.</span><span class="sxs-lookup"><span data-stu-id="8810e-113">Click Lines.</span></span>
6. <span data-ttu-id="8810e-114">Klikk Betalingsforslag.</span><span class="sxs-lookup"><span data-stu-id="8810e-114">Click Payment proposal.</span></span>
7. <span data-ttu-id="8810e-115">Klikk Opprett betalingsforslag.</span><span class="sxs-lookup"><span data-stu-id="8810e-115">Click Create payment proposal.</span></span>
8. <span data-ttu-id="8810e-116">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="8810e-116">Expand the Records to include section.</span></span>
9. <span data-ttu-id="8810e-117">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="8810e-117">Click Filter.</span></span>
10. <span data-ttu-id="8810e-118">I listen velger du raden for Leverandører-tabellen og Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="8810e-118">In the list, select the row for Vendors table and Vendor account field.</span></span>
11. <span data-ttu-id="8810e-119">Angi eller velg en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="8810e-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="8810e-120">Du kan bruke hvilke som helst kriterier for å velge leverandørtransaksjoner som skal betales, men i dette eksemplet bruker du DE-001 som en leverandørkonto.</span><span class="sxs-lookup"><span data-stu-id="8810e-120">You can apply any criteria for selecting vendor transactions to pay, for this example use DE-001 as a vendor account.</span></span>  
12. <span data-ttu-id="8810e-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8810e-121">Click OK.</span></span>
13. <span data-ttu-id="8810e-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="8810e-122">Click OK.</span></span>
14. <span data-ttu-id="8810e-123">Klikk Opprett betalinger.</span><span class="sxs-lookup"><span data-stu-id="8810e-123">Click Create payments.</span></span>

## <a name="generate-an-iso20022-payment-file"></a><span data-ttu-id="8810e-124">Generere en ISO20022-betalingsfil</span><span class="sxs-lookup"><span data-stu-id="8810e-124">Generate an ISO20022 payment file</span></span>


