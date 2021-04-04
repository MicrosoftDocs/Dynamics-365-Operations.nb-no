---
title: COLLECTEDLIST ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen COLLECTEDLIST.
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
ms.openlocfilehash: ff48170247130a03b10dc8fe2973f8d774046944
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561404"
---
# <a name="collectedlist-er-function"></a><span data-ttu-id="ec2ed-103">COLLECTEDLIST ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="ec2ed-103">COLLECTEDLIST ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ec2ed-104">`COLLECTEDLIST`-funksjonen returnerer en *Postliste*-verdi som inneholder listen over verdier som ble returnert av egenskapen **Verdi for innsamlet datanøkkel** for formatelementer og samlet inn når formatelementene ble brukt til å generere utgående dokumenter under formatkjøringen, og som oppfyller de angitte betingelsene.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-104">The `COLLECTEDLIST` function a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate outbound documents during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="ec2ed-105">Hver betingelse består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ec2ed-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ec2ed-106">Syntax</span></span>

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="ec2ed-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="ec2ed-107">Arguments</span></span>

<span data-ttu-id="ec2ed-108">`condition 1 range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ec2ed-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="ec2ed-109">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="ec2ed-110">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-110">This argument is mandatory.</span></span>

<span data-ttu-id="ec2ed-111">`condition 1 value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ec2ed-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="ec2ed-112">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Verdi for innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="ec2ed-113">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-113">This argument is mandatory.</span></span>

<span data-ttu-id="ec2ed-114">`condition N range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ec2ed-114">`condition N range`: *String*</span></span>

<span data-ttu-id="ec2ed-115">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="ec2ed-116">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-116">These additional arguments are optional.</span></span>

<span data-ttu-id="ec2ed-117">`condition N value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ec2ed-117">`condition N value`: *String*</span></span>

<span data-ttu-id="ec2ed-118">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Verdi for innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="ec2ed-119">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="ec2ed-120">Returverdier</span><span class="sxs-lookup"><span data-stu-id="ec2ed-120">Return values</span></span>

<span data-ttu-id="ec2ed-121">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="ec2ed-121">*Record list*</span></span>

<span data-ttu-id="ec2ed-122">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-122">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ec2ed-123">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="ec2ed-123">Usage notes</span></span>

<span data-ttu-id="ec2ed-124">Egenskapene **Navn på innsamlet datanøkkel** og **Verdi for innsamlet datanøkkel** kan konfigureres for enten **Sekvens**-komponenten eller **XML-element**-komponenten for et ER-format som ligger under **Vanlige\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="ec2ed-125">Denne funksjonen returnerer en tom liste når alternativet **Samle inn utdatadetaljer** for den gjeldende **Felles\\Fil**-komponenten er slått av.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-125">This function returns an empty list when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="ec2ed-126">I `condition range`-argumenter kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="ec2ed-127">I `condition value`-argumenter kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="ec2ed-128">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ec2ed-128">Example</span></span>

<span data-ttu-id="ec2ed-129">For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen [ER Bruke data med formatet utdata for telling og summering](tasks/er-format-counting-summing-1.md), som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**.</span><span class="sxs-lookup"><span data-stu-id="ec2ed-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ec2ed-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ec2ed-130">Additional resources</span></span>

[<span data-ttu-id="ec2ed-131">Datainnsamlingsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="ec2ed-131">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]