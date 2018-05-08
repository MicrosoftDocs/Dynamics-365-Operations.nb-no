---
title: Glidende gjennomsnitt
description: "Glidende gjennomsnitt er en uavbrutt kostmetode basert på gjennomsnittsprinsippet , der kostnadene for lageravganger ikke endres når innkjøpskostnaden endres. Forskjellen kapitaliseres og baseres på en proporsjonal beregning. Beløpet som gjenstår utgiftsføres."
author: AndersGirke
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: InventModelGroup
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 65531
ms.assetid: dfd10099-8f7f-44b1-917e-df37c2fe8773
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c1f8a8cf4a58177d423709f245760a5ba9ca7e4e
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="moving-average"></a>Glidende gjennomsnitt

[!include [banner](../includes/banner.md)]

Glidende gjennomsnitt er en uavbrutt kostmetode basert på gjennomsnittsprinsippet , der kostnadene for lageravganger ikke endres når innkjøpskostnaden endres. Forskjellen kapitaliseres og baseres på en proporsjonal beregning. Beløpet som gjenstår utgiftsføres. 

Når du bruker glidende gjennomsnittet, støttes ikke lagerutligninger og lagermerking. Lagerlukking påvirker ikke produkter som har et glidende gjennomsnitt som lagermodellgruppen, og genererer ikke utligninger mellom transaksjonene.

Følgende er forutsetninger når du bruker glidende gjennomsnittskostnad som etterkalkuleringsmetode.

1.  På siden **Varemodellgrupper** kan du definere en varemodellgruppe som har glidende gjennomsnitt valgt i feltet **Lagermodell**. **Obs!** Som standard når det er merket av for glidende gjennomsnitt, velges også feltet **Poster aktuell beholdning** og **Poster økonomisk lager**. 

2.  På siden **Postering**, tildel kontoene til **Prisdifferanse for glidende gjennomsnitt** og kontoene **Revaluering av kostnad for glidende gjennomsnitt** i kategorien **Lager**. Du bruker kontoen **Prisdifferanse for glidende gjennomsnitt** når kostnad må føres forholdsmessig. Dette skjer på grunn av en forskjell i kostnad mellom et kjøpsmottak og innkjøpsfakturaen og på grunn av en forskjell mellom det opprinnelige lagerantallet og den gjeldende beholdningsantallet. Bruk kontoen **Revaluering av kostnad for glidende gjennomsnitt** når du vil justere den glidende gjennomsnittskostnaden for et produkt til en ny enhetspris.
3.  På **Frigitte produkter**-siden kan du tilordne varemodellgruppen for glidende gjennomsnitt til produktet. **Obs!** Lagerlukkingsprosessen lukker bare regnskapsperioden. Det påvirker ikke produkter som har tilordnet glidende gjennomsnitt som en varemodellgruppe.

## <a name="convert-to-the-moving-average-costing-method"></a>Konverter til etterkalkuleringsmetoden for glidende gjennomsnitt
Produkter kan konverteres til å bruke lagervurderingsmetoden for glidende gjennomsnitt. Denne typen konvertering utføres vanligvis på slutten av året, etter den siste måneden i det gjeldende året er avsluttet. Det gjøres ved hjelp av den gjeldende etterkalkuleringsmodellen for produktet. Du kan endre lageretterkalkuleringsmetoden fra en etterkalkuleringsmetode som er basert på gjennomsnittskostnad eller standardkostnad til en metode som er basert på glidende gjennomsnitt. 

Hvis du endrer etterkalkuleringsmåten fra standard etterkalkuleringsmetode til metode for glidende gjennomsnitt, må du utføre følgende oppgaver:

1.  Gjør justeringer for å få lagerantall og -verdier ned i 0 (null).
2.  Når lagerverdien og -antallet er 0 (null), kan du endre varemodellgruppen til glidende gjennomsnitt.
3.  Gjør justeringer for å få antallet og verdien tilbake til lager.

