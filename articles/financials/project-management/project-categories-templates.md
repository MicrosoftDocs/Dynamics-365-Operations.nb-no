---
title: Synkronisere utgiftskategorier for prosjekt fra Project Service Automation
description: "Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjektutgiftskategorier mellom Microsoft Dynamics 365 for Finance and Operations og Dynamics 365 for Project Service Automation."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: nb-no
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="cceb3-103">Synkronisere prosjektutgiftskategorier mellom Finance and Operations og Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cceb3-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="cceb3-104">Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere prosjektutgiftskategorier mellom Microsoft Dynamics 365 for Finance and Operations og Dynamics 365 for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="cceb3-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="cceb3-105">Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i Dynamics 365 for Finance and Operations versjon 8.0.</span><span class="sxs-lookup"><span data-stu-id="cceb3-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="cceb3-106">Dataflyt for Project Service Automation og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cceb3-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="cceb3-107">Project Service Automation og Finance and Operations-integrasjonsløsningen bruker funksjonen for dataintegrasjon til å synkronisere data på tvers av Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cceb3-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="cceb3-108">Integreringsmalene som er tilgjengelige med dataintegreringsfunksjonen, muliggjør dataflyt om prosjektutgiftstransaksjonskategorier mellom Finance and Operations og Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="cceb3-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="cceb3-109">Hvis prosjektutgiftskategorier styres i Finance and Operations, er integreringsflyten først fra Finance and Operations til Project Service Automation og deretter oppdatering av integrerings-IDene for prosjektutgiftskategorier ved å synkronisere fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cceb3-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="cceb3-110">Hvis prosjektutgiftskategoriene styres i Project Service Automation, er integreringsflyten først fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cceb3-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="cceb3-111">Prosjektkategoriene må allerede være konfigurert i Finance and Operations før synkronisering fra Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="cceb3-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="cceb3-112">Synkronier deretter fra Finance and Operations tilbake til Project Service Automation og deretter fra Project Service Automation til Finance and Operations igjen.</span><span class="sxs-lookup"><span data-stu-id="cceb3-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="cceb3-113">Dette sikrer at kategoriene er koblet og duplikater ikke opprettes.</span><span class="sxs-lookup"><span data-stu-id="cceb3-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="cceb3-114">Reiseregningskategoriene for prosjektet vil vanligvis styres i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cceb3-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="cceb3-115">Hvis dette ikke er din situasjon, eller du allerede har opprettet i utgiftskategorier i Project Service Automation, må du først synkronisere med prosjektutgiftstransaksjonskategoriene (PSA til Fin and Ops) og deretter synkronisere med prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="cceb3-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="cceb3-116">Du kan deretter kjøre synkroniseringen fra PSA til Fin and Ops én gang til.</span><span class="sxs-lookup"><span data-stu-id="cceb3-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="cceb3-117">Hvis det først synkroniseres fra Project Service Automation, må prosjektkategoriene allerede være definert i Finance and Operations, og prosjektkategorier som må synkroniseres med Project Service Automation-transaksjonskategorier må være angitt som **Aktiv i journaler**.</span><span class="sxs-lookup"><span data-stu-id="cceb3-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="cceb3-118">Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cceb3-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="cceb3-119">[![Dataflyt for Project Service Automation-integrasjon med Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="cceb3-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="cceb3-120">Maler og oppgaver</span><span class="sxs-lookup"><span data-stu-id="cceb3-120">Templates and tasks</span></span>

<span data-ttu-id="cceb3-121">For å få tilgang til tilgjengelige maler velg **Prosjekter** i administrasjonssenter for Microsoft PowerApps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.</span><span class="sxs-lookup"><span data-stu-id="cceb3-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="cceb3-122">Følgende mal og underliggende oppgave brukes til å synkronisere prosjektutgiftskategorier fra Finance and Operations til Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="cceb3-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="cceb3-123">**Navnet på malen i Dataintegrering:** Prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA)</span><span class="sxs-lookup"><span data-stu-id="cceb3-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="cceb3-124">**Navnet på oppgaven i prosjektet:** Synkroniser kategorier til PSA</span><span class="sxs-lookup"><span data-stu-id="cceb3-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="cceb3-125">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="cceb3-125">Entity set</span></span>

