---
title: Konsolidere forsendelser ved å frigi til lager fra arbeidsområdet for lastplanlegging
description: Dette emnet viser et scenario der flere ordrer frigis til lageret i samme last, og deretter blir de konsolidert automatisk til forsendelser.
author: GarmMSFT
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 2dda45f475f0119b202008f6f8d95c8ccc59a1e63108dbd766a49b3551cdf778
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6720114"
---
# <a name="consolidate-shipments-by-releasing-to-warehouse-from-the-load-planning-workbench"></a>Konsolidere forsendelser ved å frigi til lager fra arbeidsområdet for lastplanlegging

[!include [banner](../includes/banner.md)]

Dette emnet viser et scenario der flere ordrer frigis til lageret i samme last, og deretter blir de konsolidert automatisk til forsendelser.

## <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

 i dette emnet refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.

## <a name="set-up-shipment-consolidation-policies-and-product-filters"></a>Definer policyer for forsendelseskonsolidering og produktfiltre

 som beskrives her, forutsetter at du allerede har aktivert funksjonen, utførte øvelsene i [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md) og opprettet policyer og andre poster som er beskrevet der. Husk å utføre øvelsene før du fortsetter med dette .

## <a name="create-the-sales-orders-for-this-scenario"></a>Opprett salgsordrene for dette 

Begynn med å opprette en samling salgsordrer du kan arbeide med. Du må arbeide med et lager som er aktivert for prosessen for avansert lager (WMS). Med mindre et annet lager er nevnt eksplisitt, må det samme lageret brukes for hvert av de følgende ordresettene.

Gå til **Kunde \> Ordrer \> Alle salgsordrer**, og opprett en samling av salgsordrer som har innstillingene som er beskrevet i følgende underinndelinger.

### <a name="create-order-set-1"></a>Opprett ordresett 1

#### <a name="sales-order-1-1"></a>Salgsordre 1-1

1. Opprett en salgsordre med følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Leveringsmåte:** *Airwa-Air*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Velg **Lager \> Reservasjon**, og velg deretter **Reserver parti** i handlingsruten for å reservere ordrelinjen.

#### <a name="sales-order-1-2"></a>Salgsordre 1-2

1. Opprett en salgsordre med følgende innstillinger:

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

## <a name="use-the-load-planning-workbench-to-create-loads-and-release-them-to-the-warehouse"></a>Bruk arbeidsområde for lastplanlegging til å opprette laster og frigi dem til lageret

Følg disse trinnene for å opprette en belastning for hvert ordresett du har opprettet for dette , og deretter frigi det til lageret.

1. Gå til **Lagerstyring \> Laster \> Arbeidsområde for lastplanlegging**.
1. I fanen **Salgslinjer** finner du og velger alle salgsordrelinjene fra ett av ordresettene du opprettet for dette .
1. I handlingsruten velger du **Legg til \> I ny last** i fanen **Tilbud og etterspørsel** for å legge til de valgte ordrelinjene i en ny last.
1. I dialogboksen **Tilordning av lastmal** velger du en lastmal i feltet **Lastmal-ID**, for eksempel *Standard lastmal*.
1. Velg **OK** for å lukke dialogboksen. 
1. I delen **Laster** finner og velger du lasten du nettopp opprettet.
1. Velg **Frigi \> Frigi til lager** for å frigi den valgte lasten til lageret.
1. Gjenta denne prosedyren for de andre tre ordresettene du opprettet for dette .

## <a name="verify-the-shipments"></a>Bekrefte forsendelsene

I den følgende prosedyren kan du kontrollere forsendelsene som er opprettet eller oppdatert som et resultat av forsendelseskonsolidering. Bruk det til å gå gjennom hvert ordresett du har opprettet for dette , og se gjennom underinndelinge nedenfor for å kontrollere at du har fått de forventede resultatene.

1. Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.
1. Finn og velg den påkrevde forsendelsen.
1. Hvis en konsolideringspolicy ble brukt da forsendelsen ble opprettet eller oppdatert, skal den vises i feltet **Policy for forsendelseskonsolidering**.

### <a name="release-order-set-1-in-one-load"></a>Frigi ordresett 1 i én last

To forsendelser skal ha blitt opprettet:

- Den første forsendelsen inneholder tre linjer og ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerMode*.
- Den andre forsendelen, som ikke bruker transportmåten *Airways*, ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerOrderNo*.

### <a name="release-order-set-2-in-one-load"></a>Frigi ordresett 2 i én last

Tre forsendelser skal ha blitt opprettet:

- Den første forsendelsen inneholder varer med statusen *Brannfarlig*.
- Hver av de to andre forsendelsene inneholder én linje med varen med statusen *Eksplosivt*.

### <a name="release-order-set-3-in-one-load"></a>Frigi ordresett 3 i én last

To forsendelser skal ha blitt opprettet:

- Den første forsendelsen inneholder ordrelinjer fra salgsordren der feltet **Kunderekvisisjon** er satt til *1*.
- Den andre forsendelsen inneholder ordrelinjer fra salgsordren der feltet **Kunderekvisisjon** er satt til *2*.

### <a name="release-order-set-4-in-one-load"></a>Frigi ordresett 4 i én last

Fire forsendelser skal ha blitt opprettet:

- Linjer fra to ordrer for kundekonto *US-003* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.
- Linjer fra to ordrer for kundekonto *US-004* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.
- Linjer fra salgsordre 4-5 og 4-6 for kundekonto *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.
- Linjer fra salgsordre 4-7 og 4-8 for kundekonto *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Kryssordre*.

## <a name="additional-resources"></a>Tilleggsressurser

- [Policyer for forsendelseskonsolidering](about-shipment-consolidation-policies.md)
- [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]