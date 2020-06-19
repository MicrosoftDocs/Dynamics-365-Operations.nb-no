---
title: Brødsmulemodul
description: Dette emnet dekker brødsmulemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 06/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1c6d846686e3214e976a55271694382d7c5973ed
ms.sourcegitcommit: 2683aacb426bfb3b541637edf1f8ec2d6cb5a745
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/01/2020
ms.locfileid: "3417398"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="8d7bd-103">Brødsmulemodul</span><span class="sxs-lookup"><span data-stu-id="8d7bd-103">Breadcrumb module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="8d7bd-104">Dette emnet dekker brødsmulemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="8d7bd-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="8d7bd-105">Overview</span></span>

<span data-ttu-id="8d7bd-106">Brødsmulemoduler brukes til å levere sekundær navigasjon på områdesider.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="8d7bd-107">De vises vanligvis øverst på en side, under overskriften.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="8d7bd-108">Selv om brødsmulemoduler kan legges til på en hvilken som helst side, brukes de oftest på sider for produktdetaljer (PDP-sider) for å vise produktkategorihierarkiet og gi en rask metode for å bevege seg rundt på et område.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="8d7bd-109">En brødsmulemodul kan også brukes til å vise en "Tilbake til resultatene"-kobling når en bruker åpner en PDP fra en søke- eller listeside.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="8d7bd-110">På denne måten kan brukere raskt gå tilbake til den filtrerte listesiden for å fortsette å handle.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="8d7bd-111">På sider som inneholder produktkategorikontekst, for eksempel PDP-er og kategorisider, viser brødsmulekategorier kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="8d7bd-112">På sider som ikke inneholder kategorikontekst, viser brødsmulemoduler **&lt;Områderot&gt; / &lt;Gjeldende side&gt;** som standard.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="8d7bd-113">Brødsmulemoduler kan også konfigureres manuelt på andre typer områdesider for å vise koblinger til bestemte sider på området.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

<span data-ttu-id="8d7bd-114">Bildet nedenfor viser et eksempel på en brødsmulemodul som viser kategorihierarkiet på en PDP.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-114">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Eksempel på en brødsmulemodul](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="8d7bd-116">Innstillinger for brødsmulemoduler</span><span class="sxs-lookup"><span data-stu-id="8d7bd-116">Breadcrumb module settings</span></span>

<span data-ttu-id="8d7bd-117">Brødsmulemodulen er avhengig av **Brødsmulevisningstype på PDP**-innstillingen, som er angitt på **Områdeinnstillinger \> Utvidelser** i områdebygger.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-117">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="8d7bd-118">Denne innstillingen har tre mulige verdier:</span><span class="sxs-lookup"><span data-stu-id="8d7bd-118">This setting has three possible values:</span></span>

- <span data-ttu-id="8d7bd-119">**Vis kategorihierarki** – Når denne verdien er valgt, viser brødsmulemodulen det fullstendige kategorihierarkiet for produktet som vises på PDP.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-119">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="8d7bd-120">**Vise tilbake til resultater** – Når denne verdien er valgt, vil brødsmulemodulen vise en "Tilbake til resultater"-kobling på en PDP hvis brukeren åpnet PDP-en fra en modul som tillater en "Tilbake til resultater"-kobling.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-120">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="8d7bd-121">Denne funksjonaliteten er tilgjengelig når brukere navigerer fra listesider for kategorier, søk, lister og anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-121">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="8d7bd-122">For å støtte denne funksjonaliteten har modulene for produktinnsamling og søkeresultater en egenskap som heter **Tillat tilbake til resultater på PDP**.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-122">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="8d7bd-123">Denne egenskapen gir deg fleksibilitet til å definere hvilke moduler som støtter koblingsfunksjonen "Tilbake til resultatene" på PDP-en.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-123">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="8d7bd-124">Når for eksempel **Vis tilbake til resultater** er valgt for **Brødsmulevisningstype på PDP**-innstillingen i brødsmulemodulen, og **Tillat tilbake til resultater på PDP** er valgt for søkeresultatmodulen for søkesiden, vises en kobling for "Tilbake til resultater" når brukere navigerer fra søkesiden til en PDP.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-124">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="8d7bd-125">**Vis kategorihierarki og tilbake til resultater** – denne verdien er en kombinasjon av de foregående to.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-125">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="8d7bd-126">Når denne verdien er valgt, vil brødsmulemodulen vise både hele kategorihierarkiet og en "Tilbake til resultater"-kobling (hvis den er konfigurert) på en PDP.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-126">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="8d7bd-127">Egenskaper for brødsmulemoduler</span><span class="sxs-lookup"><span data-stu-id="8d7bd-127">Breadcrumb module properties</span></span>

