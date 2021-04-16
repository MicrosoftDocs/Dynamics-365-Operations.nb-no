---
title: ALLITEMSQUERY ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ALLITEMSQUERY.
author: NickSelin
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
ms.openlocfilehash: 7995b497a2bd95d4aec9ae6d5f1c3cb790823ea0
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746705"
---
# <a name="allitemsquery-er-function"></a><span data-ttu-id="550a3-103">ALLITEMSQUERY ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="550a3-103">ALLITEMSQUERY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="550a3-104">`ALLITEMSQUERY`-funksjonen kjøres som en koblet SQL-spørring.</span><span class="sxs-lookup"><span data-stu-id="550a3-104">The `ALLITEMSQUERY` function runs as a joined SQL query.</span></span> <span data-ttu-id="550a3-105">Den returnerer en ny *Postliste*-verdi som er flatet ut, og består av en liste over poster som representerer alle elementer som samsvarer med den angitte banen.</span><span class="sxs-lookup"><span data-stu-id="550a3-105">It returns a new flattened *Record list* value that consists of a list of records that represent all items that match the specified path.</span></span>

## <a name="syntax"></a><span data-ttu-id="550a3-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="550a3-106">Syntax</span></span>

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a><span data-ttu-id="550a3-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="550a3-107">Arguments</span></span>

<span data-ttu-id="550a3-108">`path`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="550a3-108">`path`: *Record list*</span></span>

<span data-ttu-id="550a3-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="550a3-109">The valid path of a data source of the *Record list* data type.</span></span> <span data-ttu-id="550a3-110">Den må inneholde minst én relasjon.</span><span class="sxs-lookup"><span data-stu-id="550a3-110">It must contain at least one relation.</span></span>

## <a name="return-values"></a><span data-ttu-id="550a3-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="550a3-111">Return values</span></span>

<span data-ttu-id="550a3-112">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="550a3-112">*Record list*</span></span>

<span data-ttu-id="550a3-113">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="550a3-113">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="550a3-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="550a3-114">Usage notes</span></span>

<span data-ttu-id="550a3-115">Den angitte banen må defineres som en gyldig datakildebane til et datakildeelement av datatypen *Postliste*.</span><span class="sxs-lookup"><span data-stu-id="550a3-115">The specified path must be defined as a valid data source path of a data source element of the *Record list* data type.</span></span> <span data-ttu-id="550a3-116">Den må også inneholde minst én relasjon.</span><span class="sxs-lookup"><span data-stu-id="550a3-116">It must also contain at least one relation.</span></span> <span data-ttu-id="550a3-117">Dataelementer som banens *streng* og *dato* skal føre til en feil i ER-uttrykksverktøyet under utformingen.</span><span class="sxs-lookup"><span data-stu-id="550a3-117">Data elements such as the path *String* and *Date* should raise an error in the Electronic reporting (ER) expression builder at design time.</span></span>

<span data-ttu-id="550a3-118">Når denne funksjonen brukes på datakilder av datatypen *postliste* som refererer til et programobjekt som kan kalles direkte ved hjelp av SQL (for eksempel en tabell, enhet eller spørring), kjøres den som en sammenkoblet SQL-spørring.</span><span class="sxs-lookup"><span data-stu-id="550a3-118">When this function is applied to data sources of the *Record list* data type that refer to an application object that can be directly called by using SQL (for example, an table, entity, or query), it runs as a joined SQL query.</span></span> <span data-ttu-id="550a3-119">Hvis ikke kjører den i minnet som [ALLITEMS](er-functions-list-allitems.md)-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="550a3-119">Otherwise, it runs in memory as the [ALLITEMS](er-functions-list-allitems.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="550a3-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="550a3-120">Example</span></span>

<span data-ttu-id="550a3-121">Du definerer de følgende datakildene i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="550a3-121">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="550a3-122">En **CustInv**-datakilde av *Tabellposter*-typen som refererer til tabellen CustInvoiceTable</span><span class="sxs-lookup"><span data-stu-id="550a3-122">A **CustInv** data source of the *Table records* type that refers to the CustInvoiceTable table</span></span>
- <span data-ttu-id="550a3-123">En **FilteredInv**-datakilde av *Beregnet felt*-typen som inneholder uttrykket `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span><span class="sxs-lookup"><span data-stu-id="550a3-123">A **FilteredInv** data source of the *Calculated field* type that contains the expression `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`</span></span>
- <span data-ttu-id="550a3-124">En **JourLines**-datakilde av *Beregnet felt*-typen som inneholder uttrykket `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span><span class="sxs-lookup"><span data-stu-id="550a3-124">A **JourLines** of the *Calculated field* type that contains the expression `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`</span></span>

<span data-ttu-id="550a3-125">Når du kjører modelltilordningen for å kalle **JourLines**-datakilden, kjøres følgende SQL-setning:</span><span class="sxs-lookup"><span data-stu-id="550a3-125">When you run the model mapping to call the **JourLines** data source, the following SQL statement is run:</span></span>

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a><span data-ttu-id="550a3-126">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="550a3-126">Additional resources</span></span>

[<span data-ttu-id="550a3-127">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="550a3-127">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]