---
title: Hva er nytt eller endret i Dynamics 365 Human Resources, 19. april 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 19. april 2021.
author: marcelbf
ms.date: 04/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6734069b1448999c62a8c538f97d786fc10995e5
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8685749"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources, 19. april 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4113.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Platform update 10.0.17 (41) | -- | [Plattformoppdateringer for versjon 10.0.17 av økonomi- og driftsapper (april 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| Egendefinerte felt-støtte i fordelsbehandlingsskjemaer | [Egendefinerte felt-støtte i fordelsbehandlingsskjemaer](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [Oversikt over fordelsbehandling](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdateringer for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem |  beskrivelse |
| --- | --- | --- |
| 552164 | **Lagret visning** på **Ansattselvbetjening > Åpne kurs** fungerer ikke for kurs som inneholder en agenda | Hvis en lagret visning brukes på Åpne kurs (ESS), og ett av kursene har en tilknyttet agenda, vil ikke visningen lenger vise flere linjer for dette kurset |
| 560614 | **Fordeler > Alternativer for livshendelser** viser avvik i verktøytipsdokumentasjonen og kodevirkemåten. | Oppdaterte verktøytips i **Alternativer for livshendelser** viser riktig virkemåte. |
| 560616 | **Fordeler > Alternativer for livshendelser** kan redigeres i planen for arbeiderfordeler, men endringene berøres ikke. | Oppdatert virkemåte for alternativ for livshendelse bytter til å aktivere eller deaktivere basert på avhengige alternativer per verktøytipsdokumentasjon. |
| 565054 | Kan ikke vise **Arbeidere uten ansettelse**-listeinnholdet når **Avansert tilgang** er på. | Denne versjonen retter problemet da **Avansert tilgang** ble aktivert og bare systemadministratorer kunne vise innholdet i listen **Arbeidere uten ansettelse**. Siden denne reparasjonen er en sikkerhetsendring, må du velge den i Funksjonsbehandling. Når funksjonen er på, vil de rollene som har tilgang til skjemaet, se innholdet, selv om avansert tilgang er på. Hvis du vil ha mer informasjon, kan du se [Arbeidere uten ansettelse](hr-personnel-workers-without-employment.md). |
| 570586 | Permisjonsforespørselsvalidering mislykkes når ansettelsen avsluttes før den siste transaksjonen for denne arbeideren på tvers av alle permisjonsplanene. | Når en ansettelse avsluttes, mislykkes ikke validering av forespørselen basert på ansattes permisjonstransaksjoner.|
| 570783 | Ved å aktivere og deaktivere permisjon på tvers av firmaer i Personale endrer delte parametere hva ansatte i ett enkelt firma ser i permisjonsforespørsler. | Ansatte som er ansatt i ett enkelt firma, ser ingen endringer i å be om fri hvis parameteren er aktivert eller deaktivert. |
| 572343 | Påkrevd årsakskode vises ikke når funksjonen for permisjonsvisning på tvers av firmaer er aktivert. | Når funksjonen for permisjonsvisning på tvers av firmaer er aktivert, vises nå årsakskode som forventet. |
| 573676 | Kan ikke legge til **Periode** i **Fordelsbehandling > Koblinger > Fordelsplaner**. | Reparerte feil der **Periode** ikke kunne legges til eller oppdateres på eksisterende **Fordelsplan**-skjerma. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |
| Forbedringer i permisjon og fravær-arbeidsflyt | [Forbedringer i permisjon og fravær-arbeidsflyt](https://go.microsoft.com/fwlink/?linkid=2147528) | [Be om fritid](hr-employee-self-service-request-time-off.md)|
| Aktivere forenklet lønnsintegrering (APIer for lønnsintegrering) | [Aktiver forenklet integrering med lønnsleverandører](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>Kommer snart

| Funksjon | Detaljer |
| --- | --- |
| Ferdigheter som angis av en leder for de ansatte, kan godkjennes automatisk av en arbeidsflyt | Kommer snart. |
| Platform update 10.0.18 (42) | Plattformoppdatering 10.0.18 planlegges å rulle ut med serviceversjon 17. mai 2021. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.18 av økonomi- og driftsapper (mai 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Egendefinerte felt-støtte i rettighetsregler for fordelsbehandling  | [Egendefinert felt-støtte for rettighetsbehandling](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 1 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
