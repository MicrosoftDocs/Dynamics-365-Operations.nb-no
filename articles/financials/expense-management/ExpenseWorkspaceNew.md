---
title: Ny utforming av reiseregninger
description: Dette emnet gir informasjon om den nye utformingen av og opplevelsen for reiseregningregistrering i Microsoft Dynamics 365 for Finance and Operations. Den nye opplevelsen forenkler prosessen med å fullføre reiseregninger og reduserer tiden som kreves.
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: ryansand
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: 320984fc6be231c941df17abb7246e92f6aa4b9a
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1841063"
---
# <a name="expense-reports-reimagined"></a>Ny utforming av reiseregninger

[!include[banner](../includes/banner.md)]

Registrering av reiseregninger er endret for å forenkle prosessen med å fullføre reiseregninger og redusere tiden som kreves. Her er hovedkomponentene i den nye opplevelsen:

- Et nytt reiseregningsarbeidsområde som gir deg tilgang til representantens utgifter.
- En ny kvitteringskontrollfunksjon som viser kvitteringer på hodenivå på en bedre måte, og forenkler prosessen med å legge ved kvitteringer i utgiftslinjer.
- Et nytt skrivebeskyttet rutenett som lar deg vise mange flere utgiftslinjer og flere kolonner med data. Nå kan du se alle spesifiserte og delte linjer, sammen med de overordnede utgiftene.
- En forenklet rute for redigering av utgifter.
- Endrede feilmeldinger, varsler og policy-meldinger som sikrer at du har riktig kontekst for å forstå hva problemet er, og hvordan du løser det. Microsoft har fjernet mange meldinger som ble vist før brukere hadde mulighet til å fullføre oppgavene sine og løse problemene, for eksempel meldingen om ikke fullført spesifisering.
- En ny side for å angi hvilke felt som kreves av organisasjonen, hvilke felt som er valgfrie, og hvilke felt som ikke skal registreres. Denne siden vil redusere antall felt som brukerne må angi.
- Et nytt utseende og ny funksjonalitet for reiseregninger, slik at rapportene ikke lenger ser ut som de er utformet for regnskapsmedarbeidere.

Hvis du vil aktivere den nye opplevelsen, bruker du arbeidsområdet **Funksjonsbehandling** til å aktivere funksjonen **Ny utforming av reiseregninger**. Når du aktiverer denne funksjonen, skjer følgende handlinger:

- Det eksisterende utgiftsarbeidsområdet erstattes med det nye arbeidsområdet.
- Det legges til et nytt menyelement for synlighet av reiseregningsfelt.
- Ingen eksisterende menyelementer for reiseregninger (den eksisterende siden) eller reiseregningsfelt fjernes.
- Arbeidsflyter og alle godkjenninger fører deg fortsatt til den eksisterende reiseregningssiden.

## <a name="getting-started-video-for-new-users"></a>Video for å komme i gang for nye brukere

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

Videoen [Utgiftsopplevelse i Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) (vises over) er inkludert i [Finance and Operations-spillelisten](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) som er tilgjengelig på YouTube.

## <a name="new-features"></a>Nye funksjoner

| Ny funksjon | Beskrivelse |
|---|----|
| Synlighet av reiseregningsfelt | En ny konfigurasjonsside lar deg angi hvilke felt som skal deaktiveres for en organisasjon, hvilke felt som skal være obligatoriske, og hvilke felt som anbefales. |
| Obligatorisk felt | Ved hjelp av ny enkel konfigurasjon kan du gjøre noen felt obligatoriske uten å måtte bruke policyrammeverket. |
| Valgfrie felt | Det blir lagt til en ny side for valgfrie felt. På denne måten vil ikke ansatte føle at de må angi feltene, men feltene er likevel lett tilgjengelige. |
| Legge til ikke-tilknyttede kvitteringer | Muligheten for å legge til ikke-tilknyttede kvitteringer i reiseregninger er mer synlig fra arbeidsområdet og i reiseregningen. |
| Forbedret meldingssystem | Det er bedre innsyn i utgiftslinjer som har advarsler eller feil. |
| Reduksjon i meldinger på meldingslinjen| Antallet Infologg-meldinger er redusert, og det er gjort en innsats for å forhindre at dupliserte meldinger vises i mange tilfeller. |
| Gruppert sammen vanlige handlinger | Det er ryddet opp i grensesnittet med tillegget av en ny handlingsknapp for de mest vanlige linjenivåhandlingene og tillegget av en ellipse-knapp (...) for hodet, samt andre handlinger som ikke forekommer så ofte. |
| Nytt arbeidsområde for å øke synligheten | Et nytt arbeidsområde forener funksjoner og koblinger som lar brukere gå til forskjellige områder. |
| Legge til eksisterende utgifter og kvitteringer under utgiftsopprettingen | Når du oppretter reiseregninger, kan du legge til alle eller utvalgte utgifter og kvitteringer. |
| Valutakursberegner | Det blir lagt til en valutakursberegner der du kan beregne valutakursen for utlegg av transaksjoner med flere valutaer. |
| Lagre og legge til nye utgiftslinjer | **Lagre**- og **Ny**-knappene er tilgjengelige når nye utgifter angis, slik at du raskt kan registrere utgiftslinjer. |
| Bedre innsyn i splittede og spesifiserte linjer | Spesifiserte og delte linjer blir lagt til direkte i listen over utgifter, for å øke synligheten og hjelpe deg med å fastslå om det finnes policyfeil eller andre feil. |
| Vise kvitteringer under spesifisering | Kvitteringer kan vises under spesifisering. |

Den første versjonen fokuserer på scenarier med reiseregningregistrering. Alle scenarier for gjennomgang eller godkjenning av reiseregninger vil fortsette å bruke den eksisterende siden for reiseregningregistrering.

Følgende funksjoner finnes på den eksisterende siden, men finnes ikke ennå på den nye siden. Disse funksjonene vil bli introdusert igjen i flere kommende versjoner:

- Godkjenninger
- Godkjenninger i leverandører og muligheten til å redigere regnskapet
- Flere registreringspunkt
- Integrering av reiserekvisisjoner
- Dataenhet for innsyn i utgiftsfelt
- Post for kostgodtgjørelseutgifter
- Arbeidsflyt på linjenivå
- Støtte for midlertidige godkjennere
- Avansert spesifisering
