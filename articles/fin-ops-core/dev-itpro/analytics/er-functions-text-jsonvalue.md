---
title: JSONVALUE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen JSONVALUE.
author: NickSelin
manager: kfend
ms.date: 12/11/2019
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
ms.openlocfilehash: 203fe1b1616f724ddf3015258306e0d9e8d4f599
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570022"
---
# <a name="jsonvalue-er-function"></a><span data-ttu-id="87180-103">JSONVALUE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="87180-103">JSONVALUE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="87180-104">`JSONVALUE`-funksjonen analyserer data i JavaScript Object Notation (JSON)-format som brukes av den angitte banen, og henter en skalarverdi som har den angitte IDen.</span><span class="sxs-lookup"><span data-stu-id="87180-104">The `JSONVALUE` function parses data in JavaScript Object Notation (JSON) format that is accessed at the specified path, and it extracts a scalar value that has the specified ID.</span></span> <span data-ttu-id="87180-105">Den returnerer deretter den utpakkede skalerbare verdien som en *streng*-verdi.</span><span class="sxs-lookup"><span data-stu-id="87180-105">It then returns the extracted scalar value as a *String* value.</span></span>

## <a name="syntax"></a><span data-ttu-id="87180-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="87180-106">Syntax</span></span>

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a><span data-ttu-id="87180-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="87180-107">Arguments</span></span>

<span data-ttu-id="87180-108">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="87180-108">`input`: *String*</span></span>

<span data-ttu-id="87180-109">Den gyldige banen til en datakilde av *Streng*-typen som inneholder JSON-data.</span><span class="sxs-lookup"><span data-stu-id="87180-109">The valid path of a data source of the *String* type that contains JSON data.</span></span>

<span data-ttu-id="87180-110">`path`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="87180-110">`path`: *String*</span></span>

<span data-ttu-id="87180-111">Identifikatoren for en skalerbar verdi for JSON-data.</span><span class="sxs-lookup"><span data-stu-id="87180-111">The identifier of a scalar value of JSON data.</span></span>

## <a name="return-values"></a><span data-ttu-id="87180-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="87180-112">Return values</span></span>

<span data-ttu-id="87180-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="87180-113">*String*</span></span>

<span data-ttu-id="87180-114">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="87180-114">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="87180-115">Eksempel</span><span class="sxs-lookup"><span data-stu-id="87180-115">Example</span></span>

<span data-ttu-id="87180-116">Datakilden **JsonField** inneholder følgende data i JSON-format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span><span class="sxs-lookup"><span data-stu-id="87180-116">The **JsonField** data source contains the following data in JSON format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**.</span></span> <span data-ttu-id="87180-117">I dette tilfellet returnerer uttrykket `JSONVALUE (JsonField, "BuildNumber")` følgende verdi av *streng*-datatypen: **"7.3.1234.1"**.</span><span class="sxs-lookup"><span data-stu-id="87180-117">In this case, the expression `JSONVALUE (JsonField, "BuildNumber")` returns the following value of the *String* data type: **"7.3.1234.1"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="87180-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="87180-118">Additional resources</span></span>

[<span data-ttu-id="87180-119">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="87180-119">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]