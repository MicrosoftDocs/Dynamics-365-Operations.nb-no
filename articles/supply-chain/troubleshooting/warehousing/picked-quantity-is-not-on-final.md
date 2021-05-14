---
title: Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket
description: Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938525"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a>Du kan ikke bekrefte en forsendelse fordi varer ikke har blitt plukket

Feilkode: LoadNotPickedAndMovedToFinalShippingLocation

## <a name="symptoms"></a>Symptomer

Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:

> Noen av varene som trengs for lasten %1, har ennå ikke blitt plukket og flyttet til den endelige forsendelseslokasjonen.

Derfor kan du ikke bekrefte forsendelsen for belastningen.

## <a name="cause"></a>Årsak

Belastningen eller forsendelsen kan ikke bekreftes i gjeldende tilstand, fordi det kan hende at én av følgende betingelser finnes:

- Det relaterte arbeidet er ennå ikke plukket og flyttet til den endelige forsendelseslokasjonen.
- Det plukkede arbeidsantallet samsvarer ikke med det opprettede arbeidsantallet på belastningslinjen.

## <a name="resolution"></a>Oppløsning

Kontroller de tilknyttede salgsordrene eller overføringsordrene for belastningen eller forsendelsen. Kontroller at alt tilknyttet arbeid er fullført på den endelige forsendelseslokasjonen, og at antallet samsvarer.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg belastningen som forsendelsen ikke kan bekreftes for.
1. I hurtigfanen **Lastlinjer** velger du lastlinjen.
1. Legg merke til verdien i feltet **Antall for arbeid opprettet**.
1. I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.
1. Kontroller at arbeidet er fullført på det endelige forsendelsesstedet, og at det plukkede arbeidsantallet samsvarer med det opprettede arbeidsantallet på belastningslinjen.
1. Gjenta denne fremgangsmåten for alle belastningslinjer for å være sikker på at alle kriteriene er oppfylt.
