---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 12. juli 2021
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 12. juli 2021.
author: marcelbf
ms.date: 07/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-07-12
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d7fb922a35504b69aa8cc3d92cb981e8fb060290
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/29/2022
ms.locfileid: "9067594"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-july-12-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 12. juli 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4353.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
|  Arbeidserfaring-visning veksler | |Ved hjelp av denne funksjonen kan du bruke forskjellige datoer til å beregne arbeidserfaring som vises på siden **Strømlinjeformet ansattoppføring** og på siden **Personer**.  Dette vil være tilgjengelig i [parametere for Human Resources](/dynamics365/human-resources/hr-setup-parameters). |


### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Denne artikkelen kan være oppdatert for å inkludere feilrettingsfiler som ble tatt med i builden etter at denne artikkelen ble publisert.

| Utstedelsesnummer | Problem |  Beskrivelse |
| --- | --- | --- |
| 595871 | Ruten Om i Human Resources har feil Dataverse-terminologi | Etter endring av Common Data Service til Dataverse er terminologi oppdatert i Microsoft Dynamics 365 Human Resources-informasjonsruten (**Hjelp og støtte > Om**). |
| 598676 | Oppgaven med skjemaet for strømlinjeformet ansattoppføring kan opprette en feil når det brukes med lagret visning| Hvis "Strømlinjeformet ansattoppføring" er aktivert på siden **Arbeider**, kan programmet mislykkes hvis **Alltid åpen for redigering** er satt i lagret visning. |
| 592344 |Delen Kompensasjon for arbeidere om stilling bør bare leses når fordelsstyring er aktivert | Informasjon om kompensasjon for arbeidere opprettes ved hjelp av eldre fordeler-funksjonalitet.  Når fordelsstyring er aktivert, er feltene skrivebeskyttet. Når fordelsstyring er aktivert og **Skjul eldre fordelsskjemaer** er satt til **Ja** i delte parametere for personale, skjules kategorien **Kompensasjon for arbeidere**. |
| 598617 | Kategorien for aktivering av **HcmDiscussion**-skjema forårsaker ubegrenset løkke når tilpasninger brukes | Når både rutenett- og detaljervisningen har **Alltid er åpen for redigering** aktivert, vil koden som aktiverer kategorien i den overstyrte oppgavemetoden, være i konflikt med tilpasningen av hvilken kontroll som bør ha fokus, og oppretter en ubegrenset løkke. |
| 593553 | Journaldato-feltet i ytelsesjournalen vises i UTC | **Journaldato**-feltet for ytelsesjournaler vises i UTC-tidssonen i stedet for tidssonen som er definert i systemdatooppsettet, noe som fører til at datoen vises feil for enkelte tidssoner. |
| 586930 | Åpningsaktiviteter for ytelsesmål åpner en helt annen post | Når funksjonen for utvidet rapportvisning for ytelsesjournaler er aktivert i Funksjonsbehandling, åpnes målene for en ansatt i stedet for den valgte ansatte når du velger ytelsesmålene for utvidede rapporter i kategorien **Mitt team** i **Ansattselvbetjening**. |
| 569959 |  HcmPositionWorkerAssignmentV2-enheten tilordner ikke en arbeider til en stilling | Brukere mottok en feil da de la til en stillingstilordningspost via enheten, og publiseringen mislyktes. |
| 582259 | VETS 4212-rapporten bruker 2017-skjemaet i stedet for 2020-skjemaet | Oppdatert til 2020-format.  Hvis du vil laste inn det nye formatet, kan du gå til **Rapportkonfigurasjoner** og slette VETS-4212-rapporten i venstre kolonne. Gå til **Elektronisk rapportering - Repositorier - HR-ressurser**, og velg **Åpne**.  Velg **VETS-4212 PDF-utskrift**, og velg deretter **Importer**.|


## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |
| Aktivere forenklet lønnsintegrering (APIer for lønnsintegrering) | [Aktiver forenklet integrering med lønnsleverandører](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)|
|  Aktivere fraværsbehandling for å administrere permisjon | [Aktivere fraværsbehandling for å administrere permisjon](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) | [Konfigurer fraværsbehandlingsrollen](https://go.microsoft.com/fwlink/?linkid=2168107)|
|  Konfigurere vedleggskrav per permisjonstype | [Konfigurere vedleggskrav per permisjonstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/mandate-attachments-specific-leave-types) |[Konfigurere permisjons- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168108)|
|  Konfigurer permisjonsenheter per permisjonstype | [Konfigurer permisjonsenheter per permisjonstype](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/configure-leave-units-per-leave-type) |[Konfigurere permisjons- og fraværstyper](https://go.microsoft.com/fwlink/?linkid=2168215)|
| Gjør det mulig for ansatte å merkes som klare til betaling | [Gjør det mulig for ansatte å merkes som klare til betaling](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Klar til betaling](/dynamics365/human-resources/hr-compensation-payroll) |

## <a name="coming-soon"></a>Kommer snart

| Funksjon | Detaljer |
| --- | --- |
| Platform update 10.0.20 (44) | Plattformoppdatering 10.0.20 planlegges å rulle ut med serviceversjon 26. juli 2021. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.20 av økonomi- og driftsapper (august 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-20). |

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 1 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

