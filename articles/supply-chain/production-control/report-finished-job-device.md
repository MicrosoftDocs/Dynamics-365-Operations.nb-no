---
title: Rapportere som fullført til en lokasjon som ikke er kontrollert av nummerskilt fra jobbkortenheten
description: Dette emnet beskriver prosessen for å fullføre ferdige produkter på en produksjonsordre til lager når et nummerskilt styrer lokasjonen.
author: johanhoffmann
manager: AnnBe
ms.date: 09/06/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: 35ad27a6b8a52bfd086fbe4fc57b1681ff88fd5b
ms.sourcegitcommit: 58db26b7edf02e7c33aaaf1c934e3263aa74b01f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/11/2019
ms.locfileid: "1995148"
---
[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Rapportere som fullført til en lokasjon som ikke er kontrollert av nummerskilt fra jobbkortenheten 

Prosessen som kalles Ferdigmelding, fullfører ferdig produkter på en produksjonsordre til lageret. Hvis det ferdige produktet er aktivert for de avanserte lagerprosessene, blir produktet rapportert som ferdig til en lokasjon som kalles produksjonsutleveringssted. Hvis du vil ha informasjon om hvordan du definerer produksjonsutleveringssted, kan du se [Produksjonsutleveringssted](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Du må velge et eksisterende skiltnummeret for å fullføre denne oppgaven. Hvis produksjonsutleveringsstedet er konfigurert for sporing etter nummerskilt, må et skiltnummer inkluderes ved rapportering av produksjonsutleveringsstedet som ferdig. Feltet **Nummerskilt** vises i meldingen **Rapportfremdrift** på siden **Jobbkortenhet**. Feltet vises bare i meldingen **Rapportfremdrift** ved rapportering om den siste operasjonen i produksjonsordren. Feltet vises bare hvis varen for produksjonsordren er aktivert for lagerstyrings prosessene. 
