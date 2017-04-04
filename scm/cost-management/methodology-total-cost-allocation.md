---
title: Fordelingsmetode for totalkostnader
description: "Denne artikkelen inneholder retningslinjer for bruk av total kostnadsfordeling (TKF). TKF er en metode for å beregne kostnaden mellom hovedformelvaren for en partiordre og koproduktene som er definert for formelen."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: BOMConsistOf, PmfFormulaCoBy
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 83852
ms.assetid: 7c14c3e5-9476-4a79-a210-e77fc91cc7fc
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9ccbe5815ebb54e00265e130be9c82491aebabce
ms.openlocfilehash: c26dcc5a8caa461bce90f931bb5c584f1816526b
ms.lasthandoff: 03/31/2017


---

# <a name="total-cost-allocation-method"></a>Fordelingsmetode for totalkostnader

Denne artikkelen inneholder retningslinjer for bruk av total kostnadsfordeling (TKF). TKF er en metode for å beregne kostnaden mellom hovedformelvaren for en partiordre og koproduktene som er definert for formelen.

Totalkostnadfordeling (TKF) er en metode for å beregne kostnaden mellom hovedformelvaren for en partiordre og koproduktene som er definert for formelen. Denne metoden er dynamisk. Den beregner kostnaden som et veid gjennomsnitt mellom antallene som er ferdigmeldt for formelvaren, og koproduktene. Når TKF brukes, slipper du å se gjennom kostnadsfordelinger for hver partiordre. Hvis TKF ikke brukes, bruker formelberegningen eksisterende funksjonalitet.

## <a name="using-tca-for-coproducts"></a>Ved hjelp av TCA for coproducts
Her er noen retningslinjer for bruk av TKF for koprodukter:

-   Hvis du setter gllidebryteren **Total kostnadsfordeling** til **Ja** for en formelversjon, må koprodukter må ha en kostpris som er større enn 0 (null). Verdien kan hentes fra den aktive kostnadsversjonen for det samme området, eller for det første området for en formel som ikke er områdespesifikk. Denne betingelsen blir validert når formelen er godkjent.
-   Hvis du setter glidebyrteren **Total kostnadsfordeling** til **Ja** for formelversjonen og følgende betingelser er oppfylt, er metoden for kostnadsfordeling **TKF**, og prosenten av kostnadsfordeling er uendret:
    -   Du har lagt til koprodukter.
    -   Du har brukt en annen kostnadsfordelingsmetode for koproduktene.
-   Hvis du setter glidebyrteren **Total kostnadsfordeling** til **Nei** for formelversjonen og følgende betingelser er oppfylt, endres er etoden for kostnadsfordeling til **Manuell**, og prosenten av kostnadsfordeling er uendret:
    -   Du har lagt til koprodukter.
    -   Prosenten av kostnadsfordelingen er mer enn 0 (null).
-   Før du kan utføre en formelberegning, må du beregne prosentene for kostnadsfordeling. Du kan fullføre dette trinnet manuelt eller ved hjelp av **Estimer kost**-alternativet på **Koprodukter**-siden. **Obs!** **Estimer kost**-alternativet er bare tilgjengelig når glidebryteren **Total kostnadsfordeling** er satt til **Ja** for formelversjonen. Du kan vise den forventede fordelingen hvis partiordreantallene som er rapportert som ferdige, samsvarer med antallene som vises i formelen.
-   Når en partiordre opprettes manuelt eller en planlagt partiordre blir autorisert, kopieres verdien for glidebryteren **Total kostnadsfordeling** for formelversjonen til partiordren. Du kan imidlertid endre denne innstillingen på partiordren. Hvis gliebryteren **Total kostnadsfordeling** er satt til **Nei** for formelversjonen og deretter endres til **Ja** for partiordren, endres metoden for kostnadsfordeling for hver linje som er satt til **Manuell**, til **TKF**. Kostnadsfordelingen **Ingen** forblir uendret. Hvis glidebryteren **Total kostnadsfordeling** er satt til **Ja** for formelversjonen og deretter endres til **Nei** for partiordren, endres metoden for kostnadsfordeling for hvert koprodukt som er satt til typen **Produksjon**, til **Manuell**. Enhver beregnet prosent for kostnadsfordeling forblir uendret.
-   Siden **Kostnadsfordeling for koprodukt** viser den beregnede kostnadsfordelingsprosenten. Du kan åpne denne siden fra **Partiordre**-siden. Denne informasjonen er nyttig når produktene og antallene som er rapportert, er forskjellig fra de planlagte eller påbegynte antallene i partiordren. Når kostnaden er fullført, vises disse nye prosentvise fordelingene fra TKF på siden **Kostnadsfordeling for koprodukt**.

## <a name="calculating-the-burden-for-byproducts"></a>Beregning av byrde for biprodukter borte
Feltet **Kostnadsfordeling for biprodukt** på **Koprodukter**-siden er et opplistingsfelt som bare brukes for biprodukter. For koprodukter er verdien i dette feltet alltid **Ingen**. For biproduktlinjer bestemmer dette feltet hvordan kostnadsbeløpet for biproduktlinjen blir lagt til den totale kostnaden for produksjonen. Følgende alternativer er tilgjengelige:

-   **Ingen** – Intet beløp blir lagt til den totale kostnaden for produksjonen for denne biproduktlinjen.
-   **Prosent** – Kostnadsbeløpet beregnes som en prosentdel av totalkostnadene for råvarene som forbrukes i produksjonen. Prosentverdien som skal brukes for beregningen, angis i feltet .
-   **Per serie** – Kostnadsbeløpet beregnes som et beløp per standard partistørrelse for produksjonsordren. Dette beløpet er uavhengig av det rapporterte antallet i produksjonen. Beløpet som skal brukes for beregningen, angis i feltet .
-   **Per antall** – Kostnadsbeløpet beregnes som et beløp per rapporterte antall av formelvaren i produksjonen. Beløpet som skal brukes for beregningen, angis i feltet .



