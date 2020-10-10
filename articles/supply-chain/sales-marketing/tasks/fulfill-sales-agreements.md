---
title: Oppfylle salgsavtaler
description: Denne fremgangsmåten viser hvordan du kan oppfylle en salgsavtale ved å knytte salgsordrer til den.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreement, SalesAgreementGenerateReleaseOrder, SalesTableListPage, SalesTable, AgreementLine, SalesCreateOrder,  SalesEditLines, SalesAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b489add43bb523a7684115b942395b0d830f3c4a
ms.sourcegitcommit: 54da65a7da0efd4f0d9760c5b14ff785b28751c4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2020
ms.locfileid: "3830215"
---
# <a name="fulfill-sales-agreements"></a><span data-ttu-id="890dc-103">Oppfylle salgsavtaler</span><span class="sxs-lookup"><span data-stu-id="890dc-103">Fulfill sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="890dc-104">Denne fremgangsmåten viser hvordan du kan oppfylle en salgsavtale ved å knytte salgsordrer til den.</span><span class="sxs-lookup"><span data-stu-id="890dc-104">This procedure shows you how to fulfill a sales agreement by associating sales orders with it.</span></span> <span data-ttu-id="890dc-105">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="890dc-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="890dc-106">Før du starter denne veiledningen kontroller at du har en gyldig salgsavtale av typen "Produktverdiforpliktelse".</span><span class="sxs-lookup"><span data-stu-id="890dc-106">Before starting this guide, make sure you have an effective sales agreement of type "Product value commitment".</span></span> <span data-ttu-id="890dc-107">Du kan også kjøre oppgaveveiledningen kalt "Opprette salgsavtaler".</span><span class="sxs-lookup"><span data-stu-id="890dc-107">Alternatively, you can run the task guide called "Create sales agreements".</span></span>  




## <a name="release-a-sales-order-from-the-agreement"></a><span data-ttu-id="890dc-108">Frigi en salgsordre fra avtalen</span><span class="sxs-lookup"><span data-stu-id="890dc-108">Release a sales order from the agreement</span></span>
1. <span data-ttu-id="890dc-109">Gå til Salg og markedsføring > Salgsavtaler > Salgsavtaler.</span><span class="sxs-lookup"><span data-stu-id="890dc-109">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="890dc-110">Åpne avtalen som du vil frigi ordren mot, i listen.</span><span class="sxs-lookup"><span data-stu-id="890dc-110">In the list, open the agreement against which you want to release the order.</span></span>
3. <span data-ttu-id="890dc-111">Klikk Salgsavtale i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="890dc-111">On the Action Pane, click Sales agreement.</span></span>
4. <span data-ttu-id="890dc-112">Klikk Frigivelsesordre.</span><span class="sxs-lookup"><span data-stu-id="890dc-112">Click Release order.</span></span>
    * <span data-ttu-id="890dc-113">Som teksten øverst på siden Opprett frigivelsesordre påpeker vil detaljene som kreves for salgsordrelinjene variere avhengig av om avtalen er antalls- eller verdibasert.</span><span class="sxs-lookup"><span data-stu-id="890dc-113">As the text on top of the  Create release order page points out, the details required for the sales order lines will differ depending on whether the agreement is quantity- or value-based.</span></span>  
    * <span data-ttu-id="890dc-114">Avtalen i denne veiledningen er av typen "Produktverdiforpliktelse".</span><span class="sxs-lookup"><span data-stu-id="890dc-114">The agreement in this guide is of type "Product value commitment".</span></span> <span data-ttu-id="890dc-115">Det er derfor seksjonen Linjer på denne siden er tom.</span><span class="sxs-lookup"><span data-stu-id="890dc-115">This is why the Lines section of this page is blank.</span></span> <span data-ttu-id="890dc-116">Hvis forpliktelsen var basert på antallet, ville linjeinformasjonen bli kopiert fra avtalen.</span><span class="sxs-lookup"><span data-stu-id="890dc-116">If the commitment was based on quantity, the line information would be copied from the agreement.</span></span>  
