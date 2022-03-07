---
title: Planlagt produksjonsordre må planlegges før det kan autoriseres
description: Når du prøver å autorisere en planlagt bestilling, får du en feilmelding som angir at ordren må planlegges før den kan autoriseres.
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
ms.openlocfilehash: a360cb3cbd26e1bc1ebb1baf1a6a4d8282c28c5c
ms.sourcegitcommit: 18ca2df785e9656fdd4e8c0734eca2b2624fda10
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/22/2021
ms.locfileid: "6294150"
---
# <a name="planned-production-order-must-be-scheduled-before-it-can-be-firmed"></a>Planlagt produksjonsordre må planlegges før det kan autoriseres

Feilkode: SYS309802

## <a name="symptoms"></a>Symptomer

Når du prøver å autorisere en planlagt ordre, mottar du følgende feilmelding:

> Den planlagte produksjonsordren må planlegges før den kan autoriseres.

## <a name="cause"></a>Årsak

De planlagte start- og sluttdatoene kan ikke være tomme.

## <a name="resolution"></a>Løsning

Følg denne fremgangsmåten for å angi start- og sluttdato for den planlagte bestillingen.

1. Gå til **Hovedplanlegging \> Hovedplanlegging \> Planlagte ordrer**.
1. Åpne den planlagte ordren.
1. Angi datoer i feltene **Startdato** og **Sluttdato** i hurtigfanen **Generelt** i delen **Planlagt**.
