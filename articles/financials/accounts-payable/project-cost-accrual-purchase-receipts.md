---
title: "Påløpte prosjektkostnader på kjøpsmottak"
description: "Dette emnet beskriver hvordan påløpte prosjektkostnader fra kjøpsmottak kan spores i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CostControlCommittedCost
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 266984
ms.assetid: 61e7d2a3-5aab-4113-bccc-213f932885d2
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: ea07d8e91c94d9fdad4c2d05533981e254420188
ms.openlocfilehash: f7355dc856d97a19d0f7558061b3e2d9902dab65
ms.contentlocale: nb-no
ms.lasthandoff: 02/07/2018

---

# <a name="project-cost-accrual-on-purchase-receipts"></a><span data-ttu-id="3a296-103">Påløpte prosjektkostnader på kjøpsmottak</span><span class="sxs-lookup"><span data-stu-id="3a296-103">Project cost accrual on purchase receipts</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="3a296-104">Dette emnet beskriver hvordan påløpte prosjektkostnader fra kjøpsmottak kan spores i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span><span class="sxs-lookup"><span data-stu-id="3a296-104">This topic describes how accrued project costs from purchase receipts can be tracked in Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span> 

<span data-ttu-id="3a296-105">Fakturaer for et prosjekt ankommer ofte etter at varene og tjenestene er levert, noe som kan ha betydelig innvirkning på prosjektets nøkkelytelsesindikatorer (KPI-er).</span><span class="sxs-lookup"><span data-stu-id="3a296-105">Invoices for a project often arrive later than the goods and services are delivered, which might have a significant impact on project key performance indicators (KPIs).</span></span> <span data-ttu-id="3a296-106">Det er viktig å kunne spore disse transaksjonene i både økonomisk rapporter og prosjektrapporter.</span><span class="sxs-lookup"><span data-stu-id="3a296-106">It important to be able to track these transactions in both financial and project reports.</span></span>

<span data-ttu-id="3a296-107">Eksemplet nedenfor illustrerer dette.</span><span class="sxs-lookup"><span data-stu-id="3a296-107">The following example scenario illustrates this.</span></span> 

<span data-ttu-id="3a296-108">Contoso Consulting har startet et nytt skydistribusjonsprosjekt.</span><span class="sxs-lookup"><span data-stu-id="3a296-108">Contoso Consulting has started a new cloud deployment project.</span></span> <span data-ttu-id="3a296-109">Det opprettes en bestilling for å kjøpe en datamaskin for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3a296-109">A purchase order is created to buy a computer for the project.</span></span> <span data-ttu-id="3a296-110">Datamaskinen vil koste USD 1 500, og installeringstjenester vil koste USD 150.</span><span class="sxs-lookup"><span data-stu-id="3a296-110">The computer will cost $1500 and installation services will cost $150.</span></span> <span data-ttu-id="3a296-111">Leverandøren har levert og installert datamaskinen, men fakturaen har ennå ikke ankommet Contoso Consulting.</span><span class="sxs-lookup"><span data-stu-id="3a296-111">The vendor has delivered and installed the computer, but the invoice has not yet reached Contoso Consulting.</span></span> <span data-ttu-id="3a296-112">Prosjektlederen vil gjerne se de påløpte prosjektkostnadene på USD 1 650 før fakturaen leveres.</span><span class="sxs-lookup"><span data-stu-id="3a296-112">The project manager would like to see project cost accrual of $1650 before the invoice gets delivered.</span></span> <span data-ttu-id="3a296-113">Denne kostnaden skal også gjenspeiles i selskapets regnskapsoppgjør ved månedsslutt.</span><span class="sxs-lookup"><span data-stu-id="3a296-113">This cost should also be reflected in the company's month end financial statements.</span></span> 

<span data-ttu-id="3a296-114">De påløpte kostnadene må være registrert på finansnivå og prosjektnivå for rapporteringsformål.</span><span class="sxs-lookup"><span data-stu-id="3a296-114">The accrued cost needs to be recorded on both the financial level and project level for reporting purposes.</span></span> <span data-ttu-id="3a296-115">Den økonomiske oppdatering av produktmottaket kan spores i Finance and Operations for vare- og innkjøpskategoriene.</span><span class="sxs-lookup"><span data-stu-id="3a296-115">In Finance and Operations, the financial update of the product receipt can be tracked for the item and procurement categories.</span></span> 

