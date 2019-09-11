---
title: Opprette og oppdatere åpningstid
description: Dette emnet beskriver hvordan du oppretter og oppdaterer åpningstid i Retail Headquarters.
author: josaw1
manager: AnnBe
ms.date: 7/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rapraj
ms.search.validFrom: 2019-07-30
ms.dyn365.ops.version: Retail 10.0.1 update
ms.openlocfilehash: 1b55b91246b22951f4e1d148f59444423e1d8a3d
ms.sourcegitcommit: e54607a2c80bec4db05045825914f50947f6e31e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/22/2019
ms.locfileid: "1917518"
---
# <a name="create-and-update-store-hours"></a><span data-ttu-id="49f87-103">Opprette og oppdatere åpningstid</span><span class="sxs-lookup"><span data-stu-id="49f87-103">Create and update store hours</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="overview"></a><span data-ttu-id="49f87-104">Oversikt</span><span class="sxs-lookup"><span data-stu-id="49f87-104">Overview</span></span>

<span data-ttu-id="49f87-105">Fra ett sted kan forhandlere opprette, vedlikeholde og administrere åpningstiden for forskjellige butikker i ulike geografiske områder.</span><span class="sxs-lookup"><span data-stu-id="49f87-105">From a single place, retailers can create, maintain, and manage the store hours for different stores across geographic regions.</span></span> <span data-ttu-id="49f87-106">Åpningstiden kan deretter vises på salgsstedsterminalene.</span><span class="sxs-lookup"><span data-stu-id="49f87-106">The store hours can then be shown on point of sale (POS) terminals.</span></span> <span data-ttu-id="49f87-107">På denne måten kan kasserere dele åpningstiden med kunder og hjelpe dem som er interessert i varer i andre butikker.</span><span class="sxs-lookup"><span data-stu-id="49f87-107">In this way, cashiers can share store hours with customers and better help shoppers who are interested in inventory in other stores.</span></span> <span data-ttu-id="49f87-108">Åpningstiden kan også skrives ut på kvitteringer, i tilfelle kunder ønsker å gå tilbake til butikken senere.</span><span class="sxs-lookup"><span data-stu-id="49f87-108">The store hours can also be printed on receipts, in case customers want to return to the store later.</span></span>

<span data-ttu-id="49f87-109">Flere åpningstider kan konfigureres på tvers av ulike kanaler.</span><span class="sxs-lookup"><span data-stu-id="49f87-109">Multiple store hours can be configured across different channels.</span></span> <span data-ttu-id="49f87-110">Disse kanalene omfatter fysiske butikker, telefonsentre, mobile enheter og e-handel-områder.</span><span class="sxs-lookup"><span data-stu-id="49f87-110">These channels include brick-and-mortar stores, call centers, mobile devices, and e-Commerce sites.</span></span>

<span data-ttu-id="49f87-111">Hvis en kunde har en plukkordre for en annen butikk, kan kassereren velge datoer som plukkingen skal være tilgjengelig på, i denne butikken.</span><span class="sxs-lookup"><span data-stu-id="49f87-111">If a customer has a pickup order for a different store, the cashier can select dates when the pickup will be available in that store.</span></span> <span data-ttu-id="49f87-112">Butikkoppslaget vil inneholde en referanse til datoene og åpningstiden.</span><span class="sxs-lookup"><span data-stu-id="49f87-112">The store lookup will provide a reference to the dates and store times.</span></span> <span data-ttu-id="49f87-113">Kassereren kan velge en dato og et sted, og kan også skrive ut en hentekvittering som inneholder åpningstiden.</span><span class="sxs-lookup"><span data-stu-id="49f87-113">The cashier can select a date and location, and can also print a pickup receipt that includes the store hours.</span></span>

<span data-ttu-id="49f87-114">Denne funksjonen er tilgjengelig i Microsoft Dynamics 365 for Retail versjon 8.1.2 og senere.</span><span class="sxs-lookup"><span data-stu-id="49f87-114">This functionality is available in Microsoft Dynamics 365 for Retail versions 8.1.2 and later.</span></span>

