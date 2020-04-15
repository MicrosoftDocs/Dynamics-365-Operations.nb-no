---
title: Angi salgsavtaler
description: Dette emnet viser hvordan du oppretter en salgsavtale som forplikter en av kundene dine til å kjøpe et produkt til et avtalt beløp over tid, i bytte mot spesialrabatter.
author: omulvad
manager: AnnBe
ms.date: 08/08/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 06d251992c7facca471ac893e5a0fee333e0cbed
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3148659"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="2e8b8-103">Angi salgsavtaler</span><span class="sxs-lookup"><span data-stu-id="2e8b8-103">Enter sales agreements</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="2e8b8-104">Dette emnet viser hvordan du oppretter en salgsavtale som forplikter en av kundene dine til å kjøpe et produkt til et avtalt beløp over tid, i bytte mot spesialrabatter.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-104">This topic explains how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="2e8b8-105">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="2e8b8-106">Definere topptekst i salgsavtale</span><span class="sxs-lookup"><span data-stu-id="2e8b8-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="2e8b8-107">I navigasjonsruten går du til **Moduler > Salg og markedsføring > Salgsavtaler > Salgsavtaler**.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-107">In the navigation pane, go to **Modules > Sales and marketing > Sales agreements > Sales agreements**.</span></span>
2. <span data-ttu-id="2e8b8-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-108">Select **New**.</span></span>
3. <span data-ttu-id="2e8b8-109">Velg det ønskede oppslaget på rullegardinmenyen i **Kundekonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-109">In the **Customer account** field, select the desired record from the drop-down menu.</span></span>
4. <span data-ttu-id="2e8b8-110">Velg det ønskede oppslaget på rullegardinmenyen i **Salgsavtaleklassifisering**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-110">In the **Sales agreement classification** field, select the desired record from the drop-down menu.</span></span>
5. <span data-ttu-id="2e8b8-111">Utvid delen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-111">Expand the **General** section.</span></span>
6. <span data-ttu-id="2e8b8-112">Velg **Produktverdiforpliktelse** i feltet **Standardforpliktelse**.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-112">In the **Default commitment** field, select **Product value commitment**.</span></span> <span data-ttu-id="2e8b8-113">En forpliktelsestype er et obligatorisk vilkår som du må tilordne til avtalen for å definere hvordan avtalekontrakten skal oppfylles.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-113">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="2e8b8-114">De fire forhåndsdefinerte typene lar deg definere kundens forpliktelsesmål, uttrykt som et antall eller en verdi.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-114">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="2e8b8-115">Forpliktelsestypen for antall kan bare brukes for et bestemt produkt, men de verdibaserte typene gjelder for salg av både spesifikke og ikke-spesifikke produkter.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-115">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
7. <span data-ttu-id="2e8b8-116">I **Utløpsdato**-feltet kan du sette datoen til en fremtidig dato som du vil at avtalen skal utløpe på.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-116">In the **Expiration date** field, set the date to a future date when you want the agreement to expire.</span></span>
8. <span data-ttu-id="2e8b8-117">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-117">Select **OK**.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="2e8b8-118">Definere produktverdiforpliktelseslinjer</span><span class="sxs-lookup"><span data-stu-id="2e8b8-118">Set up product value commitment lines</span></span>
1. <span data-ttu-id="2e8b8-119">Velg **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-119">Select **Add line**.</span></span>
2. <span data-ttu-id="2e8b8-120">Velg det ønskede oppslaget fra rullegardinmenyen i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-120">In the **Item number** field, select the desired record from the drop-down menu.</span></span> <span data-ttu-id="2e8b8-121">Typen forpliktelse som du har valgt for avtalen, påvirker hva slags informasjon du kan angi for avtalelinjene.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-121">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="2e8b8-122">For en verdibasert avtale må du for eksempel angi det totale nettobeløpet (i valutaen som er avtalt) som kunden har forpliktet seg til ved kjøpet av varer fra deg.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-122">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="2e8b8-123">I dette eksemplet vil feltene **Antall** og **Enhet** på linjen være utilgjengelige fordi du oppretter en avtale for kunden om å kjøpe en bestemt verdi av et produkt.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-123">In this example the **Quantity** and **Unit** fields on the line are unavailable because you're creating an agreement for the customer to buy a specific value of a product.</span></span>   
3. <span data-ttu-id="2e8b8-124">Angi pengebeløpet som kunden har forpliktet seg til å kjøpe, i **Nettobeløp**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-124">In the **Net amount** field, enter the monetary amount that the customer has committed to buying.</span></span>
4. <span data-ttu-id="2e8b8-125">Angi en prosentverdi som skal gjelde for kundens salgsordrelinjer som er knyttet til denne avtalen, i **Rabattprosent**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-125">In the **Discount percent** field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
5. <span data-ttu-id="2e8b8-126">Vis delen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-126">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="2e8b8-127">Velg **Ja** i **Maks. håndheves**-feltet.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-127">Select **Yes** in the **Max is enforced** field.</span></span>
    - <span data-ttu-id="2e8b8-128">Hvis du velger **Maks. håndheves**, betyr det at totalbeløpet for alle salgsordrelinjene som bruker forpliktelsens spesialpriser, rabatter og/eller betalingsbetingelser, ikke må overskride beløpet som er angitt i forpliktelsen.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-128">Selecting **Max is enforced** means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    - <span data-ttu-id="2e8b8-129">Minimums- og maksimumsfrigivelsesbeløpene angir et verdiområde som må selges på hver salgsordre som bruker den valgte avtalen.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-129">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
7. <span data-ttu-id="2e8b8-130">Vis delen **Topptekst i salgsavtale**.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-130">Expand the **Sales agreement header** section.</span></span> <span data-ttu-id="2e8b8-131">Med mindre statusen for avtalen er satt til **Gjeldende**, kan ikke salgsordrer knyttes til avtalen, og derfor ikke bidra til oppfyllelse av avtalen.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-131">Unless the status of the agreement is set to **Effective**, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="2e8b8-132">Du kan endre statusen manuelt på dette stadiet.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-132">You can change the status manually at this stage.</span></span> <span data-ttu-id="2e8b8-133">Statusen vil imidlertid vanligvis endres når du bekrefter avtalen for kunden.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-133">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
8. <span data-ttu-id="2e8b8-134">Velg **Salgsavtale** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-134">On the Action Pane, select **Sales agreement**.</span></span>
9. <span data-ttu-id="2e8b8-135">Velg **Bekreftelse**.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-135">Select **Confirmation**.</span></span> <span data-ttu-id="2e8b8-136">Kontroller at alternativet **Merk avtale som gyldig** er satt til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-136">Make sure that the **Mark agreement as effective** option is set to **Yes**.</span></span>  
10. <span data-ttu-id="2e8b8-137">Velg **Ja** i feltet **Skriv ut rapport**.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-137">Select **Yes** in the **Print report** field.</span></span>
11. <span data-ttu-id="2e8b8-138">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-138">Select **OK**.</span></span>
12. <span data-ttu-id="2e8b8-139">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-139">Close the page.</span></span> <span data-ttu-id="2e8b8-140">Avtalen er nå gyldig.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-140">The agreement is now effective.</span></span> <span data-ttu-id="2e8b8-141">Du kan begynne å koble kundens ordrer til avtalen for å motregne mot forpliktelsesmålet.</span><span class="sxs-lookup"><span data-stu-id="2e8b8-141">You can start linking the customer's orders to the agreement to offset against the committed target.</span></span>  