5. <span data-ttu-id="890dc-117">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="890dc-117">Click Create.</span></span>
    * <span data-ttu-id="890dc-118">Meldingen forteller deg at en salgsordre er blitt opprettet.</span><span class="sxs-lookup"><span data-stu-id="890dc-118">The message informs you that a sales order has been created.</span></span> <span data-ttu-id="890dc-119">Ettersom bestillingen ikke inneholder noen linjer, må du legge til ordrelinjedetaljer for å fullføre frigivelsesprosessen.</span><span class="sxs-lookup"><span data-stu-id="890dc-119">Since the order does not contain any lines, you must add order line details to complete the release process.</span></span>   
6. <span data-ttu-id="890dc-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="890dc-120">Close the page.</span></span>
7. <span data-ttu-id="890dc-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="890dc-121">Close the page.</span></span>
8. <span data-ttu-id="890dc-122">Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="890dc-122">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
9. <span data-ttu-id="890dc-123">Finn og åpne ordren som ble opprettet som et resultat av ordrefrigivelsen i den forrige oppgaven, i listen.</span><span class="sxs-lookup"><span data-stu-id="890dc-123">In the list, find and open the order that was created as the result of the order release in the previous task.</span></span>
10. <span data-ttu-id="890dc-124">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="890dc-124">Click Add line.</span></span>
11. <span data-ttu-id="890dc-125">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="890dc-125">In the Item number field, click the drop-down button to open the lookup.</span></span>
12. <span data-ttu-id="890dc-126">I Varenummer-feltet skriver du inn eller velger varen som er angitt på den tilknyttede salgsavtalen.</span><span class="sxs-lookup"><span data-stu-id="890dc-126">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
13. <span data-ttu-id="890dc-127">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="890dc-127">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="890dc-128">Pass på at du angir et antall som bringer nettobeløpet under verdien for den tilknyttede salgsavtalen.</span><span class="sxs-lookup"><span data-stu-id="890dc-128">Make sure that you enter a quantity that brings the Net amount under the value of the associated sales agreement.</span></span>  
    * <span data-ttu-id="890dc-129">Legg merke til at fordi salgsordren er knyttet til avtalen, brukes den avtalte rabattprosenten på ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="890dc-129">Notice that because the sales order is linked to the agreement, the negotiated discount percent is applied to the order line.</span></span>  
14. <span data-ttu-id="890dc-130">Klikk Oppdater linje.</span><span class="sxs-lookup"><span data-stu-id="890dc-130">Click Update line.</span></span>
15. <span data-ttu-id="890dc-131">Klikk Vedlagt.</span><span class="sxs-lookup"><span data-stu-id="890dc-131">Click Attached.</span></span>
    * <span data-ttu-id="890dc-132">Siden Tilknyttet avtale viser ID-en og betingelsene i avtalen som linjen er frigitt fra.</span><span class="sxs-lookup"><span data-stu-id="890dc-132">The Attached agreement page shows the ID and terms of the agreement from which the line is released.</span></span>  
16. <span data-ttu-id="890dc-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="890dc-133">Close the page.</span></span>
17. <span data-ttu-id="890dc-134">Klikk Generelt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="890dc-134">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="890dc-135">Klikk Tilknyttet salgsavtalelinje.</span><span class="sxs-lookup"><span data-stu-id="890dc-135">Click Attached sales agreement.</span></span>
19. <span data-ttu-id="890dc-136">Vis seksjonen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="890dc-136">Expand the Line details section.</span></span>
20. <span data-ttu-id="890dc-137">Klikk kategorien Oppfyllelse.</span><span class="sxs-lookup"><span data-stu-id="890dc-137">Click the Fulfillment tab.</span></span>
    * <span data-ttu-id="890dc-138">Kategorien Oppfyllelse viser et sammendrag av alle salgsordrelinjer som er knyttet til denne forpliktelsen, og oppfyllelsestilstanden, i tillegg til beløpet eller antallet som ennå ikke er frigitt.</span><span class="sxs-lookup"><span data-stu-id="890dc-138">The Fulfillment tab shows a summary of all the sales order lines that are associated with this commitment, and their fulfillment state, as well as the amount or quantity that has not yet been released.</span></span>   
