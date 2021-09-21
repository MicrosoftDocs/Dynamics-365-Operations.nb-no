---
title: Direkte levering kan ikke behandle for WMS-aktivert lager
description: Hvis lageret har WMS aktivert, støtter det ikke direkte levering. Hvis du vil bruke direkte levering, må du velge en vare og et lager som ikke er WMS.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 090e17091e9fb92c2065679bb9b04637214e2eea
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477252"
---
# <a name="direct-delivery-not-able-to-process-for-wms-enabled-warehouse"></a>Direkte levering kan ikke behandle for WMS-aktivert lager

## <a name="symptoms"></a>Symptomer

Hvis en vare legges til en salgslinje for direkte levering fra et lager som er aktivert for lagerstyring (WMS), får du følgende feilmelding når salgslinjen oppdateres:

> Direkte levering kan ikke behandle for lager 1% fordi lagerstyring er aktivert. Angi et annet lager som ikke er aktivert for lagerstyring.

## <a name="resolution"></a>Løsning

Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning. For øyeblikket støtter ikke WMS direkte levering. Hvis du vil bruke direkte levering, må du derfor velge en vare og et lager som ikke er WMS.
