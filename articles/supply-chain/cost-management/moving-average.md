---
title: Glidende gjennomsnitt
description: Glidende gjennomsnitt er en uavbrutt kostmetode basert på gjennomsnittsprinsippet , der kostnadene for lageravganger ikke endres når innkjøpskostnaden endres. Forskjellen kapitaliseres og baseres på en proporsjonal beregning. Beløpet som gjenstår utgiftsføres.
author: AndersGirke
manager: tfehr
ms.date: 08/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: kamaybac
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0957fee111ec1fd5bb66951126869cf46d88b36e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4967489"
---
# <a name="moving-average"></a>Glidende gjennomsnitt

[!include [banner](../includes/banner.md)]

Glidende gjennomsnitt er en uavbrutt kostmetode basert på gjennomsnittsprinsippet , der kostnadene for lageravganger ikke endres når innkjøpskostnaden endres. Forskjellen kapitaliseres og baseres på en proporsjonal beregning. Beløpet som gjenstår utgiftsføres.

Når du bruker glidende gjennomsnittet, støttes ikke lagerutligninger og lagermerking. Lagerlukking påvirker ikke produkter som har et glidende gjennomsnitt som lagermodellgruppen, og genererer ikke utligninger mellom transaksjonene.

Følgende er forutsetninger når du bruker glidende gjennomsnittskostnad som etterkalkuleringsmetode.

1. På siden **Varemodellgrupper** konfigurerer du en varemodellgruppe som har **Glidende gjennomsnitt** valgt i feltet **Lagermodell**.

    > [!NOTE]
    > Nå **Glidende gjennomsnitt** som standard er valgt, er også feltene **Poster aktuell beholdning** og **Poster økonomisk lager** valgt.

1. På siden **Postering** tilordner du kontoer til **Prisdifferanse for glidende gjennomsnitt**. Du bruker kontoen **Prisdifferanse for glidende gjennomsnitt** når en kostnad må utgiftsføres proporsjonalt. Dette skjer i følgende to scenarioer:
    - Det er en forskjell i kostnaden mellom et kjøpsmottak og innkjøpsfakturaen og på grunn av at der en forskjell mellom det opprinnelige lagerantallet og den gjeldende beholdningsantallet.
    - Transaksjonene bringer lageret fra negativ til null, og det er en differanse mellom transaksjonskostnaden og den gjeldende glidende gjennomsnittskosten.

1. På siden **Postering** tilordner du kontoer til kontoene **Revaluering av kostnad for glidende gjennomsnitt** i fanen **Lager**. Du bruker kontoen **Revaluering av kostnad for glidende gjennomsnitt** når du vil justere den glidende gjennomsnittskostnaden til en ny enhetspris.

1. På siden **Frigitte produkter** kan du tilordne varemodellgruppen for glidende gjennomsnitt til produktet.

    > [!NOTE]
    > Lagerlukkingsprosessen lukker bare regnskapsperioden. Det påvirker ikke produkter som har tilordnet glidende gjennomsnitt som en varemodellgruppe.

## <a name="convert-to-the-moving-average-costing-method"></a>Konverter til etterkalkuleringsmetoden for glidende gjennomsnitt

Produkter kan konverteres til å bruke lagervurderingsmetoden for glidende gjennomsnitt. Denne typen konvertering utføres vanligvis på slutten av året, etter den siste måneden i det gjeldende året er avsluttet. Det gjøres ved hjelp av den gjeldende etterkalkuleringsmodellen for produktet. Du kan endre lageretterkalkuleringsmetoden fra en etterkalkuleringsmetode som er basert på gjennomsnittskostnad eller standardkostnad til en metode som er basert på glidende gjennomsnitt.

Hvis du endrer etterkalkuleringsmåten fra standard etterkalkuleringsmetode til metode for glidende gjennomsnitt, må du utføre følgende oppgaver:

1. Gjør justeringer for å få lagerantall og -verdier ned i 0 (null).
1. Når lagerverdien og -antallet er 0 (null), kan du endre varemodellgruppen til glidende gjennomsnitt.
1. Gjør justeringer for å få antallet og verdien tilbake til lager.

Du kan ikke endre lageretterkalkuleringsmetoden fra en metode for glidende gjennomsnitt til metoden først inn, først ut (FIFO), sist inn, først ut(LIFO) eller en metode for avveid gjennomsnitt.

