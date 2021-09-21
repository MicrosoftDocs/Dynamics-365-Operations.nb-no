---
title: Gjøre en lagerstatusendring for delvis arbeid av antall
description: Denne siden beskriver hvordan du oppretter et menyelement med de riktige innstillingene for å gjøre det mulig for arbeidere å foreta en lagerstatusendring for delvis antall i et parti.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 056ce412955808ddf126025ad917b874c54a5e62
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477150"
---
# <a name="enable-inventory-status-change-for-partial-quantity-work"></a>Aktiver lagerstatusendring for delvis arbeid av antall

## <a name="symptoms"></a>Symptomer

Du må utføre en lagerstatusendring for et delvis antall i et parti.

## <a name="resolution"></a>Løsning

Hvis du vil at arbeidere skal kunne utføre denne endringen, kan du opprette et menyelement for mobilappen Lagerstyring. Opprett (eller rediger) et menyelement som har følgende innstillinger på siden **Menyelementer på mobilenheten**:

- **Modus:** *Arbeid*
- **Bruke eksisterende arbeid:** *Nei*
- **Arbeidsopprettelsesprosess:** *Flytting*
- **Vis beholdningsstatus:** *Ja*

Du kan angi andre felter på siden slik du ønsker.
