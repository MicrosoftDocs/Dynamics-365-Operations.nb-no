---
title: Bytte mellom leverandørutforminger
description: ''
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
ms.openlocfilehash: 4e97ff0b0e6195b5e3703e15a0bb0de7644ef8d1
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2772370"
---
# <a name="switch-between-vendor-designs"></a><span data-ttu-id="d92cf-102">Bytte mellom leverandørutforminger</span><span class="sxs-lookup"><span data-stu-id="d92cf-102">Switch between vendor designs</span></span>

[!include [banner](../includes/banner.md)]

## <a name="vendor-data-flow"></a><span data-ttu-id="d92cf-103">Flyt for leverandørdata</span><span class="sxs-lookup"><span data-stu-id="d92cf-103">Vendor data flow</span></span> 

<span data-ttu-id="d92cf-104">Hvis du vil bruke andre Dynamics 365-apper for leverandørkontroll, og du vil isolere leverandørinformasjon fra kunder, kan du bruke denne grunnleggende leverandørutformingen.</span><span class="sxs-lookup"><span data-stu-id="d92cf-104">If you use other Dynamics 365 apps for vendor mastering and you want to isolate vendor information from customers, use this basic vendor design.</span></span>  

![Grunnleggende leverandørflyt](media/dual-write-switch-1.png)
 
<span data-ttu-id="d92cf-106">Hvis du bruker andre Dynamics 365-apper for leverandørkontroll, og du vil fortsatt bruke **konto**-enheten til å lagre leverandørinformasjon, kan du bruke denne utvidede leverandørutformingen.</span><span class="sxs-lookup"><span data-stu-id="d92cf-106">If you use other Dynamics 365 apps for vendor mastering and you want to continue to use the **Account** entity for storing vendor information, use this extended vendor design.</span></span> <span data-ttu-id="d92cf-107">I denne utformingen blir utvidet leverandørinformasjon som leverandør på vent-status og leverandørprofil lagret i **leverandører**-enheten i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="d92cf-107">In this design, extended vendor information like vendor on-hold status and vendor profile is stored in the **vendors** entity in Common Data Service.</span></span> 

![Utvidet flyt for leverandør](media/dual-write-switch-2.png)
 
<span data-ttu-id="d92cf-109">Følg fremgangsmåten nedenfor for å bruke den utvidede leverandørutformingen:</span><span class="sxs-lookup"><span data-stu-id="d92cf-109">Follow the below steps to use the extended vendor design:</span></span> 
 
1. <span data-ttu-id="d92cf-110">**SupplyChainCommon**-løsningspakken inneholder malene for arbeidsflytprosessen, som vist i følgende bilde.</span><span class="sxs-lookup"><span data-stu-id="d92cf-110">The **SupplyChainCommon** solution package contains the workflow process templates as shown in the following image.</span></span>
    > [!div class="mx-imgBorder"]
    > <span data-ttu-id="d92cf-111">![Maler for arbeidsflytprosess](media/dual-write-switch-3.png)</span><span class="sxs-lookup"><span data-stu-id="d92cf-111">![Workflow process templates](media/dual-write-switch-3.png)</span></span>
2. <span data-ttu-id="d92cf-112">Opprett nye arbeidsflytprosesser ved hjelp av malene for arbeidsflytprosess:</span><span class="sxs-lookup"><span data-stu-id="d92cf-112">Create new workflow processes using the workflow process templates:</span></span> 
    1. <span data-ttu-id="d92cf-113">Opprett en ny arbeidsflytprosess for **leverandør**-enheten ved hjelp av malen for arbeidsflytprosess **Opprett leverandører i kontoenhet**, og klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="d92cf-113">Create a new workflow process for the **Vendor** entity using the **Create Vendors in Account Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="d92cf-114">Denne arbeidsflyten håndterer leverandøropprettelsesscenarioet for **Konto**-enheten.</span><span class="sxs-lookup"><span data-stu-id="d92cf-114">This workflow handles the vendor creation scenario for the **Account** entity.</span></span>
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="d92cf-115">![Opprette leverandører i kontoenhet](media/dual-write-switch-4.png)</span><span class="sxs-lookup"><span data-stu-id="d92cf-115">![Create Vendors in Account Entity](media/dual-write-switch-4.png)</span></span>
    2. <span data-ttu-id="d92cf-116">Opprett en ny arbeidsflytprosess for **leverandør**-enheten ved hjelp av malen for arbeidsflytprosess **Oppdater kontoenhet**, og klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="d92cf-116">Create a new workflow process for the **Vendor** entity using the **Update Accounts Entity** workflow process template and click **OK**.</span></span> <span data-ttu-id="d92cf-117">Denne arbeidsflyten håndterer oppdateringsscenarioet for **Konto**-enheten.</span><span class="sxs-lookup"><span data-stu-id="d92cf-117">This workflow handles the vendor update scenario for the **Account** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="d92cf-118">![Oppdater kontoenhet](media/dual-write-switch-5.png)</span><span class="sxs-lookup"><span data-stu-id="d92cf-118">![Update Accounts Entity](media/dual-write-switch-5.png)</span></span>
    3. <span data-ttu-id="d92cf-119">Opprett nye arbeidsflytprosesser fra malene som ble opprettet i **Kontoer**-enheten.</span><span class="sxs-lookup"><span data-stu-id="d92cf-119">Create new workflow processes from the templates created on the **Accounts** entity.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="d92cf-120">![Opprette leverandører i leverandørenhet](media/dual-write-switch-6.png)
        > </span><span class="sxs-lookup"><span data-stu-id="d92cf-120">![Create vendors in vendors entity](media/dual-write-switch-6.png)
        > </span></span>[!div class="mx-imgBorder"]
<span data-ttu-id="d92cf-121">![Oppdater leverandørenhet](media/dual-write-switch-7.png)</span><span class="sxs-lookup"><span data-stu-id="d92cf-121">![Update vendors entity](media/dual-write-switch-7.png)</span></span>
    4. <span data-ttu-id="d92cf-122">Du kan konfigurere arbeidsflytene som sanntids- eller bakgrunns-arbeidsflyter basert på dine behov.</span><span class="sxs-lookup"><span data-stu-id="d92cf-122">You can configure the workflows as real-time or background workflows based on your requirements.</span></span> 
        > [!div class="mx-imgBorder"]
        > <span data-ttu-id="d92cf-123">![Konverter til en bakgrunnsarbeidsflyt](media/dual-write-switch-8.png)</span><span class="sxs-lookup"><span data-stu-id="d92cf-123">![Convert to a background workflow](media/dual-write-switch-8.png)</span></span>
    5. <span data-ttu-id="d92cf-124">Aktiver arbeidsflytene du opprettet for **konto**- og **leverandør**-enhetene for å begynne å bruke Customer Engagement **Konto**-enheten for lagring av leverandørinformasjon.</span><span class="sxs-lookup"><span data-stu-id="d92cf-124">Activate the workflows that you created on the **Account** and **Vendor** entities to start using the Customer Engagement **Account** entity for storing vendor information.</span></span> 
 
