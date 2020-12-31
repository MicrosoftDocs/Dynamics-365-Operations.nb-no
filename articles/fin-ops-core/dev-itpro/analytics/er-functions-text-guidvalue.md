---
title: GUIDVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen GUIDVALUE.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eb6f301cf7a39208aa23337401a9684fb5b3a73d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685961"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="4cfb2-103">GUIDVALUE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="4cfb2-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4cfb2-104">`GUIDVALUE`-funksjonen konverterer de angitte inndataene for *Streng*-datatypen til et dataelement av *GUID*-typen.</span><span class="sxs-lookup"><span data-stu-id="4cfb2-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="4cfb2-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="4cfb2-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="4cfb2-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="4cfb2-106">Arguments</span></span>

<span data-ttu-id="4cfb2-107">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="4cfb2-107">`input`: *String*</span></span>

<span data-ttu-id="4cfb2-108">Den gyldige banen til en datakilde av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="4cfb2-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4cfb2-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="4cfb2-109">Return values</span></span>

<span data-ttu-id="4cfb2-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4cfb2-110">*GUID*</span></span>

<span data-ttu-id="4cfb2-111">Den resulterende GUID-verdien (globalt unik identifikator).</span><span class="sxs-lookup"><span data-stu-id="4cfb2-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4cfb2-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="4cfb2-112">Usage notes</span></span>

<span data-ttu-id="4cfb2-113">For å konvertere i motsatt retning (det vil si å konvertere angitt inndata av *GUID*-datatypen til et dataelement av *String*-datatypen), kan du bruke funksjonen [TEXT](er-functions-text-text.md).</span><span class="sxs-lookup"><span data-stu-id="4cfb2-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="4cfb2-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4cfb2-114">Example</span></span>

<span data-ttu-id="4cfb2-115">Du definerer de følgende datakildene i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="4cfb2-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="4cfb2-116">En **myID**-datakilde av *Beregnet felt*-typen som inneholder uttrykket `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="4cfb2-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="4cfb2-117">En **Brukere**-datakilde av *Tabellposter*-typen som refererer til tabellen UserInfo</span><span class="sxs-lookup"><span data-stu-id="4cfb2-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="4cfb2-118">Du kan deretter bruke et uttrykk, for eksempel `FILTER (Users, Users.objectId = myID)`, til å filtrere UserInfo-tabellen etter **objectId**-feltet for *GUID*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="4cfb2-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4cfb2-119">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4cfb2-119">Additional resources</span></span>

[<span data-ttu-id="4cfb2-120">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="4cfb2-120">Text functions</span></span>](er-functions-category-text.md)
