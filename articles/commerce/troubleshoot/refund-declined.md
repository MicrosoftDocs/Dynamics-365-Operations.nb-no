---
title: Refusjon på en returordre avvises
description: Denne artikkelen inneholder feilsøkingsveiledning som kan hjelpe deg når en refusjon på en returordre avvises, fordi kredittkortet som brukes til fakturering, er forskjellig fra kortet som ble brukt under den opprinnelige betalingsautorisasjonen.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 8360be76fe5ef5ddfbcf290cf6272825bc1849f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879983"
---
# <a name="refund-on-a-return-order-is-declined"></a>Refusjon på en returordre avvises

[!include [banner](../../includes/banner.md)]

Denne artikkelen inneholder feilsøkingsveiledning som kan hjelpe deg når en refusjon på en returordre avvises, fordi kredittkortet som brukes til fakturering, er forskjellig fra kortet som ble brukt under den opprinnelige betalingsautorisasjonen.

## <a name="description"></a>beskrivelse

En tilbakebetaling avvises når kredittkortet som brukes til å fakturere en returordre, er forskjellig fra kortet som ble brukt under den opprinnelige betalingsautorisasjonen. Du får følgende feilmelding: Noen betalinger har ikke riktig status for postering. Valider statusen for alle betalinger før fakturering på nytt.

Detaljene for betalingsautorisasjon vil inneholde følgende feilmelding: Adyen-gatewayen SendRequest() mislyktes med statusen InternalServerError.22144; Tomt svar returnert fra Adyen. (22001);

![Feilmeldingen Refusjon på en returordre avvises.](media/refund-order-decline.jpg)

## <a name="resolution"></a>Løsning

### <a name="enable-blind-returns-in-adyen"></a>Aktivere blinde returer i Adyen

Hvis du vil aktivere blinde returer, følger du trinnene i [Feilsøke problemer med Dynamics 365 Payment Connector for Adyen](adyen-support.md) for å kontakte Adyen-kundestøttegruppen og be om at blinde returer skal aktiveres på Adyen-forretningsenheten.

## <a name="additional-resources"></a>Tilleggsressurser

[Dynamics 365 Payment Connector for Adyen](../dev-itpro/adyen-connector.md)

[Konfigurere Adyen-betalingskobling for Dynamics 365](https://docs.adyen.com/plugins/microsoft-dynamics)
