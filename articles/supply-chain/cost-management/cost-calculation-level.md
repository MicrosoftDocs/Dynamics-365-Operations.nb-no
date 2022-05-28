---
title: Kostnadsberegningsnivå
description: Dette emnet beskriver stykklistenivået som kalles Kostnadsberegningsnivå. Dette stykklistenivået utelukker produksjons- og partiordrer fra beregningene.
author: JennySong-SH
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: 10.0.12
ms.openlocfilehash: 563d866c93e9205914f633f3435ef4b46f85b814
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8679562"
---
# <a name="cost-calculation-level"></a>Kostnadsberegningsnivå

[!include [banner](../includes/banner.md)]

Stykklistenivået som heter **Kostnadsberegningsnivå**, ekskluderer produksjonsordre og partiordre fra beregningene. Systemet bruker dette nivået når det kjører kostnadsberegninger i etterkalkuleringsversjoner. I prosesser som omberegning og lagerlukking bruker systemet BOM-nivået **Stykklistenivå** i stedet.

Følgende enkle scenario viser forskjellene mellom stykklistenivåene for **Kostnadsberegningsnivå** og **Etterkalkuleringsnivå**.

Du har tre produkter: A, B og C. Produkt C er komponenten til produkt B, og produkt B er komponenten til produkt A.

- **Etterkalkuleringsnivå** tilordner følgende stykklistenivåer:

    - **Produkt A:** 0
    - **Produkt B:** 1
    - **Produkt C:** 2

- **Kostnadsberegningsnivå** tilordner følgende stykklistenivåer:

    - **Produkt A:** 0
    - **Produkt B:** 1
    - **Produkt C:** 2

En produksjonsordre for produkt C opprettes deretter, og produkt A legges til i stykklisten for produksjonsordren. Når ordren er estimert, oppdateres stykklistenivåer på følgende måte:

- **Etterkalkuleringsnivå** tilordner følgende stykklistenivåer:

    - **Produkt B:** 1
    - **Produkt C:** 2
    - **Produkt A:** 3

- **Kostnadsberegningsnivå** tilordner følgende stykklistenivåer:

    - **Produkt A:** 0
    - **Produkt B:** 1
    - **Produkt C:** 2

Denne virkemåten sikrer at endringer i stykklister for produksjonsordre ikke har innvirkning på etterfølgende kostnadsberegninger.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]