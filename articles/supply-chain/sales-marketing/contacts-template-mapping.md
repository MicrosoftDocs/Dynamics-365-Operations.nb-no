---
title: Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations
description: "Dette emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere kontakt (kontakter) og kontakt (kunder) fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 47e70cb1291e390b42b7feff844b2aca141f09b7
ms.openlocfilehash: 41e27776b94df059ada13efb9a3dbf6a29d67f36
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a>Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruke kundeemnet til kontanter løsning, ha kjennskap til [Dynamics 365 dataintegrering](/common-data-service/entity-reference/dynamics-365-integration). 

Dette emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere kontaktenheter (kontakter) og kontakt (kunder) fra Microsoft Dynamics 365 for Sales (Sales) til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).

## <a name="templates-and-tasks"></a>Maler og oppgaver

Følgende malene og underliggende oppgavene brukes til å synkronisere kontakt (kontakter) i Sales til kontakt (kunder) i Finance and Operations:

- **Navnene på malene:**

    - Kontakter (Sales to Fin and Ops)
    - Kontakter til Kunde (Sales til Fin and Ops)

- **Navnene på oppgavene i prosjektet:**

    - Kontakter
    - ContactToCustomer

Følgende synkroniseringsoppgave kreves før synkronisering av kontakt: Kontoer (Sales til Fin and Ops)

## <a name="entity-sets"></a>Enhetssett

| Salg    | CDS     | Finance and Operations |
|----------|---------|------------------------|
| Kontakter | Kontakt | CDS-kontakter           |
| Kontakter | Konto | Kunder V2           |

## <a name="entity-flow"></a>Enhetsflyt

Kontakter administreres i Sales og synkroniseres til Common Data Service (CDS) og Finance and Operations.

En kontakt i Sales kan bli en kontakt i CDS og Finance and Operations. Den kan også bli en konto i CDS og en kunde i Finance and Operations. For å finne ut om en kontakt skal plukkes i Sales for synkronisering til CDS og Finance and Operations (for eksempel kontakter i Sales &gt; Kontakt i CDS &gt; Kontakter i Finance and Operations), ser systemet på følgende egenskaper for kontakten i Sales:

- **Synkronisere til konto i CDS og kunde i Finance and Operations:** Kontakter hvor **Er aktiv kunde** er satt til **Ja**
- **Synkronisere til kontakt i CDS og kontakt i Finance and Operations:** Kontakter hvor **Er aktiv kunde** er satt til **Nei** og **Bedrift** (overordnet konto/kontakt) peker til en konto (ikke en kontakt)

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales 

Et nytt **Er aktiv kunde**-felt er blitt lagt til for kontakten. Dette feltet brukes til å skille mellom kontakter med salgsaktivitet og kontakter som ikke har salgsaktivitet. **Er aktiv kunde** er satt til **Ja** bare for kontakter som har lignende tilbud, ordrer eller fakturaer. Bare disse kontaktene synkroniseres til Finance and Operations som kunder.

