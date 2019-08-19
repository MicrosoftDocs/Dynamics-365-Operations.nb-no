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
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e8f52b73c07aad1047d6e6e7caf80daecc9c26e7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1839791"
---
# <a name="set-up-fixed-asset-groups"></a><span data-ttu-id="f626b-103">Definer anleggsmiddelgrupper</span><span class="sxs-lookup"><span data-stu-id="f626b-103">Set up fixed asset groups</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f626b-104">Denne fremgangsmåten viser hvordan du oppretter en ny anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="f626b-104">This procedure shows how to create a new fixed asset group.</span></span> <span data-ttu-id="f626b-105">Den bruker regnskapsførerrollen og demodataene for den juridiske enheten USMF.</span><span class="sxs-lookup"><span data-stu-id="f626b-105">It uses the Accountant role and demo data for the USMF legal entity.</span></span>

1. <span data-ttu-id="f626b-106">Gå til Anleggsmidler > Oppsett > Anleggsmiddelgrupper.</span><span class="sxs-lookup"><span data-stu-id="f626b-106">Go to Fixed assets > Setup > Fixed asset groups.</span></span>
2. <span data-ttu-id="f626b-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f626b-107">Click New.</span></span>
3. <span data-ttu-id="f626b-108">Skriv inn en verdi i feltet Anleggsmiddelgruppe.</span><span class="sxs-lookup"><span data-stu-id="f626b-108">In the Fixed asset group field, type a value.</span></span>
4. <span data-ttu-id="f626b-109">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="f626b-109">In the Name field, type a value.</span></span>
    * <span data-ttu-id="f626b-110">Automatisk nummerering av anleggsmidler og nummerseriekode i anleggsmiddelgruppen overstyrer innstillingene i parametere for anleggsmidler.</span><span class="sxs-lookup"><span data-stu-id="f626b-110">Autonumber fixed assets and Number sequence code on the Fixed asset group will override the settings on the Fixed assets parameters.</span></span> <span data-ttu-id="f626b-111">Du kan endre det her hvis anleggsmidlene i denne anleggsmiddelgruppen skal ha forskjellig nummerering fra andre grupper.</span><span class="sxs-lookup"><span data-stu-id="f626b-111">You can change it here if the assets in this fixed asset group will have different numbering from other groups.</span></span>  
5. <span data-ttu-id="f626b-112">Klikk Tablåer.</span><span class="sxs-lookup"><span data-stu-id="f626b-112">Click Books.</span></span>
6. <span data-ttu-id="f626b-113">Angi eller velg en verdi i feltet Tablå.</span><span class="sxs-lookup"><span data-stu-id="f626b-113">In the Book field, enter or select a value.</span></span>
    * <span data-ttu-id="f626b-114">Feltet Beregn avskrivning er satt til Ja, så anleggsmiddeltablået inkluderes i avskrivningsforslag.</span><span class="sxs-lookup"><span data-stu-id="f626b-114">The Calculate depreciation field is set to Yes, so the asset book will be included in depreciation proposals.</span></span> <span data-ttu-id="f626b-115">Hvis Beregn avskrivning er satt til Nei, vil anleggsmidlet ikke automatisk avskrives.</span><span class="sxs-lookup"><span data-stu-id="f626b-115">If Calculate depreciation is set to No, the asset will not be automatically depreciated.</span></span>  
7. <span data-ttu-id="f626b-116">Angi levetiden for anleggsmidlet i år.</span><span class="sxs-lookup"><span data-stu-id="f626b-116">Set the Service life of the asset, in years.</span></span>
    * <span data-ttu-id="f626b-117">Merk at verdien i feltet Avskrivningsperioder beregnes etter at levetiden er angitt.</span><span class="sxs-lookup"><span data-stu-id="f626b-117">Note that the Depreciation periods field value is calculated after setting the Service life.</span></span>  
8. <span data-ttu-id="f626b-118">Velg et alternativ i feltet Avskrivningskonvensjon.</span><span class="sxs-lookup"><span data-stu-id="f626b-118">In the Depreciation convention field, select an option.</span></span>
9. <span data-ttu-id="f626b-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f626b-119">Close the page.</span></span>

