---
title: "Legge til en kontroll for anbefalinger på transaksjonssiden på en salgsstedsenhet"
description: "Dette emnet beskriver hvordan du legger til en kontroll for anbefalinger på transaksjonsskjermbildet på en salgsstedsenhet ved hjelp av utforming av skjermoppsett i Microsoft Dynamics 365 for Retail."
author: ashishmsft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
ms.search.form: RetailStoreTable, RetailTillLayout
audience: Application User
ms.reviewer: josaw
ms.search.scope: Retail, Operations, Core
ms.custom: 260624
ms.assetid: a4f9d315-9951-451c-8ee6-37f9b3b15ef0
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: d9b080ff46a0fbc73ed4f8fa3f03d71e9d758cc2
ms.openlocfilehash: 86dce19011b98dace5c5df72280180e0b1c8bbaa
ms.contentlocale: nb-no
ms.lasthandoff: 01/17/2018

---

# <a name="add-a-recommendations-control-to-the-transaction-page-on-a-pos-device"></a><span data-ttu-id="a7d75-103">Legge til en kontroll for anbefalinger på transaksjonssiden på en salgsstedsenhet</span><span class="sxs-lookup"><span data-stu-id="a7d75-103">Add a recommendations control to the transaction page on a POS device</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a7d75-104">Dette emnet beskriver hvordan du legger til en kontroll for anbefalinger på transaksjonsskjermbildet på en salgsstedsenhet ved hjelp av utforming av skjermoppsett i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="a7d75-104">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="a7d75-105">Du kan vise produktanbefalingene på salgsstedsenheten når du bruker Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="a7d75-105">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="a7d75-106">*Anbefalinger* er varer som kunden kan være interessert i basert på kjøpshistorikken, varer i ønskelisten og varer som andre kunder har kjøpt på nettet og i fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="a7d75-106">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="a7d75-107">Hvis du vil vise produktanbefalinger, må du legge til en kontroll på transaksjonsskjermen med utforming av skjermoppsett.</span><span class="sxs-lookup"><span data-stu-id="a7d75-107">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="a7d75-108">Åpne utforming av oppsett</span><span class="sxs-lookup"><span data-stu-id="a7d75-108">Open Layout designer</span></span>
1.  <span data-ttu-id="a7d75-109">Gå til **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgssted** &gt; **Skjermoppsett**.</span><span class="sxs-lookup"><span data-stu-id="a7d75-109">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2.  <span data-ttu-id="a7d75-110">Bruk hurtigfilteret til å finne skjermen du vil legge til kontrollen på.</span><span class="sxs-lookup"><span data-stu-id="a7d75-110">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="a7d75-111">Filtrer for eksempel i feltet **Skjermoppsett-ID** ved å bruke verdien "F2CP16:9M".</span><span class="sxs-lookup"><span data-stu-id="a7d75-111">For example, filter on the **Screen layout ID** field using a value of ‘F2CP16:9M’.</span></span>
3.  <span data-ttu-id="a7d75-112">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="a7d75-112">In the list, find and select the desired record.</span></span> <span data-ttu-id="a7d75-113">Velg for eksempel "Navn: F2CP16:9M Skjermoppsett-ID: F2CP16:9M".</span><span class="sxs-lookup"><span data-stu-id="a7d75-113">For example, select ‘Name: F2CP16:9M Screen Layout ID: F2CP16:9M’.</span></span>
4.  <span data-ttu-id="a7d75-114">Klikk **Utforming av oppsett**.</span><span class="sxs-lookup"><span data-stu-id="a7d75-114">Click **Layout designer**.</span></span>
5.  <span data-ttu-id="a7d75-115">Følg instruksjonene for å starte utforming av oppsett.</span><span class="sxs-lookup"><span data-stu-id="a7d75-115">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="a7d75-116">Når du blir spurt etter legitimasjon, angir du den samme legitimasjonen som var i bruk da utforming av oppsett ble startet fra siden **Skjermoppsett**.</span><span class="sxs-lookup"><span data-stu-id="a7d75-116">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6.  <span data-ttu-id="a7d75-117">Når du logger deg på, vises det en side som ligner den nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a7d75-117">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="a7d75-118">Oppsettet vil være forskjellige avhengig av tilpasninger som er gjort for din butikk.</span><span class="sxs-lookup"><span data-stu-id="a7d75-118">The layout will be different depending on the customizations that were made for your store.</span></span>

<span data-ttu-id="a7d75-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Velg et visningsalternativ</span><span class="sxs-lookup"><span data-stu-id="a7d75-119">[![screenlayout-pic-1](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png) Choose a display option</span></span>
-----------------------

<span data-ttu-id="a7d75-120">Det finnes to tilgjengelige konfigurasjonsalternativer.</span><span class="sxs-lookup"><span data-stu-id="a7d75-120">There are two configurations options available.</span></span> <span data-ttu-id="a7d75-121">Velg alternativet som passer best for din butikk, og følg resten av instruksjonene for å konfigurere kontrollen.</span><span class="sxs-lookup"><span data-stu-id="a7d75-121">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="a7d75-122">De to alternativene er:</span><span class="sxs-lookup"><span data-stu-id="a7d75-122">The two options are:</span></span>
-   <span data-ttu-id="a7d75-123">Anbefalinger er alltid synlige.</span><span class="sxs-lookup"><span data-stu-id="a7d75-123">Recommendations are always visible.</span></span>
-   <span data-ttu-id="a7d75-124">Kategorien **Anbefalinger** vises i rutenettet på høyre side av skjermen.</span><span class="sxs-lookup"><span data-stu-id="a7d75-124">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

