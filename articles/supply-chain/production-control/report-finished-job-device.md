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
ms.openlocfilehash: cb809e596fd6bf3030bcee460838798435512b95
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572135"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Rapportere som fullført til en lokasjon som ikke er kontrollert av nummerskilt fra jobbkortenheten 

Prosessen som kalles Ferdigmelding, fullfører ferdig produkter på en produksjonsordre til lageret. Hvis det ferdige produktet er aktivert for de avanserte lagerprosessene, blir produktet rapportert som ferdig til en lokasjon som kalles produksjonsutleveringssted. Hvis du vil ha informasjon om hvordan du definerer produksjonsutleveringssted, kan du se [Produksjonsutleveringssted](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Du må velge et eksisterende skiltnummeret for å fullføre denne oppgaven. Hvis produksjonsutleveringsstedet er konfigurert for sporing etter nummerskilt, må et skiltnummer inkluderes ved rapportering av produksjonsutleveringsstedet som ferdig. Feltet **Nummerskilt** vises i meldingen **Rapportfremdrift** på siden **Jobbkortenhet**. Feltet vises bare i meldingen **Rapportfremdrift** ved rapportering om den siste operasjonen i produksjonsordren. Feltet vises bare hvis varen for produksjonsordren er aktivert for lagerstyrings prosessene. 
