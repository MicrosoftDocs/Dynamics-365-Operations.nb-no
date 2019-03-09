---
title: Lageroppslag på salgsstedet
description: Dette emnet beskriver alternativene som er tilgjengelige for å vise lagerinformasjon på salgsstedet (POS).
author: ashishmsft
manager: AnnBe
ms.date: 03/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application update 5, AX 8.0
ms.openlocfilehash: cd2dc460c9e862503ebbf1942dcf998d67829d86
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "314423"
---
# <a name="inventory-lookup-in-the-point-of-sale-pos"></a><span data-ttu-id="30194-103">Lageroppslag på salgsstedet</span><span class="sxs-lookup"><span data-stu-id="30194-103">Inventory lookup in the point of sale (POS)</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="30194-104">Lageroppslag på salgsstedet gjør det enklere for forhandlere å oppnå driftskvalitet i sanntid og få innsikt ved å koble sammen butikker, salgssted og back office.</span><span class="sxs-lookup"><span data-stu-id="30194-104">Inventory lookup in the point of sale (POS) helps retailers achieve real-time operational excellence and gain insights by connecting stores, the POS, and the back office.</span></span> <span data-ttu-id="30194-105">Denne funksjonaliteten gir nøyaktig sanntidsvisning av produktlageret på tvers av butikker og distribusjonssentre.</span><span class="sxs-lookup"><span data-stu-id="30194-105">This functionality provides an accurate real-time view of product inventory across stores and distribution centers.</span></span> <span data-ttu-id="30194-106">Den hjelper også forhandlerne med å øke effektiviteten og kostnadsbesparelsene ved å forbedre lagerplanlegging i sanntid.</span><span class="sxs-lookup"><span data-stu-id="30194-106">It also helps retailers drive additional efficiencies and cost savings by improving inventory planning in real time.</span></span>

<span data-ttu-id="30194-107">En nøyaktig sanntidsvisning av lageret i en organisasjon hjelper butikkansatte med å gi en rask og god kundeservice.</span><span class="sxs-lookup"><span data-stu-id="30194-107">An accurate real-time view of inventory across an organization helps store associates provide timely, superior customer service.</span></span> <span data-ttu-id="30194-108">Øyeblikket som betyr mest, er når kunden er klar til å ta en kjøpsbeslutning.</span><span class="sxs-lookup"><span data-stu-id="30194-108">The moment that matters most is the moment when the customer is ready to make a purchase decision.</span></span> <span data-ttu-id="30194-109">Det er viktig at kasserere i butikken har sanntidsinformasjon om lageret lett tilgjengelig, slik at de kan gi riktig informasjon om produktlevering og plukking.</span><span class="sxs-lookup"><span data-stu-id="30194-109">It's important that cashiers in the store have real-time inventory information at their fingertips, so that they can accurately promise product delivery and pickup.</span></span>

<span data-ttu-id="30194-110">Du kan åpne **Lageroppslag**-siden fra **Retail Modern POS**-arbeidsområdet eller **Retail Cloud POS**-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="30194-110">You can open the **Inventory lookup** page from the **Retail Modern POS** workspace or the **Retail Cloud POS** workspace.</span></span>

![Lageroppslag-flisen på hjemmesiden for salgssted](media/POSHomepage.png)

<span data-ttu-id="30194-112">På **Lageroppslag**-siden kan du kan bruke det numeriske tastaturet til å angi et produktnummer.</span><span class="sxs-lookup"><span data-stu-id="30194-112">On the **Inventory lookup** page, you can use the numeric keyboard to enter a product number.</span></span> <span data-ttu-id="30194-113">Du kan deretter vise antallet på lager for flere butikker og lagre.</span><span class="sxs-lookup"><span data-stu-id="30194-113">You can then view the on-hand quantity for multiple stores and warehouses.</span></span>

![Oppslagsiden for standardoppsett](media/InventoryLookUp.png)

