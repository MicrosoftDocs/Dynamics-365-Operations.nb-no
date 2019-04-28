---
title: Hva er nytt eller endret i Dynamics 365 for Talent Core HR (14. desember 2018)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent Core HR.
author: Darinkramer
manager: AnnBe
ms.date: 12/14/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2018-12-14
ms.dyn365.ops.version: Talent
ms.openlocfilehash: c2d209cac52665053b664a93bfb6c35e171b0948
ms.sourcegitcommit: 9796d022a8abf5c07abcdee6852ee34f06d2eb57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/12/2019
ms.locfileid: "949857"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-core-hr-december-14-2018"></a>Hva er nytt eller endret i Dynamics 365 for Talent Core HR (14. desember 2018)?

[!include [banner](includes/banner.md)]

**Build 8.1.2085**

Dette emnet beskriver funksjoner som enten er nye eller endret i Core HR.

## <a name="changes"></a>Endringer

### <a name="us---aca-affordable-care-act-support-for-tax-year-2018-1095-b-and-1095-c-forms"></a>USA - ACA (lov om Affordable Care)-støtte for skatteåret 2018 1095-B- og 1095-C-skjemaer

Hvert år må aktuelle store arbeidsgivere angi alle fulltidsansatte med 1095-C. Hvis arbeidsgiveren også gir selvforsikret dekning, må de angi 1095-C (hvis de er en større arbeidsgiver) og 1095-B (hvis de er en mindre arbeidsgiver) for ansatte, fulltid eller deltid, som dekkes av en av de tilbudte helseplanene. Denne funksjonen gir utskrivbare skjemaer for både 1095-C og 1095-B.

### <a name="during-import-submittedbypersonid-field-on-hcmperfjournalentity-is-ignored"></a>Under import ignoreres SubmittedByPersonId-feltet i HcmPerfJournalEntity

Ved import/eksport av ytelsesjournalposter ignoreres **Sendt av**-feltet. Med denne endringen gjenspeiler verdien **importert/eksportert** verdien i tabellen under eksporten. Ved import oppdateres systemet med verdien som er angitt i importfilen.

### <a name="analytics-tab-on-leave-and-absence-workspace-displays-openconnectionerror-error-for-non-system-admin-roles"></a>Analyse-kategorien i arbeidsområdet Permisjon og fravær viser feilen OpenConnectionError for ikke-systemadministratorroller

Med denne oppdateringen utstedes det ikke feil når du åpner **Analyse**-kategorien i **Permisjon og fravær**-arbeidsområdet.

### <a name="employee-self-service-position-hierarchy-drill-down-from-tile-fails-to-get-parent-node"></a>Neddrilling i Ansattselvbetjening, Stillingshierarki fra flis kan ikke hente overordnet node

En endring er gjort for å rette feilen «Henting av den overordnede noden mislyktes» når stillingshierarkiet er tilpasset for å vises i et eksisterende arbeidsområde og en stilling er valgt i hierarkiet.  

### <a name="must-be-system-admin-to-see-the-payroll-tab-in-the-position-page"></a>Må være systemadministrator for å kunne se kategorien Lønn på Stilling-siden

En endring er gjort for å inkludere de riktige sikkerhetselementene i den eksisterende rettigheten: Vedlikehold lønnsdetaljer for arbeider og stilling. Med denne endringen får lønnsadministratoren som standard tilgang til lønnsfeltene på Stilling-siden.

### <a name="error-when-submitting-performance-review-to-manager-and-the-reviewsperfperiod-placeholder-is-used-in-the-submission-instructions"></a>Feil når du sender prestasjonsvurdering til leder og plassholderen %Reviews.PerfPeriod% brukes i sendeinstruksjonene

Det er gjort en endring som retter opp feilen Nullreferanse når du bruker plassholderen %Reviews.PerfPeriod% i sendeinstruksjonene.

### <a name="workforce-power-bi-report-shows-error-when-worker-seniority-date-is-a-leap-day"></a>Workforce Power BI-rapporten viser feil når arbeiderens ansiennitetsdato er en skuddårsdag.

Med denne endringen støttes nå skuddårsdager i Power BI.

### <a name="integration-between-core-hr-and-attract"></a>Integrasjon mellom Core HR og Attract

En endring er gjort for å oppdatere integreringen mellom Core HR og Attract knyttet til kandidater som skal ansettes. For at kandidater som skal ansettes, skal vises i **Personaladministrasjon**-arbeidsområdet brukes følgende Common Data Service-enheter:

Stillingssøknad
- Statusårsak må settes til Tilbud godtatt
-   Angir kandidat og ledig stilling

