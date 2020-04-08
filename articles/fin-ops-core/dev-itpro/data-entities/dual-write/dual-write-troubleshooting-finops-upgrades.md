---
title: Feilsøke problemer i forbindelse med oppgraderinger av Finance and Operations-apper
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer knyttet til oppgraderinger av Finance and Operations-apper.
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
ms.openlocfilehash: 59384d8e8d043eb14231a471c7218ced2dddf739
ms.sourcegitcommit: 68f1485de7d64a6c9eba1088af63bd07992d972d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/27/2020
ms.locfileid: "3172883"
---
# <a name="troubleshoot-issues-related-to-upgrades-of-finance-and-operations-apps"></a>Feilsøke problemer i forbindelse med oppgraderinger av Finance and Operations-apper

[!include [banner](../../includes/banner.md)]



Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Common Data Service. Særlig gir det informasjon som kan hjelpe deg med å løse problemer knyttet til oppgraderinger av Finance and Operations-apper.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="database-synchronization-errors"></a>Databasesynkroniseringsfeil

**Nødvendig rolle for å løse problemet:** Systemadministrator

Det kan hende du får en feilmelding som ligner på følgende eksempel når du prøver å bruke **DualWriteProjectConfiguration**-enheten til å oppdatere en Finance and Operations-app til Platform update 30.

```console
Infolog diagnostic message: 'Cannot select a record in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Følg fremgangsmåten nedenfor for å løse problemet.

1. Logg på den virtuelle maskinen for Finance and Operations-appen.
2. Åpne Visual Studio som administrator, og åpne applikasjonsobjekttreet.
3. Søk etter **DualWriteProjectConfiguration**.
4. I applikasjonsobjekttreet høyreklikker du **DualWriteProjectConfiguration** og velger **Legg til i nytt prosjekt**. Velg **OK** for å opprette det nye prosjektet som bruker standardalternativer.
5. I Løsningsutforsker høyreklikker du **Prosjektegenskaper** og setter **Synkroniser database på build** til **Sann**.
6. Bygg prosjektet, og bekreft at byggingen er vellykket.
7. Velg **Synkroniser database** på **Dynamics 365**-menyen.
8. Velg **Synkroniser** for å utføre en fullstendig databasesynkronisering.
9. Når den fullstendige databasesynkroniseringen er fullført, kjører du trinnet for databasesynkronisering på nytt i Microsoft Dynamics Lifecycle Services (LCS) og bruker de manuelle oppgraderingsskriptene, slik at du kan fortsette med oppdateringen.

## <a name="missing-entity-fields-issue-on-maps"></a>Problem med manglende enhetsfelt på tilordninger

**Nødvendig rolle for å løse problemet:** Systemadministrator

På siden **Dobbel skriving** kan du få en feilmelding som ligner på følgende eksempel:

*Manglende kildefelt \<feltnavn\> i skjemaet.*

![Eksempel på feilmeldingen om manglende kildefelt](media/error_missing_field.png)

Du kan løse problemet ved først å følge disse trinnene for å kontrollere at feltene finnes i enheten.

1. Logg på den virtuelle maskinen for Finance and Operations-appen.
2. Gå til **Arbeidsområder \> Databehandling**, velg flisen **Rammeverkparametere** og deretter, i fanen **Enhetsinnstillinger**, velger du **Oppdater enhetsliste** for å oppdatere enhetene.
3. Gå til **Arbeidsområder \> Databehandling**, velg kategorien **Dataenheter**, og kontroller at enheten finnes i listen. Hvis enheten ikke er oppført, logger du på den virtuelle maskinen for Finance and Operations-appen og kontrollerer at enheten er tilgjengelig.
4. Åpne **Enhetstilordning**-siden fra **Dobbel skriving**-siden i Finance and Operations-appen.
5. Velg **Oppdater enhetsliste** for å fylle ut feltene i enhetstilordningene automatisk.

Hvis problemet fremdeles ikke er løst, følger du denne fremgangsmåten.

> [!IMPORTANT]
> Denne fremgangsmåten fører deg gjennom prosessen med å slette en enhet og deretter legge den til på nytt. Hvis du vil unngå problemer, må du følge fremgangsmåten nøye.

1. I Finance and Operations-appen går du til **Arbeidsområder \> Databehandling** og velger flisen **Dataenheter**.
2. Finn enheten som mangler feltet. Noter målenheten, oppsamlingstabellen, enhetsnavnet og andre kolonneverdier.
3. Hvis noen av behandlingsgruppene er avhengige av denne enheten, må du utføre nødvendige handlinger for behandlingsgruppene før du sletter enheten.
4. Slett enheten som mangler feltet.
5. Velg **Ny**, og legg til enheten igjen. Angi verdiene som du noterte i trinn 2.
6. Åpne **Enhetstilordning**-siden fra **Dobbel skriving**-siden i Finance and Operations-appen.
7. Velg **Oppdater enhetsliste** for å fylle ut feltene i enhetstilordningene automatisk.
