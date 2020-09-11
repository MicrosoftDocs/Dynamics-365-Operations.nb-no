---
title: Liste over ER-funksjoner i den logiske kategorien
description: Dette emnet inneholder informasjon om de logiske funksjonene som støttes i elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: e622778c60646e5cc84cd6e23a5d4954a0fe0bb3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705101"
---
# <a name="list-of-er-functions-in-the-logical-category"></a><span data-ttu-id="1b661-103">Liste over ER-funksjoner i den logiske kategorien</span><span class="sxs-lookup"><span data-stu-id="1b661-103">List of ER functions in the logical category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b661-104">Logiske funksjoner for elektronisk rapportering (ER) kan brukes til å arbeide med logiske verdier for å utføre mer enn én sammenligning i ett enkelt uttrykk eller teste flere betingelser.</span><span class="sxs-lookup"><span data-stu-id="1b661-104">Electronic reporting (ER) logical functions can be used to work with logical values to perform more than one comparison in a single expression or test multiple conditions.</span></span> <span data-ttu-id="1b661-105">Dette emnet inneholder et sammendrag av disse funksjonene.</span><span class="sxs-lookup"><span data-stu-id="1b661-105">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="1b661-106">Liste over funksjoner som støttes</span><span class="sxs-lookup"><span data-stu-id="1b661-106">List of supported functions</span></span>

| <span data-ttu-id="1b661-107">Funksjon</span><span class="sxs-lookup"><span data-stu-id="1b661-107">Function</span></span> | <span data-ttu-id="1b661-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="1b661-108">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="1b661-109">Og</span><span class="sxs-lookup"><span data-stu-id="1b661-109">And</span></span>](er-functions-logical-and.md)                       | <span data-ttu-id="1b661-110">Denne funksjonen returnerer en *boolsk* verdi av **SANN** hvis alle de angitte betingelsene er sanne.</span><span class="sxs-lookup"><span data-stu-id="1b661-110">This function returns a *Boolean* value of **TRUE** if all the specified conditions are true.</span></span> <span data-ttu-id="1b661-111">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="1b661-111">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="1b661-112">Sak</span><span class="sxs-lookup"><span data-stu-id="1b661-112">Case</span></span>](er-functions-logical-case.md)                     | <span data-ttu-id="1b661-113">Denne funksjonen evaluerer verdien til det angitte uttrykket mot de angitte alternative valgene, og returnerer resultatet av det første alternativet som tilsvarer verdien til det angitte uttrykket.</span><span class="sxs-lookup"><span data-stu-id="1b661-113">This function evaluates the value of the specified expression against the specified alternative options and returns the result of the first option that equals the value of the specified expression.</span></span> <span data-ttu-id="1b661-114">Hvis ikke returnerer den et valgfritt standard resultat hvis et standard resultat er angitt som det siste argumentet i den kalte funksjonen som ikke innledes av et alternativ.</span><span class="sxs-lookup"><span data-stu-id="1b661-114">Otherwise, it returns an optional default result, if a default result is specified as the last argument of the called function that isn't preceded by an option.</span></span> <span data-ttu-id="1b661-115">Verdien som returneres, kan være en verdi for en hvilken som helst av de støttede datatypene.</span><span class="sxs-lookup"><span data-stu-id="1b661-115">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="1b661-116">Hvis</span><span class="sxs-lookup"><span data-stu-id="1b661-116">If</span></span>](er-functions-logical-if.md)                         | <span data-ttu-id="1b661-117">Denne funksjonen returnerer den første verdien hvis den angitte betingelsen er oppfylt.</span><span class="sxs-lookup"><span data-stu-id="1b661-117">This function returns the first specified value if the specified condition is met.</span></span> <span data-ttu-id="1b661-118">Hvis ikke returneres den andre verdien som er angitt.</span><span class="sxs-lookup"><span data-stu-id="1b661-118">Otherwise, it returns the second specified value.</span></span> <span data-ttu-id="1b661-119">Verdien som returneres, kan være en verdi for en hvilken som helst av de støttede datatypene.</span><span class="sxs-lookup"><span data-stu-id="1b661-119">The value that is returned can be a value of any of the supported data types.</span></span> |
| [<span data-ttu-id="1b661-120">Ikke</span><span class="sxs-lookup"><span data-stu-id="1b661-120">Not</span></span>](er-functions-logical-not.md)                       | <span data-ttu-id="1b661-121">Denne funksjonen returnerer den omvendte logiske verdien til den angitte betingelsen som en *boolsk* verdi.</span><span class="sxs-lookup"><span data-stu-id="1b661-121">This function returns the reversed logical value of the specified condition as a *Boolean* value.</span></span> |
| [<span data-ttu-id="1b661-122">Or</span><span class="sxs-lookup"><span data-stu-id="1b661-122">Or</span></span>](er-functions-logical-or.md)                         | <span data-ttu-id="1b661-123">Denne funksjonen returnerer en *boolsk* verdi av **USANN** hvis alle de angitte betingelsene er usanne.</span><span class="sxs-lookup"><span data-stu-id="1b661-123">This function returns a *Boolean* value of **FALSE** if all the specified conditions are false.</span></span> <span data-ttu-id="1b661-124">Denne funksjonen returnerer en *boolsk* verdi av **SANN** hvis en angitt betingelse er sann.</span><span class="sxs-lookup"><span data-stu-id="1b661-124">If any specified condition is true, the function returns a *Boolean* value of **TRUE**.</span></span> |
| [<span data-ttu-id="1b661-125">ValueIn</span><span class="sxs-lookup"><span data-stu-id="1b661-125">ValueIn</span></span>](er-functions-logical-valuein.md)               | <span data-ttu-id="1b661-126">Denne funksjonen bestemmer om de angitte inndataene samsvarer med en verdi for et angitt element i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="1b661-126">This function determines whether the specified input matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="1b661-127">Den returnerer en *boolsk* verdi av **SANN** hvis de angitte inndataene samsvarer med resultatet av å kjøre det angitte uttrykket for minst én post i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="1b661-127">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="1b661-128">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="1b661-128">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |
| [<span data-ttu-id="1b661-129">ValueInLarge</span><span class="sxs-lookup"><span data-stu-id="1b661-129">ValueInLarge</span></span>](er-functions-logical-valueinlarge.md)     | <span data-ttu-id="1b661-130">Denne funksjonen bestemmer om de angitte inndataene av typen *Int64* eller *Integer* samsvarer med en verdi for et angitt element i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="1b661-130">This function determines whether the specified input of the *Int64* or *Integer* type matches any value of a specified item in the specified list.</span></span> <span data-ttu-id="1b661-131">Den returnerer en *boolsk* verdi av **SANN** hvis de angitte inndataene samsvarer med resultatet av å kjøre det angitte uttrykket for minst én post i den angitte listen.</span><span class="sxs-lookup"><span data-stu-id="1b661-131">It returns a *Boolean* value of **TRUE** if the specified input matches the result of running the specified expression for at least one record of the specified list.</span></span> <span data-ttu-id="1b661-132">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="1b661-132">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span> |


## <a name="additional-resources"></a><span data-ttu-id="1b661-133">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1b661-133">Additional resources</span></span>

[<span data-ttu-id="1b661-134">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="1b661-134">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="1b661-135">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="1b661-135">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="1b661-136">Formelspråk i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="1b661-136">Electronic reporting formula language</span></span>](er-formula-language.md)
