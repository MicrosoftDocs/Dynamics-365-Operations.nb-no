---
title: Opprett et nytt produkt
description: Denne oppgaven beskriver hvordan du oppretter et nytt delt produkt.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7a603d89749242a4c6039ab83da286ec6ab727d8
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "328545"
---
# <a name="create-a-new-product"></a><span data-ttu-id="5bea2-103">Opprett et nytt produkt</span><span class="sxs-lookup"><span data-stu-id="5bea2-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5bea2-104">Denne oppgaven beskriver hvordan du oppretter et nytt delt produkt.</span><span class="sxs-lookup"><span data-stu-id="5bea2-104">This task shows how to create a new shared product.</span></span> <span data-ttu-id="5bea2-105">Dette utføres vanligvis av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="5bea2-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="5bea2-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="5bea2-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="5bea2-107">Gå til Behandling av produktinformasjon > Produkter > Produkter.</span><span class="sxs-lookup"><span data-stu-id="5bea2-107">Go to Product information management > Products > Products.</span></span>

## <a name="create-a-product"></a><span data-ttu-id="5bea2-108">Opprette et produkt</span><span class="sxs-lookup"><span data-stu-id="5bea2-108">Create a product</span></span>
1. <span data-ttu-id="5bea2-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="5bea2-109">Click New.</span></span>
2. <span data-ttu-id="5bea2-110">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="5bea2-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="5bea2-111">Hvis det ikke er definert en nummerserie for produktnummeret, må det angis manuelt.</span><span class="sxs-lookup"><span data-stu-id="5bea2-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
3. <span data-ttu-id="5bea2-112">Skriv inn en verdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="5bea2-112">In the Product name field, type a value.</span></span>
    * <span data-ttu-id="5bea2-113">Produktnavnet er som standard søkenavnet.</span><span class="sxs-lookup"><span data-stu-id="5bea2-113">The product name defaults to the search name.</span></span> <span data-ttu-id="5bea2-114">Du kan endre verdien ved behov.</span><span class="sxs-lookup"><span data-stu-id="5bea2-114">You can change this if needed.</span></span>  
4. <span data-ttu-id="5bea2-115">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5bea2-115">Click OK.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="5bea2-116">Definere dimensjonsgrupper</span><span class="sxs-lookup"><span data-stu-id="5bea2-116">Set up dimension groups</span></span>
1. <span data-ttu-id="5bea2-117">Klikk Dimensjonsgrupper for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="5bea2-117">Click Dimension groups to open the drop dialog.</span></span>
2. <span data-ttu-id="5bea2-118">Angi eller velg en verdi i lagringsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="5bea2-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5bea2-119">Lagringsdimensjonsgruppen bestemmer hvilke lagerdimensjoner du må angi for hver transaksjon for produktet og hvordan den blir sporet på lageret.</span><span class="sxs-lookup"><span data-stu-id="5bea2-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="5bea2-120">Angi eller velg en verdi i sporingsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="5bea2-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="5bea2-121">Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner du må angi for hver transaksjon for produktet og hvordan den blir håndtert på lageret.</span><span class="sxs-lookup"><span data-stu-id="5bea2-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="5bea2-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5bea2-122">Click OK.</span></span>

