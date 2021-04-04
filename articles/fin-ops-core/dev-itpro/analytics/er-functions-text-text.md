---
title: TEXT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen TEXT
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: 5da7375020be827f432ba97740da37abe48962fc
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5560067"
---
# <a name="text-er-function"></a><span data-ttu-id="989ee-103">TEXT ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="989ee-103">TEXT ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="989ee-104">`TEXT`-funksjonen returnerer det angitte tallet som en *streng*-verdi etter at de er konvertert til en tekststreng som formateres i henhold til de nasjonale innstillingene for serveren for gjeldende forekomst av programmet.</span><span class="sxs-lookup"><span data-stu-id="989ee-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="989ee-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="989ee-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="989ee-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="989ee-106">Arguments</span></span>

<span data-ttu-id="989ee-107">`number`: *Heltall* eller *Reell*</span><span class="sxs-lookup"><span data-stu-id="989ee-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="989ee-108">Et nummer som må konverteres til en tekststreng.</span><span class="sxs-lookup"><span data-stu-id="989ee-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="989ee-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="989ee-109">Return values</span></span>

<span data-ttu-id="989ee-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="989ee-110">*String*</span></span>

<span data-ttu-id="989ee-111">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="989ee-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="989ee-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="989ee-112">Usage notes</span></span>

<span data-ttu-id="989ee-113">For verdier for *reell*-typen begrenses strengkonverteringen til to desimalplasser.</span><span class="sxs-lookup"><span data-stu-id="989ee-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="989ee-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="989ee-114">Example</span></span>

<span data-ttu-id="989ee-115">Hvis de nasjonale innstillingene for Microsoft Dynamics 365 Finance-forekomstens server er definert som **EN-US**, returnerer `TEXT (NOW ())` gjeldende dato for programøkten, 17. desember 2015, som tekststrengen **"12/17/2015 07:59:23 AM"**.</span><span class="sxs-lookup"><span data-stu-id="989ee-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="989ee-116">`TEXT (1/3)` returnerer **"0.33"**.</span><span class="sxs-lookup"><span data-stu-id="989ee-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="989ee-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="989ee-117">Additional resources</span></span>

[<span data-ttu-id="989ee-118">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="989ee-118">Text functions</span></span>](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]