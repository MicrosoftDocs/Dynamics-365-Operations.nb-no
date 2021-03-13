---
title: Sende og godkjenne prosjektbudsjett
description: Denne prosedyren viser hvordan du oppretter og sender inn budsjettet for et prosjekt.
author: RichardLuan
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Service industries
ms.author: riluan
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b871a3fef3515d3a79fb4b55406a93fc16d02faa
ms.sourcegitcommit: deac22ba5377a912d93fe408c5ae875706378c2d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/16/2021
ms.locfileid: "5018734"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="9c7dc-103">Sende og godkjenne prosjektbudsjett</span><span class="sxs-lookup"><span data-stu-id="9c7dc-103">Submit and approve project budget</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9c7dc-104">Denne prosedyren viser hvordan du oppretter og sender inn budsjettet for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="9c7dc-105">Når du oppretter et prosjektbudsjett, kan du angi estimerte inntekter og kostnader for et prosjekt, og deretter bruke disse til å kontrollere faktiske prosjekttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="9c7dc-106">I prosjektbudsjettering må alle opprinnelige budsjetter og endringer sendes til en projektarbeidsflyt for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="9c7dc-107">Arbeidsflyt gir deg bedre kontroll over prosessen og oppretter en endringshistorikkpost.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="9c7dc-108">Denne oppgaven ble opprettet med USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="9c7dc-109">Gå til **Moduler > Prosjektstyring og regnskap > Prosjekter > Alle prosjekter** i **navigasjonsruten**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-109">In the **Navigation pane**, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="9c7dc-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="9c7dc-111">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="9c7dc-112">Klikk på **Plan** i **handlingsruten**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-112">On the **Action Pane**, click **Plan**.</span></span>
5. <span data-ttu-id="9c7dc-113">Klikk på **Prosjektbudsjett**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-113">Click **Project budget**.</span></span>
6. <span data-ttu-id="9c7dc-114">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-114">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="9c7dc-115">Utvid **Kostnad**-hurtigfanen.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-115">Expand the **Cost** fastTab.</span></span>
8. <span data-ttu-id="9c7dc-116">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-116">Click **New**.</span></span>
9. <span data-ttu-id="9c7dc-117">Velg et alternativ i **Transaksjonstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-117">In the **Transaction type** field, select an option.</span></span>
10. <span data-ttu-id="9c7dc-118">Angi eller velg en verdi i **Kategori**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-118">In the **Category** field, enter or select a value.</span></span>
11. <span data-ttu-id="9c7dc-119">Angi et tall i feltet **Opprinnelig budsjett**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-119">In the **Original budget** field, enter a number.</span></span>
12. <span data-ttu-id="9c7dc-120">Vis hurtigfanen **Omsetning**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-120">Expand the **Revenues** fastTab.</span></span>
13. <span data-ttu-id="9c7dc-121">Klikk på **Ny**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-121">Click **New**.</span></span>
14. <span data-ttu-id="9c7dc-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="9c7dc-123">Velg et alternativ i **Transaksjonstype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-123">In the **Transaction type** field, select an option.</span></span>
16. <span data-ttu-id="9c7dc-124">Angi eller velg en verdi i **Kategori**-feltet.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-124">In the **Category** field, enter or select a value.</span></span>
17. <span data-ttu-id="9c7dc-125">Angi et tall i feltet **Opprinnelig budsjett**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-125">In the **Original budget** field, enter a number.</span></span>
18. <span data-ttu-id="9c7dc-126">Klikk på **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-126">Click **Save**.</span></span>
19. <span data-ttu-id="9c7dc-127">Klikk på **Arbeidsflyt**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-127">Click **Workflow**.</span></span>
20. <span data-ttu-id="9c7dc-128">Klikk på **Send**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-128">Click **Submit**.</span></span>
21. <span data-ttu-id="9c7dc-129">Skriv inn en verdi i feltet **Kommentar**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-129">In the **Comment** field, type a value.</span></span>
22. <span data-ttu-id="9c7dc-130">Klikk på **Send**.</span><span class="sxs-lookup"><span data-stu-id="9c7dc-130">Click **Submit**.</span></span>

