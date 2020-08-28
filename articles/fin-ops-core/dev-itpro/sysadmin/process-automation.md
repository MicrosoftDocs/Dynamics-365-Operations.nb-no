---
title: Prosessautomatisering
description: Dette emnet inneholder detaljer om hvordan prosessautomatisering tillater enkel planlegging av prosesser som vil bli kjørt av den satsvise serveren.
author: RyanCCarlson2
manager: tonyafehr
ms.date: 08/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: 320e18f7fc61300ed2966afef530907fc9fc5ca5
ms.sourcegitcommit: e2a47d31175bbd60acfd7a23ffea70c669358572
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2020
ms.locfileid: "3690052"
---
# <a name="process-automation"></a><span data-ttu-id="15f1f-103">Prosessautomatisering</span><span class="sxs-lookup"><span data-stu-id="15f1f-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="15f1f-104">Prosessautomatisering tillater enkel planlegging av prosesser som vil bli kjørt av den satsvise serveren.</span><span class="sxs-lookup"><span data-stu-id="15f1f-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="15f1f-105">Den oppdaterte kalendervisningen for det planlagte arbeidet gir sluttbrukerne mulighet til å vise og utføre handlinger på planlagt og fullført arbeid.</span><span class="sxs-lookup"><span data-stu-id="15f1f-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="15f1f-106">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="15f1f-106">Administration</span></span>

<span data-ttu-id="15f1f-107">Du finner siden for sentraladministrasjon for alle prosessautomatiseringer i Systemadministrasjon-modulen på **Oppsett**-menyen.</span><span class="sxs-lookup"><span data-stu-id="15f1f-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="15f1f-108">Denne siden viser en liste over alle automatiserte prosesser (serier) som er konfigurert i systemet.</span><span class="sxs-lookup"><span data-stu-id="15f1f-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="15f1f-109">Du kan også legge til nye prosessautomatiseringer direkte fra denne siden.</span><span class="sxs-lookup"><span data-stu-id="15f1f-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="15f1f-110">Når en serie er definert, kan du administrere hver serie fra denne listen.</span><span class="sxs-lookup"><span data-stu-id="15f1f-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="15f1f-111">Du kan velge å redigere hele serien, slette den, vise alle forekomster i en liste visning eller deaktivere serien hvis du vil stanse det planlagte arbeidet i en tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="15f1f-111">You can chose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a period of time.</span></span> 

<span data-ttu-id="15f1f-112">Prosesser som deaktiveres i funksjonsbehandling, vises ikke når funksjonen er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="15f1f-112">Any processes that are disabled in feature management will not show when the feature is disabled.</span></span> <span data-ttu-id="15f1f-113">I tillegg vil ikke planleggingsmotoren for prosessautomatisering planlegge noen forekomster eller bakgrunnsprosesser for en deaktivert funksjon.</span><span class="sxs-lookup"><span data-stu-id="15f1f-113">Additionally, the Process automation scheduling engine will not schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="15f1f-114">Når du aktiverer funksjonen på nytt, blir planlagte forekomster eller bakgrunnsprosesser i fortiden kjørt umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="15f1f-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span>

## <a name="calendar-view"></a><span data-ttu-id="15f1f-115">Kalendervisning</span><span class="sxs-lookup"><span data-stu-id="15f1f-115">Calendar view</span></span> 
<span data-ttu-id="15f1f-116">En av de viktigste fordelene med prosessautomatisering er muligheten til å se det planlagte arbeidet i en enkel kalendervisning.</span><span class="sxs-lookup"><span data-stu-id="15f1f-116">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="15f1f-117">I denne visningen kan du se arbeid for en uke om gangen.</span><span class="sxs-lookup"><span data-stu-id="15f1f-117">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="15f1f-118">Du vil se denne visningen på høyre side av **Prosessautomatisering**-siden.</span><span class="sxs-lookup"><span data-stu-id="15f1f-118">You will see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="15f1f-119">Det vil bli fylt ut med det planlagte arbeidet for den valgte serien.</span><span class="sxs-lookup"><span data-stu-id="15f1f-119">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="15f1f-120">[![Prosessautomatiseringskalender](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="15f1f-120">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="15f1f-121">Forekomstendringer</span><span class="sxs-lookup"><span data-stu-id="15f1f-121">Occurrence changes</span></span>
<span data-ttu-id="15f1f-122">Hver forekomst kan endres uten å påvirke andre forekomster som er definert av serien de kom fra.</span><span class="sxs-lookup"><span data-stu-id="15f1f-122">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="15f1f-123">Forekomster av planlagt arbeid kan redigeres fra kalendervisningen ved å velge **Vis/rediger**-knappen og velge **Forekomst**.</span><span class="sxs-lookup"><span data-stu-id="15f1f-123">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="15f1f-124">Dette gir deg tilgang til alle innstillingene som opprinnelig vises i veiviseren for serieoppsett, og gir deg muligheten til å utføre en engangsendring for den valgte forekomsten.</span><span class="sxs-lookup"><span data-stu-id="15f1f-124">This allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="15f1f-125">En forekomst av planlagt arbeid kan også deaktiveres ved å velge **Deaktiver**-knappen fra kalendervisningen.</span><span class="sxs-lookup"><span data-stu-id="15f1f-125">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span> 

## <a name="developer-documentation"></a><span data-ttu-id="15f1f-126">Utviklerdokumentasjon</span><span class="sxs-lookup"><span data-stu-id="15f1f-126">Developer documentation</span></span> 
<span data-ttu-id="15f1f-127">Utviklerdokumentasjon skrives for å tillate at utviklerne utvider rammeverket for prosessautomatisering.</span><span class="sxs-lookup"><span data-stu-id="15f1f-127">Developer documentation is currently being written to allow developers to extend the process automation framework.</span></span> <span data-ttu-id="15f1f-128">Denne dokumentasjonen gir informasjon om hvordan du kan opprette egendefinerte prosesser som må kjøres av den satsvise serveren som er planlagt med veiviseren for prosessautomatisering, og som vises automatisk i kalendervisningen.</span><span class="sxs-lookup"><span data-stu-id="15f1f-128">This documentation will provide information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>
