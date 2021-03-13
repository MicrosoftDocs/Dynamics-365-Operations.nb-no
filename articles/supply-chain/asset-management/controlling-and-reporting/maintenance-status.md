---
title: Vedlikeholdsstatus
description: Dette emnet forklarer hvordan du beregner vedlikeholdsstatus i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetStatusCalculate, EntAssetStatus
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: riluan
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: b5bac42d5cdc62361ee9a562e59bafa09ca7a215
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018502"
---
# <a name="maintenance-status"></a><span data-ttu-id="812ba-103">Vedlikeholdsstatus</span><span class="sxs-lookup"><span data-stu-id="812ba-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="812ba-104">I Aktivastyring kan du foreta en oversiktsberegning for en spesifikk periode for nye, aktive og fullførte vedlikeholdsforespørsler, arbeidsordrer og aktiviteter for vedlikeholdsnedetid.</span><span class="sxs-lookup"><span data-stu-id="812ba-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="812ba-105">Du kan også se antall fullførte betingelsesvurderinger for samme periode.</span><span class="sxs-lookup"><span data-stu-id="812ba-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="812ba-106">Bruk denne beregningen til å få en oversikt over arbeidsbelastningen for innkommende og fullførte vedlikeholdsforespørsler og arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="812ba-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="812ba-107">Foreta en vedlikeholdsstatusberegning</span><span class="sxs-lookup"><span data-stu-id="812ba-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="812ba-108">Klikk på **Aktivastyring** > **Forespørsler** > **Vedlikeholdsstatus**.</span><span class="sxs-lookup"><span data-stu-id="812ba-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="812ba-109">I dialogboksen **Beregn status** velger du perioden du vil gjøre beregningen for, i feltene **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="812ba-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="812ba-110">Du kan bruke **Nivå**-feltet til å angi hvor detaljert vedlikeholdslinjene skal være når det gjelder arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="812ba-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="812ba-111">Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle vedlikeholdslinjene for et arbeidssted på øverste nivå, og derfor kan det hende at statusen på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="812ba-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="812ba-112">Hvis du setter inn tallet 0 i **Nivå**-feltet, ser du et detaljert resultat som viser alle vedlikeholdslinjene på alle arbeidsstedsnivåene de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="812ba-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="812ba-113">Klikk på **OK** for å starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="812ba-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="812ba-114">Klikk på knappene **Grupper etter** for å vise det nødvendige detaljnivået for beregningen.</span><span class="sxs-lookup"><span data-stu-id="812ba-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="812ba-115">De valgte **Grupper etter**-knappen er uthevet.</span><span class="sxs-lookup"><span data-stu-id="812ba-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="812ba-116">Klikk på en knapp for å aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="812ba-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="812ba-117">Husk å klikke på **Oppdater**-knappen for å oppdatere beregningen hver gang du gjør endringer, ved å aktivere eller deaktivere **Grupper etter**-knappene eller gjøre en beregning for en ny periode.</span><span class="sxs-lookup"><span data-stu-id="812ba-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="812ba-118">Klikk på **Status** hvis du vil opprette en ny vedlikeholdsstatusberegning.</span><span class="sxs-lookup"><span data-stu-id="812ba-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="812ba-119">Resultatene som vises i **Vedlikeholdsstatus**, inkluderer bare vedlikeholdsforespørsler og arbeidsordrer med faktisk startdato og -klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="812ba-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="812ba-120">Sluttdato og -klokkeslett kan være tomt.</span><span class="sxs-lookup"><span data-stu-id="812ba-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="812ba-121">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="812ba-121">Example 1</span></span>

<span data-ttu-id="812ba-122">I skjermbildet nedenfor er knappene **År** og **Måned** aktivert.</span><span class="sxs-lookup"><span data-stu-id="812ba-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="812ba-123">Når alternativene for **Grupper etter** er valgt, får du en generell oversikt på månedlig basis av arbeidsmengde og gjennomstrømning relatert til vedlikeholdsforespørsler og arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="812ba-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Eksempel på månedlig arbeidsmengde](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="812ba-125">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="812ba-125">Example 2</span></span>

<span data-ttu-id="812ba-126">I skjermdumpen nedenfor er informasjon om arbeidssteder lagt til.</span><span class="sxs-lookup"><span data-stu-id="812ba-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="812ba-127">Nå er det mulig å sammenligne arbeidsmengde og gjennomstrømming mellom arbeidssteder, som kan representere geografiske steder, fabrikker eller arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="812ba-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Eksempel på månedlig arbeidsmengde med funksjonsplasseringer](media/14-controlling-and-reporting.png)

