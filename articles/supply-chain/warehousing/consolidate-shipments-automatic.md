---
title: Konsolidere forsendelser som frigis til lageret ved hjelp av automatisk frigivelse av salgsordrer
description: Denne artikkelen viser et scenario der flere ordrer frigis til lageret i samme automatiserte fremgangsmåte for automatisk frigivelse-til-lager.
author: Mirzaab
ms.date: 05/12/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSShipConsolidationPolicy, WHSShipConsolidationWorkbench, WHSFilterGroupTable, WHSShipmentConsolidation, WHSFilterGenerallyAvail
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: ba8e9790a5b7eb00b20fba19f452118e1f05fed0
ms.sourcegitcommit: 3d7ae22401b376d2899840b561575e8d5c55658c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/08/2022
ms.locfileid: "9428261"
---
# <a name="consolidate-shipments-released-to-the-warehouse-using-automatic-release-of-sales-orders"></a>Konsolidere forsendelser som frigis til lageret ved hjelp av automatisk frigivelse av salgsordrer

[!include [banner](../includes/banner.md)]

Denne artikkelen viser et scenario der flere ordrer frigis til lageret i samme automatiserte fremgangsmåte for automatisk frigivelse-til-lager. Ordrene blir automatisk konsolidert i forsendelser, basert på regler som er definert som policyer for forsendelseskonsolidering.

I løpet av  kan du opprette sett med salgsordrer og frigi hvert sett til lageret. Du vil deretter se over forsendelsene som ble opprettet eller oppdatert under forsendelseskonsolideringen, basert på de konfigurerte policyene.

## <a name="make-demo-data-available"></a>Gjøre demodata tilgjengelig

Scenarioet i denne artikkelen refererer til verdier og poster som er inkludert i standard demodata som leveres med Microsoft Dynamics 365 Supply Chain Management. Hvis du vil bruke verdiene som angis her etter hvert som du utfører øvelsene, må du sørge for å arbeide i et miljø der demodataene er installert, og sette den juridiske enheten til **USMF** før du begynner.

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

#### <a name="sales-order-1-2"></a>Salgsordre 1-2

1. Opprett en salgsordre med følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Leveringsmåte:** *Airwa-Air*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

#### <a name="sales-order-1-3"></a>Salgsordre 1-3

1. Opprett en salgsordre med følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Leveringsmåte:** *10*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

1. Legg til en ny ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0002* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*
    - **Leveringsmåte:** *Airwa-Air*

### <a name="create-order-set-2"></a>Opprett ordresett 2

#### <a name="sales-orders-2-1-and-2-2"></a>Salgsordrer 2-1 og 2-2

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-002*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *M9200* (en vare der filteret **Kode 4** er satt til *Brannfarlig*)
    - **Antall:** *1.00*

1. Legg til en ny ordrelinje som har følgende innstillinger:

    - **Varenummer:** *M9201* (en vare der filteret **Kode 4** er satt til *Eksplosivt*)
    - **Antall:** *1.00*
    - **Leveringsmåte:** *Airwa-Air*

### <a name="create-order-set-3"></a>Opprett ordresett 3

#### <a name="sales-order-3-1"></a>Salgsordre 3-1

1. Opprett en salgsordre med følgende innstillinger:

    - **Kundekonto:** *US-002*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *M9200* (en vare der filteret **Kode 4** er satt til *Brannfarlig*)
    - **Antall:** *1.00*

1. Legg til en ny ordrelinje som har følgende innstillinger:

    - **Varenummer:** *M9201* (en vare der filteret **Kode 4** er satt til *Eksplosivt*)
    - **Antall:** *1.00*
    - **Leveringsmåte:** *Airwa-Air*

> [!NOTE]
> Denne ordren er identisk med de to ordrene du opprettet for ordresett 2. Den er imidlertid oppført som sitt eget ordresett, ettersom du kan frigi den separat senere i dette .

### <a name="create-order-set-4"></a>Opprett ordresett 4

