---
title: Arbeidspolicyer
description: Dette emnet forklarer hvordan du konfigurerer arbeidspolicyer.
author: perlynne
ms.date: 07/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSWorkPolicy
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 39a9ba00763fac220eff16bdd42aa07cc8e35ba4
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5838136"
---
# <a name="work-policies"></a><span data-ttu-id="cc68a-103">Arbeidspolicyer</span><span class="sxs-lookup"><span data-stu-id="cc68a-103">Work policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cc68a-104">Dette emnet forklarer hvordan du konfigurerer systemet og mobilappen Lagerstyring slik at de har støtte for arbeidspolicyer.</span><span class="sxs-lookup"><span data-stu-id="cc68a-104">This topic explains how to set up the system and the Warehouse Management mobile app so that they support work policies.</span></span> <span data-ttu-id="cc68a-105">Du kan bruke denne funksjonaliteten til raskt å registrere beholdning uten å opprette plasseringsarbeid når du mottar bestillinger eller overføringsordrer, eller når du fullfører produksjonsprosesser.</span><span class="sxs-lookup"><span data-stu-id="cc68a-105">You can use this functionality to quickly register inventory without creating putaway work when you receive purchase or transfer orders, or when you complete manufacturing processes.</span></span> <span data-ttu-id="cc68a-106">Dette emnet gir generell informasjon.</span><span class="sxs-lookup"><span data-stu-id="cc68a-106">This topic provides general information.</span></span> <span data-ttu-id="cc68a-107">For detaljert informasjon som gjelder nummerskiltmottak, kan du se [Nummerskiltmottak via mobilappen Lagerstyring](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="cc68a-107">For detailed information that is related to license plate receiving, see [License plate receiving via the Warehouse Management mobile app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="cc68a-108">En arbeidspolicy kontrollerer om lagerarbeid opprettes når en produsert vare rapporteres som ferdig, eller når varer mottas ved hjelp av mobilappen Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="cc68a-108">A work policy controls whether warehouse work is created when a manufactured item is reported as finished, or when goods are received by using the Warehouse Management mobile app.</span></span> <span data-ttu-id="cc68a-109">Du definerer hver arbeidspolicy ved å definere betingelsene der den gjelder: arbeidsordretypene og -prosessene, beholdningslokasjonen og (eventuelt) produktene.</span><span class="sxs-lookup"><span data-stu-id="cc68a-109">You set up each work policy by defining the conditions where it applies: the work order types and processes, the inventory location, and (optionally) the products.</span></span> <span data-ttu-id="cc68a-110">For eksempel må en bestilling for produkt *A0001* mottas i lokasjonen *RECV* på lager *24*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-110">For example, a purchase order for product *A0001* must be received in location *RECV* in warehouse *24*.</span></span> <span data-ttu-id="cc68a-111">Senere forbrukes produktet i en annen prosess på lokasjonen *RECV*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-111">Later, the product is consumed in another process at location *RECV*.</span></span> <span data-ttu-id="cc68a-112">I dette tilfellet kan du definere en arbeidspolicy for å hindre at plasseringsarbeid blir opprettet når en arbeider rapporterer produkt *A0001* som mottatt på lokasjonen *RECV*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-112">In this case, you can set up a work policy to prevent putaway work from being created when a worker reports product *A0001* as received in location *RECV*.</span></span>

> [!NOTE]
> - <span data-ttu-id="cc68a-113">Hvis en arbeidspolicy skal være aktiv, må du definere minst én lokasjon for den på hurtigfanen **Lagerlokasjoner** på siden **Arbeidspolicyer**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-113">For a work policy to be active, you must define at least one location for it on the **Inventory locations** FastTab of the **Work policies** page.</span></span> 
> - <span data-ttu-id="cc68a-114">Du kan ikke angi samme plassering for flere arbeidspolicyer.</span><span class="sxs-lookup"><span data-stu-id="cc68a-114">You can't specify the same location for multiple work policies.</span></span>
> - <span data-ttu-id="cc68a-115">Alternativet **Skriv ut etikett** for menyelementer på mobilenheter skriver ikke ut en nummerskiltetikett med mindre arbeid er opprettet.</span><span class="sxs-lookup"><span data-stu-id="cc68a-115">The **Print label** option for mobile device menu items won't print a license plate label unless work was created.</span></span>

## <a name="activate-the-features-in-your-system"></a><span data-ttu-id="cc68a-116">Aktivere funksjonene i systemet</span><span class="sxs-lookup"><span data-stu-id="cc68a-116">Activate the features in your system</span></span>

<span data-ttu-id="cc68a-117">Hvis du vil gjøre all funksjonalitet som er beskrevet i dette emnet, tilgjengelig i systemet, kan du aktivere følgende to funksjoner i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span><span class="sxs-lookup"><span data-stu-id="cc68a-117">To make all the functionality that is described in this topic available in your system, turn on the following two features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md):</span></span>

- <span data-ttu-id="cc68a-118">Forbedringer av mottak av nummerskilter</span><span class="sxs-lookup"><span data-stu-id="cc68a-118">License plate receiving enhancements</span></span>
- <span data-ttu-id="cc68a-119">Forbedringer for arbeidspolicy for innkommende arbeid</span><span class="sxs-lookup"><span data-stu-id="cc68a-119">Work policy enhancements for inbound work</span></span>

## <a name="the-work-policies-page"></a><span data-ttu-id="cc68a-120">Siden Arbeidspolicyer</span><span class="sxs-lookup"><span data-stu-id="cc68a-120">The Work policies page</span></span>

<span data-ttu-id="cc68a-121">Når du skal definere arbeidspolicyer, går du til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidspolicyer**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-121">To set up work policies, go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span> <span data-ttu-id="cc68a-122">Deretter angir du feltene som beskrevet i følgende underdeler, på hver hurtigfane.</span><span class="sxs-lookup"><span data-stu-id="cc68a-122">Then, on each FastTab, set the fields as described in the following subsections.</span></span>

### <a name="the-work-order-types-fasttab"></a><span data-ttu-id="cc68a-123">Hurtigfanen Arbeidsordretyper</span><span class="sxs-lookup"><span data-stu-id="cc68a-123">The Work order types FastTab</span></span>

<span data-ttu-id="cc68a-124">På hurtigfanen **Arbeidsordretyper** legger du til alle arbeidsordretyper og de tilknyttede arbeidsprosessene som arbeidspolicyen gjelder for.</span><span class="sxs-lookup"><span data-stu-id="cc68a-124">On the **Work order types** FastTab, add all the work order types, and the related work processes, that the work policy applies to.</span></span> <span data-ttu-id="cc68a-125">Følgende arbeidsordretyper og relaterte arbeidsprosesser støttes for arbeidspolicyer.</span><span class="sxs-lookup"><span data-stu-id="cc68a-125">The following work order types and related work processes are supported for work policies.</span></span>

