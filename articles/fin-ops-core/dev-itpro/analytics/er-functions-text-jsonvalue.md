---
title: JSONVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen JSONVALUE.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: d8209f8ce9d244ab7c82f897e4f59283e94e0522
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915677"
---
# <span data-ttu-id="c4646-103"><a name="JSONVALUE">JSONVALUE ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="c4646-103"><a name="JSONVALUE">JSONVALUE ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c4646-104">`JSONVALUE`-funksjonen analyserer data i JavaScript Object Notation (JSON)-format som brukes av den angitte banen, og henter en skalarverdi som har den angitte IDen.</span><span class="sxs-lookup"><span data-stu-id="c4646-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="c4646-105">Den returnerer deretter den utpakkede skalerbare verdien som en *streng*-verdi.</span><span class="sxs-lookup"><span data-stu-id="c4646-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4646-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c4646-106">Syntax</span></span>

```
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="c4646-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="c4646-107">Arguments</span></span>

<span data-ttu-id="c4646-108">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="c4646-108">`input`: *String*</span></span>

<span data-ttu-id="c4646-109">Den gyldige banen til en datakilde av *Streng*-typen som inneholder JSON-data.</span><span class="sxs-lookup"><span data-stu-id="c4646-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="c4646-110">`path`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="c4646-110">`path`: *String*</span></span>

<span data-ttu-id="c4646-111">Identifikatoren for en skalerbar verdi for JSON-data.</span><span class="sxs-lookup"><span data-stu-id="c4646-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="c4646-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="c4646-112">Return values</span></span>

<span data-ttu-id="c4646-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="c4646-113">*String*</span></span>

<span data-ttu-id="c4646-114">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="c4646-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c4646-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c4646-115">Example</span></span>

<span data-ttu-id="c4646-116">Datakilden **JsonField** inneholder følgende data i JSON-format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="c4646-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="c4646-117">I dette tilfellet returnerer uttrykket `JSONVALUE (JsonField, "BuildNumber")` følgende verdi av *streng*-datatypen: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="c4646-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c4646-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c4646-118">Additional resources</span></span>

[<span data-ttu-id="c4646-119">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="c4646-119">Text functions</span></span>](er-functions-category-text.md)