> [!NOTE]
> Konvertering fra standardkost til glidende avveid gjennomsnitt er en manuell prosess.

Eksemplene nedenfor viser virkningene når etterkalkuleringsmetoden for glidende gjennomsnitt brukes. Det finnes fire konfigurasjoner:

- Differanse mellom bestilling og proporsjonalt utgiftsført kostnad
- Justering av produkt og lager for glidende gjennomsnitt
- Glidende gjennomsnitt med produksjon
- Glidende gjennomsnitt med en tilbakedatert transaksjon

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Differanse mellom bestilling og proporsjonalt utgiftsført kostnad

Produktkostnaden bestemmes av kjøpsmottaket med glidende gjennomsnitt. Når innkjøpsfakturaen posteres, hvis det er en forskjell i kostnad mellom kjøpsmottaket og innkjøpsfakturaen, justeres forskjellen proporsjonalt for de gjeldende produktene på lager, og eventuelle gjenstående beløp utgiftsføres.

I dette eksemplet opprettes og mottas en bestilling med én kostnad, og innkjøpsfakturaen posteres med en annen kostnad.

1. Opprett en bestilling for et antall på 2 og en enhetspris på 10,00.
1. Opprett et kjøpsmottak for produktet.
1. Opprett en salgsordre for et antall på 1 og en enhetspris på 10,00.
1. Opprett en kjøpsordre for et antall på 2 og en enhetspris på 12,00.

Forskjellen i enhetsprisen, 2,00, posteres til kontoen Prisdifferanse for glidende gjennomsnitt når innkjøpsfakturaen posteres. Grunnen er at to produkter ble kjøpt med en kostnad på 20,00. Ett av produktene ble solgt til en enhetspris på 10,00. Kjøpsfakturaen ble postert til en enhetspris på 12,00 med et antall på 2. Salgsprisen for produktet kan ikke posteres på 14,00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Justering av produkt og lager for glidende gjennomsnitt

Hvis du vil justere den glidende gjennomsnittskostnaden for et produkt, er det tillatt med lagerjusteringer per dagens dato. Du kan ikke tilbakedatere en lagerjustering for å rette opp den glidende gjennomsnittskostnaden for et produkt. Du kan ikke ha kostnadsflyten gjennom etterfølgende transaksjoner.

I dette eksemplet justeres den glidende gjennomsnittskostnaden til et produkt.

1. Velg produktet du vil justere den glidende gjennomsnittskostnaden for. 

 > [!NOTE]
 > Siden **Revaluering for glidende gjennomsnitt** undersøker lageret som er tilgjengelig for et produkt. Det valgte produktet har et postert antall på 1, en postert verdi på 12,00, en postert enhetskostnad på 12,00 og en enhetskostnad på 12,00.
    
1. Oppdater feltet **Enhetskostnad** til 16,00. Systemet beregner de gjenværende feltene.
1. Justeringen posteres.

> [!NOTE]
> Du kan bare justere den glidende gjennomsnittskostnaden per dagens dato.

På siden **Utligninger på bilag** kan du se en justering på 4,00 postert til kontoen Revaluering av kostnad for glidende gjennomsnitt.

## <a name="moving-average-with-production"></a>Glidende gjennomsnitt med produksjon

Glidende gjennomsnitt støtter produserte varer. Hvis du planlegger å bruke glidende gjennomsnitt i et produksjonsmiljø, velger du **Bruk estimert kostpris** på siden **Parametere for produksjonskontroll**. Dette betyr at kostprisen som blir beregnet under forhåndsberegning, brukes i stedet for den faktiske kostprisen for stykklisteberegningen.

## <a name="moving-average-with-a-backdated-transaction"></a>Glidende gjennomsnitt med en tilbakedatert transaksjon

Tilbakedaterte transaksjoner tilordnes den gjeldende, glidende gjennomsnittskostnaden, og produktets fysiske antall oppdateres, men produktets glidende gjennomsnittskostnad påvirkes ikke. I dette eksemplet med glidende gjennomsnitt posteres en tilbakedatert transaksjon for et glidende gjennomsnittsprodukt.

1. Opprett en lagerjustering for det glidende gjennomsnittsproduktet for et antall på 1 og en kostnad på 20,00.
1. Lagertransaksjonsloggen for produktet vil ligne på følgende:
    - En lagertransaksjon på 1, en kostnad på 16,00, en posteringsdato lik 15. januar og en transaksjonsdato lik 15. januar.
    - En lagerjustering på 1, en kostnad på 20,00, en posteringsdato lik 1. januar og en transaksjonsdato lik 15. januar.
