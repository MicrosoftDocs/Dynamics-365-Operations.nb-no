---
title: Konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt
description: Bruk denne prosedyren til å konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt.
author: ShylaThompson
ms.date: 06/27/2017
ms.topic: business-process
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eef755dd9a44ce24d3bfb2953cf9a52e6a8ac849
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5822885"
---
# <a name="configure-access-rights-for-a-cost-object-controller"></a><span data-ttu-id="b35ec-103">Konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="b35ec-103">Configure access rights for a cost object controller</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b35ec-104">Bruk denne prosedyren til å konfigurere tilgangsrettigheter for en kontroller for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="b35ec-104">Use this procedure to configure access rights for a cost object controller.</span></span> <span data-ttu-id="b35ec-105">Denne registreringen bruker USP2-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="b35ec-105">This recording uses the USP2 demo data company.</span></span>


## <a name="assign-the-cost-object-controller-role"></a><span data-ttu-id="b35ec-106">Tilordne rollen Kontroller for kostnadsobjekt</span><span class="sxs-lookup"><span data-stu-id="b35ec-106">Assign the cost object controller role</span></span>
1. <span data-ttu-id="b35ec-107">Gå til Systemadministrasjon > Brukere > Brukere.</span><span class="sxs-lookup"><span data-stu-id="b35ec-107">Go to System administration > Users > Users.</span></span>
2. <span data-ttu-id="b35ec-108">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="b35ec-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="b35ec-109">Du kan for eksempel filtrere på Brukernavn-feltet med verdien 'alicia'.</span><span class="sxs-lookup"><span data-stu-id="b35ec-109">For example, filter on the User name field with a value of 'alicia'.</span></span>
3. <span data-ttu-id="b35ec-110">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b35ec-110">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="b35ec-111">Klikk Tilordne roller.</span><span class="sxs-lookup"><span data-stu-id="b35ec-111">Click Assign roles.</span></span>
5. <span data-ttu-id="b35ec-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b35ec-112">In the list, find and select the desired record.</span></span>
6. <span data-ttu-id="b35ec-113">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b35ec-113">Click OK.</span></span>

## <a name="enable-access-list-security"></a><span data-ttu-id="b35ec-114">Aktiver sikkerhet for tilgangsliste</span><span class="sxs-lookup"><span data-stu-id="b35ec-114">Enable access list security</span></span>
1. <span data-ttu-id="b35ec-115">Gå til Kostnadsregnskap > Dimensjoner > Dimensjonshierarkier.</span><span class="sxs-lookup"><span data-stu-id="b35ec-115">Go to Cost accounting > Dimensions > Dimension hierarchies.</span></span>
2. <span data-ttu-id="b35ec-116">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b35ec-116">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b35ec-117">Velg Organisasjon.</span><span class="sxs-lookup"><span data-stu-id="b35ec-117">Select Organization.</span></span>  
3. <span data-ttu-id="b35ec-118">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="b35ec-118">Click Edit.</span></span>
4. <span data-ttu-id="b35ec-119">Velg Ja i feltet Hierarki for tilgangsliste.</span><span class="sxs-lookup"><span data-stu-id="b35ec-119">Select Yes in the Access list hierarchy field.</span></span>
5. <span data-ttu-id="b35ec-120">Klikk Vis hierarki.</span><span class="sxs-lookup"><span data-stu-id="b35ec-120">Click View hierarchy.</span></span>