Du kan ikke endre lageretterkalkuleringsmetoden fra en metode for glidende gjennomsnitt til metoden først inn, først ut (FIFO), sist inn, først ut(LIFO) eller en metode for avveid gjennomsnitt.

**Obs!** Konvertering fra standard kost til glidende avveid gjennomsnitt er en manuell prosess.

Eksemplene nedenfor viser virkningene når etterkalkuleringsmetoden for glidende gjennomsnitt brukes. Det finnes fire konfigurasjoner:
-   Differanse mellom bestilling og proporsjonalt utgiftsført kostnad
-   Justering av produkt og lager for glidende gjennomsnitt
-   Glidende gjennomsnitt med produksjon
-   Glidende gjennomsnitt med en tilbakedatert transaksjon

## <a name="purchase-order-and-proportionally-expensed-cost-difference"></a>Differanse mellom bestilling og proporsjonalt utgiftsført kostnad
Produktkostnaden bestemmes av kjøpsmottaket med glidende gjennomsnitt. Når innkjøpsfakturaen posteres, hvis det er en forskjell i kostnad mellom kjøpsmottaket og innkjøpsfakturaen, justeres forskjellen proporsjonalt for de gjeldende produktene på lager, og eventuelle gjenstående beløp utgiftsføres. 

I dette eksemplet opprettes og mottas en bestilling med én kostnad, og innkjøpsfakturaen posteres med en annen kostnad.

1.  Opprett en bestilling for et antall på 2 og en enhetspris på 10,00.
2.  Opprett et kjøpsmottak for produktet.
3.  Opprett en salgsordre for et antall på 1 og en enhetspris på 10,00.
4.  Opprett en kjøpsordre for et antall på 2 og en enhetspris på 12,00.

Forskjellen i enhetsprisen, 2,00, posteres til kontoen Prisdifferanse for glidende gjennomsnitt når innkjøpsfakturaen posteres. Grunnen er at to produkter ble kjøpt med en kostnad på 20,00. Ett av produktene ble solgt til en enhetspris på 10,00. Kjøpsfakturaen ble postert til en enhetspris på 12,00 med et antall på 2. Salgsprisen for produktet kan ikke posteres på 14,00.

## <a name="moving-average-product-and-inventory-adjustment"></a>Justering av produkt og lager for glidende gjennomsnitt
Hvis du vil justere den glidende gjennomsnittskostnaden for et produkt, er det tillatt med lagerjusteringer per dagens dato. Du kan ikke tilbakedatere en lagerjustering for å rette opp den glidende gjennomsnittskostnaden for et produkt. Du kan ikke ha kostnadsflyten gjennom etterfølgende transaksjoner. 

I dette eksemplet justeres den glidende gjennomsnittskostnaden til et produkt.

1.  Velg produktet som du vil justere den glidende gjennomsnittskostnaden for. **Obs!** Siden **Revaluering for glidende gjennomsnitt** undersøker lageret som er tilgjengelig for et produkt. Det valgte produktet har et postert antall på 1, en postert verdi på 12,00, en postert enhetskostnad på 12,00 og en enhetskostnad på 12,00.
2.  Oppdater feltet **Enhetskostnad** til 16,00. Systemet beregner de gjenværende feltene.
3.  Justeringen posteres.

**Obs!** Du kan bare justere den glidende gjennomsnittskostnaden per dagens dato.

På siden **Utligninger på bilag** kan du se en justering på 4,00 postert til kontoen Revaluering av kostnad for glidende gjennomsnitt.

## <a name="moving-average-with-production"></a>Glidende gjennomsnitt med produksjon
Glidende gjennomsnitt støtter produserte varer. Hvis du planlegger å bruke glidende gjennomsnitt i et produksjonsmiljø, bør du merke av for **Bruk estimert kostpris** på siden **Parametere for produksjonskontroll**. Dette betyr at kostprisen som blir beregnet under forhåndsberegning, brukes i stedet for den faktiske kostprisen for stykklisteberegningen.

