---
title: Synkronisere produkter direkte fra Finance and Operations til produkter i Sales
description: "Dette emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til Microsoft Dynamics 365 for Sales."
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 6c68c4482cacf70f003669cf335e52e47425d2f7
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a>Synkronisere produkter direkte fra Finance and Operations til produkter i Sales

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruke kundeemnet til kontanter løsning, må du ha kjennskap til [Dynamics 365-dataintegrering](/common-data-service/entity-reference/dynamics-365-integration).

Dette emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere produkter direkte fra Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til Microsoft Dynamics 365 for Sales.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflyt i Kundeemne til kontanter

Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Finance and Operations og Sales. Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales. Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Finance and Operations og Sales.

[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for PowerApps](https://preview.admin.powerapps.com/dataintegration). Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.

Følgende mal og underliggende oppgavene brukes til å synkronisere produkter fra til Finance and Operations til sales.

- **Navnet på malen i Dataintegrering:** Produkter (Fin and Ops til Sales) – direkte
- **Navnet på oppgaven i Dataintegrasjonprosjektet**: Produkter

Ingen synkroniseringsoppgaver kreves før produktsynkronisering kan utføres.

## <a name="entity-set"></a>Enhetssett

| Finance and Operations     | Salg    |
|----------------------------|----------|
| Salgbare frigitte produkter | Produkter |

## <a name="entity-flow"></a>Enhetsflyt

Produkter administreres i Finance and Operations og synkroniseres med Sales. Sataenheten **Salgbare frigitte produkter** i Finance and Operations eksporterer bare produkter som er *salgbare*. salgbare produkter er produkter som inneholder informasjon som kreves for å kunne brukes på en salgsordre. De samme reglene gjelder når et produkt er bekreftet ved å bruke **Valider**-funksjonen på siden **Frigitt produkt**.

Produktnummeret brukes som en nøkkel. Når produktvarianter synkroniseres til Sales, har hver produktvariant én enkelt produkt-ID.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

I Sales legges det til et nytt **Vedlikeholdes eksternt**-felt på produktene for å angi at et bestemt produkt vedlikeholdes eksternt. Verdien er satt til **Ja** som standard under import til Sales. Følgende verdier er tilgjengelige:

- **Ja** – Produktet kommer fra Finance and Operations, og kan ikke redigeres i Sales.
- **Nei** – Produktet ble lagt inn direkte i Sales.
- **(Tom)** – Produktet fantes i Sales før løsningen Kundeemne til kontanter ble aktivert.

Informasjonen i feltet **Vedlikeholdes eksternt** brukes til å garantere at bare tilbud og salgsordrer med eksternt vedlikeholdte produkter synkroniseres til Finance and Operations.

Eksternt vedlikeholdte produkter legges automatisk til den første gyldige prislisten med samme valuta. Prislister er ordnet alfabetisk etter navn. Produktets salgspris fra Finance and Operations brukes som prisen på prislisten. Derfor må det være en prisliste i Sales for alle produktsalgsvaluta i Finance and Operations. Valutaen på frigitte salgbare produkter er satt til regnskapsvalutaen i den juridiske enheten som produktet er eksportert fra.

> [!NOTE]
> Produktsynkronisering lykkes ikke hvis det ikke er en prisliste som har en tilhørende valuta.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

- Før du kjører synkroniseringen for første gang, må du fylle ut den spesifikke produkttabellen for eksisterende produkter i Finance and Operations. Eksisterende produkter vil ikke bli synkronisert før denne jobben er fullført.

    1. I Finance and Operations kan du bruke Søk til å søke etter **Fyll ut tabell for spesifikt produkt**.
    2. Velg **Fyll ut tabell for spesifikt produkt** for å kjøre jobben. Jobben må kjøres bare én gang.

- Pass på at den nødvendige verditilordningen for selgende måleenheten mellom Finance and Operations og Sales finnes i tilordnignen for **SalesUnitSymbol** til **DefaultUnit (Name)**.
- Oppdater verditilordningen for **enhetsgruppen** (**defaultuomscheduleid.name**), slik at den samsvarer med **enhetsgruppene** i Sales.

    Standard malverdi er **Standardenhet**.

- Kontroller at målenheter for alle produkter fra Finance and Operations finnes i Sales.
- Kontroller at prislister finnes i Sales for alle produktsalgsvaluta i Finance and Operations.
- Når produkter opprettes i Sales, får de statusen **Utkast** eller **Aktiv**. Virkemåten kontrolleres under **Innstillinger** > **Administrasjon** > **Systeminnstillinger** > **Salg** i Sales.

    Produkter som har statusen **Utkast** når de opprettes, må aktiveres før de kan legges til i tilbud eller salgsordrer.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonen nedenfor viser et eksempel på en tilordning av malen i Dataintegrering. 

> [!NOTE]
> Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Finance and Operations.

![Maltilordning i Dataintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a>Relaterte emner

[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere kontoer direkte fra Sales til kunder i Finance and Operations](accounts-template-mapping-direct.md)

[Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Finance and Operations](contacts-template-mapping-direct.md)

[Synkronisere salgsordrehoder og -linjer direkte fra Finance and Operations til Sales](sales-order-template-mapping-direct.md)

[Synkronisere salgsfakturahoder og -linjer direkte fra Finance and Operations til Sales](sales-invoice-template-mapping-direct.md)




