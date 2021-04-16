---
title: Aktivere forsinket avgiftsberegning i journaler
description: Dette emnet beskriver hvordan du aktiverer funksjonen Forsinket avgiftsberegning for å forbedre ytelsen for avgiftsberegning når det er svært mange journallinjer.
author: ericwang
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: acf5ead6ed90d4dbb41de08520cde8085a7f3935
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5823722"
---
# <a name="enable-delayed-tax-calculation-on-journals"></a><span data-ttu-id="907f1-103">Aktivere forsinket avgiftsberegning i journaler</span><span class="sxs-lookup"><span data-stu-id="907f1-103">Enable delayed tax calculation on journals</span></span>
[!include [banner](../includes/banner.md)]


<span data-ttu-id="907f1-104">Dette emnet beskriver hvordan du kan forsinke beregning av merverdiavgift på journaler.</span><span class="sxs-lookup"><span data-stu-id="907f1-104">This topic explains how you can delay sales tax calculation on journals.</span></span> <span data-ttu-id="907f1-105">Denne funksjonen bidrar til å forbedre ytelsen til avgiftsberegninger når det er mange journallinjer.</span><span class="sxs-lookup"><span data-stu-id="907f1-105">This capability helps improve the performance of tax calculations when there are many journal lines.</span></span>

<span data-ttu-id="907f1-106">Som standard beregnes mva-beløp på journallinjer når avgiftsrelaterte felt blir oppdaterte.</span><span class="sxs-lookup"><span data-stu-id="907f1-106">By default, sales tax amounts on journal lines are calculated whenever tax-related fields are updated.</span></span> <span data-ttu-id="907f1-107">Disse feltene inkluderer feltene for mva-grupper for salg og mva-grupper for varer.</span><span class="sxs-lookup"><span data-stu-id="907f1-107">These fields include the fields for sales tax groups and item sales tax groups.</span></span> <span data-ttu-id="907f1-108">Eventuelle oppdateringer til en journallinje fører til at avgiftsbeløp omberegnes for alle journallinjer.</span><span class="sxs-lookup"><span data-stu-id="907f1-108">Any update to a journal line causes tax amounts to be recalculated for all journal lines.</span></span> <span data-ttu-id="907f1-109">Selv om denne virkemåten hjelper brukeren å se avgiftsbeløp beregnet i sanntid, kan det også påvirke ytelsen hvis antall journallinjer er svært stort.</span><span class="sxs-lookup"><span data-stu-id="907f1-109">Although this behavior helps user see tax amounts calculated in real time, it can also affect performance if the number of journal lines is very large.</span></span>

<span data-ttu-id="907f1-110">Funksjonen for forsinket mva-beregning gjør at du kan forsinke mva-beregningen på journaler og dermed bidra til å løse ytelsesproblemer.</span><span class="sxs-lookup"><span data-stu-id="907f1-110">The Delayed tax calculation feature lets you delay tax calculation on journals and therefore helps fix performance issues.</span></span> <span data-ttu-id="907f1-111">Når denne funksjonen er aktivert, beregnes bare avgiftsbeløp når brukeren velger **Merverdiavgift** eller posterer journalen.</span><span class="sxs-lookup"><span data-stu-id="907f1-111">When this feature is turned on, tax amounts are calculated only when a user selects **Sales Tax** or posts the journal.</span></span>

<span data-ttu-id="907f1-112">Du kan forsinke beregningen av merverdiavgift på tre nivåer:</span><span class="sxs-lookup"><span data-stu-id="907f1-112">You can delay the calculation of sales taxes at three levels:</span></span>

- <span data-ttu-id="907f1-113">Juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="907f1-113">Legal entity</span></span>
- <span data-ttu-id="907f1-114">Journalnavn</span><span class="sxs-lookup"><span data-stu-id="907f1-114">Journal name</span></span>
- <span data-ttu-id="907f1-115">Journalhode</span><span class="sxs-lookup"><span data-stu-id="907f1-115">Journal header</span></span>