Et nytt **IsCompanyAnAccount**-felt er blitt lagt til for kontakten. Dette feltet brukes til å angi om en kontakt er koblet til et firma (overordnet konto//kontakt) av **Konto**-typen. Denne informasjonen brukes til å identifisere kontakter som skal synkroniseres til Finance and Operations som kontakter.

Et nytt **Kontaktnummer**-felt har blitt lagt til kontakten for å garantere en naturlig og unik nøkkel for integreringen. Når det opprettes en ny kontakt, en **Kontaktnummer**-verdi genereres automatisk ved hjelp av en nummerserie. Verdien består av **CON**, etterfulgt av en økende nummerserie og et suffiks på seks tegn. Her er et eksempel: **CON-01000-BVRCPS**

Når integreringsløsningen for Sales legges til i Sales, angir et oppgraderingsskript **Kontaktnummer**-feltet for eksisterende kontakter ved hjelp av nummerserien som ble beskrevet tidligere. Oppgraderingsskriptet angir også feltet **Er aktiv kunde** til **Ja** for alle kontaktene med salgsaktivitet.

## <a name="in-finance-and-operations"></a>I Finance og Operations 

Kontakter er kodet ved hjelp av egenskapen **IsContactPersonExternallyMaintained**. Denne egenskapen angir at en gitt kontakt vedlikeholdes eksternt. I så fall vedlikeholdes eksterne kontakter i Sales.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

### <a name="contact-to-contact"></a>Kontakt til kontakt

- Oppdater **ID for CDS-organisasjon** i tilordningen **Kilde &gt; CDS**.

    - Standardmalverdien for **Organization_OrganizationId [Organisasjons-ID]** er **ORG001**.
    - Standardmalverdien for **PrimaryAccount_Organization_OrganizationId [Organisasjons-ID]** er **ORG001**.

- **Kode for adresse, land og område** er obligatorisk i Finance and Operations. Hvis du vil unngå synkroniseringsfeil, kan du angi en standardverdi i tilordningen **CDS &gt; Operasjoner**. Den standardverdien brukes deretter hvis feltet er tomt i Sales. Standardmalverdien for **PrimaryAddressCountryRegionISOCode** er **USA**.
- Kontroller at det finnes en verdi for følgende felt i Finance and Operations. Hvis informasjonen ikke er nødvendig i Finance and Operations, kan du fjerne tilordningen fra tilordningen **CDS &gt; Mål**.

    - **Feltnavn i Finance and Operations:** Beslutning
    - **Tilordning:** PrimaryAccountRole = DecisionMakingRole

### <a name="contact-to-customer"></a>Kontakt til kunde

- Oppdater **ID for CDS-organisasjon** i tilordningen **Kilde &gt; CDS**. Standardmalverdien for **Organization_OrganizationId [Organisasjons-ID]** er **ORG001**.
- **Kode for adresse, land og område** er obligatorisk i Finance and Operations. Hvis du vil unngå synkroniseringsfeil, kan du angi en standardverdi i tilordningen **CDS &gt; Mal**. Den standardverdien brukes deretter hvis feltet er tomt i Sales. Standardmalverdien for **PrimaryAddressCountryRegionISOCode** er **USA**.
- **CustomerGroup** er obligatorisk i Finance and Operations. Hvis du vil unngå synkroniseringsfeil, kan du angi en standardverdi i tilordningen **CDS &gt; Mal**. Den standardverdien brukes deretter hvis feltet er tomt i Sales. Standardmalverdien for **CustomerGroupId** er **10**.
- Ved å legge til følgende tilordninger fra **CDS &gt; Mål** kan du redusere antallet manuelle oppdateringer i Finance and Operations. Du kan bruke standardverdi eller verditilordning fra for eksempel **Land/område** eller **By**.

    - **SiteId** - Et standardområde kan også defineres for produkter i Finance and Operations. Et område er nødvendig for å generere tilbud og salgsordrer i Finance and Operations. En malverdi for **SiteId** er ikke angitt.
    - **WarehouseId** - Et standardlager kan også defineres for produkter i Finance and Operations. Et lager er nødvendig for å generere tilbud og salgsordrer i Finance and Operations. En malverdi for **WarehouseId** er ikke angitt.
    - **LanguageId** - et språk er nødvendig for å generere tilbud og salgsordrer i Finance and Operations. Standardmalverdien for **LanguageId** er **en-us**.

## <a name="template-mapping-in-data-integrator"></a>Tilordninge mal i dataintegrator

Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.

### <a name="contact-to-contact"></a>Kontakt til kontakt

![Tilordninge mal i dataintegrator](./media/contacts-template-mapping-data-integrator-1.png)

![Tilordne mal for kontakter i dataintegrator](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a>Kontakt til kunde

![Tilordninge mal i dataintegrator](./media/contacts-template-mapping-data-integrator-3.png)

![Tilordne mal for kontakter i dataintegrator](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a>Relaterte emner

[Synkronisere produkter fra Finance and Operations til produkter i Sales](products-template-mapping.md)

[Synkronisere kontoer fra Sales til kunder i Finance and Operations](accounts-template-mapping.md)

[Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations](sales-quotation-template-mapping.md)

[Synkronisere salgsordrehoder og -linjer fra Finance and Operations til Sales](sales-order-template-mapping.md)

[Synkronisere salgsfakturahoder og -linjer fra Finance and Operations til Sales](sales-invoice-template-mapping.md)

