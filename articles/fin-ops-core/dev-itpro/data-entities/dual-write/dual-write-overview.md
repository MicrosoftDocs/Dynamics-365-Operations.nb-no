---
title: Oversikt over dobbel skriving
description: Dette emnet gir en oversikt over dobbel skriving, som er en integrert infrastruktur som gir interaksjon med minimal forsinkelse mellom kundeengasjementsapper og Finance and Operations-apper.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 3937850a9df716113591e49b25373beb48e3acdd
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/06/2021
ms.locfileid: "5130011"
---
# <a name="dual-write-overview"></a><span data-ttu-id="6a889-103">Oversikt over dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="6a889-103">Dual-write overview</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



## <a name="what-is-dual-write"></a><span data-ttu-id="6a889-104">Hva er dobbel skriving?</span><span class="sxs-lookup"><span data-stu-id="6a889-104">What is dual-write?</span></span>

<span data-ttu-id="6a889-105">Dobbel skriving er en integrert infrastruktur som gir nær sanntids interaksjon mellom Customer Engagement-apper og Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="6a889-105">Dual-write is an out-of-box infrastructure that provides near-real-time interaction between customer engagement apps and Finance and Operations apps.</span></span> <span data-ttu-id="6a889-106">Når data om kunder, produkter, personer og operasjoner flyter utenfor applikasjonens grenser, kan alle avdelingene i en organisasjon være på.</span><span class="sxs-lookup"><span data-stu-id="6a889-106">When data about customers, products, people, and operations flows beyond application boundaries, all departments in an organization are empowered.</span></span>

<span data-ttu-id="6a889-107">Dobbel skriving gir tett sammenkoblet, toveis integrering mellom Finance and Operations-apper og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6a889-107">Dual-write provides tightly coupled, bidirectional integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="6a889-108">Alle dataendringer i Finance and Operations-apper fører til skriving til Dataverse, og alle dataendringer i Dataverse fører til skriving til Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="6a889-108">Any data change in Finance and Operations apps causes writes to Dataverse, and any data change in Dataverse causes writes to Finance and Operations apps.</span></span> <span data-ttu-id="6a889-109">Denne automatiserte dataflyten gir en integrert brukeropplevelse på tvers av appene.</span><span class="sxs-lookup"><span data-stu-id="6a889-109">This automated data flow provides an integrated user experience across the apps.</span></span>

![Datarelasjon mellom apper](media/dual-write-overview.jpg)

<span data-ttu-id="6a889-111">Dobbel skriving har to aspkter: *infrastruktur* og *app*.</span><span class="sxs-lookup"><span data-stu-id="6a889-111">Dual-write has two aspects: an *infrastructure* aspect and an *application* aspect.</span></span>

### <a name="infrastructure"></a><span data-ttu-id="6a889-112">Infrastruktur</span><span class="sxs-lookup"><span data-stu-id="6a889-112">Infrastructure</span></span>

<span data-ttu-id="6a889-113">Infrastrukturen for dobbel skriving er utvidbar og pålitelig, og inneholder følgende nøkkelfunksjoner:</span><span class="sxs-lookup"><span data-stu-id="6a889-113">The dual-write infrastructure is extensible and reliable, and includes the following key features:</span></span>

