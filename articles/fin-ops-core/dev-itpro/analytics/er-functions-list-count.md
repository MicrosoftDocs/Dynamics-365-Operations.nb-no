---
title: COUNT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen COUNT.
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
ms.openlocfilehash: c48483a6677aaeb36eac57a57cec71bf54c7991d
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745351"
---
# <a name="count-er-function"></a><span data-ttu-id="d6dbc-103">COUNT ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="d6dbc-103">COUNT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d6dbc-104">`COUNT`-funksjonen returnerer en *Heltall*-verdi som representerer antall poster i den angitte listen, hvis listen ikke er tom.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-104">The `COUNT` function returns an *Integer* value that represents the number of records in the specified list, if the list isn't empty.</span></span> <span data-ttu-id="d6dbc-105">Hvis listen er tom, returnerer denne funksjonen **0** (null).</span><span class="sxs-lookup"><span data-stu-id="d6dbc-105">If the list is empty, this function returns **0** (zero).</span></span>

## <a name="syntax"></a><span data-ttu-id="d6dbc-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d6dbc-106">Syntax</span></span>

```vb
COUNT (list)
```

## <a name="arguments"></a><span data-ttu-id="d6dbc-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d6dbc-107">Arguments</span></span>

<span data-ttu-id="d6dbc-108">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="d6dbc-108">`list`: *Record list*</span></span>

<span data-ttu-id="d6dbc-109">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-109">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="d6dbc-110">Returverdier</span><span class="sxs-lookup"><span data-stu-id="d6dbc-110">Return values</span></span>

<span data-ttu-id="d6dbc-111">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="d6dbc-111">*Integer*</span></span>

<span data-ttu-id="d6dbc-112">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-112">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="d6dbc-113">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d6dbc-113">Example</span></span>

<span data-ttu-id="d6dbc-114">`COUNT (SPLIT("abcd" , 3))` returnerer **2** fordi `SPLIT`-funksjonen som brukes i dette eksemplet, oppretter en liste som består av to poster.</span><span class="sxs-lookup"><span data-stu-id="d6dbc-114">`COUNT (SPLIT("abcd" , 3))` returns **2**, because the `SPLIT` function that is used in this example creates a list that consists of two records.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d6dbc-115">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d6dbc-115">Additional resources</span></span>

[<span data-ttu-id="d6dbc-116">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="d6dbc-116">List functions</span></span>](er-functions-category-list.md)