Kandidat
-   Angir kandidatinformasjon

Ledig stilling
-   Angir ID for ledig stilling og deltakere for ledig stilling

Deltakere for ledig stilling
-   Angir ansettelsesansvarlig

Når en kandidat legges til personaladministrasjon, kan kandidaten nå også forkastes ved hjelp av et nytt alternativ på kandidatkortet.

## <a name="coming-soon"></a>Kommer snart

### <a name="leave-and-absence-future-leave-and-forecasting-leave-balances"></a>Permisjon og fravær: Saldoer for fremtidig permisjon og permisjonsprognoser

Med endringene som gjøres for å la ansatte planlegge avspasering og be om fremtidige fraværsforespørsler uten å påvirke gjeldende avspaseringssaldoer, endres også måten avspaseringssaldoer vises på. 

Tilgjengelig saldo som vises nå, er hvor mye avspasering som er tilgjengelig for forespørsler, inkludert avsetninger til og med i dag og alle godkjente permisjonsforespørsler til sluttidspunktet. 

Når muligheten for prognostisering gis ut, endres den viste saldoen til gjeldende avspaseringssaldo, inkludert avsetninger til og med i dag og forespørsler til og med i dag. Ansatte og ledere vil se disse oppdaterte saldoene i ansatt- og lederselvbetjening på **Fridager**-kortet og i vinduet for **avspaseringssaldoer**. Personalledere vil se disse oppdaterte saldoene i **Personer**-arbeidsområdet og i vinduet **Tilordnede permisjonsplaner** for ansatte.

## <a name="known-issue"></a>Kjent problem

### <a name="mapping-errors-in-the-integration-with-finance-and-operations"></a>Tilordningsfeil i integrasjonen med Finance and Operations

Følgende problemer er identifisert i gjeldende mal for integrering av Talent med Dynamics 365 for Finance and Operations. En ny mal blir snart publisert og skal brukes på alle nye integrasjonsprosjekter som opprettes. For eksisterende integrasjonsprosjekter kan oppgavetilordningene oppdateres. Se følgende tabell for oppdaterte tilordninger. 

>[!NOTE]
> Den overordnede jobbtilordningsoppgaven for jobbstillinger til stillinger kan ikke integrere data. Dette er et problem som undersøkes nå. Det finnes ingen løsning i gjeldende tilordning. 

Avdelinger til driftsenhet-oppgaven må ha følgende tilordninger oppdatert.

| Eksisterende kildefelt          | Nytt kildefelt |
| -------------------------------|------------------|
| cdm_description (beskrivelse)  | cdm_name (navn)  |

En ekstra tilordning må også legges til. Velg det siste **Ingen**-feltet for å legge til følgende tilordning.

| Kildefelt                   | Målfelt    |
| -------------------------------|----------------------|
| cdm_description (beskrivelse)  | NAMEALIAS (NAMEALIAS)|

De oppdaterte tilordningene skal se ut som følgende bilde.

![Avdelinger til driftsenhet-oppgaven](./media/DepartmentMapping.png)


Jobber til jobbdetaljer-oppgaven må ha følgende tilordninger oppdatert.

| Eksisterende kildefelt          | Nytt kildefelt                   |
| -------------------------------|------------------------------------|
| cdm_name (navn)                | cdm_description (beskrivelse)      |
| cdm_name (beskrivelse)         | cdm_jobdescription(jobbeskrivelse)|


De oppdaterte tilordningene skal se ut som bildet nedenfor.

![Jobber til jobbdetaljer-oppgaven](./media/JobMapping.png)

Arbeidere til arbeid-oppgaven må ha følgende tilordninger oppdatert.

| Eksisterende kildefelt                 | Nytt kildefelt                               |
| --------------------------------------|------------------------------------------------|
| cdm_emailaddress1 (e-postadresse 1)   | cdm_primaryemailaddress (primær e-postadresse) |
| cdm_telephone1 (telefon 1)          | cdm_primarytelephone (hovedtelefon)       |

Endringen av Kjønn-feltet må også oppdateres. Velg tilordningstypen **fn** (funksjon) for kjønn og oppdater følgende verditilordninger.

| Common Data Service-verdi                   | Finance and Operations-verdi                     |
| ----------------------------|--------------------------------------------------|
| 75440000                    | Mann                                             |
| 75440001                    | Kvinne                                           |
| 75440002                    | Ingen                                             | 
| 75440003                    | Ikke-spesifikt                                      |

De oppdaterte tilordningene skal se ut som følgende bilder.

![Arbeidere til arbeider-oppgaven](./media/WorkerMapping.png)

![Endring av Kjønn-feltet](./media/WorkerTransform.png)
