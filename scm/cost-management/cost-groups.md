---
title: Kostgrupper
description: Kostgrupper gir grunnlaget for segmentering og analyse av kostbidrag i de beregnede kostnadene for en produsert vare, for eksempel kostbidragene for materialer, arbeidskraft og indirekte kostnader. Begrepet "kostgruppesegmentering" har flere synonymer innenfor produksjonsindustrien, for eksempel kostnadsspesifikasjon, nedbryting av kostnader eller kostnadsklassifisering.
author: YuyuScheller
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BOMCostGroup
audience: Application User
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 50871
ms.assetid: 1855f744-f73f-4fa8-8290-a7ee126d368b
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yuyus
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: fb335a521a1a79ea7d978171d233364c58765a0b
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="cost-groups"></a>Kostgrupper

[!include[banner](../includes/banner.md)]


Kostgrupper gir grunnlaget for segmentering og analyse av kostbidrag i de beregnede kostnadene for en produsert vare, for eksempel kostbidragene for materialer, arbeidskraft og indirekte kostnader. Begrepet "kostgruppesegmentering" har flere synonymer innenfor produksjonsindustrien, for eksempel kostnadsspesifikasjon, nedbryting av kostnader eller kostnadsklassifisering. 

Begrepet "kostgruppesegmentering" har flere synonymer innenfor produksjonsindustrien, for eksempel kostnadsspesifikasjon, nedbryting av kostnader eller kostnadsklassifisering. Kostgruppesegmentering kan tjene flere formål. Her er noen eksempler:

-   Segmentering av kostnader for ulike typer materialer, for eksempel ingredienser og emballasjematerialer for hermetikkprodukter, basert på kostgruppene som er tilordnet varene.
-   Segmentering av kostnader for ulike typer operasjonsressurser, for eksempel ulike typer arbeidskraft eller maskiner, basert på kostgruppene som er tilordnet kostnadskategoriene i forbindelse med operasjonsressurser og rutingoperasjoner.
-   Segmentering av kostnader for tiden det tar å konfigurere og kjøre rutineoperasjoner, basert på kostgruppene som er tilordnet kostnadskategorier i forbindelse med rutingoperasjonene.
-   Segmentering av kostnadene for ulike typer indirekte kostnader, for eksempel arbeidsrelaterte og maskinrelaterte indirekte kostnader, basert på kostgrupper som er tilordnet indirekte kostnader i kostarkkonfigurasjonen.
-   Fungerer som grunnlag for beregning av ulike typer administrasjonskostnader i kostarkoppsettet. Dette kan inkludere ulike typer indirekte kostnader i forbindelse med ruting av informasjon om operasjonsressurser, eller informasjon om oppsett og kjøretid. Indirekte produksjonskostnader kan også være relatert til kostbidrag fra komponentmaterialer som gjenspeiler en stram produksjonsfilosofi som eliminerer behovet for ruting av informasjon.

Kostgruppesegmentering gjelder den beregnede kostnaden for en produsert vare uansett om beregningen er basert på standard kostpris eller planlagt kostpris. På **Sammendrag**-siden vises denne segmenteringen etter kostgruppe, etter nivå, eller både kostgruppe og nivå. 

Evnen til å bevare kostgruppesegmentering over flere nivåer i en produktstruktur er kjent som *oppdeling*. Oppdeling gjelder bare produserte varer som bruker en lagermodell med standard kostpris. Uten deling blir kostnadene for en produsert komponent behandlet som materialkostbidrag. Lagerparameteren for nedbryting av kostnader etter underfinansjournal, angir at kostgruppesegmentering vil bli bevart over flere nivåer i standard kostnadsberegning. Mens en policy uten nivåer betyr at kostgruppesegmentering bare gjelder for beregninger på ett nivå. På siden **Opprullet kost per kostgruppe** vises for eksempel kostgruppesegmenteringen over flere nivåer for varer med standard kostpris. 

Kostgruppesegmentering kan også gjelde for avvik for en vare med standard kostpris. En annen lagerparameter definerer om avvik skal identifiseres etter kostgruppe eller kun oppsummeres. 

En kostgruppe kan tilordnes en kostgruppetype og virkemåte for ekstra segmentering.

-   **Kostgruppetype** − Hver kostgruppe må tilordnes en kostgruppetype for å angi at kostgruppen gjelder direkte materialer, direkte produksjon, eller direkte utsetting, eller for å angi den som indirekte eller udefinert. En kostgruppe som er definert som direkte materiale, kan tilordnes varer. En kostgruppe definert som direkte produksjon kan tilordnes kostnadskategorier. En kostgruppe for direkte utsetting kan tilordnes til produkttypen service, slik at du kan klassifisere kostnader tilknyttet serviceinnkjøpet utsettingsaktiviteter. En indirekte kostgruppe kan tilordnes indirekte kostnader som tillegg eller satser. En kostgruppe som er definert som udefinert, kan tilordnes varer, kostnadskategorier eller indirekte kostnader. Tilordning av en kostgruppetype tjener flere hensikter. For det første begrenser det muligheten til å tilordne en kostgruppe og til å vise en liste med aktuelle kostgrupper. For det andre gir det ekstra segmentering til rapportering. For det tredje kan det brukes til å tilordne finanskontoer for avvik.
-   **Virkemåte** − Hver kostgruppe kan, men må ikke, tilordnes en virkemåte for å angi at kostgruppen gjelder faste eller variable kostnader. En kostgruppe som nullverdi for virkemåte, behandles som en variabel kostnad. Tilordning av virkemåte tjener bare rapporteringsformål. Kostnader kan for eksempel vises med segmentering etter faste og variable kostnader i kostarket og på siden **Opprullet kost per kostgruppe**. Hvis du tilordner en fortjenesteinnstillingsprosent til hver kostgruppe, gir stykklisteberegningen en foreslått salgspris basert på kostnader pluss påslag.





