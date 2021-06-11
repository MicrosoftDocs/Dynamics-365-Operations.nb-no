---
title: Bruke visningsinnstillinger for produktdimensjoner
description: Dette emnet dekker visningsinnstillingene for produktdimensjoner og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b901622bbfc8d6b3066879f6456a4ab618ca4076
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117239"
---
# <a name="apply-display-settings-for-product-dimensions"></a><span data-ttu-id="3c667-103">Bruke visningsinnstillinger for produktdimensjoner</span><span class="sxs-lookup"><span data-stu-id="3c667-103">Apply display settings for product dimensions</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="3c667-104">Dette emnet dekker visningsinnstillingene for produktdimensjoner og beskriver hvordan du bruker dem i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="3c667-104">This topic covers the display settings for product dimensions and describes how to apply them in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="3c667-105">Dynamics 365 Commerce støtter størrelse, stil og fargedimensjoner for å skille produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="3c667-105">Dynamics 365 Commerce supports size, style, and color dimensions to distinguish product variants.</span></span> <span data-ttu-id="3c667-106">Dimensjoner vises som regel som tekstverdier, for eksempel Liten, Middels og Stor for størrelser, og Svart og Brun for farger.</span><span class="sxs-lookup"><span data-stu-id="3c667-106">Dimensions are typically shown as text values, such as "Small," "Medium," and "Large" for sizes, and "Black" and "Brown" for colors.</span></span> <span data-ttu-id="3c667-107">Hvis et produkt støtter mange variasjoner, kan det være vanskelig å bla gjennom produktvarianter fordi flere valg kreves for å vise bildet for hver variant.</span><span class="sxs-lookup"><span data-stu-id="3c667-107">However, if a product supports many variations, it can be difficult to browse product variants, because multiple selections are required to view the image for each variant.</span></span> <span data-ttu-id="3c667-108">For å gjøre det enklere å bla gjennom produktvarianter, kan versjon 10.0.20-utgivelsen av Commerce bruke bilder og heksadesimalkoder (heksadesimal) til å vise dimensjoner som prøver.</span><span class="sxs-lookup"><span data-stu-id="3c667-108">To make it easier to browse product variants, the version 10.0.20 release of Commerce can use images and hexadecimal (hex) codes to show dimensions as swatches.</span></span>

<span data-ttu-id="3c667-109">I Commerce-områdebyggeren defineres dimensjonsinnstillinger på **Områdeinnstillinger \> Utvidelser \> Dimensjonsinnstillinger**.</span><span class="sxs-lookup"><span data-stu-id="3c667-109">In Commerce site builder, dimension settings are defined at **Site Settings \> Extensions \> Dimension Settings**.</span></span> <span data-ttu-id="3c667-110">Illustrasjonen nedenfor viser et eksempel på dimensjonsinnstillinger i områdekonfigurator.</span><span class="sxs-lookup"><span data-stu-id="3c667-110">The following illustration shows an example of dimension settings in site builder.</span></span>

![Eksempel på områdeinnstillinger i Commerce-områdebyggeren](./dev-itpro/media/swatch_site_settings.PNG)

<span data-ttu-id="3c667-112">To dimensjonsinnstillinger er tilgjengelige:</span><span class="sxs-lookup"><span data-stu-id="3c667-112">Two dimension settings are available:</span></span>

- <span data-ttu-id="3c667-113">**Dimensjoner som skal vises som bilde** – Angi hvilke dimensjoner som skal vises som prøver på e-handelsområdesider, for eksempel produktdetaljsider (PDPer) og resultatlistesider for søk.</span><span class="sxs-lookup"><span data-stu-id="3c667-113">**Dimensions to display as image** – Specify which dimensions should appear as swatches on e-commerce site pages such as product details pages (PDPs) and search result list pages.</span></span> <span data-ttu-id="3c667-114">En hvilken som helst kombinasjon av farge-, størrelse- og stildimensjoner kan vises som en prøve.</span><span class="sxs-lookup"><span data-stu-id="3c667-114">Any combination of color, size, and style dimensions can be shown as a swatch.</span></span> <span data-ttu-id="3c667-115">Hvis en dimensjon er valgt for visning som en prøve, vil gjengivelse av Commerce-modulen se etter en tilgjengelig konfigurasjon av en heksakodeprøve.</span><span class="sxs-lookup"><span data-stu-id="3c667-115">If a dimension is selected for display as a swatch, Commerce module rendering will look for an available configuration of a hex code swatch.</span></span> <span data-ttu-id="3c667-116">Hvis ingen heksakode er konfigurert, vil systemlogikk se etter en konfigurasjon av en bilde-URL-prøve.</span><span class="sxs-lookup"><span data-stu-id="3c667-116">If no hex code is configured, system logic will look for a configuration of an image URL swatch.</span></span> <span data-ttu-id="3c667-117">Hvis verken en heksakode eller en bilde-URL er konfigurert, vises teksten.</span><span class="sxs-lookup"><span data-stu-id="3c667-117">If neither a hex code nor an image URL is configured, text will be shown.</span></span>

    <span data-ttu-id="3c667-118">Illustrasjonen nedenfor viser et eksempel der en PDP på en e-handelsside inneholder farge- og størrelsesprøver.</span><span class="sxs-lookup"><span data-stu-id="3c667-118">The following illustration shows an example where a PDP on an e-commerce site includes color and size swatches.</span></span> <span data-ttu-id="3c667-119">I dette eksemplet konfigureres en heksakode for fargedimensjonen.</span><span class="sxs-lookup"><span data-stu-id="3c667-119">In this example, a hex code is configured for the color dimension.</span></span> <span data-ttu-id="3c667-120">Derfor vises prøver som farger.</span><span class="sxs-lookup"><span data-stu-id="3c667-120">Therefore, swatches are shown as colors.</span></span> <span data-ttu-id="3c667-121">Men verken en heksakode eller en bilde-URL er konfigurert for størrelsesdimensjonen.</span><span class="sxs-lookup"><span data-stu-id="3c667-121">However, neither a hex code nor an image URL is configured for the size dimension.</span></span> <span data-ttu-id="3c667-122">Derfor vises tekst.</span><span class="sxs-lookup"><span data-stu-id="3c667-122">Therefore, text is shown.</span></span>

    ![Eksempel på fargedimensjonen som vises som prøver på en produktdetaljside for e-handel](./dev-itpro/media/swatch_pdp.png)

