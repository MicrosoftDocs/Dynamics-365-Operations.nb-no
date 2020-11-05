---
title: Konfigurere et eksperiment
description: Dette emnet beskriver hvordan konfigurerer et eksperiment i en tredjepartstjeneste.
author: sushma-rao
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: sushmar
ms.search.validFrom: 2020-09-30
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 0f7db0ce009f6ee7603952891aacfdc16fcde016
ms.sourcegitcommit: b6ab46f6e5ce60e2c3d70a348827eaf60c84cae2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/01/2020
ms.locfileid: "3930260"
---
# <a name="set-up-an-experiment"></a>Konfigurere et eksperiment

Når du [definerer en hypotese og fastslår hvilke suksessmåledata du vil bruke](experimentation-identify.md), må du konfigurere eksperimentet i tredjepartstjenesten. Diagrammet nedenfor viser alle trinnene for å konfigurere og kjøre et eksperiment på et nettsted for e-handel i Dynamics 365 Commerce. Flere trinn er beskrevet i separate emner.

[ ![Brukerreise for eksperimentering – konfigurere](./media/experimentation_setup.svg) ](./media/experimentation_setup.svg#lightbox)


## <a name="set-up-your-experiment-in-the-third-party-service"></a>Konfigurere eksperimentet i tredjepartstjenesten
Nå bør du ha valgt tredjepartstjenesten for å kjøre og overvåke eksperimentet og konfigurert eksperimenteringskoblingen. Disse forutsetningene er oppført i [Eksperimentering i Dynamics 365 Commerce](experimentation-overview.md).

Følg trinnene som er nødvendige for å opprette eksperimentet i tredjepartstjenesten. Hvis koblingen er riktig konfigurert, vil den fullstendige listen over eksperimenter du konfigurerer i tredjepartstjenesten, vises i områdebygger i løpet av omtrent 5 minutter.

## <a name="set-up-your-success-metrics"></a>Konfigurere suksessmåledata
Alle eksperimenter trenger måledata for å måle virkningen av variasjonene og validere hypotesen. Følg fremgangsmåten nedenfor for å aktivere beregningen av måledataene i tredjepartstjenesten ved hjelp av hendelser fra livetelemetrihendelser fra Dynamics 365 Commerce.

1. I områdebygger velger du kategorien **Sider** i venstre navigasjonsrute, og deretter velger du siden du vil samle inn måledata for. 
1. Gå til delen **Hendelses-ID-er som skal spores** i egenskapsruten til høyre for siden eller modulen du vil spore.
1. Velg **Vis** . Det vises en liste over alle hendelses-ID-er. Kopier hendelsen du vil spore, og lim inn hendelsesnøkkelen i den angitte plasseringen i tredjepartstjenesten. Hvis du trenger mer enn én hendelse, kopierer du nøklene én om gangen. 
    - Hvis du vil lære hvordan du viser alle tilgjengelige hendelser og attributter, inkludert sidevisninger og inntektssporing, kan du se [Hendelser for Commerce-komponent for diagnose og feilsøking](dev-itpro/retail-component-events-diagnostics-troubleshooting.md).
1. Utfør eventuelle andre trinn for å spore måledata som kreves i tredjepartstjenesten.

## <a name="previous-step"></a>Forrige trinn
[Identifisere en hypotese og fastslå måledataene for et eksperiment](experimentation-identify.md) 


## <a name="next-step"></a>Neste trinn
[Koble til og redigere et eksperiment](experimentation-connect-edit.md)