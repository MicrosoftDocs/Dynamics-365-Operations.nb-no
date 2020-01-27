---
title: Topptekstmodul
description: Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: cc98419077f6f563ea2265d4e68ba809971cfbd6
ms.sourcegitcommit: ff93b8f6a11993f2cd00be2da7aa77ef0d950ab8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/03/2019
ms.locfileid: "2885484"
---
# <a name="header-module"></a>Topptekstmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet dekker topptekstmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En topptekstmodul er en spesialcontainer som brukes til å være vert for alle modulene som skal vises i toppteksten på en side. Den kan for eksempel inkludere områdelogoen, koblinger til navigasjonshierarkiet, koblinger til andre sider på området og søkefeltet.

En topptekstmodul optimaliseres automatisk for enheten som området vises på (det vil si en skrivebordsenhet eller mobilenhet). På en mobilenhet er for eksempel navigasjonsfeltet skjult i en **Meny**-knapp (som også kalles en *hamburgermeny*).

## <a name="properties-of-a-header"></a>Egenskaper for en topptekst

I likhet med generiske containere støtter en topptekstmodul egenskapene **topptekst** og **bredde**.

En topptekstmodul har flere spor. Det finnes for eksempel spor for en informasjonsmelding, navigasjonsmeny, logo, søkefelt, handlekurvikon, ønsketlisteikon og kontoinformasjon. Hvert spor støtter et bestemt sett med moduler.

## <a name="modules-that-are-available-in-a-header-module"></a>Moduler som er tilgjengelige i en overskriftsmodul

Følgende moduler kan brukes i en topptekstmodul:

- **Navigasjonsmeny** – Navigasjonsmenyen representerer kanalnavigasjonshierarkiet og andre statiske navigasjonskoblinger. Kanalnavigeringshierarkiet kan konfigureres i Dynamics 365 Retail. Konfigurerte varer vises deretter som topptekstnavigasjon. I tillegg kan statiske navigasjonskoblinger konfigureres, og relative koblinger til andre sider på området for e-handel kan angis. Selve hodet kan justeres fra venstre, høyre eller i midten.
- **Handlekurvikon** – Handlekurvikonet er et spesialikon som representerer handlekurven. Det vises i toppteksten og viser antallet varer i handlekurven. En kobling til handlekurvsiden må følge med handlekurvikonet, slik at kunder kan omadresseres til handlevognsiden når de samhandler med ikonet.
- **Ønskelisteikon** – Ikonet for ønskeliste vises i hodet og viser antallet varer som er lagt til på kundens ønskeliste. En kobling til ønskelistesiden må følge med dette konet, slik at kunder kan omadresseres til handlevognsiden når de samhandler med ikonet.
- **Påloggingsmodul** – Påloggingsmodulen vises i hodet. Den lar kundene enten logge på kontoen eller registrere seg for en konto. Hvis kunden allerede er logget på, kan modulen konfigureres til å vise koblinger til kontosiden, ordreloggsiden eller en annen side.
- **Logomodul** – Denne modulen viser logoen som representerer forhandleren og merket. Det er et bilde som har en kobling. Koblingen er vanligvis konfigurert slik at den har en omadressering til startsiden, og derfor kan kundene raskt gå tilbake til startsiden fra en hvilken som helst side på området.
- **Varsel** – Et varsel vises i toppteksten og brukes til å vise en innebygd melding som gjelder alle sidene på området. Et varsel kan for eksempel vise en melding som "Årets salg avsluttes om 2 dager".
- **Søkefelt** – Med søkefeltet kan brukere angi søkeord, slik at de kan søke etter produkter. Modulen må konfigureres med URL-adressen til søkeresultatsiden. Parameteren for spørringsstrengen kan konfigureres (standardverdien er **"q"**). Søkefeltet har et spor for automatiske forslag der modulen for automatiske forslag skal legges til.
- **Automatisk forslag** – Modulen for automatisk forslag viser resultater for automatiske forslag. Disse resultatene kan være nøkkelord, produkter eller kategorier der søkeordet finnes.

## <a name="create-a-header-module"></a>Opprette en topptekstmodul

Hvis du vil opprette en topptekstmodul, følger du trinnene nedenfor.

1. Opprett et sidefragment som inneholder en topptekstmodul.
1. Legg til moduler i sporene i hodemodulen.
1. Oppdater innstillingene for hver modul.
1. Lagre sidefragmentet. 
1. Sjekk inn siden, og publiser den.

For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.

1. På standardsiden legger du til sidefragmentet som inneholder topptekstmodulen, i toppteksten i hovedsporet.
1. Lagre malen. 
1. Sjekk inn malen, og publiser den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
