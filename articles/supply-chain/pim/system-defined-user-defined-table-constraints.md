---
title: Systemdefinerte og brukerdefinerte tabellbegrensninger
description: 'Denne artikkelen forklarer de to typene tabellbegrensninger for komponenter i en produktkonfigurasjonsmodell: brukerdefinert og systemdefinert. Tabellbegrensninger representerer matriser for tillatte attributtkombinasjoner, der hver enkelt rad definerer et sett med mulige attributtverdier.'
author: cvocph
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PCTableConstraintAttachAttributeTree, PCTableConstraintColumnSystem, PCTableConstraintContentUserDef, PCTableConstraintDefinition, PCTableConstraintWizard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19781
ms.assetid: 0a4ea930-b344-43a8-871e-d5cd077892c4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: conradv
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8fac49cde1a6098b99e6373bf9221d3357a053a2
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814520"
---
# <a name="system-defined-and-user-defined-table-constraints"></a><span data-ttu-id="daa4f-104">Systemdefinerte og brukerdefinerte tabellbegrensninger</span><span class="sxs-lookup"><span data-stu-id="daa4f-104">System-defined and user-defined table constraints</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="daa4f-105">Denne artikkelen forklarer de to typene tabellbegrensninger for komponenter i en produktkonfigurasjonsmodell: brukerdefinert og systemdefinert.</span><span class="sxs-lookup"><span data-stu-id="daa4f-105">This article explains the two types of table constraints for components in a product configuration model -  user-defined and system-defined.</span></span> <span data-ttu-id="daa4f-106">Tabellbegrensninger representerer matriser for tillatte attributtkombinasjoner, der hver enkelt rad definerer et sett med mulige attributtverdier.</span><span class="sxs-lookup"><span data-stu-id="daa4f-106">Table constraints represent matrices of the allowed attribute combinations, where each row defines one set of possible attribute values.</span></span>

<span data-ttu-id="daa4f-107">Tabellbegrensninger representerer matriser av kombinasjoner av attributter som er tillatt for komponenter i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="daa4f-107">Table constraints represent matrices of the combinations of attributes that are allowed for components in a product configuration model.</span></span> <span data-ttu-id="daa4f-108">Hver rad i tabellen definerer et sett med mulige attributtverdier.</span><span class="sxs-lookup"><span data-stu-id="daa4f-108">Each row in the table defines one set of possible attribute values.</span></span> <span data-ttu-id="daa4f-109">Du kan angi to typer begrensninger i en produktkonfigurasjonsmodell:</span><span class="sxs-lookup"><span data-stu-id="daa4f-109">You can declare two types of constraints in a product configuration model:</span></span>

-   <span data-ttu-id="daa4f-110">**Uttrykksrestriksjon** – Opprett et uttrykk som definerer relasjoner mellom attributter for å garantere at bare kompatible verdier kan velges under produktkonfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="daa4f-110">**Expression constraint** – Create an expression that defines relations between attributes to guarantee that only compatible values can be selected during product configuration.</span></span>
-   <span data-ttu-id="daa4f-111">**Tabellbegrensning** – Opprett en tabell som definerer alle kombinasjonene som er tillatt for et angitt sett med attributter.</span><span class="sxs-lookup"><span data-stu-id="daa4f-111">**Table constraint** – Create a table that defines all the combinations that are allowed for a specified set of attributes.</span></span> <span data-ttu-id="daa4f-112">Det finnes to typer tabellbegrensninger: brukerdefinerte tabellbegrensninger og systemdefinerte tabellbegrensninger.</span><span class="sxs-lookup"><span data-stu-id="daa4f-112">Two types of table constraints are available: user-defined table constraints and system-defined table constraints.</span></span>

<span data-ttu-id="daa4f-113">Denne artikkelen beskriver brukerdefinerte og systemdefinerte tabellbegrensninger for komponenter i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="daa4f-113">This article describes user-defined and system-defined table constraints for components in a product configuration model.</span></span>

