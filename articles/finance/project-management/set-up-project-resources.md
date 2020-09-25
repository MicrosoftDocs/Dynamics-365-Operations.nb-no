---
title: Definere prosjektressurser
description: Dette emnet gir informasjon om hvordan du konfigurerer eller ber om prosjektressurser.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c882e23794e3937f85b3e73774b36deaf28ac3ed
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760628"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="dcefb-103">Definere prosjektressurser</span><span class="sxs-lookup"><span data-stu-id="dcefb-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="dcefb-104">Du må opprette en kalender og knytte den til en ansatt eller en arbeider.</span><span class="sxs-lookup"><span data-stu-id="dcefb-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="dcefb-105">Kalenderen brukes til å planlegge prosjektet og arbeidstiden for ressursene som er reservert for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="dcefb-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="dcefb-106">Under kalenderoppsett kan prosjektledere gjøre ressursnivåering som en del av ressursoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="dcefb-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="dcefb-107">Basert på kalenderplanen kan restriksjoner legges på ressurser.</span><span class="sxs-lookup"><span data-stu-id="dcefb-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="dcefb-108">Du kan opprette en kalender på siden **Kalendere**.</span><span class="sxs-lookup"><span data-stu-id="dcefb-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="dcefb-109">Når du setter opp en arbeidstaker som en prosjektressurs, kan du velge blant arbeidere som jobber i selskapet som du setter opp ressurser til.</span><span class="sxs-lookup"><span data-stu-id="dcefb-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="dcefb-110">Alternativt kan du velge arbeidstakere fra andre selskaper i organisasjonen din.</span><span class="sxs-lookup"><span data-stu-id="dcefb-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="dcefb-111">Disse arbeidstakere er kjent som konserninterne ressurser.</span><span class="sxs-lookup"><span data-stu-id="dcefb-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="dcefb-112">Følgende prosedyrer forklarer hvordan du setter opp en arbeidstaker som en prosjektressurs i firmaet ditt, og hvordan du oppretter en konsernintern prosjektressurs.</span><span class="sxs-lookup"><span data-stu-id="dcefb-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="dcefb-113">Definere en arbeider som en prosjektressurs</span><span class="sxs-lookup"><span data-stu-id="dcefb-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="dcefb-114">I **Arbeidere**-listen på siden **Arbeidere**, velger du arbeideren som du legger til som en prosjektressurs, og åpner arbeiderposten.</span><span class="sxs-lookup"><span data-stu-id="dcefb-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="dcefb-115">På Handling-panelet velger du **Prosjekt** &gt; **Oppsett** &gt; **Prosjektoppsett**.</span><span class="sxs-lookup"><span data-stu-id="dcefb-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="dcefb-116">Velg en kalender, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="dcefb-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="dcefb-117">Du kan også angi standardprosjekter for en ressurs som en type førtilordning.</span><span class="sxs-lookup"><span data-stu-id="dcefb-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="dcefb-118">Førtildelinger kan brukes når ressursansvarlig eller prosjektleder vet hvilke prosjekter som ressursen vil arbeide med på forhånd.</span><span class="sxs-lookup"><span data-stu-id="dcefb-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="dcefb-119">Førtildelinger kan også være basert på forespørsel fra en prosjektsponsor eller kunde.</span><span class="sxs-lookup"><span data-stu-id="dcefb-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="dcefb-120">Hvis du vil førtilordne et prosjekt, på siden **Tilordne prosjekter** i kategorien **Prosjekter** i lsietn **Gjenværende prosjekter**, velger du det aktuelle prosjektet.</span><span class="sxs-lookup"><span data-stu-id="dcefb-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="dcefb-121">Definere en konsernintern ressurs</span><span class="sxs-lookup"><span data-stu-id="dcefb-121">Set up an intercompany resource</span></span>

<span data-ttu-id="dcefb-122">Når du setter opp en arbeidstaker som en konsernintern ressurs, må du fullføre oppsettet i både utlånsfirmaet og lånefirmaet.</span><span class="sxs-lookup"><span data-stu-id="dcefb-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="dcefb-123">I utlånsselskapet</span><span class="sxs-lookup"><span data-stu-id="dcefb-123">In the lending company</span></span>

