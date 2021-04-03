---
title: GUIDVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen GUIDVALUE.
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
ms.openlocfilehash: 552c6a42dd0e189f2f8404ce5d7f7a68fec1b216
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5564344"
---
# <a name="guidvalue-er-function"></a><span data-ttu-id="84dcf-103">GUIDVALUE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="84dcf-103">GUIDVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84dcf-104">`GUIDVALUE`-funksjonen konverterer de angitte inndataene for *Streng*-datatypen til et dataelement av *GUID*-typen.</span><span class="sxs-lookup"><span data-stu-id="84dcf-104">The `GUIDVALUE` function converts the specified input of the *String* type to a data item of the *GUID* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="84dcf-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="84dcf-105">Syntax</span></span>

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a><span data-ttu-id="84dcf-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="84dcf-106">Arguments</span></span>

<span data-ttu-id="84dcf-107">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="84dcf-107">`input`: *String*</span></span>

<span data-ttu-id="84dcf-108">Den gyldige banen til en datakilde av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="84dcf-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="84dcf-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="84dcf-109">Return values</span></span>

<span data-ttu-id="84dcf-110">*GUID*</span><span class="sxs-lookup"><span data-stu-id="84dcf-110">*GUID*</span></span>

<span data-ttu-id="84dcf-111">Den resulterende GUID-verdien (globalt unik identifikator).</span><span class="sxs-lookup"><span data-stu-id="84dcf-111">The resulting globally unique identifier (GUID) value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="84dcf-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="84dcf-112">Usage notes</span></span>

<span data-ttu-id="84dcf-113">For å konvertere i motsatt retning (det vil si å konvertere angitt inndata av *GUID*-datatypen til et dataelement av *String*-datatypen), kan du bruke funksjonen [TEXT](er-functions-text-text.md).</span><span class="sxs-lookup"><span data-stu-id="84dcf-113">To do a conversion in the opposite direction (that is, to convert specified input of the *GUID* data type to a data item of the *String* data type), you can use the [TEXT](er-functions-text-text.md) function.</span></span>

## <a name="example"></a><span data-ttu-id="84dcf-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="84dcf-114">Example</span></span>

<span data-ttu-id="84dcf-115">Du definerer de følgende datakildene i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="84dcf-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="84dcf-116">En **myID**-datakilde av *Beregnet felt*-typen som inneholder uttrykket `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span><span class="sxs-lookup"><span data-stu-id="84dcf-116">A **myID** data source of the *Calculated field* type that contains the expression `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`</span></span>
- <span data-ttu-id="84dcf-117">En **Brukere**-datakilde av *Tabellposter*-typen som refererer til tabellen UserInfo</span><span class="sxs-lookup"><span data-stu-id="84dcf-117">A **Users** data source of the *Table records* type that refers to the UserInfo table</span></span>

<span data-ttu-id="84dcf-118">Du kan deretter bruke et uttrykk, for eksempel `FILTER (Users, Users.objectId = myID)`, til å filtrere UserInfo-tabellen etter **objectId**-feltet for *GUID*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="84dcf-118">You can then use an expression such as `FILTER (Users, Users.objectId = myID)` to filter the UserInfo table by the **objectId** field of the *GUID* data type.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84dcf-119">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="84dcf-119">Additional resources</span></span>

[<span data-ttu-id="84dcf-120">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="84dcf-120">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]