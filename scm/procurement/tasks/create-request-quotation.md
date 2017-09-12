--- 
title: "Opprette en tilbudsforespørsel"
description: "Denne fremgangsmåten viser hvordan du oppretter en tilbudsforespørsel."
author: mkirknel
manager: AnnBe
ms.date: 11/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 331f516f3483acd79be4ef7b95b53adcfbef1ae2
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-request-for-quotation"></a><span data-ttu-id="14eca-103">Opprette en tilbudsforespørsel</span><span class="sxs-lookup"><span data-stu-id="14eca-103">Create a request for quotation</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="14eca-104">Denne fremgangsmåten viser hvordan du oppretter en tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="14eca-104">This procedure shows you how to create a request for quotation.</span></span> <span data-ttu-id="14eca-105">Dette gjøres vanligvis av en innkjøpsagent.</span><span class="sxs-lookup"><span data-stu-id="14eca-105">This would typically be done by a purchasing agent.</span></span> <span data-ttu-id="14eca-106">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="14eca-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="14eca-107">Du må ha definert forespørselstyper før du starter.</span><span class="sxs-lookup"><span data-stu-id="14eca-107">You need to have set up solicitation types before you start.</span></span> <span data-ttu-id="14eca-108">Når du har fullført denne oppgaven og du har opprettet og sendt en tilbudsforespørsel, kan du deretter angi svarene per leverandør, sammenligne dem og gi dem kontrakten.</span><span class="sxs-lookup"><span data-stu-id="14eca-108">Once you’ve completed this task and you’ve created and sent an RFQ you can then enter the replies per vendor, compare them, and award the contract.</span></span>


## <a name="prepare-a-new-rfq"></a><span data-ttu-id="14eca-109">Klargjøre en ny tilbudsforespørsel</span><span class="sxs-lookup"><span data-stu-id="14eca-109">Prepare a new RFQ</span></span>
1. <span data-ttu-id="14eca-110">Gå til Innkjøp og leverandører > Tilbudsforespørsler > Alle tilbudsforespørsler.</span><span class="sxs-lookup"><span data-stu-id="14eca-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="14eca-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="14eca-111">Click New.</span></span>
    * <span data-ttu-id="14eca-112">Følgende innkjøpstyper er tilgjengelige: Bestilling (dette er standard): et dokument som bekrefter tilbudet om å kjøpe produkter eller godkjenning av et tilbud om å selge produkter i bytte mot betaling.</span><span class="sxs-lookup"><span data-stu-id="14eca-112">The following purchase types are available: Purchase order (this is the default): a document that confirms the offer to buy products, or the acceptance of an offer to sell products in exchange for payment.</span></span> <span data-ttu-id="14eca-113">Bestilling: typen velges automatisk hvis du oppretter en tilbudsforespørsel direkte fra en innkjøpsrekvisisjon.</span><span class="sxs-lookup"><span data-stu-id="14eca-113">Purchase requisition: this type is automatically selected if you create an RFQ directly from a purchase requisition.</span></span> <span data-ttu-id="14eca-114">Hvis du manuelt velger dette alternativet, får du en feilmelding.</span><span class="sxs-lookup"><span data-stu-id="14eca-114">If you manually select this option, you’ll get an error.</span></span> <span data-ttu-id="14eca-115">Kjøpsavtale: En avtale om å kjøpe et spesifikt antall eller en verdi av et produkt over tid.</span><span class="sxs-lookup"><span data-stu-id="14eca-115">Purchase agreement: an agreement to purchase a specific quantity or value of product over time.</span></span> <span data-ttu-id="14eca-116">Hvis du velger dette alternativet, må du velge datointervallet som gjelder for kjøpsavtalen.</span><span class="sxs-lookup"><span data-stu-id="14eca-116">If you select this option, you must select the date range that applies to the purchase agreement.</span></span>  
3. <span data-ttu-id="14eca-117">Skriv inn en verdi i Dokumenttittel-feltet.</span><span class="sxs-lookup"><span data-stu-id="14eca-117">In the Document title field, type a value.</span></span>
4. <span data-ttu-id="14eca-118">Angi eller velg en verdi i Forespørselstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="14eca-118">In the Solicitation type field, enter or select a value.</span></span>
    * <span data-ttu-id="14eca-119">Hvis en poengberegningsmetode er knyttet til forespørselstypen, blir dette standarden for poengberegningsmetoden for tilbudsforespørselen du oppretter.</span><span class="sxs-lookup"><span data-stu-id="14eca-119">If a scoring method is associated with the solicitation type, this will be the default scoring method for the RFQ that you’re creating.</span></span> <span data-ttu-id="14eca-120">Du kan endre poengberegningsmetoden senere.</span><span class="sxs-lookup"><span data-stu-id="14eca-120">It is possible to change the scoring method later.</span></span>  
    * <span data-ttu-id="14eca-121">Angi en dato i Leveringsdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="14eca-121">In the Delivery date field, enter a date.</span></span>  
    * <span data-ttu-id="14eca-122">Velg datoen du vil motta varene innen.</span><span class="sxs-lookup"><span data-stu-id="14eca-122">Select the date by which you want to receive the items.</span></span>  
    * <span data-ttu-id="14eca-123">Angi dato og klokkeslett i feltet Utløpsdato- og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="14eca-123">In the Expiration date and time field, enter a date and time.</span></span>  
    * <span data-ttu-id="14eca-124">Angi datoen og klokkeslettet leverandører må svare på tilbudsforespørselen innen.</span><span class="sxs-lookup"><span data-stu-id="14eca-124">Specify the date and time by which vendors must respond to the RFQ.</span></span>  
