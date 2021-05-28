---
title: Utligne TDS-betalinger mot TDS-myndighetsleverandører og generere TDS-challan
description: Dette emnet forklarer hvordan du utligner TDS-betalinger (Tax Deducted at Source) mot TDS-myndighetsleverandører.
author: kailiang
ms.date: 03/12/2021
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
ms.openlocfilehash: 5b77985a75d2930267cf94d6f218d53b47e6e705
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023485"
---
# <a name="settle-tds-payments-to-tds-authority-vendors-and-generate-tds-challan"></a><span data-ttu-id="0ef3a-103">Utligne TDS-betalinger mot TDS-myndighetsleverandører og generere TDS-challan</span><span class="sxs-lookup"><span data-stu-id="0ef3a-103">Settle TDS payments to TDS authority vendors and generate TDS challan</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0ef3a-104">Dette emnet forklarer hvordan du utligner TDS-betalinger (Tax Deducted at Source) mot TDS-myndighetsleverandører.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-104">This topic explains how to settle Tax Deducted at Source (TDS) payments to TDS authority vendors.</span></span>

1. <span data-ttu-id="0ef3a-105">Gå til **Leverandører \> Betalinger \> Leverandørbetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-105">Go to **Accounts payable \> Payments \> Vendor payment journal**.</span></span>

    <span data-ttu-id="0ef3a-106">[![Siden Leverandørbetalingsjournal](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span><span class="sxs-lookup"><span data-stu-id="0ef3a-106">[![Vendor payment journal page](./media/apac-ind-TDS-51.png)](./media/apac-ind-TDS-51.png)</span></span>

2. <span data-ttu-id="0ef3a-107">Velg **Ny** for å opprette en journallinje på siden **Leverandørbetalingsjournal**.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-107">On the **Vendor payment journal** page, select **New** to create a journal line.</span></span>
3. <span data-ttu-id="0ef3a-108">I **Konto**-feltet velger du TDS-myndighetsleverandøren som TDS-betalinger skal utlignes mot.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-108">In the **Account** field, select the TDS authority vendor to settle TDS payments to.</span></span>
4. <span data-ttu-id="0ef3a-109">Velg **Utligningstransaksjoner** for å åpne siden **Utligningstransaksjoner**, der du kan vise de utlignede TDS-transaksjonene for TDS-myndighetsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-109">Select **Settlement transactions** to open the **Settlement transactions** page, where you can view the settled TDS transactions for the TDS authority vendor.</span></span>

    <span data-ttu-id="0ef3a-110">De utlignede TDS-transaksjonene for en utligningsperiode vises på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="0ef3a-110">The settled TDS transactions for a settlement period are shown in the following way:</span></span>

    - <span data-ttu-id="0ef3a-111">TDS-transaksjoner der kategorien for skattebetalertype er **Selskap**, vises som én transaksjonslinje.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-111">TDS transactions where the nature of assessee category is **Company** are shown as one transaction line.</span></span>
    - <span data-ttu-id="0ef3a-112">TDS-transaksjoner der kategorien for skattebetalertype er **HUF**, **Firma**, **Enkeltperson**, **AOP**, **BOI**, **Lokale myndigheter** eller **Andre** vises som én transaksjonslinje.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-112">TDS transactions where the nature of assessee category is **HUF**, **Firm**, **Individual**, **AOP**, **BOI**, **Local authority**, or **Others** are shown as one transaction line.</span></span>
    - <span data-ttu-id="0ef3a-113">**Beløp**-feltet inneholder det totale TDS-beløpet som skal betales til TDS-myndighetsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-113">The **Amount** field shows the total TDS amount that is due to be paid to the TDS authority vendor.</span></span>

5. <span data-ttu-id="0ef3a-114">Velg **Kildeskattransaksjoner** for å vise de ulike TDS-transaksjonene som er tatt med for utligningsposten.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-114">Select **Withholding tax transactions** to view the different TDS transactions that are included for the settlement record.</span></span> <span data-ttu-id="0ef3a-115">Du kan vise delingen av hver TDS-transaksjon som er tatt med i utligningsprosessen for utligningsperioden på denne siden.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-115">You can view the split of each TDS transaction that has been included in the settlement process for the settlement period on this page.</span></span>
6. <span data-ttu-id="0ef3a-116">I **Oversikt**-fanen merker du av for **Merk** for TDS-transaksjonene som skal utlignes mot TDS-myndighetsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-116">On the **Overview** tab, select the **Mark** check box for the TDS transactions to settle to the TDS authority vendor.</span></span>

    <span data-ttu-id="0ef3a-117">**Oversikt**-fanen viser følgende informasjon for hver åpne TDS-transaksjon:</span><span class="sxs-lookup"><span data-stu-id="0ef3a-117">The **Overview** tab shows the following information for each open TDS transaction:</span></span>

    - <span data-ttu-id="0ef3a-118">**Dato** – TDS-transaksjonsdatoen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-118">**Date** – The TDS transaction date.</span></span>
    - <span data-ttu-id="0ef3a-119">**Bilag** – Bilagsnummeret.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-119">**Voucher** – The voucher number.</span></span>
    - <span data-ttu-id="0ef3a-120">**Kilde** – Modulen som TDS-transaksjonen posteres i.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-120">**Source** – The module that the TDS transaction is posted in.</span></span>
    - <span data-ttu-id="0ef3a-121">**Leverandør/kunde** – Leverandør- eller kundekontonummeret som TDS trekkes fra.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-121">**Vendor/Customer** – The vendor or customer account number that the TDS is deducted from.</span></span>
    - <span data-ttu-id="0ef3a-122">**Navn på deductee/part** – Navnet på leverandøren eller kunden som TDS trekkes fra.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-122">**Name of deductee/party** – The name of the vendor or customer that the TDS is deducted from.</span></span>
    - <span data-ttu-id="0ef3a-123">**Skattebetalertype** – Kategorien for skattebetalertype som deductee hører til i.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-123">**Nature of assessee** – The nature of assessee category that the deductee belongs to.</span></span>
    - <span data-ttu-id="0ef3a-124">**Beløp** – Fakturabeløpet som TDS ble beregnet for.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-124">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="0ef3a-125">**Avgiftsbeløp** – TDS-beløpet som ble beregnet for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-125">**Tax amount** – The TDS amount that was calculated for the transaction.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0ef3a-126">Fjern merket for **Merk** for alle TDS-transaksjoner som ikke skal utlignes mot TDS-myndighetsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-126">Clear the **Mark** check box for any TDS transactions that should not be settled to the TDS authority vendor.</span></span>

    <span data-ttu-id="0ef3a-127">I kategorien **Generelt** viser **PAN**-feltet det permanente kontonummeret (PAN) til deductee.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-127">On the **General** tab, the **PAN** field shows the permanent account number (PAN) of the deductee.</span></span> <span data-ttu-id="0ef3a-128">**Dato**-feltet viser datoen for TDS-beregningen, og **Verdi**-feltet viser den totale prosentsatsen som ble brukt ved TDS-beregningen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-128">The **Date** field shows the date of the TDS calculation, and the **Value** field shows the total percentage that was used for the TDS calculation.</span></span>

7. <span data-ttu-id="0ef3a-129">Velg **Bilag** for å vise bilagsoppføringene for TDS-transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-129">Select **Voucher** to view the voucher entries for the TDS transaction.</span></span>
8. <span data-ttu-id="0ef3a-130">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-130">Close the page.</span></span>
10. <span data-ttu-id="0ef3a-131">Velg **Komponenter for kildeskatt** for å åpne siden **Komponenter for kildeskatt**, der du kan vise TDS-beløpet som ble beregnet per TDS-avgiftskomponent for en bestemt TDS-avgiftskode.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-131">Select **Withholding tax components** to open the **Withholding tax components** page, where you can view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span>

    <span data-ttu-id="0ef3a-132">Feltet **Avgiftskomponent** i **Oversikt**-fanen viser TDS-avgiftskomponenten som ble brukt for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-132">On the **Overview** tab, the **Tax component** field shows the TDS tax component that was used for the transaction.</span></span> <span data-ttu-id="0ef3a-133">**Beløp**-feltet viser TDS-beløpet som ble beregnet for TDS-avgiftskomponenten, i basisvalutaen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-133">The **Amount** field shows the TDS amount that was calculated for the TDS tax component, in the base currency.</span></span> <span data-ttu-id="0ef3a-134">Feltet **Akkumulert beløp** viser det totale TDS-beløpet som ble beregnet for TDS-avgiftskomponenten for alle utlignede transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-134">The **Accumulated amount** field shows the total TDS amount that was calculated for the TDS tax component for all settled transactions.</span></span>

    <span data-ttu-id="0ef3a-135">**Standardvaluta**-delen i **Beløp**-fanen viser TDS-beløpet som ble beregnet for TDS-avgiftskomponenten, i standardvalutaen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-135">On the **Amount** tab, the **Default currency** section shows the TDS amount that was calculated for the TDS tax component, in the default currency.</span></span> <span data-ttu-id="0ef3a-136">Delen **Alternativ valuta** viser beløpet i den alternative valutaen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-136">The **Secondary currency** section shows the amount in the secondary currency.</span></span>

11. <span data-ttu-id="0ef3a-137">Lukk siden **Komponenter for kildeskatt**.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-137">Close the **Withholding tax components** page.</span></span>
12. <span data-ttu-id="0ef3a-138">Merk deg at det totale beløpet som skal utlignes mot TDS-myndighetsleverandøren for utligningsperioden, oppdateres i **Beløp**-feltet på siden **Åpen transaksjonsredigering**.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-138">On the **Open transaction editing** page, in the **Amount** field, notice that the total amount to settle to the TDS authority vendor for the settlement period is updated.</span></span>
13. <span data-ttu-id="0ef3a-139">Hvis du vil utligne TDS-transaksjonene for ulike TDS-utligningsperioder mot TDS-myndighetsleverandøren, merker du av for **Merk** for transaksjonene.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-139">To settle the TDS transactions of different TDS settlement periods to the TDS authority vendor, select the **Mark** check box for the transactions.</span></span>
14. <span data-ttu-id="0ef3a-140">Lukk siden **Åpen transaksjonsredigering**.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-140">Close the **Open transaction editing** page.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0ef3a-141">Hvis det bare er valgt noen få transaksjoner for utligning på siden **Kildeskattransaksjoner**, oppdateres det totale TDS-beløpet for de valgte transaksjonene i **Rettelse**-feltet på siden **Åpen transaksjonsredigering**.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-141">If only a few transactions are selected for settlement on the **Withholding tax transactions** page, the total TDS amount of the selected transactions is updated in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="0ef3a-142">Rettelsesbeløpet oppdateres på journallinjen på **Journalbilag**-siden, og siden **Åpen transaksjonsredigering** lukkes.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-142">The correction amount is updated on the journal line on the **Journal voucher** page, and the **Open transaction editing** page is closed.</span></span>

    <span data-ttu-id="0ef3a-143">**Debet**-feltet på **Journalbilag**-siden viser totalbeløpet som skal betales til TDS-myndighetsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-143">On the **Journal voucher** page, the **Debit** field shows the total amount to pay to the TDS authority vendor.</span></span>

15. <span data-ttu-id="0ef3a-144">Angi motkontodetaljene.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-144">Enter the offset account details.</span></span>

    > [!NOTE]
    > <span data-ttu-id="0ef3a-145">Hvis TDS-transaksjoner har ulike TAN-numre (Tax Account Number), opprettes det journallinjer per TAN på **Journalbilag**-siden.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-145">If TDS transactions have different Tax Account Numbers (TANs), journal lines are created per TAN on the **Journal voucher** page.</span></span>

16. <span data-ttu-id="0ef3a-146">Velg en gebyr-ID som har gebyrtypen **Rente** eller **Andre** i feltet **Gebyr-ID** på **Betalingsgebyr**-siden, for å belaste betalingsgebyret for forsinkede betalinger til TDS-leverandøren.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-146">On the **Payment fee** tab, in the **Fee ID** field, select a fee ID that has a fee type of **Interest** or **Others** to charge the payment fee for delayed payments that are made to the TDS authority vendor.</span></span>

    <span data-ttu-id="0ef3a-147">**Navn**-feltet i delen **Selskapsopplysninger** i fanen **Avgiftsinformasjon** viser selskapsnavnet.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-147">On the **Tax information** tab, in the **Company information** section, the **Name** field shows the company name.</span></span> <span data-ttu-id="0ef3a-148">Feltet **TAN-nummer (Tax Account Number)** i **Kildeskatt**-delen viser TAN-nummeret som er knyttet til transaksjonslinjen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-148">In the **Withholding tax** section, the **Tax Account Number (TAN)** field shows the TAN that is attached to the transaction line.</span></span>

17. <span data-ttu-id="0ef3a-149">Valider og poster journalen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-149">Validate and post the journal.</span></span>
18. <span data-ttu-id="0ef3a-150">Velg **Kildeskatt \> Challan-informasjon** for å angi challan-detaljene for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-150">Select **Withholding tax \> Challan information** to enter the challan details for the transaction.</span></span>

    <span data-ttu-id="0ef3a-151">**Bilag**-feltet viser bilagsnummeret for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-151">The **Voucher** field shows the voucher number of the transaction.</span></span>
    
19. <span data-ttu-id="0ef3a-152">Merk av for **TDS innbetalt ved bokoppføring** hvis TDS-beløpet betales inn ved hjelp av bokoppføring.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-152">Select the **TDS deposited by book entry** check box if the TDS amount is deposited by using book entry.</span></span>
20. <span data-ttu-id="0ef3a-153">Angi challan-nummeret som brukes til å betale TDS-myndighetsleverandøren, i feltet **Challan-nummer**.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-153">In the **Challan number** field, enter the challan number that is used to make the payment to the TDS authority vendor.</span></span>
21. <span data-ttu-id="0ef3a-154">Angi challan-datoen i **Dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-154">In the **Date** field, enter the challan date.</span></span>
22. <span data-ttu-id="0ef3a-155">I **Banknavn**-feltet velger du navnet på banken som TDS-beløpet som skal betales til TDS-myndighetsleverandøren, skal betales inn i.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-155">In the **Bank name** field, select the name of the bank that the TDS amount that is payable to the TDS authority vendor should be deposited to.</span></span> <span data-ttu-id="0ef3a-156">Dette feltet viser alle bankkontoene som ble konfigurert for TDS-myndighetsleverandøren i **Leverandør \> Alle leverandører \> Konfigurer \> Bankkontoer**.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-156">This field lists all the bank accounts that were set up for the TDS authority vendor at **Accounts payable \> All vendors \> Set up \> Bank accounts**.</span></span>
23. <span data-ttu-id="0ef3a-157">Angi BSR-koden (Basic Statistical Return) for banken i feltet **BSR-kode**.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-157">In the **BSR code** field, enter the Basic Statistical Return (BSR) code of the bank.</span></span>
24. <span data-ttu-id="0ef3a-158">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-158">Close the page.</span></span>

### <a name="example"></a><span data-ttu-id="0ef3a-159">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0ef3a-159">Example</span></span>

<span data-ttu-id="0ef3a-160">Perioden 01.04.2009 utlignes mot TDS-komponentgruppen **Leie** ved hjelp av den periodiske TDS-utligningsprosessen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-160">The period 04/01/2009 is settled for the **Rent** TDS component group by using the periodic TDS settlement process.</span></span> <span data-ttu-id="0ef3a-161">Det totale TDS-beløpet på 141 625,00 posteres på kontoen til TDS-myndighetsleverandøren for TDS-utligningsperioden.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-161">The total TDS amount of 141,625.00 is posted to the TDS vendor authority account for the TDS settlement period.</span></span> <span data-ttu-id="0ef3a-162">Du kan vise dette beløpet i **Beløp**-feltet på siden **Åpen transaksjonsredigering** for TDS-myndighetsleverandøren.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-162">You can view this amount in the **Amount** field on the **Open transaction editing** page for the TDS authority vendor.</span></span>

<span data-ttu-id="0ef3a-163">Hvis du velger **Kildeskattransaksjoner** for å vise de ulike TDS-transaksjonene som ble utlignet for perioden, vises informasjonen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-163">If you select **Withholding tax transactions** to view the different TDS transactions that were settled for the period, the following information is shown.</span></span>

| <span data-ttu-id="0ef3a-164">TDS-beløp</span><span class="sxs-lookup"><span data-stu-id="0ef3a-164">TDS amount</span></span> |
|------------|
| <span data-ttu-id="0ef3a-165">16 995,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-165">16,995.00</span></span>  |
| <span data-ttu-id="0ef3a-166">22 660,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-166">22,660.00</span></span>  |
| <span data-ttu-id="0ef3a-167">28 325,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-167">28,325.00</span></span>  |
| <span data-ttu-id="0ef3a-168">16 995,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-168">16,995.00</span></span>  |
| <span data-ttu-id="0ef3a-169">28 325,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-169">28,325.00</span></span>  |
| <span data-ttu-id="0ef3a-170">16 995,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-170">16,995.00</span></span>  |
| <span data-ttu-id="0ef3a-171">11 330,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-171">11,330.00</span></span>  |

<span data-ttu-id="0ef3a-172">Du kan velge **Komponenter for kildeskatt** for et bestemt TDS-beløp for å vise TDS-beløpet som ble beregnet per TDS-avgiftskomponent for en bestemt TDS-avgiftskode.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-172">For a specific TDS amount, you can select **Withholding tax components** to view the TDS that was calculated per TDS tax component for a specific TDS tax code.</span></span> <span data-ttu-id="0ef3a-173">I dette eksemplet velger du **Komponenter for kildeskatt** for TDS-beløpet 16 995,00.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-173">For this example, you select **Withholding tax components** for the TDS amount 16,995.00.</span></span> <span data-ttu-id="0ef3a-174">Avgiftsbeløpet som ble beregnet per komponent for transaksjonen, vises.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-174">The tax amount that was calculated per component for the transaction is shown.</span></span>

| <span data-ttu-id="0ef3a-175">Avgiftskomponent</span><span class="sxs-lookup"><span data-stu-id="0ef3a-175">Tax component</span></span> | <span data-ttu-id="0ef3a-176">Beløp</span><span class="sxs-lookup"><span data-stu-id="0ef3a-176">Amount</span></span>    | <span data-ttu-id="0ef3a-177">Akkumulert beløp</span><span class="sxs-lookup"><span data-stu-id="0ef3a-177">Accumulated amount</span></span> |
|---------------|-----------|--------------------|
| <span data-ttu-id="0ef3a-178">TDS</span><span class="sxs-lookup"><span data-stu-id="0ef3a-178">TDS</span></span>           | <span data-ttu-id="0ef3a-179">15 000,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-179">1,5000.00</span></span> | <span data-ttu-id="0ef3a-180">125 000,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-180">125,000.00</span></span>         |
| <span data-ttu-id="0ef3a-181">Tillegg</span><span class="sxs-lookup"><span data-stu-id="0ef3a-181">Surcharge</span></span>     | <span data-ttu-id="0ef3a-182">1 500,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-182">1,500.00</span></span>  | <span data-ttu-id="0ef3a-183">12 500,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-183">12,500.00</span></span>          |
| <span data-ttu-id="0ef3a-184">PE-Cess</span><span class="sxs-lookup"><span data-stu-id="0ef3a-184">PE-Cess</span></span>       | <span data-ttu-id="0ef3a-185">330,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-185">330.00</span></span>    | <span data-ttu-id="0ef3a-186">2 750,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-186">2,750.00</span></span>           |
| <span data-ttu-id="0ef3a-187">SHE Cess</span><span class="sxs-lookup"><span data-stu-id="0ef3a-187">SHE Cess</span></span>      | <span data-ttu-id="0ef3a-188">165,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-188">165.00</span></span>    | <span data-ttu-id="0ef3a-189">1 375,00</span><span class="sxs-lookup"><span data-stu-id="0ef3a-189">1,375.00</span></span>           |

<span data-ttu-id="0ef3a-190">Hvis du bare valgte TDS-beløpene 16 995,00, 22 660,00 og 28 325,00 for utligning på siden **Kildeskattransaksjoner**, vises totalbeløpet for utligning som **67 980,00** i **Rettelse**-feltet på siden **Åpen transaksjonsredigering**.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-190">If you selected only the TDS amounts 16,995.00, 22,660.00, and 2,8325.00 for settlement on the **Withholding tax transactions** page, the total amount for settlement is shown as **67,980.00** in the **Correction** field on the **Open transaction editing** page.</span></span> <span data-ttu-id="0ef3a-191">Hvis denne transaksjonen er merket for utligning og siden **Åpen transaksjonsredigering** er lukket, vises beløpet **67 980,00** i **Debet**-feltet på **Journalbilag**-siden.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-191">If this transaction is marked for settlement, and the **Open transaction editing** page is closed, the amount **67,980.00** is shown in the **Debit** field on the **Journal voucher** page.</span></span>

<span data-ttu-id="0ef3a-192">Du kan nå postere journalen og generere TDS-challan.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-192">You can now post the journal and generate the TDS challan.</span></span>

### <a name="adjustment-of-advance-payments-that-are-made-to-tds-authority-vendors"></a><span data-ttu-id="0ef3a-193">Justering av forskuddsbetalinger til TDS-myndighetsleverandører</span><span class="sxs-lookup"><span data-stu-id="0ef3a-193">Adjustment of advance payments that are made to TDS authority vendors</span></span>

<span data-ttu-id="0ef3a-194">Hvis du vil justere en forskuddsbetaling til TDS-myndighetsleverandøren til en faktisk betaling, kan du gå til **Leverandører \> Leverandører \> Alle leverandører \> Transaksjonsredigering**.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-194">To adjust an advance payment that was made to the TDS authority vendor to an actual payment, go to **Accounts payable \> Vendors \> All vendors \> Transactions editing**.</span></span> <span data-ttu-id="0ef3a-195">Hvis den faktiske betalingen som foretas, overskrider forskuddsbetalingen, genereres to challan-numre for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-195">If the actual payment that is made exceeds the advance payment, two challan numbers are generated for the transaction.</span></span> <span data-ttu-id="0ef3a-196">Det er imidlertid bare det første challan-nummeret som vises i TDS-forespørselen.</span><span class="sxs-lookup"><span data-stu-id="0ef3a-196">However, only the first challan number is shown in the TDS inquiry.</span></span>
