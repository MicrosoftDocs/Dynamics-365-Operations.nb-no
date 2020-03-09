---
title: Vanlige spørsmål om integrasjon med Finance
description: Denne artikkelen beskriver hvilke data som synkroniseres i en integrasjon med Human Resources og Finance.
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b9cfc0964a532cd32dda029419c892fa8ae55e02
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010039"
---
# <a name="integration-with-finance-faq"></a><span data-ttu-id="ec579-103">Vanlige spørsmål om integrasjon med Finance</span><span class="sxs-lookup"><span data-stu-id="ec579-103">Integration with Finance FAQ</span></span>

<span data-ttu-id="ec579-104">Dette emnet gir svar på vanlige spørsmål som er tilknyttet hvilke data som synkroniseres når Dynamics 365 Human Resources er integrert med Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="ec579-104">This topic answers common questions associated about what data is synchronized when Dynamics 365 Human Resources is integrated with Dynamics 365 Finance.</span></span>

## <a name="is-all-data-synchronized-or-just-some-data-entities"></a><span data-ttu-id="ec579-105">Er alle data synkronisert eller bare noen dataenheter?</span><span class="sxs-lookup"><span data-stu-id="ec579-105">Is all data synchronized or just some data entities?</span></span>

<span data-ttu-id="ec579-106">Et delsett av dataene synkroniseres.</span><span class="sxs-lookup"><span data-stu-id="ec579-106">A subset of the data is synchronized.</span></span> <span data-ttu-id="ec579-107">For en liste over alle enheter, kan du se [Integrering med Dynamics 365 Finance](hr-admin-integration-finance.md).</span><span class="sxs-lookup"><span data-stu-id="ec579-107">For a list of all the entities, see [Integration with Dynamics 365 Finance](hr-admin-integration-finance.md).</span></span>

## <a name="why-dont-i-see-any-data-synced-to-common-data-service"></a><span data-ttu-id="ec579-108">Hvorfor ser jeg ingen data synkronisert til Common Data Service?</span><span class="sxs-lookup"><span data-stu-id="ec579-108">Why don't I see any data synced to Common Data Service?</span></span>

<span data-ttu-id="ec579-109">Som standard er Common Data Service-integreringen deaktivert i nye miljøer som ikke inneholder demodataene.</span><span class="sxs-lookup"><span data-stu-id="ec579-109">By default, the Common Data Service integration is turned off in new environments that don't include the provided demo data.</span></span> <span data-ttu-id="ec579-110">Som standard er den slått på i nye miljøer som inneholder demonstrasjonsdata, og datasynkronisering begynner når miljøet klargjøres.</span><span class="sxs-lookup"><span data-stu-id="ec579-110">By default, it's turned on in new environments that include demo data, and data synchronization begins when the environment is provisioned.</span></span> <span data-ttu-id="ec579-111">Når miljøet er klart til å synkronisere data, kan du aktivere integreringen.</span><span class="sxs-lookup"><span data-stu-id="ec579-111">After your environment is ready to sync data, you can turn on the integration.</span></span> <span data-ttu-id="ec579-112">Hvis du vil ha mer informasjon, kan du se [Konfigurere Common Data Service-integrasjon](hr-admin-integration-common-data-service.md).</span><span class="sxs-lookup"><span data-stu-id="ec579-112">For more information, see [Configure Common Data Service integration](hr-admin-integration-common-data-service.md).</span></span>

## <a name="can-i-create-a-new-mapping-without-using-the-templates"></a><span data-ttu-id="ec579-113">Kan jeg opprette en ny tilordning uten å bruke malene?</span><span class="sxs-lookup"><span data-stu-id="ec579-113">Can I create a new mapping without using the templates?</span></span>