| <span data-ttu-id="8d7bd-128">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="8d7bd-128">Property name</span></span> | <span data-ttu-id="8d7bd-129">Verdier</span><span class="sxs-lookup"><span data-stu-id="8d7bd-129">Values</span></span> | <span data-ttu-id="8d7bd-130">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8d7bd-130">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="8d7bd-131">Rot</span><span class="sxs-lookup"><span data-stu-id="8d7bd-131">Root</span></span> | <span data-ttu-id="8d7bd-132">Tekst eller kobling</span><span class="sxs-lookup"><span data-stu-id="8d7bd-132">Text or link</span></span>| <span data-ttu-id="8d7bd-133">Denne valgfrie egenskapen angir koblingstekst og et koblingsmål for roten til brødsmuleområdet.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-133">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="8d7bd-134">Hvis denne egenskapen ikke er konfigurert, blir det ikke definert noen rot.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-134">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="8d7bd-135">Brødsmulekobling</span><span class="sxs-lookup"><span data-stu-id="8d7bd-135">Breadcrumb link</span></span> | <span data-ttu-id="8d7bd-136">Sammenkobling</span><span class="sxs-lookup"><span data-stu-id="8d7bd-136">Link</span></span> | <span data-ttu-id="8d7bd-137">Denne valgfrie egenskapen angir koblinger for en manuelt konfigurert brødsmule, hvis disse koblingene er nødvendige.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-137">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="8d7bd-138">Koblingene vises i den rekkefølgen de er oppført i.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-138">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="8d7bd-139">Legge til en brødsmulemodul på en ny side</span><span class="sxs-lookup"><span data-stu-id="8d7bd-139">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="8d7bd-140">Hvis du vil legge til en brødsmulemodul på en PDP og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-140">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="8d7bd-141">Gå til **Områdeinnstillinger /> Utvidelser**, finn **Brødsmulevisningstype på PDP**-innstillingen og velg **Vis kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-141">Go to **Site Settings /> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="8d7bd-142">Gå til **Maler**, og velg PDP-malen.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-142">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="8d7bd-143">I **Beholder**-sporet som inneholder kjøpsboksmodulen, velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-143">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8d7bd-144">I dialogboksen **Legg til modul** velger du **Brødsmule**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-144">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8d7bd-145">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-145">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="8d7bd-146">Gå til **Sider**, og åpne en PDP som bruker PDP-malen.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-146">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="8d7bd-147">Hvis en PDP ennå ikke finnes, oppretter du en.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-147">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="8d7bd-148">I **Beholder**-sporet som inneholder kjøpsboksmodulen, velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-148">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="8d7bd-149">I dialogboksen **Legg til modul** velger du **Brødsmule**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-149">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="8d7bd-150">I egenskapsruten for **Brødsmule**-sporet, under **Rot**, velger du **Koblingstekst**.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-150">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="8d7bd-151">I **Koblingstekst**-dialogboksen skriver du **Hjem**,og under **Koblingsmål** velger du **Legg til en kobling**.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-151">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="8d7bd-152">Velg en kobling til brødsmuleroten i dialogboksen **Legg til en kobling**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-152">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="8d7bd-153">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-153">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="8d7bd-154">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="8d7bd-154">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d7bd-155">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8d7bd-155">Additional resources</span></span>

[<span data-ttu-id="8d7bd-156">Startpakke, oversikt</span><span class="sxs-lookup"><span data-stu-id="8d7bd-156">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="8d7bd-157">Oversikt over standard kategorimålside og søkeresultatside</span><span class="sxs-lookup"><span data-stu-id="8d7bd-157">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="8d7bd-158">Produktsamlingsmoduler</span><span class="sxs-lookup"><span data-stu-id="8d7bd-158">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="8d7bd-159">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="8d7bd-159">Buy box module</span></span>](add-buy-box.md)