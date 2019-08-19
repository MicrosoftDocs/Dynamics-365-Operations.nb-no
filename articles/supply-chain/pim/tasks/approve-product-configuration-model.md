---
title: Godkjenne en produktkonfigurasjonsmodell
description: Kjører du denne prosedyren krever det at minst én eksisterende produktmodellkonfigurasjon er tilgjengelig.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductModelVersion, PCApproveProductModelVersion, HcmWorkerLookUp
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: eef6568e012c311c0e5438245c011b876fc4d522
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844976"
---
# <a name="approve-a-product-configuration-model"></a><span data-ttu-id="ad566-103">Godkjenne en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="ad566-103">Approve a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad566-104">Kjører du denne prosedyren krever det at minst én eksisterende produktmodellkonfigurasjon er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="ad566-104">Running this procedure requires that at least one product configuration model is available.</span></span> <span data-ttu-id="ad566-105">Denne prosedyren bruker modellen for High-end-høyttaler i demodatafirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ad566-105">This procedure uses the High end speaker model in the demo data company USMF.</span></span> <span data-ttu-id="ad566-106">Legg merke til at denne modellen har allerede blitt godkjent, men fremgangsmåten leder deg gjennom hele prosessen.</span><span class="sxs-lookup"><span data-stu-id="ad566-106">Note that this model has already been approved, but the procedure walks you through the entire process.</span></span>

1. <span data-ttu-id="ad566-107">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="ad566-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ad566-108">Klikk Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="ad566-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="ad566-109">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ad566-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ad566-110">Velg High-end-høyttalermodellen for denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="ad566-110">Select the High end speaker model for this procedure.</span></span>  
4. <span data-ttu-id="ad566-111">Klikk Versjoner.</span><span class="sxs-lookup"><span data-stu-id="ad566-111">Click Versions.</span></span>
5. <span data-ttu-id="ad566-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ad566-112">Click New.</span></span>
6. <span data-ttu-id="ad566-113">Angi eller velg en verdi i Produktnummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="ad566-113">In the Product number field, enter or select a value.</span></span>
    * <span data-ttu-id="ad566-114">Referansen til et produkt representerer en versjon av en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="ad566-114">The reference to a product represents a version of a product configuration model.</span></span> <span data-ttu-id="ad566-115">Bare produktstandarder som har teknologien restriksjonsbasert konfigurasjon, vises i denne listen.</span><span class="sxs-lookup"><span data-stu-id="ad566-115">Only product masters which have the constraint-based configuration technology will appear in this list.</span></span>  
7. <span data-ttu-id="ad566-116">Angi en dato i Fra dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="ad566-116">In the From date field, enter a date.</span></span>
    * <span data-ttu-id="ad566-117">Velg når produktmodellversjonen vil være tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="ad566-117">Select when the product model version will be available.</span></span>  
8. <span data-ttu-id="ad566-118">Angi en dato i Til dato-feltet.</span><span class="sxs-lookup"><span data-stu-id="ad566-118">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="ad566-119">Velg en sluttdato når denne produktmodellversjonen skal utløpe, eller velg Aldri.</span><span class="sxs-lookup"><span data-stu-id="ad566-119">Select an end date when this product model version will expire, or select Never.</span></span>  
9. <span data-ttu-id="ad566-120">Klikk Godkjenn for å åpne nedtrekksdialogskjemaet.</span><span class="sxs-lookup"><span data-stu-id="ad566-120">Click Approve to open the drop dialog.</span></span>
10. <span data-ttu-id="ad566-121">Angi eller velg en verdi i feltet Godkjent av.</span><span class="sxs-lookup"><span data-stu-id="ad566-121">In the Approved by field, enter or select a value.</span></span>
    * <span data-ttu-id="ad566-122">Velg personen som er ansvarlig for godkjenning av produktmodeller for bruk i operasjoner.</span><span class="sxs-lookup"><span data-stu-id="ad566-122">Select the person who is responsible for approving product models for use in operations.</span></span>  
11. <span data-ttu-id="ad566-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ad566-123">Click OK.</span></span>
12. <span data-ttu-id="ad566-124">Velg et alternativ i Prissettingsmetode-feltet.</span><span class="sxs-lookup"><span data-stu-id="ad566-124">In the Pricing method field, select an option.</span></span>
    * <span data-ttu-id="ad566-125">Aktiver produktmodellversjonen.</span><span class="sxs-lookup"><span data-stu-id="ad566-125">Activate the product model version.</span></span> <span data-ttu-id="ad566-126">Det er bare mulig å ha ett produkt aktivt for en produktmodell om gangen.</span><span class="sxs-lookup"><span data-stu-id="ad566-126">It is only possible to have one product active for one product model at a time.</span></span>  
13. <span data-ttu-id="ad566-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ad566-127">Close the page.</span></span>

