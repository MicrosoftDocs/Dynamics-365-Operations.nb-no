---
title: Leveringsadressemodul
description: Denne artikkelen dekker leveringsadressemodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: e30e639b7ba1c0caaf72fa66d13f80d04c2e861c
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882202"
---
# <a name="shipping-address-module"></a>Leveringsadressemodul

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver leveringsadressemodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.

Med leveringsadressemodulen kan kunder legge til eller velge leveringsadressen for en ordre under betalingen. Hvis en kunde er logget på, vises alle adresser som tidligere ble lagret for denne kunden, og kunden kan velge mellom dem. Kunden kan også legge til en ny adresse. Leveringsadressemodulen brukes for alle varer i en ordre som krever levering.

Leveringsadresseformater kan defineres i Commerce Headquarters for hvert land eller område, og leveringsadressemodulen håndhever deretter regler som er spesifikk for land/område.

Når kunder angir en leveringsadresse under betalingen, har de muligheten til å lagre adressen som en primær adresse. Dette alternativet vises bare hvis en kunde er logget på.

Selv om denne leveringsadressemodulen ikke tilbyr adressevalidering, kan denne funksjonaliteten implementeres ved hjelp av tilpassing.

Illustrasjonen nedenfor viser et eksempel på en ny leveringsadressemodul på en kasseside.

![Eksempel på en leveringsadressemodul på en kasseside.](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Modulegenskaper

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Overskrift | Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En valgfri overskrift for leveringsadressemodulen. |
| Vis adressetype | **Sann** eller **Usann** | Hvis denne valgfrie egenskapen er satt til **Sann**, vises en adressetype, for eksempel **Hjem** eller **Bedrift**. Hvis ingen adressetype er angitt, lagres adressen automatisk som **Type**=**Annet**. |
| Aktiver automatisk forslag| **Sann** eller **Usann** | Hvis denne valgfrie egenskapen er satt til **Sann**, vises automatiske adresseforslag. Du får disse forslagene fra Bing-kart. Hvis du vil ha informasjon om hvordan du konfigurerer integrering av Bing-kart for området, kan du se [Butikkvelgermodul](store-selector.md). Denne funksjonen er tilgjengelig fra og med Commerce-versjon 10.0.15.|
|Alternativer for automatisk forslag| Et nummer| Hvis automatiske adresseforslag er aktivert, kan du angi flere alternativer, for eksempel maksimalt antall forslag som skal gis.|

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Legge til en leveringsadressemodul på en kasseside og angi de nødvendige egenskapene

En leveringsadressemodul kan bare legges til i en kassemodul. Hvis du vil ha mer informasjon om hvordan du konfigurerer leveringsadressemodulen og legger den til på en kasseside, se [Kassemodul](add-checkout-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Handlekurvmodul](add-cart-module.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Kassemodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsalternativmodul](delivery-options-module.md)

[Hente informasjonsmodul](pickup-info-module.md)

[Modul for ordredetaljer](order-confirmation-module.md)

[Gavekortmodul](add-giftcard.md)

[Butikkvelgermodul](store-selector.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]