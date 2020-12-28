---
title: Oversikt over farlige materialer
description: Dette emnet gir en oversikt over funksjoner som er knyttet til håndtering og dokumentasjon av farlige materialer under produktinformasjonsbehandling og lagerstyring.
author: dasani-madipalli
manager: tfehr
ms.date: 06/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: damadipa
ms.search.validFrom: 2020-06-10
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: 34c0a19308bb5159faa9a4ab06bf65e58da0deb1
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434161"
---
# <a name="hazardous-materials-overview"></a><span data-ttu-id="74dca-103">Oversikt over farlige materialer</span><span class="sxs-lookup"><span data-stu-id="74dca-103">Hazardous materials overview</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="74dca-104">For å overholde samsvar med leverings- og transportforskrifter må organisasjoner som leverer materialer som er klassifisert som farlige varer, inkludere ekstra papirarbeid med forsendelsene.</span><span class="sxs-lookup"><span data-stu-id="74dca-104">To remain compliant with shipping and transport regulations, organizations that ship materials that are classified as dangerous goods must include additional paperwork with their shipments.</span></span> <span data-ttu-id="74dca-105">Med funksjonen for farlige materialer kan kundene lagre informasjon som er relatert til frigitte varer.</span><span class="sxs-lookup"><span data-stu-id="74dca-105">The hazardous materials feature lets customers store information that is related to released items.</span></span> <span data-ttu-id="74dca-106">Denne informasjonen kan deretter brukes til å forenkle klargjøring av forsendelsesdokumentasjonen.</span><span class="sxs-lookup"><span data-stu-id="74dca-106">This information can then be used to help prepare shipping documentation.</span></span> <span data-ttu-id="74dca-107">En organisasjon som leverer farlige varer, må ha sine egne prosesser og prosedyrer for å administrere forsendelsesprosessen.</span><span class="sxs-lookup"><span data-stu-id="74dca-107">An organization that ships dangerous goods must have its own processes and procedures for managing the shipping process.</span></span> <span data-ttu-id="74dca-108">Microsoft Dynamics 365 Supply Chain Management er bare et verktøy som kan hjelpe deg med å generere de nødvendige dokumentene.</span><span class="sxs-lookup"><span data-stu-id="74dca-108">Microsoft Dynamics 365 Supply Chain Management is just a tool that can help generate the required documents.</span></span>

<span data-ttu-id="74dca-109">Diagrammet nedenfor illustrerer trinnene som trengs for å definere og bruke farlige materialer-funksjonen.</span><span class="sxs-lookup"><span data-stu-id="74dca-109">The following diagram illustrates the steps needed to set up and use the hazardous materials feature.</span></span>

<span data-ttu-id="74dca-110">![Oppsett og bruk av farlig materiale-funksjonen](media/hazmat-overview.png "Oppsett og bruk av farlig materiale-funksjonen")</span><span class="sxs-lookup"><span data-stu-id="74dca-110">![Setup and use of the hazardous materials feature](media/hazmat-overview.png "Setup and use of the hazardous materials feature")</span></span>

<span data-ttu-id="74dca-111">Farlige materialer-funksjonen er definert i Behandling av produktinformasjon og inneholder dokumenter som kan skrives ut via Lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="74dca-111">The hazardous materials feature is set up in Product information management and provides documents that can be printed through Warehouse management.</span></span> <span data-ttu-id="74dca-112">Derfor er disse områdene de to hovedområdene der du ser gjennom, konfigurerer og bruker funksjonaliteten til denne funksjonen:</span><span class="sxs-lookup"><span data-stu-id="74dca-112">Therefore, broadly speaking, those areas are the two main areas where you will review, set up, and use this feature's functionality:</span></span>

- <span data-ttu-id="74dca-113">**Behandling av produktinformasjon:** – Konfigurer kodene som skal brukes på et utgitt produkt.</span><span class="sxs-lookup"><span data-stu-id="74dca-113">**Product information management** – Set up the codes that will be applied to a released product.</span></span>
- <span data-ttu-id="74dca-114">**Lagerstyring** – Arbeid med ekstra forsendelsesdokumenter som skal skrives ut for forsendelser.</span><span class="sxs-lookup"><span data-stu-id="74dca-114">**Warehouse management** – Work with additional shipping documents that will be printed for shipments.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="74dca-115">Funksjoner for farlig materiale i Supply Chain Management tilbyr en samling av nyttige produktinformasjonsfelt og relaterte funksjoner som kan hjelpe deg med å registrere og referere til informasjon som er relatert til farlige produkter.</span><span class="sxs-lookup"><span data-stu-id="74dca-115">The hazardous materials features in Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="74dca-116">Disse funksjonene kan også hjelpe deg med å utforme og skrive ut forsendelsesdokumenter som inneholder noe av den samme informasjonen om eventuelle farlige materialer du leverer.</span><span class="sxs-lookup"><span data-stu-id="74dca-116">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="74dca-117">Systemet gjør deg imidlertid ikke automatisk i samsvar med alle gjeldende forskrifter i ditt land / din region.</span><span class="sxs-lookup"><span data-stu-id="74dca-117">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="74dca-118">Selv om disse verktøyene er ment å hjelpe deg å samsvare med på vanlige forskrifter, er de verken tilstrekkelig i seg selv eller garanterer at de er det.</span><span class="sxs-lookup"><span data-stu-id="74dca-118">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="74dca-119">Organisasjonen din er ansvarlig for å være oppmerksom på alle gjeldende forskrifter og for å gjøre alle nødvendige tiltak for å samsvare med dem.</span><span class="sxs-lookup"><span data-stu-id="74dca-119">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="74dca-120">Behandling av produktinformasjon</span><span class="sxs-lookup"><span data-stu-id="74dca-120">Product information management</span></span>

