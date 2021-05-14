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
ms.openlocfilehash: d7c0839ffbea80904ca12d1cba7ba9880f721cdd
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947526"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="6caf4-103">Oversikt over behandling av teknisk endring</span><span class="sxs-lookup"><span data-stu-id="6caf4-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="6caf4-104">Funksjonssammendrag</span><span class="sxs-lookup"><span data-stu-id="6caf4-104">Feature summary</span></span>

<span data-ttu-id="6caf4-105">Dagens produsenter krever sterk produktdataadministrasjon, versjonskontroll og behandling av teknisk endring for å lykkes i en verden med stadig reduserende produktlivssykluser, økte krav til kvalitet og pålitelighet og et større fokus på produktsikkerhet.</span><span class="sxs-lookup"><span data-stu-id="6caf4-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="6caf4-106">Behandling av teknisk endring bringer struktur og disiplin til prosessen med produktdataadministrasjon, og gjør at produkter kan defineres, frigis og endres på en kontrollert måte som støttes av arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="6caf4-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="6caf4-107"> Gjennom produktversjoner og behandling av teknisk endring kan du dokumentere, vurdere virkningen av og bruke tekniske endringer gjennom hele livssyklusen til et produkt.</span><span class="sxs-lookup"><span data-stu-id="6caf4-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="6caf4-108">Behandling av teknisk endring hjelper deg med å planlegge og administrere produktversjonering og administrere produktlivssykluser og tekniske endringer.</span><span class="sxs-lookup"><span data-stu-id="6caf4-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="6caf4-109">Her er en liste over hovedfunksjonene:</span><span class="sxs-lookup"><span data-stu-id="6caf4-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="6caf4-110">Produktversjonering</span><span class="sxs-lookup"><span data-stu-id="6caf4-110">Product versioning</span></span>
- <span data-ttu-id="6caf4-111">Forbedrede produktfrigivelsesfunksjoner som lar deg vedlikeholde produkthoveddata i én juridisk enhet (det tekniske firmaet) og publisere det fullstendig konfigurerte, frigitte produktet på andre juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="6caf4-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="6caf4-112">Regler for validering som krever at informasjon blir angitt før en produktversjon aktiveres (klargjøringskontroll)</span><span class="sxs-lookup"><span data-stu-id="6caf4-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="6caf4-113">Forbedret behandling av produktlivssyklus ved finjustert kontroll over når et frigitt produkt kan brukes i bestemte forretningsprosesser</span><span class="sxs-lookup"><span data-stu-id="6caf4-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="6caf4-114">Forespørsler om teknisk endring som støttes av arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="6caf4-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="6caf4-115">Ordrer om teknisk endring som støttes av arbeidsflyter</span><span class="sxs-lookup"><span data-stu-id="6caf4-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="6caf4-116">Den forrige videoen ([Endre administrasjonsfunksjoner i Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="6caf4-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a><span data-ttu-id="6caf4-117">Aktivere funksjonene for administrasjon av teknisk endring og versjonsdimensjon for systemet</span><span class="sxs-lookup"><span data-stu-id="6caf4-117">Turn on the engineering change management and version dimension features for your system</span></span>

<span data-ttu-id="6caf4-118">Før du kan bruke Behandling av teknisk endring, må du aktivere både funksjonen *Behandling av teknisk endring* og funksjonens konfigurasjosnøkkel.</span><span class="sxs-lookup"><span data-stu-id="6caf4-118">Before you can use engineering change management, you must enable both the *Engineering Change Management* feature and its configuration key.</span></span> <span data-ttu-id="6caf4-119">Hvis du også vil spore versjonsdimensjonen til produkter i transaksjoner (valgfritt), må du også aktivere funksjonen *Dimensjon for produktversjon* og funksjonens konfigurasjonsnøkkel.</span><span class="sxs-lookup"><span data-stu-id="6caf4-119">If you also want to track the version dimension of products in transactions (optional), then you must also enable the *Product version dimension* feature and its configuration key.</span></span>

<span data-ttu-id="6caf4-120">Først aktiverer du funksjonene ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="6caf4-120">First, turn on the features by following these steps.</span></span>

1. <span data-ttu-id="6caf4-121">Gå til arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="6caf4-121">Go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace.</span></span>
1. <span data-ttu-id="6caf4-122">Se etter oppdateringer.</span><span class="sxs-lookup"><span data-stu-id="6caf4-122">Check for updates.</span></span>
1. <span data-ttu-id="6caf4-123">Aktiver funksjonen som heter **Behandling av teknisk endring**.</span><span class="sxs-lookup"><span data-stu-id="6caf4-123">Turn on the feature that is named **Engineering Change Management**.</span></span>
1. <span data-ttu-id="6caf4-124">Hvis du vil bruke funksjonen, aktiverer du også funksjonen som kalles **Produktdimensjon – Versjon**.</span><span class="sxs-lookup"><span data-stu-id="6caf4-124">If you want to use it, then also turn on the feature that is named **Product dimension version**.</span></span>

<span data-ttu-id="6caf4-125">Deretter aktiverer du konfigurasjonsnøklene ved å følge disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="6caf4-125">Next, turn on the configuration keys by following these steps.</span></span>

1. <span data-ttu-id="6caf4-126">Sett systemet i vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="6caf4-126">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="6caf4-127">Gå til **Systemadministrasjon \> Oppsett \> Lisenskonfigurasjon**.</span><span class="sxs-lookup"><span data-stu-id="6caf4-127">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="6caf4-128">Utvid noden **Handel**.</span><span class="sxs-lookup"><span data-stu-id="6caf4-128">Expand the **Trade** node.</span></span>
1. <span data-ttu-id="6caf4-129">Aktiver konfigurasjonsnøkkelen for hovedfunksjonen ved å merke av for **Behandling av teknisk endring**.</span><span class="sxs-lookup"><span data-stu-id="6caf4-129">Enable the configuration key for the main feature by selecting the **Engineering Change Management** check box.</span></span> <span data-ttu-id="6caf4-130">(Det er ikke nødvendig å utvide noden med mindre du også vil deaktivere en eller begge delfunksjonene.)</span><span class="sxs-lookup"><span data-stu-id="6caf4-130">(It isn't necessary to expand the node unless you also want to disable one or both of its sub-features.)</span></span>
1. <span data-ttu-id="6caf4-131">Hvis du også vil bruke versjonsdimensjonen, merker du også av for **Produktdimensjon – Versjon**.</span><span class="sxs-lookup"><span data-stu-id="6caf4-131">If you also want to use the version dimension, then select the **Product dimension - Version** check box.</span></span> <span data-ttu-id="6caf4-132">(Denne avmerkingsboksen er lengre nede i listen, og ikke nestet under noden **Behandling av teknisk endring**.)</span><span class="sxs-lookup"><span data-stu-id="6caf4-132">(This check box is further down the list, not nested under the **Engineering Change Management** node.)</span></span>
1. <span data-ttu-id="6caf4-133">Deaktiver vedlikeholdsmodus, som beskrevet i [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="6caf4-133">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6caf4-134">Fra og med april 2022 blir lisensnøklene for både **Behandling av teknisk endring** og **Produktdimensjon – Versjon** aktivert som standard for alle nye installasjoner, men du kan fremdeles deaktivere dem hvis du ønsker det.</span><span class="sxs-lookup"><span data-stu-id="6caf4-134">Starting in April 2022, the license keys for both **Engineering Change Management** and **Product dimension - Version** will be enabled by default for all new installations, but you will still be able to disable them if needed.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
