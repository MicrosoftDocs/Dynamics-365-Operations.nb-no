---
title: "Definere produkter som kan være produsert eller fremskaffet"
description: "Produkter kan ha forskjellige kildeinndelinger: de kan være produsert eller fremskaffet (kjøpt). Denne artikkelen beskriver noen vanlige poeng som må vurderes når du konfigurerer produkter som støtter flere leverandører."
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ReqGroup, ReqItemTable
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 21841
ms.assetid: acc608b7-2cad-4fba-afee-9b7cc93761ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: b5ed8c93c13746249605ad8742549c23bb1e0e10
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-products-that-can-be-produced-or-procured"></a><span data-ttu-id="70dde-104">Definere produkter som kan være produsert eller fremskaffet</span><span class="sxs-lookup"><span data-stu-id="70dde-104">Set up products that can be produced or procured</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="70dde-105">Produkter kan ha forskjellige kildeinndelinger: de kan være produsert eller fremskaffet (kjøpt).</span><span class="sxs-lookup"><span data-stu-id="70dde-105">Products can be sourced in various ways -  they can be produced (manufactured) or procured (purchased).</span></span> <span data-ttu-id="70dde-106">Denne artikkelen beskriver noen vanlige poeng som må vurderes når du konfigurerer produkter som støtter flere leverandører.</span><span class="sxs-lookup"><span data-stu-id="70dde-106">This article describes some typical points to consider when you configure products to support multi-sourcing.</span></span> 

<span data-ttu-id="70dde-107">Flere leverandører brukes vanligvis for en kjøpt vare som noen ganger produseres, eller når en vare som primært er en produsert vare endres slik at det nå primært er en innkjøpt vare.</span><span class="sxs-lookup"><span data-stu-id="70dde-107">Multi-sourcing is typically used for a purchased item that is occasionally manufactured, or when an item that was primarily a manufactured item is changed so that it's now primarily a purchased item.</span></span> <span data-ttu-id="70dde-108">Varen utpekes først som en produsert vare slik at stykkliste- og ruteinformasjon kan defineres, og for å støtte produksjonsordrer for varen.</span><span class="sxs-lookup"><span data-stu-id="70dde-108">The item is first designated as a manufactured item, so that bill of materials (BOM) and route information can be defined, and to support production orders for the item.</span></span> <span data-ttu-id="70dde-109">Produksjonstypen bør settes til **Stykkliste** (eller for prosessproduksjon, **Formel** eller **Koprodukt**).</span><span class="sxs-lookup"><span data-stu-id="70dde-109">The production type should be set to **BOM** (or, for process manufacturing, **Formula** or **Co-Product**).</span></span>

<span data-ttu-id="70dde-110">Når du bruker standardkostnad, kan varekostnadsposten beregnes for den produserte varen.</span><span class="sxs-lookup"><span data-stu-id="70dde-110">When you use standard cost, the item cost record can be calculated for the manufactured item.</span></span> <span data-ttu-id="70dde-111">Varekostposten vil imidlertid ikke alltid stemme overens med standardkostprisen du ønsker å bruke til innkjøpsformål.</span><span class="sxs-lookup"><span data-stu-id="70dde-111">However, the item cost record might not match the standard cost that you want for purchasing purposes.</span></span> <span data-ttu-id="70dde-112">I dette tilfellet må standardkostprisen registreres og aktiveres manuelt for varekostnadsposten.</span><span class="sxs-lookup"><span data-stu-id="70dde-112">In this case, the standard cost must be manually entered and activated for the item cost record.</span></span> <span data-ttu-id="70dde-113">For kostnadsberegningen kan du vurdere å bruke en spesiell stykkliste og rute som representerer forsyningsblandingen av produktet i løpet av en regnskapsperiode, for å redusere avvikene over tid.</span><span class="sxs-lookup"><span data-stu-id="70dde-113">For the cost calculation, consider using a special BOM and route that represent the supply mix of the product over the course of a fiscal period, to minimize the variances over time.</span></span> <span data-ttu-id="70dde-114">I tillegg kan en produsert vare fra ett område overføres til et annet område.</span><span class="sxs-lookup"><span data-stu-id="70dde-114">Additionally, a manufactured item at one site can be transferred to another site.</span></span> <span data-ttu-id="70dde-115">Derfor må varekostnaden manuelt registreres og aktiveres for området som varen blir overført til.</span><span class="sxs-lookup"><span data-stu-id="70dde-115">Therefore, the item's cost must be manually entered and activated for the site that the item is transferred to.</span></span> <span data-ttu-id="70dde-116">Når du bruker den produserte varen som en komponent i produkter på et høyere nivå, bør komponentens kostnader behandles som en innkjøpt vare.</span><span class="sxs-lookup"><span data-stu-id="70dde-116">When you use the manufactured item as a component in higher-level products, the component's costs should be treated as a purchased item.</span></span> <span data-ttu-id="70dde-117">Denne retningslinjen gjelder uansett om komponentens kostnader beregnes eller registreres manuelt.</span><span class="sxs-lookup"><span data-stu-id="70dde-117">This guideline applies, regardless of whether the component’s costs were calculated or manually entered.</span></span> <span data-ttu-id="70dde-118">Det vil si at en stykklisteberegning bør beregne varens kostnad som om den var en innkjøpt komponent, i stedet for å beregne kostnader på grunnlag av varens stykkliste- og ruteinformasjon.</span><span class="sxs-lookup"><span data-stu-id="70dde-118">In other words, a BOM calculation should treat the item's costs as a purchased component instead of using the item's BOM and route information to calculate costs.</span></span> <span data-ttu-id="70dde-119">Du kan hindre at slike beregninger utføres ved å velge flagget for **Stopp nedbryting**, som er innebygd i stykklisteberegningsgruppen som er tilordnet til varen.</span><span class="sxs-lookup"><span data-stu-id="70dde-119">To prevent the calculation from occurring, select the **Stop explosion** flag that is embedded in the BOM calculation group that is assigned to the item.</span></span> <span data-ttu-id="70dde-120">Du kan hindre at hovedplanleggingsberegninger bryter ned behov via varen ved å angi nedbrytingshorisonten til 0 dager i varedekning eller i dekningsgruppen.</span><span class="sxs-lookup"><span data-stu-id="70dde-120">To prevent master scheduling calculations from exploding requirements through the item, set the explosion fence to 0 (zero) days in item coverage or in the coverage group.</span></span> <span data-ttu-id="70dde-121">Hovedplanleggingsberegningen vil deretter behandle varen som en innkjøpt vare, og vil ikke utføre flere beregninger for varens stykkliste og ruteinformasjon.</span><span class="sxs-lookup"><span data-stu-id="70dde-121">The master scheduling calculation will then treat the item as a purchased item and won't perform more calculations for the item's BOM and route information.</span></span>






