---
title: Lagerposteringsprofiler
description: Denne artikkelen gir en oversikt over lagerposteringsprofiler.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 24651
ms.assetid: cb82245e-8c02-429c-b36e-8db0e3e6f7e5
ms.search.region: Global
ms.author: raprofit
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cae5b39ef8e6e153fe522dee1874deae2a2cb86e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8901349"
---
# <a name="inventory-posting-profiles"></a>Lagerposteringsprofiler

[!include [banner](../includes/banner.md)]

Lagerposteringsprofiler styrer postering av transaksjoner for underfinans for beholdning til økonomimodulen. Transaksjoner for underfinans for beholdning kan genereres fra mange moduler, blant annet **salg og markedsføring**, **Innkjøp og leverandører**, **Produksjonskontroll** og mer. Transaksjoner for underfinans for lager kan posteres hver gang en vare brukes i en salgsordre eller bestilling. 

Flere transaksjoner for underfinans for beholdning kan posteres:
- Hver gang et dokument blir oppdatert.
- Når en følgeseddel for salgsordre eller faktura posteres.
- Når et produktmottak eller en faktura for en bestilling genereres.

Hvis du vil ha mer informasjon, kan du gå til underfinanstransaksjoner for lager.

## <a name="inventory-transaction-overview"></a>Oversikt over lagertransaksjon

Hver transaksjon for underfinans for lager inneholder:
 - Antall 
 - Pris 
 - Nettsted 
 - Lager 
 - Plassering 

Transaksjoner for underfinans for lager oppretter to oppføringer i økonomimodulen ved hjelp av den fysiske posteringen og den økonomiske posteringen. Hvis du vil ha mer informasjon, kan du gå til [Fysiske og økonomiske oppdateringer](/supply-chain/cost-management/physical-financial-updates.md).
Følgende eksempel er en bestilling med tre linjer. La oss si at hele ordren gjelder ett enkelt område og lager. Hver bestillingslinje har en enkelt relatert InventTrans-post – også kalt en lagertransaksjon – og hver linje har et antall på 10. Diagrammet nedenfor viser forholdet for ett bestillingshode til tre bestillingslinjer, hver med én InventTrans-post.

![Relasjonsdiagram for en bestilling med tre linjer hver med én InventTrans-post.](./media/InventTransRelationship.PNG)

Et antall på 5 mottas på den første bestillingslinjen. Det fullstendige antallet for den andre linjen og ingen mottatt antall på den tredje linjen i bestillingen. Det er nå en ny lagertransaksjon relatert til den første bestillingslinjen. Transaksjonen for den andre bestillingslinjen oppdateres til **Mottatt**, og den tredje transaksjonen vil forbli den samme. Diagrammet nedenfor viser forholdet med den ekstra InventTrans-posten for bestillingslinje 1.

![Relasjonsdiagram for en bestilling med tre linjer. Én linje mottas delvis, og viser to InventTrans-poster.](./media/InventTransRelationshipPartialReceipt.PNG)

I dette eksemplet posteres et bilag til økonomimodulen. Dette er det fysiske bilaget. Varemodellgruppen er konfigurert til å postere lagertelling, og alle varene bruker samme varemodellgruppe. Lagerposteringsprofilen bruker et enkelt sett med hovedkontoer. Det opprettes et enkelt bilag, og InventTrans-posten vil koble både InventTrans 1 og InventTrans 2 til det samme bilaget.

Deretter mottas det en faktura for antallet som mottas på linje 1 og 2. Et annet bilag opprettes i økonomimodulen. Dette er finansbilaget. Varemodellgruppen konfigureres til Poster økonomisk lager. Det nye andre bilaget er knyttet til InventTrans 1 og InventTrans 2.

Det kan finnes en tredje finanspostering for lagerunderregnskapstransaksjonene i forbindelse med lukking og utligning av lageret, avhengig av etterkalkuleringsmodellen. For mer informasjon, se [Lagerlukking](/supply-chain/cost-management/inventory-close.md). Du kan vise detaljene for alle lagertransaksjoner ved å gå til **Beholdningsstyring** > **Forespørsler og rapporter** > **Transaksjoner**.

>[!Important]
> Lagertransaksjonene deles for hver unike kombinasjon av lagerdimensjoner og for hver deloppdatering. Dette ble vist i forrige eksempel for delvise oppdateringer.

### <a name="split-inventory-based-on-inventory-dimension-example"></a>Dele lager basert på eksempel på lagerdimensjon

Bestillingslinje 3 i eksemplet er en serialisert vare. Ti serienumre registreres for bestillingen under mottaksprosessen. Lagertransaksjonen blir delt inn i 10 lagertransaksjoner. Diagrammet nedenfor viser relasjonen og flere lagertransaksjoner, der hver har et eget serienummer relatert til bestillingslinje 3.

![Relasjonsdiagram for en bestilling med tre linjer. Én linje er serialisert og viser flere InventTrans-poster](./media/InventTransRelationshipSerialNumber.PNG)

