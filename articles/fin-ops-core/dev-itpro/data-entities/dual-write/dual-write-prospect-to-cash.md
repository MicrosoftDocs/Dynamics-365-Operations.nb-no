---
title: Kundeemne til kontanter i dobbel skriving
description: Dette emnet inneholder informasjon om kundeemne til kontanter i dobbel skriving.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 01/27/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-01-27
ms.openlocfilehash: 249fde6f7bba5d6e0bc6cfde62fd792dee3f1301
ms.sourcegitcommit: 48c39c0c0949fe48b3536d9d2d0e451d561ff5c6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/09/2020
ms.locfileid: "3112492"
---
# <a name="prospect-to-cash-in-dual-write"></a>Kundeemne til kontanter i dobbel skriving

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

Et viktig mål for de fleste bedrifter er å konvertere kundeemner til kunder, og deretter opprettholde et løpende forretningsforhold med disse kundene. I Microsoft Dynamics 365-apper inntreffer kundeemne til kontanter-prosessen gjennom tilbud eller arbeidsflyter for ordrebehandling, og finansene avstemmes og føres. Integrering av kundeemne til kontanter med dobbel skriving oppretter en arbeidsflyt som tar et tilbud og en ordre som kommer fra enten Dynamics 365 Sales eller Dynamics 365 Supply Chain Management, og gjør tilbudet og ordren tilgjengelig i begge appene.

I app-grensesnittene kan du få tilgang til behandlingsstatusene og fakturainformasjonen i sanntid. Derfor er det enklere å administrere funksjoner som produktlagring, lagerhåndtering og oppfyllelse i Supply Chain Management, uten å måtte opprette tilbudene og ordrene på nytt.

![Dataflyt for dobbel skriving i kundeemne til kontanter](../dual-write/media/dual-write-prospect-to-cash[1].png)

## <a name="prerequisites-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

Før du kan synkronisere salgstilbud, må du oppdatere følgende innstillinger.

### <a name="setup-in-sales"></a>Oppsett i salg

I Sales går du til **Innstillinger \> Administrasjon \> Systeminnstillinger \> Salg**, og sørger for å bruke følgende innstillinger:

- Alternativet **Bruk systemets priskalkuleringssystem** er satt til **Ja**.
- Feltet **Rabattkalkuleringsmetode** er satt til **Linjeelement**.

### <a name="sites-and-warehouses"></a>Områder og lagre

I Supply Chain Management kreves **Område**- og **Lager**-feltene for tilbudslinjer og ordrelinjer. Hvis du angir området og lageret i standard ordreinnstillinger, blir disse feltene automatisk definert når du legger til et produkt i en tilbudslinje eller en ordrelinje. 

### <a name="number-sequences-for-quotations-and-orders"></a>Nummerserier for tilbud og ordrer

Nummerseriene for Supply Chain Management og Sales er ikke tilkoblet når tilbud og ordrer opprettes og synkroniseres i Sales og Supply Chain Management. Hvis en salgsordre som er opprettet i Sales, blir synkronisert til Supply Chain Management, har den samme salgsordrenummeret i Supply Chain Management. For å sikre at salgsordrenummeret ikke dupliseres, må du bruke andre nummerseriesystemer i de to appene.

Nummerserien i Supply Chain Management er for eksempel **1, 2, 3, 4, 5, ...**, og nummerserien i Sales er **100, 99, 98, ...**. Hvis du oppretter 100 salgsordrer i Sales, blir det generert et ordrenummer som allerede finnes i Supply Chain Management. Med andre ord vil de to nummerseriene overlappes etter hvert som salgsordrene opprettes i Supply Chain Management og Sales. I stedet kan du bruke en nummerserie som **F1, F2, F3, ...** i Supply Chain Management og en nummerserie som **C1, C2, C3, ...** i Sales. Disse nummerseriene vil aldri generere dupliserte salgsordrenumre.

## <a name="sales-quotations"></a>Salgstilbud

Salgstilbud kan opprettes i både Sales og Supply Chain Management. Hvis du oppretter et tilbud i Sales, blir det synkronisert til Supply Chain Management i sanntid. Tilsvarende, hvis du oppretter et tilbud i Supply Chain Management, blir det synkronisert til Sales i sanntid. Merk følgende punkt:

