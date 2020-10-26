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
ms.author: roschlom
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bfa1b9e43a5745eb5b5c442998597319f196f23f
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3976751"
---
# <a name="set-up-withholding-tax"></a><span data-ttu-id="ee822-103">Definere kildeskatt</span><span class="sxs-lookup"><span data-stu-id="ee822-103">Set up withholding tax</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ee822-104">Dette emnet forklarer hvordan du definerer kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="ee822-104">This topic explains how to set up withholding tax.</span></span> <span data-ttu-id="ee822-105">*Kildeskatt* er en leverandørskatt som ikke fører til merverditransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="ee822-105">*Withholding tax* is a tax on vendors that does not create sales tax transactions.</span></span> <span data-ttu-id="ee822-106">Withholding tax som beregnes for leverandørbetaling, er gjeld.</span><span class="sxs-lookup"><span data-stu-id="ee822-106">Withholding tax that is calculated on vendor payments is a liability.</span></span> <span data-ttu-id="ee822-107">Derfor kan man bare bruke balansekontoer eller gjeldskontoer til å postere withholding tax.</span><span class="sxs-lookup"><span data-stu-id="ee822-107">Therefore, only balance sheet accounts or liability accounts are valid accounts for posting withholding tax.</span></span> <span data-ttu-id="ee822-108">Denne oppgaveveiledningen beskriver hvordan du definerer kildeskatt.</span><span class="sxs-lookup"><span data-stu-id="ee822-108">This task guide demonstrates how to set up withholding tax.</span></span>

1. <span data-ttu-id="ee822-109">Gå til **Navigasjonsrute > Moduler > Avgift > Indirekte avgifter > Kildeskatt > Kildeskattkoder** .</span><span class="sxs-lookup"><span data-stu-id="ee822-109">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax codes** .</span></span>
2. <span data-ttu-id="ee822-110">Velg **Ny** .</span><span class="sxs-lookup"><span data-stu-id="ee822-110">Select **New** .</span></span>
3. <span data-ttu-id="ee822-111">Skriv inn en verdi i feltet **Kildeskattkode** .</span><span class="sxs-lookup"><span data-stu-id="ee822-111">In the **Withholding tax code** field, type a value.</span></span>
4. <span data-ttu-id="ee822-112">Angi navnet på kildeskattkoden i feltet **Navn på kildeskatt** .</span><span class="sxs-lookup"><span data-stu-id="ee822-112">In the **Withholding tax name** field, enter the name of the withholding tax code.</span></span>
5. <span data-ttu-id="ee822-113">Velg hovedkontoen for postering av kildeskattgjelden i **Hovedkonto** -feltet.</span><span class="sxs-lookup"><span data-stu-id="ee822-113">In the **Main account** field, select the main account for posting the withholding tax liability.</span></span>
6. <span data-ttu-id="ee822-114">Velg **Lagre** .</span><span class="sxs-lookup"><span data-stu-id="ee822-114">Select **Save** .</span></span>
7. <span data-ttu-id="ee822-115">Velg **Verdier** , og marker den ønskede posten i listen.</span><span class="sxs-lookup"><span data-stu-id="ee822-115">Select **Values** and mark the desired record in the list.</span></span>
8. <span data-ttu-id="ee822-116">Angi en prosent som brukes til beregning av kildeskatten, i **Verdi** -feltet.</span><span class="sxs-lookup"><span data-stu-id="ee822-116">In the **Value** field, enter a percentage used for the calculation of the withholding tax.</span></span>
9. <span data-ttu-id="ee822-117">Velg **Lagre** .</span><span class="sxs-lookup"><span data-stu-id="ee822-117">Select **Save** .</span></span>
10. <span data-ttu-id="ee822-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ee822-118">Close the page.</span></span>
11. <span data-ttu-id="ee822-119">Velg **Lagre** .</span><span class="sxs-lookup"><span data-stu-id="ee822-119">Select **Save** .</span></span>
12. <span data-ttu-id="ee822-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ee822-120">Close the page.</span></span>
13. <span data-ttu-id="ee822-121">Gå til **Navigasjonsrute > Moduler > Avgift > Indirekte avgifter > Kildeskatt > Kildeskattgrupper** .</span><span class="sxs-lookup"><span data-stu-id="ee822-121">Go to **Navigation pane > Modules > Tax > Indirect taxes > Withholding tax > Withholding tax groups** .</span></span>
14. <span data-ttu-id="ee822-122">Velg **Ny** .</span><span class="sxs-lookup"><span data-stu-id="ee822-122">Select **New** .</span></span>
15. <span data-ttu-id="ee822-123">Angi identifikatoren til kildeskattgruppen i feltet **Kildeskattgruppe** .</span><span class="sxs-lookup"><span data-stu-id="ee822-123">In the **Withholding tax group** field, enter the identifier of the withholding tax group.</span></span>
16. <span data-ttu-id="ee822-124">I **Beskrivelse** -feltet skriver du inn navnet på kildeskattgruppen.</span><span class="sxs-lookup"><span data-stu-id="ee822-124">In the **Description** field, enter the name of the withholding tax group.</span></span>
17. <span data-ttu-id="ee822-125">Velg kildeskattkoden i **Kildeskattkode** -feltet.</span><span class="sxs-lookup"><span data-stu-id="ee822-125">In the **Withholding tax code** field, select the withholding tax code.</span></span>
18. <span data-ttu-id="ee822-126">Velg **Lagre** .</span><span class="sxs-lookup"><span data-stu-id="ee822-126">Select **Save** .</span></span>
19. <span data-ttu-id="ee822-127">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ee822-127">Close the page.</span></span>

