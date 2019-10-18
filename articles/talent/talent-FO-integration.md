---
title: Vanlige spørsmål om integrering fra Dynamics 365 Talent til Dynamics 365 Finance
description: Dette emnet beskriver hvilke data som synkroniseres i en integrasjon med Talent og Finance.
author: andreabichsel
manager: AnnBe
ms.date: 09/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2018-12-31
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 5bb855e6dd7ff236b7bda9e59e12ed8cc8ab9bc9
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251020"
---
# <a name="dynamics-365-talent-to-dynamics-365-finance-integration-faq"></a><span data-ttu-id="580fc-103">Vanlige spørsmål om integrering fra Dynamics 365 Talent til Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="580fc-103">Dynamics 365 Talent to Dynamics 365 Finance integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="580fc-104">Dette emnet gir svar på vanlige spørsmål som er tilknyttet hvilke data som synkroniseres når Dynamics 365 Talent er integrert med Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="580fc-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Talent is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="580fc-105">Er alle data synkronisert eller bare noen dataenheter?</span><span class="sxs-lookup"><span data-stu-id="580fc-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="580fc-106">For Core HR synkroniseres et delsett av dataene.</span><span class="sxs-lookup"><span data-stu-id="580fc-106">For Core HR, a subset of the data is synchronized.</span></span> <span data-ttu-id="580fc-107">For en liste over alle enheter, kan du se [Integrasjon fra Dynamics 365 Talent til Dynamics 365 Finance](talent-financeandoperations-integration.md).</span><span class="sxs-lookup"><span data-stu-id="580fc-107">For a list of all the entities, see [Integration from Dynamics 365 Talent to Dynamics 365 Finance](talent-financeandoperations-integration.md).</span></span>

