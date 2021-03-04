---
title: Generell feilsøking
description: Dette emnet inneholder generell feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse.
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
ms.openlocfilehash: 6356ec6850667f32f9e9e4133686c40f0b6d76d7
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4688265"
---
# <a name="general-troubleshooting"></a>Generell feilsøking

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dette emnet inneholder generell feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="when-you-try-to-install-the-dual-write-package-by-using-the-package-deployer-tool-no-available-solutions-are-shown"></a>Når du prøver å installere dobbel skriving-pakken ved hjelp av Package Deployer-verktøyet, vises ingen tilgjengelige løsninger

Noen versjoner av Package Deployer-verktøyet er ikke kompatible med løsningspakken for dobbel skriving. Hvis du vil installere pakken, må du bruke [versjon 9.1.0.20](https://www.nuget.org/packages/Microsoft.CrmSdk.XrmTooling.PackageDeployment.Wpf/9.1.0.20) eller senere av Package Deployer-verktøyet.

Når du har installert Package Deployer-verktøyet, installerer du løsningspakken ved å følge disse trinnene.

1. Last ned den nyeste løsningspakkefilen fra Yammer.com. Når zip-filen for pakken er lastet ned, høyreklikker du den og velger **Egenskaper**. Merk av for **Fjern blokkering**, og velg deretter **Bruk**. Hvis du ikke ser avmerkingsboksen **Fjern blokkering,** er blokkeringen av zip-filen allerede fjernet, og du kan hoppe over dette trinnet.

    ![Dialogboksen Egenskaper](media/unblock_option.png)

2. Pakk ut zip-filen for pakken, og kopier alle filene i mappen **Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438**.

    ![Innholdet i mappen Dynamics365FinanceAndOperationsCommon.PackageDeployer.2.0.438](media/extract_package.png)

3. Lim inn alle de kopierte filene i **Verktøy**-mappen i Package Deployer-verktøyet. 
4. Kjør **PackageDeployer.exe** for å velge Dataverse-miljøet og installere løsningene.

    ![Innhold i Verktøy-mappen](media/paste_copied_files.png)

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Aktivere og vise plugin-sporingsloggen i Dataverse for å vise feildetaljer

**Nødvendig rolle for å aktivere sporingsloggen og vise feil**: Systemadministrator

Følg denne fremgangsmåten for å aktivere sporingsloggen.

1. Logg inn på den modelldrevne appe i Dynamics 365, åpne **Innstillinger**-siden, og velg deretter **Administrasjon** under **System**.
2. Velg **Systeminnstillinger** på siden **Administrasjon**.
3. I kategorien **Tilpassing**, i feltet **Sporing av plugin-modul og egendefinert arbeidsflytaktivitet**, velger du **Alle** for å aktivere plugin-sporingsloggen. Hvis du bare vil logge sporingslogger når det oppstår unntak, kan du velge **Unntak** i stedet.


Følg denne fremgangsmåten for å se sporingsloggen.

1. Logg inn på den modelldrevne appe i Dynamics 365, åpne **Innstillinger**-siden, og velg deretter **Sporingslogg for plugin-modul** under **Tilpassing**.
2. Finn sporingsloggene der **Typenavn**-feltet er satt til **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Dobbeltklikk et element for å vise hele loggen, og se deretter gjennom **Meldingsblokk**-teksten i hurtigfanen **Utførelse**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Aktivere feilsøkingsmodus for å feilsøke problemer med direkte synkronisering i Finance and Operations-apper

**Nødvendig rolle for å vise feilene:** Systemadministrator – dobbel skriving-feil som kommer fra Dataverse, kan vises i Finance and Operations-appen. I noen tilfeller er ikke hele teksten i feilmeldingen tilgjengelig fordi meldingen er for lang eller inneholder personlig identifiserende informasjon (PII). Du kan aktivere detaljert logging for feil ved å følge disse trinnene.

1. Alle prosjektkonfigurasjoner i Finance and Operations-apper har en **IsDebugMode**-egenskap i **DualWriteProjectConfiguration**-enheten. Åpne **DualWriteProjectConfiguration**-enheten ved hjelp av Excel-tillegget.

    > [!TIP]
    > En enkel måte å åpne enheten på er å aktivere **Utforming**-modus i Excel-tillegget og deretter legge til **DualWriteProjectConfigurationEntity** i regnearket. Hvis du vil ha mer informasjon, kan du se [Åpne enhetsdata i Excel og oppdatere dataene ved hjelp av Excel-tillegget](../../office-integration/use-excel-add-in.md).

2. Sett egenskapen **IsDebugMode** til **Ja** for prosjektet.
3. Kjør scenariet som genererer feil.
4. De detaljerte loggene er tilgjengelige i tabellen DualWriteErrorLog. Hvis du vil slå opp data i tabelleseren, bruker du følgende URL-adresse (erstatt **XXX** etter behov):

    `https://XXXaos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog`

## <a name="check-synchronization-errors-on-the-virtual-machine-for-the-finance-and-operations-app"></a>Kontrollere synkroniseringsfeil på den virtuelle maskinen for Finance and Operations-appen

**Nødvendig rolle for å vise feilene:** Systemadministrator

1. Logg på Microsoft Dynamics Lifecycle Services (LCS).
2. Åpne LCS-prosjektet du har valgt til å utføre testing av dobbel skriving for.
3. Velg flisen **Skybaserte miljøer**.
4. Bruk Eksternt skrivebord for å logge på den virtuelle maskinen for Finance and Operations-appen. Bruk den lokale kontoen som vises i LCS.
5. Åpne hendelseslisten.
6. Velg **Program- og tjenestelogger \> Microsoft \> Dynamics \> AX-DualWriteSync \> Drift**.
7. Se gjennom listen over nylige feil.

## <a name="unlink-and-link-another-dataverse-environment-from-a-finance-and-operations-app"></a>Koble fra og koble til et annet Dataverse-miljø fra en Finance and Operations-app

**Nødvendig rolle for å koble fra miljøet:** Systemansvarlig for enten Finance and Operations-app eller Dataverse.

1. Logg på Finance and Operations-appen.
2. Gå til **Arbeidsområder \> Databehandling**, og velg flisen **Dobbel skriving**.
3. Velg alle kjørende tilordninger, og klikk på **Stopp**.
4. Klikk **Koble fra miljø**.
5. Velg **Ja** for å bekrefte operasjonen.

Du kan nå koble til et nytt miljø.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Kan ikke vise informasjonsskjemaet for salgsordrelinjen 

Når du oppretter en salgsordre i Dynamics 365 Sales, kan du bli omdirigert til ordrelinjeskjemaet for Dynamics 365 Project Operations hvis du klikker på **+ Legg til produkter**. Det finnes ingen måter fra dette skjemaet å vise **Informasjon**-skjemaet for salgsordrelinje. Alternativet for **Informasjon** vises ikke i rullegardinlisten under **Ny ordrelinje**. Dette skjer fordi Project Operations er installert i ditt miljø.

Følg denne fremgangsmåten for å reaktivere alternativet for **Informasjon**-skjema:
1. Gå til **Ordrelinje**-enheten.
2. Finn **Informasjon**-skjemaet under skjemaer-noden. 
3. Velg **Informasjon**-skjemaet, og klikk deretter **Aktiver sikkerhetsroller**. 
4. Endre sikkerhetsinnstillingen til **Vis til alle**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]