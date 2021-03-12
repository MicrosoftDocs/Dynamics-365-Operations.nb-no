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
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3d2ef7d6549bdeb3ba2afd2a594f36b47c912db
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4990773"
---
# <a name="create-cost-objects"></a><span data-ttu-id="2adfe-103">Opprette kostnadsobjekter  </span><span class="sxs-lookup"><span data-stu-id="2adfe-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2adfe-104">Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for kostsenter til kostnadsregnskap via en datakobling.</span><span class="sxs-lookup"><span data-stu-id="2adfe-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="2adfe-105">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="2adfe-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="2adfe-106">Opprette nye kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="2adfe-106">Create new cost objects</span></span>
1. <span data-ttu-id="2adfe-107">Gå til Kostnadsregnskap > Dimensjoner > Kostnadsobjektdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="2adfe-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="2adfe-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2adfe-108">Click New.</span></span>
3. <span data-ttu-id="2adfe-109">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2adfe-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="2adfe-110">Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="2adfe-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="2adfe-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="2adfe-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="2adfe-112">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="2adfe-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="2adfe-113">Konfigurere datakoblingen</span><span class="sxs-lookup"><span data-stu-id="2adfe-113">Configure the data connector</span></span>
1. <span data-ttu-id="2adfe-114">Klikk Konfigurer dimensjonsmedlemsleverandør.</span><span class="sxs-lookup"><span data-stu-id="2adfe-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="2adfe-115">Velg CostCenter for å importere CostCenter-dimensjonen i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="2adfe-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="2adfe-116">Velg Kostsenter i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="2adfe-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="2adfe-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2adfe-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="2adfe-118">Importere kostsentre</span><span class="sxs-lookup"><span data-stu-id="2adfe-118">Import cost centers</span></span>
1. <span data-ttu-id="2adfe-119">Klikk Importer dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="2adfe-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="2adfe-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2adfe-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="2adfe-121">Vise de importerte kostsentrene</span><span class="sxs-lookup"><span data-stu-id="2adfe-121">View the imported cost centers</span></span>
1. <span data-ttu-id="2adfe-122">Klikk Vis dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="2adfe-122">Click View dimension members.</span></span>

