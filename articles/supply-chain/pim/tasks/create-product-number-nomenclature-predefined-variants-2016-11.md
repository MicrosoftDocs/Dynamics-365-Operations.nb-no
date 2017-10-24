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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 6294e4608b31c37aa713e3a7a2028b409b5a8366
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-product-number-for-predefined-product-variants"></a><span data-ttu-id="ae308-103">Opprette et produktnummer for forhåndsdefinerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="ae308-103">Create a product number for predefined product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ae308-104">Denne veiledningen viser hvordan du setter opp produktnummerterminologi for forhåndsdefinerte produktvarianter, og hvordan du tilordner den til riktig produktdimensjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="ae308-104">This guide shows you how to set up a product number nomenclature for predefined product variants, and how you assign it to the appropriate product dimension group.</span></span> <span data-ttu-id="ae308-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ae308-105">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="ae308-106">Den nye produktnummerterminologien tilordnes til produktdimensjonsgruppen farge og størrelse.</span><span class="sxs-lookup"><span data-stu-id="ae308-106">The new product number nomenclature is assigned to the Color and Size product dimension group.</span></span> <span data-ttu-id="ae308-107">Denne oppgaven vil vanligvis bli utført av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="ae308-107">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="ae308-108">Opprette produktnummerterminologi</span><span class="sxs-lookup"><span data-stu-id="ae308-108">Create a product number nomenclature</span></span>
1. <span data-ttu-id="ae308-109">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="ae308-109">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ae308-110">Klikk Produktterminologi.</span><span class="sxs-lookup"><span data-stu-id="ae308-110">Click Product nomenclature.</span></span>
3. <span data-ttu-id="ae308-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ae308-111">Click New.</span></span>
4. <span data-ttu-id="ae308-112">I Navn-feltet angir du et terminologinavn som hjelper deg med å identifisere målproduktdimensjonsgruppen, for eksempel ColorSize.</span><span class="sxs-lookup"><span data-stu-id="ae308-112">In the Name field, enter a nomenclature name that helps to identify the target product dimension group, for example, ColorSize..</span></span>
5. <span data-ttu-id="ae308-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ae308-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ae308-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ae308-114">Click Add.</span></span>
7. <span data-ttu-id="ae308-115">Klikk Produktstandardnummer.</span><span class="sxs-lookup"><span data-stu-id="ae308-115">Click Product master number.</span></span>
8. <span data-ttu-id="ae308-116">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ae308-116">Click Add.</span></span>
9. <span data-ttu-id="ae308-117">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="ae308-117">Click Text constant.</span></span>
10. <span data-ttu-id="ae308-118">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="ae308-118">In the Text field, type a value.</span></span>
11. <span data-ttu-id="ae308-119">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ae308-119">Click Add.</span></span>
12. <span data-ttu-id="ae308-120">Klikk Farge.</span><span class="sxs-lookup"><span data-stu-id="ae308-120">Click Color.</span></span>
13. <span data-ttu-id="ae308-121">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ae308-121">Click Add.</span></span>
14. <span data-ttu-id="ae308-122">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="ae308-122">Click Text constant.</span></span>
15. <span data-ttu-id="ae308-123">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="ae308-123">In the Text field, type a value.</span></span>
16. <span data-ttu-id="ae308-124">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ae308-124">Click Add.</span></span>
17. <span data-ttu-id="ae308-125">Klikk Størrelse.</span><span class="sxs-lookup"><span data-stu-id="ae308-125">Click Size.</span></span>
18. <span data-ttu-id="ae308-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ae308-126">Close the page.</span></span>

## <a name="assign-the-nomenclature-to-a-product-master"></a><span data-ttu-id="ae308-127">Tilordne terminologien til en produktstandard</span><span class="sxs-lookup"><span data-stu-id="ae308-127">Assign the nomenclature to a product master</span></span>
1. <span data-ttu-id="ae308-128">Klikk Produktdimensjonsgrupper.</span><span class="sxs-lookup"><span data-stu-id="ae308-128">Click Product dimension groups.</span></span>
2. <span data-ttu-id="ae308-129">Velg produktdimensjonsgruppen SizeCol.</span><span class="sxs-lookup"><span data-stu-id="ae308-129">Select the SizeCol product dimension group.</span></span>
3. <span data-ttu-id="ae308-130">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="ae308-130">Click Edit.</span></span>
4. <span data-ttu-id="ae308-131">Velg Ja i feltet Bruk nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="ae308-131">Select Yes in the Use nomenclature field.</span></span>
5. <span data-ttu-id="ae308-132">Angi eller velg en verdi i feltet Produktvariantnummerterminologi.</span><span class="sxs-lookup"><span data-stu-id="ae308-132">In the Product variant number nomenclature field, enter or select a value.</span></span>
6. <span data-ttu-id="ae308-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ae308-133">Close the page.</span></span>


