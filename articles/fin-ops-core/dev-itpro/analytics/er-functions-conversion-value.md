---
title: VALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen VALUE.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 56b32a802674725347ab496d3a09b99c8f04446d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681214"
---
# <a name="value-er-function"></a><span data-ttu-id="3ed2b-103">VALUE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="3ed2b-103">VALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3ed2b-104">`VALUE`-funksjonen returnerer en *reell* verdi som er konvertert fra den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="3ed2b-104">The `VALUE` function returns a *Real* value that is converted from the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ed2b-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="3ed2b-105">Syntax</span></span>

```vb
VALUE (text)
```

## <a name="arguments"></a><span data-ttu-id="3ed2b-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="3ed2b-106">Arguments</span></span>

<span data-ttu-id="3ed2b-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="3ed2b-107">`text`: *String*</span></span>

<span data-ttu-id="3ed2b-108">En strengverdi som må konverteres til en numerisk verdi.</span><span class="sxs-lookup"><span data-stu-id="3ed2b-108">A string value that must be converted to a numeric value.</span></span>

## <a name="return-values"></a><span data-ttu-id="3ed2b-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="3ed2b-109">Return values</span></span>

<span data-ttu-id="3ed2b-110">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="3ed2b-110">*Real*</span></span>

<span data-ttu-id="3ed2b-111">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="3ed2b-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3ed2b-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="3ed2b-112">Usage notes</span></span>

<span data-ttu-id="3ed2b-113">Komma og punktum-tegn (.) regnes som desimalskilletegn, og en foranstilt bindestrek (-) brukes som negativt fortegn.</span><span class="sxs-lookup"><span data-stu-id="3ed2b-113">Commas and dot characters (.) are considered decimal separators, and a leading hyphen (-) is used as a negative sign.</span></span> <span data-ttu-id="3ed2b-114">Det oppstår et unntak under kjøring hvis den angitte strengen inneholder andre ikke-numeriske tegn.</span><span class="sxs-lookup"><span data-stu-id="3ed2b-114">An exception is thrown at runtime if the specified string contains other non-numeric characters.</span></span>

## <a name="example-1"></a><span data-ttu-id="3ed2b-115">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="3ed2b-115">Example 1</span></span>

<span data-ttu-id="3ed2b-116">`VALUE ("1 234,56")` iverksetter et unntak.</span><span class="sxs-lookup"><span data-stu-id="3ed2b-116">`VALUE ("1 234,56")` throws an exception.</span></span>

## <a name="example-2"></a><span data-ttu-id="3ed2b-117">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="3ed2b-117">Example 2</span></span>

<span data-ttu-id="3ed2b-118">`VALUE ("1234,56")` returnerer **1234.56**.</span><span class="sxs-lookup"><span data-stu-id="3ed2b-118">`VALUE ("1234,56")` returns **1234.56**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3ed2b-119">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3ed2b-119">Additional resources</span></span>

[<span data-ttu-id="3ed2b-120">Typekonverteringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="3ed2b-120">Type conversion functions</span></span>](er-functions-category-type-conversion.md)
