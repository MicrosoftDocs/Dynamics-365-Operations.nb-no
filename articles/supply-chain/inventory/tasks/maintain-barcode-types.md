---
title: Opprettholde strekkodetyper
description: "Denne fremgangsmåten viser hvordan du definerer en ny definisjon for strekkode som kan brukes som en del av plukklisterapporten."
author: perlynne
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: bc863ce86c4dc3cbdd3a1df881eb7a6efeea1656
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---
# <a name="maintain-bar-code-types"></a><span data-ttu-id="73451-103">Opprettholde strekkodetyper</span><span class="sxs-lookup"><span data-stu-id="73451-103">Maintain bar code types</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="73451-104">Denne fremgangsmåten viser hvordan du definerer en ny definisjon for strekkode som kan brukes som en del av plukklisterapporten.</span><span class="sxs-lookup"><span data-stu-id="73451-104">This procedure shows you how to set up a new barcode definition which can then be used as part of the picking list report.</span></span> <span data-ttu-id="73451-105">Du kan gå gjennom denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="73451-105">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="73451-106">Hvis du bruker USMF, kan du bruke eksempelverdiene som vises.</span><span class="sxs-lookup"><span data-stu-id="73451-106">If you are using USMF you can use the example values that are shown.</span></span> <span data-ttu-id="73451-107">Disse oppgavene vil vanligvis utføres av en lagersjef.</span><span class="sxs-lookup"><span data-stu-id="73451-107">These tasks would typically be carried out by a warehouse manager.</span></span>

1. <span data-ttu-id="73451-108">Gå til Strekkoder.</span><span class="sxs-lookup"><span data-stu-id="73451-108">Go to Bar codes.</span></span>
2. <span data-ttu-id="73451-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="73451-109">Click New.</span></span>
3. <span data-ttu-id="73451-110">Skriv inn en verdi i feltet Strekkodeoppsett.</span><span class="sxs-lookup"><span data-stu-id="73451-110">In the Barcode setup field, type a value.</span></span>
4. <span data-ttu-id="73451-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="73451-111">In the Description field, type a value.</span></span>
5. <span data-ttu-id="73451-112">Velg et alternativ i Strekkodetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="73451-112">In the Bar code type field, select an option.</span></span>
    * <span data-ttu-id="73451-113">Hvis du bruker USMF, kan du velge "Kode 39".</span><span class="sxs-lookup"><span data-stu-id="73451-113">If you're using USMF, you can select 'Code 39'.</span></span>  
6. <span data-ttu-id="73451-114">Angi et tall i feltet Størrelse.</span><span class="sxs-lookup"><span data-stu-id="73451-114">In the Size field, enter a number.</span></span>
7. <span data-ttu-id="73451-115">Angi et tall i feltet Maksimumslengde.</span><span class="sxs-lookup"><span data-stu-id="73451-115">In the Maximum length field, enter a number.</span></span>
8. <span data-ttu-id="73451-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="73451-116">Click Save.</span></span>
9. <span data-ttu-id="73451-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="73451-117">Close the page.</span></span>
10. <span data-ttu-id="73451-118">Gå til Parametere for beholdnings- og lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="73451-118">Go to Inventory and warehouse management parameters.</span></span>
11. <span data-ttu-id="73451-119">Angi eller velg en verdi i feltet Strekkodeoppsett.</span><span class="sxs-lookup"><span data-stu-id="73451-119">In the Barcode setup field, enter or select a value.</span></span>
    * <span data-ttu-id="73451-120">Velg strekkodeoppsettet som du opprettet før, men Vær oppmerksom på at strekkodeformatet må samsvare med formatet for den unike identifikatoren for oppføringstypen som brukes i prosessen.</span><span class="sxs-lookup"><span data-stu-id="73451-120">Select the barcode setup that you created before, but be aware that the bar code format must match the format of the unique identifier for the record type used in the process.</span></span> <span data-ttu-id="73451-121">For plukkruter bør for eksempel strekkodeformatet samsvare med formatet for plukkrutereferansen, som vanligvis er en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="73451-121">For example, for picking routes, the bar code format should match the format of the picking route reference, which is typically a number sequence.</span></span>  
12. <span data-ttu-id="73451-122">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="73451-122">Click Save.</span></span>
13. <span data-ttu-id="73451-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="73451-123">Close the page.</span></span>

