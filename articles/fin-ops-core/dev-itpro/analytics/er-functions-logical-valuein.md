---
title: VALUEIN ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen VALUEIN.
author: NickSelin
manager: kfend
ms.date: 08/18/2020
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
ms.openlocfilehash: 44459ae56891a08eb11a6c254f4b4d5652a0e693
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705125"
---
# <a name=""></a><span data-ttu-id="fc96a-103"><a name="VALUEIN">VALUEIN ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="fc96a-103"><a name="VALUEIN">VALUEIN ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fc96a-104">`VALUEIN`-funksjonen bestemmer om de angitte inndataene samsvarer med en verdi for et angitt element i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-104">The `VALUEIN` function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="fc96a-105">Den returnerer en *boolsk* verdi av **SANN** hvis de angitte inndataene samsvarer med resultatet av å kjøre det angitte uttrykket for minst én post i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-105">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="fc96a-106">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="fc96a-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="fc96a-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="fc96a-107">Syntax</span></span>

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="fc96a-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="fc96a-108">Arguments</span></span>

<span data-ttu-id="fc96a-109">`input`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="fc96a-109">`input`: *Field*</span></span>

<span data-ttu-id="fc96a-110">Den gyldige banen til et element i en datakilde i *Postliste*-typen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-110">The valid path of an item of a data source of the *Record list* type.</span></span> <span data-ttu-id="fc96a-111">Verdien for dette elementet samsvares.</span><span class="sxs-lookup"><span data-stu-id="fc96a-111">The value of this item will be matched.</span></span>

<span data-ttu-id="fc96a-112">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="fc96a-112">`list`: *Record list*</span></span>

<span data-ttu-id="fc96a-113">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-113">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="fc96a-114">`list item expression`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="fc96a-114">`list item expression`: *Boolean*</span></span>

<span data-ttu-id="fc96a-115">Et gyldig betingelsesuttrykk som enten henviser til eller inneholder ett enkelt felt i den angitte listen som skal brukes for den samsvarende.</span><span class="sxs-lookup"><span data-stu-id="fc96a-115">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="fc96a-116">Returverdier</span><span class="sxs-lookup"><span data-stu-id="fc96a-116">Return values</span></span>

<span data-ttu-id="fc96a-117">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="fc96a-117">*Boolean*</span></span>

<span data-ttu-id="fc96a-118">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="fc96a-118">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fc96a-119">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="fc96a-119">Usage notes</span></span>

<span data-ttu-id="fc96a-120">Generelt oversettes `VALUEIN`-funksjonen til et sett med **OR**-betingelser.</span><span class="sxs-lookup"><span data-stu-id="fc96a-120">In general, the `VALUEIN` function is translated to a set of **OR** conditions.</span></span> <span data-ttu-id="fc96a-121">Hvis listen over **OR**-betingelser er stor, og den maksimal totale lengde på en SQL-setning kan overstiges, bør du vurdere å bruke [`VALUEINLARGE`](er-functions-logical-valueinlarge.md)-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-121">If the list of **OR** conditions is large and the maximum total length of an SQL statement might be exceeded, consider using the [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) function.</span></span>

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

<span data-ttu-id="fc96a-122">I noen tilfeller kan den oversettes til en database SQL-setning ved hjelp av `EXISTS JOIN`-operatoren.</span><span class="sxs-lookup"><span data-stu-id="fc96a-122">In some cases, it can be translated to a database SQL statement by using the `EXISTS JOIN` operator.</span></span>

## <a name="example-1"></a><span data-ttu-id="fc96a-123">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="fc96a-123">Example 1</span></span>

<span data-ttu-id="fc96a-124">Du definerer **Liste**-datakilden for *Beregnet felt*-typen i modelltilordningen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-124">In your model mapping, you define the **List** data source of the *Calculated field* type.</span></span> <span data-ttu-id="fc96a-125">Denne datakilden inneholder uttrykket `SPLIT ("a,b,c", ",")`.</span><span class="sxs-lookup"><span data-stu-id="fc96a-125">This data source contains the expression `SPLIT ("a,b,c", ",")`.</span></span>

