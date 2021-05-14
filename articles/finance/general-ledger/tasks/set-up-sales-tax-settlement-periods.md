---
title: Definere mva-utligningsperioder
description: Dette emnet forklarer hvordan du definerer mva-utligningsperioder i Dynamics 365 Finance.
author: twheeloc
ms.date: 08/05/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxPeriod
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 83587df3963d215fec020150e6b707e431c1b6eb
ms.sourcegitcommit: ab3f5d0da6eb0177bbad720e73c58926d686f168
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/26/2021
ms.locfileid: "5944783"
---
# <a name="set-up-sales-tax-settlement-periods"></a><span data-ttu-id="ddd2e-103">Definere mva-utligningsperioder</span><span class="sxs-lookup"><span data-stu-id="ddd2e-103">Set up sales tax settlement periods</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ddd2e-104">Dette emnet forklarer hvordan du definerer mva-utligningsperioder.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-104">This topic explains how to set up sales tax settlement periods.</span></span> <span data-ttu-id="ddd2e-105">Mva-utligningsperioder inneholder informasjon om periodintervallene som det må rapporteres og betales merverdiavgift for.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-105">Sales tax settlement periods contain information about the period intervals for which sales tax needs to be reported and paid.</span></span> <span data-ttu-id="ddd2e-106">En utligningsprosess kan kjøres for en utligningsperiode for et bestemt datointervall.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-106">A settlement process can be run for a settlement period for a specific date interval.</span></span> <span data-ttu-id="ddd2e-107">Alle mva-koder som er knyttet til utligningsperioden, blir utlignet.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-107">All tax codes associated with the settlement period will be settled.</span></span> <span data-ttu-id="ddd2e-108">Avhengig av oppsettet av den beslektede skattemyndigheten, posteres skattegjelden til en leverandør eller en finanskonto.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-108">Depending on the set up of the related Sales tax authority, the tax liability is posted either to a vendor or a General ledger account.</span></span>

<span data-ttu-id="ddd2e-109">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-109">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="ddd2e-110">I navigasjonsruten går du til **Moduler > Avgift > Indirekte avgifter > Merverdiavgift > Mva-utligningsperioder**.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-110">In the navigation pane, go to **Modules > Tax > Indirect taxes > Sales tax > Sales tax settlement periods**.</span></span>
2. <span data-ttu-id="ddd2e-111">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-111">Select **New**.</span></span>
3. <span data-ttu-id="ddd2e-112">Angi en verdi i feltet **Utligningsperiode**.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-112">In the **Settlement period** field, type a value.</span></span>
4. <span data-ttu-id="ddd2e-113">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-113">In the **Description** field, type a value.</span></span>
5. <span data-ttu-id="ddd2e-114">I **Skattemyndighet**-feltet velger du skattemyndigheten som skal motta rapportene og betalingene som er opprettet for utligningsperioden.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-114">In the **Authority** field, select the sales tax authority that receives the reports and the payments that are created for the settlement period.</span></span>
6. <span data-ttu-id="ddd2e-115">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-115">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="ddd2e-116">Velg det ønskede oppslaget på rullegardinmenyen i feltet **Betalingsbetingelser**.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-116">In the **Terms of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="ddd2e-117">Den relaterte skattemyndigheten kan defineres som en leverandør og mva-utligningen oppretter en åpen leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-117">The related Sales tax authority can be set up as a vendor and the Sales tax settlement will create an open vendor invoice.</span></span> <span data-ttu-id="ddd2e-118">Betalingsbetingelsene definerer forfallsdatoen for den åpne leverandørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-118">The Terms of payment defines the Due date for the open vendor invoice.</span></span>  
8. <span data-ttu-id="ddd2e-119">Velg en type for utligningsperiodeintervallet.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-119">Select a type for the settlement period intervals.</span></span>
9. <span data-ttu-id="ddd2e-120">Angi antall enheter i periodeintervallet per periode.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-120">Enter the number of Period interval units per period.</span></span> <span data-ttu-id="ddd2e-121">Et kvartal har for eksempel 3 måneder.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-121">For example, a quarter has 3 months.</span></span>
10. <span data-ttu-id="ddd2e-122">Merk av eller fjern merket i avmerkingsboksen **Bruk satsvis behandling for utligning av merverdiavgift**.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-122">Select or clear the **Use batch processing for sales tax settlement** check box.</span></span> <span data-ttu-id="ddd2e-123">Utligningsprosessen for utligningsperioden kan behandles som en satsvis jobb i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-123">The settlement process for the settlement period can be processed as batch job in the background.</span></span> <span data-ttu-id="ddd2e-124">Dette anbefales for et stort antall mva-transaksjoner i et periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-124">This is recommended for a large number of tax transactions within a period interval.</span></span>
11. <span data-ttu-id="ddd2e-125">Merk eller fjern merket i avmerkingsboksen **Hindre generering av transaksjoner for motregningsavgift**.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-125">Select or clear the **Prevent generating offset tax transactions** check box.</span></span> <span data-ttu-id="ddd2e-126">Som standard genererer systemet transaksjoner for motregningsavgift under utligningsprosessen, som kan føre til ytelsesproblemer hvis det finnes et stort antall avgiftstransaksjoner i et periodeintervall.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-126">By default, the system generates offset tax transactions during the settlement process, which cause can performance issue if there are a large number of tax transactions within a period interval.</span></span> <span data-ttu-id="ddd2e-127">Merk av i denne avmerkingsboksen for å hindre generering av transaksjoner for motregningsavgift.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-127">Select this check box to prevent generating offset tax transactions.</span></span>
12. <span data-ttu-id="ddd2e-128">Utvid kategorien **Periodeintervaller**.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-128">Expand the **Period intervals** tab.</span></span>
13. <span data-ttu-id="ddd2e-129">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-129">Select **Add**.</span></span>
14. <span data-ttu-id="ddd2e-130">Angi en dato i **Fra dato**-feltet på den nye raden.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-130">In the **From date** field in the new row, enter a date.</span></span>
15. <span data-ttu-id="ddd2e-131">Angi en dato i **Til dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-131">In the **To date** field, enter a date.</span></span>
16. <span data-ttu-id="ddd2e-132">Velg **Nytt periodeintervall**.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-132">Select **New period interval**.</span></span> <span data-ttu-id="ddd2e-133">Når det første periodeintervallet er angitt, kan du opprette nye perioder automatisk.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-133">Once the first period interval has been entered, new periods can be created automatically.</span></span> <span data-ttu-id="ddd2e-134">Du kan gå tilbake og legge til nye periodeintervallene etter behov.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-134">You can come back and add new period intervals as required.</span></span>  
17. <span data-ttu-id="ddd2e-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ddd2e-135">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
