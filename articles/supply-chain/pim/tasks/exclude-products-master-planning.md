---
title: Opprette en produktlivssyklustilstand for å utelukke produkter fra hovedplanlegging
description: Denne prosedyren viser hvordan du oppretter en ny produktlivssyklustilstand som utelukker produktene fra hovedplanlegging og beregning av stykklistenivå.
author: cvocph
manager: tfehr
ms.date: 12/05/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6bb18f876e7d279624f60f01c5fbf4e449e9ab27
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4986885"
---
# <a name="create-a-product-lifecycle-state-to-exclude-products-from-master-planning"></a><span data-ttu-id="c9d03-103">Opprette en produktlivssyklustilstand for å utelukke produkter fra hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="c9d03-103">Create a product lifecycle state to exclude products from Master planning</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="c9d03-104">Denne prosedyren viser hvordan du oppretter en ny produktlivssyklustilstand som utelukker produktene fra hovedplanlegging og beregning av stykklistenivå.</span><span class="sxs-lookup"><span data-stu-id="c9d03-104">This procedure shows how to create a new product lifecycle state that excludes the products from Master planning and BOM-level calculation.</span></span>


## <a name="create-an-obsolete-state"></a><span data-ttu-id="c9d03-105">Opprette en foreldet tilstand</span><span class="sxs-lookup"><span data-stu-id="c9d03-105">Create an obsolete state</span></span>
1. <span data-ttu-id="c9d03-106">Gå til Behandling av produktinformasjon > Oppsett > Livssyklustilstand for produkt.</span><span class="sxs-lookup"><span data-stu-id="c9d03-106">Go to Product information management > Setup > Product lifecycle state.</span></span>
2. <span data-ttu-id="c9d03-107">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="c9d03-107">Click New.</span></span>
3. <span data-ttu-id="c9d03-108">Skriv inn en verdi i feltet Tilstand.</span><span class="sxs-lookup"><span data-stu-id="c9d03-108">In the State field, type a value.</span></span>
4. <span data-ttu-id="c9d03-109">Velg Nei i Er aktiv for planlegging-feltet.</span><span class="sxs-lookup"><span data-stu-id="c9d03-109">Select No in the Is active for planning field.</span></span>
5. <span data-ttu-id="c9d03-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="c9d03-110">In the Description field, type a value.</span></span>

## <a name="associate-the-obsolete-state-to-a-released-product"></a><span data-ttu-id="c9d03-111">Knytte den utdaterte tilstanden til et frigitt produkt</span><span class="sxs-lookup"><span data-stu-id="c9d03-111">Associate the obsolete state to a released product</span></span>
1. <span data-ttu-id="c9d03-112">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="c9d03-112">Close the page.</span></span>
2. <span data-ttu-id="c9d03-113">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="c9d03-113">Go to Product information management > Products > Released products.</span></span>
3. <span data-ttu-id="c9d03-114">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="c9d03-114">Use the Quick Filter to find records.</span></span> <span data-ttu-id="c9d03-115">Du kan for eksempel filtrere på Søkenavn-feltet med verdien M00.</span><span class="sxs-lookup"><span data-stu-id="c9d03-115">For example, filter on the Search name field with a value of 'M00'.</span></span>
4. <span data-ttu-id="c9d03-116">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="c9d03-116">Click Edit.</span></span>
5. <span data-ttu-id="c9d03-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c9d03-117">In the list, mark the selected row.</span></span>
6. <span data-ttu-id="c9d03-118">Angi eller velg en verdi i feltet Livssyklustilstand for produkt.</span><span class="sxs-lookup"><span data-stu-id="c9d03-118">In the Product lifecycle state field, enter or select a value.</span></span>

