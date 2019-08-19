---
title: Aktivamål
description: Emnet forklarer hvordan du oppretter aktivamåltyper i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 06/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9c445832a649c4f6a6642036ecab325e8aa2079
ms.sourcegitcommit: 747bcd25ce7c6c20ce9eaa0027e730f74d4fd6aa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/23/2019
ms.locfileid: "1783497"
---
# <a name="asset-measures"></a><span data-ttu-id="e3e0b-103">Aktivamål</span><span class="sxs-lookup"><span data-stu-id="e3e0b-103">Asset measures</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="e3e0b-104">Emnet forklarer hvordan du oppretter aktivamåltyper i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-104">The topic explains how to create asset measure types in Asset Management.</span></span> <span data-ttu-id="e3e0b-105">Aktivamåltyper brukes til å foreta målingsregistreringer på aktiva, for eksempel når det gjelder antall produksjonstimer eller antall som produseres på aktivumet.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-105">Asset measure types are used to make measurement registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="e3e0b-106">Aktivatyper er knyttet til aktivamåltypene.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-106">Asset types are related to the asset measure types.</span></span> <span data-ttu-id="e3e0b-107">Dette betyr at et aktivamål bare kan brukes på et aktivum hvis aktivumet er definert på aktivatypen som brukes på aktivumet.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-107">This means that an asset measure can only be used on an asset if the asset measure is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="e3e0b-108">Før du kan foreta målingsregistreringer for aktiva, må du først opprette aktivamåltypene du vil bruke, i **Tellere**.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-108">Before you can make measurement registrations on assets, you first create the asset measure types you want to use in **Counters**.</span></span> <span data-ttu-id="e3e0b-109">Deretter kan du opprette målingsregistreringer for aktiva i **Aktivamål**.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-109">Next, you can create measurement registrations on assets in **Asset measures**.</span></span> 

<span data-ttu-id="e3e0b-110">Aktivamål kan brukes på vedlikeholdsplaner.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-110">Asset measures can be used on maintenance plans.</span></span> <span data-ttu-id="e3e0b-111">En vedlikeholdsplanlinje kan være av typen "Teller", for eksempel knyttet til antall produksjonstimer eller antallet som er produsert.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="e3e0b-112">En aktivaregistrering kan oppdateres manuelt eller automatisk, basert på produksjonstimer eller produsert antall.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-112">An asset measurement registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="e3e0b-113">Et aktivum kan konfigureres til å bruke én av tre oppdateringsmetoder (valgt i **Oppdater**-feltet i **Tellere**):</span><span class="sxs-lookup"><span data-stu-id="e3e0b-113">An asset measure can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="e3e0b-114">Manuell – du må registrere verdier for aktivamål manuelt.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-114">Manual - you must manually register asset measurement values.</span></span>  
- <span data-ttu-id="e3e0b-115">Produksjonstimer – telleren oppdateres automatisk basert på antall produksjonstimer.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="e3e0b-116">Produksjonsantall – telleren oppdateres automatisk basert på antallet som er produsert.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="e3e0b-117">Hvis produsert antall brukes, blir *alle* registrerte varer inkludert i målingsregistreringen, korrekt antall så vel som feil antall.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-117">If quantity produced is used, *all* registered items are included in the measurement registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="e3e0b-118">Det er alltid mulig å utføre manuelle aktivamålregistreringer om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-118">It is always possible to make manual asset measurement registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="e3e0b-119">Opprette tellertyper for aktivatellerregistreringer</span><span class="sxs-lookup"><span data-stu-id="e3e0b-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="e3e0b-120">Velg **Aktivastyring** > **Oppsett** > **Aktivatyper** > **Tellere**.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="e3e0b-121">Velg **Ny** for å opprette en ny aktivamåltype.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-121">Select **New** to create a new asset measure type.</span></span>
3. <span data-ttu-id="e3e0b-122">Sett inn en ID i **Teller**-feltet og et tellernavn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="e3e0b-123">På hurtigfanen **Generelt** velger du en målenhet i **Enhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-123">On the **General** FastTab, select a measurement unit in the **Unit** field.</span></span>
5. <span data-ttu-id="e3e0b-124">I **Oppdater**-feltet velger du oppdateringsmetoden som skal brukes for aktivamålet.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-124">In the **Update** field, select the update method to be used for the asset measure.</span></span>
6. <span data-ttu-id="e3e0b-125">Velg "Ja" på veksleknappen **Arv tellerverdier** hvis underordnede aktiva i en aktivastruktur automatisk skal arve aktivamålregistreringer som er opprettet på det overordnede aktivumet.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit asset measure registrations made on the parent asset.</span></span>
7. <span data-ttu-id="e3e0b-126">I **Total mengde**-feltet velger du summeringsmetoden som skal brukes for et aktivamål ved bruk av denne aktivamåltypen.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-126">In the **Total aggregate** field, select the summation method to be used for an asset measure using this asset measure type.</span></span> <span data-ttu-id="e3e0b-127">"Sum" er standardvalget som brukes til å legge til registrerte verdier i totalverdien kontinuerlig.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="e3e0b-128">"Gjennomsnitt" kan brukes hvis det er definert et aktivamål for å overvåke en terskel, for eksempel med temperatur, vibrasjoner eller slitasje på et aktivum.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-128">"Average" can be used if an asset measure is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="e3e0b-129">I feltet **Avvik over** setter du inn det øvre nivået i prosent for validering hvis manuelle aktivamålregistreringer er innenfor et forventet område.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-129">In the **Deviation over** field, insert the upper level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="e3e0b-130">Valideringen er basert på lineær økning i eksisterende aktivamålregistreringer.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-130">The validation is based on a linear increase in existing asset measure registrations.</span></span>
9. <span data-ttu-id="e3e0b-131">I feltet **Avvik under** setter du inn det nedre nivået i prosent for validering hvis manuelle aktivamålregistreringer er innenfor et forventet område.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-131">In the **Deviation under** field, insert the lower level in percent for validating if manual asset measure registrations are within an expected range.</span></span> <span data-ttu-id="e3e0b-132">Valideringen er basert på lineær reduksjon i eksisterende aktivamålregistreringer.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-132">The validation is based on a linear decrease in existing asset measure registrations.</span></span>
10. <span data-ttu-id="e3e0b-133">I **Type**-feltet velger du meldingstypen (informasjon, advarsel, feil) som skal vises hvis avvik utenfor det definerte området forekommer når du utfører manuelle aktivamålregistreringer.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual asset measure registrations.</span></span>
11. <span data-ttu-id="e3e0b-134">På hurtigfanen **Aktivatyper** legger du til aktivatypene som skal kunne bruke aktivamalen.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-134">On the **Asset types** FastTab, add the asset types that should be able to use the asset measure.</span></span>
12. <span data-ttu-id="e3e0b-135">På hurtigfanen **Relaterte aktivamål** legger du til aktivamålene du vil skal bli automatisk oppdatert når dette aktivamålet oppdateres.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-135">On the **Related asset measures** FastTab, add the asset measures that you want to be automatically updated when this asset measure is updated.</span></span>