<span data-ttu-id="907f1-116">Systemet gir prioritet til innstillingen for journalhodet.</span><span class="sxs-lookup"><span data-stu-id="907f1-116">The system gives priority to the setting for the journal header.</span></span> <span data-ttu-id="907f1-117">Som standard hentes denne innstillingen fra journalnavnet.</span><span class="sxs-lookup"><span data-stu-id="907f1-117">By default, this setting is taken from the journal name.</span></span> <span data-ttu-id="907f1-118">Som standard hentes innstillingen for journalnavnet fra innstillingen på siden **Parametere for økonomimodul** når journalnavnet opprettes.</span><span class="sxs-lookup"><span data-stu-id="907f1-118">By default, the setting for the journal name is taken from the setting on the **General ledger parameters** page when the journal name is created.</span></span> <span data-ttu-id="907f1-119">De følgende delene forklarer hvordan du aktiverer forsinket avgiftsberegning for juridiske enheter, journalnavn og journalhoder.</span><span class="sxs-lookup"><span data-stu-id="907f1-119">The following sections explain how to turn on delayed tax calculation for legal entities, journal names, and journal headers.</span></span>

## <a name="turn-on-delayed-tax-calculation-at-the-legal-entity-level"></a><span data-ttu-id="907f1-120">Aktivere forsinket mva-beregning på nivået for juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="907f1-120">Turn on delayed tax calculation at the legal entity level</span></span>

1. <span data-ttu-id="907f1-121">Gå til **Økonomimodul \> Finansoppsett \> Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="907f1-121">Go to **General ledger \> Ledger setup \> General ledger parameters**.</span></span>
2. <span data-ttu-id="907f1-122">I kategorien **Merverdiavgift** i hurtigfanen **Generelt** angir du alternativet **Forsinket avgiftsberegning** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="907f1-122">On the **Sales tax** tab, on the **General** FastTab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Parametere for økonomimodul-bildet](media/delayed-tax-calculation-gl.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-name-level"></a><span data-ttu-id="907f1-124">Aktivere forsinket mva-beregning på journalnavnnivå</span><span class="sxs-lookup"><span data-stu-id="907f1-124">Turn on delayed tax calculation at the journal name level</span></span>

1. <span data-ttu-id="907f1-125">Gå til **Økonomimodul \> Journaloppsett \> Journalnavn**.</span><span class="sxs-lookup"><span data-stu-id="907f1-125">Go to **General ledger \> Journal setup \> Journal names**.</span></span>
2. <span data-ttu-id="907f1-126">I hurtigfanen **Generelt** i delen **Merverdiavgift** angir du alternativet **Forsinket avgiftsberegning** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="907f1-126">On the **General** FastTab, in the **Sales tax** section, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Journalnavnbilde](media/delayed-tax-calculation-journal-name.png)

## <a name="turn-on-delayed-tax-calculation-at-the-journal-header-level"></a><span data-ttu-id="907f1-128">Aktivere forsinket mva-beregning på journalhodenivå</span><span class="sxs-lookup"><span data-stu-id="907f1-128">Turn on delayed tax calculation at the journal header level</span></span>

1. <span data-ttu-id="907f1-129">Gå til **Økonomimodul \> Journaloppføringer \> Økonomijournaler**.</span><span class="sxs-lookup"><span data-stu-id="907f1-129">Go to **General ledger \> Journal entries \> General journals**.</span></span>
2. <span data-ttu-id="907f1-130">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="907f1-130">Select **New**.</span></span>
3. <span data-ttu-id="907f1-131">Velg et journalnavn.</span><span class="sxs-lookup"><span data-stu-id="907f1-131">Select a journal name.</span></span>
4. <span data-ttu-id="907f1-132">I kategorien **Oppsett** setter du alternativet for **Forsinket avgiftsberegning** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="907f1-132">On the **Setup** tab, set the **Delayed tax calculation** option to **Yes**.</span></span>

![Bilde av økonomijournalsiden](media/delayed-tax-calculation-journal-header.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]