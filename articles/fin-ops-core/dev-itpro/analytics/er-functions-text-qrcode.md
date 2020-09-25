---
title: QRCODE ER-funksjonen
description: Dette emnet gir generell informasjon om hvordan du bruker ER-funksjonen QRCODE.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: f634976d83fb4066a953b7ab09c963214415e29b
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743764"
---
# <a name="qrcode-er-function"></a><span data-ttu-id="86382-103">QRCODE ER-funksjonen</span><span class="sxs-lookup"><span data-stu-id="86382-103">QRCODE ER function</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="86382-104">`QRCODE`-funksjonen returnerer en *Container*-verdi som presenterer et QR-kodebilde for den angitte strengen i binært format.</span><span class="sxs-lookup"><span data-stu-id="86382-104">The `QRCODE` function returns a *Container* value that presents the Quick Response code (QR code) image for the specified string in binary format.</span></span>

## <a name="syntax"></a><span data-ttu-id="86382-105">Syntaks</span><span class="sxs-lookup"><span data-stu-id="86382-105">Syntax</span></span>

```vb
QRCODE (text)
```

## <a name="arguments"></a><span data-ttu-id="86382-106">Argumenter</span><span class="sxs-lookup"><span data-stu-id="86382-106">Arguments</span></span>

<span data-ttu-id="86382-107">`text`: *Streng*</span><span class="sxs-lookup"><span data-stu-id="86382-107">`text`: *String*</span></span>

<span data-ttu-id="86382-108">En *streng*-verdi som representerer den opprinnelige teksten.</span><span class="sxs-lookup"><span data-stu-id="86382-108">A *String* value that represents the original text.</span></span>

## <a name="return-values"></a><span data-ttu-id="86382-109">Returverdier</span><span class="sxs-lookup"><span data-stu-id="86382-109">Return values</span></span>

<span data-ttu-id="86382-110">*Container*</span><span class="sxs-lookup"><span data-stu-id="86382-110">*Container*</span></span>

<span data-ttu-id="86382-111">Den resulterende binære strømmen.</span><span class="sxs-lookup"><span data-stu-id="86382-111">The resulting binary stream.</span></span>

## <a name="example"></a><span data-ttu-id="86382-112">Eksempel</span><span class="sxs-lookup"><span data-stu-id="86382-112">Example</span></span>

<span data-ttu-id="86382-113">Du kan konfigurere et elektronisk rapportering (ER)-format til å generere et utgående Microsoft Office-dokument i format (Excel-arbeidsbøker eller Word-dokumenter) ved hjelp av en forhåndsdefinert mal.</span><span class="sxs-lookup"><span data-stu-id="86382-113">You can configure an Electronic reporting (ER) format to generate an outbound document in Microsoft Office format (Excel workbooks or Word documents) by using a predefined template.</span></span> <span data-ttu-id="86382-114">Denne malen kan inneholde et **Bilde**-objekt (Excel-arbeidsbok) eller en **Bildeinnholdskontroll** (Word-dokument) som en plassholder for et bilde av en QR-kode.</span><span class="sxs-lookup"><span data-stu-id="86382-114">This template may contain a **Picture** object (Excel workbook) or a **Picture Content Control** (Word document) as a placeholder for a QR code image.</span></span> <span data-ttu-id="86382-115">Du må legge til det konfigurerte ER-formatet et **celle**-element som vil bli brukt til å fylle inn denne plassholderen.</span><span class="sxs-lookup"><span data-stu-id="86382-115">You need to add to the configured ER format a **Cell** element that will be used to fill this placeholder in.</span></span> <span data-ttu-id="86382-116">Hvis du vil angi hvilken informasjon som skal lagres i en QR-kode, må du definere en binding for dette **celle**-elementet.</span><span class="sxs-lookup"><span data-stu-id="86382-116">To specify what information will be stored in a QR code, you need to define a binding for this **Cell** element.</span></span> <span data-ttu-id="86382-117">Du kan for eksempel konfigurere en slik binding som inneholder følgende uttrykk:</span><span class="sxs-lookup"><span data-stu-id="86382-117">For example, you can configure such binding as containing the following expression:</span></span>

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

<span data-ttu-id="86382-118">Når du kjører det konfigurerte ER-formatet, blir tekstverdien for **LabelText**-feltet i **model.ListOfShelfLabels**-datakilden brukt til å generere et QR-kodebilde.</span><span class="sxs-lookup"><span data-stu-id="86382-118">When you run the configured ER format, the text value of the **LabelText** field of the **model.ListOfShelfLabels** data source will be used to generate a QR code image.</span></span> <span data-ttu-id="86382-119">Dette bildet vil erstatte en plassholder for et QR-kodebilde i dokumentmalen ved hjelp av å generere et utgående dokument.</span><span class="sxs-lookup"><span data-stu-id="86382-119">This image will replace a QR code image placeholder in the document template using to generate an outbound document.</span></span> <span data-ttu-id="86382-120">Når dette bildet av det genererte dokumentet skannes, returnerer det teksten som ble hentet fra **LabelText**-feltet i **model.ListOfShelfLabels**-datakilden.</span><span class="sxs-lookup"><span data-stu-id="86382-120">When this image of the generated document is scanned, it returns the text that was taken from the **LabelText** field of the **model.ListOfShelfLabels** data source.</span></span> <span data-ttu-id="86382-121">Hvis du vil ha mer informasjon, se [Bygge inn bilder og figurer i dokumenter d.u genererer ved hjelp av ER](electronic-reporting-embed-images-shapes.md).</span><span class="sxs-lookup"><span data-stu-id="86382-121">For more information, see [Embed images and shapes in documents that you generate by using ER](electronic-reporting-embed-images-shapes.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="86382-122">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="86382-122">Additional resources</span></span>

[<span data-ttu-id="86382-123">Tekstfunksjoner</span><span class="sxs-lookup"><span data-stu-id="86382-123">Text functions</span></span>](er-functions-category-text.md)
