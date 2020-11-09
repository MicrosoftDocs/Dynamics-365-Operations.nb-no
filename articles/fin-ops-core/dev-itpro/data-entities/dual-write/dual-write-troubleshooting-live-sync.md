---
title: Feilsøke problemer med direkte synkronisering
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer med direkte synkronisering.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
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
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 82bdcc71196c22689cc65601f98187aaa9e5e9d6
ms.sourcegitcommit: 0a741b131ed71f6345d4219a47cf5f71fec6744b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "3997308"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="3c7e2-103">Feilsøke problemer med direkte synkronisering</span><span class="sxs-lookup"><span data-stu-id="3c7e2-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="3c7e2-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="3c7e2-105">Det inneholder særlig informasjon som kan hjelpe deg med å løse problemer med direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c7e2-106">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="3c7e2-107">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="3c7e2-108">Direkte synkronisering genererer en 403 forbudt-feil når du oppretter en post i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="3c7e2-108">Live synchronization throws a 403 Forbidden error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="3c7e2-109">Du kan få følgende feilmelding når du oppretter en post i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="3c7e2-109">You might receive the following error message when you create a record in a Finance and Operations app:</span></span>

<span data-ttu-id="3c7e2-110">*\[{\\"feil\\":{\\"kode\\":\\"0x80072560\\",\\"melding\\":\\"Brukeren er ikke medlem av organisasjonen.\\"}}\], Den eksterne serveren returnerte en feil: (403) Forbudt."}}".*</span><span class="sxs-lookup"><span data-stu-id="3c7e2-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="3c7e2-111">Hvis du vil løse problemet, følger du fremgangsmåten under [Systemkrav og forutsetninger](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="3c7e2-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="3c7e2-112">Hvis du vil fullføre disse trinnene, må brukerne avdobbel skriving-programmet som er opprettet i Common Data Service, ha rollen som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-112">To complete those steps, the dual-write application users who are created in Common Data Service must have the system admin role.</span></span> <span data-ttu-id="3c7e2-113">Standard eiende team må også ha rollen som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="3c7e2-114">Direkte synkronisering for alle enheter gir konsekvent en lignende feil når du oppretter en post i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="3c7e2-114">Live synchronization for any entity consistently throws a similar error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="3c7e2-115">**Nødvendig rolle for å løse problemet:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="3c7e2-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="3c7e2-116">Du kan få en feilmelding som nedenfor hver gang du prøver å lagre enhetsdata i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="3c7e2-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="3c7e2-117">*Kan ikke lagre endringene i databasen. Arbeidsenhet kan ikke utføre transaksjonen. Kan ikke skrive data til måleenheter. Skriving til UnitOfMeasureEntity mislyktes med feilmeldingen Kan ikke synkronisere med måleenheter.*</span><span class="sxs-lookup"><span data-stu-id="3c7e2-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="3c7e2-118">Hvis du vil løse problemet, må du kontrollere at de nødvendige referansedataene finnes i både Finance and Operations-appen og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Common Data Service.</span></span> <span data-ttu-id="3c7e2-119">Hvis for eksempel kunden som du er i Finance and Operations-appen, tilhører en bestemt kundegruppe, må du kontrollere at kundegruppen finnes i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Common Data Service.</span></span>

<span data-ttu-id="3c7e2-120">Hvis det finnes data på begge sider, og du har bekreftet at problemet ikke er relatert til data, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="3c7e2-121">Stopp den tilknyttede enheten.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-121">Stop the related entity.</span></span>
2. <span data-ttu-id="3c7e2-122">Logg deg på Finance and Operations-appen, og kontroller at det finnes poster for enheten som ikke fungerer, i DualWriteProjectConfiguration- og DualWriteProjectFieldConfiguration-tabellen.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-122">Sign in to the Finance and Operations app, and make sure that records for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="3c7e2-123">Spørringen ser for eksempel slik ut som hvis **Kundenr** -enheten mislykkes.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="3c7e2-124">Hvis det finnes poster for enheten som mislyktes, selv etter at du har stoppet enhetstilordningen, sletter du postene som er relatert til enheten som ikke fungerer.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-124">If there are records for the failing entity even after you stop the entity mapping, delete the records that are related to the failing entity.</span></span> <span data-ttu-id="3c7e2-125">Noter deg **projectname** -kolonnen i DualWriteProjectConfiguration-tabellen, og hent posten i DualWriteProjectFieldConfiguration-tabellen ved hjelp av prosjektnavnet for å slette posten.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the record.</span></span>
4. <span data-ttu-id="3c7e2-126">Start enhetstilordningen.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-126">Start the entity mapping.</span></span> <span data-ttu-id="3c7e2-127">Valider om dataene er synkronisert uten problemer.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="3c7e2-128">Håndtere lese- eller skrivetilgangsfeil når du oppretter data i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="3c7e2-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="3c7e2-129">Du kan få en feilmelding av typen "Ugyldig forespørsel" som ligner på følgende eksempel når du oppretter data i en Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Eksempel på feilmeldingen om Ugyldig forespørsel](media/error_record_id_source.png)