| <span data-ttu-id="cc68a-126">Arbeidsordretype</span><span class="sxs-lookup"><span data-stu-id="cc68a-126">Work order type</span></span> | <span data-ttu-id="cc68a-127">Arbeidsprosess</span><span class="sxs-lookup"><span data-stu-id="cc68a-127">Work process</span></span> |
|---|---|
| <span data-ttu-id="cc68a-128">Råvareplukking</span><span class="sxs-lookup"><span data-stu-id="cc68a-128">Raw material picking</span></span>| <span data-ttu-id="cc68a-129">Alle relaterte prosesser</span><span class="sxs-lookup"><span data-stu-id="cc68a-129">All related processes</span></span> |
| <span data-ttu-id="cc68a-130">Plasser koprodukt og biprodukt</span><span class="sxs-lookup"><span data-stu-id="cc68a-130">Co-product and by-product put away</span></span> | <span data-ttu-id="cc68a-131">Alle relaterte prosesser</span><span class="sxs-lookup"><span data-stu-id="cc68a-131">All related processes</span></span> |
| <span data-ttu-id="cc68a-132">Plasser ferdigvarer</span><span class="sxs-lookup"><span data-stu-id="cc68a-132">Finished goods putaway</span></span> | <span data-ttu-id="cc68a-133">Alle relaterte prosesser</span><span class="sxs-lookup"><span data-stu-id="cc68a-133">All related processes</span></span> |
| <span data-ttu-id="cc68a-134">Overføringsmottak</span><span class="sxs-lookup"><span data-stu-id="cc68a-134">Transfer receipt</span></span> | <span data-ttu-id="cc68a-135">Mottak (og plassering) av nummerskilt</span><span class="sxs-lookup"><span data-stu-id="cc68a-135">License plate receiving (and putaway)</span></span> |
| <span data-ttu-id="cc68a-136">Bestillinger</span><span class="sxs-lookup"><span data-stu-id="cc68a-136">Purchase orders</span></span> | <ul><li><span data-ttu-id="cc68a-137">Mottak (og plassering) av nummerskilt</span><span class="sxs-lookup"><span data-stu-id="cc68a-137">License plate receiving (and putaway)</span></span></li><li><span data-ttu-id="cc68a-138">Mottak (og plassering) av lastvare</span><span class="sxs-lookup"><span data-stu-id="cc68a-138">Load item receiving (and putaway)</span></span></li><li><span data-ttu-id="cc68a-139">Mottak (og plassering) av bestillingslinje</span><span class="sxs-lookup"><span data-stu-id="cc68a-139">Purchase order line receiving (and putaway)</span></span></li><li><span data-ttu-id="cc68a-140">Mottak (og plassering) av bestillingsvarer</span><span class="sxs-lookup"><span data-stu-id="cc68a-140">Purchase order item receiving (and putaway)</span></span></li></ul> |

<span data-ttu-id="cc68a-141">Hvis du vil definere en arbeidspolicy slik at den gjelder flere arbeidsprosesser i samme arbeidsordretype, legger du til en egen linje for hver arbeidsprosess i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="cc68a-141">To set up a work policy so that it applies to several work processes of the same work order type, add a separate line for each work process to the grid.</span></span>

<span data-ttu-id="cc68a-142">For hver linje i rutenettet angir du feltet **Arbeidsopprettelsesmetode** til én av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="cc68a-142">For each line in the grid, set the **Work creation method** field to one of the following values:</span></span>

- <span data-ttu-id="cc68a-143">**Aldri** – Arbeidspolicyen hindrer at lagerarbeid opprettes for den valgte arbeidsordretypen og den relaterte arbeidsprosessen.</span><span class="sxs-lookup"><span data-stu-id="cc68a-143">**Never** – The work policy will prevent warehouse work from being created for the selected work order type and related work process.</span></span>
- <span data-ttu-id="cc68a-144">**Direkteoverføring** – Arbeidspolicyen vil opprette direkteoverføringsarbeid ved hjelp av policyen du velger i feltet **Navn på direkteoverføringspolicy**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-144">**Cross docking** – The work policy will create cross-docking work by using the policy that you select in the **Cross docking policy name** field.</span></span>

### <a name="the-inventory-locations-fasttab"></a><span data-ttu-id="cc68a-145">Hurtigfanen Lagerlokasjoner</span><span class="sxs-lookup"><span data-stu-id="cc68a-145">The Inventory locations FastTab</span></span>

<span data-ttu-id="cc68a-146">På hurtigfanen **Lagerlokasjoner** legger du til alle lokasjoner der denne arbeidspolicyen skal brukes.</span><span class="sxs-lookup"><span data-stu-id="cc68a-146">On the **Inventory locations** FastTab, add all the locations where this work policy should be applied.</span></span> <span data-ttu-id="cc68a-147">Hvis ingen lokasjon er knyttet til en arbeidspolicy, brukes ikke arbeidspolicyen for noen prosesser.</span><span class="sxs-lookup"><span data-stu-id="cc68a-147">If no location is associated with a work policy, the work policy won't be applied to any process.</span></span>

<span data-ttu-id="cc68a-148">Du kan ikke angi samme plassering for flere arbeidspolicyer.</span><span class="sxs-lookup"><span data-stu-id="cc68a-148">You can't specify the same location for multiple work policies.</span></span>

<span data-ttu-id="cc68a-149">Du kan bruke en lagerlokasjon som er tilordnet en lokasjonsprofil, der **Bruk sporing av nummerskilt** er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="cc68a-149">You can use a warehouse location that is assigned to a location profile where the **Use license plate tracking** option is turned off.</span></span> <span data-ttu-id="cc68a-150">I dette tilfellet vil arbeidere registrere lagerbeholdningen direkte.</span><span class="sxs-lookup"><span data-stu-id="cc68a-150">In this case, workers will directly register the on-hand inventory.</span></span>

### <a name="the-products-fasttab"></a><span data-ttu-id="cc68a-151">Hurtigfanen Produkter</span><span class="sxs-lookup"><span data-stu-id="cc68a-151">The Products FastTab</span></span>

<span data-ttu-id="cc68a-152">På **Produkter**-fanen angir du feltet **Produktvalg** for å kontrollere hvilke produkter policyen skal gjelde for:</span><span class="sxs-lookup"><span data-stu-id="cc68a-152">On the **Products** tab, set the **Product selection** field to control which products the policy should apply to:</span></span>

