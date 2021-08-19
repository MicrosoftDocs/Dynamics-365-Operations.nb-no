---
title: Varen kan ikke ha en stykkliste eller formel
description: Når du prøver å autorisere en ordre, får du en feilmelding under varevalidering. Den angir at varen ikke kan ha en stykkliste eller formel.
author: ankubik
ms.date: 06/10/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPO
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ankubik
ms.search.validFrom: 2021-06-10
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1e946adc3a04db60bf15ac7bb44163085e1c19802872964877d3929b1f79bf7d
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6730112"
---
# <a name="item-cant-have-a-bom-or-formula"></a>Varen kan ikke ha en stykkliste eller formel

Feilkode: PRO2614

## <a name="symptoms"></a>Symptomer

Når du prøver å autorisere en ordre, får du følgende feilmelding under varevalidering:

> Varen kan ikke ha en stykkliste eller formel

## <a name="resolution"></a>Løsning

Varer som har en stykkliste eller formel, må være av typen *Planleggingselement*, *Stykkliste* eller *formel*. Hvis du vil endre typen for en vare, følger du denne fremgangsmåten.

1. Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.
1. Åpne det relevante produktet.
1. I hurtigfanen **Utvikle** setter du feltet **Produksjonstype** til *Planleggingselement*, *BOM* eller *formel*.
