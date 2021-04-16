---
title: Postering av elektroniske salg og betalinger
description: Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner.
author: psimolin
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: jashanno
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a2e482b0fb5f2cf67e687c2b278bc5b54ad09839
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802677"
---
# <a name="posting-of-online-sales-and-payments"></a><span data-ttu-id="4be2b-103">Postering av elektroniske salg og betalinger</span><span class="sxs-lookup"><span data-stu-id="4be2b-103">Posting of online sales and payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4be2b-104">Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="4be2b-104">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span>

<span data-ttu-id="4be2b-105">Postering av elektroniske salg og betalinger er en prosess i to trinn.</span><span class="sxs-lookup"><span data-stu-id="4be2b-105">Posting online sales and payments is a two-stage process.</span></span>

- <span data-ttu-id="4be2b-106">Henter de elektroniske handelstransaksjonsdataene i HK.</span><span class="sxs-lookup"><span data-stu-id="4be2b-106">Pulling the online commerce transaction data in HQ.</span></span>
- <span data-ttu-id="4be2b-107">Synkroniserer ordrer for å opprette salgsordrer på hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="4be2b-107">Synchronizing orders to create sales orders in HQ.</span></span>

<span data-ttu-id="4be2b-108">Å hente elektroniske transaksjonsdata kan gjøres manuelt ved å kjøre P-jobben eller ved å opprette en gjentakende satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="4be2b-108">Pulling the online transaction data can be done either by manually running the P-job or by creating a recurrent batch job.</span></span>

### <a name="manually-running-the-p-job"></a><span data-ttu-id="4be2b-109">Kjøre P-jobben manuelt</span><span class="sxs-lookup"><span data-stu-id="4be2b-109">Manually running the P-job</span></span>

1. <span data-ttu-id="4be2b-110">Gå til Alle arbeidsområder > IT for Retail og Commerce.</span><span class="sxs-lookup"><span data-stu-id="4be2b-110">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="4be2b-111">Klikk på Distribusjonsplan.</span><span class="sxs-lookup"><span data-stu-id="4be2b-111">Click Distribution schedule.</span></span>
3. <span data-ttu-id="4be2b-112">Velg P-0001.</span><span class="sxs-lookup"><span data-stu-id="4be2b-112">Select P-0001.</span></span>
4. <span data-ttu-id="4be2b-113">Juster kanaldatabasegrupper hvis det er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="4be2b-113">Adjust channel database groups, if required.</span></span>
5. <span data-ttu-id="4be2b-114">Klikk Kjør nå.</span><span class="sxs-lookup"><span data-stu-id="4be2b-114">Click Run now.</span></span>
6. <span data-ttu-id="4be2b-115">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="4be2b-115">Click Yes.</span></span>

### <a name="scheduling-a-recurring-p-job"></a><span data-ttu-id="4be2b-116">Planlegge en regelmessig P-jobb</span><span class="sxs-lookup"><span data-stu-id="4be2b-116">Scheduling a recurring P-job</span></span>

1. <span data-ttu-id="4be2b-117">Gå til Alle arbeidsområder > IT for Retail og Commerce.</span><span class="sxs-lookup"><span data-stu-id="4be2b-117">Go to All workspaces > Retail and Commerce IT.</span></span>
2. <span data-ttu-id="4be2b-118">Klikk på Distribusjonsplan.</span><span class="sxs-lookup"><span data-stu-id="4be2b-118">Click Distribution schedule.</span></span>
3. <span data-ttu-id="4be2b-119">Velg P-0001.</span><span class="sxs-lookup"><span data-stu-id="4be2b-119">Select P-0001.</span></span>
4. <span data-ttu-id="4be2b-120">Klikk på Opprett satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="4be2b-120">Click Create batch job.</span></span>
5. <span data-ttu-id="4be2b-121">Klikk på Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="4be2b-121">Click Run in the background.</span></span>
5. <span data-ttu-id="4be2b-122">Aktiver satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="4be2b-122">Enable Batch processing.</span></span>
6. <span data-ttu-id="4be2b-123">Klikk på Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="4be2b-123">Click Recurrence..</span></span>
7. <span data-ttu-id="4be2b-124">Velg Ingen sluttdato.</span><span class="sxs-lookup"><span data-stu-id="4be2b-124">Select the No end date option.</span></span>
8. <span data-ttu-id="4be2b-125">I Antall-feltet angir du intervallet mellom kjøringer i minutter.</span><span class="sxs-lookup"><span data-stu-id="4be2b-125">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="4be2b-126">Vanligvis vil dette være 5-10.</span><span class="sxs-lookup"><span data-stu-id="4be2b-126">Typically this would be 5-10.</span></span>
9. <span data-ttu-id="4be2b-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4be2b-127">Click OK.</span></span>
10. <span data-ttu-id="4be2b-128">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4be2b-128">Click OK.</span></span>

