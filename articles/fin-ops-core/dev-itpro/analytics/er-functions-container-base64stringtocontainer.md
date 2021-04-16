---
title: ER-funksjonen Base64StringToContainer
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen (Elektronisk rapportering) Base64StringToContainer.
author: NickSelin
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 6fd08d9a2522bdf497b1926c884a4583065d9f19
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5754380"
---
# <a name="base64stringtocontainer-er-function"></a><span data-ttu-id="fb637-103">ER-funksjonen Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="fb637-103">Base64StringToContainer ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fb637-104">[Funksjonen](er-formula-language.md#functions) `BASE64STRINGTOCONTAINER` konverterer de angitte inndataene for *Streng*-typen til et dataelement av typen *[Beholder](er-functions-category-container.md)*.</span><span class="sxs-lookup"><span data-stu-id="fb637-104">The `BASE64STRINGTOCONTAINER` [function](er-formula-language.md#functions) converts the specified input of the *String* type to a data item of the *[Container](er-functions-category-container.md)* type.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb637-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="fb637-105">Syntax</span></span>

```vb
BASE64STRINGTOCONTAINER (input)
```

## <a name="arguments"></a><span data-ttu-id="fb637-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="fb637-106">Arguments</span></span>

<span data-ttu-id="fb637-107">`input`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="fb637-107">`input`: *String*</span></span>

<span data-ttu-id="fb637-108">Den gyldige banen til en datakilde av *Streng*-typen.</span><span class="sxs-lookup"><span data-stu-id="fb637-108">The valid path of a data source of the *String* type.</span></span>

## <a name="return-values"></a><span data-ttu-id="fb637-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="fb637-109">Return values</span></span>

<span data-ttu-id="fb637-110">*Beholder*</span><span class="sxs-lookup"><span data-stu-id="fb637-110">*Container*</span></span>

<span data-ttu-id="fb637-111">Den resulterende binærverdien i format for stort binærobjekt (BLOB-format).</span><span class="sxs-lookup"><span data-stu-id="fb637-111">The resulting binary value in binary large object (BLOB) format.</span></span>

## <a name="usage-notes"></a><span data-ttu-id="fb637-112">Bruksnotater</span><span class="sxs-lookup"><span data-stu-id="fb637-112">Usage notes</span></span>

<span data-ttu-id="fb637-113">Unntaket «Parameteren er ikke gyldig» oppstår hvis inndatastrengen ikke inneholder en riktig Base64-gruppe med binær-til-tekst-kodingsoppsett.</span><span class="sxs-lookup"><span data-stu-id="fb637-113">The "Parameter is not valid" exception is thrown if the input string doesn't provide a correct Base64 group of binary-to-text encoding schemes.</span></span>

## <a name="example"></a><span data-ttu-id="fb637-114">Eksempel</span><span class="sxs-lookup"><span data-stu-id="fb637-114">Example</span></span>

<span data-ttu-id="fb637-115">Du definerer de følgende datakildene i modelltilordningen:</span><span class="sxs-lookup"><span data-stu-id="fb637-115">You define the following data sources in your model mapping:</span></span>

- <span data-ttu-id="fb637-116">Rotdatakilden **DocuTypeGroupEnum** av typen *Dynamics 365 for Operations / Opplisting* som refererer til programopplistingen **DocuTypeGroup**</span><span class="sxs-lookup"><span data-stu-id="fb637-116">The root **DocuTypeGroupEnum** data source of the *Dynamics 365 for Operations / Enumeration* type that refers to the **DocuTypeGroup** application enumeration</span></span>
- <span data-ttu-id="fb637-117">Rotdatakilden **Customer** av typen *Dynamics 365 for Operations / Tabellposter* som refererer til programtabellen **CustTable**</span><span class="sxs-lookup"><span data-stu-id="fb637-117">The root **Customer** data source of the *Dynamics 365 for Operations / Table records* type that refers to the **CustTable** application table</span></span>
- <span data-ttu-id="fb637-118">Datakilden **\#Media** av typen *Beregnet felt* som konfigureres på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="fb637-118">The **\#Media** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="fb637-119">Den legges til som en underordnet datakilde for datakilden **Customer**.</span><span class="sxs-lookup"><span data-stu-id="fb637-119">It's added as a child data source of the **Customer** data source.</span></span>
    - <span data-ttu-id="fb637-120">Den inneholder uttrykket `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span><span class="sxs-lookup"><span data-stu-id="fb637-120">It contains the expression `WHERE(@.'<Relations'.'<Documents', @.'<Relations'.'<Documents'.'docuType()'.TypeGroup = DocuTypeGroupEnum.Image)`.</span></span>

- <span data-ttu-id="fb637-121">Datakilden **\#MediaAsBase64String** av typen *Beregnet felt* som konfigureres på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="fb637-121">The **\#MediaAsBase64String** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="fb637-122">Den legges til som en underordnet datakilde for datakilden **Customer.'\#Media'**.</span><span class="sxs-lookup"><span data-stu-id="fb637-122">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="fb637-123">Den inneholder uttrykket `Customer.'#Media'.'getFileContentAsBase64String()'`.</span><span class="sxs-lookup"><span data-stu-id="fb637-123">It contains the expression `Customer.'#Media'.'getFileContentAsBase64String()'`.</span></span>

- <span data-ttu-id="fb637-124">Datakilden **\#BlobFomBase64** av typen *Beregnet felt* som konfigureres på følgende måte:</span><span class="sxs-lookup"><span data-stu-id="fb637-124">The **\#BlobFomBase64** data source of the *Calculated field* type that is configured in the following way:</span></span>

    - <span data-ttu-id="fb637-125">Den legges til som en underordnet datakilde for datakilden **Customer.'\#Media'**.</span><span class="sxs-lookup"><span data-stu-id="fb637-125">It's added as a child data source of the **Customer.'\#Media'** data source.</span></span>
    - <span data-ttu-id="fb637-126">Den inneholder uttrykket `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span><span class="sxs-lookup"><span data-stu-id="fb637-126">It contains the expression `Base64StringToContainer(Customer.'#Media'.'#MediaAsBase64String')'`.</span></span>

<span data-ttu-id="fb637-127">I dette eksemplet koder datakilden **\#MediaAsBase64String** det binære innholdet i det gjeldende medievedlegget som tekst som representerer en Base64-gruppe med binær-til-tekst-kodingsoppsett.</span><span class="sxs-lookup"><span data-stu-id="fb637-127">In this example, the **\#MediaAsBase64String** data source encodes the binary content of the current media attachment as text that represents a Base64 group of binary-to-text encoding schemes.</span></span> <span data-ttu-id="fb637-128">Datakilden **\#BlobFomBase64** dekoder Base64-strengen og returnerer en binær verdi i BLOB-format.</span><span class="sxs-lookup"><span data-stu-id="fb637-128">The **\#BlobFomBase64** data source decodes the Base64 string and returns a binary value in BLOB format.</span></span>

![Eksempeldatakilder på siden ER-utforming av modelltilordning](./media/er-functions-container-base64stringtocontainer-1.png)

## <a name="additional-resources"></a><span data-ttu-id="fb637-130">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="fb637-130">Additional resources</span></span>

[<span data-ttu-id="fb637-131">Beholderfunksjoner</span><span class="sxs-lookup"><span data-stu-id="fb637-131">Container functions</span></span>](er-functions-category-container.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]