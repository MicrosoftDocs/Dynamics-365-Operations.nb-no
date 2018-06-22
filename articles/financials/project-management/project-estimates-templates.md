---
title: Synkroniser prosjektestimater fra Project Service Automation direkte til prosjektprognoser i Finance and Operations
description: "Dette emnet beskriver malene og underliggende oppgaver som brukes til å synkronisere prosjekttimeestimater og prosjektutgiftsestimater direkte fra Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 90501f40da0fdc66ad087b3bd746c908cc25711b
ms.contentlocale: nb-no
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-estimates-from-project-service-automation-directly-to-project-forecasts-in-finance-and-operations"></a>Synkroniser prosjektestimater fra Project Service Automation direkte til prosjektprognoser i Finance and Operations

Dette emnet beskriver malene og underliggende oppgaver som brukes til å synkronisere prosjekttimeestimater og prosjektutgiftsestimater direkte fra Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.

> [!NOTE]
> Prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet er tilgjengelig i Dynamics 365 for Finance and Operations versjon 8.0.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Dataflyt for Project Service Automation til Finance and Operations

Project Service Automation til Finance and Operations-integrasjonsløsningen bruker dataintegrasjonsfunksjonen til å synkronisere data på tvers av Project Service Automation og Finance and Operations. Integreringsmalene som er tilgjengelige med dataintegreringsfunksjonen, muliggjør dataflyt om prosjekttimeestimater og prosjektutgiftsestimater fra Project Service Automation til Finance and Operations.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance and Operations.

