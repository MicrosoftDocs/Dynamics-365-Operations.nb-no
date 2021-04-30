---
title: PLIT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SPLIT.
author: NickSelin
ms.date: 04/01/2021
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
ms.openlocfilehash: 26b6ddeb2880fc220283b6389327a497549a4511
ms.sourcegitcommit: 74f5b04b482b2ae023c728e0df0eb78305493c6a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2021
ms.locfileid: "5853449"
---
# <a name="split-er-function"></a><span data-ttu-id="bbdf5-103">PLIT ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="bbdf5-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bbdf5-104">`SPLIT`-funksjonen deler den angitte inndatastrengen inn i delstrenger og returnerer resultatet som en ny *Postliste*-verdi.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="bbdf5-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="bbdf5-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="bbdf5-106">Denne syntaksen brukes til å dele opp den angitte inndatastrengen i delstrenger, der hver har den angitte lengden.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="bbdf5-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="bbdf5-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="bbdf5-108">Denne syntaksen brukes til å dele opp den angitte inndatastrengen i delstrenger, basert på det angitte skilletegnet.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="bbdf5-109">Argumenter</span><span class="sxs-lookup"><span data-stu-id="bbdf5-109">Arguments</span></span>

<span data-ttu-id="bbdf5-110">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="bbdf5-110">`input`: *String*</span></span>

<span data-ttu-id="bbdf5-111">Teksten som skal deles opp.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-111">The text to split.</span></span>

<span data-ttu-id="bbdf5-112">`length`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="bbdf5-112">`length`: *Integer*</span></span>

<span data-ttu-id="bbdf5-113">Maksimumslengden på en enkelt delstreng.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="bbdf5-114">`delimiter`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="bbdf5-114">`delimiter`: *String*</span></span>

<span data-ttu-id="bbdf5-115">Et skilletegn som brukes til å skille delstrenger.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="bbdf5-116">Returverdier</span><span class="sxs-lookup"><span data-stu-id="bbdf5-116">Return values</span></span>

<span data-ttu-id="bbdf5-117">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="bbdf5-117">*Record list*</span></span>

<span data-ttu-id="bbdf5-118">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bbdf5-119">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="bbdf5-119">Usage notes</span></span>

<span data-ttu-id="bbdf5-120">Poststrukturen for listen som returneres, består av **Verdi**-feltet for *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="bbdf5-121">Hver post i listen som returneres, inneholder genererte delstrenger i dette feltet.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="bbdf5-122">Hvis `delimiter`-argumentet er tomt, består den nye listen som returneres, av én post som har **Verdi**-feltet av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="bbdf5-123">Dette feltet viser inndatateksten.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-123">This field contains the input text.</span></span>

<span data-ttu-id="bbdf5-124">Hvis `input`-argumentet er tomt, returneres det en ny, tom liste.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="bbdf5-125">Hvis enten `input` eller `delimiter`-argumentet ikke er angitt (null), iverksettes et programunntak.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="bbdf5-126">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="bbdf5-126">Example 1</span></span>

<span data-ttu-id="bbdf5-127">`SPLIT ("abcd", 3)` returnerer en ny liste som består av to poster som har **Verdi**-feltet av *Streng* typen.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="bbdf5-128">**Verdi**-feltet i den første posten inneholder teksten **"abc"**, og **Verdi**-feltet i den andre posten inneholder teksten **"d"**.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="bbdf5-129">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="bbdf5-129">Example 2</span></span>

<span data-ttu-id="bbdf5-130">`SPLIT ("XAb aBy", "aB")` returnerer en ny liste som består av tre poster som har **Verdi**-feltet av *Streng* typen.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="bbdf5-131">**Verdi**-feltet i den første posten inneholder teksten **"X"**, **Verdi**-feltet i den andre posten inneholder teksten **"&nbsp;"**, og **Verdi**-feltet i den tredje posten inneholder teksten **"y"**.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="example-3"></a><span data-ttu-id="bbdf5-132">Eksempel 3</span><span class="sxs-lookup"><span data-stu-id="bbdf5-132">Example 3</span></span>

<span data-ttu-id="bbdf5-133">Du kan bruke [INDEX](er-functions-list-index.md)-funksjonen til å få tilgang til individuelle elementer for den angitte inndatastrengen.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-133">Yo can use the [INDEX](er-functions-list-index.md) function to access individual elements of the specified input string.</span></span> <span data-ttu-id="bbdf5-134">Hvis du angir **MyList**-datakilden av **Beregnet felt**-typen og konfigurer den for `SPLIT("abc", 1)`-uttrykket, vil uttrykket `INDEX(MyList,2).Value` returnere teksten **"b"**.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-134">If you enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, the expression `INDEX(MyList,2).Value` returns the text **"b"**.</span></span>

## <a name="example-4"></a><span data-ttu-id="bbdf5-135">Eksempel 4</span><span class="sxs-lookup"><span data-stu-id="bbdf5-135">Example 4</span></span>

<span data-ttu-id="bbdf5-136">[ENUMERATE](er-functions-list-enumerate.md)-funksjonen kan også hjelpe deg med å få tilgang til individuelle elementer for den angitte inndatastrengen.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-136">The [ENUMERATE](er-functions-list-enumerate.md) function can also help you access individual elements of the specified input string.</span></span> <span data-ttu-id="bbdf5-137">Hvis du først angir **MyList**-datakilden av **Beregnet felt**-typen og konfigurer `SPLIT("abc", 1)`-uttrykket for den og deretter angir **EnumeratedList**-datakilden av **Beregnet felt**-typen og konfigurer `ENUMERATE(MyList)`-uttrykket for den, returnerer uttrykket `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` teksten **"b"**.</span><span class="sxs-lookup"><span data-stu-id="bbdf5-137">If you first enter the **MyList** data source of the **Calculated field** type and configure for it the `SPLIT("abc", 1)` expression, and then enter the **EnumeratedList** data source of the **Calculated field** type and configure for it the `ENUMERATE(MyList)` expression, the expression `FIRSTORNULL(WHERE(EnumeratedList, EnumeratedList.Number=2)).Value` returns the text **"b"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bbdf5-138">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bbdf5-138">Additional resources</span></span>

[<span data-ttu-id="bbdf5-139">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="bbdf5-139">List functions</span></span>](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
