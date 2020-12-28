---
title: Oversikt over etterkalkuleringsversjoner
description: Denne artikkelen inneholder informasjon om kostnadsversjoner, hvordan du vedlikeholder dem, og hvilke typer data som du kan inkludere dem i. Hovedformålet med en etterkalkuleringsversjon er å inneholde kostnadsposter om varer, kostnadskategorier og beregningsformler for indirekte kostnader.
author: AndersGirke
manager: tfehr
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BOMCalcDialog, BOMCalcTable, CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 54532
ms.assetid: cd239da5-f434-4d1b-8196-5414c888d76d
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: cefee7d678789f462eedbf9f9a3fbc9b591e25a2
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434697"
---
# <a name="costing-versions-overview"></a>Oversikt over etterkalkuleringsversjoner

[!include [banner](../includes/banner.md)]

Denne artikkelen inneholder informasjon om kostnadsversjoner, hvordan du vedlikeholder dem, og hvilke typer data som du kan inkludere dem i. Hovedformålet med en etterkalkuleringsversjon er å inneholde kostnadsposter om varer, kostnadskategorier og beregningsformler for indirekte kostnader.

En etterkalkuleringsversjon kan tjene ett eller flere formål avhengig av dataene som ligger i etterkalkuleringsversjonen. Hovedformålet med en etterkalkuleringsversjon er å inneholde kostnadsposter om varer, kostnadskategorier og beregningsformler for indirekte kostnader. En etterkalkuleringsversjon kan inneholde et sett med standard kostnadsposter, eller et sett med planlagte kostnadsposter som er basert på etterkalkuleringsversjonen som er tilordnet etterkalkuleringsversjonen.

## <a name="costing-versions-for-standard-or-planned-costs"></a>Etterkalkuleringsversjoner for standard kostnader eller planlagte kostnader
### <a name="standard-costs"></a>Standard kostnader

En etterkalkuleringsversjon kan støtte en standard kostnadslagermodell for varer der etterkalkuleringsversjonen inneholder et sett med standard kostnadsposter om varer og produksjonsprosesser. Kostdataene om produksjonsprosesser uttrykkes i kostnadskategorier for rutingsoperasjoner og beregningsformlene for indirekte produksjonskostnader.

### <a name="planned-costs"></a>Planlagte kostnader

En etterkalkuleringsversjon kan inneholde et sett med planlagte kostnadsposter om varer og produksjonsprosesser. En etterkalkuleringsversjon som inneholder planlagte kostnader, brukes ofte til å støtte simuleringer av kostnadsberegning, for eksempel simuleringer av innvirkningen som kostnadsendringer i innkjøpte materialer eller produksjonsprosesser har på beregnede kostnader for produserte varer. Varekostnadspostene for planlagte kostnader kan også brukes til å støtte en faktisk kostnadslagermodell ved å angi de første verdiene for varekostnader. Disse verdiene inkluderer beregningen av planlagte kostnader for produserte varer.

## <a name="entering-costs"></a>Angivelse av kostnader
Datavedlikehold for kostnadsposter i en etterkalkuleringsversjon innebærer angivelse av kostnader for innkjøpte varer og for varer som overføres mellom områder. Ekstra datavedlikehold for produsenter innebærer angivelse av kostnader for kostnadskategorier tilknyttet rutingsoperasjoner, angivelse av beregningsformler for de indirekte kostnadene som gjenspeiler produksjonskostnad, og beregning av kostnader for produserte varer. 

Varekostnadsdataene i en etterkalkuleringsversjon består av én eller flere kostnadsposter for hver vare. Når en varekostnadspost angis først, har den statusen **Uavsluttet** og en beregnet effektiv dato. Når du aktiverer varekostnadsposten, oppdateres statusen **Aktiv**, og den effektive datoen oppdateres til aktiveringsdatoen. Forskjellige varekostnadsposter kan gjenspeile forskjellige områder, ikrafttredelsesdatoer eller statuser. Når du kalkulerer kostnader for produserte varer for en fremtidig dato, bruker stykklisteberegningen kostnadsposter med den relevante effektive datoen, uansett om statusen er **Uavsluttet** eller **Aktiv**. En vares gjeldende aktive kostnadspost blir brukt for beregning av produksjonsordrekostnader og vurdering av lagertransaksjoner under en standard lagermodell for etterkalkulering. Vedlikeholdet av kostnadspostene for kostnadskategorier og formler for indirekte kostnadsberegning ligner vedlikeholdet av varekostnadsposter. 

To blokkeringspolicyer for en kostnadsversjon fastslår om uavsluttede kostnader kan vedlikeholdes, og om den uavsluttede kostnaden kan aktiveres. Bruk blokkeringspolicyene til å tillate datavedlikehold, og deretter til å hindre datavedlikehold for kostnadsposter i en etterkalkuleringsversjon. 

En etterkalkuleringsversjon kan også inneholde data om salgspriser på vare eller innkjøpspriser for stykklisteberegning.

## <a name="item-sales-prices-for-bom-calculations"></a>Salgspriser på vare for stykklisteberegning
Hovedgrunnen til å inkludere data om salgspriser er å beholde en produsert vares beregnede salgspris. Den beregnede salgsprisen kan deretter analyseres for å finne ut hvordan komponenter, ruteoperasjoner og administrasjonskostnader bidrar til kostnads- og salgsprisen. 

En sekundær årsak for å inkludere data om salgspriser er å definere salgsprisposter for komponentvarer. Disse oppføringene kan deretter brukes til å beregne salgsprisen på produserte varer. Du definerer først salgsprismodellen som er innebygd i en stykklisteberegningsgruppe, og tilordner stykklisteberegningsgruppen til innkjøpte varer. Når du utfører stykklisteberegninger med planlagte kostnader, kan du deretter velge kostprismodellen for stykklisteberegningsgruppen. 

Utover dette blir varenes salgsprisposter bare brukt som referanseinformasjon, enten de er lagt inn manuelt eller beregnet. Hvis du aktiverer en vares salgsprispost, kan du oppdatere varens grunnleggende salgspris. Den grunnleggende salgsprisen er ikke stedsbestemt og kan overstyres manuelt. Varens grunnleggende salgspris brukes som en standard salgspris på salgsordrer og salgstilbud.

## <a name="item-purchase-prices-for-bom-calculations"></a>Kjøpspriser på vare for stykklisteberegning
Hovedgrunnen til å aktivere innkjøpsprisdata er å definere innkjøpsprisposter for komponentvarer slik at disse postene kan brukes til å beregne kostnader for produserte varer. Innkjøpsprisposter på vare må angis manuelt. 

Hvis du vil aktivere innkjøpsprisinnhold, kan du først definere en stykklisteberegningsgruppe som inneholder en kostprismodell for varens innkjøpspris, og tilordne stykklisteberegningsgruppen til innkjøpte varer. Du bruker deretter en kostprismodell for stykklisteberegningsgruppen når du utfører stykklisteberegninger med planlagte kostnader til å beregne salgsprisen på produserte varer. 

Innkjøpsprisposter for varer brukes også som referanseinformasjon. Ved å endre statusen for en vares kjøpsprispost fra **Ventende** til **Aktiv** kan du oppdatere varens grunnleggende innkjøpspris. Den grunnleggende kjøpsprisen er ikke stedsbestemt og kan overstyres manuelt. Varens grunnleggende innkjøpspris brukes som en standard innkjøpspris på bestillinger.



