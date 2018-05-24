---
title: Synkronisere arbeidsordrer i Field Service til salgsordrer i Finance and Operations
description: "Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere arbeidsordrer i Field Service til salgsordrer i Finance and Operations."
author: ChristianRytt
manager: AnnBe
ms.date: 04/09/2018
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
ms.sourcegitcommit: ace66c037953f4b1b2e8b93a315faefdb090b1eb
ms.openlocfilehash: 933d9755085d507310dd46d96a492d2124647ec3
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-finance-and-operations"></a>Synkronisere arbeidsordrer i Field Service til salgsordrer i Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet drøfter maler og underliggende oppgaver som brukes til å synkronisere arbeidsordrer i Microsoft Dynamics 365 for Field Service til salgsorder i Microsoft Dynamics 365 for Finance and Operations.

[![Synkronisering av forretningsprosesser mellom Finance and Operations og Field Service](./media/field-service-integration.png)](./media/field-service-integration.png)

Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere arbeidsordrer i Field Service til salgsordrer i Finance and Operations.

## <a name="templates-and-tasks"></a>Maler og oppgaver

De følgende malene og de underliggende oppgavene brukes til å utføre synkroniseringen av arbeidsordrer i Field Service til salgsordrer i Finance and Operations.

### <a name="names-of-the-templates-in-data-integration"></a>Navn på malene i Dataintegrering

**Arbeidsordrer til salgsordrer (Field Service til Fin and Ops)**-malen brukes til å utføre synkronisering.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Navnet på oppgaven i Dataintegrasjonprosjektet

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgsordrehoder og -linjer kan inntreffe:

- Field Service-produkter (Fin and Ops til Field Service)
- Kontoer (Sales til Fin and Ops) – direkte

## <a name="entity-set"></a>Enhetssett

| **Field Service** | **Finance and Operations** |
|-------------------------|-------------------------|
| msdyn_workorders        | CDS-salgsordrehoder |
| msdyn_workorderservices | CDS-salgsordrelinjer   |
| msdyn_workorderproducts | CDS-salgsordrelinjer   |

## <a name="entity-flow"></a>Enhetsflyt

Arbeidsordrer opprettes i Field Service. Hvis arbeidsordene inkluderer bare eksternt vedlikeholdte produkter, og hvis **Arbeidsordrestatus**-verdien er forskjellig fra **Åpen – uplanlagt** og **Lukket – avbrutt**, kan arbeidsordrene synkroniseres til Finance and Operations via et CDS-dataintegreringsprosjekt. Oppdateringer av arbeidsordene synkroniseres som salgsordrer i Finance and Operations. Disse oppdateringene inneholder informasjon om opprinnelsestypen og status.

## <a name="estimated-versus-used"></a>Estimert kontra brukt

I Field Service har produkter og tjenester på arbeidsordrer både **Estimert**-verdier og **Brukt**-verdier for antall og beløp. I Finance and Operations derimot har ikke salgsordrer det samme konseptet for **Estimert**- og **Brukt**-verdier. For å støtte produkttilordning som bruker det forventede antallet på salgsordren i Finance and Operations, men for å beholde det brukte antallet som skal brukes og faktureres, synkroniserer to sett med oppgaver produktene og tjenestene på arbeidsordren. Ett sett med oppgaver for **Estimert**-verdier, og det andre settet med oppgaver for **Brukt**-verdier.

Dette gjør det mulig med scenarioer der estimerte verdier brukes for tildeling eller reservasjon i Finance and Operations, mens brukte verdier brukes for forbruk og fakturering.

### <a name="estimated"></a>Estimert

For synkronisering av produktserier brukes **Estimert**-verdier når **Linjestatus**-verdien er **Estimert**, **Tilordnet** er satt til **Ja** og **Systemstatus**-verdien ikke er **Lukket – bokført**.

For synkronisering av servicelinjer brukes **Estimert**-verdier når **Linjestatus**-verdien er **Estimert** og **Systemstatus**-verdien ikke er **Lukket – bokført**.

### <a name="used"></a>Brukt

**Brukes**-verdiene skal brukes for forbruk og fakturering. I disse tilfellene vil **Brukes**-verdiene synkroniseres.

