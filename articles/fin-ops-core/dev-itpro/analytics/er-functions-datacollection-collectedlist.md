---
title: COLLECTEDLIST ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen COLLECTEDLIST.
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
ms.openlocfilehash: 8a66ba364a7d06cd5ac03b57f07e2c5d4eb7a46d
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042602"
---
# <span data-ttu-id="df8ec-103"><a name="COLLECTEDLIST">COLLECTEDLIST ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="df8ec-103"><a name="COLLECTEDLIST">COLLECTEDLIST ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="df8ec-104">`COLLECTEDLIST`-funksjonen returnerer en *Postliste*-verdi som inneholder listen over verdier som ble returnert av egenskapen **Verdi for innsamlet datanøkkel** for formatelementer og samlet inn når formatelementene ble brukt til å generere utgående dokumenter under formatkjøringen, og som oppfyller de angitte betingelsene.</span><span class="sxs-lookup"><span data-stu-id="df8ec-104">The `COLLECTEDLIST` function a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate outbound documents during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="df8ec-105">Hver betingelse består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="df8ec-105">Each condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="df8ec-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="df8ec-106">Syntax</span></span>

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a><span data-ttu-id="df8ec-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="df8ec-107">Arguments</span></span>

<span data-ttu-id="df8ec-108">`condition 1 range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="df8ec-108">`condition 1 range`: *String*</span></span>

<span data-ttu-id="df8ec-109">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="df8ec-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span> <span data-ttu-id="df8ec-110">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="df8ec-110">This argument is mandatory.</span></span>

<span data-ttu-id="df8ec-111">`condition 1 value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="df8ec-111">`condition 1 value`: *String*</span></span>

<span data-ttu-id="df8ec-112">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Verdi for innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="df8ec-112">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="df8ec-113">Dette argumentet er obligatorisk.</span><span class="sxs-lookup"><span data-stu-id="df8ec-113">This argument is mandatory.</span></span>

<span data-ttu-id="df8ec-114">`condition N range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="df8ec-114">`condition N range`: *String*</span></span>

<span data-ttu-id="df8ec-115">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="df8ec-115">A value that is returned by the expression that has been configured in the **Collected data key name** property of an ER format component.</span></span> <span data-ttu-id="df8ec-116">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="df8ec-116">These additional arguments are optional.</span></span>

<span data-ttu-id="df8ec-117">`condition N value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="df8ec-117">`condition N value`: *String*</span></span>

<span data-ttu-id="df8ec-118">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Verdi for innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="df8ec-118">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span> <span data-ttu-id="df8ec-119">Disse tilleggsargumentene er valgfrie.</span><span class="sxs-lookup"><span data-stu-id="df8ec-119">These additional arguments are optional.</span></span>

## <a name="return-values"></a><span data-ttu-id="df8ec-120">Returverdier</span><span class="sxs-lookup"><span data-stu-id="df8ec-120">Return values</span></span>

<span data-ttu-id="df8ec-121">*Postliste*</span><span class="sxs-lookup"><span data-stu-id="df8ec-121">*Record list*</span></span>

<span data-ttu-id="df8ec-122">Den resulterende listen over oppføringer.</span><span class="sxs-lookup"><span data-stu-id="df8ec-122">The resulting list of records.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="df8ec-123">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="df8ec-123">Usage notes</span></span>

<span data-ttu-id="df8ec-124">Egenskapene **Navn på innsamlet datanøkkel** og **Verdi for innsamlet datanøkkel** kan konfigureres for enten **Sekvens**-komponenten eller **XML-element**-komponenten for et ER-format som ligger under **Vanlige\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="df8ec-124">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="df8ec-125">Denne funksjonen returnerer en tom liste når alternativet **Samle inn utdatadetaljer** for den gjeldende **Felles\\Fil**-komponenten er slått av.</span><span class="sxs-lookup"><span data-stu-id="df8ec-125">This function returns an empty list when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="df8ec-126">I `condition range`-argumenter kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="df8ec-126">In `condition range` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="df8ec-127">I `condition value`-argumenter kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="df8ec-127">In `condition value` arguments, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="df8ec-128">Eksempel</span><span class="sxs-lookup"><span data-stu-id="df8ec-128">Example</span></span>

<span data-ttu-id="df8ec-129">For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen [ER Bruke data med formatet utdata for telling og summering](tasks/er-format-counting-summing-1.md), som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**.</span><span class="sxs-lookup"><span data-stu-id="df8ec-129">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="df8ec-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="df8ec-130">Additional resources</span></span>

[<span data-ttu-id="df8ec-131">Datainnsamlingsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="df8ec-131">Data collection functions</span></span>](er-functions-category-data-collection.md)
