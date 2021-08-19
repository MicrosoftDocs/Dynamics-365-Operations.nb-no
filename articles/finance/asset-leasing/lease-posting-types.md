---
title: Leieposteringstyper
description: Dette emnet beskriver posteringstypene som brukes ved transaksjoner for leie av anleggsmidler.
author: moaamer
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetLeasePostingAccounts
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-10-28
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: 721463000c05eb1774335ccce1af39468c2aed9f179e5e88d8725f4d265d6870
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718253"
---
# <a name="lease-posting-types"></a>Leieposteringstyper

[!include [banner](../includes/banner.md)]

Dette emnet beskriver posteringstypene som brukes ved transaksjoner for leie av anleggsmidler.

## <a name="lease-asset"></a>Leieaktivum

Kontoen er knyttet til bruksrettseiendelen. Denne kontoen debiteres når en leieavtale opprinnelig gjenkjennes i henhold til de nye regnskapsstandardene for leieavtaler, Accounting Standards Codification-emne 842 (ASC 842) og International Financial Reporting Standard 16 (IFRS 16). For en modifisert leieavtale kan denne kontoen enten debiteres eller krediteres, avhengig av om endringen øker eller reduserer leieforpliktelsen.

**Eksempeljournaloppføringer:** Opprinnelig føring<br>
**Debet:** Leieaktiva XXX<br>
**Kredit:** Leieforpliktelse XXX

## <a name="lease-liability"></a>Leiegjeld

Kontoen er knyttet til leieforpliktelsen som oppstår når betalinger blir diskontert under de nye IFRS 16- og ASC 842-standardene. Denne kontoen krediteres når en leieavtale opprinnelig gjenkjennes under de nye standardene. Den debiteres for leiebetalinger og krediteres for renteavsetninger.

**Eksempeljournaloppføringer:** Opprinnelig føring<br>
**Debet:** Leieaktiva XXX<br>
**Kredit:** Leieforpliktelse XXX

**Eksempeljournalposter:** Renteavsetning<br>
**Debet:** Renteutgift XXX<br>
**Kredit:** Leieforpliktelse XXX

**Eksempeljournaloppføringer:** Leiebetaling<br>
**Debet:** Leieforpliktelse XXX<br>
**Kredit:** Leverandør-/leiebetaling XXX

## <a name="short-term-lease-liability"></a>Kortsiktig leiegjeld

Kontoen knyttes til korttidsleieforpliktelsen når journaloppføringen for omklassifisering av korttidsleieforpliktelse posteres. Denne kontoen krediteres for kortsiktig gjeld fra nedbetalingplanen på den siste dagen i måneden. Det samme beløpet blir imidlertid debitert den første dagen i neste måned.

**Eksempeljournaloppføringer:** Omklassifisering av kortsiktig leieforpliktelse<br>
**Debet:** Leieforpliktelse XXX<br>
**Kredit:** Kortsiktig leieforpliktelse XXX<br>
**Debet:** Kortsiktig leieforpliktelse XXX<br>
**Kredit:** Leieforpliktelse XXX

## <a name="depreciation-expense"></a>Avskrivningskostnad

Kontoen er knyttet til utgiften som er knyttet til avskrivningen for bruksrettseiendelen under IFRS 16, ASC 842 og finansiell leie under IAS 17 og ASC 840. Denne kontoen debiteres når en bruksrettseiendel avskrives hver måned.

**Eksempeljournaloppføringer:** Avskrivningsavsetning<br>
**Debet:** Avskrivningskostnad XXX<br>
**Kredit:** Akkumulert avskrivning XXX

## <a name="gainloss-on-lease-modification"></a>Fortjeneste/tap ved endring av leie

Kontoen er knyttet til tap eller vinning som oppstår ved leieendringer. Det kan oppstå en gevinst under en endring i leien hvis endringen reduserer leieforpliktelsen med et beløp som overskrider den bokførte verdien til bruksrettseiendelen.

En leie har for eksempel en gjeldende bokført verdi for leieforpliktelsen på $150 000 og en bokført verdi for bruksrettseiendelen på $100 000. Leieavtalen endres, og denne endringen gir en ny nåverdi av fremtidige minimums leiebetalinger (PVFMLP) på $40 000. Derfor blir leieforpliktelse debitert med $110 000 ($150 000–$40 000). Siden bruksrettseiendelen bare er $100 000, vil reduksjonen på $110 000 redusere aktivaet under 0 (null). Derfor angir regnskapsveiledningen at resten skal bokføres til en fortjenestekonto. I dette tilfellet vil den endelige journaloppføringen være en debitering av leieforpliktelsen på $110 000, en kreditering til leieaktivaet på $100 000, og en kreditering av fortjenestekontoen på $10 000.

