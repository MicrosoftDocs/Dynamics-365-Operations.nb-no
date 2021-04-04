---
title: NULLDATE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen NULLDATE.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 79d37247653aa297fdee2c770180916b9a9a5fc5
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563468"
---
# <a name="nulldate-er-function"></a><span data-ttu-id="0a475-103">NULLDATE ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="0a475-103">NULLDATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a475-104">`NULLDATE`-funksjonen returnerer en *dato*-verdi som representerer **null**-datoen (1. januar 1900).</span><span class="sxs-lookup"><span data-stu-id="0a475-104">The `NULLDATE` function returns a *Date* value that represents the **null** date (January 1, 1900).</span></span>

## <a name="syntax"></a><span data-ttu-id="0a475-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="0a475-105">Syntax</span></span>

```vb
NULLDATE () as 
```

## <a name="return-values"></a><span data-ttu-id="0a475-106">Returverdier</span><span class="sxs-lookup"><span data-stu-id="0a475-106">Return values</span></span>

<span data-ttu-id="0a475-107">*Dato*</span><span class="sxs-lookup"><span data-stu-id="0a475-107">*Date*</span></span>

<span data-ttu-id="0a475-108">Den resulterende datoverdien.</span><span class="sxs-lookup"><span data-stu-id="0a475-108">The resulting date value.</span></span>

## <a name="example-1"></a><span data-ttu-id="0a475-109">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="0a475-109">Example 1</span></span>

<span data-ttu-id="0a475-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returnerer **null**-datoen, 1. januar 1900, som **"1900-01-01"**, basert på det angitte egendefinerte formatet.</span><span class="sxs-lookup"><span data-stu-id="0a475-110">`DATEFORMAT (NULLDATE(), "yyyy-MM-dd")` returns the **null** date, January 1, 1900, as **"1900-01-01"**, based on the specified custom format.</span></span>

## <a name="example-2"></a><span data-ttu-id="0a475-111">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="0a475-111">Example 2</span></span>

<span data-ttu-id="0a475-112">Uttrykket `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returnerer **Sann** når verdien i **DocumentDate**-feltet er lik **null**-datoen.</span><span class="sxs-lookup"><span data-stu-id="0a475-112">The expression `IF( Invoice.DocumentDate = NULLDATE(), true, false)` returns **True** when the value of the **DocumentDate** field equals the **null** date.</span></span> <span data-ttu-id="0a475-113">I dette eksemplet er **Faktura** en ER-datakilde av typen **Finans/tabell-post** og refererer til CustInvoiceJour-tabellen.</span><span class="sxs-lookup"><span data-stu-id="0a475-113">In this example, **Invoice** is an Electronic reporting (ER) data source of the **Finance/Table records** type, and it refers to the CustInvoiceJour table.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0a475-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="0a475-114">Additional resources</span></span>

[<span data-ttu-id="0a475-115">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="0a475-115">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]