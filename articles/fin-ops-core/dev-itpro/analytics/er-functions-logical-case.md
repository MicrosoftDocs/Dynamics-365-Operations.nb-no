---
title: CASE ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen CASE
author: NickSelin
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
ms.openlocfilehash: 44815160957922f508fccd72174be2c4145a8d89
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5745455"
---
# <a name="case-er-function"></a><span data-ttu-id="19bd0-103">CASE ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="19bd0-103">CASE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="19bd0-104">`CASE`-funksjonen evaluerer verdien til det angitte uttrykket mot de angitte alternative valgene, og returnerer resultatet av det første alternativet som tilsvarer verdien til det angitte uttrykket.</span><span class="sxs-lookup"><span data-stu-id="19bd0-104">The `CASE` function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="19bd0-105">Hvis ikke returnerer den et valgfritt standard resultat hvis et standard resultat er angitt som det siste argumentet i den kalte funksjonen som ikke innledes av et alternativ.</span><span class="sxs-lookup"><span data-stu-id="19bd0-105">Otherwise, it returns the optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="19bd0-106">Verdien som returneres, kan være en verdi for en hvilken som helst av de støttede datatypene.</span><span class="sxs-lookup"><span data-stu-id="19bd0-106">The value that is returned can be a value of any of the supported data types.</span></span>

## <a name="syntax"></a><span data-ttu-id="19bd0-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="19bd0-107">Syntax</span></span>

```vb
CASE (expression, option 1, result 1[, option 2, result 2, …, option N, result N, default result])
```

## <a name="arguments"></a><span data-ttu-id="19bd0-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="19bd0-108">Arguments</span></span>

<span data-ttu-id="19bd0-109">`expression`: *Primitiv datatype* (boolsk, numerisk eller tekst)</span><span class="sxs-lookup"><span data-stu-id="19bd0-109">`expression`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="19bd0-110">Et gyldig uttrykk som returnerer en verdi av den primitive datatypen.</span><span class="sxs-lookup"><span data-stu-id="19bd0-110">A valid expression that returns a value of the primitive data type.</span></span>

<span data-ttu-id="19bd0-111">`option 1`: *Primitiv datatype* (boolsk, numerisk eller tekst)</span><span class="sxs-lookup"><span data-stu-id="19bd0-111">`option 1`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="19bd0-112">Et gyldig uttrykk som returnerer en verdi av den samme primitive datatypen som `expression`-argumentet for den kalte funksjonen.</span><span class="sxs-lookup"><span data-stu-id="19bd0-112">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="19bd0-113">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="19bd0-113">This argument is required.</span></span>

<span data-ttu-id="19bd0-114">`result 1`: *Hvilken som helst av datatypene som støttes*</span><span class="sxs-lookup"><span data-stu-id="19bd0-114">`result 1`: *Any of the supported data types*</span></span>

<span data-ttu-id="19bd0-115">Det returnerte resultatet som svarer til det forrige alternativet.</span><span class="sxs-lookup"><span data-stu-id="19bd0-115">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="19bd0-116">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="19bd0-116">This argument is required.</span></span>

<span data-ttu-id="19bd0-117">`option N`: *Primitiv datatype* (boolsk, numerisk eller tekst)</span><span class="sxs-lookup"><span data-stu-id="19bd0-117">`option N`: *Primitive data type* (Boolean, numeric, or text)</span></span>

<span data-ttu-id="19bd0-118">Et gyldig uttrykk som returnerer en verdi av den samme primitive datatypen som `expression`-argumentet for den kalte funksjonen.</span><span class="sxs-lookup"><span data-stu-id="19bd0-118">A valid expression that returns a value of the same primitive data type as the `expression` argument of the called function.</span></span> <span data-ttu-id="19bd0-119">Dette argumentet er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="19bd0-119">This argument is optional.</span></span>

