---
title: Kan ikke avbryte en følgeseddel etter at den er postert fra en ordre
description: Når plukk- og leveringsprosesser er aktivert for WMS, kan du ikke avbryte en følgeseddel etter at den er postert fra en salgsordre. Denne siden gir deg muligheten til å omgå dette.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: d20e66e2721560b8409eb63c3546a79adc188c7c
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/07/2021
ms.locfileid: "7477253"
---
# <a name="cant-cancel-a-packing-slip-after-its-posted-from-a-sales-order"></a>Kan ikke avbryte en følgeseddel etter at den er postert fra en salgsordre

## <a name="symptoms"></a>Symptomer

Når plukk- og leveringsprosesser er aktivert for avansert lagerstyring (WMS), kan du ikke avbryte en følgeseddel etter at den er postert fra en salgsordre.

## <a name="resolution"></a>Løsning

Hvis du vil korrigere posterte følgesedler for varer som er aktivert for WMS, må du utføre posteringen fra lasten, ikke direkte fra ordren. Microsoft har evaluert dette problemet og har funnet ut at det er en funksjonsbegrensning.  

Vanligvis kan en salgsordre som er plukket og sendt gjennom lagerstyringsprosesser, følgeseddeloppdateres fra lasten eller forsendelsen og selve salgsordredokumentet. Hvis du imidlertid følgeseddeloppdaterer salgsordren fra salgsordredokumentet, kan fremdeles ikke følgeseddeltilbakeføring utføres fra lasten eller salgsordren. Derfor anbefaler vi at du bruker følgeseddelposteringen fra lasten. I dette tilfellet blir tilbakeføringen som må gjøres fra lasten, aktivert.
