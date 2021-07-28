---
title: Refusjon på en returordre avvises
description: Dette emnet inneholder feilsøkingsveiledning som kan hjelpe deg når en refusjon på en returordre avvises, fordi kredittkortet som brukes til fakturering, er forskjellig fra kortet som ble brukt under den opprinnelige betalingsautorisasjonen.
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
ms.openlocfilehash: 89fe41d7ce57b584be34b156696b4044c4571afe
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6347278"
---
# <a name="refund-on-a-return-order-is-declined"></a>Refusjon på en returordre avvises

[!include [banner](../../includes/banner.md)]

Dette emnet inneholder feilsøkingsveiledning som kan hjelpe deg når en refusjon på en returordre avvises, fordi kredittkortet som brukes til fakturering, er forskjellig fra kortet som ble brukt under den opprinnelige betalingsautorisasjonen.

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
