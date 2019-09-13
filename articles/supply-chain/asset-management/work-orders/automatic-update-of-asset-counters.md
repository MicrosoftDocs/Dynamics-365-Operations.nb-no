---
title: Automatisk oppdatering av anleggsmiddeltellere
description: Dette emnet beskriver automatisk oppdatering av aktivatellere i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-15
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 97e6912cd37d6f82d8bf022141f04645a3364ee1
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875826"
---
# <a name="automatic-update-of-asset-counters"></a>Automatisk oppdatering av anleggsmiddeltellere

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I den forrige delen beskrives manuell registrering av anleggsmiddeltellere. Oppsett av anleggsmiddeltellere beskrives i [Tellere](../setup-for-objects/counters.md).

Tellerverdier kan også oppdateres automatisk fra produksjonsregistreringer, basert på produksjonstimer eller produksjonsantall. Dette gjøres i **Oppdater anleggsmiddeltellere**. Du kan oppdatere ett eller flere anleggsmidler ved å sette inn én parameter, **Fra dato**. Denne parameteren angir startdatoen for produksjonsregistreringer (timer eller produsert antall), som betyr startdatoen som tellerverdier skal oppdateres fra.

Alle aktiva som er relatert til en ressurs *og* og har anleggsmiddeltellere, som er definert til å oppdateres basert på produsert antall eller produksjonstimer, blir inkludert i en automatisk oppdatering, og nye tellerverdier blir opprettet.

Når det gjelder tellere basert på produksjonsantall, blir både korrekt antall og feil antall registrert i tellingen. Hvis enheten som brukes til registrering av produsert antall, er forskjellig fra enheten som brukes på telleren, konverteres antallet for å samsvare med tellerenheten.

Som nevnt ovenfor kan automatiske tellere oppdateres fra produksjonsregistreringer. Derfor må anleggsmiddelet du vil oppdatere tellere automatisk for, være relatert til en ressurs (maskin). Beskrivelsene nedenfor gir en oversikt over oppsett og behandling av produksjonsordrer (i modulen for **produksjonskontroll**), som brukes som et grunnlag for automatisk oppdatering av tellere for et anleggsmiddel i modulen **Aktivastyring**.

Når produsert antall eller produksjonstimer er registrert på ressursen, kan du oppdatere de tilknyttede anleggsmiddeltellerne.

1. Klikk på **Aktivastyring** > **Periodisk** > **Aktiva** > **Oppdater anleggsmiddeltellere**.

2. Velg startdatoen for den automatiske oppdateringen i **Fra dato**-feltet.

>[!NOTE]
>Datoen i dette feltet er datoen for arbeid som pågår fra **Rutetransaksjoner** (**Produksjonskontroll** > **Forespørsler og rapporterer** > **Produksjon** > **Rutetransaksjoner** > **Fysisk dato**-feltet).

3. Hvis du vil velge bestemte aktiva, aktivatyper eller ressurser for den automatisk oppdateringen, klikker du på **Filter** i hurtigfanen **Poster som skal inkluderes**, og gjør de aktuelle valgene.

4. På hurtigfanen **Kjør i bakgrunnen** kan du definere den automatiske oppdateringen som en satsvis jobb, om nødvendig.

![Figur 1](media/12-work-orders.png)

5. Klikk **OK**. Når den automatiske oppdateringen av anleggsmiddelteller er utført, kan du se tellerregistreringene som er knyttet til aktivumet i **Aktivatetellere** (**Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva** > velg aktivum **Tellere** -knappen).

I **Aktivateller totalt** kan du få en oversikt over den siste registreringen utført på alle tellertyper på alle anleggsmidler. Klikk **Aktivastyring** > **Forespørsler** > **Aktiva** > **Akkumulert verdi for aktivum**. Visningen ligner veldig **Aktivatellere**, men du kan ikke legge til eller redigere registreringer i **Akkumulert verdi for aktivum**. Den gjelder bare for oversikt.

![Figur 2](media/13-work-orders.png)


- Det er fremdeles mulig å opprette manuelle registreringer av tellerverdi for tellertyper som oppdateres automatisk. Se delen "Manuell oppdatering av anleggsmiddeltellere" hvis du vil ha mer informasjon.
- Du kan definere tellere relatert til en annen teller, som betyr at når en teller oppdateres, oppdateres relaterte tellere automatisk samtidig. Se emnet [Tellere](../setup-for-objects/counters.md) om oppsett av relaterte tellere.
