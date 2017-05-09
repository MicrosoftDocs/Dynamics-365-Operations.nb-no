---
title: "Nylig tilføyde redigeringsfunksjoner i oppgaveopptaker"
description: "Hvis du bruker oppgaveopptaker til å opprette oppgaveveiledninger, kan du redigere filer mer effektivt ved å bruke funksjonene som er beskrevet i denne wikien."
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

# <a name="recently-added-editing-features-in-task-recorder"></a>Nylig tilføyde redigeringsfunksjoner i oppgaveopptaker

Hvis du bruker oppgaveopptaker til å opprette oppgaveveiledninger, kan du redigere filer mer effektivt ved å bruke funksjonene som er beskrevet i denne wikien.

Disse funksjonene er tilgjengelige på menyen **Innstillinger &gt; Oppgaveopptaker &gt; Rediger opptak**.

-   Sette inn trinnene uten å spille inn hele filen på nytt.
-   Flytte trinnene under en underoppgave uten å spille inn hele filen på nytt.
-   Skjul feltene Navn på opptak og Beskrivelse

## <a name="insert-steps-without-rerecording-the-entire-file"></a>Sette inn trinnene uten å spille inn hele filen på nytt
Du kan nå legge til et trinn hvor som helst i en oppgaveveiledning uten å spille av eller spille inn hele filen på nytt.

1.  Velg trinnet du vil legge til et nytt trinn etter. Kontroller at trinnet er uthevet.

For at oppgaveopptakeren skal sette inn et trinn må du ha den riktige siden åpen. Den riktige siden er siden det nye trinnet skal utføres på. Oppgaveopptakeren har en mekanisme som bestemmer hvilken side som er aktiv, og den vil deaktivere funksjonen hvis siden ikke er åpen. 

[![Mål1](./media/tg1.png)](./media/tg1.png) 


Når du er på riktig side, blir **Sett inn trinn** tilgjengelig.

[![Mål2](./media/tg2-231x300.png)](./media/tg2.png)

2. Klikk på **Sett inn trinn**.

Når du klikker på **Sett inn trinn**, bytter Oppgaveopptaker bytter til opptaksmodus. Alle handlinger som utføres i brukergrensesnittet vil nå bli registrert og lagt til på stedet som trinn.

3. Klikk på **Stopp**.

Du kan gjenta prosessen, legge trinn eller underoppgaver etter behov (se nedenfor for underoppgaver).

4. Når du er ferdig med å redigere oppgaveveiledningen, klikker du på **Redigeringen er fullført** og velger deretter ett av alternativene for å lagre eller publisere oppgaveveiledningen.

## <a name="move-steps-under-a-subtask-without-rerecording-the-entire-file"></a>Flytte trinnene under en underoppgave uten å spille inn hele filen på nytt
Du kan flytte trinnene under en underoppgave uten å spille av eller spille inn hele filen på nytt. Du kan også flytte underoppgavetrinnet eller det siste underoppgavetrinnet hvis du vil gruppere en eksisterende blokk med trinn.

1.  Velg trinnet eller underoppgavetrinnet du vil flytte. Kontroller at trinnet er uthevet.
2.  Klikk på ellipsen, og klikk deretter på **Flytt trinn etter**.

[![Mål3](./media/tg3.png)](./media/tg3.png)

3. Velg trinnet eller underoppgavetrinnet som du vil flytte trinnet eller underoppgavetrinnet etter. Oppgaveopptakeren flytter trinnet.

4. Hvis du vil flytte det siste underoppgavetrinnet, klikker du på ellipsen, klikker på **Flytt trinn etter** og velger deretter trinnet som du vil til at det siste underoppgavetrinnet skal plasseres etter.

Hvis du vil at det første trinnet i oppgaveveiledningen skal være innenfor en underoppgave, oppretter du et underoppgavetrinn som det andre trinnet, og flytter deretter det første trinnet til det. Du kan legge til eller flytte trinn eller underoppgaver etter behov.

5. Når du er ferdig med å redigere oppgaveveiledningen, klikker du på **Redigeringen er fullført** og velger deretter ett av alternativene for å lagre eller publisere oppgaveveiledningen.

## <a name="collapse-recording-name-and-description"></a>Skjule navn på opptak og beskrivelse
Du kan vise og skjule feltene **Navn på opptak** og **Beskrivelse av opptak**. Når disse feltene er skjult, vil flere trinn vises i redigeringsruten for Oppgaveopptaker. 

[![Mål4](./media/tg4-300x252.png)](./media/tg4.png)  

<a name="see-also"></a>Se også
--------

[Lage dokumentasjon eller opplæring ved hjelp av oppgaveopptak](/dynamics365/operations/dev-itpro/user-interface/task-recorder)

[Hurtigreferanse for oppgaveopptaker](/dynamics365/operations/dev-itpro/user-interface/task-recorder-quick-reference)


