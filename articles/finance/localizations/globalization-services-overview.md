---
title: Dynamics 365-globaliseringstjenester
description: Dette emnet gir en oversikt over Microsoft Dynamics 365-globaliseringstjenester.
author: JaneA07
manager: AnnBe
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: RCS, Regulatory Configuration Services, Localization, Electronic invoicing, Tax calculation
audience: Application User
ms.reviewer: kfend
ms.custom: 97423
ms.assetid: ''
ms.search.region: Global
ms.author: janeaug
ms.search.validFrom: 2020-02-01
ms.dyn365.ops.version: AX 10.0.9
ms.openlocfilehash: 8c6f3b7fb4dec0dffe55014e9e2d60620dc3b193
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5893054"
---
# <a name="dynamics-365-globalization-services"></a><span data-ttu-id="50810-103">Dynamics 365-globaliseringstjenester</span><span class="sxs-lookup"><span data-stu-id="50810-103">Dynamics 365 globalization services</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50810-104">Følgende globaliseringstjenester kan konfigureres slik at de utvider funksjonene som finnes i enkelte Microsoft Dynamics 365 Online-tjenester:</span><span class="sxs-lookup"><span data-stu-id="50810-104">The following globalization services can be configured to extend the capabilities that exist in some Microsoft Dynamics 365 online services:</span></span>

