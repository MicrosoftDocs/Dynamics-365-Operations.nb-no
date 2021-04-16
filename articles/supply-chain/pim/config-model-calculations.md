---
title: Beregninger i produktkonfigurasjonsmodell
description: Dette emnet beskriver hvordan du oppretter beregninger for attributter i en produktkonfigurasjonsmodell
author: t-benebo
ms.date: 03/18/2021
ms.topic: article
ms.search.form: PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-03-18
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: eaf6264f060d33575740ad38e7a65158baba296b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5829624"
---
# <a name="product-configuration-model-calculations"></a><span data-ttu-id="c8c97-103">Beregninger i produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="c8c97-103">Product configuration model calculations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c8c97-104">Dette emnet beskriver hvordan du oppretter beregninger for attributter i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="c8c97-104">This topic describes how to create calculations for attributes in a product configuration model.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c8c97-105">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="c8c97-105">Prerequisites</span></span>

<span data-ttu-id="c8c97-106">Beregninger brukes til å beregne konfigurasjonsverdiene for et produkt i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="c8c97-106">Calculations are used in a product configuration model to calculate the configuration values for a product.</span></span> <span data-ttu-id="c8c97-107">Før du kan sette opp beregninger, må den relaterte produktkonfigurasjonsmodellen finnes.</span><span class="sxs-lookup"><span data-stu-id="c8c97-107">Before you can start to set up calculations, the related product configuration model must exist.</span></span> <span data-ttu-id="c8c97-108">Hvis du vil ha en oversikt over oppsettsprosessen for konfigurasjonsmodeller og de relaterte oppgavene, kan du se [Definer en produktkonfigurasjonsmodell](set-up-maintain-product-configuration-model.md).</span><span class="sxs-lookup"><span data-stu-id="c8c97-108">For an overview of the setup process for configuration models and the related tasks, see [Set up a product configuration model](set-up-maintain-product-configuration-model.md).</span></span>

## <a name="create-a-calculation"></a><span data-ttu-id="c8c97-109">Opprett en beregning</span><span class="sxs-lookup"><span data-stu-id="c8c97-109">Create a calculation</span></span>

