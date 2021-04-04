---
title: FORMATELEMENTNAME ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen FORMATELEMENTNAME.
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
ms.openlocfilehash: 1e2ee2faa2784f34d540c113622cee2090f24cef
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561308"
---
# <a name="formatelementname-er-function"></a><span data-ttu-id="d1d7c-103">FORMATELEMENTNAME ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="d1d7c-103">FORMATELEMENTNAME ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d1d7c-104">`FORMATELEMENTNAME`-funksjonen returnerer en *streng*-verdi som representerer navnet på det gjeldende ER-formatets element.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-104">The `FORMATELEMENTNAME` function returns a *String* value that represents the name of the current Electronic reporting (ER) format's element.</span></span>

## <a name="syntax"></a><span data-ttu-id="d1d7c-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="d1d7c-105">Syntax</span></span>

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a><span data-ttu-id="d1d7c-106">Returverdier</span><span class="sxs-lookup"><span data-stu-id="d1d7c-106">Return values</span></span>

<span data-ttu-id="d1d7c-107">*Streng*</span><span class="sxs-lookup"><span data-stu-id="d1d7c-107">*String*</span></span>

<span data-ttu-id="d1d7c-108">Den resulterende tekstverdien.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-108">The resulting text value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="d1d7c-109">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="d1d7c-109">Usage notes</span></span>

<span data-ttu-id="d1d7c-110">Denne funksjonen kan kalles i ER-uttrykk som er konfigurert for egenskapene **Navn på innsamlet datanøkkel** og **Verdi for innsamlet datanøkkel** for en ER-formatkomponent fra **Tekst**-gruppen som ligger under **Felles\\Fil**- komponenten der **Samle inn utdatadetaljer** er slått på.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-110">This function can be called in ER expressions that were configured for the **Collected data key name** and **Collected data key value** properties of an ER format component from the **Text** group that resides under the **Common\\File** component where the **Collect output details** option is turned on.</span></span>

## <a name="example"></a><span data-ttu-id="d1d7c-111">Eksempel</span><span class="sxs-lookup"><span data-stu-id="d1d7c-111">Example</span></span>

<span data-ttu-id="d1d7c-112">For å lære mer om bruk av denne funksjonen, se oppgaveveiledningen [ER Bruke data med formatet utdata for telling og summering](tasks/er-format-counting-summing-1.md), som er en del av forretningsprosessen **Anskaffe/utvikle komponenter for IT-tjeneste/-løsning**.</span><span class="sxs-lookup"><span data-stu-id="d1d7c-112">For more information about how to use this function, see the [ER Use data of format output for counting and summing](tasks/er-format-counting-summing-1.md) task guide, which is part of the **Acquire/Develop IT service/solution components** business process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d1d7c-113">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="d1d7c-113">Additional resources</span></span>

[<span data-ttu-id="d1d7c-114">Datainnsamlingsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="d1d7c-114">Data collection functions</span></span>](er-functions-category-data-collection.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]