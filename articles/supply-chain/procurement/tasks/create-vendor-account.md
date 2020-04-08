---
title: Opprette en leverandørkonto
description: Denne fremgangsmåten viser hvordan du oppretter en leverandørkonto, og legger til en adresse og kontaktinformasjon.
author: mkirknel
manager: AnnBe
ms.date: 06/26/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, LogisticsPostalAddressGrid, DirPartyLookup, LogisticsPostalAddress, SysLookupMultiSelectGrid
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ba585a9bb1a296bbf7181530e151d737bfa22fc2
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149602"
---
# <a name="create-a-vendor-account"></a><span data-ttu-id="d3bdd-103">Opprette en leverandørkonto</span><span class="sxs-lookup"><span data-stu-id="d3bdd-103">Create a vendor account</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d3bdd-104">Denne fremgangsmåten viser hvordan du oppretter en leverandørkonto, og legger til en adresse og kontaktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-104">This procedure shows how to create a vendor account, and add an address and contact information.</span></span> <span data-ttu-id="d3bdd-105">Fremgangsmåten viser ikke hvordan du fyller ut alle felt for innkjøp og finansielle formål.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-105">The procedure does not show how to populate all fields for purchasing and financial purposes.</span></span> <span data-ttu-id="d3bdd-106">Hvis du vil vite mer om disse feltene, kan du lese feltbeskrivelsene.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-106">To learn more about those fields, please read the field descriptions.</span></span> <span data-ttu-id="d3bdd-107">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-107">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="d3bdd-108">Leverandørkontoer opprettes vanligvis av en innkjøpsansvarlig eller kundepersonale.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-108">Vendor accounts are typically created by a procurement professional or accounts receivable personnel.</span></span>


## <a name="create-a-vendor-account"></a><span data-ttu-id="d3bdd-109">Opprette en leverandørkonto</span><span class="sxs-lookup"><span data-stu-id="d3bdd-109">Create a vendor account</span></span>
1. <span data-ttu-id="d3bdd-110">Gå til **navigasjonsruten > Moduler > Innkjøp og leverandører > Leverandører > Alle leverandører**.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-110">Go to **Navigation pane > Modules > Procurement and sourcing > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="d3bdd-111">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-111">Click **New**.</span></span>
3. <span data-ttu-id="d3bdd-112">Angi en verdi i **Leverandørkonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-112">In the **Vendor account** field, type a value.</span></span>
    - <span data-ttu-id="d3bdd-113">Verdien kan fylles ut automatisk.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-113">The value may be populated automatically.</span></span> <span data-ttu-id="d3bdd-114">I så fall kan du hoppe over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-114">If so, you can skip this step.</span></span>  
    - <span data-ttu-id="d3bdd-115">Du kan opprette leverandørkontoer for en person eller organisasjon.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-115">You can create vendor accounts for a person or organization.</span></span> <span data-ttu-id="d3bdd-116">Dette påvirker hvilke felt som er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-116">This will affect which fields are available.</span></span> <span data-ttu-id="d3bdd-117">I dette eksemplet skal vi opprette en leverandørkonto for en organisasjon.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-117">In this example, we'll create a vendor account for an organization.</span></span>   
4. <span data-ttu-id="d3bdd-118">Angi eller velg en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-118">In the **Name** field, enter or select a value.</span></span> <span data-ttu-id="d3bdd-119">Hvis leverandøren er en allerede registrert part i systemet, kan du bruke rullegardinlisten og velge dem i dette feltet, og den nye leverandørkontoen arver adresseinformasjonen og kontaktinformasjon som allerede er registrert.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-119">If your vendor is an already a registered party in your system you can use drop down and select them in this field and the new vendor account will inherit the address and contact information that's already registered.</span></span>
5. <span data-ttu-id="d3bdd-120">Angi eller velg en verdi i **Gruppe**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-120">In the **Group** field, enter or select a value.</span></span> <span data-ttu-id="d3bdd-121">Leverandørgruppen brukes til å gruppere leverandører som har én av følgende parametere felles: Betalingsbetingelser, avregn termin, finanskontoer for lagerpostering, inkludert mva-gruppen, standard finanskontoer, produktfilterkoder eller konfigurasjon av forsyningsprognose.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-121">The vendor group is used to group vendors that have any of the following parameters in common: Terms of payment, settle period, inventory posting ledger accounts – including the sales tax group, default ledger accounts, product filter codes, or supply forecast configuration.</span></span>
6. <span data-ttu-id="d3bdd-122">Angi et tall i **Antall ansatte**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-122">In the **Number of employees** field, enter a number.</span></span>
7. <span data-ttu-id="d3bdd-123">Skriv inn en verdi i feltet **Organisasjonsnummer**.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-123">In the **Organization number** field, type a value.</span></span>

