---
title: Forhåndsversjon av Dynamics 365 Commerce 10.0.30 (november 2022)
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Commerce 10.0.30.
author: josaw1
ms.date: 12/07/2022
ms.topic: article
audience: Application User
ms.reviewer: josaw
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2022-09-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: a449c7eff21c059555f9659ea932705858d26275
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831754"
---
# <a name="preview-of-dynamics-365-commerce-10030-november-2022"></a>Forhåndsversjon av Dynamics 365 Commerce 10.0.30 (november 2022)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Commerce, forhåndsversjon 10.0.30. Denne versjonen har et build-nummer 10.0.1362, og er tilgjengelig på følgende tidsplan:

- **Forhåndsversjon:** september 2022
- **Allmenn tilgjengelighet for versjon (selvoppdatering):** oktober 2022
- **Allmenn tilgjengelighet for versjon (automatisk oppdatering):** november 2022

## <a name="features-included-in-this-release"></a>Funksjoner inkludert i denne versjonen

Denne tabellen viser funksjonene i denne versjonen. Denne artikkelen kan være oppdatert for å inkludere funksjoner som ble lagt til i builden etter at denne artikkelen opprinnelig ble publisert.

| Funksjonsområde | Funksjon | Mer informasjon | Aktivert av   |
|---------|------------------|----------------|--------------| 
| Kundestøtte   | Chat på et e-handelsområde ved hjelp av en Power Virtual Agents-robot. | Denne funksjonen gjør at brukere på et e-handelsområde kan velge om de vil bruke en Power Virtual Agents-chatrobot til støtteforespørsler. | Aktiveres av administratorer/utviklere for sluttbrukere |
| Innsikt  |  Strøm driftsinnsiktshendelser for salgssted til Application Insights-kontoen. | [Få tilgang til logger i Application Insights](../dev-itpro/operational-insights.md#enable-diagnostic-events-in-application-insights)   |  Valg for IT-ekspert/utvikler   |
|  Betalinger  | PayPal-ordrestøtte utover 29-dagers autorisasjonsperiode. | Den maksimale autorisasjonsperioden for PayPal er 29 dager, og deretter må en ny autorisasjon og ordre-ID genereres. PayPal tilbyr et alternativ til dette der det kan henvises til en PayPal-ordre som en generell ordre, som tillater flere autorisasjoner og registreringer mot samme ordre-ID, i stedet for at det genereres en ny autorisasjon og ordre-ID etter 29 dager). | Når du konfigurerer PayPal-betalingskoblingen i Commerce headquarters, er feltet **OrderIntent** lagt til, og det kan inneholde to verdier:<p><p>- **Autoriser** – Denne konfigurasjonen er standard (hvis feltet er tomt, fungerer **Autoriser** som standard). Hvis du konfigurerer **OrderIntent** til **Autoriser**, korrelerer dette med PayPal-verdien **NO_INSTRUCTION** for **processing_instruction**. Ordren autoriseres med PayPal, og autorisasjonen kan ikke endres når denne verdien brukes.<p>- **Lagre** – Når **OrderIntent**-verdien er satt til **Lagre**, korrelerer dette med PayPal-verdien **ORDER_SAVED_EXPLICITLY** for **processing_instruction**. Ordrereferanser lagres i PayPal-tjenesten når denne verdien brukes.  |
| Pålogging på salgssted  | [Aktiver funksjoner for selvbetjent diagnose for pålogging på salgssted](/dynamics365-release-plan/2022wave2/commerce/dynamics365-commerce/enable-self-serve-diagnosis-capabilities-pos-sign-in)  |  Denne funksjonen gir funksjoner for selvbetjent diagnose på salgsstedet og i Commerce headquarters, slik at butikkansatte og -sjefer raskt kan identifisere og rette de underliggende årsakene til påloggingsproblemer på salgsstedet.<p><p>- Feilmeldingene som vises på påloggingsskjermen på salgsstedet ble forbedret for å gi konkret informasjon om den underliggende årsaken, slik at det blir enklere for butikkansatte å gjør det som trengs for å løse problemet.<p>- Funksjonen **Test pålogging** er tilgjengelig på **Arbeidere**-siden i Commerce headquarters, slik at butikksjefer som konfigurerer salgsstedsenheter, kan simulere salgsstedspålogging. Hvis det oppstår en påloggingsfeil, omfatter denne funksjonen gjennomførbare feilsøkingsveiledninger, slik at sjefer kan kontrollere relevante konfigurasjoner, løse problemer og validere rettelsene.  | Aktivert som standard |


## <a name="additional-resources"></a>Tilleggsressurser

### <a name="platform-updates-for-finance-and-operations-apps"></a>Platformoppdateringer for økonomi- og driftsapper

Dynamics 365 Finance 10.0.30 inneholder plattformoppdateringer. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.30 av økonomi- og driftsapper](../../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-30.md).

### <a name="bug-fixes"></a>Feilrettinger

Hvis du vil ha informasjon om feilrettinger som er inkludert i hver av oppdateringene som er en del av versjon 10.0.30, logger du på Lifecycle Services (LCS) og ser [KB-artikkelen](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468). 

### <a name="dynamics-365-and-industry-clouds-2022-release-wave-2-plan"></a>Dynamics 365 og bransjeskyer: plan for lanseringsbølge 2 for 2022

Er du spent på kommende og nylig utgitte tilleggspakkefunksjoner i våre bedriftsprogrammer eller -plattform?

Sjekk ut [Dynamics 365 og bransjeskyer: plan for lanseringsbølge 2 for 2022](/dynamics365-release-plan/2022wave2/). Vi har registrert alle detaljene, ende til ende, øverst til nederst, i et enkelt dokument som du kan bruke i planleggingen.

### <a name="removed-and-deprecated-features"></a>Funksjoner som er fjernet og avskrevet

Artikkelen [Funksjoner som er fjernet eller avskrevet i Dynamics 365 Commerce](removed-deprecated-features-commerce.md) beskriver funksjoner som er fjernet eller avskrevet for Commerce.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Før en funksjon fjernes fra produktet, vil avskrivningsvarselet bli kunngjort i artikkelen [Fjernede eller avskrevne funksjoner i Dynamics 365 Commerce](removed-deprecated-features-commerce.md) 12 måneder før fjerningen.

For oppdelingsendringer som bare påvirker kompileringstiden, men som er binære kompatible med sandkasse- og produksjonsmiljøer, vil avskrivningstiden være mindre enn 12 måneder. Dette er vanligvis funksjonelle oppdateringer som må gjøres på kompilatoren.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
