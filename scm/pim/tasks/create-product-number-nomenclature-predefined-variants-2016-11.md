--- 
title: "Opprette et produktnummer for forhåndsdefinerte produktvarianter"
description: "Denne veiledningen viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe."
author: BibiSp
manager: AnnBe
ms.date: 09/26/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 6294e4608b31c37aa713e3a7a2028b409b5a8366
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="ad9c5-103">Opprette et produktnummer for forhåndsdefinerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="ad9c5-103">Create a product number for predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ad9c5-104">Denne veiledningen viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="ad9c5-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ad9c5-106">Den nye produktnummerterminologien tilordnes til produktdimensjonsgruppen farge og størrelse.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="ad9c5-107">Denne oppgaven vil vanligvis bli utført av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="ad9c5-108">Opprette produktnummerterminologi</span><span class="sxs-lookup"><span data-stu-id="ad9c5-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="ad9c5-109">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ad9c5-110">Klikk Produktterminologi.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="ad9c5-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-111">Click New.</span></span>
4. <span data-ttu-id="ad9c5-112">I Navn-feltet angir du et terminologinavn som hjelper deg med å identifisere målproduktdimensjonsgruppen, for eksempel ColorSize.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="ad9c5-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ad9c5-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-114">Click Add.</span></span>
7. <span data-ttu-id="ad9c5-115">Klikk Produktstandardnummer.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-115">Click Product master number.</span></span>
8. <span data-ttu-id="ad9c5-116">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-116">Click Add.</span></span>
9. <span data-ttu-id="ad9c5-117">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-117">Click Text constant.</span></span>
10. <span data-ttu-id="ad9c5-118">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="ad9c5-119">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-119">Click Add.</span></span>
12. <span data-ttu-id="ad9c5-120">Klikk Farge.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-120">Click Color.</span></span>
13. <span data-ttu-id="ad9c5-121">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-121">Click Add.</span></span>
14. <span data-ttu-id="ad9c5-122">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-122">Click Text constant.</span></span>
15. <span data-ttu-id="ad9c5-123">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="ad9c5-124">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-124">Click Add.</span></span>
17. <span data-ttu-id="ad9c5-125">Klikk Størrelse.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-125">Click Size.</span></span>
18. <span data-ttu-id="ad9c5-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="ad9c5-127">Tilordne terminologien til en produktstandard</span><span class="sxs-lookup"><span data-stu-id="ad9c5-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="ad9c5-128">Klikk Produktdimensjonsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="ad9c5-129">Velg produktdimensjonsgruppen SizeCol.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="ad9c5-130">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-130">Click Edit.</span></span>
4. <span data-ttu-id="ad9c5-131">Velg Ja i feltet Bruk nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="ad9c5-132">Angi eller velg en verdi i feltet Produktvariantnummerterminologi.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="ad9c5-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ad9c5-133">Close the page.</span></span>


