---
title: Oversikt over utskrift av dokument
description: Du kan skrive ut dokumenter med en lokal skriver eller en enhet som er koblet til nettverket. Denne artikkelen gir en oversikt over hvordan dokumenter skrives ut.
author: TJVass
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
audience: IT Pro, Application User
ms.reviewer: kfend
ms.search.scope: Operations, Core
ms.custom: 69161
ms.assetid: 7815bddd-c4f4-4bc3-a29b-315458065374
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 25996cbccf3e9eec6fc29b80b8241e89b5b6b4a5
ms.sourcegitcommit: 71ec2f48185b8104ca52ff70df52263ce5f87f26
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2020
ms.locfileid: "3893285"
---
# <a name="document-printing-overview"></a><span data-ttu-id="709e9-104">Oversikt over utskrift av dokument</span><span class="sxs-lookup"><span data-stu-id="709e9-104">Document printing overview</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="709e9-105">Du kan skrive ut dokumenter med en lokal skriver eller en enhet som er koblet til nettverket.</span><span class="sxs-lookup"><span data-stu-id="709e9-105">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="709e9-106">Denne artikkelen gir en oversikt over hvordan dokumenter skrives ut.</span><span class="sxs-lookup"><span data-stu-id="709e9-106">This article provides an overview of how documents are printed.</span></span>

## <a name="printing-overview"></a><span data-ttu-id="709e9-107">Oversikt over utskrift</span><span class="sxs-lookup"><span data-stu-id="709e9-107">Printing overview</span></span>

<span data-ttu-id="709e9-108">Programmet har integrerte tjenester og klientprogrammer som gjør det enkelt å generere, lagre og distribuere dokumenter som støtter forretningsaktiviteten.</span><span class="sxs-lookup"><span data-stu-id="709e9-108">The application provides integrated services and client applications that make it easy to generate, store, and distribute documents that support business activity.</span></span> <span data-ttu-id="709e9-109">Du kan skrive ut dokumenter med en lokal skriver eller en enhet som er koblet til nettverket.</span><span class="sxs-lookup"><span data-stu-id="709e9-109">You can print documents by using either a local printer or a network-connected device.</span></span> <span data-ttu-id="709e9-110">I tillegg kan du eksportere sider og rapporter direkte fra klienten, som PDF-filer eller Microsoft Office-dokumenter.</span><span class="sxs-lookup"><span data-stu-id="709e9-110">In addition, you can export pages and reports directly from the client, as PDF files or Microsoft Office documents.</span></span> <span data-ttu-id="709e9-111">Til slutt lar den distribuerte arbeidsmengden deg skrive ut forretningsdokumenter direkte fra en mobil enhet ved hjelp av nettverksressurser.</span><span class="sxs-lookup"><span data-stu-id="709e9-111">Finally, the distributed workload lets you print business documents directly from a mobile device by using network resources.</span></span> <span data-ttu-id="709e9-112">Selv om utskriftskravene kan variere, må alle bransjer vanligvis lage papirkopier av forretningsdokumenter i programmet.</span><span class="sxs-lookup"><span data-stu-id="709e9-112">Although printing requirements might vary, all industries typically must create hard copies of business documents by using the application.</span></span> <span data-ttu-id="709e9-113">Å skrive ut dokumenter på nettverksenheter fra vertsbaserte programmer gir et unikt sett med utfordringer.</span><span class="sxs-lookup"><span data-stu-id="709e9-113">Printing documents on network devices from hosted applications presents a unique set of challenges.</span></span> <span data-ttu-id="709e9-114">Her er noen eksempler:</span><span class="sxs-lookup"><span data-stu-id="709e9-114">Here are some examples:</span></span>

- <span data-ttu-id="709e9-115">Skriverdrivere er kanskje ikke tilgjengelige på brukerens enheten.</span><span class="sxs-lookup"><span data-stu-id="709e9-115">Print drivers might not be available on the user's device.</span></span>
- <span data-ttu-id="709e9-116">Brukerens enhet er kanskje ikke koblet til firmanettverket.</span><span class="sxs-lookup"><span data-stu-id="709e9-116">The user's device might not be connected to the corporate network.</span></span>

<span data-ttu-id="709e9-117">Ved hjelp av en dedikert vert og følgende enkle trinn, kan administratorer konfigurere distribusjoner slik at brukere kan skrive ut direkte fra forretningsprogrammer på nettverksenheter.</span><span class="sxs-lookup"><span data-stu-id="709e9-117">By using a dedicated host and following a few easy steps, system administrators can configure deployments so that users can print directly from business applications on network devices.</span></span>

### <a name="application-printing-scenarios"></a><span data-ttu-id="709e9-118">Scenarioer for programutskrift</span><span class="sxs-lookup"><span data-stu-id="709e9-118">Application printing scenarios</span></span> 

