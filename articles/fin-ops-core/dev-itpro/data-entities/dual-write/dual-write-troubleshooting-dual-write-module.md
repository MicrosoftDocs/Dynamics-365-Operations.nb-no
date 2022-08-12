---
title: Feilsøk problemer med dobbel skriving i økonomi- og driftsapper
description: Denne artikkelen inneholder feilsøkingsinformasjon som kan hjelpe deg med å løse problemer med dobbel skriving-modulen i økonomi- og driftsapper.
author: RamaKrishnamoorthy
ms.date: 04/18/2022
ms.topic: article
audience: Application User, IT Pro
ms.reviewer: tfehr
ms.search.region: global
ms.author: ramasri
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: 2743b99538b332af7cc6ad8d951eede562c14235
ms.sourcegitcommit: 6781fc47606b266873385b901c302819ab211b82
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/02/2022
ms.locfileid: "9111178"
---
# <a name="troubleshoot-dual-write-issues-in-finance-and-operations-apps"></a>Feilsøk problemer med dobbel skriving i økonomi- og driftsapper

[!include [banner](../../includes/banner.md)]



Denne artikkelen inneholder feilsøkingsinformasjon om integrasjon av dobbel skriving mellom økonomi- og driftsapper og Dataverse. Mer spesifikt gir det informasjon som kan hjelpe deg med å løse problemer med **Dobbel skriving**-modulen i økonomi- og driftsapper.

> [!IMPORTANT]
> Noen av problemene som denne artikkelen løser, kan kreve administratorrollen for systemet eller legitimasjon for Microsoft Azure Active Directory (Azure AD)-leieradministrator. Delen for hvert problem forklarer om en bestemt rolle eller legitimasjon er nødvendig.

## <a name="you-cant-load-the-dual-write-module-in-a-finance-and-operations-app"></a>Du kan ikke laste inn dobbel skriving-modulen i en økonomi- og driftsapp

Hvis du ikke kan åpne **Dobbel skriving**-siden ved å velge **Dobbel skriving**-flisen i **Databehandling**-arbeidsområdet, er dataintegrasjonstjenesten sannsynligvis nede. Opprett en støtteforespørsel for å be om omstart av dataintegrasjonstjenesten.

## <a name="error-when-you-try-to-create-a-new-table-map"></a>Feil når du prøver å opprette en ny tabelltilordning

**Påkrevd legitimasjon for å løse problemet:** Den samme brukeren som konfigurere dobbelt skriving.

Du kan få følgende feilmelding når du prøver å konfigurere en ny tabell for dobbel skriving. Den eneste brukeren som kan opprette en tilordning, er brukeren som konfigurere dobbelt skriving-forbindelsen.

*Svarstatuskoden indikerer ikke fullført: 401 (uautorisert).*

## <a name="error-when-you-open-the-dual-write-user-interface"></a>Feil når du åpner bruker grensesnittet for dobbel skriving

Du kan få følgende feilmelding når du prøver å få tilgang til dobbel skriving fra arbeidsområdet **Databehandling**:

*login.microsoftonline.com kunne ikke koble til.*

Du kan løse problemet ved å logge på ved å bruke et InPrivate-vindu i Microsoft Edge, et inkognito-vindu i Chromium, eller et inkognito-vindu i Google Chrome. Du må også oppheve blokkeringen eller fjerne tredjeparts informasjonskapsler.

## <a name="error-when-you-link-the-environment-for-dual-write-or-add-a-new-table-mapping"></a>Feil når du kobler miljøet for dobbel skriving eller legger til en ny tabelltilordning

**Nødvendig rolle for å løse problemet:** Systemadministrator både i økonomi- og driftsapper og Dataverse.

Du kan støte på følgende feilmelding når du kobler eller oppretter tilordninger:

```dos
Response status code does not indicate success: 403 (tokenexchange).
Session ID: \<your session id\>
Root activity ID: \<your root activity\> id
```

Denne feilen kan oppstå hvis du ikke har tilstrekkelige tillatelser til å koble dobbel skriving eller opprette tilordninger. Denne feilen kan også oppstå hvis Dataverse-miljøet ble tilbakestilt uten å koble fra dobbel skriving. Alle brukere med rollen systemansvarlig både i økonomi- og driftsapper og Dataverse kan koble sammen miljøer. Bare brukeren som konfigurerte dobbel skriving-tilkoblingen, kan legge til nye tabelltilordninger. Etter installasjonen kan alle brukere med rollen systemansvarlig overvåke statusen og redigere tilordningene.

## <a name="error-when-you-stop-the-table-mapping"></a>Feil når du stopper tabelltilordningen

