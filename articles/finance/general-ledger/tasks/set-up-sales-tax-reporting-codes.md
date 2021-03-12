---
title: Definer mva-rapporteringskoder
description: Mva-rapporteringskodene refererer til et feltnummer som er oppført på en mva-rapport.
author: twheeloc
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxReportCollection
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 821d4abcffbca624382aa7709c02b857fcb6e349
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4994521"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="d922c-103">Definer mva-rapporteringskoder</span><span class="sxs-lookup"><span data-stu-id="d922c-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d922c-104">Mva-rapporteringskodene refererer til et feltnummer som er oppført på en mva-rapport.</span><span class="sxs-lookup"><span data-stu-id="d922c-104">The Sales tax reporting codes refer to a field number that's listed on a sales tax report.</span></span> <span data-ttu-id="d922c-105">De brukes på landspesifikke rapportoppsett.</span><span class="sxs-lookup"><span data-stu-id="d922c-105">They are used on country-specific report layouts.</span></span> <span data-ttu-id="d922c-106">De brukes også på Mva-betaling etter kode-rapporten.</span><span class="sxs-lookup"><span data-stu-id="d922c-106">They're also used on the Sales tax payment by code report.</span></span> <span data-ttu-id="d922c-107">Denne rapporten viser mva-beløp for en utligningsperiode oppsummert for hver rapporteringskode.</span><span class="sxs-lookup"><span data-stu-id="d922c-107">That report shows sales tax amounts for a settlement period summarized for each reporting code.</span></span> <span data-ttu-id="d922c-108">Når du har opprettet mva-rapporteringskodene, kan du referere til kodene i hurtigkategoriene Rapportoppsett, som du får tilgang til fra siden **Mva-kode**.</span><span class="sxs-lookup"><span data-stu-id="d922c-108">After you create Sales tax reporting codes, you can refer to those codes on the Report setup FastTabs, which you can access from the **Sales tax code** page.</span></span> 

<span data-ttu-id="d922c-109">Denne registreringen bruker demonstrasjonsfirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="d922c-109">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="d922c-110">I **navigasjonsruten** går du til **Avgift > Oppsett > Merverdiavgift > Mva-rapporteringskoder**.</span><span class="sxs-lookup"><span data-stu-id="d922c-110">In the **Navigation pane**, go to **Tax > Setup > Sales tax > Sales tax reporting codes**.</span></span>
2. <span data-ttu-id="d922c-111">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d922c-111">Click **New**.</span></span>
3. <span data-ttu-id="d922c-112">Velg rapportoppsettet som rapporteringskoden tilhører.</span><span class="sxs-lookup"><span data-stu-id="d922c-112">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="d922c-113">Dette oppsettet brukes til å filtrere de tilgjengelige rapporteringskodene for en mva-kode.</span><span class="sxs-lookup"><span data-stu-id="d922c-113">This layout is used to filter the available reporting codes for a sales tax code.</span></span> <span data-ttu-id="d922c-114">Hver mva-kode tilhører en utligningsperiode som tilhører en skattemyndighet som bruker et rapportoppsett.</span><span class="sxs-lookup"><span data-stu-id="d922c-114">Each sales tax code belongs to a settlement period, which belongs to a Sales tax authority, which uses a report layout.</span></span>  
4. <span data-ttu-id="d922c-115">Angi et tall i feltet **Rapporteringskode**.</span><span class="sxs-lookup"><span data-stu-id="d922c-115">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="d922c-116">I **Rapporttekst**-feltet angir du en beskrivelse som skal vises på rapporter.</span><span class="sxs-lookup"><span data-stu-id="d922c-116">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="d922c-117">I feltet **Kort beskrivelse** skriver du inn en kort beskrivelse for intern bruk.</span><span class="sxs-lookup"><span data-stu-id="d922c-117">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="d922c-118">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d922c-118">Click **Save**.</span></span>

