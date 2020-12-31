---
title: PLIT ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SPLIT.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e1f11d68b697fdd363f429e60a79f1e1f97bab5b
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686398"
---
# <a name="split-er-function"></a><span data-ttu-id="928e7-103">PLIT ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="928e7-103">SPLIT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="928e7-104">`SPLIT`-funksjonen deler den angitte inndatastrengen inn i delstrenger og returnerer resultatet som en ny *Postliste*-verdi.</span><span class="sxs-lookup"><span data-stu-id="928e7-104">The `SPLIT` function splits the specified input string into substrings and returns the result as a new *Record list* value.</span></span>

## <a name="syntax-1"></a><span data-ttu-id="928e7-105">Syntaks 1</span><span class="sxs-lookup"><span data-stu-id="928e7-105">Syntax 1</span></span>

```vb
SPLIT (input, length)
```

<span data-ttu-id="928e7-106">Denne syntaksen brukes til å dele opp den angitte inndatastrengen i delstrenger, der hver har den angitte lengden.</span><span class="sxs-lookup"><span data-stu-id="928e7-106">This syntax is used to split the specified input string into substrings, each of which has the specified length.</span></span>

## <a name="syntax-2"></a><span data-ttu-id="928e7-107">Syntaks 2</span><span class="sxs-lookup"><span data-stu-id="928e7-107">Syntax 2</span></span>

```vb
SPLIT (input, delimiter)
```

<span data-ttu-id="928e7-108">Denne syntaksen brukes til å dele opp den angitte inndatastrengen i delstrenger, basert på det angitte skilletegnet.</span><span class="sxs-lookup"><span data-stu-id="928e7-108">This syntax is used to split the specified input string into substrings, based on the specified delimiter.</span></span>

## <a name="arguments"></a><span data-ttu-id="928e7-109">Argumenter</span><span class="sxs-lookup"><span data-stu-id="928e7-109">Arguments</span></span>

<span data-ttu-id="928e7-110">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="928e7-110">`input`: *String*</span></span>

<span data-ttu-id="928e7-111">Teksten som skal deles opp.</span><span class="sxs-lookup"><span data-stu-id="928e7-111">The text to split.</span></span>

<span data-ttu-id="928e7-112">`length`: *Heltall*</span><span class="sxs-lookup"><span data-stu-id="928e7-112">`length`: *Integer*</span></span>

<span data-ttu-id="928e7-113">Maksimumslengden på en enkelt delstreng.</span><span class="sxs-lookup"><span data-stu-id="928e7-113">The maximum length of a single substring.</span></span>

<span data-ttu-id="928e7-114">`delimiter`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="928e7-114">`delimiter`: *String*</span></span>

<span data-ttu-id="928e7-115">Et skilletegn som brukes til å skille delstrenger.</span><span class="sxs-lookup"><span data-stu-id="928e7-115">A delimiter that is used to separate substrings.</span></span>

## <a name="return-values"></a><span data-ttu-id="928e7-116">Returverdier</span><span class="sxs-lookup"><span data-stu-id="928e7-116">Return values</span></span>

<span data-ttu-id="928e7-117">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="928e7-117">*Record list*</span></span>

<span data-ttu-id="928e7-118">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="928e7-118">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="928e7-119">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="928e7-119">Usage notes</span></span>

<span data-ttu-id="928e7-120">Poststrukturen for listen som returneres, består av **Verdi**-feltet for *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="928e7-120">The record structure of the list that is returned consists of the **Value** field of the *String* type.</span></span> <span data-ttu-id="928e7-121">Hver post i listen som returneres, inneholder genererte delstrenger i dette feltet.</span><span class="sxs-lookup"><span data-stu-id="928e7-121">Every record of the list that is returned contains generated substrings in this field.</span></span>

<span data-ttu-id="928e7-122">Hvis `delimiter`-argumentet er tomt, består den nye listen som returneres, av én post som har **Verdi**-feltet av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="928e7-122">If the `delimiter` argument is empty, the new list that is returned consists of one record that has the **Value** field of the *String* type.</span></span> <span data-ttu-id="928e7-123">Dette feltet viser inndatateksten.</span><span class="sxs-lookup"><span data-stu-id="928e7-123">This field contains the input text.</span></span>

<span data-ttu-id="928e7-124">Hvis `input`-argumentet er tomt, returneres det en ny, tom liste.</span><span class="sxs-lookup"><span data-stu-id="928e7-124">If the `input` argument is empty, a new empty list is returned.</span></span> <span data-ttu-id="928e7-125">Hvis enten `input` eller `delimiter`-argumentet ikke er angitt (null), iverksettes et programunntak.</span><span class="sxs-lookup"><span data-stu-id="928e7-125">If either the `input` or `delimiter` argument is unspecified (null), an application exception is thrown.</span></span>

## <a name="example-1"></a><span data-ttu-id="928e7-126">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="928e7-126">Example 1</span></span>

<span data-ttu-id="928e7-127">`SPLIT ("abcd", 3)` returnerer en ny liste som består av to poster som har **Verdi**-feltet av *Streng* typen.</span><span class="sxs-lookup"><span data-stu-id="928e7-127">`SPLIT ("abcd", 3)` returns a new list that consists of two records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="928e7-128">**Verdi**-feltet i den første posten inneholder teksten **"abc"**, og **Verdi**-feltet i den andre posten inneholder teksten **"d"**.</span><span class="sxs-lookup"><span data-stu-id="928e7-128">The **Value** field in the first record contains the text **"abc"**, and the **Value** field in the second record contains the text **"d"**.</span></span>

## <a name="example-2"></a><span data-ttu-id="928e7-129">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="928e7-129">Example 2</span></span>

<span data-ttu-id="928e7-130">`SPLIT ("XAb aBy", "aB")` returnerer en ny liste som består av tre poster som har **Verdi**-feltet av *Streng* typen.</span><span class="sxs-lookup"><span data-stu-id="928e7-130">`SPLIT ("XAb aBy", "aB")` returns a new list that consists of three records that have the **Value** field of the *String* type.</span></span> <span data-ttu-id="928e7-131">**Verdi**-feltet i den første posten inneholder teksten **"X"**, **Verdi**-feltet i den andre posten inneholder teksten **"&nbsp;"**, og **Verdi**-feltet i den tredje posten inneholder teksten **"y"**.</span><span class="sxs-lookup"><span data-stu-id="928e7-131">The **Value** field in the first record contains the text **"X"**, the **Value** field in the second record contains the text **"&nbsp;"**, and the **Value** field in the third record contains the text **"y"**.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="928e7-132">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="928e7-132">Additional resources</span></span>

[<span data-ttu-id="928e7-133">Listefunksjoner</span><span class="sxs-lookup"><span data-stu-id="928e7-133">List functions</span></span>](er-functions-category-list.md)
