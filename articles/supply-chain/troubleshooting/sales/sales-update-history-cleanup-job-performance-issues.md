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
ms.openlocfilehash: c02273adf90afc67b7c0ae1b82c19d489bfbd3b1
ms.sourcegitcommit: 008779c530798f563fe216810d34b2d56f2c8d3c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/14/2021
ms.locfileid: "7920080"
---
# <a name="sales-update-history-cleanup-job-fails-or-has-performance-issues"></a>Oppryddingsjobb i salgsoppdateringshistorikk mislykkes eller har ytelsesproblemer

## <a name="symptoms"></a>Symptomer

Den satsvise jobben **Opprydding av salgsoppdateringshistorikk** mislykkes eller har ytelsesproblemer.  

## <a name="cause"></a>Årsak

Dette kan skje når systemet inneholder en rekke salgsoppdateringer, som kan føre til store mengder salgsoppdateringsdata. Oppryddingsjobben prøver å rydde opp i alle disse dataene i én transaksjon. Jobben kan derfor ta svært lang tid å kjøre eller til og med mislykkes.

## <a name="resolution"></a>Oppløsning

En ny versjon av den satsvise jobben **Opprydding av salgsoppdateringshistorikk** er tilgjengelig for Supply Chain Management, versjon 10.0.19 og nyere. Denne funksjonen er ikke aktivert som standard. Hvis du vil ha mer informasjon om hvordan den fungerer og hvordan du aktiverer den i funksjonsstyring, kan du se [Forbedringer av ytelse for opprydding i salgshistorikk](../../sales-marketing/sales-update-history-cleanup-performance-improvements.md).

