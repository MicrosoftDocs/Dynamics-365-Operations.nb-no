---
title: Du kan ikke bekrefte en forsendelse på grunn av ufullstendig eller manglende arbeid
description: Du kan ikke bekrefte en forsendelse på grunn av ufullstendig eller manglende arbeid
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm, WHSContainerCloseDiag_WHSShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 59def4427f9fff32fd3839bb9f9b5d5cccdc7720f92a84f1af3adad596d8b352
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730064"
---
# <a name="you-cant-confirm-a-shipment-because-of-incomplete-or-missing-work"></a>Du kan ikke bekrefte en forsendelse på grunn av ufullstendig eller manglende arbeid

Feilkode: WAX515

## <a name="symptoms"></a>Symptomer

Når du prøver å bekrefte en forsendelse, viser systemet følgende feilmelding:

> Forsendelsen av lasten %1 kan ikke bekreftes fordi alt arbeid for lasten må være fullført.

Derfor kan du ikke bekrefte forsendelsen for belastningen.

## <a name="cause"></a>Årsak

Lasten eller forsendelsen er for øyeblikket i en tilstand der forsendelsesbekreftelsen mislykkes. Før du kan bekrefte forsendelsen, må det minst finnes noe arbeid for lasten, og alt arbeidet må ha statusen *Lukket* eller *Avbrutt*.

## <a name="resolution"></a>Oppløsning

Kontroller de tilknyttede salgsordrene eller overføringsordrene for lasten eller forsendelsen, og kontroller at alt tilknyttet arbeid er fullført eller avbrutt.

Du kan arbeide med forsendelser og laster på flere sider. De følgende underdelene gir noen eksempler.

### <a name="all-loads-page"></a>Alle laster-siden

1. Gå til **Lagerstyring \> Laster \> Alle laster**.
1. Velg belastningen som forsendelsen ikke kan bekreftes for.
1. I handlingsruten, i fanen **Laster** i gruppen **Relatert informasjon**, velger du **Arbeid**.
1. Kontroller statusen til hver arbeids-ID. En oppfølging av hver arbeids-ID som ikke har statusen *Lukket* eller *Avbrutt*.
1. Når hver arbeids-ID har statusen *Lukket* eller *Avbrutt*, forsøker du på nytt å bekrefte forsendelsen.

### <a name="all-shipments-page"></a>Alle forsendelser-siden

1. Gå til **Lagerstyring \> Forsendelser \> Alle forsendelser**.
1. Velg forsendelsen som ikke kan bekreftes.
1. Velg **Arbeidsdetaljer** i gruppen **Arbeid** i fanen **Forsendelser** i handlingsruten.
1. Kontroller statusen til hver arbeids-ID. En oppfølging av hver arbeids-ID som ikke har statusen *Lukket* eller *Avbrutt*.
1. Når hver arbeids-ID har statusen *Lukket* eller *Avbrutt*, forsøker du på nytt å bekrefte forsendelsen.

### <a name="all-work-page"></a>Alt arbeid-siden

1. Gå til **Lagerstyring \> Arbeid \> Alt arbeid**.
1. Velg arbeidet for ordrenummeret som forsendelsen ikke kan bekreftes for.
1. Velg **Bekreft forsendelse** i gruppen **Forsendelse** i fanen **Forsendelse** i handlingsruten.
1. Kontroller statusen til hver arbeids-ID. En oppfølging av hver arbeids-ID som ikke har statusen *Lukket* eller *Avbrutt*.
1. Når hver arbeids-ID har statusen *Lukket* eller *Avbrutt*, forsøker du på nytt å bekrefte forsendelsen.
