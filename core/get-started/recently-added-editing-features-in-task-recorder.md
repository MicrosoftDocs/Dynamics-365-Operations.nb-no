---
title: Nylig lagt til redigeringsfunksjonene i Oppgaveregistrering
description: "Hvis du bruker Oppgaveregistrering for å opprette hjelpelinjer for aktiviteten, kan du redigere filer mer effektivt ved å bruke funksjonene som er beskrevet i denne wikien."
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.reviewer: annbe
ms.search.scope: Core
ms.custom: 266464
ms.assetid: b4640e67-4b92-4855-8041-1bfc71aadc47
ms.search.region: global
ms.author: josaw
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: c4f9ac515eab6ed8b194fc8985f6d3fae40ced38
ms.lasthandoff: 03/31/2017


---

# <a name="recently-added-editing-features-in-task-recorder"></a>Nylig lagt til redigeringsfunksjonene i Oppgaveregistrering

Hvis du bruker Oppgaveregistrering for å opprette hjelpelinjer for aktiviteten, kan du redigere filer mer effektivt ved å bruke funksjonene som er beskrevet i denne wikien.

Disse funksjonene er tilgjengelige på den **innstillinger &gt;Oppgaveregistrering &gt;Rediger innspillingen** menyen.

-   Sette inn trinnene uten nyinnspillingen hele filen.
-   Flytte trinnene under en delaktivitet uten nyinnspillingen hele filen.
-   Skjul registrering av navn og Beskrivelse-feltene.

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Sette inn trinnene uten rerecording hele filen
Du kan nå legge et trinn hvor som helst i en aktivitet-guide uten å spille eller nyinnspillingen hele filen.

1.  Velg trinn etter som du vil bruke det nye trinnet skal settes inn. Kontroller at trinnet er uthevet.

Oppgaveregistrering å sette inn et trinn må, du ha den riktige siden åpne. Den riktige siden er siden som nytt trinn oppstår. Oppgaveregistrering har en mekanisme som bestemmer hva den aktive siden er, og vil deaktivere funksjonen hvis siden ikke er åpen. 

[![tg1](./media/tg1.png)](./media/tg1.png) 


Når du er på riktig side, **Sett inn trinn** blir tilgjengelig.

[![tg2](./media/tg2-231x300.png)](./media/tg2.png)

2. Klikk **Sett inn trinn**.

Når du klikker **Sett inn trinn**, Oppgaveregistrering bytter til opptaksmodus. Alle handlinger som utføres i Brukergrensesnittet vil nå bli registrert og lagt til på stedet som trinn.

3. Klikk **Stopp**.

Du kan gjenta prosessen, å legge til så mange delaktiviteter eller flytte så mange delaktiviteter etter behov (se nedenfor for delaktiviteter).

4. Når du er ferdig redigere TV-guiden for oppgaven, velger **gjort redigerer**, og velg deretter ett av følgende alternativer for å lagre eller publisere oppgaven TV-guiden.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Flytte trinnene under en delaktivitet uten rerecording hele filen
Du kan flytte trinnene under en delaktivitet uten å spille eller nyinnspillingen hele filen. Du kan også flytte delaktivitet-trinn eller slutten delaktivitet trinn hvis du vil gruppere en eksisterende blokk med trinnene.

1.  Velg trinn eller delaktivitet trinn som du vil flytte. Kontroller at trinnet er uthevet.
2.  En ellipse, og klikk deretter **Flytt trinn etter**.

[![tg3](./media/tg3.png)](./media/tg3.png)

3. Velg trinn eller delaktivitet trinn som du vil flytte trinn eller delaktivitet trinn etter. Oppgaveregistrering flyttes til trinn.

4. Flytt slutten delaktivitet trinn, merker du den, klikker du ellipse, klikker **Flytt trinn etter**, og velg deretter trinn etter som du vil til slutt delaktivitet trinn skal.

Hvis du vil at det første trinnet i oppgave-guide til å være innenfor en delaktivitet, opprette en delaktivitet trinn som det andre trinnet, og deretter flytte det første trinnet til den. Du kan legge til eller flytte så mange trinn eller delaktiviteter etter behov.

5. Når du er ferdig redigere TV-guiden for oppgaven, velger **gjort redigerer**, og velg deretter ett av følgende alternativer for å lagre eller publisere oppgaven TV-guiden.

## <a name="collapse-recording-name-and-description"></a>Skjul innspillingen navn og beskrivelse
Du kan utvide og skjule den **innspillingen navnet** og **registrere beskrivelse** felt. Når disse feltene er skjult, blir synlige i Oppgaveregistrering redigering ruten flere trinn. 

[![tg4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Se også
--------

[Lage dokumentasjon eller opplæring ved hjelp av oppgaveopptak](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Hurtigreferanse for registrering av aktivitet](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)


