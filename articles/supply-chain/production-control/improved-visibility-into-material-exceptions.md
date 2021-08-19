---
title: Oversikt over materialeunntak
description: Dette emnet beskriver hvordan du får bedre innsyn i unntak for råvarer for produksjonsordrer og partiordrer.
author: johanhoffmann
ms.date: 10/30/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: JmgShopSupervisorWorkspace, WHSProdWaveTableListPage, WHSProdWaveTableManageBOMPool
audience: Application User
ms.reviewer: kamaybac
ms.custom: 1705903
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2017-12-31
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: d3ea260535e76d7ac3d73d4bca930b7b4b2d22b2b2c076d4d1346785eaed85b8
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6726807"
---
# <a name="visibility-into-material-exceptions"></a>Oversikt over materialeunntak

[!include [banner](../includes/banner.md)]

I **Produksjonsstyring**-arbeidsområdet gir tre fliser deg bedre oversikt over unntak for råvarer for produksjonsordrer og partiordrer:

- Ikke-frigitte materiallinjer som krever oppmerksomhet
- Ubehandlede bølger som krever oppmerksomhet
- Åpent lagerarbeid som krever oppmerksomhet

For alle tre flisene sammenlignes råvaredatoen i stykklistelinjene og formellinjene med arbeidsområdedatoen, og også med filtrene for **Produksjonsenhet**, **Ressursgruppe** og **Ressurs** som er angitt på **Konfigurer mitt arbeidsområde**-menyen. Som standard settes arbeidsområdedatoen til gjeldende dato, men du kan justere den.

En ikke frigitt stykklistelinje eller formellinje krever tilsyn hvis råvaredatoen på linjen er den samme som eller før arbeidsområdedatoen, og hvis den oppfyller vilkårene som er definert i filtrene i arbeidsområdet.

Det blå feltet representerer en produksjonsjobb som er planlagt for en ressurs, i illustrasjonen nedenfor. Jobben er planlagt å starte 1. mai 2017 (01.05.2017). Denne datoen er råvaredatoen. Materialene som er tilordnet jobben på stykkliste- og formellinjene, må altså være klar på denne datoen. Den andre datoen i figuren, 6. mai 2017 (06.05.2017) representerer arbeidsområdedatoen. I dette eksemplet er råvaredatoen før arbeidsområdedatoen. Derfor har datoen da forbruket av råvarer skulle starte, passert, og stykkliste- og formellinjene oppfyller kriteriene for å kreve oppmerksomhet.

![Eksempel på en produksjonsjobb der råvaredatoen er før arbeidsområdedatoen.](./media/improved-visibility.png)

## <a name="unreleased-material-lines-needing-attention"></a>Ikke-frigitte materiallinjer som krever oppmerksomhet

En stykkliste- eller formellinje kan frigis til lageret på tre måter:

- Som en del av en produksjonsordre- eller partiordrefrigivelse
- Som en manuell frigivelse
- Automatisk gjennom en satsvis jobb

Hvis du vil ha mer informasjon, se [Frigi stykkliste- og formellinjer til lageret](releasing-bom-and-formula-lines-to-warehouse.md). 

Hvis en stykkliste- eller formellinje ikke er frigitt eller bare er delvis frigitt, og hvis dato- og filtervilkårene for arbeidsområdet er oppfylt, inkluderes linjen i beregningen av antallet som vises i flisen **Ikke-frigitte materiallinjer som krever oppmerksomhet**.

Når du velger flisen, åpnes **Frigi til lager**-siden. Denne siden viser antall ikke frigitte stykkliste- og formellinjer, som angis med tallet i flisen. De ikke frigitte linjene vises i det øvre rutenettet. Dette rutenettet viser antallet som opprinnelig ble beregnet for linjen, antallet som allerede er frigitt, og det gjenværende antallet som fortsatt må frigis. Du kan legge til linjer fra den øvre rutenett til det nedre rutenettet. Fra det nedre rutenettet kan du deretter frigi de valgte linjene til lageret. Du kan også justere antallet som skal frigis, fra den nedre rutenettet, slik at bare et delvis antall frigis.

## <a name="unprocessed-waves-needing-attention"></a>Ubehandlede bølger som krever oppmerksomhet

Når en stykkliste- eller formellinje frigis, legges den til en ny produksjonsbølge eller en eksisterende åpen bølge, avhengig av konfigurasjonen av produksjonsbølgemalen. Gjennom konfigurasjonen av bølgemalen kan du også definere en bølge slik at den behandles automatisk når en stykkliste- eller formellinje frigis. Når bølgen er behandlet, genereres det lagerarbeid for råvareplukking. Hvis bølgemalen er konfigurert slik at bølger ikke behandles ved frigivelsen, forblir bølgen i en ubehandlet tilstand. Flisen **Ubehandlede bølger som krever oppmerksomhet** viser antallet stykkliste- og formellinjer som er frigitt til lageret på ubehandlede bølger, og som har en råvaredato som er tidligere enn eller lik arbeidsområdedatoen. Linjene må også brukes av en operasjonsressurs som brukes på filteret i arbeidsområdet.

Når flisen er valgt, åpnes **Alle produksjonsbølger**-siden. Denne siden er filtrert etter hvor mange åpne bølger som inneholder bølgelinjer fra frigitte stykkliste- og formellinjer som oppfyller kriteriene for flisen.

### <a name="manually-maintain-production-waves"></a>Vedlikehold produksjonsbølger manuelt

På siden **Alle produksjonsbølger** kan du bruke knapper på **Bølge**-fanen i handlingsruten til å **behandle** og **frigi** en bølge manuelt. Du kan også bruke alternativet **Vedlikehold produksjoner** til å vise og vedlikeholde **Produksjonsstykklisteutvalg**-data, som brukes til å håndtere bølgeprosessen.

## <a name="open-warehouse-work-needing-attention"></a>Åpent lagerarbeid som krever oppmerksomhet

Flisen **Åpent lagerarbeid som krever oppmerksomhet** viser antallet stykkliste- og formellinjer som er frigitt til lageret, som har ubehandlet arbeid og en råvaredato som er tidligere enn eller lik arbeidsområdedatoen. Linjene må også brukes av en operasjonsressurs som brukes på filteret i arbeidsområdet.

Når flisen er valgt, åpnes **Alt arbeid**-siden. Denne siden er filtrert etter hvor mange åpne arbeidshoder som inneholder arbeidslinjer fra frigitte stykkliste- og formellinjer som oppfyller kriteriene for flisen. Fra **Alt arbeid**-siden kan du behandle arbeidet manuelt.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]