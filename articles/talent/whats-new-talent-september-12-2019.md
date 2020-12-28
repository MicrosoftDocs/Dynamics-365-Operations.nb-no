---
title: Hva er nytt eller endret i Dynamics 365 for Talent (10. september 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0aadecd5b37759492f7895ccfda1a777793a08b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4462107"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Hva er nytt eller endret i Dynamics 365 for Talent (10. september 2019)

Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

### <a name="candidate-e-mail-login"></a>E-postpålogging for kandidat

Kandidater kan nå bruke hvilken som helst e-postadresse til å opprette en konto og logge på et karriereområde i Talent for å søke på jobber og sjekke søknadsstatusen. Dette er i tillegg til at de allerede kan logge på karriereområdet i Talent ved hjelp av sine kontoer for sosiale medier eller legitimasjonen for organisasjonen.

### <a name="job-activation-and-posting"></a>Stillingsaktivering og -utlysing

Vi har gjort noen endringer i stillingsaktiveringen og -utlysingen. Du må aktivere stillinger før du legger dem inn på karriereområdet i Talent eller til eksterne stillingstavler, inkludert LinkedIn eller Broadbean.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2482. Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Du kan aktivere forhåndsvisningsfunksjoner i sandkasse- og prøvemiljøer

Når du klargjør en ny forekomst av Talent, kan du angi om forekomsttypen er Produksjon eller Sandkasse. Forekomster av typen Sandkasse gjør at nye funksjoner kan testes tidlig. Hvis du vil at en av de eksisterende forekomstene skal oppdateres til forekomsttypen Sandkasse, kan du kontakte kundestøtten for å starte endringsforespørselen.

Hvis du vil ha mer informasjon om hvordan du publiserer endringer, kan du se [Klargjøre Talent](./provisioning-talent.md).

### <a name="platform-update-29"></a>Plattform update 29

Hvis du vil ha mer informasjon om Platform update 29, kan du se [Forhåndsvisningsfunksjoner i Dynamics 365 for Finance and Operations Platform Update 29 (oktober 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>Ny jobbasisenhet er tilgjengelig i rammeverk for databehandling (347202)

Med denne versjonen er en ny grunnleggende jobbenhet tilgjengelig for import/eksport av data. 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>Avansert sikkerhetspolicy for arbeider viser feil stillinger i stillingshierarkiet (354868)

Med denne versjonen vises ikke lenger stillinger med en "tom" arbeider når brukere har begrenset tilgang.

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>Lukkeknappen for jobbskjema lukker ikke skjemaet i enkelte situasjoner (342467)

Denne versjonen inneholder en endring som gjør at jobbskjemaet lukkes i alle scenarier.

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>Ny sak i ansattpost er låst for personalsjefrollen (337111)

Med denne endringen låses ikke lenger saksskjemaet under tilgang til det fra ansattskjemaet.

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>Sluttdato for ansettelse har alltid standardverdien 23:59:59 (351492)

Med denne endringen kan du endre ansettelsesdatoen til et annet klokkeslett enn 23:59:59 når du avslutter en ansettelse manuelt.

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>Kan ikke definere utløpsdato for inntektskode via databehandling (336604)

I denne versjonen kan du definere inntekstkoder som utløper gjennom enheten **PayrollWorkerPositionEarningCodeEntity**.

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>Analyserapport for ansattutvikling viser ikke data (348737)

I denne ukes utgivelse er analysen av ansattkompetanse oppdatert for å gi nøyaktig rapportering.

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>Dato/klokkeslett for ansettelsesbetingelser er ikke standard satt til begynnelsen av dagen (349101)

Med denne endringen settes nå startdato-/klokkeslett som standard til begynnelsen av dagen, og sluttdato-/klokkeslett settes til slutten på dagen.

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>Endring av sluttdatoen for ansettelsen i Arbeiderhandling-skjemaet vises en feilmelding (354092) 

Denne endringen løser et problem ved endring av sluttdatoen for ansettelsen som en del av arbeiderhandlingen.

### <a name="applying-onboarding-checklists-across-companies-338433"></a>Bruker sjekklister jobbintroduksjon på tvers av firmaer (338433)

Denne versjonen gir nå mulighet til å bruke sjekklister for ansatte som er ansatt i andre juridiske enheter enn den påloggede juridiske enheten.

## <a name="in-preview"></a>I forhåndsvisning

### <a name="streamlined-employee-entry-and-navigation"></a>Strømlinjeformet ansattoppføring og navigasjon

Denne funksjonaliteten er nå tilgjengelig i sandkassemiljøer. Hvis du vil aktivere denne funksjonen, går du til **Systemadministrasjon > Koblinger > Oppsett > Systemparametere> Forhåndsvisningsfunksjoner**. Velg **Utvidet arbeiderskjema og navigering**. Dette vil aktivere disse endringene for alle brukere. Du kan når som helst deaktivere dette alternativet.

Hvis du vil ha mer informasjon, se [Strømlinjeformet ansattoppføring og navigasjon](./streamlined-employee-entry.md).
