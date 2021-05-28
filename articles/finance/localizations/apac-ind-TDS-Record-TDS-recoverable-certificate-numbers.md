---
title: Registrer numre på fradragsberettigede TDS-sertifikater
description: Dette emnet forklarer hvordan du bruker siden Fradragsberettigede sertifikater til å registrere sertifikatnumrene og -datoene for TDS-sertifikater (Tax Deducted at Source) for en bestemt leverandør, kunde eller finans.
author: kailiang
mms.date: 02/12/2021
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
ms.openlocfilehash: b501c331cccc6d030f36d0a13ba0a6a13c08c733
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023464"
---
# <a name="record-tds-recoverable-certificate-numbers"></a><span data-ttu-id="b714e-103">Registrer numre på fradragsberettigede TDS-sertifikater</span><span class="sxs-lookup"><span data-stu-id="b714e-103">Record TDS recoverable certificate numbers</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b714e-104">Dette emnet forklarer hvordan du bruker siden **Fradragsberettigede sertifikater** til å registrere sertifikatnumrene og -datoene for TDS-sertifikater (Tax Deducted at Source) for en bestemt leverandør, kunde eller finans.</span><span class="sxs-lookup"><span data-stu-id="b714e-104">This topic explains how to use the **Recoverable certificates** page to record the certificate numbers and dates for Tax Deducted at Source (TDS) certificates that are received for a specific vendor, customer, or ledger.</span></span> <span data-ttu-id="b714e-105">Hvis du vil oppdatere TDS-sertifikatnumrene og -datoene som er registrert for TDS-transaksjoner på denne siden, bruker du siden **Oppdater sertifikat** (**Økonomimodul \> Periodisk \> Kildeskatt \> Oppdater sertifikat**).</span><span class="sxs-lookup"><span data-stu-id="b714e-105">To update the TDS certificate numbers and dates that are recorded for TDS transactions on this page, use the **Update certificate** page (**General ledger \> Periodic \> Withholding tax \> Update certificate**).</span></span> <span data-ttu-id="b714e-106">Når du er ferdig å oppdatere TDS-sertifikatnumre, lukker du dem.</span><span class="sxs-lookup"><span data-stu-id="b714e-106">After you've finished updating TDS certificate numbers, close them.</span></span>

<span data-ttu-id="b714e-107">Følg denne fremgangsmåten for å registrere TDS-sertifikatnumrene og -datoene.</span><span class="sxs-lookup"><span data-stu-id="b714e-107">Follow these steps to record the TDS certificate numbers and dates.</span></span>

