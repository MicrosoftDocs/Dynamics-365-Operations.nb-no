---
title: Amortisere konstante kostnader for en produsert vare
description: De konstante kostnadene til en produsert vare viser oppstillingstider for operasjonene og komponentene som har et konstant antall eller et konstant svinnbeløp.
author: JennySong-SH
ms.date: 04/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, BOMCalcTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 274503
ms.assetid: 535ab25d-a031-4e8c-84ec-478f2987a1ad
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.dyn365.ops.version: AX 7.0.0
ms.search.validFrom: 2016-02-28
ms.openlocfilehash: d466395859e19874183691e697c8aca3a774d359
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/03/2022
ms.locfileid: "8675410"
---
# <a name="amortize-constant-costs-for-a-manufactured-item"></a>Amortisere konstante kostnader for en produsert vare

[!include [banner](../includes/banner.md)]

De konstante kostnadene til en produsert vare viser oppstillingstider for operasjonene og komponentene som har et konstant antall eller et konstant svinnbeløp. 

Konseptet med en kostnadspartistørrelse brukes til nedbetaling av disse konstante kostnadene i de beregnede kostnadene til en produsert vare. Dette konseptet har flere synonymer, for eksempel regnskapspartistørrelse. Konseptet med nedbetaling av konstante kostnader har også flere synonymer, for eksempel proporsjonale konstante kostnader.

Kostnadspartistørrelsesantallet for en produsert vare brukes i en stykklisteberegning. Antallet avhenger av hvordan du starter og utfører stykklisteberegningen, slik det illustreres nedenfor:

-   Standard beregningsantall i en vares stykklisteberegning − Varens standard bestillingsantall for lager fungerer som standardverdi for kostnadspartistørrelsen til varen, men standardverdien kan være et større antall for å gjenspeile varens bestillingsmultiplumsantall. Varens standard bestillingsantall og multiplum kan defineres innenfor standardinnstillingene for bestilling eller stedsbestemte bestillingsinnstillinger.
-   Angitt beregningsantall i en vares stykklisteberegning − Det angitte beregningsantallet fungerer som kostnadspartistørrelsen til varen. Beregningsantallet er i utgangspunktet varens standard bestillingsantall, men kan overstyres manuelt. Det angitte beregningsantallet representerer kostnadspartistørrelsen for den angitte varen, og for produserte komponenter som har stykklistelinjetypen produksjon. Dette er fordi det antas at komponenten vil bli produsert i et eksakt antall. Kostnadspartistørrelsen for andre produserte komponenter med stykklistelinjetypevarer viser deres standard bestillingsantall.
-   Angitt beregningsantall for produksjon-etter-ordre i en vares stykklisteberegning − Det angitte beregningsantallet fungerer som kostnadspartistørrelsen for varen og de produserte komponentene når stykklisteberegninger bruker en produksjon-etter-ordre-nedbrytingsmodus. Det antas at komponenten vil bli produsert i et eksakt antall, på samme måte som en produsert komponent i en stykklistelinjetypeproduksjon.
-   Angitt beregningsantall i en ordrespesifikk stykklisteberegning − En ordrespesifikk stykklisteberegning kan utføres for en linjevare på en salgsordre, et salgstilbud eller en serviceordre. Det angitte beregningsantallet bruker som standard antallet på linjen der varen opprinnelig kommer fra, men standardantallet kan overstyres. Du kan velge om den ordrespesifikke stykklisteberegningen skal bruke modusen produksjon-etter-ordre eller nedbryting på flere nivåer.

Det beregnede beløpet for nedbetaling av en produsert vares konstante kostnader, kalles tillegg.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]