+ <span data-ttu-id="6a889-114">Synkron og toveis dataflyt mellom programmer</span><span class="sxs-lookup"><span data-stu-id="6a889-114">Synchronous and bidirectional data flow between applications</span></span>
+ <span data-ttu-id="6a889-115">Synkronisering sammen med modus for avspilling, pause og oppsamling for å støtte systemet under tilkoblet og frakoblet/asynkron modus.</span><span class="sxs-lookup"><span data-stu-id="6a889-115">Synchronization, together with play, pause, and catchup modes to support the system during online and offline/asynchronous modes.</span></span>
+ <span data-ttu-id="6a889-116">Mulighet til å synkronisere innledende data mellom apper</span><span class="sxs-lookup"><span data-stu-id="6a889-116">Ability to sync initial data between the applications</span></span>
+ <span data-ttu-id="6a889-117">Kombinert visning av aktivitets- og feillogger for dataadministratorer</span><span class="sxs-lookup"><span data-stu-id="6a889-117">Combined view of activity and error logs for data admins</span></span>
+ <span data-ttu-id="6a889-118">Mulighet til å konfigurere egendefinerte varsler og terskler og abonnere på varslinger</span><span class="sxs-lookup"><span data-stu-id="6a889-118">Ability to configure custom alerts and thresholds, and to subscribe to notifications</span></span>
+ <span data-ttu-id="6a889-119">Intuitivt brukergrensesnitt (UI) for filtrering og transformasjoner</span><span class="sxs-lookup"><span data-stu-id="6a889-119">Intuitive user interface (UI) for filtering and transformations</span></span>
+ <span data-ttu-id="6a889-120">Mulighet til å angi og vise tabellavhengigheter og relasjoner</span><span class="sxs-lookup"><span data-stu-id="6a889-120">Ability to set and view table dependencies and relationships</span></span>
+ <span data-ttu-id="6a889-121">Utvidelse for både standard og egendefinerte tabeller og tilordninger</span><span class="sxs-lookup"><span data-stu-id="6a889-121">Extensibility for both standard and custom tables and maps</span></span>
+ <span data-ttu-id="6a889-122">Pålitelig livssyklus administrasjon for app</span><span class="sxs-lookup"><span data-stu-id="6a889-122">Reliable application lifecycle management</span></span>
+ <span data-ttu-id="6a889-123">Integrert installasjonsopplevelse for nye kunder</span><span class="sxs-lookup"><span data-stu-id="6a889-123">Out-of-box setup experience for new customers</span></span>

### <a name="application"></a><span data-ttu-id="6a889-124">Søknad</span><span class="sxs-lookup"><span data-stu-id="6a889-124">Application</span></span>

<span data-ttu-id="6a889-125">Ved dobbel skriving opprettes det en tilordning mellom konsepter i Finance and Operations-apper og konsepter i Customer Engagement-apper.</span><span class="sxs-lookup"><span data-stu-id="6a889-125">Dual-write creates a mapping between concepts in Finance and Operations apps and concepts in customer engagement apps.</span></span> <span data-ttu-id="6a889-126">Denne integreringen støtter følgende scenarier:</span><span class="sxs-lookup"><span data-stu-id="6a889-126">This integration supports the following scenarios:</span></span>

