---
title: Definer nummerserier for detaljshandelsutdrag
description: Denne artikkelen beskriver hvordan du konfigurerer nummerseriene som kreves for detaljhandelsutdrag i Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 04/27/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: analpert
ms.search.validFrom: 2022-04-12
ms.openlocfilehash: 917d7b7a905a822ca3b1e074055fe0cd4af5555b
ms.sourcegitcommit: 6616b969afd6beb11a79d8e740560bf00016ea7f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/17/2022
ms.locfileid: "9027192"
---
# <a name="set-up-number-sequences-for-retail-statements"></a>Definer nummerserier for detaljshandelsutdrag

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer nummerseriene som kreves for detaljhandelsutdrag i Microsoft Dynamics 365 Commerce.

To typer detaljhandelsutdrag brukes i Dynamics 365 Commerce: 

- **Transaksjonsutdrag** skal opprettes og posteres med høy frekvens. De brukes til å postere alle ikke-finansmessige transaksjoner i butikken til Dynamics 365 Commerce headquarters. 
- **Regnskapsoppgjør** skal opprettes og posteres én gang per virkedag. De omfatter bare lukkede skift fra detaljhandelsbutikkene som er lastet opp til Commerce Headquarters via p-jobben.

## <a name="configure-a-number-sequence-for-statement-posting"></a>Konfigurer en nummerserie for utdragspostering

Når du har fullført oppsettet for en detaljhandelsbutikk i Commerce Headquarters, må du konfigurere en unik nummerserie som skal brukes til utdrag under utdragsopprettingsprosessen.

Følg denne fremgangsmåten for å konfigurere en nummerserie for utdragspostering i Commerce headquarters.

1. Gå til **Organisasjonsadministrasjon \> Nummerserier \> Nummerserier**.
1. Velg **Ny \> Nummerserie** for å opprette en ny post.
1. På hurtigfanen **Identifikasjon**, i feltet **Nummerseriekode**, angir du en nummerseriekode.
1. Angi et navn i **Nummerserienavn**-feltet.
1. På hurtigfanen **Omfangsparametere**, i feltet **Omfang**, velger du **Driftsenhet**.
1. I feltet **Driftsenhet** velger du butikken som nummerserien skal brukes til.
1. Definer segmentene i hurtigfanen **Segmenter**.
1. Angi **Område**-feltet til **Detaljhandel** i hurtigfanen **Referanser**.
1. Sett **Referanse**-feltet til **Utdragsnummer**, og velg deretter **OK**.

    ![Hurtigfanene Identifikasjon, Områdeparametere, Segmenter og Referanser på siden Nummerserier.](media/retail-statements-num-seq-setup-01.png)

1. Oppdater feltene **Minste** og **Største** i **Nummertildeling**-delen i fanen **Generelt** slik at de samsvarer med lengden på det **alfanumeriske** segmentet du definerte i hurtigfanen **Segmenter**.
1. I hurtigfanen **Ytelse** anbefaler vi at du setter alternativet **Forhåndstildeling** til **Ja** og antall i feltet **Antall numre** til **25**.

    ![Hurtigfanene Generelt og Ytelse på siden Nummerserier.](media/retail-statements-num-seq-setup-02.png)

1. På hurtigfanen velger du **Lagre** for å lagre endringene og lukke siden.