+ Du kan legge til en rabatt i produktet på tilbudet. I dette tilfellet blir rabatten synkronisert til Supply Chain Management. Feltene **Rabatt**, **Gebyrer** og **Avgift** feltene på hodet kontrolleres av et oppsett i Supply Chain Management. Dette oppsettet støtter ikke integreringstilordning. I stedet vedlikeholdes og behandles feltene **Pris**, **Rabatt**, **Gebyrer** og **Avgift** i Supply Chain Management.
+ Feltene **Rabattprosent**, **Rabatt** og **Fraktbeløp** i salgstilbudshodet er skrivebeskyttet.
+ Feltene **Fraktvilkår**, **Betalingsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke en del av standardtilordningene. Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.

## <a name="sales-orders"></a>Salgsordre

Salgsordrer kan opprettes i både Sales og Supply Chain Management. Hvis du oppretter en salgsordre i Sales, blir den synkronisert til Supply Chain Management i sanntid. Tilsvarende, hvis du oppretter en salgsordre i Supply Chain Management, blir den synkronisert til Sales i sanntid. Merk følgende punkt:

+ Du kan bare aktivere og synkronisere ordrer fra Sales hvis alle produkter i ordren kommer fra Finance and Operations-apper. Det kan derfor ikke finnes innskrivingsprodukter.
+ Rabattberegning og -avrunding:

    - Modellen for rabattberegningen i Sales er forskjellig fra modellen for rabattberegningen i Supply Chain Management. I Supply Chain Management kan det endelige rabattbeløpet på en salgslinje være resultatet av en kombinasjon av rabattbeløp og rabattprosenter. Hvis dette endelige rabattbeløpet deles på antallet på linjen, kan det forekomme avrunding. Denne avrunding blir imidlertid ikke tatt hensyn til hvis et avrundet per enhet-rabattbeløp synkroniseres til Sales. For å sikre at hele rabattbeløpet fra en salgslinje i Supply Chain Management synkroniseres riktig med Sales, må hele beløpet synkroniseres uten at det blir delt på linjeantallet. Derfor må du definere rabattkalkuleringsmetoden som **Linjeelement** i Sales.
    - Når en salgsordrelinje synkroniseres fra Sales til Supply Chain Management, brukes hele linjerabattbeløpet. Supply Chain Management har ingen felt som kan lagre fullstendige rabattbeløpet for en linje, og beløpet deles derfor på antallet og lagres i feltet **Linjerabatt**. Avrunding som forekommer under denne delingen, lagres i feltet **Salgstillegg** på salgslinjen.

### <a name="example-synchronization-from-sales-to-supply-chain-management"></a>Eksempel: Synkronisering fra Sales til Supply Chain Management

Du har følgende salgsordre:

+ **Sales**: Antall = 3, per linjerabatt = $ 10,00
+ **Supply Chain Management:** Antall = 3, linjerabattbeløp = $ 3,33, salgstillegg= -$ 0,01

Hvis du synkroniserer fra Supply Chain Management til Sales, får du følgende resultat:

+ **Supply Chain Management:** Antall = 3, linjerabattbeløp = $ 3,33, salgstillegg= -$ 0,01
+ **Sales**: Antall = 3, per linjerabatt = = (3 × $ 3,33) + $ 0,01 = $ 10,00

## <a name="dual-write-solution-for-sales"></a>Løsning for dobbel skriving for Sales

Nye felt er lagt til enheten **Ordre** og vises på siden. De fleste av disse feltene vises i kategorien **Integrering** i Sales. Det finnes noen få spesielle felt:

+ Feltet **Behandlingsstatus** viser behandlingsstatus for en ordre i Supply Chain Management. Dette feltet er låst, og viser bare statusen for ordren fra Supply Chain Management. Følgende verdier er tilgjengelige:

    + **Aktiv** – Status etter at ordren er aktivert i Sales ved hjelp av **Aktiver**-knappen.
    + **Bekreftet**
    + **Levert**
    + **Fakturert**
    + **Delvis levert**
    + **Delvis fakturert**
    + **Plukket**
    + **Annullert**

    Følgende tabell viser hvordan behandlingsstatusen er tilordnet til verdien **CRM-statuskode**.

    | Behandlingsstatus           | CRM-statuskode    |
    |-----------------------------|--------------------|
    | Aktivt                      | Ny/ventende/på vent |
    | Bekreftet/plukket            | Pågår        |
    | Delvis levert         | Delvis            |
    | Levert                   | Komplett           |
    | Fakturert/delvis fakturert | Fakturert           |
    | Annullert                    | Ingen penger           |

