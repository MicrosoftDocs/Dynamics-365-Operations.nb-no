---
title: COUNTIF ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen COUNTIF.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: cc857a004d988a421c32722b1f69e86b7fefeb36
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743621"
---
# <a name="countif-er-function"></a><span data-ttu-id="435cb-103">COUNTIF ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="435cb-103">COUNTIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="435cb-104">`COUNTIF`-funksjonen returnerer en *Heltall*-verdi som representerer antall formatelementer som ble samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller den angitte betingelsen.</span><span class="sxs-lookup"><span data-stu-id="435cb-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="435cb-105">Betingelsen består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="435cb-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="435cb-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="435cb-106">Syntax</span></span>

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="435cb-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="435cb-107">Arguments</span></span>

<span data-ttu-id="435cb-108">`condition range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="435cb-108">`condition range`: *String*</span></span>

<span data-ttu-id="435cb-109">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="435cb-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="435cb-110">`condition value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="435cb-110">`condition value`: *String*</span></span>

<span data-ttu-id="435cb-111">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Verdi for innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="435cb-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="435cb-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="435cb-112">Return values</span></span>

<span data-ttu-id="435cb-113">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="435cb-113">*Integer*</span></span>

<span data-ttu-id="435cb-114">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="435cb-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="435cb-115">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="435cb-115">Usage notes</span></span>

<span data-ttu-id="435cb-116">Egenskapene **Navn på innsamlet datanøkkel** og **Verdi for innsamlet datanøkkel** kan konfigureres for enten **Sekvens**-komponenten eller **XML-element**-komponenten for et ER-format som ligger under **Vanlige\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="435cb-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="435cb-117">Denne funksjonen returnerer en **0**-verdi (null) når alternativet **Samle inn utdatadetaljer** for den gjeldende **Felles\\Fil**-komponenten er slått av.</span><span class="sxs-lookup"><span data-stu-id="435cb-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="435cb-118">I `condition range`-argumentet kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="435cb-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="435cb-119">I `condition value`-argumentet kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="435cb-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="435cb-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="435cb-120">Example</span></span>

<span data-ttu-id="435cb-121">For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen [ER Bruke data med formatet utdata for telling og summering](tasks/er-format-counting-summing-1.md), som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**.</span><span class="sxs-lookup"><span data-stu-id="435cb-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="435cb-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="435cb-122">Additional resources</span></span>

[<span data-ttu-id="435cb-123">Datainnsamlingsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="435cb-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