- <span data-ttu-id="50810-105">**Regulatory Configuration Service (RCS)** støtter konfigurasjonen av ulike typer elektroniske dokumenter og rapporter.</span><span class="sxs-lookup"><span data-stu-id="50810-105">**Regulatory Configuration Service (RCS)** supports the configuration of different types of electronic documents and reports.</span></span> <span data-ttu-id="50810-106">RCS er en utvidet versjon av ER-designeren (Elektronisk rapportering) der konfigurasjonsrepositoriet er en frittstående tjeneste.</span><span class="sxs-lookup"><span data-stu-id="50810-106">RCS provides an enhanced version of the Electronic reporting (ER) designer where the configuration repository is a standalone service.</span></span> <span data-ttu-id="50810-107">Hvis du vil ha mer informasjon, kan du se [Regulatory Configuration Service](rcs-overview.md).</span><span class="sxs-lookup"><span data-stu-id="50810-107">For more information, see [Regulatory Configuration Service](rcs-overview.md).</span></span>
- <span data-ttu-id="50810-108">**Elektronisk fakturering** samler sammen konfigurerbare formater for transformasjoner, digitale signaturer og konfigurerbare integrasjoner for tilkobling med eksterne nettjenester, inkludert sertifisering og svarbehandling.</span><span class="sxs-lookup"><span data-stu-id="50810-108">**Electronic Invoicing** brings together configurable formats for transformations, digital signatures, and configurable integrations for connectivity with external web services, including certification and response handling.</span></span> <span data-ttu-id="50810-109">For mer informasjon, se [Elektronisk fakturering](e-invoicing-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="50810-109">For more information, see [Electronic Invoicing](e-invoicing-service-overview.md).</span></span>
- <span data-ttu-id="50810-110">**Avgiftsberegning** gir utvidet fleksibilitet ved å støtte flere avgifts-ID-er, fastsettelse av mva-koder, avgiftsberegningsdesigneren og en kjøretidsmotor for å overholde komplekse avgiftsbestemmelser over hele verden.</span><span class="sxs-lookup"><span data-stu-id="50810-110">**Tax Calculation** provides enhanced flexibility by supporting multiple tax IDs, tax code determination, the tax calculation designer, and a runtime engine to comply with complex tax regulations worldwide.</span></span> <span data-ttu-id="50810-111">Hvis du vil ha mer informasjon, kan du se [Avgiftsberegning](global-tax-calcuation-service-overview.md).</span><span class="sxs-lookup"><span data-stu-id="50810-111">For more information, see [Tax Calculation](global-tax-calcuation-service-overview.md).</span></span>

<span data-ttu-id="50810-112">Disse globaliseringstjenestene sørger for direkte integrasjon med følgende Dynamics 365-onlinetjenester.</span><span class="sxs-lookup"><span data-stu-id="50810-112">These globalization services provide out-of-box integration with the following Dynamics 365 online services.</span></span>

| <span data-ttu-id="50810-113">Onlinetjeneste</span><span class="sxs-lookup"><span data-stu-id="50810-113">Online service</span></span> | <span data-ttu-id="50810-114">RCS</span><span class="sxs-lookup"><span data-stu-id="50810-114">RCS</span></span> | <span data-ttu-id="50810-115">Elektronisk fakturering</span><span class="sxs-lookup"><span data-stu-id="50810-115">Electronic Invoicing</span></span> | <span data-ttu-id="50810-116">Avgiftsberegning (forhåndsversjon)</span><span class="sxs-lookup"><span data-stu-id="50810-116">Tax Calculation (Preview)</span></span> |
|----------------|-----|----------------------|---------------------------|
| <span data-ttu-id="50810-117">Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="50810-117">Dynamics 365 Finance</span></span> | <span data-ttu-id="50810-118">Ja</span><span class="sxs-lookup"><span data-stu-id="50810-118">Yes</span></span> | <span data-ttu-id="50810-119">Ja</span><span class="sxs-lookup"><span data-stu-id="50810-119">Yes</span></span> | <span data-ttu-id="50810-120">Ja</span><span class="sxs-lookup"><span data-stu-id="50810-120">Yes</span></span> | 
| <span data-ttu-id="50810-121">Dynamics 365 Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="50810-121">Dynamics 365 Supply Chain Management</span></span> | <span data-ttu-id="50810-122">Ja</span><span class="sxs-lookup"><span data-stu-id="50810-122">Yes</span></span> | <span data-ttu-id="50810-123">Ja</span><span class="sxs-lookup"><span data-stu-id="50810-123">Yes</span></span> | <span data-ttu-id="50810-124">Ja</span><span class="sxs-lookup"><span data-stu-id="50810-124">Yes</span></span> | 
| <span data-ttu-id="50810-125">Dynamics 365 Project Operations</span><span class="sxs-lookup"><span data-stu-id="50810-125">Dynamics 365 Project Operations</span></span> | <span data-ttu-id="50810-126">Ja</span><span class="sxs-lookup"><span data-stu-id="50810-126">Yes</span></span> | <span data-ttu-id="50810-127">Ja</span><span class="sxs-lookup"><span data-stu-id="50810-127">Yes</span></span> | <span data-ttu-id="50810-128">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="50810-128">Not applicable</span></span> | 
| <span data-ttu-id="50810-129">Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="50810-129">Dynamics 365 Commerce</span></span> | <span data-ttu-id="50810-130">Ja</span><span class="sxs-lookup"><span data-stu-id="50810-130">Yes</span></span> | <span data-ttu-id="50810-131">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="50810-131">Not applicable</span></span> | <span data-ttu-id="50810-132">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="50810-132">Not applicable</span></span> | 

> [!NOTE]
> <span data-ttu-id="50810-133">På grunn av forskjeller i tilgjengeligheten av geografiske Azure-lokasjoner for RCS kan konfigurasjon av denne tjenesten føre til at kundedata overføres utenfor den geografiske lokasjonen som er valgt for den aktuelle Dynamics 365-onlinetjenesten.</span><span class="sxs-lookup"><span data-stu-id="50810-133">Because of differences in the availability of Azure geographic locations (geos) for RCS, configuration of this service might cause customer data to be transferred outside the geo that is selected for the applicable Dynamics 365 online service.</span></span> <span data-ttu-id="50810-134">Hvis du vil ha mer informasjon, kan du se [Dynamics 365 og Power Platform: Tilgjengelighet, dataplassering, språk og lokalisering](https://aka.ms/rcs/D365Productavailabilityguide).</span><span class="sxs-lookup"><span data-stu-id="50810-134">For more information, see [Dynamics 365 and Power Platform: Availability, data location, language, and localization](https://aka.ms/rcs/D365Productavailabilityguide).</span></span>