## <a name="add-an-address"></a><span data-ttu-id="d3bdd-124">Legge til en adresse</span><span class="sxs-lookup"><span data-stu-id="d3bdd-124">Add an address</span></span>
1. <span data-ttu-id="d3bdd-125">Vis delen **Adresser**.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-125">Expand the **Addresses** section.</span></span>
2. <span data-ttu-id="d3bdd-126">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-126">Click **Add**.</span></span>
3. <span data-ttu-id="d3bdd-127">Angi eller velg en verdi i **Formål**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-127">In the **Purpose** field, enter or select a value.</span></span> <span data-ttu-id="d3bdd-128">Du kan velge ett eller flere formål.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-128">You can select one or more purposes.</span></span> <span data-ttu-id="d3bdd-129">Disse brukes til å velge den riktige adressen for en angitt formål.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-129">These are used to select the correct address for a given purpose.</span></span> <span data-ttu-id="d3bdd-130">Hvis formålet for eksempel er "Faktura", brukes denne adressen når du sender fakturaer.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-130">For example, if the purpose is "Invoice" that address will be used when you send invoices.</span></span>
4. <span data-ttu-id="d3bdd-131">Skriv inn en verdi i feltet **Navn eller beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-131">In the **Name or description** field, type a value.</span></span>
5. <span data-ttu-id="d3bdd-132">Angi eller velg en verdi i **Land/område**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-132">In the **Country/region** field, enter or select a value.</span></span> <span data-ttu-id="d3bdd-133">Angi adressedetaljene.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-133">Enter the address details.</span></span> <span data-ttu-id="d3bdd-134">Landet/regionen du valgte, bestemmer feltene som du ser, i henhold til adresseformatet for landet/regionen.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-134">The country/region that you selected will determine the fields you are presented with, corresponding to the address format for the country/region.</span></span> 
6. <span data-ttu-id="d3bdd-135">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-135">Click **OK**.</span></span>

## <a name="add-contact-information"></a><span data-ttu-id="d3bdd-136">Legge til kontaktinformasjon</span><span class="sxs-lookup"><span data-stu-id="d3bdd-136">Add contact information</span></span>
1. <span data-ttu-id="d3bdd-137">Vis delen **Kontaktinformasjon**.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-137">Expand the **Contact information** section.</span></span>
2. <span data-ttu-id="d3bdd-138">Klikk **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-138">Click **Add**.</span></span>
3. <span data-ttu-id="d3bdd-139">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-139">In the **Description** field, type a value.</span></span>
4. <span data-ttu-id="d3bdd-140">Velg et alternativ i **Type**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-140">In the **Type** field, select an option.</span></span>
5. <span data-ttu-id="d3bdd-141">Angi en verdi i feltet **Kontaktnummer/-adresse**.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-141">In the **Contact number/address** field, type a value.</span></span> <span data-ttu-id="d3bdd-142">Du kan merke av for Primær hvis dette er hovedkontakten.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-142">You can select the Primary check box if this is the primary contact.</span></span>  
6. <span data-ttu-id="d3bdd-143">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-143">Click **Save**.</span></span>
7. <span data-ttu-id="d3bdd-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-144">Close the page.</span></span>
8. <span data-ttu-id="d3bdd-145">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d3bdd-145">Close the page.</span></span>

