---
title: Opprette en mal for fritekstfaktura
description: Denne fremgangsmåten beskriver hvordan du oppretter en mal for fritekstkundefaktura.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ee4fff7b148396faecef899c7a75365d3e1f47f3
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991171"
---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="d07bc-103">Opprette en mal for fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="d07bc-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d07bc-104">For denne gjennomgangen må du bruke demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="d07bc-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="d07bc-105">Denne fremgangsmåten er ment for brukeren som er ansvarlig for administrasjon og behandling av fakturaer for kunder.</span><span class="sxs-lookup"><span data-stu-id="d07bc-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="d07bc-106">Opprett en mal</span><span class="sxs-lookup"><span data-stu-id="d07bc-106">Create a template</span></span>

1. <span data-ttu-id="d07bc-107">Gå til Kunder > Fakturaer > Gjentakende fakturaer > Mallinjer for fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="d07bc-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="d07bc-108">Bruk dette skjemaet til å opprette maler for fritekstfaktura som kan inneholde fakturalinjer, tillegg, en regnskapsdistribusjonsmal og finanskontoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="d07bc-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="d07bc-109">Klikk Ny for å opprette en ny fritekstfakturamal.</span><span class="sxs-lookup"><span data-stu-id="d07bc-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="d07bc-110">Angi en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="d07bc-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="d07bc-111">"Malnavn" identifiserer unikt en mal for fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="d07bc-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="d07bc-112">To maler kan ikke ha samme malnavn.</span><span class="sxs-lookup"><span data-stu-id="d07bc-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="d07bc-113">Angi en beskrivelse av malen i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="d07bc-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="d07bc-114">Utvid kategorien Fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="d07bc-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="d07bc-115">I Beskrivelse-feltet angir du en beskrivelse av fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="d07bc-116">I Hovedkonto-feltet velger du en inntektskonto.</span><span class="sxs-lookup"><span data-stu-id="d07bc-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="d07bc-117">Du kan velge motposteringskontoen for en kundekreditt for det totale fakturabeløpet på Kundeposteringsprofiler-siden.</span><span class="sxs-lookup"><span data-stu-id="d07bc-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="d07bc-118">Klikk rullegardinknappen i feltet Mva-gruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d07bc-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d07bc-119">Mva-gruppen for gjeldende fakturalinje er standard mva-gruppen for kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="d07bc-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d07bc-121">I feltet Vareavgiftsgruppe velger du mva-gruppen for vare for den gjeldende fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="d07bc-122">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="d07bc-123">I Enhetspris-feltet angir eller viser du prisen per enhet for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="d07bc-124">Dette beløpet multipliseres med Antall-feltet for å bestemme fakturalinjebeløpet.</span><span class="sxs-lookup"><span data-stu-id="d07bc-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="d07bc-125">Legg til en ny linje i malen for fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="d07bc-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="d07bc-126">I Beskrivelse-feltet angir du en beskrivelse av fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="d07bc-127">I Hovedkonto-feltet velger du en inntektskonto.</span><span class="sxs-lookup"><span data-stu-id="d07bc-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="d07bc-128">Du kan velge motposteringskontoen for en kundekreditt for det totale fakturabeløpet på Kundeposteringsprofiler-siden.</span><span class="sxs-lookup"><span data-stu-id="d07bc-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="d07bc-129">Klikk rullegardinknappen i feltet Mva-gruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d07bc-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d07bc-130">Mva-gruppen for gjeldende fakturalinje er standard mva-gruppen for kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="d07bc-131">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="d07bc-132">Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="d07bc-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d07bc-133">Mva-gruppen for varesalg for den gjeldende fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="d07bc-134">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="d07bc-135">Angi eller vis antall enheter for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="d07bc-136">Dette nummeret multipliseres med verdien i Enhetspris-feltet for å bestemme fakturalinjebeløpet.</span><span class="sxs-lookup"><span data-stu-id="d07bc-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="d07bc-137">Angi eller vis prisen per enhet for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="d07bc-138">Dette beløpet multipliseres med verdien i Antall-feltet for å bestemme fakturalinjebeløpet.</span><span class="sxs-lookup"><span data-stu-id="d07bc-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="d07bc-139">Vis og endre regnskapsdistribusjonene for en enkelt linje og eventuelle underordnede linjer.</span><span class="sxs-lookup"><span data-stu-id="d07bc-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="d07bc-140">Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan omsetning, avgiften eller gebyrene skal gjøres rede for på en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="d07bc-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="d07bc-141">Oppdater regnskapsdistribusjonene for den valgte fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="d07bc-142">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="d07bc-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="d07bc-143">Lagre en fritekstfaktura som mal</span><span class="sxs-lookup"><span data-stu-id="d07bc-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="d07bc-144">Du kan også lagre en eksisterende fritekstfaktura som en mal.</span><span class="sxs-lookup"><span data-stu-id="d07bc-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="d07bc-145">Når du velger Lagre mal i kategorien Faktura, må du angi et navn og en beskrivelse for malen.</span><span class="sxs-lookup"><span data-stu-id="d07bc-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="d07bc-146">Hvis det finnes allerede en mal med det samme navnet, vises en melding om at en mal med dette navnet allerede finnes.</span><span class="sxs-lookup"><span data-stu-id="d07bc-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="d07bc-147">Du kan fremdeles klikke OK for å erstatte den.</span><span class="sxs-lookup"><span data-stu-id="d07bc-147">You can still click on Ok to replace it.</span></span> 
