---
title: "Vise og evaluere resultatene i et spørreskjema"
description: "Dette emnet forklarer hvordan du kan vise og evaluere resultatene av spørreskjemaer som respondenter fyller ut."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KMCollection, KMKnowledgeCollectorCollection, KMKnowledgeCollectorUserResults
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17444
ms.assetid: 6570206a-b2c4-4025-8715-432fe6652b78
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: b7c4a612d54f3ae8967be930c0b98e4783fd8200
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# Vise og evaluere resultatene i et spørreskjema
<a id="view-and-evaluate-the-results-of-a-questionnaire" class="xliff"></a>

[!include[banner](includes/banner.md)]


Dette emnet forklarer hvordan du kan vise og evaluere resultatene av spørreskjemaer som respondenter fyller ut. 

Etter at respondentene har fylt ut et spørreskjema, kan du vise og evaluere spørreskjemaresultatene på følgende måter:

-   **Fullførte svarøkter** – Vis informasjon om spørreskjemaene som respondentene har fylt ut, og generer rapporter for å oppsummere svar og eventuelle poeng de har fått.
-   **Resultatgrupper** – Vis resultatgruppedetaljer og -statistikk for spørreskjemaer. Resultatgruppestatistikk kan genereres for én svarøkt i et spørreskjema eller alle svarøkter.
-   **Spørreskjemastatistikk** – Angi vilkår for å beregne statistikk for en bestemt gruppe med respondenter.

Du kan også generere ulike rapporter for å vise resultater som er sortert etter person, svarøkt eller resultatgruppe. Følgende rapporter som er knyttet til utfylte spørreskjemaer, er tilgjengelige:

-   Svar
-   Svar per spørreskjema
-   Svar per person
-   Tilbakemeldingsanalyse

## Resultater fra svarøkt
<a id="answer-session-results" class="xliff"></a>
Etter at respondentene har fylt ut et spørreskjema, kan du vise resultatene fra de fullførte svarøktene. En svarøkt er én brukers svar på et spørreskjema. Du kan vise detaljer om fullførte svarøkter på **Svar**-siden. Svarøktene som er inkludert på **Svar**-siden, filtreres på ulike måter avhengig av hvordan du åpner siden:

-   Alle spørreskjemaer
-   Et bestemt spørreskjema
-   En bestemt person

På **Svar**-siden kan du vise detaljer om svar, poeng respondenten har fått, svar fra en respondent i hver resultatgruppe og spørsmålshierarkiet som ble brukt på det valgte spørreskjemaet, hvis et spørsmålshierarki ble brukt. Du kan også generere og skrive ut følgende rapporter:

-   **Resultatrapport** – Denne rapporten viser en grafisk representasjon av poengene som ble oppnådd per resultatgruppe for den valgte svarøkten.
-   **Svarrapport** – Denne rapporten viser svarene som respondenten valgte for hvert spørsmål i spørreskjemaet.
-   **Feil svar** – Denne rapporten viser informasjon som er knyttet til de uriktige svarene som respondenten har valgt.

> **Obs! **
>   **Resultater**-rapporten er bare tilgjengelig hvis du bruker resultatgrupper i spørreskjemaet, og hvis du har valgt **Resultatside** på **Spørreskjemaer**-siden. **Svar**-rapporten og **Feil svar**-rapporten er bare tilgjengelige hvis du har valgt **Svarrapport** på **Spørreskjemaer**-siden.

## Spørreskjemastatistikk
<a id="questionnaire-statistics" class="xliff"></a>
Du kan bruke spørreskjemastatistikk til å analysere resultatene av et utfylt spørreskjema, basert på beregninger du definerer. Hvis du vil definere beregninger, må du utføre følgende oppgaver:

-   Velg kriterier for å beregne og vise statistikken.
    -   Du kan vise statistikk per spørreskjema, spørsmål, spørsmålsrader eller resultatgrupper.
    -   Velg diagramtypen som skal brukes når du viser resultatene.
    -   Velg typene personer fra nettverket, for eksempel ansatte, kontaktpersoner eller søkere, du vil ta med svar for. Du kan også ta med svar fra spørreskjemaer som ble fylt ut anonymt.
    -   Definer intervaller som er basert på alder eller ansiennitet for å analysere resultater.
-   Velg eller kontroller innstillinger som innsnevrer temaet for statistikken. Når du velger et postnummer, kan du for eksempel analysere resultatene for alle respondentene innenfor et bestemt geografisk område.
-   Velg eller kontroller vilkår for å analysere resultatene etter respondent eller spørreskjemaets kjennetegn. Hvis du for eksempel velger **Postnummer**, kan du analysere sammenhengen mellom respondentens plassering og riktige svar.

Innstillingene du definerer, lagres og kan brukes til å beregne resultatene på nytt periodisk.

Se også
<a id="see-also" class="xliff"></a>
--------

[Utforme spørreskjemaer](design-questionnaires.md)

[Bruke spørreskjemaer](questionnaires.md)

[Distribuere og fylle ut spørreskjemaer](distribute-questionnaires.md)



