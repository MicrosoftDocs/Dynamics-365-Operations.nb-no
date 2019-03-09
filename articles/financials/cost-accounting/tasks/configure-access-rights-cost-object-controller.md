---
title: Konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt
description: Bruk denne prosedyren til å konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt.
author: ShylaThompson
manager: AnnBe
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6b7018f9d4926321341af94efd13911e2c69f5f5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "351177"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="556f3-103">Konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="556f3-103">Configure access rights for a cost object controller</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="556f3-104">Bruk denne prosedyren til å konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="556f3-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="556f3-105">Denne registreringen bruker USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="556f3-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="556f3-106">Tilordne rollen Kontroller for kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="556f3-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="556f3-107">Gå til Systemadministrasjon > Brukere > Brukere.</span><span class="sxs-lookup"><span data-stu-id="556f3-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="556f3-108">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="556f3-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="556f3-109">Du kan for eksempel filtrere på Brukernavn-feltet med verdien 'alicia'.</span><span class="sxs-lookup"><span data-stu-id="556f3-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="556f3-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="556f3-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="556f3-111">Klikk Tilordne roller.</span><span class="sxs-lookup"><span data-stu-id="556f3-111">Click Assign roles.</span></span>
5. <span data-ttu-id="556f3-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="556f3-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="556f3-113">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="556f3-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="556f3-114">Aktiver sikkerhet for tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="556f3-114">Enable access list security</span></span>
1. <span data-ttu-id="556f3-115">Gå til Kostnadsregnskap > Dimensjoner > Dimensjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="556f3-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="556f3-116">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="556f3-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="556f3-117">Velg Organisasjon.</span><span class="sxs-lookup"><span data-stu-id="556f3-117">Select Organization.</span></span>  
3. <span data-ttu-id="556f3-118">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="556f3-118">Click Edit.</span></span>
4. <span data-ttu-id="556f3-119">Velg Ja i feltet Hierarki for tilgangsliste.</span><span class="sxs-lookup"><span data-stu-id="556f3-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="556f3-120">Klikk Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="556f3-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="556f3-121">Tilordne tilgangsrettigheter til bruker</span><span class="sxs-lookup"><span data-stu-id="556f3-121">Assign access rights to user</span></span>
1. <span data-ttu-id="556f3-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="556f3-122">Click New.</span></span>
2. <span data-ttu-id="556f3-123">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="556f3-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="556f3-124">Angi eller velg en verdi i feltet Bruker-ID.</span><span class="sxs-lookup"><span data-stu-id="556f3-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="556f3-125">Velg Administrator.</span><span class="sxs-lookup"><span data-stu-id="556f3-125">Select Admin.</span></span>  
4. <span data-ttu-id="556f3-126">Velg 'Organisasjon\CEO\CFO\FIM' i treet.</span><span class="sxs-lookup"><span data-stu-id="556f3-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="556f3-127">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="556f3-127">Click New.</span></span>
6. <span data-ttu-id="556f3-128">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="556f3-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="556f3-129">Angi eller velg en verdi i feltet Bruker-ID.</span><span class="sxs-lookup"><span data-stu-id="556f3-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="556f3-130">Velg Alicia.</span><span class="sxs-lookup"><span data-stu-id="556f3-130">Select Alicia.</span></span>  
8. <span data-ttu-id="556f3-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="556f3-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="556f3-132">Aktivere tilgangsrettigheter i kostnadsregnskap</span><span class="sxs-lookup"><span data-stu-id="556f3-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="556f3-133">Gå til Kostnadsregnskap > Oppsett > Parametere.</span><span class="sxs-lookup"><span data-stu-id="556f3-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="556f3-134">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="556f3-134">Click the General tab.</span></span>
3. <span data-ttu-id="556f3-135">Velg Ja i feltet Aktiver visningstilgang for dimensjonsmedlemmer for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="556f3-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="556f3-136">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="556f3-136">Click Save.</span></span>
5. <span data-ttu-id="556f3-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="556f3-137">Close the page.</span></span>
6. <span data-ttu-id="556f3-138">Gå til Kostnadsregnskap > Oppsett > Konfigurasjon av arbeidsområde for kostnadskontroll.</span><span class="sxs-lookup"><span data-stu-id="556f3-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="556f3-139">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="556f3-139">Click Edit.</span></span>
8. <span data-ttu-id="556f3-140">Velg Ja i feltet Publisert.</span><span class="sxs-lookup"><span data-stu-id="556f3-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="556f3-141">Hvis du velger Ja, kan en bruker som er tilordnet en av følgende fire roller se rapportene i kostnaden control arbeidsområdet: regnskapsansvarlig, regnskapsfører, regnskapsfører clerk og kostnader objekt kontrollert.</span><span class="sxs-lookup"><span data-stu-id="556f3-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="556f3-142">Hvis du velger Nei, bare brukere som er tilordnet en av følgende roller kan se rapportene: kostnadsregnskap overordnede, regnskapsfører og regnskapsfører clerk.</span><span class="sxs-lookup"><span data-stu-id="556f3-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="556f3-143">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="556f3-143">Click Save.</span></span>

