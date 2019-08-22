---
title: Synkronisere faktiske prosjektdata direkte fra Project Service Automation til prosjektintegrasjonsjournalen for postering i Finance and Operations
description: Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere faktiske prosjektdata direkte fra Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 3b6427d7eede8fe35fcd86928c3d5b8507876e2e
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1846081"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Synkronisere faktiske prosjektdata direkte fra Project Service Automation til prosjektintegrasjonsjournalen for postering i Finance and Operations

[!include[banner](../includes/banner.md)]

Dette emnet beskriver malene og de underliggende oppgavene som brukes til å synkronisere faktiske prosjektdata direkte fra Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.

Malen synkroniserer transaksjoner fra Project Service Automation til en oppsamlingstabell i Finance and Operations. Når synkroniseringen er fullført, **må** du importere dataene fra oppsamlingstabellen til integrasjonsjournalen.

> [!NOTE]
> - Integrasjon av faktiske prosjektdata er tilgjengelig i Microsoft Dynamics 365 for Finance and Operations versjon 8.0.1 eller senere.
> - Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 når du har installert KB 4132657 og KB 4132660, vil du kunne bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske data, og du vil kunne konfigurere funksjonslåsing. Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.
> - Hvis du bruker Finance and Operations 7.3.0, og du henter gebyrtransaksjoner fra Project Service Automation, må du installere KB 4345320 for å inkludere disse gebyrene i prosjektfakturaen.
> - Hvis du skal angi merverdiavgiftsbeløp på tids- eller utgiftstransaksjoner i Project Service Automation, må du installere Project Service Automation oppdatering 7. Hvis ikke vil de faktiske avgiftsdataene ikke knyttes til de faktiske tids- og utgiftsdataene, og de blir ikke synkronisert til Finance and Operations. Kontakt kundestøtten for mer informasjon.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Dataflyt for Project Service Automation til Finance and Operations

Project Service Automation til Finance and Operations-integrasjonsløsningen bruker dataintegrasjonsfunksjonen til å synkronisere data på tvers av Project Service Automation og Finance and Operations. Integreringsmalene som er tilgjengelige med dataintegreringsfunksjonen, muliggjør dataflyt om faktiske prosjektdata fra Project Service Automation til Finance and Operations.

Illustrasjonen nedenfor viser hvordan dataene synkroniseres mellom Project Service Automation og Finance and Operations.