## <a name="user-defined-table-constraints"></a><span data-ttu-id="daa4f-114">Brukerdefinerte tabellbegrensninger</span><span class="sxs-lookup"><span data-stu-id="daa4f-114">User-defined table constraints</span></span>
<span data-ttu-id="daa4f-115">En brukerdefinert tabellbegrensning er en matrisetype som brukes til å beskrive kombinasjonene av attributtverdier som er angitt av attributtyper.</span><span class="sxs-lookup"><span data-stu-id="daa4f-115">A user-defined table constraint is a type of matrix that is used to describe the combinations of attribute values that are defined by attribute types.</span></span> <span data-ttu-id="daa4f-116">Hvis du produserer høyttalere, kan du for eksempel inkludere søyler for kabinettypen og frontgrillen i den brukerdefinerte tabellbegrensningen.</span><span class="sxs-lookup"><span data-stu-id="daa4f-116">For example, if you produce speakers, you can include columns for the cabinet finish and the front grill in the user-defined table constraint.</span></span> <span data-ttu-id="daa4f-117">Attributtypen for kabinettype har fire verdier, og attributtypen for frontgrill har tre verdier.</span><span class="sxs-lookup"><span data-stu-id="daa4f-117">The attribute type for the cabinet finish has four values, and the attribute type for the front grill has three values.</span></span> <span data-ttu-id="daa4f-118">Hvis begrensninger ikke er brukt, er det derfor 4 x 3 = 12 mulige kombinasjoner.</span><span class="sxs-lookup"><span data-stu-id="daa4f-118">Therefore, if constraints aren't used, there are 4 × 3 = 12 possible combinations.</span></span> <span data-ttu-id="daa4f-119">I dette eksemplet er imidlertid bare seks kombinasjoner tillatt, som vist i følgende tabell.</span><span class="sxs-lookup"><span data-stu-id="daa4f-119">However, in this example, only six combinations are allowed, as shown in the following table.</span></span> <span data-ttu-id="daa4f-120">Denne informasjonen vises i kategorien **Tillatte kombinasjoner** på siden **Rediger tabellbegrensning**.</span><span class="sxs-lookup"><span data-stu-id="daa4f-120">This information is displayed on the **Allowed combinations** tab on the **Edit table constraint** page.</span></span>

| <span data-ttu-id="daa4f-121">Kabinettyper</span><span class="sxs-lookup"><span data-stu-id="daa4f-121">Cabinet finish</span></span> | <span data-ttu-id="daa4f-122">Frontgrill</span><span class="sxs-lookup"><span data-stu-id="daa4f-122">Front grill</span></span> |
|----------------|-------------|
| <span data-ttu-id="daa4f-123">Svart</span><span class="sxs-lookup"><span data-stu-id="daa4f-123">Black</span></span>          | <span data-ttu-id="daa4f-124">Svart</span><span class="sxs-lookup"><span data-stu-id="daa4f-124">Black</span></span>       |
| <span data-ttu-id="daa4f-125">Svart</span><span class="sxs-lookup"><span data-stu-id="daa4f-125">Black</span></span>          | <span data-ttu-id="daa4f-126">Metall</span><span class="sxs-lookup"><span data-stu-id="daa4f-126">Metal</span></span>       |
| <span data-ttu-id="daa4f-127">Eik</span><span class="sxs-lookup"><span data-stu-id="daa4f-127">Oak</span></span>            | <span data-ttu-id="daa4f-128">Svart</span><span class="sxs-lookup"><span data-stu-id="daa4f-128">Black</span></span>       |
| <span data-ttu-id="daa4f-129">Rosewood</span><span class="sxs-lookup"><span data-stu-id="daa4f-129">Rosewood</span></span>       | <span data-ttu-id="daa4f-130">Hvit</span><span class="sxs-lookup"><span data-stu-id="daa4f-130">White</span></span>       |
| <span data-ttu-id="daa4f-131">Hvit</span><span class="sxs-lookup"><span data-stu-id="daa4f-131">White</span></span>          | <span data-ttu-id="daa4f-132">Svart</span><span class="sxs-lookup"><span data-stu-id="daa4f-132">Black</span></span>       |
| <span data-ttu-id="daa4f-133">Hvit</span><span class="sxs-lookup"><span data-stu-id="daa4f-133">White</span></span>          | <span data-ttu-id="daa4f-134">Hvit</span><span class="sxs-lookup"><span data-stu-id="daa4f-134">White</span></span>       |

