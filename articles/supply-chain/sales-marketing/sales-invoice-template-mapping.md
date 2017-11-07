---
title: Synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales
description: "Emnet diskuterer maler og underliggende oppgaver som brukes til å synkronisere salgsfakturahoder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a>Synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales

[!include[banner](../includes/banner.md)]

Emnet diskuterer maler og underliggende oppgaver som brukes til å synkronisere salgsfakturahoder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales. 

## <a name="templates-and-tasks"></a>Maler og oppgaver

Følgende maler og underliggende oppgaver brukes til å synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales:

- **Navnet på malen i Dataintegrasjon** 

     - Salgsfaktura (Fin and Ops til Sales)

- **Navnet på oppgaven i Dataintegrasjonprosjektet**

    - SalesInvoiceHeader
    - SalesInvoiceLine

Synkroniseringsoppgaver som kreves før Salgsfakturaoverskrift og linjesynkronisering:
-   Produkter (Fin and Ops til Sales)
-   Kontoer (Sales til Fin and Ops) (hvis brukt)
-   Kontakter (Sales til Fin and Ops) (hvis brukt)
-   Salgsordrehoder og -linjer (Fin and Ops til Sales)

## <a name="entity-set"></a>Enhetssett

| Finance and Operations                               | Common Data Service (CDS)              | Salg          |
|------------------------------------------------------|------------------|----------------|
| Eksternt vedlikeholdte hoder for kundesalgsfaktura | SalesInvoice     | Fakturaer       |
| Eksternt vedlikeholdte linjer for kundesalgsfaktura   | SalesInvoiceLine | InvoiceDetails |

## <a name="entity-flow"></a>Enhetsflyt

Salgsfakturaer er opprettet i Finance and Operations og synkronisert til Sales.

> [!NOTE]
> Skatt knyttet til avgifter på **Salgsfakturahode** er for øyeblikket ikke inkludert i synkronisering fra Finance and Operations til Sales. Dette er fordi Sales ikke støtter skatteinformasjon på hodenivå. Skatterelaterte kostander på linjenivå inkluderes.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

-  Et **Fakturanummerfelt** er lagt til **Faktura**-enheten og vises på siden.
 
-  Knappen **Opprett faktura** på siden **Salgsordre** er skjult fordi fakturaer vil opprettes i Finance and Operations og synkroniseres til Sales. Siden **Faktura** kan ikke redigeres fordi fakturaer vil synkroniseres fra Finance and Operations.
 
-  **Salgsordrestatus** endres automatisk til **Fakturert** når relaterte fakturaer fra Finance and Operations er synkronisert til Sales. Også eieren av salgsordren fra hvilken fakturaen ble opprettet, er tildelt som eier av fakturaen. Dette gir eieren av salgsordren muligheten til å se fakturaen.
 
## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

Før du synkroniserer salgsfakturaer, er det viktig å oppdatere systemene med følgende innstilling:

### <a name="setup-in-sales"></a>Oppsett i Sales

- Under **Oppsett** > **Administrasjon** > **Systeminnstillinger** > **Sales**, må du forsikre deg om at **Bruk systemets priskalkuleringssystem** er satt til **Ja**. 

- Under **Oppsett** > **Administrasjon** > **Systeminnstillinger** > **Sales**, må du forsikre deg om at **Rabattkalkuleringsmetode** er satt til **Linjeelement**. 

### <a name="setup-in-the-data-integration-project"></a>Oppsett i Dataintegrasjonsprosjekt

#### <a name="salesinvoiceheader-task"></a>Salgsfakturahode-oppgave

- Oppdater tilordning for **CDS-organisasjons-ID** i **Kilde** > **CDS**. 

    -  Standard malverdi for **Salgsordre_Organisasjon_Organisasjons-ID** er ORG001.
    -  Standard malverdi for **Konto_Organisasjon_Organisasjons-ID** er ORG001.
    -  Standard malverdi for **Organisasjon_Organisasjons-ID** er ORG001.

- Forsikre deg om at nødvendig tilordning eksisterer i **Kilde** > **CDS for InvoiceCountryRegionId** til **BillingAdress_Country**.

    -  Malverdi er **ValueMap** med et antall av land tilordnet.

- **Prisliste** er nødvendig for å opprette fakturaer i Sales. Oppdater **ValueMap** i **CDS** > **-destinasjon for pricelevelid.name (Prislistenavn)** til **Prisliste** som brukes i Sales per valuta. Du kan enten bruke standard **Prisliste** for enkeltvaluta eller bruke **ValueMap** hvis du har **Prisliste** i flere valutaer.

    -  Malverdi for **pricelevelid.name (Prislistenavn)** er **ValueMap** basert på **Valuta**.
    -  usd: CRM-service USA (prøve) 

#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine-oppgave

- Forsikre deg om at nødvendig tilordning eksisterer i **Kilde** > **CDS for måleenhet**.

- Forsikre deg om at nødvendig **ValueMap** for **SalesUnitSymbol** i Finance and Operations eksisterer i **Kilde** > **CDS-tilordning**. 
    
    - Malverdi med **ValueMap** er definert for **SalesUnitSymbol til Quanitiy_UOM**.
    
-  Oppdater tilordning for **CDS-organisasjons-ID i Kilde** > **CDS**. 

    -  Standard malverdi for **Salgsfaktura_Organisasjon_Organisasjons-ID** er ORG001.
    -  Standard malverdi for **Produkt_Organisasjon_Organisasjons-ID** er ORG001.
 
## <a name="template-mapping-in-data-integrator"></a>Maltilordning i Dataintegrator

> [!NOTE]
> **Betalingsbetingelser**, **Fraktbetingelser**, **Leveringsbetingelser**, **Forsendelsesmetode**, og **Leveringsmetode** er ikke en del av standard tilordning. Tilordning av disse feltene krever at verditilordning settes opp, noe som er spesifikt for dataene i organisasjonene mellom hvilke enheten som synkroniseres.

Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.

![Tilordninge mal i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Tilordninge mal i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Tilordninge mal i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Tilordninge mal i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Relaterte emner

[Synkronisere produkter fra Finance and Operations til produkter i Sales](products-template-mapping.md)

[Synkronisere kontoer fra Sales til kunder i Finance and Operations](accounts-template-mapping.md)

[Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations](contacts-template-mapping.md)

[Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations](sales-quotation-template-mapping.md)

[Synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales](sales-order-template-mapping.md)


