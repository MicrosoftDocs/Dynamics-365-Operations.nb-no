---
title: Definere kildeskatt
description: Dette emnet forklarer hvordan du definerer kildeskatt.
author: twheeloc
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 592afb7542fa44dcb1bf3f7354937d3c21fb1a87
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5813474"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="af258-103">Definere kildeskatt</span><span class="sxs-lookup"><span data-stu-id="af258-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="af258-104">Dette emnet forklarer hvordan du definerer kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="af258-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="af258-105">*Kildeskatt* er en leverandørskatt som ikke fører til merverditransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="af258-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="af258-106">Withholding tax som beregnes for leverandørbetaling, er gjeld.</span><span class="sxs-lookup"><span data-stu-id="af258-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="af258-107">Derfor kan man bare bruke balansekontoer eller gjeldskontoer til å postere withholding tax.</span><span class="sxs-lookup"><span data-stu-id="af258-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="af258-108">Denne oppgaveveiledningen beskriver hvordan du definerer kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="af258-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="af258-109">Gå til **Navigasjonsrute > Moduler > Avgift > Indirekte avgifter > Kildeskatt > Kildeskattkoder**.</span><span class="sxs-lookup"><span data-stu-id="af258-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="af258-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="af258-110">Select **New**.</span></span>
3. <span data-ttu-id="af258-111">Skriv inn en verdi i feltet **Kildeskattkode**.</span><span class="sxs-lookup"><span data-stu-id="af258-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="af258-112">Angi navnet på kildeskattkoden i feltet **Navn på kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="af258-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="af258-113">Velg hovedkontoen for postering av kildeskattgjelden i **Hovedkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="af258-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="af258-114">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="af258-114">Select **Save**.</span></span>
7. <span data-ttu-id="af258-115">Velg **Verdier**, og marker den ønskede posten i listen.</span><span class="sxs-lookup"><span data-stu-id="af258-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="af258-116">Angi en prosent som brukes til beregning av kildeskatten, i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="af258-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="af258-117">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="af258-117">Select **Save**.</span></span>
10. <span data-ttu-id="af258-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="af258-118">Close the page.</span></span>
11. <span data-ttu-id="af258-119">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="af258-119">Select **Save**.</span></span>
12. <span data-ttu-id="af258-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="af258-120">Close the page.</span></span>
13. <span data-ttu-id="af258-121">Gå til **Navigasjonsrute > Moduler > Avgift > Indirekte avgifter > Kildeskatt > Kildeskattgrupper**.</span><span class="sxs-lookup"><span data-stu-id="af258-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="af258-122">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="af258-122">Select **New**.</span></span>
15. <span data-ttu-id="af258-123">Angi identifikatoren til kildeskattgruppen i feltet **Kildeskattgruppe**.</span><span class="sxs-lookup"><span data-stu-id="af258-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="af258-124">I **Beskrivelse**-feltet skriver du inn navnet på kildeskattgruppen.</span><span class="sxs-lookup"><span data-stu-id="af258-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="af258-125">Velg kildeskattkoden i **Kildeskattkode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="af258-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="af258-126">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="af258-126">Select **Save**.</span></span>
19. <span data-ttu-id="af258-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="af258-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]