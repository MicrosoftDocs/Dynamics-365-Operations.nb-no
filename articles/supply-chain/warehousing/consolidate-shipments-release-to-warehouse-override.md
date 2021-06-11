---
title: Konsolidere forsendelser når policyen for forsendelseskonsolidering overstyres
description: Dette emnet viser et scenario der én eller flere salgslinjer må frigis manuelt til lageret fra siden Frigi til lager, og den systemdefinerte policyen for forsendelseskonsolidering må overstyres før utgivelsen.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipConsolidationSetShipment, WHSShipmentConsolidation, WHSFilterGenerallyAvail, WHSReleaseToWarehouse
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: 6928375c88a199bd9c6b48f05b38343463762920
ms.sourcegitcommit: 53b797ff1b524f581046b48cdde42f50b37495bc
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/28/2021
ms.locfileid: "6117015"
---
# <a name="consolidate-shipments-when-the-shipment-consolidation-policy-is-overridden"></a>Konsolidere forsendelser når policyen for forsendelseskonsolidering overstyres

[!include [banner](../includes/banner.md)]

Dette emnet viser et scenario der én eller flere salgslinjer må frigis manuelt til lageret fra siden **Frigi til lager**, og den systemdefinerte policyen for forsendelseskonsolidering må overstyres før utgivelsen. Det kan være nødvendig å overstyre en policy for forsendelseskonsolidering hvis en ordre som vanligvis ikke er konsolidert med åpne forsendelser, for eksempel skal konsolideres med åpne forsendelser.

I løpet av  skal du opprette et sett med salgsordrer og deretter overstyre standardinnstillingen for forsendelseskonsolidering før du frigir ordrene til lageret.

## <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

 i dette emnet refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Definer policyer for forsendelseskonsolidering og produktfiltre

 som beskrives her, forutsetter at du allerede har aktivert funksjonen, utførte øvelsene i [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og opprettet policyer og andre poster som er beskrevet der. Husk å utføre øvelsene før du fortsetter med dette .

## <a name="create-the-sales-orders-for-this-scenario"></a>Opprett salgsordrene for dette 

1. Gå til **Kunde \> Ordrer \> Alle salgsordrer**, og opprett tre identiske salgsordrer med følgende innstillinger:

    - **Kundekonto:** *US-002*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.

## <a name="release-the-sales-orders-from-the-release-to-warehouse-page"></a>Frigi salgsordrene fra siden Frigi til lager

Følg disse trinnene for å overstyre policyen for forsendelseskonsolidering under frigivelse til lageret.

1. Gå til **Lagerstyring \> Frigi til lager \> Frigi til lager**.
1. I den øvre ruten velger du den første salgsordren du opprettet for dette .
1. Velg **Legg til** for å legge til linjen i frigivelsen til lageret. Legg merke til at policyen for forsendelseskonsolidering av typen *Standard* brukes i den nederste ruten.
1. I den nederste ruten velger du **Velg ny policy for forsendelseskonsolidering**.
1. Velg en policy som tillater konsolidering med andre åpne forsendelser av samme policy. Velg for eksempel policyen *CustomerOrderNo*.
1. Velg **Frigi til lager**.
1. Velg den andre og tredje salgsordren du opprettet for dette .
1. Velg **Legg til** for å legge til linjene i frigivelsen til lageret. Legg merke til at policyen av typen *Standard* brukes i den nederste ruten.
1. Velg den andre linjen, og deretter velger du policyen *CustomerOrderNo* i feltet **Velg ny policy for forsendelseskonsolidering**.
1. Velg **Frigi til lager** for begge linjene.

## <a name="verify-the-shipments"></a>Bekrefte forsendelsene

To forsendelser skal ha blitt opprettet:

- Den første forsendelsen inneholder to linjer og ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerOrderNo*.
- Den andre forsendelsen inneholder én linje og ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *Standard*.

Følg disse trinnene for å se gjennom forsendelsene som ble opprettet.

1. Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.
1. Finn og velg den påkrevde forsendelsen.
1. I feltet **Policy for forsendelseskonsolidering** ser du gjennom konsolideringspolicyen som ble brukt da forsendelsen ble opprettet.

## <a name="additional-resources"></a>Tilleggsressurser

- [Policyer for forsendelseskonsolidering](about-shipment-consolidation-policies.md)
- [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]