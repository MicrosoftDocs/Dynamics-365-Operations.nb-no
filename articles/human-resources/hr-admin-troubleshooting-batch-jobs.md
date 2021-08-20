---
title: Optimalisere ytelsen ved å planlegge satsvise jobber utenom arbeidstid
description: Dette emnet beskriver hvordan du løser ytelsesproblemer med Microsoft Dynamics 365 Human Resources ved å planlegge tidkrevende satsvise jobber utenom arbeidstid.
author: andreabichsel
ms.date: 06/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-06-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: d2369b3209901eb2d60232a47d89284779199e1c98a56142758353d65a1faaf7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766877"
---
# <a name="optimize-performance-by-scheduling-batch-jobs-after-hours"></a>Optimalisere ytelsen ved å planlegge satsvise jobber utenom arbeidstid

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="issue"></a>Avgang

Microsoft Dynamics 365 Human Resources kan oppleve ytelsesproblemer hvis tidkrevende satsvise jobber kjøres i arbeidstiden.

## <a name="resolution"></a>Oppløsning

Planlegg følgende satsvise jobber utenom arbeidstid. Det anbefales også å se gjennom frekvensen for satsvise jobber som kjører ofte. Reduser gjentakelsen av den satsvise jobben hvis mulig. I mange tilfeller er standardfrekvensen tilstrekkelig.

Følgende satsvise jobber bør kjøres om kvelden eller utenom arbeidstid. Pass på at du kontrollerer tidssonen for disse gjentakende satsvise jobbene. Noen satsvise jobber kan bruke Stillehavskysten (normaltid).

| Satsvis jobb | Standardfrekvens |
| --- | --- |
| Opprydding i logg for satsvis jobb | 1 gang per måned |
| Eksporter opprydding i oppsamling | 1 gang per dag |
| Manglende forespørselssynkronisering for Common Data Service-integrering | 1 gang per dag |
| Systemjobb for databasekomprimering som må kjøres regelmessig utenom arbeidstid | 1 gang per dag |
| Systemjobb for databaseindeksgjenoppbygging som må kjøres regelmessig utenom arbeidstid | 1 gang per dag |

1. Velg **Systemadministrasjon** i Human Resources.

2. I **Søk**-feltet søker du etter en av de satsvise jobbene ovenfor.

3. Velg **Kjør i bakgrunnen**, og velg deretter **Regelmessighet**.

   ![Angi regelmessighet.](media/talent-batch-history-cleanup-recurrence.png)

4. Under **Definer regelmessighet** angir du **Startdato** og **Starttidspunkt** som skal utføres utenom arbeidstiden eller i helgen. Velg **Ingen sluttdato**. 

   ![Definere startdato og -klokkeslettet for regelmessighet.](media/talent-batch-history-cleanup-define-recurrence.png)

5. Velg **OK**.

6. Endre eventuelle andre parametere under **Kjør i bakgrunnen** etter behov, og velg deretter **OK**.

## <a name="additional-resources"></a>Tilleggsressurser

[Optimalisere ytelsen med oppgaver for automatisk opprydding](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]