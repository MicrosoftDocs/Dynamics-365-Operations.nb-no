---
title: Analysere innkommende dokumenter i Excel-format
description: "Dette emnet gir informasjon om utforming av elektronisk rapportering (ER)-formater for å analysere innholdet i innkommende Microsoft Excel-filer."
author: NickSelin
manager: AnnBe
ms.date: 05/25/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 220314
ms.assetid: 2685df16-5ec8-4fd7-9495-c0f653e82567
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2018-04-01
ms.dyn365.ops.version: Release 8.0
ms.translationtype: HT
ms.sourcegitcommit: 821d8927211d7ac3e479848c7e7bef9f650d4340
ms.openlocfilehash: 490a9325be25908564a40478a1ee29feea67fc02
ms.contentlocale: nb-no
ms.lasthandoff: 08/13/2018

---

# <a name="parse-incoming-documents-in-excel-format"></a><span data-ttu-id="04211-103">Analysere innkommende dokumenter i Excel-format</span><span class="sxs-lookup"><span data-stu-id="04211-103">Parse incoming documents in Excel format</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="04211-104">Du kan utforme elektronisk rapportering (ER)-formater for å analysere innkommende Microsoft Excel-filer som representerer data i Microsoft Excel-arbeidsbøker (XLSX-formatfiler).</span><span class="sxs-lookup"><span data-stu-id="04211-104">You can design Electronic reporting (ER) formats to parse incoming Microsoft Excel files that represent data in Microsoft Excel workbooks (files in XLSX format).</span></span> <span data-ttu-id="04211-105">Du kan deretter bruke innholdet fra disse filene til å oppdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="04211-105">You can then use the content from these files to update application data.</span></span> <span data-ttu-id="04211-106">Dette er nyttig hvis du:</span><span class="sxs-lookup"><span data-stu-id="04211-106">This is useful if you:</span></span>

- <span data-ttu-id="04211-107">Utformer ny modell og nytt format og ønsker å teste dem under kjøring.</span><span class="sxs-lookup"><span data-stu-id="04211-107">Design a new model and format and want to test them at run-time.</span></span> <span data-ttu-id="04211-108">I så fall vil Excel simulere de faktiske programdataene.</span><span class="sxs-lookup"><span data-stu-id="04211-108">In this case, Excel will simulate the actual application data.</span></span>
- <span data-ttu-id="04211-109">Behandle data utenfor programmet i Excel og ønsker å importere disse dataene for å sende en bestemt rapport.</span><span class="sxs-lookup"><span data-stu-id="04211-109">Manage data beyond your application in Excel and want to import this data to submit a specific report.</span></span>

<span data-ttu-id="04211-110">Hvis du vil vite mer om denne funksjonen, kan du spille av oppgaveveiledningene **ER Importer data fra en Microsoft Excel-fil (del 1: Utforme format)** og **ER Importer data fra en Microsoft Excel-fil (del 2: Importere data)** (deler av 7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)-forretningsprosessen).</span><span class="sxs-lookup"><span data-stu-id="04211-110">To learn more about this feature, play the task guides **ER Import data from a Microsoft Excel file (Part 1: Design format)** and **ER Import data from a Microsoft Excel file (Part 2: Import data)** (parts of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process).</span></span> <span data-ttu-id="04211-111">Disse oppgaveveiledningene går gjennom hvordan den innkommende Excel-filen kan analyseres ved hjelp av ER-formatet for å importere informasjon fra innkommende dokumenter og oppdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="04211-111">These task guides walk through how the incoming Excel file can be parsed by using the ER format to import information from incoming documents and update application data.</span></span> <span data-ttu-id="04211-112">Du kan laste ned oppgaveveiledningsfilene fra [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span><span class="sxs-lookup"><span data-stu-id="04211-112">You can download the task guide files from the [Microsoft Download Center](https://go.microsoft.com/fwlink/?linkid=874684).</span></span>

<span data-ttu-id="04211-113">Last ned følgende filer for å fullføre oppgaveveiledningene som er nevnt over.</span><span class="sxs-lookup"><span data-stu-id="04211-113">Download the following files to complete the task guides mentioned above.</span></span>

| <span data-ttu-id="04211-114">Innholdsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="04211-114">Content description</span></span>                         | <span data-ttu-id="04211-115">Fil</span><span class="sxs-lookup"><span data-stu-id="04211-115">File</span></span>                                                                       |
|---------------------------------------------|----------------------------------------------------------------------------|
| <span data-ttu-id="04211-116">Innkommende fil i .XLSX-format - mal</span><span class="sxs-lookup"><span data-stu-id="04211-116">Incoming file in .XLSX format - template</span></span>    | [<span data-ttu-id="04211-117">1099import-template.xlsx</span><span class="sxs-lookup"><span data-stu-id="04211-117">1099import-template.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |
| <span data-ttu-id="04211-118">Innkommende fil i .XLSX-format - eksempeldata</span><span class="sxs-lookup"><span data-stu-id="04211-118">Incoming file in .XLSX format - sample data</span></span> | [<span data-ttu-id="04211-119">1099import-data.xlsx</span><span class="sxs-lookup"><span data-stu-id="04211-119">1099import-data.xlsx</span></span>](https://go.microsoft.com/fwlink/?linkid=862266)     |

<span data-ttu-id="04211-120">Hvis du ennå ikke har spilt av følgende oppgaveveiledning [ER Opprette nødvendige konfigurasjoner for å importere data fra en ekstern fil](./tasks/er-required-configurations-import-data.md) i det gjeldende Dynamics 365 for Finance and Operation-programmet, kan du laste ned følgende fil.</span><span class="sxs-lookup"><span data-stu-id="04211-120">If you have not yet played the following task guide, [ER Create required configurations to import data from an external file](./tasks/er-required-configurations-import-data.md) in the current Dynamics 365 for Finance and Operation application, download the following file.</span></span>

| <span data-ttu-id="04211-121">Innholdsbeskrivelse</span><span class="sxs-lookup"><span data-stu-id="04211-121">Content description</span></span>    | <span data-ttu-id="04211-122">Fil</span><span class="sxs-lookup"><span data-stu-id="04211-122">File</span></span>                                                            |
|------------------------|-----------------------------------------------------------------|
| <span data-ttu-id="04211-123">ER-modellkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="04211-123">ER model configuration</span></span> | [<span data-ttu-id="04211-124">1099model.xml</span><span class="sxs-lookup"><span data-stu-id="04211-124">1099model.xml</span></span>](https://go.microsoft.com/fwlink/?linkid=862266) |

