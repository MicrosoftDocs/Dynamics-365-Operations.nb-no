---
title: Legge til en uttrykksbegrensning i en produktkonfigurasjonsmodell
description: Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails, SysClientPolymorphicCreateSelector, PCConstraintEditor, PCRuntimeConfiguratorValidate
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9cd5475e48cbcd8dcee6b228297f58e364ac503d
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920887"
---
# <a name="add-an-expression-constraint-to-a-product-configuration-model"></a><span data-ttu-id="7a9da-103">Legge til en uttrykksbegrensning i en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="7a9da-103">Add an expression constraint to a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7a9da-104">Denne fremgangsmåten beskriver hvordan du kan legge til et nytt begrensningsuttrykk i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="7a9da-104">This procedure shows how you can add a new constraint expression to a product configuration model.</span></span> <span data-ttu-id="7a9da-105">Den viser hvordan du kan kreve at hjørnebeskyttelse må brukes på en høyttaler hvis brukeren har valgt en frontgrill i metall.</span><span class="sxs-lookup"><span data-stu-id="7a9da-105">It shows how you can mandate that corner protection must be applied to a speaker if the user has selected a front grill in metal.</span></span> <span data-ttu-id="7a9da-106">Fremgangsmåten bruker komponenten for High-end-høyttaler i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="7a9da-106">The procedure uses the High end speaker component in the demo company USMF.</span></span>

## <a name="create-an-expression-constraint"></a><span data-ttu-id="7a9da-107">Opprette en uttrykksbegrensning</span><span class="sxs-lookup"><span data-stu-id="7a9da-107">Create an expression constraint</span></span>

1. <span data-ttu-id="7a9da-108">Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="7a9da-108">Go to **Product information management \> Products \> Product configuration models**.</span></span>
3. <span data-ttu-id="7a9da-109">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="7a9da-109">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="7a9da-110">Dette eksemplet bruker modellen for High-end-høyttaler.</span><span class="sxs-lookup"><span data-stu-id="7a9da-110">This example uses the high end speaker model.</span></span>  
4. <span data-ttu-id="7a9da-111">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7a9da-111">In the list, select the link in the selected row.</span></span>
5. <span data-ttu-id="7a9da-112">Utvid delen **Begrensninger**.</span><span class="sxs-lookup"><span data-stu-id="7a9da-112">Expand the **Constraints** section.</span></span>
6. <span data-ttu-id="7a9da-113">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="7a9da-113">Select **Add**.</span></span>
7. <span data-ttu-id="7a9da-114">Velg **Opprett**.</span><span class="sxs-lookup"><span data-stu-id="7a9da-114">Select **Create**.</span></span>
8. <span data-ttu-id="7a9da-115">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a9da-115">In the **Name** field, type a value.</span></span>

## <a name="enter-expression"></a><span data-ttu-id="7a9da-116">Angi uttrykk</span><span class="sxs-lookup"><span data-stu-id="7a9da-116">Enter expression</span></span>

1. <span data-ttu-id="7a9da-117">Velg **Rediger uttrykk**.</span><span class="sxs-lookup"><span data-stu-id="7a9da-117">Select **Edit expression**.</span></span>
    * <span data-ttu-id="7a9da-118">Hvis du låser opp brukergrensesnittet i oppgaveregistreringen i denne fasen, kan du bruke IntelliSense og listen over symboler til å bygge restriksjonsuttrykket.</span><span class="sxs-lookup"><span data-stu-id="7a9da-118">If you unlock the user interface in the task recording at this stage, you can use IntelliSense and the list of symbols to build the constraint expression .</span></span>  
2. <span data-ttu-id="7a9da-119">I **ConstraintBody**-feltet skriver du inn "Implies[FrontGrill=="Metal", CornerProtection]".</span><span class="sxs-lookup"><span data-stu-id="7a9da-119">In the **ConstraintBody** field, enter 'Implies[FrontGrill=="Metal", CornerProtection] '.</span></span>
    * <span data-ttu-id="7a9da-120">Denne uttrykkslogikken sier: Hvis frontgrillen er metall, må alternativet for hjørnebeskyttelse velges.</span><span class="sxs-lookup"><span data-stu-id="7a9da-120">This expression logic states: If the Front grill is  metal, then the corner protection option must be selected.</span></span>  
3. <span data-ttu-id="7a9da-121">Velg **Valider**.</span><span class="sxs-lookup"><span data-stu-id="7a9da-121">Select **Validate**.</span></span>
    * <span data-ttu-id="7a9da-122">Valideringsfunksjonen kjøres gjennom begrensningsuttrykket og sjekker for syntaksfeil.</span><span class="sxs-lookup"><span data-stu-id="7a9da-122">The validate function runs through the constraint expression and checks for syntax errors.</span></span>  
4. <span data-ttu-id="7a9da-123">Velg **Lukk**.</span><span class="sxs-lookup"><span data-stu-id="7a9da-123">Select **Close**.</span></span>
5. <span data-ttu-id="7a9da-124">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="7a9da-124">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]