- <span data-ttu-id="3c667-124">**Dimensjoner som skal vises i produktkortet** – Angi hvilke dimensjoner som skal vises på produktkort som vises i lister og på listesider.</span><span class="sxs-lookup"><span data-stu-id="3c667-124">**Dimensions to display in product card** – Specify which dimensions should appear on product cards that are shown in lists and on list pages.</span></span> <span data-ttu-id="3c667-125">Før en dimensjon kan vises på et produktkort, må denne innstillingen være aktivert for denne dimensjonen.</span><span class="sxs-lookup"><span data-stu-id="3c667-125">Before a dimension can appear on a product card, this setting must be enabled for that dimension.</span></span> <span data-ttu-id="3c667-126">Innstillingen **Dimensjoner som skal vises som bilde** bør også være aktivert.</span><span class="sxs-lookup"><span data-stu-id="3c667-126">The **Dimensions to display as image** setting should also be enabled.</span></span> <span data-ttu-id="3c667-127">Virkemåten for valg av prøve på produktkort er optimert for fargedimensjonen.</span><span class="sxs-lookup"><span data-stu-id="3c667-127">The swatch selection behavior on product cards is optimized for the color dimension.</span></span> <span data-ttu-id="3c667-128">For andre dimensjoner kan det være nødvendig å angi et visningstillegg for å tilpasse virkemåten for valg av prøve.</span><span class="sxs-lookup"><span data-stu-id="3c667-128">For other dimensions, a view extension might be required to customize swatch selection behavior.</span></span>

    <span data-ttu-id="3c667-129">Illustrasjonen nedenfor viser et eksempel der en listeside på et e-handelområde inneholder produktkort som inneholder fargeprøver.</span><span class="sxs-lookup"><span data-stu-id="3c667-129">The following illustration shows an example where a list page on an e-commerce site contains product cards that include color swatches.</span></span>

    ![Eksempel på fargedimensjonen som vises som prøver på en listeside for e-handel](./dev-itpro/media/swatch_searchresults.PNG)

<span data-ttu-id="3c667-131">Hvis du vil ha mer informasjon om hvordan du konfigurerer produktdimensjoner slik at de vises som prøver på områdesider, kan du se [Konfigurere produktdimensjonsverdier som skal vises som prøver](./dev-itpro/dimensions-swatch.md).</span><span class="sxs-lookup"><span data-stu-id="3c667-131">For information about how to configure product dimensions so that they are shown as swatches on site pages, see [Configure product dimension values to appear as swatches](./dev-itpro/dimensions-swatch.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3c667-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3c667-132">Additional resources</span></span>

[<span data-ttu-id="3c667-133">Oversikt over modulbibliotek</span><span class="sxs-lookup"><span data-stu-id="3c667-133">Module library overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="3c667-134">Modul for søkeresultater</span><span class="sxs-lookup"><span data-stu-id="3c667-134">Search results module</span></span>](search-result-module.md)

[<span data-ttu-id="3c667-135">Kjøpsboksmodul</span><span class="sxs-lookup"><span data-stu-id="3c667-135">Buy box module</span></span>](add-buy-box.md)

[<span data-ttu-id="3c667-136">Konfigurere produktdimensjonsverdier som skal vises som prøver</span><span class="sxs-lookup"><span data-stu-id="3c667-136">Configure product dimension values to appear as swatches</span></span>](./dev-itpro/dimensions-swatch.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
