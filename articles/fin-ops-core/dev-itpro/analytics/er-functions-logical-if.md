---
title: IF ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen IF.
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
ms.openlocfilehash: b8733022b44f3460e34a610140fd6d584ab990c2
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4687008"
---
# <a name="if-er-function"></a><span data-ttu-id="9c264-103">IF ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="9c264-103">IF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9c264-104">`IF`-funksjonen returnerer den første verdien hvis den angitte betingelsen er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="9c264-104">The `IF` function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="9c264-105">Hvis ikke returneres den andre verdien som er angitt.</span><span class="sxs-lookup"><span data-stu-id="9c264-105">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="9c264-106">Verdien som returneres, kan være en verdi for en hvilken som helst av de støttede datatypene.</span><span class="sxs-lookup"><span data-stu-id="9c264-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="9c264-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="9c264-107">Syntax</span></span>

```vb
IF (condition, first value, second value) as any of the supported data types
```

## <a name="arguments"></a><span data-ttu-id="9c264-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="9c264-108">Arguments</span></span>

<span data-ttu-id="9c264-109">`condition`: *Boolsk*</span><span class="sxs-lookup"><span data-stu-id="9c264-109">`condition`: *Boolean*</span></span>

<span data-ttu-id="9c264-110">Et gyldig betingelsesuttrykk som må testes.</span><span class="sxs-lookup"><span data-stu-id="9c264-110">A valid conditional expression that must be tested.</span></span>

<span data-ttu-id="9c264-111">`first value`: *Hvilken som helst av datatypene som støttes*</span><span class="sxs-lookup"><span data-stu-id="9c264-111">`first value`: *Any of the supported data types*</span></span>

<span data-ttu-id="9c264-112">Resultatet som returneres hvis betingelsen oppfylles.</span><span class="sxs-lookup"><span data-stu-id="9c264-112">The result that is returned if the condition is met.</span></span>

<span data-ttu-id="9c264-113">`second value`: *Hvilken som helst av datatypene som støttes*</span><span class="sxs-lookup"><span data-stu-id="9c264-113">`second value`: *Any of the supported data types*</span></span>

<span data-ttu-id="9c264-114">Resultatet som returneres hvis betingelsen ikke oppfylles.</span><span class="sxs-lookup"><span data-stu-id="9c264-114">The result that is returned if the condition isn't met.</span></span>

## <a name="return-values"></a><span data-ttu-id="9c264-115">Returverdier</span><span class="sxs-lookup"><span data-stu-id="9c264-115">Return values</span></span>

<span data-ttu-id="9c264-116">*Hvilken som helst av datatypene som støttes*</span><span class="sxs-lookup"><span data-stu-id="9c264-116">*Any of the supported data types*</span></span>

<span data-ttu-id="9c264-117">Resultatverdien for en hvilken som helst av de støttede datatypene.</span><span class="sxs-lookup"><span data-stu-id="9c264-117">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="9c264-118">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="9c264-118">Usage notes</span></span>

<span data-ttu-id="9c264-119">Argumentene `first value` og `second value` må angis ved hjelp av den samme datatypen.</span><span class="sxs-lookup"><span data-stu-id="9c264-119">The `first value` and `second value` arguments must be specified by using the same data type.</span></span> <span data-ttu-id="9c264-120">Et unntak er registrert ved utformingstid hvis datatypene for de konfigurerte verdiene ikke samsvarer.</span><span class="sxs-lookup"><span data-stu-id="9c264-120">An exception is thrown at design time if the data types of the configured values don't match.</span></span>

<span data-ttu-id="9c264-121">Hvis den første og andre verdien er verdier for datatypen *Container (post)* eller *Postliste*, har resultatet bare feltene som finnes i begge verdiene.</span><span class="sxs-lookup"><span data-stu-id="9c264-121">If the first value and the second value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="9c264-122">Eksempel</span><span class="sxs-lookup"><span data-stu-id="9c264-122">Example</span></span>

<span data-ttu-id="9c264-123">`IF (1=2, "condition is met", "condition is not met")` returnerer strengen **"betingelsen er ikke oppfylt"**.</span><span class="sxs-lookup"><span data-stu-id="9c264-123">`IF (1=2, "condition is met", "condition is not met")` returns the string **"condition is not met"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="9c264-124">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="9c264-124">Additional resources</span></span>

[<span data-ttu-id="9c264-125">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="9c264-125">Logical functions</span></span>](er-functions-category-logical.md)
