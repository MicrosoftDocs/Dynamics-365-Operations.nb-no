---
title: RIGHT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen RIGHT.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 13884182cb986564e81f310993747997341ffc07
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682948"
---
# <a name="right-er-function"></a><span data-ttu-id="5827d-103">RIGHT ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="5827d-103">RIGHT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5827d-104">`RIGHT`-funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra slutten av den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="5827d-104">The `RIGHT` function returns a *String* value that presents the specified number of characters from the end of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="5827d-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="5827d-105">Syntax</span></span>

```vb
RIGHT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="5827d-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="5827d-106">Arguments</span></span>

<span data-ttu-id="5827d-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="5827d-107">`text`: *String*</span></span>

<span data-ttu-id="5827d-108">En *streng*-verdi som representerer den opprinnelige teksten.</span><span class="sxs-lookup"><span data-stu-id="5827d-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="5827d-109">`number`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="5827d-109">`number`: *Integer*</span></span>

<span data-ttu-id="5827d-110">Antall tegn som må returneres fra slutten av den opprinnelige teksten.</span><span class="sxs-lookup"><span data-stu-id="5827d-110">The number of characters that must be returned from the end of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="5827d-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="5827d-111">Return values</span></span>

<span data-ttu-id="5827d-112">*Streng*</span><span class="sxs-lookup"><span data-stu-id="5827d-112">*String*</span></span>

<span data-ttu-id="5827d-113">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="5827d-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="5827d-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="5827d-114">Example</span></span>

<span data-ttu-id="5827d-115">`RIGHT ("Sample", 3)` returnerer **"ple"**.</span><span class="sxs-lookup"><span data-stu-id="5827d-115">`RIGHT ("Sample", 3)` returns **"ple"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5827d-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="5827d-116">Additional resources</span></span>

[<span data-ttu-id="5827d-117">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="5827d-117">Text functions</span></span>](er-functions-category-text.md)
