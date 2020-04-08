---
title: Oversikt over dobbel skriving
description: Dette emnet gir en oversikt over dobbel skriving. Dobbel skriving er en infrastruktur som gir nær sanntids interaksjon mellom modelldrevne Microsoft Dynamics 365-apper og Finance and Operations-apper.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 02/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 64626ebdd7fbad3d47a4b4c6bbc45bf3bc0c8277
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172790"
---
# <a name="dual-write-overview"></a><span data-ttu-id="91cf9-104">Oversikt over dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="91cf9-104">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="91cf9-105">Hva er dobbel skriving?</span><span class="sxs-lookup"><span data-stu-id="91cf9-105">What is dual-write?</span></span>

<span data-ttu-id="91cf9-106">Dobbel skriving er en integrert infrastruktur som gir nær sanntids interaksjon mellom modelldrevne apper i Microsoft Dynamics 365 og Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="91cf9-106">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between model-driven apps in Microsoft Dynamics 365 and Finance and Operations apps.</span></span> <span data-ttu-id="91cf9-107">Når data om kunder, produkter, personer og operasjoner flyter utenfor applikasjonens grenser, kan alle avdelingene i en organisasjon være på.</span><span class="sxs-lookup"><span data-stu-id="91cf9-107">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="91cf9-108">Dobbel skriving gir tett sammenkoblet, toveis integrering mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="91cf9-108">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="91cf9-109">Alle dataendringer i Finance and Operations-apper fører til skriving til Common Data Service, og alle dataendringer i Common Data Service fører til skriving til Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="91cf9-109">Any data change in Finance and Operations apps causes writes to Common Data Service, and any data change in Common Data Service causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="91cf9-110">Denne automatiserte dataflyten gir en integrert brukeropplevelse på tvers av appene.</span><span class="sxs-lookup"><span data-stu-id="91cf9-110">This automated data flow provides an integrated user experience across the apps.</span></span>

![Datarelasjon mellom apper](media/dual-write-overview.jpg)

<span data-ttu-id="91cf9-112">Dobbel skriving har to aspkter: *infrastruktur* og *app*.</span><span class="sxs-lookup"><span data-stu-id="91cf9-112">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="91cf9-113">Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="91cf9-113">Infrastructure</span></span>

<span data-ttu-id="91cf9-114">Infrastrukturen for dobbel skriving er utvidbar og pålitelig, og inneholder følgende nøkkelfunksjoner:</span><span class="sxs-lookup"><span data-stu-id="91cf9-114">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="91cf9-115">Synkron og toveis dataflyt mellom programmer</span><span class="sxs-lookup"><span data-stu-id="91cf9-115">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="91cf9-116">Synkronisering sammen med modus for avspilling, pause og oppsamling for å støtte systemet under tilkoblet og frakoblet/asynkron modus.</span><span class="sxs-lookup"><span data-stu-id="91cf9-116">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="91cf9-117">Mulighet til å synkronisere innledende data mellom apper</span><span class="sxs-lookup"><span data-stu-id="91cf9-117">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="91cf9-118">Konsolidert visning av aktivitets- og feillogger for dataadministratorer</span><span class="sxs-lookup"><span data-stu-id="91cf9-118">Consolidated view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="91cf9-119">Mulighet til å konfigurere egendefinerte varsler og terskler og abonnere på varslinger</span><span class="sxs-lookup"><span data-stu-id="91cf9-119">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="91cf9-120">Intuitivt brukergrensesnitt (UI) for filtrering og transformasjoner</span><span class="sxs-lookup"><span data-stu-id="91cf9-120">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="91cf9-121">Mulighet til å angi og vise enhetsavhengigheter og relasjoner</span><span class="sxs-lookup"><span data-stu-id="91cf9-121">Ability to set and view entity dependencies and relationships</span></span>
+ <span data-ttu-id="91cf9-122">Utvidelse for både standard og egendefinerte enheter og tilordninger</span><span class="sxs-lookup"><span data-stu-id="91cf9-122">Extensibility for both standard and custom entities and maps</span></span>
+ <span data-ttu-id="91cf9-123">Pålitelig livssyklus administrasjon for app</span><span class="sxs-lookup"><span data-stu-id="91cf9-123">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="91cf9-124">Integrert installasjonsopplevelse for nye kunder</span><span class="sxs-lookup"><span data-stu-id="91cf9-124">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="91cf9-125">Søknad</span><span class="sxs-lookup"><span data-stu-id="91cf9-125">Application</span></span>

