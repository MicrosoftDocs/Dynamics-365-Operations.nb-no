---
title: SUMIFS ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SUMIFS.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6820be1976e722f7b108b3e9303c8ed4d822ae9b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917609"
---
# <span data-ttu-id="ada19-103"><a name="SUMIFS">SUMIFS ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="ada19-103"><a name="SUMIFS">SUMIFS ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ada19-104">`SUMIFS`-funksjonen returnerer en *reell* verdi som representerer summen av verdier som ble returnert av bindinger for formatelementer og samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller de angitte betingelsene.</span><span class="sxs-lookup"><span data-stu-id="ada19-104">The `SUMIFS` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="ada19-105">Hver betingelse består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="ada19-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ada19-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ada19-106">Syntax</span></span>

```
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="ada19-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="ada19-107">Arguments</span></span>

<span data-ttu-id="ada19-108">`key name for summing`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ada19-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="ada19-109">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for ER-formatkomponenten som verdien for bindingen må brukes til summeringsformål for.</span><span class="sxs-lookup"><span data-stu-id="ada19-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="ada19-110">Egenskapen **Navn på innsamlet datanøkkel** kan konfigureres for enten en **numerisk** komponent eller en **streng**-komponent for et ER-format som ligger under **Vanlig\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="ada19-110">The **Collected data key name** property can be configured for either a **Numeric** component or a **String** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="ada19-111">`condition 1 range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ada19-111">`condition 1 range`: *String*</span></span>

<span data-ttu-id="ada19-112">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="ada19-112">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="ada19-113">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ada19-113">This argument is mandatory.</span></span>

<span data-ttu-id="ada19-114">Egenskapen **Navn på innsamlet datanøkkel** kan konfigureres for enten en **Sekvens**-komponenten eller en **XML-element** -komponenten for et ER-format som ligger under **Vanlig\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="ada19-114">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="ada19-115">`condition 1 value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ada19-115">`condition 1 value`: *String*</span></span>

<span data-ttu-id="ada19-116">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Verdi for innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="ada19-116">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="ada19-117">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ada19-117">This argument is mandatory.</span></span>

<span data-ttu-id="ada19-118">Egenskapen **Navn på innsamlet datanøkkel** kan konfigureres for enten en **Sekvens**-komponenten eller en **XML-element** -komponenten for et ER-format som ligger under **Vanlig\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="ada19-118">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="ada19-119">`condition N range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ada19-119">`condition N range`: *String*</span></span>

<span data-ttu-id="ada19-120">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="ada19-120">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="ada19-121">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="ada19-121">These additional arguments are optional.</span></span>

<span data-ttu-id="ada19-122">Egenskapen **Navn på innsamlet datanøkkel** kan konfigureres for enten en **Sekvens**-komponenten eller en **XML-element** -komponenten for et ER-format som ligger under **Vanlig\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="ada19-122">The **Collected data key name** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="ada19-123">`condition N value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ada19-123">`condition N value`: *String*</span></span>

<span data-ttu-id="ada19-124">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Verdi for innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="ada19-124">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="ada19-125">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="ada19-125">These additional arguments are optional.</span></span>

<span data-ttu-id="ada19-126">Egenskapen **Navn på innsamlet datanøkkel** kan konfigureres for enten en **Sekvens**-komponenten eller en **XML-element** -komponenten for et ER-format som ligger under **Vanlig\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="ada19-126">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="ada19-127">Returverdier</span><span class="sxs-lookup"><span data-stu-id="ada19-127">Return values</span></span>

<span data-ttu-id="ada19-128">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="ada19-128">*Real*</span></span>

<span data-ttu-id="ada19-129">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="ada19-129">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ada19-130">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="ada19-130">Usage notes</span></span>

<span data-ttu-id="ada19-131">Denne funksjonen returnerer en **0**-verdi (null) når alternativet **Samle inn utdatadetaljer** for den gjeldende **Felles\\Fil**-komponenten er slått av.</span><span class="sxs-lookup"><span data-stu-id="ada19-131">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="ada19-132">I `condition range`-argumenter kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="ada19-132">In the `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="ada19-133">I `condition value`-argumenter kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="ada19-133">In the `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="ada19-134">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ada19-134">Example</span></span>

<span data-ttu-id="ada19-135">For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen [ER Bruke data med formatet utdata for telling og summering](tasks/er-format-counting-summing-1.md), som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**.</span><span class="sxs-lookup"><span data-stu-id="ada19-135">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ada19-136">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ada19-136">Additional resources</span></span>

[<span data-ttu-id="ada19-137">Datainnsamlingsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="ada19-137">Data collection functions</span></span>](er-functions-category-data-collection.md)
