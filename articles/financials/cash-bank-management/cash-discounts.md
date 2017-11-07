---
title: Kontantrabatt
description: "Kontantrabatter konfigureres og deles for leverandører og kunder.  Den tilgjengelige kontantrabatten kan defineres på kundefaktura eller leverandørfaktura, og brukes hvis fakturaen betales innen kontantrabattdatoen."
author: kweekley
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 3741
ms.assetid: c25f9d85-2702-46aa-8e61-0b4886e069b3
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 668e3ebdd2729efb48e2833fd5beec3cefdb17b0
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="cash-discounts"></a>Kontantrabatt

[!include[banner](../includes/banner.md)]


Kontantrabatter konfigureres og deles for leverandører og kunder.  Den tilgjengelige kontantrabatten kan defineres på kundefaktura eller leverandørfaktura, og brukes hvis fakturaen betales innen kontantrabattdatoen. 

<a name="cash-discounts"></a>Kontantrabatt
--------------

Kontantrabatter for både kunder eller leverandører kan opprettes på siden for kontantrabatter. Du kan også definere, ved hjelp av feltet Neste rabattkode, en serie med kontantrabatter som kommer etter hverandre etter hvert som tidligere kontantrabattdatoer utløper. Hvis du vil ha mer informasjon, se "Eksempel: Serie med kontantrabatter" senere i dette emnet. Hvis fakturaen, kredittransaksjonen (en betaling eller en kreditnota) eller begge deler er angitt i en annen valuta enn regnskapsvalutaen for den juridiske enheten, blir kontantrabatten beregnet ved hjelp av valutakursen som er basert på datoen for betalingen eller kreditnotaen. Hvis fakturaen eller kredittdokumentet er angitt i ulike juridiske enheter, og hvis regnskapsvalutaene for de juridiske enhetene er forskjellige, hentes valutakursen fra den juridiske enheten for fakturaen, i henhold til datoen for kredittdokumentet. Hvis du vil ha mer informasjon, se "Eksempel: Valutakurser for kontantrabatter" senere i dette emnet.
Standardrekkefølge for kontantrabatthovedkonto
----------------------------------------------

Hvis en faktura betales tidsnok til å få en kontantrabatt, posteres kontantrabatten automatisk til en kontantrabatthovedkonto i henhold til følgende standardprioritet:
1.  Hovedkontoen som er angitt i feltet Alternativ kontantrabattkonto på kundesiden Utlign åpne transaksjoner eller leverandørsiden Utlign åpne transaksjoner.
2.  Hovedkontoen som er angitt i feltet Kundekontantrabatt eller i feltet Leverandørkontantrabatt for finansposteringsgruppen som er tilordnet mva-koden for fakturaen. Definer finansposteringsgrupper på siden Finansposteringsgrupper, og tilordne dem til mva-koder på siden for mva-koder.
3.  Den primære posteringskontoen på siden Kontantrabatter i feltet Hovedkonto for kunderabatter eller feltet Hovedkonto for leverandørrabatter for kontantrabattkoden som finnes på den utlignede fakturaen.
4.  Hovedkontoen for kontantrabatter, som definert på siden Kontoer for automatiske transaksjoner.

## <a name="example-series-of-cash-discounts"></a>Eksempel: Serie med kontantrabatter
Definer tre kontantrabattkoder på denne måten:
-   Kode 5D10% – En kontantrabatt på 10 % hvis beløpet betales innen 5 dager.
-   Kode 10D5% – En kontantrabatt på 5 % hvis beløpet betales innen 10 dager.
-   Kode 14D2% – En kontantrabatt på 2 % hvis beløpet betales innen 14 dager.

I feltet Neste rabattkode:
-   For 5D10%-koden velger du 10D5%.
-   For 10D5%-koden velger du 14D2%.
-   For 14D2%-koden lar du feltet Neste rabattkode stå tomt.

De tre kontantrabattene følger hverandre når betalingsdatoen overskrider den forrige kontantrabattdatoen på fakturaen. Bare én kontantrabatt gis når fakturaen er betalt, basert på hvilken kontantrabattdato som oppfylles i sekvensen med kontantrabatter.

## <a name="example-exchange-rates-for-cash-discounts"></a>Eksempel: Valutakurser for kontantrabatter
Regnskapsvalutaen for den juridiske enheten er EUR, og følgende valutakurser er angitt for USD:
-   1. februar = 110
-   1. mars = 80

Det posteres en faktura på USD 1 000 med vilkårene for kontantrabatt på 20D2% 15. februar. Regnskapsvalutabeløpet på fakturaen er 1100 EUR. En betaling på USD 980 betales med fakturaen 1. mars. Kontantrabattbeløpet er USD 20. Regnskapsvalutabeløpet for betalingen er EUR 784. Regnskapsvalutabeløpet for kontantrabatten blir beregnet ved hjelp av valutakursen 1. mars: 20 \* 80 / 100 = EUR 16.
| **Obs!**                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Hvis alternativet Beregn kontantrabatter for delvise betalinger velges på siden Kundeparametere eller Leverandørparametere, brukes valutakursen som er i kraft på datoen for hver delbetaling. |

 
=

 




