---
title: Synkronisering av salgsordrer direkte mellom Sales og Supply Chain Management
description: Dette emnet drøfter maler og underliggende oppgaver som brukes til å kjøre synkronisering av salgsordrer direkte mellom Dynamics 365 Sales og Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: AnnBe
ms.date: 05/09/2019
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
ms.openlocfilehash: 7c8831203ae30991ff8acf1926aafc2d1839aeb2
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251276"
---
# <a name="synchronization-of-sales-orders-directly-between-sales-and-supply-chain-management"></a>Synkronisering av salgsordrer direkte mellom Sales og Supply Chain Management

[!include [banner](../includes/banner.md)]

Dette emnet drøfter maler og underliggende oppgaver som brukes til å kjøre synkronisering av salgsordrer direkte mellom Dynamics 365 Sales og Dynamics 365 Supply Chain Management.

## <a name="data-flow-in-prospect-to-cash"></a>Dataflyt i Kundeemne til kontanter

Løsningen Kundeemne til kontanter bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Supply Chain Management og Sales. Kundeemne til kontanter-maler som er tilgjengelige med Dataintegrering-funksjonen,tillater flyt av data for kontoer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellom Supply Chain Management og Sales. Illustrasjonen nedenfor viser hvordan dataene blir synkronisert mellom Supply Chain Management og Sales.

