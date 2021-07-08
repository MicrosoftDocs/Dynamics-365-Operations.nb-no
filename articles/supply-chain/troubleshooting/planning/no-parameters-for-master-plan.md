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
ms.openlocfilehash: d4b64af2e30109b8560d40c4c532504611528bbe
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294148"
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