<span data-ttu-id="fc96a-126">Når en datakilde kalles og den er konfigurert som `VALUEIN ("B", List, List.Value)`-uttrykket, returneres **SANN**.</span><span class="sxs-lookup"><span data-stu-id="fc96a-126">When a data source is called, if it has been configured as the `VALUEIN ("B", List, List.Value)` expression, it returns **TRUE**.</span></span> <span data-ttu-id="fc96a-127">I dette tilfellet oversettes `VALUEIN` -funksjonen til følgende sett med betingelser: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, der `("B" = "b")` er lik **SANN**.</span><span class="sxs-lookup"><span data-stu-id="fc96a-127">In this case, the `VALUEIN` function is translated to the following set of conditions: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, where `("B" = "b")` equals **TRUE**.</span></span>

<span data-ttu-id="fc96a-128">Når en datakilde kalles og den er konfigurert som `VALUEIN ("B", List, LEFT(List.Value, 0))`-uttrykket, returneres **USANN**.</span><span class="sxs-lookup"><span data-stu-id="fc96a-128">When a data source is called, if it has been configured as the `VALUEIN ("B", List, LEFT(List.Value, 0))` expression, it returns **FALSE**.</span></span> <span data-ttu-id="fc96a-129">I dette tilfellet oversettes `VALUEIN`-funksjonen til følgende betingelse: `("B" = "")`, som ikke er lik **SANN**.</span><span class="sxs-lookup"><span data-stu-id="fc96a-129">In this case, the `VALUEIN` function is translated to the following condition: `("B" = "")`, which doesn't equal **TRUE**.</span></span>

<span data-ttu-id="fc96a-130">Den øvre grensen for antall tegn i teksten i en slik betingelse er 32 768 tegn.</span><span class="sxs-lookup"><span data-stu-id="fc96a-130">The upper limit for the number of characters in the text of such a condition is 32,768 characters.</span></span> <span data-ttu-id="fc96a-131">Du bør derfor ikke opprette datakilder som kan overstige denne grensen ved kjøretid.</span><span class="sxs-lookup"><span data-stu-id="fc96a-131">Therefore, you should not create data sources that might exceed this limit at runtime.</span></span> <span data-ttu-id="fc96a-132">Hvis grensen overskrides, slutter programmet å kjøre, og et unntak blir registrert.</span><span class="sxs-lookup"><span data-stu-id="fc96a-132">If the limit is exceeded, the application stops running, and an exception is thrown.</span></span> <span data-ttu-id="fc96a-133">Denne situasjonen kan for eksempel oppstå hvis datakilden er konfigurert som `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, og **List1** og **List2**-listene inneholder et stort antall poster.</span><span class="sxs-lookup"><span data-stu-id="fc96a-133">For example, this situation can occur if the data source is configured as `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, and the **List1** and **List2** lists contain a large volume of records.</span></span>

<span data-ttu-id="fc96a-134">I noen tilfeller kan `VALUEIN`-funksjonen oversettes til en databasesetning ved hjelp av `EXISTS JOIN`-operatoren.</span><span class="sxs-lookup"><span data-stu-id="fc96a-134">In some cases, the `VALUEIN` function is translated to a database statement by using the `EXISTS JOIN` operator.</span></span> <span data-ttu-id="fc96a-135">Denne virkemåter skjer når [`FILTER`](er-functions-list-filter.md)-funksjonen brukes og følgende betingelser er oppfylt:</span><span class="sxs-lookup"><span data-stu-id="fc96a-135">This behavior occurs when the [`FILTER`](er-functions-list-filter.md) function is used and the following conditions are met:</span></span>

- <span data-ttu-id="fc96a-136">**BE OM SPØRRING**-valget er deaktivert for datakilden for `VALUEIN`-funksjonen som refererer til listen over poster.</span><span class="sxs-lookup"><span data-stu-id="fc96a-136">The **ASK FOR QUERY** option is turned off for the data source of the `VALUEIN` function that refers to the list of records.</span></span> <span data-ttu-id="fc96a-137">Ingen flere betingelser brukes på denne datakilden ved kjøretid.</span><span class="sxs-lookup"><span data-stu-id="fc96a-137">No additional conditions will be applied to this data source at runtime.</span></span>
- <span data-ttu-id="fc96a-138">Ingen nestede uttrykk konfigureres for datakilden for `VALUEIN`-funksjonen som refererer til listen over poster.</span><span class="sxs-lookup"><span data-stu-id="fc96a-138">No nested expressions are configured for the data source of the `VALUEIN` function that refers to the list of records.</span></span>
- <span data-ttu-id="fc96a-139">Et listeelement for `VALUEIN`-funksjonen refererer til et felt for den angitte datatypen, ikke til et uttrykk eller en metode for datakilden.</span><span class="sxs-lookup"><span data-stu-id="fc96a-139">A list item of the `VALUEIN` function refers to a field of the specified data source, not to an expression or method of that data source.</span></span>

