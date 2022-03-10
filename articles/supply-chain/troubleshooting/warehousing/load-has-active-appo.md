---
title: Du kan ikke bekrefte en forsendelse på grunn av et problem med kalenderen
description: Du kan ikke bekrefte en forsendelse på grunn av et problem med kalenderen
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
ms.openlocfilehash: 8aae45beeef1934760d620874897f46a1cf901995e2b83e148a1d56898d9c717
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6735950"
---
# <a name="you-cant-confirm-a-shipment-because-of-an-issue-with-the-calendar"></a>Du kan ikke bekrefte en forsendelse på grunn av et problem med kalenderen

Feilkode: TRX2716

## <a name="symptoms"></a>Symptomer

Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:

> Kalendertype %1 krever at avtale %2 sjekkes inn og ut.

Derfor kan du ikke bekrefte forsendelsen for belastningen.

## <a name="cause"></a>Årsak

Det finnes aktive avtaler for lasten. Det finnes for eksempel en regel som krever sjåførinnsjekking. Derfor er lasten for øyeblikket i en tilstand der forsendelsesbekreftelsen mislykkes.

## <a name="resolution"></a>Oppløsning

Du må undersøke og rette eventuelle problemer med de aktive avtalene som er koblet til lasten.

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg belastningen som forsendelsen ikke kan bekreftes for.
1. På handlingsruten i fanen **Transport** i **Avtaler**-gruppen velger du **Avtaleplanlegging**.
1. Følg ett av disse trinnene:

    - Kontroller at sjåførinnsjekking/-utsjekkingen er fullført for avtalen.
    - Fullfør eller avbryt avtalen.
    - Deaktiver alternativet **Krever sjåførinnsjekking** for den relaterte avtaleregelen.
