---
title: Inkludere containervekt og -volum for last
description: "Dette emnet beskriver hvordan sette opp og bruke funksjonalitet for å inkludere containervekt og -volum for last."
author: pjacobse
manager: AnnBe
ms.date: 05/26/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 269384
ms.search.region: Global
ms.author: pjacobse
ms.search.validFrom: 2017-09-20
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: b137db6f67da30d6ac3a973940c1df1fd7268a1a
ms.openlocfilehash: ac1df9b430feb025e4a544a7ecd7baa0c919cbe4
ms.contentlocale: nb-no
ms.lasthandoff: 10/02/2017

---

# <a name="include-container-weight-and-volume-on-load"></a>Inkludere containervekt og -volum for last

[!include[banner](../includes/banner.md)]

Funksjonaliteten for å inkludere containerverk- og volum for en last gir en klar fremstilling av totalvekt og volum av beholdere og gjenstander som går på en last.

En last inneholder en enkelt forsendelse eller flere forsendelser, og disse forsendelsene inneholder forskjellige elementer som tilhører en enkelt salgsordre eller flere salgsordrer. Varene er lagret i en container, og containere lastes på en last. Elementer som er utenfor en container kan også være en del av en last. Basert på disse forholdene, beregner systemet verdier for vekt og volum på lasten ved å vurdere vekten og volumet av både beholdere og gjenstander.

Hvis de beregnede verdiene ikke er presise, kan du justere dem ved å angi de faktiske verdiene for vekt og volum på lasten. Verdiene for vekt og volum brukes i transportstyringsprosesser. For eksempel brukes verdiene i arbeidsbenken for rutesats, der de hjelper til med å definere hastigheten og ruten for last, og de brukes også til transportanbud og innsjekking av sjåføren.

## <a name="where-it-applies"></a>Der det er aktuelt

Funksjonaliteten for å inkludere containerens vekt og volum på en last gjelder i transporthåndteringsprosesser, som for eksempel arbeidsbenken for rutesats, transportanbud og innsjekking av sjåføren.

## <a name="how-it-is-set-up"></a>Hvordan det er satt opp

Antall containere som bør vurderes for en last, beregnes ut fra vekt og volum av containeren, og prosenten av containeren som brukes.

-   For å sette opp vekt og volum for en container, klikk **Lagerstyring** \> **Oppsett** \> **Containere** \> **Containertyper**.

-   For å angi containerutnyttelsesprosenten, klikk **Lagerstyring** \> **Oppsett** \> **Containere** \> **Containergrupper**, og skriv inn en verdi i feltet **Utnyttelsesprosent for container**.
