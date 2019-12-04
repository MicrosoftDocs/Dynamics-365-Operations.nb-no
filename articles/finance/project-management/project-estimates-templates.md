---
title: Synkronisere prosjektestimater direkte fra Project Service Automation til Finance and Operations
description: Dette emnet beskriver maler og de underliggende oppgavene som brukes til å synkronisere prosjekttimeestimater og prosjektutgiftsestimater direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770295"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="07388-103">Synkronisere prosjektestimater direkte fra Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="07388-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="07388-104">Dette emnet beskriver maler og de underliggende oppgavene som brukes til å synkronisere prosjekttimeestimater og prosjektutgiftsestimater direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="07388-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="07388-105">Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i versjon 8.0.</span><span class="sxs-lookup"><span data-stu-id="07388-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="07388-106">Integrasjon av faktiske data er tilgjengelig i versjon 8.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="07388-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="07388-107">Dataflyt for Project Service Automation til Finance</span><span class="sxs-lookup"><span data-stu-id="07388-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="07388-108">Project Service Automation til Finance-integrasjonsløsningen bruker funksjonen for dataintegrasjon til å synkronisere data på tvers av Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="07388-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="07388-109">Integreringsmalene som er tilgjengelige med dataintegreringsfunksjonen, muliggjør dataflyt om prosjekttimeestimater og prosjektutgiftsestimater fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="07388-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="07388-110">Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="07388-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="07388-111">[![Dataflyt for Project Service Automation-integrasjon med Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="07388-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="07388-112">Prosjekttimeestimater</span><span class="sxs-lookup"><span data-stu-id="07388-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="07388-113">Mal og oppgaver</span><span class="sxs-lookup"><span data-stu-id="07388-113">Template and tasks</span></span>

