---
title: Rapportere som fullført til en lokasjon som ikke er kontrollert av nummerskilt fra jobbkortenheten
description: Dette emnet beskriver prosessen for å fullføre ferdige produkter på en produksjonsordre til lager når et nummerskilt styrer lokasjonen.
author: johanhoffmann
manager: tfehr
ms.date: 01/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: JmgRegistration, ProdJournalTransJob, ProdJournalTransRoute, ProdParmReportFinished
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19351
ms.assetid: bcc9e242-b4b8-4144-b14d-c3c106fb40ec
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2019-09-06
ms.dyn365.ops.version: AX 10.0.6
ms.openlocfilehash: f5863202facc83afb91b380ba5666334783ccbcf
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3211175"
---
[!include [banner](../includes/banner.md)]

# <a name="report-as-finished-to-a-license-plate-controlled-location-from-the-job-card-device"></a>Rapportere som fullført til en lokasjon som ikke er kontrollert av nummerskilt fra jobbkortenheten 

Prosessen som kalles Ferdigmelding, fullfører ferdig produkter på en produksjonsordre til lageret. Hvis det ferdige produktet er aktivert for de avanserte lagerprosessene, blir produktet rapportert som ferdig til en lokasjon som kalles produksjonsutleveringssted. Hvis du vil ha informasjon om hvordan du definerer produksjonsutleveringssted, kan du se [Produksjonsutleveringssted](https://docs.microsoft.com/dynamics365/unified-operations/supply-chain/production-control/production-output-location).

Hvis produksjonsutleveringsstedet er nummerskiltkontrollert, må det oppgis et nummerskilt ved rapportering som fullført. Feltet **Nummerskilt** vises i meldingen **Rapportfremdrift** på siden **Jobbkortenhet**. Feltet er bare synlig i **Rapportfremdrift**-ledeteksten når rapportering på siste operasjon av produksjonsordren og varen for produksjonsordren er aktivert for lagerstyringsprosessene. 

Det er to alternativer for å gi nummerskiltet
- Brukeren velger et eksisterende nummerskilt i nummerskiltfeltet.
- Nummerskiltet genereres automatisk fra en nummerserie og hentes som standard til nummerskiltfeltet.

Alternativet for å få nummerskiltet genererert automatisk, konfigureres ved å velge alternativet **Generer nummerskilt** på siden **Konfigurer jobbkort for enheter**.