Du kan få følgende feilmelding når du prøver å stoppe tabelltilordningene:

*\[Forbudt\], \[{"status":403,"kilde":"","melding":"Feil fra token-utveksling: Brukeren har ikke tilgang til tilkoblingen dynamicscrmonline/xxxxxx-xxxx-xxxx-xxxxxxxx"}\], Den eksterne serveren returnerte en feil: (403) Forbidden.*

Denne feilen oppstår når det koblede Dataverse-miljøet ikke er tilgjengelig.

Du kan løse problemet ved å opprette en støtteforespørsel for data integrasjonsgruppen. Knytt til nettverkssporingen slik at dataintegrasjonsgruppen kan merke tilordningene som **Kjører ikke** i serverdelen.

## <a name="enable-parallel-processing-in-finance-and-operations-apps-to-improve-performance"></a>Aktiver parallell behandling i økonomi- og driftsapper for å forbedre ytelsen

Ved å aktivere parallell behandling kan du redusere tiden det tar å importere data fra Dynamics 365-kundeengasjementsapper og Microsoft Dataverse til økonomi- og driftsapper. 

Fullfør trinnene nedenfor for å aktivere parallell behandling i økonomi- og driftsapper.

1. Logg på Finance and Operations-miljøet.
2. Gå til **Dataadministrasjon > Rammeverkparametere**.
3. Velg **Enhetsinnstillinger**, og velg **Konfigurer parametere for utføring av enhet**.
4. Legg til parameterne for parallell behandling:
    - **Antall poster for importterskel** – Antall poster som må oppfylles før parallell behandling aktiveres.
    - **Antall importoppgaver** – Antall tråder (oppgaver) som skal kjøres parallelt.
5. Velg **Lagre**.


## <a name="errors-while-trying-to-start-a-table-mapping"></a>Feil under forsøk på å starte en tabelltilordning

### <a name="unable-to-complete-initial-data-sync"></a>Kan ikke fullføre innledende datasynkronisering

Du kan få en feil søm følgende når du prøver å kjøre den innledende datasynkroniseringen:

*Kan ikke fullføre den opprinnelige datasynkroniseringen. Feil: dobbelt skriving feil - registrering av plugin-modul mislyktes: kan ikke opprette metadata for oppslag med dobbel skriving. Feilobjektreferanse er ikke satt til en forekomst av et objekt.*

Når du forsøker å angi denne tilstanden for en tilordning til **Kjører**, kan du få følgende feil: Hurtigreparasjonen er avhengig av årsaken til feilen:

+ Hvis tilordningen har avhengige tilordninger, må du sørge for å aktivere de avhengige tilordningene for denne tabelltilordningen.
+ Tilordningen kan mangle kilde- eller målkolonner. Hvis en kolonne i økonomi- og driftsappen mangler, følger du trinnene i delen [Problemer med manglende tabellkolonner i tilordninger](dual-write-troubleshooting-finops-upgrades.md#missing-table-columns-issue-on-maps). Hvis det mangler en kolonne i Dataverse, klikker du på **Oppdater tabeller**-knappen for tilordningen, slik at kolonnene fylles ut automatisk i tilordningen på nytt.

### <a name="version-mismatch-error-and-upgrading-dual-write-solutions"></a>Feil med versjonskonflikt og oppgradering av løsninger for skrivefeil for skriveversjon

Du kan få følgende feilmeldinger når du prøver å kjøre tabelltilordningene:

+ *Kundegrupper (msdyn_customergroups): Dobbel skriving-feil – Dynamics 365 for Sales-løsningen "Dynamics365Company" har versjonskonflikt. Versjon: 2.0.2.10, påkrevd versjon: 2.0.133*
+ *Dynamics 365 for Sales-løsningen Dynamics365FinanceExtended har versjonskonflikt. Versjon: 1.0.0.0, påkrevd versjon: 2.0.227*
+ *Dynamics 365 for Sales-løsningen Dynamics365FinanceAndOperationsCommon har versjonskonflikt. Versjon: 1.0.0.0, påkrevd versjon: 2.0.133*
+ *Dynamics 365 for Sales-løsningen CurrencyExchangeRates har versjonskonflikt. Versjon: 1.0.0.0, påkrevd versjon: 2.0.133*
+ *Dynamics 365 for Sales-løsningen Dynamics365SupplyChainExtended har versjonskonflikt. Versjon: 1.0.0.0, påkrevd versjon: 2.0.227*

For å løse problemene må du oppdatere dobbel skriving-løsningene i Dataverse. Sørg for å oppgradere til den nyeste løsningen som samsvarer med den nødvendige løsningsversjonen.

[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]

