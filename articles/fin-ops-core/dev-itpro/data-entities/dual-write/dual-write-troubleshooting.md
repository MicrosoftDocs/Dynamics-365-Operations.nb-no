---
title: Generell feilsøking
description: Dette emnet inneholder generell feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: b4adc2d83667a05d14a26ace23e5bd8026df4b5f
ms.sourcegitcommit: caa41c076f731f1e02586bc129b9bc15a278d280
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/13/2021
ms.locfileid: "7380218"
---
# <a name="general-troubleshooting"></a>Generell feilsøking

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet inneholder generell feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="enable-and-view-the-plug-in-trace-log-in-dataverse-to-view-error-details"></a><a id="enable-view-trace"></a>Aktivere og vise plugin-sporingsloggen i Dataverse for å vise feildetaljer

**Nødvendig rolle for å aktivere sporingsloggen og vise feil**: Systemadministrator

Følg denne fremgangsmåten for å aktivere sporingsloggen.

1. Logg inn på kundeengasjementsappen, åpne **Innstillinger** -siden, og velg deretter **Administrasjon** under **System**.
2. Velg **Systeminnstillinger** på siden **Administrasjon**.
3. I kolonnen **Sporing av plugin-modul og egendefinert arbeidsflytaktivitet** i **Tilpassing**-fanen velger du **Alle** for å aktivere plugin-sporingsloggen. Hvis du bare vil logge sporingslogger når det oppstår unntak, kan du velge **Unntak** i stedet.


Følg denne fremgangsmåten for å se sporingsloggen.

1. Logg inn på kundeengasjementsappen, åpne **Innstillinger**-siden, og velg deretter **Sporingslogg for plugin-modul** under **Tilpassing**.
2. Finn sporingsloggene der **Typenavn**-kolonnen er satt til **Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PreCommmitPlugin**.
3. Dobbeltklikk et element for å vise hele loggen, og se deretter gjennom **Meldingsblokk**-teksten i hurtigfanen **Utførelse**.

## <a name="enable-debug-mode-to-troubleshoot-live-synchronization-issues-in-finance-and-operations-apps"></a>Aktivere feilsøkingsmodus for å feilsøke problemer med direkte synkronisering i Finance and Operations-apper

**Nødvendig rolle for å vise feilene:** Systemadministrator

Dobbel skriving-feil som kommer fra Dataverse, kan vises i Finance and Operations-appen. Du kan aktivere detaljert logging for feil ved å følge disse trinnene:

1. For alle prosjektkonfigurasjoner i Finance and Operations-apper finnes det et **IsDebugMode**-flagg i **DualWriteProjectConfiguration**-tabellen.
2. Åpne **DualWriteProjectConfiguration** ved hjelp av Excel-tillegget. Hvis du vil bruke tillegget, aktiverer du utformingsmodus i Finance and Operations Excel-tillegget og legger til **DualWriteProjectConfiguration** i arket. Hvis du vil ha mer informasjon, kan du se [Vis og oppdater enhetsdata med Excel](../../office-integration/use-excel-add-in.md).
3. Sett **IsDebugMode** til **Ja** i prosjektet.
4. Kjør scenariet som genererer feil.
5. De detaljerte loggene lagres i tabellen **DualWriteErrorLog**.
6. Hvis du vil slå opp data i tabelleseren, bruker du følgende kobling: `https://999aos.cloudax.dynamics.com/?mi=SysTableBrowser&tableName=DualWriteErrorLog` og erstatter `999` etter behov.
7. Oppdater på nytt etter [KB 4595434](https://fix.lcs.dynamics.com/Issue/Details?kb=4595434&bugId=527820&dbType=3&qc=98e5dc124ac125c57ad633d885ac612aea3ddb8f4abf9d71ab3aa354f2e06cbe), som er tilgjengelig for plattformoppdatering 37 og senere. Hvis du har denne reparasjonen installert, vil feilsøkingsmodusen registrere flere logger.  

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
4. Klikk på **Koble fra miljø**.
5. Velg **Ja** for å bekrefte operasjonen.

Du kan nå koble til et nytt miljø.

## <a name="unable-to-view-the-sales-order-line-information-form"></a>Kan ikke vise informasjonsskjemaet for salgsordrelinjen 

Når du oppretter en salgsordre i Dynamics 365 Sales, kan du bli omdirigert til ordrelinjeskjemaet for Dynamics 365 Project Operations hvis du klikker på **+ Legg til produkter**. Det finnes ingen måter fra dette skjemaet å vise **Informasjon**-skjemaet for salgsordrelinje. Alternativet for **Informasjon** vises ikke i rullegardinlisten under **Ny ordrelinje**. Dette skjer fordi Project Operations er installert i ditt miljø.

Følg denne fremgangsmåten for å reaktivere alternativet for **Informasjon**-skjema:

1. Gå til **Ordrelinje**-tabellen.
2. Finn **Informasjon**-skjemaet under skjemaer-noden.
3. Velg **Informasjon**-skjemaet, og klikk deretter **Aktiver sikkerhetsroller**.
4. Endre sikkerhetsinnstillingen til **Vis til alle**.

## <a name="how-to-enable-and-save-network-trace-so-that-traces-can-be-attached-to-support-tickets"></a>Slik aktiverer du og lagrer nettverkssporing, slik at sporinger kan knyttes til støtteforespørsler

Det kan hende at støttegruppen må gjennomgå nettverkssporing for å feilsøke enkelte problemer. Følg denne fremgangsmåten for å opprette en nettverkssporing:

### <a name="chrome"></a>Chrome

1. Trykk på **F12** i den åpnede fanen, eller velg **Utviklerverktøy** for å åpne utviklerverktøyene.
2. Åpne **Nettverk**-fanen, og skriv inn **integ** i filtertekstboksen.
3. Kjør scenariet og registrer forespørslene som blir logget.
4. Høyreklikk på oppføringene, og velg **Lagre alle som en HAR med innhold**.

### <a name="microsoft-edge"></a>Microsoft Edge

1. Trykk på **F12** i den åpnede fanen, eller velg **Utviklerverktøy** for å åpne utviklerverktøyene.
2. Åpne **Nettverk**-fanen.
3. Kjør scenarioet.
4. Velg **Lagre** for å eksportere resultatene som HAR.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
