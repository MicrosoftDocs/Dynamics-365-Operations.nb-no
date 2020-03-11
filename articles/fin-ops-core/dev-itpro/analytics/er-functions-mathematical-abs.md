---
title: ABS ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen ABS
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 214fb2808f024487795f27de45de1d4de8cead2d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041659"
---
# <span data-ttu-id="f8834-103"><a name="ABS">ABS ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="f8834-103"><a name="ABS">ABS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8834-104">`ABS`-funksjonen returnerer den absolutte (modulus) verdien til det angitte nummeret som en *reell* verdi.</span><span class="sxs-lookup"><span data-stu-id="f8834-104">The `ABS` function returns the absolute value (modulus) of the specified number as a *Real* value.</span></span> <span data-ttu-id="f8834-105">Altså returnes tallet uten fortegn.</span><span class="sxs-lookup"><span data-stu-id="f8834-105">In other words, it returns the number without its sign.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8834-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="f8834-106">Syntax</span></span>

```vb
ABS (number)
```

## <a name="arguments"></a><span data-ttu-id="f8834-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="f8834-107">Arguments</span></span>

<span data-ttu-id="f8834-108">`number`: *Reell*</span><span class="sxs-lookup"><span data-stu-id="f8834-108">`number`: *Real*</span></span>

<span data-ttu-id="f8834-109">En numerisk verdi du vil bruke modulus til.</span><span class="sxs-lookup"><span data-stu-id="f8834-109">A numeric value that you want the modulus of.</span></span>

## <a name="return-values"></a><span data-ttu-id="f8834-110">Returverdier</span><span class="sxs-lookup"><span data-stu-id="f8834-110">Return values</span></span>

<span data-ttu-id="f8834-111">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="f8834-111">*Real*</span></span>

<span data-ttu-id="f8834-112">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="f8834-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="f8834-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="f8834-113">Example</span></span>

<span data-ttu-id="f8834-114">`ABS (-1)` returnerer **1**.</span><span class="sxs-lookup"><span data-stu-id="f8834-114">`ABS (-1)` returns **1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8834-115">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="f8834-115">Additional resources</span></span>

[<span data-ttu-id="f8834-116">Matematiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="f8834-116">Mathematical functions</span></span>](er-functions-category-mathematical.md)
