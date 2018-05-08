---
title: Arbeidsflythandlinger
description: "Denne artikkelen forklarer handlingene som hver deltaker i en godkjenningsprosess for arbeidsflyt kan utføre."
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 56411
ms.assetid: 65fb711c-6474-42d1-81ed-ca657c29bf1f
ms.search.region: Global
ms.author: tjvass
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 2a4717accfa7e5879ee757820c39f000fa7d3e95
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="workflow-actions"></a>Arbeidsflythandlinger

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer handlingene som hver deltaker i en godkjenningsprosess for arbeidsflyt kan utføre.

En arbeidsflyt kan omfatte flere grupper av personer: avsenderen, personer tilordnet oppgaver, beslutningstakere og godkjennere. I følgende arbeidsflyt for reiseregning nedenfor er Erik avsenderen, medlemmer av køen er personer som er tilordnet oppgaven, Jon er beslutningstaker, og Dag, Jorunn og Karen er godkjennerne.   

[![Arbeidsflyt\_WithManualDecision](./media/workflow_withmanualdecision.gif)](./media/workflow_withmanualdecision.gif) 

De følgende avsnittene forklarer arbeidsflythandlingene hver gruppe kan utføre.

## <a name="actions-that-an-originator-can-perform"></a>Handlinger en avsender kan utføre
Avsenderen starter en arbeidsflyt ved å sende et dokument til behandling. For eksempel må Erik klikke **Send** -knappen på siden **Reiseregning** for å sende reiseregningen.

## <a name="actions-that-a-task-assignee-can-perform"></a>Handlinger som en person tilordnet en oppgave, kan utføre
En oppgave kan tilordnes til flere personer eller til en arbeidselementkø som overvåkes av flere personer. Men bare én person kan fullføre oppgaven. For eksempel har Erik sendt en reiseregning, og har sendt sine kvitteringer til organisasjonens reiseregningsavdeling for gjennomgang. 

Medlemmene av avdelingen Adventure Works-reiseregninger overvåker køen. Julie, et medlem fra avdelingen, har godtatt oppgaven med å gå gjennom Eriks reiseregningen og kvitteringer. Hun kan nå utføre én av følgende handlinger: fullføre, avvise, delegere, be om endring, tilordne eller frigi. 

**Obs!** Handlingene som er tilgjengelige, vil variere avhengig av hvordan programvareutvikleren utformet oppgaven.

### <a name="complete"></a>Fullføre

Når en bruker fullfører en oppgave, tilordnes dokumentet som ble sendt til behandling, til den neste brukeren i arbeidsflyten hvis det finnes en neste bruker. Hvis det ikke kreves mer behandling, avsluttes arbeidsflytprosessen. 

Eksempelvis har Julie, et medlem fra avdelingen for Adventure Works-reiseregninger, godtatt oppgaven med å gå gjennom Eriks reiseregning og kvitteringer. Når Julie har fullført sin gjennomgang, tilordnes dokumentet Jon.

### <a name="reject"></a>Avslå

Når en bruker avviser et dokument, avsluttes arbeidsflytprosessen. 

Eksempelvis har Julie, et medlem fra avdelingen for Adventure Works-reiseregninger, godtatt oppgaven med å gå gjennom Eriks reiseregning og kvitteringer. Hvis Julie avviser reiseregningen, avsluttes arbeidsflytprosessen. 

Erik kan deretter sende reiseregningen på nytt. Han kan foreta endringer først, eller han kan sende originalversjonen på nytt. Hvis Erik sender reiseregningen på nytt, starter arbeidsflytprosessen fra den manuelle gjennomgangsoppgaven.

### <a name="delegate"></a>Representant

Når en bruker delegerer en oppgave, tilordnes den til en annen bruker. 

Eksempelvis har Julie, et medlem fra avdelingen for Adventure Works-reiseregninger, godtatt oppgaven med å gå gjennom Eriks reiseregning og kvitteringer. Julie delegerer oppgaven til Tim, som er hennes assistent. 

Tim opptrer deretter på vegne av Julie. Derfor, når Tim fullfører sin gjennomgang, tilordnes reiseregningen til Jon, akkurat som om Julie hadde fullført oppgaven.

### <a name="request-change"></a>Be om endring

Når en bruker ber om en endring i et dokument som ble sendt, sendes det tilbake til avsenderen. 

Eksempelvis har Julie, et medlem fra avdelingen for Adventure Works-reiseregninger, godtatt oppgaven med å gå gjennom Eriks reiseregning og kvitteringer. Julie legger merke til noen feil i reiseregningen og ber om endringer. Reiseregningen sendes tilbake til Erik. 

Erik kan deretter sende reiseregningen på nytt. Han kan foreta de forespurte endringene først, eller han kan sende originalversjonen på nytt. Hvis Erik sender reiseregningen på nytt, må et medlem av arbeidselementkøen kontrollere reiseregningen og kvitteringene på nytt.

### <a name="reassign"></a>Tilordne på nytt

Medlemmene av en arbeidselementkø kan tilordne dokumenter som er i køen, på nytt til en annen kø. 

For eksempel overvåker Julie, som er medlem av avdelingen Adventure Works-reiseregninger, køen. For å balansere arbeidsmengden hun kan tilordne reiseregningen på nytt, og kvitteringene som er inkludert i den, til en annen kø.

