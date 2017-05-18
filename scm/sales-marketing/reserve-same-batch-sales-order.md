---
title: Reservere samme parti for en salgsordre
description: "Denne artikkelen beskriver hvordan du konfigurerer et produkt til å godta reservasjon for lager mot en enkelt satsvis jobb for lager."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 2f82d8bf65dcb421420eabbfe9f4c4ef0332b1cc
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="reserve-the-same-batch-for-a-sales-order"></a>Reservere samme parti for en salgsordre

[!include[banner](../includes/banner.md)]


Denne artikkelen beskriver hvordan du konfigurerer et produkt til å godta reservasjon for lager mot en enkelt satsvis jobb for lager.

Samme partireservasjon gjør at du kan reservere beholdning for en salgsordrelinje mot ett lagerparti. En kunde som bestiller tapet, kan for eksempel be om at hele ordren fylles fra samme parti for å unngå manglende overensstemmelse mellom rullene. Hvis du vil definere et produkt slik at det bruker samme partireservasjon, må følgende innstillinger være aktive i varemodellgruppen, sporingsdimensjonsgruppen, og lagringsdimensjonsgruppen du tilordner til produktet:

-   **Varemodellgrupper** – Varemodellgruppen må ha feltene **Samme partivalg** og **Konsolider krav** valgt i feltgruppen **Reservering** for beholdningspolicyer.
-   **Sporingsdimensjonsgrupper** – Sporingsdimensjonsgruppen må ha feltet **Dekningsplanlegg etter dimensjon** valgt for partinummeret.
-   **Lagringsdimensjonsgrupper** – Lagringsdimensjonsgruppen må ha feltet **Dekningsplanlegg etter dimensjon** valgt for **Område** og **Lager**.

Når du reserverer beholdning for et produkt på en salgsordrelinje som er definert for samme partivalg, prøver Microsoft Dynamics 365 for Operations å reservere det bestilte antallet fra ett lagerparti. Det tas også hensyn til eventuelle bestemte partiattributtbehov. Hvis antallet ikke kan fylles fra ett parti, vise siden **Samme partireservasjonskonflikt**. Denne siden beskriver problemene samt det du kan gjøre for å fortsette med reserveringen. Følgende forhold kan forhindre at partiet blir reservert:

-   Partidisposisjonskoden har **Blokker reservering** for salg flagget som **Blokkert**.
-   Partiet er utløpt, basert på utløpsdatoen og eventuelle gjeldende salgbare dager for kunde. Varen kan fortsett vurderes for reservasjon hvis varemodellgruppen for varen er FEFO-datokontrollert, og hvis best-før-datoen er valgt som plukkekriteriet.
-   Partiet har ikke nok holdbarhetsdager igjen, basert på utløpsdatoen og best-før-datoen, i tillegg til eventuelle salgbare dager for kunde.





