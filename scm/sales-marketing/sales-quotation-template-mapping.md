---
title: Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations
description: "Emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere salgstilbudshoder og -linjer fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition."
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
ms.openlocfilehash: 172a3da1b6d90a25ea9ebd14265e70e4a6f9bd70
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a>Synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations

[!include[banner](../includes/banner.md)]

> [!NOTE]
> Før du kan bruke kundeemnet til kontanter løsning, ha kjennskap til [Dynamics 365 dataintegrering](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration). 

Emnet beskriver malene og underliggende oppgavene som brukes til å synkronisere salgstilbudshoder og -linjer fra Microsoft Dynamics 365 for Sales (Sales) til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations). 

## <a name="template-and-tasks"></a>Mal og oppgaver

Følgende malene og underliggende oppgavene brukes til å synkronisere salgstilbudshoder og -linjer fra Sales til Finance and Operations:

- **Navnet på malen:** Salgstilbud (Sales til Finance and Operations)
- **Navnene på oppgavene i prosjektet:**

    - QuoteHeader
    - QuoteLine

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgstilbudshoder og -linjer kan inntreffe:

- Produkter
- Kontoer (hvis brukt)
- Kontakter (hvis brukt)

## <a name="entity-set"></a>Enhetssett

| Salg        | CDS           | Finance and Operations    |
|--------------|---------------|---------------------------|
| Tilbud       | Tilbud     | Salgstilbudshoder   |
| QuoteDetails | QuotationLine | CDS-salgstilbudslinjer |

## <a name="entity-flow"></a>Enhetsflyt

Salgstilbud opprettes i Sales og synkroniseres til Finance and Operations.

Salgstilbud fra Sales synkroniseres bare hvis følgende betingelser er oppfylt:

- Alle produktene i salgstilbudslinjene vedlikeholdes eksternt.
- Salgstilbudet er aktivt eller aktivert.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

Feltet **Har bare eksternt vedlikeholdte produkter** er lagt til tilbudsenheten for konsistent sporing av om salgstilbudet består av bare eksternt vedlikeholdes produkter. Hvis et salgstilbud har bare eksternt vedlikeholdte produkter, vedlikeholdes produktene i Finance and Operations. Dette kan garantere at du ikke prøver å synkronisere salgstilbudslinjer med produkter som er ukjent for Finance and Operations.

Alle produkter og linjer i tilbudet oppdateres med informasjon fra **Har bare eksternt vedlikeholdte produkter** fra tilbudshodet. Denne informasjonen finnes i feltet **Tilbud har bare eksternt vedlikeholdte produkter** på tilbudslinjeenheten.

Feltene **Rabatt**, **Gebyrer** og **Avgift** feltene kontrolleres av et sammensatt oppsett i Finance and Operations. Dette oppsettet støtter for øyeblikket ikke integreringstilordning. I den gjeldende utformingen adminstreres og håndteres feltene **Pris**, **Rabatt**, **Gebyrer** og **Avgift** av Finance and Operations.

I Sales gjør løsningen at følgende felt er skrivebeskyttet, fordi verdiene ikke er synkronisert til Finance and Operations:

- **Skrivebeskyttede felt i salgstilbudshodet:** Rabattprosent, Rabatt, Fraktbeløp
- **Skrivebeskyttede felt på salgstilbudslinjer:** Mva

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

- Før du synkroniserer salgstilbud kan du i Sales gå til **Innstillinger** &gt; **Administrasjon** &gt; **Systeminnstillinger** &gt; **Salg** og kontrollere at feltet **Rabattberegningsmetode** er angitt til **Per enhet**. Denne innstillingen garanterer at linjevarerabatten fra Sales samsvarer med innstillingen i Finance and Operations. Ellers blir ikke rabatten riktig i Finance and Operations, fordi Finance and Operations leser rabatten som en rabatt per enhet, selv om det var en rabatt per linje i Sales.
- I Finance and Operations går du til **Kunder** &gt; **Oppsett** &gt; **Kundeparametere**. På kategorien **Nummerserie** velger du nummerserien for salgstilbud og klkker deretter **Vis detaljer**. Deretter, under **Generelt oppsett**, angis feltet **Manuelt** til **Ja**.
- I Finance and Operations går du til **Kunder** &gt; **Oppsett** &gt; **Kundeparametere**. På kategorien **Forsendelser** angir du feltet **Leveringsdatokontroll** til **Ingen**. Denne innstillingen forhindrer synkronisering fra å mislykkes for salgstilbud.