+ <span data-ttu-id="6a889-127">Integrert original for kunde</span><span class="sxs-lookup"><span data-stu-id="6a889-127">Integrated customer master</span></span>
+ <span data-ttu-id="6a889-128">Tilgang til kundefordelskort og belønningspoeng</span><span class="sxs-lookup"><span data-stu-id="6a889-128">Access to customer loyalty cards and reward points</span></span>
+ <span data-ttu-id="6a889-129">Samlet produktstandardopplevelse</span><span class="sxs-lookup"><span data-stu-id="6a889-129">Unified product mastering experience</span></span>
+ <span data-ttu-id="6a889-130">Forståelse av organisasjonshierarkiet</span><span class="sxs-lookup"><span data-stu-id="6a889-130">Awareness of organization hierarchy</span></span>
+ <span data-ttu-id="6a889-131">Integrert original for leverandør</span><span class="sxs-lookup"><span data-stu-id="6a889-131">Integrated vendor master</span></span>
+ <span data-ttu-id="6a889-132">Tilgang til referansedata for finan og avgift</span><span class="sxs-lookup"><span data-stu-id="6a889-132">Access to finance and tax reference data</span></span>
+ <span data-ttu-id="6a889-133">Prismotoropplevelse etter behov</span><span class="sxs-lookup"><span data-stu-id="6a889-133">On-demand price engine experience</span></span>
+ <span data-ttu-id="6a889-134">Integrert opplevelse for kundeemne til kontant</span><span class="sxs-lookup"><span data-stu-id="6a889-134">Integrated prospect-to-cash experience</span></span>
+ <span data-ttu-id="6a889-135">Mulighet til å betjene både interne aktiva og kundeaktiva via feltagenter</span><span class="sxs-lookup"><span data-stu-id="6a889-135">Ability to serve both in-house assets and customer assets through field agents</span></span>
+ <span data-ttu-id="6a889-136">Integrert opplevelse for innkjøp til betaling</span><span class="sxs-lookup"><span data-stu-id="6a889-136">Integrated procure-to-pay experience</span></span>
+ <span data-ttu-id="6a889-137">Integrerte aktiviteter og notater for kundedata og dokumenter</span><span class="sxs-lookup"><span data-stu-id="6a889-137">Integrated activities and notes for customer data and documents</span></span>
+ <span data-ttu-id="6a889-138">Mulighet til å slå opp tilgjengelighet og detaljer for lagerbeholdning</span><span class="sxs-lookup"><span data-stu-id="6a889-138">Ability to look up on-hand inventory availability and details</span></span>
+ <span data-ttu-id="6a889-139">Opplevelse for prosjekt til kontanter</span><span class="sxs-lookup"><span data-stu-id="6a889-139">Project-to-cash experience</span></span>
+ <span data-ttu-id="6a889-140">Mulighet til å håndtere flere adresser og roller via partskonseptet</span><span class="sxs-lookup"><span data-stu-id="6a889-140">Ability to handle multiple addresses and roles through the party concept</span></span>
+ <span data-ttu-id="6a889-141">Administrasjon av enkelt kilde for brukere</span><span class="sxs-lookup"><span data-stu-id="6a889-141">Single source management for users</span></span>
+ <span data-ttu-id="6a889-142">Integrerte kanaler for detaljsalg og markedsføring</span><span class="sxs-lookup"><span data-stu-id="6a889-142">Integrated channels for retailing and marketing</span></span>
+ <span data-ttu-id="6a889-143">Innsyn i kampanjer og rabatter</span><span class="sxs-lookup"><span data-stu-id="6a889-143">Visibility into promotions and discounts</span></span>
+ <span data-ttu-id="6a889-144">Funksjoner for å be om service</span><span class="sxs-lookup"><span data-stu-id="6a889-144">Request-for-service functions</span></span>
+ <span data-ttu-id="6a889-145">Strømlinjeformede serviceoperasjoner</span><span class="sxs-lookup"><span data-stu-id="6a889-145">Streamlined service operations</span></span>

## <a name="top-reasons-to-use-dual-write"></a><span data-ttu-id="6a889-146">Gode grunner til å bruke dobbel skriving</span><span class="sxs-lookup"><span data-stu-id="6a889-146">Top reasons to use dual-write</span></span>

<span data-ttu-id="6a889-147">Dobbel skriving gir dataintegrering på tvers av Microsoft Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="6a889-147">Dual-write provides data integration across Microsoft Dynamics 365 applications.</span></span> <span data-ttu-id="6a889-148">Dette robuste rammeverket kobler sammen miljøer og gjør det mulig for forskjellige forretningsapper å fungere sammen.</span><span class="sxs-lookup"><span data-stu-id="6a889-148">This robust framework links environments and enables different business applications to work together.</span></span> <span data-ttu-id="6a889-149">Her er de viktigste grunnene til at du bør bruke dobbel skriving:</span><span class="sxs-lookup"><span data-stu-id="6a889-149">Here are the top reasons why you should use dual-write:</span></span>

