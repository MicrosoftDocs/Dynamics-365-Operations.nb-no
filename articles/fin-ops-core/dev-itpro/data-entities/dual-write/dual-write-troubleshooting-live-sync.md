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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 60839bbd1b3ae642cdd419c7df2388292776a461
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172743"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Feilsøke problemer med direkte synkronisering

[!include [banner](../../includes/banner.md)]



Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service. Det inneholder særlig informasjon som kan hjelpe deg med å løse problemer med direkte synkronisering.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Direkte synkronisering genererer en 403 forbudt-feil når du oppretter en post i en Finance and Operations-app

Du kan få følgende feilmelding når du oppretter en post i en Finance and Operations-app:

*\[{\\"feil\\":{\\"kode\\":\\"0x80072560\\",\\"melding\\":\\"Brukeren er ikke medlem av organisasjonen.\\"}}\], Den eksterne serveren returnerte en feil: (403) Forbudt."}}".*

Hvis du vil løse problemet, følger du fremgangsmåten under [Systemkrav og forutsetninger](requirements-and-prerequisites.md). Hvis du vil fullføre disse trinnene, må brukerne avdobbel skriving-programmet som er opprettet i Common Data Service, ha rollen som systemadministrator. Standard eiende team må også ha rollen som systemadministrator.

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a>Direkte synkronisering for alle enheter gir konsekvent en lignende feil når du oppretter en post i en Finance and Operations-app

**Nødvendig rolle for å løse problemet:** Systemadministrator

Du kan få en feilmelding som nedenfor hver gang du prøver å lagre enhetsdata i en Finance and Operations-app:

*Kan ikke lagre endringene i databasen. Arbeidsenhet kan ikke utføre transaksjonen. Kan ikke skrive data til måleenheter. Skriving til UnitOfMeasureEntity mislyktes med feilmeldingen Kan ikke synkronisere med måleenheter.*

Hvis du vil løse problemet, må du kontrollere at de nødvendige referansedataene finnes i både Finance and Operations-appen og Common Data Service. Hvis for eksempel kunden som du er i Finance and Operations-appen, tilhører en bestemt kundegruppe, må du kontrollere at kundegruppen finnes i Common Data Service.

Hvis det finnes data på begge sider, og du har bekreftet at problemet ikke er relatert til data, følger du denne fremgangsmåten.

1. Stopp den tilknyttede enheten.
2. Logg deg på Finance and Operations-appen, og kontroller at det finnes poster for enheten som ikke fungerer, i DualWriteProjectConfiguration- og DualWriteProjectFieldConfiguration-tabellen. Spørringen ser for eksempel slik ut som hvis **Kundenr**-enheten mislykkes.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Hvis det finnes poster for enheten som mislyktes, selv etter at du har stoppet enhetstilordningen, sletter du postene som er relatert til enheten som ikke fungerer. Noter deg **projectname**-kolonnen i DualWriteProjectConfiguration-tabellen, og hent posten i DualWriteProjectFieldConfiguration-tabellen ved hjelp av prosjektnavnet for å slette posten.
4. Start enhetstilordningen. Valider om dataene er synkronisert uten problemer.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Håndtere lese- eller skrivetilgangsfeil når du oppretter data i en Finance and Operations-app

Du kan få en feilmelding av typen "Ugyldig forespørsel" som ligner på følgende eksempel når du oppretter data i en Finance and Operations-app.

![Eksempel på feilmeldingen om Ugyldig forespørsel](media/error_record_id_source.png)

Hvis du vil løse problemet, må du tilordne den riktige sikkerhetsrollen til teamet for den tilordnede forretningsenheten for Dynamics 365 Sales eller Dynamics 365 Customer Service for å aktivere den manglende rettigheten.

1. I Finance and Operations-appen finner du forretningsenheten som er tilordnet i tilkoblingssettet for dataintegrering.

    ![Organisasjonstilordning](media/mapped_business_unit.png)

2. Logg deg på miljøet i den modelldrevne appen i Dynamics 365, naviger til **Innstilling \> Sikkerhet**, og finn teamet til den tilordnede forretningsenheten.

    ![Team til den tilordnede forretningsenheten](media/setting_security_page.png)

3. Åpne siden for teamet for redigering, og velg deretter **Behandle roller** for å åpne dialogboksen **Administrere teamroller**.

    ![Knappen Behandle roller](media/manage_team_roles.png)

4. Tilordne rollen med lese/skrivetilgang for de relevante enhetene, og velg deretter **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a>Rette opp synkroniseringsproblemer i et miljø som har et nylig endret Common Data Service-miljø

**Nødvendig rolle for å løse problemet:** Systemadministrator

Du kan få følgende feilmelding når du oppretter data i en Finance and Operations-app:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Kan ikke generere nyttelast for enhet CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Oppretting av nyttelast mislyktes med feilen Ugyldig URI: URI-en er tom."}\],"isErrorCountUpdated":true}*

Slik ser feilen ut i den modelldrevne appen i Dynamics 365:

*Det oppstod en uventet feil fra ISV-kode. (ErrorType = ClientError) Uventet unntak fra plugin-modul (Execute): Microsoft.Dynamics.Integrator.CrmPlugins.Plugin: System.Exception: kan ikke behandle enhetskonto - Et tilkoblingsforsøk mislyktes fordi den tilkoblede parten ikke svarte riktig etter en tidsperiode, eller opprettet tilkobling mislyktes fordi den tilkoblede verten ikke svarer*

Denne feilen oppstår når Common Data Service-miljøet tilbakestilles feil samtidig som du prøver å opprette data i Finance and Operations-appen.

Følg fremgangsmåten nedenfor for å løse problemet.

1. Logg på den virtuelle maskinen Finance and Operations, åpne SQL Server Management Studio (SSMS), og se etter poster i DUALWRITEPROJECTCONFIGURATIONENTITY-tabellen der **internalentityname** er lik **Kunder V3** og **externalentityname** er lik **kontoer**. Spørringen ser slik ut.

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. Bruk prosjektnavnet fra resultatene fra den forrige spørringen til å kjøre følgende spørring.

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. Kontroller at **externalenvironmentURL**-kolonnen har riktig Common Data Service- eller app-URL-adresse. Slett eventuelle duplikate poster som peker til feil Common Data Service-URL-adresse. Slett de tilsvarende postene i DUALWRITEPROJECTFIELDCONFIGURATION- og DUALWRITEPROJECTCONFIGURATION-tabellen.
4. Stopp enhetstilordningen, og start den deretter på nytt
