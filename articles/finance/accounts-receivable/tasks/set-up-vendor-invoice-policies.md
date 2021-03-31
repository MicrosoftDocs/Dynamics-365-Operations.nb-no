---
title: Definere leverandørfakturapolicyer
description: Dette emnet forklarer hvordan du konfigurerer leverandørfakturapolicyer.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendParameters,  SysPolicyListPage, SysPolicyParameters, SysPolicySourceDocumentRuleType, SysPolicy, SysPolicySourceDocumentRule, SysQueryForm, SysQueryTableLookUp, SysQueryPrefixLookUp, SysQueryFieldLookUp
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 678ef8f0b7df00aec615af26cbcadec984331060
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5220065"
---
# <a name="set-up-vendor-invoice-policies"></a><span data-ttu-id="65cb3-103">Definere leverandørfakturapolicyer</span><span class="sxs-lookup"><span data-stu-id="65cb3-103">Set up vendor invoice policies</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="65cb3-104">Dette emnet forklarer hvordan du konfigurerer leverandørfakturapolicyer.</span><span class="sxs-lookup"><span data-stu-id="65cb3-104">This topic explains how to set up vendor invoice policies.</span></span> <span data-ttu-id="65cb3-105">Leverandørfakturapolicyer kjøres når du posterer en leverandørfaktura ved hjelp av Leverandørfaktura-siden, og når du åpner siden for brudd på leverandørfakturapolicy.</span><span class="sxs-lookup"><span data-stu-id="65cb3-105">Vendor invoice policies are run when you post a vendor invoice by using the Vendor invoice page and when you open the vendor invoice Policy violations page.</span></span> <span data-ttu-id="65cb3-106">Du kan også konfigurere av arbeidsflyt for leverandørfaktura for å kjøre leverandørfakturapolicyer hver gang du sender en faktura til arbeidsflyten.</span><span class="sxs-lookup"><span data-stu-id="65cb3-106">You can also configure the vendor invoice workflow to run vendor invoice policies every time that you submit an invoice to workflow.</span></span> 

- <span data-ttu-id="65cb3-107">Leverandørfakturapolicyer gjelder ikke for fakturaer som ble opprettet i fakturaregisteret eller fakturajournalen.</span><span class="sxs-lookup"><span data-stu-id="65cb3-107">Vendor invoice policies do not apply to invoices that were created in the invoice register or invoice journal.</span></span>  
- <span data-ttu-id="65cb3-108">Validering av fakturakontroll bruker ikke leverandørfakturapolicyer, men defineres i stedet på siden Leverandørparametere.</span><span class="sxs-lookup"><span data-stu-id="65cb3-108">Invoice matching validation does not use vendor invoice policies, but is instead set up in the Accounts payable parameters page.</span></span>  
- <span data-ttu-id="65cb3-109">Denne registreringen bruker demonstrasjonsfirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="65cb3-109">This recording uses the USMF demo company.</span></span> <span data-ttu-id="65cb3-110">Rollen regnskapssjef leverandørreskontro eller regnskapssjef kan utføre disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="65cb3-110">The accounts payable manager or accounting manager role would perform these steps.</span></span> <span data-ttu-id="65cb3-111">Før du begynner, må du kontrollere at konfigurasjonsnøkkelen for fakturasamsvar er valgt.</span><span class="sxs-lookup"><span data-stu-id="65cb3-111">Before you begin, make sure that the Invoice matching configuration key is selected.</span></span>


## <a name="prepare-to-create-vendor-invoice-policies"></a><span data-ttu-id="65cb3-112">Forberede oppretting av leverandørfakturapolicyer</span><span class="sxs-lookup"><span data-stu-id="65cb3-112">Prepare to create vendor invoice policies</span></span>
1. <span data-ttu-id="65cb3-113">Gå til **Navigasjonsrute > Moduler > Leverandører > Oppsett > Leverandørparametere**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-113">Go to **Navigation pane > Modules > Accounts payable > Setup > Accounts payable parameters**.</span></span>
2. <span data-ttu-id="65cb3-114">Velg **Fakturavalidering**-fanen.</span><span class="sxs-lookup"><span data-stu-id="65cb3-114">Select the **Invoice validation** tab.</span></span>
3. <span data-ttu-id="65cb3-115">Merk av eller fjern merket for **Oppdater fakturahodestatus automatisk**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-115">Select or clear the **Automatically update invoice header** status check box.</span></span>
4. <span data-ttu-id="65cb3-116">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-116">Select **OK**.</span></span>
5. <span data-ttu-id="65cb3-117">Velg et alternativ i feltet **Poster faktura med avvik**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-117">In the **Post invoice with discrepancies** field, select an option.</span></span>
6. <span data-ttu-id="65cb3-118">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="65cb3-118">Close the page.</span></span>
7. <span data-ttu-id="65cb3-119">Gå til **Navigasjonsrute > Moduler > Leverandører > Policyoppsett > Leverandørfakturapolicyer**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-119">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
8. <span data-ttu-id="65cb3-120">Velg **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-120">Select **Parameters**.</span></span>
9. <span data-ttu-id="65cb3-121">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-121">Select **Add**.</span></span>
10. <span data-ttu-id="65cb3-122">Lukk siden for å gå tilbake til startsiden.</span><span class="sxs-lookup"><span data-stu-id="65cb3-122">Close the page to return to the home page.</span></span>