1. <span data-ttu-id="dcefb-124">Kontroller at utlånsfirmaet er valgt i Finance, og fullfør deretter prosedyren i forrige avsnitt, «Sett opp en arbeidstaker som en prosjektressurs».</span><span class="sxs-lookup"><span data-stu-id="dcefb-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="dcefb-125">På siden **Konserninternt regnskap**, velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dcefb-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="dcefb-126">I feltet **ID for juridisk enhet**, velg utlånsselskapet.</span><span class="sxs-lookup"><span data-stu-id="dcefb-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="dcefb-127">Fyll ut de resterende feltene etter behov, og velg deretter **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="dcefb-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="dcefb-128">På siden **Overføringspris**, velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="dcefb-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="dcefb-129">I feltet **Lånende juridisk enhet**, velg riktig selskap.</span><span class="sxs-lookup"><span data-stu-id="dcefb-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="dcefb-130">For å låne kun den ressursen du opprettet i begynnelsen av denne delen fra utlånsselskapet, gå til feltet **Ressurs**, og velg navnet på ressursen du har opprettet.</span><span class="sxs-lookup"><span data-stu-id="dcefb-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="dcefb-131">For å gjøre alle ressurser i det lånende selskapet tilgjengelig til utlånsselskapet lar du feltet **Ressurs** være tomt.</span><span class="sxs-lookup"><span data-stu-id="dcefb-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="dcefb-132">På siden **Parametere for prosjektledelse og regnskap**, i kategorien **Konsernintern**, velg **Aktiver konsernintern ressursplanlegging og tidsskjemaer**-alternativet som **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dcefb-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="dcefb-133">I det lånende selskapet</span><span class="sxs-lookup"><span data-stu-id="dcefb-133">In the borrowing company</span></span>

- <span data-ttu-id="dcefb-134">I søkefiltere på siden **Ressursliste**, skriv inn navnet på den ressursen du har opprettet for det lånende selskap for å bekrefte at navnet er inkludert i ressurslisten for det lånende selskap.</span><span class="sxs-lookup"><span data-stu-id="dcefb-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="dcefb-135">Be om prosjektressurser</span><span class="sxs-lookup"><span data-stu-id="dcefb-135">Request project resources</span></span>
<span data-ttu-id="dcefb-136">Funksjonaliteten for prosjektressursplanlegging lar kun ressursforvaltere distribuere bemannede ressurser på engasjementer eller prosjekter.</span><span class="sxs-lookup"><span data-stu-id="dcefb-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="dcefb-137">For å aktivere denne funksjonaliteten, fullfør følgende oppgaver, eller bekreft at de er fullført:</span><span class="sxs-lookup"><span data-stu-id="dcefb-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="dcefb-138">Definer nummerserier.</span><span class="sxs-lookup"><span data-stu-id="dcefb-138">Set up number sequences.</span></span>
- <span data-ttu-id="dcefb-139">Definer arbeidsflyter for prosjektstyring og regnskap.</span><span class="sxs-lookup"><span data-stu-id="dcefb-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="dcefb-140">Aktiver arbeidsflyten for ressursforespørsel.</span><span class="sxs-lookup"><span data-stu-id="dcefb-140">Enable resource request workflows.</span></span>

<span data-ttu-id="dcefb-141">Etter at de foregående oppgavene er fullført, kan du fullføre følgende oppgaver som du trenger:</span><span class="sxs-lookup"><span data-stu-id="dcefb-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="dcefb-142">Opprett en ressursforespørsel fra en ikke-forpliktende bemannet ressurs.</span><span class="sxs-lookup"><span data-stu-id="dcefb-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="dcefb-143">Overvåk ressursforespørsler.</span><span class="sxs-lookup"><span data-stu-id="dcefb-143">Monitor resource requests.</span></span>
- <span data-ttu-id="dcefb-144">Oppfyll ressursforespørsler.</span><span class="sxs-lookup"><span data-stu-id="dcefb-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="dcefb-145">Etterspør en bemannet ressurs fra en WBS.</span><span class="sxs-lookup"><span data-stu-id="dcefb-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="dcefb-146">Bestill ressurser til et prosjekt uten å ha en forespørsel om en bemannet ressurs.</span><span class="sxs-lookup"><span data-stu-id="dcefb-146">Book resources to a project without having a request for a staffed resource.</span></span>
