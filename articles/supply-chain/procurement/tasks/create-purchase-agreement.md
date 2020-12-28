---
title: Opprette en kjøpsavtale
description: Dette emnet fører deg gjennom oppretting av en kjøpsavtale.
author: mkirknel
manager: tfehr
ms.date: 07/18/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchAgreement, PurchAgreementCreate, InventItemIdLookupSimple, AgreementConfirmRunForm, PurchAgreementHistory
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1edfd4e56910376d0596eec5eff2af888f7dc98d
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434351"
---
# <a name="create-a-purchase-agreement"></a><span data-ttu-id="7f6b8-103">Opprette en kjøpsavtale</span><span class="sxs-lookup"><span data-stu-id="7f6b8-103">Create a purchase agreement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7f6b8-104">Dette emnet fører deg gjennom oppretting av en kjøpsavtale.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-104">This topic guides you through the creation of a purchase agreement.</span></span> <span data-ttu-id="7f6b8-105">Dette gjøres vanligvis av en innkjøpssjef.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-105">This would typically be done by a purchasing manager.</span></span> <span data-ttu-id="7f6b8-106">Du kan bruke denne fremgangsmåten i demonstrasjonsselskapet USMF eller ved hjelp av dine egne data.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-106">You can use this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="7f6b8-107">Du må ha definert kjøpsavtaleklassifiseringer før du starter.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-107">You need to have set up purchase agreement classifications before you start.</span></span> <span data-ttu-id="7f6b8-108">Når du har opprettet en avtale, kan du bruke den når du oppretter en bestilling, og dette kopierer kjøpsavtalebetingelsene til hodet og linjene i rekkefølgen som er påvirket av avtalen.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-108">Once you've created an agreement you can use it when you create a PO, and this will copy the purchase agreement conditions to the header and to any lines in the order that are affected by the agreement.</span></span>


## <a name="create-a-new-purchase-agreement"></a><span data-ttu-id="7f6b8-109">Opprette en ny kjøpsavtale</span><span class="sxs-lookup"><span data-stu-id="7f6b8-109">Create a new purchase agreement</span></span>
1. <span data-ttu-id="7f6b8-110">Gå til **Navigasjonsrute > Moduler > Innkjøp og leverandører > Kjøpsavtaler > Kjøpsavtaler**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-110">Go to **Navigation pane > Modules > Procurement and sourcing > Purchase agreements > Purchase agreements**.</span></span>
2. <span data-ttu-id="7f6b8-111">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-111">Click **New**.</span></span>
3. <span data-ttu-id="7f6b8-112">I **Leverandørkonto**-feltet velger du raden i den ønskede posten på rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-112">In the **Vendor account** field, select the drop-down menu and select the row of the desired record.</span></span>
4. <span data-ttu-id="7f6b8-113">I feltet **Klassifisering av kjøpsavtale** velger du raden i den ønskede posten på rullegardinmenyen.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-113">In the **Purchase agreement classification** field, select the drop-down menu and select the row of the desired record.</span></span>
5. <span data-ttu-id="7f6b8-114">Vis hurtigfanen **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-114">Expand the **General** FastTab.</span></span>
6. <span data-ttu-id="7f6b8-115">Angi en dato i **Utløpsdato**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-115">In the **Expiration date** field, enter a date.</span></span>

    - <span data-ttu-id="7f6b8-116">Denne utløpsdatoen er standard for alle forpliktelseslinjene og bestemmer hvor lenge hver bestemte forpliktelse er gyldig.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-116">This expiration date will be the default for all commitment lines and will determine how long each specific commitment is valid.</span></span>  