## <a name="moving-average-with-a-backdated-transaction"></a>Glidende gjennomsnitt med en tilbakedatert transaksjon
Tilbakedaterte transaksjoner tilordnes den gjeldende, glidende gjennomsnittskostnaden, og produktets fysiske antall oppdateres, men produktets glidende gjennomsnittskostnad påvirkes ikke. I dette eksemplet med glidende gjennomsnitt posteres en tilbakedatert transaksjon for et glidende gjennomsnittsprodukt.

1.  Opprett en lagerjustering for det glidende gjennomsnittsproduktet for et antall på 1 og en kostnad på 20,00.
2.  Lagertransaksjonsloggen for produktet vil ligne på følgende:
    -   En lagertransaksjon på 1, en kostnad på 16,00, en posteringsdato lik 15. januar og en transaksjonsdato lik 15. januar.
    -   En lagerjustering på 1, en kostnad på 20,00, en posteringsdato lik 1. januar og en transaksjonsdato lik 15. januar.
3.  Poster justeringen.

På **Lagertransaksjoner**-siden kan du se at 4,00 er utgiftsført da det gjeldende glidende gjennomsnittet for produktet er 16,00. Du kan postere i fortiden, men forskjellen i kostnad utgiftsføres, så den glidende gjennomsnittskostnaden påvirkes ikke.

## <a name="inventory-value-report"></a>Rapport for lagerverdi
I dette eksemplet med glidende gjennomsnitt skrives lagerverdirapporten ut for å støtte gjeldende glidende gjennomsnittsberegning for et produkt. Rapporten Lagerverdi kan skrive ut transaksjonene i kronologisk rekkefølge, sammen med kostnaden for å støtte den glidende gjennomsnittskostnadsberegningen av et produkt. Rapporten viser den glidende gjennomsnittskostnaden for produktet. I dialogboksen **Lagerverdirapporter** lar et datointervall deg velge **Transaksjonstidspunkt** eller **Posteringsdato** som du kan sortere rapporten etter. **Posteringsdato**-alternativet er slik rapporten vanligvis skrives ut. **Transaksjonstidspunkt**-alternativet er den faktiske datoen da transaksjonen rapporteres og den glidende gjennomsnittskostnaden for produktet oppdateres. Du kan skrive ut rapporten Lagerverdi ved hjelp av alternativet **Sortering etter transaksjonstidspunkt** hvis du vil se beregningen av glidende gjennomsnittskostnad over tid. Tabellen nedenfor viser transaksjonene for produktet som rapporten skrives ut for, når alternativet **Sortering etter transaksjonstidspunkt** brukes.

| Transaksjonstidspunkt | Dato         | transaksjonstype           | Antall | Beløp | Gjennomsnittlig enhetskostnad |
|------------------|--------------|----------------------------|----------|--------|-------------------|
|                  | 1. oktober    | Startsaldo          | 0        | 0,00   | 0,00              |
| 8. oktober        | 28. september | Tilbakedatert mottak          | 1        | 16,00  | 16,00             |
| 3. oktober        | 3. oktober    | Kjøpsmottak           | 2        | 20,00  | 12,00             |
| 5. oktober        | 5. oktober    | Salgsordre                | -1       | -10,00 | 13,00             |
| 7. oktober        | 7. oktober    | Innkjøpsfaktura           |          | 2,00   | 14,00             |
| 8. oktober        | 8. oktober    | Revaluering for glidende gjennomsnitt |          | 4,00   | 16,00             |
|                  | 31. oktober   | Sum                      | 2        | 32,00  | 16,00             |

 **Obs!** Du kan ikke avstemme økonomi med lager ved hjelp av **Sortering etter transaksjonstidspunkt**. Rapporten må skrives ut ved hjelp av **Posteringsdato**-alternativet.