5. <span data-ttu-id="14eca-125">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="14eca-125">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="14eca-126">Lageradresse er standard leveringsadresse.</span><span class="sxs-lookup"><span data-stu-id="14eca-126">The delivery address will default to the warehouse address.</span></span>  
6. <span data-ttu-id="14eca-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="14eca-127">Click OK.</span></span>

## <a name="add-lines"></a><span data-ttu-id="14eca-128">Legg til linjer</span><span class="sxs-lookup"><span data-stu-id="14eca-128">Add lines</span></span>
    * <span data-ttu-id="14eca-129">Når du har angitt den grunnleggende informasjonen om tilbudsforespørselen din, kan du angi varene eller tjenestene du vil at leverandører skal byr på.</span><span class="sxs-lookup"><span data-stu-id="14eca-129">After you’ve specified the basic information about your RFQ, you specify the goods or services that you want vendors to bid on.</span></span> <span data-ttu-id="14eca-130">Varen er standard linjetype.</span><span class="sxs-lookup"><span data-stu-id="14eca-130">Item is the default line type.</span></span>   
1. <span data-ttu-id="14eca-131">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="14eca-131">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="14eca-132">Hvis du bruker USMF, kan du velge T0020.</span><span class="sxs-lookup"><span data-stu-id="14eca-132">If you're using USMF, you can select T0020.</span></span>  
2. <span data-ttu-id="14eca-133">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="14eca-133">In the Quantity field, enter a number.</span></span>
3. <span data-ttu-id="14eca-134">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="14eca-134">Click Add line.</span></span>
4. <span data-ttu-id="14eca-135">Velg Kategori i Linjetype-feltet.</span><span class="sxs-lookup"><span data-stu-id="14eca-135">In the Line type field, select 'Category'.</span></span>
    * <span data-ttu-id="14eca-136">Du kan bruke kategorilinjetypen til å opprette tilbudsforespørsler for ikke-lagervarer eller tjenester.</span><span class="sxs-lookup"><span data-stu-id="14eca-136">You can use the Category line type to create RFQs for non-inventory goods or services.</span></span> <span data-ttu-id="14eca-137">Deretter må du velge typer varer eller tjenester fra et hierarki av innkjøpskategorier.</span><span class="sxs-lookup"><span data-stu-id="14eca-137">You then need to select the type of goods or services from a hierarchy of procurement categories.</span></span>  
5. <span data-ttu-id="14eca-138">Angi eller velg en verdi i feltet Innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="14eca-138">In the Procurement category field, enter or select a value.</span></span>
6. <span data-ttu-id="14eca-139">Skriv inn en verdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="14eca-139">In the Product name field, type a value.</span></span>
7. <span data-ttu-id="14eca-140">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="14eca-140">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="14eca-141">Angi eller velg en verdi i Enhet-feltet.</span><span class="sxs-lookup"><span data-stu-id="14eca-141">In the Unit field, enter or select a value.</span></span>

## <a name="add-vendors"></a><span data-ttu-id="14eca-142">Legg til leverandører</span><span class="sxs-lookup"><span data-stu-id="14eca-142">Add vendors</span></span>
1. <span data-ttu-id="14eca-143">Klikk overskriften for å endre fra visningen Linjer til overskriftsvisningen.</span><span class="sxs-lookup"><span data-stu-id="14eca-143">Click Header to change from the Lines view to the Header view.</span></span> 
2. <span data-ttu-id="14eca-144">Utvid delen Leverandør.</span><span class="sxs-lookup"><span data-stu-id="14eca-144">Expand the Vendor section.</span></span>
3. <span data-ttu-id="14eca-145">Klikk Legg til leverandører automatisk.</span><span class="sxs-lookup"><span data-stu-id="14eca-145">Click Auto-add vendors.</span></span>
    * <span data-ttu-id="14eca-146">Du kan legge til leverandører i tilbudsforespørselen automatisk, basert på innkjøpskategorien for de forespurte varene.</span><span class="sxs-lookup"><span data-stu-id="14eca-146">You can add vendors to the RFQ automatically, based on the procurement category of the items requested.</span></span> <span data-ttu-id="14eca-147">Hvis ingen leverandører er godkjent for kategoriene som er inkludert i linjene, kan du legge til leverandører manuelt.</span><span class="sxs-lookup"><span data-stu-id="14eca-147">If there are no vendors approved for the categories included in the lines you can add vendors manually.</span></span>  