<span data-ttu-id="ec579-114">Malene er startpunktet.</span><span class="sxs-lookup"><span data-stu-id="ec579-114">Templates are the starting point.</span></span> <span data-ttu-id="ec579-115">Du kan opprette din egen mal, men en mal er alltid nødvendig når du oppretter et prosjekt for integrasjon.</span><span class="sxs-lookup"><span data-stu-id="ec579-115">You can create your own template, but a template is always needed when creating an integration project.</span></span> <span data-ttu-id="ec579-116">Hvis du vil ha mer informasjon om dataintegrator (DI), maler og prosjekter, kan du se [Integrere data til Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="ec579-116">For more information about data integrator (DI), templates, and projects, see [Integrate data into Common Data Service](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="can-i-map-financial-dimensions-to-transfer-between-human-resources-and-finance"></a><span data-ttu-id="ec579-117">Kan jeg tilordne finansdimensjoner for å overføre mellom Human Resources og Finance?</span><span class="sxs-lookup"><span data-stu-id="ec579-117">Can I map financial dimensions to transfer between Human Resources and Finance?</span></span>

<span data-ttu-id="ec579-118">Finansdimensjoner er ikke i Common Data Service og er dermed ikke en del av standardmalen.</span><span class="sxs-lookup"><span data-stu-id="ec579-118">Financial dimensions aren’t currently in Common Data Service and as a result aren’t part of the default template.</span></span> <span data-ttu-id="ec579-119">Denne enheten er planlagt, men ingen tidslinje for frigivelse er for øyeblikket tilgjengelig.</span><span class="sxs-lookup"><span data-stu-id="ec579-119">This entity is planned, but currently no release timeline is available.</span></span>

<span data-ttu-id="ec579-120">For data som ligger i Finance, men ikke finnes i Human Resources, koble sammen de to systemene ved å bruke **Konfigurer koblinger** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ec579-120">For data that resides in Finance but does not exist in Human Resources, link the two systems together by using **Configure Links** in Human Resources.</span></span>

![Tilordne finansdimensjoner](media/MapFinancialDimensions.png)

## <a name="sometimes-when-i-import-employees-they-go-into-inactive-workers-in-finance-why"></a><span data-ttu-id="ec579-122">Noen ganger når jeg importerer ansatte, blir de inaktive arbeidere i Finance.</span><span class="sxs-lookup"><span data-stu-id="ec579-122">Sometimes when I import employees, they go into inactive workers in Finance.</span></span> <span data-ttu-id="ec579-123">Hvorfor?</span><span class="sxs-lookup"><span data-stu-id="ec579-123">Why?</span></span>

<span data-ttu-id="ec579-124">Du kan få denne feilen hvis ansatte ikke har en aktiv ansettelsesdetaljpost i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ec579-124">You may get this error if employees don’t have an active employment detail record in Human Resources.</span></span> <span data-ttu-id="ec579-125">Hvis du vil løse dette problemet, kan du gå til **Personaladministrasjon \> Ansatte \> Ansettelseshistorikk \> Datobehandling**, og kontroller at det finnes en aktiv ansettelsesdetaljpost.</span><span class="sxs-lookup"><span data-stu-id="ec579-125">To resolve this, go to **Personnel Management \> Employees \> Employment History \> Date Manager**, and verify that there is an active employment detail record.</span></span>

## <a name="if-i-select-to-map-only-a-subset-of-fields-will-changes-made-to-non-mapped-fields-trigger-a-sync"></a><span data-ttu-id="ec579-126">Hvis jeg velger å tilordne bare et delsett av feltene, vil endringer i ikke-tilordnede felt utløse en synkronisering?</span><span class="sxs-lookup"><span data-stu-id="ec579-126">If I select to map only a subset of fields, will changes made to non-mapped fields trigger a sync?</span></span>

<span data-ttu-id="ec579-127">Datasynkronisering følger tidsplanen for kjøring.</span><span class="sxs-lookup"><span data-stu-id="ec579-127">Data sync follows the execution schedule.</span></span> <span data-ttu-id="ec579-128">Integreringen henter en post hvis et felt i posten endres, uansett om feltet er en del av integreringstilordning.</span><span class="sxs-lookup"><span data-stu-id="ec579-128">The integration will pick up a record if any field in the record changes regardless if the field is part of integration mapping.</span></span>

## <a name="how-can-i-send-only-active-worker-changes-and-not-the-terminated-records"></a><span data-ttu-id="ec579-129">Hvordan kan jeg sende bare aktive arbeiderendringer og ikke de avsluttede postene?</span><span class="sxs-lookup"><span data-stu-id="ec579-129">How can I send only active worker changes and not the terminated records?</span></span>

<span data-ttu-id="ec579-130">Ved hjelp av "Avansert spørring" kan du filtrere og endre kildedataene før de sendes til målet.</span><span class="sxs-lookup"><span data-stu-id="ec579-130">With the use of "Advanced query", you can filter and reshape source data before passing it into the destination.</span></span>

![Avansert spørring for aktive arbeidere](media/MapOnlyActiveWorkersAdvancedQuery.png)

## <a name="can-i-specify-which-fields-to-send-to-finance-for-a-specific-entity"></a><span data-ttu-id="ec579-132">Kan jeg angi hvilke felt som skal sendes til Finance for en bestemt enhet?</span><span class="sxs-lookup"><span data-stu-id="ec579-132">Can I specify which fields to send to Finance for a specific entity?</span></span>

<span data-ttu-id="ec579-133">Feltene kan legges til eller fjernes fra integrasjonsoppgaven.</span><span class="sxs-lookup"><span data-stu-id="ec579-133">Fields can be added or removed from the integration task.</span></span> <span data-ttu-id="ec579-134">Ikke alle datafelt som finnes på Common Data Service-enheten, fylles ut fra Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ec579-134">Not all data fields that exist on the Common Data Service entity will be populated from Human Resources.</span></span>
<span data-ttu-id="ec579-135">Tilleggsdata fylles via Power Apps.</span><span class="sxs-lookup"><span data-stu-id="ec579-135">Additional data can be populated via Power Apps.</span></span>

![Legge til eller fjerne felt fra en integrasjonsoppgave](media/SpecifyFieldsIncludedInIntegration.png)

## <a name="i-set-up-integration-as-a-batch-job-but-human-resources-lost-connection-to-the-destination-system-how-can-i-send-the-same-set-of-changes-to-the-destination-system"></a><span data-ttu-id="ec579-137">Jeg har satt opp integrasjon som en satsvis jobb, men Human Resources mistet forbindelsen til målsystemet.</span><span class="sxs-lookup"><span data-stu-id="ec579-137">I set up integration as a batch job, but Human Resources lost connection to the destination system.</span></span> <span data-ttu-id="ec579-138">Hvordan kan jeg sende det samme settet med endringer til målsystemet?</span><span class="sxs-lookup"><span data-stu-id="ec579-138">How can I send the same set of changes to the destination system?</span></span>

<span data-ttu-id="ec579-139">Det kreves ingen spesielle oppsett for unntaksbehandling.</span><span class="sxs-lookup"><span data-stu-id="ec579-139">No special setup is required for exception handling.</span></span> <span data-ttu-id="ec579-140">Dataintegratoren finner og rapporterer feil som oppstår ved kilden og målet, og tillater nye manuelle forsøk.</span><span class="sxs-lookup"><span data-stu-id="ec579-140">The Data Integrator will automatically catch and report errors which occur at the source and destination and will allow manual retries.</span></span> <span data-ttu-id="ec579-141">Den tillater imidlertid ikke manuell datakorrigering.</span><span class="sxs-lookup"><span data-stu-id="ec579-141">However, it doesn’t allow manual data correction.</span></span> <span data-ttu-id="ec579-142">Hvis dataoppdateringer kreves, skal dette skje enten ved kilden eller målet.</span><span class="sxs-lookup"><span data-stu-id="ec579-142">If data updates are needed, that should happen either at the source or the destination.</span></span>

## <a name="can-i-set-up-bi-directional-integration"></a><span data-ttu-id="ec579-143">Kan jeg konfigurere toveis integrasjon?</span><span class="sxs-lookup"><span data-stu-id="ec579-143">Can I set up bi-directional integration?</span></span>

<span data-ttu-id="ec579-144">Nei, integrasjon er for tiden énveis (Human Resources til Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="ec579-144">No, integration is currently one-way (Human Resources to Finance and Operations).</span></span> <span data-ttu-id="ec579-145">Det finnes imidlertid en standardmal som er tilgjengelig for å sende data fra Human Resources til Finance.</span><span class="sxs-lookup"><span data-stu-id="ec579-145">However, there is a default template available to send data from Human Resources to Finance.</span></span>

## <a name="can-i-allow-record-deletion-as-part-of-my-integration"></a><span data-ttu-id="ec579-146">Kan jeg tillate sletting av oppføringer som en del av min integrasjon?</span><span class="sxs-lookup"><span data-stu-id="ec579-146">Can I allow record deletion as part of my integration?</span></span>

<span data-ttu-id="ec579-147">Nei, Dataintegrator registrerer ikke slettede poster for dataoverføring.</span><span class="sxs-lookup"><span data-stu-id="ec579-147">No, Data Integrator will not capture deleted records for data transfer.</span></span> <span data-ttu-id="ec579-148">Bare oppretting og oppdatering av data (UPSERT) er for øyeblikket inkludert.</span><span class="sxs-lookup"><span data-stu-id="ec579-148">Only data creation and updates (UPSERT) are currently included.</span></span>

## <a name="can-i-rerun-the-errored-execution-if-so-will-it-send-a-full-file-or-only-the-changes"></a><span data-ttu-id="ec579-149">Kan jeg utføre kjøringen med feil på nytt?</span><span class="sxs-lookup"><span data-stu-id="ec579-149">Can I rerun the errored execution?</span></span> <span data-ttu-id="ec579-150">Sendes i så fall en fullstendig fil eller bare endringene?</span><span class="sxs-lookup"><span data-stu-id="ec579-150">If so, will it send a full file or only the changes?</span></span>

<span data-ttu-id="ec579-151">Den første kjøringen av Dataintegrator er alltid en full kjøring.</span><span class="sxs-lookup"><span data-stu-id="ec579-151">The first run of Data Integrator is always a full run.</span></span> <span data-ttu-id="ec579-152">Senere kjøringer er basert på endringssporing.</span><span class="sxs-lookup"><span data-stu-id="ec579-152">Subsequent runs are based on change tracking.</span></span> <span data-ttu-id="ec579-153">Når en feilkjøring utføres, trekker den ut postene i omfanget for kjøringen og sender ut de siste endringene fra Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ec579-153">When an error run is executed, it extracts the records in scope of the run and sends out the most recent changes from Common Data Service.</span></span>

## <a name="when-i-save-the-project-i-get-the-error-project-has-mapping-errors-what-do-i-do"></a><span data-ttu-id="ec579-154">Når jeg lagrer prosjektet, får jeg feilen: "Prosjektet har tilordningsfeil."</span><span class="sxs-lookup"><span data-stu-id="ec579-154">When I save the project, I get the error: “Project has mapping errors."</span></span> <span data-ttu-id="ec579-155">Hva gjør jeg?</span><span class="sxs-lookup"><span data-stu-id="ec579-155">What do I do?</span></span>

<span data-ttu-id="ec579-156">Kontroller oppsettet for integrasjonsnøklene, foreta nødvendige endringer i oppsettet, og oppdater enhetene i prosjektet.</span><span class="sxs-lookup"><span data-stu-id="ec579-156">Check the setup of your integration keys, make any required changes to the setup, then refresh the entities in the project.</span></span>

<span data-ttu-id="ec579-157">Når standardmalen brukes, blir nøklene for integrering automatisk importert.</span><span class="sxs-lookup"><span data-stu-id="ec579-157">When the default template is used, the integration keys will be automatically imported.</span></span> <span data-ttu-id="ec579-158">Dette problemet kan oppstå når nye aktiviteter legges til i den eksisterende malen.</span><span class="sxs-lookup"><span data-stu-id="ec579-158">This issue may occur when new tasks are added to the existing template.</span></span>

## <a name="if-i-have-n-number-of-legal-entities-where-workers-have-employments-do-i-need-to-create-a-mapping-for-each-of-them"></a><span data-ttu-id="ec579-159">Hvis jeg har N antall juridiske enheter der arbeidere har ansettelser, trenger jeg å opprette en tilordning for hver av dem?</span><span class="sxs-lookup"><span data-stu-id="ec579-159">If I have N number of legal entities where workers have employments, do I need to create a mapping for each of them?</span></span>

<span data-ttu-id="ec579-160">Ja, for hver juridiske enhet i Finance må du ha et eget integrasjonsprosjekt i dataintegreringen.</span><span class="sxs-lookup"><span data-stu-id="ec579-160">Yes, for each legal entity in Finance, you'll need a separate integration project in the data integration.</span></span>

## <a name="i-need-to-transfer-data-that-is-not-part-of-the-default-template-provided-by-microsoft-can-i-do-this"></a><span data-ttu-id="ec579-161">Jeg vil overføre data som ikke er en del av standardmalen fra Microsoft.</span><span class="sxs-lookup"><span data-stu-id="ec579-161">I need to transfer data that is not part of the default template provided by Microsoft.</span></span> <span data-ttu-id="ec579-162">Kan jeg gjøre dette?</span><span class="sxs-lookup"><span data-stu-id="ec579-162">Can I do this?</span></span>

<span data-ttu-id="ec579-163">Ja, feltene kan legges til eller fjernes fra den eksisterende malen.</span><span class="sxs-lookup"><span data-stu-id="ec579-163">Yes, fields can be added to or removed from the existing template.</span></span> <span data-ttu-id="ec579-164">Malen kan endres for å ta med flere data fra andre Common Data Service-enheter.</span><span class="sxs-lookup"><span data-stu-id="ec579-164">The template can be modified to include additional data from other Common Data Service entities.</span></span> <span data-ttu-id="ec579-165">Enheten må være i Common Data Service for at den skal inkluderes i malen.</span><span class="sxs-lookup"><span data-stu-id="ec579-165">The entity must be in Common Data Service for it to be included in the template.</span></span> 

## <a name="i-just-created-new-finance-and-human-resources-environments-and-im-getting-the-error-the-data-value-violates-integrity-constraints-why"></a><span data-ttu-id="ec579-166">Jeg har nettopp opprettet nye Finance- og Human Resources-miljøer, og jeg får feilen "Dataverdien bryter integritetsbegrensninger."</span><span class="sxs-lookup"><span data-stu-id="ec579-166">I just created new Finance and Human Resources environments, and I'm getting the error "The data value violates integrity constraints."</span></span> <span data-ttu-id="ec579-167">Hvorfor?</span><span class="sxs-lookup"><span data-stu-id="ec579-167">Why?</span></span>

<span data-ttu-id="ec579-168">Årsaker til denne feilen kan omfatte:</span><span class="sxs-lookup"><span data-stu-id="ec579-168">Reasons for this error can include:</span></span>

- <span data-ttu-id="ec579-169">Dataoverføringen resulterte i duplisert postuttrekk ved kilden (Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="ec579-169">The data transfer resulted in duplicate records extraction at the source (Common Data Service).</span></span>

- <span data-ttu-id="ec579-170">Dataoverføringen har nullverdier for feltene som kreves i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ec579-170">The data transfer has null values for fields that are required in Finance and Operations.</span></span> <span data-ttu-id="ec579-171">Kontroller at dataene er i Common Data Service og oppfyller kravene fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ec579-171">Verify the data that is in Common Data Service and meets the requirements of Finance and Operations.</span></span>

## <a name="if-there-are-execution-errors-and-the-employee-id-didnt-sync-how-do-i-find-the-history-job-which-has-the-failed-employee-record"></a><span data-ttu-id="ec579-172">Hvis det er kjøringsfeil og ansatt-ID-en ikke synkroniseres, hvordan kan jeg finne den historiske jobben som har feil ansattpost?</span><span class="sxs-lookup"><span data-stu-id="ec579-172">If there are execution errors and the Employee ID didn't sync, how do I find the history job which has the failed employee record?</span></span>

<span data-ttu-id="ec579-173">Dataintegratoren oppretter flere prosjekter i Finance.</span><span class="sxs-lookup"><span data-stu-id="ec579-173">Data Integrator will create multiple projects in Finance.</span></span> <span data-ttu-id="ec579-174">Relasjonen mellom Dataintegrator-oppgaven og Finance-prosjektet er én til én.</span><span class="sxs-lookup"><span data-stu-id="ec579-174">The relationship between the Data Integrator task and the Finance project is one to one.</span></span>

<span data-ttu-id="ec579-175">Spor tiden fra Dataintegrator-kjøringshistorikken, og se etter indeksen -1 i Finance.</span><span class="sxs-lookup"><span data-stu-id="ec579-175">Trace the time from the Data Integrator execution history and look for the index -1 project in Finance.</span></span> <span data-ttu-id="ec579-176">Hvis oppgavenummeret er 9 i Dataintegrator, er indeksen i Finance 8.</span><span class="sxs-lookup"><span data-stu-id="ec579-176">If the task number is 9 in Data Integrator, the index in Finance is 8.</span></span>

1. <span data-ttu-id="ec579-177">Lagre oppgaveindeksen fra Dataintegrator (i dette eksemplet er det "9").</span><span class="sxs-lookup"><span data-stu-id="ec579-177">Capture the task index from Data Integrator (in this example it is "9").</span></span>

    ![Lagre oppgaveindeksen fra Dataintegrator](media/CaptureTaskIndex.png)

2. <span data-ttu-id="ec579-179">Spor kjøretiden for prosjektet.</span><span class="sxs-lookup"><span data-stu-id="ec579-179">Track the execution time of the project.</span></span>

    ![Spore kjøretiden for prosjektet](media/CaptureTimeOfExecution.png)

3. <span data-ttu-id="ec579-181">Identifiser indeks -1 i Finance.</span><span class="sxs-lookup"><span data-stu-id="ec579-181">In Finance, identify index - 1.</span></span> <span data-ttu-id="ec579-182">I dette eksemplet samsvarer prosjektet med suffikset "8" og utførelsestiden for indeksen "0"-prosjektet med kjøretiden i trinn 2.</span><span class="sxs-lookup"><span data-stu-id="ec579-182">In this example, the project with suffix "8" and execution time of index "0" project matches with the execution time in Step 2.</span></span>

    ![Identifisere indeks](media/IdentifyIndex.png)

## <a name="after-integrating-human-resources-and-finance-i-dont-see-my-human-resources-data-in-finance-what-do-i-do"></a><span data-ttu-id="ec579-184">Etter å ha integrert Human Resources og Finance, ser jeg ikke Human Resources-dataene mine i Finance.</span><span class="sxs-lookup"><span data-stu-id="ec579-184">After integrating Human Resources and Finance, I don’t see my Human Resources data in Finance.</span></span> <span data-ttu-id="ec579-185">Hva gjør jeg?</span><span class="sxs-lookup"><span data-stu-id="ec579-185">What do I do?</span></span>

<span data-ttu-id="ec579-186">Integreringen til Finance er en totrinns prosess.</span><span class="sxs-lookup"><span data-stu-id="ec579-186">The integration to Finance is a two-step process.</span></span> <span data-ttu-id="ec579-187">Først bekrefter du at Human Resources-dataene er oppdaterte og tilgjengelige i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="ec579-187">First, verify that the Human Resources data is updated and available in Common Data Service.</span></span> <span data-ttu-id="ec579-188">Dette er en nær sanntidssynkronisering og kan kontrolleres i Power Apps ved å se på dataene i dataenhetene.</span><span class="sxs-lookup"><span data-stu-id="ec579-188">This is a near real-time sync and can be verified in Power Apps by looking at the data within the data entities.</span></span>

![Data i Common Data Service](media/DataInCDS.png)

<span data-ttu-id="ec579-190">Hvis dataene ikke vises som forventet i Common Data Service, må du kontrollere at enheten støttes i integreringen.</span><span class="sxs-lookup"><span data-stu-id="ec579-190">If the data is not appearing as expected in Common Data Service, verify that the entity is supported in the integration.</span></span> <span data-ttu-id="ec579-191">Hvis du vil inkludere flere data i Common Data Service, må en endring utføres på Microsoft-siden.</span><span class="sxs-lookup"><span data-stu-id="ec579-191">To include additional data in Common Data Service, a change will be required on the Microsoft side.</span></span>

<span data-ttu-id="ec579-192">Hvis enheten støttes og dataene er tilgjengelige i Common Data Service, må du kontrollere tilordningen er riktig i Dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="ec579-192">If the entity is supported and the data is available in Common Data Service, verify the mapping is correct in Data Integrator.</span></span> <span data-ttu-id="ec579-193">Hvis integratoren ser ok ut, må du bekrefte at databehandlingsjobbene er kjørt.</span><span class="sxs-lookup"><span data-stu-id="ec579-193">If the integrator mapping looks okay, then verify the data management jobs have successfully run.</span></span> <span data-ttu-id="ec579-194">Feil kan oppstå under kjøring av satsvise jobber.</span><span class="sxs-lookup"><span data-stu-id="ec579-194">Errors may occur during the execution of the batch jobs.</span></span> <span data-ttu-id="ec579-195">Hvis du vil ha mer informasjon om Databehandling, kan du se [Databehandling](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span><span class="sxs-lookup"><span data-stu-id="ec579-195">For more information about Data Management, see [Data management](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json).</span></span>

## <a name="the-addresses-for-my-employees-are-incorrect-after-i-import-them-into-finance-what-should-i-do"></a><span data-ttu-id="ec579-196">Adressene til mine ansatte er feil når jeg importere dem til Finance.</span><span class="sxs-lookup"><span data-stu-id="ec579-196">The addresses for my employees are incorrect after I import them into Finance.</span></span> <span data-ttu-id="ec579-197">Hva gjør jeg?</span><span class="sxs-lookup"><span data-stu-id="ec579-197">What should I do?</span></span>

<span data-ttu-id="ec579-198">Nummerserien for **Plasserings-ID** bruker samme mønster i både Human Resources og Finance.</span><span class="sxs-lookup"><span data-stu-id="ec579-198">The number sequence for **Location ID** uses the same pattern in both Human Resources and Finance.</span></span> <span data-ttu-id="ec579-199">Nummerserien må være unik på begge sider, slik at det ikke finnes noen adressekollisjoner ved integrering av data fra Common Data Service til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="ec579-199">The number sequence needs to be unique on both sides so there are no address collisions when integrating data from Common Data Service to Finance and Operations.</span></span>

<span data-ttu-id="ec579-200">Under implementering av Human Resources må du kontrollere at nummerseriene ikke er de samme i Human Resources og Finance.</span><span class="sxs-lookup"><span data-stu-id="ec579-200">During implementation of Human Resources, verify that the number sequences are not the same in Human Resources and Finance.</span></span> <span data-ttu-id="ec579-201">Valider at alle nummerserier ikke er identiske der data kan vedlikeholdes i begge systemene.</span><span class="sxs-lookup"><span data-stu-id="ec579-201">Validate that all number sequences are not identical where data may be maintained in both systems.</span></span>

## <a name="when-creating-my-connection-set-i-am-unable-to-see-the-connection-in-the-connection-drop-down-list-what-do-i-do"></a><span data-ttu-id="ec579-202">Når jeg oppretter tilkoblingssettet mitt, vises ikke tilkoblingen i rullegardinlisten Tilkobling.</span><span class="sxs-lookup"><span data-stu-id="ec579-202">When creating my connection set, I am unable to see the connection in the Connection drop-down list.</span></span> <span data-ttu-id="ec579-203">Hva gjør jeg?</span><span class="sxs-lookup"><span data-stu-id="ec579-203">What do I do?</span></span>

<span data-ttu-id="ec579-204">Kontroller at du velger Dynamics 365 Finance og Common Data Service når du oppretter tilkoblinger.</span><span class="sxs-lookup"><span data-stu-id="ec579-204">Make sure when creating your connections, you choose Dynamics 365 Finance and Common Data Service.</span></span>

## <a name="when-syncing-employments-i-get-the-errors-companyinfo_fk-doesnt-exist-or-the-value-12312154-115959-pm-in-field-employment-end-date-is-not-found-in-the-related-table-employment-what-should-i-do"></a><span data-ttu-id="ec579-205">Under synkronisering av distribusjoner får jeg feilen "CompanyInfo_FK finnes ikke" eller "Verdien '12/31/2154 11:59:59 pm' i feltet 'Sluttdato for ansettelse' finnes ikke i den relaterte tabellen 'Ansettelse'". Hva gjør jeg?</span><span class="sxs-lookup"><span data-stu-id="ec579-205">When syncing employments, I get the errors “CompanyInfo_FK doesn’t exist" or “The value '12/31/2154 11:59:59 pm' in field 'Employment end date' is not found in the related table 'Employment'.” What should I do?</span></span>

<span data-ttu-id="ec579-206">Kontroller at du tilordner til de riktige juridiske enhetene.</span><span class="sxs-lookup"><span data-stu-id="ec579-206">Ensure that you are mapping to the correct legal entities.</span></span> <span data-ttu-id="ec579-207">Den juridiske enheten er ikke en del av standardmalen, så det forventes at hver juridiske enhet som finnes i Human Resources og Common Data Service, også finnes i Finance.</span><span class="sxs-lookup"><span data-stu-id="ec579-207">Legal entity syncing is not part of the default template, so it is expected that each legal entity that is present in Human Resources and Common Data Service is also present in Finance.</span></span>
<span data-ttu-id="ec579-208">Kontroller også at du velger de riktige juridiske enhetene for det tilknyttede tilkoblingssettet.</span><span class="sxs-lookup"><span data-stu-id="ec579-208">Also, make sure that you are selecting the correct legal entities for the associated Connection Set.</span></span>

## <a name="after-setting-up-my-project-the-field-mapping-for-finance-appears-to-be-empty-what-should-i-do"></a><span data-ttu-id="ec579-209">Når jeg har definert prosjektet, ser det ut til at felttilordningen for Finance er tomt.</span><span class="sxs-lookup"><span data-stu-id="ec579-209">After setting up my project, the field mapping for Finance appears to be empty.</span></span> <span data-ttu-id="ec579-210">Hva gjør jeg?</span><span class="sxs-lookup"><span data-stu-id="ec579-210">What should I do?</span></span>

<span data-ttu-id="ec579-211">Oppdater dataenhetene i Finance ved å gå til **Databehandling \> Rammeverkparametere \> Enhetsinnstillinger \> Oppdater enhetsliste**.</span><span class="sxs-lookup"><span data-stu-id="ec579-211">Refresh the data entities in Finance by going to **Data management \> Framework Parameters \> Entity settings \> Refresh entity list.**</span></span> <span data-ttu-id="ec579-212">Dette tar noen minutter å fullføre, og deretter skal du se tilordningene.</span><span class="sxs-lookup"><span data-stu-id="ec579-212">This should take a couple of minutes to complete, then you should see those mappings.</span></span> <span data-ttu-id="ec579-213">Dette problemet skjer ved opprettelse av nye prosjekter.</span><span class="sxs-lookup"><span data-stu-id="ec579-213">This issue occurs when new projects are created.</span></span>

![Mangler felttilordning](media/MissingFieldMapping.png)

## <a name="additional-resources"></a><span data-ttu-id="ec579-215">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="ec579-215">Additional resources</span></span>

- <span data-ttu-id="ec579-216">Dataintegrator (DI):</span><span class="sxs-lookup"><span data-stu-id="ec579-216">Data Integrator (DI):</span></span> 

  - [<span data-ttu-id="ec579-217">Integrere data til Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ec579-217">Integrate data into Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator)

  - [<span data-ttu-id="ec579-218">Feiladministrasjon og feilsøking av dataintegrator</span><span class="sxs-lookup"><span data-stu-id="ec579-218">Data Integrator error management and troubleshooting</span></span>](https://docs.microsoft.com/powerapps/administrator/data-integrator-error-management)

  - [<span data-ttu-id="ec579-219">Svare på DSR-forespørsler om systemgenererte logger i Power Apps, Microsoft Power Automate og Common Data Service</span><span class="sxs-lookup"><span data-stu-id="ec579-219">Responding to DSR requests for system-generated logs in Power Apps, Microsoft Power Automate, and Common Data Service</span></span>](https://docs.microsoft.com/powerapps/administrator/powerapps-gdpr-dsr-guide-systemlogs)

- <span data-ttu-id="ec579-220">Databehandling:</span><span class="sxs-lookup"><span data-stu-id="ec579-220">Data Management:</span></span>

  - [<span data-ttu-id="ec579-221">Databehandling</span><span class="sxs-lookup"><span data-stu-id="ec579-221">Data management</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/data-entities/data-entities-data-packages?toc=/fin-and-ops/toc.json)