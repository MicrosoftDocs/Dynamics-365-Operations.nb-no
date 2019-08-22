---
title: Lukke regnskapsåret
description: Denne prosedyren går gjennom årsavslutningsprosessen som overfører saldoer til et nytt regnskapsår.
author: aprilolson
manager: AnnBe
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c12f0842f6e8edf3b51d12d0e008eb09acf8c374
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1834932"
---
# <a name="close-the-fiscal-year"></a>Lukke regnskapsåret

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne prosedyren går gjennom årsavslutningsprosessen som overfører saldoer til et nytt regnskapsår.


## <a name="validate-year-end-close-parameters"></a>Validere årsavslutningsparametere
1. Gå til **Navigasjonsrute > Moduler > Økonomimodul > Finansoppsett > Parametere for økonomimodul**.
2. Utvid delen **Årsavslutning**.
3. Velg Ja eller Nei for alternativet **Slett årsavslutningstransaksjoner under overføring**.
    
    Hvis regnskapsåret allerede er lukket og årsavslutningen kjøres på nytt, er denne innstillingen viktig. Hvis satt til Ja, vil bilaget for den forrige årsavslutningen slettes, og et nytt bilag vil bli opprettet for alle startsaldoer for kontoer. Hvis satt til Nei, blir det forrige bilaget værende og et nytt bilag vil bare bli opprettet for å justere postene som ble postert etter den siste årsavslutningen.

4. Velg Ja eller Nei for **Opprett avslutningstransaksjoner under overføring**.

    Hvis satt til Ja, opprettes to transaksjoner. Ett bilag opprettes i regnskapsåret som lukkes, slik at saldoene for resultatfinanskontoene blir null og et ekstra bilag opprettes i det neste regnskapsåret for startsaldoene. Hvis satt til Nei, opprettet et enkelt bilag i det neste regnskapsåret for startsaldoene.  

5. Velg Ja eller Nei for **Sett regnskapsårsstatusen til permanent lukket**.

    Hvis satt til Ja, settes regnskapsårsstatusen til Lukket permanent.  Fordi et permanent lukket år ikke kan åpnes igjen, vil det være lurt å sette dette alternativet til Nei.  

6. Velg Ja eller Nei for om et **bilagsnummer skal fylles ut under årsavslutningen**.

    Hvis satt til Ja, må et bilagsnummer angis manuelt under årsavslutningsprosessen. En nummerserie brukes ikke til å generere dette bilagsnummeret. Det er lurt å sette dette til Ja.  

7. Lukk siden.
8. Gå til **Økonomimodul > Periodeavslutning > Årsavslutning**.
9. Klikk **Ny** for å opprette en årsavslutningsmal.

    En mal kan opprettes for en gruppe med juridiske enheter som årsavslutningen skal kjøres for. Denne malen kan brukes på nytt år etter år.  

10. I **Gruppenavn**-feltet skriver du inn navnet på årsavslutningsmalen.
11. Velg regnskapsåret som malen skal opprettes for, i feltet **Økonomisk kalender**.

    Bare juridiske enheter som bruker samme regnskapsår, kan grupperes sammen i årsavslutningsmalen. Dette er fordi årsavslutningen gjøres ved å velge et regnskapsår, ikke en dato.  

12. Klikk på **Lagre** i **handlingsruten**.
13. I delen **Juridiske enheter** klikker du på **Legg til** for å velge de juridiske enhetene for denne malen.
    
    Juridiske enheter kan legges ved å velge de juridiske enhetene eller velge et organisasjonshierarki.  Bare juridiske enheter med organisasjonshierarki der samme regnskapskalender er valgt, blir lagt til.  

14. Velg de juridiske enhetene eller organisasjonshierarkiet.
15. Klikk **OK**.
16. Velg Ja eller Nei i **Overfør balansedimensjon**.

    Det er lurt å sette dette alternativet til Ja for balansekontoer. Dette vil opprettholde finansdimensjonene på posterte transaksjoner når du oppretter startsaldoene for balansekontoene. For resultatkontoer kan du velge å opprettholde finansdimensjonene (Lukk alle) når saldoene flyttes til Tilbakeholdt overskudd, eller du kan angi at finansdimensjonene erstattes med en annen dimensjonsverdi (Lukk én). Hvis du velger Lukk én, kan du definere en bestemt dimensjonsverdi for hver dimensjon eller til og med la den stå tom.  

17. Klikk **Lagre**.
18. Start årsavslutningen ved å velge **Kjør årsavslutning** i **handlingsruten**. Årsavslutningen vil kjøres for den valgte malen.  
19. Velg alle eller et delsett med juridiske enheter fra malen som årsavslutningen skal kjøres for.

    Når årsavslutningen kjøres første gang, for å få startsaldoer, velger de fleste organisasjoner å kjøre årsavslutningen for alle juridiske enheter i malen. Hvis justeringer blir gjort etter dette, kan du velge å kjøre årsavslutningen for bare de juridiske enhetene som har justeringer.  

20. Klikk **OK**.
21. Velg regnskapsåret som årsavslutningen skal kjøres for.
22. Skriv inn en verdi i feltet **Bilag**. Det anbefales å ta med regnskapsåret i bilagsnummeret, slik at det blir enklere å finne årsavslutningsbilaget som er opprettet.  
23. Standardinnstillingen for årsavslutningen er å kjøre satsvis. Det er en anbefalt fremgangsmåte å kjøre langvarige prosesser i satsvis modus. Dette er vanligvis en av disse prosessene, som er grunnen til at standard er å bruke satsvis modus.  
24. Klikk **OK**.

