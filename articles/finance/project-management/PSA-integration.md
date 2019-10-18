---
title: Oversikt over Project Service Automation
description: Dette emnet inneholder informasjon om integreringsløsningen Dynamics 365 Project Service Automation til Dynamics 365 Finance.
author: KimANelson
manager: AnnBe
ms.date: 07/25/2019
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
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 31d72591041f8d8cc327aa7c6578c15731ba13c5
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250559"
---
# <a name="project-service-automation-overview"></a>Oversikt over Project Service Automation

[!include[banner](../includes/banner.md)]

Løsningen Project Service Automation til Finance bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Dynamics 365 Finance og Dynamics 365 Project Service Automation via Common Data Service. Integrasjonsmalene som er tilgjengelige i dataintegreringsfunksjonen, muliggjør flyt av prosjekter, prosjektkontrakter, prosjektkontraktlinjer, milepæler på prosjektkontraktlinjer, prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater og utgiftsestimater fra Project Service Automation til Finance.

> [!NOTE]
> - Hvis du bruker versjon 7.3.0, må du installere KB 4074835. Du vil da kunne integrere fastprisprosjekter.
> - Hvis du bruker versjon 7.3.0, og du henter gebyrtransaksjoner fra Project Service Automation, må du installere KB 4345320 for å inkludere disse gebyrene i prosjektfakturaen.
> - Hvis du bruker versjon 8.0, vil du kunne bruke prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet.
> - Hvis du bruker versjon 8.0.1 eller nyere, vil du ikke kunne synkronisere faktiske data.

Før du kan integrere Project Service Automation med Finance, må du konfigurere Project Service Automation-integrasjonsparameterne. Hvis du vil ha mer informasjon, kan du se [Project Service Automation-integreringsparameterne](PSA-parameters.md).

Denne integreringsløsningen muliggjør direkte synkronisering i følgende scenarioer:

- Oppretthold prosjektkontrakter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Opprett prosjekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Oppretthold prosjektkontraktslinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Oppretthold milepæler på prosjektkontraktlinje i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Oppretthold prosjektoppgaver i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Oppretthold utgiftstransaksjonskategorier i Finance, og synkroniser dem direkte fra Finance til Project Service Automation.
- Opprett prosjekttimeestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Opprett prosjektutgiftsestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance.
- Opprett faktiske data for prosjekttid, utgifter og avgifter i Project Service Automation, og opprett prosjekttransaksjoner i Project Service Automation-integrasjonsjournalen, slik at de kan posteres i Finance.

## <a name="data-synchronization"></a>Datasynkronisering

Illustrasjonen nedenfor viser hvordan dataene synkroniseres som en del av integreringen mellom Project Service Automation og Finance.

> [!NOTE]
> Ikke alle maler er tilgjengelige. Maler gis ut når de er fullført.

[![Integrering av Project Service Automation med Finance](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>Systemkrav for Finance

Hvis du vil bruke Project Service Automation til Finance-integrasjonsløsningen, må du installere Enterprise Edition 7.3 med Platform update 12 eller nyere.

## <a name="system-requirements-for-project-service-automation"></a>Systemkrav for Project Service Automation

Hvis du vil bruke Project Service Automation til Finance-integrasjonsløsningen, må du installere følgende komponenter:

- Dynamics 365 Project Service Automation versjon 9.0.0.0 eller senere
- Kundeemne til kontanter-løsningen for Dynamics 365 Sales, versjon 1.14.0.0 (v14) eller nyere.
- Project Service Automation til Finance-løsning for Dynamics 365 Project Service Automation versjon 1.0.0.0 eller nyere

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>Installer Project Service Automation til Finance-integrasjonsløsningen i Project Service Automation-forekomsten

Last ned Project Service Automation til Finance-integrasjonsløsningen fra [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), og følg instruksjonene som er inkludert i løsningen.
