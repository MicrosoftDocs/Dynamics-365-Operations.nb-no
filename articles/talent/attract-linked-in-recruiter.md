---
title: Kandidatsondering med LinkedIn Recruiter
description: Dette emnet gir informasjon om hvordan du bruker maskinlæring til å få jobb- og kandidatanbefalinger for jobb.
author: andreabichsel
manager: AnnBe
ms.date: 12/07/2018
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
ms.openlocfilehash: 4ac7a302e5bf589beb2b560b0ff5818e90c67139
ms.sourcegitcommit: 608e68b603afef9eb98d8fb25e90109c2473ef87
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/19/2019
ms.locfileid: "859580"
---
# <a name="sourcing-with-linkedin-recruiter"></a>Kandidatsondering med LinkedIn Recruiter
[!include[banner](../includes/banner.md)]

LinkedIn er verdens største talentdatabase og er ofte hovedsystemet som rekrutteringspersoner bruker til å finne, kommunisere med og velge kandidater for jobbene som rekrutteringspersoner vil fylle. LinkedIn Recruiter-integrering med Dynamics 365 for Talent: Attract gjør det enklere for brukere å ansette og holde dataene synkronisert mellom de to systemene.

> [!NOTE]
> Du trenger tillegget for omfattende ansettelse og LinkedIn Recruiter-plasser for å kunne bruke LinkedIn Recruiter-integrering med Attract.

## <a name="set-up-linkedin-recruiter-with-attract"></a>Sette opp LinkedIn Recruiter med Attract 

Før du kan bruke LinkedIn Recruiter-funksjonene, må du konfigurere tilgang på kontraktnivå eller firmanivå med Attract-forekomsten. For å fullføre konfigurasjonen må du arbeide med brukeren som er administrator på LinkedIn Recruiter-kontrakten. Fullfør fremgangsmåten nedenfor for å konfigurere LinkedIn Recruiter med Attract.

1.  Logg på Attract som administrator, og gå til **Administrasjonsinnstillinger**.

2.  I ruten til venstre klikker du på kategorien **LinkedIn-integrering**.

[![Attract-administratorvisning for å starte LinkedIn Recruiter-integrering](./media/LinkedInConnect.png)](./media/LinkedInConnect.png)

3.  Klikk på **Koble til** for å starte oppsettet og bli veiledet gjennom prosessen for LinkedIn-pålogging.

4.  Hvis du har plasser i flere LinkedIn-kontrakter, velger du kontrakten du vil koble til Attract-systemet. Hvis du har en plass i bare én LinkedIn-kontrakt, vil ikke dette trinnet være nødvendig.

5.  LinkedIn-kontrollprogrammet lastes nå i administrasjonsinnstillingene og viser listen over integreringer. Under **Tilkobling til rekrutteringssystem** klikker du **Forespørsel**.

[![Attract-administratorvisning for å be om LinkedIn Recruiter-integrering](./media/RequestLinkedInRSC.png)](./media/RequestLinkedInRSC.png)

6.  Etter at integreringen er forespurt fra Attract, vises det som **Partner klar** og er klar til å aktiveres fra **Administrasjonsinnstillinger for rekrutterer**. Hvis du ser **Varsle partner** på denne siden, venter du litt, klikker på **Varsle partner** og oppdaterer deretter siden. Den skal nå vises som **Partner klar**.

[![Attact-administratorvisning for å angi at Attract-siden av forespørsler er fullført](./media/PartnerReadyRSC.png)](./media/PartnerReadyRSC.png)

For å fullføre neste trinn må du ha en administratorrettighet i LinkedIn Recruiter-kontrakten.

7.  Logg på LinkedIn med administratorkontoen, og gå til LinkedIn Recruiter øverst til høyre. 

8. På **Flere**-menyen øverst på skjermen klikker du på **Administrasjonsinnstillinger**, og klikker deretter på **ATS**-kategorien.

Attract-systemet vises med et par alternativer som kan aktiveres.

9. Hvis du bare vil aktivere 1-klikk-eksport for kontrollprogrammet **In-ATS indicator** og **In-ATS Profile**, velger du **Tilgang på firmanivå**. Hvis du vil aktivere alle tilgangsfunksjoner på firmanivå pluss InMail-logg, Merknader-logg og InMail-stub-profiltilgang, velger du **Tilgang på kontraktnivå**.

10. Slå på ønsket tilgangsnivå fra LinkedIn Recruiter **Admin-ATS**-innstillingene.

[![Slå på Attract-integrering fra administratorvisningen for LinkedIn Recruiter](./media/EnableRSC.png)](./media/EnableRSC.png)

12. Gå tilbake til Attract-administatorinnstillinger som en Attract-administrator og velg kategorien **LinkedIn-integrering**. Nå skal du se at LinkedIn-kontrollprogrammet lastes inn og viser **Aktivert** med det valgte tilgangsnivået aktivert.

[![LinkedIn Recruiter-integrering er fullført](./media/RSCSetupComplete.png)](./media/RSCSetupComplete.png)

## <a name="using-linkedin-recruiter-capabilities"></a>Bruke LinkedIn Recruiter-funksjoner

Når LinkedIn Recruiter-funksjonene er aktivert av Attract-administratoren, er de tilgjengelige for ansettelsesansvarlige og rekrutterere. Hvis du vil bruke disse funksjonene, kan du koble til LinkedIn-kontoen under **Brukerinnstillinger**. Flere funksjoner vil være tilgjengelige når både adminator- og brukerinnstillinger er tilkoblet.

### <a name="in-ats-profile-widget"></a>In-ATS Profile-kontrollprogram

