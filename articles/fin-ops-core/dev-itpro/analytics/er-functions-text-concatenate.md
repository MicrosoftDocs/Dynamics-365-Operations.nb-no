---
title: CONCATENATE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CONCATENATE.
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
ms.openlocfilehash: f1a47a05127412588f4628cb425eab0379493c3c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746488"
---
# <a name="concatenate-er-function"></a><span data-ttu-id="553ec-103">CONCATENATE ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="553ec-103">CONCATENATE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="553ec-104">`CONCATENATE`-funksjonen returnerer alle de angitte tekststrengene som en *streng*-verdi etter at de er føyd sammen til én streng.</span><span class="sxs-lookup"><span data-stu-id="553ec-104">The `CONCATENATE` function returns all the specified text strings as a *String* value after they have been joined into one string.</span></span>

## <a name="syntax"></a><span data-ttu-id="553ec-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="553ec-105">Syntax</span></span>

```vb
CONCATENATE (text 1[, text 2, …, text N])
```

## <a name="arguments"></a><span data-ttu-id="553ec-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="553ec-106">Arguments</span></span>

<span data-ttu-id="553ec-107">`text 1`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="553ec-107">`text 1`: *String*</span></span>

<span data-ttu-id="553ec-108">En referanse til en datakilde for *Streng*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="553ec-108">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="553ec-109">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="553ec-109">This argument is required.</span></span>

<span data-ttu-id="553ec-110">`text N`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="553ec-110">`text N`: *String*</span></span>

<span data-ttu-id="553ec-111">En referanse til en datakilde for *Streng*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="553ec-111">A reference to a data source of the *String* data type.</span></span> <span data-ttu-id="553ec-112">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="553ec-112">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="553ec-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="553ec-113">Return values</span></span>

<span data-ttu-id="553ec-114">*Streng*</span><span class="sxs-lookup"><span data-stu-id="553ec-114">*String*</span></span>

<span data-ttu-id="553ec-115">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="553ec-115">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="553ec-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="553ec-116">Example</span></span>

<span data-ttu-id="553ec-117">`CONCATENATE ("abc", "def")` returnerer **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="553ec-117">`CONCATENATE ("abc", "def")` returns **"abcdef"**.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="553ec-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="553ec-118">Usage notes</span></span>

<span data-ttu-id="553ec-119">Uttrykket `"abc" & "def"` returnerer også **"abcdef"**.</span><span class="sxs-lookup"><span data-stu-id="553ec-119">The expression `"abc" & "def"` also returns **"abcdef"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="553ec-120">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="553ec-120">Additional resources</span></span>

[<span data-ttu-id="553ec-121">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="553ec-121">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]