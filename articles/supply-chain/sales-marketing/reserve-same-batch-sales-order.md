---
title: Reservere samme parti for en salgsordre
description: Denne artikkelen beskriver hvordan du konfigurerer et produkt til å godta reservasjon for lager mot en enkelt satsvis jobb for lager.
author: Henrikan
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: henrikan
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0d4f3ee5d99648155e663c9ad0849b0b9ae3f80e
ms.sourcegitcommit: 3b87f042a7e97f72b5aa73bef186c5426b937fec
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/29/2021
ms.locfileid: "7576622"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a>Reservere samme parti for en salgsordre

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer et produkt til å godta reservasjon for lager mot en enkelt satsvis jobb for lager.

Samme partireservasjon gjør at du kan reservere beholdning for en salgsordrelinje mot ett lagerparti. En kunde som bestiller tapet, kan for eksempel be om at hele ordren fylles fra samme parti for å unngå manglende overensstemmelse mellom rullene. Hvis du vil definere et produkt slik at det bruker samme partireservasjon, må følgende innstillinger være aktive i varemodellgruppen, sporingsdimensjonsgruppen, og lagringsdimensjonsgruppen du tilordner til produktet:

- **Varemodellgrupper** – Varemodellgruppen må ha feltene **Samme partivalg** og **Konsolider krav** valgt i feltgruppen **Reservering** for beholdningspolicyer.
- **Sporingsdimensjonsgrupper** – Sporingsdimensjonsgruppen må ha feltet **Dekningsplanlegg etter dimensjon** valgt for partinummeret.
- **Lagringsdimensjonsgrupper** – Lagringsdimensjonsgruppen må ha feltet **Dekningsplanlegg etter dimensjon** valgt for **Område** og **Lager**.

Når du reserverer beholdning for et produkt på en salgsordrelinje som er definert for samme partivalg, prøver systemet å reservere det bestilte antallet fra ett lagerparti. Det tas også hensyn til eventuelle bestemte partiattributtbehov. Hvis antallet ikke kan fylles fra ett parti, vise siden **Samme partireservasjonskonflikt**. Denne siden beskriver problemene samt det du kan gjøre for å fortsette med reserveringen. Følgende forhold kan forhindre at partiet blir reservert:

- Partidisposisjonskoden har **Blokker reservering** for salg flagget som **Blokkert**.
- Partiet er utløpt, basert på utløpsdatoen og eventuelle gjeldende salgbare dager for kunde. Varen kan fortsett vurderes for reservasjon hvis varemodellgruppen for varen er FEFO-datokontrollert, og hvis best-før-datoen er valgt som plukkekriteriet.
- Partiet har ikke nok holdbarhetsdager igjen, basert på utløpsdatoen og best-før-datoen, i tillegg til eventuelle salgbare dager for kunde.

For varer som er knyttet til en lagringsdimensjonsgruppe som har aktivert **Bruk lagerstyringsprosesser**, kan du reservere bestemte partinumre ved å bruke et reservasjonshierarki der partinummer-lagerdimensjonen er definert ovenfor lokasjonsdimensjonen. Denne typen reservasjonshierarki kalles også for *Parti-over \[lokasjon\]*. Med **Partireservering**-siden for salgs- og overføringsordrelinjer kan du også velge og reservere flere linjer basert på de tilgjengelige partinumrene. Hvis du vil ha mer informasjon om hva du skal gjøre hvis du bruker et reservasjonshierarki som har partinummerdimensjonen under lokasjonen (*Parti-under \[lokasjon\]*), kan du se [Fleksibel dimensjonsreservasjonspolicy for lagernivå](../warehousing/flexible-warehouse-level-dimension-reservation.md).


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
