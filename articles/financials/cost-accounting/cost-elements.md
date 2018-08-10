---
title: Kostnadselementdimensjoner
description: "Som en av de viktige søylene i kostnadsregnskap, brukes kostnadelementdimensjoner til å kategorisere og spore hvor kostnadene flyter til."
author: AndersGirke
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimension
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 223204
ms.assetid: 1eda0e62-760b-4737-9dfd-3c3c38d80c1a
ms.search.region: global
ms.author: shylaw
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 0f47c75b6f6f4533501070f78698de82cf70f9bd
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="cost-element-dimensions"></a>Kostnadselementdimensjoner

[!include [banner](../includes/banner.md)]

Som en av de viktige søylene i kostnadsregnskap, brukes kostnadelementdimensjoner til å kategorisere og spore hvor kostnadene flyter til. 

Et kostnadselement tilsvarer et kostnadsrelevant element i kontoplanen. I utgangspunktet kan det være en hvilken som helst type element på laveste nivå i et firma der kostnadene kan flyte til. Kostnadselementene som konsept strekker seg fra finanskontoer til alle kostnadsrelevante ressurser. Kostnadsregnskap støtter for øyeblikket finanskontoer.

## <a name="two-types-of-cost-elements"></a>To typer kostnadselementer
Det finnes to typer kostnadselementer: primære kostnadselementer og sekundære kostnadselementer. I tabellen nedenfor beskrives forskjellen mellom de to typene.

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><strong>Primære kostnadselementer</strong></td>
<td><strong>Sekundærkostnadselementer</strong></td>
</tr>
<tr class="even">
<td>De primære kostnadselementer representerer kostflyten fra finansbokføring til kostnadsregnskap. Kostnadselementstrukturen tilsvarer kontostrukturen for resultat i økonomimodulen, der en kostnadselement kan tilsvare en hovedkonto. Ikke alle hovedkontoer vil nødvendigvis vises som kostnadselementer avhengig av forretningsbehovene. Eksempler på primære kostnadselementer:
<ul>
<li>Solgte varers kost (COG-er)</li>
<li>Indirekte materialkostnader</li>
<li>Personalkostnader</li>
<li>Energikostnader</li>
</ul></td>
<td>Sekundære kostnadselementer representerer kostflyten internt fordi disse kostnadene opprettes og brukes bare i kostnadsregnskap. De brukes til å sikre at kilden til kostnadene kan spores. Disse kostnadselementene brukes i kostnadsfordelinger og beregninger for indirekte kostnader. Eksempler på sekundære kostnadselementer:
<ul>
<li>Produksjonskostnader</li>
<li>Produksjon, materiale og administrasjonskostnader for markedsføring</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="cost-element-dimensions-and-cost-element-dimension-members"></a>Kostnadselementdimensjoner og medlemmer av kostnadselementdimensjonen
Kostnadselementer kalles *kostnadselementdimensjoner* . De enkelte dimensjonsverdiene kalles *medlemmer av kostnadselementdimensjon*. Du har for eksempel en amerikansk kontoplanstruktur (COA) som er grunnlaget for den lovbestemte rapporteringen. Denne kontoplanen brukes som kostnadselementdimensjon. Kontoene, som er primært kostnadselementer, representeres som medlemmer av kostnadselementdimensjon i kostnadsregnskap. Følgende skjermbilde viser et eksempel på hovedkontoer som kostnadselementdimensjonen med de faktiske hovedkontoene som medlemmene av kostnadselementdimensjonen. 

[![kostnad-element-dimensjoner](./media/cost-element-dimensions.png)](./media/cost-element-dimensions.png)

## <a name="import-cost-element-dimension-members-through-data-connectors"></a>Importere medlemmer av kostnadselementdimensjon gjennom datakoblinger
For å forenkle oppsettet av medlemmene av kostnadselementdimensjoner i kostnadsregnskap, kan du bruke datakoblinger som er forhåndsbygget eller bygge dine egne for å hente de primære kostnadselementer fra ett eller flere kildesystemer.

## <a name="implementation-considerations"></a>Informasjon om implementering
Når kostnadselementer representerer det laveste nivået av kostnadsdetaljer, må du kontrollere at alle kostnadselementer som er nødvendig for å lage lederrapporteringen er tatt med når du implementerer kostnadselementstrukturen. Det kan være vanskelig å finne et passende antall kostnadselementer for kostnadskontroll. Når du har tusenvis av kostnadselementer, kan det være vanskelig å styre hvert kostnadselement. Du kan eventuelt gruppere kostnadselementer og styre kostnadskontroll på et aggregert nivå.