## <a name="assign-access-rights-to-user"></a><span data-ttu-id="b35ec-121">Tilordne tilgangsrettigheter til bruker</span><span class="sxs-lookup"><span data-stu-id="b35ec-121">Assign access rights to user</span></span>
1. <span data-ttu-id="b35ec-122">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b35ec-122">Click New.</span></span>
2. <span data-ttu-id="b35ec-123">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b35ec-123">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="b35ec-124">Angi eller velg en verdi i feltet Bruker-ID.</span><span class="sxs-lookup"><span data-stu-id="b35ec-124">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="b35ec-125">Velg Administrator.</span><span class="sxs-lookup"><span data-stu-id="b35ec-125">Select Admin.</span></span>  
4. <span data-ttu-id="b35ec-126">Velg 'Organisasjon\CEO\CFO\FIM' i treet.</span><span class="sxs-lookup"><span data-stu-id="b35ec-126">In the tree, select 'Organization\CEO\CFO\FIM'.</span></span>
5. <span data-ttu-id="b35ec-127">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="b35ec-127">Click New.</span></span>
6. <span data-ttu-id="b35ec-128">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="b35ec-128">In the list, mark the selected row.</span></span>
7. <span data-ttu-id="b35ec-129">Angi eller velg en verdi i feltet Bruker-ID.</span><span class="sxs-lookup"><span data-stu-id="b35ec-129">In the User ID field, enter or select a value.</span></span>
    * <span data-ttu-id="b35ec-130">Velg Alicia.</span><span class="sxs-lookup"><span data-stu-id="b35ec-130">Select Alicia.</span></span>  
8. <span data-ttu-id="b35ec-131">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b35ec-131">Click Save.</span></span>

## <a name="enable-access-rights-in-cost-accounting"></a><span data-ttu-id="b35ec-132">Aktivere tilgangsrettigheter i kostnadsregnskap</span><span class="sxs-lookup"><span data-stu-id="b35ec-132">Enable access rights in Cost accounting</span></span>
1. <span data-ttu-id="b35ec-133">Gå til Kostnadsregnskap > Oppsett > Parametere.</span><span class="sxs-lookup"><span data-stu-id="b35ec-133">Go to Cost accounting > Setup > Parameters.</span></span>
2. <span data-ttu-id="b35ec-134">Klikk kategorien Generelt.</span><span class="sxs-lookup"><span data-stu-id="b35ec-134">Click the General tab.</span></span>
3. <span data-ttu-id="b35ec-135">Velg Ja i feltet Aktiver visningstilgang for dimensjonsmedlemmer for kostnadsobjekt.</span><span class="sxs-lookup"><span data-stu-id="b35ec-135">Select Yes in the Enable view access for cost object dimension members field.</span></span>
4. <span data-ttu-id="b35ec-136">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b35ec-136">Click Save.</span></span>
5. <span data-ttu-id="b35ec-137">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b35ec-137">Close the page.</span></span>
6. <span data-ttu-id="b35ec-138">Gå til Kostnadsregnskap > Oppsett > Konfigurasjon av arbeidsområde for kostnadskontroll.</span><span class="sxs-lookup"><span data-stu-id="b35ec-138">Go to Cost accounting > Setup > Cost control workspace configuration.</span></span>
7. <span data-ttu-id="b35ec-139">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="b35ec-139">Click Edit.</span></span>
8. <span data-ttu-id="b35ec-140">Velg Ja i feltet Publisert.</span><span class="sxs-lookup"><span data-stu-id="b35ec-140">Select Yes in the Published field.</span></span>
    * <span data-ttu-id="b35ec-141">Hvis du velger Ja, kan en bruker som er tilordnet en av følgende fire roller se rapportene i kostnaden control arbeidsområdet: regnskapsansvarlig, regnskapsfører, regnskapsfører clerk og kostnader objekt kontrollert.</span><span class="sxs-lookup"><span data-stu-id="b35ec-141">If you select Yes, a user who is assigned one of the following four roles can see the reports in the Cost control workspace: cost accounting manager, cost accountant, cost accountant clerk, and cost object controller.</span></span> <span data-ttu-id="b35ec-142">Hvis du velger Nei, bare brukere som er tilordnet en av følgende roller kan se rapportene: kostnadsregnskap overordnede, regnskapsfører og regnskapsfører clerk.</span><span class="sxs-lookup"><span data-stu-id="b35ec-142">If you select No, only a user who is assigned one of the following roles can see the reports: cost accounting manager, cost accountant, and cost accountant clerk.</span></span>    
9. <span data-ttu-id="b35ec-143">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="b35ec-143">Click Save.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]