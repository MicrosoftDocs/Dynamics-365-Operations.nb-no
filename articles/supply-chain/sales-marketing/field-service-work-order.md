---
title: Synkronisere arbeidsordrer i Field Service til salgsordrer i Supply Chain Management
description: Denne artikkelen beskriver malene og de underliggende oppgavene som brukes til å synkronisere arbeidsordrer i Field Service til salgsordrer i Supply Chain Management.
author: Henrikan
ms.date: 04/09/2018
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
ms.author: henrikan
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: e64c9a954e8f5c4410f8ba370b40b7c6e76e8ae0
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8860529"
---
# <a name="synchronize-work-orders-in-field-service-to-sales-orders-in-supply-chain-management"></a>Synkronisere arbeidsordrer i Field Service til salgsordrer i Supply Chain Management

[!include[banner](../includes/banner.md)]



Denne artikkelen drøfter maler og underliggende oppgaver som brukes til å synkronisere arbeidsordrer i Dynamics 365 Field Service til salgsordrer i Dynamics 365 Supply Chain Management.

[![Synkronisering av forretningsprosesser mellom Supply Chain Management og Field Service.](./media/field-service-integration.png)](./media/field-service-integration.png)


## <a name="templates-and-tasks"></a>Maler og oppgaver

De følgende malene og de underliggende oppgavene brukes til å utføre synkroniseringen av arbeidsordrer i Field Service til salgsordrer i Supply Chain Management.

### <a name="names-of-the-templates-in-data-integration"></a>Navn på malene i Dataintegrering

**Arbeidsordrer til salgsordrer (Field Service til Supply Chain Management)**-malen brukes til å utføre synkronisering.

### <a name="names-of-the-tasks-in-the-data-integration-project"></a>Navnet på oppgaven i Dataintegrasjonprosjektet

- WorkOrderHeader
- WorkOrderServiceLineEstimate
- WorkOrderServiceLineUsed
- WorkOrderProductLineEstimate
- WorkOrderProductLineUsed

Følgende synkroniseringsoppgaver er påkrevd før synkronisering av salgsordrehoder og -linjer kan inntreffe:

- Field Service-produkter (Supply Chain Management til Field Service)
- Kontoer (Sales til Supply Chain Management) – direkte

## <a name="entity-set"></a>Enhetssett

| **Field Service** | **Supply Chain Management** |
|-------------------------|-------------------------|
| msdyn_workorders        | Dataverse-salgsordrehoder |
| msdyn_workorderservices | Dataverse-salgsordrelinjer   |
| msdyn_workorderproducts | Dataverse-salgsordrelinjer   |

## <a name="entity-flow"></a>Enhetsflyt

Arbeidsordrer opprettes i Field Service. Hvis arbeidsordene inkluderer bare eksternt vedlikeholdte produkter, og hvis **Arbeidsordrestatus**-verdien er forskjellig fra **Åpen – uplanlagt** og **Lukket – avbrutt**, kan arbeidsordrene synkroniseres til Supply Chain Management via et Microsoft Dataverse-dataintegreringsprosjekt. Oppdateringer av arbeidsordene synkroniseres som salgsordrer i Supply Chain Management. Disse oppdateringene inneholder informasjon om opprinnelsestypen og status.

## <a name="estimated-versus-used"></a>Estimert kontra brukt

I Field Service har produkter og tjenester på arbeidsordrer både **Estimert**-verdier og **Brukt**-verdier for antall og beløp. I Supply Chain Management derimot har ikke salgsordrer det samme konseptet for **Estimert**- og **Brukt**-verdier. For å støtte produkttilordning som bruker det forventede antallet på salgsordren i Supply Chain Management, men for å beholde det brukte antallet som skal brukes og faktureres, synkroniserer to sett med oppgaver produktene og tjenestene på arbeidsordren. Ett sett med oppgaver for **Estimert**-verdier, og det andre settet med oppgaver for **Brukt**-verdier.

