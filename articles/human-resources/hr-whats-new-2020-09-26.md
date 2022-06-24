---
title: Hva er nytt eller endret i Dynamics 365 Human Resources 26. september 2020
description: Denne artikkelen beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Human Resources for 26. september 2020.
author: jcart1106
ms.date: 09/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-13
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1b7a89ae8a2132c8548d9451aa235d1bccb88809
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8874253"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-26-2020"></a>Hva er nytt eller endret i Dynamics 365 Human Resources 26. september 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]



Denne artikkelen beskriver funksjoner som er nye, endret eller kommer snart i Dynamics 365 Human Resources. Hvis du vil ha mer informasjon om oppdateringsprosessen og tidsplanen, kan du se [Oppdatere prosess](hr-admin-setup-update-process.md).

Hvis du vil ha mer informasjon om nye funksjoner og deres forventede generelle tilgjengelighetsdatoer, se [Oversikt over Dynamics 365 Human Resources 2020-frigivelsesbølge 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne versjonen

Denne versjonen omfatter følgende nye funksjoner og feilrettinger. Endringer gjelder for Build-nummeret 8.1.3589-hf.3.

### <a name="new-features"></a>Nye funksjoner

Følgende funksjon er vanligvis tilgjengelig i denne versjonen:

- **Platform Update 10.0.13 er nå tilgjengelig**: Hvis du vil ha mer informasjon om denne oppdateringen, kan du se [Plattformoppdateringer for versjon 10.0.13 av økonomi- og driftsapper (oktober 2020)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-13.md).

### <a name="bug-fixes"></a>Feilrettinger

Denne versjonen inneholder følgende feilrettinger.

> [!NOTE]
> Vårt mål er å få denne informasjonen til deg så raskt som mulig. Denne artikkelen kan være oppdateringer for å inkludere feilrettingsfiler som ble tatt med i builden etter at denne artikkelen ble publisert.

| Utstedelsesnummer | Problem | Beskrivelse |
| --- | --- | --- |
| 469495 | Oppdatere standard rutenett og dialogboks for finansdimensjoner | Rutenett og dialogboks for finansdimensjoner er oppdatert i hele Human Resources. |
| 474887 | Arbeidselement for permisjonsforespørsel åpner feil kobling i en manuell beslutning | Når en arbeidsflytkonfigurasjon inneholder en manuell beslutning, fører navigering til permisjonsforespørsel fra **Arbeidselementer som er tilordnet til meg**, at feil kobling åpnes, som enten viser et tomt skjema eller en permisjonsforespørsel opprettet av den gjeldende brukeren i stedet for det som er tilordnet dem for den manuelle beslutningen. |
| 474962 | Enhet for permisjons- og fraværsparametere har felt med tvetydige etiketter | Enhetsetiketter for permisjons- og fraværsparametere er oppdatert for å bli klarere. |
| 481401 | Avsetningsbehandling henger når datogrunnlag for avsetning er etter avsetningens startdato og på slutten av måneden | Avsetningsbehandling er oppdatert til ikke å ha en forsinkelse når avsetningsdatogrunnlaget er etter startdatoen for avsetningen og på slutten av måneden. |
| 447167 | Utløpende poster inkluderer inaktive arbeidere | Kategorien **Utløpende poster** i **Personaladministrasjon** inneholdt inaktive arbeidere. Nå inneholder den bare aktive arbeidere. |
| 486840 | Feil permisjonsforespørsel åpnes fra **Arbeidselementer som er tilordnet til meg** | Valg av en permisjonsforespørsel fra **Arbeidselementer som er tilordnet til meg** åpner ikke lenger den siste permisjonsforespørselen som er tilordnet den gjeldende brukeren. |
| 506868 | Dataverse **Tittel**-felt ikke angitt for **Stilling**-enhet | **Tittel**-feltet i **Jobb** og **Stilling**-enhetene vises som ikke angitt. **Tittel**-feltet vises nå. |
| 430359 | Får ikke tilgang til avlasting for sjekklisteoppgaver med overordnet og ansattroller tilordnet | Arbeidere med en fremtidig avslutningsdato får ikke tilgang til sjekklisteoppgavene hvis de bare hadde en ansatt eller lederrolle. Brukere med bare en ansatt eller lederrolle har for øyeblikket tilgang til avlastingsaktiviteter med en fremtidig avslutningsdato. |
| 458102 | Ny ansatt vises ikke på **Lønnsinformasjon for arbeider**-enheten når den opprettes | Nye ansatte inkluderes i lønnsinformasjonsenheten for arbeideren uten å måtte åpne lønnsinformasjonen for den ansatte før du eksporterer enheten. |

## <a name="in-preview"></a>I forhåndsvisning

Følgende nye funksjoner er i forhåndsversjon. Hvis du vil ha mer informasjon om å aktivere/deaktivere funksjoner, kan du se [Behandle funksjoner](hr-admin-manage-features.md).

| Funksjon | Lanseringsplan | Dokumentasjon |
| --- | --- | --- |
| Human Resources-app i Microsoft Teams | [Ansattopplevelsen fro permisjon og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](./hr-admin-teams-leave-app.md)<br>[Behandle permisjonsforespørsler i Teams](hr-teams-leave-app.md) |
| Utvidede arbeidsflytforespørsler og -godkjenninger | [Forbedringer i arbeidsflyten for organisasjons- og personalstyring](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurasjonsalternativ for å plassere listen Arbeidselementer som er tilordnet til meg](./hr-whats-new-2020-09-03.md#configuration-option-to-position-work-items-assigned-to-me-list-477004) |

## <a name="coming-soon"></a>Kommer snart

Følgende nye funksjon er planlagt for en fremtidig frigivelse:

- [Egendefinerte koblinger i Lederselvbetjening](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service)

Hvis du vil ha en fullstendig liste over de planlagte funksjonene og de planlagte versjonene, kan du se [Oversikt over Dynamics 365 Human Resources 2019-frigivelsesbølge 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Tilleggsressurser

[Hva er nytt eller endret i Human Resources](hr-admin-whats-new.md)
[Oversikt over Dynamics 365 Human Resources 2020-frigivelsesbølge 2](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)
[Oppdateringsprosess](hr-admin-setup-update-process.md)
[Behandle funksjoner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]