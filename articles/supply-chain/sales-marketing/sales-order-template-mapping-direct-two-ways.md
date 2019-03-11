---
title: Synkronisere salgsordrer direkte mellom Sales og Finance and Operations
description: Dette emnet drøfter maler og underliggende oppgaver som brukes til å kjøre synkronisering av salgsordrer direkte mellom Microsoft Dynamics 365 for Sales og Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 10/11/2018
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
ms.openlocfilehash: 985a5a908308bc2268b80e8eef7117fdd6d54af6
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "339125"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-finance-and-operations"></a>Synkronisering av salgsordrer direkte mellom Sales og Finance and Operations

[!include [banner](../includes/banner.md)]

Dette emnet drøfter maler og underliggende oppgaver som brukes til å kjøre synkronisering av salgsordrer direkte mellom Microsoft Dynamics 365 for Sales og Microsoft Dynamics 365 for Finance and Operations.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflyt i Kundeemne til kontanter

Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Finance and Operations og Sales. Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data for kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Finance and Operations og Sales. Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Finance and Operations og Sales.

[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for PowerApps](https://preview.admin.powerapps.com/dataintegration). Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.

Følgende maler og underliggende oppgavene brukes til å kjøre synkronisering av salgsordrer direkte mellom Sales og Finance and Operations:

- **Navnet på malen i Dataintegrering**: 

    - Salgsordrer (Sales til Fin and Ops) – direkte
    - Salgsordrer (Fin and Ops til Sales) – direkte

- **Navnet på oppgaven i Dataintegrasjonprosjektet**:

    - OrderHeader
    - OrderLine

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgsfakturahoder og -linjer kan inntreffe:

- Produkter (Fin and Ops til Sales) – direkte
- Kontoer (Sales til Fin and Ops) – direkte (hvis brukt)
- Kontakter til Kunder (Sales til Fin and Ops) – direkte (hvis brukt)

## <a name="entity-set"></a>Enhetssett

| Finance and Operations  | Salg             |
|-------------------------|-------------------|
| CDS-salgsordrehoder | Salgsordrer       |
| CDS-salgsordrelinjer   | Salgsordredetaljer |

## <a name="entity-flow"></a>Enhetsflyt

Salgsordrer opprettes i Sales og synkroniseres til Finance and Opereations når **Kjør prosjekt** utløses for et prosjekt basert på malen **Salgsordrer (Fin and Ops til Sales) – direkte**. Du kan bare aktivere og synkronisere ordrer fra Sales hvis alle **Bestill produkter** består av produkter som vedlikeholdes eksternt. Det kan derfor ikke finnes innskrivingsprodukter. Når ordren er aktivert, blir salgsordren skrivebeskyttet i brukergrensesnittet. På dette tidspunktet utføres oppdateringene fra Finance and Operations. Når ordren får statusen **Bekreftet**, kan et prosjekt basert på malen **Salgsordrer (Fin and Ops til Sales) – direkte** brukes til å synkronisere oppdateringer eller fullføringsstatus fra Finance and Operations til Sales.

Du trenger ikke opprette ordrer i Sales. Du kan opprette nye salgsordrer i Finance and Operations i stedet. Når en salgsordre har statusen **Bekreftet**, synkroniseres den til Sales, som beskrevet i det forrige avsnittet.

I Finance and operations vil filtre i malen garanterer at kun relevante salgsordrer er inkludert i synkroniseringen:

- Både bestilling og fakturering av kunde på salgsordren må komme fra Sales for å inkluderes i synkroniseringen. I Finance and Operations brukes feltene **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** til å filtrere salgsordrer fra dataenhetene.
- Salgsordren i Finance and Operations må bekreftes. Kun bekreftede salgsordre eller salgsordre med høyere behandlingsstatus, for eksempel **Sendt** eller **Fakturert**, synkroniseres til Sales.
- Etter at en salgsordre er opprettet eller endret, må den satsvise jobben **Kalkuler salgstotaler** i Finance and Operations kjøres. Bare salgsordrene der salgsttotalene er beregnet, blir synkronisert Sales.

## <a name="freight-tax"></a>Fraktavgift

Sales støtter ikke avgift på hodenivå fordi avgift lagres på linjenivå. For å støtte avgift på hodenivå fra Finance and Operations, for eksempel fraktavgift, synkroniserer systemet avgift til Sales som et innskrivingsprodukt som heter **Fraktavgift**, og som har avgiftsbeløpet fra Finance and Operations. På denne måten brukes standard prisberegningen i Sales for totalsummer, selv om det er avgift på hodenivå fra Finance and Operations.

## <a name="discount-calculation-and-rounding"></a>Rabattberegning og -avrunding

Modellen for rabattberegningen i Sales er forskjellig fra modellen for rabattberegningen i Finance and Operations. I Finance and Operations kan det endelige rabattbeløpet på en salgslinje være resultatet av en kombinasjon av rabattbeløp og rabattprosenter. Hvis dette endelige rabattbeløpet deles på antallet på linjen, kan det forekomme avrunding. Denne avrunding blir imidlertid ikke tatt hensyn til hvis et avrundet per enhet-rabattbeløp synkroniseres til Sales. For å garantere at hele rabattbeløpet fra en salgslinje i Finance and Operations synkroniseres riktig med Sales, må hele beløpet synkroniseres uten at det blir delt på linjeantallet. Derfor må du definere **Rabattkalkuleringsmetode** som **Linjeelement** i Sales.

Når en salgsordrelinje synkroniseres fra Sales til Finance and Operations, brukes hele linjerabattbeløpet. Finance and Operations har ingen felt som kan lagre fullstendige rabattbeløpet for en linje, og beløpet deles derfor på antallet og lagres i feltet **Linjerabatt**. Avrunding som forekommer i denne delingen lagres i feltet **Salgstillegg** på salgslinjen.

### <a name="example"></a>Eksempel

**Synkronisere fra Sales til Finance and Operations**

- **Sales**: Antall = 3, per linjerabatt = $ 10,00
- **Finance and Operations**: Antall = 3, Linjerabattbeløp = $ 3,33, salgstillegg =-$ 0,01 

**Synkronisere fra Finance and Operations til Sales**

- **Finance and Operations**: Antall = 3, Linjerabattbeløp = $ 3,33, salgstillegg =-$ 0,01
- **Sales**: Antall = 3, per linjerabatt = = (3 × $ 3,33) + $ 0,01 = $ 10,00

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

Nye felt er lagt til enheten **Ordre** og vises på siden:

- **Er behandlet eksternt** – Sett dette alternativet til **Ja** når ordren kommer fra Finance and Operations.
- **Behandlingsstatus** – Dette feltet viser behandlingsstatus for en ordre i Finance and Operations. Følgende verdier er tilgjengelige:

    - **Utkast** – Startstatus når en ordre blir opprettet i Sales. I Sales kan du redigere ordrer med denne behandlingsstatusen.
    - **Aktiv** – Status etter at ordren er aktivert i Sales ved hjelp av **Aktiver**-knappen.
    - **Bekreftet**
    - **Følgeseddel**
    - **Fakturert**
    - **Plukket**
    - **Delvis plukket**
    - **Delvis pakket**
    - **Sendt**
    - **Delvis sendt**
    - **Delvis fakturert**
    - **Avbrutt**

Innstillingen **Har bare eksternt vedlikeholdte produkter** brukes under ordreaktivering for konsekvent sporing av om en salgsordre består av bare eksternt vedlikeholdes produkter. Hvis en salgsordre består av bare eksternt vedlikeholdte produkter, vedlikeholdes produktene i Finance and Operations. Denne innstillingen kan garantere at du ikke aktiverer og prøver å synkronisere salgsordrelinjer med produkter som er ukjent for Finance and Operations.

Knappene **Opprett faktura**, **Avbryt ordre**, **Rekalkuler**, **Få produkter** og **Søk opp adresser** på siden **Salgsordre** er skjult for eksternt behandlede ordrer fordi fakturaer vil opprettes i Finance and Operations og synkronisert til Sales. Disse ordrene kan ikke redigeres fordi salgsordreinformasjon vil bli synkronisert fra Finance and Operations etter aktivering.

Salgsordrestatus vil fortsatt være **Aktiv** for å garantere at endringer fra Finance and Operations kan flyte fra salgsordren i Sales. Dette kontrolleres ved å sette standardverdien **Statuskode \[Status\]** til **Aktiv** i Dataintegrasjonsprosjektet.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

Før du synkroniserer salgsordrer, er det viktig å oppdatere innstillingene nedenfor i systemene.

### <a name="setup-in-sales"></a>Oppsett i salg

- Kontroller at tillatelser er definert for temaet som brukeren fra Sales-tilkoblingssett er tildelt til. Hvis du bruker demomstrasjonsdata, har brukeren vanligvis administratortilgang, men teamet har ikke administratortilgang. Hvis teamet ikke har administratortilgang når du kjører prosjektet fra Dataintegrering, vil du få en feilmelding om at hovedteamet mangler.

    Gå til **Innstillinger** &gt; **Sikkerhet** &gt; **Team**, velg relevant team. velg **Administrer roller** og velg en rolle med ønskede tillatelser, for eksempel **Systemadministrator**.

- For å sørge for korrekt beregning av rabatter i Sales og Finance and Operations, må **Rabattkalkuleringsmetode** være satt til **Linjeelement**.
- Gå til **Innstillinger** &gt; **Administrasjon** &gt; **Systeminnstillinger** &gt; **Salg**, og sørger for å bruke følgende innstillinger:

    - Alternativet **Bruk systemets priskalkuleringssystem** er satt til **Ja**.
    - Feltet **Rabattkalkuleringsmetode** er satt til **Linjeelement**.

### <a name="setup-in-finance-and-operations"></a>Oppsett i Finance and Operations

- Gå til **Salg og markedsføring** &gt; **Periodiske oppgaver** &gt; **Beregn salgstotaler**, og angi at jobben skal kjøres som en satsvis jobb. Sett alternativet **Beregnede totaler for salgsordrer** til **Ja**. Dette trinnet er viktig fordi kun salgsordre med kalkulerte totale salg vil synkroniseres til Sales. Hyppigheten av den satsvise jobben skal være justert med hyppigheten av salgsordensynkroniseringen.

### <a name="setup-in-the-sales-orders-sales-to-fin-and-ops---direct-data-integration-project"></a>Oppsett i Salgsordrer (Sales til Fin and Ops) – direkte Dataintegrasjonsprosjekt

- Sørg for at nødvendig tilordning finnes for **Shipto\_country** til **DeliveryAddressCountryRegionISOCode**. Du kan gjøre tom til standardverdi i verditilordningen for å slippe å skrive inn land for nasjonale ordrer. Sett venstre side til "Tom", og høyre side til ønsket land eller område.

    Malverdien er en verditilordning der flere land eller områder er tilordnet, og der "Tom" = US.

### <a name="setup-in-the-sales-orders-fin-and-ops-to-sales---direct-data-integration-project"></a>Oppsett i Salgsordrer (Fin and Ops til Sales) – direkte Dataintegrasjonsprosjekt

#### <a name="salesheader-task"></a>Salgshode-oppgave

- En prisliste er nødvendig for å opprette ordrer i Sales. Oppdater verditilordningen for **pricelevelid.name \[Prislistenavn\]** til prislisten som brukes i Sales per valuta. Du kan bruke standard prisliste for en enkelt valuta. Hvis du har prislister i flere valutaer, kan du også bruke en verditilordning.

    Standard malverdi for **pricelevelid.name \[Prislistenavn\]** er **CRM Service USA (prøve)**.

#### <a name="salesline-task"></a>Salgslinje-oppgave

- Kontroller at den nødvendige verditilordningen finnes for **SalesUnitSymbol** i Finance and Operations.
- Kontroller at de nødvendige enhetene er definert i Sales.

    En malverdi som har en verditilordningen er definert for **SalesUnitSymbol** til **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

> [!NOTE]
> Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke en del av standardtilordningene. Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.

Følgende illustrasjoner viser et eksempel på en tilordning av malen i Dataintegrering.

> [!NOTE]
> Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Finance and Operations, eller fra Finance and Operations til Sales.

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderheader"></a>Salgsordrer (Fin and Ops til Sales) – direkte: OrderHeader

[![Maltilordning i Dataintegrering](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-fin-and-ops-to-sales---direct-orderline"></a>Salgsordrer (Fin and Ops til Sales) – direkte: OrderLine

[![Maltilordning i Dataintegrering](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderheader"></a>Salgsordrer (Sales til Fin and Ops) – direkte: OrderHeader

[![Maltilordning i Dataintegrering](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-fin-and-ops---direct-orderline"></a>Salgsordrer (Sales til Fin and Ops) – direkte: OrderLine

[![Maltilordning i Dataintegrering](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Relaterte emner

[Kundeemne til kontanter](prospect-to-cash.md)
