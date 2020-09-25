---
title: Hva er nytt eller endret i Dynamics 365 Supply Chain Management 10.0.6. (november 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Supply Chain Management 10.0.6.
author: josaw1
manager: tfehr
ms.date: 10/28/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 9ee25036488d2f7f24c1691d36239f3f34caf0cb
ms.sourcegitcommit: 5bb36b74935ffe140367fd6ecf956b4857ad12e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/14/2020
ms.locfileid: "3802925"
---
# <a name="whats-new-or-changed-in-dynamics-365-supply-chain-management-1006-november-2019"></a><span data-ttu-id="10afa-103">Hva er nytt eller endret i Dynamics 365 Supply Chain Management 10.0.6. (november 2019)</span><span class="sxs-lookup"><span data-stu-id="10afa-103">What's new or changed in Dynamics 365 Supply Chain Management 10.0.6 (November 2019)</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="10afa-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span><span class="sxs-lookup"><span data-stu-id="10afa-104">This topic describes features that are either new or changed in Microsoft Dynamics 365 Supply Chain Management 10.0.6.</span></span> <span data-ttu-id="10afa-105">Denne versjonen har et Build-nummer for 10.0.234.</span><span class="sxs-lookup"><span data-stu-id="10afa-105">This version has a build number of 10.0.234.</span></span> <span data-ttu-id="10afa-106">Når den generelle tilgjengelighetsdatoen er i november, er de nye funksjonene tilgjengelige for tidlig frigivelse i oktober.</span><span class="sxs-lookup"><span data-stu-id="10afa-106">While the general availability date is in November, the new features are available for early release in October.</span></span> <span data-ttu-id="10afa-107">Hvis du vil ha mer informasjon om versjon 10.0.6, se [Tilleggsressurser](whats-new-scm-10-0-6.md#additional-resources).</span><span class="sxs-lookup"><span data-stu-id="10afa-107">For more information about version 10.0.6, see [Additional resources](whats-new-scm-10-0-6.md#additional-resources).</span></span>

## <a name="product-configuration-models-v2-data-entity"></a><span data-ttu-id="10afa-108">V2-dataenheten produktkonfigurasjonsmodeller</span><span class="sxs-lookup"><span data-stu-id="10afa-108">Product configuration models V2 data entity</span></span>

<span data-ttu-id="10afa-109">En ny versjon for dataenheten "produktkonfigurasjonsmodeller" frigis (kalt "produktkonfigurasjonsmodeller V2").</span><span class="sxs-lookup"><span data-stu-id="10afa-109">A second version for the "product configuration models" data entity is released (called "products configuration models V2").</span></span> <span data-ttu-id="10afa-110">Standardmalen "418-produktkonfigurasjonsmodeller" må også være slik at den bruker den nye "produktkonfigurasjonsmodeller V2"-dataenheten i malene for rammeverk for import/eksport.</span><span class="sxs-lookup"><span data-stu-id="10afa-110">The default template "418-product configuration models" is also needs to be so that it uses the new "product configuration models V2" data entity in the import/export framework templates.</span></span> <span data-ttu-id="10afa-111">Malen blir ikke automatisk oppdatert, slik at du må laste malen inn fra standarden manuelt.</span><span class="sxs-lookup"><span data-stu-id="10afa-111">The template will not be auto-updated so that you will have to load the template from the default manually.</span></span> <span data-ttu-id="10afa-112">V2-enheten eksporterer én rad som separat fil i et vedlegg i stedet for innebygd, og kan løse størrelsesbegrensningene for V1-enheten.</span><span class="sxs-lookup"><span data-stu-id="10afa-112">The V2 entity exports one row as separate file in an attachment instead of inline, solving the size limitations of the V1 entity.</span></span> 
 
<span data-ttu-id="10afa-113">Hva trenger du for å gjøre denne endringen?</span><span class="sxs-lookup"><span data-stu-id="10afa-113">What do you need to do to take this change?</span></span>
-    <span data-ttu-id="10afa-114">Siden V1-enheten er avskrevet, bør du begynne å overføre fra V1 til V2.</span><span class="sxs-lookup"><span data-stu-id="10afa-114">As the V1 entity has been deprecated, you should start migrating from V1 to V2.</span></span> <span data-ttu-id="10afa-115">Hvis du bruker malen "418-produktkonfigurasjonsmodeller", kan du klikke knappen "last inn standardmaler" og laste malen "418 – produktkonfigurasjonsmodeller" på nytt.</span><span class="sxs-lookup"><span data-stu-id="10afa-115">If you are using the  "418-product configuration models" template, you can click on "load default templates" button and reload the template "418 – product configuration models"</span></span>
-    <span data-ttu-id="10afa-116">Hvis du må beholde kompatibilitet med eksisterende systemer, kan du nå fortsette å bruke den eksisterende malen og (avskrevet) V1-enheten til du flytter integreringene til den nye malen.</span><span class="sxs-lookup"><span data-stu-id="10afa-116">If you need to keep compatibility with existing systems, you can for now continue using the existing template and the (deprecated) V1 entity until you move your integrations to the new template.</span></span> 

## <a name="feature-management-enhancements"></a><span data-ttu-id="10afa-117">Forbedringer av funksjonsbehandling</span><span class="sxs-lookup"><span data-stu-id="10afa-117">Feature management enhancements</span></span>
<span data-ttu-id="10afa-118">Med funksjonsbehandling kan du nå aktivere alle nye funksjoner som standard, kreve bekreftelse for å aktivere en funksjon og aktivere alle funksjoner som ikke allerede er aktivert.</span><span class="sxs-lookup"><span data-stu-id="10afa-118">Feature management now allows you to enable all new features by default, require confirmation to enable a feature, and enable all features that have not already been enabled.</span></span> 


## <a name="purchase-agreement-responsible-party"></a><span data-ttu-id="10afa-119">Ansvarlig part for kjøpsavtale</span><span class="sxs-lookup"><span data-stu-id="10afa-119">Purchase agreement responsible party</span></span>
<span data-ttu-id="10afa-120">Du kan nå definere primære og sekundære ansvarlige parter i skjemaet Kjøpsavtaleklassifisering og resulterende kjøpsavtaler.</span><span class="sxs-lookup"><span data-stu-id="10afa-120">You now have the ability to define primary and secondary responsible parties on the Purchase agreement classification form and resulting Purchase agreements.</span></span>  <span data-ttu-id="10afa-121">Dette gir brukeren tilgang til hvem som overser avtalene.</span><span class="sxs-lookup"><span data-stu-id="10afa-121">This provides the user access to who oversees the agreements.</span></span>

## <a name="rfq-link-on-the-purchase-order-line"></a><span data-ttu-id="10afa-122">Tilbudsforespørsel-kobling på kjøpsordrelinjen</span><span class="sxs-lookup"><span data-stu-id="10afa-122">RFQ link on the Purchase order line</span></span>
<span data-ttu-id="10afa-123">Du kan legge til en referansekobling fra bestillingslinjene tilbake til de tilsvarende tilbudsforespørselslinjene de stammer fra, slik at brukeren enkelt kan få det støttende dokumentet for tilbudsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="10afa-123">You can add a reference link from the Purchase order lines back to the corresponding RFQ lines they originated from, allowing the user to easily be provided with the supporting request for quotation document.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="10afa-124">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="10afa-124">Additional resources</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="10afa-125">Feilrettinger</span><span class="sxs-lookup"><span data-stu-id="10afa-125">Bug fixes</span></span>
<span data-ttu-id="10afa-126">Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av 10.0.6, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span><span class="sxs-lookup"><span data-stu-id="10afa-126">For information about the bug fixes included in each of the updates that are part of 10.0.6, sign in to Lifecycle Services (LCS) and view the [KB article](https://fix.lcs.dynamics.com/Issue/Details?bugId=369581&dbType=3&qc=ba058110be40fe16a39469298041b1a7baf82eb65bb9df4d864602d2c6bf93d7).</span></span>

### <a name="platform-update-30"></a><span data-ttu-id="10afa-127">Plattform update 30</span><span class="sxs-lookup"><span data-stu-id="10afa-127">Platform update 30</span></span>
<span data-ttu-id="10afa-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 inkluderer Platform update 30.</span><span class="sxs-lookup"><span data-stu-id="10afa-128">Microsoft Dynamics 365 Supply Chain Management 10.0.6 includes Platform update 30.</span></span> <span data-ttu-id="10afa-129">Hvis du vil vite mer om plattformoppdatering 30, se [Hva er nytt eller endret i plattformoppdatering 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span><span class="sxs-lookup"><span data-stu-id="10afa-129">To learn more about Platform update 30, see [What's new or changed in Platform update 30](../../fin-ops-core/fin-ops/get-started/whats-new-platform-update-30.md).</span></span>

### <a name="dynamics-365-2019-release-wave-2-plan"></a><span data-ttu-id="10afa-130">Dynamics 365: 2019-frigivelsesbølge 2-planen</span><span class="sxs-lookup"><span data-stu-id="10afa-130">Dynamics 365: 2019 release wave 2 plan</span></span>
<span data-ttu-id="10afa-131">Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?</span><span class="sxs-lookup"><span data-stu-id="10afa-131">Wondering about upcoming and recently released capabilities in any of our business apps or platform?</span></span>

<span data-ttu-id="10afa-132">Se [Dynamics 365: 2019-frigivelsesbølge 2-planen](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span><span class="sxs-lookup"><span data-stu-id="10afa-132">Check out the [Dynamics 365: 2019 release wave 2 plan](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/).</span></span> <span data-ttu-id="10afa-133">Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.</span><span class="sxs-lookup"><span data-stu-id="10afa-133">We've captured all the details, end to end, top to bottom, in a single document that you can use for planning.</span></span>

### <a name="removed-and-deprecated-supply-chain-management-features"></a><span data-ttu-id="10afa-134">Fjernede og avskrevne funksjoner i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="10afa-134">Removed and deprecated Supply Chain Management features</span></span>

<span data-ttu-id="10afa-135">Emnet [Fjernede eller avskrevne funksjonene i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) beskriver funksjoner som er eller er planlagt å bli fjernet eller avskrevet for Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="10afa-135">The [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic describes features that have been or are scheduled to be removed or deprecated for Supply Chain Management.</span></span>

- <span data-ttu-id="10afa-136">En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.</span><span class="sxs-lookup"><span data-stu-id="10afa-136">A *removed* feature is no longer available in the product.</span></span>
- <span data-ttu-id="10afa-137">En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.</span><span class="sxs-lookup"><span data-stu-id="10afa-137">A *deprecated* feature is not in active development and may be removed in a future update.</span></span>

<span data-ttu-id="10afa-138">Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i emnet [Fjernede eller avskrevne funksjoner i Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) 12 måneder før fjerningen.</span><span class="sxs-lookup"><span data-stu-id="10afa-138">Before any feature is removed from the product, the deprecation notice will be announced in the [Removed or deprecated features in Dynamics 365 Supply Chain Management](removed-deprecated-features-scm-updates.md) topic 12 months prior to the removal.</span></span>

<span data-ttu-id="10afa-139">For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder.</span><span class="sxs-lookup"><span data-stu-id="10afa-139">For breaking changes that only affect compilation time, but are binary compatible with sandbox and production environments, the deprecation time will be less than 12 months.</span></span> <span data-ttu-id="10afa-140">Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.</span><span class="sxs-lookup"><span data-stu-id="10afa-140">Typically, these are functional updates that need to be made to the compiler.</span></span>
