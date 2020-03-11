---
title: FIRST ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FIRST.
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
ms.openlocfilehash: 4d10abcf15b93961bd2ba4aec22914825d9ac38c
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042096"
---
# <span data-ttu-id="4fa17-103"><a name="FIRST">FIRST ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="4fa17-103"><a name="FIRST">FIRST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4fa17-104">`FIRST`-funksjonen returnerer den første posten i den angitte listen som en *Container (post)*-verdi, hvis denne listen ikke er tom.</span><span class="sxs-lookup"><span data-stu-id="4fa17-104">The `FIRST` function returns the first record of the specified list as a *Container (record)* value, if that list isn't empty.</span></span> <span data-ttu-id="4fa17-105">Hvis listen er tom, genererer denne funksjonen et unntak.</span><span class="sxs-lookup"><span data-stu-id="4fa17-105">If the list is empty, this function throws an exception.</span></span>

## <a name="syntax"></a><span data-ttu-id="4fa17-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="4fa17-106">Syntax</span></span>

```vb
FIRST (list)
```

## <a name="arguments"></a><span data-ttu-id="4fa17-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="4fa17-107">Arguments</span></span>

<span data-ttu-id="4fa17-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="4fa17-108">`list`: *Record list*</span></span>

<span data-ttu-id="4fa17-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="4fa17-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4fa17-110">Returverdier</span><span class="sxs-lookup"><span data-stu-id="4fa17-110">Return values</span></span>

<span data-ttu-id="4fa17-111">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="4fa17-111">*Container (record)*</span></span>

<span data-ttu-id="4fa17-112">Den resulterende postvedien.</span><span class="sxs-lookup"><span data-stu-id="4fa17-112">The resulting record value.</span></span>

## <a name="example-1"></a><span data-ttu-id="4fa17-113">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="4fa17-113">Example 1</span></span>

<span data-ttu-id="4fa17-114">Uttrykket `FIRST(SPLIT("ABC",1)).Value` returnerer tekstverdien **"A"**.</span><span class="sxs-lookup"><span data-stu-id="4fa17-114">The expression `FIRST(SPLIT("ABC",1)).Value` returns the text value **"A"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="4fa17-115">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="4fa17-115">Example 2</span></span>

<span data-ttu-id="4fa17-116">Uttrykket `FIRST(SPLIT("",1)).Value` genererer et unntak under kjøring.</span><span class="sxs-lookup"><span data-stu-id="4fa17-116">The expression `FIRST(SPLIT("",1)).Value` throws an exception at runtime.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4fa17-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4fa17-117">Additional resources</span></span>

[<span data-ttu-id="4fa17-118">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="4fa17-118">List functions</span></span>](er-functions-category-list.md)
