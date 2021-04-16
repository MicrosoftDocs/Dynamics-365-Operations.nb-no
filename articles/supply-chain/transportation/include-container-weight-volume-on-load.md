---
title: Inkludere containervekt og -volum for last
description: Dette emnet beskriver hvordan sette opp og bruke funksjonalitet for å inkludere containervekt og -volum for last.
author: pjacobse
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8d747d2cdafeedf77b8b2df1cbc8debdc0675729
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5824058"
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