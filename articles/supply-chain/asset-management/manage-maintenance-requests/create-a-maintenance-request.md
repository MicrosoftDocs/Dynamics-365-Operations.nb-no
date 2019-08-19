---
title: Opprette vedlikeholdsforespørsler
description: Dette emnet forklarer hvordan du oppretter en vedlikeholdsforespørsel i Aktivastyring.
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
ms.openlocfilehash: 03e090633276cd264ad03f561ddb425a9816357e
ms.sourcegitcommit: 871b76f8808a48d282f151144829323258ffc912
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/02/2019
ms.locfileid: "1847511"
---
# <a name="create-maintenance-requests"></a><span data-ttu-id="b6d0f-103">Opprette vedlikeholdsforespørsler</span><span class="sxs-lookup"><span data-stu-id="b6d0f-103">Create maintenance requests</span></span>

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

<span data-ttu-id="b6d0f-104">Vedlikeholdsforespørsler kan brukes hvis vedlikeholdsarbeidere eller produksjonsarbeidere oppdager at utstyr krever reparasjon, men reparasjonsjobben kan ikke utføres med en gang.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-104">Maintenance requests can be used if maintenance workers or production workers discover that equipment requires repair, but the repair job can't be done right away.</span></span>

<span data-ttu-id="b6d0f-105">**Eksempel:** Mens en vedlikeholdsarbeider foretar en reparasjon, oppdager hun at et annet aktivum på samme lokasjon må ha service.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-105">**Example:** While a maintenance worker is making a repair, she discovers that another asset at the same location must be serviced.</span></span> <span data-ttu-id="b6d0f-106">Vedlikeholdsarbeideren har imidlertid ikke tid eller nødvendige reservedeler til å utføre reparasjonsjobben.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-106">However, the maintenance worker doesn't have the time or the required spare parts to do the repair job.</span></span> <span data-ttu-id="b6d0f-107">Derfor oppretter hun en vedlikeholdsforespørsel på aktivumet og angir en kort beskrivelse av problemet.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-107">Therefore, she creates a maintenance request on the asset and enters a short description of the issue.</span></span>

<span data-ttu-id="b6d0f-108">Delen **Aktive vedlikeholdsforespørsler** i ruten **Relatert informasjon** til høyre for **Alle aktiva** eller **Aktive aktiva**-siden (**Aktivastyring** \> **Felles** \> **Aktiva** \> **Alle aktiva** eller **Aktive aktiva**) viser vedlikeholdsforespørslene som er knyttet til det valgte aktivumet.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-108">The **Active maintenance requests** section of the **Related information** pane on the right side of the **All assets** or **Active assets** page (**Asset management** \> **Common** \> **Assets** \> **All assets** or **Active assets**) shows the active maintenance requests that are attached to the selected asset.</span></span>

1. <span data-ttu-id="b6d0f-109">Velg **Aktivastyring** \> **Felles** \> **Vedlikeholdsforespørsler** \> **Alle vedlilkeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-109">Select **Asset management** \> **Common** \> **Maintenance requests** \> **All maintenance requests** or **Active maintenance requests**.</span></span>
2. <span data-ttu-id="b6d0f-110">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-110">Select **New**.</span></span>
3. <span data-ttu-id="b6d0f-111">I dialogboksen **Opprett forespørsel** i feltet **Type vedlikeholdsforespørsel** velger du typen vedlikeholdsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-111">In the **Create request** dialog box, in the **Maintenance request type** field, select the type of maintenance request.</span></span> <span data-ttu-id="b6d0f-112">En standardtype foreslås.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-112">A default type is suggested.</span></span>
4. <span data-ttu-id="b6d0f-113">I **Beskrivelse**-feltet skriver du inn et navn eller en tittel som kort beskriver vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-113">In the **Description** field, enter a name or title that briefly describes the maintenance request.</span></span>
5. <span data-ttu-id="b6d0f-114">I feltene **Arbeidssted** og **Aktivum** velger du et arbeidssted eller et aktivum eller en kombinasjon av begge deler, alt etter behov.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-114">In the **Functional location** and **Asset** fields, select a functional location or an asset, or a combination of a functional location and an asset, as you require.</span></span> <span data-ttu-id="b6d0f-115">Du kan opprette en vedlikeholdsforespørsel uten å velge et aktivum, og aktivumet kan legges til i vedlikeholdsforespørselen senere.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-115">You can create a maintenance request without selecting an asset, and the asset can be added to the maintenance request later.</span></span> <span data-ttu-id="b6d0f-116">Hvis vedlikeholdspersonen som er logget på Microsoft Dynamics 365 for Finance and Operations, er knyttet til en ressurs som er knyttet til et aktivum, angis **Aktivum**-feltet automatisk.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-116">If the maintenance worker who is signed in to Microsoft Dynamics 365 for Finance and Operations is related to a resource that is related to an asset, the **Asset** field is automatically set.</span></span>

    <span data-ttu-id="b6d0f-117">Hvis en vedlikeholdsforespørsel allerede er knyttet til det valgte aktivumet, vises en meldingslinje øverst i dialogboksen **Opprett forespørsel** for å varsle deg om ID-en for den eksisterende vedlikeholdsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-117">If a maintenance request is already attached to the selected asset, a message bar appears at the top of the **Create request** dialog box to notify you about the ID of the existing maintenance request.</span></span> <span data-ttu-id="b6d0f-118">En meldingslinje varsler deg også hvis aktivumet dekkes av en garantiavtale.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-118">A message bar also notifies you if the asset is covered by a warranty agreement.</span></span>