Dette gjør det mulig med scenarioer der estimerte verdier brukes for tildeling eller reservasjon i Supply Chain Management, mens brukte verdier brukes for forbruk og fakturering.

### <a name="estimated"></a>Estimert

For synkronisering av produktserier brukes **Estimert**-verdier når **Linjestatus**-verdien er **Estimert**, **Tilordnet** er satt til **Ja** og **Systemstatus**-verdien ikke er **Lukket – bokført**.

For synkronisering av servicelinjer brukes **Estimert**-verdier når **Linjestatus**-verdien er **Estimert** og **Systemstatus**-verdien ikke er **Lukket – bokført**.

### <a name="used"></a>Brukt

**Brukes**-verdiene skal brukes for forbruk og fakturering. I disse tilfellene vil **Brukes**-verdiene synkroniseres.

Tabellen nedenfor gir en oversikt over de forskjellige kombinasjonene for produktlinjer.

| Systemstatus <br>(Field Service) | Linjestatus <br>(Field Service) | Tilordnet <br>(Field Service) |Synkroniseringsverdi <br>(Supply Chain Management) |
|--------------------|-------------|-----------|---------------------------------|
| Åpen – planlagt   | Estimert   | Ja       | Estimert                       |
| Åpen – planlagt   | Estimert   | Nei        | Brukt                            |
| Åpen – planlagt   | Brukt        | Ja       | Brukt                            |
| Åpen – planlagt   | Brukt        | Nei        | Brukt                            |
| Åpen – pågår | Estimert   | Ja       | Estimert                       |
| Åpen – pågår | Estimert   | Nei        | Brukt                            |
| Åpen – pågår | Brukt        | Ja       | Brukt                            |
| Åpen – pågår | Brukt        | Nei        | Brukt                            |
| Åpne – fullført   | Estimert   | Ja       | Estimert                       |
| Åpne – fullført   | Estimert   | Nei        | Brukt                            |
| Åpne – fullført   | Brukt        | Ja       | Brukt                            |
| Åpne – fullført   | Brukt        | Nei        | Brukt                            |
| Lukket – postert    | Estimert   | Ja       | Brukt                            |
| Lukket – postert    | Estimert   | Nei        | Brukt                            |
| Lukket – postert    | Brukt        | Ja       | Brukt                            |
| Lukket – postert    | Brukt        | Nei        | Brukt                            |

Tabellen nedenfor gir en oversikt over de forskjellige kombinasjonene for servicelinjer.

| Systemstatus <br>(Field Service) | Linjestatus <br>(Field Service) | Synkroniseringsverdi <br>(Supply Chain Management) |
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

    I dette eksemplet synkroniseres produktets **Brukt antall**-verdi **0** (null) og tjenestens **Estimert antall**-verdi **2h** til Supply Chain Management.

2. Produkter tilordnes i Field Service.

    **Systemstatus**-verdien er **Åpen – planlagt**.

    - **Produktlinje:** Estimert antall = 5ea, brukt antall = 0ea, linjestatus = estimert, tilordnet = Ja
    - **Servicelinje:** Estimert antall = 2h, brukt antall = 0h, linjestatus = estimert

    I dette eksemplet synkroniseres produktets **Estimert antall**-verdi **5ea** og tjenestens **Estimert antall**-verdi **2h** til Supply Chain Management.

3. Serviceteknikeren begynner å arbeide med arbeidsordren og registrerer materialforbruk på 6.

    **Systemstatus**-verdien er **Åpen – pågår**.

    - **Produktlinje:** Estimert antall = 5ea, brukt antall = 6ea, linjestatus = brukt, tilordnet = Ja
    - **Servicelinje:** Estimert antall = 2h, brukt antall = 0h, linjestatus = estimert

    I dette eksemplet synkroniseres produktets **Brukt antall**-verdi **6** og tjenestens **Estimert antall**-verdi **2h** til Supply Chain Management.

