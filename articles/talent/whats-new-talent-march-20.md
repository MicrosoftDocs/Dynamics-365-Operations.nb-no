---
title: Hva er nytt eller endret i Dynamics 365 Talent (20. mars 2019)?
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 03/20/2019
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
ms.search.validFrom: 2019-03-20
ms.dyn365.ops.version: Talent
ms.openlocfilehash: a7a44e1c9d8dcb4b2cc81a682a044d26cdc1149e
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2019
ms.locfileid: "2812701"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-march-20-2019"></a>Hva er nytt eller endret i Dynamics 365 Talent (20. mars 2019)?

[!include [banner](includes/banner.md)]

Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.

## <a name="changes-in-attract"></a>Endringer i Attract

### <a name="setting-the-audience-on-activities"></a>Angi målgruppe for aktiviteter
Aktiviteter i systemet kan nå definere målgruppen. Prosessrelaterte aktiviteter (for eksempel intervju, tidsplan, tilbakemelding og EEO) kan settes til Alle kandidater, interne kandidater og Eksterne kandidater. Egendefinerte aktiviteter, for eksempel Microsoft Forms, YouTube-videoer og webinnhold, kan leveres til Alle kandidater, Interne kandidater, Eksterne kandidater eller ansettelsesteam.  

### <a name="improve-career-site-job-discoverability-search-engine-optimization"></a>Forbedre jobbsynlighet i karriereområdet: Optimalisering av søkemotor
Denne funksjonen gjør det mulig for søkemotorer å nå og indeksere ledige stillinger på Attract-karriereområdet. Dette hjelper kandidatene med å søke etter jobber som er postert til Attract-karriereområdet, ved hjelp av populære søkemotorer.

### <a name="show-login-hint-to-candidates-who-forgot-their-credentials"></a>Vise påloggingstips til kandidater som har glemt legitimasjonen
Hvis en kandidat har glemt den sosiale legitimasjonen de brukte til å søke etter en jobb under åpning av en kobling som ble lagret eller sendt med e-post til dem, vil de nå se et tips med navnet på leverandøren og brukernavnet (gjort uforståelig). Dette gjør at de bruker riktig legitimasjon for å få tilgang til jobbsøknaden.

### <a name="help-internal-candidates-explore-internal-jobs"></a>Hjelpe interne kandidater å utforske interne stillinger
Et problem er løst der eksterne kandidater kunne se navnet på rekrutteringspersonen eller ansettelseslederen for en jobb. Bare interne kandidater kan nå se ansettelsesteammedlemmene for en jobb. Det er også enklere for interne kandidater å vise og søke på bare interne jobber. Når en kandidat prøver å få tilgang til koblingen for å vise eller søke på en intern jobb, må de godkjennes ved hjelp av Azure Active Directory-legitimasjon. Interne kandidater har også muligheten til å kontakte ansettelsesteammedlemmene for å uttrykke interesse for eller finne ut mer om jobben. Denne funksjonen er tilgjengelig for alle jobber for bare interne kandidater. Hvis du vil ha mer informasjon, se [Konfigurere karriereområdet i Microsoft Dynamics 365 Talent - Attract](./career-site.md).

### <a name="designate-silver-medalists-to-assign-high-value-applicants-for-future-positions"></a>Registrere personer som er innstilt som nummer to, for å tilordne søkere med høy verdi til fremtidige stillinger
Rekrutteringspersoner og -ledere vedlikeholder ofte en løpende liste over søkere som passer godt for stillingen, men som ikke kunne få et tilbud om jobb, fordi stillingen allerede var besatt. Slike søkere, som er innstilt som nummer to, er verdifulle fordi de kan bidra til å redusere tiden det tar å ansette neste gang en lignende stilling lyses ut. I Attract er det nå mulig for rekrutteringspersoner og -lederne å angi personer som er innstilt som nummer to på søkerlisten, hvis søkeren har avansert til tilbudsstadiet. Angivelsen av personer som er innstilt som nummer to, vil vises i søkerlisten for jobben, men også i talentsamlingsvisningen når disse søkerne er medlemmer av samlingene til bemanningskonsulenter eller -ledere. I tillegg vises angivelsen i loggen for jobben, som en del av talentsamlingsprofilen for en kandidat. Du kan forhåndsvise denne funksjonen ved at en administrator aktiverer den ved hjelp av [funksjonsbehandling i administrasjonssenteret](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature).

### <a name="add-applicants-to-talent-pools"></a>Legge til søkere i talentsamlinger
Nå er det enklere å legge til søkere i talentsamlinger ved å vise en ny handling i søkerlisten. Ved å velge ikonet **Legg til i talentsamling** kan bemanningskonsulenten eller -lederen velge fra listen over talentsamlinger og enkelt legge til søkere i talentsamlinger rett fra søkerlisten for en jobb.

