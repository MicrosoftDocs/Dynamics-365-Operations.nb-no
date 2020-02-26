---
title: Handlekurvmodul
description: Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 01/23/2020
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
ms.openlocfilehash: f6dd8fb56f7342eb9c877eda503a92f4a31e5863
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3025442"
---
# <a name="cart-module"></a>Handlekurvmodul


[!include [banner](includes/banner.md)]

Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En handlekurvmodul brukes til å vise varene som er lagt til i handlekurven før kunden går videre til kassen. Det inkluderer for eksempel alle varene som er lagt til i handlekurven og et ordresammendrag. Den lar også kunden bruke eller fjerne kampanjekoder.

Handlekurvmodulen støtter pålogget utsjekking og Sjekk ut som gjest. Den støtter også koblingen **Tilbake til shopping**. Du kan konfigurere ruten for denne koblingen under **Områdeinnstillinger \> Utvidelser \> Ruter**.

Handlekurvmodul gjengir data basert på handlekurv-IDen. Handlekurv-IDen er en informasjonskapsel i leseren som er tilgjengelig på hele området.

## <a name="cart-module-properties-and-slots"></a>Egenskaper og spor for handlekurvmodul

Handlekurvmodulen har egenskapen **Overskrift** som kan settes til verdier som **Handlepose** og **Varer i handlekurven**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduler som kan brukes i handlekurvmodulen

- **Tekstblokk** – Denne modulen støtter tilpassede meldinger i handlekurvmodulen. Meldingene drives av innholdsbehandlingssystemet (CMS). Alle meldinger kan legges til, for eksempel "For problemer med ordren, kontakt 1-800-Fabrikam."
- **Butikkvelger** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting. Den lar brukere angi en plassering for å finne butikker i nærheten. Butikkvelgermodulen er integrert med API-en (programmeringsgrensesnittet) for Bing-kart-geoplasseringsprogrammet for å konvertere lokasjonen til en breddegrad og lengdegrad. En API-nøkkel for Bing-kart kreves, og den må legges til på siden Delte parametere for detaljhandel i Dynamics 365 Retail. Denne modulen støtter to egenskaper, **Søkeradius** og **Vilkår for bruk-kobling**. Egenskapen **Søkeradius** definerer søkeradiusen for butikker i engelske mil. Hvis ingen verdi er angitt, brukes standard søkeradius, 50 engelske mil. Hvis Bing-kart eller en ekstern tjeneste brukes, kan egenskapen **Vilkår for bruk-kobling** brukes til å angi en kobling til vilkårene for bruk. Det kreves en vilkår for bruk-kobling for Bing-kart-tjenesten. 

## <a name="cart-module-settings"></a>Handlekurvmodulinnstillinger

Handlekurvmoduler har følgende innstillinger som kan konfigureres under **Områdeinnstillinger \> Utvidelser**:

- **Maksimalt antall** – Denne egenskapen brukes til å angi maksimalt antall for hver vare som kan legges til i handlekurven. En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.
- **Lagerbeholdning** – Når verdien er satt til **Sann**, legges det til en vare i handlekurven bare etter kjøpsboksmodulen kontrollerer at den er på lager. Denne lagerkontrollen utføres både for scenarier der varen skal leveres, og for scenarier der den skal plukkes opp i butikken. Hvis verdien settes til **Usann**, utføres det ingen lagerkontroll før en vare legges til i handlekurven, og ordren plasseres.
- **Lagerbuffer** – Denne egenskapen brukes til å angi et bufferantall for lageret. Lageret vedlikeholdes i sanntid, og når mange kunder bestiller, kan det være vanskelig å opprettholde et nøyaktig lagerantall. Når det utføres en lagerkontroll, og hvis lageret er mindre enn buffermengden, blir produktet behandlet som at det ikke finnes på lager. Derfor, når salget skjer raskt i flere kanaler og lageropptellingen ikke er fullstendig synkronisert, er det mindre fare for at en vare som ikke er på lager, blir solgt.
- **Tilbake til shopping** – Denne egenskapen brukes til å angi ruten for **Tilbake til shopping**-koblingen. Denne ruten kan konfigureres på områdenivået. Denne konfigurasjonen gjør at forhandlerne kan ta kunden tilbake til startsiden eller en annen side på området.

## <a name="commerce-scale-unit-interaction"></a>Samhandling med Commerce Scale Unit

Handlekurvmodulen henter produktinformasjon ved hjelp av API-er for Commerce Scale Unit. Handlekurv-IDen fra leserinformasjonskapselen brukes til å hente all produktinformasjon fra Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Legge til en handlekurvmodul på en side

Hvis du vil legge til en handlekurvmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett et fragment kalt **Handlekurvfragment**, og legg til en handlekurvmodul i den.
1. Legg til en overskrift i handlekurvmodulen.
1. Legg til en butikkvelgermodul i handlekurvmodulen.
1. Lagre fragmentet, fullfør redigeringen av det, og publiser det.
1. Opprett en mal som heter **Handlekurvmal**, og legg til handlekurvfragmentet som du nettopp opprettet, i det.
1. Lagre malen, fullfør redigeringen av den, og publiser den.
1. Opprett en side som bruker den nye malen.
1. Lagre og forhåndsvis siden.
1. Fullfør redigeringen av siden, og publiser den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
