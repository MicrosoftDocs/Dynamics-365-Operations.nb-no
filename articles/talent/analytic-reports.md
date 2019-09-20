---
title: Bruke analyserapporter i Microsoft Dynamics 365 for Talent - Attract
description: Dette emnet beskriver analyserapportene for å få innsikt i ansettelsesprosesser i Microsoft Dynamics 365 for Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: f69c45e885d789d05a081064f30ccd6ce6bfec52
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2019
ms.locfileid: "1742895"
---
# <a name="use-analytic-reports"></a>Bruke analyserapporter

Analyserapporter i Attract har en standardløsning for å få innsikt i ansettelsesprosesser. Tilgjengelige funksjoner omfatter:

- **Jobbanalyse:** Klikk på kategorien **Analyse** i en jobb for å vise målene for jobbens søkere.
- **Analysehub:** Klikk på **Analyse** i venstre navigasjon for å vise aggregerte mål på tvers av jobber.
- **Brukerspesifikk sikkerhet:** – Tilgang til rapporter er underlagt Attract-[rollen](security-attract.md) og jobbdeltakerrollen.
- **Kryssfiltrering:** Klikk på visuelle effekter i en rapport for å vise andre mål filtrert etter valgte data.

>[!NOTE] 
>- Denne funksjonen er for øyeblikket i [forhåndsvisning](access-preview-feature.md). Hvis du vil prøve den, må du ha [**tillegget for omfattende ansettelse**](attract-comprehensive-hiring.md).
>- Alle offentlige forhåndsvisningsrapporter vises på engelsk.
>- Rapporter oppdateres hver 3. time. Det siste oppdateringstidspunktet (i den lokale tidssonen) er plassert øverst i rapporten. Oppdateringstidene er tilnærmet og varierer avhengig av datavolum og ressursbelastning i ditt område.

## <a name="job-analytics"></a>Jobbanalyse

Jobbanalyse-rapporter er et øyeblikksbilde av ansettelsesprosessen for en jobb.  Viktige mål omfatter:

- Aktive søkere etter stadium
- Søkerkilde
- Søkertype (intern eller ekstern)

## <a name="analytics-hub"></a>Analysehub

Analysehub rapporterer samlede data på tvers av jobber for å oppdage trender i ansettelsesprosessen. Attract omfatter to standardrapporter: Sammendrag av pipeline og traktanalyse.

### <a name="pipeline-summary"></a>Sammendrag av pipeline

Rapporten Sammendrag av pipeline samler data for åpne jobber. Viktige mål omfatter:

- Søkere på tvers av alle jobber etter stadium
- Søkerkilde
- Åpne jobber etter ansiennitetsnivå

### <a name="funnel-analysis"></a>Traktanalyse

Rapporten Traktanalyse samler data for jobber som er lukket som besatt. Viktige mål omfatter:

- Tiden det tar å ansette
- Konverteringsmål (ved peking)
- Frekvens for å godta tilbud

Obs! For rapportering av mest mulig nøyaktig tid det tar å ansette, anbefales det at du bruker [Tilbudsbehandling](offer-setup.md), en funksjon som er tilgjengelig i tillegget for omfattende ansettelse.

>[!TIP] 
>Prøv å holde pekeren over visuelle effekter for mer informasjon. Hvis du for eksempel holder pekeren over de visuelle effektene for **Aktive søkere**, vises de gjennomsnittlige dagene i stadium. Ved å analysere denne informasjonen kan du få innsikt som er viktig for å redusere tiden det tar å ansette, og rekrutterere kan fokusere på måter de kan redusere tiden som brukes i hvert stadium.

## <a name="user-specific-security"></a>Brukerspesifikk sikkerhet

Attract-rapporter er tilgjengelige for Administrator-, Les alt-, Rekrutterer- og Ansettelsesansvarlig-[rollene](security-attract.md). Ikke-tilordnede brukere har ikke tilgang til noen av analyserapportsidene (Jobbanalyse eller Analysehub).

Jobbanalyse-rapporter viser data for den valgte jobben. Analysehub-rapporter samler data på tvers av alle jobber som en bruker kan vise. Brukere som kan vise både Mine jobber og Alle jobber på jobbsiden, har de samme visningene tilgjengelig i Analysehub.

## <a name="cross-filter"></a>Kryssfilter

En av de flotte funksjonene i Power BI er måten alle visuelle effekter på en rapportside er sammenkoblet på. Hvis du velger et datapunkt i en av de visuelle effektene, endres alle de andre visuelle effektene på siden som inneholder disse dataene, basert på det merkede området. Finn ut mer og se et eksempel i [Hvordan visuelle effekter kryssfiltrerer hverandre i en Power BI-rapport](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).

## <a name="export-to-excel"></a>Eksporter til Excel

Hvis du vil vise rapportdata i Excel, kan du klikke på Alternativer-menyen (tre prikker) i en visuell effekt og velge **Eksporter underliggende data**. Eksporterte data eksporteres som filtrert, og brukertillatelser i Attract respekteres. Hvis du vil ha mer informasjon, kan du se [Eksportere data fra visuelle effekter](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).
