---
title: GETCURRENTCOMPANY ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen GETCURRENTCOMPANY.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3e14c6a8aaff0a32a115117938d0e853bb34bb14
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684865"
---
# <a name="getcurrentcompany-er-function"></a><span data-ttu-id="c0037-103">GETCURRENTCOMPANY ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="c0037-103">GETCURRENTCOMPANY ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c0037-104">`GETCURRENTCOMPANY`-funksjonen returnerer en *streng*-verdi som representerer koden for den juridiske enheten (firma) som en bruker er logget på nå.</span><span class="sxs-lookup"><span data-stu-id="c0037-104">The `GETCURRENTCOMPANY` function returns a *String* value that represents the code for the legal entity (company) that a user is currently signed in to.</span></span>

## <a name="syntax"></a><span data-ttu-id="c0037-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="c0037-105">Syntax</span></span>

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a><span data-ttu-id="c0037-106">Returverdier</span><span class="sxs-lookup"><span data-stu-id="c0037-106">Return values</span></span>

<span data-ttu-id="c0037-107">*Streng*</span><span class="sxs-lookup"><span data-stu-id="c0037-107">*String*</span></span>

<span data-ttu-id="c0037-108">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="c0037-108">The resulting text value.</span></span>

## <a name="example"></a><span data-ttu-id="c0037-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="c0037-109">Example</span></span>

<span data-ttu-id="c0037-110">`GETCURRENTCOMPANY ()` returnerer **USMF** for en bruker som er logget på firmaet **Contoso Entertainment System USA**.</span><span class="sxs-lookup"><span data-stu-id="c0037-110">`GETCURRENTCOMPANY ()` returns **USMF** for a user who is signed in to the **Contoso Entertainment System USA** company.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c0037-111">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="c0037-111">Additional resources</span></span>

[<span data-ttu-id="c0037-112">Andre funksjoner (spesifikke for forretningsområder)</span><span class="sxs-lookup"><span data-stu-id="c0037-112">Other (business domain–specific) functions</span></span>](er-functions-category-other.md)
