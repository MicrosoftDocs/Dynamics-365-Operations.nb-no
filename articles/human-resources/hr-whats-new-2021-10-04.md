---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 5. oktober 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 5. oktober 2021.
author: marcelbf
ms.date: 10/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-10-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3cf83421d5385e3c95dfda6db35edfb8eb4b9336
ms.sourcegitcommit: a58dfb892e43921157014f0784bd411f5c40e454
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/04/2022
ms.locfileid: "8695767"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-5-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 5. oktober 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Microsoft Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4485.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
|---|---|---|
| Platform update 10.0.21 (45) | -- | [Plattformoppdateringer for versjon 10.0.21 av økonomi- og driftsapper (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21) |


### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdatert for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem | Beskrivelse |
|---|---|---|
| 598896 | Ansattbeløpet vises ikke før etter at den ansatte har fullført registreringen | På siden **Ansattselvbetjening** vises ikke ansattbeløpet for fordelen. Ansattbeløpet vises nå på siden **Selvbetjeningsfordeler**.  |
| 613440 | Kan ikke eksportere data fra **Dataadministrasjon** | Når data eksporteres for et prosjekt i **Dataadministrasjon**, mislykkes eksporten uventet. |
| 618327 | Lukkede og fremtidige perioder vises på siden **Rapportparameter** for fordelsoppgaven | Når du navigerer til **Fordelsoppgave** i **Ansattselvbetjening**, viser siden **Rapportparametere** hurtigfanene **Poster som skal inkluderes** og **Kjør i bakgrunnen**. Disse delene ble fjernet.|
| 618326 | En feilaktig **Rapportparameter**-siden vises i **Ansattselvbetjening** for fordelsoppgaven| Når brukeren navigerer til målsiden for **Fordelserklæringsrapport**, kunne vedkommende velge fordelsplanperioder som er lukket eller er datert i fremtiden, noe som resulterer i en tom side. Bare gjeldende fordelsplanperiode skal vises i listen. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om hvordan du aktiverer eller deaktiverer funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
|---|---|---|
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |
| Egendefinerte felt i Rettighet |[Egendefinert felt-støtte i rettighetsbehandling](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management) | [Bruke egendefinerte felt i rettighetsbehandling](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules#using-custom-fields-in-eligibility-rules) |
| Fordelsoppgave |[Fordelsoppgave](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/benefits-summary-statement) | [Fordelsoppgave](hr-benefits-statement.md) |

### <a name="benefits-statement-known-issues"></a>Kjente problemer med Fordelsoppgave

| Problem | Beskrivelse |
|---|---|
|Feil når rapport sendes via e-post ved bruk av **GER-rapportmål** | Fordelsoppgaven kan angis slik at det brukes e-postparametere på siden **GER-rapportmål**. Når rapporten fylles ut og skrives ut, får brukeren en formateringsfeil og fordelsoppgaven blir ikke sendt.|

## <a name="feature-management-changes"></a>Endringer i funksjonsbehandling

| Funksjon | Beskrivelse |
|---|---|
|Visning av utvidede rapporter for ytelsesjournaler | Denne funksjonen blir aktivert som standard i denne utgivelsen. |

## <a name="coming-soon"></a>Kommer snart

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funksjon | Detaljer |
|---|---|
| Platform update 10.0.22 (46) | Utrullingen av plattformoppdatering 10.0.22 er planlagt å begynne med serviceversjon 1. november 2021. Hvis du vil ha mer informasjon, kan du se [Plattformoppdateringer for versjon 10.0.22 av økonomi- og driftsapper (november 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-22). |



## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
