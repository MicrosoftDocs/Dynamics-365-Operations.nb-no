---
title: Innføring i API for søkersporingssystemintegrering
description: Denne artikkelen beskriver Dynamics 365 Human Resources API for søkersporingssystemintegrering.
author: andreabichsel
ms.date: 02/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 6037d09fdc484753c7e90a896ce383bd71391356
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8894708"
---
# <a name="applicant-tracking-system-integration-api-introduction"></a>Innføring i API for søkersporingssystemintegrering


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikkelen beskriver Dynamics 365 Human Resources API for søkersporingssystemintegrering. Hensikten med API-en er å aktivere strømlinjeformet integrasjon mellom Dynamics 365 Human Resources og partner-ATS-er.

![ATS-integrasjonsflyt.](media/hr-admin-integration-ats-api-introduction-flow.png)

Den integrerte erfaringen begynner i Human Resources når en ansettelsesansvarlig oppretter en rekrutteringsforespørsel. Når forespørselen er aktivert, henter ATS detaljene for forespørselen om å opprette et rekrutteringsprosjekt. Deretter følger rekrutteringsforløpet for å velge og ansette en kandidat til stillingen(e). Til slutt fullfører ATS integreringen med rundturintegrering ved å sende den valgte kandidatens post til Human Resources. Kandidatposten kan deretter gå gjennom mer pålastingsvalideringer og arbeidsflyter for å opprette ansattposten.

Human Resources har lagt til følgende komponenter for å aktivere integreringen:

1.  Funksjonalitet for å opprette en rekrutteringsforespørsel.
2.  Utvidet kandidatprofil og tilknyttede arbeidsflyter.
3.  En integrerings-API som åpner opp den nye funksjonaliteten for integrering av programmer.

Hvis du vil ha mer informasjon om hvordan du definerer og bruker rekrutteringsforespørselen og kandidatfunksjonaliteten, kan du se [Rekruttering av jobbkandidater](hr-personnel-recruit.md).

## <a name="microsoft-dataverse"></a>Microsoft Dataverse

Denne API-en er bygd på Microsoft Dataverse (tidligere kalt Common Data Service). All RESTful-samhandling med denne API-en gjøres via web-API-en for Microsoft Dataverse, som bruker OData. Denne API-en er et delsett av Dataverse-web-API-en. Dataverse-web-API-en definerer egenskaper som godkjenning, SLA-er, parti, samtidighetskontroll og feilhåndtering.

Hvis du vil ha mer generell informasjon om Microsoft Dataverse-web-API-en, kan du se:

- [Hva er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)
- [Bruke Microsoft Dataverse-web-API-en](/powerapps/developer/data-platform/webapi/overview)
- [Utviklerveiledning for Microsoft Dataverse](/powerapps/developer/data-platform)

Dokumentasjonen ovenfor inneholder detaljer og utviklerveiledning for bruk av web-API for Dataverse, for eksempel [administrasjon av godkjenning](/powerapps/developer/data-platform/webapi/authenticate-web-api), [utføre operasjoner](/powerapps/developer/data-platform/webapi/perform-operations-web-api), [bruke Postman med API-en](/powerapps/developer/data-platform/webapi/use-postman-web-api) og [bruker endringssporing eller deltatokener](/powerapps/developer/data-platform/use-change-tracking-synchronize-data-external-systems) med API-en.

### <a name="option-sets"></a>Alternativsett

Datamodellen for ATS-integrerings-API-en som er beskrevet i dette dokumentet, inneholder alternativsett som inneholder opplistingsverdier som er knyttet til enhetsegenskaper. Hvis du vil ha detaljert informasjon om hvordan du arbeider med alternativsett i web-API for Dataverse, kan du se [Opprette og oppdatere alternativsett ved hjelp av web-API-en](/powerapps/developer/data-platform/webapi/create-update-optionsets). Alternativsett defineres for hvert Dataverse-miljø.

### <a name="virtual-tables-for-human-resources-in-dataverse"></a>Virtuelle tabeller for Human Resources i Dataverse

Sluttpunktene for ATS-integrerings-API-en bruker de virtuelle tabellplattformfunksjonene i Microsoft Dataverse. Som standard distribueres ikke de virtuelle tabellene og de tilknyttede API-sluttpunktene for Human Resources-miljøene, som gjør det mulig for organisasjoner å fastslå hvilke OData-sluttpunkter som vises for miljøet. For å kunne bruke API-en må de virtuelle tabellene for Human Resources-enhetene genereres for miljøet. 

Hvis du vil ha informasjon om generering av de virtuelle tabellene for API, kan du se [Konfigurere virtuelle Dataverse-tabeller](./hr-admin-integration-common-data-service-virtual-entities.md).

## <a name="data-model"></a>Datamodell

Datamodellen er sentrert rundt to hovedenheter:

- **RecruitingRequest** representerer en forespørsel til en ATS om å rekruttere for én eller flere åpne stillinger. Hvis du vil ha en eksempelspørring, kan du se [Eksempelspørring for rekrutteringsforespørsel](hr-admin-integration-ats-api-recruiting-request-example-query.md).
- **CandidateToHire** representerer detaljer til en kandidat som har tatt imot et tilbud om en stilling. **Person** representerer personen som er kandidaten. En person kan ha flere roller i firmaet, for eksempel kandidat, arbeider, ansatt eller oppdragstaker. Hvis du vil ha en eksempelspørring, kan du se [Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md).

