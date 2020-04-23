---
title: Definere gruppeplukking
description: Dette emnet beskriver hvordan du konfigurerer gruppeplukking og hvordan du bruker varebekreftelse med gruppeplukking.
author: Mirzaab
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSClusterProfile, WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: daf8bc65dc937962e2e08b6f25805ddd3b8ee3c5
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3204292"
---
[!include[banner](../includes/banner.md)]

# <a name="set-up-cluster-picking"></a><span data-ttu-id="fb9a7-103">Definere gruppeplukking</span><span class="sxs-lookup"><span data-stu-id="fb9a7-103">Set up cluster picking</span></span>

<span data-ttu-id="fb9a7-104">Dette emnet beskriver hvordan du gir arbeiderne mulighet til å bruke mobile enheter til å gruppere plukkarbeid til klynger, slik at de kan plukke varer fra ett sted for flere arbeidsordrer samtidig.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-104">This topic describes how to enable workers to use their mobile devices to group picking work into clusters, so that they can pick items from a single location for multiple work orders at the same time.</span></span> <span data-ttu-id="fb9a7-105">Dette kalles *gruppeplukking*.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-105">This is called *cluster picking*.</span></span>

## <a name="about-cluster-picking"></a><span data-ttu-id="fb9a7-106">Om gruppeplukking</span><span class="sxs-lookup"><span data-stu-id="fb9a7-106">About cluster picking</span></span>

<span data-ttu-id="fb9a7-107">Etter at arbeidsordrer er frigitt til lageret, kan arbeideren bruke en mobilenhet til å tilordne ordrene til en gruppe.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-107">After work orders are released to the warehouse, the worker can use a mobile device to assign the orders to a cluster.</span></span> <span data-ttu-id="fb9a7-108">Gruppen organiserer plukkarbeidet for arbeideren.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-108">The cluster will organize the picking work for the worker.</span></span> <span data-ttu-id="fb9a7-109">Når en arbeidsordre tilordnes til en gruppe, må arbeideren bruke gruppeplukking for å utføre plukkarbeidet for ordren.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-109">When a work order is assigned to a cluster, the worker must use cluster picking to perform the picking work for the order.</span></span> <span data-ttu-id="fb9a7-110">Arbeideren kan ikke bruke andre metoder for plukking.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-110">The worker cannot use other picking methods.</span></span> <span data-ttu-id="fb9a7-111">Hvis en arbeidsordre tilordnes en gruppe ved en feiltakelse, må arbeideren bryte gruppen og deretter opprette den på nytt.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-111">If a work order is assigned to a cluster by mistake, the worker must break the cluster and then re-create it.</span></span>

<span data-ttu-id="fb9a7-112">Om nødvendig kan en arbeider sende en gruppe til en annen arbeider.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-112">If needed, a worker can pass a cluster to another worker.</span></span> <span data-ttu-id="fb9a7-113">Dette endrer gruppestatusen Sendt.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-113">This changes the cluster status to Passed.</span></span> <span data-ttu-id="fb9a7-114">Når arbeideren bruker en mobilenhet til å angi at plukk- og plasseringsarbeidet er fullført, må forsendelsen eller lasten bekreftes i klienten.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-114">When the worker uses a mobile device to indicate that the picking and put away work is completed, the shipment or load must be confirmed in the client.</span></span>

## <a name="set-up-cluster-picking"></a><span data-ttu-id="fb9a7-115">Definere gruppeplukking</span><span class="sxs-lookup"><span data-stu-id="fb9a7-115">Set up cluster picking</span></span>

<span data-ttu-id="fb9a7-116">Hvis du vil aktivere gruppeplukking, må du konfigurere følgende:</span><span class="sxs-lookup"><span data-stu-id="fb9a7-116">To enable cluster picking, you must set up the following:</span></span>

