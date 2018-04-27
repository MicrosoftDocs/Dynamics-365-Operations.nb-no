---
title: Stykkplukkingsbekreftelse
description: Dette emnet beskriver hvordan du definerer og bruker stykkplukkingsbekreftelse fra en mobilenhet.
author: Mirzaab
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 5ef9ab68c20ae095de03b0a0e05aa15ef5bf8a5d
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="piece-picking-confirmation"></a>Stykkplukkingsbekreftelse

[!INCLUDE [banner](../includes/banner.md)]

Med stykkplukking kan du bekrefte hver del av lagerbeholdningen gjennom plukkings- og tellingsarbeid på en mobil enhet. For plukking kan du kontrollere hvor mye arbeid som skal behandles opptil antallet som er angitt på arbeid som skal plukkes. For opptellingsarbeid kan du skanne lageret du teller opp, og spore totalbeløpet.

Når du aktiverer stykkplukking, velges produktbekreftelse automatisk. For arbeidstypen plukk aktiveres et maksimalt antall stykker. Dette gjør at du kan angi et maksimalt antall enheter som må bekreftes under arbeidsprosessen. Maksimalt antall er basert på den gjeldende arbeidsenheten som behandles. Opptellingsarbeidstypen tillater ikke et maksimum.

Du kan også bruke antall og måleenhet som er tilknyttet en skannet strekkode. Dette vil fungere for mottak på innkommende flyter inkludert mottak av kombinerte skiltnumre, bestillingsvare, overføringsordrevare og lastvare. Det fungerer også for stykkplukking der skanning av strekkoden vil legge til antallet i totalt antall bekreftede stykker som er konvertert mellom måleenheten på strekkoden og arbeidsenheten. Hvis det, ved telling av måleenheten på strekkoden, bekreftes at antallet er tillatt for opptelling på sekvensgruppen, legges antallet til totalantallet.

## <a name="where-it-applies"></a>Der det er aktuelt

Stykkplukking fungerer for alt opptellingsarbeid og for første plukking for alle typer arbeid. Stykkplukking gjelder ikke hvis varen styres av serienumre eller hvis det er en produksjons- eller kanbanplukking fra en nummerskiltlokasjon og varen er satt til oppsamling.

## <a name="set-up-piece-picking"></a>Definer stykkplukking

1.  Åpne oppsettskjemaet for arbeidsbekreftelse på et menyelement for mobilenhet: Lagerstyring > **Lagerstyring** > **Oppsett** > **Mobilenhet** > **Menyelementer på mobilenheten**. 
2. Åpne Arbeidsbekreftelsesoppsett fra menyelement for mobilenhet.

Følgende alternativer blir tilgjengelige når arbeidstypen er plukking og opptelling.


|           Alternativ           |                                                                            beskrivelse                                                                            |
|----------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Stykkplukkingsbekreftelse | Tilgjengelig for arbeidstypene plukking og opptelling. Produktbekreftelse velges automatisk. Lar deg bekrefte hver del av beholdningen fra den mobile enheten. |
|  Maksimalt antall enheter  |                   Tilgjengelig for plukkarbeid hvis stykkplukkingsbekreftelse er aktivert. Angir en grense for hvor mange enheter som du må bekrefte.                   |


