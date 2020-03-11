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
ms.openlocfilehash: 1d0c168e07252f7c423271bc808f3fca3834077f
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041521"
---
# <span data-ttu-id="2e22a-103"><a name="CONVERTCURRENCY">CONVERTCURRENCY ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="2e22a-103"><a name="CONVERTCURRENCY">CONVERTCURRENCY ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="2e22a-104">`CONVERTCURRENCY`-funksjonen returnerer en *reell* verdi som representerer resultatet av å konvertere det angitte pengebeløpet fra den angitte kildevalutaen til den angitte målvalutaen ved å bruke innstillingene for det aktuelle firmaet på den angitte datoen.</span><span class="sxs-lookup"><span data-stu-id="2e22a-104">The `CONVERTCURRENCY` function returns a *Real* value that represents the result of converting the specified monetary amount from the specified source currency to the specified target currency by using the settings of the specified company on the specified date.</span></span>

## <a name="syntax"></a><span data-ttu-id="2e22a-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="2e22a-105">Syntax</span></span>

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a><span data-ttu-id="2e22a-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="2e22a-106">Arguments</span></span>

<span data-ttu-id="2e22a-107">`amount`: *Heltall* eller *Reell*</span><span class="sxs-lookup"><span data-stu-id="2e22a-107">`amount`: *Integer* or *Real*</span></span>

<span data-ttu-id="2e22a-108">En numerisk verdi som representerer pengebeløpet som må konverteres.</span><span class="sxs-lookup"><span data-stu-id="2e22a-108">A numeric value that represents the monetary amount that must be converted.</span></span>

<span data-ttu-id="2e22a-109">`source currency`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="2e22a-109">`source currency`: *String*</span></span>

<span data-ttu-id="2e22a-110">Koden for kildevalutaen.</span><span class="sxs-lookup"><span data-stu-id="2e22a-110">The code of the source currency.</span></span>

<span data-ttu-id="2e22a-111">`target currency`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="2e22a-111">`target currency`: *String*</span></span>

<span data-ttu-id="2e22a-112">Koden for målvalutaen.</span><span class="sxs-lookup"><span data-stu-id="2e22a-112">The code of the target currency.</span></span>

<span data-ttu-id="2e22a-113">`date`: *Dato*</span><span class="sxs-lookup"><span data-stu-id="2e22a-113">`date`: *Date*</span></span>

<span data-ttu-id="2e22a-114">En *dato*-verdi som representerer datoen som brukes til å bestemme valutakursen for konverteringen.</span><span class="sxs-lookup"><span data-stu-id="2e22a-114">A *Date* value that represents the date that is used to determine the exchange rate for the conversion.</span></span>

<span data-ttu-id="2e22a-115">`company`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="2e22a-115">`company`: *String*</span></span>

<span data-ttu-id="2e22a-116">En *streng*-verdi som representerer koden til et selskap som leverer innstillingene som brukes for konverteringen.</span><span class="sxs-lookup"><span data-stu-id="2e22a-116">A *String* value that represents the code of a company that supplies the settings that are used for the conversion.</span></span>

## <a name="return-values"></a><span data-ttu-id="2e22a-117">Returverdier</span><span class="sxs-lookup"><span data-stu-id="2e22a-117">Return values</span></span>

<span data-ttu-id="2e22a-118">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="2e22a-118">*Real*</span></span>

<span data-ttu-id="2e22a-119">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="2e22a-119">The resulting numeric value.</span></span>

## <a name="example"></a><span data-ttu-id="2e22a-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="2e22a-120">Example</span></span>

<span data-ttu-id="2e22a-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returnerer tilsvarende én euro i amerikanske dollar på gjeldende øktdato, basert på innstillingene for **DEMF**-firmaet.</span><span class="sxs-lookup"><span data-stu-id="2e22a-121">`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returns the equivalent of one euro in US dollars on the current session date, based on settings for the **DEMF** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2e22a-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="2e22a-122">Additional resources</span></span>

[<span data-ttu-id="2e22a-123">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="2e22a-123">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
