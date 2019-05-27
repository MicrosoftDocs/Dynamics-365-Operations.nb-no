---
title: Parti- og nummerskiltbekreftelse
description: Dette emnet beskriver hvordan du definerer og bruker parti- og nummerskiltbekreftelse fra en mobilenhet.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSRFAutoConfirm
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: efab5b11782fd2344fb5f532272007d187c1465b
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563923"
---
# <a name="batch-and-license-plate-confirmation"></a>Parti- og nummerskiltbekreftelse

[!include [banner](../includes/banner.md)]

Partibekreftelse lar deg bekrefte at det riktige partiet velges fra mobilenheten. Første gang du plukker arbeid bare for parti over-varer, der parti over angir at partiet går høyere enn plasseringen i søkehierarkiet, må du bekrefte at partiet som plukkes, samsvarer med partiet på arbeidslinjen. 

Nummerskiltbekreftelse lar deg bekrefte at det nummerskiltet velges fra mobilenheten. Når du plukker arbeid fra en stadielokasjon, må du bekrefte at nummerskilt som plukkes, svarer til nummerskiltet som er knyttet til arbeidet. Hvis arbeidet startes ved å skanne et nummerskilt, utelates dette bekreftelsestrinnet.

## <a name="where-it-applies"></a>Der det er aktuelt
Bekreftelse gjelder i følgende scenarier:

- Partibekreftelse gjelder for de første plukkingene av arbeid for parti over-varer.
- Nummerskiltbekreftelse gjelder for plukking fra stadielokasjoner.

## <a name="set-up-batch-and-license-plate-confirmation"></a>Konfigurere parti- og nummerskiltbekreftelse
Du kan konfigurere parti- og nummerskiltbekreftelse fra menyelementene på mobilenheten.  
1.  Gå til arbeidsbekreftelsesoppsettet fra menyelementene på mobilenheten.  
2.  Velg alternativet for partibekreftelse eller nummerskiltbekreftelse. Begge alternativene er tilgjengelige for arbeidstypeplukk der automatisk bekreftelse ikke er aktivert.  
