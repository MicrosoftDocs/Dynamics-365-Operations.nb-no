---
title: Opprett nytt prosjekt
description: Dette emnet gir informasjon om hvordan du oppretter et nytt prosjekt.
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
ms.openlocfilehash: c8c52b8c1c86ea2f6e03cf439ba5930f1006ab4f
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760623"
---
# <a name="create-a-new-project"></a><span data-ttu-id="23a44-103">Opprett nytt prosjekt</span><span class="sxs-lookup"><span data-stu-id="23a44-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="23a44-104">Fullfør fremgangsmåten nedenfor for å opprette et nytt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="23a44-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="23a44-105">På siden **Prosjektledelse**, velg **Nytt prosjekt**, og skriv inn følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="23a44-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="23a44-106">**Prosjekttype:** Tid og materialer</span><span class="sxs-lookup"><span data-stu-id="23a44-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="23a44-107">**Prosjektnavn:** XYZ-oppgraderingsfase 2</span><span class="sxs-lookup"><span data-stu-id="23a44-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="23a44-108">**Prosjektgruppe:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="23a44-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="23a44-109">**Prosjektkontrakt-ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="23a44-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="23a44-110">Velg **Opprett prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="23a44-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="23a44-111">Tilordne en ressurs til et prosjekt</span><span class="sxs-lookup"><span data-stu-id="23a44-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="23a44-112">På siden **Arbeidstakere** i listen **Arbeidstakere**, velg den oppføringen for den arbeidstakeren du tidligere har satt opp kompetanse for. Åpne deretter arbeidstakerens oppføring.</span><span class="sxs-lookup"><span data-stu-id="23a44-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="23a44-113">På Handling-panelet, i kategorien **Prosjekt**, i gruppen **Oppsett**, velg **Tilordne prosjekt**.</span><span class="sxs-lookup"><span data-stu-id="23a44-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="23a44-114">På siden **Oppgaver for ressursvalideringsprosjekt**, i kategorien **Prosjekter**, i **Legg til prosjektet til valgte prosjekter**-feltet, filtrer på **XYZ oppgraderingsfase 2**-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="23a44-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="23a44-115">I vinduet **Gjenstående prosjekter**, velg ett prosjekt og velg deretter pilknappen for å legge det til vinduet **Valgte prosjekter**.</span><span class="sxs-lookup"><span data-stu-id="23a44-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="23a44-116">Du kan også tildele kategorier for en ressurs etter behov.</span><span class="sxs-lookup"><span data-stu-id="23a44-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="23a44-117">Kategoritypen er enten **Kostnad** eller **Inntekt**.</span><span class="sxs-lookup"><span data-stu-id="23a44-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="23a44-118">Kategoritypen bestemmes av organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="23a44-118">The category type is determined by your organization.</span></span> <span data-ttu-id="23a44-119">Hvis ingen kategorier er tildelt for en ressurs, finner Finance standardkategori på timepriser for kostnader og inntekter.</span><span class="sxs-lookup"><span data-stu-id="23a44-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="23a44-120">Definere egenskaper for prosjektressurs og rolle</span><span class="sxs-lookup"><span data-stu-id="23a44-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="23a44-121">En prosjektleder kan bruke prosjektetressursfunksjonaliteten til å opprette roller som kreves for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="23a44-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="23a44-122">Roller kan brukes hvis bekreftede ressurser er ukjente når ressursene blir reservert.</span><span class="sxs-lookup"><span data-stu-id="23a44-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="23a44-123">Roller kan reserveres midlertidig som planlagte ressurser, slik at du kan fortsette prosjektetplanleggingsfasene.</span><span class="sxs-lookup"><span data-stu-id="23a44-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="23a44-124">[![Eksempel på en rolle](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="23a44-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="23a44-125">**Scenario:** Contoso ble ansatt for å fullføre et tid og materialer-prosjekt som har et godkjent prosjektdokument.</span><span class="sxs-lookup"><span data-stu-id="23a44-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="23a44-126">Den underordnede prosjektlederen fullfører fremdeles omfanget av prosjektet.</span><span class="sxs-lookup"><span data-stu-id="23a44-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="23a44-127">Ressursbehandleren identifiserer de bestemte ressursene som skal reserveres, for å arbeide med det nye prosjektet.</span><span class="sxs-lookup"><span data-stu-id="23a44-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="23a44-128">På grunn av prosjektets kritiske karakter, forespurte prosjektsponsoren Senior prosjektleder som en av rollene.</span><span class="sxs-lookup"><span data-stu-id="23a44-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="23a44-129">Den ressursansvarlige må anskaffe den nye ressursen og definere rollen i systemet dersom junior prosjektleder krever ressursinformasjon under prosjektplanlegging.</span><span class="sxs-lookup"><span data-stu-id="23a44-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="23a44-130">Følgende fremgangsmåte viser hvordan ressursbehandleren kan definere rollen som overordnet prosjektleder og tilknytte ressursegenskaper til den.</span><span class="sxs-lookup"><span data-stu-id="23a44-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="23a44-131">Rollen kan senere brukes til å søke etter ressurser som samsvarer med de nødvendige ressurskompetansene.</span><span class="sxs-lookup"><span data-stu-id="23a44-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="23a44-132">På siden **Oppsett av roller**, velg **Ny** og skriv inn følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="23a44-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="23a44-133">**Rolle-ID:** Overordnet prosjektleder</span><span class="sxs-lookup"><span data-stu-id="23a44-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="23a44-134">**Beskrivelse:** Overordnet prosjektleder</span><span class="sxs-lookup"><span data-stu-id="23a44-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="23a44-135">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="23a44-135">Select **Create**.</span></span>
3. <span data-ttu-id="23a44-136">Velg rollen **Senior prosjektleder**, og velg deretter **Konfigurer egenskaper**.</span><span class="sxs-lookup"><span data-stu-id="23a44-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="23a44-137">I feltet **Egenskapstype** velger du **Ferdighet**.</span><span class="sxs-lookup"><span data-stu-id="23a44-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="23a44-138">I feltet **Tilgjengelige egenskaper**, skriv inn ferdigheten det skal søkes etter.</span><span class="sxs-lookup"><span data-stu-id="23a44-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="23a44-139">I feltet **Egenskapstype** velger du **Sertifikat**.</span><span class="sxs-lookup"><span data-stu-id="23a44-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="23a44-140">I feltet **Tilgjengelige egenskaper** angir du sertifikattypen du skal søke etter.</span><span class="sxs-lookup"><span data-stu-id="23a44-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="23a44-141">Tilordne en prosjektressurs til et prosjekt</span><span class="sxs-lookup"><span data-stu-id="23a44-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="23a44-142">På siden **Alle prosjekter**, velg **XYZ Oppgrader fase 2**-prosjektet.</span><span class="sxs-lookup"><span data-stu-id="23a44-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="23a44-143">I kategorien **Prosjektteam og planlegging**, velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="23a44-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="23a44-144">I **Rolle**-feltet velger du **Teammedlem**.</span><span class="sxs-lookup"><span data-stu-id="23a44-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="23a44-145">Velg **Bestill fra kalender**.</span><span class="sxs-lookup"><span data-stu-id="23a44-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="23a44-146">På siden **Ressurstilgjengelighet**, velg **Vis innstillinger**.</span><span class="sxs-lookup"><span data-stu-id="23a44-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="23a44-147">På siden **Juster visningsinnstillinger** angir du følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="23a44-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="23a44-148">**Format for visning av datoområde:** Dag</span><span class="sxs-lookup"><span data-stu-id="23a44-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="23a44-149">**Vis tilgjengelighetsbeskrivelser:** Ja</span><span class="sxs-lookup"><span data-stu-id="23a44-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="23a44-150">**Vis gjenstående kapasitet:** Ja</span><span class="sxs-lookup"><span data-stu-id="23a44-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="23a44-151">Velg en ressurs i listen over ressurser.</span><span class="sxs-lookup"><span data-stu-id="23a44-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="23a44-152">Velg **Forpliktende bestilling** og **Full kapasitet**.</span><span class="sxs-lookup"><span data-stu-id="23a44-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="23a44-153">Tilordne en ressurs til en standardrolle</span><span class="sxs-lookup"><span data-stu-id="23a44-153">Assign a resource to a default role</span></span>

