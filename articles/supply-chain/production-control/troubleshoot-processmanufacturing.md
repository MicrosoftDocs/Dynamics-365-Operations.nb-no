---
title: Feilsøk prosessproduksjon
description: Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med prosessproduksjon.
author: SmithaNataraj
manager: tfehr
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 63993fca2164301d31dbfa1474a4cf5eb16273e6
ms.sourcegitcommit: 8eefb4e14ae0ea27769ab2cecca747755560efa3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/13/2020
ms.locfileid: "4516843"
---
# <a name="troubleshoot-process-manufacturing"></a>Feilsøk prosessproduksjon

Dette emnet beskriver hvordan du løser problemer som kan oppstå mens du arbeider med prosessproduksjon.

## <a name="when-i-use-the-job-card-device-to-report-a-partial-quantity-on-the-last-job-in-a-production-order-all-the-previous-jobs-on-that-order-that-have-a-status-of-in-progress-are-automatically-ended"></a>Når jeg bruker prosjektkortenheten til å rapportere et delvis antall i det siste prosjektet i en produksjonsordre, avsluttes alle de forrige prosjektene i den ordren som har statusen Pågår automatisk.

Denne virkemåten er standard. På siden **Produksjonsordrestandarder** i fanen **Ferdigmeld** finnes det et alternativ som heter **Sluttmerk rute**. Hvis dette emnet er satt til *Ja*, posteres en rutekortjournal når en arbeider bruker prosjektkortenheten eller prosjektkortterminalen til å rapportere den siste operasjonen. Denne journalen markerer alle operasjoner som fullført, og avslutter alle produksjonsprosjektene. Når **Sluttmerk rute**-alternativet er satt til *Ja*, vurderer ikke systemet prosjektstatusen som arbeideren valgte da vedkommende sist rapporterte operasjonen. Systemet vurderer heller ikke om arbeideren rapporterer et fullstendig eller delvis antall.

## <a name="when-i-attempt-a-stock-closing-i-receive-the-following-warning-message-no-execution-of-backflush-costing-calculation-with-a-date-1-matching-period-end-has-been-registered"></a>Når jeg prøver å foreta en lagerlukking, får jeg følgende advarsel: Ingen utførelse av beregning av backflush-etterkalkulering med en dato %1 som samsvarer med periodeslutt, er registrert.

Hvis du ikke bruker flyten for trimmet produksjons-kostnadsflyten i utgivelser før utgivelse 10.0.13, får du følgende feilaktige advarselsmeldinger under lagerlukking:

> Du er i ferd med å utføre en lagerlukking med en dato %1. Ingen kjøringer av beregning av backflush-etterkalkulering med en dato %1 som samsvarer med periodeslutt, er registrert. Husk å kjøre en beregning av backflush-etterkalkulering med en dato for %1 som samsvarer med periodeslutt. Verdien av lagerbeholdningene, solgte varers kost og avvik er kanskje ikke riktige i underfinansjournaler eller økonomimodulen før dette er utført.

Dette problemet er løst i utgivelsen 10.0.13 og nyere. Hvis du vil ha mer informasjon, kan du se [KB 4582468](https://fix.lcs.dynamics.com/Issue/Details?kb=4582468&bugId=468844&dbType=3&qc=fcd64080446a27382cfde3e4c3bdcfb714279185932259cd11ceb0d500617296).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]