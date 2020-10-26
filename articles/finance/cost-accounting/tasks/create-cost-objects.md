---
title: 'Opprette kostnadsobjekter  '
description: Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for kostsenter til kostnadsregnskap via en datakobling.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 55f5f6e5048f70e744cb3dc82a2a279aae69b4af
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976121"
---
# <a name="create-cost-objects"></a><span data-ttu-id="fa300-103">Opprette kostnadsobjekter  </span><span class="sxs-lookup"><span data-stu-id="fa300-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fa300-104">Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for kostsenter til kostnadsregnskap via en datakobling.</span><span class="sxs-lookup"><span data-stu-id="fa300-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="fa300-105">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="fa300-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="fa300-106">Opprette nye kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="fa300-106">Create new cost objects</span></span>
1. <span data-ttu-id="fa300-107">Gå til Kostnadsregnskap > Dimensjoner > Kostnadsobjektdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="fa300-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="fa300-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="fa300-108">Click New.</span></span>
3. <span data-ttu-id="fa300-109">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="fa300-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="fa300-110">Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="fa300-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="fa300-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="fa300-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="fa300-112">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fa300-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="fa300-113">Konfigurere datakoblingen</span><span class="sxs-lookup"><span data-stu-id="fa300-113">Configure the data connector</span></span>
1. <span data-ttu-id="fa300-114">Klikk Konfigurer dimensjonsmedlemsleverandør.</span><span class="sxs-lookup"><span data-stu-id="fa300-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="fa300-115">Velg CostCenter for å importere CostCenter-dimensjonen i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="fa300-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="fa300-116">Velg Kostsenter i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="fa300-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="fa300-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="fa300-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="fa300-118">Importere kostsentre</span><span class="sxs-lookup"><span data-stu-id="fa300-118">Import cost centers</span></span>
1. <span data-ttu-id="fa300-119">Klikk Importer dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="fa300-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="fa300-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="fa300-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="fa300-121">Vise de importerte kostsentrene</span><span class="sxs-lookup"><span data-stu-id="fa300-121">View the imported cost centers</span></span>
1. <span data-ttu-id="fa300-122">Klikk Vis dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="fa300-122">Click View dimension members.</span></span>

