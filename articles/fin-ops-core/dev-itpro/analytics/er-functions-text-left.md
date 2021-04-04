---
title: LEFT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LEFT
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 6f1ec7a21a16c3a34bed9779b05f20f21815ab9d
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569998"
---
# <a name="left-er-function"></a><span data-ttu-id="28341-103">LEFT ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="28341-103">LEFT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="28341-104">`LEFT`-funksjonen returnerer en *streng*-verdi som viser det angitte antallet tegn fra starten av den angitte strengen.</span><span class="sxs-lookup"><span data-stu-id="28341-104">The `LEFT` function returns a *String* value that presents the specified number of characters from the start of the specified string.</span></span>

## <a name="syntax"></a><span data-ttu-id="28341-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="28341-105">Syntax</span></span>

```vb
LEFT (text, number)
```

## <a name="arguments"></a><span data-ttu-id="28341-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="28341-106">Arguments</span></span>

<span data-ttu-id="28341-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="28341-107">`text`: *String*</span></span>

<span data-ttu-id="28341-108">En *streng*-verdi som representerer den opprinnelige teksten.</span><span class="sxs-lookup"><span data-stu-id="28341-108">A *String* value that represents the original text.</span></span>

<span data-ttu-id="28341-109">`number`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="28341-109">`number`: *Integer*</span></span>

<span data-ttu-id="28341-110">Antall tegn som må returneres fra begynnelsen av den opprinnelige teksten.</span><span class="sxs-lookup"><span data-stu-id="28341-110">The number of characters that must be returned from the start of the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="28341-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="28341-111">Return values</span></span>

<span data-ttu-id="28341-112">*Streng*</span><span class="sxs-lookup"><span data-stu-id="28341-112">*String*</span></span>

<span data-ttu-id="28341-113">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="28341-113">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="28341-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="28341-114">Example</span></span>

<span data-ttu-id="28341-115">`LEFT ("Sample", 3)` returnerer **"Sam"**.</span><span class="sxs-lookup"><span data-stu-id="28341-115">`LEFT ("Sample", 3)` returns **"Sam"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="28341-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="28341-116">Additional resources</span></span>

[<span data-ttu-id="28341-117">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="28341-117">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]