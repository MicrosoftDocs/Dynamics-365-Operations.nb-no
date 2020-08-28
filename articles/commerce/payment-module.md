---
title: Betalingsmodul
description: Dette emnet dekker betalingsmodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: f4f6baa3c4a42a2994cab772c98d373996e2648b
ms.sourcegitcommit: ae0843763a8b6b232bb71db326fab28605ac6c53
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2020
ms.locfileid: "3661219"
---
# <a name="payment-module"></a>Betalingsmodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet dekker betalingsmodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Betalingsmodulen lar kunder betale for ordrer ved å bruke et kredittkort eller et debetkort. Betalingsintegrasjon for denne modulen leveres av Dynamics 365-betalingskoblingen for Adyen. Hvis du vil ha mer informasjon om hvordan du setter opp og konfigurerer betalingskoblingen, kan du se [Adyen-betalingskobling i Dynamics 365](dev-itpro/adyen-connector.md).

Betalingsmodulen er vert for betalingsinformasjonen som leveres via Adyen i en HTML-innebygd ramme (iframe). Betalingsmodulen fungerer sammen med Commerce Scale Unit for å hente Adyen-betalingsinformasjonen. Som en del av samhandlingen med Commerce Scale Unit kan betalingsmodulen tillate at informasjon om faktureringsadresse blir behandlet enten i iFrame eller som en separat modul. I Fabrikam-temaet vises faktureringsadressen i en egen modul. Denne fremgangsmåten gjør at du får mer fleksibilitet i formateringen, fordi adresselinjene kan gjengis slik at de ligner på linjene i leveringsadressen.

Betalingsmodulen lar også de påloggede kundene lagre betalingsinformasjonen. Betalingsinformasjonen og faktureringsadressen lagres og administreres via Adyen-betalingskoblingen.

Betalingsmodulen dekker eventuelle ordretillegg som ikke allerede dekkes av fordelspoeng eller et gavekort. Hvis totalen for en ordre er dekket av fordelspoeng eller gavekortkreditt, vil betalingsmodulen være skjult, og kunden kan plassere ordren uten den.

Adyen-betalingskoblingen støtter også sterk kundegodkjenning (SCA). En del av PSD-direktiv 2.0 (Payment Services Directive) i EU krever at netthandlere godkjennes utenfor den elektroniske handleopplevelsen når de bruker en elektronisk betalingsmetode. Under betalingsflyten blir kunder omadressert til banknettstedet. Etter godkjenning omadresseres de deretter tilbake til Commerce-betalingsflyten. Under denne omadresseringen vil informasjonen som en kunde har angitt i betalingsflyten (for eksempel leveringsadresse, leveringsalternativer, informasjon om gavekort og fordelsinformasjon), beholdes. Før du kan aktivere denne funksjonen, må betalingskoblingen være konfigurert for SCA i Commerce Headquarters. Hvis du vil ha mer informasjon, kan du se [Sterk kundegodkjenning ved hjelp av Adyen](adyen_redirect.md).

Følgende illustrasjon viser et eksempel på en gavekort-, fordels- og betalingsmodul på en kasseside.

![Eksempel på en gavekort-, fordels- og betalingsmodul på en kasseside](./media/ecommerce-payments.PNG)

## <a name="payment-module-properties"></a>Egenskaper for betalingsmodul

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Overskrift | Overskriftstekst | En valgfri overskrift for betalingsmodulen. |
| Høyden på iFrame | Piksler | IFrame-høyden, i piksler. Høyden kan imidlertid justeres etter behov. |
| Vis faktureringsadresse | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann**, vil faktureringsadressen bli betjent av Adyen inne i betalingsmodulen iFrame. Hvis den er satt til **Usann**, blir faktureringsadressen ikke betjent av Adyen, og en Commerce-bruker må konfigurere en modul til å vise faktureringsadressen på betalingssiden. |
| Overstyring av betalingsstil | CSS-kode (gjennomgripende stilark) | Fordi betalingsmodulen ligger i en iFrame, er det begrenset stilfunksjonalitet. Du kan oppnå en viss stil ved hjelp av denne egenskapen. Hvis du vil overstyre områdestiler, må du lime inn CSS-koden som verdien for denne egenskapen. Områdebygger for CSS overstyrer dette, og stiler gjelder ikke for denne modulen. |

## <a name="billing-address"></a>Faktureringsadresse

I betalingsmodulen kan kundene oppgi en faktureringsadresse for betalingsinformasjonen. I tillegg kan de bruke leveringsadressen som faktureringsadresse, slik at betalingsflyten blir enklere og raskere. Hvis egenskapen **Vis faktureringsadresse** er satt til **Usann**, må betalingsmodulen konfigureres på betalingssiden.

## <a name="add-a-payment-module-to-a-checkout-page-and-set-the-required-properties"></a>Legge til en betalingsmodul på en kasseside og angi de nødvendige egenskapene

En betalingsmodul kan bare legges til i en kassemodul. Hvis du vil ha mer informasjon om hvordan du konfigurerer en betalingsmodul for en kasseside, se [Kassemodul](add-checkout-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Handlekurvmodul](add-cart-module.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Kassemodul](add-checkout-module.md)

[Leveringsadressemodul](ship-address-module.md)

[Modul for leveringsalternativer](delivery-options-module.md)

[Ordredetaljermodul](order-confirmation-module.md)

[Gavekortmodul](add-giftcard.md)

[Dynamics 365 Payment Connector for Adyen](dev-itpro/adyen-connector.md)

[Sterk kundegodkjenning ved hjelp av Adyen](adyen_redirect.md)