7. <span data-ttu-id="7f6b8-117">I feltet **Dokumenttittel** skriver du inn et navn for kjøpsavtalen.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-117">In the **Document title** field, type a name for your purchase agreement.</span></span>

    - <span data-ttu-id="7f6b8-118">La feltet **Standardforpliktelse** være satt til **Produktantallsforpliktelse** (eller endre det hvis det ikke er satt til dette).</span><span class="sxs-lookup"><span data-stu-id="7f6b8-118">Leave the **Default commitment** field set to **Product quantity commitment** (or change it if it's not set to this).</span></span>  
    - <span data-ttu-id="7f6b8-119">Standardforpliktelsesverdien bestemmer alternativene på avtalelinjene.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-119">The default commitment value determines your options on the agreement lines.</span></span> <span data-ttu-id="7f6b8-120">Hvis du trenger en ny forpliktelsestype når du oppretter avtalelinjene, må du endre standard forpliktelsen i hodet.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-120">If you need a new commitment type when you're creating the agreement lines, you need to change the default commitment on the header.</span></span> <span data-ttu-id="7f6b8-121">Det finnes 4 forskjellige forpliktelser: **Produktantallsforpliktelse** - for et bestemt antall av et produkt; **Produktverdiforpliktelse** - for et bestemt valutabeløp for et produkt; **Verdiforpliktelse for produktkategori** - for et bestemt valutabeløp i en innkjøpskategori der beløpet kan være for en katalogvare eller en ikke-katalogvare; **Verdiforpliktelse** - for et bestemt valutabeløp som kan bli oppfylt av et hvilket som helst produkt eller en hvilken som helst innkjøpskategori.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-121">There are 4 types of commitments: **Product quantity commitment** - for a specific quantity of a product; **Product value commitment** - for a specific currency amount of a product; **Product category value commitment** - for a specific currency amount in a procurement category where the amount can be for a catalog item or a non-catalog item; **Value commitment** - for a specific currency amount which can be fulfilled by any product or by any procurement category.</span></span>  

8. <span data-ttu-id="7f6b8-122">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-122">Select **OK**.</span></span>

## <a name="add-a-commitment"></a><span data-ttu-id="7f6b8-123">Legge til en forpliktelse</span><span class="sxs-lookup"><span data-stu-id="7f6b8-123">Add a commitment</span></span>
1. <span data-ttu-id="7f6b8-124">Velg **Legg til linje**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-124">Select **Add line**.</span></span>
2. <span data-ttu-id="7f6b8-125">Velg det ønskede oppslaget fra rullegardinmenyen i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-125">In the **Item number** field, select the desired record from the drop-down menu.</span></span>
3. <span data-ttu-id="7f6b8-126">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-126">In the **Quantity** field, enter a number.</span></span> <span data-ttu-id="7f6b8-127">Dette er det totale antallet som du har avtalt å kjøpe fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-127">This is the total quantity that you have agreed to buy from your vendor.</span></span>  
4. <span data-ttu-id="7f6b8-128">Angi et tall i **Enhetspris**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-128">In the **Unit price** field, enter a number.</span></span>
5. <span data-ttu-id="7f6b8-129">Vis delen **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-129">Expand the **Line details** section.</span></span>
6. <span data-ttu-id="7f6b8-130">Angi alternativet **Max Maks. håndheves** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-130">Set the **Max is enforced** option to **Yes**.</span></span> <span data-ttu-id="7f6b8-131">**Maks. håndheves**-alternativet begrenser bruken av forpliktelse.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-131">The **Max is enforced** option limits the use of the commitment.</span></span> <span data-ttu-id="7f6b8-132">Du kan bare kjøpe opptil antallet som er angitt i **Antall**-feltet for linjen.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-132">You can only purchase up to the quantity that's specified in the **Quantity** field for the line.</span></span>  

## <a name="add-header-conditions"></a><span data-ttu-id="7f6b8-133">Legge til topptekstbetingelser</span><span class="sxs-lookup"><span data-stu-id="7f6b8-133">Add header conditions</span></span>
1. <span data-ttu-id="7f6b8-134">Velg **Alternativer** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-134">On the Action Pane, select **Options**.</span></span>
2. <span data-ttu-id="7f6b8-135">Velg **Endre visning**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-135">Select **Change view**.</span></span>
3. <span data-ttu-id="7f6b8-136">Velg **Topptekstvisning**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-136">Select **Header view**.</span></span>
4. <span data-ttu-id="7f6b8-137">Utvid **Vilkår**-delen.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-137">Expand the **Terms** section.</span></span>
5. <span data-ttu-id="7f6b8-138">Velg det ønskede oppslaget på rullegardinmenyen **Betalingsmåte**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-138">In the **Method of payment** field, select the desired record in the drop-down menu.</span></span> <span data-ttu-id="7f6b8-139">Betalingsbetingelsene fra leverandørkontoen vises her som standard.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-139">The payment terms from the vendor account are shown here by default.</span></span>  
6. <span data-ttu-id="7f6b8-140">Velg det ønskede oppslaget på rullegardinmenyen i feltet **Leveringsmåte**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-140">In the **Mode of delivery** field, select the desired record in the drop-down menu.</span></span>
7. <span data-ttu-id="7f6b8-141">Klikk rullegardinknappen i feltet **Leveringsbetingelser** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-141">In the **Delivery terms** field, select the drop-down button to open the lookup.</span></span>

## <a name="confirm-and-activate-the-agreement"></a><span data-ttu-id="7f6b8-142">Kontrollere og aktivere avtalen</span><span class="sxs-lookup"><span data-stu-id="7f6b8-142">Confirm and activate the agreement</span></span>
1. <span data-ttu-id="7f6b8-143">Klikk **Kjøpsavtale** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-143">On the Action Pane, select **Purchase agreement**.</span></span>
2. <span data-ttu-id="7f6b8-144">Velg **Bekreftelse**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-144">Select **Confirmation**.</span></span> <span data-ttu-id="7f6b8-145">Angi alternativet **Merk avtale som gyldig** som **Ja**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-145">Set the **Mark agreement as effective** option to **Yes**.</span></span>  
3. <span data-ttu-id="7f6b8-146">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-146">Select **OK**.</span></span>
4. <span data-ttu-id="7f6b8-147">Klikk **Kjøpsavtale** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-147">On the Action Pane, select **Purchase agreement**.</span></span>
5. <span data-ttu-id="7f6b8-148">Velg **Innkjøpsavtalebekreftelser**.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-148">Select **Purchase agreement confirmations**.</span></span> <span data-ttu-id="7f6b8-149">Med alternativet **Forhåndsvis/Skriv ut** kan du generere et dokument for kjøpsavtalen som du deretter kan skrive ut eller sende til leverandøren.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-149">The **Preview/Print** option allows you to generate a document for the purchase agreement which you can then print or send to the vendor.</span></span> <span data-ttu-id="7f6b8-150">Hvis du oppdaterer avtalen senere, og bekrefter den på nytt, vil begge versjoner vises her.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-150">If you update the agreement later on and re-confirm it, both versions will be shown here.</span></span>  
6. <span data-ttu-id="7f6b8-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f6b8-151">Close the page.</span></span>

