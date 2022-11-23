---
title: Behandle finanstildelingsjournal
description: Denne artikkelen beskriver hvordan du behandler en tildelingsforespørsel i Dynamics 365 Finance.
author: aprilolson
ms.date: 11/15/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocationRequest, LedgerJournalTable, LedgerJournalTransAllocation
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1f22b5042e0e3726afcb1061852fdbd8de770c61
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779399"
---
# <a name="process-ledger-allocation-journal"></a>Behandle finanstildelingsjournal

[!include [banner](../../includes/banner.md)]

Denne artikkelen beskriver hvordan du behandler en tildelingsforespørsel. Bruk siden **Behandle tildelingsforespørsel** for å opprette en tildelingsjournal som kan du kan vurdere og godkjenne før du posterer den til økonomimodul, eller posterer direkte til økonomimodul. Før du kan opprette en tildelingsjournal, må det være minst én aktiv tildelingsregel for finans. Denne oppgaven bruker demonstrasjonsfirmaet USMF.

1. Gå til **Økonomimodul > Tildelinger > Behandle tildelingsforespørsel** i navigasjonsruten.
2. Velg det ønskede oppslaget på rullegardinmenyen i **Regel**-feltet.
3. Angi en dato i **Per dato**-feltet.

    - **Per dato** er svært viktig når finans er datakilden for regelen. Denne datoen kontrollerer hvilke finanssaldoer som skal inkluderes i tildelingen.  
    - Velg **Stopp** i **Nullkilde**-feltet. Dette vil stanse tildelingsprosessen og vise en melding som indikerer at et nullbeløp er valgt.  

4. I feltet **Forslagsalternativer** velger du **Bare forslag**. Velg **Bare forslag** for å se gjennom og eventuelt godkjenne resultatet i **Tildelingsjournaler** før postering av tildelingen til økonomimodulen.  
5. Angi en dato i feltet **FIN-posteringsdato**.
6. Velg **OK**.
7. Gå til **Moduler > Økonomimodul > Tildelinger > Fordelingsjournaler** i navigasjonsruten.
8. Velg **Linjer**.
9. Velg **Poster**.
10. Velg **Poster**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
