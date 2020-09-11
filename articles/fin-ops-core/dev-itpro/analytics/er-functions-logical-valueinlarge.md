---
title: VALUEINLARGE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen VALUEINLARGE.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4630ec20e7cbca97c5e43093e6a888a5e09f41a3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705149"
---
# <a name="valueinlarge-er-function"></a><span data-ttu-id="0c9fa-103">VALUEINLARGE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="0c9fa-103">VALUEINLARGE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c9fa-104">`VALUEINLARGE`-funksjonen bestemmer om de angitte inndataene av typen *Int64* eller *Heltall* samsvarer med en verdi for et angitt element i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-104">The `VALUEINLARGE` function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="0c9fa-105">Funksjonen returnerer verdien *boolsk* som **SANN** hvis de angitte inndataene samsvarer med resultatet av å kjøre det angitte uttrykket for minst én post i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-105">The function returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="0c9fa-106">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> <span data-ttu-id="0c9fa-107">For å forstå forskjellen fra `VALUEIN`-funksjonen kan du se i delen [Bruksmerknad](#usage_note) senere i dette emnet.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-107">To understand the difference with the `VALUEIN` function, see the [Usage note](#usage_note) section later in this topic.</span></span>

## <a name="syntax"></a><span data-ttu-id="0c9fa-108">Syntaks</span><span class="sxs-lookup"><span data-stu-id="0c9fa-108">Syntax</span></span>

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a><span data-ttu-id="0c9fa-109">Argumenter</span><span class="sxs-lookup"><span data-stu-id="0c9fa-109">Arguments</span></span>

<span data-ttu-id="0c9fa-110">`input`: *Felt*</span><span class="sxs-lookup"><span data-stu-id="0c9fa-110">`input`: *Field*</span></span>

<span data-ttu-id="0c9fa-111">Den gyldige banen til et datakildeelement av *Postliste*-typen.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-111">The valid path of a data source item of the *Record list* type.</span></span> <span data-ttu-id="0c9fa-112">Verdien for dette elementet samsvares.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-112">The value of this item will be matched.</span></span>

<span data-ttu-id="0c9fa-113">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="0c9fa-113">`list`: *Record list*</span></span>

<span data-ttu-id="0c9fa-114">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-114">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="0c9fa-115">`list item expression`: *Uttrykk*</span><span class="sxs-lookup"><span data-stu-id="0c9fa-115">`list item expression`: *Expression*</span></span>

<span data-ttu-id="0c9fa-116">Et gyldig betingelsesuttrykk som enten henviser til eller inneholder ett enkelt felt i den angitte listen som skal brukes for den samsvarende.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-116">A valid conditional expression that either points to or contains a single field of the specified list that should be used for the matching.</span></span>

## <a name="return-values"></a><span data-ttu-id="0c9fa-117">Returverdier</span><span class="sxs-lookup"><span data-stu-id="0c9fa-117">Return values</span></span>

<span data-ttu-id="0c9fa-118">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="0c9fa-118">*Boolean*</span></span>

<span data-ttu-id="0c9fa-119">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-119">The resulting *Boolean* value.</span></span>

## <a name=""></a><span data-ttu-id="0c9fa-120"><a name="usage_note">Bruksnotater</a></span><span class="sxs-lookup"><span data-stu-id="0c9fa-120"><a name="usage_note">Usage notes</a></span></span>

<span data-ttu-id="0c9fa-121">Når de angitte inndataene representerer en *Int64*- eller *Heltall*-type for et datakildeelement, et kall som kan oversettes til en direkte SQL-setning, konverteres den angitte listen til en midlertidig SQL-tabell, og samsvaret utføres i databasen ved å utføre én enkelt `EXISTS JOIN`-spørring.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-121">When the specified input represents an *Int64* or *Integer* type of a data source item, the call to which is translatable to a direct SQL statement, the specified list is converted to a temporary SQL table and matching is performed in the database by executing a single `EXISTS JOIN` query.</span></span> <span data-ttu-id="0c9fa-122">Hvis ikke fungerer denne funksjonen som [`VALUEIN`](er-functions-logical-valuein.md)-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-122">Otherwise, this function works as the [`VALUEIN`](er-functions-logical-valuein.md) function.</span></span>

<span data-ttu-id="0c9fa-123">Når de angitte inndataene representerer et datakildeelement som er utformet som et annet element enn typen *Int64* og *Heltall*, oppstår det en feil under utformingen der du blir informert om at `VALUEINLARGE`-funksjonen ikke kan brukes for det konfigurerte ER-uttrykket.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-123">When the specified input represents a data source item that is designed as an item other than *Int64* and *Integer* type, an error occurs at design time informing you that the `VALUEINLARGE` function is not applicable for the configured ER expression.</span></span>

<span data-ttu-id="0c9fa-124">Når `VALUEINLARGE`-funksjonsuttrykket kjøres og mer enn én midlertidig tabell brukes i omfanget av denne utførelsen, oppstår det en kjøretidsfeil.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-124">When the `VALUEINLARGE` function expression is executed and more than one temporary table is used in scope of this execution, a runtime error occurs.</span></span>

## <a name="example"></a><span data-ttu-id="0c9fa-125">Eksempel</span><span class="sxs-lookup"><span data-stu-id="0c9fa-125">Example</span></span>

<span data-ttu-id="0c9fa-126">Du definerer de følgende datakildene i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="0c9fa-126">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="0c9fa-127">**I**-datakilden for *Tabellposter*-typen.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-127">The **In** data source of the *Table records* type.</span></span>
    - <span data-ttu-id="0c9fa-128">Denne datakilden refererer til **Intrastat**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-128">This data source refers to the **Intrastat** table.</span></span>
    - <span data-ttu-id="0c9fa-129">Alternativet **Kryssfirma** er satt til **Nei**.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-129">The **Cross-company** option is set to **No**.</span></span>
- <span data-ttu-id="0c9fa-130">**InMemory**-datakilden for *Beregnet felt*-typen.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-130">The **InMemory** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="0c9fa-131">Denne datakilden inneholder uttrykket `WHERE (In, In.Port <> "")`.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-131">This data source contains the expression `WHERE (In, In.Port <> "")`.</span></span>
- <span data-ttu-id="0c9fa-132">**InFiltered**-datakilden for *Beregnet felt*-typen.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-132">The **InFiltered** data source of the *Calculated field* type.</span></span>
    - <span data-ttu-id="0c9fa-133">Denne datakilden inneholder uttrykket `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-133">This data source contains the expression `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.</span></span>

<span data-ttu-id="0c9fa-134">Når datakilden **InFiltered** kalles i konteksten for firmaet **DEMF**, opprettes det en ny midlertidig tabell i programdatabasen, den innsamlede minnelisten for post-ID-koder settes inn i denne tabellen, og følgende SQL-setning genereres for å returnere filtrerte poster for **Intrastat**-tabellen.</span><span class="sxs-lookup"><span data-stu-id="0c9fa-134">When the data source **InFiltered** is called under the context of the company **DEMF**, a new temporary table is created in the application database, the collected in memory list of record identification codes are inserted to this table, and the following SQL statement is generated to return filtered records of the **Intrastat** table.</span></span>

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a><span data-ttu-id="0c9fa-135">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0c9fa-135">Additional resources</span></span>

[<span data-ttu-id="0c9fa-136">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="0c9fa-136">Logical functions</span></span>](er-functions-category-logical.md)

[<span data-ttu-id="0c9fa-137">VALUEIN-funksjonen</span><span class="sxs-lookup"><span data-stu-id="0c9fa-137">VALUEIN functions</span></span>](er-functions-logical-valuein.md)
