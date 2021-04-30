---
title: Vanlige spørsmål om aktivering
description: Dette emnet viser vanlige spørsmål om hvordan du kan arbeide med et Dynamics 365 Human Resources-implementeringsprosjekt.
author: rachel-profitt
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e1b4b336953ef6bd74da009b3bb44fbcf2eab5a8
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892329"
---
# <a name="go-live-faq"></a><span data-ttu-id="71179-103">Vanlige spørsmål om aktivering</span><span class="sxs-lookup"><span data-stu-id="71179-103">Go-live FAQ</span></span> 

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="71179-104">Dette emnet viser vanlige spørsmål om hvordan du kan arbeide med et Dynamics 365 Human Resources-implementeringsprosjekt.</span><span class="sxs-lookup"><span data-stu-id="71179-104">This topic lists frequently asked questions about how to go live with a Dynamics 365 Human Resources implementation project.</span></span> 

## <a name="when-can-i-configure-and-request-my-production-environment"></a><span data-ttu-id="71179-105">Når kan jeg konfigurere og be om produksjonsmiljøet?</span><span class="sxs-lookup"><span data-stu-id="71179-105">When can I configure and request my production environment?</span></span> 

<span data-ttu-id="71179-106">Vanligvis distribueres et produksjonsmiljø etter å ha oppfylt følgende kriterier:</span><span class="sxs-lookup"><span data-stu-id="71179-106">Typically, a production environment is deployed after meeting the following criteria:</span></span>

- <span data-ttu-id="71179-107">Alle tilpassinger er kodefullført.</span><span class="sxs-lookup"><span data-stu-id="71179-107">All customizations are code-complete.</span></span>
- <span data-ttu-id="71179-108">Testing av brukergodkjenning (UAT) er fullført.</span><span class="sxs-lookup"><span data-stu-id="71179-108">User acceptance testing (UAT) is complete.</span></span>
- <span data-ttu-id="71179-109">Kunden har godkjent løsningen.</span><span class="sxs-lookup"><span data-stu-id="71179-109">The customer has signed off on the solution.</span></span>
- <span data-ttu-id="71179-110">Det er ingen problemer med blokkering for aktivering.</span><span class="sxs-lookup"><span data-stu-id="71179-110">There are no blocking issues for go-live.</span></span> 

<span data-ttu-id="71179-111">Når kvalifiserte kunder er i dette stadiet, vil Microsoft FastTrack-teamet arbeide med prosjektgruppen for å utføre en aktiveringsvurdering.</span><span class="sxs-lookup"><span data-stu-id="71179-111">When qualified customers are at this stage, the Microsoft FastTrack team will work with the project team to do a go-live assessment.</span></span> 

## <a name="what-are-the-prerequisites-to-deploying-a-production-environment"></a><span data-ttu-id="71179-112">Hva er forutsetningene for å distribuere et produksjonsmiljø?</span><span class="sxs-lookup"><span data-stu-id="71179-112">What are the prerequisites to deploying a production environment?</span></span> 

<span data-ttu-id="71179-113">Hvis du vil ha en liste over forutsetningene, kan du se [Klargjøre for aktivering](hr-admin-go-live-prepare.md).</span><span class="sxs-lookup"><span data-stu-id="71179-113">For a list of the prerequisites, see [Prepare for go-live](hr-admin-go-live-prepare.md).</span></span> 

## <a name="what-is-a-go-live-assessment"></a><span data-ttu-id="71179-114">Hva er en aktiveringsvurdering?</span><span class="sxs-lookup"><span data-stu-id="71179-114">What is a go-live assessment?</span></span>  

<span data-ttu-id="71179-115">Aktiveringsvurderingen er en del av [Microsoft FastTrack-programmet](/dynamics365/fasttrack/).</span><span class="sxs-lookup"><span data-stu-id="71179-115">The go-live assessment is part of the [Microsoft FastTrack program](/dynamics365/fasttrack/).</span></span> <span data-ttu-id="71179-116">I løpet av denne gjennomgangen vurderer en løsningsarkitekt om implementeringsprosjektet er klart for en vellykket overgang og aktivering.</span><span class="sxs-lookup"><span data-stu-id="71179-116">During this review, a solution architect assesses whether an implementation project is ready for a successful cutover and go-live.</span></span> <span data-ttu-id="71179-117">Denne gjennomgangen er obligatorisk for hvert implementeringsprosjekt før du kan be om å aktivere et produksjonsmiljø.</span><span class="sxs-lookup"><span data-stu-id="71179-117">This review is mandatory for every implementation project before you can request to go live in a production environment.</span></span> 