<span data-ttu-id="709e9-119">Tabellen nedenfor beskriver de tre primære scenarioene for utskrift.</span><span class="sxs-lookup"><span data-stu-id="709e9-119">The following table describes the three primary printing scenarios.</span></span>

| <span data-ttu-id="709e9-120">Scenario</span><span class="sxs-lookup"><span data-stu-id="709e9-120">Scenario</span></span>                        | <span data-ttu-id="709e9-121">Mål</span><span class="sxs-lookup"><span data-stu-id="709e9-121">Goal</span></span>                                                      | <span data-ttu-id="709e9-122">Løsning</span><span class="sxs-lookup"><span data-stu-id="709e9-122">Solution</span></span> |
|---------------------------------|-----------------------------------------------------------|----------|
| <span data-ttu-id="709e9-123">1. Skrive ut det du ser</span><span class="sxs-lookup"><span data-stu-id="709e9-123">1. Printing what you see</span></span>        | <span data-ttu-id="709e9-124">Skriv ut det som vises i webleseren.</span><span class="sxs-lookup"><span data-stu-id="709e9-124">Print what is currently shown in the browser.</span></span>             | <span data-ttu-id="709e9-125">Det genereres en "utskriftsvennlig" versjon av websiden for leseren.</span><span class="sxs-lookup"><span data-stu-id="709e9-125">A "print-friendly" version of the webpage is generated for the browser.</span></span> |
| <span data-ttu-id="709e9-126">2. Interaktiv utskrift</span><span class="sxs-lookup"><span data-stu-id="709e9-126">2. Interactive printing</span></span>         | <span data-ttu-id="709e9-127">Skriv ut et presisjonsdokument på en lokalt tilkoblet enhet.</span><span class="sxs-lookup"><span data-stu-id="709e9-127">Print a precision document on a locally connected device.</span></span> | <span data-ttu-id="709e9-128">Du kan eksportere en PDF-versjon av rapporten, og laste den ned til leseren.</span><span class="sxs-lookup"><span data-stu-id="709e9-128">You can export a PDF version of the report and download it to the browser.</span></span> |
| <span data-ttu-id="709e9-129">3. Skrive ut på en nettverksenhet</span><span class="sxs-lookup"><span data-stu-id="709e9-129">3. Printing on a network device</span></span> | <span data-ttu-id="709e9-130">Send et presisjonsdokument til en domeneskriverenhet.</span><span class="sxs-lookup"><span data-stu-id="709e9-130">Send a precision document to a domain printer device.</span></span>     | <span data-ttu-id="709e9-131">En presisjonsdokument blir sendt til et klientprogram som kjører på en server som ligger på kundens domene.</span><span class="sxs-lookup"><span data-stu-id="709e9-131">A precision document is sent to a client application that runs on a server that is hosted in the customer's domain.</span></span> |

<span data-ttu-id="709e9-132">Fordi løsningen varierer avhengig av scenarioet, har programmer innebygde tjenester og verktøy som kan hjelpe brukerne med å oppnå målene.</span><span class="sxs-lookup"><span data-stu-id="709e9-132">Because the solution varies, depending on the scenario, applications provide built-in services and tooling to help users accomplish their goals:</span></span>

- <span data-ttu-id="709e9-133">**Scenario 1** støttes av webleserens gjengivelse av HTML5-klienten.</span><span class="sxs-lookup"><span data-stu-id="709e9-133">**Scenario 1** is supported by the browser's rendering of the HTML5 client.</span></span>
- <span data-ttu-id="709e9-134">**Scenario 2** bruker klientprogrammer og tjenester for Microsoft 365.</span><span class="sxs-lookup"><span data-stu-id="709e9-134">**Scenario 2** uses client applications and Microsoft 365 services.</span></span>
- <span data-ttu-id="709e9-135">**Scenario 3** krever støtte fra klientprogrammer og tjenester som Microsoft Azure er vert for.</span><span class="sxs-lookup"><span data-stu-id="709e9-135">**Scenario 3** requires support from client applications and from services that are hosted in Microsoft Azure.</span></span>

<span data-ttu-id="709e9-136">I tillegg til plattformen som er distribuert til Azure-abonnementet, gir Finance and Operations kunder et integrert, førsteparts Azure-program som gjør det enklere for dem å bruke domene-vertsbaserte enheter til å skrive ut dokumenter.</span><span class="sxs-lookup"><span data-stu-id="709e9-136">In addition to the platform that is deployed to the Azure subscription, Finance and Operations applications provide customers with an integrated, first-party Azure application that helps them more easily use domain-hosted devices to print documents.</span></span>

