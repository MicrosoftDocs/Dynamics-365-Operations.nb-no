---
title: Inkludere containervekt og -volum for last
description: Dette emnet beskriver hvordan sette opp og bruke funksjonalitet for å inkludere containervekt og -volum for last.
author: Henrikan
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: henrikan
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 52b42bd0b97564a493a50331d1424ca8084b389b29518f012f443d9cf722efe7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6763921"
---
# <a name="include-container-weight-and-volume-on-load"></a>Inkludere containervekt og -volum for last

[!include [banner](../includes/banner.md)]

Funksjonaliteten for å inkludere containerverk- og volum for en last gir en klar fremstilling av totalvekt og volum av beholdere og gjenstander som går på en last.

En last inneholder en enkelt forsendelse eller flere forsendelser, og disse forsendelsene inneholder forskjellige elementer som tilhører en enkelt salgsordre eller flere salgsordrer. Varene er lagret i en container, og containere lastes på en last. Elementer som er utenfor en container kan også være en del av en last. Basert på disse forholdene, beregner systemet verdier for vekt og volum på lasten ved å vurdere vekten og volumet av både beholdere og gjenstander.

Hvis de beregnede verdiene ikke er presise, kan du justere dem ved å angi de faktiske verdiene for vekt og volum på lasten. Verdiene for vekt og volum brukes i transportstyringsprosesser. For eksempel brukes verdiene i arbeidsbenken for rutesats, der de hjelper til med å definere hastigheten og ruten for last, og de brukes også til transportanbud og innsjekking av sjåføren.

## <a name="where-it-applies"></a>Der det er aktuelt

Funksjonaliteten for å inkludere containerens vekt og volum på en last gjelder i transporthåndteringsprosesser, som for eksempel arbeidsbenken for rutesats, transportanbud og innsjekking av sjåføren.

## <a name="how-it-is-set-up"></a>Hvordan det er satt opp

Antall containere som bør vurderes for en last, beregnes ut fra vekt og volum av containeren, og prosenten av containeren som brukes.

-   For å sette opp vekt og volum for en container, klikk **Lagerstyring** \> **Oppsett** \> **Containere** \> **Containertyper**.

-   For å angi containerutnyttelsesprosenten, klikk **Lagerstyring** \> **Oppsett** \> **Containere** \> **Containergrupper**, og skriv inn en verdi i feltet **Utnyttelsesprosent for container**.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]