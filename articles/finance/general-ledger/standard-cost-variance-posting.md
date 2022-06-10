---
title: Avvik i standardkostnad, postering
description: Dette emnet gir informasjon om hvordan du konfigurerer posteringsprofiler for standardkostnad.
author: rachelprofitt
ms.date: 04/25/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: InventPosting, InventItemGroup
audience: Application User
ms.search.region: Global
ms.author: raprofit
ms.openlocfilehash: bc4f1bd7c1bf7a8f214f20460b10d371d8f3c790
ms.sourcegitcommit: 1ea145dc606e243c7f51d91a5c0dd9e385bbda4a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/25/2022
ms.locfileid: "8804613"
---
# <a name="standard-cost-variance-posting"></a>Avvik i standardkostnad, postering

Når du bruker standardkostnad for én eller flere produkter i organisasjonen, må du konfigurere [forutsetningene for standard etterkalkulering](/supply-chain/cost-management/prerequisites-standard-costs.md). Dette emnet beskriver posteringskontoene som kreves for trinn 3 av forutsetningene, "Tilordne finanskontoer til vareposteringer som er relatert til avvik i standard kostpris."

Det kan forekomme forskjellige typer avvik for innkjøp og produksjonsordrer. Hvis du vil ha eksempler på produksjonsavvik, kan du se [Vanlige kilder til produksjonsavvik](/supply-chain/cost-management/common-sources-of-production-variances.md). Det oppstår avvik i kjøpsordrepris når du bruker standardkostnad for en innkjøpt vare, og det er en forskjell mellom produktets standardkost og det fakturerte beløpet på bestillingen.

## <a name="sample-posting-profile-configuration"></a>Eksempel på konfigurasjon av posteringsprofil

Følgende tabell viser eksempler på standard posteringstyper. Det inkluderer eksempelkontoer og beskrivelser.

- Kolonnen «Debet/kredit?» kolonnen angir om transaksjonen vanligvis er debet eller kredit. I noen tilfeller kan transaksjonen postere enten et debet- eller en kreditbeløp.
- "Avregningskonto"-kolonnen angir at posteringstypen er en avregningskonto. Beløpet er med andre ord postert i denne kontoen, blir automatisk tilbakeført når en senere transaksjon posteres.
- Kolonnen "P/F" angir posteringstypen. "P" representerer fysisk postering, og "F" representerer økonomisk postering.
- "Følg"-kolonnen angir om hovedkontoen for en posteringstype vanligvis er den samme som hovedkontoen for en annen posteringstype. Mer bestemt angir det posteringstypen som vanligvis brukes.

> [!NOTE]
> Hovedkontoene og hovedkontonavnene i tabellen er forslag. Vi anbefaler at du samarbeider med regnskapsføreren for å fastsette den beste konfigurasjonen for forretningsbehovet ditt.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | F/Ø | Følg | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-----|--------|-------------|
| Avvik i kjøpspris | 510310 | Avvik i kjøpspris | Utgift | Enten | Nei | F | Gjelder ikke her | Denne kontoen brukes når det er avvik mellom innkjøpsprisen og standard kostpris på en bestilling. |
| Lagerkostrevaluering | 510330 | Lagerkostrevaluering | Utgift | Enten | Nei | F | Gjelder ikke her | Denne kontoen brukes når en ny kostnadsversjon aktiveres for en standard kostprisvare for å vurdere lagerbeholdningen på nytt. |
| Kostendringsavvik | 510320 | Kostendringsavvik | Utgift | Enten | Nei | F | Gjelder ikke her | Denne kontoen brukes når det er forskjell i standardkostnader mellom områder, eller når en vare returneres og det er en endring mellom den opprinnelige standardkosten og gjeldende standardkostnad for et produkt. |
| Partistørrelsesavvik for produksjon | 510370 | Partistørrelsesavvik for produksjon | Utgift | Enten | Nei | F | Gjelder ikke her | Denne kontoen brukes når det er forskjeller mellom beregningsgrunnlaget for stykklisten og det faktiske antallet for beregningen av produksjonsordrekostnaden. |
| Avvik i produksjonspris | 510340 | Avvik i produksjonspris | Utgift | Enten | Nei | F | Gjelder ikke her | Denne kontoen brukes når det er prisdifferanser mellom den estimerte kostnaden og den faktiske kostnaden for en produksjonsordre. |
| Avvik for produksjonsantall | 510350 | Avvik for produksjonsantall | Utgift | Enten | Nei | F | Gjelder ikke her | Denne kontoen brukes når det er antallsdifferanser mellom den estimerte kostnaden og den faktiske kostnaden for en produksjonsordre. |
| Erstatningsavvik for produksjon | 510360 | Erstatningsavvik for produksjon | Utgift | Enten | Nei | F | Gjelder ikke her | Denne kontoen brukes når det er uventet forbruk på en produksjonsordre. |
| Avrundingsavvik | 618160 | Avrundingsdifferanse | Utgift | Enten | Nei | F | Gjelder ikke her | Denne kontoen brukes når det er en avrundingsdifferanse når produksjonskostnadene beregnes fra standardkostnadene. |
