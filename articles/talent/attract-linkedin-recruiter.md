---
title: Finne kandidater med LinkedIn Recruiter i Microsoft Dynamics 365 for Talent - Attract
description: Bruk LinkedIn-integreringen som leveres av Microsoft Dynamics 365 for Talent - Attract, til å finne jobbkandidater via LinkedIn Recruiter.
author: andreabichsel
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
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.search.industry: ''
ms.author: anbichse
ms.search.validFrom: 2018-10-15
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 14aba16fa81a8f25d0f88247319254407d428b2a
ms.sourcegitcommit: 7c49475402632069685df714546770d30804af7f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/11/2019
ms.locfileid: "1739455"
---
# <a name="source-candidates-with-linkedin-recruiter"></a>Finne kandidater med LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

LinkedIn er verdens største profesjonelle online-nettverk, som gir deg tilgang til verdens beste talenter. Med Microsoft Dynamics 365 for Talent: Attract kan du finne kandidater direkte fra LinkedIn. Derfor er det enklere enn noensinne å finne talentet du trenger for å besette de åpne stillingene. Når du har satt opp tilkoblingen til LinkedIn via Attract, kan du vise potensielle LinkedIn-kandidater for stillingene dine og eksportere dem til Attract med bare ett klikk.

Hvis du ikke har denne funksjonen, kan du kontakte administratoren din. Før du kan dra nytte av LinkedIn Recruiter fra Attract, må administratoren [konfigurere integrering med LinkedIn](./attract-admin-linkedin.md). Du kan deretter konfigurere tilkoblingen til LinkedIn Recruiter og begynne å finne kandidater.

## <a name="set-up-your-connection-with-linkedin-recruiter"></a>Konfigurere tilkoblingen til LinkedIn Recruiter

Før du kan begynne å arbeide med LinkedIn Recruiter via Attract, må du sette opp tilkoblingen til LinkedIn Recruiter. For dette trinnet trenger du LinkedIn Recruiter-legitimasjonen din.

1. Velg **Innstillinger**-knappen (tannhjulikonet) øverst til høyre på siden.
2. Velg **Brukerinnstillinger**.
3. I kategorien **Tilkoblinger** velger du **Koble til** ved siden av **LinkedIn**. Følg instruksjonene som gis av LinkedIn.

    ![[Sette opp tilkobling til LinkedIn Recruiter fra Attract](./media/attract-set-up-linkedin-recruiter-connection.png)](./media/attract-set-up-linkedin-recruiter-connection.png)

## <a name="view-linkedin-candidates-in-attract"></a>Vise LinkedIn-kandidater i Attract

Når du er koblet til LinkedIn Recruiter, kan du se kandidatenes LinkedIn-profiler i Attract.

1. Velg **Jobber** eller **Talentsamlinger** til venstre i Attract, og velg deretter en søker.

    ![[Vise LinkedIn-kandidater i Attract](./media/attract-view-linkedin-candidates.png)](./media/attract-view-linkedin-candidates.png)

2. Velg fanen **LinkedIn** i kandidatens profil. Du kan vise kandidatens profil, sammen med InMail-logg og LinkedIn-notatlogg.

Herfra kan du lagre kandidaten i et LinkedIn Recruiter-prosjekt, sende inMail eller bruke Oppdater meg til å angi et varsel i LinkedIn Recruiter.

> [!NOTE]
> En kandidats LinkedIn-profil vil vises i Attract når kandidatens Attract-informasjon samsvarer med LinkedIn-informasjonen. Her er samsvarsreglene som brukes:
> 
> 1. Hvis e-postadressen og medlems-ID-en for LinkedIn samsvarer i Attract og LinkedIn, vises kandidatens profil. Kandidater har fortsatt muligheten til å koble til eller koble fra LinkedIn-profilen fra Attract.
> 2. Hvis e-postadressen eller medlems-ID-en for LinkedIn ikke samsvarer, ser du en liste over mulige kandidater. Du kan deretter velge en kandidat i listen og koble profilen.
> 3. Hvis det ikke er noen gode treff, blir du varslet om at det ikke ble funnet noen treff.