1. Poster justeringen.

På siden **Lagertransaksjoner** kan du se at 4,00 er utgiftsført da det gjeldende glidende gjennomsnittet for produktet er 16,00. Du kan postere i fortiden, men forskjellen i kostnad utgiftsføres, så den glidende gjennomsnittskostnaden påvirkes ikke.

## <a name="negative-inventory-balances"></a>Negative lagersaldoer

Transaksjoner behandles på forskjellige måter, avhengig av om det nye beholdningsantallet etter transaksjonen er negativt, null eller positivt.

### <a name="new-balance-is-negative-or-zero"></a>Ny saldo er negativ eller null

Hvis det nye varebeholdningsantallet er negativt eller null, blir transaksjonen kostnadsberegnet ved gjeldende gjennomsnittskostnader. Hvis det er en forskjell mellom innkjøpsprisen og gjeldende gjennomsnittskostnader, posteres den til **Prisdifferanse for glidende gjennomsnitt**.

### <a name="new-balance-is-positive"></a>Ny saldo er positiv

Hvis den nye lagerbeholdningen er positiv etter transaksjonen, deles transaksjonen i to deler og etterberegnes på en annen måte, som oppsummert i tabellen nedenfor.

| Del | beskrivelse |
|---|---|
| Antall fra negativ til null | I lagerbeholdningen brukes den gjeldende glidende gjennomsnittskostnaden for varen i stedet for transaksjonskostnaden for den delen av mottaksantallet som øker lagersaldoen fra negativ til null. Forskjellen mellom transaksjonskostnaden og den gjeldende glidende gjennomsnittskostnaden, posteres den til **Prisdifferanse for glidende gjennomsnitt**. |
| Antall fra null til positiv | I lagerbeholdningen brukes transaksjonskostnaden for den delen av mottaksantallet som øker lagersaldoen fra null til positiv.                                                  |

## <a name="inventory-value-report"></a>Rapport for lagerverdi

I dette eksemplet med glidende gjennomsnitt skrives lagerverdirapporten ut for å støtte gjeldende glidende gjennomsnittsberegning for et produkt. Rapporten Lagerverdi kan skrive ut transaksjonene i kronologisk rekkefølge, sammen med kostnaden for å støtte den glidende gjennomsnittskostnadsberegningen av et produkt. Rapporten viser den glidende gjennomsnittskostnaden for produktet. I dialogboksen **Lagerverdirapporter** er det et datointervall som lar deg velge **Transaksjonstidspunkt** eller **Posteringsdato** som du kan sortere rapporten etter. **Posteringsdato**-alternativet er slik rapporten vanligvis skrives ut. **Transaksjonstidspunkt**-alternativet er den faktiske datoen da transaksjonen rapporteres og den glidende gjennomsnittskostnaden for produktet oppdateres. Du kan skrive ut rapporten Lagerverdi ved hjelp av alternativet **Sortering etter transaksjonstidspunkt** hvis du vil se beregningen av glidende gjennomsnittskostnad over tid. Tabellen nedenfor viser transaksjonene for produktet som rapporten skrives ut for, når alternativet **Sortering etter transaksjonstidspunkt** brukes.

| Transaksjonstidspunkt | Dato         | transaksjonstype           | Antall | Beløp | Gjennomsnittlig enhetskostnad |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. oktober    | Startsaldo          | 0        | 0,00   | 0,00              |
| 8. oktober        | 28. september | Tilbakedatert mottak          | 1        | 16,00  | 16,00             |
| 3. oktober        | 3. oktober    | Kjøpsmottak           | 2        | 20,00  | 12,00             |
| 5. oktober        | 5. oktober    | Salgsordre                | -1       | -10,00 | 13,00             |
| 7. oktober        | 7. oktober    | Innkjøpsfaktura           |          | 2,00   | 14,00             |
| 8. oktober        | 8. oktober    | Revaluering for glidende gjennomsnitt |          | 4.00   | 16.00             |
|                  | 31. oktober   | Sum                      | 2        | 32.00  | 16.00             |

> [!NOTE]
> Du kan ikke avstemme økonomi med lager ved hjelp av **Sortering etter transaksjonstidspunkt**. Rapporten må skrives ut ved hjelp av **Posteringsdato**-alternativet.
