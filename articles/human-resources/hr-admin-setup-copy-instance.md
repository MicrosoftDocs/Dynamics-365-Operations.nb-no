---
title: Kopier en forekomst
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 0bbe325edb65cad0c1912e0a6ade559e5675dc58
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010024"
---
# <a name="copy-an-instance"></a>Kopier en forekomst

Du kan bruke Microsoft Dynamics Lifecycle Services (LCS) til å kopiere en Microsoft Dynamics 365 Human Resources-database til et sandkassemiljø. Hvis du har et annet sandkassemiljø, kan du også kopiere databasen fra dette miljøet til et målrettet sandkassemiljø.

Hvis du vil kopiere en forekomst, må du sikre følgende:

- Forekomsten av Human Resources som du vil overskrive, må være et sandkassemiljø.

- Miljøene du kopierer fra og til, må være i samme område. Du kan ikke kopiere på tvers av områder.

- Du må være administrator i målmiljøet, slik at du kan logge på det etter at du har kopiert forekomsten.

- Når du kopierer Human Resources-databasen, kopierer du ikke elementene (apper eller data) som finnes i et Microsoft PowerApps-miljø. Hvis du vil ha informasjon om hvordan du kopierer elementer i et PowerApps-miljø, kan du se [Kopiere et miljø](https://docs.microsoft.com/power-platform/admin/copy-environment). PowerApps-miljøet som du vil overskrive, må være et sandkassemiljø. Du må være en global leieradministrator for å endre et PowerApps-produksjonsmiljø til et sandkassemiljø. Hvis du vil ha mer informasjon om hvordan du endrer et PowerApps-miljø, kan du se [Bytte en forekomst](https://docs.microsoft.com/dynamics365/admin/switch-instance).

## <a name="effects-of-copying-a-human-resources-database"></a>Virkninger av å kopiere en Human Resources-database

Følgende hendelser inntreffer når du kopierer en Human Resources-database:

- Kopieringsprosessen sletter den eksisterende databasen i målmiljøet. Når kopieringsprosessen er fullført, kan du ikke gjenopprette den eksisterende databasen.

- Målmiljøet vil ikke være tilgjengelig før kopieringsprosessen er fullført.

- Dokumenter i Microsoft Azure Blob-lagring kopieres ikke fra ett miljø til et annet. Derfor vil ingen dokumenter og maler som er vedlagt, bli kopiert, og de forblir i kildemiljøet.

- Alle brukere, bortsett fra administratoren og andre brukerkontoer for interne tjenester, vil bli utilgjengelige. Derfor kan administratorbrukeren slette eller nedtone data før andre brukere får tilgang til systemet igjen.

- Administratorbrukeren må utføre nødvendige konfigurasjonsendringer, for eksempel koble til integreringsendepunkter på nytt til bestemte tjenester eller URL-adresser.

## <a name="copy-the-human-resources-database"></a>Kopiere Human Resources-databasen

Hvis du vil fullføre denne oppgaven, kopierer du først en forekomst, og deretter logger du deg på administrasjonssenteret for Microsoft Power Platform for å kopiere PowerApps-miljøet.

> [!WARNING]
> Når du kopierer en forekomst, slettes databasen i målforekomsten. Målforekomsten er ikke tilgjengelig under denne prosessen.

1. Logg på LCS, og velg LCS-prosjektet som inneholder forekomsten du vil kopiere.

2. I LCS prosjektet velger du flisen **Human Resources-appbehandling**.

3. Velg forekomsten som skal kopieres, og velg deretter **Kopier**.

4. I oppgaveruten **Kopier en forekomst**, velger du forekomsten som skal overskrives, og deretter velger du **Kopier**. Vent til verdien i feltet **Kopier status** er oppdatert til **Fullført**.

   ![[Velge forekomst som skal overskrives](./media/copy-instance-select-target-instance.png)](./media/copy-instance-select-target-instance.png)

5. Velg **Power Platform**, og logg deg på administrasjonssenteret for Microsoft Power Platform.

   ![[Velg Power Platform](./media/copy-instance-select-power-platform.png)](./media/copy-instance-select-power-platform.png)

6. Velg PowerApps-miljøet som skal kopieres, og velg deretter **Kopier**.

7. Når kopieringsprosessen er fullført, logger du på målforekomsten og aktiverer Common Data Service-integrering. Hvis du vil ha mer informasjon og instruksjoner, kan du se [Konfigurere Common Data Service-integrering for arbeidsområder](https://docs.microsoft.com/dynamics365/talent/hr-common-data-service-integration).

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

Noen av disse elementene kopieres ikke fordi de er miljøspesifikke. Eksempler inkluderer postene **BatchServerConfig** og **SysCorpNetPrinters**. Andre elementer blir ikke kopiert på grunn av antallet kundestøttebilletter. Det kan for eksempel hende at dupliserte e-poster sendes fordi SMTP fortsatt er aktivert i sandkassemiljøet for godkjenning av bruker, ugyldige integrasjonsmeldinger kan bli sendt fordi de fortsatt er aktive, og brukere kan bli aktivert før administratorer kan utføre handlinger opprydding etter oppdatering.

I tillegg endres følgende statuser når du kopierer en forekomst:

- Alle brukere bortsett fra administratorer settes til **Deaktivert**.

- Alle satsvise jobber, bortsett fra enkelte systemjobber, settes til **Trekk tilbake**.

## <a name="environment-admin"></a>Miljøadministrator

Alle brukerne i sandkassemålmiljøet, inkludert administratorer, erstattes av brukerne i kildemiljøet. Før du kopierer en forekomst, må du være sikker på at du er administrator i målmiljøet. Hvis du ikke er det, vil du ikke kunne logge på målsandkassemiljøet etter at kopieringen er fullført.

Alle brukere som ikke er administrator i målsandkassemiljøet, er deaktivert for å hindre uønskede pålogginger i sandkassemiljøet. Administratorer kan reaktivere brukere om nødvendig.