21. <span data-ttu-id="890dc-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="890dc-139">Close the page.</span></span>
22. <span data-ttu-id="890dc-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="890dc-140">Close the page.</span></span>
23. <span data-ttu-id="890dc-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="890dc-141">Close the page.</span></span>

## <a name="apply-sales-agreement-in-the-order-process"></a><span data-ttu-id="890dc-142">Bruke salgsavtale i ordreprosessen</span><span class="sxs-lookup"><span data-stu-id="890dc-142">Apply sales agreement in the order process</span></span>
1. <span data-ttu-id="890dc-143">Gå til Salg og markedsføring > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="890dc-143">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="890dc-144">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="890dc-144">Click New.</span></span>
3. <span data-ttu-id="890dc-145">Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="890dc-145">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="890dc-146">Finn og velg kunden som er angitt i salgsavtalen, i listen.</span><span class="sxs-lookup"><span data-stu-id="890dc-146">In the list, find and select the customer specified on the sales agreement.</span></span>
5. <span data-ttu-id="890dc-147">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="890dc-147">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="890dc-148">Utvid delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="890dc-148">Expand the General section.</span></span>
7. <span data-ttu-id="890dc-149">Klikk rullegardinknappen i feltet Salgsavtale-ID for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="890dc-149">In the Sales agreement ID field, click the drop-down button to open the lookup.</span></span>
8. <span data-ttu-id="890dc-150">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="890dc-150">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="890dc-151">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="890dc-151">Click Yes.</span></span>
10. <span data-ttu-id="890dc-152">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="890dc-152">Click OK.</span></span>
11. <span data-ttu-id="890dc-153">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="890dc-153">In the list, mark the selected row.</span></span>
12. <span data-ttu-id="890dc-154">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="890dc-154">In the Item number field, click the drop-down button to open the lookup.</span></span>
13. <span data-ttu-id="890dc-155">I Varenummer-feltet skriver du inn eller velger varen som er angitt på den tilknyttede salgsavtalen.</span><span class="sxs-lookup"><span data-stu-id="890dc-155">In the Item number field, type or select the item that is specified on the associated sales agreement.</span></span>
14. <span data-ttu-id="890dc-156">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="890dc-156">In the list, click the link in the selected row.</span></span>
15. <span data-ttu-id="890dc-157">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="890dc-157">Click Save.</span></span>
16. <span data-ttu-id="890dc-158">Klikk Plukk og pakk i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="890dc-158">On the Action Pane, click Pick and pack.</span></span>
17. <span data-ttu-id="890dc-159">Klikk Poster følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="890dc-159">Click Post packing slip.</span></span>
18. <span data-ttu-id="890dc-160">Utvid seksjonen Parametere.</span><span class="sxs-lookup"><span data-stu-id="890dc-160">Expand the Parameters section.</span></span>
19. <span data-ttu-id="890dc-161">Velg Ja i feltet Postering.</span><span class="sxs-lookup"><span data-stu-id="890dc-161">Select Yes in the Posting field.</span></span>
20. <span data-ttu-id="890dc-162">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="890dc-162">Click OK.</span></span>
21. <span data-ttu-id="890dc-163">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="890dc-163">Click OK.</span></span>
22. <span data-ttu-id="890dc-164">Klikk Generelt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="890dc-164">On the Action Pane, click General.</span></span>
23. <span data-ttu-id="890dc-165">Klikk Tilknyttet salgsavtalelinje.</span><span class="sxs-lookup"><span data-stu-id="890dc-165">Click Attached sales agreement.</span></span>
24. <span data-ttu-id="890dc-166">Klikk kategorien Oppfyllelse.</span><span class="sxs-lookup"><span data-stu-id="890dc-166">Click the Fulfillment tab.</span></span>

