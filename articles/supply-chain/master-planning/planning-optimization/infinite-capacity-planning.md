---
title: Planlegging med ubegrenset kapasitet
description: Denne artikkelen gir informasjon om ubegrenset kapasitetsplanlegging for planleggingsoptimalisering. Den beskriver også gjeldende funksjonsbegrensninger.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: c6e0190899abb544b559bb5f26ba974155989c3a
ms.sourcegitcommit: 203c8bc263f4ab238cc7534d4dd902fd996d2b0f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2022
ms.locfileid: "9335323"
---
# <a name="scheduling-with-infinite-capacity"></a>Planlegging med ubegrenset kapasitet

[!include [banner](../../includes/banner.md)]

Funksjonen *Ubegrenset kapasitetsplanlegging for planleggingsoptimalisering* introduserer planlegging som er basert på ruteinformasjon. Det lar deg planlegge jobber basert på en rekke ruteoppsett. Planlegging for planleggingsoptimalisering dekker ofte brukte ruteinnstillinger, inkludert ruteoperasjonsrekkefølgen eller kravene for ruteoperasjonsressurser.

## <a name="turn-the-infinite-capacity-scheduling-feature-on-or-off"></a>Aktiver eller deaktiver funksjonen for ubegrenset kapasitetsplanlegging

For å bruke denne funksjonen må den være aktivert for systemet. Fra og med Supply Chain Management versjon 10.0.29 er funksjonen aktivert som standard. Administratorer kan aktivere eller deaktivere denne funksjonaliteten ved å søke etter funksjonen *Uendelig kapasitetsplanlegging for Planleggingsoptimalisering* i arbeidsområdet [Funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Hvis du vil ha mer informasjon om denne funksjonen, kan du se [ Planlegging med ressursvalg basert på funksjoner](capability-based-scheduling.md).

## <a name="added-functionality"></a>Tillagt funksjonalitet

Funksjonen *Ubegrenset kapasitetsplanlegging for planleggingsoptimalisering* aktiverer jobbplanlegging som er basert på ruteinformasjon. Derfor kan et ruteoppsett brukes til å planlegge produksjonsprosesser. Selv om denne funksjonen har noen begrensninger som den innebygde hovedplanleggingen ikke har, støtter den den vanligste funksjonaliteten som kreves for produksjonsscenarier.

Funksjonen vurderer både *enkle ruter* og *rutenettverk*. Ved å bruke **Neste**-feltet i en ruteoperasjon kan du definere komplekse ruter som har flere startpunkt og flere operasjoner som kjøres parallelt. Systemet vil vurdere komplekse rutestrukturer av denne typen under planlegging.

I tillegg støtter funksjonen *parallelle operasjoner* i ruter. Ved å bruke alternativene *primær* og *sekundær* i **Prioritet**-feltet for ruteoperasjoner, kan du definere en rutestruktur der én ruteoperasjon er den primære operasjonen, og en annen operasjon er sekundær. I dette tilfellet vil systemet vil vurdere rutestrukturen under planlegging.

Under planleggingsprosessen vurderer systemet også *ressursbehovene* som er angitt for en operasjon. Systemet bruker ressursbehov for å bestemme hvilke ressurser som kreves for å utføre operasjonen. For øyeblikket støtter funksjonen *Ubegrenset kapasitetsplanlegging for planleggingsoptimalisering* følgende typer ressursbehov:

- Ressurstype
- Ressurs
- Ressursgruppe
- Funksjon (Hvis du vil ha mer informasjon, kan du se [Planlegging med ressursvalg basert på funksjoner](capability-based-scheduling.md).)

> [!NOTE]
>
> - Hvis ressursen og/eller ressursgruppen er satt til ubegrenset kapasitet, vil hovedplanleggingen anse dem som ubegrenset kapasitet.
> - Krav som er knyttet til personale, for eksempel ferdigheter eller sertifikatkrav, støttes ennå ikke.

Funksjonen støtter også driftsegenskaper for **oppsettid** og **kjøretid**. Når du angir disse egenskapene for en ruteoperasjon, oppretter planleggingsprosessen det riktige oppsettet og de riktige prosessjobbene.

Kort oppsummert støtter planleggingsoptimalisering de mest brukte scenariene. Du kan opprette ruten, legge til primære og sekundære operasjoner, definere neste operasjoner, legge til ressursbehov og legge til oppstillingstid og kjøretid. Systemet vil deretter vurdere denne informasjonen under planlegging.

## <a name="limitations"></a>Begrensninger

Følgende begrensninger gjelder når du bruker planlegging for planleggingsoptimalisering:

- Funksjonen støtter bare ubegrenset kapasitet.
- Funksjonen støtter ikke funksjonalitet for ressursbelastning.
- Funksjonen vurderer ikke rutesvinn.
- Funksjonen støtter bare *Varighet* som det primære ressursvalget.

Legg merke til at funksjonen *Ubegrenset kapasitetsplanlegging for planleggingsoptimalisering* er forbedret. Microsoft forventer å introdusere støtte for flere planleggingsinnstillinger i fremtidige versjoner.
