---
title: Oppdatere prosess
description: Microsoft Dynamics 365 Human Resources er ekte programvare som tjeneste (SaaS) som gir kontinuerlige, berøringsfrie serviceoppdateringer for program- og plattformendringer.
author: twheeloc
ms.date: 12/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-27
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 197b3c5717494ab3c80a57cda337a9021293bf73
ms.sourcegitcommit: 68efa7b89273d04484566cbe14d3533a8fd4ee53
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/02/2022
ms.locfileid: "9819303"
---
# <a name="update-process"></a>Oppdatere prosess

_**Gjelder For:** Human Resources i den frittstående infrastrukturen_ 

> [!NOTE]
> Fra og med juli 2022 kan ikke nye Human Resources-miljøer klargjøres i den frittstående Human Resources-infrastrukturen, og nye Microsoft Dynamics Lifecycle Services-prosjekter (LCS) kan ikke opprettes i den. Kunder kan distribuere Human Resources-miljøer i infrastrukturen i Finance and Operations. Hvis du vil ha mer informasjon , kan du se [Klargjøring av Human Resources i infrastrukturen i Finance and Operations](hr-admin-setup-provision-fo.md).

> [!IMPORTANT]
> Oppdaterings- og hurtigreparasjonsprosessen i infrastrukturen for økonomi- og driftsapper er forskjellig fra den frittstående oppdaterings- og hurtigreparasjonsprosessen i Human Resources. Hvis du vil ha mer informasjon om oppdateringsprosessen, kan du se [Prosess for å flytte til den nyeste versjonen av Finance and Operations](../fin-ops-core/dev-itpro/migration-upgrade/upgrade-latest-update.md). Hvis du vil ha mer informasjon om hurtigreparasjoner, kan du se [Laste ned oppdateringer fra Lifecycle Services (LCS)](/fin-ops-core/dev-itpro/migration-upgrade/download-hotfix-lcs.md). 

Microsoft Dynamics 365 Human Resources er ekte programvare som tjeneste (SaaS) som gir kontinuerlige, berøringsfrie serviceoppdateringer. Disse oppdateringene inneholder både program- og plattformendringer som ofte gir kritiske forbedringer av tjenesten, inkludert forskriftsmessige oppdateringer.

## <a name="update-policy"></a>Oppdateringspolicy

