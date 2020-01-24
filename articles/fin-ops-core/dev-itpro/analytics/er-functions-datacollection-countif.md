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
ms.openlocfilehash: ca7c0f449aff75527e5052ba01e6fc0e29bb0fd7
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917701"
---
# <span data-ttu-id="ed932-103"><a name="COUNTIF">COUNTIF ER-funksjonen</a></span><span class="sxs-lookup"><span data-stu-id="ed932-103"><a name="COUNTIF">COUNTIF ER function</a></span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ed932-104">`COUNTIF`-funksjonen returnerer en *Heltall*-verdi som representerer antall formatelementer som ble samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller den angitte betingelsen.</span><span class="sxs-lookup"><span data-stu-id="ed932-104">The `COUNTIF` function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="ed932-105">Betingelsen består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="ed932-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="ed932-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="ed932-106">Syntax</span></span>

```
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="ed932-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="ed932-107">Arguments</span></span>

<span data-ttu-id="ed932-108">`condition range`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ed932-108">`condition range`: *String*</span></span>

<span data-ttu-id="ed932-109">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="ed932-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of an Electronic reporting (ER) format component.</span></span>

<span data-ttu-id="ed932-110">`condition value`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="ed932-110">`condition value`: *String*</span></span>

<span data-ttu-id="ed932-111">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Verdi for innsamlet datanøkkel** for en ER-formatkomponent.</span><span class="sxs-lookup"><span data-stu-id="ed932-111">A value that is returned by the expression that has been configured in the **Collected data key value** property of an ER format component.</span></span>

## <a name="return-values"></a><span data-ttu-id="ed932-112">Returverdier</span><span class="sxs-lookup"><span data-stu-id="ed932-112">Return values</span></span>

<span data-ttu-id="ed932-113">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="ed932-113">*Integer*</span></span>

<span data-ttu-id="ed932-114">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="ed932-114">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="ed932-115">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="ed932-115">Usage notes</span></span>

<span data-ttu-id="ed932-116">Egenskapene **Navn på innsamlet datanøkkel** og **Verdi for innsamlet datanøkkel** kan konfigureres for enten **Sekvens**-komponenten eller **XML-element**-komponenten for et ER-format som ligger under **Vanlige\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="ed932-116">The **Collected data key name** and **Collected data key value** properties can be configured for either the **Sequence** component or the **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

<span data-ttu-id="ed932-117">Denne funksjonen returnerer en **0**-verdi (null) når alternativet **Samle inn utdatadetaljer** for den gjeldende **Felles\\Fil**-komponenten er slått av.</span><span class="sxs-lookup"><span data-stu-id="ed932-117">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="ed932-118">I `condition range`-argumentet kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="ed932-118">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="ed932-119">I `condition value`-argumentet kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="ed932-119">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="ed932-120">Eksempel</span><span class="sxs-lookup"><span data-stu-id="ed932-120">Example</span></span>

<span data-ttu-id="ed932-121">For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen [ER Bruke data med formatet utdata for telling og summering](tasks/er-format-counting-summing-1.md), som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**.</span><span class="sxs-lookup"><span data-stu-id="ed932-121">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ed932-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ed932-122">Additional resources</span></span>

[<span data-ttu-id="ed932-123">Datainnsamlingsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="ed932-123">Data collection functions</span></span>](er-functions-category-data-collection.md)
