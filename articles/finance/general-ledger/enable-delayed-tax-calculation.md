---
title: Aktivere forsinket avgiftsberegning på journal
description: Dette emnet beskriver hvordan du bruker funksjonen **Aktivere forsinket avgiftsberegning på journal** til å forbedre ytelsen for avgiftsberegning når det er svært mange journallinjer.
author: ericwang
manager: Ann Beebe
ms.date: 09/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TaxTable
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: vstehman
ms.search.validFrom: 2019-09-18
ms.dyn365.ops.version: 10.0.7
ms.openlocfilehash: 5a8ae30a007d3e2b8b7a9bc9eb7786f6e58246d0
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2179180"
---
# <a name="enable-delayed-tax-calculation-on-journal"></a><span data-ttu-id="64001-103">Aktivere forsinket avgiftsberegning på journal</span><span class="sxs-lookup"><span data-stu-id="64001-103">Enable delayed tax calculation on journal</span></span>
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="64001-104">Dette emnet beskriver hvordan du bruker funksjonen **Aktivere forsinket avgiftsberegning på journal** til å forbedre ytelsen for avgiftsberegning når det er svært mange journallinjer.</span><span class="sxs-lookup"><span data-stu-id="64001-104">This topic explains how to use the **Enable delayed tax calculation on journal** feature to improve tax calculation performance when the volume of journal lines is huge.</span></span>

<span data-ttu-id="64001-105">Gjeldende virkemåte for avgiftsberegning for journalen utløses i sanntid når brukeren oppdaterer avgiftsrelaterte felt, for eksempel mva-gruppe/mva-gruppe for vare.</span><span class="sxs-lookup"><span data-stu-id="64001-105">Current sales tax calculation behavior on journal is real-time triggered when user updates tax related fields, e.g. sales tax group/item sales tax group.</span></span> <span data-ttu-id="64001-106">Alle oppdateringer på journallinjenivå vil beregne avgiftsbeløp på nytt på alle journallinjer.</span><span class="sxs-lookup"><span data-stu-id="64001-106">Any update at journal line level will re-calculate tax amount on all journal lines.</span></span> <span data-ttu-id="64001-107">Den hjelper brukeren med å se sanntidsberegnet avgiftsbeløp, men det kan også føre til ytelsesproblemer hvis det er svært mange journallinjer.</span><span class="sxs-lookup"><span data-stu-id="64001-107">It helps user to see real-time calculated tax amount but it could also bring performance issue if  the volume of journal lines is huge.</span></span>

<span data-ttu-id="64001-108">Denne funksjonen gir mulighet til å forsinke avgiftsberegningen for å løse ytelsesproblemer.</span><span class="sxs-lookup"><span data-stu-id="64001-108">This feature provides an option to delay tax calculation to solve performance issue.</span></span> <span data-ttu-id="64001-109">Hvis denne funksjonen er aktivert, beregnes bare avgiftsbeløp når brukeren klikker på kommandoen Merverdiavgift eller posterer journalen.</span><span class="sxs-lookup"><span data-stu-id="64001-109">If this feature is turned on, tax amount will only be calculated when user clicks "Sales Tax" command or posts the journal.</span></span>

<span data-ttu-id="64001-110">Brukeren kan aktivere/deaktivere parameteren på tre nivåer:</span><span class="sxs-lookup"><span data-stu-id="64001-110">User can turn on/off the parameter at three levels:</span></span>
- <span data-ttu-id="64001-111">Etter juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="64001-111">By legal entity</span></span>
- <span data-ttu-id="64001-112">Etter journalnavn</span><span class="sxs-lookup"><span data-stu-id="64001-112">By journal name</span></span>
- <span data-ttu-id="64001-113">Etter journalhode</span><span class="sxs-lookup"><span data-stu-id="64001-113">By journal header</span></span>

<span data-ttu-id="64001-114">Systemet vil bruke parameterverdien i journalhodet som endelig.</span><span class="sxs-lookup"><span data-stu-id="64001-114">System will take the parameter value on journal header as final.</span></span> <span data-ttu-id="64001-115">Parameterverdien i journalhodet hentes som standard fra journalnavn.</span><span class="sxs-lookup"><span data-stu-id="64001-115">Parameter value on journal header will be defaulted from journal name.</span></span> <span data-ttu-id="64001-116">Parameterverdi i journalnavn blir som standard opprettet fra økonomimodulparameteren når journalnavnet opprettes.</span><span class="sxs-lookup"><span data-stu-id="64001-116">Parameter value on journal name will be defaulted from general ledger parameter when the journal name is created.</span></span>

