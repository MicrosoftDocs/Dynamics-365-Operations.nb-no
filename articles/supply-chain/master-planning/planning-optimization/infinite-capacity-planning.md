---
title: Planlegging med ubegrenset kapasitet
description: Dette emnet gir informasjon om ubegrenset kapasitetsplanlegging for planleggingsoptimalisering. Den beskriver også gjeldende funksjonsbegrensninger.
author: t-benebo
ms.date: 09/21/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: b8f08af3b58e5c0f8480ae540478d60bb8d36193
ms.sourcegitcommit: ad1afc6893a8dc32d1363395666b0fe1d50e983a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/23/2022
ms.locfileid: "8469932"
---
# <a name="scheduling-with-infinite-capacity"></a>Planlegging med ubegrenset kapasitet

[!include [banner](../../includes/banner.md)]

Funksjonen *Ubegrenset kapasitetsplanlegging for planleggingsoptimalisering* introduserer planlegging som er basert på ruteinformasjon. Det lar deg planlegge jobber basert på en rekke ruteoppsett. Planlegging for planleggingsoptimalisering dekker ofte brukte ruteinnstillinger, inkludert ruteoperasjonsrekkefølgen eller kravene for ruteoperasjonsressurser.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Slå på funksjonen for ubegrenset kapasitetsplanlegging

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Hovedplanlegging*
- **Funksjonsnavn:** *Uendelig kapasitetsplanlegging for Planleggingsoptimalisering*

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
