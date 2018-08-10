---
title: Definere forsendelse
description: Dette emnet forklarer hvordan du bruker prosesser for innkommende forsendelseslager.
author: perlynne
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: ConsignmentDraftReplenishmentOrderJournal, ConsignmentProductReceiptLines, ConsignmentReplenishmentOrder, ConsignmentVendorPortalOnHand, InventJournalOwnershipChange, InventOnHandItemListPage, PurchTable, PurchVendorPortalConfirmedOrders, DirPartyTable, EcoResTrackingDimensionGroup, InventJournalName, InventOwner, InventTableInventoryDimensionGroups, VendTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 220834
ms.assetid: 3c9d6de4-45d4-459a-aef7-0d9ad2c22b3a
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: df5862a75646976d315fa77531d7c4fe9b1ec499
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-consignment"></a>Definere forsendelse

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du bruker prosesser for innkommende forsendelseslager.

Forsendeleslager er lager som eies av en leverandør, men lagres på ditt område. Når du er klar til å forbruke eller bruke lageret, kan du ta over eierskapet for lageret. Dette emnet inneholder informasjon om hvordan du fysisk mottar leverandøreid lagerbeholdning uten å opprette transaksjoner fra økonomimodulen, hvordan du starter en produksjonsprosess der leverandøreid lagerbeholdning kan reserveres fysisk , og hvordan du endrer eierskap for råvarer for å kunne behandle forbruket som en del av behandlingen av produksjonsordre. Det inneholder også informasjon om hvordan leverandører kan overvåke forbruk av lagerbeholdningen ved hjelp av grensesnittet for leverandørsamarbeid. 

## <a name="overview-of-the-consignment-process"></a>Oversikt over forsendelsesprosessen
Dette eksemplet har firmaet USMF en forsendelsesavtale med leverandøren US-104 for råvaren M9211CI.

1.  En etterfyllingsordre for forsendelse opprettes manuelt av en person i USMF, basert på det forventede behovet. Ordren opprettes for leverandøren UA-104, og det legges til en linje for varen MS9211CI.
2.  Leverandøren blir informert om den forventede leveringen. Dette kan skje på én av tre måter:
    -   De som arbeider hos USMF sender ordreinformasjonen til leverandøren.
    -   Leverandøren kan overvåke den forventede lagerbeholdningen ved hjelp av grensesnittet for leverandørsamarbeid.
    -   De som arbeider hos USMF filtrerer dataene på **Lagerbeholdning**-siden for å vise bare postene for leverandøren US-104 der mottaksstatusen er **Bestilt**, og de sender deretter denne informasjonen til leverandøren.
3.  Beholdningen leveres fra US-104 til USMF.
4.  Når materialet kommer frem til USMF, oppdateres etterfyllingsordren for forsendelsen med en produktkvittering. Bare det fysiske antallet for den leverandøreide lagerbeholdningen registreres. Det opprettes ingen økonomitransaksjoner fordi lageret fortsatt eies av leverandøren.
5.  Leverandøren overvåker oppdateringer for den fysiske lagerbeholdningen ved hjelp av siden **Forsendelseslager for beholdning**.
6.  Nå som det fysiske lageret er i beholdningen, reserverer produksjonsprosessen den leverandøreide beholdningen og starter produksjonsordren for de ferdige varene som skal bruke råvaren M9211CI.
7.  Eieren av de reserverte råvarene som skal forbrukes i dagens produksjonen, endres fra US-104 til USMF. Dette gjøres ved hjelp av en endringsjournal for lagereierskap. Denne prosessen oppretter bestillinger der **Opprinnelse**-feltet settes til **Forsendelse**.
8.  Leverandøren overvåker forbruket (endring i eierskap) på siden **Produkter mottatt fra forsendelseslager**, og utsteder en faktura basert på avtalene mellom de to firmaene.
9.  Produksjonsprosessen bruker råvaren via en plukkliste for produksjon. Den fysiske reservasjonen oppdateres automatisk for å gjenspeile at lagerbeholdningen eies av USMF.
10. Fakturaen fra US-104 behandles mot bestillingene som ble generert automatisk da endringsjournalen for lagereierskap ble behandlet. Utbetaling gjøres til leverandøren US-104 for beholdningen som ble brukt.

USMF utfører flere regelmessige prosesser:

-   Den fysiske flyttingen av leverandøreid lagerbeholdning mellom andre lagre behandles ved hjelp av en overføringsjournal.
-   Den fysiske lagerbeholdningen blir oppdatert ved hjelp av en **Vareopptelling**-journal. Telling kan også brukes av leverandøren for å oppdatere lagerbeholdningen, hvis de har tillatelse til å gjøre dette.

Leverandøren, US-104, kan overvåke oppdateringer ved hjelp av siden **Forsendelseslager for beholdning**.

## <a name="consignment-replenishment-orders"></a>Etterfyllingsordrer for forsendelse
En etterfyllingsordre for forsendelse er et dokument som brukes til å be om og holde oversikt over lagerantall av produkter som en leverandør har til hensikt å levere innenfor et bestemt datointervall ved å opprette bestilte lagertransaksjoner. Dette baseres vanligvis på prognose og faktisk etterspørsel av bestemte produkter. Lagerbeholdningen som skal mottas mot etterfyllingsordre for forsendelse forblir i leverandørens eierskap. Bare besittelse av produktene som er knyttet til oppdateringen av det fysiske mottaket registreres, og derfor utføres ingen økonomimodultransaksjoner. 

