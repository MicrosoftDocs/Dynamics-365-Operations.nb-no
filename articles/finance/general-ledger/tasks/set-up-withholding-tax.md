---
title: Definere kildeskatt
description: Dette emnet forklarer hvordan du definerer kildeskatt.
author: twheeloc
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxWithholdTable, TaxWithholdData, TaxWithholdGroup
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7ae7b13f743336e01f17248c8d6492b31e8044ef
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222317"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="b92b1-103">Definere kildeskatt</span><span class="sxs-lookup"><span data-stu-id="b92b1-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b92b1-104">Dette emnet forklarer hvordan du definerer kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="b92b1-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="b92b1-105">*Kildeskatt* er en leverandørskatt som ikke fører til merverditransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="b92b1-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="b92b1-106">Withholding tax som beregnes for leverandørbetaling, er gjeld.</span><span class="sxs-lookup"><span data-stu-id="b92b1-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="b92b1-107">Derfor kan man bare bruke balansekontoer eller gjeldskontoer til å postere withholding tax.</span><span class="sxs-lookup"><span data-stu-id="b92b1-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="b92b1-108">Denne oppgaveveiledningen beskriver hvordan du definerer kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="b92b1-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="b92b1-109">Gå til **Navigasjonsrute > Moduler > Avgift > Indirekte avgifter > Kildeskatt > Kildeskattkoder**.</span><span class="sxs-lookup"><span data-stu-id="b92b1-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="b92b1-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b92b1-110">Select **New**.</span></span>
3. <span data-ttu-id="b92b1-111">Skriv inn en verdi i feltet **Kildeskattkode**.</span><span class="sxs-lookup"><span data-stu-id="b92b1-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="b92b1-112">Angi navnet på kildeskattkoden i feltet **Navn på kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="b92b1-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="b92b1-113">Velg hovedkontoen for postering av kildeskattgjelden i **Hovedkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b92b1-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="b92b1-114">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b92b1-114">Select **Save**.</span></span>
7. <span data-ttu-id="b92b1-115">Velg **Verdier**, og marker den ønskede posten i listen.</span><span class="sxs-lookup"><span data-stu-id="b92b1-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="b92b1-116">Angi en prosent som brukes til beregning av kildeskatten, i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b92b1-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="b92b1-117">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b92b1-117">Select **Save**.</span></span>
10. <span data-ttu-id="b92b1-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b92b1-118">Close the page.</span></span>
11. <span data-ttu-id="b92b1-119">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b92b1-119">Select **Save**.</span></span>
12. <span data-ttu-id="b92b1-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b92b1-120">Close the page.</span></span>
13. <span data-ttu-id="b92b1-121">Gå til **Navigasjonsrute > Moduler > Avgift > Indirekte avgifter > Kildeskatt > Kildeskattgrupper**.</span><span class="sxs-lookup"><span data-stu-id="b92b1-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="b92b1-122">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b92b1-122">Select **New**.</span></span>
15. <span data-ttu-id="b92b1-123">Angi identifikatoren til kildeskattgruppen i feltet **Kildeskattgruppe**.</span><span class="sxs-lookup"><span data-stu-id="b92b1-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="b92b1-124">I **Beskrivelse**-feltet skriver du inn navnet på kildeskattgruppen.</span><span class="sxs-lookup"><span data-stu-id="b92b1-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="b92b1-125">Velg kildeskattkoden i **Kildeskattkode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b92b1-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="b92b1-126">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="b92b1-126">Select **Save**.</span></span>
19. <span data-ttu-id="b92b1-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b92b1-127">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]