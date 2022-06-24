---
title: Konvensjoner for anleggsmiddelavskrivning
description: Denne artikkelen beskriver avskrivningskonvensjoner for anleggsmidler.
author: moaamer
ms.date: 09/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: AssetDepreciationProfile
audience: Application User
ms.reviewer: kfend
ms.custom: 13891
ms.assetid: 36d1112d-921c-4fff-abe0-0ff2429848d3
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6d791461a344611437e77514e47dd5dd9b7ddb10
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858399"
---
# <a name="fixed-asset-depreciation-conventions"></a>Konvensjoner for anleggsmiddelavskrivning

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver avskrivningskonvensjoner for anleggsmidler. Avskrivningskonvensjoner brukes til å bestemme når og hvordan avskrivningen skal beregnes for både året da anleggsmiddelet anskaffes, og året da et anleggsmiddel avhendes.

Avskrivningskonvensjoner kan tilordnes til oppsettet for et anleggsmiddelgruppetablå. Hvis du vil vise eller tilordne avskrivningskonvensjonen, velger du **Anleggsmiddel**-grupper i oppsettområdet for anleggsmidler. Velg **Tablåer**-knappen. I dette tilfellet brukes avskrivningskonvensjonene som er tilordnet, som standardverdier ved opprettelse av anleggsmiddeltablåer. Avskrivningskonvensjoner kan også angis på et enkelt anleggsmiddeltablå. For å gjøre dette velger du **Tablåer** i oppsettområdet i anleggsmidler, og deretter velger du **Anleggsmiddelgrupper**-knappen.

| Avskrivningskonvensjon   | Beskrivelse |
|---------------------------|-------------|
| Ingen                      | Anleggsmidler starter avskrivningen på <strong>Tatt i bruk</strong>-datoen. |
| Halvår                 | Du kan trekke fra et halvår med avskrivning for både det første året og det siste året som eiendelen avskrives. Du kan trekke fra et helt år med avskrivning for annenhvert år i fradragsperioden. |
| Hele måneden                | Anleggsmidler som har en <strong>Tatt i bruk</strong>-dato som forekommer på ethvert tidspunkt i måneden, starter avskrivningen på den første dagen i denne måneden. For avskrivningsformål anses anleggsmidler som utgått den siste dagen i forrige måned. Den bestemte dagen i måneden når de ble trukket fra, regnes ikke med. |
| Midt i kvartal               | Hvis du vil beregne avskrivningsfradraget for året når du setter eiendelen i drift, multipliserer du avskrivningen for et helt år med prosenten for kvartalet da eiendelen settes i drift, som vist i følgende tabell.<table><thead><tr><th>Kvartal</th><th>Prosent</th></tr></thead><tbody><tr><td>Fornavn</td><td>87,5</td></tr><tr><td>Andre</td><td>62,5</td></tr><tr><td>Tredje</td><td>37,5</td></tr><tr><td>Fjerde</td><td>12.5</td></tr></tbody></table>En halvt kvartal med avskrivning utføres i kvartalet når anleggsmiddelet ble avhendet (eller kvartalet når det ble helt avskrevet). |
| Midt i måneden (1. i måned)  | Anleggsmidler som har en <strong>Tatt i bruk</strong>-dato i den første halvparten av måneden (dagene 1 til 15) begynner å avskrive på den første dagen i måneden for <strong>Tatt i bruk</strong>-datoen. Anleggsmidler som har en <strong>Tatt i bruk</strong>-dato i den andre halvparten av måneden (dag 16 til slutten av måneden) begynner å avskrive på den første dagen i måneden etter <strong>Tatt i bruk</strong>-datoen. Anleggsmidler som realiseres i den første halvdelen av måneden (dagene 1 til 15), regnes som realisert for avskrivningsformål på den siste dagen i forrige måned. Anleggsmidler som realiseres i den andre halvdelen av måneden (dag 16 til slutten av måneden), regnes som realisert for avskrivningsformål på den siste dagen i måneden for realisering. |
| Midt i måneden (15. i måned) | Hvis du vil beregne avskrivningsfradraget for året da du setter eiendelen i drift, multipliserer du avskrivningen for et helt år med en brøk. Telleren (øverste tall) i denne brøken er antall hele måneder i året som eiendelen er i drift pluss 1/2 eller (0,5). Nevneren (nederste tall) er 12. Hvis du avhender eiendelen før slutten av fradragsperioden, kan du bruke samme metode for å beregne avskrivningsfradraget for året for disposisjonen. |
| Halvår (starten på året) | Anleggsmidler som har en <strong>Tatt i bruk</strong>-dato i første halvdel av året, begynner å avskrive på den første dagen i året (fullt år). Anleggsmidler som har en <strong>Tatt i bruk</strong>-dato i andre halvdel av året, begynner å avskrive på årets midtpunkt. |
| Halvår (neste år)     | Anleggsmidler som har en <strong>Tatt i bruk</strong>-dato i første halvdel av året, begynner å avskrive på den første dagen i året (fullt år). Anleggsmidler som har en <strong>Tatt i bruk</strong>-dato i andre halvdel av året, begynner å avskrive på den første dagen i neste år. Anleggsmidler som realiseres i den første halvdelen av året, regnes som realisert for avskrivningsformål på den siste dagen i forrige år. En avskrivning som er postert i inneværende år, må tilbakeføres eller justeres ut. Anleggsmidler som realiseres i den andre halvdelen av året, betraktes som realisert for avskrivningsformål på den siste dagen i året for realisering. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
