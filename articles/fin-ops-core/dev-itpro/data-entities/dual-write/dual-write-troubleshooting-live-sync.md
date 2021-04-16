---
title: Feilsøke problemer med direkte synkronisering
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer med direkte synkronisering.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1c0dfebb3ef442f67d8489d7aed00305c02cf410
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748903"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="5e5c8-103">Feilsøke problemer med direkte synkronisering</span><span class="sxs-lookup"><span data-stu-id="5e5c8-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="5e5c8-104">Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="5e5c8-105">Det inneholder særlig informasjon som kan hjelpe deg med å løse problemer med direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="5e5c8-106">Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="5e5c8-107">Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="5e5c8-108">Direkte synkronisering genererer en 403 forbudt-feil når du oppretter en rad i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="5e5c8-108">Live synchronization throws a 403 Forbidden error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="5e5c8-109">Du kan få følgende feilmelding når du oppretter en rad i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="5e5c8-109">You might receive the following error message when you create a row in a Finance and Operations app:</span></span>

<span data-ttu-id="5e5c8-110">*\[{\\"feil\\":{\\"kode\\":\\"0x80072560\\",\\"melding\\":\\"Brukeren er ikke medlem av organisasjonen.\\"}}\], Den eksterne serveren returnerte en feil: (403) Forbudt."}}".*</span><span class="sxs-lookup"><span data-stu-id="5e5c8-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="5e5c8-111">Hvis du vil løse problemet, følger du fremgangsmåten under [Systemkrav og forutsetninger](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="5e5c8-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="5e5c8-112">Hvis du vil fullføre disse trinnene, må brukerne avdobbel skriving-programmet som er opprettet i Dataverse, ha rollen som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-112">To complete those steps, the dual-write application users who are created in Dataverse must have the system admin role.</span></span> <span data-ttu-id="5e5c8-113">Standard eiende team må også ha rollen som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="5e5c8-114">Direkte synkronisering for alle tabeller gir konsekvent en lignende feil når du oppretter en rad i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="5e5c8-114">Live synchronization for any table consistently throws a similar error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="5e5c8-115">**Nødvendig rolle for å løse problemet:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="5e5c8-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="5e5c8-116">Du kan få en feilmelding som nedenfor hver gang du prøver å lagre tabelldata i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="5e5c8-116">You might receive an error message like the following every time that you try to save table data in a Finance and Operations app:</span></span>

<span data-ttu-id="5e5c8-117">*Kan ikke lagre endringene i databasen. Arbeidsenhet kan ikke utføre transaksjonen. Kan ikke skrive data til måleenheter. Skriving til UnitOfMeasureEntity mislyktes med feilmeldingen Kan ikke synkronisere med måleenheter.*</span><span class="sxs-lookup"><span data-stu-id="5e5c8-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="5e5c8-118">Hvis du vil løse problemet, må du kontrollere at de nødvendige referansedataene finnes i både Finance and Operations-appen og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Dataverse.</span></span> <span data-ttu-id="5e5c8-119">Hvis for eksempel kunden som du er i Finance and Operations-appen, tilhører en bestemt kundegruppe, må du kontrollere at kundegruppen finnes i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Dataverse.</span></span>

<span data-ttu-id="5e5c8-120">Hvis det finnes data på begge sider, og du har bekreftet at problemet ikke er relatert til data, følger du denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="5e5c8-121">Stopp den tilknyttede tabellen.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-121">Stop the related table.</span></span>
2. <span data-ttu-id="5e5c8-122">Logg deg på Finance and Operations-appen, og kontroller at det finnes rader for tabellen som ikke fungerer, i tabellene DualWriteProjectConfiguration og DualWriteProjectFieldConfiguration.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-122">Sign in to the Finance and Operations app, and make sure that rows for the failing table exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="5e5c8-123">Spørringen ser for eksempel slik ut som hvis **Kunder**-tabellen mislykkes.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-123">For example, here is what the query looks like if the **Customers** table is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="5e5c8-124">Hvis det finnes rader for tabellen som mislyktes, selv etter at du har stoppet tabelltilordningen, sletter du radene som er knyttet til tabellen som ikke fungerer.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-124">If there are rows for the failing table even after you stop the table mapping, delete the rows that are related to the failing table.</span></span> <span data-ttu-id="5e5c8-125">Noter deg **projectname**-kolonnen i tabellen DualWriteProjectConfiguration, og hent raden i tabellen DualWriteProjectFieldConfiguration ved hjelp av prosjektnavnet for å slette raden.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the row in the DualWriteProjectFieldConfiguration table by using the project name to delete the row.</span></span>
4. <span data-ttu-id="5e5c8-126">Start tabelltilordningen.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-126">Start the table mapping.</span></span> <span data-ttu-id="5e5c8-127">Valider om dataene er synkronisert uten problemer.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="5e5c8-128">Håndtere lese- eller skrivetilgangsfeil når du oppretter data i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="5e5c8-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="5e5c8-129">Du kan få en feilmelding av typen "Ugyldig forespørsel" som ligner på følgende eksempel når du oppretter data i en Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Eksempel på feilmeldingen om Ugyldig forespørsel](media/error_record_id_source.png)

