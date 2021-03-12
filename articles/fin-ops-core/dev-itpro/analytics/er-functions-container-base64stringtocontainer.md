---
title: ER-funksjonen Base64StringToContainer
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen (Elektronisk rapportering) Base64StringToContainer.
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 0e92ae41a3e0f03cb14d4791ab768f096f2a0523
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739101"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="3accc-103">ER-funksjonen Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="3accc-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3accc-104">[Funksjonen](er-formula-language.md#functions) `BASE64STRINGTOCONTAINER` konverterer de angitte inndataene for *Streng*-typen til et dataelement av typen *[Beholder](er-functions-category-container.md)*.</span><span class="sxs-lookup"><span data-stu-id="3accc-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="3accc-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="3accc-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="3accc-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="3accc-106">Arguments</span></span>

<span data-ttu-id="3accc-107">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="3accc-107">`input`: *String*</span></span>

<span data-ttu-id="3accc-108">Den gyldige banen til en datakilde av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="3accc-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="3accc-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="3accc-109">Return values</span></span>

<span data-ttu-id="3accc-110">*Beholder*</span><span class="sxs-lookup"><span data-stu-id="3accc-110">*Container*</span></span>

<span data-ttu-id="3accc-111">Den resulterende binærverdien i format for stort binærobjekt (BLOB-format).</span><span class="sxs-lookup"><span data-stu-id="3accc-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="3accc-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="3accc-112">Usage notes</span></span>

<span data-ttu-id="3accc-113">Unntaket «Parameteren er ikke gyldig» oppstår hvis inndatastrengen ikke inneholder en riktig Base64-gruppe med binær-til-tekst-kodingsoppsett.</span><span class="sxs-lookup"><span data-stu-id="3accc-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="3accc-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="3accc-114">Example</span></span>

<span data-ttu-id="3accc-115">Du definerer de følgende datakildene i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="3accc-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="3accc-116">Rotdatakilden **DocuTypeGroupEnum** av typen *Dynamics 365 for Operations / Opplisting* som refererer til programopplistingen **DocuTypeGroup**</span><span class="sxs-lookup"><span data-stu-id="3accc-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="3accc-117">Rotdatakilden **Customer** av typen *Dynamics 365 for Operations / Tabellposter* som refererer til programtabellen **CustTable**</span><span class="sxs-lookup"><span data-stu-id="3accc-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="3accc-118">Datakilden **\#Media** av typen *Beregnet felt* som konfigureres på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="3accc-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="3accc-119">Den legges til som en underordnet datakilde for datakilden **Customer**.</span><span class="sxs-lookup"><span data-stu-id="3accc-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="3accc-120">Den inneholder uttrykket `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="3accc-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="3accc-121">Datakilden **\#MediaAsBase64String** av typen *Beregnet felt* som konfigureres på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="3accc-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="3accc-122">Den legges til som en underordnet datakilde for datakilden **Customer.'\#Media'**.</span><span class="sxs-lookup"><span data-stu-id="3accc-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="3accc-123">Den inneholder uttrykket `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="3accc-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="3accc-124">Datakilden **\#BlobFomBase64** av typen *Beregnet felt* som konfigureres på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="3accc-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="3accc-125">Den legges til som en underordnet datakilde for datakilden **Customer.'\#Media'**.</span><span class="sxs-lookup"><span data-stu-id="3accc-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="3accc-126">Den inneholder uttrykket `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="3accc-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="3accc-127">I dette eksemplet koder datakilden **\#MediaAsBase64String** det binære innholdet i det gjeldende medievedlegget som tekst som representerer en Base64-gruppe med binær-til-tekst-kodingsoppsett.</span><span class="sxs-lookup"><span data-stu-id="3accc-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="3accc-128">Datakilden **\#BlobFomBase64** dekoder Base64-strengen og returnerer en binær verdi i BLOB-format.</span><span class="sxs-lookup"><span data-stu-id="3accc-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![Eksempeldatakilder på siden ER-utforming av modelltilordning](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="3accc-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="3accc-130">Additional resources</span></span>

[<span data-ttu-id="3accc-131">Beholderfunksjoner</span><span class="sxs-lookup"><span data-stu-id="3accc-131">Container functions</span></span>](er-functions-category-container.md)
