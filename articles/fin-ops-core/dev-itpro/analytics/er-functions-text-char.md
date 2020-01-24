---
title: CHAR ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CHAR
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d42afcf97690351763138fd9e16265aa104a6bc4
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915746"
---
# <span data-ttu-id="2d9a7-103"><a name="CHAR">CHAR ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="2d9a7-103"><a name="CHAR">CHAR ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2d9a7-104">`CHAR`-funksjonen returnerer en *streng*-verdi som viser et enkelt tegn som det angitte Unicode-nummeret refererer til.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-104">The `CHAR` function returns a *String* value that presents a single character that is referenced by the specified Unicode number.</span></span>

## <a name="syntax"></a><span data-ttu-id="2d9a7-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2d9a7-105">Syntax</span></span>

```
CHAR (number)
```

## <a name="arguments"></a><span data-ttu-id="2d9a7-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2d9a7-106">Arguments</span></span>

<span data-ttu-id="2d9a7-107">`number`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="2d9a7-107">`number`: *Integer*</span></span>

<span data-ttu-id="2d9a7-108">Et tall som svarer til et forventet enkelt tegn.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-108">A number that corresponds to an expected single character.</span></span>

## <a name="return-values"></a><span data-ttu-id="2d9a7-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="2d9a7-109">Return values</span></span>

<span data-ttu-id="2d9a7-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="2d9a7-110">*String*</span></span>

<span data-ttu-id="2d9a7-111">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="2d9a7-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="2d9a7-112">Usage notes</span></span>

<span data-ttu-id="2d9a7-113">Strengen som denne funksjonen returnerer, avhenger av kodingen som er valgt i det overordnede **FIL**-formatelementet.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-113">The string that this function returns depends on the encoding that is selected in the parent **FILE** format element.</span></span> <span data-ttu-id="2d9a7-114">Listen over støttede kodinger finner du her [Kodingsklasse](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span><span class="sxs-lookup"><span data-stu-id="2d9a7-114">For a list of the supported encodings, see [Encoding class](https://msdn.microsoft.com/library/system.text.encoding(v=vs.110).aspx).</span></span>

## <a name="example"></a><span data-ttu-id="2d9a7-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2d9a7-115">Example</span></span>

<span data-ttu-id="2d9a7-116">`CHAR (255)` returnerer **"ÿ"**.</span><span class="sxs-lookup"><span data-stu-id="2d9a7-116">`CHAR (255)` returns **"ÿ"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2d9a7-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="2d9a7-117">Additional resources</span></span>

[<span data-ttu-id="2d9a7-118">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="2d9a7-118">Text functions</span></span>](er-functions-category-text.md)