4. <span data-ttu-id="14eca-148">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="14eca-148">Click Add.</span></span>
5. <span data-ttu-id="14eca-149">Angi eller velg en verdi i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="14eca-149">In the Vendor account field, enter or select a value.</span></span>
6. <span data-ttu-id="14eca-150">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="14eca-150">Click Add.</span></span>
7. <span data-ttu-id="14eca-151">Angi eller velg en verdi i Leverandørkonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="14eca-151">In the Vendor account field, enter or select a value.</span></span>
    * <span data-ttu-id="14eca-152">Når du har valgt en leverandør, blir statusen opprettet.</span><span class="sxs-lookup"><span data-stu-id="14eca-152">Once you’ve selected a vendor, the status is Created.</span></span> <span data-ttu-id="14eca-153">Dette betyr at leverandørinformasjonen er lagret i tilbudsforespørselen, men at du ikke har sendt tilbudsforespørselen til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="14eca-153">This means that the vendor information has been saved in the RFQ, but you have not sent the RFQ to the vendor.</span></span> <span data-ttu-id="14eca-154">Du kan legge til en leverandør i en tilbudsforespørsel uansett leverandørstatus.</span><span class="sxs-lookup"><span data-stu-id="14eca-154">You can add a vendor to an RFQ regardless of the vendor status.</span></span>  

## <a name="send-the-rfq-to-vendors"></a><span data-ttu-id="14eca-155">Sende tilbudsforespørselen til leverandører</span><span class="sxs-lookup"><span data-stu-id="14eca-155">Send the RFQ to vendors</span></span>
1. <span data-ttu-id="14eca-156">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="14eca-156">Click Send.</span></span>
    * <span data-ttu-id="14eca-157">På siden Sender tilbudsforespørsel kontrollerer du at leverandørene i listen er de du vil skal motta tilbudsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="14eca-157">In the Sending request for quotation page, check that the vendors in the list are the ones that you want to receive the RFQ.</span></span>  
2. <span data-ttu-id="14eca-158">Klikk Skriv ut.</span><span class="sxs-lookup"><span data-stu-id="14eca-158">Click Print.</span></span>
    * <span data-ttu-id="14eca-159">Denne dialogboksen lar deg skrive ut tilbudsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="14eca-159">This dialog allows you to print the RFQ.</span></span> <span data-ttu-id="14eca-160">Hvis du velger å skrive ut et svararket, defineres innholdet i dette i Innkjøp og leverandører-parametere.</span><span class="sxs-lookup"><span data-stu-id="14eca-160">If you choose to print a reply sheet, the contents of this are defined in Procurement and Sourcing parameters.</span></span> <span data-ttu-id="14eca-161">Hvis du vil velge hvordan du skriver ut svarark når du har åpnet dialogboksen Skriv, klikker du Avanserte utskriftsalternativer.</span><span class="sxs-lookup"><span data-stu-id="14eca-161">To choose how to print reply sheets, once you’ve opened the Print dialog, click Advanced printing options.</span></span> <span data-ttu-id="14eca-162">Én tilbudsforespørsel skrives ut for hver leverandør, som inneholder linjene har statusen Opprettet eller Sendt.</span><span class="sxs-lookup"><span data-stu-id="14eca-162">One RFQ will be printed for each vendor containing the lines that have the status of Created or Sent.</span></span> <span data-ttu-id="14eca-163">Annullerte linjer og linjer med registrerte svar, vil ikke bli skrevet ut.</span><span class="sxs-lookup"><span data-stu-id="14eca-163">Canceled lines and lines with registered replies will not be printed.</span></span>   
3. <span data-ttu-id="14eca-164">Klikk Avbryt.</span><span class="sxs-lookup"><span data-stu-id="14eca-164">Click Cancel.</span></span>
4. <span data-ttu-id="14eca-165">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="14eca-165">Click OK.</span></span>
5. <span data-ttu-id="14eca-166">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="14eca-166">Close the page.</span></span>
6. <span data-ttu-id="14eca-167">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="14eca-167">Close the page.</span></span>

## <a name="view-the-rfq-journal"></a><span data-ttu-id="14eca-168">Vise tilbudsforespørseljournalen</span><span class="sxs-lookup"><span data-stu-id="14eca-168">View the RFQ journal</span></span>
1. <span data-ttu-id="14eca-169">Gå til Innkjøp og leverandører > Tilbudsforespørsler > Oppfølging av tilbudsforespørsler > Tilbudsforespørseljournaler.</span><span class="sxs-lookup"><span data-stu-id="14eca-169">Go to Procurement and sourcing > Requests for quotations > Request for quotations follow-up > Request for quotation journals.</span></span>
2. <span data-ttu-id="14eca-170">Klikk Forhåndsvis/Skriv ut.</span><span class="sxs-lookup"><span data-stu-id="14eca-170">Click Preview/Print.</span></span>
3. <span data-ttu-id="14eca-171">Klikk Forhåndsvis original.</span><span class="sxs-lookup"><span data-stu-id="14eca-171">Click Original preview.</span></span>
4. <span data-ttu-id="14eca-172">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="14eca-172">Close the page.</span></span>
5. <span data-ttu-id="14eca-173">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="14eca-173">Close the page.</span></span>