<span data-ttu-id="23a44-154">For å hjelpe prosjektledere eller ressursforvaltere å gå videre med ressursene som kan reserveres for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="23a44-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="23a44-155">Du kan knytte en standardrolle til en eksisterende ressurs eller en nylig anskaffet ressurs.</span><span class="sxs-lookup"><span data-stu-id="23a44-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="23a44-156">Eksempel: Da Daniel ble ansatt, hadde han erfaring og ferdigheter til å fylle rollen som forretningsanalytiker.</span><span class="sxs-lookup"><span data-stu-id="23a44-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="23a44-157">Ressursbehandleren tilordnet denne rollen som Daniels standardrolle.</span><span class="sxs-lookup"><span data-stu-id="23a44-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="23a44-158">Derfor la ressursbehandleren Daniel til i et utvalg av forretningsanalytikere som er tilgjengelige for å arbeide med prosjekter.</span><span class="sxs-lookup"><span data-stu-id="23a44-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="23a44-159">Under ressursreservering kan prosjektledere filtrere rolleressursene som er tilgjengelige for arbeid på prosjekter.</span><span class="sxs-lookup"><span data-stu-id="23a44-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="23a44-160">De kan bruke denne informasjonen som én av betingelsene når de utfører analyse av beslutninger med flere kriterier under ressursoppfyllelse.</span><span class="sxs-lookup"><span data-stu-id="23a44-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="23a44-161">De kan også legge til andre ressursegenskaper i filteret for å søke etter ressurser som har bestemte ferdigheter, utdanning og erfaring for et bestemt prosjekt.</span><span class="sxs-lookup"><span data-stu-id="23a44-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="23a44-162">**Scenario:** Et godkjent prosjekt er startet, og rollen Overordnet prosjektstyrer ble reservert som en planlagt ressurs i løpet av prosjektplanleggingsfasen.</span><span class="sxs-lookup"><span data-stu-id="23a44-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="23a44-163">Ressurslederen har nå anskaffet seg en ressurs for å oppfylle rollen Overordnet prosjektleder.</span><span class="sxs-lookup"><span data-stu-id="23a44-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="23a44-164">På siden **Ressursliste**, velg **Daniel Goldschmidt**.</span><span class="sxs-lookup"><span data-stu-id="23a44-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="23a44-165">På siden **Ressursrolle**, velg **Ny** og skriv inn følgende verdier:</span><span class="sxs-lookup"><span data-stu-id="23a44-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="23a44-166">**Gjelder fra:** Skriv inn gjeldende dato.</span><span class="sxs-lookup"><span data-stu-id="23a44-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="23a44-167">**Utløper:** Skriv inn **Aldri**.</span><span class="sxs-lookup"><span data-stu-id="23a44-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="23a44-168">**Rolle:** Skriv inn **Senior prosjektleder**.</span><span class="sxs-lookup"><span data-stu-id="23a44-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="23a44-169">Velg **Lagre**, og lukk deretter siden.</span><span class="sxs-lookup"><span data-stu-id="23a44-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="23a44-170">I kategorien **Kompetanser** legger du til ferdigheten **ProjectMgmt** og **PMP**-sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="23a44-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>