<span data-ttu-id="5e5c8-131">Hvis du vil løse problemet, må du tilordne den riktige sikkerhetsrollen til teamet for den tilordnede forretningsenheten for Dynamics 365 Sales eller Dynamics 365 Customer Service for å aktivere den manglende rettigheten.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="5e5c8-132">I Finance and Operations-appen finner du forretningsenheten som er tilordnet i tilkoblingssettet for dataintegrering.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organisasjonstilordning](media/mapped_business_unit.png)

2. <span data-ttu-id="5e5c8-134">Logg deg på miljøet i den modelldrevne appen i Dynamics 365, naviger til **Innstilling \> Sikkerhet**, og finn teamet til den tilordnede forretningsenheten.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Team til den tilordnede forretningsenheten](media/setting_security_page.png)

3. <span data-ttu-id="5e5c8-136">Åpne siden for teamet for redigering, og velg deretter **Behandle roller** for å åpne dialogboksen **Administrere teamroller**.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Knappen Behandle roller](media/manage_team_roles.png)

4. <span data-ttu-id="5e5c8-138">Tilordne rollen med lese/skrivetilgang for de relevante tabellene, og velg deretter **OK**.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-138">Assign the role that has the read/write privilege for the relevant tables, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a><span data-ttu-id="5e5c8-139">Rette opp synkroniseringsproblemer i et miljø som har et nylig endret Dataverse-miljø</span><span class="sxs-lookup"><span data-stu-id="5e5c8-139">Fix synchronization issues in an environment that has a recently changed Dataverse environment</span></span>

<span data-ttu-id="5e5c8-140">**Nødvendig rolle for å løse problemet:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="5e5c8-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="5e5c8-141">Du kan få følgende feilmelding når du oppretter data i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="5e5c8-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="5e5c8-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Kan ikke generere nyttelast for enhet CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Oppretting av nyttelast mislyktes med feilen Ugyldig URI: URI-en er tom."}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="5e5c8-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="5e5c8-143">Slik ser feilen ut i den modelldrevne appen i Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="5e5c8-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="5e5c8-144">*Det oppstod en uventet feil fra ISV-kode. (ErrorType = ClientError) Uventet unntak fra plugin-modul (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: kan ikke behandle enhetskonto - Et tilkoblingsforsøk mislyktes fordi den tilkoblede parten ikke svarte riktig etter en tidsperiode, eller opprettet tilkobling mislyktes fordi den tilkoblede verten ikke svarer*</span><span class="sxs-lookup"><span data-stu-id="5e5c8-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="5e5c8-145">Denne feilen oppstår når Dataverse-miljøet tilbakestilles feil samtidig som du prøver å opprette data i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-145">This error occurs when the Dataverse environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="5e5c8-146">Følg fremgangsmåten nedenfor for å løse problemet.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="5e5c8-147">Logg på den virtuelle maskinen Finance and Operations, åpne SQL Server Management Studio (SSMS), og se etter rader i DUALWRITEPROJECTCONFIGURATIONENTITY-tabellen der **internalentityname** er lik **Kunder V3** og **externalentityname** er lik **kontoer**.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for rows in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="5e5c8-148">Spørringen ser slik ut.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="5e5c8-149">Bruk prosjektnavnet fra resultatene fra den forrige spørringen til å kjøre følgende spørring.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="5e5c8-150">Kontroller at **externalenvironmentURL**-kolonnen har riktig Dataverse- eller app-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-150">Make sure that the **externalenvironmentURL** column has the correct Dataverse or app URL.</span></span> <span data-ttu-id="5e5c8-151">Slett eventuelle duplikate rader som peker til feil Dataverse-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-151">Delete any duplicate rows that point to the wrong Dataverse URL.</span></span> <span data-ttu-id="5e5c8-152">Slett de tilsvarende radene i DUALWRITEPROJECTFIELDCONFIGURATION- og DUALWRITEPROJECTCONFIGURATION-tabellen.</span><span class="sxs-lookup"><span data-stu-id="5e5c8-152">Delete the corresponding rows in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="5e5c8-153">Stopp tabelltilordningen, og start den deretter på nytt</span><span class="sxs-lookup"><span data-stu-id="5e5c8-153">Stop the table mapping, and then restart it</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]