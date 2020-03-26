---
title: Velge bort personlige produktanbefalinger
description: Dette emnet beskriver hvordan du kan la kundene velge bort mottak av personlige anbefalinger i Microsoft Dynamics 365 Commerce.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: a6d2388e863135c2b6d51af915b606a56f0603a8
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127750"
---
# <a name="opt-out-of-personalized-recommendations"></a>Velge bort personlige produktanbefalinger

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du kan la kundene velge bort mottak av personlige anbefalinger i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Under kontooppretting konfigureres nye kunder automatisk for å motta personlige anbefalinger. Dynamics 365 Commerce har imidlertid flere metoder som forhandlere kan bruke til å la brukere velge bort mottak av disse anbefalingene og begrense behandlingen av sine personlige data. Godkjente brukere som velger bort mottak av personlige anbefalinger, vil umiddelbart stoppe å se personlige lister. I tillegg vil alle personlige data som samles inn for personlig tilpasning, bli fjernet fra tilpassede anbefalingsmodeller.

Hvis du vil ha mer informasjon om tilpassede produktanbefalinger, kan du se [Aktivere tilpassede anbefalinger](personalized-recommendations.md).

## <a name="ways-for-retailers-to-implement-an-opt-out-experience"></a>Måter som forhandlere kan bruke til å implementere mulighet for brukere å velge bort ting

Forhandlere kan implementere mulighet for brukere å velge bort ting på tre måter.

### <a name="opting-out-on-behalf-of-users"></a>Velge bort på vegne av brukeren

I Kontobehandling i Commerce-administrasjonskontoret kan forhandlere velge bort på vegne av brukeren.

1. Fra startsiden til administrasjonskontoret søker du etter **alle kunder**.
1. Søk etter og velg en kunde, og velg deretter hurtigfanen **Detaljhandel**.

    ![Hurtigfanen Detaljhandel](./media/Disablepersonalizationpart1.png)

1. Under **Personvern** angir du alternativet **Deaktiver tilpassing** til **Ja**.

    ![Personverninnstillinger](./media/Disablepersonalizationpart2.png)

1. Velg **Lagre**, og lukk siden.

### <a name="module-based-opt-out-experience"></a>Modulbasert bortvalgsopplevelse

Forhandlere kan la godkjente brukere velge bort personlige anbefalinger selv. Hvis du vil gi denne bortvalgsopplevelsen, legger du til en bortvalgsmodul for brukerne på profilsidene for kundekontoer.

### <a name="custom-extensions"></a>Egendefinerte tillegg

Forhandlere kan opprette egne tillegg for å administrere bortvalgsopplevelsen for brukere. Hvis du vil ha mer informasjon, kan du se [Kalle API-er for Retail Server](e-commerce-extensibility/call-retail-server-apis.md) og [Utvidelsesmulighet for Internett-kanal](e-commerce-extensibility/overview.md).

## <a name="obtain-a-digital-copy-of-personalized-recommendations-data-on-behalf-of-an-authenticated-user"></a>Få tak i en digital kopi av personlige anbefalingsdata på vegne av en godkjent bruker

Kunder vil kanskje skaffe en seg digital kopi av sine personlige opplysninger og også se en eksportert visning av anbefalingsresultatene. Hvis en kunde ber om denne informasjonen, må forhandleren opprette en egendefinert utvidelse som kaller API-et for Retail Server og spør etter det fullstendige resultatet fra listen **Plukkinger for deg**, basert på kundens kunde-ID. Resultatene kan deretter eksporteres i CSV-format (kommadelte verdier) og deles med kunden.

Følgende eksempel viser hvordan en forhandler kan utføre denne oppgaven.

1. Forhandleren oppretter en egendefinert utvidelse for å hente personlige anbefalingsdata på vegne av brukeren. Hvis du vil ha informasjon om hvordan du oppretter moduler, kloner eksisterende moduler, kaller API-er for Retail Server og kaller datahandlinger, kan du se [Utvidelsesmulighet for Internett-kanal](e-commerce-extensibility/overview.md).
2. Den egendefinerte utvidelsen foretar et kall til kjernedatahandlingen **get-recommendations** og sender den nødvendige informasjonen til den, basert på kravene i listen. Når det gjelder listen **Plukkinger for deg**, må utvidelsen sende riktig listenavn og kunde-ID til datahandlingen.

    En måte å opprette den egendefinerte utvidelsen på er å klone den eksisterende produktsamlingsmodulen som brukes til å returnere anbefalingsresultater. Ved å klone denne eksisterende modulen kan en forhandler endre den eksisterende koden og legge til en ny knapp som eksporterer anbefalingsresultatene til en CSV-fil. Hvis du vil ha mer informasjon, kan du se [Klone en startsettmodul](e-commerce-extensibility/clone-starter-module.md) og [Produktsamlingsmoduler](product-collection-module-overview.md).

    For en fullstendig visning av API-biblioteket for Retail Server, se [Kunde- og forbruker-API-er for Retail Server](dev-itpro/retail-server-customer-consumer-api.md).

3. Når den egendefinerte utvidelsen er opprettet, kan forhandleren eksportere en CSV-fil av alle anbefalingsresultatene, basert på den unike kunde-ID-en til den godkjente brukeren.
4. Forhandleren kan dele den eksporterte CSV-filen som inneholder den fullstendige, tilpassede listen over anbefalte produkter, med den godkjente brukeren.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktivere ADLS i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Legge til lister over anbefalinger på et e-handelsområde](add-reco-list-to-page.md)

[Legge til produktanbefalinger i POS](product.md)

[Legge til anbefalinger på transaksjonsskjermen](add-recommendations-control-pos-screen.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)
