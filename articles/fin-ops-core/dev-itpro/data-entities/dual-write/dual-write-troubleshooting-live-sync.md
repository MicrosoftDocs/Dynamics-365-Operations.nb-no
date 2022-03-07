---
title: Feilsøke problemer med direkte synkronisering
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer med direkte synkronisering.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 2dbb32647e362df05d28bbd7d845e0e4f776d8c9
ms.sourcegitcommit: 259ba130450d8a6d93a65685c22c7eb411982c92
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/24/2021
ms.locfileid: "7416711"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Feilsøke problemer med direkte synkronisering

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse. Det inneholder særlig informasjon som kan hjelpe deg med å løse problemer med direkte synkronisering.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Direkte synkronisering genererer en 403 forbudt-feil når du oppretter en rad i en Finance and Operations-app

Du kan få følgende feilmelding når du oppretter en rad i en Finance and Operations-app:

*\[{\\"feil\\":{\\"kode\\":\\"0x80072560\\",\\"melding\\":\\"Brukeren er ikke medlem av organisasjonen.\\"}}\], Den eksterne serveren returnerte en feil: (403) Forbudt."}}".*

Hvis du vil løse problemet, følger du fremgangsmåten under [Systemkrav og forutsetninger](requirements-and-prerequisites.md). Hvis du vil fullføre disse trinnene, må brukerne avdobbel skriving-programmet som er opprettet i Dataverse, ha rollen som systemadministrator. Standard eiende team må også ha rollen som systemadministrator.

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Direkte synkronisering for alle tabeller gir konsekvent en lignende feil når du oppretter en rad i en Finance and Operations-app

**Nødvendig rolle for å løse problemet:** Systemadministrator

Du kan få en feilmelding som nedenfor hver gang du prøver å lagre tabelldata i en Finance and Operations-app:

*Kan ikke lagre endringene i databasen. Arbeidsenhet kan ikke utføre transaksjonen. Kan ikke skrive data til måleenheter. Skriving til UnitOfMeasureEntity mislyktes med feilmeldingen Kan ikke synkronisere med måleenheter.*

Hvis du vil løse problemet, må du kontrollere at de nødvendige referansedataene finnes i både Finance and Operations-appen og Dataverse. Hvis for eksempel kunden som du er i Finance and Operations-appen, tilhører en bestemt kundegruppe, må du kontrollere at kundegruppen finnes i Dataverse.

Hvis det finnes data på begge sider, og du har bekreftet at problemet ikke er relatert til data, følger du denne fremgangsmåten.

1. Stopp den tilknyttede tabellen.
2. Logg deg på Finance and Operations-appen, og kontroller at det finnes rader for tabellen som ikke fungerer, i tabellene DualWriteProjectConfiguration og DualWriteProjectFieldConfiguration. Spørringen ser for eksempel slik ut som hvis **Kunder**-tabellen mislykkes.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Hvis det finnes rader for tabellen som mislyktes, selv etter at du har stoppet tabelltilordningen, sletter du radene som er knyttet til tabellen som ikke fungerer. Noter deg **projectname**-kolonnen i tabellen DualWriteProjectConfiguration, og hent raden i tabellen DualWriteProjectFieldConfiguration ved hjelp av prosjektnavnet for å slette raden.
4. Start tabelltilordningen. Valider om dataene er synkronisert uten problemer.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Håndtere lese- eller skrivetilgangsfeil når du oppretter data i en Finance and Operations-app

Du kan få en feilmelding av typen "Ugyldig forespørsel" som ligner på følgende eksempel når du oppretter data i en Finance and Operations-app.

![Eksempel på feilmeldingen om Ugyldig forespørsel.](media/error_record_id_source.png)

Hvis du vil løse problemet, må du tilordne den riktige sikkerhetsrollen til teamet for den tilordnede forretningsenheten for Dynamics 365 Sales eller Dynamics 365 Customer Service for å aktivere den manglende rettigheten.

1. I Finance and Operations-appen finner du forretningsenheten som er tilordnet i tilkoblingssettet for dataintegrering.

    ![Organisasjonstilordning.](media/mapped_business_unit.png)

2. Logg deg på miljøet i kundeengasjementsappen, naviger til **Innstilling \> Sikkerhet**, og finn teamet til den tilordnede forretningsenheten.

    ![Team til den tilordnede forretningsenheten.](media/setting_security_page.png)

3. Åpne siden for teamet for redigering, og velg deretter **Behandle roller** for å åpne dialogboksen **Administrere teamroller**.

    ![Knappen Behandle roller.](media/manage_team_roles.png)

4. Tilordne rollen med lese/skrivetilgang for de relevante tabellene, og velg deretter **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Rette opp synkroniseringsproblemer i et miljø som har et nylig endret Dataverse-miljø

**Nødvendig rolle for å løse problemet:** Systemadministrator

Du kan få følgende feilmelding når du oppretter data i en Finance and Operations-app:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Kan ikke generere nyttelast for enhet CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Oppretting av nyttelast mislyktes med feilen Ugyldig URI: URI-en er tom."}\],"isErrorCountUpdated":true}*

Slik ser feilen ut i kundeengasjementsappen:

*Det oppstod en uventet feil fra ISV-kode. (ErrorType = ClientError) Uventet unntak fra plugin-modul (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: kan ikke behandle enhetskonto - Et tilkoblingsforsøk mislyktes fordi den tilkoblede parten ikke svarte riktig etter en tidsperiode, eller opprettet tilkobling mislyktes fordi den tilkoblede verten ikke svarer*

Denne feilen oppstår når Dataverse-miljøet tilbakestilles feil samtidig som du prøver å opprette data i Finance and Operations-appen.

Følg fremgangsmåten nedenfor for å løse problemet.

1. Logg på den virtuelle maskinen Finance and Operations, åpne SQL Server Management Studio (SSMS), og se etter rader i DUALWRITEPROJECTCONFIGURATIONENTITY-tabellen der **internalentityname** er lik **Kunder V3** og **externalentityname** er lik **kontoer**. Spørringen ser slik ut.

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

3. Kontroller at **externalenvironmentURL**-kolonnen har riktig Dataverse- eller app-URL-adresse. Slett eventuelle duplikate rader som peker til feil Dataverse-URL-adresse. Slett de tilsvarende radene i DUALWRITEPROJECTFIELDCONFIGURATION- og DUALWRITEPROJECTCONFIGURATION-tabellen.
4. Stopp tabelltilordningen, og start den deretter på nytt

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