<span data-ttu-id="91cf9-126">Ved dobbel skriving opprettes det en tilordning mellom konsepter i Finance and Operations-apper og konsepter i modelldrevne apper i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="91cf9-126">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="91cf9-127">Denne integreringen støtter følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="91cf9-127">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="91cf9-128">Integrert original for kunde</span><span class="sxs-lookup"><span data-stu-id="91cf9-128">Integrated customer master</span></span>
+ <span data-ttu-id="91cf9-129">Tilgang til kundefordelskort og belønningspoeng</span><span class="sxs-lookup"><span data-stu-id="91cf9-129">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="91cf9-130">Samlet produktstandardopplevelse</span><span class="sxs-lookup"><span data-stu-id="91cf9-130">Unified product mastering experience</span></span>
+ <span data-ttu-id="91cf9-131">Forståelse av organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="91cf9-131">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="91cf9-132">Integrert original for leverandør</span><span class="sxs-lookup"><span data-stu-id="91cf9-132">Integrated vendor master</span></span>
+ <span data-ttu-id="91cf9-133">Tilgang til referansedata for finan og avgift</span><span class="sxs-lookup"><span data-stu-id="91cf9-133">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="91cf9-134">Prismotoropplevelse etter behov</span><span class="sxs-lookup"><span data-stu-id="91cf9-134">On-demand price engine experience</span></span>
+ <span data-ttu-id="91cf9-135">Integrert opplevelse for kundeemne til kontant</span><span class="sxs-lookup"><span data-stu-id="91cf9-135">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="91cf9-136">Mulighet til å betjene både interne aktiva og kundeaktiva via feltagenter</span><span class="sxs-lookup"><span data-stu-id="91cf9-136">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="91cf9-137">Integrert opplevelse for innkjøp til betaling</span><span class="sxs-lookup"><span data-stu-id="91cf9-137">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="91cf9-138">Integrerte aktiviteter og notater for kundedata og dokumenter</span><span class="sxs-lookup"><span data-stu-id="91cf9-138">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="91cf9-139">Mulighet til å slå opp tilgjengelighet og detaljer for lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="91cf9-139">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="91cf9-140">Opplevelse for prosjekt til kontanter</span><span class="sxs-lookup"><span data-stu-id="91cf9-140">Project-to-cash experience</span></span>
+ <span data-ttu-id="91cf9-141">Mulighet til å håndtere flere adresser og roller via partskonseptet</span><span class="sxs-lookup"><span data-stu-id="91cf9-141">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="91cf9-142">Administrasjon av enkelt kilde for brukere</span><span class="sxs-lookup"><span data-stu-id="91cf9-142">Single source management for users</span></span>
+ <span data-ttu-id="91cf9-143">Integrerte kanaler for detaljsalg og markedsføring</span><span class="sxs-lookup"><span data-stu-id="91cf9-143">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="91cf9-144">Innsyn i kampanjer og rabatter</span><span class="sxs-lookup"><span data-stu-id="91cf9-144">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="91cf9-145">Funksjoner for å be om service</span><span class="sxs-lookup"><span data-stu-id="91cf9-145">Request-for-service functions</span></span>
+ <span data-ttu-id="91cf9-146">Strømlinjeformede serviceoperasjoner</span><span class="sxs-lookup"><span data-stu-id="91cf9-146">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="91cf9-147">Gode grunner til å bruke dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="91cf9-147">Top reasons to use dual-write</span></span>

<span data-ttu-id="91cf9-148">Dobbel skriving gir dataintegrering på tvers av Microsoft Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="91cf9-148">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="91cf9-149">Dette robuste rammeverket kobler sammen miljøer og gjør det mulig for forskjellige forretningsapper å fungere sammen.</span><span class="sxs-lookup"><span data-stu-id="91cf9-149">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="91cf9-150">Her er de viktigste grunnene til at du bør bruke dobbel skriving:</span><span class="sxs-lookup"><span data-stu-id="91cf9-150">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="91cf9-151">Dobbel skriving gir tett sammenkoblet toveis integrering nær sagt i sanntid mellom Finance and Operations-apper og modelldrevne apper i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="91cf9-151">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="91cf9-152">Denne integreringen gjør at Microsoft Dynamics 365 kan brukes til alle forretningsløsningene dine.</span><span class="sxs-lookup"><span data-stu-id="91cf9-152">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="91cf9-153">Kunder som bruker Dynamics 365 Finance og Dynamics 365 Supply Chain Management, men som bruker løsninger fra andre enn Microsoft for Customer Relationship Management (CRM), går over til å bruke Dynamics 365 for støtte for dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="91cf9-153">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="91cf9-154">Data fra kunder, produkter, operasjoner, prosjekter og tingenes Internett flyter automatisk til Common Data Service via dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="91cf9-154">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Common Data Service through dual-write.</span></span> <span data-ttu-id="91cf9-155">Denne tilkoblingen er svært nyttig for bedrifter som er interessert i Microsoft Power Platform-utvidelser.</span><span class="sxs-lookup"><span data-stu-id="91cf9-155">This connection is very useful for businesses that are interested in Microsoft Power Platform expansions.</span></span>
+ <span data-ttu-id="91cf9-156">Infrastrukturen for dobbel skriving følger koden for ingen kode / lav kode.</span><span class="sxs-lookup"><span data-stu-id="91cf9-156">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="91cf9-157">Det kreves minimalt teknisk arbeid for å utvide standardtilordninger fra tabell til tabell og inkludere tilpassede tilordninger.</span><span class="sxs-lookup"><span data-stu-id="91cf9-157">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="91cf9-158">Dobbel skriving støtter både tilkoblet og frakoblet modus.</span><span class="sxs-lookup"><span data-stu-id="91cf9-158">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="91cf9-159">Microsoft er det eneste firmaet som tilbyr støtte for tilkoblet og frakoblet modus.</span><span class="sxs-lookup"><span data-stu-id="91cf9-159">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-users-and-architects-of-crm-products"></a><span data-ttu-id="91cf9-160">Hva betyr dobbel skriving for brukere av og arkitekter for CRM-produkter?</span><span class="sxs-lookup"><span data-stu-id="91cf9-160">What does dual-write mean for users and architects of CRM products?</span></span>

