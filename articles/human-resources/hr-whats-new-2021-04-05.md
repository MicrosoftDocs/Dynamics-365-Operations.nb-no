---
title: Hva er nytt eller endret i Dynamics 365 Human Resources, 5. april 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 5. april 2021.
author: marcelbf
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 879a500c187e7b0a11d367c4a12618a9c60c98b7
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056474"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-5-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources, 5. april 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4074.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Du kan hindre at ansatte redigerer kontaktdetaljer for virksomhet. | [Begrense at ansatte redigerer kontaktdetaljer for virksomhet.](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Begrense redigering av personlige opplysninger](./hr-employee-self-service-restrict-editing.md)|

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdateringer for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem |  beskrivelse |
| --- | --- | --- |
| 550852 | **Godkjenning**-knappen validerer ikke med obligatoriske felt angitt i **Gjennomgang**-skjemaet. | Når du angir et felt i **Gjennomgang**-skjemaet som obligatorisk og publiserer endringene for lederrollen, valideres ikke skjemaet som forventet. |
| 559564 | Historiske arbeiderhandlinger for endring i fast kompensasjon gir feil for avsluttede brukere. | Arbeiderhandling for en avsluttet ansattkompensasjon gir en feil. Når en ansatt har sluttet, gir den ansattes handling for kampanjen før oppsigelse en feil. |
| 560074 | Rullegardinlisten for ansattkategori er ikke filtrert etter **arbeidertype** og viser kategorier for ansatte og oppdragstakere. | På **Ansatt**-skjemaet skal rullegardinlisten **Ansettelseskategori** vise ansatt- eller oppdragstakerkategorier, basert på den ansattes arbeidertype. |
| 567388 | Noe av informasjonen for nyopprettede ansatte synkroniseres ikke umiddelbart i tabellen **cdm_worker** i Dataverse. | Når du oppretter en ny ansattpost, blir den nye posten synkronisert til tabellen **cdm_worker** i Dataverse, men ikke alle egenskapene vil bli inkludert i Dataverse-posten. |
| 563837 | Funksjoner som ikke er tilgjengelige i Human Resources-visningen. | Flere funksjoner som ikke gjelder for Human Resources, vises i Funksjonsadministrasjon. Disse funksjonene er nå fjernet fra listen over tilgjengelige funksjoner som kan aktiveres i Human Resources. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |

## <a name="coming-soon"></a>Kommer snart

| Funksjon | Detaljer |
| --- | --- |
| Ferdigheter som angis av en leder for de ansatte, kan godkjennes automatisk av en arbeidsflyt | Kommer snart. |
| Platform update 10.0.17 (41) | Plattformoppdatering 10.0.17 planlegges å rulle ut med neste versjon 19. april 2021. Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.17 av Finance and Operations-apper (april 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md). |

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 1 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]