---
title: Konfigurere flere B2C-leiere i et Commerce-miljø
description: Dette emnet beskriver når og hvordan du definerer flere per kanals Microsoft Azure Active Directory (Azure AD) B2C-leiere for brukergodkjenning i et dedikert Dynamics 365 Commerce-miljø.
author: BrianShook
manager: annbe
ms.date: 03/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: 2ddc8cea42ab0b5a319d4725ce8c75e57529cc63
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477762"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a>Konfigurere flere B2C-leiere i et Commerce-miljø

[!include [banner](includes/banner.md)]

Dette emnet beskriver når og hvordan du definerer flere per kanals Microsoft Azure Active Directory (Azure AD) B2C-leiere for brukergodkjenning i et dedikert Dynamics 365 Commerce-miljø.

Dynamics 365 Commerce bruker identitetstjenesten Azure AD B2C til å støtte brukerlegitimasjon og godkjenningsflyt. Brukere kan bruke godkjenningsflyt til å registrere seg, logge inn og tilbakestille passordet. Azure AD B2C lagrer sensitiv brukergodkjenningsinformasjon, for eksempel brukernavn og passord. Brukerposten er unik for hver B2C-leier og bruker enten brukernavn (e-postadresse) eller legitimasjon for sosial identitetsleverandør.

I de fleste tilfeller brukes en enkelt Azure AD B2C-leier i et Commerce-miljø. Commerce-kunder kan deretter opprette og publisere flere områder i samme Commerce-miljø, og samme kundelegitimasjon vil bli brukt på tvers av disse områdene. Hvis imidlertid områdene i miljøet skal behandles som ulike merker og vises for brukere som separate firmaer, kan en B2C-leier konfigureres for kanalen som brukes for området/merke-skillet.

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a>Betraktninger når flere B2C-leiere settes opp per kanal

Når hver kanal eller hvert område behandles som et separat firma, er det ofte best å bruke egne juridiske enheter med hensyn til brukergodkjenningsflyter i Commerce. Hvis du imidlertid vil beholde hver kanal/hvert område i samme miljø og juridisk enhet, men vil ha separate brukergodkjenninger for hvert område, er det viktig at du vurderer følgende punkter før du fortsetter:

- Brukerne vil ha egne legitimasjonsbeskrivelser for hver kanal/hvert område.

    Samme person kan ha to separate kontoer per kanal/område, fordi hver konto vil være en unik oppføring i en separat B2C-leier.

- I Microsoft Dynamics-miljøet returneres separate kundeoppføringer for søk etter globale poster.

    Hvis en bruker bruker samme e-postadresse på tvers av kanaler/områder, returnerer det globale kundesøket resultater for hver kanal/hvert område. (Det vises en kanalindikator.)

- Adresseboken kan brukes til å gruppere brukere, slik at de kan spores per kanal.
- Antallet kundeposter per kanal kan øke, og denne økningen kan påvirke ytelsen til globale kundesøk.
- B2C-leiere må nøye tilordnes til en kanal for å hindre situasjoner der kunder registrerer seg for å finne en feil leier. Ellers kan forvirring eller sporingsproblemer oppstå.

Følgende illustrasjon viser flere B2C-leiere i et Commerce-miljø.

![Flere B2C-leiere i et Commerce-miljø](media/MultiB2C_In_Environment.png)

Hvis du finner ut at bedriften krever forskjellige B2C-leiere per kanal i samme Commerce-miljø, må du utføre fremgangsmåtene i de følgende delene for å be om denne funksjonen.

## <a name="request-that-b2c-per-channel-be-enabled-in-your-environment"></a>Be om at B2C per kanal aktiveres i miljøet ditt

Hvis du vil at forskjellige B2C-leiere per kanal skal være tilgjengelige i det samme Commerce-miljøet, må du sende en forespørsel til Dynamics 365 Commerce. Hvis du vil ha mer informasjon, se [Få kundestøtte for Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md), eller diskuter dette problemet med Commerce-løsningskontakten.

## <a name="configure-b2c-tenants-in-your-environment"></a>Konfigurere B2C-leiere i ditt miljø

Hvis du vil konfigurere B2C-leiere i miljøet ditt, fullfører du de relevante fremgangsmåtene i denne delen.

### <a name="add-an-azure-ad-b2c-tenant"></a>Legge til en Azure AD B2C-leier

Følg denne fremgangsmåten for å legge til en Azure AD B2C-leier i miljøet.

