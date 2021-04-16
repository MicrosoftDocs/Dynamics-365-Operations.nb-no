---
title: EMPTYLIST ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen EMPTYLIST.
author: NickSelin
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
ms.openlocfilehash: 1e2a92d9951c3ad27503cf82f1b45026f16c3835
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746681"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="8ea9c-103">EMPTYLIST ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="8ea9c-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ea9c-104">`EMPTYLIST`-funksjonen returnerer en tom  *Postliste*-verdi ved hjelp av den angitte listen som en kilde for listestrukturen.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="8ea9c-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="8ea9c-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="8ea9c-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8ea9c-106">Arguments</span></span>

<span data-ttu-id="8ea9c-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="8ea9c-107">`list`: *Record list*</span></span>

<span data-ttu-id="8ea9c-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="8ea9c-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="8ea9c-109">Return values</span></span>

<span data-ttu-id="8ea9c-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="8ea9c-110">*Record list*</span></span>

<span data-ttu-id="8ea9c-111">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="8ea9c-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8ea9c-112">Example</span></span>

<span data-ttu-id="8ea9c-113">`EMPTYLIST (SPLIT ("abc", 1))` returnerer en ny, tom liste som har samme struktur som listen som returneres av `SPLIT`- funksjonen som brukes.</span><span class="sxs-lookup"><span data-stu-id="8ea9c-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ea9c-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8ea9c-114">Additional resources</span></span>

[<span data-ttu-id="8ea9c-115">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="8ea9c-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]