---
title: Synkronisere kontoer direkte fra Sales til kunder i Finance and Operations
description: "Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere kontoer fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations."
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: fb694db32638756328623c186594cf5ba2e7d6b8
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a>Synkronisere kontoer direkte fra Sales til kunder i Finance and Operations

[!INCLUDE [banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruke kundeemnet til kontanter løsning, må du ha kjennskap til [Dynamics 365-dataintegrering](/common-data-service/entity-reference/dynamics-365-integration).

Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere kontoer direkte fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflyt i Kundeemne til kontanter

Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Finance and Operations og Sales.  Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales. Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Finance and Operations og Sales.

[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for PowerApps](https://preview.admin.powerapps.com/dataintegration). Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.

Følgende maler og underliggende oppgaver brukes til å synkronisere kontoer fra Sales til Finance and Operations:

- **Navnet på malen i Dataintegrering:** Kontoer (Sales til Fin and Ops) – direkte
- **Navnet på oppgaven i prosjektet:** Kontoer - Kunder

Ingen synkroniseringsoppgaver kreves før konto-/kundesynkronisering kan utføres.

## <a name="entity-set"></a>Enhetssett

| Salg    | Finance and Operations |
|----------|------------------------|
| Kontoer | Kunder V2           |

## <a name="entity-flow"></a>Enhetsflyt

Kontoer administreres i Sales og synkroniseres med Finance and Operations som kunder. Egenskapen **Vedlikeholdes eksternt** på disse kundene er satt til **Ja** til å spore kunder som kommer fra ordrer. Denne informasjonen brukes til å filtrere fakturaer som synkroniseres til Sales under fakturering.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

**Kontonummer**-feltet er bare tilgjengelig på **Konto**-siden. Det er gjort en naturlig og unik nøkkel for å støtte integrering. Funksjonen for naturlig nøkkel i CRM-løsningen (Customer Relationship Management) kan påvirke kunder som bruker allerede **Kontonummer**-feltet, men som ikke bruker unike **Kontonummer**-verdier per konto. Integreringsløsningen støtter for øyeblikket ikke denne saken.

Når en ny konto opprettes, hvis en **Kontonummer**-verdi ikke finnes fra før, den genereres automatisk ved hjelp av en nummerserie. Verdien består av **ACC**, etterfulgt av en økende nummerserie og et suffiks på seks tegn. Her er et eksempel: **ACC-01000-BVRCPS**

Når det brukes integration-løsning for Sales, angir et oppgraderingsskript **Kontonummer** for eksisterende kontoer i Sales. Hvis det finnes ingen **Kontonummer**-verdier, nummerserien som ble omtalt tidligere brukes.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

- Tilordningen **CustomerGroupId** må oppdateres til en gyldig verdi i Finance and Operations. Du kan angi en standardverdi, eller du kan angi verdien ved hjelp av en verditilordningen.

    Standardmalverdien er **10**.

- Ved å legge til følgende tilordninger kan du redusere antallet manuelle oppdateringer som kreves i Finance and Operations. Du kan bruke standardverdi eller verditilordning fra for eksempel **Land/område** eller **By**.

    - **SiteId** – et område er nødvendig for å generere tilbud og salgsordrelinjer i Finance and Operations. Et standardområde kan hentes fra produktet eller fra kunden fra ordrehodet.

        Standardmalverdien er **1**.

    - **WarehouseId** – et lager er nødvendig for å behandle tilbud og salgsordrelinjer i Finance and Operations. Et standardlager kan hentes fra produktet eller fra kunden fra ordrehodet i Finance and Operations.

        Standardmalverdien er **13**.

    - **LanguageId** – et språk er nødvendig for å generere tilbud og salgsordrer i Finance and Operations. Som standard brukes språket fra ordrehodet fra kunden.

        Standardmalverdien er **en-us**.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

> [!NOTE]
> Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke inkludert i standardtilordningene. Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.

Følgende illustrasjoner viser et eksempel på en tilordning av malen i Dataintegrering. 

> [!NOTE]
> Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Finance and Operations.

![Maltilordning i Dataintegrering](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Relaterte emner


[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere kontoer direkte fra Sales til kunder i Finance and Operations](accounts-template-mapping-direct.md)

[Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Finance and Operations](contacts-template-mapping-direct.md)

[Synkronisere salgsordrehoder og -linjer direkte fra Finance and Operations til Sales](sales-order-template-mapping-direct-two-ways.md)

[Synkronisere salgsfakturahoder og -linjer direkte fra Finance and Operations til Sales](sales-invoice-template-mapping-direct.md)


