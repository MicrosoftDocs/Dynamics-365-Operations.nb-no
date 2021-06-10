---
title: Innføring i API for lønnsintegrering
description: Dette emnet beskriver API-en for lønnsintegrering i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: e6d8a1cb9619a863184460a74e472af3f06934b6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058566"
---
# <a name="payroll-integration-api-introduction"></a><span data-ttu-id="9b1a9-103">Innføring i API for lønnsintegrering</span><span class="sxs-lookup"><span data-stu-id="9b1a9-103">Payroll integration API introduction</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="9b1a9-104">Dette dokumentet beskriver API-en for lønnsintegrering i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-104">This document describes the Dynamics 365 Human Resources Payroll integration API.</span></span> <span data-ttu-id="9b1a9-105">API-en gjør det mulig å strømlinjeforme ende-til-ende-integrasjoner mellom Human Resources og partnerlønnssystemer.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-105">The API enables streamlined end-to-end integrations between Human Resources and partnering payroll systems.</span></span> <span data-ttu-id="9b1a9-106">Den integrerte opplevelsen begynner i Human Resources med ansattprofilen, lønn og fradrag og bidragsinformasjon.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-106">The integrated experience begins in Human Resources with the employee profile, salary and deduction, and contribution information.</span></span> <span data-ttu-id="9b1a9-107">Når du ansetter en ansatt og angir den nødvendige profilen og lønnsinformasjon i Human Resources, henter lønnssystemet denne informasjonen som skal brukes ved behandling av lønn.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-107">When you hire an employee and enter the required profile and pay information into Human Resources, the payroll system pulls this information to use when processing payroll.</span></span> <span data-ttu-id="9b1a9-108">Eventuelle oppdateringer som gjøres til den ansatte eller lønnsinformasjonen, trekkes også for bruk i senere lønnsutbetalinger.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-108">Any updates made to the employee or pay information are also pulled for use in later pay runs.</span></span>

![Flyten i lønnsintegrering](media/hr-admin-integration-payroll-api-introduction-flow.png)

<span data-ttu-id="9b1a9-110">Human Resources inkluderer følgende komponenter for å aktivere integreringen:</span><span class="sxs-lookup"><span data-stu-id="9b1a9-110">To enable the integration, Human Resources includes the following components:</span></span>

- <span data-ttu-id="9b1a9-111">Funksjonalitet for å merke en ansatt som klar til å betale</span><span class="sxs-lookup"><span data-stu-id="9b1a9-111">Functionality to mark an employee as ready to pay</span></span>
- <span data-ttu-id="9b1a9-112">En integrerings-API som åpner opp den nye funksjonaliteten for integrering av programmer</span><span class="sxs-lookup"><span data-stu-id="9b1a9-112">An integration API opening up the new functionality to integrating applications</span></span>

## <a name="microsoft-dataverse"></a><span data-ttu-id="9b1a9-113">Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="9b1a9-113">Microsoft Dataverse</span></span>

