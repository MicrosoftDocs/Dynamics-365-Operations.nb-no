---
title: Synkroniser faktiske prosjektdata fra Project Service Automation direkte til prosjektintegrasjonsjournalen for postering i Finance and Operations
description: "Dette emnet beskriver malene og underliggende oppgaver som brukes til å synkronisere faktiske prosjektdata direkte fra Microsoft Dynamics 365 for Project Service Automation til Dynamics 365 for Finance and Operations."
author: KimANelson
manager: AnnBe
ms.date: 05/21/2018
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
ms.openlocfilehash: 85ff049852e0b00623f47a12fb66e2c9bb9c4151
ms.contentlocale: nb-no
ms.lasthandoff: 05/29/2018

---
# <a name="synchronize-project-actuals-from-project-service-automation-directly-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synkroniser faktiske prosjektdata fra Project Service Automation direkte til prosjektintegrasjonsjournalen for postering i Finance and Operations

Dette emnet beskriver malene og underliggende oppgaver som brukes til å synkronisere faktiske prosjektdata direkte fra Microsoft Dynamics 365 for Project Service Automation til Dynamics 365 for Finance and Operations.

Malen synkroniserer transaksjoner fra Project Service Automation til en oppsamlingstabell i Finance and Operations. Når synkroniseringen er fullført, må du importere fra oppsamlingstabellen til integrasjonsjournalen.

> [!NOTE]
> Integrasjon av faktiske prosjektdata er tilgjengelig i Dynamics 365 for Finance and Operations versjon 8.01.

> [!NOTE]
> Hvis du skal angi merverdiavgiftsbeløp på tids- eller utgiftstransaksjoner i Project Service Automation, må du installere Project Service Automation-oppdatering 7. Hvis denne oppdateringen ikke installeres, vil de faktiske avgiftsdataene ikke knyttes til de faktiske tids- og utgiftsdataene, og de blir ikke synkronisert til Finance and Operations. Kontakt kundestøtten for mer informasjon.


## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Dataflyt for Project Service Automation til Finance and Operations

Project Service Automation til Finance and Operations-integrasjonsløsningen bruker dataintegrasjonsfunksjonen til å synkronisere data på tvers av Project Service Automation og Finance and Operations. Integreringsmalene som er tilgjengelige med dataintegreringsfunksjonen, muliggjør dataflyt om faktiske prosjektdata fra Project Service Automation til Finance and Operations.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance and Operations.

