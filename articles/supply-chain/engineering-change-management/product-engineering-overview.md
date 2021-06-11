---
title: Oversikt over behandling av teknisk endring
description: Dette emnet gir en oversikt over behandling av teknisk endring, som hjelper deg med å planlegge og administrere produktversjonering og administrere produktlivssykluser og tekniske endringer.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d9430fe02abe58f37d2bfd1431b4da61527d0834
ms.sourcegitcommit: 588f8343aaa654309d2ff735fd437dba6acd9d46
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6115055"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="f634a-103">Oversikt over behandling av teknisk endring</span><span class="sxs-lookup"><span data-stu-id="f634a-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="f634a-104">Funksjonssammendrag</span><span class="sxs-lookup"><span data-stu-id="f634a-104">Feature summary</span></span>

<span data-ttu-id="f634a-105">Dagens produsenter krever sterk produktdataadministrasjon, versjonskontroll og behandling av teknisk endring for å lykkes i en verden med stadig reduserende produktlivssykluser, økte krav til kvalitet og pålitelighet og et større fokus på produktsikkerhet.</span><span class="sxs-lookup"><span data-stu-id="f634a-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="f634a-106">Behandling av teknisk endring bringer struktur og disiplin til prosessen med produktdataadministrasjon, og gjør at produkter kan defineres, frigis og endres på en kontrollert måte som støttes av arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="f634a-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="f634a-107"> Gjennom produktversjoner og behandling av teknisk endring kan du dokumentere, vurdere virkningen av og bruke tekniske endringer gjennom hele livssyklusen til et produkt.</span><span class="sxs-lookup"><span data-stu-id="f634a-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="f634a-108">Behandling av teknisk endring hjelper deg med å planlegge og administrere produktversjonering og administrere produktlivssykluser og tekniske endringer.</span><span class="sxs-lookup"><span data-stu-id="f634a-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="f634a-109">Her er en liste over hovedfunksjonene:</span><span class="sxs-lookup"><span data-stu-id="f634a-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="f634a-110">Produktversjonering</span><span class="sxs-lookup"><span data-stu-id="f634a-110">Product versioning</span></span>
- <span data-ttu-id="f634a-111">Forbedrede produktfrigivelsesfunksjoner som lar deg vedlikeholde produkthoveddata i én juridisk enhet (det tekniske firmaet) og publisere det fullstendig konfigurerte, frigitte produktet på andre juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="f634a-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="f634a-112">Regler for validering som krever at informasjon blir angitt før en produktversjon aktiveres (klargjøringskontroll)</span><span class="sxs-lookup"><span data-stu-id="f634a-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="f634a-113">Forbedret behandling av produktlivssyklus ved finjustert kontroll over når et frigitt produkt kan brukes i bestemte forretningsprosesser</span><span class="sxs-lookup"><span data-stu-id="f634a-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="f634a-114">Forespørsler om teknisk endring som støttes av arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="f634a-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="f634a-115">Ordrer om teknisk endring som støttes av arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="f634a-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="f634a-116">Den forrige videoen ([Endre administrasjonsfunksjoner i Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="f634a-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a><span data-ttu-id="f634a-117">Aktivere funksjonene for administrasjon av teknisk endring og versjonsdimensjon for systemet</span><span class="sxs-lookup"><span data-stu-id="f634a-117">Turn on the engineering change management and version dimension features for your system</span></span>

<span data-ttu-id="f634a-118">Før du kan bruke Behandling av teknisk endring, må du aktivere både funksjonen *Behandling av teknisk endring* og funksjonens konfigurasjosnøkkel.</span><span class="sxs-lookup"><span data-stu-id="f634a-118">Before you can use engineering change management, you must enable both the *Engineering Change Management* feature and its configuration key.</span></span> <span data-ttu-id="f634a-119">Hvis du også vil spore versjonsdimensjonen til produkter i transaksjoner (valgfritt), må du også aktivere funksjonen *Dimensjon for produktversjon* og funksjonens konfigurasjonsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="f634a-119">If you also want to track the version dimension of products in transactions (optional), then you must also enable the *Product version dimension* feature and its configuration key.</span></span>

<span data-ttu-id="f634a-120">Først aktiverer du funksjonene ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="f634a-120">First, turn on the features by following these steps.</span></span>

