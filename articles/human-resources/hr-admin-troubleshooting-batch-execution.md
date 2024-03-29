---
title: Tilbakestille satsvise jobber som står fast
description: Denne artikkelen beskriver hvordan du løser problemer med satsvise jobber som står fast.
author: twheeloc
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2021-03-19
ms.dyn365.ops.version: Platform update 42
ms.openlocfilehash: b56a16257a45dd093d10b7550b13d6a4a1ceb1f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8896025"
---
# <a name="reset-stuck-batch-jobs"></a>Tilbakestille satsvise jobber som står fast


[!INCLUDE [PEAP](../includes/peap-2.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

## <a name="issue"></a>Problem

Microsoft Dynamics 365 Human Resources kan oppleve problemer med satsvise jobber som står fast i enten en **Kjører** eller **Avbryter**-tilstand, og som ikke fullføres.

## <a name="resolution"></a>Oppløsning

Når en satsvis jobb blir stående fast i en **Kjører**- eller **Avbryter**-tilstand, kan du tilbakestille statusen ved å fremtvingen at jobben avbrytes. Når du har avbrutt den, kan du tilbakestille den satsvise jobben ved å angi den til **Venter**-status. Deretter blir den plukket opp på nytt for utføring i neste planlagte satsvise kjøring.

1. I arbeidsområdet **Systemadministrasjon** velger du **Koblinger**-siden og velger deretter **Satsvise jobber**.

2. På listesiden **Satsvis jobb** velger du jobben som må tilbakestilles.

3. På handlingsbåndet velger du **Tving avbrudd**, og bekreft deretter handlingen.

   > [!NOTE]
   > Handlingen **Tving avbrudd** er bare tilgjengelig når den valgte satsvise jobben har statusen **Kjører** eller **Avbryter**, og ingen prosesser for satsvise kjøring eller avbrudd kjører for jobben.

4. På handlingsbåndet velger du **Endre status**.

5. På siden **Velg ny status** velger du **Venter** og velger deretter **OK**.

   ![Velge en ny status for den satsvise jobben.](./media/hr-admin-reset-batch-job-status.png)

## <a name="see-also"></a>Se også

[Optimalisere ytelsen ved å planlegge satsvise jobber etter timer](hr-admin-troubleshooting-batch-jobs.md)<br>
[Optimalisere ytelsen med oppgaver for automatisk opprydding](hr-admin-troubleshooting-batch-history.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