6. <span data-ttu-id="b6d0f-119">I feltet **Servicenivå** velger du et servicenivå som angir viktigheten av forespørselen.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-119">In the **Service level** field, select a service level that indicates the urgency of the request.</span></span>
7. <span data-ttu-id="b6d0f-120">Hvis du valgte et aktivum i trinn 5, kan du bruke feltene **Feilsymptom**, **Feilområde** og **Feiltype** til å opprette en feilregistrering.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-120">If you selected an asset in step 5, you can use the **Fault symptom**, **Fault area**, and **Fault type** fields to create a fault registration.</span></span>
8. <span data-ttu-id="b6d0f-121">Hvis vedlikeholdsforespørselen har forårsaket nedetid for vedlikehold, angir du startdatoen og klokkeslettet for nedetiden.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-121">If the maintenance request has caused maintenance downtime, enter the start date and time of the downtime.</span></span>

    <span data-ttu-id="b6d0f-122">Feltet **Startet av** blir automatisk satt til ditt navn.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-122">The **Started by** field is automatically set to your name.</span></span>

10. <span data-ttu-id="b6d0f-123">**Faktisk start**-feltet settes automatisk til gjeldende dato og klokkeslett.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-123">The **Actual start** field is automatically set to the current date and time.</span></span> <span data-ttu-id="b6d0f-124">Du kan imidlertid endre verdien etter behov.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-124">However, you can change the value as you require.</span></span>
11. <span data-ttu-id="b6d0f-125">Angi eventuelle tilleggsmerknader i feltet **Notater**.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-125">In the **Notes** field, enter any additional notes that are required.</span></span>
12. <span data-ttu-id="b6d0f-126">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-126">Select **OK**.</span></span>

![Figur 1](media/03-manage-maintenance-requests.png)

## <a name="subsequent-processing-of-maintenance-requests"></a><span data-ttu-id="b6d0f-128">Påfølgende behandling av vedlikeholdsforespørsler</span><span class="sxs-lookup"><span data-stu-id="b6d0f-128">Subsequent processing of maintenance requests</span></span>

<span data-ttu-id="b6d0f-129">Når en vedlikeholdsforespørsel er opprettet, men før den konverteres til en arbeidsordre, bør diverse informasjon oppdateres på den.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-129">After a maintenance request is created, but before it's converted to a work order, various information should be updated on it.</span></span> <span data-ttu-id="b6d0f-130">Vanligvis fullfører en planlegger eller en annen administrativ ansatt denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-130">Typically, a planner or another administrative employee completes this task.</span></span>

- <span data-ttu-id="b6d0f-131">På siden **Alle vedlikeholdsforespørsler** eller **Aktive vedlikeholdsforespørsler** velger du forespørselen du vil arbeide med, og deretter velger du **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-131">On the **All maintenance requests** or **Active maintenance requests** page, select the request to work with, and then select **Edit**.</span></span>

<span data-ttu-id="b6d0f-132">I detaljvisningen kan du oppdatere forskjellig informasjon.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-132">In the details view, you can update various information.</span></span> <span data-ttu-id="b6d0f-133">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="b6d0f-133">Here are some examples:</span></span>

- <span data-ttu-id="b6d0f-134">Velg og kontroller aktivumet.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-134">Select and verify the asset.</span></span> <span data-ttu-id="b6d0f-135">Hvis du må velge et annet aktivum senere, kan du sette alternativet **Aktivum bekreftet** til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-135">If you must select a different asset later, you can set the **Asset verified** option to **No**.</span></span>
- <span data-ttu-id="b6d0f-136">Velg en ansvarlig vedlikeholdspersongruppe og/eller en ansvarlig vedlikeholdsperson.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-136">Select a responsible maintenance worker group and/or a responsible maintenance worker.</span></span> <span data-ttu-id="b6d0f-137">Hvis du vil ha mer informasjon om nødvendig oppsett, kan du se [Ansvarlige vedlikeholdspersoner](../setup-for-maintenance-requests/responsible-workers.md).</span><span class="sxs-lookup"><span data-stu-id="b6d0f-137">For more information about the required setup, see [Responsible maintenance workers](../setup-for-maintenance-requests/responsible-workers.md).</span></span>
- <span data-ttu-id="b6d0f-138">Velg en vedlikeholdsjobbtype og, hvis denne informasjonen er relevant, en relatert vedlikeholdsjobbvariant og et jobbfag.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-138">Select a maintenance job type and, if this information is relevant, a related maintenance job variant and a job trade.</span></span>
- <span data-ttu-id="b6d0f-139">Angi geografiske koordinater i feltene **Breddegrad** og **Lengdegrad**.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-139">In the **Latitude** and **Longitude** fields, enter geographic coordinates.</span></span> <span data-ttu-id="b6d0f-140">Alle koordinater som legges til i en vedlikeholdsforespørsel, overføres automatisk til en relatert arbeidsordre.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-140">Any coordinates that are added to a maintenance request are automatically transferred to a related work order.</span></span> 

![Figur 2](media/04-manage-maintenance-requests.png)

> [!NOTE]
> <span data-ttu-id="b6d0f-142">Hvis du velger et aktivum når du oppretter en vedlikeholdsforespørsel, kan du legge til én feil i aktivumet.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-142">If you select an asset when you create a maintenance request, you can add one fault to the asset.</span></span> <span data-ttu-id="b6d0f-143">Etter at vedlikeholdsforespørselen er opprettet, kan du legge til flere feil, etter behov.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-143">After the maintenance request has been created, you can add more faults, as you require.</span></span> <span data-ttu-id="b6d0f-144">Hvis du vil legge til feil, velger du **Aktivafeil** på siden **Alle vedlikeholdsforespørsler**.</span><span class="sxs-lookup"><span data-stu-id="b6d0f-144">To add faults, select **Asset fault** on the **All maintenance requests** page.</span></span>
