---
title: FORMATELEMENTNAME ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FORMATELEMENTNAME.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef59bb44a7096f4c095ce37a89558a717748f02e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685333"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="1f2dd-103">FORMATELEMENTNAME ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="1f2dd-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f2dd-104">`FORMATELEMENTNAME`-funksjonen returnerer en *streng*-verdi som representerer navnet på det gjeldende ER-formatets element.</span><span class="sxs-lookup"><span data-stu-id="1f2dd-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="1f2dd-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="1f2dd-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="1f2dd-106">Returverdier</span><span class="sxs-lookup"><span data-stu-id="1f2dd-106">Return values</span></span>

<span data-ttu-id="1f2dd-107">*Streng*</span><span class="sxs-lookup"><span data-stu-id="1f2dd-107">*String*</span></span>

<span data-ttu-id="1f2dd-108">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="1f2dd-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="1f2dd-109">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="1f2dd-109">Usage notes</span></span>

<span data-ttu-id="1f2dd-110">Denne funksjonen kan kalles i ER-uttrykk som er konfigurert for egenskapene **Navn på innsamlet datanøkkel** og **Verdi for innsamlet datanøkkel** for en ER-formatkomponent fra **Tekst**-gruppen som ligger under **Felles\\Fil**- komponenten der **Samle inn utdatadetaljer** er slått på.</span><span class="sxs-lookup"><span data-stu-id="1f2dd-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="1f2dd-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="1f2dd-111">Example</span></span>

<span data-ttu-id="1f2dd-112">For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen [ER Bruke data med formatet utdata for telling og summering](tasks/er-format-counting-summing-1.md), som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**.</span><span class="sxs-lookup"><span data-stu-id="1f2dd-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="1f2dd-113">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="1f2dd-113">Additional resources</span></span>

[<span data-ttu-id="1f2dd-114">Datainnsamlingsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="1f2dd-114">Data collection functions</span></span>](er-functions-category-data-collection.md)
