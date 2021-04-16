---
title: Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management
description: Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere forretningsforbindelser fra Dynamics 365 Sales til Supply Chain Management.
author: ChristianRytt
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 1bf0da5ba5274b61758bc0efdc2f2167327966ad
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5831656"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a>Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Før du kan bruke kundeemnet til kontanter løsning må du ha kjennskap til [Integrere data til Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).

Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere forretningsforbindelser direkte fra Dynamics 365 Sales til Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflyt i Kundeemne til kontanter

Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Supply Chain Management og Sales.  Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data om kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Supply Chain Management og Sales. Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Supply Chain Management og Sales.

[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for Power Apps](https://preview.admin.powerapps.com/dataintegration). Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.

Følgende maler og underliggende oppgaver brukes til å synkronisere kontoer fra Sales til Supply Chain Management:

- **Navnet på malen i Dataintegrering:** Kontoer (Sales til Fin and Ops) – direkte
- **Navnet på oppgaven i prosjektet:** Kontoer - Kunder

Ingen synkroniseringsoppgaver kreves før konto-/kundesynkronisering kan utføres.

## <a name="entity-set"></a>Enhetssett

| Salg    | Supply Chain Management |
|----------|------------------------|
| Kontoer | Kunder V2           |

## <a name="entity-flow"></a>Enhetsflyt

Kontoer administreres i Sales og synkroniseres med Supply Chain Management som kunder. Egenskapen **Vedlikeholdes eksternt** på disse kundene er satt til **Ja** til å spore kunder som kommer fra ordrer. Denne informasjonen brukes til å filtrere fakturaer som synkroniseres til Sales under fakturering.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

**Kontonummer**-kolonnen er bare tilgjengelig på **Konto**-siden. Det er gjort en naturlig og unik nøkkel for å støtte integrering. Funksjonen for naturlig nøkkel i CRM-løsningen (Customer Relationship Management) kan påvirke kunder som allerede bruker **Kontonummer**-kolonnen, men som ikke bruker unike **Kontonummer**-verdier per konto. Integreringsløsningen støtter for øyeblikket ikke denne saken.

Når en ny konto opprettes, hvis en **Kontonummer**-verdi ikke finnes fra før, den genereres automatisk ved hjelp av en nummerserie. Verdien består av **ACC**, etterfulgt av en økende nummerserie og et suffiks på seks tegn. Her er et eksempel: **ACC-01000-BVRCPS**

Når integreringsløsningen brukes for Sales, angir et oppgraderingsskript **Kontonummer**-kolonnen for eksisterende kontoer i Sales. Hvis det finnes ingen **Kontonummer**-verdier, nummerserien som ble omtalt tidligere brukes.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

- Tilordningen **CustomerGroupId** må oppdateres til en gyldig verdi i Supply Chain Management. Du kan angi en standardverdi, eller du kan angi verdien ved hjelp av en verditilordningen.

    Standardmalverdien er **10**.

- Ved å legge til følgende tilordninger kan du redusere antallet manuelle oppdateringer som kreves i Supply Chain Management. Du kan bruke standardverdi eller verditilordning fra for eksempel **Land/område** eller **By**.

    - **SiteId** – et område er nødvendig for å generere tilbud og salgsordrelinjer i Supply Chain Management. Et standardområde kan hentes fra produktet eller fra kunden fra ordrehodet.

        Standardmalverdien er **1**.

    - **WarehouseId** – et lager er nødvendig for å behandle tilbud og salgsordrelinjer i Supply Chain Management. Et standardlager kan hentes fra produktet eller fra kunden fra ordrehodet i Supply Chain Management.

        Standardmalverdien er **13**.

    - **LanguageId** – et språk er nødvendig for å generere tilbud og salgsordrer i Supply Chain Management. Som standard brukes språket fra ordrehodet fra kunden.

        Standardmalverdien er **en-us**.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

> [!NOTE]
> Kolonnene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke inkludert i standardtilordningene. Hvis du vil tilordne disse kolonnene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som tabellen synkroniseres mellom.

Følgende illustrasjoner viser et eksempel på en tilordning av malen i Dataintegrering. 

> [!NOTE]
> Tilordningen viser hvilken kolonneinformasjon som vil bli synkronisert fra Sales til Supply Chain Management.

![Maltilordning i Dataintegrering](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a>Relaterte emner


[Kundeemne til kontanter](prospect-to-cash.md)

[Synkronisere kontoer direkte fra Sales til kunder i Supply Chain Management](accounts-template-mapping-direct.md)

[Synkronisere kontakter direkte fra Sales til kontakter eller kunder i Supply Chain Management](contacts-template-mapping-direct.md)

[Synkronisering av salgsordrer direkte mellom Sales og Supply Chain Management](sales-order-template-mapping-direct-two-ways.md)

[Synkronisere salgsfakturahoder og -linjer direkte fra Supply Chain Management til Sales](sales-invoice-template-mapping-direct.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]