Oppdateringer utgis regelmessig for alle miljøer. Human Resources støttes i henhold til [Microsoft Lifecycle-policyen](https://support.microsoft.com/hub/4095338/microsoft-lifecycle-policy), som gir konsekvente og forutsigbare retningslinjer for tilgjengelighet av produktstøtte.

## <a name="release-cadence"></a>Lanseringsfrekvens 

Human Resources-oppdateringer brukes for alle miljøer automatisk. Human Resources har to typer lanseringer:

- **Serviceoppdateringer**: Serviceoppdateringer omfatter også aktuelle plattformoppdateringer når de frigis. I tillegg til unntaksbaserte oppdateringer forekommer regelmessige serviceoppdateringer etter allmenn tilgjengelighet for Dynamics 365 Finance-oppdateringer. Hvis du vil ha mer informasjon om plattformversjoner, kan du se [Hva er nytt eller endret i plattformoppdateringer](../fin-ops-core/dev-itpro/get-started/whats-new-home-page.md). Oppdateringer har en trinnvis, global distribusjon på tvers av områder. Hvis du vil ha mer informasjon om oppdateringer, kan du se [Hva er nytt eller endret i Dynamics 365 Human Resources](hr-admin-whats-new.md).

- **Dataverse-løsningsoppdateringer**: Disse oppdateringene inntreffer omtrent hver sjette uke etter behov. De inneholder nye enheter og endringer i eksisterende enheter i Dataverse. Disse oppdateringene utgis i de samme regionene som oppdateringene annenhver uke, og de tar omtrent seks uker på å replisere gjennom alle datasentre. Løsningsoppdateringer kan være rettet inn mot serviceoppdateringer annenhver uke.

> [!NOTE]
> Løsningsoppdateringer er tilgjengelige på alle datasentrene når de er frigitt. Hvis du ikke vil vente på at oppdateringene skal replikeres automatisk, kan du bruke disse oppdateringene manuelt på alle miljøer i alle datasentre.

Når det er nødvendig, tilbyr Human Resources følgende typer korrigeringer:

- **Revisjon (hurtigreparasjon**): Feilrettinger som kan forekomme sammen med eller utenfor en serviceoppdatering annenhver uke

- **Nødreparasjon**: Proaktive og reaktive hurtigreparasjoner som er frittstående av natur, kan inkludere endringer bare i konfigurasjon eller kodeendringer for å løse problemer på områder direkte, og kan forekomme i stedet for en serviceoppdatering annenhver uke

Versjoner er gjennomgått, testet og godkjent i et internt miljø. Etter at buildene er godkjent, distribueres de deretter til produksjon.

## <a name="communications"></a>Kommunikasjon

Du kan finne ut hva vi arbeider med for Human Resources, og hva vi har utgitt på følgende steder:

- [Dynamics 365 Human Resources-veikart](https://dynamics.microsoft.com/roadmap/human-resources/)

- [Lanseringsplaner for Dynamics 365](/dynamics365/release-plans/)

- [Hva er nytt eller endret i Dynamics 365 Human Resources](hr-admin-whats-new.md)

- [Problemsøk i Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/issue-search-lcs.md) (bare for feil relatert til plattform)

- [Human Resources-blogg](https://community.dynamics.com/365/talent/b/dynamics365fortalent)

- [Human Resources Yammer-samfunn](https://www.yammer.com/dynamicsaxfeedbackprograms/#/threads/inGroup?type=in_group&feedId=10542230)

## <a name="preview-features-in-a-sandbox-environment"></a>Forhåndsversjoner av funksjoner i et sandkassemiljø

Du kan validere forhåndsversjoner av funksjoner i et sandkassemiljø før du aktiverer dem i produksjonsmiljøet. Hvis du vil ha mer informasjon om hvordan du aktiverer funksjoner, kan du se [Oversikt over funksjonsbehandling](../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Alle nye funksjoner blir forhåndsvist i minst 30 dager, og vanligvis 30-60 dager. Større funksjoner er vanligvis tilgjengelig i oktober og april i hvert år etter forhåndsvisningsperioden. Så snart du ser nye funksjoner i arbeidsområdet for **funksjonsbehandling**, kan du aktivere dem. Det kan hende at noen funksjoner er aktivert som standard.

Noen ganger vil en integrert funksjon være aktivert som standard og kan ikke deaktiveres (for eksempel arbeidsområdet Funksjonsbehandling).

Når en funksjon er generelt tilgjengelig, kan den aktiveres eller deaktiveres i produksjonsmiljøer. Arbeidsområdet for **funksjonsbehandling** angir når en forhåndsvisningsfunksjon blir obligatorisk. Denne datoen er vanligvis 1. oktober eller 1. april for å justeres med de halvårlige frigivelsesplanene. De kan ikke deaktivere obligatoriske funksjoner. Før den blir obligatorisk, kan du slå en funksjon på og av i alle miljøer.

Det anbefales på det sterkeste forhåndsversjoner av funksjoner i et sandkasse- eller prøvemiljø. Det er best å opprette en kopi av gjeldende produksjonsmiljø eller database i et sandkassemiljø, slik at du får den komplette opplevelsen av de nye funksjonene med dataene dine.

Hvis du vil ha mer informasjon om hvordan du klargjør et sandkassemiljø, kan du se [Klargjøre et Human Resources-prosjekt](hr-admin-setup-provision.md). Hvis du vil fjerne et testmiljø, kan du se [Fjerne en forekomst](hr-admin-setup-remove-instance.md#remove-a-test-drive-environment). 

## <a name="report-bugs"></a>Rapportere feil

Når du tester forhåndsversjoner av funksjoner eller prøver nye funksjoner, kan det hende at du finner elementer som ikke fungerer som forventet. Vi ber deg om å rapportere alle feil gjennom [Microsoft Dynamics 365-støtte](https://dynamics.microsoft.com/support/).

## <a name="see-also"></a>Se også

[Lanseringsplaner for Dynamics 365 og Power Platform](/dynamics365/release-plans)</br>
[Hva er nytt eller endret i Dynamics 365 Human Resource](hr-admin-whats-new.md)</br>
[Policy for programvarelivssyklus](../fin-ops-core/dev-itpro/migration-upgrade/versions-update-policy.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
