---
title: Vedlikeholdsanmodninger
description: Dette emnet gir en oversikt over administrasjon av vedlikeholdsanmodninger i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 56d4abee451e6e22b9b9cc2fd36a13648202e7df
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847442"
---
# <a name="maintenance-requests"></a><span data-ttu-id="a7421-103">Vedlikeholdsanmodninger</span><span class="sxs-lookup"><span data-stu-id="a7421-103">Maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="a7421-104">Vedlikeholdsanmodninger er notater eller deklarasjoner som opprettes for å varsle en leder eller planlegger at et aktivum kan kreve en vedlikeholds- eller reparasjonsjobb, men uten å opprette en arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="a7421-104">Maintenance requests are notes or declarations that are created to notify a manager or planner that an asset might require a maintenance or repair job, but without creating a work order.</span></span> <span data-ttu-id="a7421-105">Hvis innholdet i en vedlikeholdsanmodning anses som gyldig, kan en arbeidsordre opprettes basert på vedlikeholdsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a7421-105">If the contents of a maintenance request are considered valid, a work order can then be created based on the maintenance request.</span></span>

<span data-ttu-id="a7421-106">Vedlikeholdsanmodninger kan opprettes for alle aktiva i Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="a7421-106">Maintenance requests can be created for any asset in Asset Management.</span></span> <span data-ttu-id="a7421-107">Ulike typer vedlikeholdsanmodninger kan opprettes, avhengig av hvordan firmaet bruker vedlikeholdsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="a7421-107">Various types of maintenance requests can be created, depending on how your company uses maintenance requests.</span></span> <span data-ttu-id="a7421-108">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="a7421-108">Here are some examples:</span></span>

- <span data-ttu-id="a7421-109">Vedlikeholdsanmodninger</span><span class="sxs-lookup"><span data-stu-id="a7421-109">Maintenance requests</span></span>
- <span data-ttu-id="a7421-110">Notater</span><span class="sxs-lookup"><span data-stu-id="a7421-110">Notes</span></span>
- <span data-ttu-id="a7421-111">Korrigeringer eller forbedringer</span><span class="sxs-lookup"><span data-stu-id="a7421-111">Corrections or enhancements</span></span>
- <span data-ttu-id="a7421-112">Investeringer</span><span class="sxs-lookup"><span data-stu-id="a7421-112">Investments</span></span>
- <span data-ttu-id="a7421-113">Depotreparasjon (denne typen brukes når du mottar aktiva fra et annet sted, slik at du kan utføre en vedlikeholds- eller reparasjonsjobb, og deretter returnere aktivaet etter at jobben er fullført.)</span><span class="sxs-lookup"><span data-stu-id="a7421-113">Depot repair (This type is used when you receive assets from another location so that you can do a maintenance or repair job, and you then return the asset after the job is completed.)</span></span>

## <a name="view-maintenance-requests"></a><span data-ttu-id="a7421-114">Vis vedlikeholdsanmodninger</span><span class="sxs-lookup"><span data-stu-id="a7421-114">View maintenance requests</span></span>

<span data-ttu-id="a7421-115">Hvis du vil vise vedlikeholdsanmodninger, velger du **Aktivastyring** \> **Felles** \> **Vedlikeholdsanmondninger** \> **Alle vedlikeholdsanmodninger**, **Aktive vedlikeholdsanmodninger** eller **Mine vedlikeholdsforespørsler for arbeidssted**.</span><span class="sxs-lookup"><span data-stu-id="a7421-115">To view maintenance requests, select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests**, **Active maintenance requests**, or **My functional location maintenance requests**.</span></span> <span data-ttu-id="a7421-116">Hver listeside viser noe av informasjonen som er knyttet til en vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="a7421-116">Each list page shows some of the information that is related to a maintenance request.</span></span>

