---
title: Synkronisere prosjektestimater direkte fra Project Service Automation til Finance and Operations
description: "Dette emnet beskriver malene og underliggende oppgaver som brukes til å synkronisere prosjekttimeestimater og prosjektutgiftsestimater direkte fra Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronisere prosjektestimater direkte fra Project Service Automation til Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet beskriver malene og underliggende oppgaver som brukes til å synkronisere prosjekttimeestimater og prosjektutgiftsestimater direkte fra Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> - Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i Microsoft Dynamics 365 for Finance and Operations versjon 8.0.
> - Integrasjon av faktiske data er tilgjengelig i Microsoft Dynamics 365 for Finance and Operations versjon 8.0.1 eller senere.
> - Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 når du har installert KB 4132657 og KB 4132660, vil du kunne bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske data, og du vil kunne konfigurere funksjonslåsing. Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Dataflyt for Project Service Automation til Finance and Operations

Project Service Automation til Finance and Operations-integrasjonsløsningen bruker dataintegrasjonsfunksjonen til å synkronisere data på tvers av Project Service Automation og Finance and Operations. Integreringsmalene som er tilgjengelige med dataintegreringsfunksjonen, muliggjør dataflyt om prosjekttimeestimater og prosjektutgiftsestimater fra Project Service Automation til Finance and Operations.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance and Operations.

