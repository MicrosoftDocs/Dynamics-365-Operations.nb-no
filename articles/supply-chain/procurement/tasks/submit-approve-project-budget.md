---
title: Sende og godkjenne prosjektbudsjett
description: Denne prosedyren viser hvordan du oppretter og sender inn budsjettet for et prosjekt.
author: mkirknel
manager: AnnBe
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 798bbc68e625c58d56cdd769f48ba734ace1d028
ms.sourcegitcommit: e10491a2ff04f65d9f306ef6e068ee123213b23b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/21/2019
ms.locfileid: "1914867"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="c0475-103">Sende og godkjenne prosjektbudsjett</span><span class="sxs-lookup"><span data-stu-id="c0475-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c0475-104">Denne prosedyren viser hvordan du oppretter og sender inn budsjettet for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="c0475-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="c0475-105">Når du oppretter et prosjektbudsjett, kan du angi estimerte inntekter og kostnader for et prosjekt, og deretter bruke disse til å kontrollere faktiske prosjekttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="c0475-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="c0475-106">I prosjektbudsjettering må alle opprinnelige budsjetter og endringer sendes til en projektarbeidsflyt for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="c0475-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="c0475-107">Arbeidsflyt gir deg bedre kontroll over prosessen og oppretter en endringshistorikkpost.</span><span class="sxs-lookup"><span data-stu-id="c0475-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="c0475-108">Denne oppgaven ble opprettet med USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="c0475-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="c0475-109">Gå til **Moduler > Prosjektstyring og regnskap > Prosjekter > Alle prosjekter** i **navigasjonsruten**.</span><span class="sxs-lookup"><span data-stu-id="c0475-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="c0475-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="c0475-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="c0475-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c0475-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="c0475-112">Klikk **Plan** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="c0475-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="c0475-113">Klikk på **Prosjektbudsjett**.</span><span class="sxs-lookup"><span data-stu-id="c0475-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="c0475-114">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0475-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="c0475-115">Utvid **Kostnad**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="c0475-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="c0475-116">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c0475-116">Click **New**.</span></span>
9. <span data-ttu-id="c0475-117">Velg et alternativ i **Transaksjonstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0475-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="c0475-118">Angi eller velg en verdi i **Kategori**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0475-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="c0475-119">Angi et tall i feltet **Opprinnelig budsjett**.</span><span class="sxs-lookup"><span data-stu-id="c0475-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="c0475-120">Vis hurtigfanen **Omsetning**.</span><span class="sxs-lookup"><span data-stu-id="c0475-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="c0475-121">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c0475-121">Click **New**.</span></span>
14. <span data-ttu-id="c0475-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="c0475-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="c0475-123">Velg et alternativ i **Transaksjonstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0475-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="c0475-124">Angi eller velg en verdi i **Kategori**-feltet.</span><span class="sxs-lookup"><span data-stu-id="c0475-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="c0475-125">Angi et tall i feltet **Opprinnelig budsjett**.</span><span class="sxs-lookup"><span data-stu-id="c0475-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="c0475-126">Klikk **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="c0475-126">Click **Save**.</span></span>
19. <span data-ttu-id="c0475-127">Klikk på **Arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="c0475-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="c0475-128">Klikk **Send**.</span><span class="sxs-lookup"><span data-stu-id="c0475-128">Click **Submit**.</span></span>
21. <span data-ttu-id="c0475-129">Skriv inn en verdi i feltet **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="c0475-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="c0475-130">Klikk **Send**.</span><span class="sxs-lookup"><span data-stu-id="c0475-130">Click **Submit**.</span></span>