-   <span data-ttu-id="fb9a7-117">**Gruppeprofiler** – Angi om du vil generere gruppe-IDer, antall stillinger som skal brukes, når du skal bryte grupper, og hvordan du deler opp og kontrollerer plukkarbeidet, automatisk.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-117">**Cluster profiles** – Specify whether to automatically generate cluster IDs, the number of positions to use, when to break clusters, and how to sequence and verify the picking work.</span></span>

-   <span data-ttu-id="fb9a7-118">**Arbeidsmaler** – Definer hvordan du oppretter plukkarbeidet for gruppeplukking.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-118">**Work templates** – Define how to create the picking work for cluster picking.</span></span>

-   <span data-ttu-id="fb9a7-119">**Lokasjonsdirektiver** – Angi hvor du vil plukke varer fra, og hvor du vil plassere dem.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-119">**Location directives** – Specify where to pick items from, and where to put them.</span></span>

-   <span data-ttu-id="fb9a7-120">**Menyelementer på mobilenheten** – Konfigurer et menyelement for mobilenhet til å bruke eksisterende arbeid styrt av gruppeplukking.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-120">**Mobile device menu items** – Configure a mobile device menu item to use existing work that is directed by cluster picking.</span></span> <span data-ttu-id="fb9a7-121">Deretter må du legge til menyelementet på en mobilenhetsmeny slik at det blir vist på mobile enheter.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-121">You must then add the menu item to a mobile device menu so that it is displayed on mobile devices.</span></span>

-   <span data-ttu-id="fb9a7-122">**Lagerstyringsparametere** – Angi nummerserien du vil bruke hvis du vil generere identifikatorer for grupper.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-122">**Warehouse management parameters** – Specify the number sequence to use if you want to generate identifiers for clusters.</span></span>

## <a name="set-up-a-cluster-profile"></a><span data-ttu-id="fb9a7-123">Definere en gruppeprofil</span><span class="sxs-lookup"><span data-stu-id="fb9a7-123">Set up a cluster profile</span></span>

<span data-ttu-id="fb9a7-124">Hvis du vil konfigurere en gruppeprofil, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="fb9a7-124">To set up a cluster profile, follow these steps:</span></span>

1.  <span data-ttu-id="fb9a7-125">Klikk **Lagerstyring** \> **Oppsett** \> **Mobilenhet** \> **Gruppeprofiler**.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-125">Click **Warehouse management** \> **Setup** \> **Mobile device** \> **Cluster profiles**.</span></span>

2.  <span data-ttu-id="fb9a7-126">Klikk **Ny** for å opprette en ny profil.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-126">Click **New** to create a new profile.</span></span>

3.  <span data-ttu-id="fb9a7-127">Klikk **Opprett gruppe** og deretter, under **Gruppesortering**, klikker du **Ny** for å definere sorteringskriteriene for gruppen.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-127">Click **Create cluster** and, under **Cluster sorting**, click **New** to set up the sorting criteria for the cluster.</span></span> <span data-ttu-id="fb9a7-128">Sorteringskriteriene bestemmer i hvilken rekkefølge arbeideren vil utføre plukkarbeidet.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-128">The sorting criteria control the order in which the worker will perform the picking work.</span></span> <span data-ttu-id="fb9a7-129">Du kan legge til så mange kriterier som nødvendig.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-129">You can add as many criteria as needed.</span></span>

4.  <span data-ttu-id="fb9a7-130">I **Serienummer**-feltet angir du et tall for å definere rekkefølgen som sorteringskriteriene behandles i.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-130">In the **Sequence number** field, enter a number to define the order in which the sorting criteria are processed.</span></span>

5.  <span data-ttu-id="fb9a7-131">I **feltnavn**-feltet velger du feltet som bestemmer sorteringen.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-131">In the **Field name** field, select the field that will determine the sorting.</span></span> <span data-ttu-id="fb9a7-132">Hvis du for eksempel velger **WMSLocationId**-feltet, blir arbeidet sorteret etter lokasjon.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-132">For example, if you select the **WMSLocationId** field, the work will be sorted by location.</span></span>

6.  <span data-ttu-id="fb9a7-133">I **Sortering**-feltet velger du ett av følgende alternativer.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-133">In the **Sorting** field, select one of the following options.</span></span>