>[!NOTE]
><span data-ttu-id="e3e0b-136">Et relatert aktivum oppdateres automatisk bare hvis det tilknyttede aktivumet har aktivatypen som det er relatert til, i aktivamåloppsettet.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-136">A related asset measure is automatically updated only if the related asset measure has the asset type, to which it is related, in the asset measure setup.</span></span> <span data-ttu-id="e3e0b-137">For eksempel: Du definerer et aktivamål for "produksjon timer" og legger til aktivatypen "lastebilmotor".</span><span class="sxs-lookup"><span data-stu-id="e3e0b-137">For example: You set up an asset measure for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="e3e0b-138">Når dette aktivumet oppdateres, oppdateres også en beslektet teller med verdien "olje" med de samme anleggsmålverdiene.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-138">When that asset measure is updated, a related counter "Oil" is also updated with the same asset measure values.</span></span> <span data-ttu-id="e3e0b-139">Oppsettet i **Tellere** inkluderer oppsettet på timer.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="e3e0b-140">I aktivamålet "olje" må også aktivatypen "lastebilmotor" legges til på hurtigfanen **Aktivatyper** for å sikre aktivamålrelasjonen.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-140">Also, on the "Oil" asset measure, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the asset measure relation.</span></span> <span data-ttu-id="e3e0b-141">Se skjermbildene nedenfor for et eksempel på oppsettet for aktivamålene for timer og olje.</span><span class="sxs-lookup"><span data-stu-id="e3e0b-141">See the screenshots below for an example of the setup on the Hours and Oil asset measures.</span></span>

<span data-ttu-id="e3e0b-142">Når aktivatyper legges til for en aktivamåltype i **Tellere**, blir dette aktivamålet automatisk lagt til for aktivatypene på hurtigfanen **Tellere** i [Aktivatyper](../setup-for-objects/object-types.md)</span><span class="sxs-lookup"><span data-stu-id="e3e0b-142">When asset types are added to an asset measure type in **Counters**, that asset measure is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Figur 1](media/071-setup-for-objects.png)


