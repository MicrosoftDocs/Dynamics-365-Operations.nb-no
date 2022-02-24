---
title: Oversikt over inntektsføring
description: Dette emnet inneholder informasjon om funksjonen Inntektsføring. Funksjonen gir en fleksibel ramme som lar deg definere firmaspesifikke regler for å gjenkjenne både inntektsprisen og inntektsplanen for ordrer med flere elementer.
author: kweekley
manager: aolson
ms.date: 11/11/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: Customer
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 92af567499c1a8a23cd4d51e5bab48eaab2d8422
ms.sourcegitcommit: e544c51a68ad5daf748c0e877bdbde094ad40bd2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/03/2020
ms.locfileid: "4459668"
---
# <a name="revenue-recognition-overview"></a>Oversikt over inntektsføring

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Funksjonen Inntektsføring kan ikke aktiveres via Funksjonsbehandling. For øyeblikket må du bruke konfigurasjonsnøkler for å aktivere den.

Firmaer i bransjer som selger flere varer, for eksempel produkter, tjenester, abonnementer og så videre, må kunne dele opp ordrer med flere elementer, slik at inntekten kan gjenkjennes på grunnlag av et sett med firmaspesifikke og bransjespesifikke retningslinjer.

Generelt kan inntektsføringsprosessen brukes til å utføre følgende oppgaver:

* Tildele inntekt for å sikre at den relevante inntektsprisen føres på grunnlag av verdien til komponentene i ordrer med flere elementer.
* Utsette inntekt basert på en inntektsplan som representerer den kontraktsmessige tidsrammen og prosentandelene for inntektsføring over tid.

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE44iER]

Videoen [How to use revenue recognition in Dynamics 365 Finance](https://youtu.be/v3amIsiqvoo) (vises over) er inkludert i [spillelisten for Finance and Operations](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.

Funksjonen Inntektsføring gir en fleksibel ramme som lar deg definere firmaspesifikke regler for å gjenkjenne både inntektsprisen og inntektsplanen.

Frigitte produkter brukes til å støtte inntektsføring på salgsordredokumenter. De frigitte produktene inneholder oppsettet som kreves for å bestemme inntektsprisen og inntektsplanen. Salgsordren kan stamme fra et Etter regning-prosjekt.

Firmaer kan bruke funksjonen for inntektsplan uten å bruke funksjonen for inntektspris. Derfor brukes prisen på salgsordrelinjene som enten inntekt eller utsatt inntekt. Hvis det finnes en inntektsplan på salgsordrelinjen, utsettes prisen på salgsordrelinjen. Hvis det ikke finnes en inntektsplan på salgsordrelinjen, posteres prisen på salgsordrelinjen til en inntektskonto når den faktureres.

Inntektsprisen beregnes enten når salgsordren bekreftes eller når fakturaen posteres. Hvis du vil forhåndsvise inntektsprisen før fakturaen posteres, må du bekrefte salgsordren.

Når salgsordren bekreftes, opprettes det også en forventet inntektsplan hvis noen av salgsordrelinjene har en inntektsplan. Når salgsordren faktureres, slettes den forventede inntektsplanen, og den forventede inntektsplanen erstattes med den faktiske inntektsføringsplanen.

Detaljene for inntektsføringsplanen opprettholdes for hver salgsordrelinje. Den inntektsføringsansvarlige kan vise detaljene og frigi linjer til inntekt når kontraktsforpliktelsen er fullført. På slutten av hver periode kan inntektsføringsansvarlig opprette en inntektsjournal for å frigi eventuelle planleggingslinjer som forfaller på eller før en dato vedkommende definerer. Denne inntektsjournalen posteres ikke umiddelbart. Derfor kan inntektsføringsansvarlig kontrollere at de riktige beløpene frigis fra utsatt inntekt til faktisk inntekt.

Hvis en kontraktsmessig endring fører til at en ny salgsordrelinje legges til enten i den eksisterende salgsordren eller i en ny salgsordre, kan en prosess for ny tildeling kjøres for å korrigere inntektsprisen på tvers av alle linjene på salgsordrene.
