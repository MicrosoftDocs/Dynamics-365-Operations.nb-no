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
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: c5340f4dacd743600ef955c8d5228d1e2d2d2fa9
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017


---

# Stykkplukkingsbekreftelse
<a id="piece-picking-confirmation" class="xliff"></a>

[!include[banner](../includes/banner.md)]

Med stykkplukking kan du bekrefte hver del av lagerbeholdningen gjennom plukkings- og tellingsarbeid på en mobil enhet. For plukking kan du kontrollere hvor mye arbeid som skal behandles opptil antallet som er angitt på arbeid som skal plukkes. For opptellingsarbeid kan du skanne lageret du teller opp, og spore totalbeløpet.

Når du aktiverer stykkplukking, velges produktbekreftelse automatisk. For arbeidstypen plukk aktiveres et maksimalt antall stykker. Dette gjør at du kan angi et maksimalt antall enheter som må bekreftes under arbeidsprosessen. Maksimalt antall er basert på den gjeldende arbeidsenheten som behandles. Opptellingsarbeidstypen tillater ikke et maksimum.

Du kan også bruke antall og måleenhet som er tilknyttet en skannet strekkode. Dette vil fungere for mottak på innkommende flyter inkludert mottak av kombinerte skiltnumre, bestillingsvare, overføringsordrevare og lastvare. Det fungerer også for stykkplukking der skanning av strekkoden vil legge til antallet i totalt antall bekreftede stykker som er konvertert mellom måleenheten på strekkoden og arbeidsenheten. Hvis det, ved telling av måleenheten på strekkoden, bekreftes at antallet er tillatt for opptelling på sekvensgruppen, legges antallet til totalantallet.

## Der det er aktuelt
<a id="where-it-applies" class="xliff"></a>

Stykkplukking fungerer for alt opptellingsarbeid og for første plukking for alle typer arbeid. Stykkplukking gjelder ikke hvis varen styres av serienumre eller hvis det er en produksjons- eller kanbanplukking fra en nummerskiltlokasjon og varen er satt til oppsamling.

## Definer stykkplukking
<a id="set-up-piece-picking" class="xliff"></a>

1.  Åpne oppsettskjemaet for arbeidsbekreftelse på et menyelement for mobilenhet: Lagerstyring > **Lagerstyring** > **Oppsett** > **Mobilenhet** > **Menyelementer på mobilenheten**. 
2. Åpne Arbeidsbekreftelsesoppsett fra menyelement for mobilenhet.

Følgende alternativer blir tilgjengelige når arbeidstypen er plukking og opptelling.

| Alternativ        | beskrivelse   | 
| ------------- | ------------- |
| Stykkplukkingsbekreftelse   | Tilgjengelig for arbeidstypene plukking og opptelling. Produktbekreftelse velges automatisk. Lar deg bekrefte hver del av beholdningen fra den mobile enheten. | 
| Maksimalt antall enheter     | Tilgjengelig for plukkarbeid hvis stykkplukkingsbekreftelse er aktivert. Angir en grense for hvor mange enheter som du må bekrefte. |  

