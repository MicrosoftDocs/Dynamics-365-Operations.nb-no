---
title: TABLENAME2ID ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen TABLENAME2ID
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
ms.openlocfilehash: 0f94d00d9d40830d895e906ffbaa2a236f1efc43
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746561"
---
# <a name="tablename2id-er-function"></a><span data-ttu-id="8d34e-103">TABLENAME2ID ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="8d34e-103">TABLENAME2ID ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d34e-104">`TABLENAME2ID`-funksjonen returnerer en numerisk representasjon av tabell-IDen for det angitte tabellnavnet som en  *heltall*-verdi.</span><span class="sxs-lookup"><span data-stu-id="8d34e-104">The `TABLENAME2ID` function returns a numeric representation of the table ID for the specified table name as an *Integer* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="8d34e-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="8d34e-105">Syntax</span></span>

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a><span data-ttu-id="8d34e-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="8d34e-106">Arguments</span></span>

<span data-ttu-id="8d34e-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="8d34e-107">`text`: *String*</span></span>

<span data-ttu-id="8d34e-108">En tekstverdi som representerer et gyldig tabellnavn.</span><span class="sxs-lookup"><span data-stu-id="8d34e-108">A text value that represents a valid table name.</span></span>

## <a name="return-values"></a><span data-ttu-id="8d34e-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="8d34e-109">Return values</span></span>

<span data-ttu-id="8d34e-110">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="8d34e-110">*Integer*</span></span>

<span data-ttu-id="8d34e-111">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="8d34e-111">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="8d34e-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="8d34e-112">Usage notes</span></span>

<span data-ttu-id="8d34e-113">Utføring av denne funksjonen kan ha forskjellige resultater i forskjellige forekomster av Microsoft Dynamics 365 Finance, selv om det samme firmanavnet brukes.</span><span class="sxs-lookup"><span data-stu-id="8d34e-113">Execution of this function can have different results in different instances of Microsoft Dynamics 365 Finance, even if the same company name is used.</span></span>

## <a name="example"></a><span data-ttu-id="8d34e-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="8d34e-114">Example</span></span>

<span data-ttu-id="8d34e-115">`TABLENAME2ID ("Intrastat")` returnerer **1510**.</span><span class="sxs-lookup"><span data-stu-id="8d34e-115">`TABLENAME2ID ("Intrastat")` returns **1510**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8d34e-116">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8d34e-116">Additional resources</span></span>

[<span data-ttu-id="8d34e-117">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="8d34e-117">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]