---
title: Aktivamål
description: Emnet forklarer hvordan du oppretter aktivamåltyper i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetObjectCounterPart, EntAssetObjectCounterLookup, EntAssetCounterType, EntAssetObjectCounterTotals
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 41bedaaace09f632ca7506f504c3086a1dabf193
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217155"
---
# <a name="counters"></a><span data-ttu-id="b8b08-103">Tellere</span><span class="sxs-lookup"><span data-stu-id="b8b08-103">Counters</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="b8b08-104">Emnet forklarer hvordan du oppretter tellertyper i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="b8b08-104">The topic explains how to create counter types in Asset Management.</span></span> <span data-ttu-id="b8b08-105">Tellertyper brukes til å foreta tellerregistreringer på aktiva, for eksempel når det gjelder antall produksjonstimer eller antall som produseres på aktivumet.</span><span class="sxs-lookup"><span data-stu-id="b8b08-105">Counter types are used to make counter registrations on assets, for example, regarding number of production hours, or quantity produced on the asset.</span></span> <span data-ttu-id="b8b08-106">Aktivatyper er knyttet til tellertypene.</span><span class="sxs-lookup"><span data-stu-id="b8b08-106">Asset types are related to the counter types.</span></span> <span data-ttu-id="b8b08-107">Dette betyr at en teller bare kan brukes på et aktivum hvis telleren er definert på aktivatypen som brukes på aktivumet.</span><span class="sxs-lookup"><span data-stu-id="b8b08-107">This means that a counter can only be used on an asset if the counter is set up on the asset type used on the asset.</span></span>

<span data-ttu-id="b8b08-108">Før du kan foreta tellerregistreringer for aktiva, må du først opprette tellertypene du vil bruke, i **Tellere**.</span><span class="sxs-lookup"><span data-stu-id="b8b08-108">Before you can make counter registrations on assets, you first create the counter types you want to use in **Counters**.</span></span> <span data-ttu-id="b8b08-109">Deretter kan du opprette tellerregistreringer for aktiva i **Tellere**.</span><span class="sxs-lookup"><span data-stu-id="b8b08-109">Next, you can create counter registrations on assets in **Counters**.</span></span> 

<span data-ttu-id="b8b08-110">Tellere kan brukes på vedlikeholdsplaner.</span><span class="sxs-lookup"><span data-stu-id="b8b08-110">Counters can be used on maintenance plans.</span></span> <span data-ttu-id="b8b08-111">En vedlikeholdsplanlinje kan være av typen "Teller", for eksempel knyttet til antall produksjonstimer eller antallet som er produsert.</span><span class="sxs-lookup"><span data-stu-id="b8b08-111">A maintenance plan line can be of type "Counter", for example, relating to number of production hours or quantity produced.</span></span> 

<span data-ttu-id="b8b08-112">En tellerregistrering kan oppdateres manuelt eller automatisk basert på produksjonstimer eller produsert antall.</span><span class="sxs-lookup"><span data-stu-id="b8b08-112">A counter registration can be updated manually or automatically based on production hours or quantity produced.</span></span> <span data-ttu-id="b8b08-113">En teller kan konfigureres til å bruke én av tre oppdateringsmetoder (valgt i **Oppdater**-feltet i **Tellere**):</span><span class="sxs-lookup"><span data-stu-id="b8b08-113">A counter can be set up to use one of three update methods (selected in the **Update** field in **Counters**):</span></span>
  
- <span data-ttu-id="b8b08-114">Manuell – du må registrere verdier for tellere manuelt.</span><span class="sxs-lookup"><span data-stu-id="b8b08-114">Manual - you must manually register counter values.</span></span>  
- <span data-ttu-id="b8b08-115">Produksjonstimer – telleren oppdateres automatisk basert på antall produksjonstimer.</span><span class="sxs-lookup"><span data-stu-id="b8b08-115">Production hours - the counter is automatically updated based on number of production hours.</span></span>  
- <span data-ttu-id="b8b08-116">Produksjonsantall – telleren oppdateres automatisk basert på antallet som er produsert.</span><span class="sxs-lookup"><span data-stu-id="b8b08-116">Production quantity - the counter is automatically updated based on number of quantity produced.</span></span>  

