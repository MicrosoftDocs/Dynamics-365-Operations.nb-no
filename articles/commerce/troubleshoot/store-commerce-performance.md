---
title: Feilsøk ytelsesproblemer med Store Commerce-tillegget
description: Denne artikkelen beskriver hvordan du feilsøker ytelsesproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.
author: mugunthanm
ms.date: 06/01/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.search.industry: Retail
ms.author: rassadi
ms.search.validFrom: 2022-05-12
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: fef4eb7063f4acdbca5fab2ad33ec10e0cb603bd
ms.sourcegitcommit: c271b2edc4bf777f7194b09139ccbd174a359c75
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169053"
---
# <a name="troubleshoot-store-commerce-performance-issues"></a>Feilsøk ytelsesproblemer med Store Commerce-tillegget

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du feilsøker ytelsesproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.

- Når du feilsøker ytelsesproblemer for Store Commerce, må du unngå ekstern pålogging. Logg deg i stedet direkte på Store Commerce-enheten.
- Hvis Store Commerce-appen går tregt, må du kontrollere CPU, minne, nettverk og diskbruk ved hjelp av Oppgavebehandling eller Ressursovervåking. Sørg for at det ikke er noe signifikant forbruk av enhetsressursene.
- Kontroller tilkoblingsstatusen på nettverket, og bekreft at HTTPS-forespørsler/-svar ikke tar mer enn et par sekunder.
