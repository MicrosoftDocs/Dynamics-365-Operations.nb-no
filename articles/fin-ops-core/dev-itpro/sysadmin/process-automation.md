---
title: Prosessautomatisering
description: Dette emnet inneholder detaljer om hvordan prosessautomatisering tillater enkel planlegging av prosesser som vil bli kjørt av den satsvise serveren.
author: RyanCCarlson2
ms.date: 04/20/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProcessScheduleSeries
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.region: Global
ms.author: rcarlson
ms.search.validFrom: 2020-06-30
ms.dyn365.ops.version: AX 10.0.11
ms.openlocfilehash: a8722adfe410f15bc379f9b550f0618c881f067d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920835"
---
# <a name="process-automation"></a><span data-ttu-id="fcb49-103">Prosessautomatisering</span><span class="sxs-lookup"><span data-stu-id="fcb49-103">Process automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fcb49-104">Prosessautomatisering tillater enkel planlegging av prosesser som vil bli kjørt av den satsvise serveren.</span><span class="sxs-lookup"><span data-stu-id="fcb49-104">Process automation allows simple scheduling of processes that will be run by the batch server.</span></span> <span data-ttu-id="fcb49-105">Den oppdaterte kalendervisningen for det planlagte arbeidet gir sluttbrukerne mulighet til å vise og utføre handlinger på planlagt og fullført arbeid.</span><span class="sxs-lookup"><span data-stu-id="fcb49-105">The updated calendar view of the scheduled work allows end users to view and take action on scheduled and completed work.</span></span>

## <a name="administration"></a><span data-ttu-id="fcb49-106">Administrasjon</span><span class="sxs-lookup"><span data-stu-id="fcb49-106">Administration</span></span>

<span data-ttu-id="fcb49-107">Du finner siden for sentraladministrasjon for alle prosessautomatiseringer i Systemadministrasjon-modulen på **Oppsett**-menyen.</span><span class="sxs-lookup"><span data-stu-id="fcb49-107">The central administration page for all process automations is found in the System Administration module under the **Setup** menu.</span></span> <span data-ttu-id="fcb49-108">Denne siden viser en liste over alle automatiserte prosesser (serier) som er konfigurert i systemet.</span><span class="sxs-lookup"><span data-stu-id="fcb49-108">This page will list all automated processes (series) that are set up in the system.</span></span> <span data-ttu-id="fcb49-109">Du kan også legge til nye prosessautomatiseringer direkte fra denne siden.</span><span class="sxs-lookup"><span data-stu-id="fcb49-109">It will also allow you to add new process automations directly from this page.</span></span> <span data-ttu-id="fcb49-110">Når en serie er definert, kan du administrere hver serie fra denne listen.</span><span class="sxs-lookup"><span data-stu-id="fcb49-110">After a series is set up, you can manage each series from this list.</span></span> <span data-ttu-id="fcb49-111">Du kan velge å redigere hele serien, slette den, vise alle forekomster i en liste visning eller deaktivere serien hvis du vil stanse det planlagte arbeidet i en tidsperiode.</span><span class="sxs-lookup"><span data-stu-id="fcb49-111">You can choose to edit the entire series, delete it, view all occurrences in a list view, or disable the series if you would like to pause the scheduled work for a while.</span></span> 

<span data-ttu-id="fcb49-112">Prosesser som deaktiveres i funksjonsbehandling, vises ikke når funksjonen er deaktivert.</span><span class="sxs-lookup"><span data-stu-id="fcb49-112">Any processes that are disabled in feature management won't show when the feature is disabled.</span></span> <span data-ttu-id="fcb49-113">I tillegg vil ikke planleggingsmotoren for prosessautomatisering planlegge noen forekomster eller bakgrunnsprosesser for en deaktivert funksjon.</span><span class="sxs-lookup"><span data-stu-id="fcb49-113">Additionally, the process automation scheduling engine won't schedule any occurrences or background processes for a disabled feature.</span></span> <span data-ttu-id="fcb49-114">Når du aktiverer funksjonen på nytt, blir planlagte forekomster eller bakgrunnsprosesser i fortiden kjørt umiddelbart.</span><span class="sxs-lookup"><span data-stu-id="fcb49-114">Re-enabling the feature will cause any scheduled occurrences or background processes in the past to run immediately.</span></span> <span data-ttu-id="fcb49-115">Planleggingsmotoren for prosessautomatisering er avhengig av systemets satsvise jobb, **Avspørringssystem for prosessautomatisering** for å kjøres.</span><span class="sxs-lookup"><span data-stu-id="fcb49-115">The process automation scheduling engine relies on the system batch job, **Process automation polling system job** to run.</span></span> <span data-ttu-id="fcb49-116">Jobben bør ikke endres på noe tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="fcb49-116">The job shouldn't be altered or tampered with at any time.</span></span> 

