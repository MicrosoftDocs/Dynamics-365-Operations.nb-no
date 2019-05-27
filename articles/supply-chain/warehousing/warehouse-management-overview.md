---
title: Lagerstyring
description: Bruk Lagerstyring til å overvåke og automatisere lagerprosesser.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c9613070e077bced4b272b136985de5f4ddbdd0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543405"
---
# <a name="warehouse-management"></a><span data-ttu-id="8ed51-103">Lagerstyring</span><span class="sxs-lookup"><span data-stu-id="8ed51-103">Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ed51-104">Med lagerstyringsmodulen for Dynamics 365 for Finance and Operations kan du administrere lagerprosesser i produksjons-, distribusjons- og detaljhandelfirmaer.</span><span class="sxs-lookup"><span data-stu-id="8ed51-104">The Warehouse management module for Dynamics 365 for Finance and Operations lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="8ed51-105">Denne modulen har et bredt spekter av funksjoner for å støtte lageret på et optimalt nivå, når som helst.</span><span class="sxs-lookup"><span data-stu-id="8ed51-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="8ed51-106">Lagerstyring er fullt integrert med andre forretningsprosesser i Finance and Operations, slik som transport, produksjon, kvalitetskontroll, innkjøp, overføring, salg og retur.</span><span class="sxs-lookup"><span data-stu-id="8ed51-106">Warehouse management is fully integrated with other business processes in Finance and Operations such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="8ed51-107">Komme i gang</span><span class="sxs-lookup"><span data-stu-id="8ed51-107">Get started</span></span>
<span data-ttu-id="8ed51-108">For å begynne å jobbe med Lagerstyring må du fullføre oppsetttet av generelle lagerparametere for å støtte virksomhetsprosessene til selskapet ditt.</span><span class="sxs-lookup"><span data-stu-id="8ed51-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of you company.</span></span>

- <span data-ttu-id="8ed51-109">Gå til siden **Parametere for lagerstyring** under **Lagerstyring** > **Oppsett** for å sette opp generelle lagerparametere.</span><span class="sxs-lookup"><span data-stu-id="8ed51-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="8ed51-110">Du må konfigurere komponenter for arbeidsflyten for inngående og utgående lagerprosesser i henhold til bedriftens krav.</span><span class="sxs-lookup"><span data-stu-id="8ed51-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="8ed51-111">De viktigste komponentene du må konfigurere, er bølgemaler, arbeidsmaler, arbeidsutvalg og lokasjonsdirektiver.</span><span class="sxs-lookup"><span data-stu-id="8ed51-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="8ed51-112">Lagerkonfigurasjon</span><span class="sxs-lookup"><span data-stu-id="8ed51-112">Warehouse configuration</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="8ed51-113">Kontrollere lagerarbeid ved hjelp av arbeidsmaler og lokasjonsdirektiver</span><span class="sxs-lookup"><span data-stu-id="8ed51-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="8ed51-114">Definere mobilenheter for lagerarbeid</span><span class="sxs-lookup"><span data-stu-id="8ed51-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="8ed51-115">Definere et lokasjonsdirektiv for bestillings</span><span class="sxs-lookup"><span data-stu-id="8ed51-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="8ed51-116">Definere en arbeidsmal for bestillinger</span><span class="sxs-lookup"><span data-stu-id="8ed51-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="8ed51-117">Lagerstyringsprosesser</span><span class="sxs-lookup"><span data-stu-id="8ed51-117">Warehouse management processes</span></span>
- <span data-ttu-id="8ed51-118">Integrert støtte for kildedokumenter for salgsordrer, returer, overføringsordrer, produksjonsordrer og kanban</span><span class="sxs-lookup"><span data-stu-id="8ed51-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="8ed51-119">Fleksibel, inngående og utgående arbeidsflytstøtte for materiale basert på spørringer</span><span class="sxs-lookup"><span data-stu-id="8ed51-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="8ed51-120">Full integrasjon med produksjon- og transporttilbud</span><span class="sxs-lookup"><span data-stu-id="8ed51-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="8ed51-121">Full kontroll over stedsgrenseverdier og plasseringsvolumetri</span><span class="sxs-lookup"><span data-stu-id="8ed51-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="8ed51-122">Inventaregenskaper kontrollert av lagerstatus</span><span class="sxs-lookup"><span data-stu-id="8ed51-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="8ed51-123">Full batch- og serienummerstøtte</span><span class="sxs-lookup"><span data-stu-id="8ed51-123">Full batch and serial item support</span></span>
- <span data-ttu-id="8ed51-124">Ulike elementmottaksevner</span><span class="sxs-lookup"><span data-stu-id="8ed51-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="8ed51-125">Flere plukstrategier</span><span class="sxs-lookup"><span data-stu-id="8ed51-125">Multiple picking strategies</span></span>
- <span data-ttu-id="8ed51-126">Ut-av-boksen-støtte for neste generasjon strekkodeskannere</span><span class="sxs-lookup"><span data-stu-id="8ed51-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="8ed51-127">Pall-/beholdertyper for lagerprosesser</span><span class="sxs-lookup"><span data-stu-id="8ed51-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="8ed51-128">Avanserte tellingsfunksjoner</span><span class="sxs-lookup"><span data-stu-id="8ed51-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="8ed51-129">Etikettutskrift og etikettruting med Zebra ZPL-støtte</span><span class="sxs-lookup"><span data-stu-id="8ed51-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="8ed51-130">Business Intelligence-integrasjon i Power BI</span><span class="sxs-lookup"><span data-stu-id="8ed51-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="8ed51-131">Manuell og automatisk bevegelse av lager</span><span class="sxs-lookup"><span data-stu-id="8ed51-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="8ed51-132">Fullintegrert kvalitetskontroll (QMS)</span><span class="sxs-lookup"><span data-stu-id="8ed51-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="8ed51-133">Full sporbarhet av arbeidstakernes materialhåndtering</span><span class="sxs-lookup"><span data-stu-id="8ed51-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="8ed51-134">Utgående bølgebehandling</span><span class="sxs-lookup"><span data-stu-id="8ed51-134">Outbound wave processing</span></span>
- <span data-ttu-id="8ed51-135">Manuell pakking og automatisk containerstøtte</span><span class="sxs-lookup"><span data-stu-id="8ed51-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="8ed51-136">Gruppeplukking</span><span class="sxs-lookup"><span data-stu-id="8ed51-136">Cluster picking</span></span>
- <span data-ttu-id="8ed51-137">Enkel direkteoverføring</span><span class="sxs-lookup"><span data-stu-id="8ed51-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="8ed51-138">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="8ed51-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="8ed51-139">Hva er nytt og hva er under utvikling?</span><span class="sxs-lookup"><span data-stu-id="8ed51-139">What's new and in development</span></span>
<span data-ttu-id="8ed51-140">Gå til [Veikart for Microsoft Dynamics 365](https://roadmap.dynamics.com/) for å se hvilke nye funksjoner som har blitt utgitt og hvilke nye funksjoner som er under utvikling.</span><span class="sxs-lookup"><span data-stu-id="8ed51-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="8ed51-141">Blogger</span><span class="sxs-lookup"><span data-stu-id="8ed51-141">Blogs</span></span>
<span data-ttu-id="8ed51-142">Du kan finne meninger, nyheter og annen informasjon om Lagerstyring og andre løsninger på [Microsoft Dynamics 365-bloggen](https://community.dynamics.com/b/msftdynamicsblog).</span><span class="sxs-lookup"><span data-stu-id="8ed51-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 