### <a name="quoteheader"></a>QuoteHeader

- Feltet **Ønsket leveringsdato** kreves i Finance and Operations, og synkroniseringen mislykkes hvis feltet er tomt. For å unngå dette problemet, hentes en standarddato fra **Kilde &gt; CDS** hvis feltet er tomt. Datoen bør oppdateres til en ønsket verdi. For øyeblikket ikke kan du angi en verdi som **I dag** for å representere dagens dato. Du må angi en spesifikk dato. Standardmalverdien for **Ønsket leveringsdato** er **1/1/2020**.
- Feltet **Kode for adresse, land og område** er obligatorisk i Finance and Operations. For å forhindre synkroniseringsfeil, kan du angi en standardverdi som skal brukes hvis feltet er tomt i Sales. Denne standardverdien er også nyttig, fordi du ikke trenger for å skrive inn en verdi i feltet **Land område** for lokale adresser. Det finnes ingen standardmalverdi for **DeliveryAddressCountryRegionISOCode**.
- Oppdater tilordningen for **ID for CDS-organisasjon** i **Kilden &gt; CDS**, slik at den samsvarer med **CDS-organisasjon** i organisasjonsenheten:

    - Standardmalverdien for **Organization_OrganizationId** er **ORG001**.
    - Standardmalverdien for **Account_Organization_OrganizationId** er **ORG001**.
    - Standardmalverdien for **InvoiceAccount_OrganizationId** er **ORG001**.

### <a name="quoteline"></a>QuoteLine

- Oppdater tilordningen for **ID for CDS-organisasjon** i **Kilden &gt; CDS**, slik at den samsvarer med **CDS-organisasjon** i organisasjonsenheten:

    - Standardmalverdien for **Organization_OrganizationId** er **ORG001**.
    - Standardmalverdien for **Product_Organization_Organization_OrganizationId** er **ORG001**.
    - Standardmalverdien for **Quotation_Organization_Organization_OrganizationId** er **ORG001**.

- Feltet **Ønsket leveringsdato** kreves i Finance and Operations, og synkroniseringen mislykkes hvis feltet er tomt. For å unngå dette problemet, hentes en standarddato fra **Kilde &gt; CDS** hvis feltet er tomt. Datoen bør oppdateres til en ønsket verdi. For øyeblikket ikke kan du angi en verdi som **I dag** for å representere dagens dato. Du må angi en spesifikk dato. Standardmalverdien for **Ønsket leveringsdato** er **1/1/2020**.
- Du kan legge til følgende tilordninger fra **CDS &gt; Mål** for å garantere at tilbudslinjene importeres til Finance and Operations hvis det finnes ingen standardinformasjon fra kunden eller produktet:

    - **SiteId** – et område er nødvendig for å generere tilbud og salgsordrelinjer i Finance and Operations. Det finnes ingen standardmalverdi for **SiteId**.
    - **WarehouseId** – et lager er nødvendig for å behandle tilbud og salgsordrelinjer i Finance and Operations. Det finnes ingen standardmalverdi for **WarehouseId**.

- Pass på at den nødvendige verditilordningen for selgende måleenheten i Finance and Operations finnes i tilordnignen **CDS &gt; Mål** for **Quantity_UOM** til **SALESUNITSYMBOL**.

## <a name="template-mapping-in-data-integrator"></a>Tilordninge mal i dataintegrator

> [!NOTE]
> - Feltene **Rabatt**, **Gebyrer** og **Avgift** feltene kontrolleres av et sammensatt oppsett i Finance and Operations. Dette oppsettet støtter for øyeblikket ikke integreringstilordning. I den gjeldende utformingen håndteres feltene **Pris**, **Rabatt**, **Gebyrer** og **Avgift** av Finance and Operations.
> - Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke en del av standardtilordningene. Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.

Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.

### <a name="quoteheader"></a>QuoteHeader

![Tilordninge mal i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Tilordninge mal i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a>QuoteLine

![Tilordninge mal i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Tilordninge mal i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Relaterte emner

[Synkronisere produkter fra Finance and Operations til produkter i Sales](products-template-mapping.md)

[Synkronisere kontoer fra Sales til kunder i Finance and Operations](accounts-template-mapping.md)

[Synkronisere kontakter fra Sales til kontakter eller kunder i Finance and Operations](contacts-template-mapping.md)



