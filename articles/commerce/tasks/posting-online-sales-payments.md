---
title: Postering av elektroniske salg og betalinger
description: Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner.
author: psimolin
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e3bac0cab764436a618fa570901c84ab720dbc86
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414686"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="dc9b7-103">Postering av elektroniske salg og betalinger</span><span class="sxs-lookup"><span data-stu-id="dc9b7-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dc9b7-104">Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="dc9b7-105">Postering av elektroniske salg og betalinger er en prosess i to trinn.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="dc9b7-106">Henter de elektroniske handelstransaksjonsdataene i HK.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="dc9b7-107">Synkroniserer ordrer for å opprette salgsordrer på hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="dc9b7-108">Å hente elektroniske transaksjonsdata kan gjøres manuelt ved å kjøre P-jobben eller ved å opprette en gjentakende satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="dc9b7-109">Kjøre P-jobben manuelt</span><span class="sxs-lookup"><span data-stu-id="dc9b7-109">Manually running the P-job</span></span>

1. <span data-ttu-id="dc9b7-110">Gå til Alle arbeidsområder > IT for Retail og Commerce.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="dc9b7-111">Klikk på Distribusjonsplan.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="dc9b7-112">Velg P-0001.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-112">Select P-0001.</span></span>
4. <span data-ttu-id="dc9b7-113">Juster kanaldatabasegrupper hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="dc9b7-114">Klikk Kjør nå.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-114">Click Run now.</span></span>
6. <span data-ttu-id="dc9b7-115">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="dc9b7-116">Planlegge en regelmessig P-jobb</span><span class="sxs-lookup"><span data-stu-id="dc9b7-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="dc9b7-117">Gå til Alle arbeidsområder > IT for Retail og Commerce.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="dc9b7-118">Klikk på Distribusjonsplan.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="dc9b7-119">Velg P-0001.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-119">Select P-0001.</span></span>
4. <span data-ttu-id="dc9b7-120">Klikk på Opprett satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-120">Click Create batch job.</span></span>
5. <span data-ttu-id="dc9b7-121">Klikk på Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-121">Click Run in the background.</span></span>
5. <span data-ttu-id="dc9b7-122">Aktiver satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="dc9b7-123">Klikk på Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-123">Click Recurrence..</span></span>
7. <span data-ttu-id="dc9b7-124">Velg Ingen sluttdato.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-124">Select the No end date option.</span></span>
8. <span data-ttu-id="dc9b7-125">I Antall-feltet angir du intervallet mellom kjøringer i minutter.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="dc9b7-126">Vanligvis vil dette være 5-10.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="dc9b7-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-127">Click OK.</span></span>
10. <span data-ttu-id="dc9b7-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-128">Click OK.</span></span>

<span data-ttu-id="dc9b7-129">Ordrer kan synkroniseres enten ved å kjøre Synkroniser ordrer-jobben manuelt, eller ved å opprette en gjentakende satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="dc9b7-130">Kjøre ordresynkronisering manuelt</span><span class="sxs-lookup"><span data-stu-id="dc9b7-130">Manually running order synchronization</span></span> 

<span data-ttu-id="dc9b7-131">Følg denne fremgangsmåten for å kjøre jobben Synkroniser ordrer manuelt én gang.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="dc9b7-132">Gå til Alle arbeidsområder > Finans for butikk.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="dc9b7-133">Klikk Synkroniser ordrer.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="dc9b7-134">Velg Butikker etter område i Organisasjonshierarki-feltet.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="dc9b7-135">Velg en bestemt nettbutikk eller velg en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="dc9b7-136">Klikk pilen for å legge til valget.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="dc9b7-137">Klikk fanen Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="dc9b7-138">Deaktiver satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-138">Disable Batch processing</span></span>
6. <span data-ttu-id="dc9b7-139">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-139">Click Recurrence.</span></span>
7. <span data-ttu-id="dc9b7-140">Velg Avslutt etter-alternativet.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-140">Select End After option</span></span>
8. <span data-ttu-id="dc9b7-141">Angi 1 i feltet Avslutt etter.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="dc9b7-142">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-142">Click OK.</span></span>
10. <span data-ttu-id="dc9b7-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="dc9b7-144">Planlegge regelmessig ordresynkronisering</span><span class="sxs-lookup"><span data-stu-id="dc9b7-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="dc9b7-145">Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="dc9b7-146">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="dc9b7-147">Gå til Alle arbeidsområder > Finans for butikk.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="dc9b7-148">Klikk Synkroniser ordrer.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="dc9b7-149">Velg Butikker etter område i Organisasjonshierarki-feltet.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="dc9b7-150">Velg en bestemt nettbutikk eller velg en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="dc9b7-151">Klikk pilen for å legge til valget.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="dc9b7-152">Klikk fanen Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="dc9b7-153">Aktiver satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-153">Enable Batch processing</span></span>
6. <span data-ttu-id="dc9b7-154">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-154">Click Recurrence.</span></span>
7. <span data-ttu-id="dc9b7-155">Velg Ingen sluttdato.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-155">Select the No end date option.</span></span>
8. <span data-ttu-id="dc9b7-156">I Antall-feltet angir du intervallet mellom kjøringer i minutter.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="dc9b7-157">Vanligvis vil dette være 2-20.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="dc9b7-158">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-158">Click OK.</span></span>
10. <span data-ttu-id="dc9b7-159">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="dc9b7-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="dc9b7-160">Dataenheter som er involvert i prosessen</span><span class="sxs-lookup"><span data-stu-id="dc9b7-160">Data entities involved in the process</span></span>

- <span data-ttu-id="dc9b7-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="dc9b7-161">RetailTransactionTable</span></span>
- <span data-ttu-id="dc9b7-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="dc9b7-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="dc9b7-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="dc9b7-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="dc9b7-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="dc9b7-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="dc9b7-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="dc9b7-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="dc9b7-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="dc9b7-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="dc9b7-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="dc9b7-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="dc9b7-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="dc9b7-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="dc9b7-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="dc9b7-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="dc9b7-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="dc9b7-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="dc9b7-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="dc9b7-171">RetailTransactionAttributeTrans</span></span>