## <a name="export-linkedin-candidates-to-attract-with-one-click"></a>Eksportere LinkedIn-kandidater til Attract med ett klikk

Når du går gjennom kandidater i LinkedIn Recruiter, kan du eksportere dem til jobber som du har åpne i Attract. For dette trinnet må du ha tillatelse som rekrutterer eller ansettelsesansvarlig i Attract. Hvis du vil ha mer informasjon om roller i Attract, kan du se [Administrasjon av sikkerhet og rolle i Attract](https://docs.microsoft.com/dynamics365/unified-operations/talent/security-attract).

Du må også kontrollere at jobben har et jobbkandidatstadium. Hvis du vil ha mer informasjon, kan du se [Kandidataktivitet](./activities-attract.md#prospect-activity).

1. I Attract oppretter du en jobb, tilordner de riktige rollene og aktiverer jobben.
2. I LinkedIn Recruiter finner du en god kandidat for jobben og går til kandidatens profil.
3. I jobbsøk-boksen i kontaktkortet finner du jobben ved hjelp av tittelen eller jobb-ID-en som ble aktivert i Attract. Hvis du ikke finner jobben, velger du **Endre ATS** for å finne den riktige Attract-forekomsten.
4. Velg jobben, og velg deretter **Eksporter**.
5. Åpne jobben i Attract. Den eksporterte kandidaten vises i kategorien **Prospekt** for jobben.

## <a name="view-attract-information-in-linkedin-recruiter"></a>Vise Attract-informasjon i LinkedIn Recruiter

I LinkedIn Recruiter kan du kontrollere om en kandidat har søkt på andre jobber i organisasjonen, se hvor kandidaten er i forskjellige faser av jobbsøknader og vise tilbakemeldinger og kommentarer fra Attract.

1. Åpne LinkedIn Recruiter, og velg en kandidatprofil.
2. Hold markøren over **In ATS**.
3. Velg ett av følgende alternativer for å vise kandidatinformasjonen som er lagret i Attract:

    - **Jobber og statuser** – Se jobber som kandidaten er del av, den nyeste statusen og hvordan kandidaten videreutvikler seg for hver jobb.
    - **Intervjutilbakemelding**- Se tilbakemeldinger som intervjuerne har sendt i Attract.
    - **Notater** - Se eventuelle notater som er lagt inn for denne kandidaten i Attract.

    ![[Vise Attract-informasjon fra LinkedIn Recruiter](./media/attract-view-information-from-linkedin-recruiter.png)](./media/attract-view-information-from-linkedin-recruiter.png)

> [!NOTE]
> Kandidat- og søknadsdata blir ikke synkronisert med LinkedIn Recruiter hvis kandidaten ikke er forbi jobbkandidatfasen.

## <a name="view-linkedin-talent-pools"></a>Vise LinkedIn-talentsamlinger

Hvis kandidater godtar å dele sin LinkedIn-profil med en bruker i organisasjonen din, opprettes en ny kandidatpost i Attract. Disse kandidatene vises deretter i en systemopprettet LinkedIn-talentsamling.

1. I Attract, velg **Talentsamlinger** til venstre.
2. Velg LinkedIn-talentsamlingen. Du vil se en liste over kandidater og deres stub-profiler fra LinkedIn. Stub-profiler inneholder kandidatens fornavn, etternavn og e-postadresse hvis kandidaten valgte å dele det.

## <a name="see-also"></a>Se også

[Vanlige spørsmål om LinkedIn](./attract-linkedin-faq.md)

[Konfigurere integrering med LinkedIn](./attract-admin-linkedin.md)

[Opprette jobber](./creating-jobs-attract.md)

[Postere jobber til LinkedIn fra Attract](./attract-post-jobs-to-linkedin.md)

[Feilsøke integrering med LinkedIn](./attract-troubleshoot-linkedin.md)
