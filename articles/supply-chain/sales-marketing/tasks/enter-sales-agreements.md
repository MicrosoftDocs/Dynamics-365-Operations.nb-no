---
title: Angi salgsavtaler
description: Denne prosedyren viser hvordan du oppretter en salgsavtale som forplikter en av kundene dine til å kjøpe et produkt til et avtalt beløp over tid, i bytte mot spesialrabatter.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesAgreementListPage, SalesAgreementCreate, SalesAgreement, InventItemIdLookupSimple, AgreementConfirmRunForm, SrsReportViewerForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 025c9fe2f769f37b63bd79c6c3afedc31a955310
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "346876"
---
# <a name="enter-sales-agreements"></a><span data-ttu-id="bbee6-103">Angi salgsavtaler</span><span class="sxs-lookup"><span data-stu-id="bbee6-103">Enter sales agreements</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="bbee6-104">Denne prosedyren viser hvordan du oppretter en salgsavtale som forplikter en av kundene dine til å kjøpe et produkt til et avtalt beløp over tid, i bytte mot spesialrabatter.</span><span class="sxs-lookup"><span data-stu-id="bbee6-104">This procedure shows you how to create a sales agreement that commits one of your customers to buy a product for an agreed amount over time in exchange for special discounts.</span></span> <span data-ttu-id="bbee6-105">Du kan kjøre denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="bbee6-105">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="set-up-sales-agreement-header"></a><span data-ttu-id="bbee6-106">Definere topptekst i salgsavtale</span><span class="sxs-lookup"><span data-stu-id="bbee6-106">Set up sales agreement header</span></span>
1. <span data-ttu-id="bbee6-107">Gå til Salg og markedsføring > Salgsavtaler > Salgsavtaler.</span><span class="sxs-lookup"><span data-stu-id="bbee6-107">Go to Sales and marketing > Sales agreements > Sales agreements.</span></span>
2. <span data-ttu-id="bbee6-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="bbee6-108">Click New.</span></span>
3. <span data-ttu-id="bbee6-109">Klikk rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="bbee6-109">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="bbee6-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="bbee6-110">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="bbee6-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="bbee6-111">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="bbee6-112">Klikk rullegardinknappen i feltet Salgsavtaleklassifisering for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="bbee6-112">In the Sales agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="bbee6-113">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="bbee6-113">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="bbee6-114">Utvid delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="bbee6-114">Expand the General section.</span></span>
9. <span data-ttu-id="bbee6-115">Velg Produktverdiforpliktelse i feltet Standardforpliktelse.</span><span class="sxs-lookup"><span data-stu-id="bbee6-115">In the Default commitment field, select 'Product value commitment'.</span></span>
    * <span data-ttu-id="bbee6-116">En forpliktelsestype er et obligatorisk vilkår som du må tilordne til avtalen for å definere hvordan avtalekontrakten skal oppfylles.</span><span class="sxs-lookup"><span data-stu-id="bbee6-116">A commitment type is a mandatory criterion that you must assign to the agreement to define how the agreement contract will be fulfilled.</span></span> <span data-ttu-id="bbee6-117">De fire forhåndsdefinerte typene lar deg definere kundens forpliktelsesmål, uttrykt som et antall eller en verdi.</span><span class="sxs-lookup"><span data-stu-id="bbee6-117">The four predefined types let you set up the customer's commitment target, expressed as a quantity or a value.</span></span> <span data-ttu-id="bbee6-118">Forpliktelsestypen for antall kan bare brukes for et bestemt produkt, men de verdibaserte typene gjelder for salg av både spesifikke og ikke-spesifikke produkter.</span><span class="sxs-lookup"><span data-stu-id="bbee6-118">The quantity commitment type can only be applied to a specific product, but the value-based types are applicable to sales of both specific and non-specific products.</span></span>  
10. <span data-ttu-id="bbee6-119">I Utløpsdato-feltet kan du sette datoen til en fremtidig dato som du vil at avtalen skal utløpe på.</span><span class="sxs-lookup"><span data-stu-id="bbee6-119">In the Expiration date field, set the date to a future date when you want the agreement to expire.</span></span>
11. <span data-ttu-id="bbee6-120">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="bbee6-120">Click OK.</span></span>

