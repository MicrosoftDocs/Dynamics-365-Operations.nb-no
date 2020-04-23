---
title: Opprette et nytt produkt
description: Dette emnet beskriver hvordan du oppretter et nytt delt produkt.
author: ShylaThompson
manager: tfehr
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0bf15359e085b541407bb49c266f7d9505893e25
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3203716"
---
# <a name="create-a-new-product"></a><span data-ttu-id="2ae66-103">Opprette et nytt produkt</span><span class="sxs-lookup"><span data-stu-id="2ae66-103">Create a new product</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2ae66-104">Dette emnet beskriver hvordan du oppretter et nytt delt produkt.</span><span class="sxs-lookup"><span data-stu-id="2ae66-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="2ae66-105">Dette utføres vanligvis av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="2ae66-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="2ae66-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="2ae66-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="2ae66-107">Opprette et produkt</span><span class="sxs-lookup"><span data-stu-id="2ae66-107">Create a product</span></span>
1. <span data-ttu-id="2ae66-108">I navigasjonsruten går du til **Moduler > Behandling av produktinformasjon > Produkter > Produkter**.</span><span class="sxs-lookup"><span data-stu-id="2ae66-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="2ae66-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2ae66-109">Select **New**.</span></span>
3. <span data-ttu-id="2ae66-110">Skriv inn en verdi i feltet **Produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="2ae66-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="2ae66-111">Hvis det ikke er definert en nummerserie for produktnummeret, må det angis manuelt.</span><span class="sxs-lookup"><span data-stu-id="2ae66-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="2ae66-112">Skriv inn en verdi i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="2ae66-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="2ae66-113">Produktnavnet er som standard søkenavnet.</span><span class="sxs-lookup"><span data-stu-id="2ae66-113">The product name defaults to the search name.</span></span> <span data-ttu-id="2ae66-114">Du kan endre verdien ved behov.</span><span class="sxs-lookup"><span data-stu-id="2ae66-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="2ae66-115">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ae66-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="2ae66-116">Definere dimensjonsgrupper</span><span class="sxs-lookup"><span data-stu-id="2ae66-116">Set up dimension groups</span></span>
1. <span data-ttu-id="2ae66-117">Velg **Dimensjonsgrupper** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="2ae66-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="2ae66-118">Angi eller velg en verdi i **Lagringsdimensjonsgruppe**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2ae66-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="2ae66-119">Lagringsdimensjonsgruppen bestemmer hvilke lagerdimensjoner du må angi for hver transaksjon for produktet og hvordan den blir sporet på lageret.</span><span class="sxs-lookup"><span data-stu-id="2ae66-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="2ae66-120">Angi eller velg en verdi i **Sporingsdimensjonsgruppe**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2ae66-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="2ae66-121">Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner du må angi for hver transaksjon for produktet og hvordan den blir håndtert på lageret.</span><span class="sxs-lookup"><span data-stu-id="2ae66-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="2ae66-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2ae66-122">Select **OK**.</span></span>

