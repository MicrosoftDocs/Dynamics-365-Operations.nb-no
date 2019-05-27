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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543777"
---
# <a name="create-cost-objects"></a><span data-ttu-id="121a8-103">Opprette kostnadsobjekter  </span><span class="sxs-lookup"><span data-stu-id="121a8-103">Create cost objects</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="121a8-104">Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for Dynamics 365 for Finance and Operations, Enterprise Edition-kostsenter til kostnadsregnskap via en datakobling.</span><span class="sxs-lookup"><span data-stu-id="121a8-104">This procedure shows how to create cost objects by importing the Dynamics 365 for Finance and Operations, Enterprise edition cost center financial dimension into Cost accounting via a data connector.</span></span> <span data-ttu-id="121a8-105">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="121a8-105">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="121a8-106">Denne fremgangsmåten gjelder for en funksjon i kostnadsregnskap som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="121a8-106">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-objects"></a><span data-ttu-id="121a8-107">Opprette nye kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="121a8-107">Create new cost objects</span></span>
1. <span data-ttu-id="121a8-108">Gå til Kostnadsregnskap > Dimensjoner > Kostnadsobjektdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="121a8-108">Go to Cost accounting > Dimensions > Cost object dimensions.</span></span>
2. <span data-ttu-id="121a8-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="121a8-109">Click New.</span></span>
3. <span data-ttu-id="121a8-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="121a8-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="121a8-111">Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="121a8-111">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="121a8-112">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="121a8-112">In the Description field, type a value.</span></span>
6. <span data-ttu-id="121a8-113">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="121a8-113">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="121a8-114">Konfigurere datakoblingen</span><span class="sxs-lookup"><span data-stu-id="121a8-114">Configure the data connector</span></span>
1. <span data-ttu-id="121a8-115">Klikk Konfigurer dimensjonsmedlemsleverandør.</span><span class="sxs-lookup"><span data-stu-id="121a8-115">Click Configure dimension member provider.</span></span>
    * <span data-ttu-id="121a8-116">Velg CostCenter for å importere CostCenter-dimensjonen i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="121a8-116">Select CostCenter to import the CostCenter dimension into Cost accounting.</span></span>  
2. <span data-ttu-id="121a8-117">Velg Kostsenter i feltet Dimensjonsnavn.</span><span class="sxs-lookup"><span data-stu-id="121a8-117">In the Dimension name field, select Cost center.</span></span>
3. <span data-ttu-id="121a8-118">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="121a8-118">Click OK.</span></span>

## <a name="import-cost-centers"></a><span data-ttu-id="121a8-119">Importere kostsentre</span><span class="sxs-lookup"><span data-stu-id="121a8-119">Import cost centers</span></span>
1. <span data-ttu-id="121a8-120">Klikk Importer dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="121a8-120">Click Import dimension members.</span></span>
2. <span data-ttu-id="121a8-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="121a8-121">Click OK.</span></span>

## <a name="view-the-imported-cost-centers"></a><span data-ttu-id="121a8-122">Vise de importerte kostsentrene</span><span class="sxs-lookup"><span data-stu-id="121a8-122">View the imported cost centers</span></span>
1. <span data-ttu-id="121a8-123">Klikk Vis dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="121a8-123">Click View dimension members.</span></span>

