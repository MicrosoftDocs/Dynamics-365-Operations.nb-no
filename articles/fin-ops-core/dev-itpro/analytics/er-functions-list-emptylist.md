---
title: EMPTYLIST ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen EMPTYLIST.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: f6c2777065656affc992a427194286008c1df42f
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5559206"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="650a6-103">EMPTYLIST ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="650a6-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="650a6-104">`EMPTYLIST`-funksjonen returnerer en tom  *Postliste*-verdi ved hjelp av den angitte listen som en kilde for listestrukturen.</span><span class="sxs-lookup"><span data-stu-id="650a6-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="650a6-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="650a6-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="650a6-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="650a6-106">Arguments</span></span>

<span data-ttu-id="650a6-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="650a6-107">`list`: *Record list*</span></span>

<span data-ttu-id="650a6-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="650a6-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="650a6-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="650a6-109">Return values</span></span>

<span data-ttu-id="650a6-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="650a6-110">*Record list*</span></span>

<span data-ttu-id="650a6-111">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="650a6-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="650a6-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="650a6-112">Example</span></span>

<span data-ttu-id="650a6-113">`EMPTYLIST (SPLIT ("abc", 1))` returnerer en ny, tom liste som har samme struktur som listen som returneres av `SPLIT`- funksjonen som brukes.</span><span class="sxs-lookup"><span data-stu-id="650a6-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="650a6-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="650a6-114">Additional resources</span></span>

[<span data-ttu-id="650a6-115">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="650a6-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]