---
title: Synkronisere salgsfakturahoder og -linjer direkte fra Supply Chain Management til Sales
description: Dette emnet beskriver maler og underliggende oppgaver som brukes til å synkronisere salgsfakturahoder og -linjer direkte fra Dynamics 365 Supply Chain Management til Dynamics 365 Sales.
author: ChristianRytt
manager: tfehr
ms.date: 10/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 6cbc4d86ac41d90480428ec5439d1360c4d67137
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434283"
---
# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Synkronisere fakturahoder og -linjer direkte fra Finance and Operations til Sales

[!include [banner](../includes/banner.md)]

Dette emnet beskriver maler og underliggende oppgaver som brukes til å synkronisere salgsfakturahoder og -linjer direkte fra Dynamics 365 Supply Chain Management til Dynamics 365 Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflyt i Kundeemne til kontanter

Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Supply Chain Management og Sales. Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Supply Chain Management og Sales. Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Supply Chain Management og Sales.

[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for Power Apps](https://preview.admin.powerapps.com/dataintegration). Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.

Følgende mal og underliggende oppgavene brukes til å synkronisere salgsfakturahoder og -linjer fra Supply Chain Management til Sales:

- **Navnet på malen i Dataintegrering:** Salgsfakturaer (Fin and Ops til Sales) – direkte
- **Navnet på oppgaven i Dataintegrasjonprosjektet**:

    - SalesInvoiceHeader
    - SalesInvoiceLine

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgsfakturahoder og -linjer kan inntreffe:

- Produkter (Supply Chain Management til Sales) – direkte
- Kontoer (Sales til Supply Chain Management) – direkte (hvis brukt)
- Kontakter (Sales til Supply Chain Management) – direkte (hvis brukt)
- Salgsordrehoder og -linjer (Supply Chain Management til Sales) – direkte

## <a name="entity-set"></a>Enhetssett

| Forsyningskjedeadministrasjon                              | Salg          |
|------------------------------------------------------|----------------|
| Eksternt vedlikeholdte hoder for kundesalgsfaktura | Fakturaer       |
| Eksternt vedlikeholdte linjer for kundesalgsfaktura   | InvoiceDetails |

## <a name="entity-flow"></a>Enhetsflyt

Salgsfakturaer er opprettet i Supply Chain Management og synkronisert til Sales.

> [!NOTE]
> Skatt knyttet til kostnader på salgsfakturahodet er for øyeblikket ikke inkludert i synkronisering fra Supply Chain Management til Sales. Sales støtter ikke skatteinformasjon på hodenivå. Mva som er knyttet til tillegg på linjenivå er imidlertid inkludert i synkroniseringen.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

- Et **Fakturanummer**-felt er lagt til **Faktura**-enheten og vises på siden.
- Knappen **Opprett faktura** på siden **Salgsordre** er skjult fordi fakturaer vil opprettes i Supply Chain Management og synkroniseres til Sales. Siden **Faktura** kan ikke redigeres fordi fakturaer vil synkroniseres fra Supply Chain Management.
- **Salgsordrestatus**-verdien endres automatisk til **Fakturert** når relaterte fakturaer fra Supply Chain Management er synkronisert til Sales. Eieren av salgsordren som fakturaen ble opprettet fra, tildeles også som eier av fakturaen. Eieren av salgsordren kan derfor vise fakturaen.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

Før du synkroniserer salgsfakturaer, er det viktig å oppdatere innstillingene nedenfor i systemene.

### <a name="setup-in-sales"></a>Oppsett i salg

Gå til **Innstillinger** > **Administrasjon** > **Systeminnstillinger** > **Salg**, og sørger for å bruke følgende innstillinger:

- Alternativet **Bruk systemets priskalkuleringssystem** er satt til **Ja**.
- Feltet **Rabattkalkuleringsmetode** er satt til **Linjeelement**.

### <a name="setup-in-the-data-integration-project"></a>Oppsett i Dataintegrasjonsprosjekt

#### <a name="salesinvoiceheader-task"></a>Salgsfakturahode-oppgave

- Sørg for at nødvendig tilordning finnes for **InvoiceCountryRegionId** til **BillingAddress\_Country**.

    Malverdien er en verditilordning der flere land eller områder er tilordnet.

- En prisliste er nødvendig for å opprette fakturaer i Sales. Oppdater verditilordningen for **pricelevelid.name\[Prislistenavn\]** til prislisten som brukes i Sales per valuta. Du kan bruke standard prisliste for en enkelt valuta. Hvis du har prislister i flere valutaer, kan du også bruke en verditilordning.

    Malverdien for **pricelevelid.name \[Prislistenavn\]** er en verditilordning som er basert på valuta med USD = CRM Service USA (prøve).  
    
#### <a name="salesinvoiceline-task"></a>SalesInvoiceLine-oppgave

- Sørg for at nødvendig tilordning finnes for **måleenhet**.
- Kontroller at den nødvendige verditilordningen finnes for **SalesUnitSymbol** i Supply Chain Management.

    En malverdi som har en verditilordning er definert for **SalesUnitSymbol** til **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

> [!NOTE]
> Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke inkludert i standardtilordningene. Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.

Følgende illustrasjoner viser et eksempel på en tilordning av malen i Dataintegrering. 

> [!NOTE]
> Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Supply Chain Management.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Maltilordning i Dataintegrering](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Maltilordning i Dataintegrering](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Relaterte emner

[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management](accounts-template-mapping-direct.md)

[Synkronisere produkter direkte fra Supply Chain Management til produkter i Sales](products-template-mapping-direct.md)

[Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Supply Chain Management](contacts-template-mapping-direct.md)

[Synkronisering av salgsordrer direkte mellom Sales og Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)
