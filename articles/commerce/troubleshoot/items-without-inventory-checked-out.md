---
title: Varer uten lager kan sjekkes ut
description: Denne artikkelen gir feilsøkingsveiledning som kan hjelpe når kunder kan legge til varer på lager i handlekurven og gå videre til betaling.
author: Reza-Assadi
ms.date: 03/11/2021
ms.topic: Troubleshooting
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: rassadi
ms.search.validFrom: 2021-01-31
ms.dyn365.ops.version: 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.industry: Retail
ms.openlocfilehash: 3bc924e44077886b942e19b25a84f0f1d4298c13
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9282741"
---
# <a name="items-without-inventory-can-be-checked-out"></a>Varer uten lager kan sjekkes ut

[!include [banner](../../includes/banner.md)]

Denne artikkelen gir feilsøkingsveiledning som kan hjelpe når kunder kan legge til varer på lager i handlekurven og gå videre til betaling.

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
