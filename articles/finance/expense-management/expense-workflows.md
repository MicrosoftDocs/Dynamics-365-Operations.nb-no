---
title: Konfigurere arbeidsflyter for reiseregning og utlegg
description: Du kan sette opp en arbeidsflytprosess som brukes for å gjennomgå og godkjenne reise- og utleggsbilag.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cdd4d69cb86da12e4a265f89c021c238d00cad08
ms.sourcegitcommit: de5af1912201dd70aa85fdcad0b184c42405802e
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/21/2020
ms.locfileid: "3154000"
---
# <a name="set-up-workflows-for-expense-management"></a>Konfigurere arbeidsflyter for reiseregning og utlegg

[!include [banner](../includes/banner.md)]

Du kan sette opp en arbeidsflytprosess som brukes for å gjennomgå og godkjenne reise- og utleggsbilag. Dokumentene som arbeidsflyter kan defineres inkluderer kostnadsrapporter, reiserekvisisjoner og forespørsler om kontantforskudd.

En arbeidsflyt representerer en forretningsprosess. Den definerer hvordan et dokument går gjennom systemet, og angir hvem som må utføre en oppgave eller godkjenne et dokument. Det er flere fordeler ved å bruke arbeidsflytsystemet i en organisasjon:

-   **Konsekvente prosesser** – Du kan definere godkjenningsprosessen for bestemte dokumenter, for eksempel innkjøpsrekvisisjoner og reiseregningsrapporter. Ved hjelp av arbeidsflytsystemet kan du sikre at dokumenter behandles og godkjennes på en konsekvent og effektiv måte.

-   Prosessynlighet – Du kan spore status, logg og ytelsesstatistikk for en bestemt arbeidsflytforekomst. Dette gjør at du kan finne ut om det må gjøres endringer i arbeidsflyten for å forbedre effektiviteten.

-   Sentralisert arbeidsliste – Brukere kan vise en sentralisert arbeidsliste for å vise arbeidsflytoppgavene og -godkjenningene som er tilordnet dem. 

**Arbeidsflyttypene som du kan opprette**

Følgende tabell viser hvilke typer arbeidsflyter du kan opprette i **Utgifter**.


|              <strong>Type</strong>              |                   <strong>Bruk denne typen til å gjøre følgende:</strong>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <strong>Utgiftsrapport</strong>         |            Opprett arbeidsflyter for utgiftsrapporter.             |
|  <strong>Poster utgiftsrapport automatisk</strong>   |        Opprett automatiske posteringsflyter for utgiftsrapporter.        |
|       <strong>Utgiftslinjeelement</strong>        |     Opprett arbeidsflyter for godkjenning av linjeposter på utgiftsrapporter.      |
| <strong>Poster utgiftslinjevare automatisk</strong> | Opprett automatiske posteringsflyter for linjeposter på kostnadsrapporter. |
|       <strong>Reiserekvisisjon</strong>       |          Opprett arbeidsflyter for godkjenning av reiserekvisisjoner.           |
|      <strong>Forskuddsforespørsel</strong>      |         Opprett arbeidsflyter for godkjenning av forespørsler om kontantforskudd.          |
|        <strong>Mva-fradrag</strong>        | Opprett arbeidsflyter for godkjenning av tilbakebetaling av merverdiavgift (mva).  |

