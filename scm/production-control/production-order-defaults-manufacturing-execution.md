---
title: "Standardverdier for produksjonsordre i produksjonsutførelse"
description: 
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: JmgProdParameters
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 70073
ms.assetid: 620944ae-3e20-444a-807e-65495f160904
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: b310e799c1ef0756291c5f7ab886531e4caf1945
ms.lasthandoff: 03/31/2017


---

# <a name="production-order-defaults-in-manufacturing-execution"></a>Standardverdier for produksjonsordre i produksjonsutførelse

[!include[banner](../includes/banner.md)]




Du bør nøye vurdere alle innstillingene på siden **Standarder for produksjonsordre** før arbeidere begynner å gjøre registreringer på produksjonsjobber. Hvis firmaet ditt bruker multisite-funksjonaliteten, vil du kanskje definere forskjellige standarder for produksjonsordrer for hvert område. Ordrestandardene for integrasjon med produksjonskontroll defineres i følgende kategorier på siden **Standarder for produksjonsordre**:

-   **Generelt** – generelle ordrestandarder for produksjonsjobber i produksjonsutførelse.
-   **Start** – Ordrestandarder som brukes når produksjonsjobber eller -operasjoner startes.
-   **Operasjoner** – Ordrestandarder som brukes på produksjonsjobber eller -operasjoner og tilbakemeldinger for operasjoner i løpet av produksjonsprosessen.
-   **Rapporter som fullført** - Ordrestandarder som brukes når varer rapporteres som ferdigmeldt i den siste operasjonen for en produksjonsordre.
-   **Antallsvalidering** – Ordrestandarder for validering av start- og tilbakemeldingsantall på produksjonsordrer.

## <a name="types-of-production-jobs"></a>Typer produksjonsjobber
På **Operasjoner** kategorien velger du typene produksjonsjobber som krever registrering på siden **Jobbregistrering**. Vanligvis foretar arbeidere registreringer i oppsettjobber og prosessjobber. Hvis finplanlegging blir brukt, kan du imidlertid velge andre jobbtyper, for eksempel transport-jobber som ansatte også må gjøre registreringer på når en produksjonsordre blir behandlet. **Viktig:** Kontroller at alle relevante jobbtyper velges. Ellers kan det være at jobber ikke er tilgjengelig for registrering på siden **Jobbregistrering**. Juster valgene dine etter valgene som gjøres i **Jobbstyring** kolonnen på siden **Rutegrupper**. Hvis **Jobbstyring** er valgt i rutegruppen, vil jobbtypen rapporteres som ferdigmeldt på produksjonsordren. Denne rapportering skjer når jobben er rapportert som fullført i Produksjonsutførelse. Når alle jobbtyper som **Jobbstyring** er valgt for, er rapportert som fullført for en operasjon, rapporterer Produksjonsutførelse også operasjonen som fullført. **Obs!** Noen jobbtyper kan rapporteres manuelt gjennom produksjonsjournaler. I dette tilfellet velger du **Jobbstyring** for jobben, men ikke velg jobbtypen for registrering i **Operasjoner** kategorien på siden **Standarder for produksjonsordre**.

## <a name="bom-consumption-and-picking-list-journals"></a>Stykklisteforbruk og plukklistejournaler
Materialer kan settes opp slik at de forbrukes automatisk eller manuelt under produksjonen. Automatisk forbruk kontrolleres ved trekkprinsippet som er definert i stykklistlinjene, og innstillingen for feltet **Automatisk stykklisteforbruk** i produksjonsordrestandardene. Automatisk forbruk kan settes opp slik at det skjer når en produksjonsordre startes eller ferdigmeldes. Det kan også oppstå på jobbnivå når en jobb startes eller fullføres.

### <a name="controlling-material-consumption-when-a-production-order-is-started"></a>Kontrollere materialforbruk når en produksjonsordre startes

Materialforbruk under starten av en produksjonsordre styres av feltet **Automatisk stykklisteforbruk** i **Start** kategorien. Følgende verdier er tilgjengelige:

-   **Trekkprinsipp** – Når en produksjonsordre startes, forbrukes mengder av materiale i henhold til trekkprinsippet som er angitt på produksjonsstykklistelinjene. Bare materiallinjer der trekkprinsippet er satt til **Start**, vil bli brukt under produksjonsstart.
-   **Alltid** – materialantall som er proporsjonalt med antall startet, forbrukes alltid.
-   **Aldri** – antall av materialet forbrukes aldri.

### <a name="controlling-material-consumption-when-a-production-job-is-started-or-completed"></a>Kontrollere materialforbruk når en produksjonsjobb startes eller fullføres

Materialforbruk under starten eller fullførelsen av en produksjonsjobb styres av feltet **Automatisk stykklisteforbruk** i **Operasjoner** kategorien. Følgende verdier er tilgjengelige:

-   **Trekkprinsipp** – Når et antall for en produksjonsjobb startes eller fullføres, forbrukes mengder av materiale i henhold til trekkprinsippet som er angitt på produksjonsstykklistelinjene. Bare materiallinjer der trekkprinsippet er satt til **Start** eller **Fullfør**, vil bli brukt under produksjonsstart.
-   **Alltid** – materialantall som er proporsjonalt med antall startet for jobben, forbrukes alltid.
-   **Aldri** – antall av materialet forbrukes aldri.

### <a name="controlling-material-consumption-when-a-production-order-is-reported-as-finished"></a>Kontrollere materialforbruk når en produksjonsordre ferdigmeldes

Materialforbruk under ferdigmeldingsprosessen for en produksjonsordre styres av feltet **Automatisk stykklisteforbruk** i **Ferdigmeld** kategorien. Følgende verdier er tilgjengelige:

-   **Trekkprinsipp** – Når en produksjonsordre ferdigmeldt, forbrukes mengder av materiale i henhold til trekkprinsippet som er angitt på produksjonsstykklistelinjene. Bare materiallinjer der trekkprinsippet er satt til **Fullfør**, vil bli brukt under produksjonsstart.
-   **Alltid** – materialantall som er proporsjonalt med antall som er ferdigmeldt, forbrukes alltid.
-   **Aldri** – antall av materialet forbrukes aldri.