## <a name="calendar-view"></a><span data-ttu-id="fcb49-117">Kalendervisning</span><span class="sxs-lookup"><span data-stu-id="fcb49-117">Calendar view</span></span>

<span data-ttu-id="fcb49-118">En av de viktigste fordelene med prosessautomatisering er muligheten til å se det planlagte arbeidet i en enkel kalendervisning.</span><span class="sxs-lookup"><span data-stu-id="fcb49-118">One of the key benefits of process automation is the ability to see the scheduled work in a simple calendar view.</span></span>  <span data-ttu-id="fcb49-119">I denne visningen kan du se arbeid for en uke om gangen.</span><span class="sxs-lookup"><span data-stu-id="fcb49-119">This view allows you to see work for a week at a time.</span></span> <span data-ttu-id="fcb49-120">Du vil se denne visningen på høyre side av **Prosessautomatisering**-siden.</span><span class="sxs-lookup"><span data-stu-id="fcb49-120">You'll see this view on the right side of the **Process automation** page.</span></span> <span data-ttu-id="fcb49-121">Det vil bli fylt ut med det planlagte arbeidet for den valgte serien.</span><span class="sxs-lookup"><span data-stu-id="fcb49-121">It will be populated with the scheduled work for the selected series.</span></span> 

<span data-ttu-id="fcb49-122">[![Prosessautomatiseringskalender](./media/CalendarView2.png)](./media/CalendarView2.png)</span><span class="sxs-lookup"><span data-stu-id="fcb49-122">[![Process automation calendar](./media/CalendarView2.png)](./media/CalendarView2.png)</span></span>

## <a name="occurrence-changes"></a><span data-ttu-id="fcb49-123">Forekomstendringer</span><span class="sxs-lookup"><span data-stu-id="fcb49-123">Occurrence changes</span></span>

<span data-ttu-id="fcb49-124">Hver forekomst kan endres uten å påvirke andre forekomster som er definert av serien de kom fra.</span><span class="sxs-lookup"><span data-stu-id="fcb49-124">Each occurrence can be modified without impacting other occurrences defined by the series that originated them.</span></span> <span data-ttu-id="fcb49-125">Forekomster av planlagt arbeid kan redigeres fra kalendervisningen ved å velge **Vis/rediger**-knappen og velge **Forekomst**.</span><span class="sxs-lookup"><span data-stu-id="fcb49-125">Occurrences of scheduled work can be edited from the calendar view by selecting the **View/Edit** button and selecting **Occurrence**.</span></span> <span data-ttu-id="fcb49-126">Denne siden gir deg tilgang til alle innstillingene som opprinnelig vises i veiviseren for serieoppsett, og gir deg muligheten til å utføre en engangsendring for den valgte forekomsten.</span><span class="sxs-lookup"><span data-stu-id="fcb49-126">This page allows you access to all the settings originally shown in the series setup wizard and provides the ability to make a one-off change for the selected occurrence.</span></span> <span data-ttu-id="fcb49-127">En forekomst av planlagt arbeid kan også deaktiveres ved å velge **Deaktiver**-knappen fra kalendervisningen.</span><span class="sxs-lookup"><span data-stu-id="fcb49-127">An occurrence of scheduled work can also be turned off by selecting the **Disable** button from the calendar view.</span></span>

## <a name="developer-documentation"></a><span data-ttu-id="fcb49-128">Utviklerdokumentasjon</span><span class="sxs-lookup"><span data-stu-id="fcb49-128">Developer documentation</span></span>

<span data-ttu-id="fcb49-129">Rammeverk for prosessautomatisering gjør det mulig for utviklere å utvide rammeverket for prosessautomatisering.</span><span class="sxs-lookup"><span data-stu-id="fcb49-129">The process automation framework allows developers to extend the process automation framework.</span></span> <span data-ttu-id="fcb49-130">Dokumentasjonen for [Rammeverk for prosessautomatisering](../process-automation/process-automation-framework.md) gir informasjon om hvordan du kan opprette egendefinerte prosesser som må kjøres av den satsvise serveren som er planlagt med veiviseren for prosessautomatisering, og som vises automatisk i kalendervisningen.</span><span class="sxs-lookup"><span data-stu-id="fcb49-130">The [Process automation framework](../process-automation/process-automation-framework.md) documentation provides information about how you can create custom processes that you require to be run by the batch server scheduled with the process automation wizard and appear in the calendar view automatically.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
