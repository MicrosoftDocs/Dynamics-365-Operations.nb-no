---
title: Synkronisere prosjektutgiftskategorier mellom Finance and Operations og Project Service Automation
description: Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjektutgiftskategorier mellom Microsoft Dynamics 365 Finance og Dynamics 365 Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 7b0b3721c3b0755218c834d2bf77ec976be3bdcc
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770318"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="11760-103">Synkronisere prosjektutgiftskategorier mellom Finance and Operations og Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="11760-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="11760-104">Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjektutgiftskategorier mellom Dynamics 365 Finance og Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="11760-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="11760-105">Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i versjon 8.0.</span><span class="sxs-lookup"><span data-stu-id="11760-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="11760-106">Integrasjon av faktiske data er tilgjengelig i versjon 8.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="11760-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="11760-107">Hvis du bruker Enterprise Edition 7.3.0 når du har installert KB 4132657 og KB 4132660, kan du bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske data, og du kan konfigurere funksjonslåsing.</span><span class="sxs-lookup"><span data-stu-id="11760-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="11760-108">Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="11760-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="11760-109">Dataflyt for Project Service Automation og Finance</span><span class="sxs-lookup"><span data-stu-id="11760-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="11760-110">Project Service Automation og Finance-integrasjonsløsningen bruker funksjonen for dataintegrasjon til å synkronisere data på tvers av Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="11760-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="11760-111">Integreringsmalene som er tilgjengelige med dataintegreringsfunksjonen, muliggjør dataflyt om prosjektutgiftstransaksjonskategorier mellom Finance og Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="11760-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="11760-112">Hvis prosjektutgiftskategoriene styres i Finance, er integreringsflyten først fra Finance til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="11760-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="11760-113">Integrasjons-ID-ene for prosjektutgiftskategorier oppdateres deretter via synkronisering fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="11760-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="11760-114">Hvis prosjektutgiftskategoriene styres i Project Service Automation, er integreringsflyten først fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="11760-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="11760-115">Prosjektkategoriene må allerede være konfigurert i Finance før synkronisering fra Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="11760-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="11760-116">Synkronier deretter fra Finance tilbake til Project Service Automation, og deretter fra Project Service Automation til Finance igjen.</span><span class="sxs-lookup"><span data-stu-id="11760-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="11760-117">På denne måten kan du sørge for at kategoriene kobles, og at ingen duplikater opprettes.</span><span class="sxs-lookup"><span data-stu-id="11760-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="11760-118">Reiseregningskategoriene for prosjektet styres vanligvis i Finance.</span><span class="sxs-lookup"><span data-stu-id="11760-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="11760-119">Men hvis de ikke styres eller utgiftskategorier allerede er opprettet i Project Service Automation, må du først synkronisere ved å bruke malen for prosjektutgiftstransaksjonskategorier (PSA til Fin and Ops).</span><span class="sxs-lookup"><span data-stu-id="11760-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="11760-120">Synkroniser deretter ved å bruke malen for prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="11760-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="11760-121">Du kan deretter kjøre synkroniseringen fra Project Service Automation til Finance én gang til.</span><span class="sxs-lookup"><span data-stu-id="11760-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="11760-122">Hvis du synkroniserer først fra Project Service Automation, må følgende krav oppfylles i Finance før synkroniseringen kjøres:</span><span class="sxs-lookup"><span data-stu-id="11760-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="11760-123">Den delte kategorien som samsvarer med prosjektkategorien som er definert i Project Service Automation, må finnes, og den må være aktivert for både **Prosjekt** og **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="11760-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="11760-124">For hver juridiske enhet i Finance som det må integreres med, må følgende prosjektkategorier finnes:</span><span class="sxs-lookup"><span data-stu-id="11760-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="11760-125">**Prosjektkategori** finnes.</span><span class="sxs-lookup"><span data-stu-id="11760-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="11760-126">**Bruk i utgift** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="11760-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="11760-127">**Aktiv i journal** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="11760-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="11760-128">**Transaksjonstype** er satt til **Utgift**.</span><span class="sxs-lookup"><span data-stu-id="11760-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="11760-129">Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="11760-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="11760-130">[![Dataflyt for Project Service Automation-integrasjon med Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="11760-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="11760-131">Synkronisering av prosjektutgiftskategori fra Finance til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="11760-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="11760-132">Mal og oppgave</span><span class="sxs-lookup"><span data-stu-id="11760-132">Template and task</span></span>

<span data-ttu-id="11760-133">For å få tilgang til malen velg **Prosjekter** i administrasjonssenter for Microsoft Power Apps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.</span><span class="sxs-lookup"><span data-stu-id="11760-133">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="11760-134">Følgende mal og underliggende oppgave brukes til å synkronisere prosjektutgiftskategorier fra Finance til Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="11760-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="11760-135">**Navnet på malen i Dataintegrering:** Prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA)</span><span class="sxs-lookup"><span data-stu-id="11760-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="11760-136">**Navnet på oppgaven i prosjektet:** Synkroniser kategorier til PSA</span><span class="sxs-lookup"><span data-stu-id="11760-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="11760-137">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="11760-137">Entity set</span></span>

| <span data-ttu-id="11760-138">Finans</span><span class="sxs-lookup"><span data-stu-id="11760-138">Finance</span></span>                           | <span data-ttu-id="11760-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="11760-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="11760-140">Integreringsenhet for kategorier</span><span class="sxs-lookup"><span data-stu-id="11760-140">Integration entity for categories</span></span> | <span data-ttu-id="11760-141">Transaksjonskategorier</span><span class="sxs-lookup"><span data-stu-id="11760-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="11760-142">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="11760-142">Entity flow</span></span>

<span data-ttu-id="11760-143">Prosjektutgiftskategorier administreres i Finance, og de synkroniseres til Project Service Automation som transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="11760-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="11760-144">Power Query</span><span class="sxs-lookup"><span data-stu-id="11760-144">Power Query</span></span>

<span data-ttu-id="11760-145">Når du synkroniserer til Project Service Automation, må du bruke Microsoft Power Query for Excel til å angi faktureringstypen på transaksjonskategorien.</span><span class="sxs-lookup"><span data-stu-id="11760-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="11760-146">Malen for prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA) har en standardkolonne og tilordning.</span><span class="sxs-lookup"><span data-stu-id="11760-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="11760-147">Hvis du oppretter din egen mal, må du legge til en betinget kolonne i Power Query.</span><span class="sxs-lookup"><span data-stu-id="11760-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="11760-148">Følg disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="11760-148">Follow these steps.</span></span>

1. <span data-ttu-id="11760-149">Klikk på pilen for å åpne tilordningen av prosjektutgiftskategorioppgaven i malen for prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="11760-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="11760-150">Klikk på koblingen **Avansert spørring og filtrering** for å åpne Power Query.</span><span class="sxs-lookup"><span data-stu-id="11760-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="11760-151">Velg **Legg til betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="11760-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="11760-152">Angi et navn for den nye kolonnen, for eksempel **Faktureringstype**.</span><span class="sxs-lookup"><span data-stu-id="11760-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="11760-153">Angi følgende betingelse: **hvis CATEGORYID ikke er lik null, så 19235001, ellers null**.</span><span class="sxs-lookup"><span data-stu-id="11760-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="11760-154">Klikk på **OK** i kolonnen.</span><span class="sxs-lookup"><span data-stu-id="11760-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="11760-155">Husk å tilordne den nye kolonnen på siden for tilordning.</span><span class="sxs-lookup"><span data-stu-id="11760-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="11760-156">Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="11760-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="11760-157">Tilordningen viser feltinformasjonen som vil bli synkronisert fra Finance til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="11760-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="11760-158">[![Tilordning av mal](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="11760-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="11760-159">Synkronisering av prosjektutgiftskategori fra Project Service Automation til Finance</span><span class="sxs-lookup"><span data-stu-id="11760-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="11760-160">Mal og oppgave</span><span class="sxs-lookup"><span data-stu-id="11760-160">Template and task</span></span>

<span data-ttu-id="11760-161">Følgende mal og underliggende oppgave brukes til å synkronisere prosjektutgiftskategorier fra Project Service Automation til Finance:</span><span class="sxs-lookup"><span data-stu-id="11760-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="11760-162">**Navnet på malen i Dataintegrering:** Prosjektutgiftstransaksjonskategorier (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="11760-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="11760-163">**Navnet på oppgaven i prosjektet:** Synkroniser kategorier til Fin Ops</span><span class="sxs-lookup"><span data-stu-id="11760-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="11760-164">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="11760-164">Entity set</span></span>

| <span data-ttu-id="11760-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="11760-165">Project Service Automation</span></span> | <span data-ttu-id="11760-166">Finans</span><span class="sxs-lookup"><span data-stu-id="11760-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="11760-167">Transaksjonskategorier</span><span class="sxs-lookup"><span data-stu-id="11760-167">Transaction categories</span></span>     | <span data-ttu-id="11760-168">Integreringsenhet for kategorier</span><span class="sxs-lookup"><span data-stu-id="11760-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="11760-169">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="11760-169">Entity flow</span></span>

<span data-ttu-id="11760-170">Prosjektutgiftskategorier administreres i Finance, og de synkroniseres til Project Service Automation som transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="11760-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="11760-171">Synkronisering tilbake til Finance oppdaterer prosjektkategorien i Finance med integrasjons-ID-en fra Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="11760-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="11760-172">Maltilordning i Dataintegrering</span><span class="sxs-lookup"><span data-stu-id="11760-172">Template mapping in Data integration</span></span>

<span data-ttu-id="11760-173">Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="11760-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="11760-174">Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="11760-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="11760-175">[![Tilordning av mal](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="11760-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
