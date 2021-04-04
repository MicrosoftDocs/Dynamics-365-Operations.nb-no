---
title: ISOCREDREF ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ISOCREDREF.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: a9378028a4b308aae7796b861b37a5f89ddfe49c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563419"
---
# <a name="isocredref-er-function"></a><span data-ttu-id="e5e40-103">ISOCREDREF ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="e5e40-103">ISOCREDREF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e5e40-104">`ISOCREDREF`-funksjonen returnerer en *streng*-verdi som representerer en ISO-kreditorreferanse (International Organization for Standardization) basert på sifrene og de alfabetiske symbolene i det angitte fakturanummeret.</span><span class="sxs-lookup"><span data-stu-id="e5e40-104">The `ISOCREDREF` function returns a *String* value that represents an International Organization for Standardization (ISO) creditor reference, based on the digits and alphabetic symbols of the specified invoice number.</span></span>

## <a name="syntax"></a><span data-ttu-id="e5e40-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="e5e40-105">Syntax</span></span>

```vb
ISOCREDREF (invoice number digits)
```

## <a name="arguments"></a><span data-ttu-id="e5e40-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="e5e40-106">Arguments</span></span>

<span data-ttu-id="e5e40-107">`invoice number digits`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="e5e40-107">`invoice number digits`: *String*</span></span>

<span data-ttu-id="e5e40-108">En tekstverdi som representerer sifrene i et fakturanummer.</span><span class="sxs-lookup"><span data-stu-id="e5e40-108">A text value that represents the digits of an invoice number.</span></span>

## <a name="return-values"></a><span data-ttu-id="e5e40-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="e5e40-109">Return values</span></span>

<span data-ttu-id="e5e40-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="e5e40-110">*String*</span></span>

<span data-ttu-id="e5e40-111">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="e5e40-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e5e40-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="e5e40-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="e5e40-113">`invoice number digits`-argumentet må oversettes før det sendes til denne funksjonen for å eliminere symboler fra bokstaver som ikke er ISO-kompatible.</span><span class="sxs-lookup"><span data-stu-id="e5e40-113">To eliminate symbols from alphabets that are't ISO-compliant, the `invoice number digits` argument must be translated before it's passed to this function.</span></span>

## <a name="example"></a><span data-ttu-id="e5e40-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e5e40-114">Example</span></span>

<span data-ttu-id="e5e40-115">`ISOCredRef ("VEND-200002")` returnerer **"RF23VEND-200002"**.</span><span class="sxs-lookup"><span data-stu-id="e5e40-115">`ISOCredRef ("VEND-200002")` returns **"RF23VEND-200002"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e5e40-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e5e40-116">Additional resources</span></span>

[<span data-ttu-id="e5e40-117">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="e5e40-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]