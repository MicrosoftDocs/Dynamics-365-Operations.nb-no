---
title: Opprette et nytt produkt
description: Dette emnet beskriver hvordan du oppretter et nytt delt produkt.
author: ShylaThompson
manager: AnnBe
ms.date: 07/22/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductInventoryDimensionGroups
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 722414eee1e738e1438bbb40dbd9b8ca606f9245
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844807"
---
# <a name="create-a-new-product"></a><span data-ttu-id="4a6cf-103">Opprette et nytt produkt</span><span class="sxs-lookup"><span data-stu-id="4a6cf-103">Create a new product</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a6cf-104">Dette emnet beskriver hvordan du oppretter et nytt delt produkt.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-104">This topic describes how to create a new shared product.</span></span> <span data-ttu-id="4a6cf-105">Dette utføres vanligvis av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-105">It is usually carried out by a product designer.</span></span> <span data-ttu-id="4a6cf-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-product"></a><span data-ttu-id="4a6cf-107">Opprette et produkt</span><span class="sxs-lookup"><span data-stu-id="4a6cf-107">Create a product</span></span>
1. <span data-ttu-id="4a6cf-108">I navigasjonsruten går du til **Moduler > Behandling av produktinformasjon > Produkter > Produkter**.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-108">In the Navigation pane, go to **Modules > Product information management > Products > Products**.</span></span>
2. <span data-ttu-id="4a6cf-109">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-109">Select **New**.</span></span>
3. <span data-ttu-id="4a6cf-110">Skriv inn en verdi i feltet **Produktnummer**.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-110">In the **Product number** field, type a value.</span></span> <span data-ttu-id="4a6cf-111">Hvis det ikke er definert en nummerserie for produktnummeret, må det angis manuelt.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-111">If a number sequence has not been set up for the product number, it must be entered manually.</span></span>  
4. <span data-ttu-id="4a6cf-112">Skriv inn en verdi i feltet **Produktnavn**.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-112">In the **Product name** field, type a value.</span></span> <span data-ttu-id="4a6cf-113">Produktnavnet er som standard søkenavnet.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-113">The product name defaults to the search name.</span></span> <span data-ttu-id="4a6cf-114">Du kan endre verdien ved behov.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-114">You can change this if needed.</span></span>  
5. <span data-ttu-id="4a6cf-115">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-115">Select **OK**.</span></span>

## <a name="set-up-dimension-groups"></a><span data-ttu-id="4a6cf-116">Definere dimensjonsgrupper</span><span class="sxs-lookup"><span data-stu-id="4a6cf-116">Set up dimension groups</span></span>
1. <span data-ttu-id="4a6cf-117">Velg **Dimensjonsgrupper** for å åpne nedtrekksdialogen.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-117">Select **Dimension groups** to open the drop dialog.</span></span>
2. <span data-ttu-id="4a6cf-118">Angi eller velg en verdi i **Lagringsdimensjonsgruppe**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-118">In the **Storage dimension group** field, enter or select a value.</span></span> <span data-ttu-id="4a6cf-119">Lagringsdimensjonsgruppen bestemmer hvilke lagerdimensjoner du må angi for hver transaksjon for produktet og hvordan den blir sporet på lageret.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-119">The storage dimension group determines which storage dimensions you must enter on each transaction for the product and how it will be tracked in inventory.</span></span>  
3. <span data-ttu-id="4a6cf-120">Angi eller velg en verdi i **Sporingsdimensjonsgruppe**-feltet.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-120">In the **Tracking dimension group** field, enter or select a value.</span></span> <span data-ttu-id="4a6cf-121">Sporingsdimensjonsgruppen bestemmer hvilke sporingsdimensjoner du må angi for hver transaksjon for produktet og hvordan den blir håndtert på lageret.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-121">The tracking dimension group determines which tracking dimensions you must enter for each transaction for the product, and how it will be handled in inventory.</span></span>  
4. <span data-ttu-id="4a6cf-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="4a6cf-122">Select **OK**.</span></span>

