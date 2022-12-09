---
title: Finansfordelingsregler
description: Denne artikkelen gir generell informasjon om finanstildelingsregler. Den beskriver de ulike komponentene i disse tildelingsreglene og tildelingsmetodene som kan brukes for dem.
author: kweekley
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerAllocation, LedgerAllocationBasisRule, LedgerAllocationRequest, LedgerAllocationRule
audience: Application User
ms.reviewer: kfend
ms.custom: 15402
ms.assetid: 8147e148-7c11-45ef-95c6-f9889a875b54
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0691c65e6a499f713952070811cefaa7a213af7b
ms.sourcegitcommit: c364f50ea0ad50bac5c30724b6ce301d9574b653
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/18/2022
ms.locfileid: "9787560"
---
# <a name="ledger-allocation-rules"></a>Finansfordelingsregler

[!include [banner](../includes/banner.md)]

Denne artikkelen gir generell informasjon om finanstildelingsregler. Den beskriver de ulike komponentene i disse tildelingsreglene og tildelingsmetodene som kan brukes for dem.

Finansfordelingsregler brukes til automatisk å beregne og generere tildelingsjournaler og poster for fordeling av finanssaldoer eller faste beløp. Tildelingsmetoder kan være variable eller faste. Tildelingen er basert på transaksjonsvalutaverdien. Fremmed valutagevinst/tap-oppføringer posteres for eksempel til å justere regnskaps- og rapporteringsvalutabeløpene. Disse oppføringene er ikke underlagt tildelingsregler, fordi transaksjonsvalutaverdien er 0,00. Følgende tildelingsmetoder kan brukes for fordelingsregler for finans:

-   **Basis** – denne variable metoden brukes når tildelingen er avhengig av den faktiske finanssaldoen, basert på filterkriteriene. Du kan for eksempel tildele reklameutgifter basert på salget til hver avdeling i forhold til hele avdelingssalget.
-   **Fast prosent** og **Fast vekt** – For disse metodene defineres tildelingsprosent eller vekt direkte for regelen. Reklameutgifter kan for eksempel tildeles slik at avdeling A får 70 prosent av reklameutgiftene, og avdeling B får 30 prosent.
-   **Likt** – denne metoden fordeler beløpet likt til alle definerte mål. Hvis mål for eksempel er definert for avdeling A og B avdeling, kan reklameutgifter tildeles slik at både avdeling A og avdeling B får 50 prosent av reklameutgiftene.

Hvis Basis brukes som tildelingsmetoden for en tildelingsregel , må du også definer en separate basisregler for finanstildeling. Ved hjelp av prosessen "Behandle tildelingsforespørsel" kan brukerne behandle finansfordelingsregelen og forhåndsvise de resulterende tildelingspostene for journalen før de posterer eller sletter de beregnede tildelingene.

## <a name="components-of-ledger-allocation-rules"></a>Komponenter for finansfordelingsregler
Hver fordelingsregel har fire komponenter: generelt, kilde, mål og forskyvning. En tilleggskomponent, regler for finansfordelingsbasis, er nødvendig hvis Basis brukes som fordelingsmetode. Hver komponent gir en viktig del av informasjonen som kreves for å behandle fordelinger.

-   **Generelt** – Denne komponenten er der brukeren angir alternativ som omfatter, men ikke er begrenset til, tildelingsmetode og konsernintern regelinnstillinger samt angir om regelen er aktiv eller ikke.
-   **Kilde** – Denne komponenten er der brukeren angir kildedata for tildelingen. Tildelingen kan være basert på finanssaldoer (**Datakilde** = **Finans**) eller faste beløp (**Datakilde** = **Fast verdi**). Når **Datakilde** er satt til **Finans**, må kildefilterkriterier defineres for finansfordelingsregelen (for eksempel for reklameutgiftene).
-   **Mål** – Denne komponenten definerer hvordan resultatet til tildelingsberegningen skal distribueres og beregnes. Det kan for eksempel være én mållinje for hver avdeling.
-   **Forskyvning** – Denne komponenten definerer hvordan hovedkontoer og dimensjoner skal bestemmes for motoppføringene som balanserer måloppføringene. Brukerdefinerte alternativer brukes vanligvis i stedet for kontoene og dimensjonene som er basert på kilden. Når **datakilden** er satt til **Fast verdi**, kan ikke **Kilde** brukes som et alternativ.
-   **Basisregler for finanstildeling** – Disse reglene bruker egne kildefilterkriterier for å bestemme hvilke finanssaldoer som skal brukes for tildeling (for eksempel omsetning per avdeling). Hver fordelingsbasisregel kan brukes med flere fordelingsregler.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]
