---
title: Konfigurere integrering med LinkedIn for Microsoft Dynamics 365 for Talent - Attract
description: Dette emnet forklarer hvordan du konfigurerer LinkedIn-integrering for Microsoft Dynamics 365 for Talent - Attract, slik at du enkelt kan legge inn jobber på LinkedIn fra Attract, og slik at rekrutterere kan synkronisere sin rekrutteringsinformasjon med en kandidats LinkedIn-profil.
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
ms.author: anbichse
ms.search.validFrom: 2019-07-08
ms.dyn365.ops.version: Talent October 2018 update
ms.openlocfilehash: 8e42ec7d0bb74089b4e915b5a30277401e694cf9
ms.sourcegitcommit: c62756cb04549b2ff5de9b93d497e964a340335a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/17/2019
ms.locfileid: "1756228"
---
# <a name="set-up-linkedin-integration"></a>Konfigurere LinkedIn-integrering

[!include[banner](../includes/banner.md)]

Hjelp rekrutterere og ansettelsesansvarlige med å tiltrekke topptalent ved å konfigurere LinkedIn-integrasjon med Microsoft Dynamics 365 for Talent: Attract. Attract lar deg legge inn jobber direkte på LinkedIn, det største profesjonelle online-nettverket.

Jobber som du legger ut på LinkedIn via Attract, er "Begrensede oppføringer" (Limited Listings) og leveres uten ekstra kostnad til din bedrift. Disse oppføringene er bare tilgjengelige gjennom LinkedIn-programvarepartnere som Attract. De vises ikke i **Karriere**-panelet på firmaets LinkedIn-side fordi der vises bare betalte oppføringer. Men de vises når potensielle kandidater viser alle tilgjengelige jobber. Begrensede oppføringer vises også i jobbsøk på LinkedIn.

Attract har to måter å integrere med LinkedIn på slik at du kan finne kandidater på dette populære karrierenettstedet:

- Postere jobber fra Attract til LinkedIn.
- Finne kandidater fra LinkedIn til Attract.

Du konfigurerer begge alternativene i kategorien **LinkedIn-integrasjon** i administrasjonssenteret. Hvis du vil åpne administrasjonssenteret, går du til <https://attract.talent.dynamics.com/adminsettings>.

