--- 
title: "Opprette en kjøpsavtale"
description: "Denne prosedyren fører deg gjennom oppretting av en kjøpsavtale."
author: mkirknel
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: c547f825c567848b06b84ac1baaa5ae3bc6c2860
ms.contentlocale: nb-no
ms.lasthandoff: 09/11/2018

---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="4bc1b-103">Opprette en kjøpsavtale</span><span class="sxs-lookup"><span data-stu-id="4bc1b-103">Create a purchase agreement</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4bc1b-104">Denne prosedyren fører deg gjennom oppretting av en kjøpsavtale.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-104">This procedure guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="4bc1b-105">Dette gjøres vanligvis av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="4bc1b-106">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="4bc1b-107">Du må ha definert kjøpsavtaleklassifiseringer før du starter.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="4bc1b-108">Når du har opprettet en avtale, kan du bruke den når du oppretter en bestilling, og dette kopierer kjøpsavtalebetingelsene til hodet og linjene i rekkefølgen som er påvirket av avtalen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="4bc1b-109">Opprette en ny kjøpsavtale</span><span class="sxs-lookup"><span data-stu-id="4bc1b-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="4bc1b-110">Gå til Innkjøp og leverandører > Kjøpsavtaler > Kjøpsavtaler.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-110">Go to Procurement and sourcing > Purchase agreements > Purchase agreements.</span></span>
2. <span data-ttu-id="4bc1b-111">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-111">Click New.</span></span>
3. <span data-ttu-id="4bc1b-112">Klikk rullegardinknappen i Leverandørkonto-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-112">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4bc1b-113">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4bc1b-114">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-114">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4bc1b-115">Klikk rullegardinknappen i feltet Kjøpsavtaleklassifisering for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-115">In the Purchase agreement classification field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="4bc1b-116">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-116">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="4bc1b-117">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-117">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="4bc1b-118">Utvid seksjonen Generelt.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-118">Expand the General section.</span></span>
10. <span data-ttu-id="4bc1b-119">Angi en dato i Utløpsdato-feltet.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-119">In the Expiration date field, enter a date.</span></span>
    * <span data-ttu-id="4bc1b-120">Denne utløpsdatoen er standard for alle forpliktelseslinjene og bestemmer hvor lenge hver bestemte forpliktelse er gyldig.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-120">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  
11. <span data-ttu-id="4bc1b-121">I feltet Dokumenttittel skriver du inn et navn for kjøpsavtalen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-121">In the Document title field, type a name for your purchase agreement.</span></span>
    * <span data-ttu-id="4bc1b-122">La feltet Standardforpliktelse være satt til Produktantallsforpliktelse (eller endre det hvis det ikke er satt til dette).</span><span class="sxs-lookup"><span data-stu-id="4bc1b-122">Leave the Default commitment field set to Product quantity commitment (or change it if it’s not set to this).</span></span>  
    * <span data-ttu-id="4bc1b-123">Standardforpliktelsesverdien bestemmer alternativene på avtalelinjene.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-123">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="4bc1b-124">Hvis du trenger en ny forpliktelsestype når du oppretter avtalelinjene, må du endre standard forpliktelsen i hodet.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-124">If you need a new commitment type when you’re creating the agreement lines, you need to change the default commitment on the header.</span></span>  <span data-ttu-id="4bc1b-125">Det finnes 4 forskjellige forpliktelser: Produktantallsforpliktelse - for et bestemt antall av et produkt; Produktverdiforpliktelse - for et bestemt valutabeløp for et produkt; Verdiforpliktelse for produktkategori - for et bestemt valutabeløp i en innkjøpskategori der beløpet kan være for en katalogvare eller en ikke-katalogvare; Verdiforpliktelse - for et bestemt valutabeløp som kan bli oppfylt av et et hvilket som helst produkt eller en hvilken som helst innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-125">There are 4 types of commitments: Product quantity commitment - for a specific quantity of a product; Product value commitment - for a specific currency amount of a product; Product category value commitment - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; Value commitment - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  