<span data-ttu-id="9b1a9-114">Denne API-en er bygd på Microsoft Dataverse (tidligere kalt Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="9b1a9-114">This API is built on Microsoft Dataverse (formerly Common Data Service).</span></span> <span data-ttu-id="9b1a9-115">All RESTful-samhandling med denne API-en gjøres via web-API-en for Microsoft Dataverse, som bruker OData.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-115">All RESTful interaction with this API is done via the Microsoft Dataverse Web API, which uses OData.</span></span> <span data-ttu-id="9b1a9-116">Denne API-en er et delsett av Dataverse-web-API-en.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-116">This API is a subset of the Dataverse Web API.</span></span> <span data-ttu-id="9b1a9-117">Dataverse-web-API-en definerer egenskaper som godkjenning, SLA-er, parti, samtidighetskontroll og feilhåndtering.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-117">The Dataverse Web API defines characteristics such as authentication, SLAs, batch, concurrency control, and error handling.</span></span>

<span data-ttu-id="9b1a9-118">Hvis du vil ha mer generell informasjon om Microsoft Dataverse-web-API-en, kan du se:</span><span class="sxs-lookup"><span data-stu-id="9b1a9-118">For more general information about the Microsoft Dataverse Web API, see:</span></span>

- [<span data-ttu-id="9b1a9-119">Hva er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="9b1a9-119">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)
- [<span data-ttu-id="9b1a9-120">Bruke Microsoft Dataverse-web-API-en</span><span class="sxs-lookup"><span data-stu-id="9b1a9-120">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)
- [<span data-ttu-id="9b1a9-121">Utviklerveiledning for Microsoft Dataverse</span><span class="sxs-lookup"><span data-stu-id="9b1a9-121">Microsoft Dataverse developer guide</span></span>](/powerapps/developer/data-platform)

<span data-ttu-id="9b1a9-122">Denne dokumentasjonen inneholder detaljer og utviklerveiledning for bruk av Dataverse Web-API, inkludert følgende emner:</span><span class="sxs-lookup"><span data-stu-id="9b1a9-122">This documentation includes details and developer guidance for using the Dataverse Web API, including the following topics:</span></span>

- [<span data-ttu-id="9b1a9-123">Godkjenn til Microsoft Dataverse med nett-API</span><span class="sxs-lookup"><span data-stu-id="9b1a9-123">Authenticate to Microsoft Dataverse with the Web API</span></span>](/powerapps/developer/data-platform/webapi/authenticate-web-api)
- [<span data-ttu-id="9b1a9-124">Utfør operasjoner ved hjelp av nett-API</span><span class="sxs-lookup"><span data-stu-id="9b1a9-124">Perform operations using the Web API</span></span>](/powerapps/developer/data-platform/webapi/perform-operations-web-api)
- [<span data-ttu-id="9b1a9-125">Bruk Postman med nett-API</span><span class="sxs-lookup"><span data-stu-id="9b1a9-125">Use Postman with the Web API</span></span>](/powerapps/developer/data-platform/webapi/use-postman-web-api)
- [<span data-ttu-id="9b1a9-126">Bruk endringssporing til å synkronisere data med eksterne systemer</span><span class="sxs-lookup"><span data-stu-id="9b1a9-126">Use change tracking to synchronize data with external systems</span></span>](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems)

### <a name="virtual-tables-for-human-resources-in-dataverse"></a><span data-ttu-id="9b1a9-127">Virtuelle tabeller for Human Resources i Dataverse</span><span class="sxs-lookup"><span data-stu-id="9b1a9-127">Virtual tables for Human Resources in Dataverse</span></span>

<span data-ttu-id="9b1a9-128">Sluttpunktene for API-en for lønnsintegrering bruker de virtuelle tabellplattformfunksjonene i Microsoft Dataverse.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-128">The endpoints for the Payroll integration API use the virtual table platform capabilities of Microsoft Dataverse.</span></span> <span data-ttu-id="9b1a9-129">Som standard distribueres ikke de virtuelle tabellene og de tilknyttede API-sluttpunktene for Human Resources-miljøene, som gjør det mulig for organisasjoner å fastslå hvilke OData-sluttpunkter som vises for miljøet.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-129">By default, the virtual tables and their associated API endpoints aren't deployed for Human Resources environments, enabling organizations to determine which OData endpoints will be exposed for the environment.</span></span> <span data-ttu-id="9b1a9-130">For å kunne bruke API-en må de virtuelle tabellene for Human Resources-enhetene genereres for miljøet.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-130">To use the API, the virtual tables for the Human Resources entities must be generated for the environment.</span></span>

<span data-ttu-id="9b1a9-131">Hvis du vil ha informasjon om generering av de virtuelle tabellene for API, kan du se [Konfigurere virtuelle Dataverse-tabeller](./hr-admin-integration-common-data-service-virtual-entities.md).</span><span class="sxs-lookup"><span data-stu-id="9b1a9-131">For information on generating the virtual tables for the API, see [Configure Dataverse virtual tables](./hr-admin-integration-common-data-service-virtual-entities.md).</span></span>

## <a name="data-model"></a><span data-ttu-id="9b1a9-132">Datamodell</span><span class="sxs-lookup"><span data-stu-id="9b1a9-132">Data model</span></span>

<span data-ttu-id="9b1a9-133">Diagrammet nedenfor illustrerer relasjonen med API-en.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-133">The following diagram illustrates relationships within the API.</span></span> <span data-ttu-id="9b1a9-134">Flere typer har sekundærnøkler til andre, eksisterende enheter i Human Resources som ikke illustreres her.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-134">Several types have foreign keys to other, pre-existing entities in Human Resources that aren't illustrated here.</span></span> <span data-ttu-id="9b1a9-135">Dette dokumentet inneholder informasjon om enheter som er spesifikke for lønnsintegrasjonsscenarier.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-135">This document provides information on entities that are specific to payroll integration scenarios.</span></span> <span data-ttu-id="9b1a9-136">Det er imidlertid mange andre enheter i Dataverse Web-API for Human Resources som også kan være relevante for integreringen.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-136">However, there are many other entities in the Dataverse Web API for Human Resources that may also be relevant to your integration.</span></span> <span data-ttu-id="9b1a9-137">Enkelte av disse enhetene refereres til i sekundærnøkkelrelasjoner eller navigasjonsegenskaper.</span><span class="sxs-lookup"><span data-stu-id="9b1a9-137">Some of these entities are referenced in foreign key relationships or navigation properties.</span></span>

![Lønnsintegrering, API-datamodell](media/hr-admin-payroll-api-data-model.png)

## <a name="payroll-employee-and-related-entities"></a><span data-ttu-id="9b1a9-139">Lønnsansatt og relaterte enheter</span><span class="sxs-lookup"><span data-stu-id="9b1a9-139">Payroll employee and related entities</span></span>

<span data-ttu-id="9b1a9-140">Enheter:</span><span class="sxs-lookup"><span data-stu-id="9b1a9-140">Entities:</span></span>

- [<span data-ttu-id="9b1a9-141">Lønnsansatt</span><span class="sxs-lookup"><span data-stu-id="9b1a9-141">Payroll employee</span></span>](hr-admin-integration-payroll-api-payroll-employee.md)
- [<span data-ttu-id="9b1a9-142">Adresse til lønnsarbeider</span><span class="sxs-lookup"><span data-stu-id="9b1a9-142">Payroll worker address</span></span>](hr-admin-integration-payroll-api-payroll-worker-address.md)
- [<span data-ttu-id="9b1a9-143">Fast kompensasjonsplan for lønn</span><span class="sxs-lookup"><span data-stu-id="9b1a9-143">Payroll fixed compensation plan</span></span>](hr-admin-integration-ats-api-recruiting-request-education.md)
- [<span data-ttu-id="9b1a9-144">Lønnsstillingsjobb</span><span class="sxs-lookup"><span data-stu-id="9b1a9-144">Payroll position job</span></span>](hr-admin-integration-payroll-api-payroll-position-job.md)
- [<span data-ttu-id="9b1a9-145">Lønnsstilling</span><span class="sxs-lookup"><span data-stu-id="9b1a9-145">Payroll position</span></span>](hr-admin-integration-payroll-api-payroll-position.md)

## <a name="see-also"></a><span data-ttu-id="9b1a9-146">Se også</span><span class="sxs-lookup"><span data-stu-id="9b1a9-146">See also</span></span>

[<span data-ttu-id="9b1a9-147">Generer og gå gjennom lønnsenheter</span><span class="sxs-lookup"><span data-stu-id="9b1a9-147">Generate and review payroll entities</span></span>](hr-admin-integration-payroll-api-generate-review-entities.md)<br>
[<span data-ttu-id="9b1a9-148">Konfigurere parametere for Human Resources</span><span class="sxs-lookup"><span data-stu-id="9b1a9-148">Configure Human Resources parameters</span></span>](hr-setup-parameters.md)<br>
[<span data-ttu-id="9b1a9-149">Konfigurere delte parametere for Human Resources</span><span class="sxs-lookup"><span data-stu-id="9b1a9-149">Configure Human Resources shared parameters</span></span>](hr-setup-shared-parameters.md)<br>
[<span data-ttu-id="9b1a9-150">Hva er Microsoft Dataverse?</span><span class="sxs-lookup"><span data-stu-id="9b1a9-150">What is Microsoft Dataverse?</span></span>](/powerapps/maker/data-platform/data-platform-intro)<br>
[<span data-ttu-id="9b1a9-151">Bruke Microsoft Dataverse-web-API-en</span><span class="sxs-lookup"><span data-stu-id="9b1a9-151">Use the Microsoft Dataverse Web API</span></span>](/powerapps/developer/data-platform/webapi/overview)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]