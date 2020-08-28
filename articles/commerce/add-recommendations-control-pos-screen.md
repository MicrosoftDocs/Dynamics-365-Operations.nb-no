---
title: Legge til anbefalinger på transaksjonsskjermen
description: Dette emnet beskriver hvordan du legger til en kontroll for anbefalinger på transaksjonsskjermbildet på en salgsstedsenhet ved hjelp av utforming av skjermoppsett i Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: af2450b27106325a86f6db68f9791637694cda63
ms.sourcegitcommit: 8905d7a7a010e451c5435086480f66650ec54926
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2020
ms.locfileid: "3665086"
---
# <a name="add-recommendations-to-the-transaction-screen"></a><span data-ttu-id="ba4aa-103">Legge til anbefalinger på transaksjonsskjermen</span><span class="sxs-lookup"><span data-stu-id="ba4aa-103">Add recommendations to the transaction screen</span></span>

[!include [banner](includes/banner.md)]


<span data-ttu-id="ba4aa-104">Dette emnet beskriver hvordan du legger til en kontroll for anbefalinger på transaksjonsskjermbildet på en salgsstedsenhet ved hjelp av utforming av skjermoppsett i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 Commerce.</span></span> <span data-ttu-id="ba4aa-105">Hvis du vil ha mer informasjon om produktanbefalinger, kan du lese [produktanbefalingene i POS-dokumentasjonen](product.md).</span><span class="sxs-lookup"><span data-stu-id="ba4aa-105">For more information about product recommendations, read the  [product recommendations on POS documentation](product.md).</span></span>


<span data-ttu-id="ba4aa-106">Du kan vise produktanbefalingene på salgsstedsenheten når du bruker Commerce.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-106">You can display product recommendations on your POS device when you use Commerce.</span></span> <span data-ttu-id="ba4aa-107">Hvis du vil vise produktanbefalinger, må du legge til en kontroll på transaksjonsskjermen med utforming av skjermoppsett.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span> 

## <a name="open-layout-designer"></a><span data-ttu-id="ba4aa-108">Åpne utforming av oppsett</span><span class="sxs-lookup"><span data-stu-id="ba4aa-108">Open Layout designer</span></span>

