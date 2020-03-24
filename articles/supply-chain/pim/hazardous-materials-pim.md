---
title: Farlige materialer
description: Dette emnet inneholder informasjon om dokumenter om farlige materialer samt informasjon som er lagret i miljøet.
author: lachlancashMS
manager: AnnBe
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
ms.author: conradv
ms.search.validFrom: 2019-10-14
ms.dyn365.ops.version: ''
ms.openlocfilehash: 443d2eb545b2b7592e27ae037009720db0a71997
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092551"
---
# <a name="hazardous-materials"></a><span data-ttu-id="17c35-103">Farlige materialer</span><span class="sxs-lookup"><span data-stu-id="17c35-103">Hazardous materials</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="17c35-104">Informasjon om farlige materialer settes opp i administrering av produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="17c35-104">Information about hazardous materials is set up in Product information management.</span></span> <span data-ttu-id="17c35-105">Denne modulen inneholder også dokumenter som kan skrives ut via lagerstyring.</span><span class="sxs-lookup"><span data-stu-id="17c35-105">This module also provides documents that can be printed through warehouse management.</span></span>

<span data-ttu-id="17c35-106">Når du sender materialer som er klassifisert som farlig gods, må ekstra papirarbeid inkluderes i forsendelsene.</span><span class="sxs-lookup"><span data-stu-id="17c35-106">When you ship materials that are classified as dangerous goods, additional paperwork must be included with the shipments.</span></span> <span data-ttu-id="17c35-107">Med funksjonaliteten for farlige materialer kan kundene lagre klassifiseringsinformasjon og relatere den til utgitte varer.</span><span class="sxs-lookup"><span data-stu-id="17c35-107">The hazardous materials functionality lets customers store classification information and relate it to release items.</span></span> <span data-ttu-id="17c35-108">Denne informasjonen kan deretter brukes til å forenkle klargjøring av forsendelsesdokumentasjonen.</span><span class="sxs-lookup"><span data-stu-id="17c35-108">This information can then be used to help prepare shipping documentation.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="17c35-109">For å forenkle administrering av forsendelser av farlig gods lar Microsoft Dynamics 365 Supply Chain Management deg sette opp ytterligere referanseinformasjon relatert til produkter.</span><span class="sxs-lookup"><span data-stu-id="17c35-109">To help manage shipments of dangerous goods, Microsoft Dynamics 365 Supply Chain Management lets you set up additional reference information that is related to products.</span></span> <span data-ttu-id="17c35-110">Du kan også sette opp ytterligere forsendelsesdokumenter.</span><span class="sxs-lookup"><span data-stu-id="17c35-110">You can also set up additional shipment documents.</span></span> <span data-ttu-id="17c35-111">Systemet er imidlertid ikke automatisk i samsvar med forskriftene i ditt land / din region.</span><span class="sxs-lookup"><span data-stu-id="17c35-111">However, the system isn't automatically compliant with your country's or region's regulations.</span></span> <span data-ttu-id="17c35-112">Det er i stedet et verktøy som kan hjelpe deg med det samlede programmet.</span><span class="sxs-lookup"><span data-stu-id="17c35-112">Instead, it's a tool that can help your overall program.</span></span>

<span data-ttu-id="17c35-113">Før du kan bruke denne funksjonaliteten, kreves følgende konfigurasjon:</span><span class="sxs-lookup"><span data-stu-id="17c35-113">Before you can use this functionality, the following setup is required:</span></span>

- <span data-ttu-id="17c35-114">**Administrering av produktinformasjon:** Sett opp koder som kan brukes på utgitte produkter.</span><span class="sxs-lookup"><span data-stu-id="17c35-114">**Product information management:** Set up codes that can be applied to released products.</span></span>
- <span data-ttu-id="17c35-115">**Lagerstyring:** Bruk ytterligere forsendelsesdokumenter til å skrive ut forsendelsesinformasjon.</span><span class="sxs-lookup"><span data-stu-id="17c35-115">**Warehouse management:** Use additional shipping documents to print shipment information.</span></span>

