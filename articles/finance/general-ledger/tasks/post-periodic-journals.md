---
title: Postere periodiske journaler
description: Periodiske journaler kalles noen ganger gjentakelsesjournaler fordi beløpet, teksten og annen informasjon gjentas hver gang den periodiske journalen hentes.
author: aprilolson
ms.date: 11/21/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdc1d9f67a515e3cdc45e173b88982feceb0ebfd
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799393"
---
# <a name="post-periodic-journals"></a>Postere periodiske journaler

[!include [banner](../../includes/banner.md)]

Periodiske journaler kalles noen ganger gjentakelsesjournaler fordi beløpet, teksten og annen informasjon gjentas hver gang den periodiske journalen hentes. Når du oppretter den periodiske journalen, angir du tidsintervallet for gjentakelse, for eksempel dager eller måneder. Denne oppgaveveiledningen oppretter en periodisk journal med månedlig gjentakelse.

1. Gå til **Navigasjonsrute > Moduler > Økonomimodul > Periodiske oppgaver > Periodiske journaler**.
2. Klikk på **Ny**.
3. Angi eller velg en verdi i **Navn**-feltet.
4. Klikk koblingen i den valgte raden i listen.
5. Skriv inn en verdi i **Beskrivelse**-feltet. Beskrivelsen vil være navnet på den periodiske journalen når du senere henter den, så pass på å gi den et relevant navn.
6. Klikk på **Linjer** i **handlingsruten**. En periodisk journal inneholder vanligvis flere journallinjer. Denne oppgaveveiledningen legger imidlertid bare til én linje.
7. Angi en dato i **Dato**-feltet. **Dato**-feltet inneholder posteringsdatoen for neste overføring til den daglige journalen. For journaler som hentes hver måned, anbefales det å bruke datoen i måneden når det skal posteres. Dette er vanligvis den første eller siste datoen i perioden. Ved å bruke feltet **Tom dato** er det mulig å la **Dato**-feltet stå tomt og gi en dato når journalen hentes. Feltet oppdateres til neste gjentakende dato når transaksjoner hentes. 
8. Angi de ønskede verdiene i **Konto**-feltet.
9. Velg en verdi i feltet **Beskrivelse**.
10. Lukk siden.
11. Angi et tall i **Debet**-feltet.
12. Angi ønskede verdier i **Motkonto**-feltet.
13. I **Enhet**-feltet velger du **Måneder**.
14. Angi **1** i feltet **Antall enheter**.
15. Angi en dato i **Siste dato**-feltet. Hvis du angir den siste datoen i den forrige perioden, hindrer du at den gjentakende journalen ved en feil blir opprettet i feil startperiode. Siste dato oppdateres senere hver gang den periodiske journalen hentes. 
16. Klikk **Lagre**.
17. Gå til **Navigasjonsrute > Moduler > Økonomimodul > Journaloppføringer > Økonomijournaler**.
18. Klikk på **Ny**.
19. Angi eller velg en verdi i **Navn**-feltet.
20. Finn og velg ønsket post i listen.
21. Klikk koblingen i den valgte raden i listen.
22. Skriv inn en verdi i **Beskrivelse**-feltet.
23. Klikk på **Linjer** i **handlingsruten**.
24. Klikk på **Periodisk journal** i **handlingsruten**.
25. Klikk på **Hent journal**.
26. Angi en dato i **Til dato**-feltet. **Til dato** fungerer som fristen for de periodiske bilagslinjene. Basert på innstillingen for regelmessighet kan **Siste dato** og **Til-dato** på den samme linjen inkluderes mer enn én gang i den resulterende journalen. **Til**-datoen oppdateres automatisk basert på øktdatoen for siste gang den periodiske linjen ble overført til en journal. 
27. Angi eller velg en verdi i feltet **Nummer på periodisk journal**.
28. Klikk koblingen i den valgte raden i listen.
29. Klikk **OK**. Den periodiske journalen kan nå gjennomgås, godkjennes eller posteres avhengig av behov og oppsett.   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
