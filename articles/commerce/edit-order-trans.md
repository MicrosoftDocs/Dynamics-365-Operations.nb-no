---
title: Redigere og overvåke nettordretransaksjoner og asynkrone kundeordretransaksjoner
description: Dette emnet beskriver hvordan du redigerer og overvåker nettordretransaksjoner og asynkrone kundeordretransaksjoner i Microsoft Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 11/04/2020
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2018-11-15
ms.dyn365.ops.version: ''
ms.openlocfilehash: b9f2db25c8897662baa177752d0c5fc4ac6178a4
ms.sourcegitcommit: ce51ff2b6099c75dceb99de6dea9d53baf99772d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/04/2020
ms.locfileid: "4459674"
---
# <a name="edit-and-audit-online-order-and-asynchronous-customer-order-transactions"></a><span data-ttu-id="0cc16-103">Redigere og overvåke nettordretransaksjoner og asynkrone kundeordretransaksjoner</span><span class="sxs-lookup"><span data-stu-id="0cc16-103">Edit and audit online order and asynchronous customer order transactions</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cc16-104">Dette emnet beskriver hvordan du redigerer og overvåker nettordretransaksjoner og asynkrone kundeordretransaksjoner i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="0cc16-104">This topic describes how to edit and audit online order and asynchronous customer order transactions in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="0cc16-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="0cc16-105">Overview</span></span>

<span data-ttu-id="0cc16-106">Mellom Commerce-versjon 10.0.5 og 10.0.6 ble støtte lagt til for redigering av hentesalgstransaksjoner (for eksempel salg og returer) og kassastyringstransaksjoner (for eksempel flytregistrering og fjerning av betalingsmiddel).</span><span class="sxs-lookup"><span data-stu-id="0cc16-106">Between Commerce versions 10.0.5 and 10.0.6, support was added for editing cash and carry transactions (such as sales and returns) and cash management transactions (such as float entry and tender removal).</span></span> <span data-ttu-id="0cc16-107">I Commerce-versjon 10.0.7 ble støtte lagt til for redigering av nettordretransaksjoner og asynkrone kundeordretransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="0cc16-107">In Commerce version 10.0.7, support was added for editing online order transactions and asynchronous customer order transactions.</span></span>

## <a name="edit-and-audit-order-transactions"></a><span data-ttu-id="0cc16-108">Redigere og overvåke ordretransaksjoner</span><span class="sxs-lookup"><span data-stu-id="0cc16-108">Edit and audit order transactions</span></span>

