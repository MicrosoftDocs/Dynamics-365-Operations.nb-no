---
title: Arbeidsområde for lastplanlegging
description: Dette emnet beskriver hvordan du arbeider med arbeidsområde for lastplanlegging.
author: Henrikan
manager: ''
ms.date: 10/30/2020
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSLoadBuildWorkbench,TMSLoadBuildTemplateCreate,TMSLoadBuildStrategy,TMSLoadBuildTemplateApply
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: Distribution
ms.author: henrikan
ms.search.validFrom: 2020-10-30
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 480006a6d091acdf5c88fdbf0d9e625088d660d4
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5247244"
---
# <a name="load-building-workbench"></a>Arbeidsområde for lastplanlegging

Med arbeidsområde for lastplanlegging kan du bruke lastplanleggingsstrategier når du oppretter belastninger.

## <a name="create-a-load-building-strategy"></a>Opprett en lastplanleggingsstrategi

Du bruker lastplanleggingsstrategier til å bygge belastninger automatisk. Denne funksjonen kan være nyttig i følgende situasjoner:

- Hvis du ofte sender et bestemt sett med produkter, vil laststrategier hjelpe deg med å spare tid, fordi du ikke trenger å bygge den samme belastningen hver gang.
- Hvis du vil unngå halvfulle belastninger for å maksimere effektiviteten, kan laststrategier bidra til å fylle hver belastning så mye som mulig.

En laststrategiklasse som heter `TMSLoadBuildingVolumeStrategy` gir en laststrategi som heter *Volumbasert laststrategi*. Med denne strategien kan du bruke de maksimale verdiene som er angitt for høyde og vekt i lastmalen, eller du kan overstyre innstillingene ved å angi nye verdier. Denne strategien er den eneste strategien som er inkludert. (Du kan imidlertid ha noen egendefinerte strategier.)

Hvis du vil bruke den bruksklare strategien *Volumbasert strategi for lastplanlegging*, velger du den i feltet **Strategi for lastplanlegging** på siden **Arbeidsområde for lastplanlegging** (**Transportstyring &gt; Planlegging &gt; Arbeidsområde for lastplanlegging)**.

Følg denne fremgangsmåten for å opprette en strategi for lastplanlegging.

1. Gå til **Transportstyring &gt; Oppsett &gt; Lastplanlegging &gt; Strategier for lastplanlegging**.
1. I handlingsruten velger du **Generer klasseliste** for å kontrollere at du har siste versjon av alle tilgjengelige klasser.
1. Velg **Ny** i handlingsruten.
1. Angi et unikt navn for strategien, velg klassen til strategien for lastplanlegging for den, og angi en beskrivelse.
1. Velg **Lagre** i handlingsruten.
1. Velg **Parametere** i handlingsruten.
1. På siden **Parametere for strategi for lastplanlegging** velger du **Volumkapasitet** i listen, og deretter angir du i feltet **Verdi** prosentandelen av lastens totale volumkapasitet som skal tas i bruk for den nye strategien for lastplanlegging.
1. Velg **Vektkapasitet** i listen, og angi deretter i feltet **Verdi** prosentandelen av lastens totale vektkapasitet som skal tas i bruk for den nye strategien for lastplanlegging.
1. Lukk siden **Parametere for strategi for lastplanlegging**.
1. Lukk siden **Strategier for lastplanlegging**.

Nå kan du tilordne en strategi for lastplanlegging til en mal for lastplanlegging. Du kan også bruke den direkte i arbeidsområdet for lastplanlegging.

## <a name="use-a-load-building-strategy-in-the-load-building-workbench"></a>Bruk en strategi for lastplanlegging i arbeidsområdet for lastplanlegging

1. Gå til **Transportstyring &gt; Planlegging &gt; Arbeidsområde for lastplanlegging**.
1. Følg ett av disse trinnene:

    - Velg en strategi i feltet **Strategi for lastplanlegging**.
    - Hvis du har definert en lastplanleggingsmal og tilordnet strategien for lastplanlegging til den, velger du **Bruk mal** i handlingsruten i fanen **Administrer maler**. Deretter velger du en mal i feltet **Navn på lastplanleggingsmal** i rullegardinfeltet **Bruk lastplanleggingsmal**.

1. Velg én eller flere [lastmaler](load-template.md) i hurtigfanen **Lastmalsekvens**. Arbeidsområdet vil forsøke å tilpasse belastningen inn i disse beholderne, i rekkefølgen som er angitt her. Vanligvis bør du plassere de minste beholderne øverst på listen for å sikre at den minste mulige beholderen velges først.
1. Klikk på **Foreslå laster** i handlingsruten.
1. Se gjennom de foreslåtte lastene og foreslåtte lastlinjene.
1. Velg **Opprett laster** i handlingsruten for å opprette laster som er basert på kildedokumentlinjene på hurtigfanen **Foreslåtte belastningslinjer** i handlingsruten.
1. Lukk siden **Arbeidsområde for lastplanlegging**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]