---
title: SUMIF ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen SUMIF.
author: NickSelin
ms.date: 04/27/2020
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
ms.openlocfilehash: 60cf85ac0ffcdb163c12670efa3dcc7e9f05cb16
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747113"
---
# <a name="sumif-er-function"></a><span data-ttu-id="84738-103">SUMIF ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="84738-103">SUMIF ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="84738-104">`SUMIF`-funksjonen returnerer en *reell* verdi som representerer summen av verdier som ble returnert av bindinger for formatelementer og samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller den angitte betingelsen.</span><span class="sxs-lookup"><span data-stu-id="84738-104">The `SUMIF` function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="84738-105">Betingelsen består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="84738-105">The condition consists of a key range and a key value.</span></span>

## <a name="syntax"></a><span data-ttu-id="84738-106">Syntaks</span><span class="sxs-lookup"><span data-stu-id="84738-106">Syntax</span></span>

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a><span data-ttu-id="84738-107">Argumenter</span><span class="sxs-lookup"><span data-stu-id="84738-107">Arguments</span></span>

<span data-ttu-id="84738-108">`key name for summing`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="84738-108">`key name for summing`: *String*</span></span>

<span data-ttu-id="84738-109">En verdi som returneres av uttrykket som er konfigurert i egenskapen **Navn på innsamlet datanøkkel** for ER-formatkomponenten som verdien for bindingen må brukes til summeringsformål for.</span><span class="sxs-lookup"><span data-stu-id="84738-109">A value that is returned by the expression that has been configured in the **Collected data key name** property of the Electronic reporting (ER) format component for which the value of the binding must be used for summing purposes.</span></span>

<span data-ttu-id="84738-110">Egenskapen **Navn på innsamlet datanøkkel** kan konfigureres for enten en **Sekvens**-komponenten eller en **XML-element** -komponenten for et ER-format som ligger under **Vanlig\\Fil**-komponenten der alternativet **Samle inn utdatadetaljer** er aktivert.</span><span class="sxs-lookup"><span data-stu-id="84738-110">The **Collected data key value** property can be configured for either a **Sequence** component or an **XML Element** component of an ER format that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="return-values"></a><span data-ttu-id="84738-111">Returverdier</span><span class="sxs-lookup"><span data-stu-id="84738-111">Return values</span></span>

<span data-ttu-id="84738-112">*Kommatall*</span><span class="sxs-lookup"><span data-stu-id="84738-112">*Real*</span></span>

<span data-ttu-id="84738-113">Den resulterende numeriske verdien.</span><span class="sxs-lookup"><span data-stu-id="84738-113">The resulting numeric value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="84738-114">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="84738-114">Usage notes</span></span>

<span data-ttu-id="84738-115">Denne funksjonen returnerer en **0**-verdi (null) når alternativet **Samle inn utdatadetaljer** for den gjeldende **Felles\\Fil**-komponenten er slått av.</span><span class="sxs-lookup"><span data-stu-id="84738-115">This function returns a **0** (zero) value when the **Collect output details** option of the current **Common\\File** component is turned off.</span></span>

<span data-ttu-id="84738-116">I `condition range`-argumentet kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="84738-116">In the `condition range` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

<span data-ttu-id="84738-117">I `condition value`-argumentet kan jokertegnet **"\*"** brukes til å representere flere tegn.</span><span class="sxs-lookup"><span data-stu-id="84738-117">In the `condition value` argument, the wildcard character **"\*"** can be used to represent any multiple characters.</span></span>

## <a name="example"></a><span data-ttu-id="84738-118">Eksempel</span><span class="sxs-lookup"><span data-stu-id="84738-118">Example</span></span>

<span data-ttu-id="84738-119">For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen [ER Bruke data med formatet utdata for telling og summering](tasks/er-format-counting-summing-1.md), som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**.</span><span class="sxs-lookup"><span data-stu-id="84738-119">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

<span data-ttu-id="84738-120">Hvis du vil ha mer informasjon og eksempler om hvordan du bruker denne funksjonen, se [Utsette kjøringen av sekvenselementer i ER-formater](er-defer-sequence-element.md#Example) og [Utsette kjøringen av XML-elementer i ER-formater](er-defer-xml-element.md#Example).</span><span class="sxs-lookup"><span data-stu-id="84738-120">For more information and examples about using this function, see [Defer the execution of sequence elements in ER formats](er-defer-sequence-element.md#Example) and [Defer the execution of XML elements in ER formats](er-defer-xml-element.md#Example).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84738-121">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="84738-121">Additional resources</span></span>

[<span data-ttu-id="84738-122">Datainnsamlingsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="84738-122">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]