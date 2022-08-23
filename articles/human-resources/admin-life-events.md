---
title: Angi administratorrettigheter for livshendelser
description: Denne artikkelen forklarer hvordan du konfigurerer administratorrettigheter for levetidshendelser i Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/01/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BenefitWorkspace, HcmBenefitSummaryPart
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9deed240977394667cee8b107397267b182d960b
ms.sourcegitcommit: e0905a3af85d8cdc24a22e0c041cb3a391c036cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/06/2022
ms.locfileid: "9229904"
---
# <a name="set-administrator-rights-for-life-events"></a>Angi administratorrettigheter for livshendelser

[!include [banner](../includes/preview-banner.md)]

Administratorer kan oppdatere alternativer for livshendelser, avhengig av konfigurasjonsinnstillinger. På siden **Personalparametere** kan du konfigurere parametere som gjør det mulig for administratorer å foreta endringer i planvalgene. Du kan også begrense administratorer helt fra å foreta endringer.

På siden **Personaleparametere** kan du definere planendringsrestriksjoner for bekreftede planer og alternativer for livshendelse.

Hvis alternativet **Bekreftede planer** er valgt, kan det bare gjøres endringer hvis en registreringsperiode er aktiv. (Eksempler på registreringsperioder omfatter åpne registreringsperioder, nye registreringsperioder for ansettelse og registreringsperioder for livshendelse.) Hvis dette alternativet ikke er valgt, kan du når som helst foreta endringer.

Hvis alternativet **Livshendelsesalternativer** er valgt, begrenses planendringer i løpet av en levetidshendelse av alternativene for levetidshendelse som er definert i plantypen. Hvis dette alternativet ikke er valgt, kan planvalg endres under en livshendelse.

## <a name="set-plan-change-restrictions"></a>Angi planendringsrestriksjoner

Følgende felter er tilgjengelige på siden **Personalparametere** på fanen **Fordelsbehandling**:

| Felt | Beskrivelse |
|-------|-------------|
| Bekreftede planer | Velg dette alternativet hvis endringer i en plan bare er tillatt hvis en registreringsperiode er aktiv. Hvis dette alternativet ikke er valgt, kan du når som helst foreta endringer. |
| Alternativer for levetidshendelse | Velg dette hvis planendringer i løpet av en levetidshendelse er begrenset av levetidshendelsen som er definert i plantypen. Hvis dette alternativet ikke er valgt, kan planvalg endres under en livshendelse. |
