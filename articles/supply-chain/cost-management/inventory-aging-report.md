---
title: Eksempler og logikk for rapport for aldersfordeling for lager
description: Dette emnet presenterer noen eksempler som viser hvordan du kan tolke resultatene av en rapport for aldersfordeling for lager.
author: RichardLuan
manager: tfehr
ms.date: 5/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventAgingStorage, InventAgingStorageChart, InventAgingStorageDetails
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: riluan
ms.search.validFrom: 2020-5-29
ms.dyn365.ops.version: ''
ms.openlocfilehash: 1d9c70a7931c009cd53fbd28a3f4c768d04964a4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214424"
---
# <a name="inventory-aging-report-examples-and-logic"></a>Eksempler og logikk for rapport for aldersfordeling for lager

[!include [banner](../includes/banner.md)]

Dette emnet presenterer noen eksempler som viser hvordan du kan tolke resultatene av en **Aldersfordeling for lager**-rapport. Denne rapporten kategoriserer antall på lager og lagerverdier for en valgt vare eller varegruppe i flere perioder. Dette emnet viser også den interne logikken i rapporten.

Eksemplene i dette emnet viser resultater som vises på en standardrapport for **aldersfordeling for lager**. Generelt sett anbefales det imidlertid at du bruker versjonen [Lagring av rapport for aldersfordeling for lager](inventory-aging-report-storage.md) av denne rapporten, særlig når du har mange varer og lagre som må behandles. Lagring av rapport for aldersfordeling for lager lagrer hver rapport du genererer, viser resultatene som en interaktiv side og et diagram, og lar deg eksportere alle lagrede rapporter.

## <a name="sample-data-that-is-used-in-these-examples"></a>Eksempeldata som brukes i disse eksemplene

Eksemplene i dette emnet er basert på eksempeldata for lagertransaksjon som er beskrevet i denne delen.

### <a name="storage-dimension-setup"></a>Lagringsdimensjonsoppsett

Eksempelsystemet inneholder følgende oppsett av lagringsdimensjoner.

| Navn      | Aktivt | Aktuell beholdning | Økonomisk lager |
|-----------|--------|--------------------|---------------------|
| Nettsted      | Ja    | Ja                | Ja                 |
| Lager | Ja    | Ja                | Nei                  |

### <a name="inventory-model"></a>Lagermodell

For eksempelsystemet er lagermodellen for de frigitte produktene *FIFO*, og **Kostpris**-innstillingen for lagermodellen er *Ta med fysisk verdi*.

### <a name="inventory-transactions"></a>Lagertransaksjoner

Eksempelsystemet inneholder følgende lagertransaksjoner for et frigitt produkt som har varenummer *1000*.

| Referanse      | Nettsted | Lager | Tilgang   | Avgang | Fysisk dato | Økonomisk dato | Antall | Kostnadsbeløp | Fysisk kostbeløp |
|----------------|------|-----------|-----------|-------|---------------|----------------|----------|-------------|----------------------|
| Bestilling | 1    | 11        | Kjøpt |       | 15. mars      | 15. mars       | 10       | 1 000       | 1 000                |
| Bestilling | 2    | 21        | Kjøpt |       | 15. mars      | 15. mars       | 10       | 2,000       | 2,000                |
| Bestilling | 1    | 11        | Mottatt  |       | 15. april      |                | 5        |             | 375                  |
| Overføringsordre | 1    | 11        |           | Solgt  | 2. mai         | 2. mai          | -5       | -458,33     | -458,33              |
| Overføringsordre | 1    | 12        | Kjøpt |       | 2. mai         | 2. mai          | 5        | 458.33      | 458.33               |
| Salgsordre    | 1    | 12        |           | Solgt  | 3. mai         | 3. mai          | -1       | -91,67      | -91,67               |

## <a name="how-quantities-and-amounts-in-each-period-bucket-are-calculated"></a>Slik beregnes antall og beløp i hver periode

