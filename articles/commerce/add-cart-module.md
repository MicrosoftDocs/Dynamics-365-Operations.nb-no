---
title: Handlekurvmodul
description: Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 03/19/2020
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
ms.openlocfilehash: 598b35b1bd365e761d8d4c5ef214935e60b971f4
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154023"
---
# <a name="cart-module"></a>Handlekurvmodul

[!include [banner](includes/banner.md)]

Dette emnet dekker handlekurvmoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

En handlekurvmodul viser varene som er lagt til i handlekurven før kunden går videre til kassen. Modulen viser også et ordresammendrag som lar kunden bruke eller fjerne kampanjekoder.

Handlekurvmodulen støtter pålogget utsjekking og Sjekk ut som gjest. Den støtter også koblingen **Tilbake til shopping**. Du kan konfigurere ruten for denne koblingen under **Områdeinnstillinger \> Utvidelser \> Ruter**.

Handlekurvmodulen gjengir data basert på handlekurv-IDen, som er en informasjonskapsel i leseren som er tilgjengelig i hele området.

## <a name="cart-module-properties-and-slots"></a>Egenskaper og spor for handlekurvmodul

Handlekurvmodulen har egenskapen **Overskrift** som kan settes til verdier som **Handlepose** og **Varer i handlekurven**. 

## <a name="modules-that-can-be-used-in-a-cart-module"></a>Moduler som kan brukes i handlekurvmodulen

- **Tekstblokk** – Denne modulen støtter tilpassede meldinger i handlekurvmodulen. Meldingene drives av innholdsbehandlingssystemet (CMS). Alle meldinger kan legges til, for eksempel "For problemer med ordren, kontakt 1-800-Fabrikam."
- **Butikkvelger** – Denne modulen viser en liste over nærliggende butikker der en vare er tilgjengelig for henting. Den lar brukere angi en plassering for å finne butikker i nærheten. Hvis du vil ha mer informasjon om denne modulen, se [Butikkvelgermodul](store-selector.md).

## <a name="cart-module-settings"></a>Handlekurvmodulinnstillinger

Handlekurvmoduler har følgende innstillinger som kan konfigureres under **Områdeinnstillinger \> Utvidelser**:

- **Maksimalt antall** – Denne egenskapen brukes til å angi maksimalt antall for hver vare som kan legges til i handlekurven. En forhandler kan for eksempel bestemme at bare 10 av hvert produkt kan selges i en enkelt transaksjon.
- **Lagerbeholdning** – Når verdien er satt til **Sann**, legges det til en vare i handlekurven bare etter kjøpsboksmodulen kontrollerer at den er på lager. Denne lagerkontrollen utføres for scenarier der varen skal leveres, og for scenarier der den skal plukkes opp i butikken. Hvis verdien settes til **Usann**, utføres det ingen lagerkontroll før en vare legges til i handlekurven, og ordren plasseres.
- **Lagerbuffer** – Denne egenskapen brukes til å angi et bufferantall for lageret. Lageret vedlikeholdes i sanntid, og når mange kunder bestiller, kan det være vanskelig å opprettholde et nøyaktig lagerantall. Når det utføres en lagerkontroll, og hvis lageret er mindre enn buffermengden, blir produktet behandlet som at det ikke finnes på lager. Derfor, når salget skjer raskt i flere kanaler og lageropptellingen ikke er fullstendig synkronisert, er det mindre fare for at en vare som ikke er på lager, blir solgt.
- **Tilbake til shopping** – Denne egenskapen brukes til å angi ruten for **Tilbake til shopping**-koblingen. Ruten kan konfigureres på områdenivå, slik at forhandlere kan bringe kunden tilbake til hjemmesiden eller en hvilken som helst annen side på området.

## <a name="commerce-scale-unit-interaction"></a>Samhandling med Commerce Scale Unit

Handlekurvmodulen henter produktinformasjon ved hjelp av API-er for Commerce Scale Unit. Handlekurv-IDen fra leserinformasjonskapselen brukes til å hente all produktinformasjon fra Commerce Scale Unit.

## <a name="add-a-cart-module-to-a-page"></a>Legge til en handlekurvmodul på en side

Hvis du vil legge til en handlekurvmodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Opprett et fragment kalt **Handlekurvfragment**, og legg til en handlekurvmodul i det nye fragmentet.
1. Legg til en overskrift i handlekurvmodulen.
1. Legg til en butikkvelgermodul i handlekurvmodulen.
1. Lagre fragmentet, fullfør redigeringen, og publiser deretter fragmentet.
1. Opprett en mal som heter **Handlekurvmal**, og legg til handlekurvfragmentet som du nettopp opprettet.
1. Lagre malen, fullfør redigeringen, og publiser deretter malen.
1. Opprett en side som bruker den nye malen.
1. Lagre og forhåndsvis siden.
1. Fullfør redigeringen av siden, og publiser den.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Butikkvelgermodul](store-selector.md)

[Kjøpsboksmodul](add-buy-box.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
