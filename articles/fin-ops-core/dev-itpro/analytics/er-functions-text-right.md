---
title: RIGHT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen RIGHT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 75255eccf4da468b0946253f7570b1621f905cd7
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570246"
---
# <a name="right-er-function"></a><span data-ttu-id="61f6d-103">RIGHT ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="61f6d-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="61f6d-104">`RIGHT`-funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra slutten av den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="61f6d-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="61f6d-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="61f6d-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="61f6d-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="61f6d-106">Arguments</span></span>

<span data-ttu-id="61f6d-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="61f6d-107">`text`: *String*</span></span>

<span data-ttu-id="61f6d-108">En *streng*-verdi som representerer den opprinnelige teksten.</span><span class="sxs-lookup"><span data-stu-id="61f6d-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="61f6d-109">`number`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="61f6d-109">`number`: *Integer*</span></span>

<span data-ttu-id="61f6d-110">Antall tegn som må returneres fra slutten av den opprinnelige teksten.</span><span class="sxs-lookup"><span data-stu-id="61f6d-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="61f6d-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="61f6d-111">Return values</span></span>

<span data-ttu-id="61f6d-112">*Streng*</span><span class="sxs-lookup"><span data-stu-id="61f6d-112">*String*</span></span>

<span data-ttu-id="61f6d-113">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="61f6d-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="61f6d-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="61f6d-114">Example</span></span>

<span data-ttu-id="61f6d-115">`RIGHT ("Sample", 3)` returnerer **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="61f6d-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="61f6d-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="61f6d-116">Additional resources</span></span>

[<span data-ttu-id="61f6d-117">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="61f6d-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]