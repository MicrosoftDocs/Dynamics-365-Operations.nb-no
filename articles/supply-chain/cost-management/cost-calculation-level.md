---
title: Kostnadsberegningsnivå
description: Dette emnet beskriver stykklistenivået som kalles Kostnadsberegningsnivå. Dette stykklistenivået utelukker produksjons- og partiordrer fra beregningene.
author: AndersGirke
manager: tfehr
ms.date: 04/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aevengir
ms.search.validFrom: 2020-04-23
ms.dyn365.ops.version: Release 10.0.12
ms.openlocfilehash: 52b77e794ee38add556ac01d62c973b38c48a548
ms.sourcegitcommit: a3cd2783ae120ac6681431c010b9b126a9ca7d94
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/29/2020
ms.locfileid: "3410972"
---
# <a name="cost-calculation-level"></a>Kostnadsberegningsnivå

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
