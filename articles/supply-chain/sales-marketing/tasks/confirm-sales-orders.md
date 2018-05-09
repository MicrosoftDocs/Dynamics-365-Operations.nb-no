--- 
title: Bekrefte salgsordrer
description: "Denne fremgangsmåten beskriver hvordan du bekrefter salgsordrer."
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 636b23c8f87d79b0e62e5e92e79aacc33171cdfc
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="confirm-sales-orders"></a><span data-ttu-id="4e6d5-103">Bekrefte salgsordrer</span><span class="sxs-lookup"><span data-stu-id="4e6d5-103">Confirm sales orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4e6d5-104">Denne fremgangsmåten beskriver hvordan du bekrefter salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-104">This procedure demonstrates how to confirm sales orders.</span></span> <span data-ttu-id="4e6d5-105">Du vil bli vist hvordan du bekrefter en enkelt ordre, og hvordan du bekrefter flere ordrer samtidig.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-105">You’ll be shown how to confirm a single order, and how to confirm multiple orders at once.</span></span> <span data-ttu-id="4e6d5-106">Disse oppgavene vil vanligvis utføres av en salgsordrebehandler.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-106">These tasks would typically be carried out by a sales order processor.</span></span> <span data-ttu-id="4e6d5-107">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="4e6d5-108">Før du begynner kontrollerer du at det er flere åpne salgsordrer for den samme kunden.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-108">Before you start, make sure there are several open sales orders for the same customer.</span></span> <span data-ttu-id="4e6d5-109">Hvis du bruker USMF, kan du bruke US-027 for kunde.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-109">If you’re using USMF, you can use customer US-027.</span></span>


## <a name="confirm-a-single-sales-order"></a><span data-ttu-id="4e6d5-110">Bekrefte en enkelt salgsordre</span><span class="sxs-lookup"><span data-stu-id="4e6d5-110">Confirm a single sales order</span></span>
1. <span data-ttu-id="4e6d5-111">Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-111">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="4e6d5-112">Finn og velg ordren du vil bekrefte i listen.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-112">In the list, find and select the order that you want to confirm.</span></span>
3. <span data-ttu-id="4e6d5-113">Klikk koblingen på salgsordrenummeret for å åpne den valgte ordren.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-113">Click the link on the sales order number to open the selected order.</span></span>
4. <span data-ttu-id="4e6d5-114">Klikk Selg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-114">On the Action Pane, click Sell.</span></span>
5. <span data-ttu-id="4e6d5-115">Klikk Bekreft salgsordre.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-115">Click Confirm sales order.</span></span>
6. <span data-ttu-id="4e6d5-116">Vis eller skjul delen Parametere.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-116">Expand or collapse the Parameters section.</span></span>
    * <span data-ttu-id="4e6d5-117">Kontroller at feltet Postering Ja er aktivt.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-117">Make sure that the Posting Yes field is active.</span></span>  
7. <span data-ttu-id="4e6d5-118">Angi alternativet Skriv ut bekreftelse til Ja.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-118">Set the Print confirmation option to Yes.</span></span>
    * <span data-ttu-id="4e6d5-119">Feltet Kontroller kredittgrense angir metoden som brukes til å beregne kundens gjenværende kreditt.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-119">The Check credit limit field specifies the method that’s used to calculate a customer's remaining credit.</span></span> <span data-ttu-id="4e6d5-120">Den kopieres som standard fra siden Kundeparametere.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-120">By default, it’s copied from the Accounts receivable parameters page.</span></span> <span data-ttu-id="4e6d5-121">Hvis du vil hoppe over kredittgrensekontrollen ved bekreftelse av en bestemt salgsordre, setter du Kontroller kredittgrense til Ingen.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-121">If you want to skip the credit limit check when confirming a specific sales order, set the Check credit limit to None.</span></span> <span data-ttu-id="4e6d5-122">Du bør imidlertid være oppmerksom på at selv om dette feltet er satt til Ingen, vil kredittgrensekontrollen fremdeles utføres hvis alternativet Obligatorisk kredittgrense er valgt i hoveddata for kunder.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-122">However, you should be aware that even with if this field is set to None, the credit limit check will still be performed if the Mandatory credit limit option is selected on the customer master data.</span></span>  
8. <span data-ttu-id="4e6d5-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-123">Click OK.</span></span>
9. <span data-ttu-id="4e6d5-124">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-124">Click Yes.</span></span>
10. <span data-ttu-id="4e6d5-125">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-125">Close the page.</span></span>
11. <span data-ttu-id="4e6d5-126">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="4e6d5-127">Klikk Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-127">Click Change view.</span></span>
13. <span data-ttu-id="4e6d5-128">Klikk Hodevisning.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-128">Click Header view.</span></span>
    * <span data-ttu-id="4e6d5-129">Når en ordre er bekreftet, vil dokumentstatusen settes til Bekreftelse.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-129">When an order is confirmed, the Document status is set to Confirmation.</span></span>  
