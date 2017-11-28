---
title: Synkronisere kontoer fra Sales til kunder i Finance and Operations
description: "Emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere kontoer fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a>Synkronisere kontoer fra Sales til kunder i Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruke kundeemnet til kontanter løsning, ha kjennskap til [Dynamics 365 dataintegrering](/common-data-service/entity-reference/dynamics-365-integration). 

Emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere kontoer fra Microsoft Dynamics 365 for Sales (Sales) til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).

## <a name="template-and-task"></a>Mal og oppgave

Følgende malene og underliggende oppgavene brukes til å synkronisere kontoer fra Sales til Finance and Operations:

- **Navnet på malen:** Kontoer (Sales til Finance and Operations)
- **Navnet på oppgaven i prosjektet:** Kontoer - Konto - Kunder

Synkronisere oppgaver som kreves før konto / kunde synkronisering: Ingen

## <a name="entity-set"></a>Enhetssett

| Salg    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Kontoer | Konto | Kunder              |

## <a name="entity-flow"></a>Enhetsflyt

Kontoer administreres i Sales og synkroniseres med Finance and Operations som kunder. Egenskapen **Vedlikeholdes eksternt** på disse kundene er satt til **Ja** til å spore kunder som kommer fra ordrer. Denne informasjonen brukes til å filtrere fakturaer som synkroniseres til Sales under fakturering.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

**Kontonummer**-feltet er bare tilgjengelig på **Konto**-siden. Det er gjort en naturlig og unik nøkkel for å støtte integrering. Funksjonen for naturlig nøkkel i CRM-løsningen (Customer Relationship Management) kan påvirke kunder som bruker allerede **Kontonummer**-feltet, men som ikke bruker unike **Kontonummer**-verdier per konto. Integreringsløsningen støtter for øyeblikket ikke denne saken.

Når en ny konto opprettes, hvis en **Kontonummer**-verdi ikke finnes fra før, den genereres automatisk ved hjelp av en nummerserie. Verdien består av **ACC**, etterfulgt av en økende nummerserie og et suffiks på seks tegn. Her er et eksempel: **ACC-01000-BVRCPS**

Når det brukes integration-løsning for Sales, angir et oppgraderingsskript **Kontonummer** for eksisterende kontoer i Sales. Hvis det finnes ingen **Kontonummer**-verdier, nummerserien som ble omtalt tidligere brukes.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

- **CustomerGroupId**-tilordning fra **CDS&gt;-destinasjon** må oppdateres til en gyldig verdi for Finance and Operations. Du kan angi en standardverdi, eller du kan angi verdien ved hjelp av en verditilordningen. Standardmalverdien er **10**.
- **Kode for adresse, land og område** er obligatorisk i Finance and Operations. For å unngå synkroniseringsfeil kan du angi en standardverdi i kartleggingen fra **CDS&gt;-destinasjon**. Den standardverdien brukes deretter hvis feltet er tomt i Sales.

    - Standardmalverdien for **AddressCountryRegionISOCode** er **USA**.
    - Standardmalverdien for **DeliveryAddressCountryRegionISOCode** er **USA**.

- Ved å legge til følgende tilordninger fra **CDS &gt; Mål** kan du redusere antallet manuelle oppdateringer som kreves i Finance and Operations. Du kan bruke standardverdi eller verditilordning fra for eksempel **Land/område** eller **By**.

    - **SiteId** – et område er nødvendig for å generere tilbud og salgsordrelinjer i Finance and Operations. Et standardområde kan hentes fra produktet eller fra kunden fra ordrehodet. Standardmalverdien for **SiteId** er **1**.
    - **WarehouseId** – et lager er nødvendig for å behandle tilbud og salgsordrelinjer i Finance and Operations. Et standardlager kan hentes fra produktet eller fra kunden fra ordrehodet i Finance and Operations. Standardmalverdien for **WarehouseId** er **13**.
    - **LanguageId** – et språk er nødvendig for å generere tilbud og salgsordrer i Finance and Operations. Som standard brukes språket fra ordrehodet fra kunden. Standardmalverdien for **LanguageId** er **en-us**.

- Oppdater ID- en for CDS-organisasjonen (**Organization_OrganizationId**) i tilordningen av **Kilde &gt;CDS**. Standardmalverdien er **ORG001**.

## <a name="template-mapping-in-data-integrator"></a>Tilordninge mal i dataintegrator

> [!NOTE]
> Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke inkludert i standardtilordningene. Hvis du vil tilordne disse feltene, må du definere en verditilordning. Verditilordninger er spesifikke for dataene i organisasjoner som enheten synkroniseres mellom.

Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.

![Tilordninge mal i dataintegrator](./media/accounts-template-mapping-data-integrator-1.png)

![Tilordne mal for kontoer i dataintegrator](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Relaterte emner

[Synkronisere produkter fra Finance and Operations til produkter i Sales](products-template-mapping.md)

[Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations](contacts-template-mapping.md)

[Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations](sales-quotation-template-mapping.md)

[Synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales](sales-order-template-mapping.md)

[Synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales](sales-invoice-template-mapping.md)




