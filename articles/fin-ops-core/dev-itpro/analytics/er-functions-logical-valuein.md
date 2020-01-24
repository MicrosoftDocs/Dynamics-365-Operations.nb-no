---
title: VALUEIN ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen VALUEIN.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cb9a387c8b68d0da4dd485116089f1cf4c5ab72c
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915976"
---
# <span data-ttu-id="b83ff-103"><a name="VALUEIN">VALUEIN ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="b83ff-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b83ff-104">`VALUEIN`-funksjonen bestemmer om de angitte inndataene samsvarer med en verdi for et angitt element i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="b83ff-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="b83ff-105">Den returnerer en *boolsk* verdi av **SANN** hvis de angitte inndataene samsvarer med resultatet av å kjøre det angitte uttrykket for minst én post i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="b83ff-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="b83ff-106">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="b83ff-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="b83ff-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b83ff-107">Syntax</span></span>

```
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="b83ff-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="b83ff-108">Arguments</span></span>

<span data-ttu-id="b83ff-109">`input`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="b83ff-109">`input`: *Field*</span></span>

<span data-ttu-id="b83ff-110">Den gyldige banen til et element i en datakilde i *Postliste*-typen.</span><span class="sxs-lookup"><span data-stu-id="b83ff-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="b83ff-111">Verdien for dette elementet samsvares.</span><span class="sxs-lookup"><span data-stu-id="b83ff-111">The value of this item will be matched.</span></span>

<span data-ttu-id="b83ff-112">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="b83ff-112">`list`: *Record list*</span></span>

<span data-ttu-id="b83ff-113">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="b83ff-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="b83ff-114">`list item expression`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="b83ff-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="b83ff-115">Et gyldig betingelsesuttrykk som enten henviser til eller inneholder ett enkelt felt i den angitte listen som skal brukes for den samsvarende.</span><span class="sxs-lookup"><span data-stu-id="b83ff-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="b83ff-116">Returverdier</span><span class="sxs-lookup"><span data-stu-id="b83ff-116">Return values</span></span>

<span data-ttu-id="b83ff-117">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="b83ff-117">*Boolean*</span></span>

<span data-ttu-id="b83ff-118">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="b83ff-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="b83ff-119">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="b83ff-119">Usage notes</span></span>

<span data-ttu-id="b83ff-120">Generelt oversettes `VALUEIN`-funksjonen til et sett med **OR**-betingelser.</span><span class="sxs-lookup"><span data-stu-id="b83ff-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span>

```
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="b83ff-121">I noen tilfeller kan den oversettes til en database SQL-setning ved hjelp av `EXISTS JOIN`-operatoren.</span><span class="sxs-lookup"><span data-stu-id="b83ff-121">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="b83ff-122">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="b83ff-122">Example 1</span></span>

