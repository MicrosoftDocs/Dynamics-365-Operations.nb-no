---
title: Legge til en foregående aktivitet i en produksjonsflytaktivitet
description: Alle aktiviteter må være sekvensert i en produksjonsflytversjon.
author: cvocph
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LeanProductionFlow, PlanActivity, PlanActivityRelationNew, PlanActivityLookup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e64ad19c557c7b0fd8747bb9b748859e70eaa63a
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3149395"
---
# <a name="add-a-predecessor-to-a-production-flow-activity"></a><span data-ttu-id="4b92b-103">Legge til en foregående aktivitet i en produksjonsflytaktivitet</span><span class="sxs-lookup"><span data-stu-id="4b92b-103">Add a predecessor to a production flow activity</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="4b92b-104">Alle aktiviteter må være sekvensert i en produksjonsflytversjon.</span><span class="sxs-lookup"><span data-stu-id="4b92b-104">In a production flow version, all activities must be sequenced.</span></span> <span data-ttu-id="4b92b-105">En aktivitet kan ha én eller flere foregående eller etterfølgende aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="4b92b-105">An activity can have one or multiple predecessors or successors.</span></span> 

<span data-ttu-id="4b92b-106">Denne fremgangsmåten viser hvordan du knytter en foregående aktivitet til en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="4b92b-106">This procedure shows how to associate a predecessor to an activity.</span></span> 

<span data-ttu-id="4b92b-107">For å utføre denne oppgaven, trenger du en produksjonsflyt som har en utkastversjon med minst to aktiviteter som kan være koblet.</span><span class="sxs-lookup"><span data-stu-id="4b92b-107">To perform this task, you need a production flow that has the Draft version with at least two activities that can be connected.</span></span> 

<span data-ttu-id="4b92b-108">Hvis du vil ha mer informasjon, kan du se hvitboken Produksjonsflyter og -aktiviteter i lean manufacturing.</span><span class="sxs-lookup"><span data-stu-id="4b92b-108">To learn more, read the white paper "Production flows and activities in lean manufacturing."</span></span>


## <a name="find-the-production-flow-and-version"></a><span data-ttu-id="4b92b-109">Finne produksjonsflyten og versjonen</span><span class="sxs-lookup"><span data-stu-id="4b92b-109">Find the production flow and version</span></span>
1. <span data-ttu-id="4b92b-110">Gå til Produksjonskontroll > Oppsett > Lean-produksjonsflyt > Produksjonsflyter.</span><span class="sxs-lookup"><span data-stu-id="4b92b-110">Go to Production control > Setup > Lean production flow > Production flows.</span></span>
2. <span data-ttu-id="4b92b-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4b92b-111">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="4b92b-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4b92b-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="4b92b-113">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4b92b-113">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4b92b-114">Klikk Aktiviteter.</span><span class="sxs-lookup"><span data-stu-id="4b92b-114">Click Activities.</span></span>

## <a name="select-an-activity-and-add-a-predecessor"></a><span data-ttu-id="4b92b-115">Velge en aktivitet og legge til en foregående aktivitet</span><span class="sxs-lookup"><span data-stu-id="4b92b-115">Select an activity and add a predecessor</span></span>
1. <span data-ttu-id="4b92b-116">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4b92b-116">In the list, find and select the desired record.</span></span>
2. <span data-ttu-id="4b92b-117">Klikk Legg til foregående aktivitet.</span><span class="sxs-lookup"><span data-stu-id="4b92b-117">Click Add predecessor.</span></span>
3. <span data-ttu-id="4b92b-118">Angi eller velg en verdi i feltet Aktivitet.</span><span class="sxs-lookup"><span data-stu-id="4b92b-118">In the Activity field, enter or select a value.</span></span>
4. <span data-ttu-id="4b92b-119">Angi et tall i feltet Forhold for syklustid.</span><span class="sxs-lookup"><span data-stu-id="4b92b-119">In the Cycle time ratio field, enter a number.</span></span>
    * <span data-ttu-id="4b92b-120">Standard syklustidsforhold for en aktivitetsrelasjon er 1.</span><span class="sxs-lookup"><span data-stu-id="4b92b-120">The default cycle time ratio of an activity relation is 1.</span></span> <span data-ttu-id="4b92b-121">Dette forutsetter at begge aktivitetene kjører med samme hastighet eller takttid.</span><span class="sxs-lookup"><span data-stu-id="4b92b-121">This assumes that both activities run at the same pace or takt time.</span></span> <span data-ttu-id="4b92b-122">Hvis den foregående aktiviteten kjører med et høyere tempo (lavere takttid), må forholdet være lavere enn 1, og hvis den foregående aktiviteten går langsommere (høyere takttid), er syklustidsforholdet større enn 1.</span><span class="sxs-lookup"><span data-stu-id="4b92b-122">If the predecessor runs at a higher pace (lower takt time), the ratio should be lower than 1, if the predecessor runs at a slower pace (higher takt time) the cycle time ratio is greater than 1.</span></span>  
5. <span data-ttu-id="4b92b-123">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4b92b-123">Click OK.</span></span>

