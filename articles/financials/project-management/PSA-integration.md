---
title: Project Service Automation
description: "Denne løsningen bruker dataintegreringsfunksjonen til å synkronisere data på tvers av forekomster av Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service (CDS)."
author: KimANelson
manager: AnnBe
ms.date: 11/27/2017
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: 0ad9e6ba7fe8dd915681da8e671ff210de887b1e
ms.contentlocale: nb-no
ms.lasthandoff: 05/29/2018

---

# <a name="project-service-automation"></a>Project Service Automation

Project Service Automation til Finance and Operations-integreringsløsningen bruker dataintegreringsfunksjonen til å synkronisere data på tvers av forekomster av Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation via Common Data Service (CDS). Integrasjonsmalene som er tilgjengelige i dataintegreringsfunksjonen, muliggjør flyt av prosjekter, prosjektkontrakter, prosjektkontraktlinjer, milepæler på prosjektkontraktlinjer, prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater og utgiftsestimater fra Project Service Automation til Finance and Operations.

> [!NOTE] 
> Hvis du bruker Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, må du installere KB 4074835. Dermed kan du integrere fastprisprosjekter.
>
> Hvis du bruker Dynamics 365 for Finance and Operations versjon 8.0, vil du kunne bruke prosjektoppgaveintegrering, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og låsing av funksjonalitet.
>
> Hvis du bruker Dynamics 365 for Finance and Operations versjon 8.0.1, vil du kunne synkronisere faktiske data.
>
> Hvis du bruker Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0 når du har installert KB 4132657 og KB 4132660, vil du kunne bruke malene til å integrere prosjektoppgaver, utgiftstransaksjonskategorier, timeestimater, utgiftsestimater og faktiske data, og du vil kunne konfigurere funksjonslåsing. Hvis du må tilbakestille regnskapsdistribusjonene, anbefaler vi at du også installerer KB 4131710.

Før du kan integrere Project Service Automation med Finance and Operations, må du konfigurere Project Service Automation-integrasjonsparameterne. Hvis du vil ha mer informasjon, kan du se Project Service Automation-integreringsparameterne.

Denne integreringsløsningen muliggjør direkte synkronisering i følgende scenarioer:

- Oppretthold prosjektkontrakter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Opprett prosjekter i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Oppretthold prosjektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Oppretthold milepæler på prosjektkontraktlinjer i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Oppretthold prosjektoppgaver i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Oppretthold utgiftstransaksjonskategorier i Finance and Operations, og synkroniser dem direkte fra Finance and Operations til Project Service Automation.
- Opprett prosjekttimeestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.
- Opprett prosjektutgiftsestimater i Project Service Automation, og synkroniser dem direkte fra Project Service Automation til Finance and Operations.

## <a name="data-synchronization"></a>Datasynkronisering
Illustrasjonen nedenfor viser hvordan dataene synkroniseres som en del av integreringen mellom Project Service Automation og Finance and Operations.

> [!NOTE]
> Ikke alle maler er tilgjengelige. Maler gis ut når de er fullført.

[![Project Service Automation-integrasjon med Finance and Operations](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance-and-operations"></a>Systemkrav for Finance and Operations

Hvis du vil bruke Project Service Automation to Finance and Operations-integrasjonsløsningen, må du installere Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3 med plattformoppdatering 12 eller senere.

## <a name="system-requirements-for-project-service-automation"></a>Systemkrav for Project Service Automation

Hvis du vil bruke Project Service Automation til Finance and Operations-integrasjonsløsningen, må du installere følgende komponenter:

- Microsoft Dynamics 365 for Project Service Automation versjon 9.0.0.0 eller nyere.
- Kundeemne til kontanter-løsningen for Dynamics 365 for Sales, versjon 1.14.0.0 (v14) eller senere.
- Project Service Automation til Operations-løsningen for Dynamics 365 for Project Service Automation versjon 1.0.0.0 eller senere.

## <a name="install-the-project-service-automation-to-finance-and-operations-integration-solution-in-your-project-service-automation-instance"></a>Installer Project Service Automation til Finance and Operations-integrasjonsløsningen i Project Service Automation-forekomsten