<span data-ttu-id="3c7e2-131">Hvis du vil løse problemet, må du tilordne den riktige sikkerhetsrollen til teamet for den tilordnede forretningsenheten for Dynamics 365 Sales eller Dynamics 365 Customer Service for å aktivere den manglende rettigheten.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="3c7e2-132">I Finance and Operations-appen finner du forretningsenheten som er tilordnet i tilkoblingssettet for dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organisasjonstilordning](media/mapped_business_unit.png)

2. <span data-ttu-id="3c7e2-134">Logg deg på miljøet i den modelldrevne appen i Dynamics 365, naviger til **Innstilling \> Sikkerhet** , og finn teamet til den tilordnede forretningsenheten.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security** , and find the team of the mapped business unit.</span></span>

    ![Team til den tilordnede forretningsenheten](media/setting_security_page.png)

3. <span data-ttu-id="3c7e2-136">Åpne siden for teamet for redigering, og velg deretter **Behandle roller** for å åpne dialogboksen **Administrere teamroller**.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Knappen Behandle roller](media/manage_team_roles.png)

4. <span data-ttu-id="3c7e2-138">Tilordne rollen med lese/skrivetilgang for de relevante enhetene, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-138">Assign the role that has the read/write privilege for the relevant entities, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a><span data-ttu-id="3c7e2-139">Rette opp synkroniseringsproblemer i et miljø som har et nylig endret Common Data Service-miljø</span><span class="sxs-lookup"><span data-stu-id="3c7e2-139">Fix synchronization issues in an environment that has a recently changed Common Data Service environment</span></span>

<span data-ttu-id="3c7e2-140">**Nødvendig rolle for å løse problemet:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="3c7e2-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="3c7e2-141">Du kan få følgende feilmelding når du oppretter data i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="3c7e2-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="3c7e2-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":" **Kan ikke generere nyttelast for enhet CustCustomerV3Entity** ","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Oppretting av nyttelast mislyktes med feilen Ugyldig URI: URI-en er tom."}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="3c7e2-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":" **Unable to generate payload for entity CustCustomerV3Entity** ","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="3c7e2-143">Slik ser feilen ut i den modelldrevne appen i Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="3c7e2-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="3c7e2-144">*Det oppstod en uventet feil fra ISV-kode. (ErrorType = ClientError) Uventet unntak fra plugin-modul (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: kan ikke behandle enhetskonto - Et tilkoblingsforsøk mislyktes fordi den tilkoblede parten ikke svarte riktig etter en tidsperiode, eller opprettet tilkobling mislyktes fordi den tilkoblede verten ikke svarer*</span><span class="sxs-lookup"><span data-stu-id="3c7e2-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="3c7e2-145">Denne feilen oppstår når Common Data Service-miljøet tilbakestilles feil samtidig som du prøver å opprette data i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-145">This error occurs when the Common Data Service environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="3c7e2-146">Følg fremgangsmåten nedenfor for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="3c7e2-147">Logg på den virtuelle maskinen Finance and Operations, åpne SQL Server Management Studio (SSMS), og se etter poster i DUALWRITEPROJECTCONFIGURATIONENTITY-tabellen der **internalentityname** er lik **Kunder V3** og **externalentityname** er lik **kontoer**.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for records in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="3c7e2-148">Spørringen ser slik ut.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="3c7e2-149">Bruk prosjektnavnet fra resultatene fra den forrige spørringen til å kjøre følgende spørring.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="3c7e2-150">Kontroller at **externalenvironmentURL** -kolonnen har riktig Common Data Service- eller app-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-150">Make sure that the **externalenvironmentURL** column has the correct Common Data Service or app URL.</span></span> <span data-ttu-id="3c7e2-151">Slett eventuelle duplikate poster som peker til feil Common Data Service-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-151">Delete any duplicate records that point to the wrong Common Data Service URL.</span></span> <span data-ttu-id="3c7e2-152">Slett de tilsvarende postene i DUALWRITEPROJECTFIELDCONFIGURATION- og DUALWRITEPROJECTCONFIGURATION-tabellen.</span><span class="sxs-lookup"><span data-stu-id="3c7e2-152">Delete the corresponding records in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="3c7e2-153">Stopp enhetstilordningen, og start den deretter på nytt</span><span class="sxs-lookup"><span data-stu-id="3c7e2-153">Stop the entity mapping, and then restart it</span></span>
