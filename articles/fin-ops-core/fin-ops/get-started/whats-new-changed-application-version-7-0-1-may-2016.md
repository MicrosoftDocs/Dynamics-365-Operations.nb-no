---
title: Hva er nytt eller endret i Dynamics AX programversjon 7.0.1 (mai 2016)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics AX programversjon 7.0.1. Denne versjonen ble utgitt i mai 2016, og har build-nummeret 7.0.1265.23014.
author: sericks007
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.custom: 91213
ms.assetid: f0bbc78f-87fc-40e9-b46a-6655893f69be
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: c4d762a6750a295b91a1d146b7bf0ae750e2e9bd
ms.sourcegitcommit: 2f766e5bb8574d250f19180ff2e101e895097713
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/21/2021
ms.locfileid: "5923195"
---
# <a name="whats-new-or-changed-in-dynamics-ax-application-version-701-may-2016"></a><span data-ttu-id="714aa-104">Hva er nytt eller endret i Dynamics AX programversjon 7.0.1 (mai 2016)</span><span class="sxs-lookup"><span data-stu-id="714aa-104">What's new or changed in Dynamics AX application version 7.0.1 (May 2016)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="714aa-105">Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics AX programversjon 7.0.1.</span><span class="sxs-lookup"><span data-stu-id="714aa-105">This article describes features that are either new or changed in Microsoft Dynamics AX application version 7.0.1.</span></span> <span data-ttu-id="714aa-106">Denne versjonen ble utgitt i mai 2016, og har build-nummeret 7.0.1265.23014.</span><span class="sxs-lookup"><span data-stu-id="714aa-106">This version was released in May 2016 and has a build number of 7.0.1265.23014.</span></span>

## <a name="electronic-reporting-er"></a><span data-ttu-id="714aa-107">Elektronisk rapportering (ER)</span><span class="sxs-lookup"><span data-stu-id="714aa-107">Electronic reporting (ER)</span></span>

| <span data-ttu-id="714aa-108">Hva kan du gjøre?</span><span class="sxs-lookup"><span data-stu-id="714aa-108">What can you do?</span></span> | <span data-ttu-id="714aa-109">Hvorfor er dette viktig?</span><span class="sxs-lookup"><span data-stu-id="714aa-109">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="714aa-110">Konfigurer en dialogboks for kjøretid for utforming av rapporter for elektronisk rapportering (ER), slik at brukere kan velge finansdimensjonene de ønsker.</span><span class="sxs-lookup"><span data-stu-id="714aa-110">Configure a run-time dialog box for designing Electronic reporting (ER) reports, so that users can select the financial dimensions that they want.</span></span> | <span data-ttu-id="714aa-111">Ved kjøretid kan brukere velge flere finansdimensjoner i dialogboksen for å kjøre en ER-rapport.</span><span class="sxs-lookup"><span data-stu-id="714aa-111">At run time, in the dialog box for running an ER report, users can select multiple financial dimensions.</span></span> <span data-ttu-id="714aa-112">Detaljer om de valgte finansdimensjonene vises i det elektroniske dokumentet som genereres.</span><span class="sxs-lookup"><span data-stu-id="714aa-112">The details of the selected financial dimensions will be displayed in the electronic document that is generated.</span></span> |
| <span data-ttu-id="714aa-113">Konfigurer tilgang til flere finansdimensjoner under utformingen av en ER-rapport via en enkelt tilordning til den aktuelle datakilden.</span><span class="sxs-lookup"><span data-stu-id="714aa-113">Configure access to multiple financial dimensions during the design of an ER report, via a single mapping to the desired data source.</span></span> | <span data-ttu-id="714aa-114">Samme ER-rapportkonfigurasjon kan brukes til å generere elektroniske dokumenter som presenterer transaksjonsdata sammen med detaljer for finansdimensjoner, uavhengig av hvor mange finansdimensjoner som er valgt av brukeren eller konfigurert for gjeldende juridiske enhet eller forekomst.</span><span class="sxs-lookup"><span data-stu-id="714aa-114">The same ER report configuration can be used to generate electronic documents that present transactional data together with details of financial dimensions, regardless of the number of financial dimensions that are either selected by the user or configured for the current legal entity or instance.</span></span> |
| <span data-ttu-id="714aa-115">Konfigurer en ER-rapport for å skrive inn data i dynamisk genererte kolonner i et elektronisk dokument som er opprettet i OPENXML-regnearkformat.</span><span class="sxs-lookup"><span data-stu-id="714aa-115">Configure an ER report to enter data in dynamically generated columns of an electronic document that is created in OPENXML worksheet format.</span></span> | <span data-ttu-id="714aa-116">En ER-rapport kan registrere data i et OPENXML-regneark som genereres, via vannrett replikering av kolonner.</span><span class="sxs-lookup"><span data-stu-id="714aa-116">An ER report can enter data in an OPENXML worksheet that is generated, via horizontally replicating columns.</span></span> <span data-ttu-id="714aa-117">Derfor kan den samme ER-rapportkonfigurasjonen brukes på nytt for å generere elektroniske dokumenter som har et annet antall dynamisk genererte kolonner.</span><span class="sxs-lookup"><span data-stu-id="714aa-117">Therefore, the same ER report configuration can be reused to generate electronic documents that have a different number of dynamically generated columns.</span></span> |
| <span data-ttu-id="714aa-118">Konfigurer ER-mål, slik at utdataresultatet av et format rettes mot bestemte mål: fil, e-post eller arkiv (Microsoft SharePoint-mappe eller Microsoft Azure Storage).</span><span class="sxs-lookup"><span data-stu-id="714aa-118">Configure ER destinations so that the output result of a format is directed to specific destination: file, email, or archive (Microsoft SharePoint folder or Microsoft Azure Storage).</span></span> | <span data-ttu-id="714aa-119">Tidligere, da du kjørte en ER-konfigurasjon, ble det vist en meldingsboks som krevde at brukerhandling for å lagre eller åpne en fil.</span><span class="sxs-lookup"><span data-stu-id="714aa-119">Previously, when you ran an ER configuration, a message box appeared that required user action to save or open a file.</span></span> <span data-ttu-id="714aa-120">Du kan forhåndskonfigurere separat et mål for hver formatkonfigurasjon og utdatakomponent (en mappe eller en fil).</span><span class="sxs-lookup"><span data-stu-id="714aa-120">You can now pre-configure a destination for each format configuration and for each output component (a folder or a file) separately.</span></span> <span data-ttu-id="714aa-121">Brukere som har riktige tilgangsrettigheter kan også endre målinnstillingene ved kjøretid.</span><span class="sxs-lookup"><span data-stu-id="714aa-121">Users who have appropriate access rights can also modify destination settings at run time.</span></span> |

