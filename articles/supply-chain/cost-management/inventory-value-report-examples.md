---
title: Eksempler og logikk for lagerverdirapport
description: Denne artikkelen gir noen eksempler på resultater som presenteres for hver type lagerverdirapport. Lagerverdirapporter inneholder informasjon om fysisk og finansielle antall og beløp for beholdningen.
author: JennySong-SH
ms.date: 10/19/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-10-19
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: e6c6387be5204fde6ebc7a4983567801900974af
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877660"
---
# <a name="inventory-value-report-examples-and-logic"></a>Eksempler og logikk for lagerverdirapport

[!include [banner](../includes/banner.md)]

Lagerverdirapporter inneholder informasjon om fysisk og finansielle antall og beløp for beholdningen. Denne artikkelen gir noen eksempler på resultater som presenteres for hver type lagerverdirapport.

Hvis du vil ha mer informasjon om hvordan du genererer og bruker hver type lagerverdirapport, kan du se [Lagerverdirapporter](inventory-value-report-storage.md).

## <a name="sample-data-that-is-used-in-these-examples"></a>Eksempeldata som brukes i disse eksemplene

Eksemplene i denne artikkelen er basert på eksempeldata for lagertransaksjon som er beskrevet i denne delen.

### <a name="storage-dimension-setup"></a>Lagringsdimensjonsoppsett

Eksempelsystemet inneholder følgende oppsett av lagringsdimensjoner.

| Navn | Aktivt | Aktuell beholdning | Økonomisk lager |
|---|---|---|---|
| Nettsted | Ja | Ja | Ja |
| Lager | Ja | Ja | Nei |

### <a name="inventory-model"></a>Lagermodell

For eksempelsystemet er lagermodellen for de frigitte produktene *FIFO*, og **Kostpris**-feltet for lagermodellen er *Ta med fysisk verdi*.

### <a name="inventory-transactions"></a>Lagertransaksjoner

Eksempelsystemet inneholder følgende lagertransaksjoner for et frigitt produkt som har varenummer *B0001*.

| Referanse | Nettsted | Lager | Tilgang | Problem | Fysisk dato | Økonomisk dato | Antall | Kostnadsbeløp | Fysisk kostbeløp |
|---|---|---|---|---|---|---|---|---|---|
| Bestilling | 1 | 11 | Kjøpt | | 15. mars | 15. mars | 10 | 1 000 | 1 000 |
| Bestilling | 2 | 21 | Kjøpt | | 15. mars | 15. mars | 10 | 2,000 | 2,000 |
| Bestilling | 1 | 11 | Mottatt | | 15. april | | 5 | | 375 |
| Overføringsordre | 1 | 11 | | Solgt | 2. mai | 2. mai | -5 | -458,33 | -458,33 |
| Overføringsordre | 1 | 12 | Kjøpt | | 2. mai | 2. mai | 5 | 458.33 | 458.33 |
| Salgsordre | 1 | 12 | | Solgt | 3. mai | 3. mai | -1 | -91,67 | -91,67 |

### <a name="inventory-value-report-configuration"></a>Konfigurasjon av lagerverdirapporten

Eksempelsystemet inneholder en konfigurasjon for lagerverdirapporten som har følgende innstillinger:

- **Område:** *Posteringsdatoen*
- **Lager:** *Ja*
- **Beregn gjennomsnittlig enhetskostnad:** *Ja*
- **Totalt antall og verdi:** *Ja*
- **Område, Visning:** *Valgt*
- **Ressurs-ID, Visning:** *Ja*
- **Nivå:** *Totaler*

## <a name="inventory-value-report-example-1"></a>Eksempel 1 på lagerverdirapport

Tabellen og illustrasjonene nedenfor viser resultatene når du bruker eksempeldataene og rapportkonfigurasjonen som er beskrevet tidligere i denne artikkelen.

| Ressurstype | Ressurs | Nettsted | Referanse | Lager: Finansantall | Lager: Finansbeløp | Lager: Fysisk antall postert | Lager: Fysisk beløp postert | Lager: Antall | Lager: Beløp | Gjennomsnittlig enhetskost |
|---|---|---|---|---|---|---|---|---|---|---|
| Materiale | B0001 | 1 | Sluttsaldo | 9.00 | 908.33 | 5.00 | 375.00 | 14,00 | 1,283.33 | 91.67 |
| Materiale | B0001 | 2 | Sluttsaldo | 10,00 | 2,000.00 | 0.00 | 0.00 | 10,00 | 2,000.00 | 200.00 |

### <a name="standard-inventory-value-report-for-example-1"></a>Standard lagerverdirapport for eksempel 1

Illustrasjonen nedenfor viser standard **Lagerverdi**-rapport for eksempel 1. (Velg illustrasjonen for å åpne en større versjon.)

