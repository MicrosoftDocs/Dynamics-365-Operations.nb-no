--- 
title: Definer mva-rapporteringskoder
description: "Mva-rapporteringskodene refererer til et feltnummer på en mva-rapport."
author: ShylaThompson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 8937e6df85a506e47f28f7b2bcfaec1650260581
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="610ad-103">Definer mva-rapporteringskoder</span><span class="sxs-lookup"><span data-stu-id="610ad-103">Set up sales tax reporting codes</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="610ad-104">Mva-rapporteringskodene refererer til et feltnummer på en mva-rapport.</span><span class="sxs-lookup"><span data-stu-id="610ad-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="610ad-105">De brukes på landspesifikke rapportoppsett og Mva-betaling etter rapporteringskode for å skrive ut mva-beløp for en utligningsperiode som er summert per rapporteringskode.</span><span class="sxs-lookup"><span data-stu-id="610ad-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="610ad-106">Når du har opprettet mva-rapporteringskodene, kan du referere til dem i hurtigkategoriene Rapportoppsett på siden Mva-kode.</span><span class="sxs-lookup"><span data-stu-id="610ad-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="610ad-107">Denne registreringen bruker demonstrasjonsfirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="610ad-107">This recording uses the DEMF demo company.</span></span>



1. <span data-ttu-id="610ad-108">Gå til Avgift > Oppsett > Merverdiavgift > Mva-rapporteringskoder.</span><span class="sxs-lookup"><span data-stu-id="610ad-108">Go to Tax > Setup > Sales tax > Sales tax reporting codes.</span></span>
2. <span data-ttu-id="610ad-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="610ad-109">Click New.</span></span>
3. <span data-ttu-id="610ad-110">Velg rapportoppsettet som rapporteringskoden tilhører.</span><span class="sxs-lookup"><span data-stu-id="610ad-110">Select the report layout that the reporting code belongs to.</span></span>
    * <span data-ttu-id="610ad-111">Dette oppsettet brukes til å filtrere de tilgjengelige rapporteringskodene for en mva-kode.</span><span class="sxs-lookup"><span data-stu-id="610ad-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="610ad-112">Hver mva-kode tilhører en utligningsperiode som tilhører en skattemyndighet som bruker et rapportoppsett.</span><span class="sxs-lookup"><span data-stu-id="610ad-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="610ad-113">Angi et nummer som refererer til et felt i en mva-rapport.</span><span class="sxs-lookup"><span data-stu-id="610ad-113">Enter a number that refers to a field on a sales tax report.</span></span>
5. <span data-ttu-id="610ad-114">I Rapporttekst-feltet angir du en beskrivelse som skal vises på rapporter.</span><span class="sxs-lookup"><span data-stu-id="610ad-114">In the Report text field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="610ad-115">I feltet Kort beskrivelse skriver du inn en kort beskrivelse for intern bruk.</span><span class="sxs-lookup"><span data-stu-id="610ad-115">In the Brief description field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="610ad-116">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="610ad-116">Click Save.</span></span>


