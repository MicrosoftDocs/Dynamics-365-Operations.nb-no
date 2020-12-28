---
title: Planlegg vedlikeholdsplaner
description: Dette emnet beskriver planlegging av vedlikeholdsplaner i Aktivastyring.
author: josaw1
manager: tfehr
ms.date: 08/27/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: df5bcd57c611ed5f77a417a28f28fca84057d734
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434521"
---
# <a name="schedule-maintenance-plans"></a>Planlegg vedlikeholdsplaner

[!include [banner](../../includes/banner.md)]

 

Forebyggende vedlikeholdsplanlegging genererer kalenderoppføringer for aktiva, basert på oppsettet av vedlikeholdsplaner for aktivaene. Du kan planlegge kalenderoppføringer basert på valgte vedlikeholdsplaner, anleggsmiddeltyper og anleggsmidler.

1. Klikk på **Aktivastyring** > **Periodisk** > **Forebyggende vedlikehold** > **Planlegg vedlikeholdsplaner**.

2. Du kan velge et tidsintervall i feltene **Periode** og **Periodefrekvens**.

>[!NOTE]
>Feltene **Periode** og **Periodefrekvens** angir hvor langt frem i tid du vil at vedlikeholdsplanlinjer skal opprettes, basert på vedlikeholdsplanene du har opprettet (tidsbasert eller tellerbasert). I figuren nedenfor opprettes vedlikeholdsplanlinjer (= arbeidsordreforslag) fra gjeldende dato og tre måneder fremover.

3. Velg Ja på veksleknappen **Opprett automatisk hvis angitt i linjen** hvis arbeidsordrer skal opprettes automatisk i henhold til vedlikeholdsplanlinjen.

>[!NOTE]
>Hvis denne veksleknappen er satt til *Ja*, og det også er merket av for **Opprett automatisk** på vedlikeholdsplanlinjer i **Vedlikeholdsplaner**, opprettes arbeidsordrer på grunnlag av vedlikeholdsplanlinjene, og vedlikeholdsplanlinjer med statusen "Arbeidsordre opprettet" opprettes også. Hvis bare ett alternativ er valgt (**Opprett automatisk hvis angitt i linjen**-veksleknappen i denne dialogboksen eller avmerkingsboksen **Opprett automatisk** i skjemaet **Vedlikeholdsplaner**), opprettes bare vedlikeholdsplanlinjer med statusen Opprettet. I dette tilfellet opprettes ingen arbeidsordrer.

4. Det er mulig å generere kalenderoppføringer basert på vedlikeholdsplaner (tid eller teller), aktiva, aktivatyper, arbeidssteder og arbeidsstedstyper. Klikk på **Filter**-knappen, og gjør valg hvis nødvendig.

- Når det gjelder planlegging av vedlikeholdsplaner på arbeidssteder: Hvis du oppdaterer oppsettet for aktivatyper, produsenter og modeller i vedlikeholdsplaner i **Alle arbeidssteder** > hurtigfanen **Vedlikeholdsplaner** etter at du har opprettet vedlikeholdsplaner, blir eksisterende oppføringer i vedlikeholdsplanen relatert til arbeidsstedet slettet automatisk. Hvis du vil opprette nye kalenderoppføringer, som samsvarer med det oppdaterte vedlikeholdsplanoppsettet på arbeidsstedet, må du kjøre en ny tidsplan for vedlikeholdsplanen for dette arbeidsstedet. Les mer om oppsettet av aktivatyper, produsenter og modeller på arbeidssteder i [Opprette arbeidssteder](../functional-locations/create-functional-locations.md).

>*Eksempel:* Du vil opprette en vedlikeholdsplan for et bestemt arbeidssted, som betyr at alle anleggsmidler som er definert for dette arbeidsstedet på et gitt tidspunkt, blir tatt med når du planlegger vedlikeholdsplanen. I dette tilfellet oppretter du en vedlikeholdsplan og velger det bestemte arbeidsstedet, men du legger IKKE til noen aktiva i vedlikeholdsplanen. Resultatet er at når du planlegger denne vedlikeholdsplanen, opprettes vedlikeholdsplanlinjer for alle anleggsmidlene som er knyttet til arbeidsstedet på dette tidspunktet.

- Hvis du endrer aktivatyper, produsenter og modeller i **Aktivatyper**, påvirker disse endringene bare nye anleggsmidler som bruker den oppdaterte aktivatypen. Les mer om oppsett av anleggsmiddeltyper i [Aktivatyper](../setup-for-objects/object-types.md).  

5. Klikk på **OK** for å starte genereringen av vedlikeholdsplanoppføringer for aktiva. De genererte oppføringene vil vises på listesiden **Alle vedlikeholdsplaner**. Illustrasjonen nedenfor viser et eksempel på dialogboksen **Planlegg vedlikeholdsplaner**.

![Figur 1](media/09-preventive-maintenance.png)

- I dialogboksen **Planlegg vedlikeholdsplaner** kan du definere satsvise jobber i hurtigfanen **Kjør i bakgrunnen** for å generere kalenderoppføringer automatisk med jevne mellomrom.  
- Når du planlegger forebyggende vedlikehold, vil ikke vedlikeholdsplanlinjer med forventet startdato og -klokkeslett før systemdatoen og -klokkeslettet bli opprettet.  

Figuren nedenfor gir en grafisk illustrasjon av en tidsbasert beregning av vedlikeholdsplan.  

![Figur 2](media/10-preventive-maintenance.jpg)

Angående tellerbaserte vedlikeholdsplaner: I figurene nedenfor vises to forskjellige tellerregistreringssykluser. De er basert på en vedlikeholdsplan som er definert for anleggsmiddelet V0001, som forventer at aktivaet (en bil) kan kjøre cirka 2 000 km hver måned.

I det første eksemplet nås ikke de forventede 2 000 km hver måned. I henhold til den tellerbaserte vedlikeholdsplanen, er terskelen 2 000 km. Dette betyr at når du kjører en planlegging av vedlikeholdsplan, skal det opprettes en vedlikeholdsplanlinje hver gang terskelen på 2 000 kilometer nås. I eksempel 1 finnes det 4 registreringslinjer, men terskelen på 2 000 kilometer er bare nådd én gang. Dette betyr at når du kjører planlegging av vedlikeholdsplaner for dette anleggsmidlet, for eksempel for en tre-måneders periode, vil det bare bli opprettet én vedlikeholdsplanlinje.

I den neste figuren er 2 000 km eller mer registrert hver måned. Derfor opprettes det tre vedlikeholdslinjer hvis du planlegger vedlikeholdsplaner for dette anleggsmidlet for en periode på tre måneder. 

Eksemplene som beskrives her, viser at alle tellerregistreringer som er utført for et anleggsmiddel, viser en trend som beskriver slitasje på aktivaet. Trenden brukes som beregningsgrunnlag på tidspunktet for planleggingen av vedlikeholdsplanen.

![Figur 3](media/11-preventive-maintenance.png)

![Figur 4](media/12-preventive-maintenance.png)

