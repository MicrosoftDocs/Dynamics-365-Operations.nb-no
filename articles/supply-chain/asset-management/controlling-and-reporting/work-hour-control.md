---
title: Arbeidstidskontroll
description: Dette emnet beskriver arbeidstidskontroll i Aktivastyring.
author: johanhoffmann
ms.date: 08/23/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EntAssetHourControl
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 90c4f649cc9ea45341ede923294a7c5a892cd68714db356c3799430d18f5de60
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6742782"
---
# <a name="work-hour-control"></a>Arbeidstidskontroll

[!include [banner](../../includes/banner.md)]

 

I Aktivastyring kan du beregne timer for å få en oversikt over faktiske timer sammenlignet med budsjetterte timer for aktiva, arbeidssteder eller arbeidsordrer. Faktiske timer er basert på posterte transaksjoner.

## <a name="work-hour-control-for-assets-functional-locations-and-work-orders"></a>Arbeidstidskontroll for aktiva, arbeidssteder og arbeidsordrer

Beregningene for aktiva, arbeidssteder og arbeidsordrer er nesten identiske. Den eneste forskjellen er at for anleggsmidler og arbeidssteder kan du også inkludere underordnede aktiva og underordnede arbeidssteder i beregningen. Datoen er transaksjonsdatoen da registreringen ble registrert.

1. Klikk på **Aktivastyring** > **Forespørsler** > **Aktiva** > **Timekontroll for aktivum** eller **Timekontroll for arbeidssted**, eller **Aktivastyring** > **Forespørsler** > **Arbeidsordrer** > **Timekontroll for arbeidsordre**.

2. I dialogboksen **Timekontroll for aktivum**, .

3. I dialogboksen **Timekontroll for aktivum** / **Timekontroll for arbeidssted** / **Timekontroll for arbeidsordre** velger du en periode som skal beregnes, i feltene **Fra dato** og **Til dato**.

4. Hvis det er nødvendig, velger du et **finansdimensjonssett** som skal tas med i beregningen.

5. Velg "Ja" på veksleknappen **Hopp over null** hvis du ikke vil vise resultater med null timer.

6. Du kan bruke **Nivå**-feltet til å angi hvor detaljert timekontrollinjene skal være når det gjelder arbeidssted. 

    Hvis du for eksempel setter inn tallet 1 i feltet, og du har et arbeidsstedshierarki med flere nivåer, vises alle timekontrollinjer for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. 
    
    Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle timekontrollinjene på alle arbeidsstedsnivåene de er relatert til.

7. Velg Ja på veksleknappen **Inkluder underordnede aktiva** for å vise kostnader knyttet til underordnede aktiva som separate linjer.

8. Hvis du vil begrense søket, kan du velge bestemte anleggsmidler/arbeidssteder/arbeidsordrer i hurtigfanen **Poster som skal inkluderes**.

9. Klikk på **OK** for å starte beregningen.

10. På siden **Timekontroll for aktivum** klikker du på knappen **Grupper etter** for å vise det nødvendige detaljnivået for beregningen. De valgte **Grupper etter**-knappen er uthevet. Klikk på en knapp for å aktivere eller deaktivere den.

## <a name="example"></a>Eksempel

Skjermbildet nedenfor viser et eksempel på beregning av **timekontroll for aktivum**.

- Feltet **Opprinnelig budsjett** viser budsjetterte timer fra arbeidsordreprognosen. 
- Feltet **Faktiske timer** viser posterte timer på arbeidsordrer. 
- Feltet **Igangsatte timer** viser totalt antall timer som firmaet har forpliktet seg til i forhold til arbeidsordrer.

![Eksempel på beregning av timekontroll for aktivum.](media/04-controlling-and-reporting.png)

En annen måte å gjøre en timeberegning på er å velge flere aktiva i **Alle aktiva** eller **Aktive aktiva**. Deretter klikker du på knappen **Timekontroll** i hurtigfanen **Generelt**. De valgte anleggsmidlene settes automatisk inn i **Aktivum**-feltet i hurtigfanen **Poster som skal inkluderes**. Klikk på **OK** i dialogboksen **Timekontroll for aktivum**, og beregningen for de valgte anleggsmidlene vises. Den samme fremgangsmåten kan brukes for arbeidssteder i **Alle arbeidssteder** eller **Aktive arbeidssteder**, og for arbeidsordrer i **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.




[!INCLUDE[footer-include](../../../includes/footer-banner.md)]