| <span data-ttu-id="cceb3-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cceb3-126">Finance and Operations</span></span>               | <span data-ttu-id="cceb3-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cceb3-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="cceb3-128">Integreringsenhet for kategorier</span><span class="sxs-lookup"><span data-stu-id="cceb3-128">Integration entity for categories</span></span>    | <span data-ttu-id="cceb3-129">Transaksjonskategorier</span><span class="sxs-lookup"><span data-stu-id="cceb3-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="cceb3-130">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="cceb3-130">Entity flow</span></span>

<span data-ttu-id="cceb3-131">Prosjektutgiftskategorier administreres i Finance and Operations, og de synkroniseres til Project Service Automation som transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="cceb3-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="cceb3-132">Power Query</span><span class="sxs-lookup"><span data-stu-id="cceb3-132">Power Query</span></span>

<span data-ttu-id="cceb3-133">Du må bruke Microsoft Power Query til å angi faktureringstypen på transaksjonskategorien når du synkroniserer til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="cceb3-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="cceb3-134">Malen for prosjektutgiftstransaksjonskategorier (Fin and Ops til PSA) har en standardkolonne og tilordning som allerede finnes.</span><span class="sxs-lookup"><span data-stu-id="cceb3-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="cceb3-135">Hvis du oppretter din egen mal, må du legge til en betinget kolonne i Power Query.</span><span class="sxs-lookup"><span data-stu-id="cceb3-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="cceb3-136">Åpne Avansert syntaks for filtrering og spørring-skjemaet i tilordningen av prosjektutgiftskategorioppgaven.</span><span class="sxs-lookup"><span data-stu-id="cceb3-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="cceb3-137">Velg **Legg til betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="cceb3-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="cceb3-138">Gi den nye kolonnen et navn, for eksempel Faktureringstype.</span><span class="sxs-lookup"><span data-stu-id="cceb3-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="cceb3-139">Angi følgende betingelse: Hvis **CATEGORYID ikke er lik null, så 19235001, ellers null**.</span><span class="sxs-lookup"><span data-stu-id="cceb3-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="cceb3-140">Klikk på **OK** i kolonnen.</span><span class="sxs-lookup"><span data-stu-id="cceb3-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="cceb3-141">Husk å tilordne den nye kolonnen på siden for tilordning.</span><span class="sxs-lookup"><span data-stu-id="cceb3-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="cceb3-142">Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="cceb3-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="cceb3-143">Tilordningen viser feltinformasjonen som vil bli synkronisert fra Finance and Operations til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="cceb3-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="cceb3-144">[![Tilordning av mal](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cceb3-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="cceb3-145">Følgende mal og underliggende oppgave brukes til å synkronisere prosjektutgiftskategorier fra Project Service Automation til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="cceb3-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="cceb3-146">-**Navnet på malen i Dataintegrasjon:** Prosjektutgiftstransaksjonskategorier (PSA til Fin and Ops) -**Navnet på oppgaven i prosjektet:** Synkroniser kategorier til Fin Ops</span><span class="sxs-lookup"><span data-stu-id="cceb3-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="cceb3-147">Enhetssett</span><span class="sxs-lookup"><span data-stu-id="cceb3-147">Entity set</span></span>

| <span data-ttu-id="cceb3-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="cceb3-148">Project Service Automation</span></span>      | <span data-ttu-id="cceb3-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="cceb3-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="cceb3-150">Transaksjonskategorier</span><span class="sxs-lookup"><span data-stu-id="cceb3-150">Transaction categories</span></span>          | <span data-ttu-id="cceb3-151">Integreringsenhet for kategorier</span><span class="sxs-lookup"><span data-stu-id="cceb3-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="cceb3-152">Enhetsflyt</span><span class="sxs-lookup"><span data-stu-id="cceb3-152">Entity flow</span></span>

<span data-ttu-id="cceb3-153">Prosjektutgiftskategorier administreres i Finance and Operations, og de synkroniseres til Project Service Automation som transaksjonskategorier.</span><span class="sxs-lookup"><span data-stu-id="cceb3-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="cceb3-154">Synkronisering tilbake til Finance and Operations oppdaterer integrasjons-ID-en fra Project Service Automation i Finance and Operations-prosjektkategorien.</span><span class="sxs-lookup"><span data-stu-id="cceb3-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="cceb3-155">Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="cceb3-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="cceb3-156">Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="cceb3-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="cceb3-157">[![Tilordning av mal](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="cceb3-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

