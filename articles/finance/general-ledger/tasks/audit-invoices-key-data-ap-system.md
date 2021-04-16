---
title: Revidere fakturaer og nøkkeldata i Leverandører
description: Dette emnet viser hvordan du reviderer fakturaer og nøkkeldata i Leverandører.
author: saraschi2
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, PurchEditLines, VendEditInvoice, VendEditInvoiceDefaultQuantityForLinesDropDialog,  VendJournalMatch_PackingSlip, VendInvoiceMatchingDetails
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6ac1e9d8c5255b8347c9563ce9ea846933c0c9dd
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5815242"
---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="8dc0d-103">Revidere fakturaer og nøkkeldata i Leverandører</span><span class="sxs-lookup"><span data-stu-id="8dc0d-103">Audit invoices and key data in accounts payable</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="8dc0d-104">Når du mottar en faktura fra en leverandør for varer eller tjenester på en bestilling, kan det hende at forretningsprosessene krever at varene eller tjenestene er mottatt før fakturaen kan godkjennes for betaling.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="8dc0d-105">Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="8dc0d-106">På siden **Leverandørparametere** kontrollerer du at alternativet Aktiver validering av fakturakontroll er valgt, at feltet **Poster faktura med avvik** er satt til **Krev godkjenning**, og at feltet **Linjekontrollpolicy** er satt til **Treveis samsvar**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-106">In the **Accounts payable parameters** page, ensure that the Enable invoice matching validation option is selected, the **Post invoice with discrepancies** field is set to **Require approval**, and the **Line matching policy** field is set to **Three-way matching**.</span></span>

<span data-ttu-id="8dc0d-107">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="8dc0d-108">Rollen regnskapssjef leverandørreskontro eller regnskapssjef kan utføre disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="8dc0d-109">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="8dc0d-109">Create a purchase order</span></span>
1. <span data-ttu-id="8dc0d-110">Gå til **Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-110">Go to **All purchase orders**.</span></span>
2. <span data-ttu-id="8dc0d-111">Klikk **Ny**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-111">Click **New**.</span></span>
3. <span data-ttu-id="8dc0d-112">Angi en verdi i **Leverandørkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-112">In the **Vendor account** field, type a value.</span></span>
4. <span data-ttu-id="8dc0d-113">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-113">Click **OK**.</span></span>
5. <span data-ttu-id="8dc0d-114">Klikk **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-114">Click **Add line**.</span></span>
6. <span data-ttu-id="8dc0d-115">Skriv inn en verdi i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-115">In the **Item number** field, type a value.</span></span>
7. <span data-ttu-id="8dc0d-116">Klikk **Innkjøp** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-116">On the Action Pane, click **Purchase**.</span></span>
8. <span data-ttu-id="8dc0d-117">Klikk **Bekreft**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-117">Click **Confirm**.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="8dc0d-118">Postere en produktkvittering</span><span class="sxs-lookup"><span data-stu-id="8dc0d-118">Post a product receipt</span></span>
1. <span data-ttu-id="8dc0d-119">Klikk **Motta** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-119">On the Action Pane, click **Receive**.</span></span>
2. <span data-ttu-id="8dc0d-120">Klikk **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-120">Click **Product receipt**.</span></span>
3. <span data-ttu-id="8dc0d-121">Skriv inn en verdi i feltet **Produktkvittering**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-121">In the **Product receipt** field, type a value.</span></span>
4. <span data-ttu-id="8dc0d-122">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-122">Click **OK**.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="8dc0d-123">Registrere og samsvare en leverandørfakturaer med en produktkvittering</span><span class="sxs-lookup"><span data-stu-id="8dc0d-123">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="8dc0d-124">Klikk **Faktura** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-124">On the Action Pane, click **Invoice > Invoice**.</span></span>
2. <span data-ttu-id="8dc0d-125">Skriv inn en verdi i **Nummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-125">In the **Number** field, type a value.</span></span>
3. <span data-ttu-id="8dc0d-126">Klikk **Standard fra: Bestilt antall** for å åpne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-126">Click **Default from: Ordered quantity** to open the drop dialog.</span></span>
4. <span data-ttu-id="8dc0d-127">Velg et alternativ i feltet **Standardantall for linjer**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-127">In the **Default quantity for lines** field, select an option.</span></span>
5. <span data-ttu-id="8dc0d-128">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-128">Click **OK**.</span></span>
6. <span data-ttu-id="8dc0d-129">Klikk **Ja**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-129">Click **Yes**.</span></span>
7. <span data-ttu-id="8dc0d-130">Klikk **Avstem produktkvitteringer**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-130">Click **Match product receipts**.</span></span>
8. <span data-ttu-id="8dc0d-131">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-131">Click **OK**.</span></span>
9. <span data-ttu-id="8dc0d-132">Klikk **Gå gjennom** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-132">On the Action Pane, click **Review**.</span></span>
10. <span data-ttu-id="8dc0d-133">Klikk **Samsvarende detaljer**.</span><span class="sxs-lookup"><span data-stu-id="8dc0d-133">Click **Matching details**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]