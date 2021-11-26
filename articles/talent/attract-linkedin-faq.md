---
title: Vanlige spørsmål om LinkedIn-integrering
description: Dette emnet svarer på spørsmål du kan ha om integrering mellom LinkedIn og Microsoft Microsoft Dynamics 365 Talent – Attract.
author: hasrivas
manager: AnnBe
ms.date: 07/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: hasrivas
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 35428da709f480e1d3842b7e92deacba200326ee
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462083"
---
# <a name="linkedin-integration-faq"></a>Vanlige spørsmål om LinkedIn-integrering

[!include [banner](includes/banner.md)]

LinkedIn er verdens største profesjonelle online-nettverk. Microsoft Dynamics Talent: Attract er integrert med LinkedIn for å gi deg tilgang til verdens største talenter. Med Attract kan du legge inn jobber direkte på LinkedIn og hente ut kandidatinformasjon fra LinkedIn til Attract.

## <a name="for-recruiters-and-hiring-managers"></a>For rekrutteringspersoner og ansettelsesledere

Her er svar på ofte stilte spørsmål om hvordan du bruker Attract og LinkedIn sammen.

### <a name="what-linkedin-features-do-i-get-with-attract"></a>Hvilke LinkedIn-funksjoner får jeg med Attract?

Attracts integrering med LinkedIn lar deg utføre følgende oppgaver:

- [Postere jobber på LinkedIn](./attract-post-jobs-to-linkedin.md) (som gratis "Begrensede oppføringer" (Limited Listings)).
- [Finne kandidater med LinkedIn Recruiter i Microsoft Dynamics 365 Talent - Attract](./attract-linkedin-recruiter.md#export-linkedin-candidates-to-attract-with-one-click).
- [Konfigurere integrering med LinkedIn for Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md#set-up-apply-with-linkedin-in-attract).

### <a name="what-do-i-need-before-i-can-post-jobs-to-linkedin"></a>Hva trenger jeg før jeg kan legge inn jobber på LinkedIn?

Din administrator må [konfigurere LinkedIn-integrasjon i Attract](./attract-admin-linkedin.md#configure-job-posting-to-linkedin). Etter det er du klar.

### <a name="how-do-i-post-jobs-to-linkedin-from-attract"></a>Hvordan posterer jeg jobber til LinkedIn fra Attract?

Når du har opprettet en jobb i Attract, må du bare velge **Poster nå**-knappen som tilsvarer LinkedIn. For mer informasjon, se [Postere jobber til LinkedIn fra Microsoft Dynamics 365 Talent - Attract](./attract-post-jobs-to-linkedin.md#post-jobs-to-linkedin).

### <a name="can-i-get-candidate-information-from-linkedin-into-attract"></a>Kan jeg hente kandidatinformasjon fra LinkedIn til Attract?

Ja. Hvis du ser en god kandidat på LinkedIn, kan du enkelt eksportere denne kandidatens informasjon til Attract. Hvis du vil ha mer informasjon, se [Finne kandidater med LinkedIn Recruiter i Microsoft Dynamics 365 Talent - Attract](attract-linkedin-recruiter.md).

### <a name="how-can-i-get-help-accessing-linkedin-from-attract"></a>Hvordan kan jeg få hjelp med å få tilgang til LinkedIn fra Attract?

Hvis du har problemer med å logge på eller postere jobber til LinkedIn fra Attract, kan du se [Feilsøke integrering med LinkedIn og Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md).

For andre problemer med Attract, se [Få kundestøtte for Microsoft Dynamics 365 Talent](./talent-support.md). Hvis du vil ha hjelp med LinkedIn, kan du se [kundestøttesiden for LinkedIn](https://www.linkedin.com/help).

## <a name="for-admins-and-developers"></a>For administratorer og utviklere

Her er svar på ofte stilte spørsmål om hvordan du konfigurerer integrering mellom Attract og LinkedIn.

### <a name="how-do-i-configure-attract-so-that-recruiters-and-hiring-managers-can-post-jobs-to-linkedin"></a>Hvordan konfigurerer jeg Attract slik at rekrutterere og ansettelsesansvarlige kan postere jobber på LinkedIn?

Du kan konfigurere de tilgjengelige alternativene i kategorien **LinkedIn-integrasjon** i administrasjonssenteret. Hvis du vil ha mer informasjon, kan du se [Konfigurere integrering med LinkedIn for Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md).

### <a name="can-i-export-candidate-information-from-linkedin"></a>Kan jeg eksportere kandidatinformasjon fra LinkedIn?

Ja, men du må først konfigurere integrering med LinkedIn Recruiter. Hvis du vil ha mer informasjon, kan du se [Konfigurere integrering med LinkedIn for Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md).

### <a name="how-can-i-post-jobs-to-premium-job-slots-on-linkedin"></a>Hvordan kan jeg postere jobber til premium jobbplasser på LinkedIn?

Selv om Attract har en kraftig løsning for å postere jobber til LinkedIn, kan det hende at du vil trenge ekstra fleksibilitet. Det kan for eksempel være at du vil kunne postere premium jobbplasser i tillegg til de gratis "begrensede oppføringene" (Limited Listings), eller kanskje du vil at LinkedIn skal behandle dine satsvise jobbposteringer mer enn én gang per dag.

#### <a name="types-of-linkedin-job-posts"></a>Typer LinkedIn-jobbutlysinger

LinkedIn tilbyr følgende typer jobbposteringer:

- **Begrenset oppføring** – Gratis jobbposteringer som vises i søkeresultater når kandidater søker etter jobber på LinkedIn og på et selskaps LinkedIn-side. Begrensede oppføringer er rettet mot aktive jobbsøkere. Denne typen oppføring er den typen Attract gir til LinkedIn. Du kan ikke fremme Begrensede oppføringer-jobber på LinkedIn. Hvis du vil fremme begrensede oppføringer, må du arbeide med LinkedIn for å aktivere «jobbpakking» (Job Wrapping). Hvis du vil ha mer informasjon om jobbpakking, kan du se [Begrensede oppføringer kontra premium jobbplasser for jobbpakking](https://www.linkedin.com/help/recruiter/answer/79049/limited-listings-vs-premium-job-slots-for-job-wrapping) og [Vanlige spørsmål om jobbpakking pluss](https://www.linkedin.com/help/recruiter/answer/79050/job-wrapping-frequently-asked-questions).
- **Premium jobbplass** - Kjøpte posteringer som vises på ulike steder i LinkedIn, for eksempel LinkedIn-feeden, e-postmeldinger og området **Jobber du kan være interessert i**. Premium jobbplasser er rettet mot passive kandidater, men de vises også i jobbsøk.

Attract posterer jobber på LinkedIn som begrensede oppføringer. Hvis du vil bruke premium jobbplasser, må du bruke jobbpakking via LinkedIn Recruiter. Jobbpakking krever en jobbpakkingskontrakt med LinkedIn. Hvis du vil ha mer informasjon, se [Jobbpakking via LinkedIn Recruiter - oversikt](https://www.linkedin.com/help/recruiter/answer/79037).

#### <a name="frequency-of-batch-processing-on-linkedin"></a>Hyppighet i satsvis behandling på LinkedIn

LinkedIn behandler jobbutlysinger i et parti via Attract én gang per dag. Derfor kan det ta opptil 48 timer før jobber vises på LinkedIn etter at de er postert gjennom Attract. Hvis du vil at jobber skal vises raskere på LinkedIn, eller hvis du trenger mer fleksibilitet, kan du bruke Recruiter System Connect-grensesnittet (API) fra LinkedIn. Hvis du vil ha mer informasjon, kan du se [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect).

#### <a name="table-of-options-for-job-posting-to-linkedin"></a>Tabell med alternativer for jobbpostering til LinkedIn

Tabellen nedenfor beskriver de ulike alternativene for å postere jobber til LinkedIn. Den inkluderer fordelene ved hvert alternativ og tilleggsinformasjon.

|  | Attract | Jobbpakking via LinkedIn Recruiter | Recruiter System Connect-API |
|---|---|---|---|
| **Beskrivelse** | Attract posterer jobber til LinkedIn som en XML-feed. | Selskapet inngår kontrakt med LinkedIn og gir en XML-feed for postering av jobber. | Kunden bruker API-et til å synkronisere informasjon mellom Attract og LinkedIn Recruiter. |
| **Hvilken type jobb kan jeg postere?** | Begrenset oppføring | Premium jobbplass eller begrenset oppføring | Begrenset oppføring |
| **Kan jeg fremme jobben på LinkedIn?** | Nei | Premium jobbplasser: Ja<br>Begrensede oppføringer: Nei | Nei |
| **Hvor ofte posterer LinkedIn jobber?** | En gang om dagen | En gang om dagen | Flere ganger per dag, som definert av API-et |
| **Anbefalt av LinkedIn?** | Nei | Ja | Nei |
| **Hva trenger jeg?** | Kjøp av Attract | En jobbpakkingskontrakt med LinkedIn og kjøp av premium jobbplasser | En API-avtale med LinkedIn | 
| **Hvor kan jeg finne mer informasjon?** | [Konfigurere integrering med LinkedIn for Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md) | [Jobbpakking via LinkedIn Recruiter - Oversikt](https://www.linkedin.com/help/recruiter/answer/79037) | [Recruiter System Connect](https://docs.microsoft.com/linkedin/talent/recruiter-system-connect) |

> [!NOTE]
> Du trenger ikke en LinkedIn Recruiter System Connect-lisens for å postere jobber til LinkedIn med Attract.

## <a name="see-also"></a>Se også

[Konfigurere integrering med LinkedIn for Microsoft Dynamics 365 Talent - Attract](./attract-admin-linkedin.md)

[Postere jobber til LinkedIn fra Microsoft Dynamics 365 Talent - Attract](./attract-post-jobs-to-linkedin.md)

[Finne kandidater med LinkedIn Recruiter i Microsoft Dynamics 365 Talent - Attract](./attract-linkedin-recruiter.md)

[Feilsøke integrering med LinkedIn og Microsoft Dynamics 365 Talent - Attract](./attract-troubleshoot-linkedin.md)
