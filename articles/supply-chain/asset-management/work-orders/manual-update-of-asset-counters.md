---
title: Manuell oppdatering av anleggsmiddeltellere
description: Dette emnet beskriver manuell oppdatering av aktivatellere i Aktivastyring.
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
ms.openlocfilehash: 1e7c5ec288404c18b00f9dcd0e66f50744d0aa2f
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875821"
---
# <a name="manual-update-of-asset-counters"></a>Manuell oppdatering av anleggsmiddeltellere

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Tellere brukes til å opprette registreringer for et anleggsmiddel angående for eksempel antall timer i drift eller produsert antall.

Hvis tellertypen som er valgt for en teller, er satt til Arv tellerverdier (**Aktivastyring** > **Oppsett** > **Aktivatyper** > **Tellere** > **Generelt**-hurtigfanen > **Arv aktivatellerverdier**-veksleknappen satt til Ja), da, når du oppretter en ny tellerlinje av denne typen, oppdateres automatisk alle underordnede anleggsmidler som bruker samme tellertype.

I **Alle aktiva** oppretter du tellerregistreringer for timer eller antall for et aktivum basert på avlesningene for aktivaet.

1. Klikk på **Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva**.

2. Velg aktivaet i listen, og klikk på **Tellere**. I skjemaet **Aktivatellere** ser du en liste over alle tidligere tellerregistreringer for det valgte anleggsmidlet.

3. Klikk på **Ny** for å opprette en ny registrering. Anleggsmiddel-ID-en settes inn automatisk.

4. Velg den aktuelle telleren i **Teller**-feltet. Bare tellere for anleggsmiddeltypen som er valgt i anleggsmiddelet, er tilgjengelige. Den aktuelle enheten settes inn automatisk i **Enhet**-feltet.

5. Velg dato og klokkeslett for tellerregistreringen.

6. I **Verdi**-feltet setter du inn antallet siden den siste tellerregistreringen, eller setter inn totalt antall i **Aggregert verdi**-feltet.

- Hvis du fysisk installerer en ny teller på et anleggsmiddel, må du registrere endringen i anleggsmiddelet i **Aktivatellere**. Deretter må du opprette to registreringslinjer med identiske tidsstempler, og på linjen som gjelder den nye telleren, merker du av for **Tilbakestill teller**. Når du oppretter de to registreringslinjene, må den første linjen være for telleren du erstatter. I **Total**-feltet er totalt antall summen av tellertotalen for alle registrerte verdier på denne tellertypen.  
- Hvis det er merket av for **Tilbakestill teller** for et anleggsmiddel ved hjelp av en vedlikeholdsplan med intervalltypen Én gang fra... eller Når nådd..., er telleren fremdeles aktiv på den nye tellerlinjen fordi du oppretter en egen tellerlinje og begynner på nytt med en ny teller.

![Figur 1](media/11-work-orders.png)


Hvis du vil foreta tellerregistreringer på flere aktiva, kan du gjøre dette i **Aktivastyring** > **Forespørsler** > **Aktiva** > **Aktivatellere**.

>[!NOTE]
>Du kan angi et område for å definere avvik i manuelle tellerregistreringer, og typen melding som skal vises hvis registreringer er utenfor det definerte området. Se emnet [Tellere](../setup-for-objects/counters.md) om oppsett av tellere.
