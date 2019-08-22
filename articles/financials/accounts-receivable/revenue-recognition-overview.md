---
title: Oversikt over inntektsføring
description: Dette emnet inneholder informasjon om funksjonen Inntektsføring. Funksjonen gir en fleksibel ramme som lar deg definere firmaspesifikke regler for å gjenkjenne både inntektsprisen og inntektsplanen for ordrer med flere elementer.
author: kweekley
manager: aolson
ms.date: 08/24/2018
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
ms.openlocfilehash: d52a9c7315cccf668a8b9bcf7ba5cad7039e186e
ms.sourcegitcommit: 299e20b59ebefa584ed46a13da3f1a7ff709e43c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2019
ms.locfileid: "1863569"
---
# <a name="revenue-recognition-overview"></a>Oversikt over inntektsføring

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

> [!NOTE]
> Funksjonen Inntektsføring kan ikke aktiveres via Funksjonsbehandling ennå. For øyeblikket må du bruke konfigurasjonsnøkler for å aktivere den.

Firmaer i bransjer som selger flere varer, for eksempel produkter, tjenester, abonnementer og så videre, må kunne dele opp ordrer med flere elementer, slik at inntekten kan gjenkjennes på grunnlag av et sett med firmaspesifikke og bransjespesifikke retningslinjer.

Generelt kan inntektsføringsprosessen brukes til å utføre følgende oppgaver:

* Tildele inntekt for å sikre at den relevante inntektsprisen gjenkjennes på grunnlag av verdien til komponentene i ordrer med flere elementer.
* Utsette inntekt basert på en inntektsplan som representerer den kontraktsmessige tidsrammen og prosentandelene for inntektsføring over tid.

Funksjonen Inntektsføring gir en fleksibel ramme som lar deg definere firmaspesifikke regler for å gjenkjenne både inntektsprisen og inntektsplanen.

Frigitte produkter brukes til å støtte inntektsføring på salgsordredokumenter. De frigitte produktene inneholder oppsettet som kreves for å bestemme inntektsprisen og inntektsplanen. Salgsordren kan stamme fra et Etter regning-prosjekt.

Firmaer kan bruke funksjonen for inntektsplan uten å bruke funksjonen for inntektspris. Derfor brukes prisen på salgsordrelinjene som enten inntekt eller utsatt inntekt. Hvis det finnes en inntektsplan på salgsordrelinjen, utsettes prisen på salgsordrelinjen. Hvis det ikke finnes en inntektsplan på salgsordrelinjen, posteres prisen på salgsordrelinjen til en inntektskonto når den faktureres.

Inntektsprisen beregnes enten når salgsordren bekreftes eller når fakturaen posteres. Hvis du vil forhåndsvise inntektsprisen før fakturaen posteres, må du bekrefte salgsordren.

Når salgsordren bekreftes, opprettes det også en forventet inntektsplan hvis noen av salgsordrelinjene inneholder en inntektsplan. Når salgsordren faktureres, slettes den forventede inntektsplanen, og den forventede inntektsplanen erstattes med den faktiske inntektsføringsplanen.

Detaljene for inntektsføringsplanen opprettholdes for hver salgsordrelinje. Den inntektsføringsansvarlige kan vise detaljene og frigi linjer til inntekt når kontraktsforpliktelsen er fullført. På slutten av hver periode kan inntektsføringsansvarlig opprette en inntektsjournal for å frigi eventuelle planleggingslinjer som forfaller på eller før en dato som han eller hun definerer. Denne inntektsjournalen posteres ikke umiddelbart. Derfor kan inntektsføringsansvarlig kontrollere at de riktige beløpene frigis fra utsatt inntekt til faktisk inntekt.

Hvis en kontraktsmessig endring fører til at en ny salgsordrelinje legges til enten i den eksisterende salgsordren eller i en ny salgsordre, kan en omfordelingsprosess kjøres for å korrigere inntektsprisen på tvers av alle linjene i salgsordrene.