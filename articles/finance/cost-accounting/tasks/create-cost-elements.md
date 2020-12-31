---
title: 'Opprette kostnadselementer  '
description: Det finnes flere måter å opprette kostnadselementer på i kostnadsregnskap.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension, CAMAXMainAccountDimensionMemberProviderConfiguration, CAMDimensionMember
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 87f93fd7c1c42045274d6b89847b27e93614d9a4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446532"
---
# <a name="create-cost-elements"></a><span data-ttu-id="dbf71-103">Opprette kostnadselementer  </span><span class="sxs-lookup"><span data-stu-id="dbf71-103">Create cost elements</span></span> 

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dbf71-104">Det finnes flere måter å opprette kostnadselementer på i kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="dbf71-104">There are several ways to create cost elements in Cost accounting.</span></span> <span data-ttu-id="dbf71-105">Denne fremgangsmåten viser hvordan du oppretter kostnadselementer ved å importere -hovedkontoer via en datakobling.</span><span class="sxs-lookup"><span data-stu-id="dbf71-105">This procedure shows how to create cost elements by importing main accounts via a data connector.</span></span> <span data-ttu-id="dbf71-106">Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="dbf71-106">The USMF demo company was used to create this procedure.</span></span> <span data-ttu-id="dbf71-107">Denne fremgangsmåten gjelder for en funksjon i kostnadsregnskap som ble lagt til i Dynamics 365 for Operations, versjon 1611.</span><span class="sxs-lookup"><span data-stu-id="dbf71-107">This procedure is for a Cost accounting feature that was added in Dynamics 365 for Operations, version 1611.</span></span>


## <a name="create-new-cost-elements"></a><span data-ttu-id="dbf71-108">Opprette nye kostnadselementer</span><span class="sxs-lookup"><span data-stu-id="dbf71-108">Create new cost elements</span></span>
1. <span data-ttu-id="dbf71-109">Gå til Kostnadsregnskap > Dimensjoner > Kostnadselementdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="dbf71-109">Go to Cost accounting > Dimensions > Cost element dimensions.</span></span>
2. <span data-ttu-id="dbf71-110">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="dbf71-110">Click New.</span></span>
3. <span data-ttu-id="dbf71-111">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="dbf71-111">In the Name field, type a value.</span></span>
4. <span data-ttu-id="dbf71-112">Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="dbf71-112">In the Data connector for dimension members field, enter or select a value.</span></span>
5. <span data-ttu-id="dbf71-113">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="dbf71-113">In the Description field, type a value.</span></span>
6. <span data-ttu-id="dbf71-114">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="dbf71-114">Click Save.</span></span>

## <a name="configure-the-data-connector"></a><span data-ttu-id="dbf71-115">Konfigurere datakoblingen</span><span class="sxs-lookup"><span data-stu-id="dbf71-115">Configure the data connector</span></span>
1. <span data-ttu-id="dbf71-116">Klikk Konfigurer dimensjonsmedlemsleverandør.</span><span class="sxs-lookup"><span data-stu-id="dbf71-116">Click Configure dimension member provider.</span></span>
2. <span data-ttu-id="dbf71-117">Skriv inn eller velg en verdi Kontoplan-feltet.</span><span class="sxs-lookup"><span data-stu-id="dbf71-117">In the Chart of accounts field, enter or select a value.</span></span>
    * <span data-ttu-id="dbf71-118">Velg Delt for å bruke den delte kontoplanen.</span><span class="sxs-lookup"><span data-stu-id="dbf71-118">Select Shared to use the shared chart of accounts.</span></span>  
3. <span data-ttu-id="dbf71-119">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="dbf71-119">Click New.</span></span>
4. <span data-ttu-id="dbf71-120">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="dbf71-120">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="dbf71-121">Du kan bruke filtre på kontoer som oppfyller kriteriene dine.</span><span class="sxs-lookup"><span data-stu-id="dbf71-121">You can apply filters to accounts to meet your criteria.</span></span>  
5. <span data-ttu-id="dbf71-122">Angi eller velg en verdi i feltet Fra hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="dbf71-122">In the From main account field, enter or select a value.</span></span>
6. <span data-ttu-id="dbf71-123">Angi eller velg en verdi i feltet Til hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="dbf71-123">In the To main account field, enter or select a value.</span></span>
7. <span data-ttu-id="dbf71-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="dbf71-124">Click OK.</span></span>

## <a name="import-main-accounts"></a><span data-ttu-id="dbf71-125">Importer hovedkontoer</span><span class="sxs-lookup"><span data-stu-id="dbf71-125">Import main accounts</span></span>
1. <span data-ttu-id="dbf71-126">Klikk Importer dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="dbf71-126">Click Import dimension members.</span></span>
    * <span data-ttu-id="dbf71-127">Hovedkontoer blir importert til kostnadsregnskap og brukt som kostnadselementer.</span><span class="sxs-lookup"><span data-stu-id="dbf71-127">Main accounts will be imported into Cost accounting and used as cost elements.</span></span>  
2. <span data-ttu-id="dbf71-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="dbf71-128">Click OK.</span></span>

## <a name="view-the-imported-accounts-as-cost-elements"></a><span data-ttu-id="dbf71-129">Vise de importerte kontoene som kostnadselementer</span><span class="sxs-lookup"><span data-stu-id="dbf71-129">View the imported accounts as cost elements</span></span>
1. <span data-ttu-id="dbf71-130">Klikk Vis dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="dbf71-130">Click View dimension members.</span></span>
    * <span data-ttu-id="dbf71-131">Vis de importerte finanskontoene som kostnadselementer i bedriften som kostnader kan flyte til.</span><span class="sxs-lookup"><span data-stu-id="dbf71-131">View the imported ledger accounts as cost elements in your business that costs can flow to.</span></span>  

