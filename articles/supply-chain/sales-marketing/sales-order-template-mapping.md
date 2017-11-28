---
title: Synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales
description: "Emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgsordrehoder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a>Synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales

[!include[banner](../includes/banner.md)]

Emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgsordrehoder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales. 

## <a name="template-and-tasks"></a>Mal og oppgaver

Følgende maler og underliggende oppgaver brukes til å synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales:

- **Navn på mal i Dataintegrasjon** 

    - Salgsordrer (Fin and Ops til Sales)
    
- **Navn på oppgaver i Dataintegrasjonprosjektet**

    - OrderHeader
    - OrderLine

Synkroniseringsoppgaver som kreves før Salgsfakturaoverskrift og linjesynk:

- Produkter (Fin and Ops til Sales)
- Kontoer (Sales til Fin and Ops) (hvis brukt)
- Kontakter til Kunder (Sales til Fin and Ops) (hvis brukt)

## <a name="entity-set"></a>Enhetssett

| Finance and Operations |    Common Data Service (CDS)         |     Salg      |
|------------------------|----------------|----------------|
| CDS-salgsordrehoder| Salgsordre     | Salgsordrer |
| CDS-salgsordrelinjer  | Salgsordrelinje | Salgsordredetaljer|

## <a name="entity-flow"></a>Enhetsflyt

Salgsordrer er opprettet i Finance and Operations og synkronisert til Sales.

Filtre i malen sikrer at kun relevante salgsordrer er inkludert i synkroniseringen:

- Både bestilling og fakturering av kunde på salgsordren som kommer fra Sales vil inkluderes i synkroniseringen. I Finance and Operations er feltene **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** brukt til å spore synkroniseringen i dataenhetene.

- **Salgsordrene** i Finance and Operations må bekreftes. Kun de bekreftede salgsordrene eller salgsordrene med høyere behandlingsstatus, for eksempel, Levering eller Fakturering, synkroniseres til Sales.

- Etter at du har opprettet eller endret en salgsordre, må batchjobben **Kalkuler salgstotaler** i Finance and Operations utføres. Bare salgsordrene med salgstallene beregnet, blir synkronisert til CDS og Salg.

> [!NOTE]
> Skatt knyttet til kostnader på **Salgsordrehode** er for øyeblikket ikke inkludert i synkronisering fra Finance and Operations til Sales. Dette er fordi Sales ikke støtter skatteinformasjon på hodenivå. Skatterelaterte kostander på linjenivå inkluderes.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

Nye felt er lagt til enheten **Ordre** og vises på siden:

- **Er behandlet eksternt** – satt til **Ja** når ordren kommer fra Finance and Operations.

- **Behandlingsstatus** – brukes for å vises behandlingsstatus for en ordre i Finance and Operations. Verdier er:

    - Aktivt
    - Bekreftet
    - Følgeseddel
    - Fakturert
    - Plukket
    - Delvis plukket
    - Delvis pakket
    - Sendt
    - Delvis sendt
    - Delvis fakturert
    - Avbrutt

Innstillingen **Har eksternt behandlede produkter** brukes i andre salgsordrescenarier (fra Sales til Finance and Operation-synkronisering) for å holde oversikt over om salgsordren helt og holdent består av **eksternt behandlede produkter**, i hvilket tilfelle produkter er vedlikeholdt i Finance and Operations. Dette sikrer at du ikke prøver å synkronisere salgsordrelinjer for produkter som er ukjent for Finance and Operations.
 
Knappene **Opprett faktura**, **Avbryt ordre**, **Rekalkuler**, **Få produkter** og **Søk opp adresser** på siden **Salgsordre** er skjult for eksternt behandlede ordrer fordi fakturaer vil opprettes i Finance and Operations og synkronisert til Sales. Ordresiden er ikke redigerbar fordi salgsordreinformasjon vil synkroniseres fra Finance and Operations.
 
**Salgsordrestatus** vil fortsatt være aktiv for å sikre at endringer fra Finance and Operations kan flyte fra **Salgsordre** i Sales. Dette kontrolleres ved å sette standard **Statuskode [Status]** til **Aktiv** i Dataintegrasjonsprosjektet.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon 

Før synkronisering av salgsordre er det viktig å oppdatere systemet med følgende innstilling.

### <a name="setup-in-sales"></a>Oppsett i Sales