## <a name="our-sandbox-environments-are-deployed-in-the-central-us-datacenter-we-want-our-production-environments-to-be-deployed-in-the-west-us-datacenter-can-i-select-west-us-as-the-datacenter-in-my-production-configuration"></a><span data-ttu-id="71179-118">Våre sandkassemiljøer er distribuert i datasenteret USA, sentralt.</span><span class="sxs-lookup"><span data-stu-id="71179-118">Our Sandbox environments are deployed in the Central US datacenter.</span></span> <span data-ttu-id="71179-119">Vi vil at våre produksjonsmiljøer skal distribueres i datasenteret USA, vest.</span><span class="sxs-lookup"><span data-stu-id="71179-119">We want our Production environments to be deployed in the West US datacenter.</span></span> <span data-ttu-id="71179-120">Kan jeg velge USA, vest som datasenter i produksjonskonfigurasjonen?</span><span class="sxs-lookup"><span data-stu-id="71179-120">Can I select West US as the datacenter in my Production configuration?</span></span> 

<span data-ttu-id="71179-121">LCS hindrer deg ikke i å velge et annet datasenter når du distribuerer et Human Resources-miljø, men vi anbefaler sterkt at du ikke velger et annet datasenter.</span><span class="sxs-lookup"><span data-stu-id="71179-121">LCS doesn't restrict you from selecting a different data center when you deploy a Human Resources environment, but we strongly recommend not selecting a different data center.</span></span>  

<span data-ttu-id="71179-122">Hvis du vil at produksjonsmiljøet skal være i datasenteret USA, vest, bør du først distribuere dine sandkassemiljøer til datasenteret USA, vest, teste dem og deretter godkjenne.</span><span class="sxs-lookup"><span data-stu-id="71179-122">If you want your Production environment to be in the West US datacenter, you should first redeploy your Sandbox environments to the West US datacenter, test them, and sign off.</span></span> 

