---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 20. september 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 20. september 2021.
author: marcelbf
ms.date: 09/20/2021
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
ms.search.validFrom: 2021-09-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3f4fc4768f8c96678b216709f78af6d3ddfd4132
ms.sourcegitcommit: ba8ca42e43e1a5251cbbd6ddb292566164d735dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/25/2021
ms.locfileid: "7556939"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-20-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 20. september 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Microsoft Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4464.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
|---|---|---|
| Aktivere forenklet lønnsintegrering (APIer for lønnsintegrering) | [Aktiver forenklet integrering med lønnsleverandører](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md) |
| Gjør det mulig for ansatte å merkes som klare til betaling | [Gjør det mulig for ansatte å merkes som klare til betaling](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) | [Klar til betaling](/dynamics365/human-resources/hr-compensation-payroll) |

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdatert for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem | Beskrivelse |
|---|---|---|
| 619774 | Redigering av adressebeskrivelsen synkroniseres ikke til Dataverse i sanntid. | Når du redigerer beskrivelsen for en arbeideradresse, blir ikke den oppdaterte beskrivelsen synkronisert i sanntid med Dataverse. Abonnementet i tabellen **Logistikkplassering** ble oppdatert for sending av en oppdatering. |
| 614603| Feil på **Arbeider**-siden når parameteren for **ansattes handlinger** ikke er valgt. | Når du ansetter en ny arbeider eller navigerer til **Arbeider**-siden, vises følgende feil, "Feltet **Personalhandlingstype** må fylles ut", selv om **Personalhandlinger** er slått av. |
| 615367 | Kategorien **Godkjent avspasering** viser en advarsel og vises feil. | Hvis permisjonsenheten er satt til **Dager** før aktivering av funksjonen **Konfigurer permisjonsenheter per permisjonstype**, viser kategorien **Godkjent avspasering** en ugyldig advarsel og feil kolonner. |


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
| **Rapportparameter**-siden i **Ansattselvbetjening** for fordelsoppgaven er feil. | Når du navigerer til **Fordelsoppgave** i **Ansattselvbetjening**, viser siden **Rapportparametere** hurtigfanene **Poster som skal inkluderes** og **Kjør i bakgrunnen**.  Disse må fjernes. |
| Lukkede og fremtidige perioder vises på **Rapportparameter**-siden for fordelsoppgaven. | Når brukeren navigerer til målsiden for **Fordelserklæringsrapport**, kan han eller hun velge fordelsplanperioder som er lukket eller er datert i fremtiden, noe som resulterer i en tom side. Bare gjeldende fordelsplanperiode skal vises i listen. |
|Feil når rapport sendes via e-post ved bruk av GER-rapportmål. | Fordelsoppgaven kan angis slik at det brukes e-postparametere på siden **GER-rapportmål**. Når rapporten fylles ut og skrives ut, får brukeren en formateringsfeil og fordelsoppgaven blir ikke sendt.|


## <a name="coming-soon"></a>Kommer snart

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 2](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/).

| Funksjon | Detaljer |
|---|---|
| Platform update 10.0.21 (45) | Utrullingen av plattformoppdatering 10.0.21 er planlagt å begynne med serviceversjon 4. oktober 2021. Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.21 av Finance and Operations-apper (oktober 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-21). |
|Visning av utvidede rapporter for ytelsesjournaler | Denne funksjonen blir aktivert som standard i den neste utrullingen. |


## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 2 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave2/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]