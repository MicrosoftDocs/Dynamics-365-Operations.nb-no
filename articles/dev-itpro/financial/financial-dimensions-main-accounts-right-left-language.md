---
title: "Finansdimensjoner og hovedkontoer på høyre-mot-venstre-språk"
description: "Dette emnet beskriver noen av implementeringsavgjørelsene du bør ta hensyn til når du bruker et høyre-mot-venstre-språk, og du må definere finansdimensjoner og hovedkontoer."
author: aprilolson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 1d98cbff30620256c9d13e7b4a90314db150e33e
ms.openlocfilehash: 9609c052083dc3157618584da9311211ea036eba
ms.contentlocale: nb-no
ms.lasthandoff: 08/09/2018

---

# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Finansdimensjoner og hovedkontoer på høyre-mot-venstre-språk

[!include [banner](../includes/banner.md)]

Dette emnet beskriver noen av implementeringsavgjørelsene du bør ta hensyn til når du bruker et høyre-mot-venstre-språk, og du må definere finansdimensjoner og hovedkontoer.

Finansdimensjoner og hovedkontoer er nøkkelkomponentene i planleggingsfasen for en implementering. Når finansdimensjoner og hovedkontoer er opprettet i systemet, blir de brukt på sidene **Konfigurer kontostrukturer**, **Avanserte regelstrukturer** og **Konfigurasjon av finansdimensjoner for programintegrering**. Rekkefølgen som er definert på disse sidene, brukes til dataregistrering og forbruk i systemet. Noen steder i systemet vises finansdimensjonen og hovedkontoene i separate felt. Andre steder, for eksempel i journaler, vises imidlertid finansdimensjoner og hovedkontoer som en enkelt streng.

### <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Anbefalte fremgangsmåter for definering av finansdimensjoner og hovedkontoer i et høyre-mot-venstre-system

-   Når du velger skilletegn for kontoplaner, velger du ett av alternativene for dobbel skilletegn: doble bindestrek (-), dobbel strek (|) eller doble punktum (..) eller dobbel understreking (\_\_).
-   Når du oppretter finansdimensjons- og hovedkontoverdier, kan du bare bruke tall og tegn for høyre-mot-venstre-språk.
-   Unngå å bruke det valgte skilletegnet for kontoplanen i finansdimensjons- og hovedkontoverdier.

Ved å følge disse anbefalte fremgangsmåtene, kan du hjelpe å garantere konsekvent presentasjon av den brukerdefinerte ordren i hele systemet.




