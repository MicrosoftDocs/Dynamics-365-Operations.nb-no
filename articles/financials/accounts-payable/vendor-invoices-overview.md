---
title: "Oversikt over leverandørfakturaer"
description: "Denne artikkelen inneholder generell informasjon om leverandørfakturaer. Leverandørfakturaer er forespørsler om betaling for produkter og tjenester som er mottatt. Leverandørfakturaer kan representere en faktura for pågående tjenester, eller den kan være basert på bestillinger for bestemte varer og tjenester."
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 13971
ms.assetid: 0ec4dbc0-2eeb-423b-8592-4b5d37e559d3
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: de536be7b0d25a1b0f662f64a31be26dbcd10c28
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="vendor-invoices-overview"></a>Oversikt over leverandørfakturaer

[!include[banner](../includes/banner.md)]


Denne artikkelen inneholder generell informasjon om leverandørfakturaer. Leverandørfakturaer er forespørsler om betaling for produkter og tjenester som er mottatt. Leverandørfakturaer kan representere en faktura for pågående tjenester, eller den kan være basert på bestillinger for bestemte varer og tjenester. 

<a name="vendor-invoices"></a>Leverandørfakturaer
---------------

En leverandørfaktura fra en bestilling er en faktura som lages når produkter eller tjenester er mottatt i henhold til en bestilling som ble plassert hos en leverandør. Leverandørfakturaen inneholder et hode og én eller flere linjer for varer eller tjenester. En leverandørfaktura fullfører syklusen fra bestilling til produktkvittering og leverandørfaktura. 

Selv om noen leverandørfakturaer er koblet til en bestilling, kan også leverandørfakturaer inneholde linjer som ikke samsvarer med bestillingslinjer. Du kan også opprette leverandørfakturaer som ikke er knyttet til noen bestilling. Disse leverandørfakturaene kan representere pågående tjenester, for eksempel en strømregning, og du trenger ikke å referere til en bestilling når du legger dem til. 

Det finnes flere måter å angi en leverandørfaktura:

-   I leverandørfakturaregisteret kan du raskt skrive inn fakturaer som ikke refererer til en bestilling, slik at du kan avsette utgiften. Ved hjelp av journalen for godkjenning av leverandørfaktura kan du velge disse fakturaene og postere dem til leverandørsaldoen for å reversere avsetningen.
-   I leverandørfakturajournalen kan du raskt skrive inn fakturaer som ikke refererer til en bestilling, i én operasjon.
-   Leverandørfakturapuljen i kombinasjon med leverandørfakturaregisteret lar deg raskt skrive inn fakturaer for å avsette utgiften. Du kan åpne de tilknyttede bestillingene senere for å postere fakturaen mot utgiftskontoen.
-   På sidene **Åpne leverandørfakturaer** og **Ventende leverandørfakturaer** kan du opprette leverandørfakturaer fra bekreftede bestillinger.

Følgende diskusjon inneholder mer informasjon om hvordan du bruker siden **Åpne leverandørfakturaer** eller **Ventende leverandørfakturaer** til å opprette en leverandørfaktura fra en bestilling.

## <a name="understanding-invoice-line-quantities"></a>Forstå fakturalinjeantall
Når du åpner en leverandørfaktura fra en tilknyttet bestilling, opprettes fakturalinjer fra bestillingen. Som standard hentes antallet fra produktkvitteringsantallet. Du kan imidlertid bruke et av følgende standardvalg:

-   **Motta nå-antall** – Bruk dette alternativet for delvise leveringer. Standardverdien i feltet **Antall** hentes fra antallfeltet **Motta nå** på innkjøpsordren.
-   **Bestilt antall** – Bruk dette alternativet for komplette forsendelser. Standardverdien i **Antall**-feltet hentes fra **Bestilt**-antallfeltet på innkjøpsordren.
-   **Registrert antall** – Bruk dette alternativet hvis varen krever registrering, som angitt på **Varemodellgrupper**-siden. Standardverdien i **Antall**-feltet er det fysiske oppdaterte antallet som er registrert.
-   **Produktkvitteringsantall** – Bruk dette alternativet hvis en produktkvittering allerede er mottatt for ordren. Standardverdien i **Antall**-feltet er hentet fra totalt antall for tilgjengelige produktkvitteringer.
-   **Registrerte antall og tjenester** – Bruk dette alternativet hvis antall som er registrert i ankomstjournaler for lagerførte varer eller varer som ikke er på lager. Dette alternativet omfatter tjenester også, uavhengig av om de er registrert.

