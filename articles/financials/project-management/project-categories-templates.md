---
title: Synkronisere prosjektutgiftskategorier mellom Finance and Operations og Project Service Automation
description: Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjektutgiftskategorier mellom Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "347842"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="c1913-103">Synkronisere prosjektutgiftskategorier mellom Finance and Operations og Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c1913-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c1913-104">Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjektutgiftskategorier mellom Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c1913-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="c1913-105">Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i Microsoft Dynamics 365 for Finance and Operations versjon 8.0.</span><span class="sxs-lookup"><span data-stu-id="c1913-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="c1913-106">Integrasjon av faktiske data er tilgjengelig i Microsoft Dynamics 365 for Finance and Operations versjon 8.0.1 eller senere.</span><span class="sxs-lookup"><span data-stu-id="c1913-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="c1913-107">Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 når du har installert KB 4132657 og KB 4132660, vil du kunne bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske data, og du vil kunne konfigurere funksjonslåsing.</span><span class="sxs-lookup"><span data-stu-id="c1913-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="c1913-108">Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="c1913-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="c1913-109">Dataflyt for Project Service Automation og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1913-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="c1913-110">Project Service Automation og Finance and Operations-integrasjonsløsningen bruker funksjonen for dataintegrasjon til å synkronisere data på tvers av Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c1913-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="c1913-111">Integreringsmalene som er tilgjengelige med dataintegreringsfunksjonen, muliggjør dataflyt om prosjektutgiftstransaksjonskategorier mellom Finance and Operations og Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c1913-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="c1913-112">Hvis prosjektutgiftskategoriene styres i Finance and Operations, er integreringsflyten først fra Finance and Operations til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c1913-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="c1913-113">Integrasjons-ID-ene for prosjektutgiftskategorier oppdateres deretter via synkronisering fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c1913-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="c1913-114">Hvis prosjektutgiftskategoriene styres i Project Service Automation, er integreringsflyten først fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c1913-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="c1913-115">Prosjektkategoriene må allerede være konfigurert i Finance and Operations før synkronisering fra Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c1913-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="c1913-116">Synkronier deretter fra Finance and Operations tilbake til Project Service Automation, og deretter fra Project Service Automation til Finance and Operations igjen.</span><span class="sxs-lookup"><span data-stu-id="c1913-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="c1913-117">På denne måten kan du sørge for at kategoriene kobles, og at ingen duplikater opprettes.</span><span class="sxs-lookup"><span data-stu-id="c1913-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="c1913-118">Reiseregningskategoriene for prosjektet styres vanligvis i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c1913-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="c1913-119">Men hvis de ikke styres i Finance and Operations, eller hvis utgiftskategorier allerede er opprettet i Project Service Automation, må du først synkronisere ved å bruke malen for prosjektutgiftstransaksjonskategorier (PSA til Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="c1913-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="c1913-120">Synkroniser deretter ved å bruke malen for prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="c1913-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="c1913-121">Du kan deretter kjøre synkroniseringen fra Project Service Automation til Finance and Operations én gang til.</span><span class="sxs-lookup"><span data-stu-id="c1913-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="c1913-122">Hvis du synkroniserer først fra Project Service Automation, må følgende krav oppfylles i Finance and Operations før synkroniseringen kjøres:</span><span class="sxs-lookup"><span data-stu-id="c1913-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="c1913-123">Den delte kategorien som samsvarer med prosjektkategorien som er definert i Project Service Automation, må finnes, og den må være aktivert for både **Prosjekt** og **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="c1913-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="c1913-124">For hver juridiske enhet i Finance and Operations som det må integreres med, må følgende prosjektkategorier finnes:</span><span class="sxs-lookup"><span data-stu-id="c1913-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="c1913-125">**Prosjektkategori** finnes.</span><span class="sxs-lookup"><span data-stu-id="c1913-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="c1913-126">**Bruk i utgift** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="c1913-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="c1913-127">**Aktiv i journal** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="c1913-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="c1913-128">**Transaksjonstype** er satt til **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="c1913-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="c1913-129">Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c1913-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="c1913-130">[![Dataflyt for Project Service Automation-integrasjon med Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="c1913-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="c1913-131">Synkronisering av prosjektutgiftskategori fra Finance and Operations til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c1913-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="c1913-132">Mal og oppgave</span><span class="sxs-lookup"><span data-stu-id="c1913-132">Template and task</span></span>

<span data-ttu-id="c1913-133">For å få tilgang til malen velg **Prosjekter** i administrasjonssenter for Microsoft PowerApps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.</span><span class="sxs-lookup"><span data-stu-id="c1913-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c1913-134">Følgende mal og underliggende oppgave brukes til å synkronisere prosjektutgiftskategorier fra Finance and Operations til Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="c1913-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="c1913-135">**Navnet på malen i Dataintegrering:** Prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA)</span><span class="sxs-lookup"><span data-stu-id="c1913-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="c1913-136">**Navnet på oppgaven i prosjektet:** Synkroniser kategorier til PSA</span><span class="sxs-lookup"><span data-stu-id="c1913-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="c1913-137">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="c1913-137">Entity set</span></span>

