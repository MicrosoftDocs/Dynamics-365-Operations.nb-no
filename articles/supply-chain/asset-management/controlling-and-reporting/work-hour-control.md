---
title: Arbeidstidskontroll
description: Dette emnet beskriver arbeidstidskontroll i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/23/2019
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
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 916e7b8d5d494dbae0659504957f7f0798a6834b
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918378"
---
# <a name="work-hour-control"></a>Arbeidstidskontroll

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I Aktivastyring kan du beregne timer for å få en oversikt over faktiske timer sammenlignet med budsjetterte timer for aktiva, arbeidssteder eller arbeidsordrer. Faktiske timer er basert på posterte transaksjoner.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Arbeidstidskontroll for aktiva, arbeidssteder og arbeidsordrer

Beregningene for aktiva, arbeidssteder og arbeidsordrer er nesten identiske. Den eneste forskjellen er at for anleggsmidler og arbeidssteder kan du også inkludere underordnede aktiva og underordnede arbeidssteder i beregningen. Datoen er transaksjonsdatoen da registreringen ble registrert.

1. Klikk på **Aktivastyring** > **Forespørsler** > **Aktiva** > **Timekontroll for aktivum** eller **Timekontroll for arbeidssted**, eller **Aktivastyring** > **Forespørsler** > **Arbeidsordrer** > **Timekontroll for arbeidsordre**.

2. I dialogboksen **Timekontroll for aktivum**, .

3. I dialogboksen **Timekontroll for aktivum** / **Timekontroll for arbeidssted** / **Timekontroll for arbeidsordre** velger du en periode som skal beregnes, i feltene **Fra dato** og **Til dato**.

4. Hvis det er nødvendig, velger du et **finansdimensjonssett** som skal tas med i beregningen.

5. Velg "Ja" på veksleknappen **Hopp over null** hvis du ikke vil vise resultater med null timer.

6. Du kan bruke **Nivå**-feltet til å angi hvor detaljert timekontrollinjene skal være når det gjelder arbeidssted. Hvis du for eksempel setter inn tallet 1 i feltet, og du har et arbeidsstedshierarki med flere nivåer, vises alle timekontrollinjer for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle timekontrollinjene på alle arbeidsstedsnivåene de er relatert til.

7. Velg Ja på veksleknappen **Inkluder underordnede aktiva** for å vise kostnader knyttet til underordnede aktiva som separate linjer.

8. Hvis du vil begrense søket, kan du velge bestemte anleggsmidler/arbeidssteder/arbeidsordrer i hurtigfanen **Poster som skal inkluderes**.

9. Klikk på **OK** for å starte beregningen.

10. På siden **Timekontroll for aktivum** i **Grupper etter...**-handlingsrutegruppene klikker du på de relevante knappene for å vise det nødvendige detaljnivået for beregningen. De valgte handlingsrutegruppeknappene er uthevet. Klikk på en knapp for å aktivere eller deaktivere den.

Figuren nedenfor viser et eksempel på beregning av **timekontroll for aktivum**.

![Figur 1](media/04-controlling-and-reporting.png)

En annen måte å gjøre en timeberegning på er å velge flere aktiva i **Alle aktiva** eller **Aktive aktiva**. Deretter klikker du på knappen **Timekontroll** i hurtigfanen **Generelt**. De valgte anleggsmidlene settes automatisk inn i **Aktivum**-feltet i hurtigfanen **Poster som skal inkluderes**. Klikk på **OK** i dialogboksen **Timekontroll for aktivum**, og beregningen for de valgte anleggsmidlene vises. Den samme fremgangsmåten kan brukes for arbeidssteder i **Alle arbeidssteder** eller **Aktive arbeidssteder**, og for arbeidsordrer i **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

>[!NOTE]
>Feltet **Opprinnelig budsjett** viser budsjetterte timer fra arbeidsordreprognosen. Feltet **Faktiske timer** viser posterte timer på arbeidsordrer. Feltet **Igangsatte timer** viser totalt antall timer som firmaet har forpliktet seg til i forhold til arbeidsordrer.