### <a name="configure-whether-a-resume-is-required-to-apply-for-a-particular-job"></a>Konfigurere om en CV kreves for å søke på en bestemt jobb
Basert på tilbakemeldinger fra kunder kan rekrutteringspersoner nå konfigurere om det kreves en CV, i form av en opplastet fil, når det skal søkes på en bestemt jobb. Denne konfigurasjonen er en del av søknadsaktiviteten, som er tilgjengelig i ansettelsesprosessen. Når den er aktivert, vil alle potensielle søkere bli bedt om å laste opp en CV når de søker på denne stillingen. Søknaden vil ikke blir vurdert som fullført med mindre en CV er lastet opp. Dette vil redusere støyen i søkersamlingen ved å sørge for at alle søkere gir tilstrekkelig informasjon til å tillate at rekrutteringspersonen kan sortere dem.

### <a name="candidates-can-apply-to-a-job-using-their-linkedin-profile"></a>Kandidater kan søke på en jobb ved hjelp av LinkedIn-profilen
Kandidater som allerede har en oppdatert profil på LinkedIn, kan søke på jobber med ett enkelt klikk ved hjelp av denne profilen.

### <a name="track-how-a-candidate-profile-originated-in-the-system-and-where-your-applicants-discover-the-jobs-they-applied-for"></a>Spore hvor en kandidatprofil kommer fra i systemet, og hvor søkerne fant jobbene de søkte på
Du kan nå finne ut hvor profilen til en bestemt kandidat kommer fra i Attract ved å se på profilkilden under kandidatdetaljene på **Profil**-siden for en søknads- eller talentsamlingsprofil. På samme måte kan du finne ut hvordan en søker oppdaget jobben, ved å se på søknadskilden i **Søknadsaktivitet** i aktivitetsfeeden for søknaden. Denne informasjonen er også tilgjengelig i loggen for jobben i talentsamlingsprofilen. Når rekrutteringspersoner eller -ledere legger til kandidater manuelt, vil de også bli bedt om å angi søknadskilden eller kandidatprofilen. Når en kandidat søker for første gang, blir profilkilden den samme som opprinnelsen til søknaden. Du kan forhåndsvise denne funksjonen ved at en administrator aktiverer den ved hjelp av [funksjonsbehandling i administrasjonssenteret](https://docs.microsoft.com/dynamics365/unified-operations/talent/access-preview-feature). Legg merke til at eksisterende kandidater og søkere ikke har noen kildeinformasjon. Rekrutteringspersoner kan imidlertid legge til disse opplysningene manuelt.

## <a name="changes-in-onboard"></a>Endringer i Onboard

Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Endringer i Core HR

Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2195

### <a name="attract-integration-throws-duplicate-record-error-for-applications"></a>Attract-integrering viser duplisert post-feil for søknader
I denne oppdateringen er et problem med like poster løst. Dette problemet vises når du åpner **Personaladministrasjon**-arbeidsområdet.

### <a name="unable-to-close-form-when-editing-name-sequence"></a>Kan ikke lukke skjemaet ved redigering av navnerekkefølge
Endringer er gjort for å løse et problem når du redigerer navnerekkefølgen i arbeiderskjemaet.

## <a name="coming-soon"></a>Kommer snart

###  <a name="advanced-compensation-security-fixed-and-variable"></a>Avansert kompensasjonssikkerhet (fast og variabel)
I mange organisasjoner kan kompensasjons- og fordelsansvarlige bare ha tilgang til bestemte kompensasjonsposter. Disse kan være for ledere eller regionale ansatte. Med denne endringen kan HR administrere og vedlikeholde kompensasjonsplanene for ulike ansattgrupper i organisasjonen. Faste og variable planer kan tilordnes til sikkerhetsroller, som bestemmer tilgangen til planene og ansattdataene som er knyttet til dem, for eksempel lønns- eller bonusposter. Bare rollene der tilgang er gitt, kan behandle kompensasjon for disse ansatte.

###  <a name="email-support-for-alerts"></a>E-poststøtte for varsler
Med Platform update 24 for Finance and Operations kan brukere opprette varslingsregler som automatisk leverer e-postmeldinger til kontakter når de utløses av en hendelse.

### <a name="duplicate-employee-check-interface-changes"></a>Kontroller av dupliserte ansatte: Endringer i grensesnittet
Med denne endringen oppdages duplikater når du angir navnefelt, og statusen viser hvor mange duplikater som ble funnet. Du kan velge den angitte lenken for å åpne en ny side for å vurdere om du vil bruke resultatet som ble funnet. For å unngå å forstyrre dataregistreringen åpnes duplikatskjemaet ikke automatisk.