| <span data-ttu-id="c1913-138">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1913-138">Finance and Operations</span></span>            | <span data-ttu-id="c1913-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c1913-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="c1913-140">Integreringsenhet for kategorier</span><span class="sxs-lookup"><span data-stu-id="c1913-140">Integration entity for categories</span></span> | <span data-ttu-id="c1913-141">Transaksjonskategorier</span><span class="sxs-lookup"><span data-stu-id="c1913-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="c1913-142">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="c1913-142">Entity flow</span></span>

<span data-ttu-id="c1913-143">Prosjektutgiftskategorier administreres i Finance and Operations, og de synkroniseres til Project Service Automation som transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="c1913-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="c1913-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="c1913-144">Power Query</span></span>

<span data-ttu-id="c1913-145">Når du synkroniserer til Project Service Automation, må du bruke Microsoft Power Query for Excel til å angi faktureringstypen på transaksjonskategorien.</span><span class="sxs-lookup"><span data-stu-id="c1913-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="c1913-146">Malen for prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA) har en standardkolonne og tilordning.</span><span class="sxs-lookup"><span data-stu-id="c1913-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="c1913-147">Hvis du oppretter din egen mal, må du legge til en betinget kolonne i Power Query.</span><span class="sxs-lookup"><span data-stu-id="c1913-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="c1913-148">Følg disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="c1913-148">Follow these steps.</span></span>

1. <span data-ttu-id="c1913-149">Klikk på pilen for å åpne tilordningen av prosjektutgiftskategorioppgaven i malen for prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="c1913-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="c1913-150">Klikk på koblingen **Avansert spørring og filtrering** for å åpne Power Query.</span><span class="sxs-lookup"><span data-stu-id="c1913-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="c1913-151">Velg **Legg til betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="c1913-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="c1913-152">Angi et navn for den nye kolonnen, for eksempel **Faktureringstype**.</span><span class="sxs-lookup"><span data-stu-id="c1913-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="c1913-153">Angi følgende betingelse: **hvis CATEGORYID ikke er lik null, så 19235001, ellers null**.</span><span class="sxs-lookup"><span data-stu-id="c1913-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="c1913-154">Klikk på **OK** i kolonnen.</span><span class="sxs-lookup"><span data-stu-id="c1913-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="c1913-155">Husk å tilordne den nye kolonnen på siden for tilordning.</span><span class="sxs-lookup"><span data-stu-id="c1913-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="c1913-156">Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="c1913-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="c1913-157">Tilordningen viser feltinformasjonen som vil bli synkronisert fra Finance and Operations til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c1913-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="c1913-158">[![Tilordning av mal](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c1913-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="c1913-159">Synkronisering av prosjektutgiftskategori fra Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1913-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="c1913-160">Mal og oppgave</span><span class="sxs-lookup"><span data-stu-id="c1913-160">Template and task</span></span>

<span data-ttu-id="c1913-161">Følgende mal og underliggende oppgave brukes til å synkronisere prosjektutgiftskategorier fra Project Service Automation til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="c1913-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="c1913-162">**Navnet på malen i Dataintegrering:** Prosjektutgiftstransaksjonskategorier (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="c1913-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c1913-163">**Navnet på oppgaven i prosjektet:** Synkroniser kategorier til Fin Ops</span><span class="sxs-lookup"><span data-stu-id="c1913-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="c1913-164">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="c1913-164">Entity set</span></span>

| <span data-ttu-id="c1913-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c1913-165">Project Service Automation</span></span> | <span data-ttu-id="c1913-166">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c1913-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="c1913-167">Transaksjonskategorier</span><span class="sxs-lookup"><span data-stu-id="c1913-167">Transaction categories</span></span>     | <span data-ttu-id="c1913-168">Integreringsenhet for kategorier</span><span class="sxs-lookup"><span data-stu-id="c1913-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="c1913-169">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="c1913-169">Entity flow</span></span>

<span data-ttu-id="c1913-170">Prosjektutgiftskategorier administreres i Finance and Operations, og de synkroniseres til Project Service Automation som transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="c1913-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="c1913-171">Synkronisering tilbake til Finance and Operations oppdaterer prosjektkategorien i Finance and Operations med integrasjons-ID-en fra Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="c1913-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c1913-172">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="c1913-172">Template mapping in Data integration</span></span>

<span data-ttu-id="c1913-173">Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="c1913-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="c1913-174">Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c1913-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="c1913-175">[![Tilordning av mal](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c1913-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