> [!NOTE]
> Hvis du vil bruke LinkedIn Recruiter-integrering med Attract, må du ha [tillegget for omfattende ansettelse](https://docs.microsoft.com/dynamics365/unified-operations/talent/attract-comprehensive-hiring) og [LinkedIn Recruiter-lisenser](https://business.linkedin.com/talent-solutions/cx/17/08/recruiter-demo-fs2-k18). For mer informasjon, se [Hvilken versjon av Attract?](./attract-comprehensive-hiring.md).

Hvis du har problemer med å publisere jobber til LinkedIn, kan du se [Feilsøke integrering med LinkedIn](./attract-troubleshoot-linkedin.md).

Hvis du vil ha informasjon om andre måter å publisere jobber til LinkedIn på, kan du se [Vanlige spørsmål om LinkedIn](./attract-linkedin-faq.md).

## <a name="configure-job-posting-to-linkedin"></a>Konfigurere jobbpostering til LinkedIn

Før du kan legge inn jobber fra Attract til LinkedIn, trenger du en [LinkedIn-firma-ID](https://aka.ms/findID). LinkedIn-firma-IDen er en streng med tall som unikt identifiserer firmaet i LinkedIn. Hvis du vil ha mer informasjon, kan du se [Knytte LinkedIn-firma-ID-en til LinkedIn-jobbtavlen - Vanlige spørsmål](https://aka.ms/findID).

Attract sender en feed for jobbposteringene til LinkedIn, og LinkedIn sjekker for feeden omtrent én gang per dag. Det kan ta opptil 48 timer før jobbene dine er postert på nettstedet.

Jobber som posteres til LinkedIn, vises på det live LinkedIn-området. LinkedIn har ikke et testmiljø for postering av jobber. Derfor må du passe på at du ikke ved et uhell legger ut testjobber. 

1. På **Oppsett**-menyen (tannhjulssymbolet) i øvre høyre hjørne, velg **Administrasjonssenter**. Eventuelt kan du gå til <https://attract.talent.dynamics.com/adminsettings>.
2. Velg fanen **LinkedIn-integrering**.
3. Under **Firmanavn**skriver du inn navnet på firmaet, og under **firma-ID**angir du ID-en for LinkedIn-firmaet. Kontroller at firmanavnet samsvarer med navnet som vises på firmaets LinkedIn-side. Hvis du vil ha mer informasjon om firma-ID-er for LinkedIn, kan du se [Knytte LinkedIn-firma-ID-en til LinkedIn-jobbtavlen - Vanlige spørsmål](https://www.linkedin.com/help/linkedin/answer/98972).

    Hvis du må endre informasjon for organisasjonen, kan du se [Endre organisasjonens adresse, teknisk kontakt og mer](https://docs.microsoft.com/office365/admin/manage/change-address-contact-and-more). Hvis du fortsatt har problemer, kan du kontakte [kundestøtte for LinkedIn](https://www.linkedin.com/help/linkedin).

4. Velg **Lagre**.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Sette opp LinkedIn Recruiter med Attract 

Hvis du vil la rekrutterere finne jobber via LinkedIn Recruiter, må du konfigurere integrering med LinkedIn Recruiter i Attract. For å fullføre konfigurasjonen må du arbeide med brukeren som er administrator på organisasjonens LinkedIn Recruiter-kontrakt.

1. På **Oppsett**-menyen (tannhjulssymbolet) i øvre høyre hjørne, velg **Administrasjonssenter**. Eventuelt kan du gå til <https://attract.talent.dynamics.com/adminsettings>.
2. Velg fanen **LinkedIn-integrering**.

    [![Attract-administratorvisning for å starte LinkedIn Recruiter-integrering](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Velg **Koble til** for å starte oppsettet. Du vil bli veiledet gjennom påloggingsprosessen for LinkedIn.
4. Hvis du har plasser i flere LinkedIn-kontrakter, velger du kontrakten du vil koble til Attract-systemet. Hvis du har en plass i bare én LinkedIn-kontrakt, kan du hoppe over dette trinnet.
5. Under **Tilkobling til rekrutteringssystem (RSC)** velger du **Forespørsel**.

    [![Attract-administratorvisning for å be om LinkedIn Recruiter-integrering](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6. Innstillingen **Tilkobling til rekrutteringssystem (RSC)** skal nå vises som **Partner klar**. Hvis du ser **Varsle partner** på denne siden, venter du litt, velger **Varsle partner** og oppdaterer deretter siden. Innstillingen skal nå vises som **Partner klar**.

    [![Attact-administratorvisning for å angi at Attract-siden av forespørsler er fullført](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

7. For å fullføre følgende trinn må du ha administratorrettigheter i LinkedIn Recruiter-kontrakten.

    1. Logg på LinkedIn ved å bruke administratorkontoen, og velg deretter **LinkedIn Recruiter** øverst til høyre. 
    2. På **Flere**-menyen øverst på siden velger du **Administrasjonsinnstillinger**, og velger deretter **ATS**-kategorien.
    3. Hvis du vil aktivere ettklikkseksport for bare én kontrakt, må du aktivere **Kontraktnivåtilgang (for hvert sete i denne kontrakten)**. Hvis du vil aktivere det for hele firmaet, aktiverer du **Firmanivåtilgang (for hver kontrakt i firmaet)** .

    [![Slå på Attract-integrering fra administratorvisningen for LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)

8. I administrasjonssenteret for Attract velger du kategorien **LinkedIn-integrering**. Innstillingen **Tilkobling til rekrutteringssystem (RSC)** skal nå vises som **Aktivert**.

    [![LinkedIn Recruiter-integrering er fullført](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="set-up-apply-with-linkedin-in-attract"></a>Definere Søk med LinkedIn i Attract

Du kan la kandidater søke på jobbene dine ved hjelp av LinkedIn-profilene. Hvis du vil ha mer informasjon om Søk med LinkedIn, kan du se [Kraften til LinkedIn overalt: Søk med LinkedIn](https://blog.linkedin.com/2011/07/24/apply-with-linkedin).

Denne funksjonen er for øyeblikket i forhåndsvisningen. Før du følger denne fremgangsmåten, må du kontrollere at Søk med LinkedIn er aktivert. Hvis du vil ha mer informasjon om hvordan du aktiverer forhåndsvisningsfunksjoner, se [Tilgang til forhåndsvisningsfunksjoner i Talent](./access-preview-feature.md).

1. På **Oppsett**-menyen (tannhjulssymbolet) i øvre høyre hjørne, velg **Administrasjonssenter**. Eventuelt kan du gå til <https://attract.talent.dynamics.com/adminsettings>.
2. Velg fanen **LinkedIn-integrering**.

    [![Attract-administratorvisning for å starte LinkedIn Recruiter-integrering](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3. Velg **Koble til** ved siden av **Søk med LinkedIn** for å starte oppsettet. Du vil bli veiledet gjennom resten av prosessen med LinkedIn.

## <a name="see-also"></a>Se også

[Vanlige spørsmål om LinkedIn](./attract-linkedin-faq.md)

[Postere jobber på eksterne områder fra Attract](./posting-jobs-external.md)

[Finne kandidater med LinkedIn Recruiter](./attract-linkedin-recruiter.md)

[Opprette jobber](./creating-jobs-attract.md)

[Feilsøke integrering med LinkedIn](./attract-troubleshoot-linkedin.md)