<span data-ttu-id="30194-115">Antall for **Reservert** og **Bestilt** vises også for hver lokasjon.</span><span class="sxs-lookup"><span data-stu-id="30194-115">**Reserved** and **Ordered** quantities are also shown for each location.</span></span>

- <span data-ttu-id="30194-116">**Reservert** – Dette antallet refererer til **Fysisk reservert**-verdien fra back office for det angitte produktnummeret på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="30194-116">**Reserved** – This quantity refers to the **Physical reserved** value from the back office for the specified product number at the location.</span></span>
- <span data-ttu-id="30194-117">**Bestilt** – Dette antallet refererer til **Bestilt i alt**-verdien fra back office for det angitte produktnummeret på lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="30194-117">**Ordered** – This quantity refers to the **Ordered in total** value from the back office for the specified product number at the location.</span></span>

## <a name="locations-that-inventory-availability-information-is-shown-for"></a><span data-ttu-id="30194-118">Lokasjoner som lagertilgjengelighetsinformasjon vises for</span><span class="sxs-lookup"><span data-stu-id="30194-118">Locations that inventory availability information is shown for</span></span>

<span data-ttu-id="30194-119">Listen over lokasjoner inneholder to typer enheter:</span><span class="sxs-lookup"><span data-stu-id="30194-119">The list of locations includes two types of entities:</span></span>

- <span data-ttu-id="30194-120">**Detaljhandelbutikker** – Listen viser butikkene som er konfigurert ved hjelp av butikklokatorgruppen for gjeldende butikk i detaljhandelshovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="30194-120">**Retail stores** – The list shows stores that are configured by using the store locator group for the current store in the Retail headquarters.</span></span>
- <span data-ttu-id="30194-121">**Distribusjonssentre** – Forskjellige typer distribusjonssentre (for eksempel lagre) kan konfigureres i Microsoft Dynamics 365 for Retail.</span><span class="sxs-lookup"><span data-stu-id="30194-121">**Distribution centers** – Various types of distribution centers (such as warehouses) can be configured in Microsoft Dynamics 365 for Retail.</span></span> <span data-ttu-id="30194-122">Listen viser imidlertid bare informasjon om tilgjengelig lager for distribusjonssentre av standardtypen **Standard**.</span><span class="sxs-lookup"><span data-stu-id="30194-122">However, the list shows inventory availability information only for distribution centers of the **Standard** default type.</span></span>

    > [!NOTE]
    > <span data-ttu-id="30194-123">Informasjon om lagertilgjengelighet vises ikke for lagre av typen **Transitt**, **Karantene** og **Varer i ruten** for salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="30194-123">Inventory availability information isn't shown for warehouses of the **Transit**, **Quarantine**, and **Goods in Route** types for the POS.</span></span>

<span data-ttu-id="30194-124">På **Lageroppslag**-siden kan du vise tilgjengelig for ordre (ATP)-antall for hver butikk, i tillegg til gjeldende lagerbeholdningsantall, reservert antall og bestilt antall.</span><span class="sxs-lookup"><span data-stu-id="30194-124">On the **Inventory lookup** page, you can view available to promise (ATP) quantities for each store, in addition to the current on-hand quantities, reserved quantities, and ordered quantities.</span></span> <span data-ttu-id="30194-125">Velg butikken du vil vise informasjon om ATP for, og velg deretter **Vis butikktilgjengelighet**.</span><span class="sxs-lookup"><span data-stu-id="30194-125">Select the store to view the ATP information for, and then select **Show store availability**.</span></span>

![ATP-antall](media/ATP.png)

## <a name="opening-the-dimension-based-matrix-view-to-show-all-variants"></a><span data-ttu-id="30194-127">Åpne dimensjonsbasert matrisevisning for å vise alle varianter</span><span class="sxs-lookup"><span data-stu-id="30194-127">Opening the Dimension based matrix view to show all variants</span></span>