- <span data-ttu-id="cc68a-153">**Alle** – Policyen skal gjelde for alle produkter.</span><span class="sxs-lookup"><span data-stu-id="cc68a-153">**All** – The policy should apply to all products.</span></span>
- <span data-ttu-id="cc68a-154">**Valgt** – Policyen skal bare gjelde for produkter som er oppført i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="cc68a-154">**Selected** – The policy should apply only to products that are listed in the grid.</span></span> <span data-ttu-id="cc68a-155">Bruk verktøylinjen på hurtigfanen **Produkter** til å legge til produkter i rutenettet eller fjerne dem fra rutenettet.</span><span class="sxs-lookup"><span data-stu-id="cc68a-155">Use the toolbar on the **Products** FastTab to add products to the grid or remove them from the grid.</span></span>

## <a name="default-and-custom-to-locations"></a><span data-ttu-id="cc68a-156">Standard og egendefinerte "til"-lokasjoner</span><span class="sxs-lookup"><span data-stu-id="cc68a-156">Default and custom "to" locations</span></span>

> [!NOTE]
> <span data-ttu-id="cc68a-157">Hvis du vil gjøre funksjonaliteten som er beskrevet i denne delen, tilgjengelig i systemet, må du aktivere funksjonene *Forbedringer for nummerskiltmottak* og *Arbeidspolicyforbedringer for innkommende arbeid* i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cc68a-157">To make the functionality that is described in this section available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="cc68a-158">Tidligere støttet systemet bare mottak på standardlokasjonen som er definert for hvert lager.</span><span class="sxs-lookup"><span data-stu-id="cc68a-158">Previously, the system supported receiving only at the default location that is defined for each warehouse.</span></span> <span data-ttu-id="cc68a-159">Menyelementer for mobilenheter som bruker følgende arbeidsprosesser, inneholder imidlertid nå alternativet **Bruk standarddata**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-159">However, mobile device menu items that use the following work creation processes now provide the **Use default data** option.</span></span> <span data-ttu-id="cc68a-160">Ved hjelp av dette alternativet kan du tilordne en egendefinert "til"-plassering til ett eller flere menyelementer.</span><span class="sxs-lookup"><span data-stu-id="cc68a-160">This option lets you assign a custom "to" location to one or more menu items.</span></span> <span data-ttu-id="cc68a-161">(Dette alternativet var allerede tilgjengelig for enkelte andre typer menyelementer.)</span><span class="sxs-lookup"><span data-stu-id="cc68a-161">(This option was already available for some other types of menu items.)</span></span>

- <span data-ttu-id="cc68a-162">Mottak (og plassering) av nummerskilt</span><span class="sxs-lookup"><span data-stu-id="cc68a-162">License plate receiving (and putaway)</span></span>
- <span data-ttu-id="cc68a-163">Mottak (og plassering) av lastvare</span><span class="sxs-lookup"><span data-stu-id="cc68a-163">Load item receiving (and putaway)</span></span>
- <span data-ttu-id="cc68a-164">Mottak (og plassering) av bestillingslinje</span><span class="sxs-lookup"><span data-stu-id="cc68a-164">Purchase order line receiving (and putaway)</span></span>
- <span data-ttu-id="cc68a-165">Mottak (og plassering) av bestillingsvarer</span><span class="sxs-lookup"><span data-stu-id="cc68a-165">Purchase order item receiving (and putaway)</span></span>

<span data-ttu-id="cc68a-166">Innstillingen **Til-plassering** for et menyelement overstyrer standard mottakslokasjon for lageret, for alle ordrer som er behandlet med dette menyelementet.</span><span class="sxs-lookup"><span data-stu-id="cc68a-166">The **To location** setting for a menu item overrides the default receiving location for the warehouse, for all orders that are processed by using that menu item.</span></span>

<span data-ttu-id="cc68a-167">Følg denne fremgangsmåten for å konfigurere et menyelement for en mobilenhet for å støtte mottak til en egendefinert plassering.</span><span class="sxs-lookup"><span data-stu-id="cc68a-167">To set up a mobile device menu item to support receiving at a custom location, follow these steps.</span></span>

1. <span data-ttu-id="cc68a-168">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-168">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="cc68a-169">Velg eller opprett et menyelement som bruker en av arbeidsopprettingsprosessene som er oppført tidligere i denne delen.</span><span class="sxs-lookup"><span data-stu-id="cc68a-169">Select or create a menu item that uses one of the work creation processes that are listed earlier in this section.</span></span>
1. <span data-ttu-id="cc68a-170">På **Generelt**-hurtigfanen angir du **Bruk standarddata**-alternativet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-170">On the **General** FastTab, set the **Use default data** option to **Yes**.</span></span>
1. <span data-ttu-id="cc68a-171">I handlingsruten velger du **Standarddata**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-171">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="cc68a-172">Angi følgende verdier på siden **Standarddata**:</span><span class="sxs-lookup"><span data-stu-id="cc68a-172">On the **Default data** page, set the following values:</span></span>

    - <span data-ttu-id="cc68a-173">**Feltet Standarddata:** Sett dette feltet til *Til lokasjon*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-173">**Default data field:** Set this field to *To location*.</span></span>
    - <span data-ttu-id="cc68a-174">**Lager:** Velg hvilket mållager som skal brukes med dette menyelementet.</span><span class="sxs-lookup"><span data-stu-id="cc68a-174">**Warehouse:** Select the destination warehouse to use with this menu item.</span></span>
    - <span data-ttu-id="cc68a-175">**Lokasjon:** Dette feltet inneholder alle lokasjons-ID-ene som er tilgjengelige for det valgte lageret.</span><span class="sxs-lookup"><span data-stu-id="cc68a-175">**Location:** This field lists all the location IDs that are available for the selected warehouse.</span></span> <span data-ttu-id="cc68a-176">Innstillingen i dette feltet har imidlertid ingen virkning.</span><span class="sxs-lookup"><span data-stu-id="cc68a-176">However, the setting of this field doesn't actually have any effect.</span></span> <span data-ttu-id="cc68a-177">Du kan derfor la det stå tomt.</span><span class="sxs-lookup"><span data-stu-id="cc68a-177">Therefore, you can leave it blank.</span></span> <span data-ttu-id="cc68a-178">Du kan likevel bruke listen til å bekrefte ID-en du må angi, i feltet **Hardkodet verdi**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-178">Nevertheless, you can use the list to confirm the ID that you must enter in the **Hardcoded value** field.</span></span>
    - <span data-ttu-id="cc68a-179">**Hardkodet verdi:** Angi lokasjons-ID-en for mottakslokasjonen som gjelder for dette menyelementet.</span><span class="sxs-lookup"><span data-stu-id="cc68a-179">**Hardcoded value:** Enter the location ID for the receiving location that applies to this menu item.</span></span>

