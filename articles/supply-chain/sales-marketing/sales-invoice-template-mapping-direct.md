---
title: Synkronisere salgsfakturahoder og -linjer direkte fra Finance and Operations til Sales
description: "Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgsfakturahoder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: afbf4a24b737cf7221bac4b688b8801b1bcd839c
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a>Synkronisere salgsfakturahoder og -linjer direkte fra Finance and Operations til Sales

[!include [banner](../includes/banner.md)]

Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgsfakturahoder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflyt i Kundeemne til kontanter

Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Finance and Operations og Sales. Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales. Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Finance and Operations og Sales.

[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for PowerApps](https://preview.admin.powerapps.com/dataintegration). Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.

Følgende mal og underliggende oppgaver brukes til å synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales:

- **Navnet på malen i Dataintegrering:** Salgsfakturaer (Fin and Ops til Sales) – direkte
- **Navnet på oppgaven i Dataintegrasjonprosjektet**:

    - SalesInvoiceHeader
    - SalesInvoiceLine

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgsfakturahoder og -linjer kan inntreffe:

- Produkter (Fin and Ops til Sales) – direkte
- Kontoer (Sales til Fin and Ops) – direkte (hvis brukt)
- Kontakter (Sales til Fin and Ops) – direkte (hvis brukt)
- Salgsordrehoder og -linjer (Fin and Ops til Sales) – direkte

## <a name="entity-set"></a>Enhetssett

| Finance and Operations                               | Salg          |
|------------------------------------------------------|----------------|
| Eksternt vedlikeholdte hoder for kundesalgsfaktura | Fakturaer       |
| Eksternt vedlikeholdte linjer for kundesalgsfaktura   | InvoiceDetails |

## <a name="entity-flow"></a>Enhetsflyt

Salgsfakturaer er opprettet i Finance and Operations og synkronisert til Sales.

> [!NOTE]
> Skatt knyttet til kostnader på salgsfakturahodet er for øyeblikket ikke inkludert i synkronisering fra Finance and Operations til Sales. Sales støtter ikke skatteinformasjon på hodenivå. Mva som er knyttet til tillegg på linjenivå er imidlertid inkludert i synkroniseringen.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

- Et **Fakturanummer**-felt er lagt til **Faktura**-enheten og vises på siden.
- Knappen **Opprett faktura** på siden **Salgsordre** er skjult fordi fakturaer vil opprettes i Finance and Operations og synkroniseres til Sales. Siden **Faktura** kan ikke redigeres fordi fakturaer vil synkroniseres fra Finance and Operations.
- **Salgsordrestatus**-verdien endres automatisk til **Fakturert** når relaterte fakturaer fra Finance and Operations er synkronisert til Sales. Eieren av salgsordren som fakturaen ble opprettet fra, tildeles også som eier av fakturaen. Eieren av salgsordren kan derfor vise fakturaen.

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
- Kontroller at den nødvendige verditilordningen finnes for **SalesUnitSymbol** i Finance and Operations.

    En malverdi som har en verditilordning er definert for **SalesUnitSymbol** til **Quantity\_UOM**.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

> [!NOTE]
> Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke inkludert i standardtilordningene. Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.

Følgende illustrasjoner viser et eksempel på en tilordning av malen i Dataintegrering. 

> [!NOTE]
> Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Finance and Operations.

### <a name="salesinvoiceheader"></a>SalesInvoiceHeader

![Maltilordning i Dataintegrering](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a>SalesInvoiceLine

![Maltilordning i Dataintegrering](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a>Relaterte emner

[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere kontoer direkte fra Sales til kunder i Finance and Operations](accounts-template-mapping-direct.md)

[Synkronisere produkter direkte fra Finance and Operations til produkter i Sales](products-template-mapping-direct.md)

[Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Finance and Operations](contacts-template-mapping-direct.md)

[Synkronisere salgsordrehoder og -linjer direkte fra Finance and Operations til Sales](sales-order-template-mapping-direct-two-ways.md)







