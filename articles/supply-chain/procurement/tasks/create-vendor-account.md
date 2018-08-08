--- 
title: "Opprette en leverandørkonto"
description: "Denne fremgangsmåten viser hvordan du oppretter en leverandørkonto, og legger til en adresse og kontaktinformasjon."
author: mkirknel
manager: AnnBe
ms.date: 06/06/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: e978b7c0add7b262ee7d3dbcf1da8648350ea8f5
ms.contentlocale: nb-no
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-vendor-account"></a><span data-ttu-id="631d0-103">Opprette en leverandørkonto</span><span class="sxs-lookup"><span data-stu-id="631d0-103">Create a vendor account</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="631d0-104">Denne fremgangsmåten viser hvordan du oppretter en leverandørkonto, og legger til en adresse og kontaktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="631d0-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="631d0-105">Fremgangsmåten viser ikke hvordan du fyller ut alle felt for innkjøp og finansielle formål.</span><span class="sxs-lookup"><span data-stu-id="631d0-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="631d0-106">Hvis du vil vite mer om disse feltene, kan du lese feltbeskrivelsene.</span><span class="sxs-lookup"><span data-stu-id="631d0-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="631d0-107">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="631d0-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="631d0-108">Leverandørkontoer opprettes vanligvis av en innkjøpsansvarlig eller kundepersonale.</span><span class="sxs-lookup"><span data-stu-id="631d0-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="631d0-109">Opprette en leverandørkonto</span><span class="sxs-lookup"><span data-stu-id="631d0-109">Create a vendor account</span></span>
1. <span data-ttu-id="631d0-110">Gå til Innkjøp og leverandører > Leverandører > Alle leverandører.</span><span class="sxs-lookup"><span data-stu-id="631d0-110">Go to Procurement and sourcing > Vendors > All vendors.</span></span>
2. <span data-ttu-id="631d0-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="631d0-111">Click New.</span></span>
3. <span data-ttu-id="631d0-112">Angi en verdi i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="631d0-112">In the Vendor account field, type a value.</span></span>
    * <span data-ttu-id="631d0-113">Verdien kan fylles ut automatisk.</span><span class="sxs-lookup"><span data-stu-id="631d0-113">The value may be populated automatically.</span></span> <span data-ttu-id="631d0-114">I så fall kan du hoppe over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="631d0-114">If so, you can skip this step.</span></span>  
    * <span data-ttu-id="631d0-115">Du kan opprette leverandørkontoer for en person eller organisasjon.</span><span class="sxs-lookup"><span data-stu-id="631d0-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="631d0-116">Dette påvirker hvilke felt som er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="631d0-116">This will affect which fields are available.</span></span> <span data-ttu-id="631d0-117">I dette eksemplet skal vi opprette en leverandørkonto for en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="631d0-117">In this example, we’ll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="631d0-118">Angi eller velg en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="631d0-118">In the Name field, enter or select a value.</span></span>
    * <span data-ttu-id="631d0-119">Hvis leverandøren er en allerede registrert part i systemet, kan du bruke rullegardinlisten og velger dem i dette feltet, og den nye leverandørkontoen arver adresseinformasjonen og kontaktinformasjon som allerede er registrert.</span><span class="sxs-lookup"><span data-stu-id="631d0-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that’s already registered.</span></span>  
5. <span data-ttu-id="631d0-120">Angi eller velg en verdi i Gruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="631d0-120">In the Group field, enter or select a value.</span></span>
    * <span data-ttu-id="631d0-121">Leverandørgruppen brukes til å gruppere leverandører som har én av følgende parametere felles: Betalingsbetingelser; avregn termin; finanskontoer for lagerpostering, inkludert mva-gruppen; standard finanskontoer; produktfilterkoder eller konfigurasjon av forsyningsprognose.</span><span class="sxs-lookup"><span data-stu-id="631d0-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment , settle period,  inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>  