## <a name="product-information-management"></a><span data-ttu-id="17c35-116">Behandling av produktinformasjon</span><span class="sxs-lookup"><span data-stu-id="17c35-116">Product information management</span></span>

<span data-ttu-id="17c35-117">I Administrering av produktinformasjon er det et utvalg av oppsettstabeller der du kan legge til referanseinformasjon oppgitt i lister over farlig gods for vei-, luft- og sjøfrakt.</span><span class="sxs-lookup"><span data-stu-id="17c35-117">In Product information management, there is a range of setup tables where you can add the reference information that is provided in the dangerous goods lists for road, air, and sea freight.</span></span>

<span data-ttu-id="17c35-118">Her er noen av forskriftene som det ofte henvises til:</span><span class="sxs-lookup"><span data-stu-id="17c35-118">Here are some of the regulations that are often referenced:</span></span>

- <span data-ttu-id="17c35-119">**ADR** – Forskrifter som er knyttet til den internasjonale transporten av farlige gods på veier</span><span class="sxs-lookup"><span data-stu-id="17c35-119">**ADR** – Regulations that are related to the international carriage of dangerous goods by road</span></span>
- <span data-ttu-id="17c35-120">**CFR 49** – Forskrifter i USA for transport av farlig gods</span><span class="sxs-lookup"><span data-stu-id="17c35-120">**CFR 49** – Regulations in the United Sates for the carriage of dangerous goods</span></span>
- <span data-ttu-id="17c35-121">**IMDG** – Den internasjonale koden for farlige maringods (IMDG, International Marine Dangerous Goods)</span><span class="sxs-lookup"><span data-stu-id="17c35-121">**IMDG** – The International Marine Dangerous Goods (IMDG) code</span></span>
- <span data-ttu-id="17c35-122">**IATA** – Forskriftene til det internasjonale lufttransportforbundet (IATA, International Air Transport Association) for farlig gods</span><span class="sxs-lookup"><span data-stu-id="17c35-122">**IATA** – The International Air Transport Association (IATA) dangerous goods regulations</span></span>

<span data-ttu-id="17c35-123">Hver av disse forskriftene har en liste over farlig gods som inkluderer referansekoder.</span><span class="sxs-lookup"><span data-stu-id="17c35-123">Each of these regulations has a dangerous goods list that includes reference codes.</span></span> <span data-ttu-id="17c35-124">Listene for hver transporttype kombineres på delte internasjonale klassifiseringer.</span><span class="sxs-lookup"><span data-stu-id="17c35-124">The lists for each type of transport are combined on shared international classifications.</span></span> <span data-ttu-id="17c35-125">Supply Chain Management inneholder en referansetabell for de delte kodene i disse listene.</span><span class="sxs-lookup"><span data-stu-id="17c35-125">Supply Chain Management provides a reference table for the shared codes in those lists.</span></span> <span data-ttu-id="17c35-126">Hver liste har også noen unike koder som kan defineres.</span><span class="sxs-lookup"><span data-stu-id="17c35-126">Each list also has some unique codes that can be defined.</span></span>

<span data-ttu-id="17c35-127">Hvis du vil begynne å konfigurere denne informasjonen, oppretter du en forskrift som du kan bruke til å konfigurere de opprinnelige parameterne.</span><span class="sxs-lookup"><span data-stu-id="17c35-127">To start to configure this information, create a regulation that you can use to configure the initial parameters.</span></span>

## <a name="warehouse-management"></a><span data-ttu-id="17c35-128">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="17c35-128">Warehouse management</span></span>

<span data-ttu-id="17c35-129">Når en forsendelse er klargjort, kan flere nye rapporter skrives ut.</span><span class="sxs-lookup"><span data-stu-id="17c35-129">When a shipment is prepared, several new reports can be printed.</span></span> <span data-ttu-id="17c35-130">Disse rapportene bruker informasjonen du definerer i Administrering av produktinformasjon.</span><span class="sxs-lookup"><span data-stu-id="17c35-130">These reports use the information that you set up in Product information management.</span></span>