## <a name="pos--microsoft-dynamics-ax-retail"></a><span data-ttu-id="714aa-122">Salgssted – Microsoft Dynamics AX Retail</span><span class="sxs-lookup"><span data-stu-id="714aa-122">POS – Microsoft Dynamics AX Retail</span></span>

| <span data-ttu-id="714aa-123">Hva kan du gjøre?</span><span class="sxs-lookup"><span data-stu-id="714aa-123">What can you do?</span></span> | <span data-ttu-id="714aa-124">Hvorfor er dette viktig?</span><span class="sxs-lookup"><span data-stu-id="714aa-124">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="714aa-125">Bruk Google Chrome-nettleseren.</span><span class="sxs-lookup"><span data-stu-id="714aa-125">Use the Google Chrome browser.</span></span> | <span data-ttu-id="714aa-126">Forhandlere kan nå starte Skysalgssted fra Chrome-nettleseren, og kan bruke alle funksjoner som er tilgjengelige i Microsoft Edge og Internet Explorer versjon av Cloud POS.</span><span class="sxs-lookup"><span data-stu-id="714aa-126">Retailers can now start Cloud POS from the Chrome browser, and can experience all the functionality that is available in the Microsoft Edge and Internet Explorer version of Cloud POS.</span></span> |

## <a name="financial-reporting"></a><span data-ttu-id="714aa-127">Finansrapportering</span><span class="sxs-lookup"><span data-stu-id="714aa-127">Financial reporting</span></span>

| <span data-ttu-id="714aa-128">Hva kan du gjøre?</span><span class="sxs-lookup"><span data-stu-id="714aa-128">What can you do?</span></span> | <span data-ttu-id="714aa-129">Hvorfor er dette viktig?</span><span class="sxs-lookup"><span data-stu-id="714aa-129">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="714aa-130">Bygg data for finansrapportering på nytt.</span><span class="sxs-lookup"><span data-stu-id="714aa-130">Rebuild the Financial reporting data mart.</span></span> | <span data-ttu-id="714aa-131">Når du flytter Dynamics AX-databasene mellom miljøer eller gjør andre omfattende endringer i miljøet, kan det hende den økonomiske rapporteringsdatabasen må bygges på nytt.</span><span class="sxs-lookup"><span data-stu-id="714aa-131">When you move Dynamics AX databases between environments or make other invasive changes to the environment, the Financial reporting database might have to be rebuilt.</span></span> <span data-ttu-id="714aa-132">Et Windows PowerShell-skript følger nå med for å bygge databasen på nytt for deg.</span><span class="sxs-lookup"><span data-stu-id="714aa-132">A Windows PowerShell script is now provided to rebuild the database for you.</span></span> |
| <span data-ttu-id="714aa-133">Du kan ikke lenger velge alternativer for rapportutforming som ikke er gyldige.</span><span class="sxs-lookup"><span data-stu-id="714aa-133">You can no longer select report designer options that aren't valid.</span></span> | <span data-ttu-id="714aa-134">Flere alternativer for rapportutforming som ble brukt i markedsversjoner av Management Reporter, gjelder ikke for denne versjonen av Dynamics AX.</span><span class="sxs-lookup"><span data-stu-id="714aa-134">Several report designer options that were used in the in-market versions of Management reporter don't apply to this version of Dynamics AX.</span></span> <span data-ttu-id="714aa-135">Disse alternativene er knyttet til økonomisk rapportutforming, utdata og kobling.</span><span class="sxs-lookup"><span data-stu-id="714aa-135">These options were related to financial report design, output, and linking.</span></span> <span data-ttu-id="714aa-136">Disse alternativene er fjernet fra Utforming av finansrapport for å hindre at brukerfeil.</span><span class="sxs-lookup"><span data-stu-id="714aa-136">These options have been removed from the financial report designer to prevent user errors.</span></span> |

