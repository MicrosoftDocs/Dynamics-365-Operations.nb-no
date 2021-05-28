---
title: Oppdatere sertifikatnumre og -datoer for TDS-transaksjoner
description: Dette emnet forklarer hvordan du oppdaterer numrene og datoene for fradragsberettigede sertifikater som ble registrert for leverandør-, kunde- og finanskontoer for TDS (Tax Deducted at Source).
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
ms.openlocfilehash: 248de8e12703a84482b67d0899857a6efb33531c
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023474"
---
# <a name="update-certificate-numbers-and-dates-for-tds-transactions"></a><span data-ttu-id="362c4-103">Oppdatere sertifikatnumre og -datoer for TDS-transaksjoner</span><span class="sxs-lookup"><span data-stu-id="362c4-103">Update certificate numbers and dates for TDS transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="362c4-104">Dette emnet forklarer hvordan du oppdaterer numrene og datoene for fradragsberettigede sertifikater som ble registrert for leverandør-, kunde- og finanskontoer for TDS (Tax Deducted at Source).</span><span class="sxs-lookup"><span data-stu-id="362c4-104">This topic explains how to update the recoverable certificate numbers and dates that were recorded for vendor, customer, and ledger accounts for Tax Deducted at Source (TDS).</span></span> <span data-ttu-id="362c4-105">Du kan vise sertifikatene for TDS-transaksjoner på siden **Fradragsberettigede sertifikater**.</span><span class="sxs-lookup"><span data-stu-id="362c4-105">You can view the certificates for TDS transactions on the **Recoverable certificates** page.</span></span> <span data-ttu-id="362c4-106">Du kan oppdatere sertifikatene ved å bruke **Oppdater sertifikater**-siden.</span><span class="sxs-lookup"><span data-stu-id="362c4-106">You can update the certificates by using the **Update Certificates** page.</span></span>

<span data-ttu-id="362c4-107">Følg denne fremgangsmåten for å oppdatere sertifikatnumrene og -datoene for TDS-transaksjoner.</span><span class="sxs-lookup"><span data-stu-id="362c4-107">Follow these steps to update certificate numbers and dates for TDS transactions.</span></span>