- Sikre tillatelser for temaet som brukeren (fra Sales **tilkoblingssett**) er tildelt til. Hvis du bruker demodata, har brukeren vanligvis administratortilgang, men ikke teamet. Uten dette vil du få en feil som Hovedteamet mangler når du kjører prosjektet fra Dataintegrering. 

    - Under **Innstillinger** > **Sikkerhet** > **Team**, velg relevant team. Klikk **Administrer roller** og velg en rolle med ønskede tillatelser, for eksempel Systemadministrator.

- Under **Oppsett** > **Administrasjon** > **Systeminnstillinger** > **Sales**, må du forsikre deg om at **Bruk systemets priskalkuleringssystem** er satt til **Ja**. 

- Under **Oppsett** > **Administrasjon** > **Systeminnstillinger** > **Sales**, må du forsikre deg om at **Rabattkalkuleringsmetode** er satt til **Linjeelement**. 

### <a name="setup-in-finance-and-operations"></a>Oppsett i Finance and Operations

Sett **Salg og markedsføring** > **Periodiske oppgaver** > **Kalkuler salgstotaler** for å kjøre en batchjobb, med **Kalkuler totaler for salgsordrer** satt til **Ja**. Dette er viktig fordi kun salgsordre med kalkulerte totale salg vil synkroniseres til CDS og Sales. Hyppigheten av batchjobben skal være justert med hyppigheten av salgsordensynkroniseringen.

### <a name="setup-in-the-data-integration-project"></a>Oppsett i Dataintegrasjonsprosjekt

#### <a name="salesheader-task"></a>Salgshode-oppgave

- Oppdater tilordning for **CDS-organisasjons-ID i Kilde** > **CDS**.

    - Standard malverdi for **Konto_Organisasjon_Organisasjons-ID** er ORG001.
    - Standard malverdi for **InvoiceAccount_Organization_OrganizationID** er ORG001.
    - Standard malverdi for **Organisasjon_Organisasjons-ID** er ORG001.

- Sørg for at nødvendig tilordning eksister i **Kilde** > **CDS for InvoiceCountryRegionId til BillingAdress_Country** og for **DeliveryCountryRegionID til DeliveryAddress_Country**.

    - Malverdi er **ValueMap** med et antall av land tilordnet.

- **Prisliste** er nødvendig for å opprette ordrer i Sales. Oppdater **ValueMap** i **CDS** > **Destinasjon** for **pricelevelid.name [Navn på prisliste]** til **Prisliste** brukt i Sales per valuta. Du kan bruke enten standard **Prisliste** for enkeltvaluta eller bruke **ValueMap** hvis du har **Prisliste** i flere valutaer.
    
    - Standard malverdi for **pricelevelid.name (Prislistenavn)** er CRM Service USA (prøve). 

#### <a name="salesline-task"></a>Salgslinje-oppgave

- Oppdater tilordning for **CDS-organisasjons-ID i Kilde** > **CDS**. 
    
    - Standard malverdi for **Salgsordre_Organisasjon_Organisasjons-ID** er ORG001.
    - Standard malverdi for **Produkt_Organisasjon_Organisasjons-ID** er ORG001.

- Sørg for at nødvendig tilordning eksister i **Kilde** > **CDS** for **DeliverCountryRegionID** til **DeliveryAdress_Country**.

    - Malverdi er **ValueMap** med et antall av land tilordnet.
    
- Forsikre deg om at nødvendig **ValueMap** for **SalesUnitSymbol** i Finance and Operations eksisterer i **Kilde** > **CDS-tilordning**.

    - Malverdi med **ValueMap** er definert for **SalesUnitSymbol til Quanitiy_UOM**.

## <a name="template-mapping-in-data-integrator"></a>Tilordninge mal i dataintegrator

> [!NOTE]
> Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke en del av standardtilordningene. Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.

Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.

### <a name="orderheader"></a>Ordrehode

![Tilordninge mal i dataintegrator](./media/sales-order-template-mapping-data-integrator-1.png)

![Tilordninge mal i dataintegrator](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a>Ordrelinje

![Tilordninge mal i dataintegrator](./media/sales-order-template-mapping-data-integrator-3.png)

![Tilordninge mal i dataintegrator](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Relaterte emner

[Synkronisere produkter fra Finance and Operations til produkter i Sales](products-template-mapping.md)

[Synkronisere kontoer fra Sales til kunder i Finance and Operations](accounts-template-mapping.md)

[Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations](contacts-template-mapping.md)

[Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations](sales-quotation-template-mapping.md)

[Synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales](sales-invoice-template-mapping.md)


