---
title: COUNTIFS ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen COUNTIFS.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 5bc0beb20f600afdea2d58187dd2a9c26a775ec1
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561333"
---
# <a name="countifs-er-function"></a><span data-ttu-id="665c4-103">COUNTIFS ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="665c4-103">COUNTIFS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="665c4-104">`COUNTIFS`-funksjonen returnerer en *Heltall*-verdi som representerer antall formatelementer som ble samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller de angitte betingelsene.</span><span class="sxs-lookup"><span data-stu-id="665c4-104">The `COUNTIFS` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="665c4-105">Hver betingelse består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="665c4-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="665c4-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="665c4-106">Syntax</span></span>

```vb
COUNTIFS (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="665c4-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="665c4-107">Arguments</span></span>

<span data-ttu-id="665c4-108">`condition 1 range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="665c4-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="665c4-109">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="665c4-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="665c4-110">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="665c4-110">This argument is mandatory.</span></span>

<span data-ttu-id="665c4-111">`condition 1 value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="665c4-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="665c4-112">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Verdi for innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="665c4-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="665c4-113">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="665c4-113">This argument is mandatory.</span></span>

<span data-ttu-id="665c4-114">`condition N range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="665c4-114">`condition N range`: *String*</span></span>

<span data-ttu-id="665c4-115">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="665c4-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="665c4-116">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="665c4-116">These additional arguments are optional.</span></span>

<span data-ttu-id="665c4-117">`condition N value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="665c4-117">`condition N value`: *String*</span></span>

<span data-ttu-id="665c4-118">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Verdi for innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="665c4-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="665c4-119">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="665c4-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="665c4-120">Returverdier</span><span class="sxs-lookup"><span data-stu-id="665c4-120">Return values</span></span>

<span data-ttu-id="665c4-121">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="665c4-121">*Integer*</span></span>

<span data-ttu-id="665c4-122">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="665c4-122">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="665c4-123">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="665c4-123">Usage notes</span></span>

<span data-ttu-id="665c4-124">Egenskapene **Navn på innsamlet datanøkkel** og **Verdi for innsamlet datanøkkel** kan konfigureres for enten **Sekvens**-komponenten eller **XML-element**-komponenten for et ER-format som ligger under **Vanlige\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="665c4-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="665c4-125">Denne funksjonen returnerer en **0**-verdi (null) når alternativet **Samle inn utdatadetaljer** for den gjeldende **Felles\\Fil**-komponenten er slått av.</span><span class="sxs-lookup"><span data-stu-id="665c4-125">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="665c4-126">I `condition range`-argumenter kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="665c4-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="665c4-127">I `condition value`-argumenter kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="665c4-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="665c4-128">Eksempel</span><span class="sxs-lookup"><span data-stu-id="665c4-128">Example</span></span>

<span data-ttu-id="665c4-129">For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen [ER Bruke data med formatet utdata for telling og summering](tasks/er-format-counting-summing-1.md), som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**.</span><span class="sxs-lookup"><span data-stu-id="665c4-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="665c4-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="665c4-130">Additional resources</span></span>

[<span data-ttu-id="665c4-131">Datainnsamlingsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="665c4-131">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]