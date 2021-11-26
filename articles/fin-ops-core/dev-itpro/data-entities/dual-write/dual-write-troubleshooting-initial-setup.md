---
title: Feilsøke problemer under førstegangsinstallasjon
description: Dette emnet inneholder informasjon som kan hjelpe deg å løse problemer som oppstår under første konfigurasjon av integrering med dobbel skriving.
author: RamaKrishnamoorthy
ms.date: 08/10/2021
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: c9bf5d9017579b4207e09769cff38361442e3938
ms.sourcegitcommit: 9acfb9ddba9582751f53501b82a7e9e60702a613
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/10/2021
ms.locfileid: "7781446"
---
# <a name="troubleshoot-issues-during-initial-setup"></a>Feilsøke problemer under førstegangsinstallasjon

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse. Dette emnet inneholder informasjon som kan hjelpe deg med å løse problemer som kan oppstå under det første oppsettet av integrering med dobbel skriving.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="you-cant-link-a-finance-and-operations-app-to-dataverse"></a>Du kan ikke koble en Finance and Operations-app til Dataverse

**Nødvendig rolle for å konfigurere dobbel skriving:** Systemadministrator i Finance and Operations-apper og Dataverse.

Feil på **oppsett-koblingen til Dataverse**-siden skyldes vanligvis ufullstendige oppsetts- eller tillatelsesproblemer. Kontroller at hele tilstandskontrollen bestås på **Oppsett-koblingen til Dataverse**-siden, som vist i illustrasjonen nedenfor. Du kan ikke koble til dobbel skriving med mindre hele tilstandssjekken bestås.

![Vellykket tilstandssjekk.](media/health_check.png)

Du må ha legitimasjon for Azure AD-leieradministrator for å koble til Finance and Operations- og Dataverse-miljøene. Når du har koblet til miljøene, kan brukere logge på ved hjelp av kontolegitimasjonen og oppdatere en eksisterende tabelltilordning.

## <a name="find-the-limit-on-the-number-of-legal-tables-or-companies-that-can-be-linked-for-dual-write"></a>Finn grensen for antall juridiske tabeller eller firmaer som kan kobles til for dobbeltskriving

Du kan få følgende feilmelding når du prøver å aktivere tilordninger:

*Dobbel skriving-feil - Plugin-registrering mislyktes: [(Kan ikke få partisjonskart for prosjektet DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea. Feil Overskrider de maksimale partisjonene som er tillatt for tilordning av DWM-1ae35e60-4bc2-4905-88ea-69efd3b29260-7f12cb89-1550-42e2-858e-4761fc1443ea)], Det oppstod en eller flere feil.*

Gjeldende grense når du kobler miljøene er omtrent 40 juridiske tabeller. Denne feilen oppstår hvis du prøver å aktivere tilordninger, og flere enn 40 juridiske tabeller er koblet mellom miljøene.

## <a name="connection-set-failed-while-linking-environment"></a>Tilkoblingssettet mislyktes under kobling av miljø

Under kobling av miljøet for dobbel skriving mislykkes handlingen med en feilmelding:

*Lagring av tilkoblingssett mislyktes. Et element med samme nøkkel er allerede lagt til.*

Dobbel skriving støtter ikke flere juridiske enheter / firmaer med samme navn. Hvis du for eksempel har to firmaer med "DAT"-navn i Dataverse, får du denne feilmeldingen.

Hvis du vil fjerne blokkeringen for kunden, fjerner du duplikatposter fra **cdm_company**-tabellen i Dataverse. Hvis en **cdm_company**-tabell har poster med tomt navn, må du også fjerne eller rette disse postene.

## <a name="error-when-opening-the-dual-write-page-in-finance-and-operations-apps"></a>Feil når du åpner Dobbel skriving-siden i Finance and Operations-apper

Du kan få følgende feilmelding når du prøver å koble til et Dataverse-miljø for dobbel skriving:

*Svarstatuskoden indikerer ikke fullført: 404 (ikke funnet).*

Denne feilen oppstår når samtykketrinnet i appen ikke er fullført. Du kan validere om det er gitt samtykke, ved å logge deg på `portal.azure.com` ved hjelp av leieadministratorkontoen, og kontrollere om tredjepartsappen med ID-en `33976c19-1db5-4c02-810e-c243db79efde` vises i AAD-listen over Enterprise-apper. Hvis ikke, kjører du samtykketrinnet på nytt som beskrevet i neste del.

### <a name="providing-app-consent"></a>Gi apptillatelse

+ Åpne følgende URL-adresse med administratorlegitimasjonen.

    `https://login.microsoftonline.com/common/oauth2/authorize?client_id=33976c19-1db5-4c02-810e-c243db79efde&response_type=code&prompt=admin_consent`

+ Velg **Godta** for å samtykke. Du gir tillatelse til å installere appen (med `id=33976c19-1db5-4c02-810e-c243db79efde`) i leieren din.
+ Denne appen er påkrevd for at Dataverse skal kunne kommunisere med Finance and Operations-apper.

    ![Feilsøking under første konfigurasjon av synkronisering.](media/Initial-sync-setup-troubleshooting-1.png)

> [!NOTE]
> Hvis dette ikke fungerer, åpner du URL-adressen i privat modus i Microsoft Edge eller inkognitomodus i Chrome.

## <a name="finance-and-operations-environment-is-not-discoverable"></a>Finance and Operations-miljøet kan ikke oppdages

Du kan få følgende feilmelding:

*Finance and Operations-appmiljøet \*\*\*.cloudax.dynamics.com kan ikke oppdages.*

Det er to ting som kan forårsake et problem der miljøet ikke kan oppdages:

+ Brukeren som brukes til pålogging, er ikke i samme leier som Finance and Operations-forekomsten.
+ Det er noen eldre Finance and Operations-forekomster som ble driftet av Microsoft, og som hadde et problem med oppdagelse. Du kan løse dette ved å oppdatere Finance and Operations-forekomsten. Miljøet skal kunne oppdages etter enhver oppdatering.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]