> [!TIP]
> <span data-ttu-id="cc68a-180">En arbeidspolicy kan bare brukes hvis alle mottakslokasjonene er oppført i det relevante arbeidspolicyoppsettet.</span><span class="sxs-lookup"><span data-stu-id="cc68a-180">A work policy can be applied only if all the receiving locations are listed in the relevant work policy setup.</span></span> <span data-ttu-id="cc68a-181">Dette kravet gjelder uansett om du bruker standard lagermottakslokasjon eller en egendefinert "til"-lokasjon.</span><span class="sxs-lookup"><span data-stu-id="cc68a-181">This requirement applies regardless of whether you're using the default warehouse receiving location or a custom "to" location.</span></span>

## <a name="example-scenario-warehouse-receiving"></a><span data-ttu-id="cc68a-182">Eksempelscenario: Lagermottak</span><span class="sxs-lookup"><span data-stu-id="cc68a-182">Example scenario: Warehouse receiving</span></span>

<span data-ttu-id="cc68a-183">Alle produkter som mottas ved hjelp av prosessen *Mottak (og plassering) av bestillingsvare*, må registreres på lokasjonen *FL-001*, og de må være tilgjengelige på lager *24*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-183">All products that are received by the *Purchase order item receiving (and putaway)* process must be registered in location *FL-001*, and they must be available in warehouse *24*.</span></span> <span data-ttu-id="cc68a-184">Arbeid bør imidlertid ikke opprettes.</span><span class="sxs-lookup"><span data-stu-id="cc68a-184">However, work should not be created.</span></span> <span data-ttu-id="cc68a-185">Produkter som er mottatt av en annen prosess (det vil si ved hjelp av andre menyelementer for mobilenheter), bør registreres ved standard mottakslokasjon (*RECV*), og arbeid bør opprettes som vanlig.</span><span class="sxs-lookup"><span data-stu-id="cc68a-185">Products that are received by any other process (that is, by using other mobile device menu items) should be registered at the default warehouse receiving location (*RECV*), and work should be created as usual.</span></span> <span data-ttu-id="cc68a-186">(Dette scenariet viser ikke standard mottaksoppsett.)</span><span class="sxs-lookup"><span data-stu-id="cc68a-186">(This scenario doesn't show the default receiving setup.)</span></span>

<span data-ttu-id="cc68a-187">Dette scenariet krever følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="cc68a-187">This scenario requires the following elements:</span></span>

- <span data-ttu-id="cc68a-188">En arbeidspolicy for prosessen *Mottak (og plassering) av bestillingsvarer* på lokasjonen *FL-001* for alle produkter</span><span class="sxs-lookup"><span data-stu-id="cc68a-188">A work policy for the *Purchase order item receiving (and putaway)* process in location *FL-001*, for all products</span></span>
- <span data-ttu-id="cc68a-189">Menyelement på mobilenhet som har standarddata, og som setter feltet **Til-lokasjon** til *FL-001*</span><span class="sxs-lookup"><span data-stu-id="cc68a-189">A mobile device menu item that has default data, and that sets the **To location** field to *FL-001*</span></span>

### <a name="prerequisites"></a><span data-ttu-id="cc68a-190">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="cc68a-190">Prerequisites</span></span>