1. <span data-ttu-id="362c4-108">Gå til **Avgift \> Deklareringer \> Kildeskatt \> Oppdater sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="362c4-108">Go to **Tax \> Declarations \> Withholding tax \> Update certificate**.</span></span>

    <span data-ttu-id="362c4-109">[![Siden Oppdater sertifikat](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span><span class="sxs-lookup"><span data-stu-id="362c4-109">[![Update certificate page](./media/apac-ind-TDS-45.png)](./media/apac-ind-TDS-45.png)</span></span>

2. <span data-ttu-id="362c4-110">Velg **TDS** i **Avgiftstype**-feltet i **Velg**-delen på siden **Oppdater sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="362c4-110">On the **Update certificate** page, in the **Select** section, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="362c4-111">Velg kundens eller leverandørens TDS-sertifikatnummer i **Sertifikatnummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="362c4-111">In the **Certificate number** field, select the customer's or vendor's TDS certificate number.</span></span>

    > [!NOTE]
    > <span data-ttu-id="362c4-112">**Sertifikatnummer**-feltet viser bare TDS-sertifikatnumre som alternativet **Lukket** ikke er avmerket for, på siden **Fradragsberettigede sertifikater**.</span><span class="sxs-lookup"><span data-stu-id="362c4-112">The **Certificate number** field lists only TDS certificate numbers that the **Closed** check box is cleared for on the **Recoverable certificates** page.</span></span>

    <span data-ttu-id="362c4-113">**Sertifikatdato**-feltet viser sertifikatdatoen.</span><span class="sxs-lookup"><span data-stu-id="362c4-113">The **Certificate date** field shows the certificate date.</span></span> <span data-ttu-id="362c4-114">**Kontotype**-feltet viser kontotypen som TDS-sertifikatnummeret mottas for, og **Navn**-feltet viser navnet på kontoen.</span><span class="sxs-lookup"><span data-stu-id="362c4-114">The **Account type** field shows the type of account that the TDS certificate number is received for, and the **Name** field shows the name of the account.</span></span>

5. <span data-ttu-id="362c4-115">Velg start- og sluttdatoene for perioden du vil vise TDS-transaksjonene for, i feltene **Fra-dato** og **Til-dato** .</span><span class="sxs-lookup"><span data-stu-id="362c4-115">In the **From date** and **To date** fields, select the start and end dates of the period to show the TDS transactions for.</span></span>
6. <span data-ttu-id="362c4-116">Velg **Vis data** for å vise TDS-transaksjonene som ble postert i løpet av den valgte perioden.</span><span class="sxs-lookup"><span data-stu-id="362c4-116">Select **Show data** to view the TDS transactions that were posted during the selected period.</span></span>

    <span data-ttu-id="362c4-117">Rutenettet i den øvre ruten i **Oversikt**-fanen viser følgende informasjon om hver TDS-transaksjon som ble postert for leverandøren eller kunden i løpet av den valgte perioden:</span><span class="sxs-lookup"><span data-stu-id="362c4-117">On the **Overview** tab, the grid in the upper pane shows the following information about each TDS transaction that was posted for the vendor or customer during the selected period:</span></span>

    - <span data-ttu-id="362c4-118">**Bilag** – Bilagsnummeret for TDS-transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="362c4-118">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="362c4-119">**Dato** – Datoen for TDS-transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="362c4-119">**Date** – The date of the TDS transaction.</span></span>
    - <span data-ttu-id="362c4-120">**Beløp** – Fakturabeløpet som TDS ble beregnet for.</span><span class="sxs-lookup"><span data-stu-id="362c4-120">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="362c4-121">**Avgiftsbeløp** – TDS-avgiftsbeløpet som ble beregnet for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="362c4-121">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>

7. <span data-ttu-id="362c4-122">Hvis du vil flytte bestemte TDS-transaksjoner fra det øvre til det nedre rutenettet, velger du transaksjonene og deretter **Inkluder**.</span><span class="sxs-lookup"><span data-stu-id="362c4-122">To move specific TDS transactions from the upper grid to the lower grid, select the transactions, and then select **Include**.</span></span> <span data-ttu-id="362c4-123">Du kan også velge **Inkluder alle** hvis du vil flytte alle TDS-transaksjoner fra det øvre til det nedre rutenettet.</span><span class="sxs-lookup"><span data-stu-id="362c4-123">Alternatively, select **Include all** to move all TDS transactions from the upper grid to the lower grid.</span></span>

    <span data-ttu-id="362c4-124">Hvis du vil flytte bestemte TDS-transaksjoner eller alle TDS-transaksjoner fra det nedre til det øvre rutenettet, bruker du knappen **Utelat** eller **Utelat alle**.</span><span class="sxs-lookup"><span data-stu-id="362c4-124">To move specific TDS transactions or all TDS transactions from the lower grid to the upper grid, use the **Exclude** or **Exclude all** button.</span></span>

8. <span data-ttu-id="362c4-125">Velg **Oppdater** for å oppdatere feltene **Sertifikatnummer** og **Sertifikatdato** for TDS-transaksjoner i det nedre rutenettet.</span><span class="sxs-lookup"><span data-stu-id="362c4-125">Select **Update** to update the **Certificate number** and **Certificate date** fields for TDS transactions in the lower grid.</span></span>
10. <span data-ttu-id="362c4-126">Gå til **Avgift \> Indirekte avgifter \> Kildeskatt \> Fradragsberettigede sertifikater**, og velg **Forespørsel** for å vise de oppdaterte transaksjonslinjene som har de nye sertifikatnumrene på **Sertifikattransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="362c4-126">Go to **Tax \> Indirect taxes \> Withholding tax \> Recoverable certificate**, and select **Inquiry** to view the updated transaction lines that have the new certificate numbers on the **Certificate transactions** page.</span></span>

    <span data-ttu-id="362c4-127">[![Siden Sertifikattransaksjoner](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span><span class="sxs-lookup"><span data-stu-id="362c4-127">[![Certificate transactions page](./media/apac-ind-TDS-46.png)](./media/apac-ind-TDS-46.png)</span></span>
