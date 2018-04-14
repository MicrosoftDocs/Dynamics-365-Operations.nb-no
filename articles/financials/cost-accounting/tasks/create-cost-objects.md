--- 
title: 'Opprette kostnadsobjekter  '
description: "Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for Dynamics 365 for Finance and Operations-kostsenter til kostnadsregnskap via en datakobling."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: e469fc30d649aac0c544b6de9e17fd173f3ce497
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="03304-103">Opprette kostnadsobjekter  </span><span class="sxs-lookup"><span data-stu-id="03304-103">Create cost objects</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="03304-104">Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for Dynamics 365 for Finance and Operations-kostsenter til kostnadsregnskap via en datakobling.</span><span class="sxs-lookup"><span data-stu-id="03304-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="03304-105">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="03304-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="03304-106">Denne fremgangsmåten gjelder for en kostnadsregnskapsfunksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="03304-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="03304-107">Opprette nye kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="03304-107">Create new cost objects</span></span>
1. <span data-ttu-id="03304-108">Gå til Kostnadsregnskap > Dimensjoner > Kostnadsobjektdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="03304-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="03304-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="03304-109">Click New.</span></span>
3. <span data-ttu-id="03304-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="03304-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="03304-111">Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="03304-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="03304-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="03304-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="03304-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="03304-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="03304-114">Konfigurere datakoblingen</span><span class="sxs-lookup"><span data-stu-id="03304-114">Configure the data connector</span></span>
1. <span data-ttu-id="03304-115">Klikk Konfigurer dimensjonsmedlemsleverandør.</span><span class="sxs-lookup"><span data-stu-id="03304-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="03304-116">Velg CostCenter for å importere CostCenter-dimensjonen i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="03304-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="03304-117">Velg Kostsenter i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="03304-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="03304-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="03304-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="03304-119">Importere kostsentre</span><span class="sxs-lookup"><span data-stu-id="03304-119">Import cost centers</span></span>
1. <span data-ttu-id="03304-120">Klikk Importer dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="03304-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="03304-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="03304-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="03304-122">Vise de importerte kostsentrene</span><span class="sxs-lookup"><span data-stu-id="03304-122">View the imported cost centers</span></span>
1. <span data-ttu-id="03304-123">Klikk Vis dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="03304-123">Click View dimension members.</span></span>


