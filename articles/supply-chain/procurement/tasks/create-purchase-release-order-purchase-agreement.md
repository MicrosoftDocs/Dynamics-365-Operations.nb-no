--- 
title: "Opprette en frigivelsesordre for innkjøp fra en innkjøpsavtale"
description: "Denne fremgangsmåten viser hvordan du bruker en kjøpsavtale når du oppretter en bestilling."
author: mkirknel
manager: AnnBe
ms.date: 12/04/2015
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
ms.openlocfilehash: cecda03dd4d224d4319f2b0b196560389bb54195
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-purchase-release-order-from-a-purchase-agreement"></a><span data-ttu-id="5b99a-103">Opprette en frigivelsesordre for innkjøp fra en innkjøpsavtale</span><span class="sxs-lookup"><span data-stu-id="5b99a-103">Create a purchase release order from a purchase agreement</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5b99a-104">Denne fremgangsmåten viser hvordan du bruker en kjøpsavtale når du oppretter en bestilling.</span><span class="sxs-lookup"><span data-stu-id="5b99a-104">This procedure shows how to use a purchase agreement when you create a purchase order.</span></span> <span data-ttu-id="5b99a-105">Kjøpsavtalen må brukes når du oppretter bestillingen, fordi det finnes generelle vilkår som bør kopieres til bestillingshodet.</span><span class="sxs-lookup"><span data-stu-id="5b99a-105">The purchase agreement has to be applied when you create the purchase order because there are general terms that should be copied to the purchase order header.</span></span> <span data-ttu-id="5b99a-106">Denne oppgaven vil vanligvis utføres av en innkjøpsagent.</span><span class="sxs-lookup"><span data-stu-id="5b99a-106">Typically this task would be carried out by a purchasing agent.</span></span> <span data-ttu-id="5b99a-107">Som en forutsetning for denne veiledningen må du ha en gyldig kjøpsavtale med en produktantallsforpliktelse for en leverandør og varer.</span><span class="sxs-lookup"><span data-stu-id="5b99a-107">As a prerequisite for this guide, you must have an effective purchase agreement with a product quantity commitment for a vendor and items.</span></span> <span data-ttu-id="5b99a-108">Den samme fremgangsmåten kan brukes hvis du har en kjøpsavtale med andre former for forpliktelser.</span><span class="sxs-lookup"><span data-stu-id="5b99a-108">The same procedure can be used if you have a purchase agreement with other types of commitments.</span></span> <span data-ttu-id="5b99a-109">Du kan bruke denne veiledningen i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="5b99a-109">You can run this guide in demo data company USMF.</span></span> <span data-ttu-id="5b99a-110">Hvis du bruker USMF, kan du kjøre veiledningen Opprette en kjøpsavtale først for å definere de nødvendig forutsetningene for denne veiledningen.</span><span class="sxs-lookup"><span data-stu-id="5b99a-110">If you’re using USMF, you can run the “Create a purchase agreement” guide first to set up the necessary preconditions for this guide.</span></span>


## <a name="create-a-purchase-order"></a><span data-ttu-id="5b99a-111">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="5b99a-111">Create a purchase order</span></span>
1. <span data-ttu-id="5b99a-112">Åpne arbeidsområdet for bestillingsklargjøring.</span><span class="sxs-lookup"><span data-stu-id="5b99a-112">Open the purchase order preparation workspace.</span></span>
2. <span data-ttu-id="5b99a-113">Klikk Ny bestilling.</span><span class="sxs-lookup"><span data-stu-id="5b99a-113">Click New purchase order.</span></span>
3. <span data-ttu-id="5b99a-114">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5b99a-114">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="5b99a-115">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5b99a-115">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="5b99a-116">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5b99a-116">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="5b99a-117">Aktiver/deaktiver utvidelsen av delen Generelt.</span><span class="sxs-lookup"><span data-stu-id="5b99a-117">Toggle the expansion of the General section.</span></span>
7. <span data-ttu-id="5b99a-118">Klikk rullegardinknappen i feltet Kjøpsavtale for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5b99a-118">In the Purchase agreement field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5b99a-119">Alle tilgjengelige avtaler for leverandøren vises her.</span><span class="sxs-lookup"><span data-stu-id="5b99a-119">All available agreements for the vendor are listed here.</span></span> <span data-ttu-id="5b99a-120">Finn den gyldige avtalen du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="5b99a-120">Find the effective agreement that you want to use.</span></span>  
8. <span data-ttu-id="5b99a-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5b99a-121">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="5b99a-122">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="5b99a-122">Click Yes.</span></span>
10. <span data-ttu-id="5b99a-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5b99a-123">Click OK.</span></span>