Tabellen nedenfor gir en oversikt over de forskjellige kombinasjonene for produktlinjer.

| Systemstatus <br>(Field Service) | Linjestatus <br>(Field Service) | Tilordnet <br>(Field Service) |Synkroniseringsverdi <br>(Finance and Operations) |
|--------------------|-------------|-----------|---------------------------------|
| Åpen – planlagt   | Estimert   | Ja       | Estimert                       |
| Åpen – planlagt   | Estimert   | Antall        | Brukt                            |
| Åpen – planlagt   | Brukt        | Ja       | Brukt                            |
| Åpen – planlagt   | Brukt        | Antall        | Brukt                            |
| Åpen – pågår | Estimert   | Ja       | Estimert                       |
| Åpen – pågår | Estimert   | Antall        | Brukt                            |
| Åpen – pågår | Brukt        | Ja       | Brukt                            |
| Åpen – pågår | Brukt        | Antall        | Brukt                            |
| Åpne – fullført   | Estimert   | Ja       | Estimert                       |
| Åpne – fullført   | Estimert   | Antall        | Brukt                            |
| Åpne – fullført   | Brukt        | Ja       | Brukt                            |
| Åpne – fullført   | Brukt        | Antall        | Brukt                            |
| Lukket – postert    | Estimert   | Ja       | Brukt                            |
| Lukket – postert    | Estimert   | Antall        | Brukt                            |
| Lukket – postert    | Brukt        | Ja       | Brukt                            |
| Lukket – postert    | Brukt        | Antall        | Brukt                            |

Tabellen nedenfor gir en oversikt over de forskjellige kombinasjonene for servicelinjer.

| Systemstatus <br>(Field Service) | Linjestatus <br>(Field Service) | Synkroniseringsverdi <br>(Finance and Operations) |
|--------------------|-------------|-----------|
| Åpen – planlagt   | Estimert   | Estimert |
| Åpen – planlagt   | Brukt        | Brukt      |
| Åpen – pågår | Estimert   | Estimert |
| Åpen – pågår | Brukt        | Brukt      |
| Åpne – fullført   | Estimert   | Estimert |
| Åpne – fullført   | Brukt        | Brukt      |
| Lukket – postert    | Estimert   | Brukt      |
| Lukket – postert    | Brukt        | Brukt      |

Synkronisering av **Estimert**-verdier i forhold til **Brukt**-verdier behandles ved hjelp av to sett med oppgaver for produkt- og servicelinjer. Forhåndsdefinerte filtre utløser den riktige oppgaven, og den underliggende tilordningen sikrer at de riktige verdiene for **Forventet** og **Brukt** synkroniseres.

### <a name="example"></a>Eksempel

1. En arbeidsordre opprettes og planlegges i Field Service.

    **Systemstatus**-verdien er **Åpen – planlagt**.

    - **Produktlinje:** Estimert antall = 5ea, brukt antall = 0ea, linjestatus = estimert, tilordnet = Nei
    - **Servicelinje:** Estimert antall = 2h, brukt antall = 0h, linjestatus = estimert

    I dette eksemplet synkroniseres produktets **Brukt antall**-verdi **0** (null) og tjenestens **Estimert antall**-verdi **2h** til Finance and Operations.

2. Produkter tilordnes i Field Service.

    **Systemstatus**-verdien er **Åpen – planlagt**.

    - **Produktlinje:** Estimert antall = 5ea, brukt antall = 0ea, linjestatus = estimert, tilordnet = Ja
    - **Servicelinje:** Estimert antall = 2h, brukt antall = 0h, linjestatus = estimert

    I dette eksemplet synkroniseres produktets **Estimert antall**-verdi **5ea** og tjenestens **Estimert antall**-verdi **2h** til Finance and Operations.

3. Serviceteknikeren begynner å arbeide med arbeidsordren og registrerer materialforbruk på 6.

    **Systemstatus**-verdien er **Åpen – pågår**.

    - **Produktlinje:** Estimert antall = 5ea, brukt antall = 6ea, linjestatus = brukt, tilordnet = Ja
    - **Servicelinje:** Estimert antall = 2h, brukt antall = 0h, linjestatus = estimert

    I dette eksemplet synkroniseres produktets **Brukt antall**-verdi **6** og tjenestens **Estimert antall**-verdi **2h** til Finance and Operations.

