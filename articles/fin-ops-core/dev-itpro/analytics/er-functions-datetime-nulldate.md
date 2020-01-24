---
title: NULLDATE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NULLDATE.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 7761342c6759c11591e06fc7c32f0ddd8bef407a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916321"
---
# <span data-ttu-id="2d034-103"><a name="NULLDATE">NULLDATE ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="2d034-103"><a name="NULLDATE">NULLDATE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d034-104">`NULLDATE`-funksjonen returnerer en *dato*-verdi som representerer **null**-datoen (1. januar 1900).</span><span class="sxs-lookup"><span data-stu-id="2d034-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="2d034-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2d034-105">Syntax</span></span>

```
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="2d034-106">Returverdier</span><span class="sxs-lookup"><span data-stu-id="2d034-106">Return values</span></span>

<span data-ttu-id="2d034-107">*Dato*</span><span class="sxs-lookup"><span data-stu-id="2d034-107">*Date*</span></span>

<span data-ttu-id="2d034-108">Den resulterende datoverdien.</span><span class="sxs-lookup"><span data-stu-id="2d034-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="2d034-109">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="2d034-109">Example 1</span></span>

<span data-ttu-id="2d034-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returnerer **null**-datoen, 1. januar 1900, som **"1900-01-01"**, basert på det angitte egendefinerte formatet.</span><span class="sxs-lookup"><span data-stu-id="2d034-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="2d034-111">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="2d034-111">Example 2</span></span>

<span data-ttu-id="2d034-112">Uttrykket `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returnerer **Sann** når verdien i **DocumentDate**-feltet er lik **null**-datoen.</span><span class="sxs-lookup"><span data-stu-id="2d034-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="2d034-113">I dette eksemplet er **Faktura** en ER-datakilde av typen **Finans/tabell-post** og refererer til CustInvoiceJour-tabellen.</span><span class="sxs-lookup"><span data-stu-id="2d034-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d034-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="2d034-114">Additional resources</span></span>

[<span data-ttu-id="2d034-115">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="2d034-115">Date and time functions</span></span>](er-functions-category-datetime.md)
