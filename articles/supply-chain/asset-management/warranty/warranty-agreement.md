---
title: Garantiavtaler
description: Dette emnet beskriver garantiavtaler i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 71905d5b362c80d48b78210b59cacfb1e7899757
ms.sourcegitcommit: 802dbf0a744d70f9e546632d419415b0993331ab
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2019
ms.locfileid: "1874699"
---
# <a name="warranty-agreements"></a><span data-ttu-id="64ad8-103">Garantiavtaler</span><span class="sxs-lookup"><span data-stu-id="64ad8-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


<span data-ttu-id="64ad8-104">I Aktivastyring kan du definere garantibetingelser som kan knyttes til et anleggsmiddel eller en anleggsmiddeltype.</span><span class="sxs-lookup"><span data-stu-id="64ad8-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="64ad8-105">Garantibetingelser opprettes for en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="64ad8-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="64ad8-106">Garanti kan defineres for å gi fullstendig dekning eller delvis dekning, og du kan definere betingelser som er knyttet til timer, utgifter og varer.</span><span class="sxs-lookup"><span data-stu-id="64ad8-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="64ad8-107">Det første trinnet er å opprette eventuelle leverandørgarantiavtaler du har for utstyret ditt.</span><span class="sxs-lookup"><span data-stu-id="64ad8-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="64ad8-108">Deretter knytter du garantiavtaler til anleggsmidler eller anleggsmiddeltyper.</span><span class="sxs-lookup"><span data-stu-id="64ad8-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="64ad8-109">Leverandørgarantiavtaler brukes bare til informasjonsformål.</span><span class="sxs-lookup"><span data-stu-id="64ad8-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="64ad8-110">Hvis det er definert en leverandørgaranti for et anleggsmiddel, kan du se garantidekningsperioden for anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="64ad8-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="64ad8-111">Opprette en garantiavtale</span><span class="sxs-lookup"><span data-stu-id="64ad8-111">Create a warranty agreement</span></span>

<span data-ttu-id="64ad8-112">En garantiavtale kan inkludere flere avtalelinjer for å dekke garantien for arbeidstimer, utgifter og varer.</span><span class="sxs-lookup"><span data-stu-id="64ad8-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="64ad8-113">Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Garanti**.</span><span class="sxs-lookup"><span data-stu-id="64ad8-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="64ad8-114">Velg **Ny** for å opprette et produkt.</span><span class="sxs-lookup"><span data-stu-id="64ad8-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="64ad8-115">Angi en garanti-ID i **Garanti**-feltet.</span><span class="sxs-lookup"><span data-stu-id="64ad8-115">In the **Warranty** field, enter a warranty ID.</span></span>
4. <span data-ttu-id="64ad8-116">Angi en beskrivelse i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="64ad8-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="64ad8-117">I hurtigfanen **Detaljer** viser **Aktiva**-feltet antall aktive anleggsmidler som bruker garantiavtalen.</span><span class="sxs-lookup"><span data-stu-id="64ad8-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="64ad8-118">I hurtigfanene **Timegaranti** og **Varegaranti** følger du denne fremgangsmåten for å legge til linjer som skal inkluderes i en garantiavtale som gjelder for timer eller varer:</span><span class="sxs-lookup"><span data-stu-id="64ad8-118">On the **Hour warranty** and **Item warranty** FastTabs, follow these steps to add lines that should be included in a warranty agreement that pertains to hours or items:</span></span>

    1. <span data-ttu-id="64ad8-119">Velg **Legg til linje** for å legge til en ny betingelse i garantien.</span><span class="sxs-lookup"><span data-stu-id="64ad8-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="64ad8-120">Et sekvensielt linjenummer angis automatisk i feltet **Linje**.</span><span class="sxs-lookup"><span data-stu-id="64ad8-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="64ad8-121">Velg type garantiperiode i **Periode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="64ad8-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="64ad8-122">Angi et tall i **Intervall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="64ad8-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="64ad8-123">Dette feltet definerer antall perioder som garantien skal være gyldig for.</span><span class="sxs-lookup"><span data-stu-id="64ad8-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="64ad8-124">I **Prosent**-feltet angir du dekningsprosenten for garantilinjen.</span><span class="sxs-lookup"><span data-stu-id="64ad8-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="64ad8-125">Prosentsatsen viser hvor mye som dekkes av firmaet.</span><span class="sxs-lookup"><span data-stu-id="64ad8-125">The percentage indicates how much is covered by your company.</span></span>

![Figur 1](media/01-warranty.png)
