---
title: Aktivere lønnsprosessen for timeregistrering
description: Denne fremgangsmåten viser hvordan du aktiverer lønnsprosessen for timeregistrering.
author: johanhoffmann
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgPayTable, JmgPayRate, JmgPayAgreementTable, JmgPayAgreementLine, HcmWorker
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0174f438396d814d153befe4a59a79b6eebb2288
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560192"
---
# <a name="enable-the-payroll-process-for-time-and-attendance"></a><span data-ttu-id="4b15a-103">Aktivere lønnsprosessen for timeregistrering</span><span class="sxs-lookup"><span data-stu-id="4b15a-103">Enable the payroll process for time and attendance</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4b15a-104">Denne fremgangsmåten viser hvordan du aktiverer lønnsprosessen for timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="4b15a-104">This procedure shows how to enable the payroll process for time and attendance.</span></span> <span data-ttu-id="4b15a-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="4b15a-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-pay-type-with-a-related-pay-rate"></a><span data-ttu-id="4b15a-106">Opprette en lønnstype med en relatert lønnssats</span><span class="sxs-lookup"><span data-stu-id="4b15a-106">Create a pay type with a related pay rate</span></span>
1. <span data-ttu-id="4b15a-107">Timeregistrering > Oppsett > Lønn > Lønnstyper</span><span class="sxs-lookup"><span data-stu-id="4b15a-107">Time and attendance > Setup > Payroll > Pay types</span></span>
2. <span data-ttu-id="4b15a-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4b15a-108">Click New.</span></span>
3. <span data-ttu-id="4b15a-109">Skriv inn en verdi i Lønnstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b15a-109">In the Pay type field, type a value.</span></span>
4. <span data-ttu-id="4b15a-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4b15a-110">In the Description field, type a value.</span></span>
5. <span data-ttu-id="4b15a-111">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4b15a-111">Click Save.</span></span>
6. <span data-ttu-id="4b15a-112">Klikk Satser.</span><span class="sxs-lookup"><span data-stu-id="4b15a-112">Click Rates.</span></span>
    * <span data-ttu-id="4b15a-113">Satser for lønnstyper defineres for bestemte tidsintervaller, og enkeltstående satser kan opprettes for ansatte.</span><span class="sxs-lookup"><span data-stu-id="4b15a-113">Rates for pay types are set up for specific time intervals, and individual rates can be created for workers.</span></span> <span data-ttu-id="4b15a-114">Det er ikke alltid nødvendig å opprette satser for lønnstyper i timeregistrering.</span><span class="sxs-lookup"><span data-stu-id="4b15a-114">It is not always necessary to create rates for pay types in time and attendance.</span></span> <span data-ttu-id="4b15a-115">Denne informasjonen kan allerede finnes i lønnssystemet som brukes til å generere lønn.</span><span class="sxs-lookup"><span data-stu-id="4b15a-115">This information may already exist in the payroll system that is used to generate wages.</span></span>  
7. <span data-ttu-id="4b15a-116">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4b15a-116">Click New.</span></span>
8. <span data-ttu-id="4b15a-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4b15a-117">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="4b15a-118">Angi et tall i Sats-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b15a-118">In the Rate field, enter a number.</span></span>
10. <span data-ttu-id="4b15a-119">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4b15a-119">Click Save.</span></span>

## <a name="create-a-pay-agreement"></a><span data-ttu-id="4b15a-120">Opprette en lønnsavtale</span><span class="sxs-lookup"><span data-stu-id="4b15a-120">Create a pay agreement</span></span>
1. <span data-ttu-id="4b15a-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b15a-121">Close the page.</span></span>
2. <span data-ttu-id="4b15a-122">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b15a-122">Close the page.</span></span>
3. <span data-ttu-id="4b15a-123">Gå til Lønnsavtaler.</span><span class="sxs-lookup"><span data-stu-id="4b15a-123">Go to Pay agreements.</span></span>
    * <span data-ttu-id="4b15a-124">Timeregistrering > Oppsett > Lønnsavtaler</span><span class="sxs-lookup"><span data-stu-id="4b15a-124">Time and attendance > Setup > Pay agreements</span></span>  
4. <span data-ttu-id="4b15a-125">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4b15a-125">Click New.</span></span>
5. <span data-ttu-id="4b15a-126">Skriv inn en verdi i Lønnsavtale-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b15a-126">In the Pay agreement field, type a value.</span></span>
6. <span data-ttu-id="4b15a-127">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4b15a-127">In the Description field, type a value.</span></span>
7. <span data-ttu-id="4b15a-128">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4b15a-128">Click Save.</span></span>
8. <span data-ttu-id="4b15a-129">Klikk Avtalelinjer.</span><span class="sxs-lookup"><span data-stu-id="4b15a-129">Click Agreement lines.</span></span>
9. <span data-ttu-id="4b15a-130">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4b15a-130">Click New.</span></span>
10. <span data-ttu-id="4b15a-131">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4b15a-131">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="4b15a-132">Angi eller velg en verdi i Profiltype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b15a-132">In the Profile type field, enter or select a value.</span></span>
12. <span data-ttu-id="4b15a-133">Angi eller velg en verdi i Lønnstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b15a-133">In the Pay type field, enter or select a value.</span></span>

## <a name="set-up-pay-agreement-for-time-and-registration-worker"></a><span data-ttu-id="4b15a-134">Sette opp lønnsavtale for tid og registrering for arbeider</span><span class="sxs-lookup"><span data-stu-id="4b15a-134">Set up pay agreement for time and registration worker</span></span>
1. <span data-ttu-id="4b15a-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b15a-135">Close the page.</span></span>
2. <span data-ttu-id="4b15a-136">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4b15a-136">Close the page.</span></span>
3. <span data-ttu-id="4b15a-137">Gå til Tidsregistreringsarbeidere.</span><span class="sxs-lookup"><span data-stu-id="4b15a-137">Go to Time registration workers.</span></span>
    * <span data-ttu-id="4b15a-138">Timeregistrering > Oppsett > Tidsregistreringsarbeidere</span><span class="sxs-lookup"><span data-stu-id="4b15a-138">Time and attendance > Setup > Time registration workers</span></span>  
4. <span data-ttu-id="4b15a-139">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4b15a-139">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="4b15a-140">Klikk kategorien Ansettelse.</span><span class="sxs-lookup"><span data-stu-id="4b15a-140">Click the Employment tab.</span></span>
6. <span data-ttu-id="4b15a-141">Utvid delen Tidsregistrering.</span><span class="sxs-lookup"><span data-stu-id="4b15a-141">Expand the Time registration section.</span></span>
7. <span data-ttu-id="4b15a-142">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="4b15a-142">Click Edit.</span></span>
8. <span data-ttu-id="4b15a-143">Angi eller velg en verdi i Lønnsavtale-feltet.</span><span class="sxs-lookup"><span data-stu-id="4b15a-143">In the Pay agreement field, enter or select a value.</span></span>

