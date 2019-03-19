---
title: Konsekvenskontroll for detaljhandelstransaksjon
description: Dette emnet beskriver funksjonaliteten for konsekvenskontroll for detaljhandelstransaksjon i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: 8b373ce3cfd1183a082e2b1ebaf8c907b16e581e
ms.sourcegitcommit: ca4562fafa33b3512f0a5e246b15545fcf53e834
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/12/2019
ms.locfileid: "379999"
---
# <a name="retail-transaction-consistency-checker"></a>Konsekvenskontroll for detaljhandelstransaksjon


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Dette emnet beskriver funksjonaliteten for konsekvenskontroll for detaljhandelstransaksjon som blir introdusert i Microsoft Dynamics 365 for Finance and Operations versjon 8.1.3. Konsekvenskontrollen identifiserer og isolerer inkonsekvente transaksjoner før de blir plukket opp av utdragsposteringsprosessen.

Når et utdrag posteres i Retail, kan postering mislykkes på grunn av inkonsekvente data i transaksjonstabellene. Dataproblemet kan forårsakes av uforutsette problemer i POS-programmet, eller hvis transaksjoner ikke ble riktig importert fra POS-tredjepartssystemer. Eksempler på hvordan disse inkonsekvensene kan vises: 

  - Transaksjonsbeløpet i toppteksttabellen samsvarer ikke med transaksjonsbeløpet på linjene.
  - Linjeantallet i toppteksttabellen samsvarer ikke med antallet linjer i transaksjonstabellen.
  - Avgifter i toppteksttabellen samsvarer ikke med mva-beløpet på linjene. 
  
Når inkonsekvente transaksjoner blir plukket opp av prosessen, blir inkonsekvente salgsfakturaer og betalingsjournaler opprettet, og derfor mislykkes hele utdragsposteringsprosessen. Gjenoppretting av utdrag fra en slik tilstand omfatter avanserte datakorrigeringer på tvers av flere transaksjonstabeller. Konsekvenskontrollen for detaljhandelstransaksjon hindrer slike problemer.

Diagrammet nedenfor illustrerer posteringsprosessen med konsekvenskontrollen for transaksjon.

![Utdragsposteringsprosess med konsekvenskontroll for detaljhandelstransaksjon](./media/validchecker.png "Utdragsposteringsprosess med konsekvenskontroll for detaljhandelstransaksjon")

Den satsvise prosessen **Valider butikktransaksjoner** kontrollerer konsekvensen i transaksjonstabellene for detaljhandel for følgende scenarier.

- Kundekonto – validerer at kundekontoen i transaksjonstabellene for detaljhandel finnes i malen Hovedkontorkunde.
- Linjeantall – validerer at antallet linjer, som gjengitt i transaksjonstoppteksttabellen, samsvarer med antallet linjer i salgstransaksjonstabellene.

## <a name="set-up-the-consistency-checker"></a>Definere konsekvenskontrollen
Konfigurer den satsvise prosessen Valider butikktransaksjoner på **Detaljhandel \> Detaljhandel-IT \> POS-postering** for periodiske kjøringer. Den satsvise jobben kan planlegges basert på butikkens organisasjonshierarki, på samme måte som prosessene Beregne utdrag satsvis og Postere utdrag satsvis blir definert. Det anbefales at du konfigurerer denne satsvise prosessen til å kjøre flere ganger daglig, og planlegg den slik at den kjøres på slutten av hver kjøring av P-jobb.

## <a name="results-of-validation-process"></a>Resultater av valideringsprosess
Resultatene av valideringskontrollen av den satsvise prosessen er kodet på den aktuelle detaljhandelstransaksjonen. Feltet **Valideringsstatus** i transaksjonsposten for detaljhandel er satt til **Vellykket** eller **Feil**, og datoen for siste valideringskjøring vises i feltet **Tidspunkt for siste validering**.

Hvis du vil vise mer beskrivende feiltekst som er knyttet til en valideringsfeil, velger du den relevante transaksjonsposten for detaljhandel og klikker knappen **Valideringsfeil**.

Transaksjoner som ikke består valideringskontrollen, og transaksjoner som ennå ikke er validert, vil ikke trekkes inn i utdrag. I løpet av prosessen Beregn utdrag vil brukere bli varslet hvis det finnes transaksjoner som kunne ha vært inkludert i utdraget, men som ikke ble inkludert.

Hvis det finnes en valideringsfeil, er den eneste måten å rette opp feilen på, å kontakte Microsofts kundestøtte. Denne funksjonen vil bli lagt til i en fremtidig versjon slik at brukere kan fikse postene som mislyktes i brukergrensesnittet. Loggings- og overvåkingsfunksjoner vil også bli gjort tilgjengelige for sporing av historikken for endringene.

> [!NOTE]
> Flere valideringsregler for å støtte flere scenarier vil bli lagt til i en fremtidig versjon.
