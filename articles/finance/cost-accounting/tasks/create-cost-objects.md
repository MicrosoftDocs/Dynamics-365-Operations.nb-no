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
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ed020348e50158362fda7b6b36dcdb17c48b4532
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3142323"
---
# <a name="create-cost-objects"></a><span data-ttu-id="ebf6c-103">Opprette kostnadsobjekter  </span><span class="sxs-lookup"><span data-stu-id="ebf6c-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ebf6c-104">Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for kostsenter til kostnadsregnskap via en datakobling.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="ebf6c-105">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="ebf6c-106">Opprette nye kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="ebf6c-106">Create new cost objects</span></span>
1. <span data-ttu-id="ebf6c-107">Gå til Kostnadsregnskap > Dimensjoner > Kostnadsobjektdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="ebf6c-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-108">Click New.</span></span>
3. <span data-ttu-id="ebf6c-109">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="ebf6c-110">Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="ebf6c-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="ebf6c-112">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="ebf6c-113">Konfigurere datakoblingen</span><span class="sxs-lookup"><span data-stu-id="ebf6c-113">Configure the data connector</span></span>
1. <span data-ttu-id="ebf6c-114">Klikk Konfigurer dimensjonsmedlemsleverandør.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="ebf6c-115">Velg CostCenter for å importere CostCenter-dimensjonen i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="ebf6c-116">Velg Kostsenter i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="ebf6c-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="ebf6c-118">Importere kostsentre</span><span class="sxs-lookup"><span data-stu-id="ebf6c-118">Import cost centers</span></span>
1. <span data-ttu-id="ebf6c-119">Klikk Importer dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="ebf6c-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="ebf6c-121">Vise de importerte kostsentrene</span><span class="sxs-lookup"><span data-stu-id="ebf6c-121">View the imported cost centers</span></span>
1. <span data-ttu-id="ebf6c-122">Klikk Vis dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="ebf6c-122">Click View dimension members.</span></span>

