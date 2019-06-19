---
title: Legge til en kontroll for anbefalinger på transaksjonsskjermen på salgsstedsenheter
description: Dette emnet beskriver hvordan du legger til en kontroll for anbefalinger på transaksjonsskjermbildet på en salgsstedsenhet ved hjelp av utforming av skjermoppsett i Microsoft Dynamics 365 for Retail.
author: ashishmsft
manager: AnnBe
ms.date: 02/05/2018
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
ms.openlocfilehash: f17da3db6fbc19548544a0c6c090a0b6db093673
ms.sourcegitcommit: e2fb0846fcc6298050a0ec82c302e5eb5254e0b5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/27/2019
ms.locfileid: "1606855"
---
# <a name="add-a-recommendations-control-to-the-transaction-screen-on-pos-devices"></a><span data-ttu-id="168f9-103">Legge til en kontroll for anbefalinger på transaksjonsskjermen på salgsstedsenheter</span><span class="sxs-lookup"><span data-stu-id="168f9-103">Add a recommendations control to the transaction screen on POS devices</span></span>

[!include [banner](includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="168f9-104">Vi fjerner gjeldende versjon av produktanbefalingstjenesten fordi vi utformer denne funksjonen på nytt med en bedre algoritme og nyere detaljhandelsorienterte funksjoner.</span><span class="sxs-lookup"><span data-stu-id="168f9-104">We are removing the current version of the product recommendation service as we redesign this feature with a better algorithm and newer retail-oriented capabilities.</span></span> <span data-ttu-id="168f9-105">Hvis du vil ha mer informasjon, kan du se [Fjernede eller avskrevne funksjoner](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span><span class="sxs-lookup"><span data-stu-id="168f9-105">For more information see [Removed or deprecated features](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/migration-upgrade/deprecated-features).</span></span>

<span data-ttu-id="168f9-106">Dette emnet beskriver hvordan du legger til en kontroll for anbefalinger på transaksjonsskjermbildet på en salgsstedsenhet ved hjelp av utforming av skjermoppsett i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="168f9-106">This topic describes how to add a recommendations control to the transaction screen on a point of sale (POS) device using the screen layout designer in Microsoft Dynamics 365 for Retail.</span></span>

<span data-ttu-id="168f9-107">Du kan vise produktanbefalingene på salgsstedsenheten når du bruker Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="168f9-107">You can display product recommendations on your POS device when you use Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="168f9-108">*Anbefalinger* er varer som kunden kan være interessert i basert på kjøpshistorikken, varer i ønskelisten og varer som andre kunder har kjøpt på nettet og i fysiske butikker.</span><span class="sxs-lookup"><span data-stu-id="168f9-108">*Recommendations* are items that your customer might be interested in based on their purchase history, items in their wish list, and items that other customers purchased online and in brick-and-mortar stores.</span></span> <span data-ttu-id="168f9-109">Hvis du vil vise produktanbefalinger, må du legge til en kontroll på transaksjonsskjermen med utforming av skjermoppsett.</span><span class="sxs-lookup"><span data-stu-id="168f9-109">To display product recommendations, you need to add a control to the transaction screen using the screen layout designer.</span></span>

## <a name="open-layout-designer"></a><span data-ttu-id="168f9-110">Åpne utforming av oppsett</span><span class="sxs-lookup"><span data-stu-id="168f9-110">Open Layout designer</span></span>

1. <span data-ttu-id="168f9-111">Gå til **Detaljhandel** &gt; **Kanaloppsett** &gt; **Salgsstedsoppsett** &gt; **Salgssted** &gt; **Skjermoppsett**.</span><span class="sxs-lookup"><span data-stu-id="168f9-111">Go to **Retail** &gt; **Channel setup** &gt; **POS setup** &gt; **POS** &gt; **Screen layouts**.</span></span>
2. <span data-ttu-id="168f9-112">Bruk hurtigfilteret til å finne skjermen du vil legge til kontrollen på.</span><span class="sxs-lookup"><span data-stu-id="168f9-112">Use the Quick Filter to find the screen that you want to add the control to.</span></span> <span data-ttu-id="168f9-113">Filtrer for eksempel i feltet **Skjermoppsett-ID** ved å bruke verdien **F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="168f9-113">For example, filter on the **Screen layout ID** field using a value of **F2CP16:9M**.</span></span>
3. <span data-ttu-id="168f9-114">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="168f9-114">In the list, find and select the desired record.</span></span> <span data-ttu-id="168f9-115">Velg for eksempel **Navn: F2CP16:9M Skjermoppsett-ID: F2CP16:9M**.</span><span class="sxs-lookup"><span data-stu-id="168f9-115">For example, select **Name: F2CP16:9M Screen Layout ID: F2CP16:9M**.</span></span>
4. <span data-ttu-id="168f9-116">Klikk **Utforming av oppsett**.</span><span class="sxs-lookup"><span data-stu-id="168f9-116">Click **Layout designer**.</span></span>
5. <span data-ttu-id="168f9-117">Følg instruksjonene for å starte utforming av oppsett.</span><span class="sxs-lookup"><span data-stu-id="168f9-117">Follow the prompts to launch the layout designer.</span></span> <span data-ttu-id="168f9-118">Når du blir spurt etter legitimasjon, angir du den samme legitimasjonen som var i bruk da utforming av oppsett ble startet fra siden **Skjermoppsett**.</span><span class="sxs-lookup"><span data-stu-id="168f9-118">When prompted for credentials, enter the same credentials that were in use when the Layout designer was launched from **Screen layouts** page.</span></span>
6. <span data-ttu-id="168f9-119">Når du logger deg på, vises det en side som ligner den nedenfor.</span><span class="sxs-lookup"><span data-stu-id="168f9-119">When you log in, a page similar to the one below appears.</span></span> <span data-ttu-id="168f9-120">Oppsettet vil være forskjellige avhengig av tilpasninger som er gjort for din butikk.</span><span class="sxs-lookup"><span data-stu-id="168f9-120">The layout will be different depending on the customizations that were made for your store.</span></span>

    <span data-ttu-id="168f9-121">[![Utforming av oppsett](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span><span class="sxs-lookup"><span data-stu-id="168f9-121">[![Layout designer](./media/screenlayout-pic-1.png)](./media/screenlayout-pic-1.png)</span></span>

## <a name="choose-a-display-option"></a><span data-ttu-id="168f9-122">Velge et visningsalternativ</span><span class="sxs-lookup"><span data-stu-id="168f9-122">Choose a display option</span></span>

<span data-ttu-id="168f9-123">Det finnes to tilgjengelige konfigurasjonsalternativer.</span><span class="sxs-lookup"><span data-stu-id="168f9-123">There are two configurations options available.</span></span> <span data-ttu-id="168f9-124">Velg alternativet som passer best for din butikk, og følg resten av instruksjonene for å konfigurere kontrollen.</span><span class="sxs-lookup"><span data-stu-id="168f9-124">Choose the option that works best for your store, and follow the remaining instructions to finish setting up the control.</span></span> <span data-ttu-id="168f9-125">De to alternativene er:</span><span class="sxs-lookup"><span data-stu-id="168f9-125">The two options are:</span></span>

- <span data-ttu-id="168f9-126">Anbefalinger er alltid synlige.</span><span class="sxs-lookup"><span data-stu-id="168f9-126">Recommendations are always visible.</span></span>
- <span data-ttu-id="168f9-127">Kategorien **Anbefalinger** vises i rutenettet på høyre side av skjermen.</span><span class="sxs-lookup"><span data-stu-id="168f9-127">A **Recommendations** tab appears in the grid on the right side of the screen.</span></span>

### <a name="make-recommendations-always-visible"></a><span data-ttu-id="168f9-128">Gjøre anbefalinger alltid synlige</span><span class="sxs-lookup"><span data-stu-id="168f9-128">Make recommendations always visible</span></span>

1. <span data-ttu-id="168f9-129">Reduser høyden på detaljområdet for transaksjonslinjer slik at det er samme høyde som kundepanelet til venstre.</span><span class="sxs-lookup"><span data-stu-id="168f9-129">Reduce the height of the transaction lines details area so that it is the same height as the customer panel to its left.</span></span>

    <span data-ttu-id="168f9-130">[![Høyde på detaljområdet for transaksjonslinjer er redusert](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span><span class="sxs-lookup"><span data-stu-id="168f9-130">[![Height of the transaction lines details area reduced](./media/screenlayout-pic-2.png)](./media/screenlayout-pic-2.png)</span></span>

2. <span data-ttu-id="168f9-131">På menyen til venstre drar og slipper du kontrollen for anbefalinger til mellom detaljområdet for transaksjonslinjer og knappegruppen nederst i midten på transaksjonsskjermen.</span><span class="sxs-lookup"><span data-stu-id="168f9-131">From the menu on the left, drag and drop the recommendations control to between the transaction line details area and the button grid in the center bottom of the transaction screen.</span></span> <span data-ttu-id="168f9-132">Endre størrelse på kontrollen slik at den passer i dette området.</span><span class="sxs-lookup"><span data-stu-id="168f9-132">Resize the control so it fits in that space.</span></span>

    <span data-ttu-id="168f9-133">[![Anbefalingskontroll er lagt til i oppsettet](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span><span class="sxs-lookup"><span data-stu-id="168f9-133">[![Recommendations control added to the layout](./media/screenlayout-pic-3.png)](./media/screenlayout-pic-3.png)</span></span>

3. <span data-ttu-id="168f9-134">Klikk **X** for å lagre og avslutte utforming av oppsett.</span><span class="sxs-lookup"><span data-stu-id="168f9-134">Click the **X** to save and exit Layout designer.</span></span>
4. <span data-ttu-id="168f9-135">Gå til **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplaner** i Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="168f9-135">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
5. <span data-ttu-id="168f9-136">Velg  **1090, Kasser** i listen.</span><span class="sxs-lookup"><span data-stu-id="168f9-136">In the list, select **1090 Registers**.</span></span>
6. <span data-ttu-id="168f9-137">Klikk **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="168f9-137">Click **Run now**.</span></span>

### <a name="add-a-recommendations-tab-to-the-button-grid-on-the-right-side-of-the-screen"></a><span data-ttu-id="168f9-138">Legge til kategorien Anbefalinger i knappegruppen på høyre side av skjermen</span><span class="sxs-lookup"><span data-stu-id="168f9-138">Add a Recommendations tab to the button grid on the right side of the screen</span></span>

1. <span data-ttu-id="168f9-139">Høyreklikk i det tomme området under den siste kategorien i knappegruppen plassert på høyre side av siden.</span><span class="sxs-lookup"><span data-stu-id="168f9-139">Right-click in the empty space below the last tab on the button grid located on the right side of the page.</span></span>
2. <span data-ttu-id="168f9-140">Klikk på **Tilpass**.</span><span class="sxs-lookup"><span data-stu-id="168f9-140">Click **Customize**.</span></span>

    <span data-ttu-id="168f9-141">[![Tilpasning – Kategorikontroll-dialogboks](./media/pic-5.png)](./media/pic-5.png)</span><span class="sxs-lookup"><span data-stu-id="168f9-141">[![Customization - Tab control dialog box](./media/pic-5.png)](./media/pic-5.png)</span></span>

3. <span data-ttu-id="168f9-142">Klikk **Ny kategori**.</span><span class="sxs-lookup"><span data-stu-id="168f9-142">Click **New tab**.</span></span>
4. <span data-ttu-id="168f9-143">Finn den nye kategorien som du nettopp la til.</span><span class="sxs-lookup"><span data-stu-id="168f9-143">Find the new tab that you just added.</span></span> <span data-ttu-id="168f9-144">Du må kanskje rulle nedover.</span><span class="sxs-lookup"><span data-stu-id="168f9-144">You may need to scroll down.</span></span>
5. <span data-ttu-id="168f9-145">I rullegardinlisten **Innhold** velger du **Anbefalte produkter**.</span><span class="sxs-lookup"><span data-stu-id="168f9-145">In the **Contents** drop-down, select **Recommended products**.</span></span>

    <span data-ttu-id="168f9-146">[![Valg av Anbefalte produkter i Innhold-feltet](./media/pic-6.png)](./media/pic-6.png)</span><span class="sxs-lookup"><span data-stu-id="168f9-146">[![Selecting Recommended products in the Contents field](./media/pic-6.png)](./media/pic-6.png)</span></span>

6. <span data-ttu-id="168f9-147">I **Etikett**-feltet, skriv inn et navn for anbefalingsfanen. For eksempel, skriv «Anbefalte produkter».</span><span class="sxs-lookup"><span data-stu-id="168f9-147">In the **Label** field, type a name for the recommendations tab. For example, type 'Recommended products'.</span></span>
7. <span data-ttu-id="168f9-148">I **Bilde**-feltet velger du bildet som skal vises i kategorien.</span><span class="sxs-lookup"><span data-stu-id="168f9-148">In the **Image** field, select the image to appear on the tab.</span></span>
8. <span data-ttu-id="168f9-149">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="168f9-149">Click **OK**.</span></span> <span data-ttu-id="168f9-150">Den nye kategorien vises i knappegruppen.</span><span class="sxs-lookup"><span data-stu-id="168f9-150">The new tab appears in the button grid.</span></span>
9. <span data-ttu-id="168f9-151">Klikk **X** for å lagre og avslutte utforming av oppsett.</span><span class="sxs-lookup"><span data-stu-id="168f9-151">Click the **X** to save and exit Layout designer.</span></span>
10. <span data-ttu-id="168f9-152">Gå til **Detaljhandel** &gt; **IT for detaljhandel** &gt; **Distribusjonsplaner** i Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="168f9-152">In Dynamics 365 for Retail, go to **Retail** &gt; **Retail IT** &gt; **Distribution schedules**.</span></span>
11. <span data-ttu-id="168f9-153">Velg  **1090, Kasser** i listen.</span><span class="sxs-lookup"><span data-stu-id="168f9-153">In the list, select **1090 Registers**.</span></span>
12. <span data-ttu-id="168f9-154">Klikk **Kjør nå**.</span><span class="sxs-lookup"><span data-stu-id="168f9-154">Click **Run now**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="168f9-155">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="168f9-155">Additional resources</span></span>

[<span data-ttu-id="168f9-156">Oversikt over personlige produktanbefalinger</span><span class="sxs-lookup"><span data-stu-id="168f9-156">Personalized product recommendations overview</span></span>](personalized-product-recommendations.md)
