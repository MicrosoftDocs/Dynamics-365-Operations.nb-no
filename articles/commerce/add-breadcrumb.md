---
title: Brødsmulemodul
description: Dette emnet dekker brødsmulemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/20/2020
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
ms.openlocfilehash: ec9f5c72b03d9fd76055369e24491db5c7633cdf
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517166"
---
# <a name="breadcrumb-module"></a><span data-ttu-id="cd70d-103">Brødsmulemodul</span><span class="sxs-lookup"><span data-stu-id="cd70d-103">Breadcrumb module</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="cd70d-104">Dette emnet dekker brødsmulemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="cd70d-104">This topic covers breadcrumb modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="cd70d-105">Oversikt</span><span class="sxs-lookup"><span data-stu-id="cd70d-105">Overview</span></span>

<span data-ttu-id="cd70d-106">Brødsmulemoduler brukes til å levere sekundær navigasjon på områdesider.</span><span class="sxs-lookup"><span data-stu-id="cd70d-106">Breadcrumb modules are used to provide secondary navigation on site pages.</span></span> <span data-ttu-id="cd70d-107">De vises vanligvis øverst på en side, under overskriften.</span><span class="sxs-lookup"><span data-stu-id="cd70d-107">They are typically shown at the top of a page, below the header.</span></span> <span data-ttu-id="cd70d-108">Selv om brødsmulemoduler kan legges til på en hvilken som helst side, brukes de oftest på sider for produktdetaljer (PDP-sider) for å vise produktkategorihierarkiet og gi en rask metode for å bevege seg rundt på et område.</span><span class="sxs-lookup"><span data-stu-id="cd70d-108">Although breadcrumb modules can be added to any page, they are most often used on product details pages (PDPs), to show the product category hierarchy and provide a quick way to move around a site.</span></span> <span data-ttu-id="cd70d-109">En brødsmulemodul kan også brukes til å vise en "Tilbake til resultatene"-kobling når en bruker åpner en PDP fra en søke- eller listeside.</span><span class="sxs-lookup"><span data-stu-id="cd70d-109">A breadcrumb module can also be used to show a "Back to results" link when users open a PDP from a search or list page.</span></span> <span data-ttu-id="cd70d-110">På denne måten kan brukere raskt gå tilbake til den filtrerte listesiden for å fortsette å handle.</span><span class="sxs-lookup"><span data-stu-id="cd70d-110">In this way, users can quickly return to their filtered list page to continue shopping.</span></span>

<span data-ttu-id="cd70d-111">På sider som inneholder produktkategorikontekst, for eksempel PDP-er og kategorisider, viser brødsmulekategorier kategorihierarkiet.</span><span class="sxs-lookup"><span data-stu-id="cd70d-111">On pages that have product category context, such as PDPs and category pages, breadcrumb modules show the category hierarchy.</span></span> <span data-ttu-id="cd70d-112">På sider som ikke inneholder kategorikontekst, viser brødsmulemoduler **&lt;Områderot&gt; / &lt;Gjeldende side&gt;** som standard.</span><span class="sxs-lookup"><span data-stu-id="cd70d-112">On pages that don't have category context, breadcrumb modules show **&lt;Site root&gt; / &lt;Current page&gt;** by default.</span></span> <span data-ttu-id="cd70d-113">Brødsmulemoduler kan også konfigureres manuelt på andre typer områdesider for å vise koblinger til bestemte sider på området.</span><span class="sxs-lookup"><span data-stu-id="cd70d-113">Breadcrumb modules can also be manually configured on other types of site pages to show links to specific pages on the site.</span></span>

> [!NOTE]
> <span data-ttu-id="cd70d-114">Brødsmulemodulen er tilgjengelig i Dynamics 365 Commerce 10.0.12-versjonen.</span><span class="sxs-lookup"><span data-stu-id="cd70d-114">The breadcrumb module is available in the Dynamics 365 Commerce 10.0.12 release.</span></span>

<span data-ttu-id="cd70d-115">Bildet nedenfor viser et eksempel på en brødsmulemodul som viser kategorihierarkiet på en PDP.</span><span class="sxs-lookup"><span data-stu-id="cd70d-115">The following image shows an example of a breadcrumb module that shows the category hierarchy on a PDP.</span></span>

