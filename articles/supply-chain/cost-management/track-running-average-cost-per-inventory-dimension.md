---
title: Spore glidende gjennomsnitt av kostpris per lagerdimensjon
description: En lagerdimensjonsgruppe er knyttet til hver lagervare. Det glidende gjennomsnittet av kostprisen for en vare beregnes derfor på grunnlag av et utvalg av lagerdimensjoner som spores økonomisk.
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventOnhandItem
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 75053
ms.assetid: 68cc00f4-0f7a-4a7d-be90-8f2e0d0563d3
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: bdf8115bef3b56b9148539b4add95c5b1e8cd9c7
ms.sourcegitcommit: d37fb09101c30858bcb975931b3d8f947d72017b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2569185"
---
# <a name="track-running-average-cost-per-inventory-dimension"></a>Spore glidende gjennomsnitt av kostpris per lagerdimensjon

[!include [banner](../includes/banner.md)]

En lagerdimensjonsgruppe er knyttet til hver lagervare. Det glidende gjennomsnittet av kostprisen for en vare beregnes derfor på grunnlag av et utvalg av lagerdimensjoner som spores økonomisk.

Det finnes tre typer lagerdimensjoner: produkt, lagring og sporing. Produktdimensjonene inkluderer konfigurasjon, størrelse og farge. Produktdimensjoner spores alltid økonomisk. Lagrings- og sporingsdimensjoner omfatter område, lager, sted, lagerstatus, nummerskilt, partinummer og serienummer. Du kan bestemme hvilke lagrings- og sporingsdimensjoner som spores økonomisk. 

**Eksempel 1** 

Hvis lagerdimensjonsgruppen som er knyttet til varen, spores økonomisk etter lager, vil det glidende gjennomsnittet av kostprisen beregnes for hvert lager. Følgende bestillinger er fakturert:

-   En bestilling av et antall på 2 til en kostpris på USD 10,00 er fakturert for lageret HL.
-   En bestilling av et antall på 3 til en kostpris på USD 12,00 er fakturert for lageret HL.
-   En bestilling av et antall på 5 til en kostpris på USD 15,00 er fakturert for lageret ML.

Løpende gjennomsnittlig kostpris for lageret HL er USD 11,20, og den løpende gjennomsnittlige kostprisen for lageret ML er USD 15,00. En salgsordrefaktura posteres for lageret HL. Verdien av lageret og kostnader for solgte varer (før lagerlukking kjøres og uten merking) er USD 11,20. En ny salgsordrefaktura posteres for lageret HL. Verdien av lageret og kostnader for solgte varer (før lagerlukking kjøres og uten merking) er USD 15,00. 

**Eksempel 2** Hvis lagringsdimensjonsgruppen som er knyttet til varen, spores økonomisk etter lager og sporingsdimensjonsgruppen spores økonomisk etter partinummer, blir det glidende gjennomsnittet av kostprisen beregnet for hvert parti. 

**Obs!** Vi anbefaler at du alltid viser kostprisen for alle økonomiske dimensjoner som spores. Følgende bestillinger er fakturert:

-   En bestilling av et antall på 2 til en kostpris på USD 10,00 er fakturert for lageret HL og partiet AAA.
-   En bestilling av et antall på 3 til en kostpris på USD 12,00 er fakturert for lageret HL og partiet AAA.
-   En bestilling av et antall på 2 til en kostpris på USD 15,00 er fakturert for lageret HL og partiet BBB.

Løpende gjennomsnittlig kostpris for lageret HL og parti AAA er USD 11,20, og den løpende gjennomsnittlige kostprisen for lageret ML og parti BBB er USD 15,00.



