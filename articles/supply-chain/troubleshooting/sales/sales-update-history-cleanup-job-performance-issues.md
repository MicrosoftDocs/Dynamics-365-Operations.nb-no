---
title: Oppryddingsjobb i salgsoppdateringshistorikk mislykkes eller har ytelsesproblemer
description: Den satsvise jobben for opprydding av salgshistorikk kan mislykkes eller ta lang tid hvis det er store mengder salgsoppdateringsdata.
author: myvakalo
ms.date: 10/05/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: myvakalo
ms.search.validFrom: 2021-09-29
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 124fb90ecafd4f4cccbd8a8bb443694c95365732
ms.sourcegitcommit: 197e6ddee84522fd587c6e4ee4f9089101e301c2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2022
ms.locfileid: "8570347"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Oppryddingsjobb i salgsoppdateringshistorikk mislykkes eller har ytelsesproblemer

## <a name="symptoms"></a>Symptomer

Den satsvise jobben **Opprydding av salgsoppdateringshistorikk** mislykkes eller har ytelsesproblemer.  

## <a name="cause"></a>Årsak

Dette kan skje når systemet inneholder en rekke salgsoppdateringer, som kan føre til store mengder salgsoppdateringsdata. Oppryddingsjobben prøver å rydde opp i alle disse dataene i én transaksjon. Jobben kan derfor ta svært lang tid å kjøre eller til og med mislykkes.

## <a name="resolution"></a>Oppløsning

En ny versjon av den satsvise jobben **Opprydding av salgsoppdateringshistorikk** er tilgjengelig for Supply Chain Management, versjon 10.0.19 og nyere. Denne funksjonen er ikke aktivert som standard. Hvis du vil ha mer informasjon om hvordan den fungerer og hvordan du aktiverer den i funksjonsstyring, kan du se [Planlegg opprydding i salgshistorikkdata](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