<span data-ttu-id="fc96a-140">Vurder å bruke dette alternativet i stedet for [`WHERE`](er-functions-list-where.md)-funksjonen som er beskrevet tidligere i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="fc96a-140">Consider using this option instead of the [`WHERE`](er-functions-list-where.md) function that is described earlier in this example.</span></span>

## <a name="example-2"></a><span data-ttu-id="fc96a-141">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="fc96a-141">Example 2</span></span>

<span data-ttu-id="fc96a-142">Du definerer de følgende datakildene i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="fc96a-142">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="fc96a-143">**I**-datakilden for *Tabellposter*-typen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-143">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="fc96a-144">Denne datakilden refererer til Intrastat-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-144">This data source refers to the Intrastat table.</span></span>
- <span data-ttu-id="fc96a-145">**Port**-datakilden for *Tabellposter*-typen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-145">The **Port** data source of the *Table records* type.</span></span> <span data-ttu-id="fc96a-146">Denne datakilden refererer til IntrastatPort-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-146">This data source refers to the IntrastatPort table.</span></span>

<span data-ttu-id="fc96a-147">Når en datakilde kalles opp som er konfigurert som uttrykket `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, genereres følgende SQL-setning for å returnere filtrerte poster i Intrastat-tabellen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-147">When a data source is called that has been configured as the `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)` expression, the following SQL statement is generated to return filtered records of the Intrastat table.</span></span>

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

<span data-ttu-id="fc96a-148">For **dataAreaId**-feltene genereres den endelige SQL-setningen ved hjelp av `IN`-operatoren.</span><span class="sxs-lookup"><span data-stu-id="fc96a-148">For **dataAreaId** fields, the final SQL statement is generated by the using `IN` operator.</span></span>

## <a name="example-3"></a><span data-ttu-id="fc96a-149">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="fc96a-149">Example 3</span></span>

<span data-ttu-id="fc96a-150">Du definerer de følgende datakildene i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="fc96a-150">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="fc96a-151">**Le**-datakilden for *Beregnet felt*-typen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-151">The **Le** data source of the *Calculated field* type.</span></span> <span data-ttu-id="fc96a-152">Denne datakilden inneholder uttrykket `SPLIT ("DEMF,GBSI,USMF", ",")`.</span><span class="sxs-lookup"><span data-stu-id="fc96a-152">This data source contains the expression `SPLIT ("DEMF,GBSI,USMF", ",")`.</span></span>
- <span data-ttu-id="fc96a-153">**I**-datakilden for *Tabellposter*-typen.</span><span class="sxs-lookup"><span data-stu-id="fc96a-153">The **In** data source of the *Table records* type.</span></span> <span data-ttu-id="fc96a-154">Denne datakilden refererer til Intrastat-tabellen, og alternativet **Kryssfirma** er aktivert for den.</span><span class="sxs-lookup"><span data-stu-id="fc96a-154">This data source refers to the Intrastat table, and the **Cross-company** option is turned on for it.</span></span>

<span data-ttu-id="fc96a-155">Når en datakilde kalles opp som er konfigurert som uttrykket `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, inneholder den endelige SQL-setningen følgende betingelse.</span><span class="sxs-lookup"><span data-stu-id="fc96a-155">When a data source is called that has been configured as the `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)` expression, the final SQL statement contains the following condition.</span></span>

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a><span data-ttu-id="fc96a-156">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fc96a-156">Additional resources</span></span>

[<span data-ttu-id="fc96a-157">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="fc96a-157">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="fc96a-158">VALUEINLARGE-funksjoner</span><span class="sxs-lookup"><span data-stu-id="fc96a-158">VALUEINLARGE functions</span></span>](er-functions-logical-valueinlarge.md)