<span data-ttu-id="07388-114">For å få tilgang til tilgjengelige maler velg **Prosjekter** i administrasjonssenter for Microsoft Power Apps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.</span><span class="sxs-lookup"><span data-stu-id="07388-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="07388-115">Følgende mal og underliggende oppgaver brukes til å synkronisere prosjekttimeestimater fra Project Service Automation til Finance:</span><span class="sxs-lookup"><span data-stu-id="07388-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="07388-116">**Navnet på malen i Dataintegrering:** Prosjekttimeestimater (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="07388-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="07388-117">**Navn på oppgavene i prosjektet:**</span><span class="sxs-lookup"><span data-stu-id="07388-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="07388-118">Transaksjonsrelasjoner</span><span class="sxs-lookup"><span data-stu-id="07388-118">Transaction relationships</span></span>
    - <span data-ttu-id="07388-119">Utgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="07388-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="07388-120">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="07388-120">Entity set</span></span>

| <span data-ttu-id="07388-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="07388-121">Project Service Automation</span></span> | <span data-ttu-id="07388-122">Finans</span><span class="sxs-lookup"><span data-stu-id="07388-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="07388-123">Prosjektoppgaver</span><span class="sxs-lookup"><span data-stu-id="07388-123">Project tasks</span></span>              | <span data-ttu-id="07388-124">Integreringsenhet for prosjekttimeestimater</span><span class="sxs-lookup"><span data-stu-id="07388-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="07388-125">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="07388-125">Entity flow</span></span>

<span data-ttu-id="07388-126">Prosjekttimeestimater administreres i Project Service Automation, og de synkroniseres til Finance som prosjekttimeprognoser.</span><span class="sxs-lookup"><span data-stu-id="07388-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="07388-127">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="07388-127">Prerequisites</span></span>

<span data-ttu-id="07388-128">Før synkronisering av prosjekttimeestimater kan skje, må du synkronisere prosjekter, prosjektoppgaver og transaksjonskategorier for prosjektutgifter.</span><span class="sxs-lookup"><span data-stu-id="07388-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="07388-129">Power Query</span><span class="sxs-lookup"><span data-stu-id="07388-129">Power Query</span></span>

<span data-ttu-id="07388-130">I prosjekttimeestimatmalen kan du bruke Microsoft Power Query for Excel til å fullføre disse oppgavene:</span><span class="sxs-lookup"><span data-stu-id="07388-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="07388-131">Angi standard prognosemodell-ID som skal brukes når integreringen oppretter nye timeprognoser.</span><span class="sxs-lookup"><span data-stu-id="07388-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="07388-132">Filtrer ut alle ressursspesifikke poster i oppgaven som ikke blir integrerte i timeprognoser.</span><span class="sxs-lookup"><span data-stu-id="07388-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="07388-133">Filtrere ut eventuelle tomme transaksjonskategorirader.</span><span class="sxs-lookup"><span data-stu-id="07388-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="07388-134">Hvis du ikke gjør dette, kan det resultere i feil timeprognoser.</span><span class="sxs-lookup"><span data-stu-id="07388-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="07388-135">Angi standard prognosemodell-ID</span><span class="sxs-lookup"><span data-stu-id="07388-135">Set the default forecast model ID</span></span>

<span data-ttu-id="07388-136">For å oppdatere standard prognosemodell-ID i malen, klikker du på **Tilordne**-pilen for å åpne tilordningen.</span><span class="sxs-lookup"><span data-stu-id="07388-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="07388-137">Velg deretter koblingen **Avansert spørring og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="07388-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="07388-138">Hvis du bruker standard prosjekttimeestimater (PSA til Fin and Ops), velger du **Innsatt betingelse** i liste over **Brukte trinn**.</span><span class="sxs-lookup"><span data-stu-id="07388-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="07388-139">I **Funksjon**-oppføringen erstatter du **O\_forecast** med navnet på prognosemodell-ID-en som skal brukes med integreringen.</span><span class="sxs-lookup"><span data-stu-id="07388-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="07388-140">Standardmalen har en prognosemodell-ID fra demodataene.</span><span class="sxs-lookup"><span data-stu-id="07388-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="07388-141">Hvis du oppretter en ny mal, må du legge til denne kolonnen.</span><span class="sxs-lookup"><span data-stu-id="07388-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="07388-142">I Power Query velger du **Legg til betinget kolonne** og angir et navn på den nye kolonnen, for eksempel **Model-ID**.</span><span class="sxs-lookup"><span data-stu-id="07388-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="07388-143">Angi betingelsen for kolonnen, der hvis prosjektoppgave ikke er null, så \<skriv inn ID for prognosemodell\> >, hvis ikke null.</span><span class="sxs-lookup"><span data-stu-id="07388-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="07388-144">Filtrere ut ressursspesifikke poster</span><span class="sxs-lookup"><span data-stu-id="07388-144">Filter out resource-specific records</span></span>

<span data-ttu-id="07388-145">Malen for prosjekttimeestimater (PSA til Fin and Ops) har et standardfilter som fjerner ressursspesifikke poster.</span><span class="sxs-lookup"><span data-stu-id="07388-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="07388-146">Hvis du oppretter din egen mal, må du legge til dette filteret.</span><span class="sxs-lookup"><span data-stu-id="07388-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="07388-147">Velg koblingen **Avanserte spørring og filtrering** for å filtrere på kolonnen **msdyn\_islinetask**, slik at bare **Usann**-poster inkluderes.</span><span class="sxs-lookup"><span data-stu-id="07388-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="07388-148">Filtrere ut tomme transaksjonskategorirader</span><span class="sxs-lookup"><span data-stu-id="07388-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="07388-149">Du må legge til et filter hvis du vil fjerne alle rader med tomme transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="07388-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="07388-150">Denne oppgaven er nødvendig uansett om du bruker standardmalen eller oppretter din egen mal.</span><span class="sxs-lookup"><span data-stu-id="07388-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="07388-151">Dette filteret fjerner sammendragsrader som kommer fra Project Service Automation som kan føre til at timeprognoser i Finance blir feil.</span><span class="sxs-lookup"><span data-stu-id="07388-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="07388-152">Velg koblingen **Avansert spørring og filtrering** for å filtrere ut null-poster i kolonnen **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="07388-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="07388-153">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="07388-153">Template mapping in Data integration</span></span>

<span data-ttu-id="07388-154">Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="07388-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="07388-155">Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="07388-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="07388-156">[![Tilordning av mal](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="07388-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="07388-157">Prosjektutgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="07388-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="07388-158">Mal og oppgaver</span><span class="sxs-lookup"><span data-stu-id="07388-158">Template and tasks</span></span>

<span data-ttu-id="07388-159">Følgende mal og underliggende oppgaver brukes til å synkronisere prosjektutgiftsestimater fra Project Service Automation til Finance:</span><span class="sxs-lookup"><span data-stu-id="07388-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="07388-160">**Navnet på malen i Dataintegrering:** Prosjektutgiftsestimater (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="07388-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="07388-161">**Navn på oppgavene i prosjektet:**</span><span class="sxs-lookup"><span data-stu-id="07388-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="07388-162">Transaksjonsrelasjoner</span><span class="sxs-lookup"><span data-stu-id="07388-162">Transaction relationships</span></span> 
    - <span data-ttu-id="07388-163">Utgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="07388-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="07388-164">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="07388-164">Entity set</span></span>

| <span data-ttu-id="07388-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="07388-165">Project Service Automation</span></span> | <span data-ttu-id="07388-166">Finans</span><span class="sxs-lookup"><span data-stu-id="07388-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="07388-167">Transaksjonstilkoblinger</span><span class="sxs-lookup"><span data-stu-id="07388-167">Transaction Connections</span></span>    | <span data-ttu-id="07388-168">Integreringsenhet for relasjoner for prosjekttransaksjon</span><span class="sxs-lookup"><span data-stu-id="07388-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="07388-169">Estimatlinjer</span><span class="sxs-lookup"><span data-stu-id="07388-169">Estimate Lines</span></span>             | <span data-ttu-id="07388-170">Integreringsenhet for prosjektutgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="07388-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="07388-171">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="07388-171">Entity flow</span></span>

<span data-ttu-id="07388-172">Prosjektutgiftsestimater administreres i Project Service Automation, og de synkroniseres til Finance som prosjektutgiftsprognoser.</span><span class="sxs-lookup"><span data-stu-id="07388-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="07388-173">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="07388-173">Prerequisites</span></span>

<span data-ttu-id="07388-174">Før synkronisering av prosjektutgiftsestimater kan skje, må du synkronisere prosjekter, prosjektoppgaver og transaksjonskategorier for prosjektutgifter.</span><span class="sxs-lookup"><span data-stu-id="07388-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="07388-175">Power Query</span><span class="sxs-lookup"><span data-stu-id="07388-175">Power Query</span></span>

<span data-ttu-id="07388-176">I prosjektutgiftsestimatmalen må du bruke Power Query til å fullføre følgende oppgaver:</span><span class="sxs-lookup"><span data-stu-id="07388-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="07388-177">Filtrere for å inkludere bare linjepostene for utgiftsestimat.</span><span class="sxs-lookup"><span data-stu-id="07388-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="07388-178">Angi standard prognosemodell-ID som skal brukes når integreringen oppretter nye timeprognoser.</span><span class="sxs-lookup"><span data-stu-id="07388-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="07388-179">Transformere faktureringstypene.</span><span class="sxs-lookup"><span data-stu-id="07388-179">Transform the billing types.</span></span>
- <span data-ttu-id="07388-180">Transformere transaksjonstypene.</span><span class="sxs-lookup"><span data-stu-id="07388-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="07388-181">Filtrere for å inkludere bare linjene for utgiftsestimat</span><span class="sxs-lookup"><span data-stu-id="07388-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="07388-182">Malen for prosjektutgiftsestimater (PSA til Fin and Ops) har et standardfilter som bare omfatter utgiftslinjer i integreringen.</span><span class="sxs-lookup"><span data-stu-id="07388-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="07388-183">Hvis du oppretter din egen mal, må du legge til dette filteret.</span><span class="sxs-lookup"><span data-stu-id="07388-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="07388-184">Velg **Transaksjonsrelasjoner**, og klikk deretter **Tilordne**-pilen for å åpne tilordningen.</span><span class="sxs-lookup"><span data-stu-id="07388-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="07388-185">Velg koblingen **Avansert spørring og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="07388-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="07388-186">Filtrer kolonnen **msdyn\_transactiontype1** for å inkludere bare **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="07388-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="07388-187">Angi standard prognosemodell-ID</span><span class="sxs-lookup"><span data-stu-id="07388-187">Set the default forecast model ID</span></span>

<span data-ttu-id="07388-188">For å oppdatere standard prognosemodell-ID i malen, velger du oppgaven **Utgiftsestimater**, og deretter klikker du på **Tilordne**-pilen for å åpne tilordningen.</span><span class="sxs-lookup"><span data-stu-id="07388-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="07388-189">Velg koblingen **Avansert spørring og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="07388-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="07388-190">Hvis du bruker standardmalen for prosjektutgiftsestimater (PSA til Fin and Ops), velger du den første **Innsatt betingelse** i delen **Brukte trinn** i Power Query.</span><span class="sxs-lookup"><span data-stu-id="07388-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="07388-191">I **Funksjon**-oppføringen erstatter du **O\_forecast** med navnet på prognosemodell-ID-en som skal brukes med integreringen.</span><span class="sxs-lookup"><span data-stu-id="07388-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="07388-192">Standardmalen har en prognosemodell-ID fra demodataene.</span><span class="sxs-lookup"><span data-stu-id="07388-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="07388-193">Hvis du oppretter en ny mal, må du legge til denne kolonnen.</span><span class="sxs-lookup"><span data-stu-id="07388-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="07388-194">I Power Query velger du **Legg til betinget kolonne** og angir et navn på den nye kolonnen, for eksempel **Model-ID**.</span><span class="sxs-lookup"><span data-stu-id="07388-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="07388-195">Angi betingelsen for kolonnen, der hvis estimatlinje-ID ikke er null, så \<skriv inn prognosemodell-ID\>, hvis ikke null.</span><span class="sxs-lookup"><span data-stu-id="07388-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="07388-196">Transformere faktureringstypene</span><span class="sxs-lookup"><span data-stu-id="07388-196">Transform the billing types</span></span>

<span data-ttu-id="07388-197">Malen for prosjektutgiftsestimater (PSA til Fin and Ops) inkluderer en betinget kolonne som brukes til å transformere faktureringstypene som ble mottatt fra Project Service Automation under integreringen.</span><span class="sxs-lookup"><span data-stu-id="07388-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="07388-198">Hvis du oppretter din egen mal, må du legge til denne betingede kolonnen.</span><span class="sxs-lookup"><span data-stu-id="07388-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="07388-199">Velg koblingen **Avansert spørring og filtrering**, og velg deretter **Legg til betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="07388-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="07388-200">Angi et navn for den nye kolonnen, for eksempel **Faktureringstype**.</span><span class="sxs-lookup"><span data-stu-id="07388-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="07388-201">Angi deretter følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="07388-201">Then enter the following condition:</span></span>

<span data-ttu-id="07388-202">Hvis **msdyn\_billingtype** = 192350000, så **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="07388-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="07388-203">ellers hvis **msdyn\_billingtype** = 192350001, så **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="07388-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="07388-204">ellers hvis **msdyn\_billingtype** = 192350002, så **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="07388-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="07388-205">ellers **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="07388-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="07388-206">Transformere transaksjonstypene</span><span class="sxs-lookup"><span data-stu-id="07388-206">Transform the transaction types</span></span>

<span data-ttu-id="07388-207">Malen for prosjektutgiftsestimater (PSA til Fin and Ops) inkluderer en betinget kolonne som brukes til å transformere transaksjonstypene som ble mottatt fra Project Service Automation under integreringen.</span><span class="sxs-lookup"><span data-stu-id="07388-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="07388-208">Hvis du oppretter din egen mal, må du legge til denne betingede kolonnen.</span><span class="sxs-lookup"><span data-stu-id="07388-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="07388-209">Velg koblingen **Avansert spørring og filtrering**, og velg deretter **Legg til betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="07388-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="07388-210">Angi et navn for den nye kolonnen, for eksempel **Transaksjonstype**.</span><span class="sxs-lookup"><span data-stu-id="07388-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="07388-211">Angi deretter følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="07388-211">Then enter the following condition:</span></span>

<span data-ttu-id="07388-212">Hvis **msdyn\_transactiontypecode** = 192350000, så **Cost**</span><span class="sxs-lookup"><span data-stu-id="07388-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="07388-213">ellers hvis **msdyn\_transactiontypecode** = 192350005, så **Sales**</span><span class="sxs-lookup"><span data-stu-id="07388-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="07388-214">ellers **null**</span><span class="sxs-lookup"><span data-stu-id="07388-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="07388-215">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="07388-215">Template mapping in Data integration</span></span>

<span data-ttu-id="07388-216">Illustrasjonen nedenfor viser eksempler på maloppgavetilordningene i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="07388-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="07388-217">Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="07388-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="07388-218">[![Tilordning av mal](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="07388-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="07388-219">[![Tilordning av mal](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="07388-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
