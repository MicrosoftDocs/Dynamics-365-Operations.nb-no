---
title: LEFT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LEFT
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 112852ab955fdf8de9f78cc93486cc1d5f048517
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743789"
---
# <a name="left-er-function"></a><span data-ttu-id="08346-103">LEFT ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="08346-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="08346-104">`LEFT`-funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra starten av den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="08346-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="08346-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="08346-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="08346-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="08346-106">Arguments</span></span>

<span data-ttu-id="08346-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="08346-107">`text`: *String*</span></span>

<span data-ttu-id="08346-108">En *streng*-verdi som representerer den opprinnelige teksten.</span><span class="sxs-lookup"><span data-stu-id="08346-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="08346-109">`number`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="08346-109">`number`: *Integer*</span></span>

<span data-ttu-id="08346-110">Antall tegn som må returneres fra begynnelsen av den opprinnelige teksten.</span><span class="sxs-lookup"><span data-stu-id="08346-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="08346-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="08346-111">Return values</span></span>

<span data-ttu-id="08346-112">*Streng*</span><span class="sxs-lookup"><span data-stu-id="08346-112">*String*</span></span>

<span data-ttu-id="08346-113">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="08346-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="08346-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="08346-114">Example</span></span>

<span data-ttu-id="08346-115">`LEFT ("Sample", 3)` returnerer **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="08346-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="08346-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="08346-116">Additional resources</span></span>

[<span data-ttu-id="08346-117">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="08346-117">Text functions</span></span>](er-functions-category-text.md)