Hvis den juridiske enheten bruker fakturakontroll, kan du vise resultatene av antallssamsvaret i **Samsvar i antall i produktkvittering**-kolonnen. Du kan også bruke **Samsvarende detaljer**-menykommando på **Gjennomgang**-fanen for å vise resultatene av antallssamsvaret.

## <a name="adding-a-line-that-wasnt-on-the-purchase-order"></a>Legger til en linje som ikke var på bestillingen.
Du kan legge til en ny linje som ikke var på bestillingen, i leverandørfakturaen. Du må velge et varenummer eller en innkjøpskategori. Du kan deretter legge til antall, priser og beløp på linjen. Linjen inkluderes bare i kontrollpolicyer for fakturatotaler.

## <a name="submitting-a-vendor-invoice-for-review"></a>Sende en leverandørfaktura til vurdering
Organisasjonen kan bruke arbeidsflyter til å administrere vurderingsprosessen for leverandørfakturaer. Det kan bli nødvendig med arbeidsflytvurdering for fakturahodet, fakturalinjen eller begge. Arbeidsflytkontrollene gjelder for hodet eller linjen, avhengig av hvor fokuset er når du klikker kontrollen. I stedet for **Poster**-knappen vises en **Send**-knapp som du kan bruke til å sende leverandørfakturaen gjennom vurderingsprosessen.

## <a name="matching-vendor-invoices-to-product-receipts"></a>Samsvare leverandørfakturaer med produktkvitteringer
Du kan angi og lagre informasjon for leverandørfakturaer, og du kan samsvare fakturalinjer med produktkvitteringslinjer. Du kan også samsvare delvist antall for en linje. 

Du kan opprette en leverandørfaktura basert på linjeelementene for produktkvittering som er mottatt til nå, selv om ikke alle varene i en bestemt bestilling er mottatt ennå. Du kan for eksempel bruke dette alternativet hvis en leverandør sender én faktura per måned som dekker alle leveringer vedkommende sendte i løpet av den måneden. Hver produktkvittering representerer en delvis eller komplett levering av varene i bestillingen. 

Når du posterer fakturaen, oppdateres **Fakturarest**-antallet for hver vare til totalantallet som er mottatt for de valgte produktkvitteringene. Hvis både **Fakturarest**-antallet og **Gjenstående levering**-antallet for alle varer på bestillingen er 0 (null), endres statusen for bestillingen til **Fakturert**. Hvis **Fakturarest**-antallet ikke er 0, endres ikke statusen for bestillingen, og flere fakturaer kan registreres på den.

Dette alternativet forutsetter at minst én produktkvittering er postert for bestillingen. Leverandørfakturaen er basert på disse produktkvitteringene og gjenspeiler antallet i dem. Finansinformasjonen for fakturaen er basert på informasjonen du angir når du posterer fakturaen.

Hvis du vil ha mer informasjon, se [Registrere leverandørfaktura og avstemme mot mottatt antall](../accounts-receivable/tasks/record-vendor-invoice-match-against-received-quantity.md).

## <a name="working-with-multiple-invoices"></a>Arbeide med flere fakturaer

Du kan arbeide med flere fakturaer samtidig og postere alle samtidig. Hvis du må opprette flere fakturaer, bruker du **Ventende leverandørfakturaer**-siden. Hvis du må postere og skrive ut flere leverandørfakturaer, bruker du fakturagodkjenningsjournalsiden. Hvis du bruker fakturagodkjenningsjournalen, må minst én produktkvittering posteres for bestillingen, og en faktura for bestillingen må posteres i en ankomstregistrering. Den økonomiske informasjonen for fakturaen kommer fra fakturaen som ble postert i registret.


Du finner mer informasjon under: 

 - [Definere leverandørfakturapolicyer](../accounts-receivable/tasks/set-up-vendor-invoice-policies.md) 

 - [Registrere fakturadata i Leverandører ved hjelp av en leverandørfaktura](tasks/key-invoice-data-ap-system-vendor-invoice.md)
 
 - [Registrere fakturadata i Leverandører ved hjelp av en godkjenningsjournal](tasks/key-invoice-data-into-ap-system-approval-journal.md)
  
 - [Registrere fakturadata i AP-systemet ved hjelp av fakturapulje](tasks/key-invoice-data-into-ap-system-invoice-pool.md)
 
 - [Registrere en leverandørfaktura i fakturajournalen](tasks/record-vendor-invoice-invoice-journal.md)


