---
title: Stykkplukkingsbekreftelse
description: Med stykkplukking kan du bekrefte hver del av lagerbeholdningen gjennom plukkings- og tellingsarbeid på en mobil enhet.
author: Mirzaab
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSRFAutoConfirm, WHSRFMenuItem
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a925685b80c635cf036f19748e16d415953ed5fdda7b81498baeade35ccbfcab
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766008"
---
# <a name="piece-picking-confirmation"></a>Stykkplukkingsbekreftelse

[!include [banner](../includes/banner.md)]

Med stykkplukking kan du bekrefte hver del av lagerbeholdningen gjennom plukkings- og tellingsarbeid på en mobil enhet. For plukking kan du kontrollere hvor mye arbeid som skal behandles opptil antallet som er angitt på arbeid som skal plukkes. For opptellingsarbeid kan du skanne lageret du teller opp, og spore totalbeløpet.

Når du aktiverer stykkplukking, velges produktbekreftelse automatisk. For arbeidstypen plukk kan du angi et maksimalt antall stykker. Dette gjør at du kan angi et maksimalt antall enheter som må bekreftes under arbeidsprosessen. Maksimalt antall er basert på den gjeldende arbeidsenheten som behandles. Opptellingsarbeidstypen tillater ikke et maksimum.

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



[!INCLUDE[footer-include](../../includes/footer-banner.md)]