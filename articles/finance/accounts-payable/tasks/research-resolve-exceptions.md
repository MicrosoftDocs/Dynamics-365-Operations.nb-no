---
title: Undersøke eller løse unntak
description: Leverandørfakturapolicyer kjøres når du posterer en leverandørfaktura ved hjelp av Leverandørfaktura-siden, og når du åpner siden for brudd på leverandørfakturapolicy.
author: abruer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 995d68f6224b6dfbb1928c907ad991b86fc47668
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4446339"
---
# <a name="research-or-resolve-exceptions"></a><span data-ttu-id="fc1fd-103">Undersøke eller løse unntak</span><span class="sxs-lookup"><span data-stu-id="fc1fd-103">Research or resolve exceptions</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="fc1fd-104">Leverandørfakturapolicyer kjøres når du posterer en leverandørfaktura ved hjelp av Leverandørfaktura-siden, og når du åpner siden for brudd på leverandørfakturapolicy.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-104">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="fc1fd-105">Du kan også konfigurere av arbeidsflyt for leverandørfaktura for å kjøre leverandørfakturapolicyer hver gang du sender en faktura til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-105">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

<span data-ttu-id="fc1fd-106">Leverandørfakturapolicyer gjelder ikke for fakturaer som ble opprettet i fakturaregisteret eller fakturajournalen.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-106">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span> 

<span data-ttu-id="fc1fd-107">Validering av fakturakontroll bruker ikke leverandørfakturapolicyer, men defineres i stedet på siden Leverandørparametere.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-107">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>

<span data-ttu-id="fc1fd-108">Denne registreringen bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-108">This recording uses the USMF demo company.</span></span> <span data-ttu-id="fc1fd-109">Rollen regnskapssjef leverandørreskontro eller regnskapssjef kan utføre disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-109">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="fc1fd-110">Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-110">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="fc1fd-111">Forberede oppretting av leverandørfakturapolicyer</span><span class="sxs-lookup"><span data-stu-id="fc1fd-111">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="fc1fd-112">Gå til Leverandører > Oppsett > Leverandørparametere.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-112">Go to Accounts payable > Setup > Accounts payable parameters.</span></span>
2. <span data-ttu-id="fc1fd-113">Klikk kategorien Fakturavalidering.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-113">Click the Invoice validation tab.</span></span>
3. <span data-ttu-id="fc1fd-114">Merk av eller fjern merket for Oppdater fakturahodestatus automatisk.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-114">Select or clear the Automatically update invoice header status check box.</span></span>
4. <span data-ttu-id="fc1fd-115">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-115">Click OK.</span></span>
5. <span data-ttu-id="fc1fd-116">Velg et alternativ i feltet Poster faktura med avvik.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-116">In the Post invoice with discrepancies field, select an option.</span></span>
6. <span data-ttu-id="fc1fd-117">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-117">Close the page.</span></span>
7. <span data-ttu-id="fc1fd-118">Gå til Leverandører > Policyoppsett > Leverandørfakturapolicyer.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-118">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
8. <span data-ttu-id="fc1fd-119">Klikk Parametere.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-119">Click Parameters.</span></span>
9. <span data-ttu-id="fc1fd-120">Klikk btnAdd.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-120">Click btnAdd.</span></span>
10. <span data-ttu-id="fc1fd-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-121">Close the page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="fc1fd-122">Opprette policyregeltyper for leverandørfakturaer</span><span class="sxs-lookup"><span data-stu-id="fc1fd-122">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="fc1fd-123">Gå til Leverandører > Policyoppsett > Policyregeltyper for leverandørfaktura.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-123">Go to Accounts payable > Policy setup > Vendor invoice policy rule types.</span></span>
2. <span data-ttu-id="fc1fd-124">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-124">Click New.</span></span>
3. <span data-ttu-id="fc1fd-125">Skriv inn en verdi i feltet Regelnavn.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-125">In the Rule name field, type a value.</span></span>
4. <span data-ttu-id="fc1fd-126">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-126">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fc1fd-127">Klikk rullegardinknappen i Spørringsnavn-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-127">In the Query name field, click the drop-down button to open the lookup.</span></span>
6. <span data-ttu-id="fc1fd-128">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-128">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="fc1fd-129">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-129">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="fc1fd-130">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-130">Click Save.</span></span>
9. <span data-ttu-id="fc1fd-131">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-131">Close the page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="fc1fd-132">Definere en leverandørfakturapolicy</span><span class="sxs-lookup"><span data-stu-id="fc1fd-132">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="fc1fd-133">Gå til Leverandører > Policyoppsett > Leverandørfakturapolicyer.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-133">Go to Accounts payable > Policy setup > Vendor invoice policies.</span></span>
2. <span data-ttu-id="fc1fd-134">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-134">Click New.</span></span>
3. <span data-ttu-id="fc1fd-135">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-135">In the Name field, type a value.</span></span>
4. <span data-ttu-id="fc1fd-136">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-136">In the Description field, type a value.</span></span>
5. <span data-ttu-id="fc1fd-137">Vis eller skjul delen Policyorganisasjoner.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-137">Expand or collapse the Policy organizations section.</span></span>
6. <span data-ttu-id="fc1fd-138">Velg "Contoso Entertainment System USA" i treet.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-138">In the tree, select 'Contoso Entertainment System USA'.</span></span>
7. <span data-ttu-id="fc1fd-139">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-139">Click Add.</span></span>
8. <span data-ttu-id="fc1fd-140">Vis eller skjul delen Policyregler.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-140">Expand or collapse the Policy rules section.</span></span>
9. <span data-ttu-id="fc1fd-141">Klikk Opprett policyregel.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-141">Click Create policy rule.</span></span>
10. <span data-ttu-id="fc1fd-142">Skriv inn en verdi i feltet Beskrivelse av policyregel.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-142">In the Policy rule description field, type a value.</span></span>
11. <span data-ttu-id="fc1fd-143">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-143">Click Filter.</span></span>
12. <span data-ttu-id="fc1fd-144">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-144">Click Add.</span></span>
13. <span data-ttu-id="fc1fd-145">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-145">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="fc1fd-146">Klikk rullegardinknappen i Tabell-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-146">In the Table field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="fc1fd-147">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-147">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="fc1fd-148">Klikk rullegardinknappen i feltet Avledet tabell for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-148">In the Derived table field, click the drop-down button to open the lookup.</span></span>
17. <span data-ttu-id="fc1fd-149">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-149">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="fc1fd-150">Klikk rullegardinknappen i Felt-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-150">In the Field field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="fc1fd-151">Skriv inn en verdi i Felt-feltet.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-151">In the Field field, type a value.</span></span>
20. <span data-ttu-id="fc1fd-152">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-152">Close the page.</span></span>
21. <span data-ttu-id="fc1fd-153">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-153">In the Criteria field, type a value.</span></span>
22. <span data-ttu-id="fc1fd-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-154">Click OK.</span></span>
23. <span data-ttu-id="fc1fd-155">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-155">Click OK.</span></span>
24. <span data-ttu-id="fc1fd-156">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-156">Close the page.</span></span>
25. <span data-ttu-id="fc1fd-157">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="fc1fd-157">Close the page.</span></span>