[![Dataflyt for Project Service Automation-integrasjon med Finance and Operations](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Faktiske prosjektdata fra Project Service Automation

### <a name="template-and-tasks"></a>Mal og oppgaver

For å få tilgang til tilgjengelige maler velg **Prosjekter** i administrasjonssenter for Microsoft PowerApps, og deretter, i øvre høyre hjørne, velg **Nytt prosjekt** for å velge offentlige maler.

Følgende mal og underliggende oppgaver brukes til å synkronisere faktiske prosjektdata fra Project Service Automation til Finance and Operations:

- **Navnet på malen i Dataintegrering:** Faktiske prosjektdata (PSA til Fin and Ops)
- **Navn på oppgavene i prosjektet:**

    - Faktiske beløp
    - TransactionConnections

### <a name="entity-set"></a>Enhetssett

| Project Service Automation | Finance and Operations                                   |
|----------------------------|----------------------------------------------------------|
| Faktiske beløp                    | Enhet for integrering av faktiske prosjektdata                   |
| Transaksjonstilkoblinger    | Integreringsenhet for relasjoner for prosjekttransaksjon |

### <a name="entity-flow"></a>Enhetsflyt

Faktiske prosjektdata administreres i Project Service Automation, og de synkroniseres til prosjektinterasjonsjournalen i Finance and Operations. Regnskapet brukes basert på standard finansdimensjoner og posteringsoppsettet.

### <a name="prerequisites"></a>Nødvendig programvare

Før synkronisering av faktiske data kan skje, må du konfigurere Project Service Automation-integrasjonsparametere og synkronisere prosjekter, prosjektoppgaver og prosjektutgiftstransaksjonskategorier.

### <a name="power-query"></a>Power Query

I malen for faktiske prosjektdata kan du bruke Microsoft Power Query for Excel til å fullføre disse oppgavene:

- Transformere Project Service Automation-transaksjonstypen til riktig transaksjonstype i Finance and Operations. Denne transformasjonen er allerede definert i malen for faktiske prosjektdata (PSA til Fin and Ops).
- Transformer Project Service Automation-faktureringstype til riktig faktureringstype i Finance and Operations. Denne transformasjonen er allerede definert i malen for faktiske prosjektdata (PSA til Fin and Ops). Faktureringstypen tilordnes deretter til linjeegenskapen basert på konfigurasjonen på siden **Integreringsparametere for Project Service Automation**.
- Filtrer til bestemte ressursorganisasjonsenheter som må synkroniseres med denne malen.
- Hvis faktisk konsernintern tid eller faktiske konserne utgifter blir synkronisert til Finance and Operations, må du gjøre om kontraktorganisasjonsenheten til riktig juridisk enhet i Finance and Operations. I malen for faktiske prosjektdata (PSA til Fin and Ops) er en betinget kolonne definert basert på demodata. Du må oppdatere sist innsatte betingelseskolonne til riktige juridiske enheter. Hvis ikke kan det resultere i en integrasjonsfeil eller at feil faktiske transaksjoner importeres til Finance and Operations.
- Hvis faktisk konsernintern tid eller faktiske konserne utgifter ikke synkroniseres til Finance and operations, må du slette sist innsatte betingelseskolonne fra malen. Hvis ikke kan det resultere i en integrasjonsfeil eller at feil faktiske transaksjoner importeres til Finance and Operations.

#### <a name="contract-organizational-unit"></a>Kontraktorganisasjonsenhet
For å oppdatere den innsatte betingelseskolonnen i malen klikker du på **Tilordne**-pilen for å åpne tilordningen. Velg koblingen **Avansert spørring og filtrering** for å åpne Power Query.

- Hvis du bruker standardmalen for faktiske prosjektdata (PSA til Fin and Ops), velger du siste **Innsatt betingelse** i delen **Brukte trinn** i Power Query. I **Funksjon**-oppføringen erstatter du **USSI** med navnet på den juridiske enhet som skal brukes med integreringen. Legg til flere betingelser i **Funksjon**-oppføringen etter behov, og oppdater **else**-betingelsen fra **USMF** til riktig juridisk enhet.
- Hvis du oppretter en ny mal, må du legge til kolonnen for å støtte konsernintern(e) tid og utgifter. Velg **Legg til betinget kolonne**, og angi et navn for kolonnen, for eksempel **JuridiskEnhet**. Angi en betingelse for kolonnen, der hvis **msdyn\_contractorganizationalunitid.msdyn\_name** er \<organisasjonsenhet\>, deretter \<angi den juridiske enheten\>, hvis ikke null.

### <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonene nedenfor viser et eksempel på maloppgavetilordning i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Project Service Automation til Finance and Operations.

[![Tilordning av mal](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Tilordning av mal](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importere fra oppsamlingstabell etter integrering fra Project Service Automation

Import fra periodisk prosess for oppsamlingstabell må utføres etter synkronisering av faktiske data fra Project Service Automation til Finance and Operations. Denne prosessen importerer prosjekttransaksjonene fra oppsamlingstabellen til Project Service Automation-integrasjonsjournalen, der regnskapet brukes og de importerte transaksjonene kan posteres. Vi anbefaler at du kjører denne prosessen i satsvis modus. Om ønskelig kan den defineres til å kjøre som en gjentakende satsvis jobb.

## <a name="update-actuals-from-finance-and-operations"></a>Oppdatere faktiske data fra Finance and Operations

### <a name="template-and-tasks"></a>Mal og oppgaver

Følgende mal og underliggende oppgaver brukes til å synkronisere bilagsnummeret og merverdiavgifter for posterte prosjekttransaksjoner fra Finance and Operations til Project Service Automation:

- **Navnet på malen i Dataintegrering:** Faktiske prosjektdata-oppdatering (Fin Ops til PSA)
- **Navn på oppgavene i prosjektet:**

    - Faktiske beløp 
    - TransactionConnections

### <a name="entity-set"></a>Enhetssett

| Finance and Operations                                   | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Enhet for integrering av faktiske prosjektdata                   | Faktiske beløp                    |
| Integreringsenhet for relasjoner for prosjekttransaksjon | Transaksjonstilkoblinger    |

### <a name="entity-flow"></a>Enhetsflyt

Faktiske prosjektdata administreres i Project Service Automation, og de synkroniseres til prosjektinterasjonsjournalen i Finance and Operations. Når faktiske data er postert i Finance and Operations, oppdateres de i Project Service Automation med bilagsnummeret fra Finance and Operations. Hvis merverdiavgifter ble lagt til i Finance and Operations, opprettes nye faktiske avgiftsdata i Project Service Automation.

### <a name="power-query"></a>Power Query

I oppdateringsmalen for faktiske prosjektdata kan du bruke Power Query til å fullføre disse oppgavene:

- Transformer Finance and Operations-transaksjonstypen til riktig transaksjonstype i Project Service Automation. Denne transformasjonen er allerede definert i malen for oppdatering av faktiske prosjektdata (PSA til Fin and Ops).
- Transformer Finance and Operations-faktureringstypen til riktig faktureringstype i Project Service Automation. Denne transformasjonen er allerede definert i malen for oppdatering av faktiske prosjektdata (PSA til Fin and Ops).

### <a name="template-mapping-in-data-integration"></a>Maltilordning i Dataintegrering

Illustrasjonen nedenfor viser eksempler på maloppgavetilordningene i Dataintegrering. Tilordningen viser feltinformasjonen som vil bli synkronisert fra Finance and Operations til Project Service Automation.

[![Tilordning av mal](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Tilordning av mal](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)