![Figur 1](media/01-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="a7421-118">Bruk listesiden **Mine vedlikeholdsforespørsler for arbeidssted** for å vise en liste over vedlikeholdsforespørsler som inneholder enten arbeidssteder som du er knyttet til som arbeider, eller aktiva som er installert på arbeidssteder som du knyttet til som arbeider.</span><span class="sxs-lookup"><span data-stu-id="a7421-118">Use the **My functional location maintenance requests** list page to view a list of maintenance requests that contain either functional locations that you're related to as a worker or assets that are installed on functional locations that you're related to as a worker.</span></span> <span data-ttu-id="a7421-119">(Hvis du vil ha informasjon om hvordan du definerer arbeidssteder for vedlikeholdspersoner, kan du se [Vedlikeholdspersoner og arbeidsgrupper](../setup-for-objects/workers-and-worker-groups.md).)</span><span class="sxs-lookup"><span data-stu-id="a7421-119">(For information about how to set up functional locations on maintenance workers, see [Maintenance workers and worker groups](../setup-for-objects/workers-and-worker-groups.md).)</span></span>
> 
> <span data-ttu-id="a7421-120">Selv om kundekontoinformasjon er tilgjengelig i Aktivaservicestyring (eksternt vedlikehold), er den ikke tilgjengelig i Aktivastyring (internt vedlikehold).</span><span class="sxs-lookup"><span data-stu-id="a7421-120">Although customer account information is available in Asset Service Management (external maintenance), it isn't available in Asset Management (internal maintenance).</span></span>

<span data-ttu-id="a7421-121">Hvis du vil åpne detaljvisningen for en post, går du til listesiden **Alle vedlikeholdsanmodninger**, og i rutenettvisningen velger du en kobling i kolonnen **Vedlikeholdsanmodning**.</span><span class="sxs-lookup"><span data-stu-id="a7421-121">To open the details view of a record, on the **All maintenance requests** list page, in the grid view, select a link in the **Maintenance request** column.</span></span>

![Figur 2](media/02-manage-maintenance-requests.png)

<span data-ttu-id="a7421-123">Knappene i handlingsruten er ordnet i kategorier.</span><span class="sxs-lookup"><span data-stu-id="a7421-123">The buttons on the Action Pane are organized on tabs.</span></span> <span data-ttu-id="a7421-124">Følgende tabell beskriver kort hvilke knapper som er knyttet til Aktivastyring.</span><span class="sxs-lookup"><span data-stu-id="a7421-124">The following table briefly describes the buttons that are related to Asset Management.</span></span>

| <span data-ttu-id="a7421-125">Navn på knapp</span><span class="sxs-lookup"><span data-stu-id="a7421-125">Button name</span></span>                      | <span data-ttu-id="a7421-126">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a7421-126">Description</span></span> |
|----------------------------------|-------------|
| <span data-ttu-id="a7421-127">Rediger</span><span class="sxs-lookup"><span data-stu-id="a7421-127">Edit</span></span>                             | <span data-ttu-id="a7421-128">Rediger den valgte vedlikeholdsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a7421-128">Edit the selected maintenance request.</span></span> |
| <span data-ttu-id="a7421-129">Nye</span><span class="sxs-lookup"><span data-stu-id="a7421-129">New</span></span>                              | <span data-ttu-id="a7421-130">Opprett en ny vedlikeholdsanmodning.</span><span class="sxs-lookup"><span data-stu-id="a7421-130">Create a new maintenance request.</span></span> |
| <span data-ttu-id="a7421-131">Slett</span><span class="sxs-lookup"><span data-stu-id="a7421-131">Delete</span></span>                           | <span data-ttu-id="a7421-132">Slett den valgte vedlikeholdsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a7421-132">Delete the selected maintenance request.</span></span> |
| <span data-ttu-id="a7421-133">Arbeidsordresamling</span><span class="sxs-lookup"><span data-stu-id="a7421-133">Work order pool</span></span>                  | <span data-ttu-id="a7421-134">Koble den valgte vedlikeholdsanmodningen til en arbeidsordresamling.</span><span class="sxs-lookup"><span data-stu-id="a7421-134">Connect the selected maintenance request to a work order pool.</span></span> |
| <span data-ttu-id="a7421-135">Arbeidsordre</span><span class="sxs-lookup"><span data-stu-id="a7421-135">Work order</span></span>                       | <span data-ttu-id="a7421-136">Opprett en arbeidsordre, basert på den valgte vedlikeholdsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a7421-136">Create a work order, based on the selected maintenance request.</span></span> |
| <span data-ttu-id="a7421-137">Aktivumfeil</span><span class="sxs-lookup"><span data-stu-id="a7421-137">Asset fault</span></span>                      | <span data-ttu-id="a7421-138">Klikk på **Aktivumfeil**, der du kan opprette en feilregistrering for den valgte vedlikeholdsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a7421-138">Click **Asset faults**, where you can create a fault registration on the selected maintenance request.</span></span> |
| <span data-ttu-id="a7421-139">Arbeidsordrer</span><span class="sxs-lookup"><span data-stu-id="a7421-139">Work orders</span></span>                      | <span data-ttu-id="a7421-140">Vis en liste over alle arbeidsordrer som er koblet til den valgte vedlikeholdsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a7421-140">Show a list of all work orders that are connected to the selected maintenance request.</span></span> |
| <span data-ttu-id="a7421-141">Oppdater tilstand for vedlikeholdsanmodning</span><span class="sxs-lookup"><span data-stu-id="a7421-141">Update maintenance request state</span></span> | <span data-ttu-id="a7421-142">Oppdater tilstanden for vedlikeholdsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a7421-142">Update the maintenance request state.</span></span> |
| <span data-ttu-id="a7421-143">Logg for livsløpstilstand</span><span class="sxs-lookup"><span data-stu-id="a7421-143">Lifecycle state log</span></span>              | <span data-ttu-id="a7421-144">Vis en logg som viser livsløpstilstandene til den valgte vedlikeholdsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a7421-144">View a log that shows the lifecycle states of the selected maintenance request.</span></span> |
| <span data-ttu-id="a7421-145">Detaljer om vedlikeholdsanmodninger</span><span class="sxs-lookup"><span data-stu-id="a7421-145">Maintenance request details</span></span>      | <span data-ttu-id="a7421-146">Skriv ut en rapport som viser detaljer om den valgte vedlikeholdsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a7421-146">Print a report that shows details of the selected maintenance request.</span></span> |
| <span data-ttu-id="a7421-147">Send ut aktivumlån</span><span class="sxs-lookup"><span data-stu-id="a7421-147">Send loan asset</span></span>                  | <span data-ttu-id="a7421-148">Velg et aktivumlån som skal være en midlertidig erstatning for aktivumet som er valgt i den valgte vedlikeholdsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="a7421-148">Select a loan asset that should be a temporary replacement for the asset that is selected on the selected maintenance request.</span></span> |
| <span data-ttu-id="a7421-149">Returner lån av gjenstander</span><span class="sxs-lookup"><span data-stu-id="a7421-149">Return loan asset</span></span>                | <span data-ttu-id="a7421-150">Registrer aktivumlånet som returnert.</span><span class="sxs-lookup"><span data-stu-id="a7421-150">Register the loan asset as returned.</span></span> |