12. <span data-ttu-id="4bc1b-126">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-126">Click OK.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="4bc1b-127">Legge til en forpliktelse</span><span class="sxs-lookup"><span data-stu-id="4bc1b-127">Add a commitment</span></span>
1. <span data-ttu-id="4bc1b-128">Klikk Legg til linje.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-128">Click Add line.</span></span>
2. <span data-ttu-id="4bc1b-129">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-129">In the list, mark the selected row.</span></span>
3. <span data-ttu-id="4bc1b-130">Klikk rullegardinknappen i Varenummer-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-130">In the Item number field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4bc1b-131">Velg produktet du vil legge til en forpliktelse for.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-131">Select the product you want to add a commitment for.</span></span>
5. <span data-ttu-id="4bc1b-132">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-132">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4bc1b-133">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-133">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="4bc1b-134">Dette er det totale antallet som du har avtalt å kjøpe fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-134">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
7. <span data-ttu-id="4bc1b-135">Angi et tall i feltet Enhetspris.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-135">In the Unit price field, enter a number.</span></span>
8. <span data-ttu-id="4bc1b-136">Vis seksjonen Linjedetaljer.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-136">Expand the Line details section.</span></span>
9. <span data-ttu-id="4bc1b-137">Angi alternativet Maks. håndheves til Ja.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-137">Set the Max is enforced option to Yes.</span></span>
    * <span data-ttu-id="4bc1b-138">Maks. håndheves-alternativet begrenser bruken av forpliktelse.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-138">The Max is enforced option limits the use of the commitment.</span></span> <span data-ttu-id="4bc1b-139">Du kan bare kjøpe opptil antallet som er angitt i Antall-feltet for linjen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-139">You can only purchase up to the quantity that's specified in the Quantity field for the line.</span></span>  
10. <span data-ttu-id="4bc1b-140">Skjul Linjedetaljer-delen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-140">Collapse the Line details section.</span></span>

## <a name="add-header-conditions"></a><span data-ttu-id="4bc1b-141">Legge til topptekstbetingelser</span><span class="sxs-lookup"><span data-stu-id="4bc1b-141">Add header conditions</span></span>
1. <span data-ttu-id="4bc1b-142">Klikk Alternativer i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-142">On the Action Pane, click Options.</span></span>
2. <span data-ttu-id="4bc1b-143">Klikk Bytt visning.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-143">Click Change view.</span></span>
3. <span data-ttu-id="4bc1b-144">Klikk Hodevisning.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-144">Click Header view.</span></span>
4. <span data-ttu-id="4bc1b-145">Utvid Vilkår-delen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-145">Expand the Terms section.</span></span>
5. <span data-ttu-id="4bc1b-146">Klikk rullegardinknappen i Betalingsmåte-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-146">In the Method of payment field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="4bc1b-147">Betalingsbetingelsene fra leverandørkontoen vises her som standard.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-147">The payment terms from the vendor account are shown here by default.</span></span>       
6. <span data-ttu-id="4bc1b-148">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-148">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="4bc1b-149">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-149">In the list, click the link in the selected row.</span></span>
8. <span data-ttu-id="4bc1b-150">Klikk rullegardinknappen i feltet Leveringsmåte for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-150">In the Mode of delivery field, click the drop-down button to open the lookup.</span></span>
9. <span data-ttu-id="4bc1b-151">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-151">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="4bc1b-152">Klikk rullegardinknappen i feltet Leveringsbetingelser for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-152">In the Delivery terms field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="4bc1b-153">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-153">In the list, click the link in the selected row.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="4bc1b-154">Kontrollere og aktivere avtalen</span><span class="sxs-lookup"><span data-stu-id="4bc1b-154">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="4bc1b-155">Klikk Kjøpsavtale i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-155">On the Action Pane, click Purchase agreement.</span></span>
2. <span data-ttu-id="4bc1b-156">Klikk Bekreftelse.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-156">Click Confirmation.</span></span>
    * <span data-ttu-id="4bc1b-157">Angi alternativet Merk avtale som gyldig som Ja.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-157">Set the Mark agreement as effective option to Yes.</span></span>  
3. <span data-ttu-id="4bc1b-158">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-158">Click OK.</span></span>
4. <span data-ttu-id="4bc1b-159">Klikk Kjøpsavtale i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-159">On the Action Pane, click Purchase agreement.</span></span>
5. <span data-ttu-id="4bc1b-160">Klikk Innkjøpsavtalebekreftelser.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-160">Click Purchase agreement confirmations.</span></span>
    * <span data-ttu-id="4bc1b-161">Med alternativet Forhåndsvis/Skriv ut kan du generere et dokument for kjøpsavtalen som du kan deretter skrive ut eller sende til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-161">The Preview/Print option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="4bc1b-162">Hvis du oppdaterer avtalen senere, og bekrefter den på nytt, vil begge versjoner vises her.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-162">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="4bc1b-163">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4bc1b-163">Close the page.</span></span>