14. <span data-ttu-id="4e6d5-130">Klikk Selg i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-130">On the Action Pane, click Sell.</span></span>
15. <span data-ttu-id="4e6d5-131">Klikk Salgsordrebekreftelse.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-131">Click Sales order confirmation.</span></span>
16. <span data-ttu-id="4e6d5-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-132">Close the page.</span></span>

## <a name="confirm-multiple-sales-orders-at-once"></a><span data-ttu-id="4e6d5-133">Bekrefte flere salgsordrer samtidig</span><span class="sxs-lookup"><span data-stu-id="4e6d5-133">Confirm multiple sales orders at once</span></span>
1. <span data-ttu-id="4e6d5-134">Gå til Salg og markedsføring > Salgsordrer > Ordrebekreftelse > Bekreft salgsordre.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-134">Go to Sales and marketing > Sales orders > Order confirmation > Confirm sales order.</span></span>
2. <span data-ttu-id="4e6d5-135">Klikk Velg.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-135">Click Select.</span></span>
3. <span data-ttu-id="4e6d5-136">I listen i kategorien Område finner og velger du posten som refererer til feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-136">In the list on the Range tab, find and select the record that references the Customer account field.</span></span>
4. <span data-ttu-id="4e6d5-137">Klikk rullegardinknappen i Kriterier-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-137">In the Criteria field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="4e6d5-138">I listen finner og merker du kundekontoen som har flere ordrer som du vil massebekrefte.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-138">In the list, find and select the customer account that has multiple orders which you want to mass confirm.</span></span>
    * <span data-ttu-id="4e6d5-139">Hvis du bruker USMF, kan du velge kontoen US-027.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-139">If you’re using USMF, you can select account US-027.</span></span>  
6. <span data-ttu-id="4e6d5-140">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-140">Click OK.</span></span>
    * <span data-ttu-id="4e6d5-141">Kategorien Oversikt viser en liste over ordrene som samsvarer med spørringskriteriene.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-141">The Overview tab displays a list of the orders that match the query criteria.</span></span> <span data-ttu-id="4e6d5-142">Disse vil være inkludert i bekreftelsen.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-142">These will be included in the confirmation.</span></span>  
    * <span data-ttu-id="4e6d5-143">Samleoppdatering for-feltet angir parameteren som er ordrene som skal summeres etter, i ett bekreftelsesdokument.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-143">The Summary update for field specifies the parameter by which multiple orders are to be summarized into one confirmation document.</span></span> <span data-ttu-id="4e6d5-144">Som standard kopieres alternativet fra innstillingen Standardverdier for samleoppdatering på siden Kundeparametere.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-144">By default, the option is copied from the Default values for summary update setting on the Accounts receivable parameters page.</span></span>  
7. <span data-ttu-id="4e6d5-145">I feltet Samleoppdatering for velger du Ordre.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-145">In the Summary update for field, select 'Order'.</span></span>
    * <span data-ttu-id="4e6d5-146">Minimumsparameterne som kreves for å opprette samleoppdateringer, er fakturakonto og valuta.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-146">The minimum parameters that are required to create summary updates are Invoice account and Currency.</span></span> <span data-ttu-id="4e6d5-147">Dette betyr at samleoppdateringer som har forskjellige fakturakontoer og forskjellige valutaer ikke er tillatt.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-147">This means that summary updates that have different invoice accounts and different currencies are not allowed.</span></span> <span data-ttu-id="4e6d5-148">Tilleggsparametere kan settes opp på siden Parametere for samleoppdatering, som er tilgjengelig fra siden Kundeparametere.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-148">Additional parameters can be set up in the Summary update parameters page which is accessible from the Accounts receivable parameters page.</span></span>  
8. <span data-ttu-id="4e6d5-149">Klikk rullegardinknappen i feltet Salgsordre for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-149">In the Sales order field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4e6d5-150">Velg ordrenummeret som du vil skal være samleordren, i listen.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-150">In the list, select the order number that you want to be the summary order.</span></span>
10. <span data-ttu-id="4e6d5-151">Klikk Ordne.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-151">Click Arrange.</span></span>
11. <span data-ttu-id="4e6d5-152">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-152">Click OK.</span></span>
12. <span data-ttu-id="4e6d5-153">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4e6d5-153">Click OK.</span></span>