<span data-ttu-id="580fc-108">For Attract og Onboard hører alle data til i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="580fc-108">For Attract and Onboard, all data is native to Common Data Service.</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="580fc-109">Kan jeg opprette en ny tilordning uten å bruke malene?</span><span class="sxs-lookup"><span data-stu-id="580fc-109">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="580fc-110">Malene er startpunktet.</span><span class="sxs-lookup"><span data-stu-id="580fc-110">Templates are the starting point.</span></span> <span data-ttu-id="580fc-111">Du kan opprette din egen mal, men en mal er alltid nødvendig når du oppretter et prosjekt for integrasjon.</span><span class="sxs-lookup"><span data-stu-id="580fc-111">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="580fc-112">Hvis du vil ha mer informasjon om dataintegrator (DI), maler og prosjekter, kan du se [Integrere data til Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="580fc-112">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-talent-and-finance"></a><span data-ttu-id="580fc-113">Kan jeg tilordne finansdimensjoner for å overføre mellom Talent og Finance?</span><span class="sxs-lookup"><span data-stu-id="580fc-113">Can I map financial dimensions to transfer between Talent and Finance?</span></span>

<span data-ttu-id="580fc-114">Finansdimensjoner er ikke i Common Data Service og er dermed ikke en del av standardmalen.</span><span class="sxs-lookup"><span data-stu-id="580fc-114">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="580fc-115">Denne enheten er planlagt, men ingen tidslinje for frigivelse er for øyeblikket tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="580fc-115">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="580fc-116">For data som ligger i Finance, men ikke finnes i Talent, koble sammen de to systemene ved å bruke **Konfigurer koblinger** i Talent.</span><span class="sxs-lookup"><span data-stu-id="580fc-116">For data that resides in Finance but does not exist in Talent, link the two systems together by using **Configure Links** in Talent.</span></span> <span data-ttu-id="580fc-117">Hvis du vil ha mer informasjon om hvordan du konfigurerer koblinger mellom Talent og Finance, kan du se [Hva er nytt eller endret i Dynamics 365 Talent: Core HR (31. oktober 2018)](whats-new-talent-october-31.md).</span><span class="sxs-lookup"><span data-stu-id="580fc-117">For more information about how to configure links between Talent and Finance, see [What's new or changed in Dynamics 365 Talent: Core HR (October 31, 2018)](whats-new-talent-october-31.md).</span></span>

![Tilordne finansdimensjoner](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="580fc-119">Noen ganger når jeg importerer ansatte, blir de inaktive arbeidere i Finance.</span><span class="sxs-lookup"><span data-stu-id="580fc-119">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="580fc-120">Hvorfor?</span><span class="sxs-lookup"><span data-stu-id="580fc-120">Why?</span></span>

<span data-ttu-id="580fc-121">Du kan få denne feilen hvis ansatte ikke har en aktiv ansettelsesdetaljpost i Talent.</span><span class="sxs-lookup"><span data-stu-id="580fc-121">You may get this error if employees don’t have an active employment detail record in Talent.</span></span> <span data-ttu-id="580fc-122">Hvis du vil løse dette problemet, kan du gå til **Personaladministrasjon \> Ansatte \> Ansettelseshistorikk \> Datobehandling**, og kontroller at det finnes en aktiv ansettelsesdetaljpost.</span><span class="sxs-lookup"><span data-stu-id="580fc-122">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="580fc-123">Hvis jeg velger å tilordne bare et delsett av feltene, vil endringer i ikke-tilordnede felt utløse en synkronisering?</span><span class="sxs-lookup"><span data-stu-id="580fc-123">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="580fc-124">Datasynkronisering følger tidsplanen for kjøring.</span><span class="sxs-lookup"><span data-stu-id="580fc-124">Data sync follows the execution schedule.</span></span> <span data-ttu-id="580fc-125">Integreringen henter en post hvis et felt i posten endres, uansett om feltet er en del av integreringstilordning.</span><span class="sxs-lookup"><span data-stu-id="580fc-125">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="580fc-126">Hvordan kan jeg sende bare aktive arbeiderendringer og ikke de avsluttede postene?</span><span class="sxs-lookup"><span data-stu-id="580fc-126">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="580fc-127">Ved hjelp av "Avansert spørring" kan du filtrere og endre kildedataene før de sendes til målet.</span><span class="sxs-lookup"><span data-stu-id="580fc-127">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Avansert spørring for aktive arbeidere](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="580fc-129">Kan jeg angi hvilke felt som skal sendes til Finance for en bestemt enhet?</span><span class="sxs-lookup"><span data-stu-id="580fc-129">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="580fc-130">Feltene kan legges til eller fjernes fra integrasjonsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="580fc-130">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="580fc-131">Ikke alle datafelt som finnes på Common Data Service-enheten, fylles ut fra Core HR.</span><span class="sxs-lookup"><span data-stu-id="580fc-131">Not all data fields that exist on the Common Data Service entity will be populated from Core HR.</span></span>
<span data-ttu-id="580fc-132">Tilleggsdata fylles via PowerApps.</span><span class="sxs-lookup"><span data-stu-id="580fc-132">Additional data can be populated via PowerApps.</span></span>

![Legge til eller fjerne felt fra en integrasjonsoppgave](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-talent-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="580fc-134">Jeg har satt opp integrasjon som en satsvis jobb, men Talent mistet forbindelsen til målsystemet.</span><span class="sxs-lookup"><span data-stu-id="580fc-134">I set up integration as a batch job, but Talent lost connection to the destination system.</span></span> <span data-ttu-id="580fc-135">Hvordan kan jeg sende det samme settet med endringer til målsystemet?</span><span class="sxs-lookup"><span data-stu-id="580fc-135">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="580fc-136">Det kreves ingen spesielle oppsett for unntaksbehandling.</span><span class="sxs-lookup"><span data-stu-id="580fc-136">No special setup is required for exception handling.</span></span> <span data-ttu-id="580fc-137">Dataintegratoren finner og rapporterer feil som oppstår ved kilden og målet, og tillater nye manuelle forsøk.</span><span class="sxs-lookup"><span data-stu-id="580fc-137">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="580fc-138">Den tillater imidlertid ikke manuell datakorrigering.</span><span class="sxs-lookup"><span data-stu-id="580fc-138">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="580fc-139">Hvis dataoppdateringer kreves, skal dette skje enten ved kilden eller målet.</span><span class="sxs-lookup"><span data-stu-id="580fc-139">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="580fc-140">Kan jeg konfigurere toveis integrasjon?</span><span class="sxs-lookup"><span data-stu-id="580fc-140">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="580fc-141">Nei, integrasjon er énveis (fra Talent til Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="580fc-141">No, integration is currently one-way (Talent to Finance and Operations).</span></span> <span data-ttu-id="580fc-142">Det finnes imidlertid en standardmal som er tilgjengelig for å sende data fra Talent til Finance.</span><span class="sxs-lookup"><span data-stu-id="580fc-142">However, there is a default template available to send data from Talent to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="580fc-143">Kan jeg tillate sletting av oppføringer som en del av min integrasjon?</span><span class="sxs-lookup"><span data-stu-id="580fc-143">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="580fc-144">Nei, Dataintegrator registrerer ikke slettede poster for dataoverføring.</span><span class="sxs-lookup"><span data-stu-id="580fc-144">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="580fc-145">Bare oppretting og oppdatering av data (UPSERT) er for øyeblikket inkludert.</span><span class="sxs-lookup"><span data-stu-id="580fc-145">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="580fc-146">Kan jeg utføre kjøringen med feil på nytt?</span><span class="sxs-lookup"><span data-stu-id="580fc-146">Can I rerun the errored execution?</span></span> <span data-ttu-id="580fc-147">Sendes i så fall en fullstendig fil eller bare endringene?</span><span class="sxs-lookup"><span data-stu-id="580fc-147">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="580fc-148">Den første kjøringen av Dataintegrator er alltid en full kjøring.</span><span class="sxs-lookup"><span data-stu-id="580fc-148">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="580fc-149">Senere kjøringer er basert på endringssporing.</span><span class="sxs-lookup"><span data-stu-id="580fc-149">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="580fc-150">Når en feilkjøring utføres, trekker den ut postene i omfanget for kjøringen og sender ut de siste endringene fra Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="580fc-150">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="580fc-151">Når jeg lagrer prosjektet, får jeg feilen: "Prosjektet har tilordningsfeil."</span><span class="sxs-lookup"><span data-stu-id="580fc-151">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="580fc-152">Hva gjør jeg?</span><span class="sxs-lookup"><span data-stu-id="580fc-152">What do I do?</span></span>

<span data-ttu-id="580fc-153">Kontroller oppsettet for integrasjonsnøklene, foreta nødvendige endringer i oppsettet, og oppdater enhetene i prosjektet.</span><span class="sxs-lookup"><span data-stu-id="580fc-153">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="580fc-154">Når standardmalen brukes, blir nøklene for integrering automatisk importert.</span><span class="sxs-lookup"><span data-stu-id="580fc-154">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="580fc-155">Dette problemet kan oppstå når nye aktiviteter legges til i den eksisterende malen.</span><span class="sxs-lookup"><span data-stu-id="580fc-155">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="580fc-156">Hvis jeg har N antall juridiske enheter der arbeidere har ansettelser, trenger jeg å opprette en tilordning for hver av dem?</span><span class="sxs-lookup"><span data-stu-id="580fc-156">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="580fc-157">Ja, for hver juridiske enhet i Finance må du ha et eget integrasjonsprosjekt i dataintegreringen.</span><span class="sxs-lookup"><span data-stu-id="580fc-157">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="580fc-158">Jeg vil overføre data som ikke er en del av standardmalen fra Microsoft.</span><span class="sxs-lookup"><span data-stu-id="580fc-158">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="580fc-159">Kan jeg gjøre dette?</span><span class="sxs-lookup"><span data-stu-id="580fc-159">Can I do this?</span></span>

<span data-ttu-id="580fc-160">Ja, feltene kan legges til eller fjernes fra den eksisterende malen.</span><span class="sxs-lookup"><span data-stu-id="580fc-160">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="580fc-161">Malen kan endres for å ta med flere data fra andre Common Data Service-enheter.</span><span class="sxs-lookup"><span data-stu-id="580fc-161">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="580fc-162">Enheten må være i Common Data Service for at den skal inkluderes i malen.</span><span class="sxs-lookup"><span data-stu-id="580fc-162">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-talent-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="580fc-163">Jeg har nettopp opprettet nye Finance- og Talent-miljøer, og jeg får feilen "Dataverdien bryter integritetsbegrensninger."</span><span class="sxs-lookup"><span data-stu-id="580fc-163">I just created new Finance and Talent environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="580fc-164">Hvorfor?</span><span class="sxs-lookup"><span data-stu-id="580fc-164">Why?</span></span>

<span data-ttu-id="580fc-165">Årsaker til denne feilen kan omfatte:</span><span class="sxs-lookup"><span data-stu-id="580fc-165">Reasons for this error can include:</span></span>

- <span data-ttu-id="580fc-166">Dataoverføringen resulterte i duplisert postuttrekk ved kilden (Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="580fc-166">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="580fc-167">Dataoverføringen har nullverdier for feltene som kreves i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="580fc-167">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="580fc-168">Kontroller at dataene er i Common Data Service og oppfyller kravene fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="580fc-168">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="580fc-169">Hvis det er kjøringsfeil og ansatt-ID-en ikke synkroniseres, hvordan kan jeg finne den historiske jobben som har feil ansattpost?</span><span class="sxs-lookup"><span data-stu-id="580fc-169">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="580fc-170">Dataintegratoren oppretter flere prosjekter i Finance.</span><span class="sxs-lookup"><span data-stu-id="580fc-170">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="580fc-171">Relasjonen mellom Dataintegrator-oppgaven og Finance-prosjektet er én til én.</span><span class="sxs-lookup"><span data-stu-id="580fc-171">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="580fc-172">Spor tiden fra Dataintegrator-kjøringshistorikken, og se etter indeksen -1 i Finance.</span><span class="sxs-lookup"><span data-stu-id="580fc-172">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="580fc-173">Hvis oppgavenummeret er 9 i Dataintegrator, er indeksen i Finance 8.</span><span class="sxs-lookup"><span data-stu-id="580fc-173">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="580fc-174">Lagre oppgaveindeksen fra Dataintegrator (i dette eksemplet er det "9").</span><span class="sxs-lookup"><span data-stu-id="580fc-174">Capture the task index from Data Integrator (in this example it is "9").</span></span>

![Lagre oppgaveindeksen fra Dataintegrator](media/CaptureTaskIndex.png)

2. <span data-ttu-id="580fc-176">Spor kjøretiden for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="580fc-176">Track the execution time of the project.</span></span>

![Spore kjøretiden for prosjektet](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="580fc-178">Identifiser indeks -1 i Finance.</span><span class="sxs-lookup"><span data-stu-id="580fc-178">In Finance, identify index - 1.</span></span> <span data-ttu-id="580fc-179">I dette eksemplet samsvarer prosjektet med suffikset "8" og utførelsestiden for indeksen "0"-prosjektet med kjøretiden i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="580fc-179">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

![Identifisere indeks](media/IdentifyIndex.png)

## <a name="after-integrating-talent-and-finance-i-dont-see-my-talent-data-in-finance-what-do-i-do"></a><span data-ttu-id="580fc-181">Etter integrering av Talent og Finance vises ikke Talent-dataene mine i Finance.</span><span class="sxs-lookup"><span data-stu-id="580fc-181">After integrating Talent and Finance, I don’t see my Talent data in Finance.</span></span> <span data-ttu-id="580fc-182">Hva gjør jeg?</span><span class="sxs-lookup"><span data-stu-id="580fc-182">What do I do?</span></span>

<span data-ttu-id="580fc-183">Integreringen til Finance er en totrinns prosess.</span><span class="sxs-lookup"><span data-stu-id="580fc-183">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="580fc-184">Først bekrefter du at Talent-dataene er oppdaterte og tilgjengelige i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="580fc-184">First, verify that the Talent data is updated and available in Common Data Service.</span></span> <span data-ttu-id="580fc-185">Dette er en nær sanntidssynkronisering og kan kontrolleres i PowerApps ved å se på dataene i dataenhetene.</span><span class="sxs-lookup"><span data-stu-id="580fc-185">This is a near real-time sync and can be verified in PowerApps by looking at the data within the data entities.</span></span>

![Data i Common Data Service](media/DataInCDS.png)

<span data-ttu-id="580fc-187">Hvis dataene ikke vises som forventet i Common Data Service, må du kontrollere at enheten støttes i integreringen.</span><span class="sxs-lookup"><span data-stu-id="580fc-187">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="580fc-188">Hvis du vil inkludere flere data i Common Data Service, må en endring utføres på Microsoft-siden.</span><span class="sxs-lookup"><span data-stu-id="580fc-188">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="580fc-189">Hvis enheten støttes og dataene er tilgjengelige i Common Data Service, må du kontrollere tilordningen er riktig i Dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="580fc-189">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="580fc-190">Hvis integratoren ser ok ut, må du bekrefte at databehandlingsjobbene er kjørt.</span><span class="sxs-lookup"><span data-stu-id="580fc-190">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="580fc-191">Feil kan oppstå under kjøring av satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="580fc-191">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="580fc-192">Hvis du vil ha mer informasjon om Databehandling, kan du se [Databehandling](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="580fc-192">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="580fc-193">Adressene til mine ansatte er feil når jeg importere dem til Finance.</span><span class="sxs-lookup"><span data-stu-id="580fc-193">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="580fc-194">Hva gjør jeg?</span><span class="sxs-lookup"><span data-stu-id="580fc-194">What should I do?</span></span>

<span data-ttu-id="580fc-195">Nummerserien for **Plasserings-ID** bruker samme mønster i både Talent og Finance.</span><span class="sxs-lookup"><span data-stu-id="580fc-195">The number sequence for **Location ID** uses the same pattern in both Talent and Finance.</span></span> <span data-ttu-id="580fc-196">Nummerserien må være unik på begge sider, slik at det ikke finnes noen adressekollisjoner ved integrering av data fra Common Data Service til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="580fc-196">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="580fc-197">Under implementering av Talent må du kontrollere at nummerseriene ikke er de samme i Talent og Finance.</span><span class="sxs-lookup"><span data-stu-id="580fc-197">During implementation of Talent, verify that the number sequences are not the same in Talent and Finance.</span></span> <span data-ttu-id="580fc-198">Valider at alle nummerserier ikke er identiske der data kan vedlikeholdes i begge systemene.</span><span class="sxs-lookup"><span data-stu-id="580fc-198">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="580fc-199">Når jeg oppretter tilkoblingssettet mitt, vises ikke tilkoblingen i rullegardinlisten Tilkobling.</span><span class="sxs-lookup"><span data-stu-id="580fc-199">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="580fc-200">Hva gjør jeg?</span><span class="sxs-lookup"><span data-stu-id="580fc-200">What do I do?</span></span>

<span data-ttu-id="580fc-201">Kontroller at du velger Dynamics 365 Finance og Common Data Service når du oppretter tilkoblinger.</span><span class="sxs-lookup"><span data-stu-id="580fc-201">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="580fc-202">Under synkronisering av distribusjoner får jeg feilen "CompanyInfo_FK finnes ikke" eller "Verdien '12/31/2154 11:59:59 pm' i feltet 'Sluttdato for ansettelse' finnes ikke i den relaterte tabellen 'Ansettelse'". Hva gjør jeg?</span><span class="sxs-lookup"><span data-stu-id="580fc-202">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="580fc-203">Kontroller at du tilordner til de riktige juridiske enhetene.</span><span class="sxs-lookup"><span data-stu-id="580fc-203">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="580fc-204">Den juridiske enheten er ikke en del av standardmalen, så det forventes at hver juridiske enhet som finnes i Talent og Common Data Service, også finnes i Finance.</span><span class="sxs-lookup"><span data-stu-id="580fc-204">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Talent and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="580fc-205">Kontroller også at du velger de riktige juridiske enhetene for det tilknyttede tilkoblingssettet.</span><span class="sxs-lookup"><span data-stu-id="580fc-205">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="580fc-206">Når jeg har definert prosjektet, ser det ut til at felttilordningen for Finance er tomt.</span><span class="sxs-lookup"><span data-stu-id="580fc-206">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="580fc-207">Hva gjør jeg?</span><span class="sxs-lookup"><span data-stu-id="580fc-207">What should I do?</span></span>

<span data-ttu-id="580fc-208">Oppdater dataenhetene i Finance ved å gå til **Databehandling \> Rammeverkparametere \> Enhetsinnstillinger \> Oppdater enhetsliste**.</span><span class="sxs-lookup"><span data-stu-id="580fc-208">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="580fc-209">Dette tar noen minutter å fullføre, og deretter skal du se tilordningene.</span><span class="sxs-lookup"><span data-stu-id="580fc-209">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="580fc-210">Dette problemet skjer ved opprettelse av nye prosjekter.</span><span class="sxs-lookup"><span data-stu-id="580fc-210">This issue occurs when new projects are created.</span></span>

![Mangler felttilordning](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="580fc-212">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="580fc-212">Additional resources</span></span>

- <span data-ttu-id="580fc-213">Dataintegrator (DI):</span><span class="sxs-lookup"><span data-stu-id="580fc-213">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="580fc-214">Integrere data til Common Data Service</span><span class="sxs-lookup"><span data-stu-id="580fc-214">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="580fc-215">Feiladministrasjon og feilsøking av dataintegrator</span><span class="sxs-lookup"><span data-stu-id="580fc-215">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="580fc-216">Svare på DSR-forespørsler om systemgenererte logger i PowerApps, Microsoft Flow og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="580fc-216">Responding to DSR requests for system-generated logs in PowerApps, Microsoft Flow, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="580fc-217">Databehandling:</span><span class="sxs-lookup"><span data-stu-id="580fc-217">Data Management:</span></span>

  - [<span data-ttu-id="580fc-218">Databehandling</span><span class="sxs-lookup"><span data-stu-id="580fc-218">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)