<span data-ttu-id="3a296-116">For varer går du til siden **Leverandørparametere** og velger alternativet **Poster mottakssedler til finans**.</span><span class="sxs-lookup"><span data-stu-id="3a296-116">For items, on the **Accounts payable parameters** page, select the **Post product receipts to ledger** option.</span></span>
<span data-ttu-id="3a296-117">[![Avsetninger1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span><span class="sxs-lookup"><span data-stu-id="3a296-117">[![accruals1](./media/accruals1-1024x409.png)](./media/accruals1.png)</span></span> 

<span data-ttu-id="3a296-118">For innkjøpskategorier går du til siden **Kategoripolicyregel**, velger **Innkjøpspolicyer** og velger deretter **Avsett innkjøpsutgift ved mottak** for hver innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="3a296-118">For procurement categories, on the **Category policy rule** page, select **Purchasing** policies, and then select **Accrue purchase expense on receipt** for each procurement category.</span></span>
<span data-ttu-id="3a296-119">[![Avsetninger2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span><span class="sxs-lookup"><span data-stu-id="3a296-119">[![accruals2](./media/accruals2-1024x569.png)](./media/accruals2.png)</span></span> 

<span data-ttu-id="3a296-120">Kontoene **Innkjøpsutgift, ikke-fakturert** og **Innkjøp, avsetning** i **Posteringsoppsett** vil bli brukt ved postering av bilag som er knyttet til mottaksseddelen.</span><span class="sxs-lookup"><span data-stu-id="3a296-120">The **Purchase expenditure un-invoiced** and **Purchase accrual** accounts in **Posting setup** will be used when vouchers that are related to the product receipt are posted.</span></span>
<span data-ttu-id="3a296-121">[![Avsetninger3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span><span class="sxs-lookup"><span data-stu-id="3a296-121">[![accruals3](./media/accruals3-1024x429.png)](./media/accruals3.png)</span></span> 

<span data-ttu-id="3a296-122">La oss bruke det samme scenariet og se hvordan postering av en mottaksseddel vil ha innvirkning på finans- og prosjektinformasjon.</span><span class="sxs-lookup"><span data-stu-id="3a296-122">Using this same scenario, let's see how posting a product receipt will impact General ledger and Project information.</span></span> 

<span data-ttu-id="3a296-123">**Trinn 1:** Opprett og bekreft en ny bestilling for prosjektet for å registrere innkjøp av en datamaskin til USD 1 500 og installasjonstjenester til USD 150.</span><span class="sxs-lookup"><span data-stu-id="3a296-123">**Step 1:** Create and confirm a new purchase order for the project to record the purchase of a computer for $1500 and installation services for $150.</span></span>
<span data-ttu-id="3a296-124">[![Avsetninger4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span><span class="sxs-lookup"><span data-stu-id="3a296-124">[![accruals4](./media/accruals4-1024x497.png)](./media/accruals4.png)</span></span> 

<span data-ttu-id="3a296-125">Når bestillingen er bekreftet, blir det opprettet transaksjoner for den igangsatte kostnaden for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="3a296-125">When the purchase order is confirmed, transactions for the committed cost are created for the project.</span></span> 
<span data-ttu-id="3a296-126">[![Avsetninger5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span><span class="sxs-lookup"><span data-stu-id="3a296-126">[![accruals5](./media/accruals5-1024x219.png)](./media/accruals5.png)</span></span> 

> [!NOTE]
> <span data-ttu-id="3a296-127">Transaksjonene for den igangsatte kostnaden vil feltet **Transaksjonsopprinnelse** satt til **Bestilling**.</span><span class="sxs-lookup"><span data-stu-id="3a296-127">The transactions for the committed cost will have the **Transaction Origin** field set to **Purchase Order**.</span></span> <span data-ttu-id="3a296-128">Oppretting og bekreftelse av en bestilling oppretter ikke transaksjoner for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="3a296-128">Creating and confirming a purchase order does not create transactions for a project.</span></span> 

<span data-ttu-id="3a296-129">**Trinn 2:** Varer og tjenester blir levert, og en mottaksseddel registreres.</span><span class="sxs-lookup"><span data-stu-id="3a296-129">**Step 2:** Goods and services get delivered and a product receipt is registered.</span></span> 

<span data-ttu-id="3a296-130">Postering av en mottaksseddel vil generere og postere et bilag i Finans.</span><span class="sxs-lookup"><span data-stu-id="3a296-130">Posting a product receipt will generate and post a voucher to the ledger.</span></span> <span data-ttu-id="3a296-131">Bilaget vil debitere kontoen Innkjøpsutgift, ikke-fakturert og kreditere kontoen Innkjøpsavsetning.</span><span class="sxs-lookup"><span data-stu-id="3a296-131">The voucher will debit the purchase expenditure, un-invoiced account, and credit purchase accrual account.</span></span> 
<span data-ttu-id="3a296-132">[![Avsetninger6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span><span class="sxs-lookup"><span data-stu-id="3a296-132">[![accruals6](./media/accruals6-1024x214.png)](./media/accruals6.png)</span></span>

> [!NOTE]
> <span data-ttu-id="3a296-133">Postering av en mottaksseddel bruker posteringsoppsettet for innkjøpskategorier og produkter, og ikke posteringsoppsettet for prosjektkategorier.</span><span class="sxs-lookup"><span data-stu-id="3a296-133">Posting a product receipt will use the posting setup for procurement categories and products, and not the posting setup for the project categories.</span></span> <span data-ttu-id="3a296-134">Oppsettet må justeres for å gjenspeile riktig økonomiske innvirkningen av Innkjøpsavsetning.</span><span class="sxs-lookup"><span data-stu-id="3a296-134">In order to correctly reflect financial impact of purchase accruals, this setup needs to be aligned.</span></span> 

<span data-ttu-id="3a296-135">Det er mulig å tilordne innkjøpskategorier til prosjektkategorier på siden **Innkjøpskategori**.</span><span class="sxs-lookup"><span data-stu-id="3a296-135">It is possible to map procurement categories to project categories on the **Procurement category** page.</span></span>
<span data-ttu-id="3a296-136">[![Avsetninger7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span><span class="sxs-lookup"><span data-stu-id="3a296-136">[![accruals7](./media/accruals7-1024x390.png)](./media/accruals7.png)</span></span>

<span data-ttu-id="3a296-137">**Trinn 3:** Opprett et leverandørfakturautkast.</span><span class="sxs-lookup"><span data-stu-id="3a296-137">**Step 3:** Create a draft vendor invoice.</span></span> 

<span data-ttu-id="3a296-138">I Finance and Operations vil ikke postering av en produktkvittering påvirke prosjektinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="3a296-138">In Finance and Operations, posting a product receipt does not impact project information.</span></span> <span data-ttu-id="3a296-139">For å omgå dette kan du generere et leverandørfakturautkast direkte etter postering av mottaksseddelen.</span><span class="sxs-lookup"><span data-stu-id="3a296-139">As a workaround, you could generate a draft vendor invoice right after posting the purchase receipt.</span></span> <span data-ttu-id="3a296-140">Gå til siden **Bestilling** &gt; kategorien **Faktura** &gt; **Generer** &gt; **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="3a296-140">Go to the **Purchase Order** page &gt; **Invoice tab** &gt; **Generate** &gt; **Invoice**.</span></span> <span data-ttu-id="3a296-141">Dette oppretter et ventende fakturadokumentet som oppdaterer prosjektinformasjonen.</span><span class="sxs-lookup"><span data-stu-id="3a296-141">This creates a pending invoice document that updates project information.</span></span> 

<span data-ttu-id="3a296-142">Oppretting av et leverandørfakturautkast genererer ventende prosjekttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="3a296-142">Creating a draft vendor invoice will generate pending project transactions.</span></span> 
<span data-ttu-id="3a296-143">[![Avsetninger8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span><span class="sxs-lookup"><span data-stu-id="3a296-143">[![accruals8](./media/accruals8-1024x225.png)](./media/accruals8.png)</span></span> 

<span data-ttu-id="3a296-144">På siden **Igangsatt kost** vil poster som ble opprettet i trinn 1, bli lukket, og nye poster vil bli opprettet for å gjenspeile igansatt kost som kommer fra den ventende leverandørfakturaen.</span><span class="sxs-lookup"><span data-stu-id="3a296-144">In the **Committed cost** page, records created in step 1 will be closed and new records will be created to reflect cost commitment coming from the pending vendor invoice.</span></span> <span data-ttu-id="3a296-145">Feltet **Transaksjonsopprinnelse** for den igangsatte kostnaden vil bli satt til **Leverandørfaktura**.</span><span class="sxs-lookup"><span data-stu-id="3a296-145">The **Transaction origin** field for the committed cost will be set to **Vendor invoice**.</span></span>
<span data-ttu-id="3a296-146">[![Avsetninger9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span><span class="sxs-lookup"><span data-stu-id="3a296-146">[![accruals9](./media/accruals9-1024x200.png)](./media/accruals9.png)</span></span>

<span data-ttu-id="3a296-147">Leverandørfakturaen forblir i en ventetilstand til den faktiske leverandørfakturaen ankommer.</span><span class="sxs-lookup"><span data-stu-id="3a296-147">The vendor invoice will remain in a pending state until the actual vendor invoice arrives.</span></span>




