---
title: Opprette forbruksrapporter
description: Dette emnet forklarer hvordan du oppretter forbruksrapporter i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: eecfb101af9a91f515aab221181c54d53e358a68
ms.sourcegitcommit: fb66731f05207094149a6bc7b8549a4dabbb071a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/22/2019
ms.locfileid: "2652431"
---
# <a name="create-consumption-reports"></a>Opprette forbruksrapporter

[!include [banner](../../includes/banner.md)]

 

Når du har opprettet og postert forbruksregistreringer på arbeidsordrer i Aktivastyring, er to rapporter tilgjengelige for visning av forbruksdetaljer.


## <a name="asset-consumption-report"></a>Forbruksrapport for aktivum

Når du har bokført forbruk på arbeidsordrer, kan du skrive ut en forbruksrapport for aktivum. Rapporten viser timer, timekostnader, varekostnader og utgifter som er bokført for aktiva.

1. Klikk **Aktivastyring** > **Rapporter** > **Aktiva** > **Aktivumforbruk**.

2. I dialogboksen **Aktivumforbruk** velger du parameterne og detaljnivået du vil se, ved å velge **Ja** på de aktuelle veksleknappene og sette inn et arbeidsstedsnivå i **Vis**-delen.
    - Du kan bruke **Nivåer**-feltet til å angi hvor detaljert anleggsmiddellinjene skal være når det gjelder arbeidssteder. 
    
        Hvis du for eksempel setter inn tallet 1 i feltet, og du har en arbeidsstedsstruktur med flere nivåer, vises alle aktiva for et arbeidssted på øverste nivå, og derfor kan det hende at en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. 
        
        Hvis du setter inn tallet 0 i **Nivåer**-feltet, vil du se et detaljert resultat som viser alle aktiva på alle arbeidsstedsnivåene de er relatert til. 
        
    - Velg **Ja** på veksleknappen **Sum på alle underordnede aktiva** for å vise summer for hvert underaktivum i rapporten.

3. Velg et datointervall i **Datoer**-delen.

4. I hurtigfanen **Mål** velger du om du vil vise rapporten på skjermen, skrive den ut eller lagre den som en fil eller e-post.

5. Hvis det er nødvendig, kan du velge å vise bestemte anleggsmidler i rapporten. I hurtigfanen **Poster som skal inkluderes** klikker du **Filtrer** og legger til anleggsmidlene du vil ha med i rapporten.

6. Klikk på **OK** for å generere rapporten.


## <a name="work-order-consumption-report"></a>Forbruksrapport for arbeidsordre

Når du har bokført forbruk på arbeidsordrer, kan du skrive ut en forbruksrapport for arbeidsordre. Rapporten viser timer, timekostnader, varekostnader og utgifter som er bokført for arbeidsordrer.

1. Klikk på **Aktivastyring** > **Rapporter** > **Arbeidsordrer** > **Arbeidsordreforbruk**.

2. I dialogboksen **Arbeidsordreforbruk** velger du parameterne du vil ta med i rapporten, ved å velge **Ja** på de aktuelle veksleknappene i **Vis**-delen.

3. Velg et datointervall i **Datoer**-delen.

4. I hurtigfanen **Mål** velger du om du vil vise rapporten på skjermen, skrive den ut eller lagre den som en fil eller e-post.

5. Hvis det er nødvendig, kan du velge å vise bestemte arbeidsordrer i rapporten. I hurtigfanen **Poster som skal inkluderes** klikker du **Filtrer** og legger til arbeidsordrene du vil ha med i rapporten.

6. Klikk på **OK** for å generere rapporten.


>[!NOTE]
>Du kan også generere en [arbeidsordrerapport](../work-orders/work-order-report.md), som inneholder flere arbeidsordredetaljer.