1. <span data-ttu-id="f634a-121">Gå til arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f634a-121">Go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace.</span></span>
1. <span data-ttu-id="f634a-122">Se etter oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="f634a-122">Check for updates.</span></span>
1. <span data-ttu-id="f634a-123">Aktiver funksjonen som heter *Behandling av teknisk endring*.</span><span class="sxs-lookup"><span data-stu-id="f634a-123">Turn on the feature that is named *Engineering Change Management*.</span></span>
1. <span data-ttu-id="f634a-124">Hvis du vil bruke funksjonen, aktiverer du også funksjonen som kalles *Produktdimensjon – Versjon*.</span><span class="sxs-lookup"><span data-stu-id="f634a-124">If you want to use it, also turn on the feature that is named *Product dimension version*.</span></span>

<span data-ttu-id="f634a-125">Deretter aktiverer du konfigurasjonsnøklene ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="f634a-125">Next, turn on the configuration keys by following these steps.</span></span>

1. <span data-ttu-id="f634a-126">Sett systemet i vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="f634a-126">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="f634a-127">Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="f634a-127">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="f634a-128">Utvid noden **Handel**.</span><span class="sxs-lookup"><span data-stu-id="f634a-128">Expand the **Trade** node.</span></span>
1. <span data-ttu-id="f634a-129">Aktiver konfigurasjonsnøkkelen for hovedfunksjonen ved å merke av for **Behandling av teknisk endring**.</span><span class="sxs-lookup"><span data-stu-id="f634a-129">Enable the configuration key for the main feature by selecting the **Engineering Change Management** checkbox.</span></span>
1. <span data-ttu-id="f634a-130">Utvid noden **Behandling av teknisk endring**, og merk av for eller fjern merket i de følgende avmerkingsboksene etter behov (avhengig av funksjonene du vil bruke):</span><span class="sxs-lookup"><span data-stu-id="f634a-130">Expand the **Engineering Change Management** node, and select or clear the following checkboxes as required (depending on the features that you want to use):</span></span>

    - <span data-ttu-id="f634a-131">**Attributtsøk** – Merk av i avmerkingsboksen for å aktivere [attributtsøkfunksjonen](engineering-attributes-and-search.md).</span><span class="sxs-lookup"><span data-stu-id="f634a-131">**Attribute search** – Select this checkbox to enable the [attribute search feature](engineering-attributes-and-search.md).</span></span> <span data-ttu-id="f634a-132">Vi anbefaler at du aktiverer denne funksjonen, men du kan fjerne merket i denne boksen hvis du ikke vil bruke den.</span><span class="sxs-lookup"><span data-stu-id="f634a-132">We recommend enabling this feature, but you can clear this checkbox if you won't use it.</span></span>
    - <span data-ttu-id="f634a-133">**Endringsstyring for prosessproduksjon** – Merk av i denne avmerkingsboksen hvis du vil bruke Styring av teknisk endring til å administrere endringer i formler for prosessproduksjon.</span><span class="sxs-lookup"><span data-stu-id="f634a-133">**Change management for process manufacturing** – Select this checkbox if you want to use Engineering change management features to manage changes in formulas for process manufacturing.</span></span> <span data-ttu-id="f634a-134">Hvis du ikke trenger å administrere formler, kan du fjerne merket i denne avmerkingsboksen.</span><span class="sxs-lookup"><span data-stu-id="f634a-134">If you don't have to manage formulas, you can clear this checkbox.</span></span> <span data-ttu-id="f634a-135">Hvis du vil ha mer informasjon, kan du se [Behandle endringer i formler og ingrediensene](manage-formula-changes.md).</span><span class="sxs-lookup"><span data-stu-id="f634a-135">For more information, see [Manage changes in formulas and their ingredients](manage-formula-changes.md).</span></span>

1. <span data-ttu-id="f634a-136">Hvis du også vil bruke versjonsdimensjonen, merker du av for **Produktdimensjon – Versjon**.</span><span class="sxs-lookup"><span data-stu-id="f634a-136">If you also want to use the version dimension, then select the **Product dimension - Version** checkbox.</span></span> <span data-ttu-id="f634a-137">(Denne avmerkingsboksen er lengre nede i listen, og ikke nestet under noden **Behandling av teknisk endring**.)</span><span class="sxs-lookup"><span data-stu-id="f634a-137">(This checkbox is further down the list, not nested under the **Engineering Change Management** node.)</span></span>
1. <span data-ttu-id="f634a-138">Deaktiver vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="f634a-138">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f634a-139">Fra og med april 2022 blir lisensnøklene for både **Behandling av teknisk endring** og **Produktdimensjon – Versjon** aktivert som standard for alle nye installasjoner, men du kan fremdeles deaktivere dem hvis du ønsker det.</span><span class="sxs-lookup"><span data-stu-id="f634a-139">Starting in April 2022, the license keys for both **Engineering Change Management** and **Product dimension - Version** will be enabled by default for all new installations, but you will still be able to disable them if needed.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
