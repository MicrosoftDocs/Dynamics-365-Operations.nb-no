---
title: 'Opprette kostnadsobjekter  '
description: Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for kostsenter til kostnadsregnskap via en datakobling.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1219cb15ecec7c156579c5cf7c3a3511a141e00b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5810060"
---
# <a name="create-cost-objects"></a><span data-ttu-id="da512-103">Opprette kostnadsobjekter  </span><span class="sxs-lookup"><span data-stu-id="da512-103">Create cost objects</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da512-104">Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for kostsenter til kostnadsregnskap via en datakobling.</span><span class="sxs-lookup"><span data-stu-id="da512-104">This procedure shows how to create cost objects by importing the cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="da512-105">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="da512-105">The USMF demo company was used to create this procedure.</span></span> 


## <a name="create-new-cost-objects"></a><span data-ttu-id="da512-106">Opprette nye kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="da512-106">Create new cost objects</span></span>
1. <span data-ttu-id="da512-107">Gå til Kostnadsregnskap > Dimensjoner > Kostnadsobjektdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="da512-107">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="da512-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="da512-108">Click New.</span></span>
3. <span data-ttu-id="da512-109">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="da512-109">In the Name field, type a value.</span></span>
4. <span data-ttu-id="da512-110">Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="da512-110">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="da512-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="da512-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="da512-112">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="da512-112">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="da512-113">Konfigurere datakoblingen</span><span class="sxs-lookup"><span data-stu-id="da512-113">Configure the data connector</span></span>
1. <span data-ttu-id="da512-114">Klikk Konfigurer dimensjonsmedlemsleverandør.</span><span class="sxs-lookup"><span data-stu-id="da512-114">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="da512-115">Velg CostCenter for å importere CostCenter-dimensjonen i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="da512-115">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="da512-116">Velg Kostsenter i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="da512-116">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="da512-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="da512-117">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="da512-118">Importere kostsentre</span><span class="sxs-lookup"><span data-stu-id="da512-118">Import cost centers</span></span>
1. <span data-ttu-id="da512-119">Klikk Importer dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="da512-119">Click Import dimension members.</span></span>
2. <span data-ttu-id="da512-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="da512-120">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="da512-121">Vise de importerte kostsentrene</span><span class="sxs-lookup"><span data-stu-id="da512-121">View the imported cost centers</span></span>
1. <span data-ttu-id="da512-122">Klikk Vis dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="da512-122">Click View dimension members.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]