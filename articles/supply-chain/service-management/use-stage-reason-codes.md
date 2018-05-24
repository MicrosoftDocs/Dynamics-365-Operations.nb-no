---
title: "Bruke stadieårsakskoder"
description: "Du kan bruke en årsakskode til å angi hvorfor en servicenivåavtale (SLA) har blitt annullert, eller hvorfor en serviceordre har overskredet tidsbegrensningen som er definert i servicenivåavtalen."
author: YuyuScheller
manager: AnnBe
ms.date: 05/07/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAServiceOrderTable, SMAParameters
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: YuyuScheller
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: e42172fe1b484b91e9a3e3d05d438e7e9b0b0eb4
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---


# <a name="use-stage-reason-codes"></a>Bruke stadieårsakskoder 

[!include [banner](../includes/banner.md)]


Du kan bruke en årsakskode til å angi hvorfor en servicenivåavtale (SLA) har blitt annullert, eller hvorfor en serviceordre har overskredet tidsbegrensningen som er definert i servicenivåavtalen.

Eu kan også angi at en årsakskode kreves når en når en servicenivåavtale annulleres eller når tidsbegrensningen overskrider tiden som er angitt i serviceavtalen vor serviceordren.

Hvis tidsbegrensningen er overskredet på en serviceavtale, må du angi en årsakskode i følgende situasjoner:

  - Når en serviceordre flyttes til et stadium som stopper tidsregistreringen mot servicenivåavtalen for serviceordren.

  - Når serviceordren godkjennes.

  - Når tidsregistrering stoppes manuelt.

## <a name="set-up-reason-codes"></a>Definer årsakskoder

1.  Klikk **Servicestyring** \> **Oppsett** \> **Serviceordrer** \> **Stadieårsakskoder**.

2.  I skjemaet **Stadieårsakskoder** klikker du **Ny** for å opprette en ny årsakskode.

3.  I feltet **Stadieårsakskode** angir du en unik årsakskode for stadium.

4.  I **Beskrivelse**-feltet angir du en beskrivelse av stadieårsakskoden.

5.  Lukk skjemaet for å lagre endringene.

## <a name="require-reason-codes-when-a-service-level-agreement-is-canceled"></a>Kreve årsakskoder når en servicenivåavtale annulleres

1.  Klikk **Servicestyring** \> **Oppsett** \> **Servicestyringsparametere**.

2.  I skjemaet **Servicestyringsparametere** klikker du **Generelt**-koblingen og velger deretter **Årsakskode for avbrudd**.

## <a name="require-reason-codes-when-the-a-service-order-exceeds-the-time-limit-that-is-set-by-the-service-level-agreement"></a>Kreve årsakskoder når en serviceordre overskrider tidsbegrensningen som er definert i servicenivåavtalen.

1.  Klikk **Servicestyring** \> **Oppsett** \> **Servicestyringsparametere**.

2.  I skjemaet **Servicestyringsparametere** klikker du **Generelt**-koblingen og velger deretter **Årsakskode for tidsoverskridelse**.

## <a name="see-also"></a>Se også

[Starte og stoppe tidsregistrering på en serviceordre](start-and-stop-time-recording-on-a-service-order.md)

  



