---
title: Topptekstmodul
description: Denne artikkelen dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 63c298f36f64f2e107d3df3c0c5f3b6445546aa1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9275792"
---
# <a name="header-module"></a>Topptekstmodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker topptekstmoduler og beskriver hvordan du oppretter sideoverskrifter i Microsoft Dynamics 365 Commerce.

I Dynamics 365 Commerce vises et topptekstområde som et sidefragment som inkluderer topptekst, promobanner og samtykkingsmoduler for informasjonskapsler. 

Topptekstmodulen inneholder en områdelogo, koblinger til navigasjonshierarkiet, koblinger til andre sider på området, en handlekurvikonmodul, et ønskelistesymbol, påloggingsalternativer og søkefelt. En topptekstmodul optimaliseres automatisk for enheten som området vises på (altså for en skrivebordsenhet eller mobilenhet). På en mobilenhet er for eksempel navigasjonsfeltet skjult i en **Meny**-knapp (som også kalles en *hamburgermeny*).

Bildet nedenfor viser et eksempel på en topptekstmodul på en hjemmeside.

![Eksempel på en topptekstmodul.](./media/ecommerce-header.png)

## <a name="properties-of-a-header-module"></a>Egenskaper for en topptekstmodul

En topptekstmodul støtter **Logobilde**, **Logokobling** og egenskaper for **Min konto-koblinger**. 

**Logobilde**- og **Logokobling**-egenskapene brukes til å definere en logo på siden. Hvis du vil ha mer informasjon, kan du se [Legge til en logo](add-logo.md). 

Egenskapen **Min konto-koblinger** kan brukes til å definere kontosider som områdeeieren ønsker å vise hurtigkoblinger for i toppteksten.

## <a name="modules-that-are-available-within-a-header-module"></a>Moduler som er tilgjengelige i en overskriftsmodul

Følgende moduler kan brukes i en topptekstmodul:

- **Navigasjonsmeny** – Navigasjonsmenyen representerer kanalnavigasjonshierarkiet og andre statiske navigasjonskoblinger. Hvis du vil ha mer informasjon, kan du se [Navigasjonsmenymodul](nav-menu-module.md).

- **Søk** – Med søkemodulen kan brukere angi søkeord for å søke etter produkter. URL-adressen til standard søkeside og parameterne for søkespørringen må angis under **Områdeinnstillinger \> Utvidelser**. Søkemodulen har egenskaper som lar deg skjule søkeknappen eller etiketten etter behov. Søkemodulen støtter også alternativer for automatiske forslag, for eksempel søkeresultater for produkt, nøkkelord og kategori.

- **Handlekurvikon** – Handlekurvikonmodulen representerer handlekurvikonet, som viser antall varer i handlekurven på et gitt tidspunkt. Hvis du vil ha mer informasjon, se [Handlekurvikonmodulen](cart-icon-module.md).

- **Områdevelger** - Områdevelgermodulen lar brukere bla gjennom forskjellige forhåndsdefinerte områder, basert på marked, regioner og nasjonale innstillinger. Hvis du vil ha mer informasjon, se [Områdevelgermodul](site-selector.md).

- **Butikkvelger** - Butikkvelgermodulen kan tas med i en hodemoduls butikkvelgerspor. Det gjør det mulig for brukere å søke etter og finne nærliggende butikker. Brukere kan også angi en foretrukket butikk. Denne butikken vil deretter bli vist i hodet. Når butikkvelgermodulen er inkludert i hodemodulen, må **Modus**-egenskapen angis til **Søk etter butikker**. Hvis du vil ha mer informasjon, se [Butikkvelgermodul](store-selector.md).

> [!NOTE]
> - Støtte for bruk av handlekurvikon-modulen i hodemoduler er tilgjengelig fra Dynamics 365 Commerce 10.0.11-versjonen.
> - Støtte for bruk av områdevelger-modulen i hodemoduler er tilgjengelig fra Dynamics 365 Commerce 10.0.14-versjonen.
> - Støtte for bruk av butikkvelger-modulen i hodemoduler er tilgjengelig fra Dynamics 365 Commerce 10.0.15-versjonen.

## <a name="header-module-in-the-adventure-works-theme"></a>Hodemodulen i Adventure Works-emnet

I Adventure Works-emnet støtter hodemodulen **Mobillogo**-egenskapen. Ved hjelp av denne egenskapen kan det angis en logo for mobilvisningsrapporter. **Mobillogo**-egenskapen er tilgjengelig som moduldefinisjonsnummer.

> [!IMPORTANT]
> Adventure Works-temaet er tilgjengelig fra Dynamics 365 Commerce-10.0.20-versjonen.

## <a name="create-a-header-fragment-for-a-page"></a>Opprette et topptekstfragment for en side

Hvis du vil opprette et topptekstfragment, følger du trinnene nedenfor.

1. Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.
1. I dialogboksen **Velg et fragment** velger du **Beholder**-modulen, skriver inn et navn på fragmentet og velger **OK**.
1. Velg **Standardbeholder**-sporet. Deretter går du til egenskapsfanen på høyre side og angir egenskapen for **Bredde** til **Fyll skjerm**.
1. I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du modulene **Samtykke til informasjonskapsler**, **Topptekst** og **Promobanner**, og deretter velger du **OK**.
1. I ruten Egenskaper i modulen **Promobanner** velge rdu **Legg til melding**, og deretter velger du **Melding**.
1. I dialogboksen **Melding** legger du til tekst og koblinger for kampanjeinnholdet, og deretter velger du **OK**.
1. I ruten Egenskaper i modulen **Samtykke til informasjonskapsler** legger du til og konfigurerer tekst og en kobling til siden med nettstedspersonvern.
1. I **Navigasjonsmeny**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Navigasjonsmeny**-modulen, og deretter velger du **OK**.
1. I ruten Egenskape rfor navigasjonsmenymodulen velger du **Retail Server** under **Kilde til navigasjonsmeny**.
1. I ruten Egenskaper for navigasjonsmenymodulen velger du **Legg til menyelement** under **Statiske menyelementer**, og deretter velger du **Menyelement**. 
1. I dialogboksen **Menyelement** skriver du inn "Kontakt" under **Menyelementtekst**.
1. I dialogboksen **Menyelement** velger du **Legg til en kobling** under **Koblingsmål for menyelement**.
1. I dialogboksen **Legg til en kobling** velger du URL-adressen for nettstedets Kontakt-side, og deretter velger du **OK**.  
1. Velg **OK** i dialogboksen **Menyelement**.
1. I **Søk**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Søk**-modulen, og deretter velger du **OK**.
1. Konfigurer egenskapene for søkemodulen i egenskapsruten etter behov.
1. I **Handlevogn**-sporet i topptekstmodulen velger du ellipseknappen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Handlekurvikon**-modulen, og deretter velger du **OK**.
1. Konfigurer egenskapene for handlevognikon-modulen i egenskapsruten etter behov. Hvis du vil at handlekurvikonet skal vise et sammendrag av handlekurven (også kjent som en minikurv) når brukerne holder pekeren over den, velger du **Vis minikurv**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere det.

For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.

1. I **Topptekst**-sporet på **Standardside**-modulen legger du til bunntekstfragmentet du opprettet.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Beholdermodul](add-container-module.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Promobannermodul](add-alert.md)

[Navigasjonsmenymodul](nav-menu-module.md) 

[Informasjonskapselsamtykke](cookie-consent-module.md)

[Bunntekstmodul](author-footer-module.md)

[Områdevelgermodul](site-selector.md)

[Butikkvelgermodul](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