#### <a name="sales-order-4-1"></a>Salgsordre 4-1

1. Opprett en salgsordre med følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Kunderekvisisjon:** *1*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

### <a name="create-order-set-5"></a>Opprett ordresett 5

#### <a name="sales-orders-5-1-and-5-2"></a>Salgsordrer 5-1 og 5-2

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Kunderekvisisjon:** *2*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

#### <a name="sales-order-5-3"></a>Salgsordre 5-3

1. Opprett en salgsordre med følgende innstillinger:

    - **Kundekonto:** *US-001*
    - **Kunderekvisisjon:** *1*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

### <a name="create-order-set-6"></a>Opprett ordresett 6

#### <a name="sales-orders-6-1-and-6-2"></a>Salgsordrer 6-1 og 6-2

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-003*
    - **Kunderekvisisjon:** *2*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

#### <a name="sales-orders-6-3-and-6-4"></a>Salgsordrer 6-3 og 6-4

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-004*
    - **Kunderekvisisjon:** *1*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

#### <a name="sales-orders-6-5-and-6-6"></a>Salgsordrer 6-5 og 6-6

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-007*
    - **Område:** *6*
    - **Lager:** *61*
    - **Pulje:** *ShipCons*

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

#### <a name="sales-orders-6-7-and-6-8"></a>Salgsordrer 6-7 og 6-8

1. Opprett to identiske salgsordrer som har følgende innstillinger:

    - **Kundekonto:** *US-007*
    - **Område:** *6*
    - **Lager:** *61*
    - **Pulje:** La dette feltet stå tomt.

1. Legg til en ordrelinje som har følgende innstillinger:

    - **Varenummer:** *A0001* (en vare uten **Kode 4**-filter tilordnet)
    - **Antall:** *1.00*

## <a name="automatic-release-of-sales-orders-to-the-warehouse"></a>Automatisk frigivelse av salgsordrer til lageret

For hvert sett med salgsordrer du har opprettet tidligere, vil du fullføre en fremgangsmåte for automatisk frigivelse til lageret. I hvert tilfelle vil du arbeide med den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) som finnes her.

### <a name="basic-release-to-warehouse-procedure"></a><a name="release-procedure"></a>Grunnleggende fremgangsmåte for frigivelse til lager

For hvert sett med salgsordrer du har opprettet tidligere, fullfører du de tre fremgangsmåtene som er skissert i følgende underinndelinger.

#### <a name="update-the-wave-template-that-will-be-used-during-release"></a>Oppdatere bølgemalen som vil bli brukt under frigivelse

1. Gå til **Lagerstyring \> Oppsett \> Bølger \> Bølgemaler**.
1. Angi verdien *Forsendelse* for feltet **Bølgemaltype**.
1. Finn og velg bølgemalen som er knyttet til lageret du brukte i ordresettene du opprettet for dette . Hvis du for eksempel brukte lager *24*, velger du bølgemalen **24 Standardforsendelse**. Hvis du brukte lager *61*, velger du bølgemalen **61 Forsendelse**.
1. I handlingsruten velger du **Rediger**.
1. Sett alternativet **Behandle bølge ved frigivelse til lager** til *Nei*.

#### <a name="release-to-the-warehouse"></a>Frigi til lageret

1. Gå til **Lagerstyring \> Frigi til lager \> Automatisk frigivelse av salgsordrer**.
1. Angi verdien *Alle* for feltet **Antall som skal frigis**.
1. I hurtigfanen **Poster som skal inkluderes** velger du **Filter** for å åpne dialogboksen for spørring.
1. Velg **Legg til** i fanen **Område** for å legge til en rad som har følgende innstillinger i rutenettet:

    - **Tabell:** *Salgsordre*
    - **Avledet tabell:** *Salgsordre*
    - **Felt:** *Salgsordre*
    - **Vilkår:** Angi en kommadelt liste over salgsordrenumrene fra ønsket ordresett.

