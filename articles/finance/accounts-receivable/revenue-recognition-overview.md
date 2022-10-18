---
title: Oversikt over inntektsføring (inneholder video)
description: Denne artikkelen inneholder informasjon om funksjonen Inntektsføring. Funksjonen gir en fleksibel ramme som lar deg definere firmaspesifikke regler for å gjenkjenne både inntektsprisen og inntektsplanen for ordrer med flere elementer.
author: bking
ms.date: 03/15/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: bking
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 5bf07356b5613f438034f8dabac7db197e69a6c8
ms.sourcegitcommit: c5f2cba3c2b0758e536eeaaa40506659a53085e1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/12/2022
ms.locfileid: "9644037"
---
# <a name="revenue-recognition-overview"></a>Oversikt over inntektsføring

[!include [banner](../includes/banner.md)]

>[!NOTE]
>Denne funksjonaliteten blir avskrevet i oktober 2023, og nye brukere må bruke abonnementsfakturering.

Firmaer i bransjer som selger flere varer, for eksempel produkter, tjenester, abonnementer og så videre, må kunne dele opp ordrer med flere elementer, slik at inntekten kan gjenkjennes på grunnlag av et sett med firmaspesifikke og bransjespesifikke retningslinjer.

Inntektsføring, inkludert buntfunksjonalitet, innhold som ikke støttes for bruk i Commerce-kanaler (e-handel, salgssted, telefonsenter). Varer som konfigureres med inntektsføring, bør ikke legges til i ordrer eller transaksjoner som er opprettet i Commerce-kanaler.

Generelt kan inntektsføringsprosessen brukes til å utføre følgende oppgaver:

* Tildele inntekt for å sørge for at den relevante inntektsprisen føres på grunnlag av verdien til komponentene i ordrer med flere elementer.
* Utsette inntekt basert på en inntektsplan som representerer den kontraktsmessige tidsrammen og prosentandelene for inntektsføring over tid.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

Videoen [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (vises ovenfor) er inkludert i [spillelisten for Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), som er tilgjengelig på YouTube.

Funksjonen Inntektsføring gir en fleksibel ramme som lar deg definere firmaspesifikke regler for å gjenkjenne både inntektsprisen og inntektsplanen.

Frigitte produkter brukes til å støtte inntektsføring på salgsordredokumenter. De frigitte produktene inneholder oppsettet som kreves for å bestemme inntektsprisen og inntektsplanen. Salgsordren kan stamme fra et Etter regning-prosjekt.

Firmaer kan bruke funksjonen for inntektsplan uten å bruke funksjonen for inntektspris. Derfor brukes prisen på salgsordrelinjene som enten inntekt eller utsatt inntekt. Hvis det finnes en inntektsplan på salgsordrelinjen, utsettes prisen på salgsordrelinjen. Hvis det ikke finnes en inntektsplan på salgsordrelinjen, posteres prisen på salgsordrelinjen til en inntektskonto når den faktureres.

Inntektsprisen beregnes enten når salgsordren bekreftes eller når fakturaen posteres. Hvis du vil forhåndsvise inntektsprisen før fakturaen posteres, må du bekrefte salgsordren.

Når salgsordren bekreftes, opprettes det også en forventet inntektsplan hvis noen av salgsordrelinjene har en inntektsplan. Når salgsordren faktureres, slettes den forventede inntektsplanen, og den forventede inntektsplanen erstattes med den faktiske inntektsføringsplanen.

Detaljene for inntektsføringsplanen opprettholdes for hver salgsordrelinje. Den inntektsføringsansvarlige kan vise detaljene og frigi linjer til inntekt når kontraktsforpliktelsen er fullført. På slutten av hver periode kan inntektsføringsansvarlig opprette en inntektsjournal for å frigi eventuelle planleggingslinjer som forfaller på eller før en dato vedkommende definerer. Denne inntektsjournalen posteres ikke umiddelbart. Derfor kan inntektsføringsansvarlig kontrollere at de riktige beløpene frigis fra utsatt inntekt til faktisk inntekt.

Hvis en kontraktsmessig endring fører til at en ny salgsordrelinje legges til enten i den eksisterende salgsordren eller i en ny salgsordre, kan en prosess for ny tildeling kjøres for å korrigere inntektsprisen på tvers av alle linjene på salgsordrene.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

