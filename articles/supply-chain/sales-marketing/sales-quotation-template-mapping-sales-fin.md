---
title: Synkronisere salgstilbudshoder og -linjer direkte fra Sales til Finance and Operations
description: Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgstilbudshoder og -linjer direkte fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations.
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
ms.openlocfilehash: efe943f5c874ed041ce7984272ebc19f57cca6ef
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "313802"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a>Synkronisere salgstilbudshoder og -linjer direkte fra Sales til Finance and Operations

[!include [banner](../includes/banner.md)]

Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere salgstilbudshoder og -linjer direkte fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> Før du kan bruke kundeemnet til kontanter løsning må du ha kjennskap til [Integrere data til Common Data Service for Apps](https://docs.microsoft.com/en-us/powerapps/administrator/data-integrator).

## <a name="data-flow-in-prospect-to-cash"></a>Dataflyt i Kundeemne til kontanter

Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Finance and Operations og Sales. Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data for kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales. Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Finance and Operations og Sales.

[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="template-and-tasks"></a>Mal og oppgaver

Følgende mal og underliggende oppgavene brukes til å synkronisere salgstilbudshoder og -linjer direkte fra Sales til Finance and Operations:

- **Navnet på malen i Dataintegrering:** Salgstilbud (Sales til Fin and Ops) – direkte
- **Navnet på oppgaven i Dataintegrasjonprosjektet**:

    - QuoteHeader
    - QuoteLine

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgstilbudshoder og -linjer kan inntreffe:

- Produkter (Fin and Ops til Sales) – direkte
- Kontoer (Sales til Fin and Ops) – direkte (hvis brukt)
- Kontakter til Kunder (Sales til Fin and Ops) – direkte (hvis brukt)

## <a name="entity-set"></a>Enhetssett

| Salg        | Finance and Operations     |
|--------------|----------------------------|
| Tilbud       | CDS-salgstilbudshode |
| QuoteDetails | CDS-salgstilbudslinjer  |

## <a name="entity-flow"></a>Enhetsflyt

Salgstilbud opprettes i Sales og synkroniseres til Finance and Operations.

Salgstilbud fra Sales synkroniseres bare hvis følgende betingelser er oppfylt:

- Alle tilbudsproduktene i salgstilbudet vedlikeholdes eksternt.
- Når du har klikket på **Aktiver tilbud**, er salgstilbudet aktivert.

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

Feltet **Har bare eksternt vedlikeholdte produkter** er lagt til **tilbudsenheten** for konsistent sporing av om salgstilbudet består av bare eksternt vedlikeholdes produkter. Hvis et salgstilbud har bare eksternt vedlikeholdte produkter, vedlikeholdes produktene i Finance and Operations. Dette kan garantere at du ikke prøver å synkronisere salgstilbudslinjer med produkter som er ukjent for Finance and Operations.

Alle tilbudsprodukter i salgstilbudet oppdateres med informasjon fra **Har bare eksternt vedlikeholdte produkter** fra salgstilbudshodet. Denne informasjonen finnes i feltet **Tilbud har bare eksternt vedlikeholdte produkter** på **QuoteDetails**-enheten.

En rabatt kan legges til tilbudsproduktet og vil bli synkronisert til Finance and Operations. Feltene **Rabatt**, **Gebyrer** og **Avgift** feltene på hodet kontrolleres av et oppsett i Finance and Operations. Dette oppsettet støtter for øyeblikket ikke integreringstilordning. I den gjeldende utformingen adminstreres og vedlikeholdes feltene **Pris**, **Rabatt**, **Gebyrer** og **Avgift** i Finance and Operations.

I Sales gjør løsningen at følgende felt er skrivebeskyttet, fordi verdiene ikke er synkronisert til Finance and Operations:

- Skrivebeskyttede felt i salgstilbudshodet: **Rabattprosent**, **Rabatt** og **Fraktbeløp**
- Skrivebeskyttede felt på tilbudsprodukter: **Mva**

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

Før salgstilbud synkroniseres, er det viktig at du oppdaterer innstillingene nedenfor.

### <a name="setup-in-sales"></a>Oppsett i salg

- Kontroller at tillatelser er definert for temaet som brukeren fra Sales-tilkoblingssett er tildelt til. Hvis du bruker demomstrasjonsdata, har brukeren vanligvis administratortilgang, men teamet har ikke administratortilgang. Hvis teamet ikke har administratortilgang når du kjører prosjektet fra Dataintegrering, vil du få en feilmelding om at hovedteamet mangler.

    Hvis du vil angi tillatelser for teamet, kan du gå til **Innstillinger** &gt; **Sikkerhet** &gt; **Team** og velge det aktuelle teamet. Velg **Administrer roller**, og velg deretter en rolle som har de ønskede tillatelsene, for eksempel **Systemansvarlig**.

- Gå til **Innstillinger** &gt; **Administrasjon** &gt; **Systeminnstillinger** &gt; **Salg**, og sørger for å bruke følgende innstillinger:

    - Alternativet **Bruk systemets priskalkuleringssystem** er satt til **Ja**.
    - Feltet **Rabattkalkuleringsmetode** er satt til **Linjeelement**.

### <a name="setup-in-the-data-integration-project"></a>Oppsett i Dataintegrasjonsprosjekt

#### <a name="quoteheader"></a>QuoteHeader

- Sørg for at nødvendig tilordning finnes for **Shipto\_country** til **DeliveryAddressCountryRegionISOCode**. I den tilordnede verdien kan du definere en standardverdi som brukes hvis verdien er tom. La venstre side være tom, og sett høyre side til ønsket land eller område. På denne måten kan har du ikke skrive inn landet eller området for nasjonale ordrer.

    Malverdien er en verditilordning der flere land eller områder er tilordnet, og der en tom verdi er verdien for **US**.

#### <a name="quoteline"></a>QuoteLine

- Kontroller at den nødvendige verditilordningen finnes for **SalesUnitSymbol** i Finance and Operations.
- Kontroller at de nødvendige enhetene er definert i Sales.

    En malverdi som har en verditilordningen er definert for **oumid.name** til **SalesUnitSymbol**.

- Valgfritt: Du kan legge til følgende tilordninger for å garantere at salgstilbudslinjene importeres til Finance and Operations hvis det finnes ingen standardinformasjon fra kunden eller produktet:

    - **SiteId** – et område er nødvendig for å generere tilbud og salgsordrelinjer i Finance and Operations. Det finnes ingen standardmalverdi for **SiteId**.
    - **WarehouseId** – et lager er nødvendig for å behandle tilbud og salgsordrelinjer i Finance and Operations. Det finnes ingen standardmalverdi for **WarehouseId**.

## <a name="template-mapping-in-data-integrator"></a>Tilordninge mal i dataintegrator

> [!NOTE]
> - Feltene **Rabatt**, **Gebyrer** og **Avgift** feltene kontrolleres av et sammensatt oppsett i Finance and Operations. Dette oppsettet støtter for øyeblikket ikke integreringstilordning. I den gjeldende utformingen håndteres feltene **Pris**, **Rabatt**, **Gebyrer** og **Avgift** av Finance and Operations.
> - Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke en del av standardtilordningene. Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.

Følgende illustrasjoner viser et eksempel på en tilordning av malen i dataintegratoren.

### <a name="quoteheader"></a>QuoteHeader

![Tilordninge mal i dataintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a>QuoteLine

![Tilordninge mal i dataintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a>Relaterte emner

[Kundeemne til kontanter](prospect-to-cash.md)

