---
title: Postere periodiske journaler
description: Periodiske journaler kalles noen ganger gjentakelsesjournaler fordi beløpet, teksten og annen informasjon gjentas hver gang den periodiske journalen hentes.
author: aprilolson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 241023c36723fa2dba5646e997b649741142c0ad
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834956"
---
# <a name="post-periodic-journals"></a>Postere periodiske journaler

[!include [task guide banner](../../includes/task-guide-banner.md)]

Periodiske journaler kalles noen ganger gjentakelsesjournaler fordi beløpet, teksten og annen informasjon gjentas hver gang den periodiske journalen hentes. Når du oppretter den periodiske journalen, angir du tidsintervallet for gjentakelse, for eksempel dager eller måneder. Denne oppgaveveiledningen oppretter en periodisk journal med månedlig gjentakelse.



1. Gå til Økonomimodul > Periodiske oppgaver > Periodiske journaler.
2. Klikk Ny.
3. Angi eller velg en verdi i Navn-feltet.
4. Klikk koblingen i den valgte raden i listen.
5. Skriv inn en verdi i feltet Beskrivelse.
    * Beskrivelsen vil være navnet på den periodiske journalen når du senere henter den, så pass på å gi den et relevant navn.  
6. Klikk Linjer.
    * En periodisk journal inneholder vanligvis flere journallinjer. Denne oppgaveveiledningen legger imidlertid bare til én linje.  
7. Angi en dato i Dato-feltet.
    * Dato-feltet inneholder posteringsdatoen for neste overføring til den daglige journalen. For journaler som hentes hver måned, anbefales det å bruke datoen i måneden når det skal posteres, vanligvis første eller siste datoen i perioden. Det er mulig å la Dato-feltet stå tomt og gi en dato når journalen hentes, ved hjelp av det tomme Dato-feltet.    Feltet oppdateres automatisk til neste gjentakende dato når transaksjoner hentes.  
8. Angi de ønskede verdiene i Konto-feltet.
9. Skriv inn en verdi i feltet Beskrivelse.
10. Lukk siden.
11. Angi et tall i Debet-feltet.
12. Angi ønskede verdier i Motkonto-feltet.
13. Velg Måneder i Enhet-feltet.
14. Angi 1 i feltet Antall enheter.
15. Angi en dato i Siste dato-feltet.
    * Hvis du angir den siste datoen i den forrige perioden, hindrer du at den gjentakende journalen ved en feil blir opprettet i feil startperiode. Siste dato oppdateres senere hver gang den periodiske journalen hentes.  
16. Klikk Lagre.
17. Gå til standard instrumentbord.
18. Gå til Økonomimodul > Journaloppføringer > Økonomijournaler.
19. Klikk Ny.
20. Angi eller velg en verdi i Navn-feltet.
21. Finn og velg ønsket post i listen.
22. Klikk koblingen i den valgte raden i listen.
23. Skriv inn en verdi i feltet Beskrivelse.
24. Klikk Linjer.
25. Klikk Periodisk journal.
26. Klikk Hent journal.
27. Angi en dato i Til dato-feltet.
    * Til-datoen fungerer som fristen for de periodiske bilagslinjene. Basert på innstillingen for regelmessighet kan den siste datoen og til-datoen på den samme linjen inkluderes mer enn én gang i den resulterende journalen. Til-datoen oppdateres automatisk basert på øktdatoen for siste gang den periodiske linjen ble overført til en journal.  
28. Angi eller velg en verdi i feltet Nummer på periodisk journal.
29. Klikk koblingen i den valgte raden i listen.
30. Klikk OK.
    * Den periodiske journalen kan nå gjennomgås, godkjennes eller posteres avhengig av behov og oppsett.  