<span data-ttu-id="4be2b-129">Ordrer kan synkroniseres enten ved å kjøre Synkroniser ordrer-jobben manuelt, eller ved å opprette en gjentakende satsvis jobb.</span><span class="sxs-lookup"><span data-stu-id="4be2b-129">Orders can be synchronized either by manually running the "Synchronize orders"-job or by creating a recurring batch job.</span></span>

### <a name="manually-running-order-synchronization"></a><span data-ttu-id="4be2b-130">Kjøre ordresynkronisering manuelt</span><span class="sxs-lookup"><span data-stu-id="4be2b-130">Manually running order synchronization</span></span> 

<span data-ttu-id="4be2b-131">Følg denne fremgangsmåten for å kjøre jobben Synkroniser ordrer manuelt én gang.</span><span class="sxs-lookup"><span data-stu-id="4be2b-131">Follow these steps to manually run "Synchronize orders" job once.</span></span>

1. <span data-ttu-id="4be2b-132">Gå til Alle arbeidsområder > Finans for butikk.</span><span class="sxs-lookup"><span data-stu-id="4be2b-132">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="4be2b-133">Klikk Synkroniser ordrer.</span><span class="sxs-lookup"><span data-stu-id="4be2b-133">Click Synchronize orders.</span></span>
3. <span data-ttu-id="4be2b-134">Velg Butikker etter område i Organisasjonshierarki-feltet.</span><span class="sxs-lookup"><span data-stu-id="4be2b-134">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="4be2b-135">Velg en bestemt nettbutikk eller velg en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.</span><span class="sxs-lookup"><span data-stu-id="4be2b-135">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="4be2b-136">Klikk pilen for å legge til valget.</span><span class="sxs-lookup"><span data-stu-id="4be2b-136">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="4be2b-137">Klikk fanen Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="4be2b-137">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="4be2b-138">Deaktiver satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="4be2b-138">Disable Batch processing</span></span>
6. <span data-ttu-id="4be2b-139">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="4be2b-139">Click Recurrence.</span></span>
7. <span data-ttu-id="4be2b-140">Velg Avslutt etter-alternativet.</span><span class="sxs-lookup"><span data-stu-id="4be2b-140">Select End After option</span></span>
8. <span data-ttu-id="4be2b-141">Angi 1 i feltet Avslutt etter.</span><span class="sxs-lookup"><span data-stu-id="4be2b-141">In the End After field, enter 1.</span></span>
9. <span data-ttu-id="4be2b-142">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4be2b-142">Click OK.</span></span>
10. <span data-ttu-id="4be2b-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4be2b-143">Click OK.</span></span>

### <a name="scheduling-recurring-order-synchronization"></a><span data-ttu-id="4be2b-144">Planlegge regelmessig ordresynkronisering</span><span class="sxs-lookup"><span data-stu-id="4be2b-144">Scheduling recurring order synchronization</span></span>

<span data-ttu-id="4be2b-145">Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å opprette salgsordrer og betalinger for nettbutikktransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="4be2b-145">This procedure walks through configuring and running a recurrent batch job to create sales orders and payments for online store transactions.</span></span> <span data-ttu-id="4be2b-146">Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.</span><span class="sxs-lookup"><span data-stu-id="4be2b-146">This procedure uses the USRT company in demo data.</span></span>

1. <span data-ttu-id="4be2b-147">Gå til Alle arbeidsområder > Finans for butikk.</span><span class="sxs-lookup"><span data-stu-id="4be2b-147">Go to All workspaces > Store financials.</span></span>
2. <span data-ttu-id="4be2b-148">Klikk Synkroniser ordrer.</span><span class="sxs-lookup"><span data-stu-id="4be2b-148">Click Synchronize orders.</span></span>
3. <span data-ttu-id="4be2b-149">Velg Butikker etter område i Organisasjonshierarki-feltet.</span><span class="sxs-lookup"><span data-stu-id="4be2b-149">In the Organization hierarchy field, select 'Stores by Region'.</span></span>
    * <span data-ttu-id="4be2b-150">Velg en bestemt nettbutikk eller velg en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.</span><span class="sxs-lookup"><span data-stu-id="4be2b-150">Select either a specific online store, or select a node if you want to create the batch job for a group of stores.</span></span>  
    * <span data-ttu-id="4be2b-151">Klikk pilen for å legge til valget.</span><span class="sxs-lookup"><span data-stu-id="4be2b-151">Click the arrow to add your selection.</span></span>  
