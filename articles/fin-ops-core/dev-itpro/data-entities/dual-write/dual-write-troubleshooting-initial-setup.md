---
title: Feilsøk problemer under førstegangsinstallasjon
description: Denne artikkelen inneholder informasjon som kan hjelpe deg å løse problemer som oppstår under første konfigurasjon av integrering med dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d33fc6f4895b53f16cc6957a3a2fc6b1abe90a2f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9289522"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Feilsøk problemer under førstegangsinstallasjon

[!include [banner](../../includes/banner.md)]

Denne artikkelen inneholder feilsøkingsinformasjon om integrasjon av dobbel skriving mellom økonomi- og driftsapper og Dataverse. Dette emnet inneholder informasjon som kan hjelpe deg med å løse problemer som kan oppstå under det første oppsettet av integrering med dobbel skriving.

> [!IMPORTANT]
> Noen av problemene som denne artikkelen løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Du kan ikke koble en økonomi- og driftsapp til Dataverse

**Nødvendig rolle for å konfigurere dobbel skriving:** Systemadministrator i økonomi- og driftsapper og Dataverse.

Feil på **oppsett-koblingen til Dataverse**-siden skyldes vanligvis ufullstendige oppsetts- eller tillatelsesproblemer. Kontroller at hele tilstandskontrollen bestås på **Oppsett-koblingen til Dataverse**-siden, som vist i illustrasjonen nedenfor. Du kan ikke koble til dobbel skriving med mindre hele tilstandssjekken bestås.

![Vellykket tilstandssjekk.](media/health_check.png)

Du må ha legitimasjon for Azure AD-leieradministrator for å koble til økonomi- og driftsmiljøet og Dataverse-miljøet. Når du har koblet til miljøene, kan brukere logge på ved hjelp av kontolegitimasjonen og oppdatere en eksisterende tabelltilordning.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Finn grensen for antall juridiske tabeller eller firmaer som kan kobles til for dobbeltskriving

Du kan få følgende feilmelding når du prøver å aktivere tilordninger:

*Dobbel skriving-feil - Plugin-registrering mislyktes: [(Kan ikke få partisjonskart for prosjektet DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Feil Overskrider de maksimale partisjonene som er tillatt for tilordning av DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], Det oppstod en eller flere feil.*

Gjeldende grense når du kobler miljøene er omtrent 40 juridiske tabeller. Denne feilen oppstår hvis du prøver å aktivere tilordninger, og flere enn 40 juridiske tabeller er koblet mellom miljøene.

## <a name="connection-set-failed-while-linking-environment"></a>Tilkoblingssettet mislyktes under kobling av miljø

Under kobling av miljøet for dobbel skriving mislykkes handlingen med en feilmelding:

*Lagring av tilkoblingssett mislyktes. Et element med samme nøkkel er allerede lagt til.*

Dobbel skriving støtter ikke flere juridiske enheter / firmaer med samme navn. Hvis du for eksempel har to firmaer med "DAT"-navn i Dataverse, får du denne feilmeldingen.

Hvis du vil fjerne blokkeringen for kunden, fjerner du duplikatposter fra **cdm_company**-tabellen i Dataverse. Hvis en **cdm_company**-tabell har poster med tomt navn, må du også fjerne eller rette disse postene.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Feil når du åpner Dobbel skriving-siden i økonomi- og driftsapper

Du kan få følgende feilmelding når du prøver å koble til et Dataverse-miljø for dobbel skriving:

*Svarstatuskoden indikerer ikke fullført: 404 (ikke funnet).*

Denne feilen oppstår når samtykketrinnet i appen ikke er fullført. Du kan validere om det er gitt samtykke, ved å logge deg på `portal.azure.com` ved hjelp av leieadministratorkontoen, og kontrollere om tredjepartsappen med ID-en `33976c19-1db5-4c02-810e-c243db79efde` vises i AAD-listen over Enterprise-apper. Hvis ikke, kjører du samtykketrinnet på nytt som beskrevet i neste del.

### <a name="providing-app-consent"></a>Gi apptillatelse

+ Åpne følgende URL-adresse med administratorlegitimasjonen.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Velg **Godta** for å samtykke. Du gir tillatelse til å installere appen (med `id=33976c19-1db5-4c02-810e-c243db79efde`) i leieren din.
+ Denne appen er påkrevd for at Dataverse skal kunne kommunisere med økonomi- og driftsapper.

    ![Feilsøking under første konfigurasjon av synkronisering.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Hvis dette ikke fungerer, åpner du URL-adressen i privat modus i Microsoft Edge eller inkognitomodus i Chrome.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Økonomi- og driftsmiljø kan ikke oppdages

Du kan få følgende feilmelding:

*Økonomi- og driftsappmiljøet \*\*\*.cloudax.dynamics.com kan ikke oppdages.*

Det er to ting som kan forårsake et problem der miljøet ikke kan oppdages:

+ Brukeren som brukes til pålogging, er ikke i samme leier som økonomi- og driftsforekomsten.
+ Det er noen eldre økonomi- og driftsforekomster som ble driftet av Microsoft, og som hadde et problem med oppdagelse. Du kan løse dette ved å oppdatere økonomi- og driftsforekomsten. Miljøet skal kunne oppdages etter enhver oppdatering.

## <a name="403-forbidden-error-while-connections-are-being-created"></a>403-feil (forbudt) når tilkoblinger opprettes

Som en del av koblingsprosessen for skrivetilgang opprettes det to Power Apps-tilkoblinger (også kalt *Apihub*) på vegne av brukeren i det koblede Dataverse-miljøet. Hvis kunden ikke har en lisens for Power Apps-miljøet, mislykkes opprettelsen av ApiHub-tilkoblingene, og det vises en 403-feil (forbudt). Her er et eksempel på feilmeldingen:

> MSG=\[Kan ikke konfigurere miljø for dobbel skriving. Feildetaljer:Svarstatuskoden indikerer ikke fullført: 403 (forbudt). - Svarstatuskoden indikerer ikke fullført: 403 (forbudt).\] STACKTRACE=\[   ved Microsoft.Dynamics.Integrator.ProjectManagementService.DualWrite.DualWriteConnectionSetProcessor.\<CreateDualWriteConnectionSetAsync\>d\_\_29.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\DualWrite\\DualWriteConnectionSetProcessor.cs:line 297 --- Slutt på stakkspor fra forrige plassering der unntak ble utløst --- av System.Runtime.ExceptionServices.ExceptionDispatchInfo.Throw() ved System.Runtime.CompilerServices.TaskAwaiter.HandleNonSuccessAndDebuggerNotification(Task task) ved Microsoft.Dynamics.Integrator.ProjectManagementService.Controllers.DualWriteEnvironmentManagementController.\<SetupDualWriteEnvironmentAsync\>d\_\_34.MoveNext() in X:\\bt\\1158727\\repo\\src\\ProjectManagementService\\Controllers\\DualWriteEnvironmentManagementController.cs:line 265\]

Denne feilen oppstår på grunn av mangel på Power Apps-lisens. Tildel en passende lisens (for eksempel plan for Power Apps-prøveversjon 2) til brukeren slik at brukeren har tillatelse til å opprette tilkoblingene. Hvis du vil kontrollere lisensen, kan kunden gå til [Min konto](https://portal.office.com/account/?ref=MeControl#subscriptions)-nettstedet for å vise lisensene som er tildelt brukeren i øyeblikket.

Hvis du vil ha mer informasjon om Power Apps-lisens, kan du se følgende artikler:

- [Tildel lisenser til brukere](/microsoft-365/admin/manage/assign-licenses-to-users?view=o365-worldwide)
- [Kjøp Power Apps for organisasjonen](/power-platform/admin/signup-for-powerapps-admin)

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

