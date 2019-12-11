---
title: Handlekurvmodul
description: Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1c910f08e5999ec586b5cb656d5769e9d4abd069
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696767"
---
# <a name="cart-module"></a>Handlekurvmodul

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En handlekurvmodul er container som brukes til å være vert for alle modulene som kreves for å vise varer som er i handlekurven. Det inkluderer for eksempel alle varene som er lagt til i handlekurven, ordresammendrag og kampanjekoder.

Handlekurvmodul gjengir data basert på handlekurv-IDen. Handlekurv-IDen er en informasjonskapsel i leseren som er tilgjengelig på hele området.

## <a name="cart-module-properties-and-slots"></a>Egenskaper og spor for handlekurvmodul

Som en container styrer en handlekurvmodul enkelte grunnleggende egenskaper, for eksempel overskriften og bredden. Overskriften er vanligvis tekst, for eksempel **Handlepose**, **Handlekurv** eller **varer i handlekurven**. Breddeinnstillingen bestemmer om modulene i beholderen må passe i denne beholderen, eller om de kan fylle skjermen.

Handlekurvsiden er delt inn i flere områder: handlekurvlinjeelementer, ordresammendrag og kasse og "finn i butikk"-funksjonalitet. Hver region er tilordnet et spor i handlevognmodulen, og hvert spor godtar et forhånds definert sett med moduler.

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduler som kan brukes i handlekurvmodulen

- **Linjeelementer for handlekurv** – Denne modulen viser et sammendrag av hver vare som er lagt til i handlekurven. Informasjonen omfatter produkttittelen, valgte dimensjoner, pris, antall og rabatter. Denne modulen støtter også handlinger som "fjern fra kurv" og "legg til i ønskeliste". For hver linjevare finnes det et alternativ for å levere varen eller plukke den opp fra butikken. Dette alternativet må konfigureres separat i plukkingen i butikkmodulen.
- **Ordresammendrag** – Denne modulen viser et ordresammendrag. Informasjonen omfatter delsum, forsendelse, avgifter og sparing. En overskrift kan konfigureres for denne modulen.
- **Promokode** – Denne modulen lar kundene løse inn kampanjekoder. En kampanjekode kan brukes eller fjernes.
- **Kasse** – Denne modulen starter utsjekkingshandlingen og omdirigerer brukeren til utsjekkingssiden. Tre koblinger må konfigureres for denne modulen:

    - **Kasse** – Denne koblingen tvinger kunder til å logge seg på hvis de ikke allerede er logget på.
    - **Sjekk ut som gjest** – Med denne koblingen kan anonyme kunder legge inn ordrer. Den vises bare når kunder ikke er logget på.
    - **Tilbake til shopping** – Med denne koblingen kan kunder til å gå til startsiden og en annen side, slik at de kan fortsette å handle.

- **Innholdsrik blokk** – Denne modulen støtter tilpassede meldinger i handlekurvmodulen. Meldingene drives av innholdsbehandlingssystemet (CMS). Alle meldinger kan legges til, for eksempel "For problemer med en ordre, kontakt 1-800-Fabrikam".
- **Hent i butikk** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting. Som standard viser denne modulen butikker som er innen en 50 kilometers radius til kundenslokasjonen. Radiusen for søk kan imidlertid tilpasses i modulen. For hver butikk utføres det en lagerkontroll, hvis lagerkontrollfunksjonaliteten er aktivert, og det vises en gjeldende på lager- eller tomt-melding.
- **Butikksøk etter Bing-kart** – Denne modulen kan brukes i hente i butikk-modulen. Den lar kunder søke etter butikker ved å angi en lokasjon. APIen (programmeringsgrensesnittet) for Bing-kart-geoplasseringsprogrammet brukes til å konvertere lokasjonen som kunden anga, til en breddegrad og en lengdegrad. Hvis denne modulen ikke brukes, vises bare butikker som er nær kundens gjeldende lokasjon, og kunden kan ikke søke etter en annen lokasjon.

## <a name="cart-module-settings"></a>Handlekurvmodulinnstillinger

Handlevognmoduler har tre innstillinger som kan konfigureres:

- **Maksimalt antall** – Maksimalt antall for hver vare som kan legges til i handlekurven. En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.
- **Lagerbeholdning** – Når verdien er satt til **Sann**, legges det til en vare i handlekurven bare etter kjøpsboksmodulen kontrollerer at den er på lager. Denne lagerkontrollen utføres både for scenarier der varen skal leveres, og for scenarier der den skal plukkes opp i butikken. Hvis verdien settes til **Usann**, utføres det ingen lagerkontroll før en vare legges til i handlekurven, og ordren plasseres.
- **Lagerbuffer** – Lageret vedlikeholdes i sanntid, og når mange kunder bestiller, kan det være vanskelig å opprettholde et nøyaktig lagerantall. Derfor kan en buffer defineres for lager. Når det utføres en lagerkontroll, og hvis lageret er mindre enn buffermengden, blir produktet behandlet som at det ikke finnes på lager. Derfor, når salget skjer raskt i flere kanaler, slik at lageropptellingen ikke er fullstendig synkronisert, er det mindre fare for at en vare som ikke er på lager, blir solgt.

## <a name="retail-server-interaction"></a>Interaksjon med detaljhandelsserver

Handlekurvmodulen henter produktinformasjon ved hjelp av API-er for Retail Server. Handlekurv-IDen fra lesereninformasjonskapselen brukes til å hente all produktinformasjon fra Retail server.

## <a name="add-a-cart-module-to-a-page"></a>Legge til en handlekurvmodul på en side

Hvis du vil legge til en handlekurvmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett et fragment kalt **handlekurvfragment**, og legg til en handlekurvmodul i den.
1. I **Linjeelementer for handlekurv**-sporet i handlekurvmodulen legger du til handlekurvmodulen.
1. I **Ordresammendrag**-sporet legger du til en ordresammendragsmodul.
1. Legg til en promokodemodul i **Promokode**-sporet.
1. Legg til en kassemodul i **Kasse**-modulen.
1. I **Finn i butikk**-sporet legger du til en plukking i butikkmodul.
1. I hent i butikk-modulen velger du **Butikksøk**-sporet og legger til et butikksøk etter Bing-kart-modulen.
1. Sjekk inn fragmentet, og publiser det.
1. Opprett en mal som heter **handlekurvmal**, og legg til handlekurvfragmentet som du nettopp opprettet, i det.
1. Lagre malen, sjekk den inn og publiser den.
1. Opprett en side som bruker den nye malen.
1. Lagre og forhåndsvis siden.
1. Sjekk inn siden, og publiser den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