## <a name="configure-store-hours"></a><span data-ttu-id="49f87-115">Konfigurere åpningstid</span><span class="sxs-lookup"><span data-stu-id="49f87-115">Configure store hours</span></span>

<span data-ttu-id="49f87-116">Hvis du vil konfigurere åpningstid, gjør du følgende:</span><span class="sxs-lookup"><span data-stu-id="49f87-116">Follow these steps to configure store hours.</span></span>

1. <span data-ttu-id="49f87-117">Gå til **Retail** \> **Kanaloppsett** \> **Åpningstid**.</span><span class="sxs-lookup"><span data-stu-id="49f87-117">Go to **Retail** \> **Channel Setup** \> **Store hours**.</span></span>
2. <span data-ttu-id="49f87-118">Velg **Ny** for å opprette en ny mal for åpningstid.</span><span class="sxs-lookup"><span data-stu-id="49f87-118">Select **New** to create a new store hours template.</span></span> <span data-ttu-id="49f87-119">Hvis du vil bruke en eksisterende mal, velger du malen i den venstre ruten.</span><span class="sxs-lookup"><span data-stu-id="49f87-119">To use an existing template, select the template in the left pane.</span></span>
3. <span data-ttu-id="49f87-120">I dialogboksen **Legg til område** definerer du datoområdet, åpningstiden og eventuelle helligdager.</span><span class="sxs-lookup"><span data-stu-id="49f87-120">In the **Add range** dialog box, define the date range, the store hours, and any holidays that are required.</span></span>

    - <span data-ttu-id="49f87-121">Hvis åpningstiden ikke endres, velger du **Slutter ikke** i feltet **Sluttdato**.</span><span class="sxs-lookup"><span data-stu-id="49f87-121">If store hours don't change, select **Never ends** in the **End date** field.</span></span>
    - <span data-ttu-id="49f87-122">Hvis åpningstiden gjelder en bestemt måned, uke eller dag, angir du de aktuelle datoene i feltene **Startdato** og **Sluttdato**.</span><span class="sxs-lookup"><span data-stu-id="49f87-122">If the store hours are for a specific month, week, or day, set the appropriate dates in the **Start Date** and **End date** fields.</span></span>

    > [!NOTE]
    > <span data-ttu-id="49f87-123">Du kan opprette flere maler som har overlappende start- og sluttdatoer.</span><span class="sxs-lookup"><span data-stu-id="49f87-123">You can create multiple templates that have overlapping start and end dates.</span></span> <span data-ttu-id="49f87-124">Derfor kan du for eksempel definere åpningstid for butikker i forskjellige tidssoner.</span><span class="sxs-lookup"><span data-stu-id="49f87-124">Therefore, you can, for example, define store hours for stores in different time zones.</span></span>

    <span data-ttu-id="49f87-125">![Dialogboksen Legg til område](../dev-itpro/media/Storehours1.png "Dialogboksen Legg til område")</span><span class="sxs-lookup"><span data-stu-id="49f87-125">![Add range dialog box](../dev-itpro/media/Storehours1.png "Add range dialog box")</span></span>

4. <span data-ttu-id="49f87-126">Knytt åpningstidsmalen til butikkene der den skal brukes.</span><span class="sxs-lookup"><span data-stu-id="49f87-126">Associate the store hours template with the stores where it will be used.</span></span> <span data-ttu-id="49f87-127">I dialogboksen **Velg organisasjonsnoder** velger du butikkene, områdene og organisasjonene som malen skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="49f87-127">In the **Choose organization nodes** dialog box, select the stores, regions, and organizations that the template should be associated with.</span></span>

    - <span data-ttu-id="49f87-128">Bare én åpningstidsmal kan knyttes til hver butikk.</span><span class="sxs-lookup"><span data-stu-id="49f87-128">Only one store hours template can be associated with each store.</span></span>
    - <span data-ttu-id="49f87-129">Bruk pilknappene til å velge butikker, områder eller organisasjoner.</span><span class="sxs-lookup"><span data-stu-id="49f87-129">Use the arrow buttons to select stores, regions, or organizations.</span></span> <span data-ttu-id="49f87-130">Kalenderen vil være tilgjengelig for butikkene eller butikkgruppene, og den vil være synlig på salgsstedet for referanse.</span><span class="sxs-lookup"><span data-stu-id="49f87-130">The calendar will be available to the stores or store groups, and it will be visible at the POS for reference.</span></span>

    <span data-ttu-id="49f87-131">![Dialogboksen Velg organisasjonsnoder](../dev-itpro/media/Storehours2.png "Dialogboksen Velg organisasjonsnoder")</span><span class="sxs-lookup"><span data-stu-id="49f87-131">![Choose organization nodes dialog box](../dev-itpro/media/Storehours2.png "Choose organization nodes dialog box")</span></span>