[![Lagerverdirapport for eksempel 1.](media/inventory-value-report-ex1-small.png "Lagerverdirapport for eksempel 1")](media/inventory-value-report-ex1.png)

### <a name="inventory-value-report-storage-report-for-example-1"></a>Rapport for oppbevaring av lagerverdi for eksempel 1

Illustrasjonen nedenfor viser standard **Lagring av lagerverdirapport** for eksempel 1. (Velg illustrasjonen for å åpne en større versjon.)

[![Rapport for oppbevaring av lagerverdi for eksempel 1.](media/inventory-value-report-storage-ex1-small.png "Rapport for oppbevaring av lagerverdi for eksempel 1")](media/inventory-value-report-storage-ex1.png)

## <a name="inventory-value-report-example-2"></a>Eksempel 2 på lagerverdirapport

Følgende tabell og illustrasjoner viser resultatene når du bruker eksempeldataene som beskrives tidligere i denne artikkelen, men du endrer verdien i **Nivå**-feltet til *Transaksjoner* i rapportkonfigurasjonen, og du angir **Fra dato**-feltet til *15. mars* når du kjører rapporten.

| Ressurstype | Ressurs | Nettsted | Dato | Tall | Referanse | Lager: Finansantall | Lager: Finansbeløp | Lager: Fysisk antall postert | Lager: Fysisk beløp postert | Lager: Antall | Lager: Beløp |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materiale | B0001 | 1 | 15.03.2021 | 00000126 | Bestilling | 0.00 | 0.00 | 10,00 | 1,000.00 | **10.00** | **1,000.00** |
| Materiale | B0001 | 1 | 15.03.2021 | 00000126 | Bestilling | 10,00 | 1,000.00 | -10,00 | -1 000,00 | **0.00** | **0.00** |
| Materiale | B0001 | 1 | 15.04.2021 | 00000128 | Bestilling | 0.00 | 0.00 | 5.00 | 375.00 | **5.00** | **375.00** |
| Materiale | B0001 | 1 | 2.5.2021 | 000003 | Sending av overføringsordre | -5,00 | -458,33 | 0.00 | 0.00 | **-5.00** | **-458.33** |
| Materiale | B0001 | 1 | 2.5.2021 | 000003 | Mottak av overføringsordre | 5.00 | 458.33 | 0.00 | 0.00 | **5.00** | **458.33** |
| Materiale | B0001 | 1 | 3.5.2021 | 000835 | Salgsordre | 0.00 | 0.00 | -1.00 | -91,67 | **-1.00** | **-91.67** |
| Materiale | B0001 | 1 | 3.5.2021 | 000835 | Salgsordre | -1.00 | -91,67 | 1.00 | 91.67 | **0.00** | **0.00** |
| Materiale | B0001 | 2 | 15.03.2021 | 00000127 | Bestilling | 0.00 | 0.00 | 10,00 | 2,000.00 | **10.00** | **2,000.00** |
| Materiale | B0001 | 2 | 15.03.2021 | 00000127 | Bestilling | 10,00 | 2,000.00 | -10,00 | -2 000,00 | **0.00** | **0.00** |
| Materiale | B0001 | 2 | 2.5.2021 | 000003 | Sending av overføringsordre | 5.00 | 458.33 | 0.00 | 0.00 | **5.00** | **458.33** |
| Materiale | B0001 | 2 | 2.5.2021 | 000003 | Mottak av overføringsordre | -5,00 | -458,33 | 0.00 | 0.00 | **-5.00** | **-458.33** |

### <a name="standard-inventory-value-report-for-example-2"></a>Standard lagerverdirapport for eksempel 2

Illustrasjonen nedenfor viser standard **Lagerverdi**-rapport for eksempel 2. (Velg illustrasjonen for å åpne en større versjon.)

[![Lagerverdirapport for eksempel 2.](media/inventory-value-report-ex2-small.png "Lagerverdirapport for eksempel 2")](media/inventory-value-report-ex2.png)

### <a name="inventory-value-report-storage-report-for-example-2"></a>Rapport for oppbevaring av lagerverdi for eksempel 2

Illustrasjonen nedenfor viser standard **Lagring av lagerverdirapport** for eksempel 2. (Velg illustrasjonen for å åpne en større versjon.)

[![Rapport for oppbevaring av lagerverdi for eksempel 2.](media/inventory-value-report-storage-ex2-small.png "Rapport for oppbevaring av lagerverdi for eksempel 2")](media/inventory-value-report-storage-ex2.png)

## <a name="inventory-value-report-example-3"></a>Eksempel 3 på lagerverdirapport

Vi anbefaler at du kjører lagerverdirapporter etter omberegning eller lagerlukking, slik at du har transaksjonene og beløpene som påvirkes av omberegningen eller lagerlukkingen.

Følgende delseksjoner viser lagerverdirapporter som genereres etter at du har lukket lageret frem til 30. mai.