## <a name="financial-management"></a><span data-ttu-id="714aa-137">Økonomistyring</span><span class="sxs-lookup"><span data-stu-id="714aa-137">Financial management</span></span>

| <span data-ttu-id="714aa-138">Hva kan du gjøre?</span><span class="sxs-lookup"><span data-stu-id="714aa-138">What can you do?</span></span> | <span data-ttu-id="714aa-139">Hvorfor er dette viktig?</span><span class="sxs-lookup"><span data-stu-id="714aa-139">Why is this important?</span></span> |
|------------------|------------------------|
| <span data-ttu-id="714aa-140">Generer positive pay-filer for leverandørbetalinger.</span><span class="sxs-lookup"><span data-stu-id="714aa-140">Generate positive pay files for accounts payable payments.</span></span> | <span data-ttu-id="714aa-141">Positive pay-filer kan genereres for å hjelpe banker med å forhindre sjekksvindel.</span><span class="sxs-lookup"><span data-stu-id="714aa-141">Positive pay files can be generated to help prevent check fraud.</span></span> |

## <a name="warehouse-and-production"></a><span data-ttu-id="714aa-142">Lager og produksjon</span><span class="sxs-lookup"><span data-stu-id="714aa-142">Warehouse and production</span></span>

<table>
<thead>
<tr>
<th><span data-ttu-id="714aa-143">Hva kan du gjøre?</span><span class="sxs-lookup"><span data-stu-id="714aa-143">What can you do?</span></span></th>
<th><span data-ttu-id="714aa-144">Hvorfor er dette viktig?</span><span class="sxs-lookup"><span data-stu-id="714aa-144">Why is this important?</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="714aa-145">Definere en arbeidspolicy for lager som styrer opprettingen av arbeidet for sett produkter på bestemte lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="714aa-145">Define a warehouse work policy that controls the creation of work for a set of products at specific locations.</span></span></td>
<td><span data-ttu-id="714aa-146">Lagerprosesser inkluderer ikke alltid arbeid.</span><span class="sxs-lookup"><span data-stu-id="714aa-146">Warehouse processes don't always include work.</span></span> <span data-ttu-id="714aa-147">Ved å bruke den nye arbeidspolicyen for lager, kan du hindre oppretting av arbeid for råvareplukking og plassering av ferdige varer for et sett med produkter på bestemte lokasjoner.</span><span class="sxs-lookup"><span data-stu-id="714aa-147">By using the new warehouse work policy, you can prevent work from being created for raw material picking and put-away of finished goods for a set of products at specific locations.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="714aa-148">Angi at en målplassering for produksjon ikke styres av nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="714aa-148">Specify that a production output location isn't license plate–controlled.</span></span></td>
<td><span data-ttu-id="714aa-149">Du kan nå angi at en målplassering for produksjon ikke styres av nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="714aa-149">You can now specify that a product output location isn't license plate–controlled.</span></span> <span data-ttu-id="714aa-150">Denne funksjonen er for eksempel nyttig når en foregående produksjonsordre rapporterer varer som ferdige direkte til en lokasjon som fungerer som produksjonsinnleveringslokasjon for en etterfølgende produksjonsordre.</span><span class="sxs-lookup"><span data-stu-id="714aa-150">For example, this feature is useful when an upstream production order reports items as finished directly to a location that acts as production input location for a downstream production order.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="714aa-151">Støtte for stykklister som inneholder varer med ulike produktdimensjoner av den samme varen.</span><span class="sxs-lookup"><span data-stu-id="714aa-151">Support BOMs that include items with different product dimensions of the same item.</span></span></td>
<td><span data-ttu-id="714aa-152">Når du bruker ett eller flere av produktdimensjonene i produksjon, kan det oppstå situasjoner der du vil produsere en vare basert på en annen variant av den samme varen.</span><span class="sxs-lookup"><span data-stu-id="714aa-152">When using one or multiple of the product dimensions in production, you can have situations where you would like to produce an item, based on a different variant of the same item.</span></span> <span data-ttu-id="714aa-153">Hvis du vil ha mer informasjon, kan du se <a href="/archive/blogs/axmfg/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item">denne bloggen</a>.</span><span class="sxs-lookup"><span data-stu-id="714aa-153">For more information, see <a href="/archive/blogs/axmfg/support-for-boms-that-includes-items-with-different-product-dimensions-of-the-same-item">this blog</a>.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="714aa-154">Produksjonsordrer med sirkelstrukturer på første nivå av stykklistene, utelates fra stykklistenivåberegning for planlegging av materialressurs.</span><span class="sxs-lookup"><span data-stu-id="714aa-154">Production orders with circular structures at the first level of their BOMs are excluded from BOM level calculation for material resource planning.</span></span></td>
<td><span data-ttu-id="714aa-155">Det er ikke mulig å tilordne riktige stykklistenivåer til produktvarianter for produksjonsordrer som kan forårsake sirkularitet i stykklistehierarkiet.</span><span class="sxs-lookup"><span data-stu-id="714aa-155">It is not possible to assign correct BOM levels to product variants for production orders that cause circularity in the BOM hierarchy.</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="714aa-156">Beregne separate stykklistenivåer for planlegging av materialressur og kostnadsberegning:</span><span class="sxs-lookup"><span data-stu-id="714aa-156">Calculate separate BOM levels for material resource planning and cost calculation:</span></span>
<ul>
<li><span data-ttu-id="714aa-157">For planlegging av materialressurs beregnes stykklistenivåer i den nye <strong>ReqItemLevel</strong>-tabellen.</span><span class="sxs-lookup"><span data-stu-id="714aa-157">For material resource planning, BOM levels are calculated in the new <strong>ReqItemLevel</strong> table.</span></span> <span data-ttu-id="714aa-158">Avsluttede produksjonsordrer ignoreres i beregningen.</span><span class="sxs-lookup"><span data-stu-id="714aa-158">Ended production orders are ignored in the calculation.</span></span></li>
<li><span data-ttu-id="714aa-159">For beregning av produksjonskostnader, beregnes stykklistenivåer i <strong>InventTable</strong>.</span><span class="sxs-lookup"><span data-stu-id="714aa-159">For production cost calculation, BOM levels are calculated in the <strong>InventTable</strong>.</span></span> <span data-ttu-id="714aa-160">Avsluttede produksjonsordrer inkluderes i beregningen.</span><span class="sxs-lookup"><span data-stu-id="714aa-160">Ended production orders are included in the calculation.</span></span></li>
</ul>
</td>
<td>
<ul>
<li><span data-ttu-id="714aa-161">Når du kjører planlegging av materialressurser, for eksempel hovedplanlegging, planlegging og nedbryting, må bare stykklistenivåer for planlegging av materialressurs beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="714aa-161">When running material resource planning, for example, master planning plan scheduling and explosion, only BOM levels used for material resource planning need to be recalculated.</span></span> <span data-ttu-id="714aa-162">Det er med andre ord ikke nødvendig å beregne stykklistenivåer som brukes for etterkalkulering av produksjon.</span><span class="sxs-lookup"><span data-stu-id="714aa-162">In other words, there is no need to calculate BOM levels used for production costing calculation.</span></span></li>
<li><span data-ttu-id="714aa-163">Når du kjører etterkalkuleringsoperasjoner, for eksempel lageravslutning, må bare stykklistenivåer som brukes for etterkalkulering av produksjonen beregnes på nytt.</span><span class="sxs-lookup"><span data-stu-id="714aa-163">When running costing operations, for example, inventory closing, only BOM levels used for production costing calculation need to be recalculated.</span></span></li>
</ul>
</td>
</tr>
</tbody>
</table>

## <a name="additional-resources"></a><span data-ttu-id="714aa-164">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="714aa-164">Additional resources</span></span>

[<span data-ttu-id="714aa-165">Startside for Hva er nytt eller endret i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="714aa-165">What's new or changed in Finance and Operations home page</span></span>](whats-new-changed.md)

[<span data-ttu-id="714aa-166">Nye eller oppdaterte oppgaveveiledninger (mai 2016)</span><span class="sxs-lookup"><span data-stu-id="714aa-166">New or updated task guides (May 2016)</span></span>](new-updated-task-guides-available-may-2016.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]