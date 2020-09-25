---
title: EMPTYLIST ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen EMPTYLIST.
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
ms.openlocfilehash: 747b661d0dee4e9c27741e167c89f9ef7eefa470
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745327"
---
# <a name="emptylist-er-function"></a><span data-ttu-id="95fd9-103">EMPTYLIST ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="95fd9-103">EMPTYLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="95fd9-104">`EMPTYLIST`-funksjonen returnerer en tom  *Postliste*-verdi ved hjelp av den angitte listen som en kilde for listestrukturen.</span><span class="sxs-lookup"><span data-stu-id="95fd9-104">The `EMPTYLIST` function returns an empty *Record list* value by using the specified list as a source for the list structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="95fd9-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="95fd9-105">Syntax</span></span>

```vb
EMPTYLIST (list)
```

## <a name="arguments"></a><span data-ttu-id="95fd9-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="95fd9-106">Arguments</span></span>

<span data-ttu-id="95fd9-107">`list`: *Postliste*</span><span class="sxs-lookup"><span data-stu-id="95fd9-107">`list`: *Record list*</span></span>

<span data-ttu-id="95fd9-108">Den gyldige banen til en datakilde av *Postliste*-datatypen.</span><span class="sxs-lookup"><span data-stu-id="95fd9-108">The valid path of a data source of the *Record list* data type.</span></span>

## <a name="return-values"></a><span data-ttu-id="95fd9-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="95fd9-109">Return values</span></span>

<span data-ttu-id="95fd9-110">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="95fd9-110">*Record list*</span></span>

<span data-ttu-id="95fd9-111">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="95fd9-111">The resulting list of records.</span></span>

## <a name="example"></a><span data-ttu-id="95fd9-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="95fd9-112">Example</span></span>

<span data-ttu-id="95fd9-113">`EMPTYLIST (SPLIT ("abc", 1))` returnerer en ny, tom liste som har samme struktur som listen som returneres av `SPLIT`- funksjonen som brukes.</span><span class="sxs-lookup"><span data-stu-id="95fd9-113">`EMPTYLIST (SPLIT ("abc", 1))` returns a new empty list that has the same structure as the list that is returned by the `SPLIT` function that is used.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="95fd9-114">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="95fd9-114">Additional resources</span></span>

[<span data-ttu-id="95fd9-115">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="95fd9-115">List functions</span></span>](er-functions-category-list.md)