<span data-ttu-id="91cf9-161">Dobbel skriving automatiserer dataflyten mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="91cf9-161">Dual-write automates the data flow between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="91cf9-162">I fremtidige versjoner vil begrepene i modelldrevne apper i Dynamics 365 (for eksempel kunde, kontakt, tilbud og ordre) for skaleres til kunder i mellomsjiktet og det øvre sjiktet.</span><span class="sxs-lookup"><span data-stu-id="91cf9-162">In future releases, concepts in model-driven apps in Dynamics 365 (for example, customer, contact, quotation, and order) will be scaled to mid-market and upper-mid-market customers.</span></span>

<span data-ttu-id="91cf9-163">I den første versjonen håndteres det meste av automatiseringen av løsninger for dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="91cf9-163">In the first release, most of the automation is handled by dual-write solutions.</span></span> <span data-ttu-id="91cf9-164">I fremtidige versjoner blir disse løsningene en del av Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="91cf9-164">In future releases, those solutions will become part of Common Data Service.</span></span> <span data-ttu-id="91cf9-165">Ved å forstå de kommende endringene i Common Data Service kan du spare deg selv for innsats på lang sikt.</span><span class="sxs-lookup"><span data-stu-id="91cf9-165">By understanding the upcoming changes to Common Data Service, you can save yourself effort in the long term.</span></span> <span data-ttu-id="91cf9-166">Her er noen av de viktige endringene:</span><span class="sxs-lookup"><span data-stu-id="91cf9-166">Here are some of the crucial changes:</span></span>

+ <span data-ttu-id="91cf9-167">Common Data Service vil ha nye konsepter, for eksempel firma og part.</span><span class="sxs-lookup"><span data-stu-id="91cf9-167">Common Data Service will have new concepts, such as company and party.</span></span> <span data-ttu-id="91cf9-168">Disse konseptene vil påvirke alle apper som er utviklet med Common Data Service, for eksempel Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service.</span><span class="sxs-lookup"><span data-stu-id="91cf9-168">These concepts will affect all apps that are built on Common Data Service, such as Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service.</span></span>
+ <span data-ttu-id="91cf9-169">Aktiviteter og notater er enhetlig og utvides for å støtte både C1-ere (brukere av systemet) og C2-ere (kunder av systemet).</span><span class="sxs-lookup"><span data-stu-id="91cf9-169">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>
+ <span data-ttu-id="91cf9-170">Her er noen av de kommende endringene i Common Data Service:</span><span class="sxs-lookup"><span data-stu-id="91cf9-170">Here are some of the upcoming changes in Common Data Service:</span></span>

    - <span data-ttu-id="91cf9-171">Datatypen for desimaler erstatter datatypen for penger.</span><span class="sxs-lookup"><span data-stu-id="91cf9-171">The decimal data type will replace the money data type.</span></span>
    - <span data-ttu-id="91cf9-172">Datoeffektivitet vil støtte tidligere, nåværende og fremtidige data på samme sted.</span><span class="sxs-lookup"><span data-stu-id="91cf9-172">Date effectivity will support past, present, and future data in the same place.</span></span>
    - <span data-ttu-id="91cf9-173">Det vil være mer støtte for valuta og valutakurser, og API-et (Application Programming Interface) **Valutakurs** vil bli revidert.</span><span class="sxs-lookup"><span data-stu-id="91cf9-173">There will be more support for currency and exchange rates, and the **Exchange Rate** application programming interface (API) will be revised.</span></span>
    - <span data-ttu-id="91cf9-174">Enhetskonverteringer vil støttes.</span><span class="sxs-lookup"><span data-stu-id="91cf9-174">Unit conversions will be supported.</span></span>

<span data-ttu-id="91cf9-175">Hvis du vil ha mer informasjon om kommende endringer, kan du se [Data i Common Data Service – fase 1 og 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span><span class="sxs-lookup"><span data-stu-id="91cf9-175">For more information about upcoming changes, see [Data in Common Data Service – phase 1 & 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/finance-operations-crossapp-capabilities/data-common-data-service-phase-1).</span></span>