Hvis hvert serienummer mottas på ett enkelt produktmottak i eksemplet over, opprettes det ett ekstra bilag. Det fysiske bilagsfeltet blir koblet til hvert serienummer. Det samme gjelder for den økonomiske oppdateringen når du fakturerer bestillingen.

## <a name="inventory-transactions"></a>Lagertransaksjoner

Du kan vise lagertransaksjoner på lagertransaksjonssiden på siden **Lagertransaksjoner** under **Lagerstyring** eller **Kostnadsstyring**. Du kan også vise lagertransaksjoner relatert til en bestemt kildedokumentlinje, for eksempel en bestillingslinje eller salgsordrelinje, ved å velge **Lager** og deretter velge **Transaksjoner**. 

Siden **Lagertransaksjoner** inneholder følgende felt.

| Felt            | Beskrivelse                                 |
|------------------|------------------------------------------------------------------------------------------------------------------------------------------------|
| Varenummer      | Varenummeret som er relatert til transaksjonen.                                                                  |
| Fysisk dato    | Datoen når beholdningen ankommer til lageret, går ut av lageret, blir forbrukt i produksjon eller blir produsert. For eksempel posteringsdatoen på
følgeseddelposteringen for en salgsordre eller av produktmottaksposteringen for en bestilling.                             |
| Økonomisk dato   | Datoen da lagertransaksjonen lukkes og kostnaden registreres i økonomimodulen. For eksempel posteringsdatoen på fakturaen 
generering for en salgsordre eller bestilling. Oppdateringer til referansedokumentet er ikke tillatt etter at den økonomiske datoen er fylt ut. |
| Referanse        | Angir kilden til transaksjonen og dokumenttypen som vises i **Nummer**-feltet. For eksempel salgsordre, bestilling eller overføringsordremottak.                                                 |
| Tall           | Angir referanse-IDen for en transaksjon. Hvis for eksempel **Referanse**-feltet viser salgsordre, viser **Nummer**-feltet salgsordrenummeret.                                                       |
| Mottak (status) | For lagertransaksjoner som er mottak, angir dette feltet statusen for mottaket. En bestilling er for eksempel et mottak, og statusen kan være **Bestilt** eller **Kjøpt**.                                                            |
| Avgang (status)   | For lagertransaksjoner som er avganger, angir dette feltet statusen for avgangen. En salgsordre er for eksempel en avgang, og statusen kan være **I ordre** eller **Solgt**.                         |
| Antall         | Antallet av lagertransaksjonen. Positive tall brukes for mottak til lager, mens negative tall brukes for avganger fra lageret.                                                                                                                          |
| Enhet             | Måleenheten som antallet uttrykkes i.                                                                                   |
| Faktisk vekt-antall      | Faktisk vekt-antall for transaksjonen. Hvis du vil ha mer informasjon, kan du gå til [Om faktisk vekst-varer](/dynamicsax-2012/appuser-itpro/about-catch-weight-items.).       |
| Faktisk vekt-enhet          | Måleenheten for faktisk vekt som faktisk vekt-antallet uttrykkes i.                                                         |
| Kostnadsbeløp      | Endelig kostnad for lagertransaksjonen. Dette feltet fylles ut når en transaksjon oppdateres finansielt. Avhengig av etterkalkuleringsmetoden kan lagerlukkings- og justeringsprosessen oppdatere dette feltet.                            |

## <a name="inventory-status"></a>Beholdningsstatus

Hver lagertransaksjon har en status som vises enten i **Mottak**- eller **Avgang**-feltet. Feltet som brukes, avhenger av typen lagertransaksjoner. Mottak er transaksjoner som øker lageret. For eksempel en bestilling med et positivt antall eller en salgsordreretur med et negativt antall. Avganger er lagertransaksjoner som minsker lageret. For eksempel en salgsordre med et positivt antall eller en bestillingsretur med et negativt antall.

### <a name="receipt-status"></a>Tilgangsstatus

I tabellen nedenfor beskrives **Mottak**-status.

| **Tilgangsstatus** | **Beskrivelse**       |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------|
| Bestilt            | Den opprinnelige statusen til en lagertransaksjon som representerer et mottak. Dette omfatter bestillinger med et positivt antall, produksjonsordrer eller salgsordrereturer med et negativt antall.                                                   |
| Registrert         | Denne statusen brukes når en totrinns mottaksprosess er på plass, eller når vareankomst brukes til å angi at produktet er ankommet. Den brukes når bunke- eller serienumre "tildeles" eller registreres i ordren. Hvis du vil ha mer informasjon om vareankomst, kan du gå til [Ankomstoversikt](/supply-chain/inventory/arrival-overview.md). |
| Mottatt           | Denne statusen brukes når transaksjonen fysisk oppdateres. For en bestilling er dette når produktkvitteringen posteres. For en salgsordreretur er dette når følgeseddelen posteres.                                                                            |
| Kjøpt          | Denne statusen brukes når transaksjonen økonomisk oppdateres. For en bestilling eller salgsordreretur, er dette når fakturaen genereres.                                                                                             |

### <a name="issue-status"></a>Avgangsstatus

