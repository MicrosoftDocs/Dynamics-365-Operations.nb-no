---
title: Nummerskilt som mottar via lagerappen
description: Dette emnet forklarer hvordan du konfigurerer appen for lagerstyring for å støtte bruk av en prosess for nummerskiltmottak for å motta fysisk beholdning.
author: perlynne
manager: tfehr
ms.date: 03/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-03-31
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 7d5ac6598ab80ece0164d7c92f5d84e91d21b385
ms.sourcegitcommit: ffd845d4230646499b6f074cb43e69ab95787671
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/07/2020
ms.locfileid: "3346382"
---
# <a name="license-plate-receiving-via-the-warehousing-app"></a><span data-ttu-id="19533-103">Nummerskilt som mottar via lagerappen</span><span class="sxs-lookup"><span data-stu-id="19533-103">License plate receiving via the warehousing app</span></span>

<span data-ttu-id="19533-104">Dette emnet forklarer hvordan du konfigurerer appen for lagerstyring, slik at den støtter bruk av en prosess for nummerskiltmottak for å motta fysisk beholdning.</span><span class="sxs-lookup"><span data-stu-id="19533-104">This topic explains how to set up the warehousing app so that it supports using a license plate receiving process to receive physical inventory.</span></span>

<span data-ttu-id="19533-105">Du kan bruke denne funksjonaliteten til raskt å registrere mottak av innkommende beholdning som er relatert til et forhåndsvarsel for forsendelse.</span><span class="sxs-lookup"><span data-stu-id="19533-105">You can use this functionality to quickly record the receipt of inbound inventory that is related to an advance ship notice (ASN).</span></span> <span data-ttu-id="19533-106">Systemet oppretter automatisk et forhåndsvarsel for forsendelse når lagerstyringsprosesser brukes til å sende en overføringsordre.</span><span class="sxs-lookup"><span data-stu-id="19533-106">The system automatically creates an ASN when warehouse management processes are used to ship a transfer order.</span></span> <span data-ttu-id="19533-107">For bestillingsprosessen kan et forhåndsvarsel for forsendelse registreres manuelt, eller det kan importeres automatisk ved hjelp av en innkommende dataenhetsprosess for forhåndsvarsel for forsendelse.</span><span class="sxs-lookup"><span data-stu-id="19533-107">For the purchase order process, an ASN can be manually recorded, or it can be automatically imported by using an inbound ASN data entity process.</span></span>

<span data-ttu-id="19533-108">Dataene fra forhåndsvarselet for forsendelse knyttet til laster og forsendelser via *emballasjestrukturer*, der paller (overordnede nummerskilt) kan inneholde saker (nestede nummerskilt).</span><span class="sxs-lookup"><span data-stu-id="19533-108">The ASN data is linked to loads and shipments via the *packing structures*, where pallets (parent license plates) can contain cases (nested license plates).</span></span>

> [!NOTE]
> <span data-ttu-id="19533-109">Hvis du vil redusere antallet lagertransaksjoner når det brukes emballasjestrukturer som har nestede nummerskilt, registrerer systemet den fysiske lagerbeholdningen på det overordnede nummerskiltet.</span><span class="sxs-lookup"><span data-stu-id="19533-109">To reduce the number of inventory transactions when packing structures that have nested license plates are used, the system records the physical on-hand inventory on the parent license plate.</span></span> <span data-ttu-id="19533-110">For å utløse flytting av den fysiske lagerbeholdningen fra det overordnede nummerskiltet til de nestede nummerskiltene, basert på pakkestrukturdataene, må mobilenheten inneholde et menyelement som er basert på arbeidsopprettingsproessen *Pakk til nestede nummerskilt*.</span><span class="sxs-lookup"><span data-stu-id="19533-110">To trigger the movement of the physical on-hand inventory from the parent license plate to the nested license plates, based on the packing structure data, the mobile device must provide a menu item that is based on the *Pack to nested license plates* work creation process.</span></span>

<!-- To be used later (will require further editing):
## Warehousing mobile device app processing

When a worker scans an incoming license plate ID, the system initializes a license plate receiving process. Based on this information, the content of the license plate (data coming from the ASN) gets physically registered at the inbound dock location. The flows that follow will depend your business process needs.

## Work policies

As with (for example) the *Report as finished* mobile device menu item process, the license plate receiving process supports several workflows based on the defined setup.

