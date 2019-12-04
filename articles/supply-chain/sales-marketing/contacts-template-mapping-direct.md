---
title: Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Supply Chain Management
description: Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere enhetene Kontakt (kontakter) og Kontakt (kunder) fra Dynamics 365 Sales til Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 141464f2ce7cb4ccfd2a8fb7a266e657e8f52015
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2019
ms.locfileid: "2814127"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a>Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Supply Chain Management

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruke kundeemnet til kontanter løsning må du ha kjennskap til [Integrere data til Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere enhetene Kontakt (kontakter) og Kontakt (kunder) direkte fra Dynamics 365 Sales til Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflyt i Kundeemne til kontanter

Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Supply Chain Management og Sales. Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Supply Chain Management og Sales. Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Supply Chain Management og Sales.

[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for PowerApps](https://preview.admin.powerapps.com/dataintegration). Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.

Følgende malene og underliggende oppgavene brukes til å synkronisere kontakt (kontakter)-enheter i Sales til kontakt (kunder)-enheter i Supply Chain Management.

- **Navn på malene i Dataintegrering**

    - Kontakter (Sales til Supply Chain Management) – direkte
    - Kontakter til kunde (Sales til Supply Chain Management) – direkte

- **Navnet på oppgaven i Dataintegrasjonprosjektet**

    - Kontakter
    - ContactToCustomer

Følgende synkroniseringsoppgave kreves før synkronisering av kontakt kan utføres: Kontoer (Sales til Supply Chain Management)

## <a name="entity-sets"></a>Enhetssett

| Salg    | Forsyningskjedeadministrasjon |
|----------|------------------------|
| Kontakter | CDS-kontakter           |
| Kontakter | Kunder V2           |

## <a name="entity-flow"></a>Enhetsflyt

Kontakter administreres i Sales og synkroniseres med Supply Chain Management.

En kontakt i Sales kan bli en kontakt eller kunde i Supply Chain Management. For å fastslå om en kontakt i Sales skal synkroniseres med Supply Chain Management som en kontakt eller en kunde, vurderer systemet følgende egenskaper for kontakten i Sales:

- **Synkronisere til en kunde i Supply Chain Management**: Kontakter hvor **Er aktiv kunde** er satt til **Ja**
- **Synkronisere til en kontakt i Supply Chain Management**: Kontakter hvor **Er aktiv kunde** er satt til **Nei** og **Bedrift** (overordnet konto/kontakt) peker til en konto (ikke en kontakt)

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

Et nytt **Er aktiv kunde**-felt er blitt lagt til for kontakten. Dette feltet brukes til å skille mellom kontakter med salgsaktivitet og kontakter som ikke har salgsaktivitet. **Er aktiv kunde** er satt til **Ja** bare for kontakter som har lignende tilbud, ordrer eller fakturaer. Bare disse kontaktene synkroniseres til Supply Chain Management som kunder.

Et nytt **IsCompanyAnAccount**-felt er blitt lagt til for kontakten. Dette feltet brukes til å angi om en kontakt er koblet til et firma (overordnet konto//kontakt) av **Konto**-typen. Denne informasjonen brukes til å identifisere kontakter som skal synkroniseres til Supply Chain Management som kontakter.

Et nytt **Kontaktnummer**-felt har blitt lagt til kontakten for å garantere en naturlig og unik nøkkel for integreringen. Når det opprettes en ny kontakt, en **Kontaktnummer**-verdi genereres automatisk ved hjelp av en nummerserie. Verdien består av **CON**, etterfulgt av en økende nummerserie og et suffiks på seks tegn. Her er et eksempel: **CON-01000-BVRCPS**

Når integreringsløsningen for Sales legges til, angir et oppgraderingsskript **Kontaktnummer**-feltet for eksisterende kontakter ved hjelp av nummerserien som ble beskrevet tidligere. Oppgraderingsskriptet angir også feltet **Er aktiv kunde** til **Ja** for alle kontaktene med salgsaktivitet.

## <a name="in-supply-chain-management"></a>I Supply Chain Management

Kontakter er kodet ved hjelp av egenskapen **IsContactPersonExternallyMaintained**. Denne egenskapen angir at en gitt kontakt vedlikeholdes eksternt. I så fall vedlikeholdes eksterne kontakter i Sales.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

### <a name="contact-to-customer"></a>Kontakt til kunde

- **CustomerGroup** kreves i Supply Chain Management. Hvis du vil unngå synkroniseringsfeil, kan du angi en standardverdi i tilordningen. Den standardverdien brukes deretter hvis feltet er tomt i Sales.

    Standardmalverdien er **10**.

- Ved å legge til følgende tilordninger kan du redusere antallet manuelle oppdateringer som kreves i Supply Chain Management. Du kan bruke standardverdi eller verditilordning fra for eksempel **Land/område** eller **By**.

    - **SiteId** – Et standardområde kan også defineres for produkter i Supply Chain Management. Et område er nødvendig for å generere tilbud og salgsordrer i Supply Chain Management.

        En malverdi for **SiteId** er ikke angitt.

    - **WarehouseId** – Et standardlager kan også defineres for produkter i Supply Chain Management. Et lager er nødvendig for å generere tilbud og salgsordrer i Supply Chain Management.

        En malverdi for **WarehouseId** er ikke angitt.

    - **LanguageId** – et språk er nødvendig for å generere tilbud og salgsordrer i Supply Chain Management.
    
        Standardmalverdien er **en-us**.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser et eksempel på en tilordning av malen i Dataintegrering. 

> [!NOTE]
> Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Supply Chain Management.

### <a name="contact-to-contact"></a>Kontakt til kontakt

![Maltilordning i Dataintegrator](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a>Kontakt til kunde

![Maltilordning i Dataintegrator](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a>Relaterte emner

[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management](accounts-template-mapping-direct.md)

[Synkronisere produkter direkte fra Supply Chain Management til produkter i Sales](products-template-mapping-direct.md)

[Synkronisering av salgsordrer direkte mellom Sales og Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Synkronisere salgsfakturahoder og -linjer direkte fra Supply Chain Management til Sales](sales-invoice-template-mapping-direct.md)


