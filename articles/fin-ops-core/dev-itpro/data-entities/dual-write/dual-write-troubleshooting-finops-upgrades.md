---
title: Feilsøk problemer fra oppgraderinger av Finance and Operations-apper
description: Denne artikkelen inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer knyttet til oppgraderinger av økonomi- og driftsapper.
author: RamaKrishnamoorthy
ms.date: 03/16/2020
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-01-06
ms.openlocfilehash: 954268b03be2be90f67dc9b7756f33215856864a
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882149"
---
# <a name="troubleshoot-issues-from-upgrades-of-finance-and-operations-apps"></a>Feilsøk problemer fra oppgraderinger av Finance and Operations-apper

[!include [banner](../../includes/banner.md)]





Denne artikkelen inneholder feilsøkingsinformasjon om integrasjon av dobbel skriving mellom økonomi- og driftsapper og Dataverse. Særlig gir det informasjon som kan hjelpe deg med å løse problemer knyttet til oppgraderinger av økonomi- og driftsapper.

> [!IMPORTANT]
> Noen av problemene som denne artikkelen løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="database-synchronization-errors"></a>Databasesynkroniseringsfeil

**Nødvendig rolle for å løse problemet:** Systemadministrator

Det kan hende du får en feilmelding som ligner på følgende eksempel når du prøver å bruke tabellen **DualWriteProjectConfiguration** til å oppdatere en økonomi- og driftsapp til Platform update 30.

```console
Infolog diagnostic message: 'Cannot select a row in Dual write project sync (DualWriteProjectConfiguration). The SQL database has issued an error.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Object Server Database Synchronizer: ' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: '[Microsoft][ODBC Driver 17 for SQL Server][SQL Server]Invalid column name 'ISDELETE'.' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'SELECT T1.PROJECTNAME,T1.EXTERNALENTITYNAME,T1.INTERNALENTITYNAME,T1.EXTERNALENVIRONMENTURL,T1.STATUS,T1.ENABLEBATCHLOOKUP,T1.PARTITIONMAP,T1.QUERYFILTEREXPRESSION,T1.INTEGRATIONKEY,T1.ISDELETE,T1.ISDEBUGMODE,T1.RECVERSION,T1.PARTITION,T1.RECID FROM DUALWRITEPROJECTCONFIGURATION T1 WHERE (PARTITION=5637144576)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'session 1043 (Admin)' on category 'Error'. 10/28/2019 15:18:20: Infolog diagnostic message: 'Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN.' on category 'Error'.
10/28/2019 15:18:20: Application configuration sync failed.
Microsoft.Dynamics.AX.Framework.Database.TableSyncException: Custom action threw exception(s), please investigate before synchronizing again: 'InfoException:Stack trace: Call to TTSCOMMIT without first calling TTSBEGIN."
```

Følg fremgangsmåten nedenfor for å løse problemet.

1. Logg på den virtuelle maskinen for økonomi- og driftsappen.
2. Åpne Visual Studio som administrator, og åpne applikasjonsobjekttreet.
3. Søk etter **DualWriteProjectConfiguration**.
4. I applikasjonsobjekttreet høyreklikker du **DualWriteProjectConfiguration** og velger **Legg til i nytt prosjekt**. Velg **OK** for å opprette det nye prosjektet som bruker standardalternativer.
5. I Løsningsutforsker høyreklikker du **Prosjektegenskaper** og setter **Synkroniser database på build** til **Sann**.
6. Bygg prosjektet, og bekreft at byggingen er vellykket.
7. Velg **Synkroniser database** på **Dynamics 365**-menyen.
8. Velg **Synkroniser** for å utføre en fullstendig databasesynkronisering.
9. Når den fullstendige databasesynkroniseringen er fullført, kjører du trinnet for databasesynkronisering på nytt i Microsoft Dynamics Lifecycle Services (LCS) og bruker de manuelle oppgraderingsskriptene, slik at du kan fortsette med oppdateringen.

## <a name="missing-table-columns-issue-on-maps"></a>Problemer med manglende tabellkolonner i tilordninger

**Nødvendig rolle for å løse problemet:** Systemadministrator

På siden **Dobbel skriving** kan du få en feilmelding som ligner på følgende eksempel:

*Manglende kildefelt feltnavn \<field name\> i skjemaet.*

![Eksempel på feilmeldingen om manglende kildekolonne.](media/error_missing_field.png)

Du kan løse problemet ved først å følge disse trinnene for å kontrollere at kolonnene finnes i tabellen.

1. Logg på den virtuelle maskinen for økonomi- og driftsappen.
2. Gå til **Arbeidsområder \> Databehandling**, velg flisen **Rammeverkparametere** og deretter, i fanen **Tabellinnstillinger**, velger du **Oppdater tabelliste** for å oppdatere tabellene.
3. Gå til **Arbeidsområder \> Databehandling**, velg fanen **Datatabeller**, og kontroller at tabellen finnes i listen. Hvis tabellen ikke er oppført, logger du på den virtuelle maskinen for økonomi- og driftsappen og kontrollerer at tabellen er tilgjengelig.
4. Åpne **Tabelltilordning**-siden fra **Dobbel skriving**-siden i økonomi- og driftsappen.
5. Velg **Oppdater tabelliste** for å fylle ut kolonnene i tabelltilordningene automatisk.

Hvis problemet fremdeles ikke er løst, følger du denne fremgangsmåten.

> [!IMPORTANT]
> Denne fremgangsmåten fører deg gjennom prosessen med å slette en tabell og deretter legge den til på nytt. Hvis du vil unngå problemer, må du følge fremgangsmåten nøye.

1. I økonomi- og driftsappen går du til **Arbeidsområder \> Databehandling** og velger flisen **Datatabeller**.
2. Finn tabellen som mangler attributtet. Klikk **Endre måltilordning** på verktøylinjen.
3. Klikk på **Generer tilordning** under **Tilordne oppsamling til mål**.
4. Åpne **Tabelltilordning**-siden fra **Dobbel skriving**-siden i økonomi- og driftsappen.
5. Hvis attributtet ikke fylles ut automatisk på kartet, legger du det til manuelt ved å klikke **Legg til attributt** og deretter **Lagre**. 
6. Velg kartet, og klikk **Kjør**.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]