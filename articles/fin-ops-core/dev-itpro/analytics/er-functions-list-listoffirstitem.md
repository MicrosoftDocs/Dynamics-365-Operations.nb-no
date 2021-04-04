---
title: LISTOFFIRSTITEM ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LISTOFFIRSTITEM.
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
ms.openlocfilehash: f2e1f7e55c61f883aebb9d5a522a883a9a9de694
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5569846"
---
# <a name="listoffirstitem-er-function"></a><span data-ttu-id="eac44-103">LISTOFFIRSTITEM ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="eac44-103">LISTOFFIRSTITEM ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="eac44-104">`LISTOFFIRSTITEM` -funksjonen returnerer en *Postliste*-verdi som består av bare den første posten i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="eac44-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="eac44-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="eac44-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="eac44-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="eac44-106">Arguments</span></span>

<span data-ttu-id="eac44-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="eac44-107">`list`: *Record list*</span></span>

<span data-ttu-id="eac44-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="eac44-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="eac44-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="eac44-109">Return values</span></span>

<span data-ttu-id="eac44-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="eac44-110">*Record list*</span></span>

<span data-ttu-id="eac44-111">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="eac44-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="eac44-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="eac44-112">Example</span></span>

<span data-ttu-id="eac44-113">Uttrykket `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returnerer tekstverdien **"A"**.</span><span class="sxs-lookup"><span data-stu-id="eac44-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="eac44-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="eac44-114">Additional resources</span></span>

[<span data-ttu-id="eac44-115">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="eac44-115">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]