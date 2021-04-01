---
title: Slå opp gjeldende priser og rabatter
description: Denne fremgangsmåten viser hvordan du finner prisen og/eller rabatten for et produkt som for øyeblikket er gyldig for en bestemt kunde, uten å opprette en salgsordre.
author: omulvad
manager: tfehr
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 37893b914f02f34071e1d8951a5df993e053f1b1
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5255019"
---
# <a name="look-up-applicable-prices-and-discounts"></a><span data-ttu-id="9183c-103">Slå opp gjeldende priser og rabatter</span><span class="sxs-lookup"><span data-stu-id="9183c-103">Look up applicable prices and discounts</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9183c-104">Denne fremgangsmåten viser hvordan du finner prisen og/eller rabatten for et produkt som for øyeblikket er gyldig for en bestemt kunde, uten å opprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="9183c-104">This procedure shows how to find the price and/or discount for a product which is currently valid for a specific customer, without creating a sales order.</span></span> <span data-ttu-id="9183c-105">Fremgangsmåten hjelper deg med et konkret eksempel, og du må følge dette eksemplet ved hjelp av USMF-demofirmaet for å velge de nødvendige verdiene.</span><span class="sxs-lookup"><span data-stu-id="9183c-105">The procedure walks through a specific example, and you need follow the example using the USMF demo company in order to select the necessary values.</span></span>


## <a name="find-the-applicable-price"></a><span data-ttu-id="9183c-106">Finne den aktuelle prisen</span><span class="sxs-lookup"><span data-stu-id="9183c-106">Find the applicable price</span></span>
1. <span data-ttu-id="9183c-107">Gå til Salg og markedsføring > Priser og rabatter > Søk etter priser.</span><span class="sxs-lookup"><span data-stu-id="9183c-107">Go to Sales and marketing > Prices and discounts > Find prices.</span></span>
2. <span data-ttu-id="9183c-108">Klikk på rullegardinknappen i Kundekonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="9183c-108">In the Customer account field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="9183c-109">Finn og velg kunde US-001 i listen.</span><span class="sxs-lookup"><span data-stu-id="9183c-109">In the list, find and select customer US-001.</span></span>
4. <span data-ttu-id="9183c-110">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9183c-110">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="9183c-111">Skriv inn T0004 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="9183c-111">In the Item number field, type 'T0004'.</span></span>
    * <span data-ttu-id="9183c-112">Antall-feltet er som standard satt til 1.</span><span class="sxs-lookup"><span data-stu-id="9183c-112">By default, the Quantity field is set to 1.</span></span> <span data-ttu-id="9183c-113">Men hvis du vet størrelsen på ordren som kunden har til hensikt å plassere for det aktuelle produktet, angir du denne verdien i stedet.</span><span class="sxs-lookup"><span data-stu-id="9183c-113">However, if you know the size of the order that the customer intends to place for the product in question, then enter this value instead.</span></span> <span data-ttu-id="9183c-114">Denne informasjonen er relevant hvis forretningsavtalene med kunden har antallsintervaller, det vil si at produktets pris avhenger av det minste antallet som kjøpes.</span><span class="sxs-lookup"><span data-stu-id="9183c-114">This information is relevant if the trade agreements with the customer have quantity breaks, that is, the product's price depends on the minimum quantity purchased.</span></span>  
6. <span data-ttu-id="9183c-115">Angi en dato for når kunden forventes å plassere en ordre, i feltet Dato.</span><span class="sxs-lookup"><span data-stu-id="9183c-115">In the Date field, enter a date for when the customer expects to place an order.</span></span> 
    * <span data-ttu-id="9183c-116">Datoen kan være dagens dato eller en dato i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="9183c-116">The date can be today's date or any date in the future.</span></span>  
    * <span data-ttu-id="9183c-117">Systemet returnerer nå prisen som gjelder for det valgte produktet når det kjøpes av den valgte kunden på den valgte datoen med et angitt antall.</span><span class="sxs-lookup"><span data-stu-id="9183c-117">The system now returns the price that is valid for the selected product when bought by the selected customer on the selected date with a specified quantity.</span></span> <span data-ttu-id="9183c-118">Hvis kunden US-001 i dette eksemplet kjøper i dag 1 enhet av produktet T0004, vil de bli belastet CAD 350 per enhet.</span><span class="sxs-lookup"><span data-stu-id="9183c-118">In this example, if the customer US-001 bought 1 unit of product T0004 today, they would be charged 350 CAD a unit.</span></span> <span data-ttu-id="9183c-119">Denne prisen kommer fra en eksisterende og aktiv forretningsavtale med kunden.</span><span class="sxs-lookup"><span data-stu-id="9183c-119">This price comes from an existing and active trade agreement with the customer.</span></span>      <span data-ttu-id="9183c-120">Andre felt på siden inneholder flere detaljer om produktet pris og kostnader (hvis konfigurert på produktstandarden), og beregnet fortjeneste.</span><span class="sxs-lookup"><span data-stu-id="9183c-120">Other fields on the page provide more details about the product price and product cost (if set up on the product master), and calculated profitability.</span></span>  
    * <span data-ttu-id="9183c-121">Hvis alternativet Vis relaterte produktvarianter er valgt, betyr det at det finnes flere forretningsavtaler for produktets varianter.</span><span class="sxs-lookup"><span data-stu-id="9183c-121">If the Show related product variants option is selected, it means that there are additional trade agreements for product's variants.</span></span>  