<span data-ttu-id="b83ff-123">Du definerer **Liste**-datakilden for *Beregnet felt*-typen i modelltilordningen.</span><span class="sxs-lookup"><span data-stu-id="b83ff-123">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b83ff-124">Denne datakilden inneholder uttrykket `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="b83ff-124">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="b83ff-125">Når en datakilde kalles og den er konfigurert som `VALUEIN ("B", List, List.Value)`-uttrykket, returneres **SANN**.</span><span class="sxs-lookup"><span data-stu-id="b83ff-125">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="b83ff-126">I dette tilfellet oversettes `VALUEIN` -funksjonen til følgende sett med betingelser: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, der `("B" = "b")` er lik **SANN**.</span><span class="sxs-lookup"><span data-stu-id="b83ff-126">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="b83ff-127">Når en datakilde kalles og den er konfigurert som `VALUEIN ("B", List, LEFT(List.Value, 0))`-uttrykket, returneres **USANN**.</span><span class="sxs-lookup"><span data-stu-id="b83ff-127">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="b83ff-128">I dette tilfellet oversettes `VALUEIN`-funksjonen til følgende betingelse: `("B" = "")`, som ikke er lik **SANN**.</span><span class="sxs-lookup"><span data-stu-id="b83ff-128">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="b83ff-129">Den øvre grensen for antall tegn i teksten i en slik betingelse er 32 768 tegn.</span><span class="sxs-lookup"><span data-stu-id="b83ff-129">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="b83ff-130">Du bør derfor ikke opprette datakilder som kan overstige denne grensen ved kjøretid.</span><span class="sxs-lookup"><span data-stu-id="b83ff-130">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="b83ff-131">Hvis grensen overskrides, slutter programmet å kjøre, og et unntak blir registrert.</span><span class="sxs-lookup"><span data-stu-id="b83ff-131">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="b83ff-132">Denne situasjonen kan for eksempel oppstå hvis datakilden er konfigurert som `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, og **List1** og **List2**-listene inneholder et stort antall poster.</span><span class="sxs-lookup"><span data-stu-id="b83ff-132">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="b83ff-133">I noen tilfeller kan `VALUEIN`-funksjonen oversettes til en databasesetning ved hjelp av `EXISTS JOIN`-operatoren.</span><span class="sxs-lookup"><span data-stu-id="b83ff-133">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="b83ff-134">Denne virkemåter skjer når [FILTER](er-functions-list-filter.md)-funksjonen brukes og følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="b83ff-134">This behavior occurs when the [FILTER](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="b83ff-135">**BE OM SPØRRING**-valget er deaktivert for datakilden for `VALUEIN`-funksjonen som refererer til listen over poster.</span><span class="sxs-lookup"><span data-stu-id="b83ff-135">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="b83ff-136">Ingen flere betingelser brukes på denne datakilden ved kjøretid.</span><span class="sxs-lookup"><span data-stu-id="b83ff-136">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="b83ff-137">Ingen nestede uttrykk konfigureres for datakilden for `VALUEIN`-funksjonen som refererer til listen over poster.</span><span class="sxs-lookup"><span data-stu-id="b83ff-137">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="b83ff-138">Et listeelement for `VALUEIN`-funksjonen refererer til et felt for den angitte datatypen, ikke til et uttrykk eller en metode for datakilden.</span><span class="sxs-lookup"><span data-stu-id="b83ff-138">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="b83ff-139">Vurder å bruke dette alternativet i stedet for [WHERE](er-functions-list-where.md)-funksjonen som er beskrevet tidligere i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="b83ff-139">Consider using this option instead of the [WHERE](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="b83ff-140">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="b83ff-140">Example 2</span></span>

<span data-ttu-id="b83ff-141">Du definerer de følgende datakildene i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="b83ff-141">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="b83ff-142">**I**-datakilden for *Tabellposter*-typen.</span><span class="sxs-lookup"><span data-stu-id="b83ff-142">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="b83ff-143">Denne datakilden refererer til Intrastat-tabellen.</span><span class="sxs-lookup"><span data-stu-id="b83ff-143">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="b83ff-144">**Port**-datakilden for *Tabellposter*-typen.</span><span class="sxs-lookup"><span data-stu-id="b83ff-144">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="b83ff-145">Denne datakilden refererer til IntrastatPort-tabellen.</span><span class="sxs-lookup"><span data-stu-id="b83ff-145">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="b83ff-146">Når en datakilde kalles opp som er konfigurert som uttrykket `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, genereres følgende SQL-setning for å returnere filtrerte poster i Intrastat-tabellen.</span><span class="sxs-lookup"><span data-stu-id="b83ff-146">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="b83ff-147">For **dataAreaId**-feltene genereres den endelige SQL-setningen ved hjelp av `IN`-operatoren.</span><span class="sxs-lookup"><span data-stu-id="b83ff-147">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="b83ff-148">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="b83ff-148">Example 3</span></span>

<span data-ttu-id="b83ff-149">Du definerer de følgende datakildene i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="b83ff-149">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="b83ff-150">**Le**-datakilden for *Beregnet felt*-typen.</span><span class="sxs-lookup"><span data-stu-id="b83ff-150">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="b83ff-151">Denne datakilden inneholder uttrykket `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="b83ff-151">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="b83ff-152">**I**-datakilden for *Tabellposter*-typen.</span><span class="sxs-lookup"><span data-stu-id="b83ff-152">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="b83ff-153">Denne datakilden refererer til Intrastat-tabellen, og alternativet **Kryssfirma** er aktivert for den.</span><span class="sxs-lookup"><span data-stu-id="b83ff-153">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="b83ff-154">Når en datakilde kalles opp som er konfigurert som uttrykket `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, inneholder den endelige SQL-setningen følgende betingelse.</span><span class="sxs-lookup"><span data-stu-id="b83ff-154">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="b83ff-155">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b83ff-155">Additional resources</span></span>

[<span data-ttu-id="b83ff-156">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="b83ff-156">Logical functions</span></span>](er-functions-category-logical.md)
