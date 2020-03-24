---
title: Aktiver produktanbefalinger
description: Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 03/12/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail, eCommerce
ms.author: bebeale
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 879fccb063ca0b74e0f022a9edf6a15f7d1311ae
ms.sourcegitcommit: 1e7e7c4bc197b0a42e4d53d2a54600a2fb125b69
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/13/2020
ms.locfileid: "3127888"
---
# <a name="enable-product-recommendations"></a>Aktiver produktanbefalinger

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder. Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Anbefalinger, forhåndssjekk

Før du aktiverer, må du være oppmerksom på at produktanbefalinger bare støttes for Handel-kunder som har migrert lagringen til bruk av Azure Data Lake Storage (ADLS). 

Hvis du vil se trinn for aktivering av ADLS, kan du se [Slik aktiverer du ADLS i et Dynamics 365-miljø](enable-ADLS-environment.md).

Kontroller også at RetailSale-mål er aktivert. Hvis du vil lære mer om denne konfigureringsprosessen, går du [hit.](https://docs.microsoft.com/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Aktivere anbefalinger

Gjør følgende for å aktivere produktanbefalinger.

1. Gå til **Detaljhandel og handel &gt; Produktanbefalinger &gt; Anbefalingsparametere**.
1. Velg **Anbefalingslister** i listen over delte parametere.
1. Sett alternativet **Aktiver anbefalinger** til **Ja**.

![aktivere produktanbefalinger](./media/enableproductrecommendations.png)

> [!NOTE]
> Denne fremgangsmåten starter prosessen med å generere produktanbefalingslister. Opptil flere timer kan være nødvendig før listene er tilgjengelige og kan sees ved salgsstedet (POS) eller i Dynamics 365 Commerce.

## <a name="configure-recommendation-list-parameters"></a>Konfigurere parametere for anbefalingsliste

Den AI-ML-baserte produktanbefalingslisten gir som standard foreslåtte verdier. Du kan endre standardverdiene som foreslås, slik at de passer til forretningsflyten. Hvis du vil ha mer informasjon om hvordan du endrer standardparametere, kan du gå til [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Vis anbefalinger på salgsstedsenheter

Når du har aktivert anbefalinger i Handel-administrasjonskontoret, må anbefalingspanelet legges til i skjermbildet for kontroll av POS-skjermen ved hjelp av oppsettverktøyet. Hvis du vil lære om denne prosessen, kan du se [Legge til en anbefalingskontroll på transaksjonsskjermbildet på salgsstedsenheter](add-recommendations-control-pos-screen.md). 

## <a name="enable-personalized-recommendations"></a>Aktivere tilpassede anbefalinger

Hvis du vil finne ut mer om hvordan du mottar tilpassede anbefalinger, kan du se [Aktivere tilpassede anbefalinger](personalized-recommendations.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktivere ADLS i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Legge til lister over anbefalinger på et e-handelsområde](add-reco-list-to-page.md)

[Legge til produktanbefalinger i POS](product.md)

[Legge til anbefalinger på transaksjonsskjermen](add-recommendations-control-pos-screen.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette kuraterte anbefalinger manuelt](create-editorial-recommendation-lists.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)

