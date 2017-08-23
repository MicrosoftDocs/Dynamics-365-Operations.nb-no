---
title: Synkronisere produkter fra Finance and Operations til produkter i Sales
description: "Dette emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til Microsoft Dynamics 365 for Sales."
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a>Synkronisere produkter fra Finance and Operations til produkter i Sales

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruke kundeemnet til kontanter løsning, ha kjennskap til [Dynamics 365 dataintegrering](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration). 

Dette emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til Microsoft Dynamics 365 for Sales.

## <a name="template-and-task"></a>Mal og oppgave

Følgende maler og underliggende oppgaver brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) til Microsoft Dynamics 365 for Sales (Sales).

-   Navnet på malen: Produkter (Finance and Operations til Sales)

-   Navnet på oppgaven i prosjektet: Produkter

Synkronisere oppgaver som kreves synkronisering av produkt: Ingen

## <a name="entity-set"></a>Enhetssett

| **Finance and Operations** | **CDS** | **Salg**  |
|----------------------------|---------|------------|
| Salgbare frigitte produkter | Produkt | Produkter   |

## <a name="entity-flow"></a>Enhetsflyt

Produkter administreres i Finance and Operations og synkroniseres med Sales. Dataenheten **Salgbare frigitte produkter** i Finance and Operations eksporterer bare produkter som er salgbare, som betyr at produktene har informasjonen som kreves for å brukes på en salgsordre. De samme reglene gjelder når et produkt er bekreftet med **Valider**-funksjonen på siden **Frigitt produkt**.

**Produktnummer** brukes som nøkkel, noe som betyr at produktvarianter synkroniseres til CDS og Sales med individuelle **produkt-ID-er** per **produktvariant**.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

I Sales legges det til et nytt felt på produktene **Vedlikeholdes eksternt** for å angi at et bestemt produkt vedlikeholdes eksternt. Verdien er satt til **Ja** som standard under import til Sales.

-   **Vedlikeholdes eksternt = Ja**: Product stammer fra Finance and Operations og kan ikke redigeres i Sales.

-   **Vedlikeholdes eksternt = Nei**: Produktet angis direkte i Sales.

-   **Vedlikeholdes eksternt = tom**: Produktet finnes i Sales før aktivering av kundeemnet til kontantløsning.

Informasjonen i **Vedlikeholdes eksternt** brukes til å sikre at bare **tilbud** og **ordrer** med **eksternt vedlikeholdte produkter** synkroniseres til Finance and Operations.

**Eksternt vedlikeholdte produkter** legges automatisk til den første gyldige **prislisten** med samme valuta. Legg merke til at listen er sortert alfabetisk etter **navn**. Produktets salgspris fra Finance and Operations brukes som prisen på **prislisten**. Dette betyr at det må være en **prisliste** i Sales for hver **produktsalgsvaluta** i Finance and Operations. Valuta på frigitte salgbare produkter er satt til regnskapsvalutaen i den juridiske enheten som produktet er eksportert fra.

> [!NOTE]
> Produktsynkronisering kan ikke fullføres uten en **prisliste** med tilhørende valuta.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

-   Før du kjører den første synkroniseringen, må du fylle ut den **spesifikke produkttabellen** for eksisterende produkter i Finance and Operations. Eksisterende produkter vil ikke bli synkronisert før denne jobben er fullført.

    -   I Finance and Operations kan du bruke Søk til å søke etter **Fyll ut tabell for spesifikt produkt**.

    -   Klikk **Fyll ut tabell for spesifikt produkt** for å kjøre jobben. Denne jobben må bare kjøres én gang.

-   Pass på at den obligatoriske **ValueMap** for salg av **målenheten** i Finance and Operations finnes i **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.

-   Pass på at **støttede desimaler** for måleenheten oppfyller dine krav i **CDS -\> Destination**. Hvis du må ha forskjellige verdier per enhet, kan dette gjøres med **ValueMap** fra enheten, for eksempel [Each : 0] & [Pound : 2].

    -   Malverdien er 0 som standard.

-   Oppdater **ID-en for CDS-organisasjonen Organization_OrganizationId** i **Source -\> CDS**.

    -   Malverdien er ORG001 som standard.

-   Oppdater **ValueMap** for **enhetsgruppen** (**defaultuomscheduleid.name**) i **CDS -\> Destination** til å samsvare med **enhetsgruppene** i Sales.

    -   Malverdien er **Standardenhet** som standard.

-   Kontroller at alle målenheter for produktsalg fra Finance and Operations finnes i Sales, med verdien **CDS-plukklister**.

-   Kontroller at **Prislister** finnes i Sales for hver produktsalgsvaluta i Finance and Operations.

-   Produkter kan opprettes i Sales med statusen **Utkast** eller **Aktive**. Dette styres i **Systeminnstillinger** under **Salg** i Sales.

    -   Produkter som er opprettet med utkaststatus, må aktiveres før de kan legges til i et **tilbud** eller en **salgsordre**.

## <a name="template-mapping-in-data-integrator"></a>Tilordninge mal i dataintegrator

Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.

![tilordne mal i dataintegrator](./media/products-template-mapping-data-integrator-1.png)

![tilordne mal for produkter i dataintegrator](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Relaterte emner

[Synkronisere kontoer fra Sales til kunder i Finance and Operations](accounts-template-mapping.md)

[Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations](contacts-template-mapping.md)

[Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations](sales-quotation-template-mapping.md)

