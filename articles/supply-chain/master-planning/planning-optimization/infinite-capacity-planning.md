---
title: Planlegging med ubegrenset kapasitet
description: Dette emnet gir informasjon om ubegrenset kapasitetsplanlegging for planleggingsoptimalisering. Den beskriver også gjeldende funksjonsbegrensninger.
author: crytt
ms.date: 6/9/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc40dc2bcf1969e4c566b624a9425638e69ab2a17892f035aeabb74068aadd14
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718978"
---
# <a name="scheduling-with-infinite-capacity"></a>Planlegging med ubegrenset kapasitet

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Funksjonen *Ubegrenset kapasitetsplanlegging for planleggingsoptimalisering* introduserer planlegging som er basert på ruteinformasjon. Det lar deg planlegge jobber basert på en rekke ruteoppsett. Planlegging for planleggingsoptimalisering dekker ofte brukte ruteinnstillinger, inkludert ruteoperasjonsrekkefølgen eller kravene for ruteoperasjonsressurser.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Slå på funksjonen for ubegrenset kapasitetsplanlegging

Hvis systemet ikke allerede inneholder funksjonen som er beskrevet i dette emnet, kan du åpne arbeidsområdet [Funksjonsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funksjonen *Ubegrenset kapasitetsplanlegging for planleggingsoptimalisering*.

## <a name="added-functionality"></a>Tillagt funksjonalitet

Funksjonen *Ubegrenset kapasitetsplanlegging for planleggingsoptimalisering* aktiverer jobbplanlegging som er basert på ruteinformasjon. Derfor kan et ruteoppsett brukes til å planlegge produksjonsprosesser. Selv om denne funksjonen har noen begrensninger som den innebygde hovedplanleggingen ikke har, støtter den den vanligste funksjonaliteten som kreves for produksjonsscenarier.

Funksjonen vurderer både *enkle ruter* og *rutenettverk*. Ved å bruke **Neste**-feltet i en ruteoperasjon kan du definere komplekse ruter som har flere startpunkt og flere operasjoner som kjøres parallelt. Systemet vil vurdere komplekse rutestrukturer av denne typen under planlegging.

I tillegg støtter funksjonen *parallelle operasjoner* i ruter. Ved å bruke alternativene *primær* og *sekundær* i **Prioritet**-feltet for ruteoperasjoner, kan du definere en rutestruktur der én ruteoperasjon er den primære operasjonen, og en annen operasjon er sekundær. I dette tilfellet vil systemet vil vurdere rutestrukturen under planlegging.

Under planleggingsprosessen vurderer systemet også *ressursbehovene* som er angitt for en operasjon. Systemet bruker ressursbehov for å bestemme hvilke ressurser som kreves for å utføre operasjonen. For øyeblikket støtter funksjonen *Ubegrenset kapasitetsplanlegging for planleggingsoptimalisering* følgende typer ressursbehov:

- Ressurstype
- Ressurs
- Ressursgruppe
- Funksjon

> [!NOTE]
> Krav som er knyttet til personale, for eksempel ferdigheter eller sertifikatkrav, støttes ennå ikke.

Funksjonen støtter også driftsegenskaper for **oppsettid** og **kjøretid**. Når du angir disse egenskapene for en ruteoperasjon, oppretter planleggingsprosessen det riktige oppsettet og de riktige prosessjobbene.

Kort oppsummert støtter planleggingsoptimalisering de mest brukte scenariene. Du kan opprette ruten, legge til primære og sekundære operasjoner, definere neste operasjoner, legge til ressursbehov og legge til oppstillingstid og kjøretid. Systemet vil deretter vurdere denne informasjonen under planlegging.

## <a name="limitations"></a>Begrensninger

Følgende begrensninger gjelder når du bruker planlegging for planleggingsoptimalisering:

- Funksjonen støtter bare jobbplanlegging. Innstillinger som er knyttet til grovplanlegging, vurderes ikke under planlegging, uavhengig av planleggingsmetoden for hovedplaner.
- Funksjonen støtter bare ubegrenset kapasitet.
- Funksjonen støtter ikke funksjonalitet for ressursbelastning.
- Funksjonen vurderer ikke rutesvinn.
- Funksjonen støtter bare *Varighet* som det primære ressursvalget.

Legg merke til at funksjonen *Ubegrenset kapasitetsplanlegging for planleggingsoptimalisering* er forbedret. Microsoft forventer å introdusere støtte for flere planleggingsinnstillinger i fremtidige versjoner.