#### <a name="to-make-recommendations-always-visible"></a><span data-ttu-id="a7d75-125">Slik gjør du anbefalinger alltid synlige:</span><span class="sxs-lookup"><span data-stu-id="a7d75-125">To make recommendations always visible</span></span>

1.  <span data-ttu-id="a7d75-126">Reduser høyden på detaljområdet for transaksjonslinjer slik at det er samme høyde som kundepanelet til venstre. [](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="a7d75-126">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.[](./media/pic-2.png)[![screenlayout-pic-2](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>
2.  <span data-ttu-id="a7d75-127">På menyen til venstre drar og slipper du kontrollen for anbefalinger til mellom detaljområdet for transaksjonslinjer og knappegruppen nederst i midten på transaksjonsskjermen.</span><span class="sxs-lookup"><span data-stu-id="a7d75-127">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="a7d75-128">Endre størrelse på kontrollen slik at den passer i dette området.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="a7d75-128">Resize the control so it fits in that space.[](./media/pic-3.png)[![screenlayout-pic-3](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>
3.  <span data-ttu-id="a7d75-129">Klikk **X** for å lagre og avslutte utforming av oppsett.</span><span class="sxs-lookup"><span data-stu-id="a7d75-129">Click the **X** to save and exit Layout designer.</span></span>
4.  <span data-ttu-id="a7d75-130">I Dynamics 365 for Retail går du til **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplaner**.</span><span class="sxs-lookup"><span data-stu-id="a7d75-130">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5.  <span data-ttu-id="a7d75-131">Velg **1090, Kasser** i listen.</span><span class="sxs-lookup"><span data-stu-id="a7d75-131">In the list, select **1090 Registers**.</span></span>
6.  <span data-ttu-id="a7d75-132">Klikk **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="a7d75-132">Click **Run now**.</span></span>

#### <a name="to-add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="a7d75-133">Slik legger du til kategorien Anbefalinger i knappegruppen på høyre side av skjermen</span><span class="sxs-lookup"><span data-stu-id="a7d75-133">To add a Recommendations tab to the button grid on the right side of the screen</span></span>

1.  <span data-ttu-id="a7d75-134">Høyreklikk i det tomme området under den siste kategorien i knappegruppen plassert på høyre side av siden.</span><span class="sxs-lookup"><span data-stu-id="a7d75-134">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2.  <span data-ttu-id="a7d75-135">Klikk **Tilpass**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="a7d75-135">Click **Customize**.[![pic-5](./media/pic-5.png)](./media/pic-5.png)</span></span>
3.  <span data-ttu-id="a7d75-136">Klikk **Ny kategori**.</span><span class="sxs-lookup"><span data-stu-id="a7d75-136">Click **New tab**.</span></span>
4.  <span data-ttu-id="a7d75-137">Finn den nye kategorien som du nettopp la til.</span><span class="sxs-lookup"><span data-stu-id="a7d75-137">Find the new tab that you just added.</span></span> <span data-ttu-id="a7d75-138">Du må kanskje rulle nedover.</span><span class="sxs-lookup"><span data-stu-id="a7d75-138">You may need to scroll down.</span></span>
5.  <span data-ttu-id="a7d75-139">I rullegardinlisten **Innhold** velger du **Anbefalte produkter**.</span><span class="sxs-lookup"><span data-stu-id="a7d75-139">In the **Contents** drop-down, select **Recommended products**.</span></span> <span data-ttu-id="a7d75-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="a7d75-140">[![pic-6](./media/pic-6.png)](./media/pic-6.png)</span></span>
6.  <span data-ttu-id="a7d75-141">I **Etikett**-feltet, skriv inn et navn for anbefalingsfanen. For eksempel, skriv «Anbefalte produkter».</span><span class="sxs-lookup"><span data-stu-id="a7d75-141">In the **Label** field, type a name for the recommendations tab. For example, type ‘Recommended products’.</span></span>
7.  <span data-ttu-id="a7d75-142">I **Bilde**-feltet velger du bildet som skal vises i kategorien.</span><span class="sxs-lookup"><span data-stu-id="a7d75-142">In the **Image** field, select the image to appear on the tab.</span></span>
8.  <span data-ttu-id="a7d75-143">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="a7d75-143">Click **OK**.</span></span> <span data-ttu-id="a7d75-144">Den nye kategorien vises i knappegruppen.</span><span class="sxs-lookup"><span data-stu-id="a7d75-144">The new tab appears in the button grid.</span></span>
9.  <span data-ttu-id="a7d75-145">Klikk **X** for å lagre og avslutte utforming av oppsett.</span><span class="sxs-lookup"><span data-stu-id="a7d75-145">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="a7d75-146">I Dynamics 365 for Retail går du til **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplaner**.</span><span class="sxs-lookup"><span data-stu-id="a7d75-146">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="a7d75-147">Velg **1090, Kasser** i listen.</span><span class="sxs-lookup"><span data-stu-id="a7d75-147">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="a7d75-148">Klikk **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="a7d75-148">Click **Run now**.</span></span>


<a name="see-also"></a><span data-ttu-id="a7d75-149">Se også</span><span class="sxs-lookup"><span data-stu-id="a7d75-149">See also</span></span>
--------

[<span data-ttu-id="a7d75-150">Oversikt over personlige produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="a7d75-150">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)