<span data-ttu-id="30194-128">På **Produktdetaljer**-siden i en produktstandard eller på **Lageroppslag**-siden velger du **Vis alle varianter** fra programfeltet nederst på siden.</span><span class="sxs-lookup"><span data-stu-id="30194-128">On the **Product details** page of a product master, or on the **Inventory lookup** page, select **View all variants** from the app-bar at bottom of the page.</span></span> <span data-ttu-id="30194-129">**Dimensjonsbasert matrise**-visningen for den første oppstarten fra disse sidene viser lagertilgjengelighetsinformasjon for alle varianter av et produkt for gjeldende butikk.</span><span class="sxs-lookup"><span data-stu-id="30194-129">The **Dimension based matrix** view for the initial launch from these pages shows the inventory availability information for all variants of a product for the current store.</span></span>

> [!NOTE]
> <span data-ttu-id="30194-130">**Vis alle varianter**-knappen er bare tilgjengelig for vareproduktstandarder som har produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="30194-130">The **View all variants** button is available only for item product masters that have product variants.</span></span> <span data-ttu-id="30194-131">Den er ikke tilgjengelig for frittstående produkter eller pakker.</span><span class="sxs-lookup"><span data-stu-id="30194-131">It isn't available for standalone products or kits.</span></span>

![Vis alle varianter-knappen på Lageroppslag-siden](media/StandardToMatrix.png)

<span data-ttu-id="30194-133">Velg **Vis alle varianter** på **Produktdetaljer**-siden i en produktstandard, eller på **Lageroppslag**-siden, uten å velge en plassering, for å gå til **Dimensjonsbasert matrise**-visningen og vise lagertilgjengelighetsinformasjon for alle varianter av et produkt for gjeldende butikk.</span><span class="sxs-lookup"><span data-stu-id="30194-133">Select **View all variants** on the **Product details** page of a product master, or on the **Inventory lookup** page, without selecting a location, to go to the **Dimension based matrix** view to view the inventory availability information for all variants of a product for the current store.</span></span>

![Dimensjonsbasert matrisevisning for Lageroppslag-siden](media/Matrix.png)

> [!NOTE]
> <span data-ttu-id="30194-135">I forrige illustrasjon er visningsrekkefølgen for dimensjonene alfabetisk, fordi visningsrekkefølgen for dimensjoner ikke ble konfigurert for det valgte produktet.</span><span class="sxs-lookup"><span data-stu-id="30194-135">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="30194-136">I **Dimensjonsbasert matrise**-visningen inkluderer cellene for produktvariantene en beholdningsverdi i nedre høyre hjørne.</span><span class="sxs-lookup"><span data-stu-id="30194-136">In the **Dimension based matrix** view, the cells for the product variants include an on-hand value in the lower-right corner.</span></span> <span data-ttu-id="30194-137">Tabellen nedenfor forklarer betydningen av ulike verdier.</span><span class="sxs-lookup"><span data-stu-id="30194-137">The following table explains the meaning of the various values.</span></span>

| <span data-ttu-id="30194-138">Beholdningsverdi</span><span class="sxs-lookup"><span data-stu-id="30194-138">On-hand value</span></span>                            | <span data-ttu-id="30194-139">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="30194-139">Description</span></span> |
|------------------------------------------|-------------|
| <span data-ttu-id="30194-140">Numerisk verdi som er større enn 0 (null)</span><span class="sxs-lookup"><span data-stu-id="30194-140">Numeric value that is more than 0 (zero)</span></span> | <span data-ttu-id="30194-141">En variant er frigitt til den valgte plasseringen, og du kan utføre flere handlinger i cellen.</span><span class="sxs-lookup"><span data-stu-id="30194-141">A variant has been released to the selected location, and you can perform additional actions in the cell.</span></span> <span data-ttu-id="30194-142">(Disse handlingene beskrives nærmere i senere i dette emnet.)</span><span class="sxs-lookup"><span data-stu-id="30194-142">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="30194-143">**0** (null)</span><span class="sxs-lookup"><span data-stu-id="30194-143">**0** (zero)</span></span>                             | <span data-ttu-id="30194-144">En variant er frigitt til den valgte plasseringen, men varen er ikke tilgjengelig på den valgte plasseringen.</span><span class="sxs-lookup"><span data-stu-id="30194-144">A variant has been released to the selected location, but the item isn't available in selected location.</span></span> <span data-ttu-id="30194-145">Du kan imidlertid utføre flere handlinger i cellen.</span><span class="sxs-lookup"><span data-stu-id="30194-145">However, you can perform additional actions in the cell.</span></span> <span data-ttu-id="30194-146">(Disse handlingene beskrives nærmere i senere i dette emnet.)</span><span class="sxs-lookup"><span data-stu-id="30194-146">(These actions are described in more detail later in this topic.)</span></span> |
| <span data-ttu-id="30194-147">**i/t** eller en inaktiv celle</span><span class="sxs-lookup"><span data-stu-id="30194-147">**n/a** or an inactive cell</span></span>              | <span data-ttu-id="30194-148">En variant er ikke frigitt til den valgte plasseringen, og du kan ikke utføre flere handlinger i cellen.</span><span class="sxs-lookup"><span data-stu-id="30194-148">A variant hasn't been released to the selected location, and you can't perform additional actions in the cell.</span></span> |

