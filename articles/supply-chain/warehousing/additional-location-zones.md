---
title: Ekstra lokasjonssoner
description: Dette emnet gir en oversikt over de nye lokasjonssonene som er lagt til i Microsoft Dynamics 365 Supply Chain Management.
author: Mirzaab
manager: tfehr
ms.date: 07/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLocationBuild
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations, Supply Chain Management
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-07-01
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: c0bed8c95760b3dee350048c5f824f974b784f26
ms.sourcegitcommit: 7b7cc93c0f78c6bfc7a3ea66a74a29ba0f218553
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/04/2020
ms.locfileid: "3658340"
---
# <a name="additional-location-zones"></a><span data-ttu-id="1594d-103">Ekstra lokasjonssoner</span><span class="sxs-lookup"><span data-stu-id="1594d-103">Additional location zones</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1594d-104">Tre nye sonefelt er tilgjengelige i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1594d-104">Three new zone fields are available in Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="1594d-105">Lagerledere kan bruke dem til å definere flere lagerorganisasjoner eller -oppsett.</span><span class="sxs-lookup"><span data-stu-id="1594d-105">Warehouse managers can use them to define additional warehouse organizations or layouts.</span></span> <span data-ttu-id="1594d-106">De nye sonefeltene kan enten angis manuelt eller ved hjelp av veiviseren for **lokasjonsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="1594d-106">The new zone fields can be set either manually or by using the **Location setup** wizard.</span></span> <span data-ttu-id="1594d-107">De kan brukes i alle spørringer eller filtreringer som bruker Lokasjoner-tabellen.</span><span class="sxs-lookup"><span data-stu-id="1594d-107">They can be used in any query or filtering that uses the Locations table.</span></span>

<span data-ttu-id="1594d-108">Ingen ekstra oppsett er nødvendig for å bruke sonefeltene.</span><span class="sxs-lookup"><span data-stu-id="1594d-108">No additional setup is required to use the zone fields.</span></span>

## <a name="turn-on-the-additional-location-zone-feature"></a><span data-ttu-id="1594d-109">Aktiver funksjonen for Ekstra lokasjonssone</span><span class="sxs-lookup"><span data-stu-id="1594d-109">Turn on the Additional location zone feature</span></span>

<span data-ttu-id="1594d-110">Før du kan bruke *Ekstra lokasjonssone*-funksjonen, må den aktiveres i systemet.</span><span class="sxs-lookup"><span data-stu-id="1594d-110">Before you can use the *Additional location zone* feature, it must be turned on in your system.</span></span> <span data-ttu-id="1594d-111">Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den hvis den kreves.</span><span class="sxs-lookup"><span data-stu-id="1594d-111">Admins can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on if it's required.</span></span> <span data-ttu-id="1594d-112">I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="1594d-112">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="1594d-113">**Modul:** *Lagerstyring*</span><span class="sxs-lookup"><span data-stu-id="1594d-113">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="1594d-114">**Funksjonsnavn:** *Ekstra lokasjonssone*</span><span class="sxs-lookup"><span data-stu-id="1594d-114">**Feature name:** *Additional location zone*</span></span>

## <a name="use-location-zones"></a><span data-ttu-id="1594d-115">Bruke lokasjonssoner</span><span class="sxs-lookup"><span data-stu-id="1594d-115">Use location zones</span></span>

1. <span data-ttu-id="1594d-116">Gå til **Lagerstyring \> Oppsett \> Lager \> Veiviser for lokasjonsoppsett**.</span><span class="sxs-lookup"><span data-stu-id="1594d-116">Go to **Warehouse management \> Setup \> Warehouse \> Location setup wizard**.</span></span>
2. <span data-ttu-id="1594d-117">Angi følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="1594d-117">Set the following values:</span></span>

    - <span data-ttu-id="1594d-118">I **Lager**-feltet velger du _62_.</span><span class="sxs-lookup"><span data-stu-id="1594d-118">In the **Warehouse** field, select _62_.</span></span>
    - <span data-ttu-id="1594d-119">Velg _GULV_ i feltet **Sone-ID**.</span><span class="sxs-lookup"><span data-stu-id="1594d-119">In the **Zone ID** field, select _FLOOR_.</span></span>
    - <span data-ttu-id="1594d-120">Velg _PICKZONE1_ i feltet **Ekstra sone 1**.</span><span class="sxs-lookup"><span data-stu-id="1594d-120">In the **Additional Zone 1** field, select _PICKZONE1_.</span></span>
    - <span data-ttu-id="1594d-121">Velg _WEBSHOP1_ i feltet **Ekstra sone 2**.</span><span class="sxs-lookup"><span data-stu-id="1594d-121">In the **Additional Zone 2** field, select _WEBSHOP1_.</span></span>
    - <span data-ttu-id="1594d-122">Velg _GULV_ i **Lokasjonsprofil-ID**-feltet.</span><span class="sxs-lookup"><span data-stu-id="1594d-122">In the **Location profile ID** field, select _FLOOR_.</span></span>

3. <span data-ttu-id="1594d-123">Velg **Gulv**-linjen.</span><span class="sxs-lookup"><span data-stu-id="1594d-123">Select the **Floor** line.</span></span>
4. <span data-ttu-id="1594d-124">Angi **1** i feltet _Fra-nummer_.</span><span class="sxs-lookup"><span data-stu-id="1594d-124">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="1594d-125">Angi **3** i feltet _Til-nummer_.</span><span class="sxs-lookup"><span data-stu-id="1594d-125">In the **To number** field, enter _3_.</span></span>
5. <span data-ttu-id="1594d-126">Velg **Gang**-linjen.</span><span class="sxs-lookup"><span data-stu-id="1594d-126">Select the **Aisle** line.</span></span>
6. <span data-ttu-id="1594d-127">Angi **1** i feltet _Fra-nummer_.</span><span class="sxs-lookup"><span data-stu-id="1594d-127">In the **From number** field, enter _1_.</span></span> <span data-ttu-id="1594d-128">Angi **5** i feltet _Til-nummer_.</span><span class="sxs-lookup"><span data-stu-id="1594d-128">In the **To number** field, enter _5_.</span></span>
7. <span data-ttu-id="1594d-129">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="1594d-129">Select **Create**.</span></span>
8. <span data-ttu-id="1594d-130">Du mottar meldinger som angir at nye lokasjoner er lagt til.</span><span class="sxs-lookup"><span data-stu-id="1594d-130">You receive messages that state that new locations have been added.</span></span> <span data-ttu-id="1594d-131">Velg **Vis meldinger**-knappen for å vise meldingene.</span><span class="sxs-lookup"><span data-stu-id="1594d-131">Select the **Show messages** button to view the messages.</span></span>
9. <span data-ttu-id="1594d-132">Gå til **Lagerstyring \> Oppsett \> Lager \> Lokasjoner**.</span><span class="sxs-lookup"><span data-stu-id="1594d-132">Go to **Warehouse management \> Setup \> Warehouse \> Locations**.</span></span> <span data-ttu-id="1594d-133">De nye lokasjonene vises i listen, og alle sonefeltene er tilgjengelige (det vil si det eksisterende sonefeltet og de nye ekstra sonefeltene).</span><span class="sxs-lookup"><span data-stu-id="1594d-133">The new locations appear in the list, and all zone fields are available (that is, the existing zone field and the new additional zone fields).</span></span>
