---
title: Begrensninger på etterkalkuleringsversjoner for standard kostpris
description: Dette emnet beskriver begrensninger som gjelder for etterkalkuleringsversjoner for standard kostpriser.
author: AndersGirke
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
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9d828e2413a20c4e61d162a31d3c2ed2b18718b
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187680"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Begrensninger på etterkalkuleringsversjoner for standard kostpris

[!include [banner](../includes/banner.md)]

Dette emnet beskriver begrensninger som gjelder for etterkalkuleringsversjoner for standard kostpriser. 

Begrensningene nedenfor sikrer at prinsippene for etterkalkulering av standard kostpriser overholdes:

-  Tillegg må inkluderes i en vares kostnad. Tilleggene for en produsert vare representerer de amortiserte konstante kostnadene i stykkliste- og ruteinformasjon. Derfor må tilleggene inkluderes i enhetskostnaden. Tilleggene for en innkjøpt vare er også inkludert i varens enhetskostnad.

-  Beregning av standard kostpriser for produserte varer må bygge på kostnadspostene i en etterkalkuleringsversjon for standard kostpriser. Alternative kilder til kostnadsdata kan bare brukes sammen med en etterkalkuleringsversjon for planlagte kostnader, for eksempel forretningsavtaler om innkjøpspris for innkjøpte varer. Alternative kilder til kostnadsdata defineres av stykklisteberegningsgruppen.

-  Stykklisteberegninger må utføres med nedbryting på ett enkelt nivå.

Varekostnadsdata for standard kostpriser kan kopieres til en annen etterkalkuleringsversjon som inneholder standard kostpriser eller planlagte kostnader. Imidlertid kan varekostnadsdataene for planlagte kostnader ikke kopieres til en etterkalkuleringsversjon som inneholder standard kostpriser, fordi begrensningene det vises til tidligere i dette emnet, ikke gjelder planlagte kostnader.

## <a name="related-topics"></a>Relaterte emner

[Oversikt over etterkalkuleringsversjoner](costing-versions.md)

[Oppdatere standardkostnader i et ikke-produksjonsmiljø](update-standard-costs-non-manufacturing-environment.md)

[Forberede vedlikehold av standard kostpris for produserte varer](update-standard-costs-manufacturing-environment.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]