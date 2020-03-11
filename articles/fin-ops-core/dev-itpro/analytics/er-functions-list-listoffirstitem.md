---
title: LISTOFFIRSTITEM ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen LISTOFFIRSTITEM.
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
ms.openlocfilehash: 8cd48732280c9af0b89129a32b42285207f97fb7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041981"
---
# <span data-ttu-id="2ff9a-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="2ff9a-103"><a name="LISTOFFIRSTITEM">LISTOFFIRSTITEM ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2ff9a-104">`LISTOFFIRSTITEM` -funksjonen returnerer en *Postliste*-verdi som består av bare den første posten i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="2ff9a-104">The `LISTOFFIRSTITEM` function returns a *Record list* value that consists of only the first record of the specified list.</span></span>

## <a name="syntax"></a><span data-ttu-id="2ff9a-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2ff9a-105">Syntax</span></span>

```vb
LISTOFFIRSTITEM (list)
```

## <a name="arguments"></a><span data-ttu-id="2ff9a-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2ff9a-106">Arguments</span></span>

<span data-ttu-id="2ff9a-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="2ff9a-107">`list`: *Record list*</span></span>

<span data-ttu-id="2ff9a-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="2ff9a-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="2ff9a-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="2ff9a-109">Return values</span></span>

<span data-ttu-id="2ff9a-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="2ff9a-110">*Record list*</span></span>

<span data-ttu-id="2ff9a-111">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="2ff9a-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="2ff9a-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2ff9a-112">Example</span></span>

<span data-ttu-id="2ff9a-113">Uttrykket `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returnerer tekstverdien **"A"**.</span><span class="sxs-lookup"><span data-stu-id="2ff9a-113">The expression `FIRST( LISTOFFIRSTITEM ( SPLIT ("ABC",1))).Value` returns the text value **"A"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ff9a-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="2ff9a-114">Additional resources</span></span>

[<span data-ttu-id="2ff9a-115">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="2ff9a-115">List functions</span></span>](er-functions-category-list.md)