| <span data-ttu-id="fb9a7-134">**Alternativ**</span><span class="sxs-lookup"><span data-stu-id="fb9a7-134">**Option**</span></span>     | <span data-ttu-id="fb9a7-135">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="fb9a7-135">**Description**</span></span>                                                                                                                                                                                                                    |
|----------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="fb9a7-136">**Stigende**</span><span class="sxs-lookup"><span data-stu-id="fb9a7-136">**Ascending**</span></span>  | <span data-ttu-id="fb9a7-137">Plukkarbeid er delt inn i en stigende rekkefølge basert på sorteringskriteriene.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-137">Picking work is sequenced in ascending order based on the sorting criteria.</span></span> <span data-ttu-id="fb9a7-138">Hvis du for eksempel bruker **WMSLocationId**-feltet som sorteringskriterium, og lokasjons-IDene 1, 2, 3 og 4, plukker du først fra lokasjon 4.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-138">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 4 first.</span></span> |
| <span data-ttu-id="fb9a7-139">**Synkende**</span><span class="sxs-lookup"><span data-stu-id="fb9a7-139">**Descending**</span></span> | <span data-ttu-id="fb9a7-140">Plukkarbeid er delt inn i en synkende rekkefølge basert på sorteringskriteriene.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-140">Picking work is sequenced in descending order based on the sorting criteria.</span></span> <span data-ttu-id="fb9a7-141">Hvis du for eksempel bruker **WMSLocationId**-feltet som sorteringskriterium, og lokasjons-IDene 1, 2, 3 og 4, plukker du først fra lokasjon 1.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-141">For example, if you use the **WMSLocationId** field as sorting criteria, and your location IDs are 1, 2, 3, and 4, you will pick from location 1 first.</span></span> |

## <a name="item-confirmation"></a><span data-ttu-id="fb9a7-142">Varebekreftelse</span><span class="sxs-lookup"><span data-stu-id="fb9a7-142">Item confirmation</span></span>

<span data-ttu-id="fb9a7-143">Når gruppeplukking brukes, er varebekreftelse avgjørende for å bekrefte varene som legges til i grupper.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-143">When cluster picking is applied, item confirmation is crucial to verify the items that are added to clusters.</span></span> <span data-ttu-id="fb9a7-144">Du kan bekrefte varer i gruppeplukking mens gruppeplukkingen utføres.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-144">You can verify items in cluster picking during the cluster picking process.</span></span> <span data-ttu-id="fb9a7-145">Oppsettet er basert på strekkodeoppsettet for produkt.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-145">The setup is based on the product bar code setup.</span></span>

### <a name="set-up-item-verification-with-cluster-picking"></a><span data-ttu-id="fb9a7-146">Definere varebekreftelse med gruppeplukking</span><span class="sxs-lookup"><span data-stu-id="fb9a7-146">Set up item verification with cluster picking</span></span>

1.  <span data-ttu-id="fb9a7-147">Åpne oppsettskjemaet for arbeidsbekreftelse på et menyelement for mobilenhet: **Lagerstyring** \> **Lagerstyring** \> **Oppsett** \> **Mobilenhet** \> **Menyelementer på mobilenheten**.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-147">On a mobile device menu item, open the setup form for work confirmation: **Warehouse management** \> **Warehouse management** \> **Setup** \> **Mobile device** \> **Mobile device menu items**.</span></span>

2.  <span data-ttu-id="fb9a7-148">Åpne **Arbeidsbekreftelsesoppsett** fra menyelementet på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-148">From the mobile device menu item, open **Work confirmation setup**.</span></span> <span data-ttu-id="fb9a7-149">Med alternativet **Produktbekreftelse** kan du bekrefte hver del av beholdningen fra den mobile enheten når den skannes.</span><span class="sxs-lookup"><span data-stu-id="fb9a7-149">The **Product confirmation** option allows you to verify each piece of inventory from the mobile device when scanned.</span></span>
