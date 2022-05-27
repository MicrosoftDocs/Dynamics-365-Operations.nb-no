---
title: Lukke regnskapsåret
description: Denne prosedyren går gjennom årsavslutningsprosessen som overfører saldoer til et nytt regnskapsår.
author: aprilolson
ms.date: 07/11/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerParameters, LedgerFiscalCloseGroup, LedgerFiscalCloseAddLedger, SysLookupMultiSelectGrid, LedgerFiscalCloseRunGroup
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 8eb36cb856d191d64561060e7de4a1f9fd947882
ms.sourcegitcommit: 1d2eeacad11c28889681504cdc509c90e3e8ea86
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/05/2022
ms.locfileid: "8717481"
---
# <a name="close-the-fiscal-year"></a>Lukke regnskapsåret

[!include [banner](../../includes/banner.md)]

Denne prosedyren går gjennom årsavslutningsprosessen som overfører saldoer til et nytt regnskapsår.


## <a name="validate-year-end-close-parameters"></a>Validere årsavslutningsparametere
1. Gå til **Navigasjonsrute > Moduler > Økonomimodul > Finansoppsett > Parametere for økonomimodul**.
2. Utvid delen **Årsavslutning**.
3. Velg **Ja** eller **Nei** for alternativet **Slett årsavslutningstransaksjoner under overføring**.
    
Hvis regnskapsåret allerede er lukket og årsavslutningen kjøres på nytt, er denne innstillingen viktig. Hvis **Ja** er angitt, vil bilaget for den forrige årsavslutningen slettes, og et nytt bilag vil bli opprettet for alle startsaldoer for kontoer. Hvis **Nei** er angitt, blir det forrige bilaget værende, og et nytt bilag vil bare bli opprettet for å justere postene som ble postert etter den siste årsavslutningen.

4. Velg **Ja** eller **Nei** for alternativet **Opprett avslutningstransaksjoner under overføring**.

Hvis **Ja** er angitt, opprettes to transaksjoner. Ett bilag opprettes i regnskapsåret som lukkes, slik at saldoene for alle finanskontoene blir null og et ekstra bilag opprettes i det neste regnskapsåret for startsaldoene. Hvis **Nei** er angitt, opprettes ett bilag i det neste regnskapsåret for startsaldoene.  

5. Velg **Ja** eller **Nei** for alternativet **Sett regnskapsårsstatusen til permanent lukket**.

Hvis **Ja** er angitt, settes regnskapsårsstatusen til Lukket permanent. Fordi et permanent lukket år ikke kan åpnes igjen, vil det være lurt å sette dette alternativet til **Nei**.  

6. Velg **Ja** eller **Nei** for alternativet **Bilagsnummer skal fylles ut under årsavslutningen**.

Hvis **Ja** er angitt, må et bilagsnummer angis manuelt under årsavslutningsprosessen. En nummerserie brukes ikke til å generere dette bilagsnummeret. Vi anbefaler å angi **Ja** for dette.  

7. Lukk siden.
8. Gå til **Økonomimodul > Periodeavslutning > Årsavslutning**.
9. Klikk **Ny** for å opprette en årsavslutningsmal.

En mal kan opprettes for en gruppe med juridiske enheter som årsavslutningen skal kjøres for. Denne malen kan brukes på nytt år etter år.  

10. I **Gruppenavn**-feltet skriver du inn navnet på årsavslutningsmalen.
11. Velg regnskapsåret som malen skal opprettes for, i feltet **Økonomisk kalender**.

Bare juridiske enheter som bruker samme regnskapsår, kan grupperes sammen i årsavslutningsmalen. Dette er fordi årsavslutningen gjøres ved å velge et regnskapsår, ikke en dato.  

12. Klikk på **Lagre** i **handlingsruten**.
13. I delen **Juridiske enheter** klikker du på **Legg til** for å velge de juridiske enhetene for denne malen.
    
Juridiske enheter kan legges ved å velge de juridiske enhetene eller velge et organisasjonshierarki. Bare juridiske enheter med organisasjonshierarki der samme regnskapskalender er valgt, blir lagt til.  

14. Velg de juridiske enhetene eller organisasjonshierarkiet.
15. Klikk på **OK**.
16. Velg **Ja** eller **Nei** i **Overfør balansedimensjon**.

Vi anbefaler å angi **Ja** for dette alternativet for balansekontoer. Dette vil opprettholde finansdimensjonene på posterte transaksjoner når du oppretter startsaldoene for balansekontoene. For resultatkontoer kan du velge å opprettholde finansdimensjonene (**Lukk alle**) når saldoene flyttes til Tilbakeholdt overskudd, eller du kan angi at finansdimensjonene erstattes med en annen dimensjonsverdi (**Lukk én**). Hvis du velger **Lukk én**, kan du definere en bestemt dimensjonsverdi for hver dimensjon eller til og med la den stå tom.  

17. Klikk **Lagre**.
18. Start årsavslutningen ved å velge **Kjør årsavslutning** i **handlingsruten**. Årsavslutningen vil kjøres for den valgte malen.  
19. Velg alle eller et delsett med juridiske enheter fra malen som årsavslutningen skal kjøres for.

Når årsavslutningen kjøres første gang, for å få startsaldoer, velger de fleste organisasjoner å kjøre årsavslutningen for alle juridiske enheter i malen. Hvis justeringer blir gjort etter dette, kan du velge å kjøre årsavslutningen for bare de juridiske enhetene som har justeringer.  

20. Klikk **OK**.
21. Velg regnskapsåret som årsavslutningen skal kjøres for.
22. Skriv inn en verdi i feltet **Bilag**. Det anbefales å ta med regnskapsåret i bilagsnummeret, slik at det blir enklere å finne årsavslutningsbilaget som er opprettet.  
23. Standardinnstillingen for årsavslutningen er å kjøre satsvis. Det er en anbefalt fremgangsmåte å kjøre langvarige prosesser i satsvis modus. Dette er vanligvis en av disse prosessene, som er grunnen til at standard er å bruke satsvis modus.  
24. Klikk **OK**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