<span data-ttu-id="30194-149">Du kan også endre pivot for dimensjoner ved å velge den nye dimensjonen som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="30194-149">You can also change the pivot for dimensions by selecting the new dimension to use.</span></span>

![Endre pivot](media/ChangePivot.png)

![Pivot endret](media/PivotChanged.png)

> [!NOTE]
> <span data-ttu-id="30194-152">I de foregående illustrasjonene er visningsrekkefølgen for dimensjonene for det valgte produktet egendefinert (ikke-alfabetisk).</span><span class="sxs-lookup"><span data-stu-id="30194-152">In the preceding illustrations, the display order of the dimensions for the selected product is custom (non-alphabetic).</span></span> <span data-ttu-id="30194-153">Den er basert på visningsrekkefølgen for dimensjoner som er angitt i back office.</span><span class="sxs-lookup"><span data-stu-id="30194-153">It's based on the dimension display order that is set in the back office.</span></span>

<span data-ttu-id="30194-154">I tillegg i **Dimensjonsbasert matrise**-visningen kan flere handlinger utføres og bidra til å øke produktiviteten til butikkmedarbeidere.</span><span class="sxs-lookup"><span data-stu-id="30194-154">Additionally, in the **Dimension based matrix** view, more actions can be performed to help boost a store associate's productivity.</span></span> <span data-ttu-id="30194-155">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="30194-155">Here are some examples:</span></span>

- <span data-ttu-id="30194-156">Endre butikkplasseringen for å slå opp varetilgjengeligheten til alle produktvarianter på andre lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="30194-156">Change the store location to look up the inventory availability of all product variants at other locations.</span></span> <span data-ttu-id="30194-157">Disse plasseringene inkluderer andre butikker i butikklokatorgruppen og distribusjonssentrene for standardtypen **Standard**.</span><span class="sxs-lookup"><span data-stu-id="30194-157">These locations include other stores in the store locator group and distribution centers of the **Standard** default type.</span></span>
- <span data-ttu-id="30194-158">Selg en individuell produktvariant til en kunde ved hjelp av hentesalg, henting i butikken eller levering til en adresse.</span><span class="sxs-lookup"><span data-stu-id="30194-158">Sell an individual product variant to a customer by using cash and carry, in-store pickup, or shipment to an address.</span></span>
- <span data-ttu-id="30194-159">Gi kunden ATP-informasjon for en enkelt produktvariant på et bestemt sted.</span><span class="sxs-lookup"><span data-stu-id="30194-159">Provide the customer with ATP information for an individual product variant at a specific location.</span></span>

![Flere handlinger på variantfliser](media/VariantActions.png)

> [!NOTE]
> <span data-ttu-id="30194-161">I forrige illustrasjon er visningsrekkefølgen for dimensjonene alfabetisk, fordi visningsrekkefølgen for dimensjoner ikke ble konfigurert for det valgte produktet.</span><span class="sxs-lookup"><span data-stu-id="30194-161">In the preceding illustration, the display order of the dimensions is alphabetic, because the display order of dimensions wasn't configured for the selected product.</span></span>