4. Serviceteknikeren fullfører arbeidsordren og registrerer brukt tid på 1,5 time.

    **Systemstatus**-verdien er **Åpen – fullført**.

    - **Produktlinje:** Estimert antall = 5ea, brukt antall = 6ea, linjestatus = brukt, tilordnet = Ja
    - **Servicelinje:** Estimert antall = 2h, brukt antall = 1,5h, linjestatus = brukt

    I dette eksemplet synkroniseres produktets **Brukt antall**-verdi **6** og tjenestens **Estimert antall** på **1,5h** til Finance and Operations.

## <a name="sales-order-origin-and-status"></a>Salgsordreopprinnelse og -status

### <a name="sales-origin"></a>Salgsopprinnelse

Hvis du vil holde oversikt over salgsordrer i Finance and Operations som kommer fra arbeidsordrer, kan du opprette en salgsopprinnelse der **Tilordning av opprinnelsestype** er satt til **Ja** og **Salgsopprinnelsestype**-feltet er satt til **Integrering av arbeidsordre**.

Som standard velger tilordningen salgsopprinnelsen for salgsopprinnelsestypen **Integrering av arbeidsordre** som er opprettet fra arbeidsordrer. Dette kan være nyttig når du arbeider med salgsordren i Finance and Operations. Du må kontrollere at salgsordrer som stammer fra arbeidsordrer, ikke synkroniseres tilbake til Field Service som arbeidsordrer.

Hvis du vil ha mer informasjon om hvordan du oppretter riktig salgsopprinnelsesoppsett i Finance and Operations, kan du se delen Forutsetninger og tilordningsdefinisjon i dette emnet.

### <a name="status"></a>Status

Når salgsordren stammer fra en arbeidsordre, vises feltet **Status for ekstern arbeidsordre** i **Oppsett**-kategorien i salgsordrehodet. Dette feltet viser systemstatusen fra arbeidsordren i Field Service, for å spore statusen for synkronisert arbeidsordre for salgsordrer i Finance and Operations. Dette feltet kan også hjelpe brukeren av Finance and Operations å bestemme når salgsordren skal leveres eller faktureres.

**Status for ekstern arbeidsordre**-feltet kan ha følgende verdier:

- Åpen – planlagt
- Åpen – pågår
- Åpne – fullført
- Lukket – postert

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service

For å støtte integrasjon mellom Field Service og Finance and Operations, kreves det ekstra funksjonalitet fra Field Service CRM-løsningen. Løsningen inneholder følgende endringer.

### <a name="work-order-entity"></a>Arbeidsordreenhet

Feltet **Har bare eksternt vedlikeholdte produkter** er lagt til i **Arbeidsordre**-enheten og vises på siden. Det brukes til å spore om en arbeidsordre utelukkende består av eksternt vedlikeholdte produkter. En arbeidsordre består av bare eksternt vedlikeholdte produkter når alle relaterte produkter vedlikeholdes i Finance and Operations. Dette feltet sikrer at brukere ikke synkroniserer arbeidsordrer med produkter som er ukjent for Finance and Operations.

### <a name="work-order-product-entity"></a>Arbeidsordreproduktenhet

