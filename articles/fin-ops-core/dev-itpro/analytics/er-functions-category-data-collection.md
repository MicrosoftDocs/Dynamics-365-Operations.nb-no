---
title: Liste over ER-funksjoner i datainnsamlingskategorien
description: Dette emnet inneholder informasjon om datainnsamlingsfunksjonene som støttes i elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 0ec6092f2992df91433bb8aaa4212fca2a0abf7c
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686299"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="bebef-103">Liste over ER-funksjoner i datainnsamlingskategorien</span><span class="sxs-lookup"><span data-stu-id="bebef-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bebef-104">Datainnsamlingsfunksjoner for elektronisk rapportering (ER) brukes til å telle og summere i et ER-format som kjøres, basert på data fra utdataene som allerede er generert i **Tekst**- eller **Xml**-format.</span><span class="sxs-lookup"><span data-stu-id="bebef-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="bebef-105">Denne fremgangsmåten brukes til å forbedre ytelsen til et ER-format som kjøres, til å angi verdier for løpende totaler i genererte dokumenter og til andre formål.</span><span class="sxs-lookup"><span data-stu-id="bebef-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="bebef-106">Dette emnet inneholder et sammendrag av disse funksjonene.</span><span class="sxs-lookup"><span data-stu-id="bebef-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="bebef-107">Liste over funksjoner som støttes</span><span class="sxs-lookup"><span data-stu-id="bebef-107">List of supported functions</span></span>

| <span data-ttu-id="bebef-108">Funksjon</span><span class="sxs-lookup"><span data-stu-id="bebef-108">Function</span></span> | <span data-ttu-id="bebef-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="bebef-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="bebef-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="bebef-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="bebef-111">Denne funksjonen returnerer en *Postliste*-verdi som inneholder listen over verdier som ble returnert av egenskapen **Verdi for innsamlet datanøkkel** for formatelementer og samlet inn når formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller de angitte betingelsene.</span><span class="sxs-lookup"><span data-stu-id="bebef-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="bebef-112">Hver betingelse består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="bebef-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="bebef-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="bebef-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="bebef-114">Denne funksjonen returnerer en *Heltall*-verdi som representerer antall formatelementer som ble samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller den angitte betingelsen.</span><span class="sxs-lookup"><span data-stu-id="bebef-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="bebef-115">Betingelsen består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="bebef-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="bebef-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="bebef-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="bebef-117">Denne funksjonen returnerer en *Heltall*-verdi som representerer antall formatelementer som ble samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller de angitte betingelsene.</span><span class="sxs-lookup"><span data-stu-id="bebef-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="bebef-118">Hver betingelse består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="bebef-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="bebef-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="bebef-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="bebef-120">Denne funksjonen returnerer en *streng*-verdi som representerer navnet på det gjeldende ER-formatets element.</span><span class="sxs-lookup"><span data-stu-id="bebef-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="bebef-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="bebef-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="bebef-122">Denne funksjonen returnerer en *Reell*-verdi som representerer summen av verdier som ble returnert av bindinger for formatelementer og samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller den angitte betingelsen.</span><span class="sxs-lookup"><span data-stu-id="bebef-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="bebef-123">Betingelsen består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="bebef-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="bebef-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="bebef-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="bebef-125">Denne funksjonen returnerer en *Reell*-verdi som representerer summen av verdier som ble returnert av bindinger for formatelementer og samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller de angitte betingelsene.</span><span class="sxs-lookup"><span data-stu-id="bebef-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="bebef-126">Hver betingelse består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="bebef-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="bebef-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="bebef-127">Additional resources</span></span>

[<span data-ttu-id="bebef-128">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="bebef-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="bebef-129">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="bebef-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="bebef-130">Formelspråk i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="bebef-130">Electronic reporting formula language</span></span>](er-formula-language.md)
