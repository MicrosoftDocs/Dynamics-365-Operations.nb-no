---
title: Forberede vedlikehold av standard kostpris for produserte varer
description: Denne artikkelen beskriver fremgangsmåten for å forberede vedlikehold av kostnader for produserte varer.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 423da8022faf8066c5aa524c49c5071d0871de04
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8886022"
---
# <a name="prepare-to-maintain-standard-costs-for-manufactured-items"></a>Forberede vedlikehold av standard kostpris for produserte varer

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver fremgangsmåten for å forberede vedlikehold av kostnader for produserte varer. Fremgangsmåten for produserte varierer litt fra trinnene for innkjøpte varer.

Reglene som tilordnes produserte varer kan påvirke kostnadsberegningene for de overordnede produserte varene. Når du skal forberede vedlikehold av kostpris for produserte varer, gjør du følgende.

1. Tilordne en varemodellgruppe til den produserte varen. 

   Varemodellgruppen identifiserer at standard kostpris brukes.

2. Tilordne en varegruppe til den produserte varen. 

   Varegruppen inneholder finanskontoer som gjelder for den produserte varen. Finanskontoen for en produsert vare som har en lagermodell med standard kostpris, omfatter flere produksjonsprisavvik, kostnadsendringsavvik og lagerkostnadsrevalueringen.

3. Tilordne lagermåleenheten til varen. 

   Varens kost uttrykkes alltid i varens lagermåleenhet.

4. Ikke tilordne en kostgruppe til den produserte varer med mindre varen skal behandles som en innkjøpt vare.

5. Tilordne en stykklisteberegningsgruppe til den produserte varen. 

   Varens stykklisteberegningsgruppe definerer advarselsbetingelsene som gjelder. Når en stykklisteberegning er fullført, kan dermed advarslene genereres om mulige kilder for beregningsfeil. En advarselsmelding kan for eksempel angi når en aktiv stykkliste eller rute ikke eksisterer. Stykklisteberegningsgruppen inneholder en stopp nedbryting-regel som angir når en produsert vare skal behandles som en innkjøpt vare.

6. Hvis den produserte varen har konstantkostnader, tilordner du et standard ordreantall til den. 

   Standard ordreantall er en regnskapspartistørrelse for amortisering av konstante kostnader. Eksempler på konstante kostnader omfatter oppstillingstid i ruteoperasjoner og en konstant komponentmengde i stykklisten.

7. Definer stykklisten for den produserte varen. 

   En eller flere stykklisteversjoner kan defineres for en produsert vare. Kontroller at versjonene du vil ha, er markert som godkjent og aktive, og at de gjelder i det datointervallet du vil ha. Stykklisteversjonen kan gjelde for hele firmaet eller bare for området.

8. Definer rutingen for den produserte varen. 

   En eller flere ruteversjoner kan defineres for en produsert vare. Kontroller at versjonene du vil ha, er markert som godkjent og aktive, og at de gjelder i det datointervallet du vil ha. Ruteversjonen kan bare gjelde for området.

Hvis du vil bruke rutinginformasjon til kostnadsformål, kreves det flere klargjøringstrinn. Kostnadskategoriene som er tilordet ruteoperasjoner, må for eksempel korrigeres og fullføres.

## <a name="related-articles"></a>Relaterte artikler

[Amortisere konstante kostnader for en produsert vare](amortize-constant-costs-manufactured-item.md)

[Definere produkter som kan være produsert eller fremskaffet](manufactured-items-treated-as-purchased-items.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]