- Feltet **Ordre har bare eksternt vedlikeholdte produkter** er lagt til i **Arbeidsordreprodukt**-enheten og vises på siden. Det brukes til å spore om arbeidsordreproduktet vedlikeholdes i Finance and Operations. Dette feltet sikrer at brukere ikke synkroniserer arbeidsordreprodukter som er ukjent for Finance and Operations.
- Feltet **Hodesystemstatus** er lagt til i **Arbeidsordreprodukt**-enheten og vises på siden. Det brukes til å spore systemstatusen til arbeidsordren og hjelper med å garantere riktig filtrering når arbeidsordreprodukter synkroniseres til Finance and Operations. Når filtre er definert for integreringsoppgavene, brukes også **Hodesystemstatus**-informasjonen til å bestemme om estimert- eller brukt-verdiene skal synkroniseres.
- **Fakturert enhetsbeløp**-feltet viser beløpet som er fakturert per faktisk enhet som brukes. Verdien beregnes som **Totalbeløp**-verdien dividert med **Faktisk antall**-verdien. Feltet brukes for integrering til systemer som ikke støtter forskjellige verdier for det brukte antallet og det fakturerte antallet. Dette feltet vises ikke i brukergrensesnittet. 
- **Fakturert rabattbeløp**-feltet beregnes som **Rabattbeløp**-verdien pluss avrundingen fra beregningen av **Fakturert enhetsbeløp**-verdien. Dette feltet brukes for integrering og vises ikke i brukergrensesnittet.
- **Desimalantallet**-feltet lagrer verdien fra **Antall**-feltet som et desimaltall. Dette feltet brukes for integrering og vises ikke i brukergrensesnittet. 
- Verdien i **Brukt**-felt tilbakestilles til **0** (null) hvis **Linjestatus**-verdien for arbeidsordreproduktet endres fra **Brukt** til **Estimert**. Denne endringen bidrar til å hindre situasjoner der et bruk antall som er angitt ved en feiltakelse, brukes for synkronisering når **Linjestatus**-verdien er **Estimert** og **Tilordet**-alternativet er satt til **Nei**.

### <a name="work-order-service-entity"></a>Arbeidsordreserviceenhet

- Feltet **Ordre har bare eksternt vedlikeholdte produkter** er lagt til i **Arbeidsordreservice**-enheten og vises på siden. Det brukes til å spore om arbeidsordreservicen vedlikeholdes i Finance and Operations. Dette feltet sikrer at brukere ikke synkroniserer arbeidsordreservicer som er ukjent for Finance and Operations.
- Feltet **Hodesystemstatus** er lagt til i **Arbeidsordreservice**-enheten og vises på siden. Det brukes til å spore systemstatusen til arbeidsordren og hjelper med å garantere riktig filtrering når arbeidsordreservicer synkroniseres til Finance and Operations. Når filtre er definert for integreringsoppgavene, brukes også **Hodesystemstatus**-informasjonen til å bestemme om estimert- eller brukt-verdiene skal synkroniseres.
- **Varighet i timer**-feltet lagrer verdien fra **Varighet**-feltet etter at denne verdien er konvertert fra minutter til timer. Dette feltet brukes for integrering og vises ikke i brukergrensesnittet.
- **Estimert varighet i timer**-feltet lagrer verdien fra **Estimert varighet**-feltet etter at denne verdien er konvertert fra minutter til timer. Dette feltet brukes for integrering og vises ikke i brukergrensesnittet.
- **Fakturert enhetsbeløp**-feltet lagrer beløpet som er fakturert per faktisk enhet som brukes. Verdien beregnes som **Totalbeløp**-verdien dividert med **Faktisk antall**-verdien. Dett feltet brukes for integrering til systemer som ikke støtter forskjellige verdier for det brukte antallet og det fakturerte antallet. Feltet vises ikke i brukergrensesnittet.
- **Fakturert rabattbeløp**-feltet beregnes som **Rabattbeløp**-verdien pluss avrundingen fra beregningen av **Fakturert enhetsbeløp**-verdien. Dette feltet brukes for integrering og vises ikke i brukergrensesnittet.
- **Ekstern linjeordre**-feltet er et beregnet negativt linjeordrenummer som kan brukes i eksterne systemer der arbeidsordreprodukt og servicelinjer kombineres. Dette feltet gjør at arbeidsordreprodukter som settes inn, kan ha positive linjenumre og arbeideordreservicer kan ha negative linjenumre. Verdien for dette feltet beregnes som **Linjeordre**-verdien multiplisert med -1. Feltet vises ikke i brukergrensesnittet.
- Verdien i **Brukt**-felt tilbakestilles til **0** (null) hvis **Linjestatus**-verdien for arbeidsordreservice endres fra **Brukt** til **Estimert** av en eller annen grunn. Denne endringen bidrar til å hindre situasjoner der et bruk antall som er angitt ved en feiltakelse, brukes for synkronisering når **Linjestatus**-verdien er **Estimert** og **Hodesystemstatus**-verdien er **Lukket - postert**.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

Før du synkroniserer arbeidsordrer, er det viktig å oppdatere innstillingene nedenfor i systemene.

### <a name="setup-in-field-service"></a>Oppsett i Field Service

