---
title: CONVERTCURRENCY ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CONVERTCURRENCY.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: bf972c6c2cc798811a9fb3bd3a355ac6ffca5a60
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915953"
---
# <span data-ttu-id="e3120-103"><a name="CONVERTCURRENCY">CONVERTCURRENCY ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="e3120-103"><a name="CONVERTCURRENCY">CONVERTCURRENCY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e3120-104">`CONVERTCURRENCY`-funksjonen returnerer en *reell* verdi som representerer resultatet av å konvertere det angitte pengebeløpet fra den angitte kildevalutaen til den angitte målvalutaen ved å bruke innstillingene for det aktuelle firmaet på den angitte datoen.</span><span class="sxs-lookup"><span data-stu-id="e3120-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="e3120-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="e3120-105">Syntax</span></span>

```
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="e3120-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="e3120-106">Arguments</span></span>

<span data-ttu-id="e3120-107">`amount`: *Heltall* eller *Reell*</span><span class="sxs-lookup"><span data-stu-id="e3120-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="e3120-108">En numerisk verdi som representerer pengebeløpet som må konverteres.</span><span class="sxs-lookup"><span data-stu-id="e3120-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="e3120-109">`source currency`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="e3120-109">`source currency`: *String*</span></span>

<span data-ttu-id="e3120-110">Koden for kildevalutaen.</span><span class="sxs-lookup"><span data-stu-id="e3120-110">The code of the source currency.</span></span>

<span data-ttu-id="e3120-111">`target currency`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="e3120-111">`target currency`: *String*</span></span>

<span data-ttu-id="e3120-112">Koden for målvalutaen.</span><span class="sxs-lookup"><span data-stu-id="e3120-112">The code of the target currency.</span></span>

<span data-ttu-id="e3120-113">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="e3120-113">`date`: *Date*</span></span>

<span data-ttu-id="e3120-114">En *dato*-verdi som representerer datoen som brukes til å bestemme valutakursen for konverteringen.</span><span class="sxs-lookup"><span data-stu-id="e3120-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="e3120-115">`company`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="e3120-115">`company`: *String*</span></span>

<span data-ttu-id="e3120-116">En *streng*-verdi som representerer koden til et selskap som leverer innstillingene som brukes for konverteringen.</span><span class="sxs-lookup"><span data-stu-id="e3120-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="e3120-117">Returverdier</span><span class="sxs-lookup"><span data-stu-id="e3120-117">Return values</span></span>

<span data-ttu-id="e3120-118">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="e3120-118">*Real*</span></span>

<span data-ttu-id="e3120-119">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="e3120-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="e3120-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="e3120-120">Example</span></span>

<span data-ttu-id="e3120-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returnerer tilsvarende én euro i amerikanske dollar på gjeldende øktdato, basert på innstillingene for **DEMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="e3120-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3120-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="e3120-122">Additional resources</span></span>

[<span data-ttu-id="e3120-123">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="e3120-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
