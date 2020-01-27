---
title: Legge til en logo
description: Dette emnet beskriver hvordan du legger til en logo på området ditt i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 23bac9aae6beb59912bbc9e1f2c6958c007550b0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914630"
---
# <a name="add-a-logo"></a>Legge til en logo

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du legger til en logo på området ditt i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Noe av det første du gjør når du bygger området, er å legge til selskapet eller merkelogoen i overskriften til området. Den elektroniske startpakken for Dynamics 365 Commerce gir en modul som gjør denne oppgaven lett.

Du kan legge til en logo direkte i en mal, et oppsett eller en side. På denne måten kan du enkelt endre logoen som vises på bestemte sider eller i grupper med sider. Dette emnet dekker imidlertid det hyppigste scenarioet, der du legger til logoen din i et topptekstfragment som kan brukes på nytt på tvers av alle sidene på området.

## <a name="prerequisites"></a>Forutsetninger

Før du kan legge til en logo på alle sidene på området, må du fullføre disse oppgavene.

1. Last opp logoen din til den digitale innholdsbehandleren, som du kan få tilgang til fra **Aktiva**-siden.
1. Lag et topptekstfragment. Hvis du vil ha mer informasjon om hvordan du oppretter og bruker fragmenter, se [Arbeide med fragmenter](work-with-fragments.md).
1. Inkluder topptekstfragmentet i malen som sidene på området bruker for alternativene for oppsett og modul. Hvis du vil ha mer informasjon om maler, kan du se [Arbeide med maler](work-with-templates.md).

## <a name="add-a-logo-to-a-header-fragment"></a>Legge til en logo i et topptekstfragment

Følg denne fremgangsmåten for å legge til en logo i topptekstfragmentet for området.

1. Velg **Fragmenter** i navigasjonsruten til venstre, og velg deretter topptekstfragmentet du har opprettet.
2. Velg **Sjekk ut**.
3. Utvid **Topptekst**-sporet og **Logo**-sporet.
4. Velg ellipseknappen (**...**) for **Logo**-sporet, og velg deretter **Legg til modul**.
5. Velg logomodulen.
6. I egenskapsruten til høyre konfigurerer du logomodulen slik at den viser logoen din.
7. Lagre topptekstfragmentet, sjekk det inn, og publiser det.

Når du har publisert det oppdaterte topptekstfragmentet, vil alle områdesidene som bruker malen som inneholder topptekstfragmentet, vise logoen.

## <a name="additional-resources"></a>Tilleggsressurser

[Velge et områdetema](select-site-theme.md)

[Arbeide med CSS-overstyringsfiler](css-override-files.md)

[Legge til et favorittikon](add-favicon.md)

[Legge til en velkomstmelding](add-welcome-message.md)

[Legge til en opphavsrettserklæring](add-copyright-notice.md)

[Legge til språk på området](add-languages-to-site.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)