<span data-ttu-id="71179-123">Hvis du vil ha informasjon om hvordan du velger riktig datasenter, se [Nettverkskrav](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements).</span><span class="sxs-lookup"><span data-stu-id="71179-123">For information about selecting the correct datacenter, see [Network requirements](../fin-ops-core/fin-ops/get-started/system-requirements.md#network-requirements).</span></span> 

## <a name="what-level-of-access-do-i-have-to-the-azure-resources-for-my-human-resources-environments"></a><span data-ttu-id="71179-124">Hvilket tilgangsnivå har jeg til Azure-ressursene for Human Resources-miljøene?</span><span class="sxs-lookup"><span data-stu-id="71179-124">What level of access do I have to the Azure resources for my Human Resources environments?</span></span>  

<span data-ttu-id="71179-125">Tilgang til Human Resources-miljøene er begrenset.</span><span class="sxs-lookup"><span data-stu-id="71179-125">Access to the Human Resources environments is limited.</span></span> <span data-ttu-id="71179-126">Du får ikke tilgang til den virtuelle maskinen (VM) eller Microsoft Internet Information Services (IIS).</span><span class="sxs-lookup"><span data-stu-id="71179-126">You can't access the virtual machine (VM) or Microsoft Internet Information Services (IIS).</span></span> <span data-ttu-id="71179-127">Du får heller ikke tilgang til databasen gjennom Microsoft SQL Server Management Studio.</span><span class="sxs-lookup"><span data-stu-id="71179-127">You also can't access the database through Microsoft SQL Server Management Studio.</span></span> 

<span data-ttu-id="71179-128">Selv om du ikke kan få tilgang til Azure-ressursene eller Dynamics 365 Human Resources-miljøet direkte, kan du bruke flere funksjoner for å få tilgang til dataene:</span><span class="sxs-lookup"><span data-stu-id="71179-128">Although you can't access your Azure resources or Dynamics 365 Human Resources environment directly, there are additional features you can use to access your data:</span></span>

- <span data-ttu-id="71179-129">Du kan distribuere en Azure SQL-database i din egen Azure-leier og bruke funksjonen Vise din egen database (BYOD) til å synkronisere data.</span><span class="sxs-lookup"><span data-stu-id="71179-129">You can deploy an Azure SQL database in your own Azure tenant and use the Bring Your Own Database (BYOD) feature to synchronize data.</span></span> <span data-ttu-id="71179-130">Hvis du vil ha mer informasjon, kan du se [Vise din egen database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span><span class="sxs-lookup"><span data-stu-id="71179-130">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span>

- <span data-ttu-id="71179-131">Du kan bruke Dataverse-integrering til å synkronisere utvalgte enheter i Dataverse-databasen.</span><span class="sxs-lookup"><span data-stu-id="71179-131">You can use Dataverse integration to synchronize select entities into the Dataverse database.</span></span> <span data-ttu-id="71179-132">Hvis du vil ha mer informasjon, kan du se [Dataverse-tabeller](hr-developer-entities.md).</span><span class="sxs-lookup"><span data-stu-id="71179-132">For more information, see [Dataverse tables](hr-developer-entities.md).</span></span> 

## <a name="how-often-is-my-production-database-backed-up"></a><span data-ttu-id="71179-133">Hvor ofte sikkerhetskopieres produksjonsdatabasen?</span><span class="sxs-lookup"><span data-stu-id="71179-133">How often is my production database backed up?</span></span> 

<span data-ttu-id="71179-134">Databaser beskyttes av automatisk sikkerhetskopiering med følgende frekvenser:</span><span class="sxs-lookup"><span data-stu-id="71179-134">Databases are protected by automatic backups at the following frequencies:</span></span>

| <span data-ttu-id="71179-135">Type sikkerhetskopiering</span><span class="sxs-lookup"><span data-stu-id="71179-135">Type of backup</span></span> | <span data-ttu-id="71179-136">Frekvens</span><span class="sxs-lookup"><span data-stu-id="71179-136">Frequency</span></span> |
| --- | --- |
| <span data-ttu-id="71179-137">Full sikkerhetskopi av database</span><span class="sxs-lookup"><span data-stu-id="71179-137">Full database backup</span></span> | <span data-ttu-id="71179-138">Ukentlig</span><span class="sxs-lookup"><span data-stu-id="71179-138">Weekly</span></span> |
| <span data-ttu-id="71179-139">Differensiell sikkerhetskopi av database</span><span class="sxs-lookup"><span data-stu-id="71179-139">Differential database backup</span></span> | <span data-ttu-id="71179-140">Hver 12-24. time</span><span class="sxs-lookup"><span data-stu-id="71179-140">Every 12-24 hours</span></span> |
| <span data-ttu-id="71179-141">Sikkerhetskopi av transaksjonslogg</span><span class="sxs-lookup"><span data-stu-id="71179-141">Transaction log backup</span></span> | <span data-ttu-id="71179-142">Hver 5 til 10 minutter</span><span class="sxs-lookup"><span data-stu-id="71179-142">Every 5 to 10 minutes</span></span> |

<span data-ttu-id="71179-143">Microsoft beholder tilstrekkelige sikkerhetskopier for å tillate tidspunktbasert gjenoppretting (PITR) i løpet av de siste 14 dagene.</span><span class="sxs-lookup"><span data-stu-id="71179-143">Microsoft retains sufficient backups to allow for Point in Time Restore (PITR) within the last 14 days.</span></span> 

<span data-ttu-id="71179-144">Hvis du vil ha mer informasjon, se [Lær om automatisk sikkerhetskopiering av SQL-databasen](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span><span class="sxs-lookup"><span data-stu-id="71179-144">For more information, see [Learn about automatic SQL Database backups](/azure/azure-sql/database/automated-backups-overview?tabs=single-database).</span></span> 

## <a name="can-i-request-a-copy-of-the-backup-of-my-production-database"></a><span data-ttu-id="71179-145">Kan jeg be om en kopi av sikkerhetskopien av produksjonsdatabasen?</span><span class="sxs-lookup"><span data-stu-id="71179-145">Can I request a copy of the backup of my production database?</span></span> 

<span data-ttu-id="71179-146">Nr.</span><span class="sxs-lookup"><span data-stu-id="71179-146">No.</span></span> <span data-ttu-id="71179-147">Du kan imidlertid sende en tjenesteforespørsel om databaseoppdatering for å kopiere produksjonsmiljøet til sandkassemiljøet.</span><span class="sxs-lookup"><span data-stu-id="71179-147">You can submit a database refresh service request to copy your Production environment to your Sandbox environment, however.</span></span> <span data-ttu-id="71179-148">Du kan distribuere en Azure SQL-database i din egen Azure-leier og bruke BYOD-funksjonen til å synkronisere data fra produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="71179-148">You can deploy an Azure SQL database in your own Azure tenant and use the BYOD feature to synchronize data from your Production environment.</span></span> <span data-ttu-id="71179-149">Hvis du vil ha mer informasjon, kan du se [Vise din egen database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span><span class="sxs-lookup"><span data-stu-id="71179-149">For more information, see [Bring your own database (BYOD)](../fin-ops-core/dev-itpro/analytics/export-entities-to-your-own-database.md).</span></span> 

## <a name="how-do-i-move-my-sandbox-environment-to-production-for-go-live"></a><span data-ttu-id="71179-150">Hvordan flytter jeg sandkassemiljøet til produksjon for aktivering?</span><span class="sxs-lookup"><span data-stu-id="71179-150">How do I move my Sandbox environment to Production for go-live?</span></span> 

<span data-ttu-id="71179-151">Fordi en kopieringsfunksjon ikke er tilgjengelig for å flytte ditt miljø fra et sandkasse- til et produksjonsmiljø, må du bruke datapakker til å flytte data til produksjonsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="71179-151">Because a copy feature isn't available to move your environment from a Sandbox to a Production environment, you must use data packages to move data into your Production environment.</span></span>  

<span data-ttu-id="71179-152">Det anbefales at du vedlikeholder en klar liste over enheter som er konfigurert i sandkassen gjennom hele prosjektet.</span><span class="sxs-lookup"><span data-stu-id="71179-152">We recommend maintaining a clear list of entities configured in your Sandbox throughout the project.</span></span> <span data-ttu-id="71179-153">Deretter tester du prosessen med overgang og migrering av datapakker som er nødvendig for aktivering.</span><span class="sxs-lookup"><span data-stu-id="71179-153">Then test the process of cutover and migration of any data packages needed for your go-live.</span></span> <span data-ttu-id="71179-154">Du må manuelt flytte datapakker til produksjonsmiljøet når du er klar for aktivering.</span><span class="sxs-lookup"><span data-stu-id="71179-154">You must manually move any data packages into the Production environment when you are ready to go live.</span></span> 

## <a name="what-should-i-do-if-my-production-environment-is-down"></a><span data-ttu-id="71179-155">Hva bør jeg gjøre hvis produksjonsmiljøet er nede?</span><span class="sxs-lookup"><span data-stu-id="71179-155">What should I do if my Production environment is down?</span></span> 

<span data-ttu-id="71179-156">Hvis du vil rapportere en produksjonsnedetid, følger du prosessen som er beskrevet i [Rapportere en produksjonsnedetid](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md).</span><span class="sxs-lookup"><span data-stu-id="71179-156">To report a Production outage, follow the process described in [Report a production outage](../fin-ops-core/dev-itpro/lifecycle-services/report-production-outage.md).</span></span> 

 ## <a name="see-also"></a><span data-ttu-id="71179-157">Se også</span><span class="sxs-lookup"><span data-stu-id="71179-157">See also</span></span>

 [<span data-ttu-id="71179-158">Klargjøre for aktivering</span><span class="sxs-lookup"><span data-stu-id="71179-158">Prepare for go-live</span></span>](hr-admin-go-live-prepare.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]