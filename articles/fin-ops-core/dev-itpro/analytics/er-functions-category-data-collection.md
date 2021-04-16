---
title: Liste over ER-funksjoner i datainnsamlingskategorien
description: Dette emnet inneholder informasjon om datainnsamlingsfunksjonene som støttes i elektronisk rapportering (ER).
author: NickSelin
ms.date: 12/04/2019
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
ms.openlocfilehash: 31b5e7b08a3de77d461fff5e42164975e53dfe1e
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748069"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a><span data-ttu-id="a5eb9-103">Liste over ER-funksjoner i datainnsamlingskategorien</span><span class="sxs-lookup"><span data-stu-id="a5eb9-103">List of ER functions in the data collection category</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a5eb9-104">Datainnsamlingsfunksjoner for elektronisk rapportering (ER) brukes til å telle og summere i et ER-format som kjøres, basert på data fra utdataene som allerede er generert i **Tekst**- eller **Xml**-format.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-104">Electronic reporting (ER) data collection functions are used to do counting and summing in an ER format that is being run, based on data of the output that has already been generated in **Text** or **Xml** format.</span></span> <span data-ttu-id="a5eb9-105">Denne fremgangsmåten brukes til å forbedre ytelsen til et ER-format som kjøres, til å angi verdier for løpende totaler i genererte dokumenter og til andre formål.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-105">This approach is used to help improve performance of an ER format that is run, to enter values of running totals in generated documents, and for other purposes.</span></span> <span data-ttu-id="a5eb9-106">Dette emnet inneholder et sammendrag av disse funksjonene.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-106">This topic provides a summary of these functions.</span></span>

## <a name="list-of-supported-functions"></a><span data-ttu-id="a5eb9-107">Liste over funksjoner som støttes</span><span class="sxs-lookup"><span data-stu-id="a5eb9-107">List of supported functions</span></span>

| <span data-ttu-id="a5eb9-108">Funksjon</span><span class="sxs-lookup"><span data-stu-id="a5eb9-108">Function</span></span> | <span data-ttu-id="a5eb9-109">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a5eb9-109">Description</span></span> |
|----------|-------------|
| [<span data-ttu-id="a5eb9-110">CollectedList</span><span class="sxs-lookup"><span data-stu-id="a5eb9-110">CollectedList</span></span>](er-functions-datacollection-collectedlist.md) | <span data-ttu-id="a5eb9-111">Denne funksjonen returnerer en *Postliste*-verdi som inneholder listen over verdier som ble returnert av egenskapen **Verdi for innsamlet datanøkkel** for formatelementer og samlet inn når formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller de angitte betingelsene.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-111">This function returns a *Record list* value that contains the list of values that were returned by the **Collected data key value** property of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="a5eb9-112">Hver betingelse består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-112">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="a5eb9-113">CountIF</span><span class="sxs-lookup"><span data-stu-id="a5eb9-113">CountIF</span></span>](er-functions-datacollection-countif.md) | <span data-ttu-id="a5eb9-114">Denne funksjonen returnerer en *Heltall*-verdi som representerer antall formatelementer som ble samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller den angitte betingelsen.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-114">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="a5eb9-115">Betingelsen består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-115">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="a5eb9-116">CountIFs</span><span class="sxs-lookup"><span data-stu-id="a5eb9-116">CountIFs</span></span>](er-functions-datacollection-countifs.md) | <span data-ttu-id="a5eb9-117">Denne funksjonen returnerer en *Heltall*-verdi som representerer antall formatelementer som ble samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller de angitte betingelsene.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-117">This function returns an *Integer* value that represents the number of format elements that was collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="a5eb9-118">Hver betingelse består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-118">Each condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="a5eb9-119">FormatElementName</span><span class="sxs-lookup"><span data-stu-id="a5eb9-119">FormatElementName</span></span>](er-functions-datacollection-formatelementname.md) | <span data-ttu-id="a5eb9-120">Denne funksjonen returnerer en *streng*-verdi som representerer navnet på det gjeldende ER-formatets element.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-120">This function returns a *String* value that represents the name of the current ER format's element.</span></span> |
| [<span data-ttu-id="a5eb9-121">SumIF</span><span class="sxs-lookup"><span data-stu-id="a5eb9-121">SumIF</span></span>](er-functions-datacollection-sumif.md) | <span data-ttu-id="a5eb9-122">Denne funksjonen returnerer en *Reell*-verdi som representerer summen av verdier som ble returnert av bindinger for formatelementer og samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller den angitte betingelsen.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-122">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified condition.</span></span> <span data-ttu-id="a5eb9-123">Betingelsen består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-123">The condition consists of a key range and a key value.</span></span> |
| [<span data-ttu-id="a5eb9-124">SumIFs</span><span class="sxs-lookup"><span data-stu-id="a5eb9-124">SumIFs</span></span>](er-functions-datacollection-sumifs.md) | <span data-ttu-id="a5eb9-125">Denne funksjonen returnerer en *Reell*-verdi som representerer summen av verdier som ble returnert av bindinger for formatelementer og samlet inn da formatelementene ble brukt til å generere et utgående dokument under formatkjøringen, og som oppfyller de angitte betingelsene.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-125">This function returns a *Real* value that represents the sum of values that were returned by bindings of format elements and collected when the format elements were used to generate an outbound document during the format run, and that satisfies the specified conditions.</span></span> <span data-ttu-id="a5eb9-126">Hver betingelse består av et nøkkelområde og en nøkkelverdi.</span><span class="sxs-lookup"><span data-stu-id="a5eb9-126">Each condition consists of a key range and a key value.</span></span> |

## <a name="additional-resources"></a><span data-ttu-id="a5eb9-127">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="a5eb9-127">Additional resources</span></span>

[<span data-ttu-id="a5eb9-128">Oversikt over elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a5eb9-128">Electronic Reporting overview</span></span>](general-electronic-reporting.md)

[<span data-ttu-id="a5eb9-129">Formeldesigner i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a5eb9-129">Formula designer in Electronic reporting</span></span>](general-electronic-reporting-formula-designer.md)

[<span data-ttu-id="a5eb9-130">Formelspråk i elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="a5eb9-130">Electronic reporting formula language</span></span>](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]