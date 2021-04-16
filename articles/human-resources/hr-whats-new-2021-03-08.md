---
title: Nyheter eller enderinger i Dynamics 365 Human Resources 8. mars 2021
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 8. mars 2021.
author: marcelbf
ms.date: 03/08/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-03-08
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 7029f1dab1f10c2b237fafb7b5d8eeff9fa7a543
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5790290"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-march-08-2021"></a>Nyheter eller enderinger i Dynamics 365 Human Resources 08. mars 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Dette emnet beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources.

Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.4017.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjoner er allment tilgjengelige i denne versjonen.

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Visning av permisjon for ledere på tvers av firmaer | [Visning av ansattpermisjon for ledere på tvers av firmaer](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurere permisjons- og fraværsparametere](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Dette emnet kan være oppdateringer for å inkludere feilrettingsfiler som ble tatt med i builden etter at dette emnet ble publisert.

| Utstedelsesnummer | Problem |  beskrivelse |
| --- | --- | --- |
| 486611 | Permisjon vises i permisjonskalenderen når **Deaktiver permisjon i alle kalendere** er aktivert | Hvis **Deaktiver permisjon i alle kalendere** er aktivert, vises ikke lenger permisjonsinformasjon når funksjonen for utvidelser i permisjons- og fraværskalenderen er aktivert.|
| 508972 | Enheten Banktransaksjon for permisjon og fravær mangler validering av registrering | Når du bruker enheten Banktransaksjon for permisjon og fravær, kan ansatte som ikke er registrert i en plan, ikke lenger importeres. |
| 554854 | Oppdatering av en kalender i enheten Ansettelse mislykkes hvis standard juridisk enhet i Brukeralternativer er forskjellig | Bruk av enheten Ansettelse til å oppdatere kalenderen for en ansatt, fører ikke lenger til en feil hvis den standard juridiske enheten i Brukeralternativer er forskjellig. |
| 558347 | "Kan ikke opprette en post i skjemakonfigurasjoner (FormRunConfiguration)" vises ved lasting av startsiden. | Tilpassinger fører til at feilen "Kan ikke opprette en post i skjemakonfigurasjoner (FormRunConfiguration)" vises ved lasting av startsiden. |
| 557327 | Arbeidsområdet for fordelsstyring: Forskjellen vises over rutenettet. | Løste brukeropplevelsesproblem med utilsiktet avstand som vises på tabellrutenettgrensene i arbeidsområdet Fordeler. |
| 557334 | Arbeidsområdet Fordelsbehandling: Rullegardinlisten for valg av **Periode** må bare vises i fanen **Sammendrag** | Rullegardinlisten for valg av **Periode** for fordeler vises nå bare når fanen **Sammendrag** er aktiv i arbeidsområdet Fordeler, og ikke i delene **Prosessresultater** og **Koblinger**. |
| 557336 | Arbeidsområdet Fordelsstyring: Teksten **Åpen registrering med utsjekkede planer** er avkortet i flisvisningen. | Endret tekst i flisvisningen til **Utsjekkede planer... åpen registrering** for å unngå avkorting av nødvendig kontekst. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Arbeidsområde for fordelsbehandling | [Arbeidsområdet Fordelsbehandling (forhåndsversjon)](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbeidsområde for fordelsbehandling](hr-benefits-management-workspace.md) |
| Du kan hindre at ansatte redigerer kontaktdetaljer for virksomhet. | [Begrense at ansatte redigerer kontaktdetaljer for virksomhet.](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/restrict-employees-editing-business-contact-details) | [Begrense redigering av personlige opplysninger](hr-employee-self-service-restrict-editing.md)|

## <a name="coming-soon"></a>Kommer snart

| Funksjon | Detaljer |
| --- | --- |
| Ferdigheter som angis av en leder for de ansatte, kan godkjennes automatisk av en arbeidsflyt | Kommer snart. |

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2021-frigivelsesbølge 1](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheter eller endringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversikt over lanseringsbølge 1 i 2021 for Dynamics 365 Human Resources](https://docs.microsoft.com/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Oppdatere prosess](hr-admin-setup-update-process.md)</br>
[Behandle funksjoner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
