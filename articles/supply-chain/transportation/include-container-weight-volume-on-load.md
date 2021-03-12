---
title: Inkludere containervekt og -volum for last
description: Dette emnet beskriver hvordan sette opp og bruke funksjonalitet for å inkludere containervekt og -volum for last.
author: pjacobse
manager: tfehr
ms.date: 05/26/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TMSRateRouteWorkbench, TMSDriverLogListPage, TMSTransportationTender
audience: Application User
ms.reviewer: kamaybac
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b8fb40a0fe1606b856f58f5bc517c7f1aff85e4d
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4977519"
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
