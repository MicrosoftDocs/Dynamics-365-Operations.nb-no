---
title: CONVERTCURRENCY ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CONVERTCURRENCY.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 0f0d5bace9b62cf6f0d7576744a6cc271666bf73
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567646"
---
# <a name="convertcurrency-er-function"></a><span data-ttu-id="1f6c1-103">CONVERTCURRENCY ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="1f6c1-103">CONVERTCURRENCY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f6c1-104">`CONVERTCURRENCY`-funksjonen returnerer en *reell* verdi som representerer resultatet av å konvertere det angitte pengebeløpet fra den angitte kildevalutaen til den angitte målvalutaen ved å bruke innstillingene for det aktuelle firmaet på den angitte datoen.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f6c1-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="1f6c1-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="1f6c1-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="1f6c1-106">Arguments</span></span>

<span data-ttu-id="1f6c1-107">`amount`: *Heltall* eller *Reell*</span><span class="sxs-lookup"><span data-stu-id="1f6c1-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="1f6c1-108">En numerisk verdi som representerer pengebeløpet som må konverteres.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="1f6c1-109">`source currency`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="1f6c1-109">`source currency`: *String*</span></span>

<span data-ttu-id="1f6c1-110">Koden for kildevalutaen.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-110">The code of the source currency.</span></span>

<span data-ttu-id="1f6c1-111">`target currency`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="1f6c1-111">`target currency`: *String*</span></span>

<span data-ttu-id="1f6c1-112">Koden for målvalutaen.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-112">The code of the target currency.</span></span>

<span data-ttu-id="1f6c1-113">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="1f6c1-113">`date`: *Date*</span></span>

<span data-ttu-id="1f6c1-114">En *dato*-verdi som representerer datoen som brukes til å bestemme valutakursen for konverteringen.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="1f6c1-115">`company`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="1f6c1-115">`company`: *String*</span></span>

<span data-ttu-id="1f6c1-116">En *streng*-verdi som representerer koden til et selskap som leverer innstillingene som brukes for konverteringen.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="1f6c1-117">Returverdier</span><span class="sxs-lookup"><span data-stu-id="1f6c1-117">Return values</span></span>

<span data-ttu-id="1f6c1-118">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="1f6c1-118">*Real*</span></span>

<span data-ttu-id="1f6c1-119">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="1f6c1-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="1f6c1-120">Example</span></span>

<span data-ttu-id="1f6c1-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returnerer tilsvarende én euro i amerikanske dollar på gjeldende øktdato, basert på innstillingene for **DEMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="1f6c1-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f6c1-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1f6c1-122">Additional resources</span></span>

[<span data-ttu-id="1f6c1-123">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="1f6c1-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]