4. Serviceteknikeren fullfører arbeidsordren og registrerer brukt tid på 1,5 time.

    **Systemstatus**-verdien er **Åpen – fullført**.

    - **Produktlinje:** Estimert antall = 5ea, brukt antall = 6ea, linjestatus = brukt, tilordnet = Ja
    - **Servicelinje:** Estimert antall = 2h, brukt antall = 1,5h, linjestatus = brukt

    I dette eksemplet synkroniseres produktets **Brukt antall**-verdi **6** og tjenestens **Brukt antall** på **1,5h** til Supply Chain Management.

## <a name="sales-order-origin-and-status"></a>Salgsordreopprinnelse og -status

### <a name="sales-origin"></a>Salgsopprinnelse

Hvis du vil holde oversikt over salgsordrer som kommer fra arbeidsordrer, kan du opprette en salgsopprinnelse der **Tilordning av opprinnelsestype** er satt til **Ja** og **Salgsopprinnelsestype**-feltet er satt til **Integrering av arbeidsordre**.

Som standard velger tilordningen salgsopprinnelsen for salgsopprinnelsestypen **Integrering av arbeidsordre** som er opprettet fra arbeidsordrer. Dette kan være nyttig når du arbeider med salgsordren i Supply Chain Management. Du må kontrollere at salgsordrer som stammer fra arbeidsordrer, ikke synkroniseres tilbake til Field Service som arbeidsordrer.

Hvis du vil ha mer informasjon om hvordan du oppretter riktig salgsopprinnelsesoppsett i Supply Chain Management, kan du se delen Forutsetninger og tilordningsdefinisjon i denne artikkelen.

### <a name="status"></a>Status

Når salgsordren stammer fra en arbeidsordre, vises feltet **Status for ekstern arbeidsordre** i **Oppsett**-fanen i salgsordrehodet. Dette feltet viser systemstatusen fra arbeidsordren i Field Service, for å spore statusen for synkronisert arbeidsordre for salgsordrer i Supply Chain Management. Dette feltet kan også hjelpe brukeren av Supply Chain Management å bestemme når salgsordren skal leveres eller faktureres.

**Status for ekstern arbeidsordre**-feltet kan ha følgende verdier:

- Åpen – planlagt
- Åpen – pågår
- Åpne – fullført
- Lukket – postert

## <a name="field-service-crm-solution"></a>CRM-løsning for Field Service

For å støtte integrasjon mellom Field Service og Supply Chain Management, kreves det ekstra funksjonalitet fra Field Service CRM-løsningen. Løsningen inneholder følgende endringer.

### <a name="work-order-entity"></a>Arbeidsordreenhet

Feltet **Har bare eksternt vedlikeholdte produkter** er lagt til i **Arbeidsordre**-enheten og vises på siden. Det brukes til å spore om en arbeidsordre utelukkende består av eksternt vedlikeholdte produkter. En arbeidsordre består av bare eksternt vedlikeholdte produkter når alle relaterte produkter vedlikeholdes i Supply Chain Management. Dette feltet sikrer at brukere ikke synkroniserer arbeidsordrer med produkter som er ukjent for Supply Chain Management.

### <a name="work-order-product-entity"></a>Arbeidsordreproduktenhet