>[!NOTE]
><span data-ttu-id="b8b08-117">Hvis produsert antall brukes, blir *alle* registrerte varer inkludert i tellerregistreringen, korrekt antall så vel som feil antall.</span><span class="sxs-lookup"><span data-stu-id="b8b08-117">If quantity produced is used, *all* registered items are included in the counter registration, good quantity as well as error quantity.</span></span> <span data-ttu-id="b8b08-118">Det er alltid mulig å utføre manuelle tellerregistreringer om nødvendig.</span><span class="sxs-lookup"><span data-stu-id="b8b08-118">It is always possible to make manual counter registrations, if required.</span></span>

## <a name="create-counter-types-for-asset-counter-registrations"></a><span data-ttu-id="b8b08-119">Opprette tellertyper for aktivatellerregistreringer</span><span class="sxs-lookup"><span data-stu-id="b8b08-119">Create counter types for asset counter registrations</span></span>

1. <span data-ttu-id="b8b08-120">Velg **Aktivastyring** > **Oppsett** > **Aktivatyper** > **Tellere**.</span><span class="sxs-lookup"><span data-stu-id="b8b08-120">Select **Asset management** > **Setup** > **Asset types** > **Counters**.</span></span>
2. <span data-ttu-id="b8b08-121">Velg **Ny** for å opprette en ny tellertype.</span><span class="sxs-lookup"><span data-stu-id="b8b08-121">Select **New** to create a new counter type.</span></span>
3. <span data-ttu-id="b8b08-122">Sett inn en ID i **Teller**-feltet og et tellernavn i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b8b08-122">Insert an ID in the **Counter** field, and a counter name in the **Name** field.</span></span>
4. <span data-ttu-id="b8b08-123">På hurtigfanen **Generelt** velger du en tellerenhet i **Enhet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="b8b08-123">On the **General** FastTab, select a counter unit in the **Unit** field.</span></span>
5. <span data-ttu-id="b8b08-124">I **Oppdater**-feltet velger du oppdateringsmetoden som skal brukes for telleren.</span><span class="sxs-lookup"><span data-stu-id="b8b08-124">In the **Update** field, select the update method to be used for the counter.</span></span>
6. <span data-ttu-id="b8b08-125">Velg "Ja" på veksleknappen **Arv tellerverdier** hvis underordnede aktiva i en aktivastruktur automatisk skal arve tellerregistreringer som er opprettet på det overordnede objektet.</span><span class="sxs-lookup"><span data-stu-id="b8b08-125">Select "Yes" on the **Inherit counter values** toggle button if child assets in an asset structure should automatically inherit counter registrations made on the parent asset.</span></span>
7. <span data-ttu-id="b8b08-126">I **Total mengde**-feltet velger du summeringsmetoden som skal brukes for en teller ved bruk av denne tellertypen.</span><span class="sxs-lookup"><span data-stu-id="b8b08-126">In the **Total aggregate** field, select the summation method to be used for a counter using this counter type.</span></span> <span data-ttu-id="b8b08-127">"Sum" er standardvalget som brukes til å legge til registrerte verdier i totalverdien kontinuerlig.</span><span class="sxs-lookup"><span data-stu-id="b8b08-127">"Sum" is the standard selection used to continuously add registered values to the total value.</span></span> <span data-ttu-id="b8b08-128">"Gjennomsnitt" kan brukes hvis det er definert en teller for å overvåke en terskel, for eksempel med temperatur, vibrasjoner eller slitasje på et aktivum.</span><span class="sxs-lookup"><span data-stu-id="b8b08-128">"Average" can be used if a counter is set up to monitor a threshold, for example, regarding temperature, vibrations, or wear and tear on an asset.</span></span> 
8. <span data-ttu-id="b8b08-129">I feltet **Avvik over** setter du inn det øvre nivået i prosent for validering hvis manuelle tellerregistreringer er innenfor et forventet område.</span><span class="sxs-lookup"><span data-stu-id="b8b08-129">In the **Deviation over** field, insert the upper level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="b8b08-130">Valideringen er basert på lineær økning i eksisterende tellerregistreringer.</span><span class="sxs-lookup"><span data-stu-id="b8b08-130">The validation is based on a linear increase in existing counter registrations.</span></span>
9. <span data-ttu-id="b8b08-131">I feltet **Avvik under** setter du inn det nedre nivået i prosent for validering hvis manuelle tellerregistreringer er innenfor et forventet område.</span><span class="sxs-lookup"><span data-stu-id="b8b08-131">In the **Deviation under** field, insert the lower level in percent for validating if manual counter registrations are within an expected range.</span></span> <span data-ttu-id="b8b08-132">Valideringen er basert på lineær reduksjon i eksisterende tellerregistreringer.</span><span class="sxs-lookup"><span data-stu-id="b8b08-132">The validation is based on a linear decrease in existing counter registrations.</span></span>
10. <span data-ttu-id="b8b08-133">I **Type**-feltet velger du meldingstypen (informasjon, advarsel, feil) som skal vises hvis avvik utenfor det definerte området forekommer når du utfører manuelle tellerregistreringer.</span><span class="sxs-lookup"><span data-stu-id="b8b08-133">In the **Type** field, select the type of message (information, warning, error) to be shown if deviations outside the defined range occur when you make manual counter registrations.</span></span>
11. <span data-ttu-id="b8b08-134">På hurtigfanen **Aktivatyper** legger du til aktivatypene som skal kunne bruke telleren.</span><span class="sxs-lookup"><span data-stu-id="b8b08-134">On the **Asset types** FastTab, add the asset types that should be able to use the counter.</span></span>
12. <span data-ttu-id="b8b08-135">På hurtigfanen **Relaterte aktivatellere** legger du til telleren du vil skal bli automatisk oppdatert når denne telleren oppdateres.</span><span class="sxs-lookup"><span data-stu-id="b8b08-135">On the **Related asset counters** FastTab, add the counter that you want to be automatically updated when this counter is updated.</span></span>