1. Logg inn på Commerce-områdebyggeren for ditt miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-leietakere, må du være systemadministrator for Commerce-miljøet.
1. Velg **Leierinnstillinger** i navigasjonsruten til venstre for å utvide den.
1. Velg **B2C-innstillinger**, og velg deretter **Behandle**.
1. Velg **Legg til B2C-program**, og angi deretter følgende informasjon:

    - **Programnavn**: Angi navnet som skal brukes for programmet i konteksten for administrasjon av det i Commerce. Vi anbefaler at du bruker programnavnet du valgte da du konfigurerte Azure AD B2C-programmet i Azure-portalen. På denne måten kan du bidra til å redusere forvirring når du administrerer B2C-leiere i Commerce.
    - **Navn på leietaker**: Angi navnet på B2C-leieren slik det vises i Azure-portalen.
    - **Policy-ID for glemt passord**: Angi policy-IDen (navnet på policyen i Azure-portalen).
    - **Policy-ID for registrering/pålogging**: Angi policy-IDen (navnet på policyen i Azure-portalen).
    - **Klient-GUID**: Angi Azure AD B2C-leier-IDen slik den vises i Azure-portalen (ikke program-IDen for B2C-leieren).
    - **Policy-ID for redigering av profil**: Angi policy-IDen (navnet på policyen i Azure-portalen).

1. Når du er ferdig med å angi denne informasjonen, velger du **OK** for å lagre endringene.

> [!NOTE]
> Du bør la felt som **Omfang**, **Ikke-interaktiv policy-ID**, **Ikke-interaktiv klient-ID**, **Egendefinert domene for pålogging** og **Policy-ID for registrering** stå tomme, med mindre Dynamics 365 Commerce-teamet instruerer deg om å angi dem.
Den nye Azure AD B2C-leieren skal nå vises i listen under **Behandle B2C-programmer**.

### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a>Administrere eller slette en Azure AD B2C-leier

1. Logg inn på Commerce-områdebyggeren for ditt miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-leietakere, må du være systemadministrator for Commerce-miljøet.
1. Velg **Leierinnstillinger** i navigasjonsruten til venstre for å utvide den.
1. Velg **B2C-innstillinger**, og velg deretter **Behandle**.
1. Hvis du vil redigere en B2C-leier, velger du blyantsymbolet ved siden av den. Hvis du vil slette en B2C-leier, velger du papirkurvsymbolet ved siden av.
1. Velg **Lagre**, og velg deretter **Publiser** for å aktivere endringene.

> [!WARNING]
> Når en B2C-leier er konfigurert for et aktivt/publisert område, kan brukere ha registrert seg ved å bruke kontoer som finnes på leieren. Hvis du sletter en konfigurert leier på menyen **Leierinnstillinger \> B2C-leier**, fjerner du tilknytningen av B2C-leieren fra områder som er knyttet til en hvilken som helst kanal i leieren. I dette tilfellet kan det hende at brukerne ikke lenger kan logge på kontoene sine. Vær derfor svært forsiktig når du sletter en konfigurert leier.
>
> Når en konfigurert leier slettes, vil B2C-leieren og -postene fortsatt bli opprettholdt, men Commerce-systemkonfigurasjonen for denne leieren vil bli endret eller fjernet. Brukere som prøver å registrere seg eller logge på området, vil opprette en ny forretningsforbindelsesoppføring i den standard eller nylig tilknyttede B2C-leieren som er konfigurert for kanalen på området.
## <a name="configure-your-channel-with-a-b2c-tenant"></a>Konfigurere kanalen med en B2C-leier

1. Logg inn på Commerce-områdebyggeren for ditt miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-leietakere, må du være systemadministrator for Commerce-miljøet.
1. Velg **Områdeinnstillinger** i navigasjonsruten til venstre for å utvide den.
1. Velg **Kanaler**, og velg deretter kanalen som skal konfigureres.
1. I egenskaper-ruten til høyre i feltet **Velg B2C-program** velger du den konfigurerte Azure AD B2C-leieren som skal brukes for denne kanalen.
1. Velg **Lagre og publiser** på kommandolinjen for å utføre den nye eller oppdaterte konfigurasjonen.

> [!WARNING]
> Hvis du endrer B2C-programmet som er tilordnet til kanalen, fjerner du de gjeldende referansene som er opprettet for alle brukere som allerede har registrert seg i miljøet. I dette tilfellet vil ingen legitimasjoner som er knyttet til det tilordnede B2C-programmet, være tilgjengelig for brukerne. Derfor kan du bare endre en Azure AD B2C-konfigurasjon hvis du konfigurerer kanalen for første gang, og ingen brukere har muligheten til å registrere seg. Hvis ikke kan det hende at brukerne må registrere seg på nytt for å opprette en post i den nye Azure AD B2C-leieren.
## <a name="additional-resources"></a>Tilleggsressurser

[Konfigurere domenenavnet](configure-your-domain-name.md)

[Distribuere en ny e-handelsleier](deploy-ecommerce-site.md)

[Opprette et e-handelsområde](create-ecommerce-site.md)

[Knytte et Dynamics 365 Commerce-nettsted til en nettkanal](associate-site-online-store.md)

[Administrere robots.txt-filer](manage-robots-txt-files.md)

[Laste opp masseomdirigeringer for URL-adresse](upload-bulk-redirects.md)

[Konfigurere en B2C-leier i Commerce](set-up-B2C-tenant.md)

[Definere egendefinerte sider for brukerpålogginger](custom-pages-user-logins.md)

[Legge til støtte for et innholdsleveringsnettverk (CDN)](add-cdn-support.md)

[Aktivere stedsbasert butikkregistrering](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