- Feltet **Ordre har bare eksternt vedlikeholdte produkter** er lagt til i **Arbeidsordreprodukt**-enheten og vises på siden. Det brukes til å spore om arbeidsordreproduktet vedlikeholdes i Supply Chain Management. Dette feltet sikrer at brukere ikke synkroniserer arbeidsordreprodukter som er ukjent for Supply Chain Management.
- Feltet **Hodesystemstatus** er lagt til i **Arbeidsordreprodukt**-enheten og vises på siden. Det brukes til å spore systemstatusen til arbeidsordren og hjelper med å garantere riktig filtrering når arbeidsordreprodukter synkroniseres til Supply Chain Management. Når filtre er definert for integreringsoppgavene, brukes også **Hodesystemstatus**-informasjonen til å bestemme om estimert- eller brukt-verdiene skal synkroniseres.
- **Fakturert enhetsbeløp**-feltet viser beløpet som er fakturert per faktisk enhet som brukes. Verdien beregnes som **Totalbeløp**-verdien dividert med **Faktisk antall**-verdien. Feltet brukes for integrering til systemer som ikke støtter forskjellige verdier for det brukte antallet og det fakturerte antallet. Dette feltet vises ikke i brukergrensesnittet. 
- **Fakturert rabattbeløp**-feltet beregnes som **Rabattbeløp**-verdien pluss avrundingen fra beregningen av **Fakturert enhetsbeløp**-verdien. Dette feltet brukes for integrering og vises ikke i brukergrensesnittet.
- **Desimalantallet**-feltet lagrer verdien fra **Antall**-feltet som et desimaltall. Dette feltet brukes for integrering og vises ikke i brukergrensesnittet. 
- Verdien i **Brukt**-felt tilbakestilles til **0** (null) hvis **Linjestatus**-verdien for arbeidsordreproduktet endres fra **Brukt** til **Estimert**. Denne endringen bidrar til å hindre situasjoner der et bruk antall som er angitt ved en feiltakelse, brukes for synkronisering når **Linjestatus**-verdien er **Estimert** og **Tilordet**-alternativet er satt til **Nei**.

### <a name="work-order-service-entity"></a>Arbeidsordreserviceenhet

- Feltet **Ordre har bare eksternt vedlikeholdte produkter** er lagt til i **Arbeidsordreservice**-enheten og vises på siden. Det brukes til å spore om arbeidsordretjenesten vedlikeholdes i Supply Chain Management. Dette feltet sikrer at brukere ikke synkroniserer arbeidsordretjenester som er ukjent for Supply Chain Management.
- Feltet **Hodesystemstatus** er lagt til i **Arbeidsordreservice**-enheten og vises på siden. Det brukes til å spore systemstatusen til arbeidsordren og hjelper med å garantere riktig filtrering når arbeidsordretjenester synkroniseres til Supply Chain Management. Når filtre er definert for integreringsoppgavene, brukes også **Hodesystemstatus**-informasjonen til å bestemme om estimert- eller brukt-verdiene skal synkroniseres.
- **Varighet i timer**-feltet lagrer verdien fra **Varighet**-feltet etter at denne verdien er konvertert fra minutter til timer. Dette feltet brukes for integrering og vises ikke i brukergrensesnittet.
- **Estimert varighet i timer**-feltet lagrer verdien fra **Estimert varighet**-feltet etter at denne verdien er konvertert fra minutter til timer. Dette feltet brukes for integrering og vises ikke i brukergrensesnittet.
- **Fakturert enhetsbeløp**-feltet lagrer beløpet som er fakturert per faktisk enhet som brukes. Verdien beregnes som **Totalbeløp**-verdien dividert med **Faktisk antall**-verdien. Dett feltet brukes for integrering til systemer som ikke støtter forskjellige verdier for det brukte antallet og det fakturerte antallet. Feltet vises ikke i brukergrensesnittet.
- **Fakturert rabattbeløp**-feltet beregnes som **Rabattbeløp**-verdien pluss avrundingen fra beregningen av **Fakturert enhetsbeløp**-verdien. Dette feltet brukes for integrering og vises ikke i brukergrensesnittet.
- **Ekstern linjeordre**-feltet er et beregnet negativt linjeordrenummer som kan brukes i eksterne systemer der arbeidsordreprodukt og servicelinjer kombineres. Dette feltet gjør at arbeidsordreprodukter som settes inn, kan ha positive linjenumre og arbeideordreservicer kan ha negative linjenumre. Verdien for dette feltet beregnes som **Linjeordre**-verdien multiplisert med -1. Feltet vises ikke i brukergrensesnittet.
- Verdien i **Brukt**-felt tilbakestilles til **0** (null) hvis **Linjestatus**-verdien for arbeidsordreservice endres fra **Brukt** til **Estimert** av en eller annen grunn. Denne endringen bidrar til å hindre situasjoner der et bruk antall som er angitt ved en feiltakelse, brukes for synkronisering når **Linjestatus**-verdien er **Estimert** og **Hodesystemstatus**-verdien er **Lukket - postert**.