### <a name="release"></a>Frigi

Et medlem av en arbeidselementkø kan noen ganger godta en aktivitet, men deretter bestemmer deg for at han eller hun ikke kan fullføre oppgaven. I så fall kan personen som godtok oppgaven, frigi dokumentet tilbake til arbeidselementkøen. 

Eksempelvis har Julie, et medlem fra avdelingen for Adventure Works-reiseregninger, godtatt oppgaven med å gå gjennom Eriks reiseregning og kvitteringer. Hvis Julie bestemmer seg for at hun ikke kan fullføre oppgaven, kan hun frigi dokumentet. Reiseregningen returneres til køen slik at andre medlemmer av avdelingen Adventure Works-reiseregninger kan fullføre oppgaven.

## <a name="actions-that-a-decision-maker-can-perform"></a>Handlinger som en beslutningstaker kan utføre
Vanligvis tilordnes et dokument til en beslutningstaker fordi det er et spørsmål som må besvares av beslutningstaker. Svaret på spørsmålet er vanligvis **Ja** eller **Nei** eller **Sann** eller **Usann**. Hvis beslutningstakeren ikke velger et av disse valgene, kan han eller hun delegere beslutningen.

### <a name="choice-1-or-choice-2"></a>\[Valg 1\] eller \[Valg 2\]

En beslutningstaker må svare på spørsmål som er knyttet til dokumentet. Svaret på spørsmålet er vanligvis **Ja** eller **Nei** eller **Sann** eller **Usann**. Svaret som en beslutningstaker velger, bestemmer arbeidsflytgrenen som brukes til å behandle dokumentet. 

Eksempelvis tilordnes Eriks reiseregningen til Jon. Jon må bestemme om informasjonen i dokumentet krever et kall til Eriks sjef. Hvis Jon bestemmer seg for at det kreves en samtale, tilordnes reiseregningen til Anita, som deretter må ringe Eriks sjef. Hvis Jon bestemmer seg for at en samtale ikke er nødvendig, tilordnes reiseregningen til Dag for godkjenning.

### <a name="delegate"></a>Representant

Når en beslutningstaker delegerer en avgjørelse, tilordnes dokumentet til en annen bruker som må ta beslutningen. 

Eksempelvis tilordnes Eriks reiseregningen til Jon. Jon delegerer beslutningen til Maria, som er hans assistent. 

Maria opptrer deretter på vegne av Jon. Hvis Maria bestemmer seg for å ringe Sams sjef, tilordnes reiseregningen til Anita, som deretter må ringe Eriks sjef. Hvis Maria bestemmer seg for at en samtale ikke er nødvendig, tilordnes reiseregningen til Dag for godkjenning.

## <a name="actions-that-an-approver-can-perform"></a>Handlinger en godkjenner kan utføre
Når et dokument tilordnes en godkjenner, kan han eller hun utføre én av følgende handlinger: godkjenne, avvise, delegere eller be om endring.

### <a name="approve"></a>Godkjenne

Når en godkjenner godkjenner et dokument, tilordnes dokumentert den neste brukeren i arbeidsflyten, hvis det er en neste bruker. Hvis det ikke kreves mer behandling, avsluttes arbeidsflytprosessen. 

For eksempel har Erik sendt en reiseregning på NOK 6 000, og dette dokumentet er tilordnet Dag. Når Dag godkjenner dokumentet, tilordnes det til Jorunn for godkjenning. Når Jorunn har godkjent reiseregningen, avsluttes arbeidsflytprosessen.

### <a name="reject"></a>Avslå

Når en godkjenner avviser et dokument, avsluttes arbeidsflytprosessen. 

For eksempel har Erik sendt en reiseregning på NOK 12 000, og dette dokumentet er tilordnet Jorunn. Hvis Jorunn avviser reiseregningsrapporten, avsluttes arbeidsflytprosessen. 

Erik kan deretter sende reiseregningen på nytt. Han kan foreta endringer først, eller han kan sende originalversjonen av reiseregningen på nytt. Hvis Erik sender reiseregningen på nytt, starter arbeidsflytprosessen fra godkjenningprosessen.

### <a name="delegate"></a>Representant

Når en godkjenner delegerer et dokument, tilordnes det til en annen bruker for godkjenning. 

For eksempel har Erik sendt en reiseregning på NOK 12 000, og dette dokumentet er tilordnet Dag. Dag delegerer reiseregningsrapporten til Karen. 

Karen fungerer deretter på vegne av Dag. Dette betyr at når Karen godkjenner dokumentet, tilordnes det til Jorunn for godkjenning, som om Dag hadde godkjent det. Når Jorunn har godkjent dokumentet, sendes det til Karen for godkjenning.

### <a name="request-change"></a>Be om endring

Når en godkjenner ber om en endring i et dokument, sendes det tilbake til avsenderen. 

For eksempel har Erik sendt en reiseregning på NOK 12 000, og dette dokumentet er tilordnet Jorunn. Hvis Jorunn ber om en endring, sendes reiseregningsrapporten tilbake til Erik. 

Erik kan deretter sende reiseregningen på nytt. Han kan foreta de forespurte endringer først, eller han kan sende originalversjonen av reiseregningen på nytt. Hvis Erik sender reiseregningsrapporten på nytt, sendes den til Dag for godkjenning, fordi han er den første godkjenneren i godkjenningsprosessen.