+ <span data-ttu-id="6a889-150">Dobbel skriving gir tett sammenkoblet toveis integrering nær sagt i sanntid mellom Finance and Operations-apper og modelldrevne apper i Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="6a889-150">Dual-write provides tightly coupled, near-real-time, and bidirectional integration between Finance and Operations apps and model-driven apps in Dynamics 365.</span></span> <span data-ttu-id="6a889-151">Denne integreringen gjør at Microsoft Dynamics 365 kan brukes til alle forretningsløsningene dine.</span><span class="sxs-lookup"><span data-stu-id="6a889-151">This integration makes Microsoft Dynamics 365 the one-stop shop for all your business solutions.</span></span> <span data-ttu-id="6a889-152">Kunder som bruker Dynamics 365 Finance og Dynamics 365 Supply Chain Management, men som bruker løsninger fra andre enn Microsoft for Customer Relationship Management (CRM), går over til å bruke Dynamics 365 for støtte for dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="6a889-152">Customers who use Dynamics 365 Finance and Dynamics 365 Supply Chain Management, but who use non-Microsoft solutions for customer relationship management (CRM), are moving toward Dynamics 365 for its dual-write support.</span></span>
+ <span data-ttu-id="6a889-153">Data fra kunder, produkter, operasjoner, prosjekter og tingenes Internett flyter automatisk til Dataverse via dobbel skriving.</span><span class="sxs-lookup"><span data-stu-id="6a889-153">Data from customers, products, operations, projects, and the Internet of Things (IoT) automatically flows to Dataverse through dual-write.</span></span> <span data-ttu-id="6a889-154">Denne tilkoblingen er nyttig for bedrifter som er interessert i Power Platform-utvidelser.</span><span class="sxs-lookup"><span data-stu-id="6a889-154">This connection is useful for businesses that are interested in Power Platform expansions.</span></span>
+ <span data-ttu-id="6a889-155">Infrastrukturen for dobbel skriving følger koden for ingen kode / lav kode.</span><span class="sxs-lookup"><span data-stu-id="6a889-155">The dual-write infrastructure follows the no-code/low-code principle.</span></span> <span data-ttu-id="6a889-156">Det kreves minimalt teknisk arbeid for å utvide standardtilordninger fra tabell til tabell og inkludere tilpassede tilordninger.</span><span class="sxs-lookup"><span data-stu-id="6a889-156">Minimal engineering effort is required to extend the standard table-to-table maps and to include custom maps.</span></span>
+ <span data-ttu-id="6a889-157">Dobbel skriving støtter både tilkoblet og frakoblet modus.</span><span class="sxs-lookup"><span data-stu-id="6a889-157">Dual-write supports both online mode and offline mode.</span></span> <span data-ttu-id="6a889-158">Microsoft er det eneste firmaet som tilbyr støtte for tilkoblet og frakoblet modus.</span><span class="sxs-lookup"><span data-stu-id="6a889-158">Microsoft is the only company that offers support for online and offline modes.</span></span>

## <a name="what-does-dual-write-mean-for-developers-and-architects-of-customer-engagement-apps"></a><a id="developer-architect"></a><span data-ttu-id="6a889-159">Hva innebærer toveis skriving av utviklere og arkitekter for Customer Engagement-apper?</span><span class="sxs-lookup"><span data-stu-id="6a889-159">What does dual-write mean for developers and architects of customer engagement apps?</span></span>

<span data-ttu-id="6a889-160">Dobbel skriving automatiserer dataflyten mellom Finance and Operations-apper og Customer Engagement-apper.</span><span class="sxs-lookup"><span data-stu-id="6a889-160">Dual-write automates the data flow between Finance and Operations apps and customer engagement apps.</span></span> <span data-ttu-id="6a889-161">Dobbel skriving består av to AppSource-løsninger som er installert på Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6a889-161">Dual-write consists of two AppSource solutions that are installed on Dataverse.</span></span> <span data-ttu-id="6a889-162">Løsningene utvider tabellskjemaet, programtilleggene og arbeidsflytene på Dataverse slik at de kan skaleres til ERP-størrelse.</span><span class="sxs-lookup"><span data-stu-id="6a889-162">The solutions expand the table schema, plugins, and workflows on Dataverse so that they can scale to ERP size.</span></span> <span data-ttu-id="6a889-163">For å få en vellykket implementering, må utviklere og utarbeidere av Customer Engagement-apper forstå disse endringene og samarbeide med sine motparter om Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="6a889-163">For a successful implementation, developers and architects of customer engagement apps must understand these changes and collaborate with their counterparts on Finance and Operations apps.</span></span>

<span data-ttu-id="6a889-164">For å opprette paritet med Finance and Operations-apper, gjør dobbelt skriving noen viktige endringer i Dataverse-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="6a889-164">To create parity with Finance and Operations applications, dual-write makes some crucial changes in the Dataverse schema.</span></span> <span data-ttu-id="6a889-165">Hvis du forstår planen, kan du unngå noe utformings- og utviklingsarbeid er i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="6a889-165">If you understand the plan, you can avoid some design and development rework in the future.</span></span>

