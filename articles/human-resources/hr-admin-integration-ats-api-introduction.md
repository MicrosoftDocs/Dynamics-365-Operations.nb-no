---
title: Innføring i API for søkersporingssystemintegrering
description: Dette emnet beskriver Dynamics 365 Human Resources API for søkersporingssystemintegrering.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 48e368fe69443a5105ddba78a887bf9159bfe52a
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125599"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a><span data-ttu-id="f0d03-103">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="f0d03-103">Applicant Tracking System integration API introduction</span></span>

<span data-ttu-id="f0d03-104">Dette emnet beskriver Dynamics 365 Human Resources API for søkersporingssystemintegrering.</span><span class="sxs-lookup"><span data-stu-id="f0d03-104">This topic describes the Dynamics 365 Human Resources Applicant Tracking System (ATS) integration API.</span></span> <span data-ttu-id="f0d03-105">Hensikten med API-en er å aktivere strømlinjeformet integrasjon mellom Dynamics 365 Human Resources og partner-ATS-er.</span><span class="sxs-lookup"><span data-stu-id="f0d03-105">The intent of the API is to enable streamlined integrations between Dynamics 365 Human Resources and partnering ATSs.</span></span>

![ATS-integrasjonsflyt](media/hr-admin-integration-ats-api-introduction-flow.png)

<span data-ttu-id="f0d03-107">Den integrerte erfaringen begynner i Human Resources når en ansettelsesansvarlig oppretter en rekrutteringsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="f0d03-107">The integrated experience begins in Human Resources when a hiring manager creates a recruiting request.</span></span> <span data-ttu-id="f0d03-108">Når forespørselen er aktivert, henter ATS detaljene for forespørselen om å opprette et rekrutteringsprosjekt.</span><span class="sxs-lookup"><span data-stu-id="f0d03-108">When the request is activated, the ATS pulls the detail for the request to create a recruiting project.</span></span> <span data-ttu-id="f0d03-109">Deretter følger rekrutteringsforløpet for å velge og ansette en kandidat til stillingen(e).</span><span class="sxs-lookup"><span data-stu-id="f0d03-109">Then it follows the recruiting pipeline to select and hire a candidate for the position(s).</span></span> <span data-ttu-id="f0d03-110">Til slutt fullfører ATS integreringen med rundturintegrering ved å sende den valgte kandidatens post til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="f0d03-110">Finally, the ATS completes the round-trip integration by sending the selected candidate’s record into Human Resources.</span></span> <span data-ttu-id="f0d03-111">Kandidatposten kan deretter gå gjennom mer pålastingsvalideringer og arbeidsflyter for å opprette ansattposten.</span><span class="sxs-lookup"><span data-stu-id="f0d03-111">The candidate record can then go through more onboarding validations and workflows to create the employee record.</span></span>

<span data-ttu-id="f0d03-112">Human Resources har lagt til følgende komponenter for å aktivere integreringen:</span><span class="sxs-lookup"><span data-stu-id="f0d03-112">To enable the integration, Human Resources has added the following components:</span></span>

1.  <span data-ttu-id="f0d03-113">Funksjonalitet for å opprette en rekrutteringsforespørsel.</span><span class="sxs-lookup"><span data-stu-id="f0d03-113">Functionality to create a recruiting request.</span></span>
2.  <span data-ttu-id="f0d03-114">Utvidet kandidatprofil og tilknyttede arbeidsflyter.</span><span class="sxs-lookup"><span data-stu-id="f0d03-114">An expanded candidate profile and related workflows.</span></span>
3.  <span data-ttu-id="f0d03-115">En integrerings-API som åpner opp den nye funksjonaliteten for integrering av programmer.</span><span class="sxs-lookup"><span data-stu-id="f0d03-115">An integration API opening up the new functionality to integrating applications.</span></span>

<span data-ttu-id="f0d03-116">Hvis du vil ha mer informasjon om hvordan du definerer og bruker rekrutteringsforespørselen og kandidatfunksjonaliteten, kan du se [Rekruttering av jobbkandidater](hr-personnel-recruit.md).</span><span class="sxs-lookup"><span data-stu-id="f0d03-116">For more information about setting up and using the recruiting request and candidate functionality, see [Recruit job candidates](hr-personnel-recruit.md).</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="f0d03-117">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="f0d03-117">Microsoft Dataverse</span></span>

