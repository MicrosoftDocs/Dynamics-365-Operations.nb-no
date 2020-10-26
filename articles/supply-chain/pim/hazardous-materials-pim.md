---
title: Farlige materialer
description: Dette emnet inneholder informasjon om dokumenter om farlige materialer samt informasjon som er lagret i miljøet.
author: lachlancashMS
manager: tfehr
ms.date: 01/10/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations, Retail
ms.custom: 19171
ms.assetid: 81fa3709-4ab8-4fbf-9806-359892a05985
ms.search.region: Global
ms.search.industry: Retail
ms.author: kamaybac
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: feee6b348ac1870295a894ad988278b23a3f30a3
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979046"
---
# <a name="hazardous-materials"></a><span data-ttu-id="8d56e-103">Farlige materialer</span><span class="sxs-lookup"><span data-stu-id="8d56e-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="8d56e-104">Informasjon om farlige materialer settes opp i administrering av produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="8d56e-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="8d56e-105">Denne modulen inneholder også dokumenter som kan skrives ut via lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="8d56e-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="8d56e-106">Når du sender materialer som er klassifisert som farlig gods, må ekstra papirarbeid inkluderes i forsendelsene.</span><span class="sxs-lookup"><span data-stu-id="8d56e-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="8d56e-107">Med funksjonaliteten for farlige materialer kan kundene lagre klassifiseringsinformasjon og relatere den til utgitte varer.</span><span class="sxs-lookup"><span data-stu-id="8d56e-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="8d56e-108">Denne informasjonen kan deretter brukes til å forenkle klargjøring av forsendelsesdokumentasjonen.</span><span class="sxs-lookup"><span data-stu-id="8d56e-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="8d56e-109">Funksjoner for farlig materiale i Microsoft Dynamics 365 Supply Chain Management tilbyr en samling av nyttige produktinformasjonsfelt og relaterte funksjoner som kan hjelpe deg med å registrere og referere til informasjon som er relatert til farlige produkter.</span><span class="sxs-lookup"><span data-stu-id="8d56e-109">The hazardous materials features in Microsoft Dynamics 365 Supply Chain Management provide a collection of useful product information fields and related functionality that can help you record and reference information that is related to your hazardous products.</span></span> <span data-ttu-id="8d56e-110">Disse funksjonene kan også hjelpe deg med å utforme og skrive ut forsendelsesdokumenter som inneholder noe av den samme informasjonen om eventuelle farlige materialer du leverer.</span><span class="sxs-lookup"><span data-stu-id="8d56e-110">These features can also help you design and print shipment documents that include some of the same information about any hazardous materials that you're shipping.</span></span> <span data-ttu-id="8d56e-111">Systemet gjør deg imidlertid ikke automatisk i samsvar med alle gjeldende forskrifter i ditt land / din region.</span><span class="sxs-lookup"><span data-stu-id="8d56e-111">However, the system won't automatically make you compliant with all applicable regulations in your country or region.</span></span> <span data-ttu-id="8d56e-112">Selv om disse verktøyene er ment å hjelpe deg å samsvare med på vanlige forskrifter, er de verken tilstrekkelig i seg selv eller garanterer at de er det.</span><span class="sxs-lookup"><span data-stu-id="8d56e-112">Although these tools are intended to help you comply with common regulations, they are neither sufficient in themselves nor guaranteed to be so.</span></span> <span data-ttu-id="8d56e-113">Organisasjonen din er ansvarlig for å være oppmerksom på alle gjeldende forskrifter og for å gjøre alle nødvendige tiltak for å samsvare med dem.</span><span class="sxs-lookup"><span data-stu-id="8d56e-113">Your organization is responsible for being aware of all applicable regulations and for taking all necessary steps to comply with them.</span></span>

<span data-ttu-id="8d56e-114">Før du kan bruke denne funksjonaliteten, kreves følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="8d56e-114">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="8d56e-115">**Administrering av produktinformasjon:** Sett opp koder som kan brukes på utgitte produkter.</span><span class="sxs-lookup"><span data-stu-id="8d56e-115">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="8d56e-116">**Lagerstyring:** Bruk ytterligere forsendelsesdokumenter til å skrive ut forsendelsesinformasjon.</span><span class="sxs-lookup"><span data-stu-id="8d56e-116">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="8d56e-117">Behandling av produktinformasjon</span><span class="sxs-lookup"><span data-stu-id="8d56e-117">Product information management</span></span>

<span data-ttu-id="8d56e-118">I Administrering av produktinformasjon er det et utvalg av oppsettstabeller der du kan legge til referanseinformasjon oppgitt i lister over farlig gods for vei-, luft- og sjøfrakt.</span><span class="sxs-lookup"><span data-stu-id="8d56e-118">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="8d56e-119">Her er noen av forskriftene som det ofte henvises til:</span><span class="sxs-lookup"><span data-stu-id="8d56e-119">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="8d56e-120">**ADR** – Forskrifter som er knyttet til den internasjonale transporten av farlige gods på veier</span><span class="sxs-lookup"><span data-stu-id="8d56e-120">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="8d56e-121">**CFR 49** – Forskrifter i USA for transport av farlig gods</span><span class="sxs-lookup"><span data-stu-id="8d56e-121">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="8d56e-122">**IMDG** – Den internasjonale koden for farlige maringods (IMDG, International Marine Dangerous Goods)</span><span class="sxs-lookup"><span data-stu-id="8d56e-122">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="8d56e-123">**IATA** – Forskriftene til det internasjonale lufttransportforbundet (IATA, International Air Transport Association) for farlig gods</span><span class="sxs-lookup"><span data-stu-id="8d56e-123">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="8d56e-124">Hver av disse forskriftene har en liste over farlig gods som inkluderer referansekoder.</span><span class="sxs-lookup"><span data-stu-id="8d56e-124">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="8d56e-125">Listene for hver transporttype kombineres på delte internasjonale klassifiseringer.</span><span class="sxs-lookup"><span data-stu-id="8d56e-125">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="8d56e-126">Supply Chain Management inneholder en referansetabell for de delte kodene i disse listene.</span><span class="sxs-lookup"><span data-stu-id="8d56e-126">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="8d56e-127">Hver liste har også noen unike koder som kan defineres.</span><span class="sxs-lookup"><span data-stu-id="8d56e-127">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="8d56e-128">Hvis du vil begynne å konfigurere denne informasjonen, oppretter du en forskrift som du kan bruke til å konfigurere de opprinnelige parameterne.</span><span class="sxs-lookup"><span data-stu-id="8d56e-128">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="8d56e-129">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="8d56e-129">Warehouse management</span></span>

<span data-ttu-id="8d56e-130">Når en forsendelse er klargjort, kan flere nye rapporter skrives ut.</span><span class="sxs-lookup"><span data-stu-id="8d56e-130">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="8d56e-131">Disse rapportene bruker informasjonen du definerer i Administrering av produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="8d56e-131">These reports use the information that you set up in Product information management.</span></span>
