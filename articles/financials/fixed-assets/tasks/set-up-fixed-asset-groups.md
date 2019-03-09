---
title: Definer anleggsmiddelgrupper
description: Denne fremgangsmåten viser hvordan du oppretter en ny anleggsmiddelgruppe.
author: saraschi2
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: AssetGroup, AssetGroupBookSetup
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 48784ef4eb12a4a1cae3387e3a45afdf34f2a0fd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "321806"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="dc865-103">Definer anleggsmiddelgrupper</span><span class="sxs-lookup"><span data-stu-id="dc865-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="dc865-104">Denne fremgangsmåten viser hvordan du oppretter en ny anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="dc865-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="dc865-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="dc865-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="dc865-106">Gå til Anleggsmidler > Oppsett > Anleggsmiddelgrupper.</span><span class="sxs-lookup"><span data-stu-id="dc865-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="dc865-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="dc865-107">Click New.</span></span>
3. <span data-ttu-id="dc865-108">Skriv inn en verdi i feltet Anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="dc865-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="dc865-109">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="dc865-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="dc865-110">Automatisk nummerering av anleggsmidler og nummerseriekode i anleggsmiddelgruppen overstyrer innstillingene i parametere for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="dc865-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="dc865-111">Du kan endre det her hvis anleggsmidlene i denne anleggsmiddelgruppen skal ha forskjellig nummerering fra andre grupper.</span><span class="sxs-lookup"><span data-stu-id="dc865-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="dc865-112">Klikk Tablåer.</span><span class="sxs-lookup"><span data-stu-id="dc865-112">Click Books.</span></span>
6. <span data-ttu-id="dc865-113">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="dc865-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="dc865-114">Feltet Beregn avskrivning er satt til Ja, så anleggsmiddeltablået inkluderes i avskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="dc865-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="dc865-115">Hvis Beregn avskrivning er satt til Nei, vil anleggsmidlet ikke automatisk avskrives.</span><span class="sxs-lookup"><span data-stu-id="dc865-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="dc865-116">Angi levetiden for anleggsmidlet i år.</span><span class="sxs-lookup"><span data-stu-id="dc865-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="dc865-117">Merk at verdien i feltet Avskrivningsperioder beregnes etter at levetiden er angitt.</span><span class="sxs-lookup"><span data-stu-id="dc865-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="dc865-118">Velg et alternativ i feltet Avskrivningskonvensjon.</span><span class="sxs-lookup"><span data-stu-id="dc865-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="dc865-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="dc865-119">Close the page.</span></span>

