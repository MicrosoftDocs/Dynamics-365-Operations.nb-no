---
title: TEXT ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen TEXT
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: c08aca949ffc7e62009bf3f6c664d96b368f43e7
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040903"
---
# <span data-ttu-id="4f00d-103"><a name="TEXT">TEXT ER-funksjon</a></span><span class="sxs-lookup"><span data-stu-id="4f00d-103"><a name="TEXT">TEXT ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4f00d-104">`TEXT`-funksjonen returnerer det angitte tallet som en *streng*-verdi etter at de er konvertert til en tekststreng som formateres i henhold til de nasjonale innstillingene for serveren for gjeldende forekomst av programmet.</span><span class="sxs-lookup"><span data-stu-id="4f00d-104">The `TEXT` function returns the specified number as a *String* value after it has been converted to a text string that is formatted according to the server locale settings of the current application instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="4f00d-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="4f00d-105">Syntax</span></span>

```vb
TEXT (number)
```

## <a name="arguments"></a><span data-ttu-id="4f00d-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="4f00d-106">Arguments</span></span>

<span data-ttu-id="4f00d-107">`number`: *Heltall* eller *Reell*</span><span class="sxs-lookup"><span data-stu-id="4f00d-107">`number`: *Integer* or *Real*</span></span>

<span data-ttu-id="4f00d-108">Et nummer som må konverteres til en tekststreng.</span><span class="sxs-lookup"><span data-stu-id="4f00d-108">A number that must be converted to a text string.</span></span>

## <a name="return-values"></a><span data-ttu-id="4f00d-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="4f00d-109">Return values</span></span>

<span data-ttu-id="4f00d-110">*Streng*</span><span class="sxs-lookup"><span data-stu-id="4f00d-110">*String*</span></span>

<span data-ttu-id="4f00d-111">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="4f00d-111">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="4f00d-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="4f00d-112">Usage notes</span></span>

<span data-ttu-id="4f00d-113">For verdier for *reell*-typen begrenses strengkonverteringen til to desimalplasser.</span><span class="sxs-lookup"><span data-stu-id="4f00d-113">For values of the *Real* type, the string conversion is limited to two decimal places.</span></span>

## <a name="example"></a><span data-ttu-id="4f00d-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="4f00d-114">Example</span></span>

<span data-ttu-id="4f00d-115">Hvis de nasjonale innstillingene for Microsoft Dynamics 365 Finance-forekomstens server er definert som **EN-US**, returnerer `TEXT (NOW ())` gjeldende dato for programøkten, 17. desember 2015, som tekststrengen **"12/17/2015 07:59:23 AM"**.</span><span class="sxs-lookup"><span data-stu-id="4f00d-115">If the server locale of the Microsoft Dynamics 365 Finance instance is defined as **EN-US**, `TEXT (NOW ())` returns the current Finance session date, December 17, 2015, as the text string **"12/17/2015 07:59:23 AM"**.</span></span> <span data-ttu-id="4f00d-116">`TEXT (1/3)` returnerer **"0.33"**.</span><span class="sxs-lookup"><span data-stu-id="4f00d-116">`TEXT (1/3)` returns **"0.33"**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4f00d-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="4f00d-117">Additional resources</span></span>

[<span data-ttu-id="4f00d-118">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="4f00d-118">Text functions</span></span>](er-functions-category-text.md)