![Eksempel på en brødsmulemodul](./media/ecommerce-breadcrumb.PNG)

## <a name="breadcrumb-module-settings"></a><span data-ttu-id="cd70d-117">Innstillinger for brødsmulemoduler</span><span class="sxs-lookup"><span data-stu-id="cd70d-117">Breadcrumb module settings</span></span>

<span data-ttu-id="cd70d-118">Brødsmulemodulen er avhengig av **Brødsmulevisningstype på PDP**-innstillingen, som er angitt på **Områdeinnstillinger \> Utvidelser** i områdebygger.</span><span class="sxs-lookup"><span data-stu-id="cd70d-118">The breadcrumb module relies on the **Breadcrumb display type on PDP** setting, which is defined at **Site Settings \> Extensions** in site builder.</span></span> <span data-ttu-id="cd70d-119">Denne innstillingen har tre mulige verdier:</span><span class="sxs-lookup"><span data-stu-id="cd70d-119">This setting has three possible values:</span></span>

- <span data-ttu-id="cd70d-120">**Vis kategorihierarki** – Når denne verdien er valgt, viser brødsmulemodulen det fullstendige kategorihierarkiet for produktet som vises på PDP.</span><span class="sxs-lookup"><span data-stu-id="cd70d-120">**Show category hierarchy** – When this value is selected, the breadcrumb module will show the full category hierarchy of the product that is viewed on the PDP.</span></span>
- <span data-ttu-id="cd70d-121">**Vise tilbake til resultater** – Når denne verdien er valgt, vil brødsmulemodulen vise en "Tilbake til resultater"-kobling på en PDP hvis brukeren åpnet PDP-en fra en modul som tillater en "Tilbake til resultater"-kobling.</span><span class="sxs-lookup"><span data-stu-id="cd70d-121">**Show back to results** – When this value is selected, the breadcrumb module will show a "Back to results" link on a PDP if the user opened the PDP from a module that allows for a "Back to results" link.</span></span> <span data-ttu-id="cd70d-122">Denne funksjonaliteten er tilgjengelig når brukere navigerer fra listesider for kategorier, søk, lister og anbefalinger.</span><span class="sxs-lookup"><span data-stu-id="cd70d-122">This functionality is available when users navigate from category, search, list, and recommendation lists pages.</span></span> <span data-ttu-id="cd70d-123">For å støtte denne funksjonaliteten har modulene for produktinnsamling og søkeresultater en egenskap som heter **Tillat tilbake til resultater på PDP**.</span><span class="sxs-lookup"><span data-stu-id="cd70d-123">To support this functionality, product collection and search results modules have a property that is named **Allow back to results on PDP**.</span></span> <span data-ttu-id="cd70d-124">Denne egenskapen gir deg fleksibilitet til å definere hvilke moduler som støtter koblingsfunksjonen "Tilbake til resultatene" på PDP-en.</span><span class="sxs-lookup"><span data-stu-id="cd70d-124">This property gives you the flexibility to define which modules should support the "Back to results" link functionality on the PDP.</span></span> <span data-ttu-id="cd70d-125">Når for eksempel **Vis tilbake til resultater** er valgt for **Brødsmulevisningstype på PDP**-innstillingen i brødsmulemodulen, og **Tillat tilbake til resultater på PDP** er valgt for søkeresultatmodulen for søkesiden, vises en kobling for "Tilbake til resultater" når brukere navigerer fra søkesiden til en PDP.</span><span class="sxs-lookup"><span data-stu-id="cd70d-125">For example, when **Show back to results** is selected for the **Breadcrumb display type on PDP** setting of the breadcrumb module, and **Allow back to results on PDP** is selected for the search page search results module, a "Back to results" link will be shown when users navigate from the search page to a PDP.</span></span>
- <span data-ttu-id="cd70d-126">**Vis kategorihierarki og tilbake til resultater** – denne verdien er en kombinasjon av de foregående to.</span><span class="sxs-lookup"><span data-stu-id="cd70d-126">**Show category hierarchy and back to results** – This value is a combination of the previous two.</span></span> <span data-ttu-id="cd70d-127">Når denne verdien er valgt, vil brødsmulemodulen vise både hele kategorihierarkiet og en "Tilbake til resultater"-kobling (hvis den er konfigurert) på en PDP.</span><span class="sxs-lookup"><span data-stu-id="cd70d-127">When this value is selected, the breadcrumb module will show both the full category hierarchy and a "Back to results" link (if it's configured) on a PDP.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="cd70d-128">Disse innstillingene er tilgjengelige i Dynamics 365 Commerce 10.0.12-versjonen.</span><span class="sxs-lookup"><span data-stu-id="cd70d-128">These settings are available in the Dynamics 365 Commerce 10.0.12 release.</span></span> <span data-ttu-id="cd70d-129">Hvis du oppdaterer fra en eldre versjon av Dynamics 365 Commerce, må du manuelt oppdatere appsettings.json-filen.</span><span class="sxs-lookup"><span data-stu-id="cd70d-129">If you are updating from an older version of Dynamics 365 Commerce, you must manually update the appsettings.json file.</span></span> <span data-ttu-id="cd70d-130">Hvis du vil ha instruksjoner om oppdatering av appsettings.json-filen, se [Oppdateringer for SDK og modulbibliotek](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span><span class="sxs-lookup"><span data-stu-id="cd70d-130">For instructions on updating the appsettings.json file, see [SDK and module library updates](e-commerce-extensibility/sdk-updates.md#update-the-appsettingsjson-file).</span></span>

## <a name="breadcrumb-module-properties"></a><span data-ttu-id="cd70d-131">Egenskaper for brødsmulemoduler</span><span class="sxs-lookup"><span data-stu-id="cd70d-131">Breadcrumb module properties</span></span>

| <span data-ttu-id="cd70d-132">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="cd70d-132">Property name</span></span> | <span data-ttu-id="cd70d-133">Verdier</span><span class="sxs-lookup"><span data-stu-id="cd70d-133">Values</span></span> | <span data-ttu-id="cd70d-134">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cd70d-134">Description</span></span> |
|---------------|--------|-------------|
| <span data-ttu-id="cd70d-135">Rot</span><span class="sxs-lookup"><span data-stu-id="cd70d-135">Root</span></span> | <span data-ttu-id="cd70d-136">Tekst eller kobling</span><span class="sxs-lookup"><span data-stu-id="cd70d-136">Text or link</span></span>| <span data-ttu-id="cd70d-137">Denne valgfrie egenskapen angir koblingstekst og et koblingsmål for roten til brødsmuleområdet.</span><span class="sxs-lookup"><span data-stu-id="cd70d-137">This optional property specifies link text and a link target for the breadcrumb site root.</span></span> <span data-ttu-id="cd70d-138">Hvis denne egenskapen ikke er konfigurert, blir det ikke definert noen rot.</span><span class="sxs-lookup"><span data-stu-id="cd70d-138">If this property isn't configured, no root will be defined.</span></span> |
| <span data-ttu-id="cd70d-139">Brødsmulekobling</span><span class="sxs-lookup"><span data-stu-id="cd70d-139">Breadcrumb link</span></span> | <span data-ttu-id="cd70d-140">Sammenkobling</span><span class="sxs-lookup"><span data-stu-id="cd70d-140">Link</span></span> | <span data-ttu-id="cd70d-141">Denne valgfrie egenskapen angir koblinger for en manuelt konfigurert brødsmule, hvis disse koblingene er nødvendige.</span><span class="sxs-lookup"><span data-stu-id="cd70d-141">This optional property specifies links for a manually configured breadcrumb, if these links are required.</span></span> <span data-ttu-id="cd70d-142">Koblingene vises i den rekkefølgen de er oppført i.</span><span class="sxs-lookup"><span data-stu-id="cd70d-142">Links appear in the order that they are listed in.</span></span> |

## <a name="add-a-breadcrumb-module-to-a-new-page"></a><span data-ttu-id="cd70d-143">Legge til en brødsmulemodul på en ny side</span><span class="sxs-lookup"><span data-stu-id="cd70d-143">Add a breadcrumb module to a new page</span></span>

<span data-ttu-id="cd70d-144">Hvis du vil legge til en brødsmulemodul på en PDP og angi de nødvendige egenskapene, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="cd70d-144">To add a breadcrumb module to a PDP and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="cd70d-145">Gå til **Områdeinnstillinger \> Utvidelser**, finn **Brødsmulevisningstype på PDP**-innstillingen og velg **Vis kategorihierarki**.</span><span class="sxs-lookup"><span data-stu-id="cd70d-145">Go to **Site Settings \> Extensions**, and then, for the **Breadcrumb display type on PDP** setting, select **Show category hierarchy**.</span></span>
1. <span data-ttu-id="cd70d-146">Gå til **Maler**, og velg PDP-malen.</span><span class="sxs-lookup"><span data-stu-id="cd70d-146">Go to **Templates**, and select the PDP template.</span></span>
1. <span data-ttu-id="cd70d-147">I **Beholder**-sporet som inneholder kjøpsboksmodulen, velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="cd70d-147">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cd70d-148">I dialogboksen **Legg til modul** velger du **Brødsmule**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd70d-148">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cd70d-149">Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="cd70d-149">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>
1. <span data-ttu-id="cd70d-150">Gå til **Sider**, og åpne en PDP som bruker PDP-malen.</span><span class="sxs-lookup"><span data-stu-id="cd70d-150">Go to **Pages**, and open a PDP that uses the PDP template.</span></span> <span data-ttu-id="cd70d-151">Hvis en PDP ennå ikke finnes, oppretter du en.</span><span class="sxs-lookup"><span data-stu-id="cd70d-151">If a PDP doesn't yet exist, create one.</span></span>
1. <span data-ttu-id="cd70d-152">I **Beholder**-sporet som inneholder kjøpsboksmodulen, velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.</span><span class="sxs-lookup"><span data-stu-id="cd70d-152">In the **Container** slot that contains the buy box module, select the ellipsis (**...**), and then select **Add Module**.</span></span>
1. <span data-ttu-id="cd70d-153">I dialogboksen **Legg til modul** velger du **Brødsmule**-modulen, og deretter velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd70d-153">In the **Add Module** dialog box, select the **Breadcrumb** module, and then select **OK**.</span></span>
1. <span data-ttu-id="cd70d-154">I egenskapsruten for **Brødsmule**-sporet, under **Rot**, velger du **Koblingstekst**.</span><span class="sxs-lookup"><span data-stu-id="cd70d-154">In the properties pane of the **Breadcrumb** slot, under **Root**, select **Link text**.</span></span>
1. <span data-ttu-id="cd70d-155">I **Koblingstekst**-dialogboksen skriver du **Hjem**,og under **Koblingsmål** velger du **Legg til en kobling**.</span><span class="sxs-lookup"><span data-stu-id="cd70d-155">In the **Link text** dialog box, enter **Home**, and then, under **Link target**, select **Add a link**.</span></span>
1. <span data-ttu-id="cd70d-156">Velg en kobling til brødsmuleroten i dialogboksen **Legg til en kobling**, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd70d-156">In the **Add a link** dialog box, select a link for the breadcrumb root, and then select **OK**.</span></span>
1. <span data-ttu-id="cd70d-157">Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.</span><span class="sxs-lookup"><span data-stu-id="cd70d-157">Select **Save**, and then select **Preview** to preview the page.</span></span>
1. <span data-ttu-id="cd70d-158">Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.</span><span class="sxs-lookup"><span data-stu-id="cd70d-158">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd70d-159">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="cd70d-159">Additional resources</span></span>

[<span data-ttu-id="cd70d-160">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="cd70d-160">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="cd70d-161">Navigasjonsmenymodul</span><span class="sxs-lookup"><span data-stu-id="cd70d-161">Navigation menu module</span></span>](nav-menu-module.md)

[<span data-ttu-id="cd70d-162">Områdevelgermodul</span><span class="sxs-lookup"><span data-stu-id="cd70d-162">Site selector module</span></span>](site-selector.md)

[<span data-ttu-id="cd70d-163">Oversikt over standard kategorimålside og søkeresultatside</span><span class="sxs-lookup"><span data-stu-id="cd70d-163">Overview of default category landing page and search results page</span></span>](category-search-page-overview.md)

[<span data-ttu-id="cd70d-164">Produktsamlingsmoduler</span><span class="sxs-lookup"><span data-stu-id="cd70d-164">Product collection modules</span></span>](product-collection-module-overview.md)

[<span data-ttu-id="cd70d-165">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="cd70d-165">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="cd70d-166">Oppdateringer for SDK og modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="cd70d-166">SDK and module library updates</span></span>](e-commerce-extensibility/sdk-updates.md)