<span data-ttu-id="64001-117">Feltene Faktisk mva-beløp og Beregnet mva-beløp i journalen, skjules hvis denne parameteren er aktivert.</span><span class="sxs-lookup"><span data-stu-id="64001-117">"Actual sales tax amount" and "Calculated sales tax amount" fields on journal will be hided if this parameter is turned on.</span></span> <span data-ttu-id="64001-118">Formålet kan ikke forvirre brukeren fordi verdien av disse to feltene alltid viser 0 før brukeren utløser avgiftsberegningen.</span><span class="sxs-lookup"><span data-stu-id="64001-118">The purpose is not to confuse user because the value of these two fields will always show 0 before user trigger the tax calculation.</span></span>

## <a name="enable-delayed-tax-calculation-by-legal-entity"></a><span data-ttu-id="64001-119">Aktivere forsinket avgiftsberegning etter juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="64001-119">Enable delayed tax calculation by legal entity</span></span>

1. <span data-ttu-id="64001-120">Gå til **Økonomimodul > Finansoppsett > Parametere for økonomimodul**.</span><span class="sxs-lookup"><span data-stu-id="64001-120">Go to **General ledger > Ledger setup > General ledger parameters**</span></span>
2. <span data-ttu-id="64001-121">Klikk på **Merverdiavgift**.</span><span class="sxs-lookup"><span data-stu-id="64001-121">Click **Sales tax** tab</span></span>
3. <span data-ttu-id="64001-122">I hurtigfanen **Generelt** finner du parameteren **Forsinket avgiftsberegning** og aktiverer/deaktiverer den</span><span class="sxs-lookup"><span data-stu-id="64001-122">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-gl.png)



## <a name="enable-delayed-tax-calculation-by-journal-name"></a><span data-ttu-id="64001-123">Aktivere forsinket avgiftsberegning etter journalnavn</span><span class="sxs-lookup"><span data-stu-id="64001-123">Enable delayed tax calculation by journal name</span></span>

1. <span data-ttu-id="64001-124">Gå til **Økonomimodul > Journaloppsett > Journalnavn**.</span><span class="sxs-lookup"><span data-stu-id="64001-124">Go to **General ledger > Journal setup > Journal names**</span></span>
2. <span data-ttu-id="64001-125">I hurtigfanen **Generelt** finner du parameteren **Forsinket avgiftsberegning** og aktiverer/deaktiverer den</span><span class="sxs-lookup"><span data-stu-id="64001-125">Under **General** fast tab, find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-name.png)

## <a name="enable-delayed-tax-calculation-by-journal"></a><span data-ttu-id="64001-126">Aktivere forsinket avgiftsberegning etter journal</span><span class="sxs-lookup"><span data-stu-id="64001-126">Enable delayed tax calculation by journal</span></span>

1. <span data-ttu-id="64001-127">Gå til **Økonomimodul > Journaloppføringer > Økonomijournaler**</span><span class="sxs-lookup"><span data-stu-id="64001-127">Go to **General ledger > Journal entries > General journals**</span></span>
2. <span data-ttu-id="64001-128">Klikk på **Ny**</span><span class="sxs-lookup"><span data-stu-id="64001-128">Click **New**</span></span>
3. <span data-ttu-id="64001-129">Velg et journalnavn</span><span class="sxs-lookup"><span data-stu-id="64001-129">Select a journal name</span></span>
4. <span data-ttu-id="64001-130">Klikk på **Oppsett**</span><span class="sxs-lookup"><span data-stu-id="64001-130">Click **Setup**</span></span>
5. <span data-ttu-id="64001-131">Finn parameteren **Forsinket avgiftsberegning** og aktiverer/deaktiverer den</span><span class="sxs-lookup"><span data-stu-id="64001-131">Find parameter **Delayed tax calculation**, turn on/off it</span></span>

![](media/delayed-tax-calculation-journal-header.png)