+ <span data-ttu-id="6a889-166">Når du har installert pakken for dobbel skriving AppSource, vil Dataverse ha de nye begrepene, for eksempel firma og part.</span><span class="sxs-lookup"><span data-stu-id="6a889-166">When the dual-write AppSource package is installed, Dataverse will have new concepts such as company and party.</span></span> <span data-ttu-id="6a889-167">Disse konseptene hjelper apper som er bygget på Dataverse, inkludert Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service og Dynamics 365 Field Service, til å samhandle sømløst med Finance and Operations-apper.</span><span class="sxs-lookup"><span data-stu-id="6a889-167">These concepts help applications built on Dataverse, including Dynamics 365 Sales, Dynamics 365 Marketing, Dynamics 365 Customer Service, and Dynamics 365 Field Service, to interact seamlessly with Finance and Operations apps.</span></span>

+ <span data-ttu-id="6a889-168">Aktiviteter og notater er enhetlig og utvides for å støtte både C1-ere (brukere av systemet) og C2-ere (kunder av systemet).</span><span class="sxs-lookup"><span data-stu-id="6a889-168">Activities and notes are unified and expanded to support both C1s (users of the system) and C2s (customers of the system).</span></span>

+ <span data-ttu-id="6a889-169">Hvis du vil hindre tap av data under overføring av valuta mellom Finance and Operations-apper og Dataverse, kan du utvide antallet desimaler i valutadatatypen for Customer Engagement-apper.</span><span class="sxs-lookup"><span data-stu-id="6a889-169">To prevent data loss during currency transmission between Finance and Operations apps and the Dataverse, you'll be able to extend the number of decimal places in the currency data type of customers engagement apps.</span></span> <span data-ttu-id="6a889-170">Funksjonen oversetter eksisterende rader automatisk til den nye utvidede tilstanden på metadatalaget.</span><span class="sxs-lookup"><span data-stu-id="6a889-170">The feature autotranslates existing rows to the new extended state at the metadata layer.</span></span> <span data-ttu-id="6a889-171">I løpet av denne prosessen blir valutaverdien oversatt til desimaldata i stedet for pengedata, og valutaverdien støtter 10 desimalplasser.</span><span class="sxs-lookup"><span data-stu-id="6a889-171">During this process, the currency value is translated to decimal data rather than money data, and the currency value supports 10 decimal places.</span></span> <span data-ttu-id="6a889-172">Denne funksjonen er valgfri, og organisasjoner som ikke trenger mer enn fire desimaler med presisjon, trenger ikke å velge den.</span><span class="sxs-lookup"><span data-stu-id="6a889-172">This feature is opt-in, and organizations that don't need more than 4 decimal places of precision do not need to opt in.</span></span> <span data-ttu-id="6a889-173">Hvis du vil ha mer informasjon, kan du se [Overføring av valutadatatype for dobbel skriving](currrency-decimal-places.md).</span><span class="sxs-lookup"><span data-stu-id="6a889-173">For more information, see [Currency data-type migration for dual-write](currrency-decimal-places.md).</span></span>

+ <span data-ttu-id="6a889-174">[Datoeffektivitet](../../dev-tools/date-effectivity.md) blir lagt til i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="6a889-174">[Date effectivity](../../dev-tools/date-effectivity.md) will be added to Dataverse.</span></span> <span data-ttu-id="6a889-175">Den vil støtte tidligere, nåværende og fremtidige data i samme tabell.</span><span class="sxs-lookup"><span data-stu-id="6a889-175">It will support past, present, and future data on the same table.</span></span>

+ <span data-ttu-id="6a889-176">[Enhetskonverteringer](../../../../supply-chain/pim/tasks/manage-unit-measure.md) for produkt støttes for produkter, tilbud, ordrer og fakturaer.</span><span class="sxs-lookup"><span data-stu-id="6a889-176">Product [unit conversions](../../../../supply-chain/pim/tasks/manage-unit-measure.md) are supported for products, quotes, orders, and invoices.</span></span>

<span data-ttu-id="6a889-177">Hvis du vil ha mer informasjon om kommende endringer, kan du se [Nyheter eller endringer i dobbel skriving](whats-new-dual-write.md).</span><span class="sxs-lookup"><span data-stu-id="6a889-177">For more information about upcoming changes, see [What's new or changed in dual-write](whats-new-dual-write.md).</span></span>