Du kan vise den kandidatens LinkedIn-profil i Attract. LinkedIn-kontrollprogrammet viser kandidatprofilen når ATS-informasjonen samsvarer med LinkedIn-informasjonen til brukerne.

Hvis du vil vise en profil, går du til kandidatprofilen fra et jobb- eller talentutvalg. I kandidatprofilen velger du den **LinkedIn**-kategorien, og profil-kontrollprogrammet lastes inn. Du kan også lagre kandidaten i LinkedIn Recruiter-prosjektene fra denne siden.
1. Hvis LinkedIn fant treff basert på e-post og LinkedIn-medlems-ID (nøyaktig samsvar), vises kandidatens profil. Brukeren har fortsatt et valg for å koble til / koble fra profilen.

2. Hvis LinkedIn ikke finner kandidaten basert på e-posten eller medlems-ID-en, vises en liste over potensielle kandidattreff basert på kandidatens navn, og brukeren kan velge ett av dem og koble til profilen.  

3. Hvis LinkedIn ikke finner en kandidat basert på navnet, returneres det at ingen treff ble funnet.

### <a name="1-click-export"></a>1-klikk-eksport 

Under utvelgelsen av kandidater i LinkedIn, kan du eksportere kandidaten til jobbene som du har åpne, med ett klikk. Bruk følgende fremgangsmåte for å utføre eksport med ett klikk. Før du fullfører denne fremgangsmåten, kontrollerer du at du er en tilordnet rollen som ansettelsesansvarlig eller rekrutterer for jobben, og at jobben har et **Kundeemne**-stadium.

1.  Opprett jobben, tilordne de riktige rollene og aktiverer jobben.

2.  Når jobben er aktivert, kan du gå til LinkedIn Recruiter.

3.  Finn kandidaten du leter etter, og gå til den aktuelle profilen.

4.  Bruk jobbsøk-boksen i kontaktkortet til å finne jobben ved hjelp av tittelen eller jobb-IDen som ble aktivert i Attract. Hvis du ikke finner jobben, klikker du **Endre ATS** for å finne den riktige Attract-forekomsten.

5. Når jobben er merket, klikker du **Eksporter**. Kandidaten hentes nå av Attract.

6.  Gå til Attract og åpne den aktuelle jobben. Du finner kandidaten du nettopp eksporterte, i **Kundeemne**-stadiet for jobben.

### <a name="in-ats-indicator"></a>In-ATS-indikator 

Ved hjelp av LinkedIn-rekrutterer kan du kontrollere om en kandidat har søkt på andre jobber i organisasjonen, se hvor de er i forskjellige faser av jobbsøknader og vise tilbakemeldinger og kommentarer fra Attract i LinkedIn Recruiter.

1.  Åpne LinkedIn Recruiter, og finn kandidatprofilen du leter etter.

2.  Bla ned for å se **In-ATS**-delen på kandidatens profil.

3.  Du kan bruke dette kontrollprogrammet til å vise all informasjon om kandidaten som finnes i Attract fra LinkedIn Recruiter-visningen.

4.  Velg **Jobber og statuser**-kategorien for å vise jobbene de er en del av, den siste statusen og hvordan de har flyttet mot hver jobb.

5.  Velg **Intervjutilbakemelding**-kategorien for å se tilbakemeldinger som intervjuerne har sendt i Attract.

6.  Velg **Merknader**-kategorien for å vise merknader som er registrert for denne søkeren i Attract.

> [!NOTE]
> Kandidat- og søknadsdata blir ikke synkronisert til LinkedIn Recruiter hvis kandidaten ikke er forbi jobbkandidatfasen.

### <a name="inmail-history"></a>InMail-historikk

LinkedIn InMail-loggen er tilgjengelig med tilgang på kontraktnivå med LinkedIn Recruiter. Når den er aktivert, kan du vise hele InMail-loggen for kandidaten. Du kan også se hvem andre fra organisasjonen som har utvekslet InMail med kandidaten, men du ikke kan vise meldinger mellom dem.

Hvis du vil vise InMail-loggen, går du til en kandidats profil, går til **LinkedIn**-kategorien og blar til bunnen av siden for å vise loggen. Du kan vise InMail-historikken hvis du har hatt en diskusjon med kandidaten. Meldinger fra InMail synkroniseres med Attract annenhver time.

### <a name="notes-history"></a>Notatlogg 

LinkedIn-notatloggen er tilgjengelig med tilgang på kontraktnivå med LinkedIn Recruiter. Når den er aktivert, kan du vise merknadene som er registrert om kandidaten som av ulike rekrutterere fra organisasjonen.

Hvis du vil vise notatloggen, går du til en kandidats profil, går til **LinkedIn**-kategorien og blar til bunnen av siden for å vise loggen. Du kan vise alle merknadene om kandidaten fra LinkedIn Recruiter.

### <a name="inmail-stub-profile"></a>InMail-stub-profil

InMail-stub-profilen er tilgjengelig med tilgang på kontraktnivå med LinkedIn Recruiter. Hvis kandidater er enige om å dele sine LinkedIn-profiler med alle brukere i organisasjonen, kan du spore kandidater i Attract, så opprettes en ny kandidatpost for hver kandidat. Du kan vise kandidatens e-postadresse hvis kandidaten allerede finnes i systemet med en e-postadresse, eller har valgt å dele e-postadressen med rekruttereren.

Hvis du vil vise listen over kandidater, kan du gå til **Talentutvalg** for å se et systemopprettet LinkedIn-talentutvalg. Dette talentutvalget inneholder listen over kandidater og stub-profiler som mottatt fra LinkedIn, og viser kandidatens fornavn og etternavn. Kandidatens e-post-ID vises hvis kandidaten har valgt å dele e-postadressen.
