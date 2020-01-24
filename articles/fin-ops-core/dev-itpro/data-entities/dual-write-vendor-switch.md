---
title: Bytte mellom leverandørutforminger
description: Dette emnet beskriver hvordan du bytter mellom integreringen av leverandørdata mellom Finance and Operations-apper og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-09-20
ms.openlocfilehash: 204d788e72e79e7acf744d24cbeacb0f9b47da7d
ms.sourcegitcommit: 3306e451f04df01c51d8d332306b135d8ae1e254
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/09/2019
ms.locfileid: "2902731"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="c9a81-103">Bytte mellom leverandørutforminger</span><span class="sxs-lookup"><span data-stu-id="c9a81-103">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="c9a81-104">Flyt for leverandørdata</span><span class="sxs-lookup"><span data-stu-id="c9a81-104">Vendor data flow</span></span> 

<span data-ttu-id="c9a81-105">Hvis du vil bruke andre Dynamics 365-apper for leverandørkontroll, og du vil isolere leverandørinformasjon fra kunder, kan du bruke denne grunnleggende leverandørutformingen.</span><span class="sxs-lookup"><span data-stu-id="c9a81-105">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Grunnleggende leverandørflyt](media/dual-write-vendor-data-flow.png)
 
<span data-ttu-id="c9a81-107">Hvis du bruker andre Dynamics 365-apper for leverandørkontroll, og du vil fortsatt bruke **konto**-enheten til å lagre leverandørinformasjon, kan du bruke denne utvidede leverandørutformingen.</span><span class="sxs-lookup"><span data-stu-id="c9a81-107">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="c9a81-108">I denne utformingen blir utvidet leverandørinformasjon som leverandør på vent-status og leverandørprofil lagret i **leverandører**-enheten i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c9a81-108">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Utvidet flyt for leverandør](media/dual-write-vendor-detail.jpg)
 
<span data-ttu-id="c9a81-110">Følg fremgangsmåten nedenfor for å bruke den utvidede leverandørutformingen:</span><span class="sxs-lookup"><span data-stu-id="c9a81-110">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="c9a81-111">**SupplyChainCommon**-løsningspakken inneholder malene for arbeidsflytprosessen, som vist i følgende bilde.</span><span class="sxs-lookup"><span data-stu-id="c9a81-111">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="c9a81-112">![Maler for arbeidsflytprosess](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="c9a81-112">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="c9a81-113">Opprett nye arbeidsflytprosesser ved hjelp av malene for arbeidsflytprosess:</span><span class="sxs-lookup"><span data-stu-id="c9a81-113">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="c9a81-114">Opprett en ny arbeidsflytprosess for **leverandør**-enheten ved hjelp av malen for arbeidsflytprosess **Opprett leverandører i kontoenhet**, og klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9a81-114">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="c9a81-115">Denne arbeidsflyten håndterer leverandøropprettelsesscenarioet for **Konto**-enheten.</span><span class="sxs-lookup"><span data-stu-id="c9a81-115">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="c9a81-116">![Opprette leverandører i kontoenhet](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="c9a81-116">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="c9a81-117">Opprett en ny arbeidsflytprosess for **leverandør**-enheten ved hjelp av malen for arbeidsflytprosess **Oppdater kontoenhet**, og klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="c9a81-117">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="c9a81-118">Denne arbeidsflyten håndterer oppdateringsscenarioet for **Konto**-enheten.</span><span class="sxs-lookup"><span data-stu-id="c9a81-118">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="c9a81-119">![Oppdater kontoenhet](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="c9a81-119">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="c9a81-120">Opprett nye arbeidsflytprosesser fra malene som ble opprettet i **Kontoer**-enheten.</span><span class="sxs-lookup"><span data-stu-id="c9a81-120">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="c9a81-121">![Opprette leverandører i leverandørenhet](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="c9a81-121">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="c9a81-122">![Oppdater leverandørenhet](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="c9a81-122">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="c9a81-123">Du kan konfigurere arbeidsflytene som sanntids- eller bakgrunns-arbeidsflyter basert på dine behov.</span><span class="sxs-lookup"><span data-stu-id="c9a81-123">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="c9a81-124">![Konverter til en bakgrunnsarbeidsflyt](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="c9a81-124">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="c9a81-125">Aktiver arbeidsflytene du opprettet for **konto**- og **leverandør**-enhetene for å begynne å bruke **Konto**-enheten for lagring av leverandørinformasjon.</span><span class="sxs-lookup"><span data-stu-id="c9a81-125">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the **Account** entity for storing vendor information.</span></span> 
 