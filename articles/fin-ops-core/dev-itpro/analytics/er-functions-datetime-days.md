---
title: DAYS ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen DAYS
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 0252a68aebaa9af95de561b88ceb0666b3460d79
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5563492"
---
# <a name="days-er-function"></a><span data-ttu-id="d351b-103">DAYS ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="d351b-103">DAYS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d351b-104">`DAYS`-funksjonen returnerer en *Heltall*-verdi som representerer antall dager mellom en angitt dato og en annen angitt dato.</span><span class="sxs-lookup"><span data-stu-id="d351b-104">The `DAYS` function returns an *Integer* value that represents the number of days between one specified date and a second specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="d351b-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d351b-105">Syntax</span></span>

```vb
DAYS (date 1, date 2) as Integer
```

## <a name="arguments"></a><span data-ttu-id="d351b-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="d351b-106">Arguments</span></span>

<span data-ttu-id="d351b-107">`date 1`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="d351b-107">`date 1`: *Date*</span></span>

<span data-ttu-id="d351b-108">En datoverdi som representerer startdatoen for beregningen av antall dager.</span><span class="sxs-lookup"><span data-stu-id="d351b-108">A date value that represents the start date for the calculation of the number of days.</span></span>

<span data-ttu-id="d351b-109">`date 2`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="d351b-109">`date 2`: *Date*</span></span>

<span data-ttu-id="d351b-110">En datoverdi som representerer sluttdatoen for beregningen av antall dager.</span><span class="sxs-lookup"><span data-stu-id="d351b-110">A date value that represents the end date for the calculation of the number of days.</span></span>

## <a name="return-values"></a><span data-ttu-id="d351b-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="d351b-111">Return values</span></span>

<span data-ttu-id="d351b-112">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="d351b-112">*Integer*</span></span>

<span data-ttu-id="d351b-113">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="d351b-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d351b-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="d351b-114">Usage notes</span></span>

<span data-ttu-id="d351b-115">`DAYS` returnerer en positiv verdi når den første datoen er senere enn den andre datoen, returnerer **0** (null) når den første datoen er lik den andre datoen, og returnerer en negativ verdi når den første datoen er før den andre datoen.</span><span class="sxs-lookup"><span data-stu-id="d351b-115">The `DAYS` function returns a positive value when the first date is later than the second date, it returns **0** (zero) when the first date equals the second date, and it returns a negative value when the first date is earlier than the second date.</span></span>

## <a name="example"></a><span data-ttu-id="d351b-116">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d351b-116">Example</span></span>

<span data-ttu-id="d351b-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returnerer **-1**.</span><span class="sxs-lookup"><span data-stu-id="d351b-117">`DAYS (TODAY (), DATEVALUE( DATETIMEFORMAT( ADDDAYS ( NOW(), 1), "yyyyMMdd"), "yyyyMMdd"))` returns **-1**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d351b-118">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d351b-118">Additional resources</span></span>

[<span data-ttu-id="d351b-119">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="d351b-119">Date and time functions</span></span>](er-functions-category-datetime.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]