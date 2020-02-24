---
title: Oppdateringsprosess
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1817e072805bafbf0d5a9eb2698ef75abc75ad68
ms.sourcegitcommit: 4e62c22b53693c201baa646a8f047edb5a0a2747
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/07/2020
ms.locfileid: "3031096"
---
# <a name="update-process"></a>Oppdateringsprosess

Microsoft Dynamics 365 Human Resources er ekte programvare som tjeneste (SaaS) som gir kontinuerlige, berøringsfrie serviceoppdateringer. Disse oppdateringene inneholder både program- og plattformendringer som ofte gir kritiske forbedringer av tjenesten, inkludert forskriftsmessige oppdateringer.

## <a name="update-policy"></a>Oppdateringspolicy

Oppdateringer utgis regelmessig for alle miljøer. Human Resources støttes i henhold til [Microsoft Lifecycle-policyen](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), som gir konsekvente og forutsigbare retningslinjer for tilgjengelighet av produktstøtte.

## <a name="release-cadence"></a>Lanseringsfrekvens

Human Resources-oppdateringer brukes for alle miljøer automatisk. Human Resources har to typer lanseringer:

- **Serviceoppdateringer**: ukentlige oppdateringer som inneholder feilrettinger og nye funksjoner. Serviceoppdateringer omfatter også aktuelle plattformoppdateringer når de frigis. For en oversikt over når plattformoppdateringer frigis, se [Tabell 3: Plattformutgaver](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy#table-3-platform-releases). Ukentlige oppdateringer frigir vanligvis på onsdager. Hvis du vil ha mer informasjon om ukentlige oppdateringer, kan du se [Hva er nytt eller endret i Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365/talent/whats-new).

    Alle støttede datasentre oppdateres ukentlig med mindre annet er angitt. Ukentlige oppdateringer begynner vanligvis på onsdager og fullføres søndager. USA, Australia, Europa, Storbritannia, Asia og Canada er inkludert i ukentlige oppdateringer. 

- **Common Data Service-løsningsoppdateringer**: Disse oppdateringene inntreffer omtrent hver sjette uke etter behov. De inneholder nye enheter og endringer i eksisterende enheter i Common Data Service. Disse oppdateringene utgis i de samme regionene som de ukentlige oppdateringene, og de tar omtrent seks uker på å replisere gjennom alle datasentre. Løsningsoppdateringer kan være rettet inn mot ukentlige serviceoppdateringer.

Følgende tabell viser et eksempel på en tidsplan:

| Uke | Oppdateringstype |
| --- | --- |
| 1 | Serviceoppdatering (alle områder) |
| 2 | Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 1) |
| 3 | Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 2) |
| 4 | Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 3) |
| 5 | Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 4) |
| 6 | Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 5) |
| 7 | Serviceoppdatering (alle områder) + løsningsoppdatering (områder i uke 6) |
| 8 | Serviceoppdatering (alle områder) |

> [!NOTE]
> Løsningsoppdateringer er tilgjengelige på alle datasentrene når de er frigitt. Hvis du ikke vil vente på at oppdateringene skal replikeres automatisk, kan du bruke disse oppdateringene manuelt på alle miljøer i alle datasentre.

Når det er nødvendig, tilbyr Human Resources også følgende typer korrigeringer:

- **Revisjon (hurti reparasjon**): feilrettinger som kan forekomme sammen med eller utenfor en ukentlig serviceoppdatering

- **Nødreparasjon**: proaktive og reaktive hurtigreparasjoner som er frittstående av natur, kan inkludere endringer bare i konfigurasjon eller kodeendringer for å løse problemer på områder direkte, og kan forekomme i stedet for en ukentlig serviceoppdatering

Versjoner er gjennomgått, testet og godkjent i et internt miljø. Etter at buildene er godkjent, distribueres de deretter til produksjon.

## <a name="exceptions-in-2019"></a>Unntak i 2019

Følgende datoer er unntak fra den vanlige utgivelsesplanen:

| Dato | Beskrivelse |
| --- | --- |
| Uken fra 25. november | Ingen oppdateringer |
| Uken fra 16. desember | Bare mindre oppdateringer |
| Uken fra 23. desember | Ingen oppdateringer |
| Uken fra 30. desember | Ingen oppdateringer |

## <a name="communications"></a>Kommunikasjoner

Du kan finne ut hva vi arbeider med for Human Resources, og hva vi har utgitt på følgende steder:

- [Dynamics 365 Human Resources-veikart](https://dynamics.microsoft.com/roadmap/talent/)

- [Lanseringsplaner for Dynamics 365](https://docs.microsoft.com/dynamics365/release-plans/)

- [Hva er nytt eller endret i Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Problemsøk i Lifecycle Services (LCS)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs) (bare for feil relatert til plattform)

- [Human Resources-blogg](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer-samfunn](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Forhåndsversjoner av funksjoner i et sandkassemiljø

Du kan validere forhåndsversjoner av funksjoner i et sandkassemiljø før du aktiverer dem i produksjonsmiljøet. Hvis du vil ha mer informasjon om hvordan du aktiverer funksjoner, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).

Alle nye funksjoner blir forhåndsvist i minst 30 dager, og vanligvis 30-60 dager. Større funksjoner er vanligvis tilgjengelig i oktober og april i hvert år etter forhåndsvisningsperioden. Så snart du ser nye funksjoner i arbeidsområdet for funksjonsbehandling, kan du aktivere dem. Det kan hende at noen funksjoner er aktivert som standard.

Noen ganger vil en integrert funksjon være aktivert som standard og kan ikke deaktiveres (for eksempel arbeidsområdet Funksjonsbehandling).

Når en funksjon er generelt tilgjengelig, kan den aktiveres eller deaktiveres i produksjonsmiljøer. Arbeidsområdet for funksjonsbehandling angir når en forhåndsvisningsfunksjon blir obligatorisk. Denne datoen er vanligvis 1. oktober eller 1. april for å justeres med de halvårlige frigivelsesplanene. De kan ikke deaktivere obligatoriske funksjoner. Før den blir obligatorisk, kan du slå en funksjon på og av i alle miljøer.

Vi anbefaler på det sterkeste forhåndsversjoner av funksjoner i et sandkasse- eller prøvemiljø. Det er best å opprette en kopi av gjeldende produksjonsmiljø eller database i et sandkassemiljø, slik at du får den komplette opplevelsen av de nye funksjonene med dataene dine.

Hvis du vil ha mer informasjon om hvordan du klargjør et sandkassemiljø, kan du se [Klargjøre et Human Resources-prosjekt](hr-admin-setup-provision.md). Hvis du vil fjerne et testmiljø, kan du se [Fjerne en forekomst](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Rapportere feil

Når du tester forhåndsversjoner av funksjoner eller prøver nye funksjoner, kan det hende at du finner elementer som ikke fungerer som forventet. Vi ber deg om å rapportere alle feil gjennom [Microsoft Dynamics 365-støtte](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Se også

- [Lanseringsplaner for Dynamics 365 og Power Platform](https://docs.microsoft.com/dynamics365/release-plans)
- [Hva er nytt eller endret i Dynamics 365 Human Resource](hr-admin-whats-new.md)
- [Policy for programvarelivssyklus](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy)

