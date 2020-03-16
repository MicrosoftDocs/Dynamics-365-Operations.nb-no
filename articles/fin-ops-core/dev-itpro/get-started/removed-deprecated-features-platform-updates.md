---
title: Fjernede eller avskrevne Platform-funksjoner
description: Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning i plattformoppdateringer av Finance and Operations-apper.
author: sericks007
manager: AnnBe
ms.date: 02/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2020-02-29
ms.dyn365.ops.version: Platform update 33
ms.openlocfilehash: 66e1420c7053c0df9f42b15c55aba1a8c869f02a
ms.sourcegitcommit: 2cc3b89efdd90f8d80883b7a271d7885282ba3e8
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/26/2020
ms.locfileid: "3087889"
---
# <a name="removed-or-deprecated-platform-features"></a>Fjernede eller avskrevne Platform-funksjoner

[!include [banner](../includes/banner.md)]

Dette emnet beskriver funksjoner som er fjernet eller som er planlagt for fjerning i plattformoppdateringer av Finance and Operations-apper.

- En *fjernet* funksjon er ikke lenger tilgjengelig i produktet.
- En *avskrevet* funksjon er ikke i aktiv utvikling og kan bli fjernet i en fremtidig oppdatering.

Denne listen er ment å hjelpe deg med å vurdere disse fjerningene og avskrivningene for din egen planlegging. 

> [!NOTE]
> Detaljert informasjon om objekter i Finance and Operations-apper finnes i [Tekniske referanserapporter](https://mbs.microsoft.com/customersource/northamerica/AX/downloads/reports/axtechrefrep). Du kan sammenligne de ulike versjonene av disse rapportene for å lære om objekter som er endret eller fjernet i hver versjon av Finance and Operations-apper.

## <a name="platform-update-32"></a>Plattform update 32

### <a name="workflow-request-change-dialog-box-no-longer-includes-user-selection-drop-down-list"></a>Dialogboksen Endring av arbeidsflytforespørsel inneholder ikke lenger en rullegardinliste for brukervalg
|   |  |
|------------|--------------------|
| **Årsak til avskrivning/fjerning** | Dette var et sikkerhetsproblem fordi endringsforespørselen kunne sendes til en utilsiktet bruker. Dette var også et bruksproblem, fordi det tvang brukeren til å finne ut hvem arbeidsflytavsenderen var, og manuelt velge dem.  |
| **Erstattet med en annen funksjon?**   | Nei |
| **Berørte produktområder**         | Arbeidsflyt |
| **Distribusjonsalternativ**              | Alle |
| **Status**                         | Rullegardinlisten for brukervalg ble fjernet fra dialogboksen for forespørselsendring i Platform Update 32. Forespørsler om forespørselsendring sendes automatisk til avsenderen som planlagt. Hvis du vil ha mer informasjon om denne funksjonaliteten, kan du se [Handlinger i godkjenningsprosesser i en arbeidsflyt](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/workflow-actions?toc=%2Fdynamics365%2Fcommerce%2Ftoc.json#request-change). |

## <a name="previous-announcements-about-removed-or-deprecated-features"></a>Tidligere kunngjøringer om fjernede eller avskrevne funksjoner
Hvis du vil lære mer om funksjoner som er fjernet eller avskrevet i tidligere versjoner, kan du se [Fjernede eller avskrevne funksjoner i tidligere versjoner](../migration-upgrade/deprecated-features.md).

