---
title: Du kan ikke bekrefte en forsendelse fordi antallet overskrider underleveringsprosenten
description: Du kan ikke bekrefte en forsendelse fordi antallet overskrider underleveringsprosenten
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5339b9d800f7454e2a00c230a8d5deca3979c074
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938523"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-underdelivery-percentage"></a>Du kan ikke bekrefte en forsendelse fordi antallet overskrider underleveringsprosenten

Feilkode: WAX1687

## <a name="symptoms"></a>Symptomer

Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:

> Forsendelsen for last %1 kan ikke bekreftes, fordi antallet for varen %2 overskrider prosenten som er definert for underlevering.

Derfor kan du ikke bekrefte forsendelsen for belastningen.

## <a name="cause"></a>Årsak

Antallet for lasten eller forsendelsen er bare delvis plukket. Antallet er under det plukkede antallet med en prosent som er utenfor den tillatte underleveringsprosenten.

## <a name="resolution"></a>Oppløsning

Du kan løse dette problemet ved å fullføre én eller flere av følgende oppgaver:

- Angi lastlinjeantallet.
- Angi underleveringsprosenten.

### <a name="set-the-load-line-quantity"></a>Angi lastlinjeantallet

Følg denne fremgangsmåten for å angi lastlinjeantallet.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg belastningen som forsendelsen ikke kan bekreftes for.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som overskrider underleveringsprosenten.
1. I hurtigfanen **Linjedetaljer** velger du **Ordre**.
1. I **Antall**-feltet angir du verdien til det plukkede antallet (det vil si til verdien **Antall for arbeid opprettet**), slik at forsendelsesbekreftelse kan skje.

### <a name="set-the-underdelivery-percentage"></a>Angi underleveringsprosenten

Følg denne fremgangsmåten for å angi underleveringsprosenten.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg belastningen som forsendelsen ikke kan bekreftes for.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen for varen som overskrider underleveringsprosenten.
1. I hurtigfanen **Linjedetaljer** velger du **Generelt**.
1. I **Underlevering**-feltet angir du verdien til en større prosent som legger til rette for antallet som er plukket mot lastantallet, slik at forsendelsesbekreftelsen kan skje.