[![Dataflyt for Project Service Automation-integrasjon med Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Prosjekttimeestimater

### <a name="template-and-tasks"></a>Mal og oppgaver

For å få tilgang til de tilgjengelige malene velg **Prosjekter** i administrasjonssenter for Microsoft PowerApps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.

Følgende mal og underliggende oppgaver brukes til å synkronisere prosjekttimeestimater fra Project Service Automation til Finance and Operations:

- **Navnet på malen i Dataintegrering:** Prosjekttimeestimater (PSA til Fin and Ops)
- **Navn på oppgavene i prosjektet:**

    - Transaksjonsrelasjoner
    - Utgiftsestimater

### <a name="entity-set"></a>Enhetssett

| Project Service Automation | Finance and Operations                        |
|----------------------------|-----------------------------------------------|
| Prosjektoppgaver              | Integreringsenhet for prosjekttimeestimater |

### <a name="entity-flow"></a>Enhetsflyt

Prosjekttimeestimater administreres i Project Service Automation, og de synkroniseres til Finance and Operations som prosjekttimeprognoser.

### <a name="prerequisites"></a>Nødvendig programvare

Før synkronisering av prosjekttimeestimater kan skje, må du synkronisere prosjekter, prosjektoppgaver og transaksjonskategorier for prosjektutgifter.

### <a name="power-query"></a>Power Query

I prosjekttimeestimatmalen kan du bruke Microsoft Power Query for Excel til å fullføre disse oppgavene:

- Angi standard prognosemodell-ID som skal brukes når integreringen oppretter nye timeprognoser.
- Filtrer ut alle ressursspesifikke poster i oppgaven som ikke blir integrerte i timeprognoser.
- Filtrere ut eventuelle tomme transaksjonskategorirader. Hvis du ikke gjør dette, kan det resultere i feil timeprognoser.

#### <a name="set-the-default-forecast-model-id"></a>Angi standard prognosemodell-ID

For å oppdatere standard prognosemodell-ID i malen, klikker du på **Tilordne**-pilen for å åpne tilordningen. Velg deretter koblingen **Avansert spørring og filtrering**.

- Hvis du bruker standard prosjekttimeestimater (PSA til Fin and Ops), velger du **Innsatt betingelse** i liste over **Brukte trinn**. I **Funksjon**-oppføringen erstatter du **O\_forecast** med navnet på prognosemodell-ID-en som skal brukes med integreringen. Standardmalen har en prognosemodell-ID fra demodataene.
- Hvis du oppretter en ny mal, må du legge til denne kolonnen. I Power Query velger du **Legg til betinget kolonne** og angir et navn på den nye kolonnen, for eksempel **Model-ID**. Angi betingelsen for kolonnen, der hvis prosjektoppgave ikke er null, så \<skriv inn ID for prognosemodell\> >, hvis ikke null.

#### <a name="filter-out-resource-specific-records"></a>Filtrere ut ressursspesifikke poster

Malen for prosjekttimeestimater (PSA til Fin and Ops) har et standardfilter som fjerner ressursspesifikke poster. Hvis du oppretter din egen mal, må du legge til dette filteret. Velg koblingen **Avanserte spørring og filtrering** for å filtrere på kolonnen **msdyn\_islinetask**, slik at bare **Usann**-poster inkluderes.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtrere ut tomme transaksjonskategorirader

Du må legge til et filter hvis du vil fjerne alle rader med tomme transaksjonskategorier. Denne oppgaven er nødvendig uansett om du bruker standardmalen eller oppretter din egen mal. Dette filteret fjerner sammendragsrader som kommer fra Project Service Automation som kan føre til at timeprognoser i Finance and Operations blir feil. Velg koblingen **Avansert spørring og filtrering** for å filtrere ut null-poster i kolonnen **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.

[![Tilordning av mal](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Prosjektutgiftsestimater

### <a name="template-and-tasks"></a>Mal og oppgaver

Følgende mal og underliggende oppgaver brukes til å synkronisere prosjektutgiftsestimater fra Project Service Automation til Finance and Operations:

- **Navnet på malen i Dataintegrering:** Prosjektutgiftsestimater (PSA til Fin and Ops)
- **Navn på oppgavene i prosjektet:**

    - Transaksjonsrelasjoner 
    - Utgiftsestimater

### <a name="entity-set"></a>Enhetssett

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| Transaksjonstilkoblinger    | Integreringsenhet for relasjoner for prosjekttransaksjon |
| Estimatlinjer             | Integreringsenhet for prosjektutgiftsestimater         |

### <a name="entity-flow"></a>Enhetsflyt

Prosjektutgiftsestimater administreres i Project Service Automation, og de synkroniseres til Finance and Operations som prosjektutgiftsprognoser.

### <a name="prerequisites"></a>Nødvendig programvare

Før synkronisering av prosjektutgiftsestimater kan skje, må du synkronisere prosjekter, prosjektoppgaver og transaksjonskategorier for prosjektutgifter.

### <a name="power-query"></a>Power Query

I prosjektutgiftsestimatmalen må du bruke Power Query til å fullføre følgende oppgaver:

- Filtrere for å inkludere bare linjepostene for utgiftsestimat.
- Angi standard prognosemodell-ID som skal brukes når integreringen oppretter nye timeprognoser.
- Transformere faktureringstypene.
- Transformere transaksjonstypene.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrere for å inkludere bare linjene for utgiftsestimat

Malen for prosjektutgiftsestimater (PSA til Fin and Ops) har et standardfilter som bare omfatter utgiftslinjer i integreringen. Hvis du oppretter din egen mal, må du legge til dette filteret. Velg **Transaksjonsrelasjoner**, og klikk deretter **Tilordne**-pilen for å åpne tilordningen. Velg koblingen **Avansert spørring og filtrering**. Filtrer kolonnen **msdyn\_transactiontype1** for å inkludere bare **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Angi standard prognosemodell-ID

For å oppdatere standard prognosemodell-ID i malen, velger du oppgaven **Utgiftsestimater**, og deretter klikker du på **Tilordne**-pilen for å åpne tilordningen. Velg koblingen **Avansert spørring og filtrering**.

- Hvis du bruker standardmalen for prosjektutgiftsestimater (PSA til Fin and Ops), velger du den første **Innsatt betingelse** i delen **Brukte trinn** i Power Query. I **Funksjon**-oppføringen erstatter du **O\_forecast** med navnet på prognosemodell-ID-en som skal brukes med integreringen. Standardmalen har en prognosemodell-ID fra demodataene.
- Hvis du oppretter en ny mal, må du legge til denne kolonnen. I Power Query velger du **Legg til betinget kolonne** og angir et navn på den nye kolonnen, for eksempel **Model-ID**. Angi betingelsen for kolonnen, der hvis estimatlinje-ID ikke er null, så \<skriv inn prognosemodell-ID\>, hvis ikke null.

#### <a name="transform-the-billing-types"></a>Transformere faktureringstypene

Malen for prosjektutgiftsestimater (PSA til Fin and Ops) inkluderer en betinget kolonne som brukes til å transformere faktureringstypene som ble mottatt fra Project Service Automation under integreringen. Hvis du oppretter din egen mal, må du legge til denne betingede kolonnen. Velg koblingen **Avansert spørring og filtrering**, og velg deretter **Legg til betinget kolonne**. Angi et navn for den nye kolonnen, for eksempel **Faktureringstype**. Angi deretter følgende betingelse:

Hvis **msdyn\_billingtype** = 192350000, så **NonChargeable**  
ellers hvis **msdyn\_billingtype** = 192350001, så **Chargeable**  
ellers hvis **msdyn\_billingtype** = 192350002, så **Complimentary**  
ellers **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Transformere transaksjonstypene

Malen for prosjektutgiftsestimater (PSA til Fin and Ops) inkluderer en betinget kolonne som brukes til å transformere transaksjonstypene som ble mottatt fra Project Service Automation under integreringen. Hvis du oppretter din egen mal, må du legge til denne betingede kolonnen. Velg koblingen **Avansert spørring og filtrering**, og velg deretter **Legg til betinget kolonne**. Angi et navn for den nye kolonnen, for eksempel **Transaksjonstype**. Angi deretter følgende betingelse:

Hvis **msdyn\_transactiontypecode** = 192350000, så **Cost**  
ellers hvis **msdyn\_transactiontypecode** = 192350005, så **Sales**  
ellers **null**

### <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonen nedenfor viser eksempler på maloppgavetilordningene i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.

[![Tilordning av mal](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Tilordning av mal](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)