7. <span data-ttu-id="9183c-122">Klikk på avmerkingsboksen Vis relaterte produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="9183c-122">Click the Show related product variants checkbox.</span></span>
    * <span data-ttu-id="9183c-123">En liste over produktvariantene vises med informasjon om dimensjonene.</span><span class="sxs-lookup"><span data-stu-id="9183c-123">A list of the product variants is shown, with information about their dimensions.</span></span>  
8. <span data-ttu-id="9183c-124">I listen merker du linjen som representerer fargen hvit.</span><span class="sxs-lookup"><span data-stu-id="9183c-124">In the list, mark the line representing color White.</span></span>
    * <span data-ttu-id="9183c-125">Legg merke til at produktprisen nå er forskjellig fra den som ble vist tidligere da den ikke ble angitt per dimensjon.</span><span class="sxs-lookup"><span data-stu-id="9183c-125">Notice, that the product price is now different from the one displayed previously when it was not specified per dimension.</span></span>  
9. <span data-ttu-id="9183c-126">Klikk på Vis salgspriser.</span><span class="sxs-lookup"><span data-stu-id="9183c-126">Click View sales prices.</span></span>
    * <span data-ttu-id="9183c-127">Siden Pris (salg) viser alle forretningsavtalene som gjelder for produktet, inkludert variantene.</span><span class="sxs-lookup"><span data-stu-id="9183c-127">The Price (sales) page displays all the trade agreements applicable to the product, including its variants.</span></span>  
10. <span data-ttu-id="9183c-128">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9183c-128">Close the page.</span></span>

## <a name="find-the-applicable-discount"></a><span data-ttu-id="9183c-129">Finne den aktuelle rabatten</span><span class="sxs-lookup"><span data-stu-id="9183c-129">Find the applicable discount</span></span>
<span data-ttu-id="9183c-130">Kontroller at Kundekonto-feltet inneholder kundenummeret US-001 </span><span class="sxs-lookup"><span data-stu-id="9183c-130">Make sure the Customer account field contains customer number US-001</span></span>   
1. <span data-ttu-id="9183c-131">Skriv inn T0012 i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="9183c-131">In the Item number field, type 'T0012'.</span></span>
    * <span data-ttu-id="9183c-132">Kontroller at Antall-feltet er satt til 1.</span><span class="sxs-lookup"><span data-stu-id="9183c-132">Make sure the Quantity field is set to 1.</span></span>  
    * <span data-ttu-id="9183c-133">De følgende prissettingsdetaljene som vises for produktet T0012, kommer fra én eller flere forretningsavtaler: enhetsprisen er CAD 1 000 og rabattprosenten er 5.</span><span class="sxs-lookup"><span data-stu-id="9183c-133">The following pricing details shown for product T0012 come from one or more trade agreements: The unit price is 1,000 CAD and the discount percentage is 5.</span></span>  
2. <span data-ttu-id="9183c-134">Sett verdien for Antall til 20.</span><span class="sxs-lookup"><span data-stu-id="9183c-134">Set Quantity to '20'.</span></span>
    * <span data-ttu-id="9183c-135">Det økte ordreantallet fører til at linjerabatten som tilbys til kunden, endres fra 5 til 7 prosent.</span><span class="sxs-lookup"><span data-stu-id="9183c-135">The increased order quantity causes the line discount that will be offered to the customer to change from 5 to 7 percent.</span></span>  
    * <span data-ttu-id="9183c-136">Nettobeløpet beregnes basert på enhetspris, rabatt og det totale antallet.</span><span class="sxs-lookup"><span data-stu-id="9183c-136">The Net amount is calculated based on the unit price, discount and the total quantity.</span></span>  
3. <span data-ttu-id="9183c-137">Klikk på Vis linjerabatt.</span><span class="sxs-lookup"><span data-stu-id="9183c-137">Click View line discount.</span></span>
    * <span data-ttu-id="9183c-138">Det finnes to linjerabattavtaler for produktet T0012, som angir en rabatt på 5 prosent for et ordrelinjeantall fra 1 til 10 og 7 prosent rabatt for ordremengder som overstiger 10.</span><span class="sxs-lookup"><span data-stu-id="9183c-138">There are two line discount agreements for product T0012, specifying a 5 percent discount for an order line quantity from 1 to 10, and 7 percent discount for order quantities above 10.</span></span> <span data-ttu-id="9183c-139">Legg merke til at rabattene brukes i en gruppe med produkter, i dette eksemplet gruppekoden 01, som produkt T0012 er et medlem av.</span><span class="sxs-lookup"><span data-stu-id="9183c-139">Note that the discounts are applied to a group of products, in this example, Group code 01, of which product T0012 is a member.</span></span>  
4. <span data-ttu-id="9183c-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="9183c-140">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]