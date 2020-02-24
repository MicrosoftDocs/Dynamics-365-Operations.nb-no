---
title: Aktiver produktanbefalinger
description: Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 10/1/2019
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
ms.openlocfilehash: 2d3f1bc2526eeacb4bd6338a0679eadd95a75989
ms.sourcegitcommit: b5ecde955a69f577de46e7db10e89caaedeb2b49
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3024962"
---
# <a name="enable-product-recommendations"></a>Aktiver produktanbefalinger

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder. Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Anbefalinger, forhåndssjekk

Før du aktiverer, må du være oppmerksom på at produktanbefalinger bare støttes for Handel-kunder som har migrert lagringen til bruk av Azure Data Lake Storage (ADLS). 

Hvis du vil se trinn for aktivering av ADLS, kan du se [Slik aktiverer du ADLS i et Dynamics 365-miljø](enable-ADLS-environment.md).

Kontroller også at RetailSale-mål er aktivert. Hvis du vil lære mer om denne konfigureringsprosessen, går du [hit.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


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

[Aktivere tilpassede anbefalinger](personalized-recommendations.md)

[Legge til produktanbefalingslisten på sider](add-reco-list-to-page.md)

[Legge til anbefalingspanel til POS-enheter](add-recommendations-control-pos-screen.md)

[Oversikt over produktsamlingsmodul](product-collection-module-overview.md)

[Aktivere ADLS i Dynamics 365-miljøet](enable-ADLS-environment.md)