<span data-ttu-id="c8c97-110">En beregning består av et uttrykk og et målattributt.</span><span class="sxs-lookup"><span data-stu-id="c8c97-110">A calculation consists of an expression and a target attribute.</span></span> <span data-ttu-id="c8c97-111">Hvis du vil ha mer informasjon, kan du se [Vanlige spørsmål om beregninger for produktkonfigurasjonsmodeller](calculate-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="c8c97-111">For more information, see [Calculations for product configuration models FAQ](calculate-product-configuration-models.md).</span></span>

<span data-ttu-id="c8c97-112">Følg denne fremgangsmåten for å opprette en beregning for en eksisterende produktmodell.</span><span class="sxs-lookup"><span data-stu-id="c8c97-112">To create a calculation for an existing product model, follow these steps.</span></span>

1. <span data-ttu-id="c8c97-113">Gå til **Behandling av produktinformasjon \> Felles \> Produktkonfigurasjonsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="c8c97-113">Go to **Product information management \> Common \> Product configuration models**.</span></span>
1. <span data-ttu-id="c8c97-114">Åpne en produktkonfigurasjonsmodell, og velg deretter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="c8c97-114">Open a product configuration model, and then select **Edit**.</span></span>
1. <span data-ttu-id="c8c97-115">På **Beregninger**-hurtigfanen velger du **Legg til** for å legge til en beregning, og deretter angir du følgende felter:</span><span class="sxs-lookup"><span data-stu-id="c8c97-115">On the **Calculations** FastTab, select **Add** to add a calculation, and then set the following fields:</span></span>

    - <span data-ttu-id="c8c97-116">**Navn** – Angi et navn for beregningen.</span><span class="sxs-lookup"><span data-stu-id="c8c97-116">**Name** – Enter a name for the calculation.</span></span>
    - <span data-ttu-id="c8c97-117">**Beskrivelse** – Angi en beskrivelse av beregningen.</span><span class="sxs-lookup"><span data-stu-id="c8c97-117">**Description** – Enter a description of the calculation.</span></span>
    - <span data-ttu-id="c8c97-118">**Målattributt** – Velg attributtet som du gjør beregningen for.</span><span class="sxs-lookup"><span data-stu-id="c8c97-118">**Target attribute** – Select the attribute that you're making the calculation for.</span></span>

1. <span data-ttu-id="c8c97-119">Velg **Rediger uttrykk**.</span><span class="sxs-lookup"><span data-stu-id="c8c97-119">Select **Edit expression**.</span></span>
1. <span data-ttu-id="c8c97-120">I dialogboksen **Angi en beregning** legger du til de nødvendige attributtene, operatorene og verdiene i uttrykket.</span><span class="sxs-lookup"><span data-stu-id="c8c97-120">In the **Enter a calculation** dialog box, add the required attributes, operators, and values to the expression.</span></span> <span data-ttu-id="c8c97-121">Hvis du vil ha mer informasjon om hvordan du kan arbeide med disse elementene, kan du se [Uttrykksbegrensninger og tabellbegrensninger i produktkonfigurasjonsmodeller](expression-constraints-table-constraints-product-configuration-models.md).</span><span class="sxs-lookup"><span data-stu-id="c8c97-121">For more information about how to work with these elements, see [Expression constraints and table constraints in product configuration models](expression-constraints-table-constraints-product-configuration-models.md).</span></span>
1. <span data-ttu-id="c8c97-122">Når uttrykket er klart, velger du **OK**.</span><span class="sxs-lookup"><span data-stu-id="c8c97-122">When your expression is ready, select **OK**.</span></span>

## <a name="calculation-examples"></a><span data-ttu-id="c8c97-123">Beregningseksempler</span><span class="sxs-lookup"><span data-stu-id="c8c97-123">Calculation examples</span></span>

<span data-ttu-id="c8c97-124">Denne delen gir noen eksempler som viser hvordan beregninger fungerer.</span><span class="sxs-lookup"><span data-stu-id="c8c97-124">This section provides a few examples that show how calculations work.</span></span>

### <a name="example-1"></a><span data-ttu-id="c8c97-125">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="c8c97-125">Example 1</span></span>

<span data-ttu-id="c8c97-126">Målattributtet er boolsk, og beregningen bruker følgende betingede uttrykk:</span><span class="sxs-lookup"><span data-stu-id="c8c97-126">The target attribute is Boolean, and the calculation uses the following conditional expression:</span></span>

`If[(decimalAttribute1 / decimalAttribute2) < 1, True, False]`

<span data-ttu-id="c8c97-127">Dette uttrykket returnerer verdien *Sann* til målattributtet hvis `decimalAttribute2` er større enn eller lik `decimalAttribute1`.</span><span class="sxs-lookup"><span data-stu-id="c8c97-127">This expression returns a value of *True* to the target attribute if `decimalAttribute2` is greater than or equal to `decimalAttribute1`.</span></span> <span data-ttu-id="c8c97-128">Hvis ikke returneres den boolske verdien *Usann*.</span><span class="sxs-lookup"><span data-stu-id="c8c97-128">Otherwise, it returns a value of *False*.</span></span>

### <a name="example-2"></a><span data-ttu-id="c8c97-129">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="c8c97-129">Example 2</span></span>

<span data-ttu-id="c8c97-130">I dette eksemplet brukes tekstattributtet `textFixedList` som målattributtet.</span><span class="sxs-lookup"><span data-stu-id="c8c97-130">This example uses the text attribute `textFixedList` as the target attribute.</span></span> <span data-ttu-id="c8c97-131">Dette attributtet inneholder følgende faste liste.</span><span class="sxs-lookup"><span data-stu-id="c8c97-131">This attribute contains the following fixed list.</span></span>

| <span data-ttu-id="c8c97-132">Verdi</span><span class="sxs-lookup"><span data-stu-id="c8c97-132">Value</span></span> | <span data-ttu-id="c8c97-133">Problemløserverdi</span><span class="sxs-lookup"><span data-stu-id="c8c97-133">Solver value</span></span> |
|---|---|
| <span data-ttu-id="c8c97-134">A</span><span class="sxs-lookup"><span data-stu-id="c8c97-134">A</span></span> | <span data-ttu-id="c8c97-135">1a</span><span class="sxs-lookup"><span data-stu-id="c8c97-135">1a</span></span> |
| <span data-ttu-id="c8c97-136">T</span><span class="sxs-lookup"><span data-stu-id="c8c97-136">B</span></span> | <span data-ttu-id="c8c97-137">2b</span><span class="sxs-lookup"><span data-stu-id="c8c97-137">2b</span></span> |
| <span data-ttu-id="c8c97-138">K</span><span class="sxs-lookup"><span data-stu-id="c8c97-138">C</span></span> | <span data-ttu-id="c8c97-139">2c</span><span class="sxs-lookup"><span data-stu-id="c8c97-139">2c</span></span> |

<span data-ttu-id="c8c97-140">Følgende skjermbilde viser hvordan innstillingene for dette attributtet kan se ut i systemet.</span><span class="sxs-lookup"><span data-stu-id="c8c97-140">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="c8c97-141">![Attributtytypeinnstillinger for eksempel 2](media/model-calculations-example2.png "Attributtytypeinnstillinger for eksempel 2")</span><span class="sxs-lookup"><span data-stu-id="c8c97-141">![Attribute type settings for example 2](media/model-calculations-example2.png "Attribute type settings for example 2")</span></span>

<span data-ttu-id="c8c97-142">Attributtet brukes i følgende betingede setning:</span><span class="sxs-lookup"><span data-stu-id="c8c97-142">The attribute is used in the following conditional statement:</span></span>

`If[integerAttribute < 150, 0, 2]`

<span data-ttu-id="c8c97-143">Hvis `integerAttribute` er mindre enn 150, returneres tekstverdien til den første posten i den faste listen, *A*. Ellers returneres tekstverdien til den tredje posten i den faste listen, *C*.</span><span class="sxs-lookup"><span data-stu-id="c8c97-143">If `integerAttribute` is less than 150, this statement returns the text value of the first record in the fixed list, *A*. Otherwise, it returns the text value of the third record in the fixed list, *C*.</span></span>

> [!NOTE]
> <span data-ttu-id="c8c97-144">Den faste listen tilsvarer en nullbasert opplisting, og du får tilgang til verdiene via den aktuelle heltallsverdien.</span><span class="sxs-lookup"><span data-stu-id="c8c97-144">The fixed list is equivalent to a zero-based enumeration (enum), and its values are accessed by the appropriate integer value.</span></span> <span data-ttu-id="c8c97-145">Derfor sammenlignes den første faste listeverdien (*A*) med *0*, den andre verdien (*B*) sammenlignes med *1*, og den tredje verdien (*C*) sammenlignes med *2*.</span><span class="sxs-lookup"><span data-stu-id="c8c97-145">Therefore, the first fixed list value (*A*) is matched to *0*, the second value (*B*) is matched to *1*, and the third value (*C*) is matched to *2*.</span></span>

### <a name="example-3"></a><span data-ttu-id="c8c97-146">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="c8c97-146">Example 3</span></span>

<span data-ttu-id="c8c97-147">I dette eksemplet brukes måltattributtet `textFixedList` fra forrige eksempel.</span><span class="sxs-lookup"><span data-stu-id="c8c97-147">This example uses the `textFixedList` target attribute from the previous example.</span></span> <span data-ttu-id="c8c97-148">Det bruker også et annet tekstattributt, `textAttribute`, som inneholder følgende faste liste.</span><span class="sxs-lookup"><span data-stu-id="c8c97-148">It also uses another text attribute, `textAttribute`, that contains the following fixed list.</span></span>

| <span data-ttu-id="c8c97-149">Verdi</span><span class="sxs-lookup"><span data-stu-id="c8c97-149">Value</span></span> | <span data-ttu-id="c8c97-150">Problemløserverdi</span><span class="sxs-lookup"><span data-stu-id="c8c97-150">Solver value</span></span> |
|---|---|
| <span data-ttu-id="c8c97-151">AA</span><span class="sxs-lookup"><span data-stu-id="c8c97-151">AA</span></span> | <span data-ttu-id="c8c97-152">1aa</span><span class="sxs-lookup"><span data-stu-id="c8c97-152">1aa</span></span> |
| <span data-ttu-id="c8c97-153">BB</span><span class="sxs-lookup"><span data-stu-id="c8c97-153">BB</span></span> | <span data-ttu-id="c8c97-154">2bb</span><span class="sxs-lookup"><span data-stu-id="c8c97-154">2bb</span></span> |

<span data-ttu-id="c8c97-155">Følgende skjermbilde viser hvordan innstillingene for dette attributtet kan se ut i systemet.</span><span class="sxs-lookup"><span data-stu-id="c8c97-155">The following screenshot shows how the settings for this attribute might look in your system.</span></span>

<span data-ttu-id="c8c97-156">![Attributtytypeinnstillinger for eksempel 3](media/model-calculations-example3.png "Attributtytypeinnstillinger for eksempel 3")</span><span class="sxs-lookup"><span data-stu-id="c8c97-156">![Attribute type settings for example 3](media/model-calculations-example3.png "Attribute type settings for example 3")</span></span>

<span data-ttu-id="c8c97-157">Verdien for `textFixedList`-attributtet beregnes ved hjelp av følgende betingede setning:</span><span class="sxs-lookup"><span data-stu-id="c8c97-157">The value for the `textFixedList` attribute is calculated by using the following conditional statement:</span></span>

`If[textAttribute == "1aa", 0, 2]`

<span data-ttu-id="c8c97-158">Hvis `textAttribute`-verdien har en løserverdi som er lik *1aa*, returnerer dette uttrykket tekstverdien til den første posten i den faste `textFixedList`-listen, *A*. Ellers returneres tekstverdien til den tredje posten i den faste `textFixedList`-listen, *C*.</span><span class="sxs-lookup"><span data-stu-id="c8c97-158">If the `textAttribute` value has a solver value that equals *1aa*, this expression returns the text value of the first record in the `textFixedList` fixed list, *A*. Otherwise, it returns the text value of the third record in the `textFixedList` fixed list, *C*.</span></span>

> [!NOTE]
> - <span data-ttu-id="c8c97-159">Den betingede setningen må bruke løserverdien til attributtet.</span><span class="sxs-lookup"><span data-stu-id="c8c97-159">The conditional statement must use the solver value of the attribute.</span></span>
> - <span data-ttu-id="c8c97-160">Bare tekstattributter i en fast liste kan brukes i beregninger.</span><span class="sxs-lookup"><span data-stu-id="c8c97-160">Only fixed-list text attributes can be used in calculations.</span></span>

## <a name="see-also"></a><span data-ttu-id="c8c97-161">Se også</span><span class="sxs-lookup"><span data-stu-id="c8c97-161">See also</span></span>

- [<span data-ttu-id="c8c97-162">Vanlige spørsmål om beregninger for produktkonfigurasjonsmodeller</span><span class="sxs-lookup"><span data-stu-id="c8c97-162">Calculations for product configuration models FAQ</span></span>](calculate-product-configuration-models.md)
- [<span data-ttu-id="c8c97-163">Legge til en uttrykksbegrensning i en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="c8c97-163">Add an expression constraint to a product configuration model</span></span>](tasks/add-expression-constraint-product-configuration-model.md)
- [<span data-ttu-id="c8c97-164">Oversikt over produktkonfigurasjonsmodeller</span><span class="sxs-lookup"><span data-stu-id="c8c97-164">Product configuration models overview</span></span>](product-configuration-models.md)
