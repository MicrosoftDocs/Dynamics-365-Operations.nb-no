---
title: ALLITEMSQUERY ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ALLITEMSQUERY.
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
ms.openlocfilehash: 37546fccf804a4522638147d39206997e8c0c24c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745375"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="1fef0-103">ALLITEMSQUERY ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="1fef0-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1fef0-104">`ALLITEMSQUERY`-funksjonen kjøres som en koblet SQL-spørring.</span><span class="sxs-lookup"><span data-stu-id="1fef0-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="1fef0-105">Den returnerer en ny *Postliste*-verdi som er flatet ut, og består av en liste over poster som representerer alle elementer som samsvarer med den angitte banen.</span><span class="sxs-lookup"><span data-stu-id="1fef0-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="1fef0-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="1fef0-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="1fef0-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="1fef0-107">Arguments</span></span>

<span data-ttu-id="1fef0-108">`path`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="1fef0-108">`path`: *Record list*</span></span>

<span data-ttu-id="1fef0-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="1fef0-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="1fef0-110">Den må inneholde minst én relasjon.</span><span class="sxs-lookup"><span data-stu-id="1fef0-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="1fef0-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="1fef0-111">Return values</span></span>

<span data-ttu-id="1fef0-112">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="1fef0-112">*Record list*</span></span>

<span data-ttu-id="1fef0-113">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="1fef0-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1fef0-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="1fef0-114">Usage notes</span></span>

<span data-ttu-id="1fef0-115">Den angitte banen må defineres som en gyldig datakildebane til et datakildeelement av datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="1fef0-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="1fef0-116">Den må også inneholde minst én relasjon.</span><span class="sxs-lookup"><span data-stu-id="1fef0-116">It must also contain at least one relation.</span></span> <span data-ttu-id="1fef0-117">Dataelementer som banens *streng* og *dato* skal føre til en feil i ER-uttrykksverktøyet under utformingen.</span><span class="sxs-lookup"><span data-stu-id="1fef0-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="1fef0-118">Når denne funksjonen brukes på datakilder av datatypen *postliste* som refererer til et programobjekt som kan kalles direkte ved hjelp av SQL (for eksempel en tabell, enhet eller spørring), kjøres den som en sammenkoblet SQL-spørring.</span><span class="sxs-lookup"><span data-stu-id="1fef0-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="1fef0-119">Hvis ikke kjører den i minnet som [ALLITEMS](er-functions-list-allitems.md)-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="1fef0-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="1fef0-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="1fef0-120">Example</span></span>

<span data-ttu-id="1fef0-121">Du definerer de følgende datakildene i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="1fef0-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="1fef0-122">En **CustInv**-datakilde av *Tabellposter*-typen som refererer til tabellen CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="1fef0-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="1fef0-123">En **FilteredInv**-datakilde av *Beregnet felt*-typen som inneholder uttrykket `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="1fef0-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="1fef0-124">En **JourLines**-datakilde av *Beregnet felt*-typen som inneholder uttrykket `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="1fef0-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="1fef0-125">Når du kjører modelltilordningen for å kalle **JourLines**-datakilden, kjøres følgende SQL-setning:</span><span class="sxs-lookup"><span data-stu-id="1fef0-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="1fef0-126">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1fef0-126">Additional resources</span></span>

[<span data-ttu-id="1fef0-127">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="1fef0-127">List functions</span></span>](er-functions-category-list.md)