## <a name="create-policy-rule-types-for-vendor-invoices"></a><span data-ttu-id="65cb3-123">Opprette policyregeltyper for leverandørfakturaer</span><span class="sxs-lookup"><span data-stu-id="65cb3-123">Create policy rule types for vendor invoices</span></span>
1. <span data-ttu-id="65cb3-124">Gå til **Navigasjonsrute > Moduler > Leverandører > Policyoppsett > Policyregeltyper for leverandørfaktura**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-124">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policy rule types**.</span></span>
2. <span data-ttu-id="65cb3-125">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-125">Select **New**.</span></span>
3. <span data-ttu-id="65cb3-126">Angi verdier i feltene **Regelnavn** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-126">In the **Rule name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="65cb3-127">I feltet **Spørringsnavn** velger du rullegardinknappen for å åpne oppslaget, og velg deretter den ønskede posten.</span><span class="sxs-lookup"><span data-stu-id="65cb3-127">In the **Query name** field, select the drop-down button to open the lookup, then select the desired record.</span></span>
5. <span data-ttu-id="65cb3-128">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-128">Select **Save**.</span></span>
6. <span data-ttu-id="65cb3-129">Lukk siden for å gå tilbake til startsiden.</span><span class="sxs-lookup"><span data-stu-id="65cb3-129">Close the page to return to the home page.</span></span>

## <a name="define-a-vendor-invoice-policy"></a><span data-ttu-id="65cb3-130">Definere en leverandørfakturapolicy</span><span class="sxs-lookup"><span data-stu-id="65cb3-130">Define a vendor invoice policy</span></span>
1. <span data-ttu-id="65cb3-131">Gå til **Navigasjonsrute > Moduler > Leverandører > Policyoppsett > Leverandørfakturapolicyer**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-131">Go to **Navigation pane > Modules > Accounts payable > Policy setup > Vendor invoice policies**.</span></span>
2. <span data-ttu-id="65cb3-132">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-132">Select **New**.</span></span>
3. <span data-ttu-id="65cb3-133">Angi verdier i feltene **Navn** og **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-133">In the **Name** and **Description** fields, type values.</span></span>
4. <span data-ttu-id="65cb3-134">Vis eller skjul delen **Policyorganisasjoner**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-134">Expand or collapse the **Policy organizations** section.</span></span>
5. <span data-ttu-id="65cb3-135">Velg **Contoso Entertainment System USA** i treet.</span><span class="sxs-lookup"><span data-stu-id="65cb3-135">In the tree, select **Contoso Entertainment System USA**.</span></span>
6. <span data-ttu-id="65cb3-136">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-136">Select **Add**.</span></span>
7. <span data-ttu-id="65cb3-137">Vis eller skjul delen **Policyregler**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-137">Expand or collapse the **Policy rules** section.</span></span>
8. <span data-ttu-id="65cb3-138">Velg **Opprett policyregel**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-138">Select **Create policy rule**.</span></span>
9. <span data-ttu-id="65cb3-139">Skriv inn en verdi i feltet **Beskrivelse av policyregel**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-139">In the **Policy rule description** field, type a value.</span></span>
10. <span data-ttu-id="65cb3-140">Velg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-140">Select **Filter**.</span></span>
11. <span data-ttu-id="65cb3-141">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-141">Select **Add**.</span></span> <span data-ttu-id="65cb3-142">Velg den ønskede posten.</span><span class="sxs-lookup"><span data-stu-id="65cb3-142">Select the desired record.</span></span>
12. <span data-ttu-id="65cb3-143">I feltene **Tabell**, **Avledet tabell** og **Felt** velger eller angir du alternativer fra rullegardinmenyene.</span><span class="sxs-lookup"><span data-stu-id="65cb3-143">In the **Table**, **Derived table**, and **Field** fields, select or enter options from the drop-down menus.</span></span>
13. <span data-ttu-id="65cb3-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="65cb3-144">Close the page.</span></span>
14. <span data-ttu-id="65cb3-145">Skriv inn en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="65cb3-145">In the **Criteria** field, type a value.</span></span>
15. <span data-ttu-id="65cb3-146">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-146">Select **OK**.</span></span>
16. <span data-ttu-id="65cb3-147">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="65cb3-147">Select **OK**.</span></span>
17. <span data-ttu-id="65cb3-148">Lukk sidene for å gå tilbake til startsiden.</span><span class="sxs-lookup"><span data-stu-id="65cb3-148">Close the pages to return to the home page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]