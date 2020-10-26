---
title: Definer mva-rapporteringskoder
description: Mva-rapporteringskodene refererer til et feltnummer på en mva-rapport.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c18f4fb0db31a959647bb10d2b99d940646676e
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976799"
---
# <a name="set-up-sales-tax-reporting-codes"></a><span data-ttu-id="a601c-103">Definer mva-rapporteringskoder</span><span class="sxs-lookup"><span data-stu-id="a601c-103">Set up sales tax reporting codes</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a601c-104">Mva-rapporteringskodene refererer til et feltnummer på en mva-rapport.</span><span class="sxs-lookup"><span data-stu-id="a601c-104">The Sales tax reporting codes refer to a field number on a sales tax report.</span></span> <span data-ttu-id="a601c-105">De brukes på landspesifikke rapportoppsett og Mva-betaling etter rapporteringskode for å skrive ut mva-beløp for en utligningsperiode som er summert per rapporteringskode.</span><span class="sxs-lookup"><span data-stu-id="a601c-105">They are used on country specific report layouts and the Sales tax payment by code report to print sales tax amounts for a settlement period summarized per reporting code.</span></span> <span data-ttu-id="a601c-106">Når du har opprettet mva-rapporteringskodene, kan du referere til dem i hurtigkategoriene Rapportoppsett på siden Mva-kode.</span><span class="sxs-lookup"><span data-stu-id="a601c-106">After you create Sales tax reporting codes, you can refer to them on the Report setup FastTabs in the Sales tax code page.</span></span> 

<span data-ttu-id="a601c-107">Denne registreringen bruker demonstrasjonsfirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="a601c-107">This recording uses the DEMF demo company.</span></span>

1. <span data-ttu-id="a601c-108">I **navigasjonsruten** går du til **Avgift > Oppsett > Merverdiavgift > Mva-rapporteringskoder** .</span><span class="sxs-lookup"><span data-stu-id="a601c-108">In the **Navigation pane** , go to **Tax > Setup > Sales tax > Sales tax reporting codes** .</span></span>
2. <span data-ttu-id="a601c-109">Klikk på **Ny** .</span><span class="sxs-lookup"><span data-stu-id="a601c-109">Click **New** .</span></span>
3. <span data-ttu-id="a601c-110">Velg rapportoppsettet som rapporteringskoden tilhører.</span><span class="sxs-lookup"><span data-stu-id="a601c-110">Select the report layout that the reporting code belongs to.</span></span> <span data-ttu-id="a601c-111">Dette oppsettet brukes til å filtrere de tilgjengelige rapporteringskodene for en mva-kode.</span><span class="sxs-lookup"><span data-stu-id="a601c-111">This layout is used to filter the available reporting codes for a Sales tax code.</span></span> <span data-ttu-id="a601c-112">Hver mva-kode tilhører en utligningsperiode som tilhører en skattemyndighet som bruker et rapportoppsett.</span><span class="sxs-lookup"><span data-stu-id="a601c-112">Each Sales tax code belongs to a settlement period which belongs to a Sales tax authority which uses a Report layout.</span></span>  
4. <span data-ttu-id="a601c-113">Angi et tall i feltet **Rapporteringskode** .</span><span class="sxs-lookup"><span data-stu-id="a601c-113">In the **Reporting code** field, enter a number.</span></span>
5. <span data-ttu-id="a601c-114">I **Rapporttekst** -feltet angir du en beskrivelse som skal vises på rapporter.</span><span class="sxs-lookup"><span data-stu-id="a601c-114">In the **Report text** field, enter a description to display on reports.</span></span>
6. <span data-ttu-id="a601c-115">I feltet **Kort beskrivelse** skriver du inn en kort beskrivelse for intern bruk.</span><span class="sxs-lookup"><span data-stu-id="a601c-115">In the **Brief description** field, enter a description for internal purposes.</span></span>
7. <span data-ttu-id="a601c-116">Klikk **Lagre** .</span><span class="sxs-lookup"><span data-stu-id="a601c-116">Click **Save** .</span></span>

