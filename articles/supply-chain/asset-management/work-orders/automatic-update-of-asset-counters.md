---
title: Automatisk oppdatering av anleggsmiddeltellere
description: Denne artikkelen beskriver automatisk oppdatering av aktivatellere i Aktivastyring.
author: johanhoffmann
ms.date: 10/15/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8ea84259eb8f12becdcf008ed9222a44b2626a0d
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9016224"
---
# <a name="automatic-update-of-asset-counters"></a>Automatisk oppdatering av anleggsmiddeltellere

[!include [banner](../../includes/banner.md)]

Hvis du vil ha informasjon om manuell registrering av aktivatellere, se [Manuell oppdatering av aktivatellere](../work-orders/manual-update-of-asset-counters.md) Hvis du vil ha informasjon om hvordan du definerer aktivatellere, se [Tellere](../setup-for-objects/counters.md).

Tellerverdier kan også oppdateres automatisk fra produksjonsregistreringer, basert på produksjonstimer eller produksjonsantall (dvs. antallet som produseres). Denne oppdateringen utføres på siden **Oppdater aktivatellere**. Du kan oppdatere ett eller flere aktiva ved å angi én parameter, **Fra dato**. Denne parameteren angir startdatoen for produksjonsregistreringer (produksjonstimer eller produksjonsantall). Den angir med andre ord datoen som tellerverdiene skal oppdateres fra.

Alle aktiva som er relatert til en ressurs *og* som har aktivatellere som er definert til å oppdateres basert på produksjonstimene eller produksjonsantallet, blir inkludert i en automatisk oppdatering. Nye tellerverdier blir opprettet.

For tellere som er basert på produksjonsantallet, inneholder tellingen både antall korrekte og antall feil som er registrert. Hvis enheten som brukes til registrering av produsert antall, er forskjellig fra enheten som brukes for telleren, konverteres antallet slik at det samsvarer med tellerenheten.

Som nevnt ovenfor kan automatiske tellere oppdateres fra produksjonsregistreringer. Derfor må anleggsmiddelet du vil oppdatere tellere automatisk for, være relatert til en ressurs (maskin). Når produsert antall eller produksjonstimer er registrert på ressursen, kan du oppdatere de tilknyttede anleggsmiddeltellerne.

1. Velg **Aktivastyring** > **Periodisk** > **Aktiva** > **Oppdater aktivatellere**.

2. Velg startdatoen for den automatiske oppdateringen i **Fra dato**-feltet.

    >[!NOTE]
    >Datoen i dette feltet er datoen for arbeid som pågår fra **Rutetransaksjoner** (**Produksjonskontroll** > **Forespørsler og rapporterer** > **Produksjon** > **Rutetransaksjoner** > **Fysisk dato**-feltet).

3. I hurtigfanen **Poster som skal inkluderes** kan du velge bestemte aktiva, aktivatyper eller ressurser for den automatiske oppdateringen. Velg **Filter**, og gjør de relevante valgene.

4. På hurtigfanen **Kjør i bakgrunnen** kan du definere den automatiske oppdateringen som en satsvis jobb, slik du ønsker.

    Illustrasjonen nedenfor viser et eksempel på dialogboksen **Oppdater aktivatellere**.

    ![Figur 1.](media/12-work-orders.png)

5. Velg **OK**. 

Når oppdateringen for den automatiske aktivatelleren er utført, kan du vise tellerregistreringer som er knyttet til aktivumet, på siden **Aktivatellere**. Velg **Aktivastyring** > **Aktiva** > **Alle aktiva**, velg aktivumet, gå til handlingsruten, **Aktiva**-fanen, **Forebyggende**-gruppen, og velg **Tellere**.

På siden **Akkumulert verdi for aktivum** kan du få en oversikt over den siste registreringen som er utført på alle tellertyper på alle aktiva. Velg **Aktivastyring** > **Forespørsler** > **Aktiva** > **Akkumulert verdi for aktivum**. Denne siden ligner på siden **Aktivatellere**, men du kan ikke legge til eller redigere registreringer. Den er bare en oversikt.

Illustrasjonen nedenfor viser et eksempel på siden **Akkumulert verdi for aktivum**.

![Figur 2.](media/13-work-orders.png)

Merk følgende punkt:

- Det er fremdeles mulig å opprette manuelle registreringer av tellerverdi for tellertyper som oppdateres automatisk. Se [Manuell oppdatering av anleggsmiddeltellere](../work-orders/manual-update-of-asset-counters.md) hvis du vil ha mer informasjon.

- Du kan definere tellere som er relatert til en annen teller. I dette tilfellet oppdateres tilknyttede tellere automatisk samtidig når en teller oppdateres. Hvis du vil ha informasjon om hvordan du definerer relaterte tellere, se [Tellere](../setup-for-objects/counters.md).



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]