**Eier**-dimensjonen brukes til å skille informasjon om hvilken lagerbeholdning som eies av leverandøren og hvilken som eies av den juridiske enheten for mottak. Etterfyllingsordrelinjer for forsendelse har statusen **Åpen ordre** så lenge det fullstendige antallet linjer ikke er mottatt eller kansellert. Når det fullstendige antallet er mottatt eller kansellert, endres statusen til **Fullført**. Den fysiske lagerbeholdningen som er knyttet til en etterfyllingsordre for forsendelse kan registreres ved hjelp av en registreringsprosess i tillegg til en oppdateringsprosess for produktmottak. Registreringen kan utføres som del av vareankomstprosessen eller ved å oppdatere ordrelinjene manuelt. Når oppdateringsprosess for produktmottak brukes, opprettes en post i produktkvitteringsjournalen, som kan brukes til å bekrefte mottak av varer til leverandørene.

[![forsendelse-etterfylling-ordre](./media/consignment-replenishment-order.png)](./media/consignment-replenishment-order.png)

## <a name="inventory-ownership-change-journal"></a>Endringsjournal for lagereierskap
Endring av eier av lagerbeholdningen fra leverandør til den juridiske enhet av mottak, gjøres ved hjelp av en endringsjournal for lagereierskap. Ingen forventede lagertransaksjoner opprettes for journalen. De eneste lagertransaksjonene som opprettes er de som er knyttet til en postert journal. Når journalen posteres:

-   Den leverandøreide lagerbeholdningen utstedes ved hjelp av referansen **Endring av eierskap** med statusen **Solgt**.
-   Lagerbeholdningen mottas av den juridiske enheten som forbruker den, ved hjelp av ved hjelp av en mottaksseddel som oppdateres med en lagertransaksjon på bestillingen. Dette setter statusen for ordren til **Mottatt**. Bestillinger som brukes for forsendelser har **Opprinnelse**-feltet satt til **Forsendelse**.

Det er ikke mulig å oppdatere antallet på bestillingslinjene for forsendelsen når bestillingen er opprettet.

[![Endringsjournal for lagereierskap](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Leverandørsamarbeid i forsendelsesprosesser
Grensesnittet for leverandørsamarbeid har tre sider som er knyttet til prosessen for innkommende forsendelse:

-   **Bruk av forsendelseslager** **for bestillinger** – Viser detaljert bestillingsinformasjon knyttet til endring av eierskap fra forsendelsesprosessen.
-   **Produkter mottatt fra forsendelseslager** – Viser informasjon om varene og antallet som oppdateres på mottakssedler under prosessen for endring av eierskapet.
-   **Forsendelseslager for beholdning** – Viser informasjon om forsendelsesvarene som det forventes at de leverer, og varene som allerede er fysisk tilgjengelige hos kunden.

## <a name="inventory-owners"></a>Beholdningseiere
Hvis du vil registrere fysisk forsendelse for innkommende lager, må du definere en leverandøreier. Dette gjøres på siden **Lagereier**. Når du velger en **leverandørkonto**, genereres det standardverdier for feltene **Navn** og **Eier**. Verdien i **Eier**-feltet vil være synlig for leverandøren, slik at du kanskje vil endre dette hvis dine navn på leverandørkontoer ikke er enkle for eksterne brukere å gjenkjenne. Det er mulig å redigere **Eier**-feltet, men bare frem til når du lagrer posten **Lagereier**. **Navn**-feltet fylles ut med navnet på parten som leverandørkontoen som er knyttet til, og dette kan ikke endres.

[![Beholdningseiere](./media/inventory-owners.png)](./media/inventory-owners.png)

## <a name="tracking-dimension-group"></a>Sporingsdimensjonsgruppe
Varer som skal brukes i forsendelsesprosesser må være knyttet til en **sporingsdimensjonsgruppe** der **Eier**-dimensjonen er satt til **Aktiv**. Alternativene **Fysisk beholdning** og **Økonomisk lager** er alltid valgt for eierdimensjonen. **Dekningsplanlegg etter dimensjon** er aldri er valgt.

[![Sporingsdimensjonsgruppe](./media/tracking-dimension-group.png)](./media/tracking-dimension-group.png)

## <a name="inventory-ownership-change-journal"></a>Endringsjournal for lagereierskap
Journalen **Endring av lagereierskap** brukes til å registrere overføring av eierskap av forsendelseslageret fra leverandøren til den juridiske enheten som forbruker det. Det må identifiseres med et lagerjournalnavn, på samme måte som en hvilken som helst annen lagerjournal. Disse navnene opprettes på siden **Navn på lagerjournal**, og **Journaltype** må være satt til **Endring av eierskap**.

[![Endringsjournal for lagereierskap](./media/inventory-ownership-change-journal.png)](./media/inventory-ownership-change-journal.png)

## <a name="vendor-collaboration-in-consignment-processes"></a>Leverandørsamarbeid i forsendelsesprosesser
Hvis leverandørene bruker grensesnittet for leverandørsamarbeid, kan de bruke dette til å overvåke forbruket av beholdningen på området. Hvis du vil ha mer informasjon om hvordan du definerer leverandører med leverandørsamarbeid, kan du se [Konfigurere sikkerhet for brukere av leverandørsamarbeid](../procurement/configure-security-vendor-portal-users.md).






