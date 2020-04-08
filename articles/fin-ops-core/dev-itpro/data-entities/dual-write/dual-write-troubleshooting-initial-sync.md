---
title: Feilsøke problemer under første synkronisering
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering.
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
ms.openlocfilehash: d51b547093825a6e7730b5fdfcfb1c081776c63c
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172720"
---
# <a name="troubleshoot-issues-during-initial-synchronization"></a>Feilsøke problemer under første synkronisering

[!include [banner](../../includes/banner.md)]



Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service. Det inneholder informasjon som kan hjelpe deg med å løse problemer som kan oppstå under første synkronisering. 

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="check-for-initial-synchronization-errors-in-a-finance-and-operations-app"></a>Se etter innledende synkroniseringsfeil i en Finance and Operations-app

Når du har aktivert tilordningsmalene, skal statusen for tilordningene være **Kjører**. Hvis statusen er **Kjører ikke**, oppstod det feil under første synkronisering. Hvis du vil vise feilene, velger du kategorien **Detaljer om innledende synkronisering** på siden **Dobbel skriving**.

![Kategorien Detaljer om innledende synkronisering](media/initial_sync_status.png)

## <a name="you-cant-complete-initial-synchronization-400-bad-request"></a>Du kan ikke fullføre første synkronisering: 400 Ugyldig forespørsel

**Nødvendig rolle for å løse problemet:** Systemadministrator

Du kan få følgende feilmelding når du prøver å kjøre tilordningen og den innledende synkroniseringen:

*Den eksterne serveren returnerte en feil: (400) Ugyldig forespørsel.), AX-eksporten oppdaget en feil*

Her er et eksempel på hele feilmeldingen.

```console
Dual write Initial Sync completed with status: Error. Following are the details:
Executed leg: From AX Financial dimensions to CRM msdyn_dimensionattributes
with exported records count: 0, ImportRecordsErrorCount: 0,
ImportRecordsInsertedCount: 0 and ImportRecordsUpdatedCount: 0
ErrorsDetails:
Dual write Initial sync failed
Message: ([Bad Request], The remote server returned an error: (400) Bad Request.), AX export encountered an error
Stacktrace: at
Microsoft.Dynamics.Integrator.QueryGenerator.AxClient.\<ExportAxPackage\>d__16.MoveNext()
in X:\\bt\\1024532\\repo\\src\\Core\\QueryGenerator\\AxClient.cs:line 265
\--- End of stack trace from previous location where exception was thrown ---
at System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw()
at System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task)
at Microsoft.D365.ServicePlatform.Context.ServiceContext.Activity.\<ExecuteAsync\>d__11\`2.MoveNext()
\--- End of stack trace from previous location where exception was thrown ---
```

Hvis denne feilen oppstår konsekvent, og du ikke kan fullføre den første synkroniseringen, følger du denne fremgangsmåten for å løse problemet.

1. Logg på den virtuelle maskinen for Finance and Operations-appen.
2. Åpne Microsoft Management Console. 
3. I **Tjenester**-ruten kontrollerer du at tjenesten for rammeverk for dataimport/-eksport for Microsoft Dynamics 365. Start den på nytt hvis den er stoppet, fordi den første synkroniseringen krever det.

## <a name="initial-synchronization-error-403-forbidden"></a>Innledende synkroniseringsfeil: 403 forbudt

Du kan få følgende feilmelding under innledende synkronisering:

*(\[Forbudt\], Den eksterne serveren returnerte en feil: (403) Forbudt.), AX-eksporten oppdaget en feil*

Følg fremgangsmåten nedenfor for å løse problemet.

1. Logg på Finance and Operations-appen.
2. På siden **Azure Active Directory-programmer** sletter du **DtAppID**-klienten, og deretter legger du den til på nytt.

![Liste over Azure AD-programmer](media/aad_applications.png)

## <a name="self-reference-failures-during-initial-synchronization"></a>Selvreferansefeil under innledende synkronisering

Du kan få en feilmelding som ligner på følgende eksempel hvis noen av tilordningene har selvreferanser:

*På leverandører V2, følgende feil: Post-ID: ny post, ErrorMessage: Kunne ikke løse GUIDen for feltet: msdyn\_invoicevendoraccountnumber.msdyn:\_vendoraccountnumber. Oppslagsverdien ble ikke funnet: CN-001. Prøv denne URL-adressen for å kontrollere om referansedataene finnes: `https://sampleorg.crm.dynamics.com/api/data/v9.0/msdyn_vendors?$select=msdyn_vendoraccountnumber,msdyn_vendorid&$filter=msdyn_vendoraccountnumber` eq 'CN-001'*

Denne typen feil oppstår under innledende synkronisering av tilordninger som har selvreferanser. I det foregående eksemplet refererer feltfakturakontoen til leverandørenheten.

Hvis du vil løse problemet, må du kanskje kjøre tilordningen to ganger før den første synkroniseringen er vellykket.

