---
title: Tilgjengelighetsfunksjoner
description: "Dette emnet beskriver funksjonaliteten som er utviklet for å hjelpe brukere som har ulike funksjonshemminger. Det finnes for eksempel funksjoner for personer som bruker tekniske hjelpefunksjoner for syn som Windows Skjermleser."
author: TLeforMicrosoft
manager: AnnBe
ms.date: 11/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: tlefor
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.3
ms.translationtype: HT
ms.sourcegitcommit: 158caf6c05515069b58121a72df1b7fe16bae236
ms.openlocfilehash: bd71d2dee7ff7984f2088a64e9943b2541c88451
ms.contentlocale: nb-no
ms.lasthandoff: 11/16/2017

---

# <a name="accessibility-features"></a>Tilgjengelighetsfunksjoner

Dette emnet beskriver funksjonaliteten som er utviklet for å hjelpe brukere som har ulike funksjonshemminger. Det finnes for eksempel funksjoner for personer som bruker tekniske hjelpefunksjoner for syn som Microsoft Windows Skjermleser.

## <a name="windows-narrator-and-keyboard-only-access"></a>Windows Skjermleser og bare tastaturtilgang

Alle felt og kontroller har en etikett og en beskrivelse av gjeldende snarveier. Skjermlesere kan lese etiketten og beskrivelsen.

## <a name="shortcuts-for-the-most-frequently-performed-actions"></a>Snarveier for de vanligste handlingene

For de fleste brukere innebærer systembruk mye dataregistrering og tastaturbruk hver eneste dag. For å forbedre brukeropplevelsen har vi opprettet snarveier som hjelper deg med å «hoppe» rundt på skjermen og snarveier for spesielle handlinger. Hvis du vil ha mer informasjon, kan du se [Hurtigtaster](shortcut-keys.md).

## <a name="navigation-search"></a>Navigasjonssøk

En side som blir åpnet ved hjelp av Navigasjonsrute-menyen, ruten lengst til venstre, er også tilgjengelig fra **Søk**-boksen. Trykk på Alt+G for å flytte fokus til **Søk**-boksen, og skriv deretter inn navnet på eller beskrivelsen av siden.

!["Bankkonto" angitt i Søk-boksen](media/6d08b0be32808221023e2aa92d69fd70.png)

Hvis du vil ha mer informasjon, kan du se [Navigasjonssøk](navigation-search.md).

> [!NOTE]
> Du kan navigere direkte bare til toppnivåsider. Sekundære sider er avhengige av informasjon eller kontekst fra den overordnede siden.

## <a name="action-search-for-keyboard-only-users-or-for-heads-down-data-entry"></a>Handlingssøk for brukere som bare bruker tastatur eller for direkte dataregistrering

Alle handlinger som angis på en side, er tilgjengelige fra et tastatur via tabulatorsekvensen. Informasjon om tabulatorsekvensen er angitt senere i dette emnet. Hvis du vil kjøre handlinger mer direkte, kan du bruke handlingssøkefunksjonen.

### <a name="example"></a>Eksempel

Du vil kjøre **Logg for e-postvarsling**-handlingen som vises i **E-postvarsling**-gruppen i **Ordre**-kategorien i handlingsruten.

![Handlingen Logg for e-postvarsling i handlingsruten](media/f0d78399e7fafcd85ded1cd1e3d34f3c.jpg)

Ett alternativ er å bruke tastaturet. Trykk på Ctrl+F6 for å flytte fokus til handlingsruten, og trykk deretter Tab gjentatte ganger for å gå gjennom alle kategoriene og handlingene til **Logg for e-postvarsling**-handlingen har fokus.

Du kan imidlertid også kjøre handlingen mer direkte. Trykk på Ctrl+apostrof (') fra hvor som helst på siden for å vise søkeboksen for handlinger.

![Søkebok for handlinger](media/80f7e8c5ac412fdf2c8a12f7728f135a.jpg)

I søkeboksen skriver du inn ord som beskriver handlingen. Handlingen blir gjort tilgjengelig for deg, og du kan kjøre den direkte. Hvis du for eksempel skriver inn **e-post**, **vars** (ett delvis ord) eller **logg**, kan du "hoppe" til funksjonen Logg for e-postvarsling.

!["E-post" angitt i Søk-boksen](media/image4.png) !["Vars" angitt i Søk-boksen](media/image5.png) !["Logg" angitt i Søk-boksen](media/image6.png)

Når du er ferdig, kan du trykke Ctrl+apostrof på nytt for å få fokus tilbake på feltet som du arbeidet med før du kjørte handlingssøket.

Hvis du vil ha mer informasjon, kan du se [Handlingssøk](action-search.md).

## <a name="tab-sequence"></a>Kategorisekvens

I daglig systembruk er ikke alle felt nødvendige for å utføre vanlige oppgaver. Derfor, som standard, er kategorisekvensen optimalisert. Tabulatorstopp er bare angitt på de feltene som er viktige for vanlige scenarier.

Det kan imidlertid være at noen av feltene som du bruker ofte til å utføre oppgaver, ikke er inkludert i standardkategorisekvensen. I dette tilfellet, hvis du bruker Windows Skjermleser, kan du bruke Windows Skjermlesers tastaturhandlinger til å få tilgang til disse feltene og undersøke innholdet deres. Du kan også slå på **Utvidet tabulatorsekvens**-alternativet på **Alternativer**-siden. Dette alternativet gjør alle redigerbare og skrivebeskyttede felt del av kategorisekvensen. Du kan deretter bruke sidetilpassing til å opprette en egendefinert kategorisekvens, og utelate felt som du ikke trenger i kategorisekvensen. Hvis du vil ha mer informasjon om tilpassing, se [Tilpasse brukeropplevelsen](personalize-user-experience.md).

![Utvidet tabulatorsekvens-alternativet](media/8c0f12bbb3f26032997ef0ba95d89b6a.png)

## <a name="form-patterns"></a>Skjemamønstre

Nesten 90 prosent av sidene i produktet er basert på et lite sett med mønstre. Disse mønstrene kalles *skjemamønstre*. Hvert skjemamønster brukes til å gi handlingene som utføres oftest på siden. Et skjemamønster bidrar til å gjøre det mer gjenkjennelig og enklere å forstå, fordi handlinger og data som brukes ofte, alltid vises på samme sted på forskjellige sider. På grunn av det lave antallet skjemamønstre, kan brukere enkelt lære systemet uansett hvor mange sider det inneholder, og kan trygt bruke det etter at de har gjenkjent skjemamønstrene.

Hvis du vil vite mer om skjemamønstre, kan du se [Skjemastiler og -mønstre](../../dev-itpro/user-interface/form-styles-patterns.md).

## <a name="responsive-layout"></a>Responsiv oppsett

Produktet er utformet for å fungere med forskjellige enheter og formfaktorer, fra de minste skjermene til store skjermer som har den høyeste oppløsningen. Vår responsive oppsettsmotor lar brukere zoome inn til et forstørrelsesnivå på 200 prosent (eller i enkelte tilfeller mer enn 200 prosent).

## <a name="guidance-to-help-developers-and-customers-incorporate-accessible-thinking-in-their-customizations"></a>Veiledning for å hjelpe utviklere og kunder å ta med tilgjengelighetshensyn i sine tilpassinger

Hvis du vil vite mer om Microsofts anbefalte fremgangsmåter for hvordan du aktiverer tilgjengelighet, kan du se [Tilgjengelighet i skjemaer, produkter og kontroller](../../dev-itpro/user-interface/enable-accessibility.md).

