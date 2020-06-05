---
title: Konsolidere forsendelser manuelt ved hjelp av siden Konsolider forsendelser
description: Dette emnet viser et scenario der flere ordrer frigis til lageret, og deretter blir de konsolidert senere ved hjelp av siden Konsolider forsendelser.
author: GarmMSFT
manager: tfehr
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: v-olbara
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: acc6e1d09894b57d2bb063bacbcddef239c1a8bd
ms.sourcegitcommit: 8a2127c5af6cdbda30ccc1f9bef9bd4ab61e9e50
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2020
ms.locfileid: "3383830"
---
# <a name="consolidate-shipments-manually-by-using-the-consolidate-shipments-page"></a>Konsolidere forsendelser manuelt ved hjelp av siden Konsolider forsendelser

[!include [banner](../includes/banner.md)]

Dette emnet viser et scenario der flere ordrer frigis til lageret, og deretter blir de konsolidert senere ved hjelp av siden **Konsolider forsendelser**.

## <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

 i dette emnet refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Definer policyer for forsendelseskonsolidering og produktfiltre

 som beskrives her, forutsetter at du allerede har aktivert funksjonen, utførte øvelsene i [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og opprettet policyer og andre poster som er beskrevet der. Husk å utføre øvelsene før du fortsetter med dette .

## <a name="create-the-sales-orders-for-this-scenario"></a>Opprett salgsordrene for dette 

Begynn med å opprette en samling salgsordrer du kan arbeide med. Du må arbeide med et lager som er aktivert for prosessen for avansert lager (WMS). Med mindre et annet lager er nevnt eksplisitt, må det samme lageret brukes for hvert av de følgende ordresettene.

Gå til **Kunde \> Ordrer \> Alle salgsordrer**, og opprett en samling av salgsordrer som har innstillingene som er beskrevet i følgende underinndelinger.

### <a name="create-sales-orders-1-and-2"></a>Opprette salgsordre 1 og 2

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-007*
    - **Pulje:** *ShipCons*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.

### <a name="create-sales-orders-3-and-4"></a>Opprette salgsordre 3 og 4

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-007*
    - **Pulje:** La dette feltet stå tomt.

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.

## <a name="release-the-orders-to-the-warehouse"></a>Frigi ordrene til lageret

Følg disse trinnene for å frigi hver salgsordre du har opprettet for dette , til lageret.

1. Gå til **Kunde \> Ordrer \> Alle salgsordrer**.
1. Finn og velg salgosordren som skal frigis.
1. I handlingsruten velger du **Handlinger \> Frigi til lager** i kategorien **Lager** for å frigi den valgte salgsordren.
1. Gjenta denne prosedyren for hver salgsordre du opprettet for dette .

## <a name="consolidate-shipments"></a>Konsolider forsendelser

1. Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.
1. Finn og velg en forsendelse som ble opprettet da salgsordre 1 ble frigitt til lageret. (Feltet **Policy for forsendelseskonsolidering** for forsendelsen må settes til *Ordrepulje*.)
1. I handlingsruten velger du **Forsendelser \> Konsolider forsendelser** i kategorien **Forsendeler**.
1. Kontroller forsendelsene som er foreslått for konsolidering. Bare én forsendelse som har samme policy, bør foreslås for konsolidering.
1. Lukk siden **Forsendelseskonsolidering**.
1. Finn og velg en forsendelse som ble opprettet da salgsordre 3 ble frigitt til lageret. (Feltet **Policy for forsendelseskonsolidering** for forsendelsen må settes til *Standard*.)
1. I handlingsruten velger du **Forsendelser \> Konsolider forsendelser** i kategorien **Forsendeler**.
1. Kontroller at ingen forsendelser er foreslått for konsolidering.
1. Velg **Vis filtre**.
1. I ruten **Filtre** fjerner du filteret **Ordrenummer**, og deretter velger du **Bruk**.
1. Kontroller forsendelsene som er foreslått for konsolidering. Bare én forsendelse som har samme policy, bør foreslås for konsolidering.

## <a name="additional-resources"></a>Tilleggsressurser

- [Policyer for forsendelseskonsolidering](about-shipment-consolidation-policies.md)
- [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md)