+ Knappene **Opprett faktura** og **Avbryt ordre** på **Salgsordre**-siden er skjult i Sales.
+ **Salgsordrestatus**-verdien vil fortsatt være **Aktiv** for å sikre at endringer fra Supply Chain Management kan flyte fra salgsordren i Sales. Dette kontrolleres ved å sette standardverdien **Statuskode \[Status\]** til **Aktiv**.

## <a name="invoices"></a>Fakturaer

Salgsfakturaer er opprettet i Supply Chain Management og synkronisert til Sales. Merk følgende punkt:

+ Et **Fakturanummer**-felt er lagt til **Faktura**-enheten og vises på siden.
+ Knappen **Opprett faktura** på siden **Salgsordre** er skjult fordi fakturaer vil opprettes i Supply Chain Management og synkroniseres til Sales. Siden **Faktura** kan ikke redigeres fordi fakturaer vil synkroniseres fra Supply Chain Management.
+ **Salgsordrestatus**-verdien endres automatisk til **Fakturert** når relaterte fakturaer fra Supply Chain Management er synkronisert til Sales. Eieren av salgsordren som fakturaen ble opprettet fra, tildeles også som eier av fakturaen. Eieren av salgsordren kan derfor vise fakturaen.
+ Feltene **Fraktvilkår**, **Leveringsbetingelser** og **Leveringsmåte** er ikke inkludert i standardtilordningene. Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.

## <a name="templates"></a>Maler

Kundeemne til kontanter inkluderer en samling enhetstilordninger for viktige områder som fungerer sammen under datasamhandling, som vist i følgende tabell.

| Finance and Operations-apper | Modelldrevne apper i Dynamics 365 | beskrivelse |
|-----------------------------|-----------------------------------|-------------|
| Salgsfakturahoder V2    | fakturaer                          |             |
| Salgsfakturalinjer V2      | invoicedetails                    |             |
| CDS-salgsordrehoder     | salesorders                       |             |
| CDS-salgsordrelinjer       | salesorderdetails                 |             |
| Koder for salgsordregrunnlag    | msdyn\_salesorderorigins          |             |
| CDS-salgstilbudshode  | tilbud                            |             |
| CDS-salgstilbudslinjer   | quotedetails                      |             |

Her er relaterte kjerneenhetstilordninger for kundeemne til kontanter:

+ [Kunder V3 til kontoer](customer-mapping.md#customers-v3-to-accounts)
+ [CDS-kontakter V2 til kontakter](customer-mapping.md#cds-contacts-v2-to-contacts)
+ [Kunder V3 til kontakter](customer-mapping.md#customers-v3-to-contacts)
+ [Frigitte produkter V2 til msdyn_sharedproductdetails](product-mapping.md#released-products-v2-to-msdyn_sharedproductdetails)
+ [Alle produkter til msdyn_globalproducts](product-mapping.md#all-products-to-msdyn_globalproducts)
+ [Prisliste](product-mapping.md)

[!include [symbols](../../includes/dual-write-symbols.md)]

[!include [sales invoice](includes/SalesInvoiceHeaderV2Entity-invoice.md)]

[!include [sales invoice line](includes/SalesInvoiceLineV2Entity-invoicedetail.md)]

[!include [sales order header](includes/SalesOrderHeaderCDSEntity-salesorder.md)]

[!include [sales order line](includes/SalesOrderLineCDSEntity-salesorderdetails.md)]

[!include [sales order origin](includes/SalesOrderOriginEntity-msdyn-salesorderorigin.md)]

[!include [sales quotation header](includes/SalesQuotationHeaderCDSEntity-quote.md)]

[!include [sales quotation line](includes/SalesQuotationLineCDSEntity-QuoteDetails.md)]
