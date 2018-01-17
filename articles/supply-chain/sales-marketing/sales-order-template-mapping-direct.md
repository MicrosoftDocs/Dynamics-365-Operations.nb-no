---
title: Synkronisere salgsordrehoder og -linjer direkte fra Finance and Operations til Sales
description: "Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgsordrehoder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Synkronisere salgsordrehoder og -linjer direkte fra Finance and Operations til Sales

[!include[banner](../includes/banner.md)]

Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgsordrehoder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflyt i Kundeemne til kontanter

Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Finance and Operations og Sales. Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales. Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Finance and Operations og Sales.

[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for PowerApps](https://preview.admin.powerapps.com/dataintegration). Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.

Følgende mal og underliggende oppgaver brukes til å synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales:

- **Navnet på malen i Dataintegrering:** Salgsordrer (Fin and Ops til Sales) – direkte
- **Navnet på oppgaven i Dataintegrasjonprosjektet**:

    - OrderHeader
    - OrderLine

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgsfakturahoder og -linjer kan inntreffe:

- Produkter (Fin and Ops til Sales) – direkte
- Kontoer (Sales til Fin and Ops) – direkte (hvis brukt)
- Kontakter til Kunder (Sales til Fin and Ops) – direkte (hvis brukt)

## <a name="entity-set"></a>Enhetssett

| Finance and Operations  | Salg             |
|-------------------------|-------------------|
| CDS-salgsordrehoder | Salgsordrer       |
| CDS-salgsordrelinjer   | Salgsordredetaljer |

## <a name="entity-flow"></a>Enhetsflyt

Salgsordrer er opprettet i Finance and Operations og synkronisert til Sales.

Filtre i malen garanterer at kun relevante salgsordrer er inkludert i synkroniseringen:

- Både bestilling og fakturering av kunde på salgsordren som kommer fra Sales vil inkluderes i synkroniseringen. I Finance and Operations brukes feltene **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** til å spore synkroniseringen i dataenhetene.
- Salgsordren i Finance and Operations må bekreftes. Kun bekreftede salgsordre eller salgsordre med høyere behandlingsstatus, for eksempel **Sendt** eller **Fakturert**, synkroniseres til Sales.
- Etter at en salgsordre er opprettet eller endret, må den satsvise jobben **Kalkuler salgstotaler** i Finance and Operations kjøres. Bare salgsordrene der salgsttotalene er beregnet, blir synkronisert Sales.

> [!NOTE]
> Skatt knyttet til kostnader på Salgsordrehode er for øyeblikket ikke inkludert i synkronisering fra Finance and Operations til Sales. Sales støtter ikke skatteinformasjon på hodenivå. Mva som er knyttet til tillegg på linjenivå er imidlertid inkludert i synkroniseringen.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

Nye felt er lagt til enheten **Ordre** og vises på siden:

- **Er behandlet eksternt** – Sett dette alternativet til **Ja** når ordren kommer fra Finance and Operations.
- **Behandlingsstatus** – Dette feltet viser behandlingsstatus for en ordre i Finance and Operations. Følgende verdier er tilgjengelige:

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

Innstillingen **Har bare eksternt vedlikeholdte produkter** brukes i andre salgsordrescenarier (for eksempel synkronisering fra Sales til Finance and Operation) for å holde oversikt over om en salgsordre helt og holdent består av eksternt behandlede produkter. Hvis en salgsordre består av bare eksternt vedlikeholdte produkter, vedlikeholdes produktene i Finance and Operations. Denne innstillingen kan garantere at du ikke prøver å synkronisere salgsordrelinjer med produkter som er ukjent for Finance and Operations.

Knappene **Opprett faktura**, **Avbryt ordre**, **Rekalkuler**, **Få produkter** og **Søk opp adresser** på siden **Salgsordre** er skjult for eksternt behandlede ordrer fordi fakturaer vil opprettes i Finance and Operations og synkronisert til Sales. Ordresiden kan ikke redigeres fordi salgsordreinformasjon vil bli synkronisert fra Finance and Operations.

Salgsordrestatus vil fortsatt være **Aktiv** for å garantere at endringer fra Finance and Operations kan flyte fra salgsordren i Sales. Dette kontrolleres ved å sette standardverdien **Statuskode \[Status\]** til **Aktiv** i Dataintegrasjonsprosjektet.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

Før du synkroniserer salgsordrer, er det viktig å oppdatere innstillingene nedenfor i systemene.

### <a name="setup-in-sales"></a>Oppsett i salg

- Kontroller at tillatelser er definert for temaet som brukeren fra Sales-tilkoblingssett er tildelt til. Hvis du bruker demomstrasjonsdata, har brukeren vanligvis administratortilgang, men teamet har ikke administratortilgang. Hvis teamet ikke også har administratortilgang når du kjører prosjektet fra Dataintegrering, vil du få en feilmelding om at hovedteamet mangler.

    Gå til **Innstillinger** > **Sikkerhet** > **Team**, velg relevant team. velg **Administrer roller** og velg en rolle med ønskede tillatelser, for eksempel **Systemadministrator**.

- Gå til **Innstillinger** > **Administrasjon** > **Systeminnstillinger** > **Salg**, og sørger for å bruke følgende innstillinger:

    - Alternativet **Bruk systemets priskalkuleringssystem** er satt til **Ja**.
    - Feltet **Rabattkalkuleringsmetode** er satt til **Linjeelement**.

### <a name="setup-in-finance-and-operations"></a>Oppsett i Finance and Operations

Gå til **Salg og markedsføring** > **Periodiske oppgaver** > **Beregn salgstotaler**, og angi at jobben skal kjøres som en satsvis jobb. Sett alternativet **Beregnede totaler for salgsordrer** til **Ja**. Dette trinnet er viktig fordi kun salgsordre med kalkulerte totale salg vil synkroniseres til Sales. Hyppigheten av den satsvise jobben skal være justert med hyppigheten av salgsordensynkroniseringen.

### <a name="setup-in-the-data-integration-project"></a>Oppsett i Dataintegrasjonsprosjekt

#### <a name="salesheader-task"></a>Salgshode-oppgave

- Sørg for at nødvendig tilordning finnes for **InvoiceCountryRegionId** til **BillingAddress\_Country** og for **DeliveryCountryRegionId** til **DeliveryAddress\_Country**.

    Malverdien er en verditilordning der flere land eller områder er tilordnet.

- En prisliste er nødvendig for å opprette ordrer i Sales. Oppdater verditilordningen for **pricelevelid.name\[Prislistenavn\]** til prislisten som brukes i Sales per valuta. Du kan bruke standard prisliste for en enkelt valuta. Hvis du har prislister i flere valutaer, kan du også bruke en verditilordning.

    Standard malverdi for **pricelevelid.name\[(Prislistenavn)\]** er **CRM Service USA (prøve)**.

#### <a name="salesline-task"></a>Salgslinje-oppgave

- Sørg for at nødvendig tilordning finnes for **DeliveryCountryRegionId** til **DeliveryAddress\_Country**.

    Malverdien er en verditilordning der flere land eller områder er tilordnet.

- Kontroller at den nødvendige verditilordningen finnes for **SalesUnitSymbol** i Finance and Operations.

    En malverdi som har en verditilordning er definert for **SalesUnitSymbol** til **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

> [!NOTE]
> Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke inkludert i standardtilordningene. Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.

Følgende illustrasjoner viser et eksempel på en tilordning av malen i Dataintegrering. 

> [!NOTE]
> Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Finance and Operations.

### <a name="orderheader"></a>OrderHeader

![Maltilordning i Dataintegrator](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a>OrderLine

![Maltilordning i Dataintegrator](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Relaterte emner

[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere kontoer direkte fra Sales til kunder i Finance and Operations](accounts-template-mapping-direct.md)

[Synkronisere produkter direkte fra Finance and Operations til produkter i Sales](products-template-mapping-direct.md)

[Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Finance and Operations](contacts-template-mapping-direct.md)

[Synkronisere salgsfakturahoder og -linjer direkte fra Finance and Operations til Sales](sales-invoice-template-mapping-direct.md)




