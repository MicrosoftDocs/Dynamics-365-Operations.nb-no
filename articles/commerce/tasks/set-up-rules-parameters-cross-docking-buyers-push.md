---
title: " Definere regler og parametere for direkteoverføring og sentralt innkjøp"
description: Denne prosedyren beskriver fremgangsmåten for å opprette etterfyllingsregler.
author: josaw1
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailReplenishmentRuleTable, RetailReplenishmentTreeLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9bccd92946783628dce37c3fd018e4dd927efd49
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3141141"
---
# <a name="set-up-rules-and-parameters-for-cross-docking-and-buyers-push"></a><span data-ttu-id="4bb35-103"> Definere regler og parametere for direkteoverføring og sentralt innkjøp</span><span class="sxs-lookup"><span data-stu-id="4bb35-103">Set up rules and parameters for cross docking and buyer's push</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4bb35-104">Denne prosedyren beskriver fremgangsmåten for å opprette etterfyllingsregler.</span><span class="sxs-lookup"><span data-stu-id="4bb35-104">This procedure demonstrates the steps to create Replenishment rules.</span></span> <span data-ttu-id="4bb35-105">Etterfyllingsregler kan brukes til å kontrollere hvordan produkter distribueres til butikkene når du bruker direkteoverføring og sentralt innkjøp.</span><span class="sxs-lookup"><span data-stu-id="4bb35-105">Replenishment rules can be used to control how products are distributed to stores when using Cross-docking and Buyer´s push.</span></span> <span data-ttu-id="4bb35-106">Etterfyllingsregler kan angis for butikker eller butikkgrupper.</span><span class="sxs-lookup"><span data-stu-id="4bb35-106">Replenishment rules can be set up for stores or store groups.</span></span> <span data-ttu-id="4bb35-107">Vekten som er definert for hver linje i en regel, styrer hvordan antallene av produkter blir fordelt mellom butikkene når etterfyllingsregler brukes som distribusjonsmetode i direkteoverføring eller sentralt innkjøp.</span><span class="sxs-lookup"><span data-stu-id="4bb35-107">The weight defined for each line in a rule will control how the quantities of products will get distributed between the stores when using Replenishment rules as the distribution method in Cross-docking or Buyer´s push.</span></span> <span data-ttu-id="4bb35-108">Denne prosedyren bruker demonstrasjonsfirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="4bb35-108">This procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="4bb35-109">Gå til Etterfyllingsregler.</span><span class="sxs-lookup"><span data-stu-id="4bb35-109">Go to Replenishment rules.</span></span>
2. <span data-ttu-id="4bb35-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4bb35-110">Click New.</span></span>
3. <span data-ttu-id="4bb35-111">Skriv inn en verdi i feltet Etterfyllingsregel.</span><span class="sxs-lookup"><span data-stu-id="4bb35-111">In the Replenishment rule field, type a value.</span></span>
4. <span data-ttu-id="4bb35-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4bb35-112">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4bb35-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4bb35-113">Click Save.</span></span>
6. <span data-ttu-id="4bb35-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4bb35-114">Click Add.</span></span>
7. <span data-ttu-id="4bb35-115">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4bb35-115">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="4bb35-116">Du kan velge Etterfyllingshierarki eller Kanal for typen.</span><span class="sxs-lookup"><span data-stu-id="4bb35-116">You can choose Replenishment hierarchy or Channel for the type.</span></span> <span data-ttu-id="4bb35-117">Verdien angir om valget i Navn blir et hierarki av kanaler eller en bestemt kanal.</span><span class="sxs-lookup"><span data-stu-id="4bb35-117">The value controls whether the selection in Name will be a hierarchy of channels or a specific channel.</span></span>  <span data-ttu-id="4bb35-118">La det for eksempel stå som Etterfyllingshierarki..</span><span class="sxs-lookup"><span data-stu-id="4bb35-118">For this example, leave it set as Replenishment hierarchy.</span></span>  
8. <span data-ttu-id="4bb35-119">Velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4bb35-119">In the Name field, select a value.</span></span>
    * <span data-ttu-id="4bb35-120">Standardvektverdien fylles ut fra vekten som er definert i lageret.</span><span class="sxs-lookup"><span data-stu-id="4bb35-120">The default weight value is populated from the weight defined on the warehouse.</span></span>  <span data-ttu-id="4bb35-121">Vekten kan brukes til etterfyllingsregelen eller du kan angi en ny vekt i Vekt-feltet.</span><span class="sxs-lookup"><span data-stu-id="4bb35-121">This weight can be used for the Replenishment rule or you can enter a new weight in the Weight field.</span></span>  
9. <span data-ttu-id="4bb35-122">Angi et tall i Vekt-feltet.</span><span class="sxs-lookup"><span data-stu-id="4bb35-122">In the Weight field, enter a number.</span></span>
10. <span data-ttu-id="4bb35-123">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="4bb35-123">Click Add.</span></span>
11. <span data-ttu-id="4bb35-124">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4bb35-124">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="4bb35-125">Velg Kanal i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="4bb35-125">In the Type field, select 'Channel'.</span></span>
13. <span data-ttu-id="4bb35-126">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="4bb35-126">In the Name field, enter or select a value.</span></span>
14. <span data-ttu-id="4bb35-127">Angi et tall i Vekt-feltet.</span><span class="sxs-lookup"><span data-stu-id="4bb35-127">In the Weight field, enter a number.</span></span>
15. <span data-ttu-id="4bb35-128">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4bb35-128">Click Save.</span></span>