- Kontroller at nummerserien som brukes til arbeidsorder i Field Service, ikke overlapper nummerserien som brukes for salgsordrer i Finance and Operations. Ellers kan eksisterende salgsordrer oppdateres feil i Field Service eller Finance and Operations.
- **Oppretting av arbeidsordrefaktura**-feltet må settes til **Aldri**, fordi faktureringen foretas fra Finance and Operations. Gå til **Field Service** \> **Innstillinger** \> **Administrasjon** \> **Field Service-innstillinger**, og kontroller at **Oppretting av arbeidsordrefaktura**-feltet er satt til **Aldri**.

### <a name="setup-in-finance-and-operations"></a>Oppsett i Finance and Operations

Arbeidsordreintegrasjon krever at du definerer salgsopprinnelsen. Salgsopprinnelsen brukes til å skille salgsordrer i Finance and Operations som ble opprettet fra arbeidsorder i Field Service. Når en salgsordre har en salgsopprinnelse av typen **Arbeidsordreintegrasjon**, vises **Ekstern arbeidsordrestatus**-feltet i salgsordrehodet. I tillegg kan salgsopprinnelsen sikre at salgsordrer som ble opprettet fra arbeidsorder i Field Service, filtreres ut under synkronisering av salgsordrer fra Finance and Operations til Field Service.

1. Gå til **Salg og markedsføring** \> **Oppsett** \> **Salgsorder** \> **Salgsopprinnelse**.
2. Velg **Ny** for å opprette en ny salgsopprinnelse.
3. I **Salgsopprinnelse**-feltet angir du et navn for salgsopprinnelsen, for eksempel **Arbeidsordre**.
4. I **Beskrivelse**-feltet skriver du inn en beskrivelse, for eksempel **Arbeidsordre i Field Service**.
5. Merk av for **Tilordning av opprinnelsestype**.
6. Sett **Salgsopprinnelsestype**-feltet til **Integrering av arbeidsordre**.
7. Velg **Lagre**.


### <a name="setup-in-data-integration"></a>Oppsett i Dataintegrering

Kontroller at **Integration-nøkkelen** finnes for **msdyn_workorders**
1. Gå til Dataintegrering
2. Velg fanen **Tilkoblingssett**
3. Velg tilkoblingssettet som brukes for synkronisering av arbeidsordre
4. Velg fanen **Integreringsnøkkel**
5. Finn msdyn_workorders og kontroller at nøkkelen **msdyn_name (arbeidsordrenummer)** blir lagt til. Hvis den ikke vises, kan du legge den ved å klikke **Legg til nøkkel**, og klikke **Lagre** øverst på siden

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Følgende illustrasjoner viser en tilordning av malen i Dataintegrering.

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderheader"></a>Arbeidordrer til salgsordrer (Field Service til Fin og Ops): WorkOrderHeader

Filter: (msdyn_systemstatus ne 690970005) and (msdyn_systemstatus ne 690970000) og (msdynce_hasexternallymaintainedproductsonly eq true)

[![Maltilordning i Dataintegrering](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineestimate"></a>Arbeidordrer til salgsordrer (Field Service til Fin og Ops): WorkOrderServiceLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og (msdyn_linestatus eq 690970000) and (msdynce_headersystemstatus ne 690970004)

[![Maltilordning i Dataintegrering](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderservicelineused"></a>Arbeidordrer til salgsordrer (Field Service til Fin og Ops): WorkOrderServiceLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og ((msdyn_linestatus eq 690970001) eller (msdynce_headersystemstatus eq 690970004))

[![Maltilordning i Dataintegrering](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineestimate"></a>Arbeidordrer til salgsordrer (Field Service til Fin og Ops): WorkOrderProductLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og (msdyn_linestatus eq 690970000) and (msdynce_headersystemstatus ne 690970004) og (msdyn_allocated eq true)

[![Maltilordning i Dataintegrering](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-fin-and-ops-workorderproductlineused"></a>Arbeidordrer til salgsordrer (Field Service til Fin og Ops): WorkOrderProductLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og ((msdyn_linestatus eq 690970001) eller (msdynce_headersystemstatus eq 690970004) eller (msdyn_allocated ne true))

[![Maltilordning i Dataintegrering](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)

