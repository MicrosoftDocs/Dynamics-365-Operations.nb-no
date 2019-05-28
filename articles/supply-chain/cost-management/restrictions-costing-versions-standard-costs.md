---
title: Begrensninger på etterkalkuleringsversjoner for standard kostpris
description: Dette emnet beskriver begrensninger som gjelder for etterkalkuleringsversjoner for standard kostpriser.
author: AndersGirke
manager: AnnBe
ms.date: 01/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.industry: Manufacturing
ms.author: aevengir
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c0383f78ea5cfa42183e0bfe8a96d7d3866766e7
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1547728"
---
#  <a name="restrictions-on-costing-versions-for-standard-costs"></a>Begrensninger på etterkalkuleringsversjoner for standard kostpris

[!include [banner](../includes/banner.md)]

Dette emnet beskriver begrensninger som gjelder for etterkalkuleringsversjoner for standard kostpriser. 

Begrensningene nedenfor sikrer at prinsippene for etterkalkulering av standard kostpriser overholdes:

-  Tillegg må inkluderes i en vares kostnad. Tilleggene for en produsert vare representerer de amortiserte konstante kostnadene i stykkliste- og ruteinformasjon. Derfor må tilleggene inkluderes i enhetskostnaden. Tilleggene for en innkjøpt vare er også inkludert i varens enhetskostnad.

-  Beregning av standard kostpriser for produserte varer må bygge på kostnadspostene i en etterkalkuleringsversjon for standard kostpriser. Alternative kilder til kostnadsdata kan bare brukes sammen med en etterkalkuleringsversjon for planlagte kostnader, for eksempel forretningsavtaler om innkjøpspris for innkjøpte varer. Alternative kilder til kostnadsdata defineres av stykklisteberegningsgruppen.

-  Stykklisteberegninger må utføres med nedbryting på ett enkelt nivå.

Varekostnadsdata for standard kostpriser kan kopieres til en annen etterkalkuleringsversjon som inneholder standard kostpriser eller planlagte kostnader. Imidlertid kan varekostnadsdataene for planlagte kostnader ikke kopieres til en etterkalkuleringsversjon som inneholder standard kostpriser, fordi begrensningene det vises til tidligere i dette emnet, ikke gjelder planlagte kostnader.

<a name="related-topics"></a>Relaterte emner
--------

[Etterkalkuleringsversjoner](costing-versions.md)

[Oppdatere standardkostnader i et ikke-produksjonsmiljø](update-standard-costs-non-manufacturing-environment.md)

[Forberede vedlikehold av standard kostpris for produserte varer](update-standard-costs-manufacturing-environment.md)