### <a name="example-3-when-the-totals-level-is-used"></a>Eksempel 3 når Totaler-nivået brukes

Tabellen nedenfor viser resultatene når du bruker eksempeldataene og rapportkonfigurasjonen som er beskrevet tidligere i denne artikkelen. (I denne rapportkonfigurasjonen er **Nivå**-feltet satt til *Totaler*.)

| Ressurstype | Ressurs | Nettsted | Referanse | Lager: Finansantall | Lager: Finansbeløp | Lager: Fysisk antall postert | Lager: Fysisk beløp postert | Lager: Antall | Lager: Beløp | Gjennomsnittlig enhetskost |
|---|---|---|---|---|---|---|---|---|---|---|
| Materiale | B0001 | 1 | Sluttsaldo | 9.00 | 900.00 | 5.00 | 375.00 | 14,00 | 1,275.00 | 91.07 |
| Materiale | B0001 | 2 | Sluttsaldo | 10,00 | 2,000.00 | 0.00 | 0.00 | 10,00 | 2,000.00 | 200.00 |

### <a name="example-3-when-the-transactions-level-is-used"></a>Eksempel 3 når Transaksjoner-nivået brukes

Følgende tabell viser resultatene når du bruker eksempeldataene som beskrives tidligere i denne artikkelen, men du endrer verdien i **Nivå**-feltet til *Transaksjoner* i rapportkonfigurasjonen.

| Ressurstype | Ressurs | Nettsted | Dato | Tall | Referanse | Lager: Finansantall | Lager: Finansbeløp | Lager: Fysisk antall postert | Lager: Fysisk beløp postert | Lager: Antall | Lager: Beløp |
|---|---|---|---|---|---|---|---|---|---|---|---|
| Materiale | B0001 | 1 | 15.03.2021 | 00000126 | Bestilling | 0.00 | 0.00 | 10,00 | 1,000.00 | 10,00 | 1,000.00 |
| Materiale | B0001 | 1 | 15.03.2021 | 00000126 | Bestilling | 10,00 | 1,000.00 | -10,00 | -1 000,00 | 0.00 | 0.00 |
| Materiale | B0001 | 1 | 15.04.2021 | 00000128 | Bestilling | 0.00 | 0.00 | 5.00 | 375.00 | 5.00 | 375.00 |
| Materiale | B0001 | 1 | 2.5.2021 | 000003 | Sending av overføringsordre | -5,00 | -458,33 | 0.00 | 0.00 | -5,00 | -458,33 |
| Materiale | B0001 | 1 | 2.5.2021 | 000003 | Mottak av overføringsordre | 5.00 | 458.33 | 0.00 | 0.00 | 5.00 | 458.33 |
| Materiale | B0001 | 1 | 3.5.2021 | 000835 | Salgsordre | 0.00 | 0.00 | -1.00 | -91,67 | -1.00 | -91,67 |
| Materiale | B0001 | 1 | 3.5.2021 | 000835 | Salgsordre | -1.00 | -91,67 | 1.00 | 91.67 | 0.00 | 0.00 |
| Materiale | B0001 | 1 | 31.05.2021 | 000835 | Salgsordre | 0.00 | -8,33 | 0.00 | 0.00 | 0.00 | -8,33 |
| Materiale | B0001 | 1 | 31.05.2021 | 000003 | Sending av overføringsordre | 0.00 | -41,67 | 0.00 | 0.00 | 0.00 | -41,67 |
| Materiale | B0001 | 1 | 31.05.2021 | 000003 | Mottak av overføringsordre | 0.00 | 41.67 | 0.00 | 0.00 | 0.00 | 41.67 |
| Materiale | B0001 | 2 | 15.03.2021 | 00000127 | Bestilling | 0.00 | 0.00 | 10,00 | 2,000.00 | 10,00 | 2,000.00 |
| Materiale | B0001 | 2 | 15.03.2021 | 00000127 | Bestilling | 10,00 | 2,000.00 | -10,00 | -2 000,00 | 0.00 | 0.00 |
| Materiale | B0001 | 2 | 2.5.2021 | 000003 | Sending av overføringsordre | 5.00 | 458.33 | 0.00 | 0.00 | 5.00 | 458.33 |
| Materiale | B0001 | 2 | 2.5.2021 | 000003 | Mottak av overføringsordre | -5,00 | -458,33 | 0.00 | 0.00 | -5,00 | -458,33 |
| Materiale | B0001 | 2 | 31.05.2021 | 000003 | Sending av overføringsordre | 0.00 | 41.67 | 0.00 | 0.00 | 0.00 | 41.67 |
| Materiale | B0001 | 2 | 31.05.2021 | 000003 | Mottak av overføringsordre | 0.00 | -41,67 | 0.00 | 0.00 | 0.00 | -41,67 |
