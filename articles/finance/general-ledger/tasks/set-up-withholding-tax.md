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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 10e7018c79e54841d0729636b08ad475a94d20d5
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2185963"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="e68a9-103">Definere kildeskatt</span><span class="sxs-lookup"><span data-stu-id="e68a9-103">Set up withholding tax</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e68a9-104">Dette emnet forklarer hvordan du definerer kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="e68a9-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="e68a9-105">*Kildeskatt* er en leverandørskatt som ikke fører til merverditransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="e68a9-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="e68a9-106">Withholding tax som beregnes for leverandørbetaling, er gjeld.</span><span class="sxs-lookup"><span data-stu-id="e68a9-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="e68a9-107">Derfor kan man bare bruke balansekontoer eller gjeldskontoer til å postere withholding tax.</span><span class="sxs-lookup"><span data-stu-id="e68a9-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="e68a9-108">Denne oppgaveveiledningen beskriver hvordan du definerer kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="e68a9-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="e68a9-109">Gå til **Navigasjonsrute > Moduler > Avgift > Indirekte avgifter > Kildeskatt > Kildeskattkoder**.</span><span class="sxs-lookup"><span data-stu-id="e68a9-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes**.</span></span>
2. <span data-ttu-id="e68a9-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e68a9-110">Select **New**.</span></span>
3. <span data-ttu-id="e68a9-111">Skriv inn en verdi i feltet **Kildeskattkode**.</span><span class="sxs-lookup"><span data-stu-id="e68a9-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="e68a9-112">Angi navnet på kildeskattkoden i feltet **Navn på kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="e68a9-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="e68a9-113">Velg hovedkontoen for postering av kildeskattgjelden i **Hovedkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e68a9-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="e68a9-114">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e68a9-114">Select **Save**.</span></span>
7. <span data-ttu-id="e68a9-115">Velg **Verdier**, og marker den ønskede posten i listen.</span><span class="sxs-lookup"><span data-stu-id="e68a9-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="e68a9-116">Angi en prosent som brukes til beregning av kildeskatten, i **Verdi**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e68a9-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="e68a9-117">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e68a9-117">Select **Save**.</span></span>
10. <span data-ttu-id="e68a9-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e68a9-118">Close the page.</span></span>
11. <span data-ttu-id="e68a9-119">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e68a9-119">Select **Save**.</span></span>
12. <span data-ttu-id="e68a9-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e68a9-120">Close the page.</span></span>
13. <span data-ttu-id="e68a9-121">Gå til **Navigasjonsrute > Moduler > Avgift > Indirekte avgifter > Kildeskatt > Kildeskattgrupper**.</span><span class="sxs-lookup"><span data-stu-id="e68a9-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups**.</span></span>
14. <span data-ttu-id="e68a9-122">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e68a9-122">Select **New**.</span></span>
15. <span data-ttu-id="e68a9-123">Angi identifikatoren til kildeskattgruppen i feltet **Kildeskattgruppe**.</span><span class="sxs-lookup"><span data-stu-id="e68a9-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="e68a9-124">I **Beskrivelse**-feltet skriver du inn navnet på kildeskattgruppen.</span><span class="sxs-lookup"><span data-stu-id="e68a9-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="e68a9-125">Velg kildeskattkoden i **Kildeskattkode**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e68a9-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="e68a9-126">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="e68a9-126">Select **Save**.</span></span>
19. <span data-ttu-id="e68a9-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="e68a9-127">Close the page.</span></span>

