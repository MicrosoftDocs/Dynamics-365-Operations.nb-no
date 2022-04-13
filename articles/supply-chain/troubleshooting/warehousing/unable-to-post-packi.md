---
title: Kan ikke postere følgeseddel for en stanset salgsordrelinje
description: Du kan ikke postere en følgeseddel for en stanset salgsordrelinje
author: smithanataraj
ms.date: 03/07/2022
ms.topic: article
ms.search.form: WHSLoadTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mfp
ms.search.validFrom: 2022-03-07
ms.dyn365.ops.version: 10.0.26
ms.openlocfilehash: 115cfe79e075eb36f73203818acdbb5e31fc0bad
ms.sourcegitcommit: c0f7ee7f8837fec881e97b2a3f12e7f63cf96882
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/22/2022
ms.locfileid: "8462855"
---
# <a name="cant-post-packing-slip-for-a-stopped-a-sales-order-line"></a>Kan ikke postere følgeseddel for en stanset salgsordrelinje

Feilkode: SYS13203

## <a name="symptoms"></a>Symptomer

Når du prøver å postere en følgeseddel for en last, viser systemet følgende feilmelding:

> Kan ikke postere følgeseddel når en salgsordrelinje stanses etter å ha bekreftet at antallet for utgående forsendelse A ikke kan plukkes.

## <a name="cause"></a>Årsak

Én eller flere av de relaterte salgsordrelinjene kan være stanset, noe som betyr at systemet vil hindre ytterligere behandling av salgsordren. Det betyr blant annet at systemet ikke vil postere en følgeseddel for ordren.

En bruker kan for eksempel ha bestemt seg for å stoppe én eller flere ordrelinjer fordi kunden kalte tilbake og annullerte ordren. Hvis den utgående forsendelsen allerede er bekreftet, vil imidlertid forsendelsen som inneholder salgsordren, allerede fysisk ha forlatt lageret, noe som betyr at det ikke vil ha noen virkning å stanse salgsordrelinjene. Siden det ikke lenger er mulig å stanse forsendelsen fysisk, kan du like godt oppheve stansen av linjer, slik at du kan postere følgeseddelen. Du må da behandle den annullerte ordren som en retur.

## <a name="resolution"></a>Oppløsning

Hvis du vil postere følgeseddelen, må du kontrollere at ingen av de relevante salgsordrelinjene er stoppet ved å gjøre følgende:

1. Gå til **Alle salgsordrer \> Salg og markedsføring \> Alle salgsordrer**.
1. Finn og åpne salgsordren du har problemer med.
1. På hurtigfanen **Salgsordrelinjer** velger du en salgsordrelinje.
1. På hurtigfanen **Linjedetaljer** åpner du **Generelt**-fanen og kontrollerer at **Stanset**-feltet er angitt til *Nei*.
1. Fortsett med arbeidet til alle de relevante salgslinjene ikke lenger er stanset.
1. Prøv deretter å postere følgeseddelen for lasten eller salgsordren på nytt.
