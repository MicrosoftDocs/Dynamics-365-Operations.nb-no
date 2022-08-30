---
title: Konsolidere forsendelser ved hjelp av arbeidsområdet for forsendelseskonsolidering
description: Denne artikkelen viser et scenario der flere ordrer frigis til lageret, og deretter blir de konsolidert til forsendelser senere ved hjelp av arbeidsområdet for forsendelseskonsolidering.
author: Mirzaab
ms.date: 08/09/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSShipConsolidationSetShipment
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.6
ms.openlocfilehash: db8dc5101b223a0033284d8e6c494721871809d8
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335803"
---
# <a name="consolidate-shipments-by-using-the-shipment-consolidation-workbench"></a>Konsolidere forsendelser ved hjelp av arbeidsområdet for forsendelseskonsolidering

[!include [banner](../includes/banner.md)]

Denne artikkelen viser et scenario der flere ordrer frigis til lageret, og deretter blir de konsolidert til forsendelser senere ved hjelp av arbeidsområdet for forsendelseskonsolidering.

## <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

Scenarioet i denne artikkelen refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Definer policyer for forsendelseskonsolidering og produktfiltre

 som beskrives her, forutsetter at du allerede har aktivert funksjonen, utførte øvelsene i [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og opprettet policyer og andre poster som er beskrevet der. Husk å utføre øvelsene før du fortsetter med dette .

## <a name="turn-the-manual-shipment-consolidation-feature-on-or-off"></a>Aktiver eller deaktiver funksjonen Manuell forsendelseskonsolidering

For å bruke manuell forsendelseskonsolidering må den være aktivert for systemet. Fra og med Supply Chain Management versjon 10.0.29 er funksjonen aktivert som standard. Administratorer kan aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Manuell forsendelseskonsolidering* i arbeidsområdet [Funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Du må også aktivere funksjonen *Konsolider forsendelse* før du kan opprette policyer (i Supply Chain Management, versjon 10.0.29 er funksjonen obligatorisk, og kan ikke deaktiveres). Hvis du vil ha mer informasjon, kan du se [Konfigurer policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md).

## <a name="create-the-sales-orders-for-this-scenario"></a>Opprett salgsordrene for dette 

Begynn med å opprette en samling salgsordrer du kan arbeide med. Du må arbeide med et lager som er aktivert for prosessen for avansert lager (WMS). Med mindre et annet lager er nevnt eksplisitt, må det samme lageret brukes for hvert av de følgende ordresettene.

Gå til **Kunde \> Ordrer \> Alle salgsordrer**, og opprett en samling av salgsordrer som har innstillingene som er beskrevet i følgende underinndelinger.

### <a name="create-order-set-1"></a>Opprett ordresett 1

#### <a name="sales-orders-1-1-and-1-2"></a>Salgsordrer 1-1 og 1-2

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Leveringsmåte:** *Airwa-Air*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.

#### <a name="sales-order-1-3"></a>Salgsordre 1-3

1. Opprett en salgsordre med følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Leveringsmåte:** *10*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.
1. Legg til en ny ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0002* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*
    - **Leveringsmåte:** *Airwa-Air*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere den nye ordrelinjen.

### <a name="create-order-set-2"></a>Opprett ordresett 2

#### <a name="sales-orders-2-1-and-2-2"></a>Salgsordrer 2-1 og 2-2

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-002*
    - **Leveringsmåte:** *Airwa-Air*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *M9200* (en vare der filteret **Kode 4** er satt til *Brannfarlig*)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.
1. Legg til en ny ordrelinje som har følgende innstillinger:

    - **Varenummer:** *M9201* (en vare der filteret **Kode 4** er satt til *Eksplosivt*)
    - **Antall:** *1.00*
    - **Leveringsmåte:** *Airwa-Air*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere den nye ordrelinjen.

### <a name="create-order-set-3"></a>Opprett ordresett 3

#### <a name="sales-orders-3-1-and-3-2"></a>Salgsordrer 3-1 og 3-2

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Kunderekvisisjon:** *1*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.

#### <a name="sales-orders-3-3-and-3-4"></a>Salgsordrer 3-3 og 3-4

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Kunderekvisisjon:** *2*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.

### <a name="create-order-set-4"></a>Opprett ordresett 4

#### <a name="sales-orders-4-1-and-4-2"></a>Salgsordrer 4-1 og 4-2

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-003*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.

#### <a name="sales-orders-4-3-and-4-4"></a>Salgsordrer 4-3 og 4-4

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-004*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.

#### <a name="sales-orders-4-5-and-4-6"></a>Salgsordrer 4-5 og 4-6

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-007*
    - **Område:** *6*
    - **Lager:** *61*
    - **Pulje:** *ShipCons*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.

#### <a name="sales-orders-4-7-and-4-8"></a>Salgsordrer 4-7 og 4-8

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-007*
    - **Område:** *6*
    - **Lager:** *61*
    - **Pulje:** La dette feltet stå tomt.

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.

## <a name="release-the-orders-to-the-warehouse"></a>Frigi ordrene til lageret

Følg disse trinnene for å frigi hver salgsordre du har opprettet for dette , til lageret.

1. Gå til **Kunde \> Ordrer \> Alle salgsordrer**.
1. Finn og velg salgosordren som skal frigis.
1. I handlingsruten velger du **Handlinger \> Frigi til lager** i fanen **Lager** for å frigi den valgte salgsordren.
1. Gjenta denne prosedyren for hver salgsordre du opprettet for dette .

## <a name="consolidate-the-shipments-by-using-the-shipment-consolidation-workbench"></a>Konsolidere forsendelsene ved hjelp av arbeidsområdet for forsendelseskonsolidering

1. Gå til **Lagerstyring \> Frigi til lager \> Arbeidsområde for forsendelseskonsolidering**.
1. I handlingsruten velger du **Rediger spørring**.
1. Velg **Legg til** i fanen **Område** i dialogboksen for redigeringsprogrammet for spørring for å legge til en rad som har følgende innstillinger i rutenettet:

    - **Tabell:** *Salgsordrer*
    - **Felt:** *Salgsordre*
    - **Vilkår:** Angi en kommadelt liste over salgsordrenumrene for hvert ordresett du har opprettet for dette .

1. Velg **OK** for å lagre spørringen og lukke dialogboksen.
1. Velg **Konsolider forsendelser** i handlingsruten.
1. Merk alle forsendelsene, og velg deretter **Konsolider** i handlingsruten.

## <a name="verify-the-shipments"></a>Bekrefte forsendelsene

I den følgende prosedyren kan du kontrollere forsendelsene som er opprettet eller oppdatert som et resultat av forsendelseskonsolidering. Bruk det til å gå gjennom hvert ordresett du har opprettet for dette , og se gjennom underinndelinge nedenfor for å kontrollere at du har fått de forventede resultatene.

1. Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.
1. Finn og velg den påkrevde forsendelsen.
1. Hvis en konsolideringspolicy ble brukt da forsendelsen ble opprettet eller oppdatert, skal den vises i feltet **Policy for forsendelseskonsolidering**.

### <a name="related-shipments-for-order-set-1"></a>Relaterte forsendelser for ordresett 1

To forsendelser skal ha blitt opprettet:

- Den første forsendelsen inneholder tre linjer og ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerMode*.
- Den andre forsendelen, som ikke bruker transportmåten *Airways*, ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerOrderNo*.

### <a name="related-shipments-for-order-set-2"></a>Relaterte forsendelser for ordresett 2

Tre forsendelser skal ha blitt opprettet:

- Den første forsendelsen inneholder varer med statusen *Brannfarlig*.
- Hver av de to andre forsendelsene inneholder én linje med varen med statusen *Eksplosivt*.

### <a name="related-shipments-for-order-set-3"></a>Relaterte forsendelser for ordresett 3

To forsendelser skal ha blitt opprettet:

- Den første forsendelsen inneholder ordrelinjer fra salgsordren der feltet **Kunderekvisisjon** er satt til *1*.
- Den andre forsendelsen inneholder ordrelinjer fra salgsordren der feltet **Kunderekvisisjon** er satt til *2*.

### <a name="related-shipments-for-order-set-4"></a>Relaterte forsendelser for ordresett 4

Fire forsendelser skal ha blitt opprettet:

- Linjer fra to ordrer for kunde *US-003* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.
- Linjer fra to ordrer for kunde *US-004* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.
- Linjer fra salgsordre 4-5 og 4-6 for kunde *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.
- Linjer fra salgsordre 4-7 og 4-8 for kunde *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Kryssordre*.

## <a name="additional-resources"></a>Tilleggsressurser

- [Policyer for forsendelseskonsolidering](about-shipment-consolidation-policies.md)
- [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]