<span data-ttu-id="19bd0-120">`result N`: *Hvilken som helst av datatypene som støttes*</span><span class="sxs-lookup"><span data-stu-id="19bd0-120">`result N`: *Any of the supported data types*</span></span>

<span data-ttu-id="19bd0-121">Det returnerte resultatet som svarer til det forrige alternativet.</span><span class="sxs-lookup"><span data-stu-id="19bd0-121">The returned result that corresponds to the preceding option.</span></span> <span data-ttu-id="19bd0-122">Dette argumentet er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="19bd0-122">This argument is optional.</span></span>

<span data-ttu-id="19bd0-123">`default result`: *Hvilken som helst av datatypene som støttes*</span><span class="sxs-lookup"><span data-stu-id="19bd0-123">`default result`: *Any of the supported data types*</span></span>

<span data-ttu-id="19bd0-124">Resultatet som skal returneres hvis det ikke finnes noen treff.</span><span class="sxs-lookup"><span data-stu-id="19bd0-124">The result that should be returned if there is no match.</span></span> <span data-ttu-id="19bd0-125">Dette argumentet er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="19bd0-125">This argument is optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="19bd0-126">Returverdier</span><span class="sxs-lookup"><span data-stu-id="19bd0-126">Return values</span></span>

<span data-ttu-id="19bd0-127">*Hvilken som helst av datatypene som støttes*</span><span class="sxs-lookup"><span data-stu-id="19bd0-127">*Any of the supported data types*</span></span>

<span data-ttu-id="19bd0-128">Resultatverdien for en hvilken som helst av de støttede datatypene.</span><span class="sxs-lookup"><span data-stu-id="19bd0-128">The resulting value of any of the supported data types.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="19bd0-129">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="19bd0-129">Usage notes</span></span>

<span data-ttu-id="19bd0-130">Det oppstår et unntak under kjøring hvis det ikke finnes noen samsvar og et valgfritt standardresultat ikke er definert.</span><span class="sxs-lookup"><span data-stu-id="19bd0-130">An exception is thrown at runtime if there is no match and an optional default result isn't defined.</span></span>

<span data-ttu-id="19bd0-131">Alle resultater må angis ved hjelp av den samme datatypen.</span><span class="sxs-lookup"><span data-stu-id="19bd0-131">All results must be specified by using the same data type.</span></span> <span data-ttu-id="19bd0-132">Et unntak er registrert ved utformingstid hvis datatypene for de konfigurerte resultatene ikke samsvarer.</span><span class="sxs-lookup"><span data-stu-id="19bd0-132">An exception is thrown at design time if the data types of the configured results don't match.</span></span>

<span data-ttu-id="19bd0-133">Hvis den første resultatverdien og *N*-te resultatverdien er verdier for datatypen *Container (post)* eller *postliste*, har resultatet bare feltene som finnes i begge verdiene.</span><span class="sxs-lookup"><span data-stu-id="19bd0-133">If the first result value and the *N* th result value are values of the *Container (record)* or *Record list* data type, the result has only the fields that exist in both values.</span></span>

## <a name="example"></a><span data-ttu-id="19bd0-134">Eksempel</span><span class="sxs-lookup"><span data-stu-id="19bd0-134">Example</span></span>

<span data-ttu-id="19bd0-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returnerer strengen **"WINTER"** hvis gjeldende programøktdato er mellom oktober og desember.</span><span class="sxs-lookup"><span data-stu-id="19bd0-135">`CASE( DATETIMEFORMAT( NOW(), "MM"), "10", "WINTER", "11", "WINTER", "12", "WINTER", "")` returns the string **"WINTER"** if the current application session date is between October and December.</span></span> <span data-ttu-id="19bd0-136">Ellers returneres en tom streng.</span><span class="sxs-lookup"><span data-stu-id="19bd0-136">Otherwise, it returns a blank string.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="19bd0-137">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="19bd0-137">Additional resources</span></span>

[<span data-ttu-id="19bd0-138">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="19bd0-138">Logical functions</span></span>](er-functions-category-logical.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]