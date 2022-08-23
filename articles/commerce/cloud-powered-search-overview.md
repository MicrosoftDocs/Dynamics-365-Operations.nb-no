---
title: Oversikt over skybaserte søk
description: Denne artikkelen gir en oversikt over skydrevne søk i Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 02/28/2022
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.assetid: ''
ms.openlocfilehash: ed80ff42ea5c6e6a904ea2855953d006f66aad37
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273673"
---
# <a name="cloud-powered-search-overview"></a>Oversikt over skybaserte søk

[!include [banner](includes/banner.md)]

Denne artikkelen gir en oversikt over skydrevne søk i Microsoft Dynamics 365 Commerce.

Produktoppdaging bidrar til å garantere at kunder raskt og enkelt kan finne produkter ved å bla gjennom kategorier, søke og filtrere. Forhandlere betrakter produktoppdagelse som et primært verktøy for kundeinteraksjon på tvers av kanaler basert på CSU (Cloud Scale Unit), for eksempel e-handel og salgssted.

Kundene er vant til nesten umiddelbare svartider i websøkemotorer, avanserte webområder for e-handel, sosiale apper, automatiske forslag som vises når de skriver inn søkeord, filterbasert navigasjon og utheving. Hvis kunder ikke raskt finner produktet de ser etter i én e-handelsbutikk, nøler de ikke med å gå til en annen e-handelsbutikk.

Den skybaserte produktoppdagelsen i Commerce hjelper forhandlere med å fortsette å øke kundelojaliteten og konverteringssatsene på tvers av kanaler basert på CSU.

Commerce-søkeopplevelsen har forbedrede funksjoner for å hjelpe forhandlere med å oppnå bedre produktoppdagelse. Samtidig gir disse funksjonene skalerbarheten og ytelsen som kreves for trafikk i e-handel.

## <a name="browse-and-search"></a>Bla gjennom og søke

Søkerelevans og ytelse er nøkkelfaktorer i omnikanalopplevelsen, fordi produktoppdaging hovedsakelig er avhengig av søkefunksjonalitet for informasjonshenting og innholdsnavigasjon. En effektiv bla- og søkeopplevelse bidrar til å øke konverteringen.

Illustrasjonen nedenfor viser et eksempel på vanlig bla- og søkefunksjonalitet.

![Målside for søk.](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Filterbasert navigasjon og valgsammendrag 

Filterbasert navigasjon gjør at kundene enklere kan søke etter innhold ved å la dem filtrere på presiseringer som er koblet til termer i et termsett. Når en kunde har valgt og brukt presiseringer, vises et sammendrag av valgene. 

Ved hjelp av filterbasert navigasjon kan du konfigurere ulike presiseringer for ulike termer i et termsett uten å måtte opprette flere sider. 

Illustrasjonen nedenfor viser et eksempel på hvordan filterbasert navigasjon brukes i et søk.

![Valgsammendrag.](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Dyptgående automatiske forslag

Gjeldende funksjonalitet for automatiske forslag viser nøkkelord som utløser et søk etter det samsvarende nøkkelordet. På grunn av nye forbedringer i Commerce kan kunder ofte oppdage koblinger til produkter før de er skrevet ferdig.

Commerce støtter også funksjonalitet for nøkkelordtreff i ulike kategorier. Med denne funksjonen kan kunder se antallet samsvarende nøkkelord på tvers av kategorier og utløse et søk etter et nøkkelord i andre kategorier.

Illustrasjonen nedenfor viser et eksempel der det brukes dyptgående automatiske forslag.

![dyptgående automatiske forslag.](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Sorter

Sorteringsfunksjoner lar kundene sortere, søke etter og bla gjennom kategoriresultater og finjustere dem etter kriterier som pris, produktnavn og produktnummer. Hvis du aktiverer [Produktanbefalinger](product-recommendations.md) i miljøet ditt, kan kundene også sortere resultater basert på avanserte sorteringskriterier som nye, bestselgere og trendy.


> [!NOTE]
> Disse skydrevne søkefunksjonene er tilgjengelige fra versjon 10.0.8. Kontroller at det finnes en oppføring for ProductSearch.UseAzureSearch i **Handelsparametere > Konfigurasjonsparametere**, og at true er angitt for denne oppføringen. 
![Konfigurasjonsparametere for skydrevet søk.](./media/CloudPoweredSearchConfigurationParameters.png)
>Avanserte sorteringsalternativer som nye, bestselgere og trendy er tilgjengelige med Commerce SSK-versjonen av 9.35+ og Dynamics 365 Commerce 10.0.20-utgaven.  


## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over standard kategorimålside og søkeresultatside](category-search-page-overview.md)

[Behandle metadata for søkemotor](manage-seo-metadata.md)


[!INCLUDE [footer-include](../includes/footer-banner.md)]
