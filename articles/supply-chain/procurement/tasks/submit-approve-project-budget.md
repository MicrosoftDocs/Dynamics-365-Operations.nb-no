---
title: Sende og godkjenne prosjektbudsjett
description: Denne prosedyren viser hvordan du oppretter og sender inn budsjettet for et prosjekt.
author: mkirknel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjBudget, WorkflowSubmitDialog
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f727e19d3f8c424b1c59e52602b7e907151f4492
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "328729"
---
# <a name="submit-and-approve-project-budget"></a><span data-ttu-id="46415-103">Sende og godkjenne prosjektbudsjett</span><span class="sxs-lookup"><span data-stu-id="46415-103">Submit and approve project budget</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="46415-104">Denne prosedyren viser hvordan du oppretter og sender inn budsjettet for et prosjekt.</span><span class="sxs-lookup"><span data-stu-id="46415-104">This procedure shows you how to create and submit the budget for a project.</span></span> 

<span data-ttu-id="46415-105">Når du oppretter et prosjektbudsjett, kan du angi estimerte inntekter og kostnader for et prosjekt, og deretter bruke disse til å kontrollere faktiske prosjekttransaksjoner.</span><span class="sxs-lookup"><span data-stu-id="46415-105">When you create a project budget, you can enter estimated revenues and costs for a project, and then use those to control actual project transactions.</span></span> <span data-ttu-id="46415-106">I prosjektbudsjettering må alle opprinnelige budsjetter og endringer sendes til en projektarbeidsflyt for godkjenning.</span><span class="sxs-lookup"><span data-stu-id="46415-106">In project budgeting, all original budgets and revisions must be sent to project workflow for approval.</span></span> <span data-ttu-id="46415-107">Arbeidsflyt gir deg bedre kontroll over prosessen og oppretter en endringshistorikkpost.</span><span class="sxs-lookup"><span data-stu-id="46415-107">Workflow gives you increased control over the process and creates a change history record.</span></span>

<span data-ttu-id="46415-108">Denne oppgaven ble opprettet med USSI-datasettet.</span><span class="sxs-lookup"><span data-stu-id="46415-108">This task was created using the USSI data set.</span></span>

1. <span data-ttu-id="46415-109">Gå til Prosjektstyring og regnskap > Prosjekter > Alle prosjekter.</span><span class="sxs-lookup"><span data-stu-id="46415-109">Go to Project management and accounting > Projects > All projects.</span></span>
2. <span data-ttu-id="46415-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="46415-110">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="46415-111">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="46415-111">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="46415-112">Klikk Plan i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="46415-112">On the Action Pane, click Plan.</span></span>
5. <span data-ttu-id="46415-113">Klikk Prosjektbudsjett.</span><span class="sxs-lookup"><span data-stu-id="46415-113">Click Project budget.</span></span>
6. <span data-ttu-id="46415-114">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="46415-114">In the Description field, type a value.</span></span>
7. <span data-ttu-id="46415-115">Utvid delen Kostnad.</span><span class="sxs-lookup"><span data-stu-id="46415-115">Expand the Cost section</span></span>
8. <span data-ttu-id="46415-116">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="46415-116">Click New.</span></span>
9. <span data-ttu-id="46415-117">Velg et alternativ i Transaksjonstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="46415-117">In the Transaction type field, select an option.</span></span>
10. <span data-ttu-id="46415-118">Angi eller velg en verdi i Kategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="46415-118">In the Category field, enter or select a value.</span></span>
11. <span data-ttu-id="46415-119">Angi et tall i feltet Opprinnelig budsjett.</span><span class="sxs-lookup"><span data-stu-id="46415-119">In the Original budget field, enter a number.</span></span>
12. <span data-ttu-id="46415-120">Utvid delen Omsetning.</span><span class="sxs-lookup"><span data-stu-id="46415-120">Expand the Revenues section.</span></span>
13. <span data-ttu-id="46415-121">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="46415-121">Click New.</span></span>
14. <span data-ttu-id="46415-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="46415-122">In the list, mark the selected row.</span></span>
15. <span data-ttu-id="46415-123">Velg et alternativ i Transaksjonstype-feltet.</span><span class="sxs-lookup"><span data-stu-id="46415-123">In the Transaction type field, select an option.</span></span>
16. <span data-ttu-id="46415-124">Angi eller velg en verdi i Kategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="46415-124">In the Category field, enter or select a value.</span></span>
17. <span data-ttu-id="46415-125">Angi et tall i feltet Opprinnelig budsjett.</span><span class="sxs-lookup"><span data-stu-id="46415-125">In the Original budget field, enter a number.</span></span>
18. <span data-ttu-id="46415-126">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="46415-126">Click Save.</span></span>
19. <span data-ttu-id="46415-127">Klikk Arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="46415-127">Click Workflow.</span></span>
20. <span data-ttu-id="46415-128">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="46415-128">Click Submit.</span></span>
21. <span data-ttu-id="46415-129">Skriv inn en verdi i feltet Kommentar.</span><span class="sxs-lookup"><span data-stu-id="46415-129">In the Comment field, type a value.</span></span>
22. <span data-ttu-id="46415-130">Klikk Send.</span><span class="sxs-lookup"><span data-stu-id="46415-130">Click Submit.</span></span>

