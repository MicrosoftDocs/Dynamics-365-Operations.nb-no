---
title: Kostnads- og datokontroll
description: Dette emnet beskriver kostnads- og datokontroll i Aktivastyring.
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
ms.openlocfilehash: 2bcd1584f6a858f7589387fbfe96267b7c16176a
ms.sourcegitcommit: 2292b54e2da96f71b59ec9ccf17cd32d3d1d8b21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/23/2019
ms.locfileid: "1918401"
---
# <a name="cost-and-date-control"></a>Kostnads- og datokontroll

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I Aktivastyring kan du beregne kostnader for å få en oversikt over faktiske kostnader sammenlignet med budsjetterte kostnader for aktiva, arbeidssteder og arbeidsordrer. Faktiske kostnader er basert på posterte transaksjoner. Du kan også foreta en datoberegning hvis du vil sammenligne planlagte start- og sluttdatoer med faktiske start- og sluttdatoer på arbeidsordrer.

## <a name="cost-control-for-assets-functional-locations-and-work-orders"></a>Kostnadskontroll for aktiva, arbeidssteder og arbeidsordrer

Beregningene for aktiva, arbeidssteder og arbeidsordrer er nesten identiske. Den eneste forskjellen er at for anleggsmidler og arbeidssteder kan du også inkludere underordnede aktiva og underordnede arbeidssteder i beregningen. Datoen er transaksjonsdatoen da registreringen ble registrert.

1. Klikk på **Aktivastyring** > **Forespørsler** > **Aktiva** > **Kostnadskontroll for aktivum** eller **Kostnadskontroll for arbeidssted**, eller **Aktivastyring** > **Forespørsler** > **Arbeidsordrer** > **Kostnadskontroll for arbeidsordre**.

2. I dialogboksen **Kostnadskontroll for aktivum** / **Kostnadskontroll for arbeidssted** / **Kostnadskontroll for arbeidsordre** velger du en periode som skal beregnes.

3. Hvis det er nødvendig, velger du et finansdimensjonssett som skal tas med i beregningen.

4. Velg "Ja" på veksleknappen **Hopp over null** hvis du ikke vil vise resultater med en nullverdi.

5. Du kan bruke **Nivå**-feltet til å angi hvor detaljert kostnadskontrollinjene skal være når det gjelder arbeidssted. Hvis du for eksempel setter inn tallet 1 i feltet, og du har et arbeidsstedshierarki med flere nivåer, vises alle kostnadskontrollinjer for et arbeidssted på øverste nivå, og derfor kan det hende at timene på en linje blir lagt til fra arbeidssteder plassert på et lavere nivå. Hvis du setter inn tallet 0 i **Nivå**-feltet, vil du se et detaljert resultat som viser alle kostnadskontrollinjene på alle arbeidsstedsnivåene de er relatert til.

6. Velg "Ja" på veksleknappen **Vis åpen igangsatt kost** hvis du vil inkludere den aktuelle kolonnen i beregningen.

7. Velg Ja på veksleknappen **Inkluder underordnede aktiva** for å vise kostnader knyttet til underordnede aktiva som separate linjer.

8. Hvis du vil begrense søket, kan du velge bestemte anleggsmidler/arbeidssteder/arbeidsordrer i hurtigfanen **Poster som skal inkluderes**.

9. Klikk på **OK** for å starte beregningen.

Figuren nedenfor viser et eksempel på dialogboksen **Kostnadskontroll for aktivum**.

![Figur 1](media/01-controlling-and-reporting.png)

10. På siden **Kostnadskontroll for aktivum** i **Grupper etter...**-handlingsrutegruppene klikker du på de relevante knappene for å vise det nødvendige detaljnivået for beregningen. De valgte handlingsrutegruppeknappene er uthevet. Klikk på en knapp for å aktivere eller deaktivere den.

Figuren nedenfor viser et eksempel på beregningsresultater i **Kostnadskontroll for aktivum**.

![Figur 2](media/02-controlling-and-reporting.png)

En annen måte å gjøre en kostnadsberegning på er å velge flere aktiva i **Alle aktiva** eller **Aktive aktiva**. Deretter klikker du **Kostnadskontroll**-knappen i fanen **Generelt**. I dialogboksen **Kostnadskontroll for aktivum** settes de valgte anleggsmidlene automatisk inn i **Aktivum**-feltet i hurtigfanen **Poster som skal inkluderes**. Klikk **OK**, så vises den en beregning av kostnadene for de valgte anleggsmidlene. Den samme fremgangsmåten kan brukes for arbeidssteder i **Alle arbeidssteder** eller **Aktive arbeidssteder**, og for arbeidsordrer i **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

>[!NOTE]
>Feltet **Opprinnelig budsjett** viser budsjettkostnader fra arbeidsordreprognosen. Feltet **Igangsatt kost** viser det totale utgiftsbeløpet som en juridisk enhet har avtalt å betale. Feltet **Åpen igangsatt kost** viser forpliktelser som skal betales for varer, timer og tjenester du har bestilt eller mottatt, men ennå ikke betalt for. Når alle forbruksregistreringene er postert, tas de tilknyttede kostnadene med i **Faktiske kostnader**-feltet.

## <a name="work-order-date-control"></a>Datokontroll for arbeidsordre

Bruk denne siden til å få en oversikt over forventede start- og sluttdatoer sammenlignet med faktiske start- og sluttdatoer på arbeidsordrer.

1. Klikk **Aktivastyring** > **Forespørsler** > **Arbeidsordrer** > **Datokontroll for arbeidsordre**.

2. Klikk **Beregn**.

3. Velg et arbeidssted i **Arbeidssted**-feltet.

4. Sett inn perioden du vil gjøre beregningen for, i feltene **Fra dato** og **Til dato**. Alle arbeidsordrer med forventet start i perioden, blir inkludert.

5. Klikk **OK**.

6. I handlingsrutegruppene **Grupper etter...** klikker du de relevante knappene for å vise det nødvendige detaljnivået for beregningen. De valgte handlingsrutegruppeknappene er uthevet. Klikk på en knapp for å aktivere eller deaktivere den.

Figuren nedenfor viser et eksempel på beregningsresultater i **Datokontroll for arbeidsordre**.

![Figur 3](media/03-controlling-and-reporting.png)

- Feltet **Gj.sn. oppstartsforsinkelse** viser forskjellen i dager mellom planlagt startdato for en arbeidsordre sammenlignet med faktisk startdato. Hvis for eksempel den faktiske startdatoen var to dager før den planlagte startdatoen, vil -2 vises i dette feltet.  
- Feltet **Gj.sn. sluttforsinkelse** viser forskjellen i dager mellom planlagt sluttdato for en arbeidsordre sammenlignet med faktisk sluttdato. Hvis for eksempel den faktiske sluttdatoen var tre dager etter den planlagte sluttdatoen, vil 3 vises i dette feltet.  
- **Forekomster**-feltene viser antall ganger avvik forekommer i forhold til planlagt og faktisk startdato, og planlagt og faktisk sluttdato i arbeidsordren.
