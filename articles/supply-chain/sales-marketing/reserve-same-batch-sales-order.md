---
title: Reservere samme parti for en salgsordre
description: "Denne artikkelen beskriver hvordan du konfigurerer et produkt til å godta reservasjon for lager mot en enkelt satsvis jobb for lager."
author: omulvad
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: omulvad
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: aef3a52f4cb2d5af47a8c25a67e6c2076fa1ff03
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>Reservere samme parti for en salgsordre

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer et produkt til å godta reservasjon for lager mot en enkelt satsvis jobb for lager.

Samme partireservasjon gjør at du kan reservere beholdning for en salgsordrelinje mot ett lagerparti. En kunde som bestiller tapet, kan for eksempel be om at hele ordren fylles fra samme parti for å unngå manglende overensstemmelse mellom rullene. Hvis du vil definere et produkt slik at det bruker samme partireservasjon, må følgende innstillinger være aktive i varemodellgruppen, sporingsdimensjonsgruppen, og lagringsdimensjonsgruppen du tilordner til produktet:

-   **Varemodellgrupper** – Varemodellgruppen må ha feltene **Samme partivalg** og **Konsolider krav** valgt i feltgruppen **Reservering** for beholdningspolicyer.
-   **Sporingsdimensjonsgrupper** – Sporingsdimensjonsgruppen må ha feltet **Dekningsplanlegg etter dimensjon** valgt for partinummeret.
-   **Lagringsdimensjonsgrupper** – Lagringsdimensjonsgruppen må ha feltet **Dekningsplanlegg etter dimensjon** valgt for **Område** og **Lager**.

Når du reserverer beholdning for et produkt på en salgsordrelinje som er definert for samme partivalg, prøver Microsoft Dynamics 365 for Finance and Operations å reservere det bestilte antallet fra ett lagerparti. Det tas også hensyn til eventuelle bestemte partiattributtbehov. Hvis antallet ikke kan fylles fra ett parti, vise siden **Samme partireservasjonskonflikt**. Denne siden beskriver problemene samt det du kan gjøre for å fortsette med reserveringen. Følgende forhold kan forhindre at partiet blir reservert:

-   Partidisposisjonskoden har **Blokker reservering** for salg flagget som **Blokkert**.
-   Partiet er utløpt, basert på utløpsdatoen og eventuelle gjeldende salgbare dager for kunde. Varen kan fortsett vurderes for reservasjon hvis varemodellgruppen for varen er FEFO-datokontrollert, og hvis best-før-datoen er valgt som plukkekriteriet.
-   Partiet har ikke nok holdbarhetsdager igjen, basert på utløpsdatoen og best-før-datoen, i tillegg til eventuelle salgbare dager for kunde.





