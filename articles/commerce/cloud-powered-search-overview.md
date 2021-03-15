---
title: Oversikt over skybaserte søk
description: Dette emnet gir en oversikt over skydrevne søk i Microsoft Dynamics 365 Commerce.
author: ashishmsft
manager: annbe
ms.date: 06/29/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 5a9cb82053640b7abdba420e087d0707208979de
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "4997656"
---
# <a name="cloud-powered-search-overview"></a>Oversikt over skybaserte søk


[!include [banner](includes/banner.md)]

Dette emnet gir en oversikt over skydrevne søk i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Produktoppdaging bidrar til å garantere at kunder raskt og enkelt kan finne produkter ved å bla gjennom kategorier, søke og filtrere. Forhandlere vurderer produktgjenkjenning som et primært verktøy for kundeinteraksjon på tvers av alle kanaler.

Kundene er vant til nesten umiddelbare svartider i websøkemotorer, avanserte webområder for e-handel, sosiale apper, automatiske forslag som vises når de skriver inn søkeord, filterbasert navigasjon og utheving. Hvis kunder ikke finner produktet de leter etter raskt nok i én e-handelsbutikk, vil de ikke nøle med å gå til en annen e-handelsbutikk.

Den skybaserte produktregistreringen i Dynamics 365 Commerce hjelper forhandlere med å fortsette å øke kundelojaliteten og konverteringssatsene på tvers av alle kanaler, både e-handelskanaler og salgsstedskanaler (POS).

Dynamics 365 Commerce-søkeopplevelsen har forbedrede funksjoner for å hjelpe forhandlere med å oppnå bedre produktoppdaging. Samtidig gir disse funksjonene skalerbarheten og ytelsen som kreves for trafikk i e-handel.

## <a name="browse-and-search"></a>Bla gjennom og søke

Søkerelevans og ytelse er nøkkelfaktorer i omnikanalopplevelsen, fordi produktoppdaging hovedsakelig er avhengig av søkefunksjonalitet for informasjonshenting og innholdsnavigasjon. En effektiv bla- og søkeopplevelse bidrar til å øke konverteringen.

Illustrasjonen nedenfor viser et eksempel på vanlig bla- og søkefunksjonalitet.

![Målside for søk](./media/SearchLanding.png)

## <a name="faceted-navigation-and-choice-summary"></a>Filterbasert navigasjon og valgsammendrag 

Filterbasert navigasjon gjør at kundene enklere kan søke etter innhold ved å la dem filtrere på presiseringer som er koblet til termer i et termsett. Når en kunde har valgt og brukt presiseringer, vises et sammendrag av valgene. 

Ved hjelp av filterbasert navigasjon kan du konfigurere ulike presiseringer for ulike termer i et termsett uten å måtte opprette flere sider. 

Illustrasjonen nedenfor viser et eksempel på hvordan filterbasert navigasjon brukes i et søk.

![Valgsammendrag](./media/ChoiceSummary.png)

## <a name="immersive-autosuggest"></a>Dyptgående automatiske forslag

Gjeldende funksjonalitet for automatiske forslag viser bare nøkkelord som utløser et søk etter det samsvarende nøkkelordet. På grunn av nye forbedringer i Dynamics 365 Commerce kan kunder ofte oppdage koblinger til produkter før de er skrevet ferdig.

Dynamics 365 Commerce støtter også funksjonalitet for nøkkelordtreff i ulike kategorier. Med denne funksjonen kan kunder se antallet samsvarende nøkkelord på tvers av kategorier og utløse et søk etter et nøkkelord i andre kategorier.

Illustrasjonen nedenfor viser et eksempel der det brukes dyptgående automatiske forslag.

![dyptgående automatiske forslag](./media/ImmersiveAutoSuggestUX.png)

## <a name="sort"></a>Sorter

Bedre sortering i Dynamics 365 Commerce lar kundene sortere, søke etter og bla gjennom søkeresultater og finjustere dem etter kriterier som pris, produktnavn og produktnummer. Kunder kan også sortere resultatene basert på om et produkt er nytt, bestselgende eller nylig lagt til.

>[!NOTE]
>Disse skydrevne søkefunksjonene er tilgjengelige fra versjon 10.0.8. Kontroller at det under **Handelsparametere > Konfigurasjonsparametere** finnes en oppføring for ProductSearch. UseAzureSearch satt til true. 
![Konfigurasjonsparametere for skydrevet søk](./media/CloudPoweredSearchConfigurationParameters.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over standard kategorimålside og søkeresultatside](category-search-page-overview.md)

[Behandle metadata for søkemotor](manage-seo-metadata.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]