>[!NOTE]
><span data-ttu-id="b8b08-136">En relatert teller oppdateres automatisk bare hvis den tilknyttede telleren har aktivatypen som den er relatert til, i telleroppsettet.</span><span class="sxs-lookup"><span data-stu-id="b8b08-136">A related counter is automatically updated only if the related counter has the asset type, to which it is related, in the counter setup.</span></span> <span data-ttu-id="b8b08-137">For eksempel: Du definerer en teller for "Produksjonstimer" og legger til aktivatypen "Lastebilmotor".</span><span class="sxs-lookup"><span data-stu-id="b8b08-137">For example: You set up a counter for "Production hours" and add the asset type "Truck Engine".</span></span> <span data-ttu-id="b8b08-138">Når denne telleren oppdateres, oppdateres også en beslektet teller med verdien "olje" med de samme tellerverdiene.</span><span class="sxs-lookup"><span data-stu-id="b8b08-138">When that counter is updated, a related counter "Oil" is also updated with the same counter values.</span></span> <span data-ttu-id="b8b08-139">Oppsettet i **Tellere** inkluderer oppsettet på timer.</span><span class="sxs-lookup"><span data-stu-id="b8b08-139">The setup in **Counters** includes the setup on "Hours".</span></span> <span data-ttu-id="b8b08-140">I telleren "olje" må også aktivatypen "Lastebilmotor" legges til på hurtigfanen **Aktivatyper** for å sikre tellerrelasjonen.</span><span class="sxs-lookup"><span data-stu-id="b8b08-140">Also, on the "Oil" counter, the asset type "Truck Engine" should be added to the **Asset types** FastTab to ensure the counter relation.</span></span> <span data-ttu-id="b8b08-141">Se skjermbildene nedenfor for et eksempel på oppsettet for tellerne for timer og olje.</span><span class="sxs-lookup"><span data-stu-id="b8b08-141">See the screenshots below for an example of the setup on the Hours and Oil counters.</span></span>

<span data-ttu-id="b8b08-142">Når aktivatyper legges til for en tellertype i **Tellere**, blir denne telleren automatisk lagt til for aktivatypene på hurtigfanen **Tellere** i [Aktivatyper](../setup-for-objects/object-types.md)</span><span class="sxs-lookup"><span data-stu-id="b8b08-142">When asset types are added to a counter type in **Counters**, that counter is automatically added to the asset types on the **Counters** FastTab in [Asset types](../setup-for-objects/object-types.md).</span></span>

![Figur 1](media/071-setup-for-objects.png)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]