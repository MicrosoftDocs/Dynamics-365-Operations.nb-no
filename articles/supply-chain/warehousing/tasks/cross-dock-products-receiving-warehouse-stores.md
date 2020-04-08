---
title: Direkteoverføre produkter fra mottakende lager til butikker
description: Denne prosedyren hjelper deg gjennom trinnene med å opprette og behandle en direkteoverføring ved distribusjon av produkter fra mottaksstedet for en bestilling til én eller flere butikker.
author: ShylaThompson
manager: AnnBe
ms.date: 02/17/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f297a9bbb8ad5d1cd701626783e7db75c94fa842
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148383"
---
# <a name="cross-dock-products-from-receiving-warehouse-to-stores"></a><span data-ttu-id="d5150-103">Direkteoverføre produkter fra mottakende lager til butikker</span><span class="sxs-lookup"><span data-stu-id="d5150-103">Cross-dock products from receiving warehouse to stores</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d5150-104">Denne prosedyren hjelper deg gjennom trinnene med å opprette og behandle en direkteoverføring ved distribusjon av produkter fra mottaksstedet for en bestilling til én eller flere butikker.</span><span class="sxs-lookup"><span data-stu-id="d5150-104">This procedure walks through the steps to create and process a Cross-dock to distribute products from the receiving location of a purchase order to one or many stores.</span></span> <span data-ttu-id="d5150-105">Brukeren kan definere flere konfigurasjoner og få systemet til å foreslå hvordan produktene skal distribueres, eller manuelt angi hvor produktene skal distribueres og hvor mye som skal distribueres til hver butikk.</span><span class="sxs-lookup"><span data-stu-id="d5150-105">The user can define multiple configurations and have the system suggest how to distribute the products, or manually enter where the products are distributed to and how much gets distributed to each store.</span></span> <span data-ttu-id="d5150-106">Prosedyren inneholder ikke oppsettet av dataene som skal brukes i direkteoverføringen, for eksempel etterfyllingsregler, organisasjonshierarkier og vekt.</span><span class="sxs-lookup"><span data-stu-id="d5150-106">The procedure doesn't include setup of data that can be used in the Cross-dock, such as replenishment rules, organizational hierarchies, and store weights.</span></span> <span data-ttu-id="d5150-107">Prosedyren bruker demonstrasjonsfirmaet USRT.</span><span class="sxs-lookup"><span data-stu-id="d5150-107">The procedure uses the USRT demo company.</span></span>

1. <span data-ttu-id="d5150-108">Gå til Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="d5150-108">Go to All purchase orders.</span></span>
2. <span data-ttu-id="d5150-109">Velg en bestilling fra listen og klikk koblingen for å åpne den.</span><span class="sxs-lookup"><span data-stu-id="d5150-109">Select a purchase order in the list and click the link to open the order.</span></span>
3. <span data-ttu-id="d5150-110">Klikk Retail og Commerce i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="d5150-110">On the Action Pane, click Retail and Commerce.</span></span>
4. <span data-ttu-id="d5150-111">Klikk Direkteoverføring.</span><span class="sxs-lookup"><span data-stu-id="d5150-111">Click Cross docking.</span></span>
5. <span data-ttu-id="d5150-112">Klikk Rediger</span><span class="sxs-lookup"><span data-stu-id="d5150-112">Click Edit.</span></span>
    * <span data-ttu-id="d5150-113">Kategorien kan brukes til å filtrere elementene i Linjer-delen.</span><span class="sxs-lookup"><span data-stu-id="d5150-113">The category can be used to filter the items in the Lines section.</span></span>  
6. <span data-ttu-id="d5150-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d5150-114">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="d5150-115">Skriv inn en verdi i feltet Direkteoverføringsantall for å angi hvor mye av antallet som kjøpes av det valgte produktet, som skal distribueres.</span><span class="sxs-lookup"><span data-stu-id="d5150-115">In the Cross docking quantity field, type a value to specify how much of the quantity being purchased of the selected product should be distributed.</span></span>
8. <span data-ttu-id="d5150-116">Skriv inn en verdi i feltet Flere direkteoverføringsantall for å angi antallene som skal distribueres av de tilgjengelige produktene som kjøpes.</span><span class="sxs-lookup"><span data-stu-id="d5150-116">In the Additional cross docking quantity field, enter a value to specify the quantities to distribute for the available products being purchased</span></span>
9. <span data-ttu-id="d5150-117">Angi Lokasjonsvekt i feltet Distribusjon.</span><span class="sxs-lookup"><span data-stu-id="d5150-117">In the Distribution field, enter 'Location weight'.</span></span>
    * <span data-ttu-id="d5150-118">Du kan velge å bruke ulike regler for distribusjon for de andre typene.</span><span class="sxs-lookup"><span data-stu-id="d5150-118">You can select the other types to use different rules for the distribution.</span></span>  
10. <span data-ttu-id="d5150-119">Angi eller velg en verdi i feltet Etterfyllingshierarki.</span><span class="sxs-lookup"><span data-stu-id="d5150-119">In the Replenishment hierarchy field, select a value.</span></span>
11. <span data-ttu-id="d5150-120">Velg Ja i feltet Respekter sortimenter.</span><span class="sxs-lookup"><span data-stu-id="d5150-120">Select Yes in the Respect assortments field.</span></span>
12. <span data-ttu-id="d5150-121">Klikk Beregn antall.</span><span class="sxs-lookup"><span data-stu-id="d5150-121">Click Calculate quantities.</span></span>
13. <span data-ttu-id="d5150-122">Klikk Opprett ordre.</span><span class="sxs-lookup"><span data-stu-id="d5150-122">Click Create order.</span></span>
14. <span data-ttu-id="d5150-123">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="d5150-123">Click Yes.</span></span>
15. <span data-ttu-id="d5150-124">Finn og velg et lager som mottok produktene, i listen.</span><span class="sxs-lookup"><span data-stu-id="d5150-124">In the list, find and select a warehouse that received products</span></span>
16. <span data-ttu-id="d5150-125">Klikk Ordre for å vise ordrer som ble opprettet for det valgte lageret.</span><span class="sxs-lookup"><span data-stu-id="d5150-125">Click Order to view the orders that got created for the selected warehouse</span></span>