Ved å bruke eksempeldataene som er beskrevet i de forrige delene, kan du kjøre en rapport for **aldersfordeling for lager** med følgende innstillinger:

- **Per dato:** *9. mai 2020*
- **Område:** *Visning*
- **Lager:** *Nei*
- **Varenummer:** *Total*
- **Aldersfordelingsperiode:** Sett dette feltet til å generere månedlige perioder.

I dette tilfellet vil innholdet i rapporten som genereres, ligne følgende eksempel.

<table>
<thead>
<tr>
    <th rowspan="2">Varenummer</th>
    <th rowspan="2">Nettsted</th>
    <th rowspan="2">Antall på lager</th>
    <th rowspan="2">Beholdningsverdi</th>
    <th rowspan="2">Lagerverdiantall</th>
    <th rowspan="2">Lagerverdi</th>
    <th rowspan="2">Gjennomsnittlig enhetskostnad</th>
    <th colspan="2">5/8/2020–5/1/2020</th>
    <th colspan="2">4/30/2020–4/1/2020</th>
    <th colspan="2">3/31/2020–3/1/2020</th>
</tr>
<tr>
    <th>P1:Antall</th>
    <th>P1:Beløp</th>
    <th>P2:Antall</th>
    <th>P2:Beløp</th>
    <th>P3:Antall</th>
    <th>P3:Beløp</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>9.00</td>
    <td>825.00</td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 totaler</strong></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>19</strong></td>
    <td><strong>2,825.00</strong></td>
</tr>
</tfoot>
</table>

Merk deg følgende detaljer i denne eksempelrapporten:

- Verdiene **Lagerverdiantall**, **Lagerverdi** og **Gjennomsnittlig enhetskostnad** som vises i rapporten, er verdier for den økonomiske lagerdimensjonen (**Område** i dette tilfellet).

    Rapporten viser for eksempel følgende informasjon for område 1:

    - Verdien **Lagerverdiantall** er *14* (= 10 + 5 – 5 + 5 – 1).
    - Verdien **Lagerverdi** er *1283,33* (= 1000 + 375 – 458,33 + 458,33 – 91,67).
    - Verdien **Gjennomsnittlig enhetskostnad** er *91,67*.
    - Verdien **Beholdningsverdi** og **Beløp** i hver periode beregnes ved hjelp av verdien **Gjennomsnittlig enhetskostnad**.

- Rapporten bestemmer lagerbeholdningen for hver periode ved å summere det totale mottatte beholdningsantallet for hver periode. Deretter brukes prinsippet først-inn-først-ut (FIFO) til å trekke fra det totale utstedte antallet, uansett lagermodellen som varene bruker.

Hvis du kjører samme rapport på nytt, men denne gangen angir både verdiene **Område** og **Lager** til *Visning*, vil den nye rapporten ligne på følgende eksempel.

<table>
<thead>
<tr>
    <th rowspan="2">Varenummer</th>
    <th rowspan="2">Nettsted</th>
    <th rowspan="2">Lager</th>
    <th rowspan="2">Antall på lager</th>
    <th rowspan="2">Beholdningsverdi</th>
    <th rowspan="2">Lagerverdiantall</th>
    <th rowspan="2">Lagerverdi</th>
    <th rowspan="2">Gjennomsnittlig enhetskostnad</th>
    <th colspan="2">5/8/2020–5/1/2020</th>
    <th colspan="2">4/30/2020–4/1/2020</th>
    <th colspan="2">3/31/2020–3/1/2020</th>
</tr>
<tr>
    <th>P1:Antall</th>
    <th>P1:Beløp</th>
    <th>P2:Antall</th>
    <th>P2:Beløp</th>
    <th>P3:Antall</th>
    <th>P3:Beløp</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>916.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td></td>
    <td></td>
    <td>5.00</td>
    <td>458.33</td>
    <td>5.00</td>
    <td>458.33</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>366.67</td>
    <td>14</td>
    <td>1,283.33</td>
    <td>91.67</td>
    <td>4.00</td>
    <td>366.67</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 totaler</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,283.33</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>366.67</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>458.33</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,458.33</strong></td>
