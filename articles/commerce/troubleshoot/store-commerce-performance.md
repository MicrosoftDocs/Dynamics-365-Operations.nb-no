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
ms.openlocfilehash: b690e35b2df736f3e277260e6f752ef5240b0938
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8870498"
---
# <a name="troubleshoot-store-commerce-performance-issues"></a>Feilsøk ytelsesproblemer med Store Commerce-tillegget

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Denne artikkelen beskriver hvordan du feilsøker ytelsesproblemer i Microsoft Dynamics 365 Commerce Store Commerce-appen.

- Når du feilsøker ytelsesproblemer for Store Commerce, må du unngå ekstern pålogging. Logg deg i stedet direkte på Store Commerce-enheten.
- Hvis Store Commerce-appen går tregt, må du kontrollere CPU, minne, nettverk og diskbruk ved hjelp av Oppgavebehandling eller Ressursovervåking. Sørg for at det ikke er noe signifikant forbruk av enhetsressursene.
- Kontroller tilkoblingsstatusen på nettverket, og bekreft at HTTPS-forespørsler/-svar ikke tar mer enn et par sekunder.
