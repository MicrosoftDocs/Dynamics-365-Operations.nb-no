---
title: Du kan ikke bekrefte en forsendelse fordi kunden er på vent
description: Du kan ikke bekrefte en forsendelse fordi kunden er på vent.
author: GalynaFedorova
ms.date: 07/30/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-07-30
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 82b28e7cfd8c88e453cdd09398f5a92f605eab15a17d33defa0b9729a53c05b6
ms.sourcegitcommit: fa5ff2a0822aac16b518a2aea0d3389f79793390
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/07/2021
ms.locfileid: "7012197"
---
# <a name="you-cant-confirm-a-shipment-because-the-customer-is-on-hold"></a>Du kan ikke bekrefte en forsendelse fordi kunden er på vent

Feilkode: WAX:CustomerOnHoldShipmentCannotBeConfirmed

## <a name="symptoms"></a>Symptomer

Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:

> Forsendelsen %1 kan ikke bekreftes fordi kunden er sperret for %2.

Derfor kan du ikke bekrefte forsendelsen for belastningen.

## <a name="cause"></a>Årsak

Kundekontoen for belastningen eller forsendelsen er på vent. Derfor forhindrer kundens status forsendelsesbekreftelse.

## <a name="resolution"></a>Løsning

Bruk fremgangsmåten nedenfor for å fjerne blokkeringen for kundekontoen.

1. Gå til **Kunder \> Kunder \> Alle kunder**.
1. Åpne kundekontoen som forsendelsen ikke kan bekreftes for.
1. Sett feltet **Fakturerings- og levering på vent** i hurtigfanen **Kredit og purringer** til *Nei*.
1. Gjenta denne fremgangsmåten for alle blokkerte kunder for belastningen.