I tabellen nedenfor beskrives **Avgang**-status.

| **Avgangsstatus**  | **Beskrivelse**            |
|-------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| I ordre/bestilling          | Den opprinnelige statusen til en lagertransaksjon som representerer et avgang. Dette omfatter salgsordrer med et positivt antall, produksjonsordrers stykklister eller formellinjer eller salgsordrereturer med et negativt antall.                                             |
| Reservert av bestilt  | Denne lagerstatusen angir at lager reserveres mot en ordre som er opprettet, men som ennå ikke er fysisk mottatt på lageret. Når lageret mottas, oppdateres statusen automatisk til **Fysisk reservert**. Hvis du vil ha mer informasjon om reserveringer, kan du gå til [Reserver lagerantall](/supply-chain/inventory/reserve-inventory-quantities.md). |
| Fysisk reservert | Denne statusen angir at lageret er tilordnet eller reservert mot en bestemt ordre. Når lageret er reservert, er det ikke fysisk tilgjengelig for andre ordrer.                                 |
| Plukket         | Dette viser at beholdningen er plukket fra lageret. Beholdningen er fortsatt fysisk på lageret, er ikke fjernet, men har ingen tilgang til andre ordrer.  |
| Fratrukket          | Denne statusen brukes når transaksjonen fysisk oppdateres. For en salgsordre er dette når følgeseddelen posteres. For en bestillingsretur, er dette når produktmottaket posteres.                                                                      |
| Solgt              | Dette er statusen som brukes når transaksjonen økonomisk oppdateres. For en bestilling eller salgsordre, er dette når fakturaen genereres.|

Hvis du vil ha mer informasjon om lagertransaksjoner, kan du gå til [Detalj om lagertransaksjoner](/supply-chain/inventory/inventory-transactions-details.md).

## <a name="configure-an-inventory-posting-profile"></a>Konfigurere en beholdningsposteringsprofil

For å konfigurere en beholdningsposteringsprofil, følger du disse trinnene:

1.  Åpne **Lagerstyring** > **Oppsett** > **Postering** > **Postering**.
2.  Velg kategorien for typen transaksjon. Velg for eksempel **Bestilling**.
3.  Velg alternativknappen for posteringstypen. Velg for eksempel **Innkjøpsutgift for utgift**.
4.  Velg **Ny**.
5.  I feltet **Varekode** velger du et alternativ for **Tabell**, **Gruppe** eller **Alle** eller **Kategori**. Hvis du for eksempel vil konfigurere en posteringsprofil for en bestemt varegruppe, velger du **Gruppe**.
     - Hvis du valgte **Tabell** i trinn 5, velger du det spesifikke Varenummer for posteringsprofilen i feltet **Varerelasjon**.
     - Hvis du valgte **Gruppe** i trinn 5, velger du den spesifikke **Varegruppe** for posteringsprofilen i feltet **Varerelasjon**.
     - Hvis du valgte **Alle** i trinn 5, blir feltet **Varerelasjon** stående tomt.
     - Hvis du valgte **Kategori** i trinn 5, blir feltet **Varerelasjon** stående tomt. Bruk feltet **Kategorirelasjon** til å velge kategorien som posteringsprofilen gjelder for.

6.  Velg et alternativ for **Tabell**, **Gruppe** eller **Alle** i **Kontokode**-feltet. Hvis du for eksempel vil bruke posteringsprofilen på alle leverandører, velger du **Alle**.
     - Hvis du valgte **Tabell** i trinn 5, velger du det spesifikke leverandørnummer for posteringsprofilen i feltet **Kontorelasjon**.
     - Hvis du valgte **Gruppe** i trinn 5, velger du den spesifikke leverandørgruppe for posteringsprofilen i feltet **Kontorelasjon**.
     - Hvis du valgte **Alle** i trinn 5, blir feltet **Kontorelasjon** stående tomt.

7.  Hvis du vil tilknytte en bestemt avgiftsgruppe som har den valgte posteringstypen, velger du en **Merverdiavgiftsgruppe**. Hvis du lar dette feltet stå tomt, gjelder posteringstypen alle eksisterende avgiftsgrupper. Posteringer som er angitt for avgiftsgrupper, gjelder bare transaksjoner for salg og kjøp.
8.  Angi kontonummeret for å postere kontotype til feltet **Hovedkonto**. Hvis du ikke allerede har opprettet et kontonummer som skal brukes som regnskapstype, kan du opprette en ny konto. Du oppretter en ny konto på siden **Detaljer om hovedkonto** i økonomimodulen.

## <a name="additional-resources"></a>Tilleggsressurser

Hver kategori på siden for **Lagerposteringsprofil** er knyttet til en underfinans i Dynamics 365 Supply Chain Management. Hvis du vil ha mer informasjon, kan du gå til:
-   [Salgsordrepostering](sales-order-posting.md)
-   [Bestillingspostering](purchase-order-posting.md)
-   [Lagerpostering](inventory-posting.md)
-   [Postering for produksjonskontroll](production-posting.md)
-   [Avvik i standardkostnad, postering](standard-cost-variance-posting.md)