[![Dataflyt i Kundeemne til kontanter](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)

## <a name="templates-and-tasks"></a>Maler og oppgaver

Hvis du vil ha tilgang til de tilgjengelige malene, kan du åpne [administrasjonssenteret for PowerApps](https://preview.admin.powerapps.com/dataintegration). Velg **Prosjekter**, og velg deretter **Nytt prosjekt** til øverst til høyre for å velge offentlig maler.

Følgende maler og underliggende oppgavene brukes til å kjøre synkronisering av salgsordrer direkte mellom Sales og Supply Chain Management.

- **Navnet på malen i Dataintegrering**: 

    - Salgsordrer (Sales til Supply Chain Management) – direkte
    - Salgsordrer (Supply Chain Management til Sales) – direkte

- **Navnet på oppgaven i Dataintegrasjonprosjektet**:

    - OrderHeader
    - OrderLine

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgsfakturahoder og -linjer kan inntreffe:

- Produkter (Supply Chain Management til Sales) – direkte
- Kontoer (Sales til Supply Chain Management) – direkte (hvis brukt)
- Kontakter til Kunder (Sales til Supply Chain Management) – direkte (hvis brukt)

## <a name="entity-set"></a>Enhetssett

| Forsyningskjedeadministrasjon  | Salg             |
|-------------------------|-------------------|
| CDS-salgsordrehoder | Salgsordrer       |
| CDS-salgsordrelinjer   | Salgsordredetaljer |

## <a name="entity-flow"></a>Enhetsflyt

Salgsordrer opprettes i Sales og synkroniseres til Supply Chain Management når **Kjør prosjekt** utløses for et prosjekt basert på malen **Salgsordrer (Sales til Supply Chain Management) – direkte**. Du kan bare aktivere og synkronisere ordrer fra Sales hvis alle **Bestill produkter** består av produkter som vedlikeholdes eksternt. Det kan derfor ikke finnes innskrivingsprodukter. Når ordren er aktivert, blir salgsordren skrivebeskyttet i brukergrensesnittet. På dette tidspunktet utføres oppdateringene fra Supply Chain Management. Når ordren får statusen **Bekreftet**, kan et prosjekt basert på malen **Salgsordrer (Supply Chain Management til Sales) – direkte** brukes til å synkronisere oppdateringer eller fullføringsstatus fra Supply Chain Management til Sales.

Du trenger ikke opprette ordrer i Sales. Du kan opprette nye salgsordrer i Supply Chain Management i stedet. Når en salgsordre har statusen **Bekreftet**, synkroniseres den til Sales, som beskrevet i det forrige avsnittet.

I Supply Chain Management vil filtre i malen garanterer at kun relevante salgsordrer er inkludert i synkroniseringen:

- Både bestilling og fakturering av kunde på salgsordren må komme fra Sales for å inkluderes i synkroniseringen. I Supply Chain Management brukes feltene **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** til å filtrere salgsordrer fra dataenhetene.
- Salgsordren i Supply Chain Management må bekreftes. Kun bekreftede salgsordre eller salgsordre med høyere behandlingsstatus, for eksempel **Sendt** eller **Fakturert**, synkroniseres til Sales.
- Etter at en salgsordre er opprettet eller endret, må den satsvise jobben **Kalkuler salgstotaler** i Supply Chain Management kjøres. Bare salgsordrene der salgsttotalene er beregnet, blir synkronisert Sales.

## <a name="freight-tax"></a>Fraktavgift

Sales støtter ikke avgift på hodenivå fordi avgift lagres på linjenivå. For å støtte avgift på hodenivå fra Supply Chain Management, for eksempel fraktavgift, synkroniserer systemet avgift til Sales som et innskrivingsprodukt som heter **Fraktavgift**, og som har avgiftsbeløpet fra Supply Chain Management. På denne måten brukes standard prisberegningen i Sales for totalsummer, selv om det er avgift på hodenivå fra Supply Chain Management.

## <a name="discount-calculation-and-rounding"></a>Rabattberegning og -avrunding

Modellen for rabattberegningen i Sales er forskjellig fra modellen for rabattberegningen i Supply Chain Management. I Supply Chain Management kan det endelige rabattbeløpet på en salgslinje være resultatet av en kombinasjon av rabattbeløp og rabattprosenter. Hvis dette endelige rabattbeløpet deles på antallet på linjen, kan det forekomme avrunding. Denne avrunding blir imidlertid ikke tatt hensyn til hvis et avrundet per enhet-rabattbeløp synkroniseres til Sales. For å garantere at hele rabattbeløpet fra en salgslinje i Supply Chain Management synkroniseres riktig med Sales, må hele beløpet synkroniseres uten at det blir delt på linjeantallet. Derfor må du definere **Rabattkalkuleringsmetode** som **Linjeelement** i Sales.

Når en salgsordrelinje synkroniseres fra Sales til Supply Chain Management, brukes hele linjerabattbeløpet. Supply Chain Management har ingen felt som kan lagre fullstendige rabattbeløpet for en linje, og beløpet deles derfor på antallet og lagres i feltet **Linjerabatt**. Avrunding som forekommer i denne delingen lagres i feltet **Salgstillegg** på salgslinjen.

### <a name="example"></a>Eksempel

**Synkronisering fra Sales til Supply Chain Management**

- **Sales**: Antall = 3, per linjerabatt = $ 10,00
- **Supply Chain Management:** Antall = 3, linjerabattbeløp = $ 3,33, salgstillegg = -$ 0,01 

**Synkronisering fra Supply Chain Management til Sales**

- **Supply Chain Management:** Antall = 3, linjerabattbeløp = $ 3,33, salgstillegg = -$ 0,01
- **Sales**: Antall = 3, per linjerabatt = = (3 × $ 3,33) + $ 0,01 = $ 10,00

## <a name="prospect-to-cash-solution-for-sales"></a>Kundeemnet til kontanter løsning for Sales

Nye felt er lagt til enheten **Ordre** og vises på siden:

- **Vedlikeholdes eksternt** – Sett dette alternativet til **Ja** når ordren kommer fra Supply Chain Management.
- **Behandlingsstatus** – Dette feltet viser behandlingsstatus for en ordre i Supply Chain Management. Følgende verdier er tilgjengelige:

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

Innstillingen **Har bare eksternt vedlikeholdte produkter** brukes under ordreaktivering for konsekvent sporing av om en salgsordre består av bare eksternt vedlikeholdes produkter. Hvis en salgsordre består av bare eksternt vedlikeholdte produkter, vedlikeholdes produktene i Supply Chain Management. Denne innstillingen kan garantere at du ikke aktiverer og prøver å synkronisere salgsordrelinjer med produkter som er ukjent for Supply Chain Management.

Knappene **Opprett faktura**, **Avbryt ordre**, **Omberegn**, **Få produkter** og **Søk opp adresser** på siden **Salgsordre** er skjult for eksternt behandlede ordrer fordi fakturaer vil opprettes i Supply Chain Management og synkronisert til Sales. Disse ordrene kan ikke redigeres fordi salgsordreinformasjon vil bli synkronisert fra Supply Chain Management etter aktivering.

Salgsordrestatus vil fortsatt være **Aktiv** for å garantere at endringer fra Supply Chain Management kan flyte fra salgsordren i Sales. Dette kontrolleres ved å sette standardverdien **Statuskode \[Status\]** til **Aktiv** i Dataintegrasjonsprosjektet.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

Før du synkroniserer salgsordrer, er det viktig å oppdatere innstillingene nedenfor i systemene.

### <a name="setup-in-sales"></a>Oppsett i salg

- Kontroller at tillatelser er definert for temaet som brukeren fra Sales-tilkoblingssett er tildelt til. Hvis du bruker demomstrasjonsdata, har brukeren vanligvis administratortilgang, men teamet har ikke administratortilgang. Hvis teamet ikke har administratortilgang når du kjører prosjektet fra Dataintegrering, vil du få en feilmelding om at hovedteamet mangler.

    Gå til **Innstillinger** &gt; **Sikkerhet** &gt; **Team**, velg relevant team. velg **Administrer roller** og velg en rolle med ønskede tillatelser, for eksempel **Systemadministrator**.

- For å sørge for korrekt beregning av rabatter i Sales og Supply Chain Management, må **Rabattkalkuleringsmetode** være satt til **Linjeelement**.
- Gå til **Innstillinger** &gt; **Administrasjon** &gt; **Systeminnstillinger** &gt; **Salg**, og sørger for å bruke følgende innstillinger:

    - Alternativet **Bruk systemets priskalkuleringssystem** er satt til **Ja**.
    - Feltet **Rabattkalkuleringsmetode** er satt til **Linjeelement**.

### <a name="setup-in-supply-chain-management"></a>Oppsett i Supply Chain Management

- Gå til **Salg og markedsføring** &gt; **Periodiske oppgaver** &gt; **Beregn salgstotaler**, og angi at jobben skal kjøres som en satsvis jobb. Sett alternativet **Beregnede totaler for salgsordrer** til **Ja**. Dette trinnet er viktig fordi kun salgsordre med kalkulerte totale salg vil synkroniseres til Sales. Hyppigheten av den satsvise jobben skal være justert med hyppigheten av salgsordensynkroniseringen.

Hvis du også bruker arbeidsordreintegrering, må du definere salgsopprinnelsen. Salgsopprinnelsen brukes til å skille salgsordrer i Supply Chain Management som ble opprettet fra arbeidsorder i Field Service. Når en salgsordre har en salgsopprinnelse av typen **Arbeidsordreintegrasjon**, vises **Ekstern arbeidsordrestatus**-feltet i salgsordrehodet. I tillegg kan salgsopprinnelsen sikre at salgsordrer som ble opprettet fra arbeidsorder i Field Service, filtreres ut under synkronisering av salgsordrer fra Supply Chain Management til Field Service.

1. Gå til **Salg og markedsføring** \> **Oppsett** \> **Salgsorder** \> **Salgsopprinnelse**.
2. Velg **Ny** for å opprette en ny salgsopprinnelse.
3. I **Salgsopprinnelse**-feltet angir du et navn for salgsopprinnelsen, for eksempel **Salgsordre**.
4. I **Beskrivelse**-feltet skriver du inn en beskrivelse, for eksempel **Salgsordre fra Sales**.
5. Merk av for **Tilordning av opprinnelsestype**.
6. Sett **Salgsopprinnelsestype**-feltet til **Integrering av salgsordre**.
7. Velg **Lagre**.

### <a name="setup-in-the-sales-orders-sales-to-supply-chain-management---direct-data-integration-project"></a>Oppsett i Salgsordrer (Sales til Supply Chain Management) – direkte Dataintegrasjonsprosjekt

- Sørg for at nødvendig tilordning finnes for **Shipto\_country** til **DeliveryAddressCountryRegionISOCode**. Du kan gjøre tom til standardverdi i verditilordningen for å slippe å skrive inn land for nasjonale ordrer. Sett venstre side til "Tom", og høyre side til ønsket land eller område.

    Malverdien er en verditilordning der flere land eller områder er tilordnet, og der "Tom" = US.

### <a name="setup-in-the-sales-orders-supply-chain-management-to-sales---direct-data-integration-project"></a>Oppsett i Salgsordrer (Supply Chain Management til Sales) – direkte Dataintegrasjonsprosjekt

#### <a name="salesheader-task"></a>Salgshode-oppgave

- En prisliste er nødvendig for å opprette ordrer i Sales. Oppdater verditilordningen for **pricelevelid.name \[Prislistenavn\]** til prislisten som brukes i Sales per valuta. Du kan bruke standard prisliste for en enkelt valuta. Hvis du har prislister i flere valutaer, kan du også bruke en verditilordning.

    Standard malverdi for **pricelevelid.name \[Prislistenavn\]** er **CRM Service USA (prøve)**.

#### <a name="salesline-task"></a>Salgslinje-oppgave

- Kontroller at den nødvendige verditilordningen finnes for **SalesUnitSymbol** i Supply Chain Management.
- Kontroller at de nødvendige enhetene er definert i Sales.

    En malverdi som har en verditilordningen er definert for **SalesUnitSymbol** til **oumid.name**.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

> [!NOTE]
> Feltene **Betalingsbetingelser**, **Fraktvilkår**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringsmåte** er ikke en del av standardtilordningene. Hvis du vil tilordne disse feltene, må du definere en verditilordning som er spesifikk for dataene i organisasjoner som enheten synkroniseres mellom.

Følgende illustrasjoner viser et eksempel på en tilordning av malen i Dataintegrering.

> [!NOTE]
> Tilordningen viser hvilken feltinformasjon som vil bli synkronisert fra Sales til Supply Chain Management eller fra Supply Chain Management til Sales.

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderheader"></a>Salgsordrer (Supply Chain Management til Sales) – direkte: OrderHeader

[![Maltilordning i Dataintegrering](./media/sales-order-direct-template-mapping-data-integrator-1.png)](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="sales-orders-supply-chain-management-to-sales---direct-orderline"></a>Salgsordrer (Supply Chain Management til Sales) – direkte: OrderLine

[![Maltilordning i Dataintegrering](./media/sales-order-direct-template-mapping-data-integrator-2.png)](./media/sales-order-direct-template-mapping-data-integrator-2.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderheader"></a>Salgsordrer Sales til (Supply Chain Management) – direkte: OrderHeader

[![Maltilordning i Dataintegrering](./media/sales-order-direct-template-mapping-data-integrator-3.png)](./media/sales-order-direct-template-mapping-data-integrator-3.png)

### <a name="sales-orders-sales-to-supply-chain-management---direct-orderline"></a>Salgsordrer (Sales til Supply Chain Management) – direkte: OrderLine

[![Maltilordning i Dataintegrering](./media/sales-order-direct-template-mapping-data-integrator-4.png)](./media/sales-order-direct-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a>Relaterte emner

[Kundeemne til kontanter](prospect-to-cash.md)
