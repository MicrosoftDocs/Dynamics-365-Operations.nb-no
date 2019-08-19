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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8f63827977f080aa78fb385c60f757ad6b710005
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841255"
---
# <a name="create-cost-objects"></a><span data-ttu-id="b4c77-103">Opprette kostnadsobjekter  </span><span class="sxs-lookup"><span data-stu-id="b4c77-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b4c77-104">Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for Dynamics 365 for Finance and Operations, Enterprise Edition-kostsenter til kostnadsregnskap via en datakobling.</span><span class="sxs-lookup"><span data-stu-id="b4c77-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="b4c77-105">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="b4c77-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="b4c77-106">Denne fremgangsmåten gjelder for en funksjon i kostnadsregnskap som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="b4c77-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="b4c77-107">Opprette nye kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="b4c77-107">Create new cost objects</span></span>
1. <span data-ttu-id="b4c77-108">Gå til Kostnadsregnskap > Dimensjoner > Kostnadsobjektdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="b4c77-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="b4c77-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b4c77-109">Click New.</span></span>
3. <span data-ttu-id="b4c77-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="b4c77-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="b4c77-111">Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="b4c77-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="b4c77-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="b4c77-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="b4c77-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b4c77-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="b4c77-114">Konfigurere datakoblingen</span><span class="sxs-lookup"><span data-stu-id="b4c77-114">Configure the data connector</span></span>
1. <span data-ttu-id="b4c77-115">Klikk Konfigurer dimensjonsmedlemsleverandør.</span><span class="sxs-lookup"><span data-stu-id="b4c77-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="b4c77-116">Velg CostCenter for å importere CostCenter-dimensjonen i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="b4c77-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="b4c77-117">Velg Kostsenter i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="b4c77-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="b4c77-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b4c77-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="b4c77-119">Importere kostsentre</span><span class="sxs-lookup"><span data-stu-id="b4c77-119">Import cost centers</span></span>
1. <span data-ttu-id="b4c77-120">Klikk Importer dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="b4c77-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="b4c77-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b4c77-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="b4c77-122">Vise de importerte kostsentrene</span><span class="sxs-lookup"><span data-stu-id="b4c77-122">View the imported cost centers</span></span>
1. <span data-ttu-id="b4c77-123">Klikk Vis dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="b4c77-123">Click View dimension members.</span></span>

