---
title: Garantiavtaler
description: Dette emnet beskriver garantiavtaler i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: f049165fd12dfae672293e0c30ddb186ad3ed12c
ms.sourcegitcommit: 18c5ef10e311f3dd2dbf45c6439ae6beff921af8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2020
ms.locfileid: "3719244"
---
# <a name="warranty-agreements"></a><span data-ttu-id="26621-103">Garantiavtaler</span><span class="sxs-lookup"><span data-stu-id="26621-103">Warranty agreements</span></span>

[!include [banner](../../includes/banner.md)]

 


<span data-ttu-id="26621-104">I Aktivastyring kan du definere garantibetingelser som kan knyttes til et anleggsmiddel eller en anleggsmiddeltype.</span><span class="sxs-lookup"><span data-stu-id="26621-104">In Asset Management, you can set up warranty terms that can be connected to an asset or an asset type.</span></span> <span data-ttu-id="26621-105">Garantibetingelser opprettes for en bestemt periode.</span><span class="sxs-lookup"><span data-stu-id="26621-105">Warranty terms are created for a specific period.</span></span> <span data-ttu-id="26621-106">Garanti kan defineres for å gi fullstendig dekning eller delvis dekning, og du kan definere betingelser som er knyttet til timer, utgifter og varer.</span><span class="sxs-lookup"><span data-stu-id="26621-106">Warranty can be set up to provide full coverage or partial coverage, and you can set up terms that are related to hours, expenses, and items.</span></span>

<span data-ttu-id="26621-107">Det første trinnet er å opprette eventuelle leverandørgarantiavtaler du har for utstyret ditt.</span><span class="sxs-lookup"><span data-stu-id="26621-107">The first step is to create any vendor warranty agreements that you have for your equipment.</span></span> <span data-ttu-id="26621-108">Deretter knytter du garantiavtaler til anleggsmidler eller anleggsmiddeltyper.</span><span class="sxs-lookup"><span data-stu-id="26621-108">You then attach warranty agreements to assets or asset types.</span></span> <span data-ttu-id="26621-109">Leverandørgarantiavtaler brukes bare til informasjonsformål.</span><span class="sxs-lookup"><span data-stu-id="26621-109">Vendor warranty agreements are used only for informational purposes.</span></span> <span data-ttu-id="26621-110">Hvis det er definert en leverandørgaranti for et anleggsmiddel, kan du se garantidekningsperioden for anleggsmidlet.</span><span class="sxs-lookup"><span data-stu-id="26621-110">If vendor warranty is set up on an asset, you can see the warranty coverage period on the asset.</span></span>

## <a name="create-a-warranty-agreement"></a><span data-ttu-id="26621-111">Opprette en garantiavtale</span><span class="sxs-lookup"><span data-stu-id="26621-111">Create a warranty agreement</span></span>

<span data-ttu-id="26621-112">En garantiavtale kan inkludere flere avtalelinjer for å dekke garantien for arbeidstimer, utgifter og varer.</span><span class="sxs-lookup"><span data-stu-id="26621-112">A warranty agreement can include several agreement lines to cover the warranty for work hours, expenses, and items.</span></span>

1. <span data-ttu-id="26621-113">Velg **Aktivastyring** \> **Oppsett** \> **Aktiva** \> **Garanti**.</span><span class="sxs-lookup"><span data-stu-id="26621-113">Select **Asset management** \> **Setup** \> **Assets** \> **Warranty**.</span></span>
2. <span data-ttu-id="26621-114">Velg **Ny** for å opprette et produkt.</span><span class="sxs-lookup"><span data-stu-id="26621-114">Select **New** to create a product.</span></span>
3. <span data-ttu-id="26621-115">Angi en garanti-ID i **Garanti**-feltet.</span><span class="sxs-lookup"><span data-stu-id="26621-115">In the **Warranty** field, enter a warranty ID.</span></span> 
4. <span data-ttu-id="26621-116">Angi en beskrivelse i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="26621-116">In the **Name** field, enter a description.</span></span>

    <span data-ttu-id="26621-117">I hurtigfanen **Detaljer** viser **Aktiva**-feltet antall aktive anleggsmidler som bruker garantiavtalen.</span><span class="sxs-lookup"><span data-stu-id="26621-117">On the **Details** FastTab, the **Assets** field shows the number of active assets that use the warranty agreement.</span></span>

5. <span data-ttu-id="26621-118">På hurtigfanen **Garantilinjer** følger du denne fremgangsmåten for å legge til linjer som skal tas med i en garantiavtale:</span><span class="sxs-lookup"><span data-stu-id="26621-118">On the **Warranty lines** FastTab, follow these steps to add lines that should be included in a warranty agreement:</span></span>

    1. <span data-ttu-id="26621-119">Velg **Legg til linje** for å legge til en ny betingelse i garantien.</span><span class="sxs-lookup"><span data-stu-id="26621-119">Select **Add line** to add a new condition to the warranty.</span></span> <span data-ttu-id="26621-120">Et sekvensielt linjenummer angis automatisk i feltet **Linje**.</span><span class="sxs-lookup"><span data-stu-id="26621-120">A sequential line number is automatically entered in the **Line** field.</span></span>
    2. <span data-ttu-id="26621-121">Velg type garantiperiode i **Periode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="26621-121">In the **Period** field, select the type of warranty period.</span></span>
    3. <span data-ttu-id="26621-122">Angi et tall i **Intervall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="26621-122">In the **Interval** field, enter a number.</span></span> <span data-ttu-id="26621-123">Dette feltet definerer antall perioder som garantien skal være gyldig for.</span><span class="sxs-lookup"><span data-stu-id="26621-123">This field defines the number of periods that the warranty should be valid for.</span></span>
    4. <span data-ttu-id="26621-124">I **Prosent**-feltet angir du dekningsprosenten for garantilinjen.</span><span class="sxs-lookup"><span data-stu-id="26621-124">In the **Percent** field, enter the coverage percentage for the warranty line.</span></span> <span data-ttu-id="26621-125">Prosentsatsen viser hvor mye som dekkes av firmaet.</span><span class="sxs-lookup"><span data-stu-id="26621-125">The percentage indicates how much is covered by your company.</span></span>

![Garantiside](media/01-warranty.png)