<span data-ttu-id="74dca-121">Behandling av produktinformasjon inneholder et utvalg av oppsettabeller der du kan angi referanseinformasjon for de ulike listene over farlige varer for vei-, luft- og sjøfrakt.</span><span class="sxs-lookup"><span data-stu-id="74dca-121">Product information management provides a range of setup tables where you can enter reference information for the various dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="74dca-122">Følgende felles forskrifter ble referert til da denne funksjonaliteten ble utviklet:</span><span class="sxs-lookup"><span data-stu-id="74dca-122">The following common regulations were referenced when this functionality was developed:</span></span>

- <span data-ttu-id="74dca-123">**ADR** – Forskrifter som er knyttet til den internasjonale transporten av farlige gods på veier</span><span class="sxs-lookup"><span data-stu-id="74dca-123">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="74dca-124">**CFR 49** – Forskrifter i USA for transport av farlig gods</span><span class="sxs-lookup"><span data-stu-id="74dca-124">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="74dca-125">**IMDG** – Den internasjonale koden for farlige maringods (IMDG, International Marine Dangerous Goods)</span><span class="sxs-lookup"><span data-stu-id="74dca-125">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="74dca-126">**IATA** – Forskriftene til det internasjonale lufttransportforbundet (IATA, International Air Transport Association) for farlig gods</span><span class="sxs-lookup"><span data-stu-id="74dca-126">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="74dca-127">Hvert sett med forskrifter inneholder standardiserte lister over farlige varer og referansekoder.</span><span class="sxs-lookup"><span data-stu-id="74dca-127">Each set of regulations provides standardized lists of dangerous goods and reference codes.</span></span> <span data-ttu-id="74dca-128">Supply Chain Management inneholder derfor en referansetabell for de felles kodene i disse listene.</span><span class="sxs-lookup"><span data-stu-id="74dca-128">Therefore, Supply Chain Management provides a reference table for the common codes on those lists.</span></span> <span data-ttu-id="74dca-129">Hver liste har også noen unike koder som du kan definere.</span><span class="sxs-lookup"><span data-stu-id="74dca-129">Each list also has some unique codes that you can define.</span></span>

<span data-ttu-id="74dca-130">Hvis du vil ha mer informasjon om hvordan du definerer forskrifter og verdier for farlige materialer, og hvordan du tilordner verdiene til de relevante produktene, kan du se følgende emner:</span><span class="sxs-lookup"><span data-stu-id="74dca-130">For more information about how to set up regulations and values for hazardous materials, and how to assign the values to relevant products, see the following topics:</span></span>

- [<span data-ttu-id="74dca-131">Definere farlige materialer</span><span class="sxs-lookup"><span data-stu-id="74dca-131">Set up hazardous materials</span></span>](hazmat-setup.md)
- [<span data-ttu-id="74dca-132">Farlige materialer i produkter, ordrer, forsendelser og laster</span><span class="sxs-lookup"><span data-stu-id="74dca-132">Hazardous materials in products, orders, shipments, and loads</span></span>](hazmat-items.md)

## <a name="warehouse-management"></a><span data-ttu-id="74dca-133">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="74dca-133">Warehouse management</span></span>

<span data-ttu-id="74dca-134">Når du klargjør en forsendelse i Lagerstyring, vil du kunne skrive ut flere nye rapporter som bruker informasjonen du har definert i Behandling av produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="74dca-134">When you prepare a shipment in Warehouse management, you will be able to print several new reports that use the information that you set up in Product information management.</span></span> <span data-ttu-id="74dca-135">Hvis du vil ha mer informasjon om tilgjengelige rapporter og hvordan du bruker dem, kan du se [Forespørsler og rapporter om farlige materialer](hazmat-reports.md).</span><span class="sxs-lookup"><span data-stu-id="74dca-135">For more information about the available reports and how to use them, see [Hazardous materials inquiries and reports](hazmat-reports.md).</span></span>
