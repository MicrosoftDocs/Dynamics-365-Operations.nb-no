---
title: FILTER ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FILTER.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: adeefd08531f59e478efbb45ab294b3bc8216f4c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042165"
---
# <span data-ttu-id="bde09-103"><a name="FILTER">FILTER ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="bde09-103"><a name="FILTER">FILTER ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bde09-104">`FILTER`-funksjonen returnerer den angitte listen som en *Postliste*-verdi etter at spørringen er endret, slik at den filtrerer etter den angitte betingelsen.</span><span class="sxs-lookup"><span data-stu-id="bde09-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="bde09-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="bde09-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="bde09-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="bde09-106">Arguments</span></span>

<span data-ttu-id="bde09-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="bde09-107">`list`: *Record list*</span></span>

<span data-ttu-id="bde09-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="bde09-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="bde09-109">`condition`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="bde09-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="bde09-110">Et gyldig betingelsesuttrykk som brukes til å filtrere poster i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="bde09-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="bde09-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="bde09-111">Return values</span></span>

<span data-ttu-id="bde09-112">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="bde09-112">*Record list*</span></span>

<span data-ttu-id="bde09-113">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="bde09-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bde09-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="bde09-114">Usage notes</span></span>

<span data-ttu-id="bde09-115">Denne funksjonen er ulik [WHERE](er-functions-list-where.md)-funksjonen fordi den angitte betingelsen brukes på en ER-datakilde av typen *Tabellposter* på databasenivået.</span><span class="sxs-lookup"><span data-stu-id="bde09-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="bde09-116">Listen og betingelsen kan defineres ved hjelp av tabeller og relasjoner.</span><span class="sxs-lookup"><span data-stu-id="bde09-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="bde09-117">Hvis ett av eller begge argumentene som er konfigurert for denne funksjonen (`list` og `condition`), ikke tillater at denne forespørselen skal oversettes til det direkte SQL-kallet, utløses et unntak ved utformingstid.</span><span class="sxs-lookup"><span data-stu-id="bde09-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="bde09-118">Dette unntaket informerer brukeren om at enten `list` eller `condition` ikke kan brukes til å spørre databasen.</span><span class="sxs-lookup"><span data-stu-id="bde09-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="bde09-119">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="bde09-119">Example 1</span></span>

<span data-ttu-id="bde09-120">Hvis **Vendor** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer uttrykket `FILTER (Vendors, Vendors.VendGroup = "40")` en liste over bare leverandører som tilhører leverandørgruppe 40.</span><span class="sxs-lookup"><span data-stu-id="bde09-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="bde09-121">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="bde09-121">Example 2</span></span>

<span data-ttu-id="bde09-122">Hvis **Vendor** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, og **parmVendorBankGroup** er konfigurert som en ER-datakilde som returnerer en verdi av *Streng*-datatypen, returnerer uttrykket `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` en liste over bare leverandørkontoene som tilhører en spesifikk bankgruppe.</span><span class="sxs-lookup"><span data-stu-id="bde09-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="bde09-123">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="bde09-123">Example 3</span></span>

<span data-ttu-id="bde09-124">Du angir datakilde **DS** av *Beregnet felt*-typen som inneholder uttrykket `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="bde09-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="bde09-125">Deretter skriver du inn et annet uttrykk, `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="bde09-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="bde09-126">Når du prøver å lagre dette uttrykket i ER-formeldesigneren, utløses følgende unntak: "Valideringsfeil: Listeuttrykket for FILTER-funksjonen er ikke søkbart."</span><span class="sxs-lookup"><span data-stu-id="bde09-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bde09-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bde09-127">Additional resources</span></span>

[<span data-ttu-id="bde09-128">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="bde09-128">List functions</span></span>](er-functions-category-list.md)
