---
title: Leveringsadressemodul
description: Dette emnet dekker leveringsadressemodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: aeaa410fde29b285fdbbdd6acac19b0c4e917aa5
ms.sourcegitcommit: 12d271bb26c7490e7525d9b4bbf125cdc39fef43
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/07/2020
ms.locfileid: "4414805"
---
# <a name="shipping-address-module"></a>Leveringsadressemodul

[!include [banner](includes/banner.md)]

Dette emnet beskriver leveringsadressemodulen og forklarer hvordan du konfigurerer den i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Med leveringsadressemodulen kan kunder legge til eller velge leveringsadressen for en ordre under betalingen. Hvis en kunde er logget på, vises alle adresser som tidligere ble lagret for denne kunden, og kunden kan velge mellom dem. Kunden kan også legge til en ny adresse. Leveringsadressemodulen brukes for alle varer i en ordre som krever levering.

Leveringsadresseformater kan defineres i Commerce Headquarters for hvert land eller område, og leveringsadressemodulen håndhever deretter regler som er spesifikk for land/område.

Når kunder angir en leveringsadresse under betalingen, har de muligheten til å lagre adressen som en primær adresse. Dette alternativet vises bare hvis en kunde er logget på.

Selv om denne leveringsadressemodulen ikke tilbyr adressevalidering, kan denne funksjonaliteten implementeres ved hjelp av tilpassing.

Illustrasjonen nedenfor viser et eksempel på en ny leveringsadressemodul på en kasseside.

![Eksempel på en leveringsadressemodul på en kasseside](./media/ecommerce-shippingaddress.PNG)

## <a name="module-properties"></a>Modulegenskaper

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Overskrift | Overskriftstekst og en overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | En valgfri overskrift for leveringsadressemodulen. |
| Vis adressetype | **Sann** eller **Usann** | Hvis denne valgfrie egenskapen er satt til **Sann**, vises en adressetype, for eksempel **Hjem** eller **Bedrift**. Hvis ingen adressetype er angitt, lagres adressen automatisk som **Type**=**Annet**. |

## <a name="add-a-shipping-address-module-to-a-checkout-page-and-set-the-required-properties"></a>Legge til en leveringsadressemodul på en kasseside og angi de nødvendige egenskapene

En leveringsadressemodul kan bare legges til i en kassemodul. Hvis du vil ha mer informasjon om hvordan du konfigurerer leveringsadressemodulen og legger den til på en kasseside, se [Kassemodul](add-checkout-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Handlekurvmodul](add-cart-module.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Kassemodul](add-checkout-module.md)

[Betalingsmodul](payment-module.md)

[Leveringsalternativmodul](delivery-options-module.md)

[Henteinformasjonsmodul](pickup-info-module.md)

[Ordredetaljermodul](order-confirmation-module.md)

[Gavekortmodul](add-giftcard.md)
