---
title: Opprette et purreforløp
description: Bruk denne oppgaveveiledningen til å opprette et purreforløp.
author: mikefalkner
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CollectionLetterCourse
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: db5264f6d8d7723ff01d13e99728c2bfebcb4515
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1567449"
---
# <a name="create-a-collection-letter-sequence"></a><span data-ttu-id="a842e-103">Opprette et purreforløp</span><span class="sxs-lookup"><span data-stu-id="a842e-103">Create a collection letter sequence</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a842e-104">Bruk denne oppgaveveiledningen til å opprette et purreforløp.</span><span class="sxs-lookup"><span data-stu-id="a842e-104">Use this task guide to create a collection letter sequence.</span></span> <span data-ttu-id="a842e-105">Denne oppgaven bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="a842e-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="a842e-106">Gå til Kreditt og innkreving > Oppsett > Definer purreforløp.</span><span class="sxs-lookup"><span data-stu-id="a842e-106">Go to Credit and collections > Setup > Set up collection letter sequence.</span></span>
2. <span data-ttu-id="a842e-107">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a842e-107">Click New.</span></span>
3. <span data-ttu-id="a842e-108">I Purreforløp-feltet angir du en sekvens-ID som representerer rekkefølgen.</span><span class="sxs-lookup"><span data-stu-id="a842e-108">In the Collection letter sequence field, enter a sequence ID that will represent the sequence.</span></span> <span data-ttu-id="a842e-109">Den brukes når du oppretter en posteringsprofil.</span><span class="sxs-lookup"><span data-stu-id="a842e-109">It will be used when you set up a posting profile.</span></span>
4. <span data-ttu-id="a842e-110">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a842e-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a842e-111">Betalingsbetingelsene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="a842e-111">The terms of payment is optional.</span></span> <span data-ttu-id="a842e-112">Hvis du angir en verdi her, bruker purregebyrfakturaen disse betalingsbetingelsene i stedet for betalingsbetingelsene som er lagret med kunden.</span><span class="sxs-lookup"><span data-stu-id="a842e-112">If you enter a value here, the collection letter fee invoice will use these terms of payment instead of the terms of payment stored with the customer.</span></span>  
5. <span data-ttu-id="a842e-113">I Purrekode-feltet velger du koden for den første purringen du vil sende.</span><span class="sxs-lookup"><span data-stu-id="a842e-113">In the collection letter code field, select the code for the first collection letter that you want to send.</span></span>
    * <span data-ttu-id="a842e-114">Den første purringen opprettes i henhold til forfallsdatoen på fakturaen, verdien du angir for respittperioden i Dager-feltet på denne linjen, og annen informasjon du angir på denne linjen.</span><span class="sxs-lookup"><span data-stu-id="a842e-114">The first collection letter is created according to the due date on the invoice, the value that you enter for the grace period in the Days field on this line, and other information that you enter on this line.</span></span>  
6. <span data-ttu-id="a842e-115">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a842e-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a842e-116">Valutaen for gebyret er som standard kundevalutaen.</span><span class="sxs-lookup"><span data-stu-id="a842e-116">The currency for the fee defaults to the customer currency.</span></span> <span data-ttu-id="a842e-117">Denne valutakoden kan være forskjellig fra fakturavalutaen.</span><span class="sxs-lookup"><span data-stu-id="a842e-117">This currency code can be different than the invoice currency.</span></span>  
7. <span data-ttu-id="a842e-118">Klikk Legg til for å legge til den neste purringen som skal sendes i sekvensen</span><span class="sxs-lookup"><span data-stu-id="a842e-118">Click Add to add the next collection letter that will be sent in the sequence</span></span>
    * <span data-ttu-id="a842e-119">I mange tilfeller er den første purringen bare en advarsel.</span><span class="sxs-lookup"><span data-stu-id="a842e-119">In many cases, the first collection letter is just a warning.</span></span> <span data-ttu-id="a842e-120">Du kan legge til gebyrer om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="a842e-120">You can add fees if needed.</span></span>  
8. <span data-ttu-id="a842e-121">I Purrekode-feltet velger du koden for den neste purringen som skal sendes i sekvensen.</span><span class="sxs-lookup"><span data-stu-id="a842e-121">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
9. <span data-ttu-id="a842e-122">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="a842e-122">In the Description field, type a value.</span></span>
10. <span data-ttu-id="a842e-123">Velg inntektskontoen som skal brukes for gebyrer, i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="a842e-123">In the main account field, select the revenue account that will be used for fees.</span></span>
11. <span data-ttu-id="a842e-124">Angi gebyret som skal belastes når denne purringen posteres.</span><span class="sxs-lookup"><span data-stu-id="a842e-124">Enter the fee that will be charged when this collection letter is posted.</span></span>
12. <span data-ttu-id="a842e-125">Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="a842e-125">In the Item sales tax group field, click the drop down button to open the lookup.</span></span>
    * <span data-ttu-id="a842e-126">Velg en mva-gruppe for vare hvis merverdiavgift må beregnes på gebyret.</span><span class="sxs-lookup"><span data-stu-id="a842e-126">Select an item sales tax group if sales taxes must be calculated on the fee.</span></span>  
