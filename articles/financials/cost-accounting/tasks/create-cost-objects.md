--- 
title: 'Opprette kostnadsobjekter  '
description: "Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for Dynamics 365 for Finance and Operations, Enterprise Edition-kostsenter til kostnadsregnskap via en datakobling."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.contentlocale: nb-no
ms.lasthandoff: 09/14/2018

---
# <a name="create-cost-objects"></a><span data-ttu-id="a2bee-103">Opprette kostnadsobjekter  </span><span class="sxs-lookup"><span data-stu-id="a2bee-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a2bee-104">Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for Dynamics 365 for Finance and Operations, Enterprise Edition-kostsenter til kostnadsregnskap via en datakobling.</span><span class="sxs-lookup"><span data-stu-id="a2bee-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="a2bee-105">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="a2bee-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="a2bee-106">Denne fremgangsmåten gjelder for en kostnadsregnskapsfunksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="a2bee-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="a2bee-107">Opprette nye kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="a2bee-107">Create new cost objects</span></span>
1. <span data-ttu-id="a2bee-108">Gå til Kostnadsregnskap > Dimensjoner > Kostnadsobjektdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="a2bee-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="a2bee-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a2bee-109">Click New.</span></span>
3. <span data-ttu-id="a2bee-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a2bee-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="a2bee-111">Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="a2bee-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="a2bee-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a2bee-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a2bee-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="a2bee-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="a2bee-114">Konfigurere datakoblingen</span><span class="sxs-lookup"><span data-stu-id="a2bee-114">Configure the data connector</span></span>
1. <span data-ttu-id="a2bee-115">Klikk Konfigurer dimensjonsmedlemsleverandør.</span><span class="sxs-lookup"><span data-stu-id="a2bee-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="a2bee-116">Velg CostCenter for å importere CostCenter-dimensjonen i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="a2bee-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="a2bee-117">Velg Kostsenter i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="a2bee-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="a2bee-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a2bee-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="a2bee-119">Importere kostsentre</span><span class="sxs-lookup"><span data-stu-id="a2bee-119">Import cost centers</span></span>
1. <span data-ttu-id="a2bee-120">Klikk Importer dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="a2bee-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="a2bee-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a2bee-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="a2bee-122">Vise de importerte kostsentrene</span><span class="sxs-lookup"><span data-stu-id="a2bee-122">View the imported cost centers</span></span>
1. <span data-ttu-id="a2bee-123">Klikk Vis dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="a2bee-123">Click View dimension members.</span></span>