[![Dataflyt for Project Service Automation-integrasjon med Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)


## <a name="templates-and-tasks"></a>Maler og oppgaver

For å få tilgang til de tilgjengelige malene velg **Prosjekter** i administrasjonssenter for Microsoft PowerApps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.

Følgende mal og underliggende oppgaver brukes til å synkronisere faktiske prosjektdata fra Project Service Automation til Finance and Operations:

-  **Navnet på malen i Dataintegrering:** Faktiske prosjektdata (PSA til Fin and Ops)

-  **Navn på oppgavene i prosjektet:** 
    - Faktiske beløp 
    - TransactionConnections

## <a name="entity-set"></a>Enhetssett

| Project Service Automation      | Finance and Operations                                      |
|---------------------------------|-------------------------------------------------------------|
| Faktiske beløp                         | Enhet for integrering av faktiske prosjektdata                      |
| Transaksjonstilkoblinger         | Integreringsenhet for relasjoner for prosjekttransaksjon    |

## <a name="entity-flow"></a>Enhetsflyt

Faktiske prosjektdata administreres i Project Service Automation, og de synkroniseres til Finance and Operations til prosjektinterasjonsjournalen. Regnskapet brukes basert på standard finansdimensjoner og posteringsoppsett.

## <a name="preconditions"></a>Forhåndskrav

Før synkronisering av faktiske data kan skje, må du konfigurere Project Service Automation-integrasjonsparametere og synkronisere prosjekter, prosjektoppgaver og prosjektutgiftstransaksjonskategorier.

## <a name="power-query"></a>Power Query

Du må bruke Microsoft Power Query i malen for faktiske prosjektdata til å:
- Transformere Project Service Automation-**transaksjonstypen** til riktig **transaksjonstype** i Finance and Operations. Malen for faktiske prosjektdata (PSA til Fin and Ops) har allerede denne transformasjonen definert.
- Transformere Project Service Automation-**faktureringstype** til riktig **faktureringstype** i Finance and Operations. Malen for faktiske prosjektdata (PSA til Fin and Ops) har allerede denne transformasjonen definert. Faktureringstypen tilordnes deretter til **linjeegenskap** basert på konfigurasjonen i Dynamics 365 for Project Service Automation-integrasjonsparameterskjemaet.
- Filtrer til bestemte **Ressursorganisasjonsenheter** som skal synkroniseres med denne malen.
- Hvis **faktisk konsernintern tid eller faktiske konserne utgifter** blir synkronisert til Finance and Operations, må du gjøre om **kontraktorganisasjonsenheten** til riktig **juridisk enhet** i Finance and Operations. Malen for faktiske prosjektdata (PSA til Fin and Ops) har en betinget kolonne definert basert på demodata. Du må oppdatere sist innsatte betingelseskolonne til riktige juridiske enheter. Hvis ikke kan det resultere i en integrasjonsfeil eller at feil faktiske transaksjoner importeres til Finance and Operations.
- Hvis **faktisk konsernintern tid eller faktiske konserne utgifter** ikke synkroniseres til Finance and operations, må du slette sist innsatte betingelseskolonne fra malen. Hvis ikke kan det resultere i en integrasjonsfeil eller at feil faktiske transaksjoner importeres til Finance and Operations.

### <a name="contract-organizational-unit"></a>Kontraktorganisasjonsenheten
For å oppdatere den innsatte betingelseskolonnen i malen klikker du på **Tilordne**-pilen for å åpne tilordningen. Velg for å åpne avanserte spørring og filtrering.
- Hvis du bruker standardmalen for Microsoft Project faktiske data (PSA til Fin and Ops), velger du lasat **Innsatt betingelse** i delen **Brukte trinn**. I **Funksjon**-oppføringen erstatt **USSI** med navnet på **Juridisk enhet** som skal brukes med integreringen. Legg til flere betingelser etter behov i **Funksjon**-oppføringen, og oppdater **else**-betingelsen fra **USMF** til riktig **Juridisk enhet**.
- Hvis du oppretter en ny mal, må du legge til denne kolonnen for å støtte konsernintern(e) tid og utgifter. Velg **Legg til betinget kolonne**, og gi kolonnen et navn, for eksempel JuridiskEnhet. Angi vilkåret for kolonnen, der hvis msdyn_contractorganizationalunitid.msdyn_name er <organizational unit>, så <enter the Legal entity>, hvis ikke null.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonen nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.

[![Tilordning av mal](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Tilordning av mal](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table"></a>Importer fra oppsamlingstabell

Import fra periodisk prosess for oppsamlingstabell må utføres etter synkronisering av faktiske data fra Project Service Automation til Finance and Operations. Denne prosessen importerer prosjekttransaksjonene fra oppsamlingstabellen til Project Service Automation-integrasjonsjournalen, der regnskapet brukes og de importerte transaksjonene kan posteres. Det anbefales at du kjører denne prosessen i satsvis modus, og om ønskelig kan defineres til å kjøre som en gjentakende satsvis jobb.

## <a name="update-actuals"></a>Oppdatere faktiske data

Følgende mal og underliggende oppgaver brukes til å synkronisere bilagsnummeret og merverdiavgifter for posterte prosjekttransaksjoner fra Finance and Operations til Project Service Automation:

-  **Navnet på malen i Dataintegrering:** Faktiske prosjektdata-oppdatering (Fin Ops til PSA)
-  **Navn på oppgavene i prosjektet:** 
     - Faktiske beløp 
     - TransactionConnections

## <a name="entity-set"></a>Enhetssett

| Finance and Operations                                         | Project Service Automation        |
|----------------------------------------------------------------|-----------------------------------|
| Enhet for integrering av faktiske prosjektdata                         | Faktiske beløp                           |
| Integreringsenhet for relasjoner for prosjekttransaksjon       | Transaksjonstilkoblinger           |

## <a name="entity-flow"></a>Enhetsflyt

Faktiske prosjektdata administreres i Project Service Automation, og de synkroniseres til Finance and Operations til prosjektinterasjonsjournalen. Når det er postert i Finance and Operations, oppdateres faktiske data i Project Service Automation med bilagsnummeret fra Finance and Operations. Hvis merverdiavgifter ble lagt til i Finance and Operations, opprettes nye faktiske avgiftsdata i Project Service Automation.

## <a name="power-query"></a>Power Query

Du må bruke Microsoft Power Query i oppdateringsmalen for faktiske prosjektdata til å:
- Transformer Finance and Operations-**transaksjonstypen** til riktig **transaksjonstype** i Project Service Automation. Malen for oppdatering av faktiske prosjektdata (Fin Ops til PSA) har allerede denne transformasjonen definert.
- Transformere Finance and Operations-**faktureringstype** til riktig **faktureringstype** i Project Service Automation. Malen for oppdatering av faktiske prosjektdata (Fin Ops til PSA) har allerede denne transformasjonen definert.

## <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonen nedenfor viser eksempler på maloppgavetilordningene i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Finance and Operations til Project Service Automation.

[![Tilordning av mal](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Tilordning av mal](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)