5. <span data-ttu-id="49f87-132">På siden **Distribusjonsplan** kjører du jobbene **1070** og **1090** for å gjøre åpningstiden tilgjengelig for salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="49f87-132">On the **Distribution schedule** page, run the **1070** and **1090** jobs to make the store hours available to the POS.</span></span>

## <a name="add-store-hours-to-printed-receipts"></a><span data-ttu-id="49f87-133">Legge til åpningstid på utskrevne kvitteringer</span><span class="sxs-lookup"><span data-stu-id="49f87-133">Add store hours to printed receipts</span></span>

<span data-ttu-id="49f87-134">Følg disse trinnene for å legge til åpningstid på utskrevne salgsstedskvitteringer.</span><span class="sxs-lookup"><span data-stu-id="49f87-134">Follow these steps to add store hours to the printed POS receipts.</span></span>

1. <span data-ttu-id="49f87-135">Åpne kvitteringsutformingen.</span><span class="sxs-lookup"><span data-stu-id="49f87-135">Open the receipt designer.</span></span>
2. <span data-ttu-id="49f87-136">Velg **Bunntekst** i hjørnet nederst til venstre.</span><span class="sxs-lookup"><span data-stu-id="49f87-136">Select **Footer** in the lower-left corner.</span></span>
3. <span data-ttu-id="49f87-137">Dra elementet **Åpningstid** fra venstre rute til bunnteksten nederst i kvitteringsmalen.</span><span class="sxs-lookup"><span data-stu-id="49f87-137">Drag the **Store hours** element from the left pane to the footer at the bottom of the receipt template.</span></span>
4. <span data-ttu-id="49f87-138">Du kan redigere standardetiketten på **Åpningstid**-elementet etter behov.</span><span class="sxs-lookup"><span data-stu-id="49f87-138">You can edit the default label on the **Store hours** element as you require.</span></span>
5. <span data-ttu-id="49f87-139">Lagre kvitteringen, og lukk kvitteringsutformingen.</span><span class="sxs-lookup"><span data-stu-id="49f87-139">Save the receipt, and close the receipt designer.</span></span>
6. <span data-ttu-id="49f87-140">På siden **Distribusjonsplan** kjører du jobbene **1070** og **1090**.</span><span class="sxs-lookup"><span data-stu-id="49f87-140">On the **Distribution schedule** page, run the **1070** and **1090** jobs.</span></span>
7. <span data-ttu-id="49f87-141">Logg på salgsstedet.</span><span class="sxs-lookup"><span data-stu-id="49f87-141">Sign in to the POS.</span></span>
8. <span data-ttu-id="49f87-142">Fullfør et salg, og velg å skrive ut en kvittering.</span><span class="sxs-lookup"><span data-stu-id="49f87-142">Complete a sale, and select to print a receipt.</span></span>

<span data-ttu-id="49f87-143">Salgsstedskvitteringer inneholder nå åpningstid.</span><span class="sxs-lookup"><span data-stu-id="49f87-143">POS receipts now include the store hours.</span></span> <span data-ttu-id="49f87-144">Hvis helligdager er inkludert i malen, vises de på kvitteringen.</span><span class="sxs-lookup"><span data-stu-id="49f87-144">If any holidays were included in the template, they are shown on the receipt.</span></span>

<span data-ttu-id="49f87-145">![Eksempel på kvittering](../dev-itpro/media/Storehours3.png "Eksempel på kvittering")</span><span class="sxs-lookup"><span data-stu-id="49f87-145">![Receipt example](../dev-itpro/media/Storehours3.png "Receipt example")</span></span>