## <a name="preconditions-and-mapping-setup"></a>Forutsetninger og tilordningsdefinisjon

Før du synkroniserer arbeidsordrer, er det viktig å oppdatere innstillingene nedenfor i systemene.

### <a name="setup-in-field-service"></a>Oppsett i Field Service

- Kontroller at nummerserien som brukes til arbeidsorder i Field Service, ikke overlapper nummerserien som brukes for salgsordrer i Supply Chain Management. Ellers kan eksisterende salgsordrer oppdateres feil i Field Service eller Supply Chain Management.
- **Oppretting av arbeidsordrefaktura**-feltet må settes til **Aldri**, fordi faktureringen foretas fra Supply Chain Management. Gå til **Field Service** \> **Innstillinger** \> **Administrasjon** \> **Field Service-innstillinger**, og kontroller at **Oppretting av arbeidsordrefaktura**-feltet er satt til **Aldri**.

### <a name="setup-in-supply-chain-management"></a>Oppsett i Supply Chain Management

Arbeidsordreintegrasjon krever at du definerer salgsopprinnelsen. Salgsopprinnelsen brukes til å skille salgsordrer i Supply Chain Management som ble opprettet fra arbeidsorder i Field Service. Når en salgsordre har en salgsopprinnelse av typen **Arbeidsordreintegrasjon**, vises **Ekstern arbeidsordrestatus**-feltet i salgsordrehodet. I tillegg kan salgsopprinnelsen sikre at salgsordrer som ble opprettet fra arbeidsorder i Field Service, filtreres ut under synkronisering av salgsordrer fra Supply Chain Management til Field Service.

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

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderheader"></a>Arbeidsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderHeader

Filter: (msdyn_systemstatus ne 690970005) and (msdyn_systemstatus ne 690970000) og (msdynce_hasexternallymaintainedproductsonly eq true)

[![Maltilordning i dataintegrering for arbeidsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderHeader.](./media/FSWorkOrder1.png )](./media/FSWorkOrder1.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineestimate"></a>Arbeidsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderServiceLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og (msdyn_linestatus eq 690970000) and (msdynce_headersystemstatus ne 690970004)

[![Maltilordning i dataintegrering for arbeidsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderServiceLineEstimate.](./media/FSWorkOrder2.png )](./media/FSWorkOrder2.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderservicelineused"></a>Arbeidsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderServiceLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og ((msdyn_linestatus eq 690970001) eller (msdynce_headersystemstatus eq 690970004))

[![Maltilordning i dataintegrering for arbeidsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderServiceLineUsed.](./media/FSWorkOrder3.png )](./media/FSWorkOrder3.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineestimate"></a>Arbeidsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderProductLineEstimate

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og (msdyn_linestatus eq 690970000) and (msdynce_headersystemstatus ne 690970004) og (msdyn_allocated eq true)

[![Maltilordning i dataintegrering for arbeidsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderProductLineEstimate.](./media/FSWorkOrder4.png )](./media/FSWorkOrder4.png)

### <a name="work-orders-to-sales-orders-field-service-to-supply-chain-management-workorderproductlineused"></a>Arbeidsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderProductLineUsed

Filter: (msdynce_headersystemstatus ne 690970005) og (msdynce_headersystemstatus ne 690970000) og (msdynce_orderhasexternalmaintainedproductsonly eq true) og ((msdyn_linestatus eq 690970001) eller (msdynce_headersystemstatus eq 690970004) eller (msdyn_allocated ne true))

[![Maltilordning i dataintegrering for arbeidsordrer til salgsordrer (Field Service til Supply Chain Management): WorkOrderProductLineUsed.](./media/FSWorkOrder5.png )](./media/FSWorkOrder5.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]