---
title: Kopier en forekomst
description: Du kan bruke Microsoft Dynamics Lifecycle Services (LCS) til å kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkassemiljø.
author: twheeloc
ms.date: 07/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 20a2ffb44f9b99800146e3365e6f0d6df8e9a75e
ms.sourcegitcommit: 66d129874635d34a8b29c57762ecf1564e4dc233
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9324268"
---
# <a name="copy-an-instance"></a>Kopier en forekomst

_**Gjelder For:** Human Resources i den frittstående infrastrukturen_ 

> [!NOTE]
> Fra og med juni 2022 kan Human Resources-miljøer kun distribueres i infrastrukturen i økonomi- og driftsapper. Hvis du vil ha mer informasjon , kan du se [Klargjøring av Human Resources i infrastrukturen i Finance and Operations](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Infrastrukturen for Finance and Operations støtter ikke en kopieringsforekomstfunksjon. Du kan distribuere nye miljøer og bruke databasebevegelser til å opprette kopier. For mer informasjon om selvbetjenste distribusjoner kan du se [Oversikt over distribusjon av selvbetjening](../fin-ops-core/dev-itpro/deployment/infrastructure-stack.md). Hvis du vil ha mer informasjon om databasebevegelser i Finance and Operations-infrastrukturen, kan du se [Startsiden for databaseflyttingsoperasjoner](../fin-ops-core/dev-itpro/database/dbmovement-operations.md).

Du kan bruke Microsoft Dynamics Lifecycle Services (LCS) til å kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkassemiljø. Hvis du har et annet sandkassemiljø, kan du også kopiere databasen fra dette miljøet til et målrettet sandkassemiljø.

Hvis du vil kopiere en forekomst, må du tenke på følgende tips:

- Forekomsten av Human Resources som du vil overskrive, må være et sandkassemiljø.

- Miljøene du kopierer fra og til, må være i samme område. Du kan ikke kopiere på tvers av områder.

- Du må være administrator i målmiljøet, slik at du kan logge på det etter at du har kopiert forekomsten.

- Når du kopierer Human Resources-databasen, kopierer du ikke elementene (apper eller data) som finnes i et Microsoft Power Apps-miljø. Hvis du vil ha informasjon om hvordan du kopierer elementer i et Power Apps-miljø, kan du se [Kopiere et miljø](/power-platform/admin/copy-environment). Power Apps-miljøet som du vil overskrive, må være et sandkassemiljø. Du må være en global leieradministrator for å endre et Power Apps-produksjonsmiljø til et sandkassemiljø. Hvis du vil ha mer informasjon om hvordan du endrer et Power Apps-miljø, kan du se [Bytte en forekomst](/dynamics365/admin/switch-instance).

- Hvis du kopierer en forekomst inn i sandkassemiljøet og vil integrere sandkassemiljøet i Dataverse, må du bruke egendefinerte felt på nytt i Dataverse-tabeller. Se [Bruke egendefinerte felt i Dataverse](hr-admin-setup-copy-instance.md?apply-custom-fields-to-common-data-service).

## <a name="effects-of-copying-a-human-resources-database"></a>Virkninger av å kopiere en Human Resources-database

> [!Note]
> Fra og med august 2022 er Dokumenter i Microsoft Azure Blob-lagring inkludert når du kopierer et produksjonsmiljø til et sandkassemiljø. Alle dokumenter og maler som er vedlagt, blir kopiert over fra kildemiljøet til målmiljøet.

Følgende hendelser inntreffer når du kopierer en Human Resources-database:

- Kopieringsprosessen sletter den eksisterende databasen i målmiljøet. Når kopieringsprosessen er fullført, kan du ikke gjenopprette den eksisterende databasen.

- Målmiljøet vil ikke være tilgjengelig før kopieringsprosessen er fullført.

- Alle brukere, bortsett fra de som har sikkerhetsrollen Systemadministrator og andre interne tjenestebrukerkontoer, vil ikke være tilgjengelige. Administratorbrukeren kan slette data før andre brukere får tilgang til systemet igjen.

- Alle brukere med sikkerhetsrollen Systemadministrator må utføre nødvendige konfigurasjonsendringer, for eksempel koble til integreringsendepunkter på nytt til bestemte tjenester eller URL-adresser.

## <a name="copy-the-human-resources-database"></a>Kopiere Human Resources-databasen

Hvis du vil fullføre denne oppgaven, kopierer du først en forekomst, og deretter logger du deg på administrasjonssenteret for Microsoft Power Platform for å kopiere Power Apps-miljøet.

> [!WARNING]
> Når du kopierer en forekomst, slettes databasen i målforekomsten. Målforekomsten er ikke tilgjengelig under denne prosessen.

1. Logg på LCS, og velg LCS-prosjektet som inneholder forekomsten du vil kopiere.

2. I LCS prosjektet velger du flisen **Human Resources-appbehandling**.

3. Velg forekomsten som skal kopieres, og velg deretter **Kopier**.

4. I oppgaveruten **Kopier en forekomst**, velger du forekomsten som skal overskrives, og deretter velger du **Kopier**. Vent til feltet **Kopier status** er oppdatert til **Fullført**.

   ![[Velg forekomsten du vil skrive over.](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Velg **Power Platform**, og logg deg på administrasjonssenteret for Microsoft Power Platform.

   ![[Velg Power Platform.](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Velg Power Apps-miljøet som skal kopieres, og velg deretter **Kopier**.

Hvis du vil ha mer informasjon om kopiering av Power Apps-miljøer, kan du se [Kopiere et miljø](/power-platform/admin/copy-environment#copy-an-environment-1).

7. Når kopieringsprosessen er fullført, logger du på målforekomsten og aktiverer Dataverse-integrering. Hvis du vil ha mer informasjon og instruksjoner, kan du se [Konfigurere Dataverse-integrering for arbeidsområder](./hr-admin-integration-common-data-service.md).

## <a name="data-elements-and-statuses"></a>Dataelementer og -statuser

Følgende dataelementer kopieres ikke når du kopierer en Human Resources-forekomst:

- E-postadresser i **LogisticsElectronicAddress**-tabellen

- Loggen for den satsvise jobben i tabellene **BatchJobHistory**, **BatchHistory** og **BatchConstraintHistory** tables

- SMTP-passordet (Simple Mail Transfer Protocol) i **SysEmailSMTPPassword**-tabellen

- SMTP-reléserveren i **SysEmailParameters**-tabellen

- Innstillinger for utskriftsbehandling i tabellene **PrintMgmtSettings** og **PrintMgmtDocInstance**

- Miljøspesifikke poster i tabellene **SysServerConfig**, **SysServerSessions**, **SysCorpNetPrinters**, **SysClientSessions**, **BatchServerConfig** og **BatchServerGroup**

- Dokumentvedlegg i DocuValue-tabellen. Disse vedleggene omfatter alle Microsoft Office-maler som ble overskrevet i kildemiljøet

- Tilkoblingsstrengen i **PersonnelIntegrationConfiguration**-tabellen

Noen av disse elementene kopieres ikke fordi de er miljøspesifikke. Eksempler inkluderer postene **BatchServerConfig** og **SysCorpNetPrinters**. Andre elementer blir ikke kopiert på grunn av antallet kundestøttebilletter. For eksempel:

- Det kan hende at det sendes dupliserte e-postmeldinger fordi SMTP fortsatt er aktivert i miljøet for testing av brukeraksept (sandkasse).

- Det kan hende at ugyldige integrasjonsmeldinger sendes fordi de satsvise jobbene fortsatt er aktive.

- Brukere kan være aktivert før administratorer kan utføre oppryddingshandlinger etter oppdatering.

I tillegg endres følgende statuser når du kopierer en forekomst:

- Alle brukere, bortsett fra de som har sikkerhetsrollen Systemadministrator, settes til **Deaktivert**.

- Alle satsvise jobber, bortsett fra enkelte systemjobber, settes til **Trekk tilbake**.

## <a name="environment-admin"></a>Miljøadministrator

Alle brukerne i sandkassemålmiljøet, inkludert administratorer, erstattes av brukerne i kildemiljøet. Før du kopierer en forekomst, må du være sikker på at du er administrator i kildemiljøet. Hvis du ikke er det, vil du ikke kunne logge på målsandkassemiljøet etter at kopieringen er fullført.

Alle brukere som ikke er administrator i målsandkassemiljøet, er deaktivert for å hindre uønskede pålogginger i sandkassemiljøet. Administratorer kan reaktivere brukere om nødvendig.

## <a name="apply-custom-fields-to-dataverse"></a>Bruke egendefinerte felt i Dataverse

Hvis du kopierer en forekomst inn i sandkassemiljøet og vil integrere sandkassemiljøet i Dataverse, må du bruke egendefinerte felt på nytt i Dataverse-tabeller.

For hvert egendefinerte felt som vises på Dataverse-tabeller, gjør du følgende:

1. Gå til det egendefinerte feltet og velg **Rediger**.

2. Fjern merket i **Aktivert**-feltet for hver cdm_*-enhet som det egendefinerte feltet er aktivert på.

3. Velg **Bruk endringer**.

4. Velg **Rediger** på nytt.

5. Velg feltet **Aktivert** for hver cdm_*-enhet som det egendefinerte feltet er aktivert på.

6. Velg **Bruk endringer** på nytt.

Prosessen med å fjerne valg, aktivere endringer, velge på nytt og bruke endringer på nytt ber skjemaet om å oppdatere i Dataverse for å inkludere de egendefinerte feltene.

Hvis du vil ha mer informasjon om egendefinerte felt, kan du se [Opprette og arbeide med egendefinerte felt](../fin-ops-core/fin-ops/get-started/user-defined-fields.md).

## <a name="see-also"></a>Se også

[Klargjøre Human Resources](hr-admin-setup-provision.md)</br>
[Fjerne en forekomst](hr-admin-setup-remove-instance.md)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
