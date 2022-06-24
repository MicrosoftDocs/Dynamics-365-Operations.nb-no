---
title: Finansdimensjoner og hovedkontoer på høyre-mot-venstre-språk
description: Denne artikkelen beskriver beslutningene du må ta når du bruker et høyre-mot-venstre-språk, og du må definere finansdimensjoner og hovedkontoer.
author: RyanCCarlson2
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 222564
ms.assetid: 875dcebb-1bbb-4841-a8c6-9e134da07e96
ms.search.region: global
ms.author: rcarlson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: b1e2c0ef5cd405232332847078c70af42f056e17
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8866767"
---
# <a name="financial-dimensions-and-main-accounts-in-right-to-left-languages"></a>Finansdimensjoner og hovedkontoer på høyre-mot-venstre-språk

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver noen av implementeringsavgjørelsene du bør ta hensyn til når du bruker et høyre-mot-venstre-språk, og du må definere finansdimensjoner og hovedkontoer.

Finansdimensjoner og hovedkontoer er nøkkelkomponentene i planleggingsfasen for en implementering. Når finansdimensjoner og hovedkontoer er opprettet i systemet, blir de brukt på sidene **Konfigurer kontostrukturer**, **Avanserte regelstrukturer** og **Konfigurasjon av finansdimensjoner for programintegrering**. Rekkefølgen som er definert på disse sidene, brukes til dataregistrering og forbruk i systemet. Noen steder i systemet vises finansdimensjonen og hovedkontoene i separate felt. Andre steder, for eksempel i journaler, vises finansdimensjoner og hovedkontoer som en enkelt streng.

## <a name="best-practices-for-setting-up-financial-dimensions-and-main-accounts-in-a-right-to-left-system"></a>Anbefalte fremgangsmåter for definering av finansdimensjoner og hovedkontoer i et høyre-mot-venstre-system

- Når du velger skilletegn for kontoplaner, velger du ett av alternativene for dobbel skilletegn: doble bindestrek (`--`), dobbel strek (`||`) eller doble punktum (`..`) eller dobbel understreking (`\\`).
- Når du oppretter finansdimensjons- og hovedkontoverdier, kan du bare bruke tall og tegn for høyre-mot-venstre-språk.
- Unngå å bruke det valgte skilletegnet for kontoplanen i finansdimensjons- og hovedkontoverdier.

Ved å følge disse anbefalte fremgangsmåtene, kan du hjelpe å garantere konsekvent presentasjon av den brukerdefinerte ordren i hele systemet.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
