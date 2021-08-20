---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 22. juni 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 22. juni 2021.
author: marcelbf
ms.date: 06/22/2021
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
ms.search.validFrom: 2021-06-22
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 897c25df96017c5be1ae789027d178ca6b3ccc0410b4f65c7d2557b39e840134
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735357"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-june-22-2021"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 22. juni 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4258.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Informere brukere om arbeidere uten ansettelsesfunksjon – Når avansert tilgang er på, og funksjonen **Vis alle arbeidere uten ansettelse** er deaktivert i funksjonsstyring, blir det vist et banner for arbeiderne uten ansettelsesskjema. Ved hjelp av denne funksjonen får brukeren spørsmål om å aktivere funksjonen **Vis alle arbeidere uten ansettelse**. | Gjelder ikke| [Arbeidere uten ansettelse](/dynamics365/human-resources/hr-personnel-workers-without-employment)|
| Egendefinerte felt-støtte for rettighetsregler for fordelsbehandling | [Egendefinert felt-støtte for rettighetsbehandling](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |[Konfigurere rettighetsregler](/dynamics365/human-resources/hr-benefits-setup-eligibility-rules) |
| Overvåking av permisjonsavsetningstransaksjon | Gjelder ikke | [Overvåking av permisjonsavsetningstransaksjon](hr-leave-and-absence-accrue.md)|
| Forbedringer i permisjon og fravær-arbeidsflyt | [Forbedringer i permisjon og fravær-arbeidsflyt](https://go.microsoft.com/fwlink/?linkid=2147528) | [Be om fritid](hr-employee-self-service-request-time-off.md)|

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdateringer for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem |  beskrivelse |
| --- | --- | --- |
| 583052 | Bruker som mottar tilbakemelding, kan redigere den mottatte tilbakemeldingen | Når en ansatt som mottar tilbakemelding på en ytelsesjournal, velger **Legg til ekstern kobling**, kan du redigere skjemaet, slik at den ansatte kan redigere tilbakemelding om ytelsen de har mottatt. |
| 522281 | Hvis du velger antall ansatte på kompensasjonsstrukturflisene i Kompensasjonsstyring, fører det til uriktige resultater| Når du driller ned i kompensasjonsplanene fra arbeidsområdet for kompensasjon, vises det riktige antallet ansatte nå. |
| 580683 | Brukere som er tilordnet til Ansatt- og Lederroller, kan ikke legge ved merknader eller oppdatere en ytelsesjournal | Brukere som er tilordnet til Ansatt- og Lederroller, kan ikke legge ved merknader eller oppdatere en ytelsesjournal. Brukeren mottar feilmeldingen "Kan ikke opprette en post i ytelsesjournaloppføring (HcmPerfJournal). Tillatelse til sikkerhetspolicy nektet." |
| 583077 | Fødselsdatoen til en ansatt i permisjons- og fraværsfirmakalenderen viser feil dato | Brukerne kan vise riktig fødselsdato for de ansatte i firmakalenderen for permisjon og fravær. |
| 586996 | Funksjonen for visning på tvers av firmaer fører til at saldoer blir tomme når tilgang er begrenset til ett enkelt firma | Brukere kan vise saldoer for fremtidige permisjoner for ansatte på riktig måte når permisjonsvisning på tvers av firmaer er aktivert. |
| 581014 | Aktivering av permisjon på tvers av firmaer og fraværsvisning forårsaker en feil når du ser fremtidige saldoer | Feil som medførte at brukere som så på fremtidige permisjonssaldoer der permisjonsvisning på tvers av firmaer er aktivert, er løst. |
| 509404 | Arbeidsstokkanalyse for avdeling tar ikke hensyn til flytting av ansatte mellom avdelinger. | Når en ansatt migrerer fra én avdeling til en annen, gjenspeiler ikke dataene for antall ansatte i avdelingen den gamle avdelingen der den ansatte flyttes fra, hvis stillingsdetaljen er utløpt inneværende år. |
| 584851 | Fordelingsregelen "Ingen" for frynsegodekreditt gir aldri kreditt |Fordelsregelen for fleksibel kreditt "Ingen" førte til at ansatte fikk null i kreditt for fordelsperioden, uansett når de ble ansatt. Dette er rettet, slik at en ansatt skal få fulle fleksible kreditter hvis de ansettes før fordelsperioden begynner, og ingen hvis de ansettes etter at perioden begynner. |
| 584897 | Duplisering av avgiften "Bruk grunnleggende ekstern funksjonalitet" fører til en feil | Under forsøk på å duplisere avgiften "Bruk grunnleggende ekstern funksjonalitet", mottok brukeren feilen "Finner ikke objekt med identifikatoren UserDefinedAppHostDialogView." |
| 575692 | Avsetning av permisjon og fravær er ikke tilgjengelig for ventende arbeidere | Permisjons- og fraværsavsetning kan kjøres på fremtidige ansettelser når **Strømlinjeformet ansattoppføring** er aktivert. |
| 580110 | Når du legger til et firma i lønningsintegrering, tilbakestilles integreringen, slik at de bruker alle enhetene, selv om du har angitt at alternativet ikke skal oppdatere prosjektet | Hvis en kunde har fjernet enheter eller endret dataprosjektet for lønnsintegrering, og alternativet er angitt til å hindre automatisk oppdatering av prosjektet, vil et nytt firma i integreringen ignorere innstillingen og oppdatere prosjektet.  |
| 584518 |Registrere ytelsesproblem ved fordelsbehandling | Denne feilen omhandlet ytelsesproblemer i registreringsprosessen for eldre fordeler. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |
| Aktivere forenklet lønnsintegrering (APIer for lønnsintegrering) | [Aktiver forenklet integrering med lønnsleverandører](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [API for lønnsintegrering](hr-admin-integration-payroll-api-introduction.md)|


## <a name="coming-soon"></a>Kommer snart

| Funksjon | Detaljer |
| --- | --- |
| Platform update 10.0.19 (43) | Plattformoppdatering 10.0.19 planlegges å rulle ut med serviceversjon 28. juni 2021. Hvis du vil ha mer informasjon, kan du se [Platformoppdateringer for versjon 10.0.19 av Finance and Operations-apper (juni 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-19). |
|  Arbeidserfaring-visning veksler | Ved hjelp av denne funksjonen kan du bruke forskjellige datoer til å beregne arbeidserfaring som vises i skjemaet **Strømlinjeformet ansattoppføring** og i skjemaet **Personer**.  Dette vil være tilgjengelig i parametere for Human Resources. |
|  Aktivere fraværsbehandling for å administrere permisjon | [Aktivere fraværsbehandling for å administrere permisjon](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-absence-manager-manage-leave) |
|  Obligatoriske vedlegg for bestemte permisjonstyper | Med denne funksjonen kan administratorer legge til mandatvedlegg når permisjonsforespørsler sendes for bestemte permisjonstyper. |
|  Konfigurer permisjonsenheter per permisjonstype | Ved hjelp av denne funksjonen kan administratorer konfigurere permisjonsenheter (timer eller dager) for hver permisjonstype.  |
| Gjør det mulig for ansatte å merkes som klare til betaling | [Gjør det mulig for ansatte å merkes som klare til betaling](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-employees-be-marked-as-ready-pay) |

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 1 i 2021 for Dynamics 365 Human Resources](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