### Work policies with work creation

Registration of physical on-hand where either the same warehouse worker immediately process a put-away work process following the inbound receiving (License plate receiving and put away) or where the registration and put away process gets handled as two different warehouse operations (License plate receiving) following the processing of the put-away work by using the existing work process via another mobile device menu item.

## Work policies without work creation

You can use the license plate receiving process without creating work by using the *License plate receiving without creating work* feature.

By defining **Work policies** with a **Work order type** of *Transfer receipt* and/or *Purchase orders*, and using the **Process** for **License plate receiving (and put away)**, the two Warehousing app process:

- License plate receiving
- License plate receiving and put away

will not create work, but only register the inbound physical inventory on the license plate at the inbound receiving dock.

For more information about the *Report as finished* production scenario, see the [Warehouse work policies overview](warehouse-work-policies.md).

-->

## <a name="show-or-skip-the-receiving-summary-page"></a><span data-ttu-id="19533-111">Vise eller hoppe over mottakssammendragssiden</span><span class="sxs-lookup"><span data-stu-id="19533-111">Show or skip the receiving summary page</span></span>

<span data-ttu-id="19533-112">Du kan bruke funksjonen *Kontroller om det skal vises en mottakssammendragsside på mobilenheter* for å dra nytte av en mer detaljert flyt i appen for lagerstyring som en del av prosessen for mottak av nummerskilt.</span><span class="sxs-lookup"><span data-stu-id="19533-112">You can use the *Control whether to display a receiving summary page on mobile devices* feature to take advantage of an additional detailed warehousing app flow as part of the license plate receiving process.</span></span>

<span data-ttu-id="19533-113">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="19533-113">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="19533-114">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den.</span><span class="sxs-lookup"><span data-stu-id="19533-114">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="19533-115">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="19533-115">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="19533-116">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="19533-116">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="19533-117">**Funksjonsnavn:** *Kontroller om det skal vises en mottakssammendragsside på mobilenheter*</span><span class="sxs-lookup"><span data-stu-id="19533-117">**Feature name:** *Control whether to display a receiving summary page on mobile devices*</span></span>

<span data-ttu-id="19533-118">Når denne funksjonen er aktivert, vil menyelementer på mobilenheter for mottak av nummerskilt eller mottak og plassering av nummerskilt gi en innstilling for **visning av mottakssammendragsside**.</span><span class="sxs-lookup"><span data-stu-id="19533-118">When this feature is turned on, mobile device menu items for license plate receiving or license plate receiving and put-away will provide a **Display receiving summary page** setting.</span></span> <span data-ttu-id="19533-119">Denne innstillingen har følgende alternativer:</span><span class="sxs-lookup"><span data-stu-id="19533-119">This setting has the following options:</span></span>

- <span data-ttu-id="19533-120">**Vis et detaljert sammendrag** – Ved nummerskiltmottak får arbeiderne se en ekstra side som viser hele forhåndsvarselet om forsendelse.</span><span class="sxs-lookup"><span data-stu-id="19533-120">**Display a detailed summary** – During license plate receiving, workers will see an extra page that shows the full ASN information.</span></span>
- <span data-ttu-id="19533-121">**Hopp over sammendrag** – Arbeiderne ser ikke hele forhåndsvarselet om forsendelse.</span><span class="sxs-lookup"><span data-stu-id="19533-121">**Skip the summary** – Workers won't see the full ASN information.</span></span> <span data-ttu-id="19533-122">Lagerarbeiderne kan heller ikke angi en disposisjonskode eller legge til unntak under mottaksprosessen.</span><span class="sxs-lookup"><span data-stu-id="19533-122">Warehouse workers also won't be able to set a disposition code or add exceptions during the receiving process.</span></span>

## <a name="prevent-transfer-ordershipped-license-plates-from-being-used-at-warehouses-other-than-the-destination-warehouse"></a><span data-ttu-id="19533-123">Forhindre nummerskilt sendt via overføringsordre fra å brukes på andre lagre enn destinasjonslageret</span><span class="sxs-lookup"><span data-stu-id="19533-123">Prevent transfer order–shipped license plates from being used at warehouses other than the destination warehouse</span></span>

