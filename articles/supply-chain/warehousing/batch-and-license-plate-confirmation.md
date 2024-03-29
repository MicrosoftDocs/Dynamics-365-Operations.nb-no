---
title: Parti- og nummerskiltbekreftelse
description: Denne artikkelen beskriver hvordan du definerer og bruker parti- og nummerskiltbekreftelse fra en mobilenhet.
author: Mirzaab
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef0d528d23c1ee9424e35e29d39121d42ba548e5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903731"
---
# <a name="batch-and-license-plate-confirmation"></a>Parti- og nummerskiltbekreftelse

[!include [banner](../includes/banner.md)]

Partibekreftelse lar deg bekrefte at det riktige partiet velges fra mobilenheten. Første gang du plukker arbeid bare for *Parti-over\[sted\]*, der parti over angir at partiet er plassert høyere enn plasseringen i søkehierarkiet, må du bekrefte at partiet som plukkes, samsvarer med partiet på arbeidslinjen.

Nummerskiltbekreftelse lar deg bekrefte at det nummerskiltet velges fra mobilenheten. Når du plukker arbeid fra en stadielokasjon, må du bekrefte at nummerskilt som plukkes, svarer til nummerskiltet som er knyttet til arbeidet. Hvis arbeidet startes ved å skanne et nummerskilt, utelates dette bekreftelsestrinnet.

## <a name="where-it-applies"></a>Der det er aktuelt

Bekreftelse gjelder i følgende scenarier:

- Partibekreftelse gjelder for de første plukkingene av arbeid for parti over-varer.
- Nummerskiltbekreftelse gjelder for plukking fra stadielokasjoner.

> [!IMPORTANT]
> Etterfylling støttes ikke for nummerskiltbekreftelse. Når du utfører etterfyllingsarbeid, opprettes det ikke noe trinn for nummerskiltbekreftelse.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Konfigurere parti- og nummerskiltbekreftelse

Du kan konfigurere parti- og nummerskiltbekreftelse fra menyelementene på mobilenheten.

1. Gå til arbeidsbekreftelsesoppsettet fra menyelementene på mobilenheten.  
1. Velg alternativet for partibekreftelse eller nummerskiltbekreftelse. Begge alternativene er tilgjengelige for arbeidstypeplukk der automatisk bekreftelse ikke er aktivert.  


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