1. <span data-ttu-id="ba4aa-109">Gå til **Retail og Commerce** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgssted** &gt; **Skjermoppsett**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-109">Go to **Retail and Commerce** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="ba4aa-110">Bruk hurtigfilteret til å finne skjermen du vil legge til kontrollen på.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="ba4aa-111">Filtrer for eksempel i feltet **Skjermoppsett-ID** ved å bruke verdien **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-111">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="ba4aa-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="ba4aa-113">Velg for eksempel **Navn: F2CP16:9M Skjermoppsett-ID: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-113">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="ba4aa-114">Klikk **Utforming av oppsett**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-114">Click **Layout designer**.</span></span>
5. <span data-ttu-id="ba4aa-115">Følg instruksjonene for å starte utforming av oppsett.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="ba4aa-116">Når du blir spurt etter legitimasjon, angir du den samme legitimasjonen som var i bruk da utforming av oppsett ble startet fra siden **Skjermoppsett**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="ba4aa-117">Når du logger deg på, vises det en side som ligner den nedenfor.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="ba4aa-118">Oppsettet vil være forskjellige avhengig av tilpasninger som er gjort for din butikk.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-118">The layout will be different depending on the customizations that were made for your store.</span></span>


    <span data-ttu-id="ba4aa-119">[![Utforming av oppsett](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="ba4aa-119">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="ba4aa-120">Velge et visningsalternativ</span><span class="sxs-lookup"><span data-stu-id="ba4aa-120">Choose a display option</span></span>

<span data-ttu-id="ba4aa-121">Det finnes to tilgjengelige konfigurasjonsalternativer.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-121">There are two configurations options available.</span></span> <span data-ttu-id="ba4aa-122">Velg alternativet som passer best for din butikk, og følg resten av instruksjonene for å konfigurere kontrollen.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-122">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="ba4aa-123">De to alternativene er:</span><span class="sxs-lookup"><span data-stu-id="ba4aa-123">The two options are:</span></span>

- <span data-ttu-id="ba4aa-124">Anbefalinger er alltid synlige.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-124">Recommendations are always visible.</span></span>
- <span data-ttu-id="ba4aa-125">Kategorien **Anbefalinger** vises i rutenettet på høyre side av skjermen.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-125">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="ba4aa-126">Gjøre anbefalinger alltid synlige</span><span class="sxs-lookup"><span data-stu-id="ba4aa-126">Make recommendations always visible</span></span>


1. <span data-ttu-id="ba4aa-127">Reduser høyden på detaljområdet for transaksjonslinjer slik at det er samme høyde som kundepanelet til venstre.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-127">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>


    <span data-ttu-id="ba4aa-128">[![Høyde på detaljområdet for transaksjonslinjer er redusert](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="ba4aa-128">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="ba4aa-129">På menyen til venstre drar og slipper du kontrollen for anbefalinger til mellom detaljområdet for transaksjonslinjer og knappegruppen nederst i midten på transaksjonsskjermen.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-129">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="ba4aa-130">Endre størrelse på kontrollen slik at den passer i dette området.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-130">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="ba4aa-131">[![Anbefalingskontroll er lagt til i oppsettet](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="ba4aa-131">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>


3. <span data-ttu-id="ba4aa-132">Klikk **X** for å lagre og avslutte utforming av oppsett.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-132">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="ba4aa-133">I Commerce går du til **Retail og Commerce** &gt; **IT for Retail og Commerce** &gt;**Distribusjonsplaner**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-133">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="ba4aa-134">Velg **1090, Kasser** i listen.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-134">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="ba4aa-135">Klikk **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-135">Click **Run now**.</span></span>


### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="ba4aa-136">Legge til kategorien Anbefalinger i knappegruppen på høyre side av skjermen</span><span class="sxs-lookup"><span data-stu-id="ba4aa-136">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="ba4aa-137">Høyreklikk i det tomme området under den siste kategorien i knappegruppen plassert på høyre side av siden.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-137">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>

2. <span data-ttu-id="ba4aa-138">Klikk på **Tilpass**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-138">Click **Customize**.</span></span>

    <span data-ttu-id="ba4aa-139">[![Tilpasning – Kategorikontroll-dialogboks](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="ba4aa-139">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="ba4aa-140">Klikk **Ny kategori**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-140">Click **New tab**.</span></span>
4. <span data-ttu-id="ba4aa-141">Finn den nye kategorien som du nettopp la til.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-141">Find the new tab that you just added.</span></span> <span data-ttu-id="ba4aa-142">Du må kanskje rulle nedover.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-142">You may need to scroll down.</span></span>
5. <span data-ttu-id="ba4aa-143">I rullegardinlisten **Innhold** velger du **Anbefalte produkter**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-143">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="ba4aa-144">[![Valg av Anbefalte produkter i Innhold-feltet](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="ba4aa-144">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="ba4aa-145">I **Etikett**-feltet, skriv inn et navn for anbefalingsfanen. For eksempel, skriv «Anbefalte produkter».</span><span class="sxs-lookup"><span data-stu-id="ba4aa-145">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="ba4aa-146">I **Bilde**-feltet velger du bildet som skal vises i kategorien.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-146">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="ba4aa-147">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-147">Click **OK**.</span></span> <span data-ttu-id="ba4aa-148">Den nye kategorien vises i knappegruppen.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-148">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="ba4aa-149">Klikk **X** for å lagre og avslutte utforming av oppsett.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-149">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="ba4aa-150">I Commerce går du til **Retail og Commerce** &gt; **IT for Retail og Commerce** &gt;**Distribusjonsplaner**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-150">In Commerce, go to **Retail and Commerce** &gt; **Retail and Commerce IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="ba4aa-151">Velg **1090, Kasser** i listen.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-151">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="ba4aa-152">Klikk **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="ba4aa-152">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ba4aa-153">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ba4aa-153">Additional resources</span></span>

[<span data-ttu-id="ba4aa-154">Oversikt over produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="ba4aa-154">Product recommendations overview</span></span>](product-recommendations.md)

[<span data-ttu-id="ba4aa-155">Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="ba4aa-155">Enable Azure Data Lake Storage in a Dynamics 365 Commerce environment</span></span>](enable-adls-environment.md)

[<span data-ttu-id="ba4aa-156">Aktiver produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="ba4aa-156">Enable product recommendations</span></span>](enable-product-recommendations.md)

[<span data-ttu-id="ba4aa-157">Aktivere personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="ba4aa-157">Enable personalized recommendations</span></span>](personalized-recommendations.md)

[<span data-ttu-id="ba4aa-158">Velge bort personlige anbefalinger</span><span class="sxs-lookup"><span data-stu-id="ba4aa-158">Opt out of personalized recommendations</span></span>](personalization-gdpr.md)

[<span data-ttu-id="ba4aa-159">Aktivere Kjøp lignende utseender-anbefalinger</span><span class="sxs-lookup"><span data-stu-id="ba4aa-159">Enable "shop similar looks" recommendations</span></span>](shop-similar-looks.md)

[<span data-ttu-id="ba4aa-160">Legge til produktanbefalinger på salgssted</span><span class="sxs-lookup"><span data-stu-id="ba4aa-160">Add product recommendations on POS</span></span>](product.md)

[<span data-ttu-id="ba4aa-161">Justere anbefalingsresultater for AI-ML</span><span class="sxs-lookup"><span data-stu-id="ba4aa-161">Adjust AI-ML recommendations results</span></span>](modify-product-recommendation-results.md)

[<span data-ttu-id="ba4aa-162">Opprette kuraterte anbefalinger manuelt</span><span class="sxs-lookup"><span data-stu-id="ba4aa-162">Manually create curated recommendations</span></span>](create-editorial-recommendation-lists.md)

[<span data-ttu-id="ba4aa-163">Opprette anbefalinger med demonstrasjonsdata</span><span class="sxs-lookup"><span data-stu-id="ba4aa-163">Create recommendations with demo data</span></span>](product-recommendations-demo-data.md)

[<span data-ttu-id="ba4aa-164">Vanlige spørsmål om produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="ba4aa-164">Product recommendations FAQ</span></span>](faq-recommendations.md)
