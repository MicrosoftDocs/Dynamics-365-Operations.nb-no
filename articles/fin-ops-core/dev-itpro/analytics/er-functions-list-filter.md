---
title: FILTER ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FILTER.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0e90db1836a93dab42be5dc91e9ea478163a1437
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559705"
---
# <a name="filter-er-function"></a><span data-ttu-id="90e5c-103">FILTER ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="90e5c-103">FILTER ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="90e5c-104">`FILTER`-funksjonen returnerer den angitte listen som en *Postliste*-verdi etter at spørringen er endret, slik at den filtrerer etter den angitte betingelsen.</span><span class="sxs-lookup"><span data-stu-id="90e5c-104">The `FILTER` function returns the specified list as a *Record list* value after the query has been changed so that it filters for the specified condition.</span></span>

## <a name="syntax"></a><span data-ttu-id="90e5c-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="90e5c-105">Syntax</span></span>

```vb
FILTER (list, condition)
```

## <a name="arguments"></a><span data-ttu-id="90e5c-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="90e5c-106">Arguments</span></span>

<span data-ttu-id="90e5c-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="90e5c-107">`list`: *Record list*</span></span>

<span data-ttu-id="90e5c-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="90e5c-108">The valid path of a data source of the *Record list* data type.</span></span>

<span data-ttu-id="90e5c-109">`condition`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="90e5c-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="90e5c-110">Et gyldig betingelsesuttrykk som brukes til å filtrere poster i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="90e5c-110">A valid conditional expression that is used to filter records of the specified list.</span></span>

## <a name="return-values"></a><span data-ttu-id="90e5c-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="90e5c-111">Return values</span></span>

<span data-ttu-id="90e5c-112">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="90e5c-112">*Record list*</span></span>

<span data-ttu-id="90e5c-113">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="90e5c-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="90e5c-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="90e5c-114">Usage notes</span></span>

<span data-ttu-id="90e5c-115">Denne funksjonen er ulik [WHERE](er-functions-list-where.md)-funksjonen fordi den angitte betingelsen brukes på en ER-datakilde av typen *Tabellposter* på databasenivået.</span><span class="sxs-lookup"><span data-stu-id="90e5c-115">This function differs from the [WHERE](er-functions-list-where.md) function, because the specified condition is applied to any Electronic reporting (ER) data source of the *Table records* type at the database level.</span></span> <span data-ttu-id="90e5c-116">Listen og betingelsen kan defineres ved hjelp av tabeller og relasjoner.</span><span class="sxs-lookup"><span data-stu-id="90e5c-116">The list and condition can be defined by using tables and relations.</span></span>

<span data-ttu-id="90e5c-117">Hvis ett av eller begge argumentene som er konfigurert for denne funksjonen (`list` og `condition`), ikke tillater at denne forespørselen skal oversettes til det direkte SQL-kallet, utløses et unntak ved utformingstid.</span><span class="sxs-lookup"><span data-stu-id="90e5c-117">If one or both arguments that are configured for this function (`list` and `condition`) don't allow this request to be translated to the direct SQL call, an exception is thrown at design time.</span></span> <span data-ttu-id="90e5c-118">Dette unntaket informerer brukeren om at enten `list` eller `condition` ikke kan brukes til å spørre databasen.</span><span class="sxs-lookup"><span data-stu-id="90e5c-118">This exception informs the user that either `list` or `condition` can't be used to query the database.</span></span>

## <a name="example-1"></a><span data-ttu-id="90e5c-119">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="90e5c-119">Example 1</span></span>

<span data-ttu-id="90e5c-120">Hvis **Vendor** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, returnerer uttrykket `FILTER (Vendors, Vendors.VendGroup = "40")` en liste over bare leverandører som tilhører leverandørgruppe 40.</span><span class="sxs-lookup"><span data-stu-id="90e5c-120">If **Vendor** is configured as an ER data source that refers to the VendTable table, the expression `FILTER (Vendors, Vendors.VendGroup = "40")` returns a list of only vendors that belong to vendor group 40.</span></span>

## <a name="example-2"></a><span data-ttu-id="90e5c-121">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="90e5c-121">Example 2</span></span>

<span data-ttu-id="90e5c-122">Hvis **Vendor** er konfigurert som en ER-datakilde som refererer til VendTable-tabellen, og **parmVendorBankGroup** er konfigurert som en ER-datakilde som returnerer en verdi av *Streng*-datatypen, returnerer uttrykket `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` en liste over bare leverandørkontoene som tilhører en spesifikk bankgruppe.</span><span class="sxs-lookup"><span data-stu-id="90e5c-122">If **Vendor** is configured as an ER data source that refers to the VendTable table, and if **parmVendorBankGroup** is configured as an ER data source that returns a value of the *String* data type, the expression `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` returns a list of only vendor accounts that belong to a specific bank group.</span></span>

## <a name="example-3"></a><span data-ttu-id="90e5c-123">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="90e5c-123">Example 3</span></span>

<span data-ttu-id="90e5c-124">Du angir datakilde **DS** av *Beregnet felt*-typen som inneholder uttrykket `SPLIT ("A,B,C", ",")`.</span><span class="sxs-lookup"><span data-stu-id="90e5c-124">You enter data source **DS** of the *Calculated field* type, and it contains the expression `SPLIT ("A,B,C", ",")`.</span></span> <span data-ttu-id="90e5c-125">Deretter skriver du inn et annet uttrykk, `FILTER( DS, DS.Value = "B")`.</span><span class="sxs-lookup"><span data-stu-id="90e5c-125">You then enter another expression, `FILTER( DS, DS.Value = "B")`.</span></span> <span data-ttu-id="90e5c-126">Når du prøver å lagre dette uttrykket i ER-formeldesigneren, utløses følgende unntak: "Valideringsfeil: Listeuttrykket for FILTER-funksjonen er ikke søkbart."</span><span class="sxs-lookup"><span data-stu-id="90e5c-126">When you try to save this expression in the ER formula designer, the following exception is thrown: "Validation error: The list expression of FILTER function is not queryable."</span></span>

## <a name="additional-resources"></a><span data-ttu-id="90e5c-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="90e5c-127">Additional resources</span></span>

[<span data-ttu-id="90e5c-128">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="90e5c-128">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]