[![Dataflyt for Project Service Automation-integrasjon med Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)


## <a name="templates-and-tasks"></a>Maler og oppgaver

For å få tilgang til de tilgjengelige malene velg **Prosjekter** i administrasjonssenter for Microsoft PowerApps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.

Følgende mal og underliggende oppgaver brukes til å synkronisere prosjekttimeestimater fra Project Service Automation til Finance and Operations:

-  **Navnet på malen i Dataintegrering:** Prosjekttimeestimater (PSA til Fin and Ops)

-  **Navn på oppgavene i prosjektet:** 
    - Transaksjonsrelasjoner 
    - Utgiftsestimater

## <a name="entity-set"></a>Enhetssett

| Project Service Automation      | Finance and Operations                          |
|---------------------------------|-------------------------------------------------|
| Prosjektoppgaver                   | Integreringsenhet for prosjekttimeestimater   |

## <a name="entity-flow"></a>Enhetsflyt

Prosjekttimeestimater administreres i Project Service Automation, og de synkroniseres til Finance and Operations som prosjekttimeprognoser.

## <a name="preconditions"></a>Forhåndskrav

Før synkronisering av prosjekttimeestimater kan skje, må du synkronisere prosjekter, prosjektoppgaver og transaksjonskategorier for prosjektutgifter.

## <a name="power-query"></a>Power Query

Du må bruke Microsoft Power Query i malen for prosjekttimeestimater for å:
- Angi **Prognosemodell-ID** som skal brukes når integreringen oppretter nye timeprognoser.
- Filtrere ut alle ressursspesifikke poster i oppgaven som ikke blir integrerte i timeprognoser
- Filtrere ut eventuelle tomme transaksjonskategorirader. Hvis du ikke gjør dette, kan det resultere i feil timeprognoser.

### <a name="forecast-model-id"></a>ID for prognosemodell
For å oppdatere standard prognosemodell-ID i malen, klikker du på **Tilordne**-pilen for å åpne tilordningen. Velg for å åpne avanserte spørring og filtrering.
- Hvis du bruker standardmalen for Microsoft Project-timeestimater (PSA til Fin and Ops), velger du **Innsatt betingelse** i delen **Brukte trinn**. I **Funksjon**-oppføringen erstatt **O_forecast** med navnet på **ID for prognosemodell** som skal brukes med integreringen. Standardmalen har en prognosemodell-ID fra demodataene.
- Hvis du oppretter en ny mal, må du legge til denne kolonnen. Velg **Legg til betinget kolonne**, og gi kolonnen et navn, for eksempel Modell-ID. Angi vilkåret for kolonnen, der hvis Prosjektoppgave ikke er null, så <enter the forecast model ID>, hvis ikke null.

### <a name="filter-out-resource-specific-records"></a>Filtrere ut ressursspesifikke poster
Malen for prosjekttimeestimater (PSA til Fin and Ops) har et standardfilter som fjerner ressursspesifikke poster. Hvis du oppretter din egen mal, må du legge til dette filteret. I Avanserte spørring og filtrering-skjermaet, velg å filtrere på kolonnen **msdyn_islinetask** for å bare inkludere **Usann**-poster.

### <a name="filter-out-empty-transaction-category-rows"></a>Filtrere ut tomme transaksjonskategorirader
Du må legge til et filter hvis du vil fjerne alle rader med tomme transaksjonskategorier. Dette er nødvendig uansett om du bruker standardmalen eller oppretter din egen mal. Dette filteret fjerner sammendragsrader som kommer fra Project Service Automation som kan føre til at timeprognoser i Finance and Operations blir feil. I skjemaet Avansert spørring og filtrering kan du velge å filtrere ut null-poster i kolonnen **msdyn_transactioncategory_value**.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.

[![Tilordning av mal](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

Følgende mal og underliggende oppgave brukes til å synkronisere prosjektutgiftsestimater fra Project Service Automation til Finance and Operations:

-  **Navnet på malen i Dataintegrering:** Prosjektutgiftsestimater (PSA til Fin and Ops)
-  **Navn på oppgavene i prosjektet:** 
     - Transaksjonsrelasjoner 
     - Utgiftsestimater

## <a name="entity-set"></a>Enhetssett

| Project Service Automation      | Finance and Operations                                     |
|---------------------------------|------------------------------------------------------------|
| Transaksjonstilkoblinger         | Integreringsenhet for relasjoner for prosjekttransaksjon.   |
| Estimatlinjer                  | Integreringsenhet for prosjektutgiftsestimater.           |

## <a name="entity-flow"></a>Enhetsflyt

Prosjektutgiftsestimater administreres i Project Service Automation, og de synkroniseres til Finance and Operations som prosjektutgiftsprognoser.

## <a name="prerequisites"></a>Nødvendig programvare

Før synkronisering av prosjektutgiftsestimater kan skje, må du synkronisere prosjekter, prosjektoppgaver og transaksjonskategorier for prosjektutgifter.

## <a name="power-query"></a>Power Query

Du må bruke Microsoft Power Query i malen for prosjektutgiftsestimater for å:
- Filtrere for å inkludere bare linjepostene for utgiftsestimat
- Angi **Prognosemodell-ID** som skal brukes når integreringen oppretter nye timeprognoser.
- Transformere faktureringstypene.
- Transformere transaksjonstypene.

### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtrere for å inkludere bare linjene for utgiftsestimat
Malen for prosjektutgiftsestimater (PSA til Fin and Ops) har et standardfilter som bare omfatter utgiftslinjer i integreringen. Hvis du oppretter din egen mal, må du legge til dette filteret. Velg transaksjonsrelasjonsoppgaven, og klikk **Tilordne**-pilen. Velg **Avansert syntaks for filtrering og spørring**. Filtrer **msdyn_transactiontype1**-kolonnen for å inkludere bare **msdyn_estimateline**.

### <a name="forecast-model-id"></a>ID for prognosemodell
For å oppdatere standard prognosemodell-ID i malen, klikker du på **Tilordne**-pilen for utgiftsestimatoppgaven for å åpne tilordningen. Velg for å åpne avanserte spørring og filtrering.
- Hvis du bruker standardmalen for Microsoft Project-utgiftsestimater (PSA til Fin and Ops), velger du den første **Innsatt betingelse** i delen **Brukte trinn**. I **Funksjon**-oppføringen erstatt **O_forecast** med navnet på **ID for prognosemodell** som skal brukes med integreringen. Standardmalen har en prognosemodell-ID fra demodataene.
- Hvis du oppretter en ny mal, må du legge til denne kolonnen. Velg **Legg til betinget kolonne**, og gi kolonnen et navn, for eksempel Modell-ID. Angi betingelsen for kolonnen, der hvis estimatlinje-ID ikke er null, så < skriv inn ID for prognosemodell >, hvis ikke null.

### <a name="transform-the-billing-types"></a>Transformere faktureringstypene
Malen for prosjektutgiftsestimater (PSA til Fin and Ops) har en betinget kolonne lagt til for å transformere faktureringstypene som ble mottatt fra Project Service Automation under integreringen.
- Hvis du oppretter din egen mal, må du legge til denne betingede kolonnen. I skjemaet Avansert spørring og filtrering velger du **Legg til betinget kolonne**. Gi kolonnen et navn, for eksempel "Faktureringstype". Betingelsen som skal angis, er som følger:

    Hvis **msdyn_billingtype** = 192350000, så **NonChargeable** ellers hvis **msdyn_billingtype** = 192350001, så **Chargeable** ellers hvis **msdyn_billingtype** = 192350002, så **Complimentary** ellers **NotAvailable**

### <a name="transform-the-transaction-types"></a>Transformere transaksjonstypene
Malen for prosjektutgiftsestimater (PSA til Fin and Ops) har en betinget kolonne lagt til for å transformere transaksjonstypene som ble mottatt fra Project Service Automation under integreringen.
- Hvis du oppretter din egen mal, må du legge til denne betingede kolonnen. I skjemaet Avansert spørring og filtrering velger du **Legg til betinget kolonne**. Gi den nye kolonnen et navn, for eksempel Transaksjonstype. Betingelsen som skal angis, er som følger: Hvis **msdyn_transactiontypecode** = 192350000, så **Cost** ellers hvis **msdyn_transactiontypecode** = 192350005, så **Sales** ellers **null**

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonen nedenfor viser eksempler på maloppgavetilordningene i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.

[![Tilordning av mal](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Tilordning av mal](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)




