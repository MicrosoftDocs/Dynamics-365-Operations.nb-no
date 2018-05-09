--- 
title: "Revidere fakturaer og nøkkeldata i Leverandører"
description: "Når du mottar en faktura fra en leverandør for varer eller tjenester på en bestilling, kan det hende at forretningsprosessene krever at varene eller tjenestene er mottatt før fakturaen kan godkjennes for betaling."
author: saraschi2
manager: AnnBe
ms.date: 02/16/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: cba7a6519847945cd3e9e524b8871a1dad9984d4
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="audit-invoices-and-key-data-in-accounts-payable"></a><span data-ttu-id="f12cc-103">Revidere fakturaer og nøkkeldata i Leverandører</span><span class="sxs-lookup"><span data-stu-id="f12cc-103">Audit invoices and key data in accounts payable</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f12cc-104">Når du mottar en faktura fra en leverandør for varer eller tjenester på en bestilling, kan det hende at forretningsprosessene krever at varene eller tjenestene er mottatt før fakturaen kan godkjennes for betaling.</span><span class="sxs-lookup"><span data-stu-id="f12cc-104">When you receive an invoice from a vendor for goods or services on a purchase order, the business processes might require that the goods or services be received before the invoice can be approved for payment.</span></span> <span data-ttu-id="f12cc-105">Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt.</span><span class="sxs-lookup"><span data-stu-id="f12cc-105">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span> 

<span data-ttu-id="f12cc-106">På siden Leverandørparametere kontrollerer du at alternativet Aktiver validering av fakturakontroll er valgt, at feltet Poster faktura med avvik er satt til Krev godkjenning, og at Linjekontrollpolicy-feltet er satt til Treveis samsvar.</span><span class="sxs-lookup"><span data-stu-id="f12cc-106">In the Accounts payable parameters page, ensure that the Enable invoice matching validation option is selected, the Post invoice with discrepancies field is set to Require approval, and the Line matching policy field is set to Three-way matching.</span></span>

<span data-ttu-id="f12cc-107">Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="f12cc-107">This procedure uses the USMF demo company.</span></span> <span data-ttu-id="f12cc-108">Rollen regnskapssjef leverandørreskontro eller regnskapssjef kan utføre disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="f12cc-108">The accounts payable manager or accounting manager role would perform these steps.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="f12cc-109">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="f12cc-109">Create a purchase order</span></span>
1. <span data-ttu-id="f12cc-110">Gå til Alle bestillinger.</span><span class="sxs-lookup"><span data-stu-id="f12cc-110">Go to All purchase orders.</span></span>
2. <span data-ttu-id="f12cc-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f12cc-111">Click New.</span></span>
3. <span data-ttu-id="f12cc-112">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="f12cc-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="f12cc-113">Angi en verdi i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="f12cc-113">In the Vendor account field, type a value.</span></span>
5. <span data-ttu-id="f12cc-114">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f12cc-114">Click OK.</span></span>
6. <span data-ttu-id="f12cc-115">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="f12cc-115">Click Add line.</span></span>
7. <span data-ttu-id="f12cc-116">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f12cc-116">In the Item number field, type a value.</span></span>
8. <span data-ttu-id="f12cc-117">Klikk Kjøp i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f12cc-117">On the Action Pane, click Purchase.</span></span>
9. <span data-ttu-id="f12cc-118">Klikk Bekreft.</span><span class="sxs-lookup"><span data-stu-id="f12cc-118">Click Confirm.</span></span>

## <a name="post-a-product-receipt"></a><span data-ttu-id="f12cc-119">Postere en produktkvittering</span><span class="sxs-lookup"><span data-stu-id="f12cc-119">Post a product receipt</span></span>
1. <span data-ttu-id="f12cc-120">Klikk Motta i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f12cc-120">On the Action Pane, click Receive.</span></span>
2. <span data-ttu-id="f12cc-121">Klikk Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="f12cc-121">Click Product receipt.</span></span>
3. <span data-ttu-id="f12cc-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f12cc-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f12cc-123">Skriv inn en verdi i feltet Produktkvittering.</span><span class="sxs-lookup"><span data-stu-id="f12cc-123">In the Product receipt field, type a value.</span></span>
5. <span data-ttu-id="f12cc-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f12cc-124">Click OK.</span></span>

## <a name="record-and-match-a-vendor-invoice-to-a-product-receipt"></a><span data-ttu-id="f12cc-125">Registrere og samsvare en leverandørfakturaer med en produktkvittering</span><span class="sxs-lookup"><span data-stu-id="f12cc-125">Record and match a vendor invoice to a product receipt</span></span>
1. <span data-ttu-id="f12cc-126">Klikk Faktura i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f12cc-126">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="f12cc-127">Klikk Faktura.</span><span class="sxs-lookup"><span data-stu-id="f12cc-127">Click Invoice.</span></span>
3. <span data-ttu-id="f12cc-128">Skriv inn en verdi i Nummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="f12cc-128">In the Number field, type a value.</span></span>
4. <span data-ttu-id="f12cc-129">Klikk Standard fra: Bestilt antall for å åpne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="f12cc-129">Click Default from: Ordered quantity to open the drop dialog.</span></span>
5. <span data-ttu-id="f12cc-130">Velg et alternativ i feltet Standardantall for linjer.</span><span class="sxs-lookup"><span data-stu-id="f12cc-130">In the Default quantity for lines field, select an option.</span></span>
6. <span data-ttu-id="f12cc-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f12cc-131">Click OK.</span></span>
7. <span data-ttu-id="f12cc-132">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="f12cc-132">Click Yes.</span></span>
8. <span data-ttu-id="f12cc-133">Klikk Avstem produktkvitteringer.</span><span class="sxs-lookup"><span data-stu-id="f12cc-133">Click Match product receipts.</span></span>
9. <span data-ttu-id="f12cc-134">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f12cc-134">Click OK.</span></span>
10. <span data-ttu-id="f12cc-135">Klikk Gå gjennom i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f12cc-135">On the Action Pane, click Review.</span></span>
11. <span data-ttu-id="f12cc-136">Klikk Samsvarende detaljer.</span><span class="sxs-lookup"><span data-stu-id="f12cc-136">Click Matching details.</span></span>