## <a name="add-a-line"></a><span data-ttu-id="5b99a-124">Legge til en linje</span><span class="sxs-lookup"><span data-stu-id="5b99a-124">Add a line</span></span>
1. <span data-ttu-id="5b99a-125">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="5b99a-125">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="5b99a-126">Hvis det finnes bestemte dimensjoner for lager eller lokasjon for forpliktelsen, må du angi de samme verdiene på bestillingslinjen for å ta i bruk avtalen.</span><span class="sxs-lookup"><span data-stu-id="5b99a-126">If there are specific inventory or location dimensions on the commitment you must enter the same values on the purchase order line to make use of the agreement.</span></span>  
2. <span data-ttu-id="5b99a-127">Klikk rullegardinknappen i Område-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="5b99a-127">In the Site field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="5b99a-128">Området kan allerede være fylt ut med standardverdien fra bestillingen, eller fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="5b99a-128">The site may already be populated with the default value from the order, or from the vendor.</span></span> <span data-ttu-id="5b99a-129">Hvis dette er tilfelle, kan du hoppe over dette trinnet.</span><span class="sxs-lookup"><span data-stu-id="5b99a-129">If this is the case, skip this step.</span></span>  
3. <span data-ttu-id="5b99a-130">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5b99a-130">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="5b99a-131">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="5b99a-131">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="5b99a-132">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="5b99a-132">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="5b99a-133">Valider at prisen er kopiert fra forpliktelsen.</span><span class="sxs-lookup"><span data-stu-id="5b99a-133">Validate that the price is copied from the commitment.</span></span>  

## <a name="look-up-the-commitment"></a><span data-ttu-id="5b99a-134">Slå opp forpliktelsen</span><span class="sxs-lookup"><span data-stu-id="5b99a-134">Look up the commitment</span></span>
1. <span data-ttu-id="5b99a-135">Klikk Oppdater linje.</span><span class="sxs-lookup"><span data-stu-id="5b99a-135">Click Update line.</span></span>
2. <span data-ttu-id="5b99a-136">Klikk Vedlagt.</span><span class="sxs-lookup"><span data-stu-id="5b99a-136">Click Attached.</span></span>
    * <span data-ttu-id="5b99a-137">Her finner du detaljer for kjøpsavtalen.</span><span class="sxs-lookup"><span data-stu-id="5b99a-137">Here you can get details for the purchase agreement.</span></span> <span data-ttu-id="5b99a-138">Du kan for eksempel se prisen og om prisen og rabatten er fast, noe som betyr at hvis du endrer prisen eller rabatten i bestillingen til en annen verdi enn i forpliktelsen, fjernes koblingen slik at bestillingslinjen ikke oppfyller forpliktelsen.</span><span class="sxs-lookup"><span data-stu-id="5b99a-138">For example, you can see the price and whether the price and discount are fixed, which means that if you change price or discount on the purchase order to a different value than on the commitment, the system will remove the link so the purchase order line does not fulfill the commitment.</span></span> <span data-ttu-id="5b99a-139">Du kan også se om Maks. håndheves-alternativet er valgt, noe som betyr at antallet på forpliktelsen ikke kan overskrides ved å summere alle kjøpene som oppfyller forpliktelsen.</span><span class="sxs-lookup"><span data-stu-id="5b99a-139">You can also see if the Max is enforced option is selected, which means that the quantity on the commitment cannot be exceeded by summing all of the purchases that fulfill the commitment.</span></span>  
3. <span data-ttu-id="5b99a-140">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5b99a-140">Close the page.</span></span>

## <a name="look-up-the-purchase-agreement"></a><span data-ttu-id="5b99a-141">Slå opp kjøpsavtalen</span><span class="sxs-lookup"><span data-stu-id="5b99a-141">Look up the purchase agreement</span></span>
1. <span data-ttu-id="5b99a-142">Klikk Generelt i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="5b99a-142">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="5b99a-143">Klikk Kjøpsavtale.</span><span class="sxs-lookup"><span data-stu-id="5b99a-143">Click Purchase agreement.</span></span>
3. <span data-ttu-id="5b99a-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5b99a-144">Close the page.</span></span>
4. <span data-ttu-id="5b99a-145">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5b99a-145">Close the page.</span></span>


