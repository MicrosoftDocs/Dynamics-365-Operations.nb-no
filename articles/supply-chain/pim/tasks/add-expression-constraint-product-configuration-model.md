---
title: Legge til en uttrykksbegrensning i en produktkonfigurasjonsmodell
description: Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 56f94b82f8b2642b12a993bde7d6bb323da79f98
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547154"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="ea65f-103">Legge til en uttrykksbegrensning i en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="ea65f-103">Add an expression constraint to a product configuration model</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ea65f-104">Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="ea65f-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="ea65f-105">Den viser hvordan du kan kreve at hjørnebeskyttelse må brukes på en høyttaler hvis brukeren har valgt en frontgrill i metall.</span><span class="sxs-lookup"><span data-stu-id="ea65f-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="ea65f-106">Fremgangsmåten bruker komponenten for High-end-høyttaler i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="ea65f-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>


## <a name="create-an-expression-constraint"></a><span data-ttu-id="ea65f-107">Opprette en uttrykksbegrensning</span><span class="sxs-lookup"><span data-stu-id="ea65f-107">Create an expression constraint</span></span>
1. <span data-ttu-id="ea65f-108">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="ea65f-108">Click Product variant model definition.</span></span>
2. <span data-ttu-id="ea65f-109">Klikk Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="ea65f-109">Click Product configuration models.</span></span>
3. <span data-ttu-id="ea65f-110">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="ea65f-110">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="ea65f-111">Dette eksemplet bruker modellen for High-end-høyttaler.</span><span class="sxs-lookup"><span data-stu-id="ea65f-111">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="ea65f-112">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ea65f-112">In the list, click the link in the selected row.</span></span>
5. <span data-ttu-id="ea65f-113">Utvid delen Begrensninger.</span><span class="sxs-lookup"><span data-stu-id="ea65f-113">Expand the Constraints section.</span></span>
6. <span data-ttu-id="ea65f-114">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="ea65f-114">Click Add.</span></span>
7. <span data-ttu-id="ea65f-115">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="ea65f-115">Click Create.</span></span>
8. <span data-ttu-id="ea65f-116">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="ea65f-116">In the Name field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="ea65f-117">Angi uttrykk</span><span class="sxs-lookup"><span data-stu-id="ea65f-117">Enter expression</span></span>
1. <span data-ttu-id="ea65f-118">Klikk Rediger uttrykk.</span><span class="sxs-lookup"><span data-stu-id="ea65f-118">Click Edit expression.</span></span>
    * <span data-ttu-id="ea65f-119">Hvis du låser opp brukergrensesnittet i oppgaveregistreringen i denne fasen, kan du bruke IntelliSense og listen over symboler til å bygge restriksjonsuttrykket.</span><span class="sxs-lookup"><span data-stu-id="ea65f-119">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="ea65f-120">I ConstraintBody-feltet skriver du inn "Implies[FrontGrill=="Metal", CornerProtection]".</span><span class="sxs-lookup"><span data-stu-id="ea65f-120">In the ConstraintBody field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="ea65f-121">Denne uttrykkslogikken sier: Hvis frontgrillen er metall, må alternativet for hjørnebeskyttelse velges.</span><span class="sxs-lookup"><span data-stu-id="ea65f-121">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="ea65f-122">Klikk Valider.</span><span class="sxs-lookup"><span data-stu-id="ea65f-122">Click Validate.</span></span>
    * <span data-ttu-id="ea65f-123">Valideringsfunksjonen kjøres gjennom begrensningsuttrykket og sjekker for syntaksfeil.</span><span class="sxs-lookup"><span data-stu-id="ea65f-123">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="ea65f-124">Klikk Lukk.</span><span class="sxs-lookup"><span data-stu-id="ea65f-124">Click Close.</span></span>
5. <span data-ttu-id="ea65f-125">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="ea65f-125">Click OK.</span></span>

