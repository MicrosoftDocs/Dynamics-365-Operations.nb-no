---
title: Begrensninger på etterkalkuleringsversjoner for standard kostpris
description: Denne artikkelen beskriver begrensninger som gjelder for etterkalkuleringsversjoner for standard kostpriser.
author: JennySong-SH
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8c5c00ae8952e2c80d97d039271a6f5c63e9a72f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8867992"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Begrensninger på etterkalkuleringsversjoner for standard kostpris

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver begrensninger som gjelder for etterkalkuleringsversjoner for standard kostpriser. 

Begrensningene nedenfor sikrer at prinsippene for etterkalkulering av standard kostpriser overholdes:

-  Tillegg må inkluderes i en vares kostnad. Tilleggene for en produsert vare representerer de amortiserte konstante kostnadene i stykkliste- og ruteinformasjon. Derfor må tilleggene inkluderes i enhetskostnaden. Tilleggene for en innkjøpt vare er også inkludert i varens enhetskostnad.

-  Beregning av standard kostpriser for produserte varer må bygge på kostnadspostene i en etterkalkuleringsversjon for standard kostpriser. Alternative kilder til kostnadsdata kan bare brukes sammen med en etterkalkuleringsversjon for planlagte kostnader, for eksempel forretningsavtaler om innkjøpspris for innkjøpte varer. Alternative kilder til kostnadsdata defineres av stykklisteberegningsgruppen.

-  Stykklisteberegninger må utføres med nedbryting på ett enkelt nivå.

Varekostnadsdata for standard kostpriser kan kopieres til en annen etterkalkuleringsversjon som inneholder standard kostpriser eller planlagte kostnader. Imidlertid kan varekostnadsdataene for planlagte kostnader ikke kopieres til en etterkalkuleringsversjon som inneholder standard kostpriser, fordi begrensningene det vises til tidligere i denne artikkelen, ikke gjelder planlagte kostnader.

## <a name="related-articles"></a>Relaterte artikler

[Oversikt over etterkalkuleringsversjoner](costing-versions.md)

[Oppdatere standardkostnader i et ikke-produksjonsmiljø](update-standard-costs-non-manufacturing-environment.md)

[Forberede vedlikehold av standard kostpris for produserte varer](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]