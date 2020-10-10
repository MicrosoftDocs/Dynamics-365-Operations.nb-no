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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 43389db93032ec29adb805f86ae04a686803176f
ms.sourcegitcommit: c986d5234b81d31cc6d054298be6f6ec92c1754c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3889583"
---
# <a name="maintenance-status"></a><span data-ttu-id="157cf-103">Vedlikeholdsstatus</span><span class="sxs-lookup"><span data-stu-id="157cf-103">Maintenance status</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="157cf-104">I Aktivastyring kan du foreta en oversiktsberegning for en spesifikk periode for nye, aktive og fullførte vedlikeholdsforespørsler, arbeidsordrer og aktiviteter for vedlikeholdsnedetid.</span><span class="sxs-lookup"><span data-stu-id="157cf-104">In Asset Management, you can make an overview calculation for a specific period for new, active, and completed maintenance requests, work orders, and maintenance downtime activities.</span></span> <span data-ttu-id="157cf-105">Du kan også se antall fullførte betingelsesvurderinger for samme periode.</span><span class="sxs-lookup"><span data-stu-id="157cf-105">You can also see the number of completed condition assessments for the same period.</span></span> <span data-ttu-id="157cf-106">Bruk denne beregningen til å få en oversikt over arbeidsbelastningen for innkommende og fullførte vedlikeholdsforespørsler og arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="157cf-106">Use this calculation to get an overview of workload for incoming and completed maintenance requests and work orders.</span></span>

## <a name="make-a-maintenance-status-calculation"></a><span data-ttu-id="157cf-107">Foreta en vedlikeholdsstatusberegning</span><span class="sxs-lookup"><span data-stu-id="157cf-107">Make a maintenance status calculation</span></span>

1. <span data-ttu-id="157cf-108">Klikk på **Aktivastyring** > **Forespørsler** > **Vedlikeholdsstatus**.</span><span class="sxs-lookup"><span data-stu-id="157cf-108">Click **Asset management** > **Inquiries** > **Maintenance status**.</span></span>

2. <span data-ttu-id="157cf-109">I dialogboksen **Beregn status** velger du perioden du vil gjøre beregningen for, i feltene **Fra dato** og **Til dato**.</span><span class="sxs-lookup"><span data-stu-id="157cf-109">In the **Calculate status** dialog, select the time range that you want to make the calculation in the **From date** and **To date** fields.</span></span>

3. <span data-ttu-id="157cf-110">Du kan bruke **Nivå**-feltet til å angi hvor detaljert vedlikeholdslinjene skal være når det gjelder arbeidssted.</span><span class="sxs-lookup"><span data-stu-id="157cf-110">You can use the **Level** field to indicate how detailed you want the maintenance lines to be regarding functional locations.</span></span> 

  <span data-ttu-id="157cf-111">Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle vedlikeholdslinjene for et arbeidssted på øverste nivå, og derfor kan det hende at statusen på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå.</span><span class="sxs-lookup"><span data-stu-id="157cf-111">For example, if you insert the number "1" in the field, and you have a multi-level functional location structure, all maintenance lines for a functional location will be shown on the top level, and therefore the status on a line may be added up from functional locations located at a lower level.</span></span> 
  
  <span data-ttu-id="157cf-112">Hvis du setter inn tallet 0 i **Nivå**-feltet, ser du et detaljert resultat som viser alle vedlikeholdslinjene på alle arbeidsstedsnivåene de er relatert til.</span><span class="sxs-lookup"><span data-stu-id="157cf-112">If you insert the number "0" in the **Level** field, you see a detailed result showing all maintenance lines on all the functional location levels to which they are related.</span></span>

4. <span data-ttu-id="157cf-113">Klikk på **OK** for å starte beregningen.</span><span class="sxs-lookup"><span data-stu-id="157cf-113">Click **OK** to start the calculation.</span></span>

5. <span data-ttu-id="157cf-114">Klikk på knappene **Grupper etter** for å vise det nødvendige detaljnivået for beregningen.</span><span class="sxs-lookup"><span data-stu-id="157cf-114">Click the **Group by** buttons to show the required detail level of the calculation.</span></span> <span data-ttu-id="157cf-115">De valgte **Grupper etter**-knappen er uthevet.</span><span class="sxs-lookup"><span data-stu-id="157cf-115">The selected **Group by** buttons are highlighted.</span></span> <span data-ttu-id="157cf-116">Klikk på en knapp for å aktivere eller deaktivere den.</span><span class="sxs-lookup"><span data-stu-id="157cf-116">Click on a button to activate or deactivate it.</span></span>

6. <span data-ttu-id="157cf-117">Husk å klikke på **Oppdater**-knappen for å oppdatere beregningen hver gang du gjør endringer, ved å aktivere eller deaktivere **Grupper etter**-knappene eller gjøre en beregning for en ny periode.</span><span class="sxs-lookup"><span data-stu-id="157cf-117">Remember to click the **Update** button to update the calculation each time you make changes by activating or deactivating **Group by** buttons, or by making a calculation for a new period.</span></span>

7. <span data-ttu-id="157cf-118">Klikk på **Status** hvis du vil opprette en ny vedlikeholdsstatusberegning.</span><span class="sxs-lookup"><span data-stu-id="157cf-118">Click **Status** if you want to create a new maintenance status calculation.</span></span>

>[!NOTE]
><span data-ttu-id="157cf-119">Resultatene som vises i **Vedlikeholdsstatus**, inkluderer bare vedlikeholdsforespørsler og arbeidsordrer med faktisk startdato og -klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="157cf-119">The results shown in **Maintenance status** only include maintenance requests and work orders that have an actual start date and time.</span></span> <span data-ttu-id="157cf-120">Sluttdato og -klokkeslett kan være tomt.</span><span class="sxs-lookup"><span data-stu-id="157cf-120">End date and time may be blank.</span></span>

## <a name="example-1"></a><span data-ttu-id="157cf-121">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="157cf-121">Example 1</span></span>

<span data-ttu-id="157cf-122">I skjermbildet nedenfor er knappene **År** og **Måned** aktivert.</span><span class="sxs-lookup"><span data-stu-id="157cf-122">In the screenshot below, the **Year** and **Month** buttons have been activated.</span></span> <span data-ttu-id="157cf-123">Når alternativene for **Grupper etter** er valgt, får du en generell oversikt på månedlig basis av arbeidsmengde og gjennomstrømning relatert til vedlikeholdsforespørsler og arbeidsordrer.</span><span class="sxs-lookup"><span data-stu-id="157cf-123">With these **Group by** options selected, you get a general overview on a monthly basis of workload and throughput related to maintenance requests and work orders.</span></span> 

![Eksempel på månedlig arbeidsmengde](media/13-controlling-and-reporting.png)

## <a name="example-2"></a><span data-ttu-id="157cf-125">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="157cf-125">Example 2</span></span>

<span data-ttu-id="157cf-126">I skjermdumpen nedenfor er informasjon om arbeidssteder lagt til.</span><span class="sxs-lookup"><span data-stu-id="157cf-126">In the screenshot below, information about functional locations has been added.</span></span> <span data-ttu-id="157cf-127">Nå er det mulig å sammenligne arbeidsmengde og gjennomstrømming mellom arbeidssteder, som kan representere geografiske steder, fabrikker eller arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="157cf-127">Now it is possible to compare workload and throughput across functional locations, which may represent geographical locations, factories, or work areas.</span></span> 

![Eksempel på månedlig arbeidsmengde med funksjonsplasseringer](media/14-controlling-and-reporting.png)