Diagrammet nedenfor illustrerer relasjonen med API-en. Flere typer har sekundærnøkler til andre, eksisterende enheter i Human Resources som ikke illustreres her. Dette dokumentet inneholder informasjon om enheter som er spesifikke for rekrutteringsintegrasjonsscenarier. Det er imidlertid mange andre enheter i Dataverse-web-APIen for Dynamics 365 Human Resources som også kan være relevante for integreringen. Det kan for eksempel også hende du trenger detaljer for arbeidere, jobber, stillinger eller andre enheter som ikke er definert her. Mange av disse enhetene refereres til i sekundærnøkkelrelasjoner eller navigasjonsegenskaper.

![ATS-integrering, API-datamodell.](media/hr-admin-integration-ats-api-data-model.png)

## <a name="recruiting-request-and-related-entities-and-option-sets"></a>Rekrutteringsforespørsel og relaterte enheter og alternativsett

Eksempelspørring: 

- [Eksempelspørring for rekrutteringsforespørsel](hr-admin-integration-ats-api-recruiting-request-example-query.md)

Enheter:

- [Rekrutteringsforespørsel](hr-admin-integration-ats-api-recruiting-request.md)
- [Rekrutteringsforespørselsstilling](hr-admin-integration-ats-api-recruiting-request-position.md)
- [Rekrutteringsforespørselsferdighet](hr-admin-integration-ats-api-recruiting-request-skill.md)
- [Rekrutteringsforespørselsutdanning](hr-admin-integration-ats-api-recruiting-request-education.md)
- [Rekrutteringsforespørselssted](hr-admin-integration-ats-api-recruiting-request-location.md)

Alternativsett:

- [Jobbfritaksstatus](hr-admin-integration-ats-api-job-exempt-status.md)
- [Status for rekrutteringsforespørselsstilling](hr-admin-integration-ats-api-recruiting-request-position-status.md)
- [Rekrutteringsforespørselsstatus](hr-admin-integration-ats-api-recruiting-request-status.md)
- [Forskriftsmessig jobbkategori](hr-admin-integration-ats-api-regulatory-job-category.md)

## <a name="candidate-to-hire-and-related-entities-and-option-sets"></a>Kandidat for ansettelse og relaterte enheter og alternativsett

Eksempelspørring:

- [Eksempelspørring for Kandidat for ansettelse](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

Enheter:

- [Ansettelseskandidat](hr-admin-integration-ats-api-candidate-to-hire.md)
- [Person](hr-admin-integration-ats-api-person.md)
- [Personutdanning](hr-admin-integration-ats-api-person-education.md)
- [Persons yrkeserfaring](hr-admin-integration-ats-api-person-professional-experience.md)
- [Personadresse](hr-admin-integration-ats-api-person-address.md)
- [Partskontakt](hr-admin-integration-ats-api-party-contact.md)
- [Personferdighet](hr-admin-integration-ats-api-person-skill.md)
- [Vurderingsnivå](hr-admin-integration-ats-api-rating-level.md)
- [Personsertifikat](hr-admin-integration-ats-api-person-certificate.md)
- [Attesttype](hr-admin-integration-ats-api-certificate-type.md)
- [Personscreening](hr-admin-integration-ats-api-person-screening.md)
- [Screeningtyper](hr-admin-integration-ats-api-screening-types.md)
- [Personidentifikasjonsnummer](hr-admin-integration-ats-api-person-identification-number.md)

Alternativsett:

- [Søkerintegreringsresultat](hr-admin-integration-ats-api-applicant-integration-result.md)
- [Tomt Ja Nei](hr-admin-integration-ats-api-blank-yes-no.md)
- [Fullføringsstatus](hr-admin-integration-ats-api-completion-status.md)
- [Kontakttype](hr-admin-integration-ats-api-contact-type.md)
- [Utdanningskredittbasis](hr-admin-integration-ats-api-education-credit-basis.md)
- [Kjønn](hr-admin-integration-ats-api-gender.md)
- [Sivilstand](hr-admin-integration-ats-api-marital-status.md)
- [Måneder i året](hr-admin-integration-ats-api-months-of-year.md)
- [Nei Ja](hr-admin-integration-ats-api-no-yes.md)
- [Periodeenhet](hr-admin-integration-ats-api-period-unit.md)
- [Screeningfrekvens](hr-admin-integration-ats-api-screening-frequency.md)
- [Screeningfrekvens genereres fra](hr-admin-integration-ats-api-screening-frequency-generate-from.md)
- [Kompetansenivåtype](hr-admin-integration-ats-api-skill-level-type.md)

## <a name="see-also"></a>Se også

[Rekruttere jobbkandidater](hr-personnel-recruit.md)<br>
[Hva er Microsoft Dataverse?](/powerapps/maker/data-platform/data-platform-intro)<br>
[Bruke Microsoft Dataverse-web-API-en](/powerapps/developer/data-platform/webapi/overview)<br>
[Opprette og oppdatere alternativsett ved hjelp av web-API](/powerapps/developer/data-platform/webapi/create-update-optionsets)<br>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