## <a name="set-up-product-value-commitment-lines"></a><span data-ttu-id="bbee6-121">Definere produktverdiforpliktelseslinjer</span><span class="sxs-lookup"><span data-stu-id="bbee6-121">Set up product value commitment lines</span></span>
1. <span data-ttu-id="bbee6-122">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="bbee6-122">Click Add line.</span></span>
2. <span data-ttu-id="bbee6-123">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="bbee6-123">In the Item number field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="bbee6-124">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="bbee6-124">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="bbee6-125">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="bbee6-125">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="bbee6-126">Typen forpliktelse som du har valgt for avtalen, påvirker hva slags informasjon du kan angi for avtalelinjene.</span><span class="sxs-lookup"><span data-stu-id="bbee6-126">The type of commitment that you have chosen for the agreement affects the kind of information you can enter for the agreement lines.</span></span> <span data-ttu-id="bbee6-127">For en verdibasert avtale må du for eksempel angi det totale nettobeløpet (i valutaen som er avtalt) som kunden har forpliktet seg til ved kjøpet av varer fra deg.</span><span class="sxs-lookup"><span data-stu-id="bbee6-127">For example, for a value-based agreement you must specify the total net amount (in the agreed currency) for which the customer commits to buys goods from you.</span></span> <span data-ttu-id="bbee6-128">I dette eksemplet vil feltene Antall og Enhet på linjen være utilgjengelige fordi du oppretter en avtale for kunden om å kjøpe en bestemt verdi av et produkt.</span><span class="sxs-lookup"><span data-stu-id="bbee6-128">In this example the Quantity and Unit fields on the line are unavailable because you’re creating an agreement for the customer to buy a specific value of a product.</span></span>   
5. <span data-ttu-id="bbee6-129">Angi pengebeløpet som kunden har forpliktet seg til å kjøpe, i Nettobeløp-feltet.</span><span class="sxs-lookup"><span data-stu-id="bbee6-129">In the Net amount field, enter the monetary amount that the customer has committed to buying.</span></span>
6. <span data-ttu-id="bbee6-130">Angi en prosentverdi som skal gjelde for kundens salgsordrelinjer som er knyttet til denne avtalen, i Rabattprosent-feltet.</span><span class="sxs-lookup"><span data-stu-id="bbee6-130">In the Discount percent field, enter a percentage value that will apply to the customer's sales order lines that are linked to this agreement.</span></span>
7. <span data-ttu-id="bbee6-131">Vis seksjonen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="bbee6-131">Expand the Line details section.</span></span>
8. <span data-ttu-id="bbee6-132">Velg Ja i Maks. håndheves-feltet.</span><span class="sxs-lookup"><span data-stu-id="bbee6-132">Select Yes in the Max is enforced field.</span></span>
    * <span data-ttu-id="bbee6-133">Hvis du velger Maks. håndheves, betyr det at totalbeløpet for alle salgsordrelinjene som bruker forpliktelsens spesialpriser, rabatter og/eller betalingsbetingelser, ikke må overskride beløpet som er angitt i forpliktelsen.</span><span class="sxs-lookup"><span data-stu-id="bbee6-133">Selecting Max is enforced means that the total amount of all the sales order lines that use the commitment's special prices, discounts and/or payment terms must not exceed the amount specified on the commitment.</span></span>  
    * <span data-ttu-id="bbee6-134">Minimums- og maksimumsfrigivelsesbeløpene angir et verdiområde som må selges på hver salgsordre som bruker den valgte avtalen.</span><span class="sxs-lookup"><span data-stu-id="bbee6-134">The minimum and maximum release amounts specify a range of values that must be sold on each sales order that uses the selected agreement.</span></span>   
9. <span data-ttu-id="bbee6-135">Vis delen Topptekst i salgsavtale.</span><span class="sxs-lookup"><span data-stu-id="bbee6-135">Expand the Sales agreement header section.</span></span>
    * <span data-ttu-id="bbee6-136">Med mindre statusen for avtalen er satt til Gjeldende, kan ikke salgsordrer knyttes til avtalen, og derfor ikke bidra til oppfyllelse av avtalen.</span><span class="sxs-lookup"><span data-stu-id="bbee6-136">Unless the status of the agreement is set to Effective, sales orders cannot be associated with the agreement and can therefore not contribute to the fulfilment of that agreement.</span></span> <span data-ttu-id="bbee6-137">Du kan endre statusen manuelt på dette stadiet.</span><span class="sxs-lookup"><span data-stu-id="bbee6-137">You can change the status manually at this stage.</span></span> <span data-ttu-id="bbee6-138">Statusen vil imidlertid vanligvis endres når du bekrefter avtalen for kunden.</span><span class="sxs-lookup"><span data-stu-id="bbee6-138">However, the status would normally be changed when you confirm the agreement for the customer.</span></span>  
10. <span data-ttu-id="bbee6-139">Klikk Salgsavtale i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="bbee6-139">On the Action Pane, click Sales agreement.</span></span>
11. <span data-ttu-id="bbee6-140">Klikk Bekreftelse.</span><span class="sxs-lookup"><span data-stu-id="bbee6-140">Click Confirmation.</span></span>
    * <span data-ttu-id="bbee6-141">Kontroller at alternativet Merk avtale som gyldig er satt til Ja.</span><span class="sxs-lookup"><span data-stu-id="bbee6-141">Make sure that the Mark agreement as effective option is set to Yes.</span></span>  
12. <span data-ttu-id="bbee6-142">Velg Ja i feltet Skriv ut rapport.</span><span class="sxs-lookup"><span data-stu-id="bbee6-142">Select Yes in the Print report field.</span></span>
13. <span data-ttu-id="bbee6-143">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="bbee6-143">Click OK.</span></span>
14. <span data-ttu-id="bbee6-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bbee6-144">Close the page.</span></span>
    * <span data-ttu-id="bbee6-145">Avtalen er nå gyldig, og du kan begynne å koble kundens ordrer til avtalen for å motregne mot forpliktelsesmålet.</span><span class="sxs-lookup"><span data-stu-id="bbee6-145">The agreement is now effective and you can start linking the customer's orders to the agreement, to offset against the committed target.</span></span>  

