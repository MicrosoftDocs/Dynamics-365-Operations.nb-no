---
title: Opprette en rentekode med et område
description: Rentekoder kan defineres til å beregne forskjellige rentebeløp basert på et verdiområde.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Interest, CustInterestRange
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c0c5b20ff6fff2bc62daca68c46e949a38df8d92
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446288"
---
# <a name="create-an-interest-code-with-a-range"></a><span data-ttu-id="74b92-103">Opprette en rentekode med et område</span><span class="sxs-lookup"><span data-stu-id="74b92-103">Create an interest code with a range</span></span>

[!include [banner](../../includes/banner.md)]
<span data-ttu-id="74b92-104">Rentekoder kan defineres til å beregne forskjellige rentebeløp basert på et verdiområde.</span><span class="sxs-lookup"><span data-stu-id="74b92-104">Interest codes can be set up to calculate different interest amounts based on a range of values.</span></span> <span data-ttu-id="74b92-105">Denne prosedyren viser hvordan du legger til en rentekode og legger til et område i den.</span><span class="sxs-lookup"><span data-stu-id="74b92-105">This procedure will show you how to add an interest code and add a range to it.</span></span>

1. <span data-ttu-id="74b92-106">Gå til Kreditt og innkreving > Rente > Definer rentekoder.</span><span class="sxs-lookup"><span data-stu-id="74b92-106">Go to Credit and collections > Interest > Set up interest codes.</span></span>
2. <span data-ttu-id="74b92-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="74b92-107">Click New.</span></span>
3. <span data-ttu-id="74b92-108">Skriv inn navnet på rentekoden i Rentekode-feltet.</span><span class="sxs-lookup"><span data-stu-id="74b92-108">In the Interest code field, enter the name of the interest code.</span></span>
4. <span data-ttu-id="74b92-109">I Beskrivelse-feltet skriver du inn en beskrivelse for rentekoden.</span><span class="sxs-lookup"><span data-stu-id="74b92-109">In the Description field, enter a description for the interest code.</span></span>
5. <span data-ttu-id="74b92-110">Velg Måned.</span><span class="sxs-lookup"><span data-stu-id="74b92-110">Select Month.</span></span>
6. <span data-ttu-id="74b92-111">Utvid delen Inntekter.</span><span class="sxs-lookup"><span data-stu-id="74b92-111">Expand the Earnings section.</span></span>
7. <span data-ttu-id="74b92-112">Utvid delen Inntjening etter valuta.</span><span class="sxs-lookup"><span data-stu-id="74b92-112">Expand the Earnings by currency section.</span></span>
8. <span data-ttu-id="74b92-113">Angi ønskede verdier i feltet Posteringskonto for finans.</span><span class="sxs-lookup"><span data-stu-id="74b92-113">In the Ledger posting account field, specify the desired values.</span></span>
9. <span data-ttu-id="74b92-114">Velg Måneder i feltet Rente etter intervall.</span><span class="sxs-lookup"><span data-stu-id="74b92-114">In the Interest by range field, select 'Months'.</span></span>
10. <span data-ttu-id="74b92-115">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="74b92-115">Click Add.</span></span>
11. <span data-ttu-id="74b92-116">I Beskrivelse-feltet angir du en beskrivelse for valutaen og området.</span><span class="sxs-lookup"><span data-stu-id="74b92-116">In the Description field, enter a description for this currency and range.</span></span>
12. <span data-ttu-id="74b92-117">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="74b92-117">Click Save.</span></span>
13. <span data-ttu-id="74b92-118">Klikk Områder.</span><span class="sxs-lookup"><span data-stu-id="74b92-118">Click Ranges.</span></span>
14. <span data-ttu-id="74b92-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="74b92-119">Click New.</span></span>
15. <span data-ttu-id="74b92-120">Sett Fra-verdien til 0, og angi deretter renteprosenten per måned som skal brukes til å beregne renten.</span><span class="sxs-lookup"><span data-stu-id="74b92-120">Enter the From value as 0 and then enter the interest percent per month that will be used to calculate the interest.</span></span> <span data-ttu-id="74b92-121">I vårt eksempel er det 1,5.</span><span class="sxs-lookup"><span data-stu-id="74b92-121">For our example, it is 1.5.</span></span>
16. <span data-ttu-id="74b92-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="74b92-122">Click New.</span></span>
17. <span data-ttu-id="74b92-123">Sett neste Fra-verdi til 4, som er den første måneden du skal beregne et nytt rentebeløp for.</span><span class="sxs-lookup"><span data-stu-id="74b92-123">Enter the next From value as 4, which is the first month that you will be calculating a new interest amount.</span></span>
18. <span data-ttu-id="74b92-124">Angi renteprosenten per måned som skal brukes til å beregne renten med start i måned 4.</span><span class="sxs-lookup"><span data-stu-id="74b92-124">Enter the interest percent per month that will be used to calculate the interest starting in month 4.</span></span> <span data-ttu-id="74b92-125">I vårt eksempel er det 2,0.</span><span class="sxs-lookup"><span data-stu-id="74b92-125">For this example, it is 2.0.</span></span>
19. <span data-ttu-id="74b92-126">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="74b92-126">Click New.</span></span>
20. <span data-ttu-id="74b92-127">Sett neste Fra-verdi til 7, som er den neste måneden du skal beregne et nytt rentebeløp for.</span><span class="sxs-lookup"><span data-stu-id="74b92-127">Enter the next From value as 7, which is the next month that you will be calculating a new interest amount.</span></span>
21. <span data-ttu-id="74b92-128">Angi renteprosenten per måned som skal brukes til å beregne renten med start i måned 7.</span><span class="sxs-lookup"><span data-stu-id="74b92-128">Enter the interest percent per month that will be used to calculate the interest starting in month 7.</span></span> <span data-ttu-id="74b92-129">I vårt eksempel er det 2,5.</span><span class="sxs-lookup"><span data-stu-id="74b92-129">For this example, it is 2.5.</span></span>
22. <span data-ttu-id="74b92-130">Klikk Lukk for å fullføre oppsettet.</span><span class="sxs-lookup"><span data-stu-id="74b92-130">Click Close to complete the setup.</span></span>

