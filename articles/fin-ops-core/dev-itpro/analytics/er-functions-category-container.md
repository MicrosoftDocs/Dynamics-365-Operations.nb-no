---
title: Liste over ER-funksjoner i beholderkategorien
description: Dette emnet inneholder informasjon om beholderfunksjonene som støttes i Elektronisk rapportering (ER).
author: NickSelin
manager: kfend
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
ms.openlocfilehash: b7e7d770c334647f8f11338d49b39a2e9cb5c04c
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561764"
---
# <a name="list-of-er-functions-in-the-container-category"></a><span data-ttu-id="6c2b6-103">Liste over ER-funksjoner i beholderkategorien</span><span class="sxs-lookup"><span data-stu-id="6c2b6-103">List of ER functions in the container category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="6c2b6-104">Beholder [funksjoner](er-formula-language.md#functions) for [Elektronisk rapportering (ER)](general-electronic-reporting.md) kan brukes til å utføre operasjoner som omfatter datakilder av datatypen *Beholder*.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-104">[Electronic reporting (ER)](general-electronic-reporting.md) container [functions](er-formula-language.md#functions) can be used to perform operations that involve data sources of the *Container* data type.</span></span> <span data-ttu-id="6c2b6-105">Disse operasjonene skjer når behandlingsdataene representerer en samling binære data i format for stort binærobjekt (BLOB-format).</span><span class="sxs-lookup"><span data-stu-id="6c2b6-105">These operations occur when the processing data represents a collection of binary data in binary large object (BLOB) format.</span></span> <span data-ttu-id="6c2b6-106">Dette emnet inneholder et sammendrag av disse funksjonene.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="6c2b6-107">Liste over funksjoner som støttes</span><span class="sxs-lookup"><span data-stu-id="6c2b6-107">List of supported functions</span></span>

| <span data-ttu-id="6c2b6-108">Funksjon</span><span class="sxs-lookup"><span data-stu-id="6c2b6-108">Function</span></span> | <span data-ttu-id="6c2b6-109">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6c2b6-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="6c2b6-110">Base64StringToContainer</span><span class="sxs-lookup"><span data-stu-id="6c2b6-110">Base64StringToContainer</span></span>](er-functions-container-base64stringtocontainer.md) | <span data-ttu-id="6c2b6-111">Denne funksjonen returnerer en *Beholder*-verdi som består av binært innhold som dekodes fra den angitte ASCII-strengen som representerer en Base64-gruppe med binær-til-tekst-kodingsoppsett.</span><span class="sxs-lookup"><span data-stu-id="6c2b6-111">This function returns a *Container* value that consists of binary content that is decoded from the specified ASCII string that represents a Base64 group of binary-to-text encoding schemes.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="6c2b6-112">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="6c2b6-112">Additional resources</span></span>

[<span data-ttu-id="6c2b6-113">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="6c2b6-113">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="6c2b6-114">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="6c2b6-114">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="6c2b6-115">Formelspråk i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="6c2b6-115">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]