---
title: Feilsøke problemer med dobbel skriving i Finance and Operations-apper
description: Dette emnet inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer med dobbel skriving-modulen i Finance and Operations-apper.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9bff8ad0c5716648dec6eadfb21412a2b17f155e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2021
ms.locfileid: "5561232"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Feilsøke problemer med dobbel skriving i Finance and Operations-apper

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dette emnet inneholder feilsøkingsinformasjon om dobbel skriving-integrasjon mellom Finance and Operations-apper og Dataverse. Mer spesifikt gir det informasjon som kan hjelpe deg med å løse problemer med **Dobbel skriving**-modulen i Finance and Operations-apper.

> [!IMPORTANT]
> Noen av problemene som dette emnet løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Du kan ikke laste inn dobbel skriving-modulen i en Finance and Operations-app

Hvis du ikke kan åpne **Dobbel skriving**-siden ved å velge **Dobbel skriving**-flisen i **Databehandling**-arbeidsområdet, er dataintegrasjonstjenesten sannsynligvis nede. Opprett en støtteforespørsel for å be om omstart av dataintegrasjonstjenesten.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Feil når du prøver å opprette en ny tabelltilordning

**Påkrevd legitimasjon for å løse problemet:** Den samme brukeren som konfigurere dobbelt skriving.

Du kan få følgende feilmelding når du prøver å konfigurere en ny tabell for dobbel skriving. Den eneste brukeren som kan opprette en tilordning, er brukeren som konfigurere dobbelt skriving-forbindelsen.

*Svarstatuskoden indikerer ikke fullført: 401 (uautorisert)*


## <a name="error-when-you-open-the-dual-write-user-interface"></a>Feil når du åpner bruker grensesnittet for dobbel skriving

Du kan få følgende feilmelding når du prøver å få tilgang til dobbel skriving fra arbeidsområdet **Databehandling**:

*login.microsoftonline.com kunne ikke koble til.*

Du kan løse problemet ved å logge på ved å bruke et InPrivate-vindu i Microsoft Edge, et inkognito-vindu i Chromium, eller et inkognito-vindu i Google Chrome. Du må også oppheve blokkeringen eller fjerne tredjeparts informasjonskapsler.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Feil når du kobler miljøet for dobbel skriving eller legger til en ny tabelltilordning

**Nødvendig rolle for å løse problemet:** Systemadministrator i både Finance and Operations-apper og Dataverse.

Du kan støte på følgende feilmelding når du kobler eller oppretter tilordninger:

*Svarstatuskoden indikerer ikke fullført: 403 (tokenexchange).<br> Økt-ID: \<your session id\><br> Rotaktivitet-ID: \<your root activity id\>*

Denne feilen kan oppstå hvis du ikke har tilstrekkelige tillatelser til å koble dobbel skriving eller opprette tilordninger. Denne feilen kan også oppstå hvis Dataverse-miljøet ble tilbakestilt uten å koble fra dobbel skriving. Alle brukere med rollen systemansvarlig i både Finance and Operations-apper og Dataverse kan koble sammen miljøer. Bare brukeren som konfigurerte dobbel skriving-tilkoblingen, kan legge til nye tabelltilordninger. Etter installasjonen kan alle brukere med rollen systemansvarlig overvåke statusen og redigere tilordningene.

## <a name="error-when-you-stop-the-table-mapping"></a>Feil når du stopper tabelltilordningen

Du kan få følgende feilmelding når du prøver å stoppe tabelltilordningene:

*\[Forbudt\], \[{"status":403,"kilde":"","melding":"Feil fra token-utveksling: Brukeren har ikke tilgang til tilkoblingen dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Den eksterne serveren returnerte en feil: (403) Forbidden.*

Denne feilen oppstår når det koblede Dataverse-miljøet ikke er tilgjengelig.

Du kan løse problemet ved å opprette en støtteforespørsel for data integrasjonsgruppen. Knytt til nettverkssporingen slik at dataintegrasjonsgruppen kan merke tilordningene som **Kjører ikke** i serverdelen.

## <a name="error-while-trying-to-start-a-table-mapping"></a>Feil under forsøk på å starte en tabelltilordning

Det kan hende du får en feilmelding som nedenfor når du forsøker å angi denne tilstanden for en tilordning til **Kjører**:

*Kan ikke fullføre den opprinnelige datasynkroniseringen. Feil: dobbelt skriving feil - registrering av plugin-modul mislyktes: kan ikke opprette metadata for oppslag med dobbel skriving. Feilobjektreferanse er ikke satt til en forekomst av et objekt.*

Hurtigreparasjonen for denne feilen er avhengig av årsaken til feilen:

+ Hvis tilordningen har avhengige tilordninger, må du sørge for å aktivere de avhengige tilordningene for denne tabelltilordningen.
+ Tilordningen kan mangle kilde- eller målkolonner. Hvis en kolonne i Finance and Operations-appen mangler, følger du trinnene i delen [Problemer med manglende tabellkolonner i tilordninger](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Hvis det mangler en kolonne i Dataverse, klikker du på **Oppdater tabeller**-knappen for tilordningen, slik at kolonnene fylles ut automatisk i tilordningen på nytt.


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]