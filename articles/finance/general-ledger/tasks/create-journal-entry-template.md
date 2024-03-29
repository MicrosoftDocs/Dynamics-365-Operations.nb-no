---
title: Opprette en journaloppføring ved hjelp av en mal
description: Posterte journalbilag kan lagres som bilagsmaler og brukes i et nytt journalbilag.
author: aprilolson
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 05cb878b570c45a2f7358ad60e6e01c7af17dc90
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8716502"
---
# <a name="create-a-journal-entry-using-template"></a>Opprette en journaloppføring ved hjelp av en mal

[!include [banner](../../includes/banner.md)]

Posterte journalbilag kan lagres som bilagsmaler og brukes i et nytt journalbilag. Denne fremgangsmåten bruker demonstrasjonsfirmaet USMF.

1. Gå til **Navigasjonsrute > Moduler > Økonomimodul > Journaloppføringer > Økonomijournaler**.
2. Klikk **Ny** i **handlingsruten**. Denne prosedyren starter ved å opprette og postere et journalbilag, men eventuelle tidligere posterte journalbilag kan lagres som en mal.  
3. Klikk på rullegardinknappen i **Navn**-feltet for å åpne oppslaget.
4. Finn og velg ønsket post i listen.
5. Klikk koblingen i den valgte raden i listen.
6. Klikk **Linjer**.
7. Angi en verdi i **Kontotype**-feltet.
8. Skriv inn en verdi i **Beskrivelse**-feltet.
9. Skriv inn en verdi i **Debet**-feltet.
10. Klikk på **Ny**.
11. Angi en verdi i **Kontotype**-feltet.
12. Skriv inn en verdi i **Beskrivelse**-feltet.
13. Skriv inn en verdi i **Debet**-feltet.
14. Klikk på **Ny**.
14. Angi de ønskede verdiene i **Konto**-feltet.
15. Skriv inn en verdi i **Beskrivelse**-feltet.
16. Skriv inn en verdi i **Kredit**-feltet for å balansere bilaget.
17. Klikk **Poster** i **handlingsruten**.
18. Klikk **Funksjoner**.
19. Klikk **Lagre bilag som mal**.
20. Denne fremgangsmåten forutsetter en **maltype som prosent**. Klikk OK.
    - Prosent: beløpene i bilaget konverteres til prosentfaktorer, som gjør at alle beløp kan brukes når bilagsmalen er valgt.
    - Beløp: de faktiske beløpene lagres og brukes.  
21. Klikk **Økonomijournaler**.
22. Klikk på **Ny**.
23. Klikk på rullegardinknappen i **Navn**-feltet for å åpne oppslaget.
24. Klikk koblingen i den valgte raden i listen.
25. Klikk **Linjer**.
26. Klikk **Funksjoner**.
27. Klikk **Velg bilagsmal**.
28. Finn malen som du opprettet før. Klikk **OK**. Du må kanskje klikke **Forrige trinn** og deretter velge riktig mal hvis det finnes andre maler.  
29. I feltet **Beløp** kan du angi beløpet som skal brukes for bilaget. **Beløp**-feltet vises bare hvis bilagsmalen er av typen Prosent.  
30. Klikk **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
