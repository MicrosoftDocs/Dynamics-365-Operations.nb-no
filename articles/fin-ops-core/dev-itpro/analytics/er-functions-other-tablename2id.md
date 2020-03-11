---
title: TABLENAME2ID ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen TABLENAME2ID
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
ms.openlocfilehash: 951de1d1505508ebb6abeff5b80ecef10573e117
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041276"
---
# <span data-ttu-id="210b3-103"><a name="TABLENAME2ID">TABLENAME2ID ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="210b3-103"><a name="TABLENAME2ID">TABLENAME2ID ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="210b3-104">`TABLENAME2ID`-funksjonen returnerer en numerisk representasjon av tabell-IDen for det angitte tabellnavnet som en  *heltall*-verdi.</span><span class="sxs-lookup"><span data-stu-id="210b3-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="210b3-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="210b3-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="210b3-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="210b3-106">Arguments</span></span>

<span data-ttu-id="210b3-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="210b3-107">`text`: *String*</span></span>

<span data-ttu-id="210b3-108">En tekstverdi som representerer et gyldig tabellnavn.</span><span class="sxs-lookup"><span data-stu-id="210b3-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="210b3-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="210b3-109">Return values</span></span>

<span data-ttu-id="210b3-110">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="210b3-110">*Integer*</span></span>

<span data-ttu-id="210b3-111">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="210b3-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="210b3-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="210b3-112">Usage notes</span></span>

<span data-ttu-id="210b3-113">Utføring av denne funksjonen kan ha forskjellige resultater i forskjellige forekomster av Microsoft Dynamics 365 Finance, selv om det samme firmanavnet brukes.</span><span class="sxs-lookup"><span data-stu-id="210b3-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="210b3-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="210b3-114">Example</span></span>

<span data-ttu-id="210b3-115">`TABLENAME2ID ("Intrastat")` returnerer **1510**.</span><span class="sxs-lookup"><span data-stu-id="210b3-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="210b3-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="210b3-116">Additional resources</span></span>

[<span data-ttu-id="210b3-117">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="210b3-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
