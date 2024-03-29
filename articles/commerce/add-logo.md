---
title: Legge til en logo
description: Denne artikkelen beskriver hvordan du legger til en logo på området ditt i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.search.form: ''
ms.openlocfilehash: 4bd47907791edfd0ab81282bd1e465ac54172cdf
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278104"
---
# <a name="add-a-logo"></a>Legge til en logo

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du legger til en logo på området ditt i Microsoft Dynamics 365 Commerce.

Noe av det første du gjør når du bygger området, er å legge til selskapet eller merkelogoen i overskriften til området. Det elektroniske modulbiblioteket for Dynamics 365 Commerce gir en modul som gjør denne oppgaven lett.

Du kan legge til en logo direkte i en mal, et oppsett eller en side. På denne måten kan du enkelt endre logoen som vises på bestemte sider eller i grupper med sider. Denne artikkelen dekker imidlertid det hyppigste scenarioet, der du legger til logoen din i et topptekstfragment som kan brukes på nytt på tvers av alle sidene på området.

## <a name="prerequisites"></a>Forutsetninger

Før du kan legge til en logo på alle sidene på området, må du fullføre disse oppgavene.

1. Last opp logoen til mediebiblioteket.
1. Lag et topptekstfragment. Hvis du vil ha mer informasjon om hvordan du oppretter og bruker fragmenter, se [Arbeide med fragmenter](work-with-fragments.md).
1. Inkluder topptekstfragmentet i malen som sidene på området bruker for alternativene for oppsett og modul. Hvis du vil ha mer informasjon om maler, kan du se [Arbeide med maler](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Legge til en logo i et topptekstfragment

Følg denne fremgangsmåten for å legge til en logo i topptekstfragmentet for området.

1. Velg **Fragmenter** i navigasjonsruten til venstre.
1. Velg topptekstfragmentet du opprettet, og velg deretter **Rediger**.
1. Utvid hodemodulen.
1. I egenskapsruten for hodemodulen angir du et bilde og en kobling for logoen. 
1. Lagre topptekstfragmentet, fullfør redigeringen av det, og publiser det.

Når du har publisert det oppdaterte topptekstfragmentet, vil alle områdesidene som bruker malen som inneholder topptekstfragmentet, vise logoen.

## <a name="additional-resources"></a>Tilleggsressurser

[Velge et områdetema](select-site-theme.md)

[Arbeide med CSS-overstyringsfiler](css-override-files.md)

[Legge til et favorittikon](add-favicon.md)

[Legge til en opphavsrettserklæring](add-copyright-notice.md)

[Legge til språk på området](add-languages-to-site.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
