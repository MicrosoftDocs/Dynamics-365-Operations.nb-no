---
title: Parametere for hovedplanen finnes ikke
description: Når du prøver å autorisere en planlagt bestilling, får du en feilmelding som angir at det ikke finnes parametere for hovedplanen.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d039b79684f87e7791fb9dae7cbdc6ced220bc092d9a0ab624616c1c345986da
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6756781"
---
# <a name="parameters-for-the-master-plan-dont-exist"></a>Parametere for hovedplanen finnes ikke

Feilkode: SYS25368

## <a name="symptoms"></a>Symptomer

Når du prøver å autorisere en planlagt ordre, mottar du følgende feilmelding:

> Parametere for hovedplanen %1 finnes ikke.

## <a name="cause"></a>Årsak

På grunn av konfigurasjonsproblemer finner ikke systemet innstillingene for den angitte planen.

## <a name="resolution"></a>Løsning

- Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**, og kontroller at det finnes en plan som har det angitte navnet.