13. <span data-ttu-id="a842e-127">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a842e-127">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="a842e-128">Angi den minste forfalte saldoen som kreves før å en purring sendes.</span><span class="sxs-lookup"><span data-stu-id="a842e-128">Enter the minimum overdue balance required before a collection letter is sent.</span></span>
15. <span data-ttu-id="a842e-129">Angi antall respittdager du vil tillate.</span><span class="sxs-lookup"><span data-stu-id="a842e-129">Enter the number of grace days that you will allow.</span></span>
    * <span data-ttu-id="a842e-130">Dette er antall dager etter forfallsdatoen som en purring kan genereres.</span><span class="sxs-lookup"><span data-stu-id="a842e-130">This is the number of days after the due date that a collection letter can be generated.</span></span> <span data-ttu-id="a842e-131">Forfallsdatoen som brukes i beregningen, avhenger av plasseringen av purringen i purreforløpet: ⦁ Respittperioden for purring 1 er relativ til forfallsdatoen på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="a842e-131">The due date that is used for the calculation depends on the position of the collection letter in the collection letter sequence:   ⦁    The grace period for collection letter 1 is relative to the due date on the invoice.</span></span>  <span data-ttu-id="a842e-132">⦁ Respittperioden for purringer 2 og høyere er relativ til datoen da forrige purring posteres eller skrives ut, avhengig av valget i feltet Oppdatere purrekode på siden Kundeparametere.</span><span class="sxs-lookup"><span data-stu-id="a842e-132">⦁ The grace period for collection letters 2 and higher is relative to the date that the previous collection letter is posted or printed, depending on the selection in the Update collection letter code field in the Accounts receivable parameters page.</span></span>  
16. <span data-ttu-id="a842e-133">Klikk Legg til for å legge til den siste purringen i sekvensen.</span><span class="sxs-lookup"><span data-stu-id="a842e-133">Click Add to add the last collection letter in the sequence.</span></span>
    * <span data-ttu-id="a842e-134">Du kan legge til opptil fem purrekoder for et purreforløp.</span><span class="sxs-lookup"><span data-stu-id="a842e-134">You can add up to five collection letter codes for a collection letter sequence.</span></span>  
17. <span data-ttu-id="a842e-135">I Purrekode-feltet velger du koden for den neste purringen som skal sendes i sekvensen.</span><span class="sxs-lookup"><span data-stu-id="a842e-135">In the collection letter code field, select the next collection letter that will be sent in the sequence.</span></span>
18. <span data-ttu-id="a842e-136">Skriv inn en verdi i Beskrivelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="a842e-136">In the Description field, type a value.</span></span>
19. <span data-ttu-id="a842e-137">Angi de ønskede verdiene i Hovedkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="a842e-137">In the Main account field, specify the desired values.</span></span>
20. <span data-ttu-id="a842e-138">Angi et tall i feltet Gebyr i valuta.</span><span class="sxs-lookup"><span data-stu-id="a842e-138">In the Fee in currency field, enter a number.</span></span>
21. <span data-ttu-id="a842e-139">Klikk rullegardinknappen i feltet Merverdiavgiftsgruppe for vare: for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="a842e-139">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
22. <span data-ttu-id="a842e-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a842e-140">In the list, click the link in the selected row.</span></span>
23. <span data-ttu-id="a842e-141">Angi et nummer i feltet Minste forfalte saldo.</span><span class="sxs-lookup"><span data-stu-id="a842e-141">In the Minimum overdue balance field, enter a number.</span></span>
24. <span data-ttu-id="a842e-142">Angi et tall i Dager-feltet.</span><span class="sxs-lookup"><span data-stu-id="a842e-142">In the Days field, enter a number.</span></span>
25. <span data-ttu-id="a842e-143">Merk av i avmerkingsboksen for å sperre kunden for videre leveranser og fakturering.</span><span class="sxs-lookup"><span data-stu-id="a842e-143">Select this check box to stop the customer from additional deliveries and invoicing.</span></span>
    * <span data-ttu-id="a842e-144">Hvis du vil oppheve blokkeringen av kontoen, velger du Nei i feltet Fakturering og levering på vent på Kunder-siden.</span><span class="sxs-lookup"><span data-stu-id="a842e-144">To unblock the account, select No in the Invoicing and delivery on hold field in the Customers page.</span></span>  
26. <span data-ttu-id="a842e-145">Utvid Merknad-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="a842e-145">Expand the Note fasttab.</span></span>
27. <span data-ttu-id="a842e-146">Angi teksten som skal vises på purringen for valgt purrekode.</span><span class="sxs-lookup"><span data-stu-id="a842e-146">Enter the text to appear on the collection letter for the selected collection letter code.</span></span>
    * <span data-ttu-id="a842e-147">Du kan oversette denne teksten til flere språk ved hjelp av Oversettelser-menyen over notat-boksen.</span><span class="sxs-lookup"><span data-stu-id="a842e-147">You can translate this text in to multiple languages using the Translations menu above the note box.</span></span>  