1. Velg **OK** for å lagre spørringen.
1. Velg **OK** for å starte prosedyren *Automatisk frigivelse til lager*.

#### <a name="review-the-shipment-that-is-created-or-updated"></a>Gå gjennom forsendelsen som er opprettet eller oppdatert

1. Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.
1. Finn og velg den påkrevde forsendelsen.
1. Hvis en konsolideringspolicy ble brukt da forsendelsen ble opprettet eller oppdatert, skal den vises i feltet **Policy for forsendelseskonsolidering**.

### <a name="release-sales-orders-from-order-set-1"></a>Frigi salgsordrer fra ordresett 1

Følg den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) for å frigi salgsordrene fra ordresett 1.

Når du er ferdig, skal du kunne se at to forsendelser ble opprettet:

- Den første forsendelsen inneholder tre linjer og ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerMode*.
- Den andre forsendelen, som ikke bruker transportmåten *Airways*, ble opprettet ved hjelp av policyen for forsendelseskonsolidering for *CustomerOrderNo*.

### <a name="release-sales-orders-from-order-set-2"></a>Frigi salgsordrer fra ordresett 2

Følg den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) for å frigi salgsordrene fra ordresett 2.

Når du er ferdig, skal du kunne se at tre forsendelser ble opprettet:

- Den første forsendelsen inneholder varer med statusen *Brannfarlig*.
- Hver av de to andre forsendelsene inneholder én linje med varen med statusen *Eksplosivt*.

### <a name="release-sales-orders-from-order-set-3"></a>Frigi salgsordrer fra ordresett 3

Følg den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) for å frigi salgsordrene fra ordresett 3.

Når du er ferdig, skal du kunne se at følgende handlinger oppstod:

- En eksisterende forsendelse (forsendelsen som ble opprettet da ordresett 2 ble frigitt til lageret) ble oppdatert. En linje som har elementet *Brannfarlig*, ble lagt til.
- Én ny forsendelse ble opprettet, og den inneholder elementet *Eksplosivt*.

### <a name="release-sales-orders-from-order-set-4"></a>Frigi salgsordrer fra ordresett 4

Følg den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) for å frigi salgsordrene fra ordresett 4.

Når du er ferdig, skal du kunne se at den eksisterende forsendelsen (der feltet **Kunderekvisisjon** er satt til *1*) ble oppdatert. En ny linje ble lagt til for forsendelsen.

### <a name="release-sales-orders-from-order-set-5"></a>Frigi salgsordrer fra ordresett 5

Følg den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) for å frigi salgsordrene fra ordresett 5.

Når du er ferdig, skal du kunne se at følgende handlinger oppstod:

- En eksisterende forsendelse (der feltet **Kunderekvisisjon** er satt til *1*) ble oppdatert. En linje fra salgsordre 5-3 (der feltet **Kunderekvisisjon** er satt til *1*) ble lagt til for salgsordren.
- Én ny forsendelse ble opprettet, der linjer fra salgsordre 5-1 og 5-2 grupperes i én forsendelse.

### <a name="release-sales-orders-from-order-set-6"></a>Frigi salgsordrer fra ordresett 6

Følg den [grunnleggende fremgangsmåten for frigivelse til lager](#release-procedure) for å frigi salgsordrene fra ordresett 6.

Når du er ferdig, skal du kunne se at fire forsendelser ble opprettet:

- Linjer fra to ordrer for kunde *US-003* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.
- Linjer fra to ordrer for kunde *US-004* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.
- Linjer fra salgsordre 6-5 og 6-6 for kunde *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Ordrepulje*.
- Linjer fra salgsordre 6-7 og 6-8 for kunde *US-007* ble gruppert i én forsendelse ved hjelp av policyen for forsendelseskonsolidering for *Kryssordre*.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over policyer for forsendelseskonsolidering](about-shipment-consolidation-policies.md)
- [Konfigurere policyer for forsendelseskonsolidering](configure-shipment-consolidation-policies.md)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]