4. <span data-ttu-id="4be2b-152">Klikk fanen Kjør i bakgrunnen.</span><span class="sxs-lookup"><span data-stu-id="4be2b-152">Click the Run in the background tab.</span></span>
5. <span data-ttu-id="4be2b-153">Aktiver satsvis behandling.</span><span class="sxs-lookup"><span data-stu-id="4be2b-153">Enable Batch processing</span></span>
6. <span data-ttu-id="4be2b-154">Klikk Regelmessighet.</span><span class="sxs-lookup"><span data-stu-id="4be2b-154">Click Recurrence.</span></span>
7. <span data-ttu-id="4be2b-155">Velg Ingen sluttdato.</span><span class="sxs-lookup"><span data-stu-id="4be2b-155">Select the No end date option.</span></span>
8. <span data-ttu-id="4be2b-156">I Antall-feltet angir du intervallet mellom kjøringer i minutter.</span><span class="sxs-lookup"><span data-stu-id="4be2b-156">In the Count field, enter interval between the runs in minutes.</span></span> <span data-ttu-id="4be2b-157">Vanligvis vil dette være 2-20.</span><span class="sxs-lookup"><span data-stu-id="4be2b-157">Typically this would be 2-20</span></span>
9. <span data-ttu-id="4be2b-158">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4be2b-158">Click OK.</span></span>
10. <span data-ttu-id="4be2b-159">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4be2b-159">Click OK.</span></span>

## <a name="data-entities-involved-in-the-process"></a><span data-ttu-id="4be2b-160">Dataenheter som er involvert i prosessen</span><span class="sxs-lookup"><span data-stu-id="4be2b-160">Data entities involved in the process</span></span>

- <span data-ttu-id="4be2b-161">RetailTransactionTable</span><span class="sxs-lookup"><span data-stu-id="4be2b-161">RetailTransactionTable</span></span>
- <span data-ttu-id="4be2b-162">RetailTransactionAddressTrans</span><span class="sxs-lookup"><span data-stu-id="4be2b-162">RetailTransactionAddressTrans</span></span>
- <span data-ttu-id="4be2b-163">RetailTransactionInfocodeTrans</span><span class="sxs-lookup"><span data-stu-id="4be2b-163">RetailTransactionInfocodeTrans</span></span>
- <span data-ttu-id="4be2b-164">RetailTransactionTaxTrans</span><span class="sxs-lookup"><span data-stu-id="4be2b-164">RetailTransactionTaxTrans</span></span>
- <span data-ttu-id="4be2b-165">RetailTransactionSalesTrans</span><span class="sxs-lookup"><span data-stu-id="4be2b-165">RetailTransactionSalesTrans</span></span>
- <span data-ttu-id="4be2b-166">RetailTransactionTaxMeasure</span><span class="sxs-lookup"><span data-stu-id="4be2b-166">RetailTransactionTaxMeasure</span></span>
- <span data-ttu-id="4be2b-167">RetailTransactionDiscountTrans</span><span class="sxs-lookup"><span data-stu-id="4be2b-167">RetailTransactionDiscountTrans</span></span>
- <span data-ttu-id="4be2b-168">RetailTransactionTaxTransGTE</span><span class="sxs-lookup"><span data-stu-id="4be2b-168">RetailTransactionTaxTransGTE</span></span>
- <span data-ttu-id="4be2b-169">RetailTransactionMarkupTrans</span><span class="sxs-lookup"><span data-stu-id="4be2b-169">RetailTransactionMarkupTrans</span></span>
- <span data-ttu-id="4be2b-170">RetailTransactionPaymentTrans</span><span class="sxs-lookup"><span data-stu-id="4be2b-170">RetailTransactionPaymentTrans</span></span>
- <span data-ttu-id="4be2b-171">RetailTransactionAttributeTrans</span><span class="sxs-lookup"><span data-stu-id="4be2b-171">RetailTransactionAttributeTrans</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]