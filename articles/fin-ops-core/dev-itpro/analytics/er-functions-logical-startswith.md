---
title: ER-funksjonen STARTSWITH
description: Dette emnet gir generell informasjon om hvordan du bruker funksjonen ER-funksjonen STARTSWITH.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 50883bb604d2d1f2947545ce27fa02099e70b0e6
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048848"
---
# <a name="startswith-er-function"></a><span data-ttu-id="81e6d-103">ER-funksjonen STARTSWITH</span><span class="sxs-lookup"><span data-stu-id="81e6d-103">STARTSWITH ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81e6d-104">Funksjonen `STARTSWITH` bestemmer om de angitte inndataene starter med den angitte teksten.</span><span class="sxs-lookup"><span data-stu-id="81e6d-104">The `STARTSWITH` function determines whether the specified input starts with the specified text.</span></span> <span data-ttu-id="81e6d-105">Den returnerer den *boolske* verdien **SANN** hvis de angitte inndataene starter med den angitte teksten.</span><span class="sxs-lookup"><span data-stu-id="81e6d-105">It returns a *Boolean* value of **TRUE** if the specified input starts with the specified text.</span></span> <span data-ttu-id="81e6d-106">Hvis ikke returneres den *boolske* verdien **USANN**.</span><span class="sxs-lookup"><span data-stu-id="81e6d-106">Otherwise, it returns a *Boolean* value of **FALSE**.</span></span>

## <a name="syntax"></a><span data-ttu-id="81e6d-107">Syntaks</span><span class="sxs-lookup"><span data-stu-id="81e6d-107">Syntax</span></span>

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a><span data-ttu-id="81e6d-108">Argumenter</span><span class="sxs-lookup"><span data-stu-id="81e6d-108">Arguments</span></span>

<span data-ttu-id="81e6d-109">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="81e6d-109">`input`: *String*</span></span>

<span data-ttu-id="81e6d-110">Den gyldige banen til et element for en datakilde for typen *Streng* eller en strengkonstant. Verdien starter kanskje det andre argumentet.</span><span class="sxs-lookup"><span data-stu-id="81e6d-110">The valid path of an item of a data source of the *String* type or a string constant, the value of which might start with the second argument.</span></span>

<span data-ttu-id="81e6d-111">`start text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="81e6d-111">`start text`: *String*</span></span>

<span data-ttu-id="81e6d-112">Den gyldige banen for en datakilde for datatypen *Streng* eller en strengkonstant. Verdien finnes kanskje på starten av det første argumentet.</span><span class="sxs-lookup"><span data-stu-id="81e6d-112">The valid path of a data source of the *String* data type or a string constant, the value of which might be at the beginning of the first argument.</span></span>

## <a name="return-values"></a><span data-ttu-id="81e6d-113">Returverdier</span><span class="sxs-lookup"><span data-stu-id="81e6d-113">Return values</span></span>

<span data-ttu-id="81e6d-114">*Boolsk*</span><span class="sxs-lookup"><span data-stu-id="81e6d-114">*Boolean*</span></span>

<span data-ttu-id="81e6d-115">Den resulterende *boolske* verdien.</span><span class="sxs-lookup"><span data-stu-id="81e6d-115">The resulting *Boolean* value.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="81e6d-116">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="81e6d-116">Usage notes</span></span>

<span data-ttu-id="81e6d-117">Denne funksjonen kan bare brukes til å angi et betingelsesuttrykk for funksjonen [FILTER](er-functions-list-filter.md) når den relevante tilordningen er konfigurert i [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) for å få tilgang til [Microsoft Dataverse](/power-platform/admin/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="81e6d-117">This function can be used to specify a condition expression of the [FILTER](er-functions-list-filter.md) function only when the relevant mapping is configured in [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) to access [Microsoft Dataverse](/power-platform/admin/data-integrator).</span></span> <span data-ttu-id="81e6d-118">Ellers opprettes det et unntak på utformingstidspunktet.</span><span class="sxs-lookup"><span data-stu-id="81e6d-118">Otherwise, an exception is thrown at design time.</span></span> <span data-ttu-id="81e6d-119">Meldingen du mottar, anbefaler at du bruker funksjonen [WHERE](er-functions-list-where.md) i stedet for funksjonen `FILTER`.</span><span class="sxs-lookup"><span data-stu-id="81e6d-119">The message that you receive recommends that you use the [WHERE](er-functions-list-where.md) function instead of the `FILTER` function.</span></span>

## <a name="example-1"></a><span data-ttu-id="81e6d-120">Eksempel 1</span><span class="sxs-lookup"><span data-stu-id="81e6d-120">Example 1</span></span>

<span data-ttu-id="81e6d-121">Uttrykket `STARTSWITH ("abc", "d")` returnerer **USANN**, mens uttrykket `STARTSWITH ("abc", "A")` returnerer **SANN**.</span><span class="sxs-lookup"><span data-stu-id="81e6d-121">The expression `STARTSWITH ("abc", "d")` returns **FALSE**, whereas the expression `STARTSWITH ("abc", "A")` returns **TRUE**.</span></span>

## <a name="example-2"></a><span data-ttu-id="81e6d-122">Eksempel 2</span><span class="sxs-lookup"><span data-stu-id="81e6d-122">Example 2</span></span>

<span data-ttu-id="81e6d-123">Uttrykket `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returnerer **TRUE** hvis verdien for feltet **Adresse** for datakilden **modell** startes med strengen **123 Coffee Street**.</span><span class="sxs-lookup"><span data-stu-id="81e6d-123">The expression `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returns **TRUE** if the value of the **Address** field of the **model** data source starts with the string **123 Coffee Street**.</span></span> <span data-ttu-id="81e6d-124">Hvis ikke returnes **USANN**.</span><span class="sxs-lookup"><span data-stu-id="81e6d-124">Otherwise, it returns **FALSE**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="81e6d-125">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="81e6d-125">Additional resources</span></span>

[<span data-ttu-id="81e6d-126">Logiske funksjoner</span><span class="sxs-lookup"><span data-stu-id="81e6d-126">Logical functions</span></span>](er-functions-category-logical.md)
