---
title: 'Opprette kostnadsobjekter  '
description: Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for Dynamics 365 for Finance and Operations, Enterprise Edition-kostsenter til kostnadsregnskap via en datakobling.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXFinancialDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1e12de1d51658092fb19f652cef7c1cc78b255b5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "322680"
---
# <a name="create-cost-objects"></a><span data-ttu-id="f5d5e-103">Opprette kostnadsobjekter  </span><span class="sxs-lookup"><span data-stu-id="f5d5e-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f5d5e-104">Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for Dynamics 365 for Finance and Operations, Enterprise Edition-kostsenter til kostnadsregnskap via en datakobling.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="f5d5e-105">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="f5d5e-106">Denne fremgangsmåten gjelder for en funksjon i kostnadsregnskap som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="f5d5e-107">Opprette nye kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="f5d5e-107">Create new cost objects</span></span>
1. <span data-ttu-id="f5d5e-108">Gå til Kostnadsregnskap > Dimensjoner > Kostnadsobjektdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="f5d5e-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-109">Click New.</span></span>
3. <span data-ttu-id="f5d5e-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="f5d5e-111">Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="f5d5e-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="f5d5e-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="f5d5e-114">Konfigurere datakoblingen</span><span class="sxs-lookup"><span data-stu-id="f5d5e-114">Configure the data connector</span></span>
1. <span data-ttu-id="f5d5e-115">Klikk Konfigurer dimensjonsmedlemsleverandør.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="f5d5e-116">Velg CostCenter for å importere CostCenter-dimensjonen i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="f5d5e-117">Velg Kostsenter i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="f5d5e-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="f5d5e-119">Importere kostsentre</span><span class="sxs-lookup"><span data-stu-id="f5d5e-119">Import cost centers</span></span>
1. <span data-ttu-id="f5d5e-120">Klikk Importer dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="f5d5e-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="f5d5e-122">Vise de importerte kostsentrene</span><span class="sxs-lookup"><span data-stu-id="f5d5e-122">View the imported cost centers</span></span>
1. <span data-ttu-id="f5d5e-123">Klikk Vis dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="f5d5e-123">Click View dimension members.</span></span>

