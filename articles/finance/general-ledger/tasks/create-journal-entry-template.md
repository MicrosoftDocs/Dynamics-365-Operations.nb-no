---
title: Opprette en journaloppføring ved hjelp av en mal
description: Posterte journalbilag kan lagres som bilagsmaler og brukes i et nytt journalbilag.
author: aprilolson
manager: AnnBe
ms.date: 07/01/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransDaily, LedgerJournalTransVoucherTemplate
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 360df29e6349fd4d42d6d14af646e929b73943bd
ms.sourcegitcommit: 57e1dafa186fec77ddd8ba9425d238e36e0f0998
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3145169"
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

