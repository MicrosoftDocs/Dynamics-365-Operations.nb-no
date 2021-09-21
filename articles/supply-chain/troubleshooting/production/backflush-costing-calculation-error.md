---
title: Feil under backflush-etterkalkulering under lagerlukking
description: I tidligere versjoner kan du ha mottatt en feil under backflush-etterkalkulering under lagerlukking. Problemet er løst.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: ae92b7121998d6b1ba2f08ea5736c55637867fbf
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477185"
---
# <a name="backflush-costing-calculation-error-during-inventory-closing"></a>Feil under backflush-etterkalkulering under lagerlukking

## <a name="symptoms"></a>Symptomer

Hvis du ikke bruker flyten for trimmet produksjons-kostnadsflyten i utgivelser før utgivelse 10.0.13, får du følgende feilaktige advarselsmeldinger under lagerlukking:

> Du er i ferd med å utføre en lagerlukking med en dato %1. Ingen kjøringer av beregning av backflush-etterkalkulering med en dato %1 som samsvarer med periodeslutt, er registrert. Husk å kjøre en beregning av backflush-etterkalkulering med en dato for %1 som samsvarer med periodeslutt. Verdien av lagerbeholdningene, solgte varers kost og avvik er kanskje ikke riktige i underfinansjournaler eller økonomimodulen før dette er utført.

## <a name="resolution"></a>Løsning

Dette problemet er løst i utgivelsen 10.0.13 og nyere. Hvis du vil ha mer informasjon, kan du se [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).
