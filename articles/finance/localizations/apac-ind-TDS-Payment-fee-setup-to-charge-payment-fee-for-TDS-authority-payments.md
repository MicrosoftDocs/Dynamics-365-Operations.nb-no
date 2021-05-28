---
title: Konfigurere betalingsgebyrer for TDS-myndighetsbetalinger
description: Dette emnet forklarer hvordan du konfigurerer betalingsgebyrer som belastes for TDS-myndighetsbetalinger (Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: b52331bb1c7a1bc2c764008112f3df9cc0385995
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023493"
---
# <a name="set-up-payment-fees-for-tds-authority-payments"></a><span data-ttu-id="beb21-103">Konfigurere betalingsgebyrer for TDS-myndighetsbetalinger</span><span class="sxs-lookup"><span data-stu-id="beb21-103">Set up payment fees for TDS authority payments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="beb21-104">Dette emnet forklarer hvordan du konfigurerer betalingsgebyrer som belastes for TDS-myndighetsbetalinger (Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="beb21-104">This topic explains how to set up payment fees that are charged for Tax Deducted at Source (TDS) authority payments.</span></span>

1. <span data-ttu-id="beb21-105">Gå til **Leverandører \> Betalingsoppsett \> Betalingsgebyr**.</span><span class="sxs-lookup"><span data-stu-id="beb21-105">Go to **Accounts payable \> Payment setup \> Payment fee**.</span></span>

    <span data-ttu-id="beb21-106">[![Siden Betalingsgebyr](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span><span class="sxs-lookup"><span data-stu-id="beb21-106">[![Payment fee page](./media/apac-ind-TDS-28.png)](./media/apac-ind-TDS-28.png)</span></span>

2. <span data-ttu-id="beb21-107">Velg **Nytt** for å opprette et betalingsgebyr, og angi de nødvendige detaljene.</span><span class="sxs-lookup"><span data-stu-id="beb21-107">Select **New** to create a payment fee, and enter the required details.</span></span>
3. <span data-ttu-id="beb21-108">Velg typen betalingsgebyr i **Gebyrtype**-feltet:</span><span class="sxs-lookup"><span data-stu-id="beb21-108">In the **Fee type** field, select the type of payment fee:</span></span>

    - <span data-ttu-id="beb21-109">**None**</span><span class="sxs-lookup"><span data-stu-id="beb21-109">**None**</span></span>
    - <span data-ttu-id="beb21-110">**Rente** – Rente belastes for sene betalinger til TDS-myndighetsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="beb21-110">**Interest** – Interest is charged on late payments that are made to the TDS authority vendor.</span></span>
    - <span data-ttu-id="beb21-111">**Andre** – Andre tillegg belastes for sene betalinger til TDS-myndighetsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="beb21-111">**Others** – Other charges are charged on late payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="beb21-112">Hvis du velger **Rente** eller **Andre**, settes **Tillegg**-feltet automatisk til **Finans**.</span><span class="sxs-lookup"><span data-stu-id="beb21-112">If you select **Interest** or **Others**, the **Charge** field is automatically set to **Ledger**.</span></span>

4. <span data-ttu-id="beb21-113">Hvis du valgte **Rente** eller **Andre** i **Felttype**-feltet, velger du finanskontoen du vil postere renten eller andre tillegg på, i **Hovedkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="beb21-113">If you selected **Interest** or **Others** in the **Field type** field, in the **Main account** field, select the ledger account to post the interest or other charges to.</span></span>
5. <span data-ttu-id="beb21-114">Angi de andre nødvendige opplysningene.</span><span class="sxs-lookup"><span data-stu-id="beb21-114">Enter the other required details.</span></span>
6. <span data-ttu-id="beb21-115">Velg **Oppsett av betalingsgebyr** i handlingsruten for å åpne siden **Oppsett av betalingsgebyr**, der du kan konfigurere betalingsgebyrer for ulike kombinasjoner av banker, betalingsmåter, betalingsspesifikasjoner, valutaer og datointervaller.</span><span class="sxs-lookup"><span data-stu-id="beb21-115">On the Action Pane, select **Payment fee setup** to open the **Payment fee setup** page, where you can set up payment fees for various combinations of banks, methods of payment, payment specifications, currencies, and date intervals.</span></span>

    <span data-ttu-id="beb21-116">[![Siden Oppsett av betalingsgebyr](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span><span class="sxs-lookup"><span data-stu-id="beb21-116">[![Payment fee setup page](./media/apac-ind-TDS-21.png)](./media/apac-ind-TDS-21.png)</span></span>

7. <span data-ttu-id="beb21-117">Angi hvilke banker du vil definere betalingsgebyret for, i **Grupperinger**-feltet i **Oversikt**-fanen:</span><span class="sxs-lookup"><span data-stu-id="beb21-117">On the **Overview** tab, in the **Groupings** field, specify which banks you're setting up the payment fee for:</span></span>

    - <span data-ttu-id="beb21-118">**Tabell** – Gebyret er gyldig for en bestemt bankkonto.</span><span class="sxs-lookup"><span data-stu-id="beb21-118">**Table** – The fee is valid for a specific bank account.</span></span>
    - <span data-ttu-id="beb21-119">**Gruppe** – Gebyret er gyldig for en bestemt bankgruppe.</span><span class="sxs-lookup"><span data-stu-id="beb21-119">**Group** – The fee is valid for a specific bank group.</span></span>
    - <span data-ttu-id="beb21-120">**Alle** – Gebyret er gyldig for alle bankkontoene.</span><span class="sxs-lookup"><span data-stu-id="beb21-120">**All** – The fee is valid for all the bank accounts.</span></span>

8. <span data-ttu-id="beb21-121">Hvis du valgte **Tabell** eller **Gruppe** i **Grupperinger**-feltet, velger du den bestemte bankkontoen eller bankgruppen du definerer betalingsgebyret for, i **Bankrelasjon**-feltet.</span><span class="sxs-lookup"><span data-stu-id="beb21-121">If you selected **Table** or **Group** in the **Groupings** field, in the **Bank relation** field, select the specific bank account or bank group that you're setting up the payment fee for.</span></span>
9. <span data-ttu-id="beb21-122">Velg betalingsmåten for betaling av gebyrer i **Betalingsmåte**-feltet.</span><span class="sxs-lookup"><span data-stu-id="beb21-122">In the **Method of payment** field, select the method of payment for the payment of fees.</span></span>
10. <span data-ttu-id="beb21-123">Velg eller angi betalingsspesifikasjonskoden som er generert på siden **Betalingsspesifikasjon**, i feltet **Betalingsspesifikasjon**.</span><span class="sxs-lookup"><span data-stu-id="beb21-123">In the **Payment specification** field, select or enter the payment specification code that was generated on the **Payment specification** page.</span></span>
    - <span data-ttu-id="beb21-124">Betalingsspesifikasjonen brukes med betalingsmåter for elektronisk pengeoverføring.</span><span class="sxs-lookup"><span data-stu-id="beb21-124">The Payment specification is used with electronic fund transfer methods of payment.</span></span>
12. <span data-ttu-id="beb21-125">Velg valutaen som aktiverer gebyret, i **Betalingsvaluta**-feltet.</span><span class="sxs-lookup"><span data-stu-id="beb21-125">In the **Payment currency** field, select the currency that activates the fee.</span></span> <span data-ttu-id="beb21-126">Bare transaksjoner som bruker den valgte valutaen, kan aktivere gebyret.</span><span class="sxs-lookup"><span data-stu-id="beb21-126">Only transactions that use the selected currency can activate the fee.</span></span> <span data-ttu-id="beb21-127">Hvis du lar dette feltet stå tomt, aktiverer alle valutaer gebyret.</span><span class="sxs-lookup"><span data-stu-id="beb21-127">If you leave this field blank, all currencies activate the fee.</span></span>
13. <span data-ttu-id="beb21-128">Velg beregningsmetoden i feltet **Prosent/beløp**.</span><span class="sxs-lookup"><span data-stu-id="beb21-128">In the **Percentage/Amount** field, select the calculation method.</span></span> <span data-ttu-id="beb21-129">Alternativene er **Beløp**, **Prosent** og **Intervall**.</span><span class="sxs-lookup"><span data-stu-id="beb21-129">The options are **Amount**, **Percent**, and **Interval**.</span></span>
14. <span data-ttu-id="beb21-130">I **Gebyrbeløp**-feltet angir du gebyrbeløpet som enten en prosent av betalingen eller beløpet for én betaling.</span><span class="sxs-lookup"><span data-stu-id="beb21-130">In the **Fee amount** field, specify the fee amount as either a percentage of the payment or the amount for one payment.</span></span>
15. <span data-ttu-id="beb21-131">Angi valutakoden for gebyret i **Gebyrvaluta**-feltet.</span><span class="sxs-lookup"><span data-stu-id="beb21-131">In the **Fee currency** field, specify the currency code for the fee.</span></span>
16. <span data-ttu-id="beb21-132">Velg **Generelt**-fanen for å vise eller endre detaljene for den valgte bankkontoen.</span><span class="sxs-lookup"><span data-stu-id="beb21-132">Select the **General** tab to view or modify the details for the selected bank account.</span></span>

    <span data-ttu-id="beb21-133">[![Fanen Generelt](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span><span class="sxs-lookup"><span data-stu-id="beb21-133">[![General tab](./media/apac-ind-TDS-22.png)](./media/apac-ind-TDS-22.png)</span></span>

16. <span data-ttu-id="beb21-134">I **Minimum**-feltet angir du minimumsbeløpet for transaksjonen som skal aktivere gebyret.</span><span class="sxs-lookup"><span data-stu-id="beb21-134">In the **Minimum** field, enter the minimum transaction amount that activates the fee.</span></span>
17. <span data-ttu-id="beb21-135">I **Maksimum**-feltet angir du maksimumsbeløpet for transaksjonen som skal aktivere gebyret.</span><span class="sxs-lookup"><span data-stu-id="beb21-135">In the **Maximum** field, enter the maximum transaction amount that activates the fee.</span></span>
18. <span data-ttu-id="beb21-136">I feltene **Fra-dato** og **Til-dato** definerer du et datointervall for beregning av gebyrer.</span><span class="sxs-lookup"><span data-stu-id="beb21-136">In the **From date** and **To date** fields, define a date range for calculating fees.</span></span>
19. <span data-ttu-id="beb21-137">I **Minimumsgebyr**-feltet angir du gebyrbeløpet som enten en prosent av betalingen eller beløpet for én betaling.</span><span class="sxs-lookup"><span data-stu-id="beb21-137">In the **Minimum fee** field, specify the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
20. <span data-ttu-id="beb21-138">I feltet **Mva-gruppe** velger du mva-gruppen som skal brukes til å beregne mva for avgiftsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="beb21-138">In the **Sales tax group** field, select the sales tax group to use to calculate the sales tax for the fee amount.</span></span>
21. <span data-ttu-id="beb21-139">I feltet **Vare, mva-gruppe** velger du mva-gruppen for vare som skal brukes til å beregne mva for vare for avgiftsbeløpet.</span><span class="sxs-lookup"><span data-stu-id="beb21-139">In the **Item sales tax group** field, select the item sales tax group to use to calculate the item sales tax for the fee amount.</span></span>
22. <span data-ttu-id="beb21-140">Velg **Intervall**-fanen.</span><span class="sxs-lookup"><span data-stu-id="beb21-140">Select the **Interval** tab.</span></span> 

    <span data-ttu-id="beb21-141">[![Intervall-fanen](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span><span class="sxs-lookup"><span data-stu-id="beb21-141">[![Interval tab](./media/apac-ind-TDS-23.png)](./media/apac-ind-TDS-23.png)</span></span>

23. <span data-ttu-id="beb21-142">Angi antall dager mellom posteringsdatoen (diskonteringsdato) for betalingen og forfallsdatoen for egenvekselen i **Dager**-feltet.</span><span class="sxs-lookup"><span data-stu-id="beb21-142">In the **Days** field, enter the number of days between the posting date (discounting date) of the payment and the due date of the promissory note.</span></span>
24. <span data-ttu-id="beb21-143">I feltet **Prosent/beløp** velger du om spesifikasjonen er en prosent eller et angitt beløp.</span><span class="sxs-lookup"><span data-stu-id="beb21-143">In the **Percentage/Amount** field, select whether the specification is a percentage or a set amount.</span></span>
25. <span data-ttu-id="beb21-144">I **Gebyrbeløp**-feltet angir du gebyrbeløpet som enten en prosent av betalingen eller beløpet for én betaling.</span><span class="sxs-lookup"><span data-stu-id="beb21-144">In the **Fee amount** field, enter the amount of the fee as either a percentage of the payment or the amount for one payment.</span></span>
26. <span data-ttu-id="beb21-145">Lukk siden **Oppsett av betalingsgebyr**.</span><span class="sxs-lookup"><span data-stu-id="beb21-145">Close the **Payment fee setup** page.</span></span>
27. <span data-ttu-id="beb21-146">Lukk **Betalingsgebyr**-siden.</span><span class="sxs-lookup"><span data-stu-id="beb21-146">Close the **Payment fee** page.</span></span>
