--- 
title: Definere kildeskatt
description: "Withholding tax er en leverandørskatt som ikke fører til merverditransaksjoner."
author: twheeloc
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 39ebd6a1a326b0ff2943957c9606e91852d524ce
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="7cae3-103">Definere kildeskatt</span><span class="sxs-lookup"><span data-stu-id="7cae3-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7cae3-104">Withholding tax er en leverandørskatt som ikke fører til merverditransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="7cae3-104">Withholding tax is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="7cae3-105">Withholding tax som beregnes for leverandørbetaling, er gjeld.</span><span class="sxs-lookup"><span data-stu-id="7cae3-105">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="7cae3-106">Derfor kan man bare bruke balansekontoer eller gjeldskontoer til å postere withholding tax.</span><span class="sxs-lookup"><span data-stu-id="7cae3-106">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="7cae3-107">Denne oppgaveveiledningen beskriver hvordan du definerer kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="7cae3-107">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="7cae3-108">Gå til Avgift > Indirekte avgifter > Kildeskatt > Kildeskattkoder.</span><span class="sxs-lookup"><span data-stu-id="7cae3-108">Go to Tax > Indirect taxes > Withholding tax > Withholding tax codes.</span></span>
2. <span data-ttu-id="7cae3-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7cae3-109">Click New.</span></span>
3. <span data-ttu-id="7cae3-110">Skriv inn en verdi i feltet Kildeskattkode.</span><span class="sxs-lookup"><span data-stu-id="7cae3-110">In the Withholding tax code field, type a value.</span></span>
4. <span data-ttu-id="7cae3-111">Angi navnet på kildeskattkoden i feltet Navn på kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="7cae3-111">In the Withholding tax name field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="7cae3-112">Velg hovedkontoen for postering av kildeskattgjelden i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="7cae3-112">In the Main account field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="7cae3-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7cae3-113">Click Save.</span></span>
7. <span data-ttu-id="7cae3-114">Velg Verdier.</span><span class="sxs-lookup"><span data-stu-id="7cae3-114">Click Values.</span></span>
8. <span data-ttu-id="7cae3-115">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7cae3-115">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="7cae3-116">Angi en prosent som brukes til beregning av kildeskatten, i Verdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="7cae3-116">In the Value field, enter a percentage used for the calculation of the withholding tax.</span></span>
10. <span data-ttu-id="7cae3-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7cae3-117">Click Save.</span></span>
11. <span data-ttu-id="7cae3-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7cae3-118">Close the page.</span></span>
12. <span data-ttu-id="7cae3-119">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7cae3-119">Click Save.</span></span>
13. <span data-ttu-id="7cae3-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7cae3-120">Close the page.</span></span>
14. <span data-ttu-id="7cae3-121">Gå til Avgift > Indirekte avgifter > Kildeskatt > Kildeskattgrupper.</span><span class="sxs-lookup"><span data-stu-id="7cae3-121">Go to Tax > Indirect taxes > Withholding tax > Withholding tax groups.</span></span>
15. <span data-ttu-id="7cae3-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7cae3-122">Click New.</span></span>
16. <span data-ttu-id="7cae3-123">Angi identifikatoren til kildeskattgruppen i feltet Kildeskattgruppe.</span><span class="sxs-lookup"><span data-stu-id="7cae3-123">In the Withholding tax group field, enter the identifier of the withholding tax group.</span></span>
17. <span data-ttu-id="7cae3-124">I Beskrivelse-feltet skriver du inn navnet på kildeskattgruppen.</span><span class="sxs-lookup"><span data-stu-id="7cae3-124">In the Description field, enter the name of the withholding tax group.</span></span>
18. <span data-ttu-id="7cae3-125">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7cae3-125">In the list, mark the selected row.</span></span>
19. <span data-ttu-id="7cae3-126">Velg kildeskattkoden i Kildeskattkode-feltet.</span><span class="sxs-lookup"><span data-stu-id="7cae3-126">In the Withholding tax code field, select the withholding tax code.</span></span>
20. <span data-ttu-id="7cae3-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7cae3-127">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="7cae3-128">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7cae3-128">Click Save.</span></span>