</tr>
</tfoot>
</table>

Denne gangen er område 1 delt inn i to rader, én for lager 11 og én for lager 12. Verdiene **Lagerverdiantall**, **Lagerverdi** og **Gjennomsnittlig enhetskostnad** er imidlertid de samme fordi **Lager** ikke er en økonomisk lagerdimensjon.

Legg også merke til at antallsdistribusjonen for område 1 er forskjellig. I den første rapporten du kjørte, ignorerte systemet overføringsordren som ble funnet på det samme området, og trakk fra antallet av salgsfakturaen fra **3/31/2020–3/1/2020**-perioden i område 1. I den nye rapporten trekker imidlertid systemet fra antallet for salgsfakturaen fra **5/8/2020–5/1/2020**-perioden i lager 12.

## <a name="effects-of-inventory-closing"></a>Virkninger av lagerlukking

Hvis du kjører lagerlukking for mai og deretter kjører den forrige rapporten på nytt, men du angir feltet **Per dato** til *31. mai 2020*, vil du se følgende resultater:

- Verdiene **Beholdningsverdi** og **Gjennomsnittlig enhetskostnad** oppdateres.
- Verdien **Beholdningsverdi** og verdiene **Beløp** i hver periode oppdateres i henhold til dette.

Den nye rapporten vil ligne på følgende eksempel.

<table>
<thead>
<tr>
    <th rowspan="2">Varenummer</th>
    <th rowspan="2">Nettsted</th>
    <th rowspan="2">Lager</th>
    <th rowspan="2">Antall på lager</th>
    <th rowspan="2">Beholdningsverdi</th>
    <th rowspan="2">Lagerverdiantall</th>
    <th rowspan="2">Lagerverdi</th>
    <th rowspan="2">Gjennomsnittlig enhetskostnad</th>
    <th colspan="2">5/31/2020–5/1/2020</th>
    <th colspan="2">4/30/2020–4/1/2020</th>
    <th colspan="2">3/31/2020–3/1/2020</th>
</tr>
<tr>
    <th>P1:Antall</th>
    <th>P1:Beløp</th>
    <th>P2:Antall</th>
    <th>P2:Beløp</th>
    <th>P3:Antall</th>
    <th>P3:Beløp</th>
</tr>
</thead>
<tbody>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>11</td>
    <td>10</td>
    <td>910.70</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>0.00</td>
    <td></td>
    <td>5.00</td>
    <td>455.36</td>
    <td>5.00</td>
    <td>455.36</td>
</tr>
<tr>
    <td>1000</td>
    <td>1</td>
    <td>12</td>
    <td>4</td>
    <td>364.29</td>
    <td>14</td>
    <td>1,275.00</td>
    <td>91.07</td>
    <td>4.00</td>
    <td>364.29</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
</tr>
<tr>
    <td>1000</td>
    <td>2</td>
    <td></td>
    <td>10</td>
    <td>2,000.00</td>
    <td>10</td>
    <td>2,000.00</td>
    <td>200.00</td>
    <td></td>
    <td></td>
    <td></td>
    <td></td>
    <td>10,00</td>
    <td>2,000.00</td>
</tr>
</tbody>
<tfoot>
<tr>
    <td><strong>1000 totaler</strong></td>
    <td></td>
    <td></td>
    <td><strong>24.00</strong></td>
    <td><strong>3,275.00</strong></td>
    <td></td>
    <td></td>
    <td></td>
    <td><strong>4.00</strong></td>
    <td><strong>364.29</strong></td>
    <td><strong>5.00</strong></td>
    <td><strong>455.36</strong></td>
    <td><strong>15</strong></td>
    <td><strong>2,455.36</strong></td>
</tr>
</tfoot>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]