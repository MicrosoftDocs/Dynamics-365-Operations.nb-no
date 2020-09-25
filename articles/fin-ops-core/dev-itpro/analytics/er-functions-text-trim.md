---
title: TRIM ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen TRIM
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a1f7999ccbcd167280cca1abc48377c36d2bc15f
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744221"
---
# <a name="trim-er-function"></a><span data-ttu-id="85bcc-103">TRIM ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="85bcc-103">TRIM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="85bcc-104">`TRIM`-funksjonen returnerer den angitte tekststrengen som en *streng*-verdi etter at innledende og etterfølgende mellomrom er avkortet, og når flere mellomrom mellom ord er fjernet.</span><span class="sxs-lookup"><span data-stu-id="85bcc-104">The `TRIM` function returns the specified text string as a *String* value after leading and trailing spaces have been truncated, and after multiple spaces between words have been removed.</span></span>

## <a name="syntax"></a><span data-ttu-id="85bcc-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="85bcc-105">Syntax</span></span>

```vb
TRIM (text )
```

## <a name="arguments"></a><span data-ttu-id="85bcc-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="85bcc-106">Arguments</span></span>

<span data-ttu-id="85bcc-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="85bcc-107">`text`: *String*</span></span>

<span data-ttu-id="85bcc-108">Den gyldige banen til en datakilde av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="85bcc-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="85bcc-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="85bcc-109">Return values</span></span>

<span data-ttu-id="85bcc-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="85bcc-110">*String*</span></span>

<span data-ttu-id="85bcc-111">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="85bcc-111">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="85bcc-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="85bcc-112">Example</span></span>

<span data-ttu-id="85bcc-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returnerer **"Eksempeltekst"**.</span><span class="sxs-lookup"><span data-stu-id="85bcc-113">`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returns **"Sample text"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="85bcc-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="85bcc-114">Additional resources</span></span>

[<span data-ttu-id="85bcc-115">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="85bcc-115">Text functions</span></span>](er-functions-category-text.md)
