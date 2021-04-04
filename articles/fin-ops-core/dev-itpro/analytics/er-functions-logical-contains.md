---
title: ER-funksjonen CONTAINS
description: Dette emnet gir generell informasjon om hvordan du bruker funksjonen ER-funksjonen CONTAINS.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: 81964681688cebf870bc9b6c59aff0b7fdd82449
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557542"
---
# <a name="contains-er-function"></a><span data-ttu-id="bb10d-103">ER-funksjonen CONTAINS</span><span class="sxs-lookup"><span data-stu-id="bb10d-103">CONTAINS ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bb10d-104">Funksjonen `CONTAINS` bestemmer om de angitte inndataene inneholder den angitte teksten.</span><span class="sxs-lookup"><span data-stu-id="bb10d-104">The `CONTAINS` function determines whether the specified input contains the specified text.</span></span> <span data-ttu-id="bb10d-105">Den returnerer den *boolske* verdien **SANN** hvis de angitte inndataene inneholder den angitte teksten.</span><span class="sxs-lookup"><span data-stu-id="bb10d-105">It returns a *Boolean* value of **TRUE** if the specified input contains the specified text.</span></span> <span data-ttu-id="bb10d-106">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="bb10d-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb10d-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="bb10d-107">Syntax</span></span>

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a><span data-ttu-id="bb10d-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="bb10d-108">Arguments</span></span>

<span data-ttu-id="bb10d-109">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="bb10d-109">`input`: *String*</span></span>

<span data-ttu-id="bb10d-110">Den gyldige banen til et element for en datakilde for typen *Streng* eller en strengkonstant. Verdien kan inneholde det andre argumentet.</span><span class="sxs-lookup"><span data-stu-id="bb10d-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might contain the second argument.</span></span>

<span data-ttu-id="bb10d-111">`search text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="bb10d-111">`search text`: *String*</span></span>

<span data-ttu-id="bb10d-112">Den gyldige banen for en datakilde for datatypen *Streng* eller en strengkonstant. Verdien finnes kanskje i det første argumentet.</span><span class="sxs-lookup"><span data-stu-id="bb10d-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be contained in the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="bb10d-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="bb10d-113">Return values</span></span>

<span data-ttu-id="bb10d-114">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="bb10d-114">*Boolean*</span></span>

<span data-ttu-id="bb10d-115">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="bb10d-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="bb10d-116">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="bb10d-116">Usage notes</span></span>

<span data-ttu-id="bb10d-117">Denne funksjonen kan bare brukes til å angi et betingelsesuttrykk for funksjonen [FILTER](er-functions-list-filter.md) når den relevante tilordningen er konfigurert i [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) for å få tilgang til [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span><span class="sxs-lookup"><span data-stu-id="bb10d-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](../data-entities/data-integration-cds.md).</span></span> <span data-ttu-id="bb10d-118">Ellers opprettes det et unntak på utformingstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="bb10d-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="bb10d-119">Meldingen du mottar, anbefaler at du bruker funksjonen [WHERE](er-functions-list-where.md) i stedet for funksjonen `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="bb10d-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="bb10d-120">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="bb10d-120">Example 1</span></span>

<span data-ttu-id="bb10d-121">Uttrykket `CONTAINS ("abc", "d")` returnerer **USANN**, mens uttrykket `CONTAINS ("abc", "C")` returnerer **SANN**.</span><span class="sxs-lookup"><span data-stu-id="bb10d-121">The expression `CONTAINS ("abc", "d")` returns **FALSE**, whereas the expression `CONTAINS ("abc", "C")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="bb10d-122">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="bb10d-122">Example 2</span></span>

<span data-ttu-id="bb10d-123">Uttrykket `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returnerer **SANN** hvis verdien til feltet **Adresse** i datakilden **modell** inneholder strengen **DEU**.</span><span class="sxs-lookup"><span data-stu-id="bb10d-123">The expression `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returns **TRUE** if the value of the **Address** field of the **model** data source contains the string **DEU**.</span></span> <span data-ttu-id="bb10d-124">Hvis ikke returnes **USANN**.</span><span class="sxs-lookup"><span data-stu-id="bb10d-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="bb10d-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bb10d-125">Additional resources</span></span>

[<span data-ttu-id="bb10d-126">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="bb10d-126">Logical functions</span></span>](er-functions-category-logical.md)