<span data-ttu-id="0cc16-109">Følg denne fremgangsmåten for å redigere og overvåke transaksjoner i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="0cc16-109">To edit and audit order transactions in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="0cc16-110">Installer [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span><span class="sxs-lookup"><span data-stu-id="0cc16-110">Install the [Microsoft Dynamics Office Add-in](https://appsource.microsoft.com/product/office/WA104379629?tab=Overview).</span></span>
1. <span data-ttu-id="0cc16-111">På siden **Detaljhandelsparametere** i kategorien **Kundeordrer** angir du en sperrekode i hurtigfanen **Ordre** for **Sperrekode for ordresynkroniseringsfeil**.</span><span class="sxs-lookup"><span data-stu-id="0cc16-111">On the **Retail parameters** page, on the **Customer orders** tab, on the **Order** FastTab, specify a hold code for **Hold code for order synchronization errors**.</span></span>
1. <span data-ttu-id="0cc16-112">Åpne arbeidsområdet **Finans for handelsbutikk**.</span><span class="sxs-lookup"><span data-stu-id="0cc16-112">Open the **Store financials** workspace.</span></span> <span data-ttu-id="0cc16-113">Flisene **Synkroniseringsfeil for nettordre** og **Synkroniseringsfeil for kundeordre** inneholder en forhåndsfiltrert visning av siden Detaljhandelstransaksjon.</span><span class="sxs-lookup"><span data-stu-id="0cc16-113">The **Online order synchronization errors** and **Customer order synchronization errors** tiles provide a prefiltered view of the retail transaction page.</span></span> <span data-ttu-id="0cc16-114">Hver side viser transaksjonspostene som ikke ble synkronisert for tilsvarende ordretype.</span><span class="sxs-lookup"><span data-stu-id="0cc16-114">Each shows the transaction records that have failed synchronization for the corresponding order type.</span></span>
1. <span data-ttu-id="0cc16-115">Åpne siden **Synkroniseringsfeil for nettordre** eller **Synkroniseringsfeil for kundeordre**.</span><span class="sxs-lookup"><span data-stu-id="0cc16-115">Open either the **Online order synchronization errors** page or the **Customer order synchronization errors** page.</span></span> <span data-ttu-id="0cc16-116">Velg en post for å vise detaljer om synkroniseringsfeil.</span><span class="sxs-lookup"><span data-stu-id="0cc16-116">Select a record to view the synchronization error details.</span></span> <span data-ttu-id="0cc16-117">Hurtigfanen **Synkroniseringsstatus** inneholder følgende feildetaljer:</span><span class="sxs-lookup"><span data-stu-id="0cc16-117">The **Synchronization status** FastTab provides the following error details:</span></span>

    - <span data-ttu-id="0cc16-118">Status for ventende ordre</span><span class="sxs-lookup"><span data-stu-id="0cc16-118">Pending order status</span></span>
    - <span data-ttu-id="0cc16-119">Detaljer om ordrefeil</span><span class="sxs-lookup"><span data-stu-id="0cc16-119">Order error details</span></span>
    - <span data-ttu-id="0cc16-120">Endringsdato og -klokkeslett</span><span class="sxs-lookup"><span data-stu-id="0cc16-120">Modified date and time</span></span>
    - <span data-ttu-id="0cc16-121">Antall nye forsøk</span><span class="sxs-lookup"><span data-stu-id="0cc16-121">Retry count</span></span>

1. <span data-ttu-id="0cc16-122">Hvis feildetaljene indikerer at posten må repareres, velger du **Office-tillegg**, og deretter velger du **Rediger valgt transaksjon**.</span><span class="sxs-lookup"><span data-stu-id="0cc16-122">If the error details indicate that the record must be fixed, select **Office Add in**, and then select **Edit selected transaction**.</span></span> <span data-ttu-id="0cc16-123">Det åpnes en Excel-fil som viser detaljene for den valgte transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-123">An Excel file that shows the details of the selected transaction is opened.</span></span>

    - <span data-ttu-id="0cc16-124">Hvis transaksjonen som skal redigeres, er en nettordretransaksjon, inneholder Excel-filen følgende regneark:</span><span class="sxs-lookup"><span data-stu-id="0cc16-124">If the transaction that is being edited is an online order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="0cc16-125">**Transaksjon** – Dette regnearket har hodedetaljene for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-125">**Transaction** – This worksheet has the header details for the transaction.</span></span>
        - <span data-ttu-id="0cc16-126">**Salgstransaksjon** – Dette regnearket har linjedetaljene for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-126">**Sales transaction** – This worksheet has the line details for the transaction.</span></span>
        - <span data-ttu-id="0cc16-127">**Betalingstransaksjoner** – Dette regnearket har detaljene for betalingslinjene for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-127">**Payment transactions** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="0cc16-128">**Rabattransaksjoner** – Dette regnearket har rabattrelaterte detaljer for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-128">**Discount transactions** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="0cc16-129">**Avgiftstransaksjoner** – Dette regnearket har avgiftsrelaterte detaljer for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-129">**Tax transactions** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="0cc16-130">**Gebyrtransaksjoner** – Dette regnearket har gebyrrelaterte data for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-130">**Charges transactions** – This worksheet has the charges-related data for the transaction.</span></span>

    - <span data-ttu-id="0cc16-131">Hvis transaksjonen som skal redigeres, er en asynkron kundeordretransaksjon, inneholder Excel-filen følgende regneark:</span><span class="sxs-lookup"><span data-stu-id="0cc16-131">If the transaction that is being edited is an asynchronous customer order transaction, the Excel file contains the following worksheets:</span></span>

        - <span data-ttu-id="0cc16-132">**Linjer** – Dette regnearket har hode- og linjedetaljene for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-132">**Lines** – This worksheet has the header and line details for the transaction.</span></span>
        - <span data-ttu-id="0cc16-133">**Betalinger** – Dette regnearket har detaljene for betalingslinjene for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-133">**Payments** – This worksheet has the details of the payment lines for the transaction.</span></span>
        - <span data-ttu-id="0cc16-134">**Rabatter** – Dette regnearket har rabattrelaterte detaljer for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-134">**Discounts** – This worksheet has the discount-related details for the transaction.</span></span>
        - <span data-ttu-id="0cc16-135">**Avgifter** – Dette regnearket har avgiftsrelaterte detaljer for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-135">**Taxes** – This worksheet has the tax-related details for the transaction.</span></span>
        - <span data-ttu-id="0cc16-136">**Gebyrer** – Dette regnearket har gebyrrelaterte data for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-136">**Charges** – This worksheet has the charges-related data for the transaction.</span></span>

1. <span data-ttu-id="0cc16-137">Velg **Redigering** I feltet **Status for ventende ordre** I Excel-filen, og publiser deretter endringen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-137">In the Excel file, in the **Pending order status** field, enter **Editing**, and then publish the change.</span></span> <span data-ttu-id="0cc16-138">På denne måten hindrer du at jobben **Synkroniseringsordre** som kjører i satsvis modus, hopper over denne posten under behandling.</span><span class="sxs-lookup"><span data-stu-id="0cc16-138">In this way, you prevent the **Synchronize order** job that is running in batch mode from skipping this record during processing.</span></span>
1. <span data-ttu-id="0cc16-139">I Excel-filen endrer du de aktuelle feltene, og deretter laster du opp dataene tilbake til Commerce Headquarters ved hjelp av publiseringsfunksjonen i Dynamics Excel-tillegget.</span><span class="sxs-lookup"><span data-stu-id="0cc16-139">In the Excel file, modify the appropriate fields, and then upload the data back into Commerce headquarters by using the publishing functionality of the Dynamics Excel Add-in.</span></span> <span data-ttu-id="0cc16-140">Etter at dataene er publisert, vil endringene gjenspeiles i systemet.</span><span class="sxs-lookup"><span data-stu-id="0cc16-140">After the data is published, the changes will be reflected in the system.</span></span> <span data-ttu-id="0cc16-141">Under publiseringen utføres det ingen validering for endringer som brukerne gjør.</span><span class="sxs-lookup"><span data-stu-id="0cc16-141">During publication, no validation is done for changes that users make.</span></span>
1. <span data-ttu-id="0cc16-142">Du kan vise et fullstendig overvåkingsspor for endringene ved å velge **Vis overvåkingsspor** i hodet for **Detaljhandelstransaksjon** for endringer på hodenivå, og i den relevante delen og posten på den riktige transaksjonssiden.</span><span class="sxs-lookup"><span data-stu-id="0cc16-142">You can view a complete audit trail of the changes by selecting **View audit trail** in the **Retail transaction** header for the header-level changes, and in the relevant section and record on the appropriate transaction page.</span></span> <span data-ttu-id="0cc16-143">Alle endringer som er knyttet til salgslinjer, vises for eksempel på siden **Salgstransaksjoner**, og alle endringer som er relatert til betalinger, vises på siden **Betalingstransaksjoner**.</span><span class="sxs-lookup"><span data-stu-id="0cc16-143">For example, all changes that are related to sales lines will be shown on the **Sales transactions** page, and all changes that are related to payments will be shown on the **Payment transactions** page.</span></span> <span data-ttu-id="0cc16-144">Følgende overvåkingsdetaljer beholdes for endringene:</span><span class="sxs-lookup"><span data-stu-id="0cc16-144">The following audit details are maintained for the changes:</span></span>

    - <span data-ttu-id="0cc16-145">Endringsdato og -klokkeslett</span><span class="sxs-lookup"><span data-stu-id="0cc16-145">Modified date and time</span></span>
    - <span data-ttu-id="0cc16-146">Felt</span><span class="sxs-lookup"><span data-stu-id="0cc16-146">Field</span></span>
    - <span data-ttu-id="0cc16-147">Gammel verdi</span><span class="sxs-lookup"><span data-stu-id="0cc16-147">Old value</span></span>
    - <span data-ttu-id="0cc16-148">Ny verdi</span><span class="sxs-lookup"><span data-stu-id="0cc16-148">New value</span></span>
    - <span data-ttu-id="0cc16-149">Endret av</span><span class="sxs-lookup"><span data-stu-id="0cc16-149">Modified by</span></span>

1. <span data-ttu-id="0cc16-150">Etter at du har utført og publisert endringene, velger du **Synkroniser ordre** for å starte synkroniseringsprosessen umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="0cc16-150">After you've made and published your changes, select **Synchronize order** to immediately start the synchronization process.</span></span> <span data-ttu-id="0cc16-151">Du kan også vente på at synkroniseringsprosessen som kjører i satsvis modus, skal behandle transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="0cc16-151">Alternatively, you can wait for the synchronization process that is running in batch mode to process the transaction.</span></span>

<span data-ttu-id="0cc16-152">Når ordrene er synkronisert, settes de som standard i en sperrestatus basert på sperrekoden som er definert i Commerce-parameterne.</span><span class="sxs-lookup"><span data-stu-id="0cc16-152">By default, after the orders are successfully synced, they are put in a hold status, based on the hold code that is defined in the Commerce parameters.</span></span> <span data-ttu-id="0cc16-153">Sperringen av ordrene må fjernes før ordrene kan behandles videre for oppfylling eller andre operasjoner.</span><span class="sxs-lookup"><span data-stu-id="0cc16-153">The hold on the orders must be removed before the orders can be processed further for fulfillment or other operations.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0cc16-154">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0cc16-154">Additional resources</span></span>

[<span data-ttu-id="0cc16-155">Redigere og overvåke hentesalgs- og kassastyringstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="0cc16-155">Edit and audit cash and carry and cash management transactions</span></span>](edit-cash-trans.md)

[<span data-ttu-id="0cc16-156">Redigere finansdimensjoner for detaljhandelstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="0cc16-156">Edit financial dimensions for retail transactions</span></span>](edit-financial-dim.md)

[<span data-ttu-id="0cc16-157">Opprette en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="0cc16-157">Create an Excel workbook to edit retail transactions</span></span>](create-excel-edit.md)

[<span data-ttu-id="0cc16-158">Legge til felt i en Excel-arbeidsbok for å redigere detaljhandelstransaksjoner</span><span class="sxs-lookup"><span data-stu-id="0cc16-158">Add fields to an Excel workbook to edit retail transactions</span></span>](add-fields-excel.md)