<span data-ttu-id="f0d03-118">Denne API-en er bygd på Microsoft Dataverse (tidligere kalt Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="f0d03-118">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="f0d03-119">All RESTful-samhandling med denne API-en gjøres via web-API-en for Microsoft Dataverse, som bruker OData.</span><span class="sxs-lookup"><span data-stu-id="f0d03-119">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="f0d03-120">Denne API-en er et delsett av Dataverse-web-API-en.</span><span class="sxs-lookup"><span data-stu-id="f0d03-120">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="f0d03-121">Dataverse-web-API-en definerer egenskaper som godkjenning, SLA-er, parti, samtidighetskontroll og feilhåndtering.</span><span class="sxs-lookup"><span data-stu-id="f0d03-121">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="f0d03-122">Hvis du vil ha mer generell informasjon om Microsoft Dataverse-web-API-en, kan du se:</span><span class="sxs-lookup"><span data-stu-id="f0d03-122">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="f0d03-123">Hva er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="f0d03-123">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="f0d03-124">Bruke Microsoft Dataverse-web-API-en</span><span class="sxs-lookup"><span data-stu-id="f0d03-124">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="f0d03-125">Utviklerveiledning for Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="f0d03-125">Microsoft Dataverse developer guide</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform)

<span data-ttu-id="f0d03-126">Dokumentasjonen ovenfor inneholder detaljer og utviklerveiledning for bruk av web-API for Dataverse, for eksempel [administrasjon av godkjenning](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [utføre operasjoner](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [bruke Postman med API-en](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api) og [bruker endringssporing eller deltatokener](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) med API-en.</span><span class="sxs-lookup"><span data-stu-id="f0d03-126">The above documentation includes detail and developer guidance on using the Dataverse Web API, such as [managing authentication](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/authenticate-web-api), [performing operations](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/perform-operations-web-api), [using Postman with the API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/use-postman-web-api), and [using change tracking or delta tokens](https://docs.microsoft.com/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) with the API.</span></span>

### <a name="option-sets"></a><span data-ttu-id="f0d03-127">Alternativsett</span><span class="sxs-lookup"><span data-stu-id="f0d03-127">Option sets</span></span>

<span data-ttu-id="f0d03-128">Datamodellen for ATS-integrerings-API-en som er beskrevet i dette dokumentet, inneholder alternativsett som inneholder opplistingsverdier som er knyttet til enhetsegenskaper.</span><span class="sxs-lookup"><span data-stu-id="f0d03-128">The data model for the ATS integration API described in this document includes option sets that provide enumerated values associated with entity properties.</span></span> <span data-ttu-id="f0d03-129">Hvis du vil ha detaljert informasjon om hvordan du arbeider med alternativsett i web-API for Dataverse, kan du se [Opprette og oppdatere alternativsett ved hjelp av web-API-en](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span><span class="sxs-lookup"><span data-stu-id="f0d03-129">For detail on working with option sets in the Dataverse Web API, see [Create and update option sets using the Web API](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets).</span></span> <span data-ttu-id="f0d03-130">Alternativsett defineres for hvert Dataverse-miljø.</span><span class="sxs-lookup"><span data-stu-id="f0d03-130">Option sets are defined for each Dataverse environment.</span></span>

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="f0d03-131">Virtuelle tabeller for Human Resources i Dataverse</span><span class="sxs-lookup"><span data-stu-id="f0d03-131">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="f0d03-132">Sluttpunktene for ATS-integrerings-API-en bruker de virtuelle tabellplattformfunksjonene i Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="f0d03-132">The endpoints for the ATS integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="f0d03-133">Som standard distribueres ikke de virtuelle tabellene og de tilknyttede API-sluttpunktene for Human Resources-miljøene, som gjør det mulig for organisasjoner å fastslå hvilke OData-sluttpunkter som vises for miljøet.</span><span class="sxs-lookup"><span data-stu-id="f0d03-133">By default, the virtual tables and their associated API endpoints are not deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="f0d03-134">For å kunne bruke API-en må de virtuelle tabellene for Human Resources-enhetene genereres for miljøet.</span><span class="sxs-lookup"><span data-stu-id="f0d03-134">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span> 

<span data-ttu-id="f0d03-135">Hvis du vil ha informasjon om generering av de virtuelle tabellene for API, kan du se [Konfigurere virtuelle Dataverse-tabeller](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span><span class="sxs-lookup"><span data-stu-id="f0d03-135">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-common-data-service-virtual-entities).</span></span>

## <a name="data-model"></a><span data-ttu-id="f0d03-136">Datamodell</span><span class="sxs-lookup"><span data-stu-id="f0d03-136">Data model</span></span>

<span data-ttu-id="f0d03-137">Datamodellen er sentrert rundt to hovedenheter:</span><span class="sxs-lookup"><span data-stu-id="f0d03-137">The data model is centered around two main entities:</span></span>

- <span data-ttu-id="f0d03-138">**RecruitingRequest** representerer en forespørsel til en ATS om å rekruttere for én eller flere åpne stillinger. Hvis du vil ha en eksempelspørring, kan du se [Eksempelspørring for rekrutteringsforespørsel](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="f0d03-138">**RecruitingRequest** represents a request to an ATS to recruit for one or more open positions.For an example query, see [Example query for Recruiting request](hr-admin-integration-ats-api-recruiting-request-example-query.md).</span></span>
- <span data-ttu-id="f0d03-139">**CandidateToHire** representerer detaljer til en kandidat som har tatt imot et tilbud om en stilling.</span><span class="sxs-lookup"><span data-stu-id="f0d03-139">**CandidateToHire** represents details of a candidate who has accepted an offer for a position.</span></span> <span data-ttu-id="f0d03-140">**Person** representerer personen som er kandidaten.</span><span class="sxs-lookup"><span data-stu-id="f0d03-140">**Person** represents the individual who is the candidate.</span></span> <span data-ttu-id="f0d03-141">En person kan ha flere roller i firmaet, for eksempel kandidat, arbeider, ansatt eller oppdragstaker.</span><span class="sxs-lookup"><span data-stu-id="f0d03-141">A person can have multiple roles in the company, such as candidate, worker, employee, or contractor.</span></span> <span data-ttu-id="f0d03-142">Hvis du vil ha en eksempelspørring, kan du se [Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span><span class="sxs-lookup"><span data-stu-id="f0d03-142">For an example query, see [Example query for Candidate to hire](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).</span></span>

<span data-ttu-id="f0d03-143">Diagrammet nedenfor illustrerer relasjonen med API-en.</span><span class="sxs-lookup"><span data-stu-id="f0d03-143">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="f0d03-144">Flere typer har sekundærnøkler til andre, eksisterende enheter i Human Resources som ikke illustreres her.</span><span class="sxs-lookup"><span data-stu-id="f0d03-144">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="f0d03-145">Dette dokumentet inneholder informasjon om enheter som er spesifikke for rekrutteringsintegrasjonsscenarier.</span><span class="sxs-lookup"><span data-stu-id="f0d03-145">This document provides information on entities that are specific to recruiting integration scenarios.</span></span> <span data-ttu-id="f0d03-146">Det er imidlertid mange andre enheter i Dataverse-web-APIen for Dynamics 365 Human Resources som også kan være relevante for integreringen.</span><span class="sxs-lookup"><span data-stu-id="f0d03-146">However, there are many other entities in the Dataverse Web API for Dynamics 365 Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="f0d03-147">Det kan for eksempel også hende du trenger detaljer for arbeidere, jobber, stillinger eller andre enheter som ikke er definert her.</span><span class="sxs-lookup"><span data-stu-id="f0d03-147">For example, you may also need detail for workers, jobs, positions, or other entities not defined here.</span></span> <span data-ttu-id="f0d03-148">Mange av disse enhetene refereres til i sekundærnøkkelrelasjoner eller navigasjonsegenskaper.</span><span class="sxs-lookup"><span data-stu-id="f0d03-148">Many of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![ATS-integrering, API-datamodell](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a><span data-ttu-id="f0d03-150">Rekrutteringsforespørsel og relaterte enheter og alternativsett</span><span class="sxs-lookup"><span data-stu-id="f0d03-150">Recruiting request and related entities and option sets</span></span>

<span data-ttu-id="f0d03-151">Eksempelspørring:</span><span class="sxs-lookup"><span data-stu-id="f0d03-151">Example query:</span></span> 

- [<span data-ttu-id="f0d03-152">Eksempelspørring for rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="f0d03-152">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)

<span data-ttu-id="f0d03-153">Enheter:</span><span class="sxs-lookup"><span data-stu-id="f0d03-153">Entities:</span></span>

- [<span data-ttu-id="f0d03-154">Rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="f0d03-154">Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request.md)
- [<span data-ttu-id="f0d03-155">Rekrutteringsforespørselsstilling</span><span class="sxs-lookup"><span data-stu-id="f0d03-155">Recruiting request position</span></span>](hr-admin-integration-ats-api-recruiting-request-position.md)
- [<span data-ttu-id="f0d03-156">Rekrutteringsforespørselsferdighet</span><span class="sxs-lookup"><span data-stu-id="f0d03-156">Recruiting request skill</span></span>](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [<span data-ttu-id="f0d03-157">Rekrutteringsforespørselsutdanning</span><span class="sxs-lookup"><span data-stu-id="f0d03-157">Recruiting request education</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="f0d03-158">Rekrutteringsforespørselssted</span><span class="sxs-lookup"><span data-stu-id="f0d03-158">Recruiting request location</span></span>](hr-admin-integration-ats-api-recruiting-request-location.md)

<span data-ttu-id="f0d03-159">Alternativsett:</span><span class="sxs-lookup"><span data-stu-id="f0d03-159">Option sets:</span></span>

- [<span data-ttu-id="f0d03-160">Jobbfritaksstatus</span><span class="sxs-lookup"><span data-stu-id="f0d03-160">Job exempt status</span></span>](hr-admin-integration-ats-api-job-exempt-status.md)
- [<span data-ttu-id="f0d03-161">Status for rekrutteringsforespørselsstilling</span><span class="sxs-lookup"><span data-stu-id="f0d03-161">Recruiting request position status</span></span>](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [<span data-ttu-id="f0d03-162">Rekrutteringsforespørselsstatus</span><span class="sxs-lookup"><span data-stu-id="f0d03-162">Recruiting request status</span></span>](hr-admin-integration-ats-api-recruiting-request-status.md)
- [<span data-ttu-id="f0d03-163">Forskriftsmessig jobbkategori</span><span class="sxs-lookup"><span data-stu-id="f0d03-163">Regulatory job category</span></span>](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a><span data-ttu-id="f0d03-164">Kandidat for ansettelse og relaterte enheter og alternativsett</span><span class="sxs-lookup"><span data-stu-id="f0d03-164">Candidate to hire and related entities and option sets</span></span>

<span data-ttu-id="f0d03-165">Eksempelspørring:</span><span class="sxs-lookup"><span data-stu-id="f0d03-165">Example query:</span></span>

- [<span data-ttu-id="f0d03-166">Eksempelspørring for Kandidat for ansettelse</span><span class="sxs-lookup"><span data-stu-id="f0d03-166">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

<span data-ttu-id="f0d03-167">Enheter:</span><span class="sxs-lookup"><span data-stu-id="f0d03-167">Entities:</span></span>

- [<span data-ttu-id="f0d03-168">Ansettelseskandidat</span><span class="sxs-lookup"><span data-stu-id="f0d03-168">Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire.md)
- [<span data-ttu-id="f0d03-169">Person</span><span class="sxs-lookup"><span data-stu-id="f0d03-169">Person</span></span>](hr-admin-integration-ats-api-person.md)
- [<span data-ttu-id="f0d03-170">Personutdanning</span><span class="sxs-lookup"><span data-stu-id="f0d03-170">Person education</span></span>](hr-admin-integration-ats-api-person-education.md)
- [<span data-ttu-id="f0d03-171">Persons yrkeserfaring</span><span class="sxs-lookup"><span data-stu-id="f0d03-171">Person professional experience</span></span>](hr-admin-integration-ats-api-person-professional-experience.md)
- [<span data-ttu-id="f0d03-172">Personadresse</span><span class="sxs-lookup"><span data-stu-id="f0d03-172">Person address</span></span>](hr-admin-integration-ats-api-person-address.md)
- [<span data-ttu-id="f0d03-173">Partskontakt</span><span class="sxs-lookup"><span data-stu-id="f0d03-173">Party contact</span></span>](hr-admin-integration-ats-api-party-contact.md)
- [<span data-ttu-id="f0d03-174">Personferdighet</span><span class="sxs-lookup"><span data-stu-id="f0d03-174">Person skill</span></span>](hr-admin-integration-ats-api-person-skill.md)
- [<span data-ttu-id="f0d03-175">Vurderingsnivå</span><span class="sxs-lookup"><span data-stu-id="f0d03-175">Rating level</span></span>](hr-admin-integration-ats-api-rating-level.md)
- [<span data-ttu-id="f0d03-176">Personsertifikat</span><span class="sxs-lookup"><span data-stu-id="f0d03-176">Person certificate</span></span>](hr-admin-integration-ats-api-person-certificate.md)
- [<span data-ttu-id="f0d03-177">Attesttype</span><span class="sxs-lookup"><span data-stu-id="f0d03-177">Certificate type</span></span>](hr-admin-integration-ats-api-certificate-type.md)
- [<span data-ttu-id="f0d03-178">Personscreening</span><span class="sxs-lookup"><span data-stu-id="f0d03-178">Person screening</span></span>](hr-admin-integration-ats-api-person-screening.md)
- [<span data-ttu-id="f0d03-179">Screeningtyper</span><span class="sxs-lookup"><span data-stu-id="f0d03-179">Screening types</span></span>](hr-admin-integration-ats-api-screening-types.md)
- [<span data-ttu-id="f0d03-180">Personidentifikasjonsnummer</span><span class="sxs-lookup"><span data-stu-id="f0d03-180">Person identification number</span></span>](hr-admin-integration-ats-api-person-identification-number.md)

<span data-ttu-id="f0d03-181">Alternativsett:</span><span class="sxs-lookup"><span data-stu-id="f0d03-181">Option sets:</span></span>

- [<span data-ttu-id="f0d03-182">Søkerintegreringsresultat</span><span class="sxs-lookup"><span data-stu-id="f0d03-182">Applicant integration result</span></span>](hr-admin-integration-ats-api-applicant-integration-result.md)
- [<span data-ttu-id="f0d03-183">Tomt Ja Nei</span><span class="sxs-lookup"><span data-stu-id="f0d03-183">Blank Yes No</span></span>](hr-admin-integration-ats-api-blank-yes-no.md)
- [<span data-ttu-id="f0d03-184">Fullføringsstatus</span><span class="sxs-lookup"><span data-stu-id="f0d03-184">Completion status</span></span>](hr-admin-integration-ats-api-completion-status.md)
- [<span data-ttu-id="f0d03-185">Kontakttype</span><span class="sxs-lookup"><span data-stu-id="f0d03-185">Contact type</span></span>](hr-admin-integration-ats-api-contact-type.md)
- [<span data-ttu-id="f0d03-186">Studiepoenggrunnlag for utdanning</span><span class="sxs-lookup"><span data-stu-id="f0d03-186">Education credit basis</span></span>](hr-admin-integration-ats-api-education-credit-basis.md)
- [<span data-ttu-id="f0d03-187">Kjønn</span><span class="sxs-lookup"><span data-stu-id="f0d03-187">Gender</span></span>](hr-admin-integration-ats-api-gender.md)
- [<span data-ttu-id="f0d03-188">Sivilstand</span><span class="sxs-lookup"><span data-stu-id="f0d03-188">Marital status</span></span>](hr-admin-integration-ats-api-marital-status.md)
- [<span data-ttu-id="f0d03-189">Måneder i året</span><span class="sxs-lookup"><span data-stu-id="f0d03-189">Months of year</span></span>](hr-admin-integration-ats-api-months-of-year.md)
- [<span data-ttu-id="f0d03-190">Nei Ja</span><span class="sxs-lookup"><span data-stu-id="f0d03-190">No Yes</span></span>](hr-admin-integration-ats-api-no-yes.md)
- [<span data-ttu-id="f0d03-191">Periodeenhet</span><span class="sxs-lookup"><span data-stu-id="f0d03-191">Period unit</span></span>](hr-admin-integration-ats-api-period-unit.md)
- [<span data-ttu-id="f0d03-192">Screeningfrekvens</span><span class="sxs-lookup"><span data-stu-id="f0d03-192">Screening frequency</span></span>](hr-admin-integration-ats-api-screening-frequency.md)
- [<span data-ttu-id="f0d03-193">Screeningfrekvens genereres fra</span><span class="sxs-lookup"><span data-stu-id="f0d03-193">Screening frequency generate from</span></span>](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [<span data-ttu-id="f0d03-194">Kompetansenivåtype</span><span class="sxs-lookup"><span data-stu-id="f0d03-194">Skill level type</span></span>](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a><span data-ttu-id="f0d03-195">Se også</span><span class="sxs-lookup"><span data-stu-id="f0d03-195">See also</span></span>

[<span data-ttu-id="f0d03-196">Rekruttere jobbkandidater</span><span class="sxs-lookup"><span data-stu-id="f0d03-196">Recruit job candidates</span></span>](hr-personnel-recruit.md)<br>
[<span data-ttu-id="f0d03-197">Hva er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="f0d03-197">What is Microsoft Dataverse?</span></span>](https://docs.microsoft.com/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="f0d03-198">Bruke Microsoft Dataverse-web-API-en</span><span class="sxs-lookup"><span data-stu-id="f0d03-198">Use the Microsoft Dataverse Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/overview)<br>
[<span data-ttu-id="f0d03-199">Opprette og oppdatere alternativsett ved hjelp av web-API</span><span class="sxs-lookup"><span data-stu-id="f0d03-199">Create and update option sets using the Web API</span></span>](https://docs.microsoft.com/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>