<span data-ttu-id="30194-162">Tabellen nedenfor inneholder mer informasjon om flere handlinger som er tilgjengelige.</span><span class="sxs-lookup"><span data-stu-id="30194-162">The following table provides more information about the additional actions that are available.</span></span>

| <span data-ttu-id="30194-163">Handling</span><span class="sxs-lookup"><span data-stu-id="30194-163">Action</span></span>               | <span data-ttu-id="30194-164">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="30194-164">Description</span></span> |
|----------------------|-------------|
| <span data-ttu-id="30194-165">Selg nå</span><span class="sxs-lookup"><span data-stu-id="30194-165">Sell now</span></span>             | <span data-ttu-id="30194-166">Legg til den valgte varevarianten i transaksjonen, og omdiriger brukeren til skjermbildet for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="30194-166">Add the selected item variant to the transaction, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="30194-167">(Denne handlingen er ikke tilgjengelig når den valgte plasseringen er et distribusjonssenter.)</span><span class="sxs-lookup"><span data-stu-id="30194-167">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="30194-168">Hent i butikk</span><span class="sxs-lookup"><span data-stu-id="30194-168">Pick up in store</span></span>     | <span data-ttu-id="30194-169">Opprett en kundeordre for produktvarianten som plukkes fra den valgte plasseringen, og omdiriger brukeren til skjermbildet for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="30194-169">Create a customer order for the product variant that will be picked up from the selected location, and redirect the user to the transaction screen.</span></span> <span data-ttu-id="30194-170">(Denne handlingen er ikke tilgjengelig når den valgte plasseringen er et distribusjonssenter.)</span><span class="sxs-lookup"><span data-stu-id="30194-170">(This action isn't available when the selected location is a distribution center.)</span></span> |
| <span data-ttu-id="30194-171">Send produkt</span><span class="sxs-lookup"><span data-stu-id="30194-171">Ship product</span></span>         | <span data-ttu-id="30194-172">Opprett en kundeordre for produktvarianten som sendes fra den valgte plasseringen, og omdiriger brukeren til skjermbildet for transaksjonen.</span><span class="sxs-lookup"><span data-stu-id="30194-172">Create a customer order for the product variant that will be shipped from the selected location, and redirect the user to the transaction screen.</span></span> |
| <span data-ttu-id="30194-173">Tilgjengelighet</span><span class="sxs-lookup"><span data-stu-id="30194-173">Availability</span></span>         | <span data-ttu-id="30194-174">Vis ATP-informasjonen for den valgte variantkombinasjonen for det valgte stedet.</span><span class="sxs-lookup"><span data-stu-id="30194-174">Show the ATP information for the selected variant combination for the selected location.</span></span> |
| <span data-ttu-id="30194-175">Vis alle lokasjoner</span><span class="sxs-lookup"><span data-stu-id="30194-175">Show all locations</span></span>   | <span data-ttu-id="30194-176">Bytt til visningen for standard lageroppslag, og uthev lagertilgjengelighetsinformasjon for varevarianten i alle butikkene i butikklokatorgruppen, og også i distribusjonssentre av typen **Standard**.</span><span class="sxs-lookup"><span data-stu-id="30194-176">Switch to the standard inventory lookup view, and highlight inventory availability information for the item variant across all stores in the store locator group, and also in distribution centers of the **Standard/Default** type.</span></span> |
| <span data-ttu-id="30194-177">Vis produktdetaljer</span><span class="sxs-lookup"><span data-stu-id="30194-177">View product details</span></span> | <span data-ttu-id="30194-178">Omdiriger brukeren til **Produktdetaljer**-siden for den tilknyttede produktstandarden.</span><span class="sxs-lookup"><span data-stu-id="30194-178">Redirect the user to the **Product details** page of the associated product master.</span></span> |