<span data-ttu-id="daa4f-135">Brukerdefinerte tabellbegrensninger defineres av statiske tabellinndata som fungerer på samme måte som en uttrykksrestriksjon.</span><span class="sxs-lookup"><span data-stu-id="daa4f-135">User-defined table constraints are defined by static table input that works the same way as an expression constraint.</span></span> <span data-ttu-id="daa4f-136">Når du bruker en brukerdefinert tabellbegrensning, er fordelen at tabeller ofte er enklere å opprette, forstå og vedlikeholde enn lange uttrykksrestriksjoner.</span><span class="sxs-lookup"><span data-stu-id="daa4f-136">When you use a user-defined table constraint, the advantage is that tables are often easier to create, understand, and maintain than long expression constraints.</span></span>

## <a name="system-defined-table-constraints"></a><span data-ttu-id="daa4f-137">Systemdefinerte tabellbegrensninger</span><span class="sxs-lookup"><span data-stu-id="daa4f-137">System-defined table constraints</span></span>
<span data-ttu-id="daa4f-138">En systemdefinert tabellbegrensning oppretter en dynamisk tilordning mellom en attributtype og et felt i en tabell.</span><span class="sxs-lookup"><span data-stu-id="daa4f-138">A system-defined table constraint creates a dynamic mapping between an attribute type and a field in a table.</span></span> <span data-ttu-id="daa4f-139">Når en systemdefinert tabellbegrensning er inkludert i en produktkonfigurasjonsmodell, garanterer tilordningen at dataene i tabellen vises i stedet for verdiene for attributtypen.</span><span class="sxs-lookup"><span data-stu-id="daa4f-139">When a system-defined table constraint is included in a product configuration model, the mapping guarantees that the data in the table is shown instead of the values of the attribute type.</span></span> <span data-ttu-id="daa4f-140">Resultatet er en dynamisk betingelse, fordi tabellinnholdet kan endres (for eksempel av andre moduler).</span><span class="sxs-lookup"><span data-stu-id="daa4f-140">The result is a dynamic constraint, because the table contents can be modified (for example, by other modules).</span></span>  

<span data-ttu-id="daa4f-141">Når du oppretter en systemdefinert tabellbegrensning, velger du en tabell, definerer eventuelt spørringen som skal brukes, og knytter deretter attributtyper til feltene i den valgte tabellen.</span><span class="sxs-lookup"><span data-stu-id="daa4f-141">When you create a system-defined table constraint, you select a table, optionally define the query to use, and then associate attribute types to the fields in the selected table.</span></span> <span data-ttu-id="daa4f-142">Felttypene må samsvare med typene attributtyper.</span><span class="sxs-lookup"><span data-stu-id="daa4f-142">The types of fields must match the types of attribute types.</span></span>  

<span data-ttu-id="daa4f-143">Før en tabellbegrensning kan tre i kraft i en produktkonfigurasjonsmodell, må tabellbegrensningen inkluderes i en betingelse på en av komponentene for modellen.</span><span class="sxs-lookup"><span data-stu-id="daa4f-143">Before a table constraint can take effect on a product configuration model, the table constraint must be included in a constraint on one of the model's components.</span></span> <span data-ttu-id="daa4f-144">Fremgangsmåten er å opprette en ny begrensning, velge tabellbegrensningstypen og deretter velge definisjonen av tabellbegrensning som skal brukes.</span><span class="sxs-lookup"><span data-stu-id="daa4f-144">The procedure is to create a new constraint, select the table constraint type, and then select the table constraint definition to use.</span></span> <span data-ttu-id="daa4f-145">Til slutt må alle felt i tabellbegrensningen tilordnes til attributter i produktkonfigurasjonsmodellen.</span><span class="sxs-lookup"><span data-stu-id="daa4f-145">Finally, all fields in the table constraint must be mapped to attributes in the product configuration model.</span></span>

<a name="additional-resources"></a><span data-ttu-id="daa4f-146">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="daa4f-146">Additional resources</span></span>
--------

[<span data-ttu-id="daa4f-147">Oversikt over produktkonfigurasjonsmodeller</span><span class="sxs-lookup"><span data-stu-id="daa4f-147">Product configuration models overview</span></span>](product-configuration-models.md)