## <a name="service-overview"></a><span data-ttu-id="709e9-137">Serviceoversikt</span><span class="sxs-lookup"><span data-stu-id="709e9-137">Service overview</span></span>
<span data-ttu-id="709e9-138">Mens dokumenter som produseres av de vertsbaserte programmene venter på å skrives ut på en enhet som er koblet til nettverket, lagres de i Azure blob-lageret.</span><span class="sxs-lookup"><span data-stu-id="709e9-138">While documents that are produced by the hosted applications are waiting to be printed on a network-connected device, they are stored in Azure blob storage.</span></span> <span data-ttu-id="709e9-139">[Installere dokumentrutingsagenten slik at nettverksutskrift kan brukes](install-document-routing-agent.md)  bruker Azure-godkjenning til å opprette en sikker kanal til Azure-tjenestene.</span><span class="sxs-lookup"><span data-stu-id="709e9-139">The [Install the Document Routing Agent to enable network printing](install-document-routing-agent.md) uses Azure authentication to establish a secure channel to the Azure services.</span></span>

<span data-ttu-id="709e9-140">**Utførelsessekvens**</span><span class="sxs-lookup"><span data-stu-id="709e9-140">**Execution sequence**</span></span>

1. <span data-ttu-id="709e9-141">Rapporten genereres av Microsoft SQL Server Reporting Services (SSRS) og lagres i Azure blob-lageret.</span><span class="sxs-lookup"><span data-stu-id="709e9-141">The report is generated by Microsoft SQL Server Reporting Services (SSRS) and stored in Azure blob storage.</span></span> <span data-ttu-id="709e9-142">Tilknyttede skriverinnstillinger lagres sammen med dokumentet.</span><span class="sxs-lookup"><span data-stu-id="709e9-142">Attached printer settings are stored together with the document.</span></span>
2. <span data-ttu-id="709e9-143">Dokumentrutingsagenten spør Azure Service Bus-køen om aktive jobber.</span><span class="sxs-lookup"><span data-stu-id="709e9-143">The Document Routing Agent queries the Azure Service Bus queue for active jobs.</span></span>
3. <span data-ttu-id="709e9-144">Dokumentet lastes ned av dokumentrutingsagenten og sendes i kø til nettverksskriveren.</span><span class="sxs-lookup"><span data-stu-id="709e9-144">The document is downloaded by the Document Routing Agent and spooled to the network printer.</span></span>

<span data-ttu-id="709e9-145">Den klientbaserte løsningen lar kundene administrere skalaen for utskriftsbehovene deres.</span><span class="sxs-lookup"><span data-stu-id="709e9-145">The client-based solution lets customers manage the scale of their printing needs.</span></span> <span data-ttu-id="709e9-146">Kunder som har store utskriftsmengder, kan installere mange dokumentrutingsagenter for å øke antallet samtidige utskriftsoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="709e9-146">Customers who have heavy-volume printing workloads can install many Document Routing Agents to increase the number of concurrent printing operations.</span></span> <span data-ttu-id="709e9-147">Noen kunder trenger også svært få installasjoner av dokumentrutingsagenten for å håndtere forventede utskriftsbehov.</span><span class="sxs-lookup"><span data-stu-id="709e9-147">Alternatively, some customers require very few installations of the Document Routing Agent to handle their anticipated printing needs.</span></span>

### <a name="service-components-for-network-printing"></a><span data-ttu-id="709e9-148">Servicekomponenter for nettverksutskrift</span><span class="sxs-lookup"><span data-stu-id="709e9-148">Service components for network printing</span></span>

<span data-ttu-id="709e9-149">Diagrammet nedenfor viser de grunnleggende komponentene som bidrar til å støtte nettverksutskriftsoperasjoner.</span><span class="sxs-lookup"><span data-stu-id="709e9-149">The following diagram shows the basic components that help support network printing operations.</span></span>

<span data-ttu-id="709e9-150">[![Servicekomponenter for nettverksutskrift\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span><span class="sxs-lookup"><span data-stu-id="709e9-150">[![service-components-for-network-printing\_2016](./media/service-components-for-network-printing_2016.png)](./media/service-components-for-network-printing_2016.png)</span></span>

<span data-ttu-id="709e9-151">Legg merke til at én enkelt skriver kan registreres med flere dokumentrutingsagenter.</span><span class="sxs-lookup"><span data-stu-id="709e9-151">Note that a single printer can be registered with multiple Document Routing Agents.</span></span> <span data-ttu-id="709e9-152">Hvis du vil løse skriverinnstillingene, bruker den vertsbaserte tjenesten nettverksbanen som entydig identifiserer hver nettverksskriver.</span><span class="sxs-lookup"><span data-stu-id="709e9-152">To resolve the printer preferences, the hosted service uses the network path that uniquely identifies every network printer.</span></span> <span data-ttu-id="709e9-153">Resultatet er at selv om en skriver er registrert av flere klienter, vises den som et enkelt valg i listen over skrivere som er tilgjengelige programmer.</span><span class="sxs-lookup"><span data-stu-id="709e9-153">As a result, even when a printer is registered by multiple clients, it appears as a single selection in the list of printers available in applications.</span></span>