<span data-ttu-id="cc68a-191">Hvis du vil gjøre funksjonaliteten som er beskrevet i dette scenarioet, tilgjengelig i systemet, må du aktivere funksjonene *Forbedringer for nummerskiltmottak* og *Arbeidspolicyforbedringer for innkommende arbeid* i [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="cc68a-191">To make the functionality that is described in this scenario available in your system, you must turn on the *License plate receiving enhancements* and *Work policy enhancements for inbound work* features in [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

<span data-ttu-id="cc68a-192">Dette scenarioet bruker standard demonstrasjonsdata.</span><span class="sxs-lookup"><span data-stu-id="cc68a-192">This scenario uses the standard demo data.</span></span> <span data-ttu-id="cc68a-193">Hvis du vil arbeide deg gjennom det ved å bruke verdiene som presenteres her, må du derfor arbeide på et system der standard demodata er installert.</span><span class="sxs-lookup"><span data-stu-id="cc68a-193">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="cc68a-194">Du må også velge den juridiske enheten **USMF**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-194">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-work-policy"></a><span data-ttu-id="cc68a-195">Definere en arbeidspolicy</span><span class="sxs-lookup"><span data-stu-id="cc68a-195">Set up a work policy</span></span>

1. <span data-ttu-id="cc68a-196">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidspolicyer**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-196">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="cc68a-197">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-197">Select **New**.</span></span>
1. <span data-ttu-id="cc68a-198">I feltet **Arbeidspolicynavn** angir du *Ikke plasseringsarbeid for innkjøpsvare*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-198">In the **Work policy name** field, enter *No purchase item putaway work*.</span></span>
1. <span data-ttu-id="cc68a-199">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-199">Select **Save**.</span></span>
1. <span data-ttu-id="cc68a-200">På hurtigfanen **Arbeidsordretyper** velger du **Legg til** for å legge til en rad i rutenettet, og angi deretter følgende verdier for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="cc68a-200">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="cc68a-201">**Arbeidsordretype:** *Bestillinger*</span><span class="sxs-lookup"><span data-stu-id="cc68a-201">**Work order type:** *Purchase orders*</span></span>
    - <span data-ttu-id="cc68a-202">**Arbeidsprosess:** *Mottak (og plassering) av bestillingsvarer*</span><span class="sxs-lookup"><span data-stu-id="cc68a-202">**Work process:** *Purchase order item receiving (and putaway)*</span></span>
    - <span data-ttu-id="cc68a-203">**Arbeidsopprettelsesmetode:** *Aldri*</span><span class="sxs-lookup"><span data-stu-id="cc68a-203">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="cc68a-204">**Navn på direkteoverføringspolicy:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="cc68a-204">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="cc68a-205">På hurtigfanen **Lagerlokasjoner** velger du **Legg til** for å legge til en rad i rutenettet, og angi deretter følgende verdier for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="cc68a-205">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="cc68a-206">**Lager:** *24*</span><span class="sxs-lookup"><span data-stu-id="cc68a-206">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="cc68a-207">**Lokasjon:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="cc68a-207">**Location:** *FL-001*</span></span>

1. <span data-ttu-id="cc68a-208">På hurtigfanen **Produkter** angir du feltet **Produktvalg** til *Alle*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-208">On the **Products** FastTab, set the **Product selection** field to *All*.</span></span>
1. <span data-ttu-id="cc68a-209">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-209">Select **Save**.</span></span>

### <a name="set-up-a-mobile-device-menu-item-to-change-the-receiving-location"></a><span data-ttu-id="cc68a-210">Definere et menyelement for mobilenhet for å endre mottakslokasjonen</span><span class="sxs-lookup"><span data-stu-id="cc68a-210">Set up a mobile device menu item to change the receiving location</span></span>

1. <span data-ttu-id="cc68a-211">Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-211">Go to **Warehouse management \> Setup \> Mobile device \> Mobile device menu items**.</span></span>
1. <span data-ttu-id="cc68a-212">Velg det eksisterende menyelementet **Kjøpsmottak** i den venstre ruten.</span><span class="sxs-lookup"><span data-stu-id="cc68a-212">In the left pane, select the existing **Purchase receive** menu item.</span></span>
1. <span data-ttu-id="cc68a-213">På **Generelt**-hurtigfanen angir du **Bruk standarddata**-alternativet til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-213">On the **General** FastTab, set the **Use default data** option to *Yes*.</span></span>
1. <span data-ttu-id="cc68a-214">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-214">Select **Save**.</span></span>
1. <span data-ttu-id="cc68a-215">I handlingsruten velger du **Standarddata**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-215">On the Action Pane, select **Default data**.</span></span>
1. <span data-ttu-id="cc68a-216">På siden **Standarddata** velger du **Ny** i handlingsruten for å legge til en rad i rutenettet, og angi deretter følgende verdier for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="cc68a-216">On the **Default data** page, on the Action Pane, select **New** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="cc68a-217">**Feltet Standarddata:** *Til-plassering*</span><span class="sxs-lookup"><span data-stu-id="cc68a-217">**Default data field:** *To location*</span></span>
    - <span data-ttu-id="cc68a-218">**Lager:** *24*</span><span class="sxs-lookup"><span data-stu-id="cc68a-218">**Warehouse:** *24*</span></span>
    - <span data-ttu-id="cc68a-219">**Lokasjon:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="cc68a-219">**Location:** Leave this field blank.</span></span>
    - <span data-ttu-id="cc68a-220">**Hardkodet verdi:** *FL-001*</span><span class="sxs-lookup"><span data-stu-id="cc68a-220">**Hardcoded value:** *FL-001*</span></span>

1. <span data-ttu-id="cc68a-221">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-221">Select **Save**.</span></span>

### <a name="receive-a-purchase-order-without-creating-work"></a><span data-ttu-id="cc68a-222">Motta en bestilling uten å opprette arbeid</span><span class="sxs-lookup"><span data-stu-id="cc68a-222">Receive a purchase order without creating work</span></span>

<span data-ttu-id="cc68a-223">Eksemplet i denne delen viser hvordan du mottar en bestillingsvare, men uten å opprette arbeid, på en lokasjon som er forskjellig fra standard mottakslokasjon som er definert for lageret.</span><span class="sxs-lookup"><span data-stu-id="cc68a-223">The example in this section shows how to receive a purchase order item, but without creating work, at a location that differs from the default receiving location that is set up for the warehouse.</span></span> <span data-ttu-id="cc68a-224">Dette eksemplet bruker arbeidspolicyen og varen fra mobilenheten som du opprettet tidligere i dette scenariet.</span><span class="sxs-lookup"><span data-stu-id="cc68a-224">This example uses the work policy and mobile device item that you created earlier in this scenario.</span></span>

#### <a name="create-a-purchase-order"></a><span data-ttu-id="cc68a-225">Opprette en bestilling</span><span class="sxs-lookup"><span data-stu-id="cc68a-225">Create a purchase order</span></span>

1. <span data-ttu-id="cc68a-226">Gå til **Innkjøp og leverandører \> Bestillinger \> Alle bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-226">Go to **Procurement and sourcing \> Purchase orders \> All purchase orders**.</span></span>
1. <span data-ttu-id="cc68a-227">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-227">Select **New**.</span></span>
1. <span data-ttu-id="cc68a-228">I **Opprett bestilling**-dialogboksen angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="cc68a-228">In the **Create purchase order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="cc68a-229">**Leverandørkonto:** *US-101*</span><span class="sxs-lookup"><span data-stu-id="cc68a-229">**Vendor account:** *US-101*</span></span>
    - <span data-ttu-id="cc68a-230">**Område:** *2*</span><span class="sxs-lookup"><span data-stu-id="cc68a-230">**Site:** *2*</span></span>
    - <span data-ttu-id="cc68a-231">**Lager:** *24*</span><span class="sxs-lookup"><span data-stu-id="cc68a-231">**Warehouse:** *24*</span></span>

1. <span data-ttu-id="cc68a-232">Velg **OK** for å lukke dialogboksen og opprette den nye bestillingen.</span><span class="sxs-lookup"><span data-stu-id="cc68a-232">Select **OK** to close the dialog box and open the new purchase order.</span></span>
1. <span data-ttu-id="cc68a-233">På hurtigfanen **Bestillingslinjer** angir du følgende verdier for den tomme raden:</span><span class="sxs-lookup"><span data-stu-id="cc68a-233">On the **Purchase order lines** FastTab, set the following values for the empty row:</span></span>

    - <span data-ttu-id="cc68a-234">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="cc68a-234">**Item number:** *A0001*</span></span>
    - <span data-ttu-id="cc68a-235">**Antall:** *1*</span><span class="sxs-lookup"><span data-stu-id="cc68a-235">**Quantity:** *1*</span></span>

1. <span data-ttu-id="cc68a-236">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-236">Select **Save**.</span></span>
1. <span data-ttu-id="cc68a-237">Noter deg bestillingsnummeret.</span><span class="sxs-lookup"><span data-stu-id="cc68a-237">Make a note of the purchase order number.</span></span>

#### <a name="receive-a-purchase-order"></a><span data-ttu-id="cc68a-238">Motta en bestilling</span><span class="sxs-lookup"><span data-stu-id="cc68a-238">Receive a purchase order</span></span>

1. <span data-ttu-id="cc68a-239">På mobilenheten logger du deg på lager *24* ved å bruke *24* som bruker-ID og *1* som passord.</span><span class="sxs-lookup"><span data-stu-id="cc68a-239">On the mobile device, sign in to warehouse *24* by using *24* as the user ID and *1* as the password.</span></span>
1. <span data-ttu-id="cc68a-240">Velg **Innkommende**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-240">Select **Inbound**.</span></span>
1. <span data-ttu-id="cc68a-241">Velg **Kjøpsmottak**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-241">Select **Purchase receive**.</span></span> <span data-ttu-id="cc68a-242">**Lokasjon**-feltet bør settes til *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-242">The **Location** field should be set to *FL-001*.</span></span>
1. <span data-ttu-id="cc68a-243">Angi bestillingsnummeret for bestillingen som du opprettet i den forrige fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="cc68a-243">Enter the purchase order number for the purchase order that you created in the previous procedure.</span></span>
1. <span data-ttu-id="cc68a-244">I **VarenummerI**-feltet angir du *A0001*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-244">In the **Item number** field, enter *A0001*.</span></span>
1. <span data-ttu-id="cc68a-245">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-245">Select **OK**.</span></span>
1. <span data-ttu-id="cc68a-246">I feltet **Antall** angi *1*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-246">In the **Quantity** field, enter *1*.</span></span>
1. <span data-ttu-id="cc68a-247">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-247">Select **OK**.</span></span>

<span data-ttu-id="cc68a-248">Bestillingen er nå mottatt, men intet arbeid er tilknyttet den.</span><span class="sxs-lookup"><span data-stu-id="cc68a-248">The purchase order is now received, but no work is associated with it.</span></span> <span data-ttu-id="cc68a-249">Lagerbeholdningen er oppdatert, og et antall på *1* for vare *A0001* er nå tilgjengelig på lokasjonen *FL-001*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-249">The on-hand inventory has been updated, and a quantity of *1* of item *A0001* is now available at location *FL-001*.</span></span>

## <a name="example-scenario-manufacturing"></a><span data-ttu-id="cc68a-250">Eksempelscenario: Produksjon</span><span class="sxs-lookup"><span data-stu-id="cc68a-250">Example scenario: Manufacturing</span></span>

<span data-ttu-id="cc68a-251">I eksemplet nedenfor er det to produksjonsordrer, *PRD-001* og *PRD-002*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-251">In the following example, there are two production orders, *PRD-001* and *PRD-002*.</span></span> <span data-ttu-id="cc68a-252">Produksjonsordren *PRD-001* har en operasjon kalt *Montering*, der produktet *SC1* rapporteres som ferdig til lokasjonen *001*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-252">Production order *PRD-001* has an operation that is named *Assembly*, where product *SC1* is being reported as finished to location *001*.</span></span> <span data-ttu-id="cc68a-253">Produksjonsordren *PRD-002* er en operasjon kalt *Maling*, og den bruker *SC1*-produktet fra lokasjonen *001*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-253">Production order *PRD-002* has an operation that is named *Painting* and consumes product *SC1* from location *001*.</span></span> <span data-ttu-id="cc68a-254">Produksjonsordren *PRD-002* bruker også råvaren *RM1* fra lokasjonen *001*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-254">Production order *PRD-002* also consumes raw material *RM1* from location *001*.</span></span> <span data-ttu-id="cc68a-255">Råmaterialet *RM1* er lagret i lagerlokasjonen *BULK-001* og blir plukket til lokasjon *001* av lagerarbeid for plukking av råvarer.</span><span class="sxs-lookup"><span data-stu-id="cc68a-255">Raw material *RM1* is stored in warehouse location *BULK-001* and will be picked to location *001* by warehouse work for raw material picking.</span></span> <span data-ttu-id="cc68a-256">Plukkarbeidet blir generert når produksjonen *PRD-002* frigis.</span><span class="sxs-lookup"><span data-stu-id="cc68a-256">The picking work is generated when production *PRD-002* is released.</span></span>

<span data-ttu-id="cc68a-257">[![Arbeidspolicyer for lager](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span><span class="sxs-lookup"><span data-stu-id="cc68a-257">[![Warehouse work policies](./media/warehouse-work-policies.png)](./media/warehouse-work-policies.png)</span></span>

<span data-ttu-id="cc68a-258">Når du planlegger å konfigurere en arbeidspolicy for lageret i dette scenariet, bør du vurdere følgende punkter:</span><span class="sxs-lookup"><span data-stu-id="cc68a-258">When you're planning to configure a warehouse work policy for this scenario, you should consider the following points:</span></span>

- <span data-ttu-id="cc68a-259">Lagerarbeid for plassering av ferdigvarer er ikke nødvendig når du rapporterer produktet *SC1* som ferdig fra produksjonordren *PRD-001* til lokasjonen *001*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-259">Warehouse work for putaway of finished goods isn't required when you report product *SC1* as finished from production order *PRD-001* to location *001*.</span></span> <span data-ttu-id="cc68a-260">Årsaken til dette er at operasjonen *Maling* for produksjonsordre *PRD-002* bruker produktet *SC1* på samme lokasjon.</span><span class="sxs-lookup"><span data-stu-id="cc68a-260">The reason is that the *Painting* operation for production order *PRD-002* consumes product *SC1* at the same location.</span></span>
- <span data-ttu-id="cc68a-261">Lagerarbeid for plukking av råvarer kreves for å flytte råvaren *RM1* fra lagerlokasjonen *BULK-001* til lokasjonen *001*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-261">Warehouse work for raw material picking is required to move raw material *RM1* from warehouse location *BULK-001* to location *001*.</span></span>

<span data-ttu-id="cc68a-262">Her er et eksempel på en arbeidspolicy som du kan sette opp, basert på disse hensynene:</span><span class="sxs-lookup"><span data-stu-id="cc68a-262">Here is an example of a work policy that you can set up, based on these considerations:</span></span>

- <span data-ttu-id="cc68a-263">**Arbeidspolicynavn:** *Ikke plasseringsarbeid*</span><span class="sxs-lookup"><span data-stu-id="cc68a-263">**Work policy name:** *No putaway work*</span></span>
- <span data-ttu-id="cc68a-264">**Arbeidsordretyper:** *Plasser ferdigvarer* og *Plasser koprodukt og biprodukt*</span><span class="sxs-lookup"><span data-stu-id="cc68a-264">**Work order types:** *Finished goods put away* and *Co-product and by-product put away*</span></span>
- <span data-ttu-id="cc68a-265">**Lagerlokasjoner:** Lager *51* og lokasjon *001*</span><span class="sxs-lookup"><span data-stu-id="cc68a-265">**Inventory locations:** Warehouse *51* and location *001*</span></span>
- <span data-ttu-id="cc68a-266">**Produkter:** *SC1*</span><span class="sxs-lookup"><span data-stu-id="cc68a-266">**Products:** *SC1*</span></span>

<span data-ttu-id="cc68a-267">Eksempelscenarioet nedenfor inneholder trinnvise instruksjoner om hvordan du definerer lagerarbeidspolicyen i dette scenariet.</span><span class="sxs-lookup"><span data-stu-id="cc68a-267">The following example scenario provides step-by-step instructions for setting up the warehouse work policy for this scenario.</span></span>

## <a name="example-scenario-report-as-finished-to-a-location-that-isnt-license-platecontrolled"></a><span data-ttu-id="cc68a-268">Eksempelscenario: Rapportere som ferdig til en lokasjon som ikke er nummerskiltkontrollert</span><span class="sxs-lookup"><span data-stu-id="cc68a-268">Example scenario: Report as finished to a location that isn't license plate–controlled</span></span>

<span data-ttu-id="cc68a-269">Dette scenarioet viser et eksempel der en produksjonsordre rapporteres som ferdig til en lokasjon som ikke er nummerskiltkontrollert.</span><span class="sxs-lookup"><span data-stu-id="cc68a-269">This scenario shows an example where a production order is reported as finished to a location that isn't license plate–controlled.</span></span>

<span data-ttu-id="cc68a-270">Dette scenarioet bruker standard demonstrasjonsdata.</span><span class="sxs-lookup"><span data-stu-id="cc68a-270">This scenario uses the standard demo data.</span></span> <span data-ttu-id="cc68a-271">Hvis du vil arbeide deg gjennom det ved å bruke verdiene som presenteres her, må du derfor arbeide på et system der standard demodata er installert.</span><span class="sxs-lookup"><span data-stu-id="cc68a-271">Therefore, if you want to work through it by using the values that are provided here, you must work on a system where demo data is installed.</span></span> <span data-ttu-id="cc68a-272">Du må også velge den juridiske enheten **USMF**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-272">Additionally, you must select the **USMF** legal entity.</span></span>

### <a name="set-up-a-warehouse-work-policy"></a><span data-ttu-id="cc68a-273">Definere en lagerarbeidspolicy</span><span class="sxs-lookup"><span data-stu-id="cc68a-273">Set up a warehouse work policy</span></span>

<span data-ttu-id="cc68a-274">Lagerprosesser inkluderer ikke alltid lagerarbeid.</span><span class="sxs-lookup"><span data-stu-id="cc68a-274">Warehouse processes don't always include warehouse work.</span></span> <span data-ttu-id="cc68a-275">Ved å definere en arbeidspolicy, kan du hindre oppretting av arbeid for råvareplukking og plassering av ferdige varer for et sett med produkter på bestemte lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="cc68a-275">By defining a work policy, you can prevent the creation of work for raw material picking and putaway of finished goods for a set of products at specific locations.</span></span>

1. <span data-ttu-id="cc68a-276">Gå til **Lagerstyring \> Oppsett \> Arbeid \> Arbeidspolicyer**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-276">Go to **Warehouse management \> Setup \> Work \> Work policies**.</span></span>
1. <span data-ttu-id="cc68a-277">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-277">Select **New**.</span></span>
1. <span data-ttu-id="cc68a-278">I feltet **Arbeidspolicynavn** angir du *Ikke plasseringsarbeid*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-278">In the **Work policy name** field, enter *No putaway work*.</span></span>
1. <span data-ttu-id="cc68a-279">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cc68a-279">On the Action Pane, select **Save**.</span></span>
1. <span data-ttu-id="cc68a-280">På hurtigfanen **Arbeidsordretyper** velger du **Legg til** for å legge til en rad i rutenettet, og angi deretter følgende verdier for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="cc68a-280">On the **Work order types** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="cc68a-281">**Arbeidsordretype:** *Plasser ferdigvarer*</span><span class="sxs-lookup"><span data-stu-id="cc68a-281">**Work order type:** *Finished goods put away*</span></span>
    - <span data-ttu-id="cc68a-282">**Arbeidsprosess:** *Alle relaterte arbeidsprosesser*</span><span class="sxs-lookup"><span data-stu-id="cc68a-282">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="cc68a-283">**Arbeidsopprettelsesmetode:** *Aldri*</span><span class="sxs-lookup"><span data-stu-id="cc68a-283">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="cc68a-284">**Navn på direkteoverføringspolicy:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="cc68a-284">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="cc68a-285">Velg **Legg til** på nytt for å legge til nok en rad i rutenettet, og angi deretter følgende verdier for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="cc68a-285">Select **Add** again to add a second row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="cc68a-286">**Arbeidsordretype:** *Plasser koprodukt og biprodukt*</span><span class="sxs-lookup"><span data-stu-id="cc68a-286">**Work order type:** *Co-product and by-product put away*</span></span>
    - <span data-ttu-id="cc68a-287">**Arbeidsprosess:** *Alle relaterte arbeidsprosesser*</span><span class="sxs-lookup"><span data-stu-id="cc68a-287">**Work process:** *All related work processes*</span></span>
    - <span data-ttu-id="cc68a-288">**Arbeidsopprettelsesmetode:** *Aldri*</span><span class="sxs-lookup"><span data-stu-id="cc68a-288">**Work creation method:** *Never*</span></span>
    - <span data-ttu-id="cc68a-289">**Navn på direkteoverføringspolicy:** La dette feltet stå tomt.</span><span class="sxs-lookup"><span data-stu-id="cc68a-289">**Cross docking policy name:** Leave this field blank.</span></span>

1. <span data-ttu-id="cc68a-290">På hurtigfanen **Lagerlokasjoner** velger du **Legg til** for å legge til en rad i rutenettet, og angi deretter følgende verdier for den nye raden:</span><span class="sxs-lookup"><span data-stu-id="cc68a-290">On the **Inventory locations** FastTab, select **Add** to add a row to the grid, and then set the following values for the new row:</span></span>

    - <span data-ttu-id="cc68a-291">**Lager:** *51*</span><span class="sxs-lookup"><span data-stu-id="cc68a-291">**Warehouse:** *51*</span></span>
    - <span data-ttu-id="cc68a-292">**Lokasjon:** *001*</span><span class="sxs-lookup"><span data-stu-id="cc68a-292">**Location:** *001*</span></span>

1. <span data-ttu-id="cc68a-293">På hurtigfanen **Produkter** angir du feltet **Produktvalg** til *Valgt*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-293">On the **Products** FastTab, set the **Product selection** field to *Selected*.</span></span>
1. <span data-ttu-id="cc68a-294">På **Produkter**-hurtigfanen velger du **Legg til** for å legge til en rad i rutenettet.</span><span class="sxs-lookup"><span data-stu-id="cc68a-294">On the **Products** FastTab, select **Add** to add a row to the grid.</span></span>
1. <span data-ttu-id="cc68a-295">I den nye raden setter du **Varenummer**-feltet til *L0101*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-295">In the new row, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="cc68a-296">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cc68a-296">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-an-output-location"></a><span data-ttu-id="cc68a-297">Definere en utleveringslokasjon</span><span class="sxs-lookup"><span data-stu-id="cc68a-297">Set up an output location</span></span>

1. <span data-ttu-id="cc68a-298">Gå til **Organisasjonsstyring \> Ressurser \> Ressursgrupper**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-298">Go to **Organization administration \> Resources \> Resource groups**.</span></span>
1. <span data-ttu-id="cc68a-299">Velg ressursgruppe **5102** i den venstre ruten.</span><span class="sxs-lookup"><span data-stu-id="cc68a-299">In the left pane, select resource group **5102**.</span></span>
1. <span data-ttu-id="cc68a-300">Angi følgende verdier i **Generelt**-hurtigfanen:</span><span class="sxs-lookup"><span data-stu-id="cc68a-300">On the **General** FastTab, set the following values:</span></span>

    - <span data-ttu-id="cc68a-301">**Utleveringslager:** *51*</span><span class="sxs-lookup"><span data-stu-id="cc68a-301">**Output warehouse:** *51*</span></span>
    - <span data-ttu-id="cc68a-302">**Utleveringssted:** *001*</span><span class="sxs-lookup"><span data-stu-id="cc68a-302">**Output location:** *001*</span></span>

1. <span data-ttu-id="cc68a-303">Velg **Lagre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cc68a-303">On the Action Pane, select **Save**.</span></span>

> [!NOTE]
> <span data-ttu-id="cc68a-304">Lokasjonen *001* er ikke en nummerskiltkontrollert lokasjon.</span><span class="sxs-lookup"><span data-stu-id="cc68a-304">Location *001* isn't a license plate–controlled location.</span></span> <span data-ttu-id="cc68a-305">Du kan definere en utleveringslokasjon som ikke er nummerskiltkontrollert, hvis det finnes en gjeldende arbeidspolicy for lokasjonen.</span><span class="sxs-lookup"><span data-stu-id="cc68a-305">You can set up an output location that isn't license plate–controlled only if an applicable work policy exists for the location.</span></span>

### <a name="create-a-production-order-and-report-it-as-finished"></a><span data-ttu-id="cc68a-306">Opprette en produksjonsordre og rapportere den som avsluttet</span><span class="sxs-lookup"><span data-stu-id="cc68a-306">Create a production order and report it as finished</span></span>

1. <span data-ttu-id="cc68a-307">Gå til **Produksjonskontroll \> Produksjonsordrer \> Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-307">Go to **Production control \> Production orders \> All production orders**.</span></span>
1. <span data-ttu-id="cc68a-308">Velg **Ny produksjonsordre** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cc68a-308">On the Action Pane, select **New production order**.</span></span>
1. <span data-ttu-id="cc68a-309">I dialogboksen **Opprett produksjonsordre** setter du **Varenummer**-feltet til *L0101*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-309">In the **Create production order** dialog box, set the **Item number** field to *L0101*.</span></span>
1. <span data-ttu-id="cc68a-310">Velg **Opprett** for å opprette orden og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="cc68a-310">Select **Create** to create the order and close the dialog box.</span></span>

    <span data-ttu-id="cc68a-311">Det legges til en ny produksjons ordre i rutenettet på siden **Alle produksjonsordrer**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-311">A new production order is added to the grid on the **All production orders** page.</span></span>

    <span data-ttu-id="cc68a-312">La den nye produksjonsordren være valgt.</span><span class="sxs-lookup"><span data-stu-id="cc68a-312">Keep the new production order selected.</span></span>

1. <span data-ttu-id="cc68a-313">I handlingsruten, i fanen **Produksjonsordre**, i **Prosess**-gruppen, velger du **Estimat**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-313">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Estimate**.</span></span>
1. <span data-ttu-id="cc68a-314">I dialogboksen **Estimat** leser du estimatet og velger deretter **OK** for å lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="cc68a-314">In the **Estimate** dialog box, read the estimate, and then select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="cc68a-315">I handlingsruten, i fanen **Produksjonsordre**, i **Prosess**-gruppen, velger du **Start**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-315">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Start**.</span></span>
1. <span data-ttu-id="cc68a-316">I dialogboksen **Start**, på **Generelt**-fanen, angir du feltet **Automatisk stykklisteforbruk** til *Aldri*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-316">In the **Start** dialog box, on the **General** tab, set the **Automatic BOM consumption** field to *Never*.</span></span>
1. <span data-ttu-id="cc68a-317">Velg **OK** for å lagre innstillingen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="cc68a-317">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="cc68a-318">I handlingsruten, i fanen **Produksjonsordre**, i **Prosess**-gruppen, velger du **Ferdigmeld**.</span><span class="sxs-lookup"><span data-stu-id="cc68a-318">On the Action Pane, on the **Production order** tab, in the **Process** group, select **Report as finished**.</span></span>
1. <span data-ttu-id="cc68a-319">I dialogboksen **Ferdigmeld**, på **Generelt**-fanen, setter du **Godtar feil** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-319">In the **Report as finished** dialog box, on the **General** tab, set the **Accept error** option to *Yes*.</span></span>
1. <span data-ttu-id="cc68a-320">Velg **OK** for å lagre innstillingen og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="cc68a-320">Select **OK** to save your setting and close the dialog box.</span></span>
1. <span data-ttu-id="cc68a-321">Velg **Arbeidsdetaljer** i gruppen **Generelt** i fanen **Lager** i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="cc68a-321">On the Action Pane, on the **Warehouse** tab, in the **General** group, select **Work details**.</span></span>

<span data-ttu-id="cc68a-322">Når produksjonsordren rapporteres som fullført, genereres det ikke arbeid for plassering.</span><span class="sxs-lookup"><span data-stu-id="cc68a-322">When the production order is reported as finished, no work is generated for putaway.</span></span> <span data-ttu-id="cc68a-323">Dette skjer fordi en arbeidspolicy er definert som hindrer at arbeidet blir generert når produktet *L0101* rapporteres som ferdig til lokasjon *001*.</span><span class="sxs-lookup"><span data-stu-id="cc68a-323">This behavior occurs because a work policy is defined that prevents work from being generated when product *L0101* is reported as finished to location *001*.</span></span>

## <a name="more-information"></a><span data-ttu-id="cc68a-324">Mer informasjon</span><span class="sxs-lookup"><span data-stu-id="cc68a-324">More information</span></span>

<span data-ttu-id="cc68a-325">Hvis du vil ha mer informasjon om menyelementer for mobilenheter, kan du se [Definere mobilenheter for lagerarbeid](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="cc68a-325">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>

<span data-ttu-id="cc68a-326">For mer informasjon om nummerskiltmottak og arbeidspolicyer, se [Nummerskiltmottak via mobilappen Lagerstyring](warehousing-mobile-device-app-license-plate-receiving.md).</span><span class="sxs-lookup"><span data-stu-id="cc68a-326">For more information about license plate receiving and work policies, see [License plate receiving via the Warehouse Management mobile app](warehousing-mobile-device-app-license-plate-receiving.md).</span></span>

<span data-ttu-id="cc68a-327">For mer informasjon om innkommende lastadministrasjon for lagerstyring, se [Lagerhåndtering av innkommende laster for bestillinger](inbound-load-handling.md).</span><span class="sxs-lookup"><span data-stu-id="cc68a-327">For more information about inbound load management, see [Warehouse handling of inbound loads for purchase orders](inbound-load-handling.md).</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]