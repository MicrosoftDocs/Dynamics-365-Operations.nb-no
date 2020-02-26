---
title: Konsekvenskontroll for detaljhandelstransaksjon
description: Dette emnet beskriver funksjonaliteten for konsekvenskontroll for transaksjon i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
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
ms.openlocfilehash: 3da8bdf6feb932e074680b6cb80e1b7b71f9a82b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004257"
---
# <a name="retail-transaction-consistency-checker"></a>Konsekvenskontroll for detaljhandelstransaksjon


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Dette emnet beskriver funksjonaliteten for konsekvenskontroll for transaksjon i Microsoft Dynamics 365 Commerce. Konsekvenskontrollen identifiserer og isolerer inkonsekvente transaksjoner før de blir plukket opp av utdragsposteringsprosessen.

Når et utdrag posteres, kan postering mislykkes på grunn av inkonsekvente data i transaksjonstabellene i Commerce. Dataproblemet kan forårsakes av uforutsette problemer i POS-programmet, eller hvis transaksjoner ikke ble riktig importert fra POS-tredjepartssystemer. Eksempler på hvordan disse inkonsekvensene kan vises: 

- Transaksjonsbeløpet i toppteksttabellen samsvarer ikke med transaksjonsbeløpet på linjene.
- Linjeantallet i toppteksttabellen samsvarer ikke med antallet linjer i transaksjonstabellen.
- Avgifter i toppteksttabellen samsvarer ikke med mva-beløpet på linjene. 

Når inkonsekvente transaksjoner blir plukket opp av prosessen, blir inkonsekvente salgsfakturaer og betalingsjournaler opprettet, og derfor mislykkes hele utdragsposteringsprosessen. Gjenoppretting av utdrag fra en slik tilstand omfatter avanserte datakorrigeringer på tvers av flere transaksjonstabeller. Konsekvenskontrollen for transaksjon hindrer slike problemer.

Diagrammet nedenfor illustrerer posteringsprosessen med konsekvenskontrollen for transaksjon.

![Posteringsprosess for utdrag med konsekvenskontroll for transaksjon](./media/validchecker.png "Posteringsprosess for utdrag med konsekvenskontroll for detaljhandelstransaksjon")

Den satsvise prosessen **Valider butikktransaksjoner** kontrollerer konsekvensen i transaksjonstabellene for Commerce for følgende scenarier.

- **Kundekonto** – validerer at kundekontoen i transaksjonstabellene finnes i malen Hovedkontorkunde.
- **Linjeantall** – validerer at antallet linjer, som gjengitt i transaksjonstoppteksttabellen, samsvarer med antallet linjer i salgstransaksjonstabellene.
- **Pris inkluderer avgift** – validerer at parameteren **Pris inkluderer avgift** er konsekvent i alle transaksjonslinjene.
- **Betalingsbeløp** – validerer at betalingspostene samsvarer med betalingsbeløpet i hodet.
- **Bruttobeløp** – validerer at bruttobeløpet i hodet er summen av nettobeløpene på linjene pluss avgiftsbeløpet.
- **Nettobeløp** – validerer at nettobeløpet i toppteksten er summen av nettobeløpene på linjene.
- **Under-/overbetaling** – validerer at differansen mellom bruttobeløpet i toppteksten og betalingsbeløpet ikke overskrider konfigurasjonen for maksimal under-/overbetaling.
- **Rabattbeløp** – validerer at rabattbeløpet i rabattabellene og rabattbeløpet i tabellene med transaksjonslinjer er konsekvente, og at rabattbeløpet i toppteksten er summen av rabattbeløpene på linjene.
- **Linjerabatt** – validerer at linjerabatten på transaksjonslinjen er summen av alle linjene i rabattabellen som tilsvarer transaksjonslinjen.
- **Gavekortvare** – Commerce støtter ikke retur av gavekortvarer. Saldoen på et gavekort kan imidlertid innløses i kontanter. En gavekortvare som behandles som en returlinje i stedet for en linje for innløsing i kontanter, vil mislykkes i utdragsposteringsprosessen. Valideringsprosessen for gavekortvarer sikrer at de eneste returlinjene for gavekortvarer i transaksjonstabellene er linjene for innløsing av gavekort i kontanter.
- **Negativ pris** – validerer at det ikke finnes transaksjonslinjer med negativ pris.
- **Vare og variant** – validerer at varer og varianter på transaksjonslinjene finnes i hovedfilen for varer og varianter.
- **Avgiftsbeløp** – validerer at mva-poster samsvarer med avgiftsbeløpet på linjene.
- **Serienummer** – validerer at serienummeret finnes i transaksjonslinjene for varer som styres av serienummer.
- **Fortegn** – validerer at fortegnet for antallet og nettobeløpet er det samme i alle transaksjonslinjene.
- **Forretningsdato** – validerer at regnskapsperiodene for alle forretningsdatoene for transaksjonene er åpne.

## <a name="set-up-the-consistency-checker"></a>Definere konsekvenskontrollen

Konfigurer den satsvise prosessen Valider butikktransaksjoner på **Detaljhandel og handel \> IT for Detaljhandel og handel \> Salgsstedspostering** for periodiske kjøringer. Den satsvise jobben kan planlegges basert på butikkens organisasjonshierarki, på samme måte som prosessene Beregne utdrag satsvis og Postere utdrag satsvis blir definert. Det anbefales at du konfigurerer denne satsvise prosessen til å kjøre flere ganger daglig, og planlegg den slik at den kjøres på slutten av hver kjøring av P-jobb.

## <a name="results-of-validation-process"></a>Resultater av valideringsprosess

Resultatene av valideringskontrollen av den satsvise prosessen er kodet på den aktuelle transaksjonen. Feltet **Valideringsstatus** i transaksjonsposten er satt til **Vellykket** eller **Feil**, og datoen for siste valideringskjøring vises i feltet **Tidspunkt for siste validering**.

Hvis du vil vise mer beskrivende feiltekst som er knyttet til en valideringsfeil, velger du den relevante transaksjonsposten og klikker knappen **Valideringsfeil**.

Transaksjoner som ikke består valideringskontrollen, og transaksjoner som ennå ikke er validert, vil ikke trekkes inn i utdrag. I løpet av prosessen Beregn utdrag vil brukere bli varslet hvis det finnes transaksjoner som kunne ha vært inkludert i utdraget, men som ikke ble inkludert.

Hvis det finnes en valideringsfeil, er den eneste måten å rette opp feilen på, å kontakte Microsofts kundestøtte. Denne funksjonen vil bli lagt til i en fremtidig versjon slik at brukere kan fikse postene som mislyktes i brukergrensesnittet. Loggings- og overvåkingsfunksjoner vil også bli gjort tilgjengelige for sporing av historikken for endringene.

> [!NOTE]
> Flere valideringsregler for å støtte flere scenarier vil bli lagt til i en fremtidig versjon.
