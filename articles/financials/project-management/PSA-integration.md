---
title: Project Service Automation
description: Dette emnet gir informasjon om integrasjonsløsningen Project Service Automation til Finance and Operations. Denne integreringsløsningen bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service.
author: KimANelson
manager: AnnBe
ms.date: 06/29/2018
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
ms.openlocfilehash: 4b1d2ae69899a2937d47f6547ee4ba72b2d1ece4
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "335698"
---
# <a name="project-service-automation"></a>Project Service Automation

[!include[banner](../includes/banner.md)]

Løsningen Project Service Automation til Finance and Operations bruker Dataintegrering-funksjonen til å synkronisere data på tvers av forekomster av Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service. Integrasjonsmalene som er tilgjengelige i dataintegreringsfunksjonen, muliggjør flyt av prosjekter, prosjektkontrakter, prosjektkontraktlinjer, milepæler på prosjektkontraktlinjer, prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater og utgiftsestimater fra Project Service Automation til Finance and Operations.

> [!NOTE]
> - Hvis du bruker Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3.0 når du har installert KB 4132657 og KB 4132660, vil du kunne bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske data, og du vil kunne konfigurere funksjonslåsing. Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.
> - Hvis du bruker Finance and Operations 7.3.0, må du installere KB 4074835. Du vil da kunne integrere fastprisprosjekter.
> - Hvis du bruker Finance and Operations 7.3.0, og du henter gebyrtransaksjoner fra Project Service Automation, må du installere KB 4345320 for å inkludere disse gebyrene i prosjektfakturaen.
> - Hvis du bruker Microsoft Dynamics 365 for Finance and Operations versjon 8.0, vil du kunne bruke prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet.
> - Hvis du bruker Microsoft Dynamics 365 for Finance and Operations versjon 8.0.1 eller senere, vil du ikke kunne synkronisere faktiske data.

Før du kan integrere Project Service Automation med Finance and Operations, må du konfigurere Project Service Automation-integrasjonsparameterne. Hvis du vil ha mer informasjon, kan du se [Project Service Automation-integreringsparameterne](PSA-parameters.md).

Denne integreringsløsningen muliggjør direkte synkronisering i følgende scenarioer:

- Oppretthold prosjektkontrakter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Opprett prosjekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Oppretthold prosjektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Oppretthold milepæler på prosjektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Oppretthold prosjektoppgaver i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Oppretthold utgiftstransaksjonskategorier i Finance and Operations, og synkroniser dem direkte fra Finance and Operations til Project Service Automation.
- Opprett prosjekttimeestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Opprett prosjektutgiftsestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Opprett faktiske data for prosjekttid, utgifter og avgifter i Project Service Automation, og opprett prosjekttransaksjoner i Project Service Automation-integrasjonsjournalen, slik at de kan posteres i Finance and Operations.

## <a name="data-synchronization"></a>Datasynkronisering

Illustrasjonen nedenfor viser hvordan dataene synkroniseres som en del av integreringen mellom Project Service Automation og Finance and Operations.

> [!NOTE]
> Ikke alle maler er tilgjengelige. Maler gis ut når de er fullført.

[![Project Service Automation-integrasjon med Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Systemkrav for Finance and Operations

Hvis du vil bruke Project Service Automation to Finance and Operations-integrasjonsløsningen, må du installere Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition 7.3 med plattformoppdatering 12 eller senere.

## <a name="system-requirements-for-project-service-automation"></a>Systemkrav for Project Service Automation

Hvis du vil bruke Project Service Automation til Finance and Operations-integrasjonsløsningen, må du installere følgende komponenter:

- Microsoft Dynamics 365 for Project Service Automation versjon 9.0.0.0 eller senere
- Kundeemne til kontanter-løsningen for Microsoft Dynamics 365 for Sales, versjon 1.14.0.0 (v14) eller senere
- Project Service Automation til Finance and Operations-løsning for Microsoft Dynamics 365 for Project Service Automation versjon 1.0.0.0 eller senere

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Installer Project Service Automation til Finance and Operations-integrasjonsløsningen i Project Service Automation-forekomsten

Last ned Project Service Automation til Finance and Operations-integrasjonsløsningen fra [Microsoft Download Center](https://www.microsoft.com/en-us/download/details.aspx?id=57016), og følg instruksjonene som er inkludert i løsningen.