1. <span data-ttu-id="b714e-108">Gå til **Avgift \> Indirekte avgift \> Kildeskatt \> Fradragsberettigede sertifikater**.</span><span class="sxs-lookup"><span data-stu-id="b714e-108">Go to **Tax \> Indirect tax \> Withholding tax \> Recoverable certificates**.</span></span>

    <span data-ttu-id="b714e-109">[![Siden Fradragsberettigede sertifikater](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span><span class="sxs-lookup"><span data-stu-id="b714e-109">[![Recoverable certificates page](./media/apac-ind-TDS-49.png)](./media/apac-ind-TDS-49.png)</span></span> 

2. <span data-ttu-id="b714e-110">Velg **TDS** i **Avgiftstype**-feltet på siden **Fradragsberettigede sertifikater**.</span><span class="sxs-lookup"><span data-stu-id="b714e-110">On the **Recoverable certificates** page, in the **Tax type** field, select **TDS**.</span></span>
3. <span data-ttu-id="b714e-111">Velg **Ny** for å opprette en oppføring.</span><span class="sxs-lookup"><span data-stu-id="b714e-111">Select **New** to create a record.</span></span>
4. <span data-ttu-id="b714e-112">Angi TDS-sertifikatnummeret i **Sertifikatnummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b714e-112">In the **Certificate number** field, enter the TDS certificate number.</span></span>
5. <span data-ttu-id="b714e-113">I **Kontotype**-feltet velger du kontotypen som TDS-sertifikatet mottas for: **Leverandør**, **Kunde** eller **Finans**.</span><span class="sxs-lookup"><span data-stu-id="b714e-113">In the **Account type** field, select the type of account that the TDS certificate is received for: **Vendor**, **Customer**, or **Ledger**.</span></span>
6. <span data-ttu-id="b714e-114">I **Konto**-feltet velger du nummeret på leverandør-, kunde- eller finanskontoen, avhengig av kontotypen du har valgt.</span><span class="sxs-lookup"><span data-stu-id="b714e-114">In the **Account** field, select the vendor, customer, or ledger account number, depending on the account type that you selected.</span></span> <span data-ttu-id="b714e-115">**Navn**-feltet viser navnet på leverandør-, kunde- eller finanskontoen.</span><span class="sxs-lookup"><span data-stu-id="b714e-115">The **Name** field shows the name of the vendor, customer, or ledger account.</span></span>
7. <span data-ttu-id="b714e-116">I **Sertifikatbeløp**-feltet angir du beløpet på TDS-sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="b714e-116">In the **Certificate amount** field, enter the amount of the TDS certificate.</span></span>
8. <span data-ttu-id="b714e-117">Angi sertifikatdatoen for sertifikatnummeret i **Dato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b714e-117">In the **Date** field, enter the certificate date for the certificate number.</span></span>
9. <span data-ttu-id="b714e-118">Velg **Forespørsler** for å åpne siden **Sertifikattransaksjoner**, der du kan vise TDS-transaksjonene som TDS-sertifikatnummeret og -datoen er oppdatert for.</span><span class="sxs-lookup"><span data-stu-id="b714e-118">Select **Inquiries** to open the **Certificate transactions** page, where you can view the TDS transactions that the TDS certificate number and date are updated for.</span></span> <span data-ttu-id="b714e-119">Denne informasjonen kan oppdateres på siden **Oppdater sertifikat** (**Avgift \> Deklareringer \> Kildeskatt \> Oppdater sertifikat**).</span><span class="sxs-lookup"><span data-stu-id="b714e-119">This information can be updated on the **Update certificate** page (**Tax \> Declarations \> Withholding tax \> Update certificate**).</span></span>

    <span data-ttu-id="b714e-120">Siden **Oppdater sertifikat** viser følgende informasjon for hver TDS-transaksjon:</span><span class="sxs-lookup"><span data-stu-id="b714e-120">The **Update certificate** page shows the following information for each TDS transaction:</span></span>

    - <span data-ttu-id="b714e-121">**Dato** – Posteringsdatoen for TDS-transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="b714e-121">**Date** – The posting date of the TDS transaction.</span></span>
    - <span data-ttu-id="b714e-122">**Bilag** – Bilagsnummeret for TDS-transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="b714e-122">**Voucher** – The voucher number of the TDS transaction.</span></span>
    - <span data-ttu-id="b714e-123">**Kilde** – Modulen som TDS-transaksjonen ble opprettet i.</span><span class="sxs-lookup"><span data-stu-id="b714e-123">**Source** – The module that the TDS transaction was created in.</span></span>
    - <span data-ttu-id="b714e-124">**Konto** – Nummeret på leverandør-, kunde- eller finanskontoen som TDS-transaksjonen ble opprettet for.</span><span class="sxs-lookup"><span data-stu-id="b714e-124">**Account** – The vendor, customer, or ledger account number that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="b714e-125">**Navn** – Navnet på leverandør-, kunde- eller finanskontoen som TDS-transaksjonen ble opprettet for.</span><span class="sxs-lookup"><span data-stu-id="b714e-125">**Name** – The name of the vendor, customer, or ledger account that the TDS transaction was created for.</span></span>
    - <span data-ttu-id="b714e-126">**Beløp** – Fakturabeløpet som TDS ble beregnet for.</span><span class="sxs-lookup"><span data-stu-id="b714e-126">**Amount** – The invoice amount that the TDS was calculated on.</span></span>
    - <span data-ttu-id="b714e-127">**Avgiftsbeløp** – TDS-avgiftsbeløpet som ble beregnet for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="b714e-127">**Tax amount** – The TDS tax amount that was calculated for the transaction.</span></span>
    - <span data-ttu-id="b714e-128">**Sertifikatdato** – TDS-sertifikatdatoen som ble oppdatert for TDS-transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="b714e-128">**Certificate date** – The TDS certificate date that was updated for the TDS transaction.</span></span>
    - <span data-ttu-id="b714e-129">**Sertifikatnummer** – TDS-sertifikatnummeret som ble oppdatert for TDS-transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="b714e-129">**Certificate number** – TDS certificate number that was updated for the TDS transaction.</span></span>

10. <span data-ttu-id="b714e-130">Merk av for **Lukket** på siden **Fradragsberettigede sertifikater** for å lukke TDS-sertifikatnummeret etter at du er ferdig å oppdatere det for TDS-transaksjoner på siden **Oppdater sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="b714e-130">On the **Recoverable certificates** page, select the **Closed** check box to close the TDS certificate number after you've finished updating it for TDS transactions on the **Update certificate** page.</span></span>

    <span data-ttu-id="b714e-131">Hvis du vil merke av for **Lukket** for alle poster på siden, velger du **Merk alle**.</span><span class="sxs-lookup"><span data-stu-id="b714e-131">To select the **Closed** check box for all records on the page, select **Mark all**.</span></span>

    > [!NOTE]
    > <span data-ttu-id="b714e-132">TDS-sertifikatnumre som alternativet **Lukket** er merket av for, er ikke tilgjengelige på siden **Oppdater sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="b714e-132">TDS certificate numbers that the **Closed** check box is selected for aren't available on the **Update certificate** page.</span></span>
