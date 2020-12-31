---
title: SESSIONNOW ER-funksjon
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SESSIONNOW.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: d70acb06194a28af0cc85eea440e9e4e937bc3bb
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683849"
---
# <a name="sessionnow-er-function"></a><span data-ttu-id="b105f-103">SESSIONNOW ER-funksjon</span><span class="sxs-lookup"><span data-stu-id="b105f-103">SESSIONNOW ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b105f-104">`SESSIONNOW`-funksjonen returnerer en *DateTime*-verdi som representerer gjeldende dato og klokkeslett for programøkt.</span><span class="sxs-lookup"><span data-stu-id="b105f-104">The `SESSIONNOW` function returns a *DateTime* value that represents the current application session date and time.</span></span>

## <a name="syntax"></a><span data-ttu-id="b105f-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="b105f-105">Syntax</span></span>

```vb
SESSIONNOW ()
```

## <a name="return-values"></a><span data-ttu-id="b105f-106">Returverdier</span><span class="sxs-lookup"><span data-stu-id="b105f-106">Return values</span></span>

<span data-ttu-id="b105f-107">*DateTime*</span><span class="sxs-lookup"><span data-stu-id="b105f-107">*DateTime*</span></span>

<span data-ttu-id="b105f-108">Den resulterende dato/klokkeslett-verdien.</span><span class="sxs-lookup"><span data-stu-id="b105f-108">The resulting date/time value.</span></span>

## <a name="example"></a><span data-ttu-id="b105f-109">Eksempel</span><span class="sxs-lookup"><span data-stu-id="b105f-109">Example</span></span>

<span data-ttu-id="b105f-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returnerer gjeldende dato/klokkeslett-verdi for programøkt, 24. desember 2015, som **"24.12.2015"**, basert på den valgte tyske kulturen og det angitte formatet.</span><span class="sxs-lookup"><span data-stu-id="b105f-110">`DATETIMEFORMAT (SESSIONNOW(), "d", "DE")` returns the current application session date/time value, December 24, 2015, as **"24.12.2015"**, based on the selected German culture and the specified format.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b105f-111">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="b105f-111">Additional resources</span></span>

[<span data-ttu-id="b105f-112">Dato- og klokkeslettfunksjoner</span><span class="sxs-lookup"><span data-stu-id="b105f-112">Date and time functions</span></span>](er-functions-category-datetime.md)
