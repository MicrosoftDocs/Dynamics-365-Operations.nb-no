---
title: Opprette dimensjoner og importere dimensjonsmedlemmer
description: Kostnadsregnskap er en uavhengig modul som krever hoveddata fra andre moduler.
author: ShylaThompson
manager: AnnBe
ms.date: 09/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 256254
ms.assetid: e1b0a6e3-0c72-4a7d-90e1-20f870c6dbad
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: a7db93e1877034051b6add4c11ddfe7cd7d17e0b
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841591"
---
# <a name="create-dimensions-and-import-dimension-members"></a><span data-ttu-id="66214-103">Opprette dimensjoner og importere dimensjonsmedlemmer</span><span class="sxs-lookup"><span data-stu-id="66214-103">Create dimensions and import dimension members</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="66214-104">Kostnadsregnskap er en uavhengig modul som krever data fra andre moduler.</span><span class="sxs-lookup"><span data-stu-id="66214-104">Cost accounting is an independent module that requires data from other modules.</span></span> <span data-ttu-id="66214-105">Disse dataene kategoriseres i følgende:</span><span class="sxs-lookup"><span data-stu-id="66214-105">This data is categorized into the following:</span></span>

-  <span data-ttu-id="66214-106">Kostnadselementer</span><span class="sxs-lookup"><span data-stu-id="66214-106">Cost elements</span></span>
-  <span data-ttu-id="66214-107">Kostnadsobjekter</span><span class="sxs-lookup"><span data-stu-id="66214-107">Cost objects</span></span>
-  <span data-ttu-id="66214-108">Statistiske dimensjoner</span><span class="sxs-lookup"><span data-stu-id="66214-108">Statistical dimensions</span></span>

<span data-ttu-id="66214-109">Et **Kostnadselement** korresponderer til et kostnadsrelevant element i diagrammet over kontoer.</span><span class="sxs-lookup"><span data-stu-id="66214-109">A **Cost element** corresponds to a cost-relevant item in the chart of accounts.</span></span> <span data-ttu-id="66214-110">Et **Kostnadsobjekt** korresponderer til enhver form for økonomisk dimensjon, for eksempel produkter, kostnadssteder og prosjekter som du vil estimere, tildele kostnader til eller måle direkte.</span><span class="sxs-lookup"><span data-stu-id="66214-110">A **Cost object** corresponds to any type of financial dimension, such as products, cost centers, and projects that you want to estimate, allocate costs to, or measure directly.</span></span> <span data-ttu-id="66214-111">En **Statistisk dimensjon** og dens medlemmer brukes for å registrere ikke-monetære oppføringer.</span><span class="sxs-lookup"><span data-stu-id="66214-111">A **Statistical dimension** and its members are used to register non-monetary entries.</span></span> <span data-ttu-id="66214-112">Medlemmer av statistisk dimensjon kan brukes som en fordelingsbase i kostnadsfordeling og allokering</span><span class="sxs-lookup"><span data-stu-id="66214-112">Statistical dimension members can be used as an allocation base in cost distribution and allocation</span></span> 

<span data-ttu-id="66214-113">De følgende diagrammer illustrerer dimensjoner som brukes for kostnadsregnskap.</span><span class="sxs-lookup"><span data-stu-id="66214-113">The following diagram illustrates the dimensions that are used in Cost accounting.</span></span>

<span data-ttu-id="66214-114">[![Dimensjoner for kostnadsregnskap](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span><span class="sxs-lookup"><span data-stu-id="66214-114">[![Cost accounting dimensions](./media/cost-eos-dimensions.png)](./media/cost-eos-dimensions.png)</span></span>

<span data-ttu-id="66214-115">Etter at data er import i Kostnadsregnskap kan du bruke det for å bygge ulike perspektiver som gir innsikt til ledere på alle nivåer i organisasjonen.</span><span class="sxs-lookup"><span data-stu-id="66214-115">After the data is imported into Cost accounting, you can use it to build various perspectives that provide insights to managers at all levels of the organization.</span></span> <span data-ttu-id="66214-116">Følgende emner gir informasjon om hvordan du lager dimensjoner og importerer dimensjonsmedlemmer.</span><span class="sxs-lookup"><span data-stu-id="66214-116">The following topics provide information about creating dimensions and importing dimension members.</span></span> 

-  [<span data-ttu-id="66214-117">Kostnadselementdimensjoner</span><span class="sxs-lookup"><span data-stu-id="66214-117">Cost element dimensions</span></span>](cost-elements.md)
-  [<span data-ttu-id="66214-118">Opprette kostnadselementer (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="66214-118">Create cost elements (Task guide)</span></span>](./tasks/create-cost-elements.md)
-  [<span data-ttu-id="66214-119">Kostnadsobjektdimensjoner</span><span class="sxs-lookup"><span data-stu-id="66214-119">Cost object dimensions</span></span>](cost-objects.md)
-  [<span data-ttu-id="66214-120">Opprette kostnadselementer (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="66214-120">Create cost elements (Task guide)</span></span>](./tasks/create-cost-objects.md)
-  [<span data-ttu-id="66214-121">Tilordne dimensjonsmedlemmer for kostnadselement til et felles sett med dimensjonsmedlemmer</span><span class="sxs-lookup"><span data-stu-id="66214-121">Map cost element dimension members to a common set of dimension members</span></span>](map-cost-elements-dimension-members.md)
-  [<span data-ttu-id="66214-122">Tilordne en kostnadselementdimensjon (oppgaveveiledning)</span><span class="sxs-lookup"><span data-stu-id="66214-122">Map a cost element dimension (Task guide)</span></span>](./tasks/map-cost-element-dimension.md)
-  [<span data-ttu-id="66214-123">Statistiske dimensjonsmedlemmer og maler for leverandør av statistisk måling</span><span class="sxs-lookup"><span data-stu-id="66214-123">Statistical dimension members and statistical measure provider templates</span></span>](statistical-measure-provider-template.md)






