---
title: Innkjøp
description: Dette emnet beskriver innkjøp i Aktivastyring.
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
ms.openlocfilehash: 1678dbe2432e4be46aebb40a12e73dfd695c3e77
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875817"
---
# <a name="procurement"></a>Innkjøp


[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]

I Aktivastyring kan du få en oversikt over innkjøpsrekvisisjoner og bestillinger knyttet til arbeidsordrer. Det er også mulig å opprette en bestilling eller en innkjøpsrekvisisjon fra en arbeidsordre.

I listen **Innkjøpsrekvisisjon for arbeidsordre** (**Aktivastyring** > **Felles** > **Innkjøp** > **Innkjøpsrekvisisjon for arbeidsordre**) ser du en liste over innkjøpsrekvisisjoner knyttet til arbeidsordrer.

- Velg en arbeidsordrejobb i listen **Innkjøpsrekvisisjon for arbeidsordre**, og klikk på **Innkjøpsrekvisisjons**-knappen for å åpne den tilknyttede innkjøpsrekvisisjonen.  
- Velg en arbeidsordrejobb i listen **Innkjøpsrekvisisjon for arbeidsordre**, og klikk på **Arbeidsordre**-knappen for å åpne den tilknyttede arbeidsordren.  
- Velg en arbeidsordrejobb i listen **Innkjøpsrekvisisjon for arbeidsordre** og klikk på **Vare der brukt**-knappen hvis du vil ha en oversikt over hvor i Aktivastyring varen på den valgte linjen brukes, i forhold til aktiva, vedlikeholdsjobbtypestandarder, reservedeler og arbeidsordrer. 

![Figur 1](media/08-work-orders.png)


I listen **Arbeidsordrekjøp** (**Aktivastyring for bedrift** > **Felles** > **Innkjøp** > **Arbeidsordrekjøp**) kan du se en liste over bestillinger knyttet til arbeidsordrer.

- Velg en arbeidsordrejobb i listen **Arbeidsordrekjøp**, og klikk på **Bestilling**-knappen for å åpne den tilknyttede bestillingen.  
- Velg en arbeidsordrejobb i listen **Arbeidsordrekjøp**, og klikk på **Arbeidsordre**-knappen for å åpne den tilknyttede arbeidsordren.  
- Velg en arbeidsordrejobb i listen **Arbeidsordrekjøp** og klikk på **Vare der brukt**-knappen hvis du vil ha en oversikt over hvor i Aktivastyring varen på den valgte linjen brukes, i forhold til aktiva, vedlikeholdsjobbtypestandarder, reservedeler og arbeidsordrer. 

![Figur 2](media/09-work-orders.png)


I listene som vises ovenfor, plasseres et ikon for leveringsdatokontroll til høyre på hver linje. Hvis ikonet viser et utropstegn i en rød sirkel, betyr det at levering i den tilknyttede innkjøpsrekvisisjonen eller bestillingen kan bli forsinket.

I en innkjøpsrekvisisjon finner du datoen som brukes til å beregne mulig forsinkelse, i **Innkjøpsrekvisisjoner**-skjemaet > hurtigfanen **Innkjøpsrekvisisjonshode** > **Ønsket dato**-feltet. Denne datoen sammenlignes med den tilgjengelige datoen i arbeidsordren eller arbeidsordrejobben på samme måte som bestillingsdatoen.

I en bestilling er datoen som brukes til å beregne mulig forsinkelse, datoen knyttet til bestillingslinjen, som vises i **Bestilling**-skjemaet > velg bestillingslinje > **Linjedetaljer**-hurtigfanen > **Oppsett**-kategorien > **Bekreftet leveringsdato**-feltet. Hvis dette feltet ikke er fylt ut, brukes datoen i **Leveringsdato**-feltet i hurtigfanen **Bestillingshode**. Én av disse datoene sammenlignes med den tilgjengelige datoen i arbeidsordren eller arbeidsordrejobben i følgende rekkefølge:

- Faktisk startdato i arbeidsordren, eller  

- Planlagt startdato i den tilknyttede arbeidsordrejobben, eller  

- Planlagt startdato i arbeidsordren, eller  

- Forventet startdato i arbeidsordren  


## <a name="create-purchase-order-from-a-work-order"></a>Opprette bestilling fra en arbeidsordre

I **Alle arbeidsordrer** velger du en arbeidsordrejobb og oppretter en tilknyttet bestilling eller en innkjøpsrekvisisjon. Dette gjøres for å sikre prosjektrelasjoner mellom bestillingen eller innkjøpsrekvisisjonen og arbeidsordren.

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. I listen **Alle arbeidsordrer** eller **Aktive arbeidsordrer** velger du arbeidsordren du vil opprette en bestilling for, og klikker på **Rediger**.

3. I **Arbeidsordre**-skjemaet > hurtigfanen **Vedlikeholdsjobber for arbeidsordre** velger du arbeidsordrejobben som du vil opprette bestillingen for.

4. Klikk på **Vareoppgaver** > **Bestilling fra arbeidsordrejobb**.

5. Klikk på **Ny** på listesiden **Prosjektbestillinger**.

6. Opprett bestillingen.

>[!NOTE]
>Det å opprette en innkjøpsrekvisisjon er nesten identisk med å opprette en bestilling. Den eneste forskjellen er at du i fremgangsmåten ovenfor klikker på **Vareoppgaver** > **Innkjøpsrekvisisjon fra arbeidsordrejobb** i trinn 2.

## <a name="project-relation-between-work-order-and-purchase-order-or-purchase-requisition"></a>Prosjektrelasjon mellom arbeidsordre og bestilling eller innkjøpsrekvisisjon

En bestillingslinje eller innkjøpsrekvisisjonslinje er knyttet til en arbeidsordrejobb via arbeidsordreprosjektet og det tilknyttede prosjektaktivitetsnummeret. Når du oppretter en bestilling eller en innkjøpsrekvisisjon fra en arbeidsordrejobb, er det tilknyttede prosjektaktivitetsnummeret obligatorisk. Prosjektaktivitetsnummeret settes automatisk inn på en bestilling eller innkjøpsrekvisisjon hvis den tilknyttede arbeidsordren inneholder arbeidsordrejobber som alle bruker den samme vedlikeholdsjobbtypen. Hvis arbeidsordrejobbene inneholder forskjellige vedlikeholdsjobbtyper, må prosjektaktivitetsnummeret settes inn manuelt.

Hvis du vil se eller sette inn aktivitetsnummeret som er knyttet til en bestillingslinje, åpner du **Arbeidsordrekjøp** > velger bestillingsposten > klikker på bestillingen i **Bestilling**-kolonnen > **Linjedetaljer**-hurtigfanen > **Prosjekt**-kategorien > **Aktivitetsnummer**-feltet.


![Figur 3](media/10-work-orders.png)


Tilsvarende, hvis du vil se eller sette inn aktivitetsnummeret som er knyttet til en linje for arbeidsordreinnkjøpsrekvisisjon, åpner du **Innkjøpsrekvisisjon for arbeidsordre** > velger innkjøpsrekvisisjonsposten > klikker på innkjøpsrekvisisjonen i **Innkjøpsrekvisisjon**-kolonnen > **Linjedetaljer**-hurtigfanen > **Prosjekt**-kategorien > **Aktivitetsnummer**-feltet.

