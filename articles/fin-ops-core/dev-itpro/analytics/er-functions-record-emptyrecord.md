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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2e46fcef3d53483b782ac39a0661fc0edc8d861c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743956"
---
# <a name="emptyrecord-er-function"></a><span data-ttu-id="4996b-103">EMPTYRECORD ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="4996b-103">EMPTYRECORD ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4996b-104">`EMPTYRECORD`-funksjonen returnerer en nullverdi for *Container (post)*-verdi som har samme struktur som den angitte postlisten eller posten.</span><span class="sxs-lookup"><span data-stu-id="4996b-104">The `EMPTYRECORD` function returns a null *Container (record)* value that has the same structure as the specified record list or record.</span></span>

## <a name="syntax"></a><span data-ttu-id="4996b-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="4996b-105">Syntax</span></span>

```vb
EMPTYRECORD (list)
```

## <a name="arguments"></a><span data-ttu-id="4996b-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="4996b-106">Arguments</span></span>

<span data-ttu-id="4996b-107">`list`: *Postliste* eller *Container (post)*</span><span class="sxs-lookup"><span data-stu-id="4996b-107">`list`: *Record list* or *Container (record)*</span></span>

<span data-ttu-id="4996b-108">Den gyldige banen til en datakilde for typen *Postliste* eller *Container (record)*.</span><span class="sxs-lookup"><span data-stu-id="4996b-108">The valid path of a data source of either the *Record list* or *Container (record)* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="4996b-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="4996b-109">Return values</span></span>

<span data-ttu-id="4996b-110">*Container (post)*</span><span class="sxs-lookup"><span data-stu-id="4996b-110">*Container (record)*</span></span>

<span data-ttu-id="4996b-111">Den resulterende postvedien.</span><span class="sxs-lookup"><span data-stu-id="4996b-111">The resulting record value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4996b-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="4996b-112">Usage notes</span></span>

> [!NOTE] 
> <span data-ttu-id="4996b-113">En null-post er en post der alle felt har en tom verdi.</span><span class="sxs-lookup"><span data-stu-id="4996b-113">A null record is a record where all fields have an empty value.</span></span> <span data-ttu-id="4996b-114">En tom verdi er **0** (null) for tall, en tom streng for strenger og så videre.</span><span class="sxs-lookup"><span data-stu-id="4996b-114">An empty value is **0** (zero) for numbers, an empty string for strings, and so on.</span></span>

## <a name="example"></a><span data-ttu-id="4996b-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4996b-115">Example</span></span>

<span data-ttu-id="4996b-116">`EMPTYRECORD (SPLIT ("abc", 1))` returnerer en ny, tom post som har samme struktur som listen som returneres av `SPLIT`- funksjonen.</span><span class="sxs-lookup"><span data-stu-id="4996b-116">`EMPTYRECORD (SPLIT ("abc", 1))` returns a new empty record that has the same structure as the list that is returned by the `SPLIT` function.</span></span> <span data-ttu-id="4996b-117">Hvis du vil ha mer informasjon, kan du se [SPLIT](er-functions-list-split.md).</span><span class="sxs-lookup"><span data-stu-id="4996b-117">For more information, see [SPLIT](er-functions-list-split.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4996b-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4996b-118">Additional resources</span></span>

[<span data-ttu-id="4996b-119">Registreringsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="4996b-119">Record functions</span></span>](er-functions-category-record.md)
