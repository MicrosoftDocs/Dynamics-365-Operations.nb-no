---
title: EMPTYRECORD ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen EMPTYRECORD.
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
ms.openlocfilehash: d50b31fcbbb99050fca46b0a5ce10cc3fd243691
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684817"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="e198a-103">EMPTYRECORD ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="e198a-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e198a-104">`EMPTYRECORD`-funksjonen returnerer en nullverdi for *Container (post)*-verdi som har samme struktur som den angitte postlisten eller posten.</span><span class="sxs-lookup"><span data-stu-id="e198a-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="e198a-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="e198a-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="e198a-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="e198a-106">Arguments</span></span>

<span data-ttu-id="e198a-107">`list`: *Postliste* eller *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="e198a-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="e198a-108">Den gyldige banen til en datakilde for typen *Postliste* eller *Container (record)*.</span><span class="sxs-lookup"><span data-stu-id="e198a-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="e198a-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="e198a-109">Return values</span></span>

<span data-ttu-id="e198a-110">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="e198a-110">*Container (record)*</span></span>

<span data-ttu-id="e198a-111">Den resulterende postvedien.</span><span class="sxs-lookup"><span data-stu-id="e198a-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="e198a-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="e198a-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="e198a-113">En null-post er en post der alle felt har en tom verdi.</span><span class="sxs-lookup"><span data-stu-id="e198a-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="e198a-114">En tom verdi er **0** (null) for tall, en tom streng for strenger og så videre.</span><span class="sxs-lookup"><span data-stu-id="e198a-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="e198a-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e198a-115">Example</span></span>

<span data-ttu-id="e198a-116">`EMPTYRECORD (SPLIT ("abc", 1))` returnerer en ny, tom post som har samme struktur som listen som returneres av `SPLIT`- funksjonen.</span><span class="sxs-lookup"><span data-stu-id="e198a-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="e198a-117">Hvis du vil ha mer informasjon, kan du se [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="e198a-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e198a-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e198a-118">Additional resources</span></span>

[<span data-ttu-id="e198a-119">Registreringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="e198a-119">Record functions</span></span>](er-functions-category-record.md)