6. <span data-ttu-id="631d0-122">Angi et tall i Antall ansatte-feltet.</span><span class="sxs-lookup"><span data-stu-id="631d0-122">In the Number of employees field, enter a number.</span></span>
7. <span data-ttu-id="631d0-123">Skriv inn en verdi i feltet Organisasjonsnummer.</span><span class="sxs-lookup"><span data-stu-id="631d0-123">In the Organization number field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="631d0-124">Legge til en adresse</span><span class="sxs-lookup"><span data-stu-id="631d0-124">Add an address</span></span>
1. <span data-ttu-id="631d0-125">Utvid seksjonen Adresser.</span><span class="sxs-lookup"><span data-stu-id="631d0-125">Expand the Addresses section.</span></span>
2. <span data-ttu-id="631d0-126">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="631d0-126">Click Add.</span></span>
3. <span data-ttu-id="631d0-127">Angi eller velg en verdi i Formål-feltet.</span><span class="sxs-lookup"><span data-stu-id="631d0-127">In the Purpose field, enter or select a value.</span></span>
    * <span data-ttu-id="631d0-128">Du kan velge ett eller flere formål.</span><span class="sxs-lookup"><span data-stu-id="631d0-128">You can select one or more purposes.</span></span> <span data-ttu-id="631d0-129">Disse brukes til å velge den riktige adressen for en angitt formål.</span><span class="sxs-lookup"><span data-stu-id="631d0-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="631d0-130">Hvis formålet for eksempel er "Faktura", brukes denne adressen når du sender fakturaer.</span><span class="sxs-lookup"><span data-stu-id="631d0-130">For example, if the purpose is “Invoice” that address will be used when you send invoices.</span></span>  
4. <span data-ttu-id="631d0-131">Skriv inn en verdi i feltet Navn eller beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="631d0-131">In the Name or description field, type a value.</span></span>
5. <span data-ttu-id="631d0-132">Angi eller velg en verdi i Land/område-feltet.</span><span class="sxs-lookup"><span data-stu-id="631d0-132">In the Country/region field, enter or select a value.</span></span>
    * <span data-ttu-id="631d0-133">Angi adressedetaljene.</span><span class="sxs-lookup"><span data-stu-id="631d0-133">Enter the address details.</span></span> <span data-ttu-id="631d0-134">Landet/regionen du valgte, bestemmer feltene som du ser, i henhold til adresseformatet for landet/regionen.</span><span class="sxs-lookup"><span data-stu-id="631d0-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span>   
6. <span data-ttu-id="631d0-135">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="631d0-135">Click OK.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="631d0-136">Legge til kontaktinformasjon</span><span class="sxs-lookup"><span data-stu-id="631d0-136">Add contact information</span></span>
1. <span data-ttu-id="631d0-137">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="631d0-137">Click Add.</span></span>
2. <span data-ttu-id="631d0-138">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="631d0-138">In the Description field, type a value.</span></span>
3. <span data-ttu-id="631d0-139">Velg et alternativ i Type-feltet.</span><span class="sxs-lookup"><span data-stu-id="631d0-139">In the Type field, select an option.</span></span>
4. <span data-ttu-id="631d0-140">Angi en verdi i feltet Kontaktnummer/-adresse.</span><span class="sxs-lookup"><span data-stu-id="631d0-140">In the Contact number/address field, type a value.</span></span>
    * <span data-ttu-id="631d0-141">Du kan merke av for Primær hvis dette er hovedkontakten.</span><span class="sxs-lookup"><span data-stu-id="631d0-141">You can select the Primary check box if this is the primary contact.</span></span>  
5. <span data-ttu-id="631d0-142">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="631d0-142">Click Save.</span></span>
6. <span data-ttu-id="631d0-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="631d0-143">Close the page.</span></span>
7. <span data-ttu-id="631d0-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="631d0-144">Close the page.</span></span>


