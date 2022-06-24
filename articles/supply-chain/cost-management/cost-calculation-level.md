---
title: Kostnadsberegningsnivå
description: Denne artikkelen beskriver stykklistenivået som kalles Kostnadsberegningsnivå. Dette stykklistenivået utelukker produksjons- og partiordrer fra beregningene.
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
ms.openlocfilehash: 647ef4b13b864cfdbb7905fe7a0d340e85f6c1e6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850880"
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