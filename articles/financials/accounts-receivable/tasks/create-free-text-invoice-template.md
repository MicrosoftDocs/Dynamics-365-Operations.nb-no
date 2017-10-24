--- 
title: Opprette en mal for fritekstfaktura
description: Denne registreringen bruker demonstrasjonsfirmaet USMF.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9c9811b348d81cd735c5b75ca48e0a56a8d52be
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="fd147-103">Opprette en mal for fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="fd147-103">Create a free text invoice template</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="fd147-104">Denne registreringen bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="fd147-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="fd147-105">Registreringen er ment for brukeren som er ansvarlig for administrasjon og behandling av fakturaer for kunder.</span><span class="sxs-lookup"><span data-stu-id="fd147-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="fd147-106">Gå til Kunder > Fakturaer > Gjentakende fakturaer > Mallinjer for fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="fd147-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="fd147-107">Bruk dette skjemaet til å opprette maler for fritekstfaktura som kan inneholde fakturalinjer, tillegg, en regnskapsdistribusjonsmal og finanskontoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="fd147-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="fd147-108">Klikk Ny for å opprette en ny fritekstfakturamal.</span><span class="sxs-lookup"><span data-stu-id="fd147-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="fd147-109">Angi en verdi i Malnavn-feltet.</span><span class="sxs-lookup"><span data-stu-id="fd147-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="fd147-110">"Malnavn" identifiserer unikt en mal for fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="fd147-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="fd147-111">To maler kan ikke ha samme malnavn.</span><span class="sxs-lookup"><span data-stu-id="fd147-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="fd147-112">Angi en beskrivelse av malen i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="fd147-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="fd147-113">Utvid kategorien Fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="fd147-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="fd147-114">I Beskrivelse-feltet angir du en beskrivelse av fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="fd147-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="fd147-115">I Hovedkonto-feltet velger du en inntektskonto.</span><span class="sxs-lookup"><span data-stu-id="fd147-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="fd147-116">Du kan velge motposteringskontoen for en kundekreditt for det totale fakturabeløpet på Kundeposteringsprofiler-siden.</span><span class="sxs-lookup"><span data-stu-id="fd147-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="fd147-117">Klikk rullegardinknappen i feltet Mva-gruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fd147-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="fd147-118">Mva-gruppen for gjeldende fakturalinje er standard mva-gruppen for kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="fd147-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="fd147-119">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fd147-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="fd147-120">I feltet Vareavgiftsgruppe velger du mva-gruppen for vare for den gjeldende fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="fd147-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="fd147-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fd147-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="fd147-122">I Enhetspris-feltet angir eller viser du prisen per enhet for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="fd147-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="fd147-123">Dette beløpet multipliseres med Antall-feltet for å bestemme fakturalinjebeløpet.</span><span class="sxs-lookup"><span data-stu-id="fd147-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="fd147-124">Legg til en ny linje i malen for fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="fd147-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="fd147-125">I Beskrivelse-feltet angir du en beskrivelse av fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="fd147-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="fd147-126">I Hovedkonto-feltet velger du en inntektskonto.</span><span class="sxs-lookup"><span data-stu-id="fd147-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="fd147-127">Du kan velge motposteringskontoen for en kundekreditt for det totale fakturabeløpet på Kundeposteringsprofiler-siden.</span><span class="sxs-lookup"><span data-stu-id="fd147-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="fd147-128">Klikk rullegardinknappen i feltet Mva-gruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fd147-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="fd147-129">Mva-gruppen for gjeldende fakturalinje er standard mva-gruppen for kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="fd147-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="fd147-130">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fd147-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="fd147-131">Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fd147-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="fd147-132">Mva-gruppen for varesalg for den gjeldende fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="fd147-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="fd147-133">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fd147-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="fd147-134">Angi eller vis antall enheter for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="fd147-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="fd147-135">Dette nummeret multipliseres med verdien i Enhetspris-feltet for å bestemme fakturalinjebeløpet.</span><span class="sxs-lookup"><span data-stu-id="fd147-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="fd147-136">Angi eller vis prisen per enhet for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="fd147-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="fd147-137">Dette beløpet multipliseres med verdien i Antall-feltet for å bestemme fakturalinjebeløpet.</span><span class="sxs-lookup"><span data-stu-id="fd147-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="fd147-138">Vis og endre regnskapsdistribusjonene for en enkelt linje og eventuelle underordnede linjer.</span><span class="sxs-lookup"><span data-stu-id="fd147-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="fd147-139">Regnskapsdistribusjoner brukes til å definere hvordan beløp skal gjøres rede for, for eksempel hvordan omsetning, avgiften eller gebyrene skal gjøres rede for på en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="fd147-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="fd147-140">Oppdater regnskapsdistribusjonene for den valgte fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="fd147-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="fd147-141">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="fd147-141">Click Close.</span></span>


