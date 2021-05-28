---
title: Varer uten lager kan sjekkes ut
description: Dette emnet gir feilsøkingsveiledning som kan hjelpe når kunder kan legge til varer på lager i handlekurven og gå videre til betaling.
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
ms.openlocfilehash: 4fa7769044c45faffd9ff61b3de8e6217a5e0354
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6018464"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Varer uten lager kan sjekkes ut

[!include [banner](../../includes/banner.md)]

Dette emnet gir feilsøkingsveiledning som kan hjelpe når kunder kan legge til varer på lager i handlekurven og gå videre til betaling.

## <a name="description"></a>beskrivelse

Brukerne kan legge til en vare i handlekurven, selv om det ikke finnes lagerbeholdning i butikken, og deretter gå videre til betalingssiden.

## <a name="resolution"></a>Oppløsning

### <a name="enable-the-show-out-of-stock-errors-property-in-commerce-site-builder"></a>Aktivere egenskapen Vis ut av lagerfeil i Commerce Site Builder

Hvis du vil aktivere egenskapen **Vis feil for utsolgte varer** i Commerce-områdebyggeren, gjør du følgende.

1. Velg området du arbeider på.
1. Velg **Sider** i navigasjonsruten til venstre.
1. Velg **CartPage** for å åpne den.
1. Velg sporet **Handlekurv 1**, velg **Rediger**, og merk deretter av for **Vis feil for utsolgte varer** i ruten for egenskaper.
1. Lagre og publiser siden.

## <a name="additional-resources"></a>Tilleggsressurser

[Bruke lagerinnstillinger](../inventory-settings.md)

[Beregne lagertilgjengelighet for detaljhandelskanaler](../calculated-inventory-retail-channels.md)

[Konfigurere lagerbuffere og lagernivåer](../inventory-buffers-levels.md)