<span data-ttu-id="19533-124">En mottaksprosess for nummerskilt kan ikke brukes hvis et forhåndsvarsel for forsendelse inneholder en nummerskilt-ID som allerede finnes og har fysiske lagerbeholdningsdata på en annen lagerlokasjon enn lagerlokasjonen der registreringen av nummerskiltet skjer.</span><span class="sxs-lookup"><span data-stu-id="19533-124">A license plate receiving process can't be used if an ASN contains a license plate ID that already exists and has physical on-hand data at a warehouse location other than the warehouse location where the license plate registration is occurring.</span></span>

<span data-ttu-id="19533-125">For scenarier for overføringsordrer der transittlageret ikke sporer nummerskilt (og derfor ikke ikke sporer fysisk lagerbeholdning per nummerskilt), kan du bruke de funksjonen *Forhindre nummerskilt sendt via overføringsordre fra å brukes på andre lagre enn destinasjonslageret* å hindre fysiske lagerbeholdningsoppdateringer av nummerskilt som er under transitt.</span><span class="sxs-lookup"><span data-stu-id="19533-125">For transfer order scenarios where the transit warehouse doesn't track license plates (and therefore also doesn't track physical on-hand inventory per license plate), you can use the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature to prevent physical on-hand updates of license plates that are in transit.</span></span>

<span data-ttu-id="19533-126">Før du kan bruke denne funksjonen, må den være aktivert i systemet.</span><span class="sxs-lookup"><span data-stu-id="19533-126">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="19533-127">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den.</span><span class="sxs-lookup"><span data-stu-id="19533-127">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="19533-128">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="19533-128">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="19533-129">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="19533-129">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="19533-130">**Funksjonsnavn:** *Forhindre nummerskilt sendt via overføringsordre fra å brukes på andre lagre enn destinasjonslageret*</span><span class="sxs-lookup"><span data-stu-id="19533-130">**Feature name:** *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse*</span></span>

<span data-ttu-id="19533-131">Følg denne fremgangsmåten for å administrere funksjonaliteten når denne funksjonen er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="19533-131">To manage the functionality when this feature is available, follow these steps.</span></span>

1. <span data-ttu-id="19533-132">Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.</span><span class="sxs-lookup"><span data-stu-id="19533-132">Go to **Warehouse management \> Setup \> Warehouse management parameters**.</span></span>
1. <span data-ttu-id="19533-133">I kategorien **Generelt**, på hurtigfanen **Nummerskilt**, angir du feltet **Policy for lagernummerskilt i transitt** til en av følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="19533-133">On the **General** tab, on the **License plates** FastTab, set the **Transit warehouse license plate policy** field to one of the following values:</span></span>

    - <span data-ttu-id="19533-134">**Tillat gjenbruk av ikke-sporede nummerskilt** – Systemet fungerer på samme måte som når unksjonen den *Forhindre nummerskilt sendt via overføringsordre fra å brukes på andre lagre enn destinasjonslageret* ikke er tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="19533-134">**Allow reuse of non-tracked license plate** – The system works the same way that it works when the *Prevent transfer order shipped license plates from being used on other warehouses than the destination warehouse* feature isn't available.</span></span> <span data-ttu-id="19533-135">Denne verdien er standardinnstillingen når du aktiverer funksjonen for første gang.</span><span class="sxs-lookup"><span data-stu-id="19533-135">This value is the default setting when you first activate the feature.</span></span>
    - <span data-ttu-id="19533-136">**Hindre gjenbruk av ikke-sporede nummerskilt** – Bare lagerbeholdninger som er relatert til et sendt nummerskilt, vil bli tillatt på destinasjonslageret før overføringsordren er mottatt.</span><span class="sxs-lookup"><span data-stu-id="19533-136">**Prevent reuse of non-tracked license plate** – Only on-hand updates that are related to a shipped license plate will be allowed at the destination warehouse until the transfer order has been received.</span></span>

## <a name="more-information"></a><span data-ttu-id="19533-137">Mer informasjon</span><span class="sxs-lookup"><span data-stu-id="19533-137">More information</span></span>

<!-- To read more about inbound loads, see [Link for Inbound load (Olga's doc.)] -->

<span data-ttu-id="19533-138">Hvis du vil ha mer informasjon om menyelementer for mobilenheter, kan du se [Definere mobilenheter for lagerarbeid](configure-mobile-devices-warehouse.md).</span><span class="sxs-lookup"><span data-stu-id="19533-138">For more information about mobile device menu items, see [Set up mobile devices for warehouse work](configure-mobile-devices-warehouse.md).</span></span>
