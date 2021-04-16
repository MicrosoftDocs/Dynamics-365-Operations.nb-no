---
title: Analysere innkommende dokumenter i JSON-format
description: Dette emnet beskriver hvordan du konfigurerer ER-formater (elektroniske rapporter) for å analysere innkommende dokumenter i JSON-format (JavaScript Object Notation).
author: kfend
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 4e598dc15b619c2f6a0525ea18c371484ca26fa4
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5755160"
---
# <a name="parse-incoming-documents-in-json-format"></a><span data-ttu-id="9fa96-103">Analysere innkommende dokumenter i JSON-format</span><span class="sxs-lookup"><span data-stu-id="9fa96-103">Parse incoming documents in JSON format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9fa96-104">Du kan utforme ER-formater (elektronisk rapportering) for å analysere innkommende elektroniske dokumenter som representerer data i et tekstformat som er basert på JavaScript (med andre ord filer i JSON-format \[JavaScript Object Notation\]).</span><span class="sxs-lookup"><span data-stu-id="9fa96-104">You can design Electronic reporting (ER) formats to parse incoming electronic documents that represent data in a text format that is based on JavaScript (in other words, files in JavaScript Object Notation \[JSON\] format).</span></span>

<span data-ttu-id="9fa96-105">Hvis du vil ha mer informasjon om denne funksjonen, kan du laste ned filene i følgende tabell og deretter spille av oppgaveveiledningen «ER Opprette en formatkonfigurasjon for å importere data fra en ekstern JSON-fil».</span><span class="sxs-lookup"><span data-stu-id="9fa96-105">To learn more about this feature, download the files in the following table, and then play the ER Create a format configuration to import data from an external JSON file task guide.</span></span> <span data-ttu-id="9fa96-106">Denne oppgaveveiledningen viser hvordan et ER-format kan brukes til å analysere en innkommende JSON-fil for å oppdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="9fa96-106">This task guide shows how an ER format can be used to parse an incoming JSON file to update application data.</span></span>

| <span data-ttu-id="9fa96-107">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="9fa96-107">Title</span></span>                                  | <span data-ttu-id="9fa96-108">Filnavn</span><span class="sxs-lookup"><span data-stu-id="9fa96-108">File name</span></span> |
|----------------------------------------|-----------|
| <span data-ttu-id="9fa96-109">ER-formatkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="9fa96-109">ER format configuration</span></span>                | [<span data-ttu-id="9fa96-110">Format for import av leverandørenes trans_JSON.xml</span><span class="sxs-lookup"><span data-stu-id="9fa96-110">Format for importing vendors' trans_JSON.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |
| <span data-ttu-id="9fa96-111">Eksempel på innkommende fil i CSV-format</span><span class="sxs-lookup"><span data-stu-id="9fa96-111">Sample of incoming file in .csv format</span></span> | [<span data-ttu-id="9fa96-112">1099entries_JSON.txt</span><span class="sxs-lookup"><span data-stu-id="9fa96-112">1099entries_JSON.txt</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |

## <a name="requirements"></a><span data-ttu-id="9fa96-113">Behov</span><span class="sxs-lookup"><span data-stu-id="9fa96-113">Requirements</span></span>

<span data-ttu-id="9fa96-114">Før du fullfører oppgaveveiledningen «ER Opprette en formatkonfigurasjon for å importere data fra en ekstern JSON-fil», må følgende krav oppfylles:</span><span class="sxs-lookup"><span data-stu-id="9fa96-114">Before you complete the ER Create a format configuration to import data from an external JSON file task guide, the following requirement must be met:</span></span>

- <span data-ttu-id="9fa96-115">Overordnede elementer i JSON-filen kan bare være objektelementer.</span><span class="sxs-lookup"><span data-stu-id="9fa96-115">Parent elements in the JSON file can be only object elements.</span></span>
- <span data-ttu-id="9fa96-116">Nestede elementer for et objekt bør være egenskapselementer, slik at du lager en gyldig JSON-struktur.</span><span class="sxs-lookup"><span data-stu-id="9fa96-116">Nested elements for an object should be property elements, so that a valid JSON structure is created.</span></span>
- <span data-ttu-id="9fa96-117">JSON-matriser kan bare være nestede elementer i egenskapselementene for et objekt.</span><span class="sxs-lookup"><span data-stu-id="9fa96-117">JSON arrays can be only nested elements of the property elements of an object.</span></span>
- <span data-ttu-id="9fa96-118">JSON-matriser kan bare inneholde JSON-objekter.</span><span class="sxs-lookup"><span data-stu-id="9fa96-118">JSON arrays can contain only JSON objects.</span></span> <span data-ttu-id="9fa96-119">De kan ikke inneholde direkte strengverdier / numeriske verdier og nestede matriser.</span><span class="sxs-lookup"><span data-stu-id="9fa96-119">They can't contain direct string/numeric values and nested arrays.</span></span> <span data-ttu-id="9fa96-120">Elementer i disse matrisene analyseres i rekkefølge, slik de er angitt i formatet.</span><span class="sxs-lookup"><span data-stu-id="9fa96-120">Elements in these arrays will be parsed in order, as they are specified in the format.</span></span> <span data-ttu-id="9fa96-121">Multiplisitet-innstillingene for hvert JSON-objekt blir vurdert.</span><span class="sxs-lookup"><span data-stu-id="9fa96-121">Multiplicity settings on each JSON object will be considered.</span></span>

<span data-ttu-id="9fa96-122">Du må i tillegg fullføre oppgaveveiledningen [ER Opprette nødvendige konfigurasjoner for å importere data fra en ekstern fil](tasks/er-required-configurations-import-data.md) hvis du ikke allerede har fullført den.</span><span class="sxs-lookup"><span data-stu-id="9fa96-122">Additionally, you must complete the [ER Create required configurations to import data from an external file](tasks/er-required-configurations-import-data.md) task guide if you haven't already completed it.</span></span> <span data-ttu-id="9fa96-123">Last ned følgende file for å fullføre oppgaveveiledningen.</span><span class="sxs-lookup"><span data-stu-id="9fa96-123">Download the following file to complete the task guide.</span></span>

| <span data-ttu-id="9fa96-124">Stillingstittel</span><span class="sxs-lookup"><span data-stu-id="9fa96-124">Title</span></span>                  | <span data-ttu-id="9fa96-125">Filnavn</span><span class="sxs-lookup"><span data-stu-id="9fa96-125">File name</span></span> |
|------------------------|-----------|
| <span data-ttu-id="9fa96-126">ER-modellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="9fa96-126">ER model configuration</span></span> | [<span data-ttu-id="9fa96-127">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="9fa96-127">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=874111) |


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]