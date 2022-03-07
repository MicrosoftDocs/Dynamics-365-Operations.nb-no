---
title: Kostark
description: Definisjon av kostark innebærer to mål. Som det første målet definerer du formatet for visning av informasjon om kostnader for solgte varer for en produsert vare eller produksjonsordre. Den formaterte visningen kalles et kostark. Som det andre målet definerer du grunnlaget for beregning av indirekte kostnader. Oppsetet av kostarket byger på kostgruppefunksjonen for visning av informasjon og for de indirekte kostnadsberegningsformlene. De to målene for oppsett av etterkalkuleringsark er beskrevet i denne artikkelen.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostSheetDesigner, CostSheetCalculationFactor
audience: Application User
ms.reviewer: kamaybac
ms.custom: 53201
ms.assetid: e7d72b43-3892-49ae-8821-9eede3f4d24a
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34924491b92a043354354d6421df7e9af2dda68d
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5232380"
---
# <a name="costing-sheets"></a>Kostark

[!include [banner](../includes/banner.md)]

Definisjon av kostark innebærer to mål. Som det første målet definerer du formatet for visning av informasjon om kostnader for solgte varer for en produsert vare eller produksjonsordre. Den formaterte visningen kalles et kostark. Som det andre målet definerer du grunnlaget for beregning av indirekte kostnader. Oppsetet av kostarket byger på kostgruppefunksjonen for visning av informasjon og for de indirekte kostnadsberegningsformlene. De to målene for oppsett av etterkalkuleringsark er beskrevet i denne artikkelen. 

Et kostark er den formaterte visningen av informasjon om kostnader for solgte varer for en produsert vare eller produksjonsordre. Når du definerer et kostark, kan du definere formatet for informasjonen og også definere grunnlaget for beregning av indirekte kostnader. Oppsettet av kostarket bygger på kostgruppefunksjonene for visning av informasjon og for formlene som brukes til å beregne indirekte kostnader. Her er mer informasjon om de to målene for oppsett av kostark:
-   **Definer formatet for kostarket.** Det brukerdefinerte formatet for et kostark identifiserer segmenteringen av kostnader som består av en produsert vares kostnader for solgte varer. Varens informasjon om solgte varers kost kan for eksempel segmenteres i materialer, arbeid og indirekte kostnader basert på kostgrupper. Disse kostnadsgruppene er tilordnet til varer, kostnadskategorier for rutingoperasjoner og formler for beregning av indirekte kostnader. Formatet for kostarket krever vanligvis midlertidige totaler når flere kostgrupper er definert. For eksempel samling av flere kostgrupper som tilhører materialet. Definisjonen av et kostarkformat er valgfri, men et kostarkformat må være definert hvis indirekte kostnader skal beregnes.
-   **Definer grunnlaget for beregning av indirekte kostnader.** Indirekte kostnader gjenspeiler produksjon av indirekte kostnader som er knyttet til produksjon av en produsert vare. En formel for beregning av indirekte kostnader kan uttrykkes som et tillegg eller en sats. Et tillegg representerer en prosent av verdien, mens en sats representerer et beløp per time for en rutingsoperasjon. En kostgruppe definerer grunnlaget for beregningsformelen, for eksempel et 100 prosent tillegg for en kostgruppe for en arbeidskostgruppe eller en timespris på NOK 250,00 for en maskinkostgruppe. Hvis du vil definere en beregningsformel og kostgruppegrunnlaget, krever kostarkoppsettet identifikasjon av kostgruppen som representerer de indirekte kostnadene og valget av et tillegg eller en sats.

Hver beregningsformel må angis som en kostnadspost. Kostnadsposten består av en angitt kostnadsversjon, en tilleggsprosent, eller et satsbeløp, kostgruppegrunnlaget, en status og en gyldighetsdato. Når en kostnadspost angis først, har den statusen **Uavsluttet** og en effektiv dato. Når du aktiverer kostnadsposten, oppdateres statusen Aktiv, slik at posten er den gjeldende aktive posten, og den effektive datoen oppdateres til aktiveringsdatoen. Kostnadsposten kan også angi et område for en beregningsformel for et bestemt område. Alternativt kan du la **Område**-feltet stå tomt for å angi at beregningsformelen er en formel for hele firmaet. Kostnadsposten kan også bestå av en angitt vare eller varegruppe når beregningsformelen er merket som en per vare-formel. 

Gjeldende aktive kostnadsposter for beregningsformler for indirekte kostnader, brukes til å estimere produksjonsordrekostnader. De brukes også til å beregne faktiske kostnader som er relatert til faktisk forbruk av tid og materialer. Poster for uavsluttet kostnad brukes i stykklisteberegninger for en fremtidig dato. 

To blokkeringspolicyer for en kostnadsversjon fastslår om uavsluttede kostnader kan vedlikeholdes, og om den uavsluttede kostnaden kan startes. Bruk blokkeringspolicyene for å tillate datavedlikehold og deretter for å hindre datavedlikehold for kostnadsdataene i en kostnadsversjon. 

Når du har definert kostarkformatet og beregninger for indirekte kostnader, må du utføre et eget trinn for å validere og lagre informasjonen. Kostarket representerer et firmaformat for å vise informasjon om kostnadene for solgte varer på en konsekvent måte. 

Kostarket vises som en del av siden **Beregn varekostnad**. Kostarket kan vises for en produsert vares beregnede kostnadspost på **Varepris**-siden, eller for en ordrespesifikk beregningspost på siden **Resultater for stykklisteberegning**  Det kan også vises som en del av **Prisberegning**-siden for en produksjonsordre.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]