**Eksempeljournaloppføringer:** Leieendring<br>
**Debet:** Leieforpliktelse XXX<br>
**Kredit:** Leieaktiva XXX<br>
**Kredit:** Fortjeneste XXX

## <a name="accumulated-depreciation"></a>Akkumulert avskrivning

Kontoen er knyttet til kontoen for bruksrettseiendelen. Denne kontoen krediteres når en avskrivningskostnad posteres.

**Eksempeljournaloppføringer:** Avskrivningsavsetning<br>
**Debet:** Avskrivningskostnad XXX<br>
**Kredit:** Akkumulert avskrivning XXX

## <a name="variable-payment"></a>Variabel betaling

Kontoen er knyttet til variable leiebetalinger som produseres ved hjelp av en indeksverdiregulering under ASC 842, ASC 840 og IAS 17-leieavtaler. I leiebetalingsplanen er variable betalinger inkludert i **Variabel betaling**-kolonnen. Denne kontoen debiteres når det opprettes en faktura mot en betalingsplanlinje som inneholder en variabel betaling.

**Eksempeljournaloppføringer:** Leiebetaling<br>
**Debet:** Leieforpliktelse XXX<br>
**Debet:** Variabel betaling XXX<br>
**Kredit:** Leverandør-/leiebetaling XXX

## <a name="deferred-rent-asset-liability"></a>Aktiva med utsatt leie (gjeld)

Kontoen er knyttet til aktiva med utsatt leie eller gjeld som fremstilles av en leieavtale med utsatt leie. Denne kontoen debiteres når en faktura posteres mot en leieavtale med utsatt leie, hvis leiebetalingsbeløpet er mer enn periodens lineær renteutgift. Den krediteres hvis leiebetalingen er mindre enn periodens lineær renteutgift.

**Eksempel på journaloppføringer:** Leiebetaling (leieavtale med utsatt leie)<br>
**Debet:** Leieutgift XXX<br>
**Kredit:** Utsatt leieavgift (gjeld) XXX<br>
**Kredit:** Leverandør-/leiebetaling XXX

## <a name="lease-expense"></a>Leieutgift

Kontoen er knyttet til leieutgiften hvis leieavtalen klassifiseres som en leieavtale med utsatt leie. Denne kontoen debiteres når en faktura posteres mot en leieavtale med utsatt leie.

**Eksempel på journaloppføringer:** Leiebetaling (leieavtale med utsatt leie)<br>
**Debet:** Leieutgift XXX<br>
**Kredit:** Utsatt leieavgift (gjeld) XXX<br>
**Kredit:** Leverandør-/leiebetaling XXX

## <a name="impairment-expense"></a>Verdiforringelsesutgift

Kontoen posteres mot når en leieavtale svekkes. Denne kontoen debiteres, mens bruksrettseiendelskontoen krediteres direkte.

**Eksempeljournaloppføringer:** Leiebetaling<br>
**Debet:** Verdiforringelsesutgift XXX<br>
**Kredit:** Bruksrettseiendel XXX

## <a name="lease-payment"></a>Leiebetaling

Kontoen posteres mot hvis parameteren **Betal til leverandør** er deaktivert. Denne kontoen krediteres i stedet for leverandøren hvis parameteren er deaktivert.

**Eksempeljournaloppføringer:** Leiebetaling<br>
**Debet:** Leieforpliktelse XXX<br>
**Kredit:** Leiebetaling XXX

## <a name="expense-type-postings"></a>Utgiftstypeposteringer

Kontoen som velges for hver utgiftstype, debiteres når det genereres en betaling for denne utgiftstypen. Kontoen som er angitt for utgiftstypen **Forsikring**, debiteres eksempelvis når en journaloppføring for faktura eller betaling opprettes ut fra fullbyrdelseskostnadsplanen for forsikringsutgifter.

**Eksempeljournaloppføringer:** Forsikringsbetaling<br>
**Debet:** Forsikringsutgiftstypekonto XXX<br>
**Kredit:** Motkonto XXX

> [!NOTE]
> Motkontoen velges på leienivå på linjene for betalingsplanen for fullbyrdelseskostnad. Denne motkontoen kan knyttes til leverandøren eller til en finanskonto.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
