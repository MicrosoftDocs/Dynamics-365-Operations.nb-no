---
title: "Generere elektroniske dokumenter og oppdatere programdata ved hjelp av verktøyet for elektronisk rapportering"
description: "Du kan utforme elektronisk rapportering (ER)-formater som kan brukes i Finance and Operations-programmet for å generere utgående elektroniske dokumenter. Du kan også utforme ER-formatene som analyserer innkommende elektroniske dokumenter og bruke innholdet i disse dokumentene til å oppdatere programdata."
author: NickSelin
manager: AnnBe
ms.date: 11/01/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ERSolutionTable, ERVendorTable, ERWorkspace
audience: Developer, IT Pro, Application user
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 27621
ms.assetid: 018a11ae-854c-4f36-9358-8c39baca882d
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1b49dd7f4cfa0da68337554f21008bd41f9bdda1
ms.contentlocale: nb-no
ms.lasthandoff: 04/13/2018

---

# <a name="generate-electronic-documents-and-update-application-data-using-the-electronic-reporting-tool"></a><span data-ttu-id="327fe-104">Generere elektroniske dokumenter og oppdatere programdata ved hjelp av verktøyet for elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="327fe-104">Generate electronic documents and update application data using the Electronic reporting tool</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="327fe-105">Du kan utforme elektronisk rapportering (ER)-formater som kan brukes i Finance and Operations-programmet for å generere utgående elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="327fe-105">You can design Electronic reporting (ER) formats that can be used in the Finance and Operations application to generate outgoing electronic documents.</span></span> <span data-ttu-id="327fe-106">Du kan også utforme ER-formatene som analyserer innkommende elektroniske dokumenter og bruke innholdet i disse dokumentene til å oppdatere programdata.</span><span class="sxs-lookup"><span data-stu-id="327fe-106">You can also design ER formats that parse incoming electronic documents and use the content in those documents to update application data.</span></span> 

<span data-ttu-id="327fe-107">Med denne funksjonen kan et enkelt ER-format brukes til å generere utgående elektroniske dokumenter, og deretter oppdatere programdataene.</span><span class="sxs-lookup"><span data-stu-id="327fe-107">With this functionality, a single ER format can be used to generate outgoing electronic documents and then update the application data.</span></span> <span data-ttu-id="327fe-108">Denne funksjonen kan brukes i følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="327fe-108">This feature can be used in the following scenarios:</span></span>

- <span data-ttu-id="327fe-109">For å hindre gjentatt bruk av programdata i påfølgende prosesser, kan du merke et programs data umiddelbart etter at de er brukt til å generere elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="327fe-109">To prevent repeated usage of application data in subsequent processes you can mark an application’s data immediately after it is used to generate electronic documents.</span></span> <span data-ttu-id="327fe-110">Du kan for eksempel merke betalingstransaksjoner som allerede behandlet umiddelbart etter at de er inkludert i en generert betalingsmelding.</span><span class="sxs-lookup"><span data-stu-id="327fe-110">For example, you can mark payment transactions as already processed immediately after they have been included in a generated payment message.</span></span>
- <span data-ttu-id="327fe-111">For å lagre behandlingsdetaljene for elektroniske dokumenter som er generert ved hjelp av ER-logikk.</span><span class="sxs-lookup"><span data-stu-id="327fe-111">To store the processing details of electronic documents that have been generated using ER logic.</span></span> <span data-ttu-id="327fe-112">For eksempel en unik betalingsmeldingsidentifikasjon som genereres ved hjelp av ER-uttrykket.</span><span class="sxs-lookup"><span data-stu-id="327fe-112">For example, a unique payment message identification that is generated using the ER expression.</span></span> <span data-ttu-id="327fe-113">Uttrykket er basert på informasjonen som er angitt i ER-dialogboksennår ER-formatet kjøres for å generere dokumenter.</span><span class="sxs-lookup"><span data-stu-id="327fe-113">The expression is based on information entered in the ER dialog box when the ER format is run to generate documents.</span></span>

<span data-ttu-id="327fe-114">Hvis du vil vite mer om denne funksjonen, kan du spille av settet med oppgaveveiledninger ER Generere elektroniske dokumenter med oppdatering av programdata (del av 7.5.4.3 forretningsprosessen Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)), som leder deg gjennom detaljene for Intrastat-rapportering og arkivering.</span><span class="sxs-lookup"><span data-stu-id="327fe-114">To learn more about this feature, play the set of ER Generate documents with application data update Task guides (part of the 7.5.4.3 Acquire/Develop IT service/solution components (10677) business process), which walk you through the details of Intrastat reporting and archiving.</span></span> <span data-ttu-id="327fe-115">Følgende filer er nødvendig for å gjennomføre enkelte trinn i disse oppgaveveiledningene.</span><span class="sxs-lookup"><span data-stu-id="327fe-115">The following files are required to complete certain steps in these Task guides.</span></span> <span data-ttu-id="327fe-116">Last ned og lagre disse filene på den lokale datamaskinen.</span><span class="sxs-lookup"><span data-stu-id="327fe-116">Download and save these files to your local machine.</span></span>

- [<span data-ttu-id="327fe-117">ER-datamodellkonfigurasjon: Intrastat (modell)</span><span class="sxs-lookup"><span data-stu-id="327fe-117">ER data model configuration: Intrastat (model)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="327fe-118">ER-modelltilordningskonfigurasjon: Intrastat (tilordning)</span><span class="sxs-lookup"><span data-stu-id="327fe-118">ER model mapping configuration: Intrastat (mapping)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)
- [<span data-ttu-id="327fe-119">ER-formatkonfigurasjon: Intrastat (format)</span><span class="sxs-lookup"><span data-stu-id="327fe-119">ER format configuration: Intrastat (format)</span></span>](https://go.microsoft.com/fwlink/?linkid=849038)

