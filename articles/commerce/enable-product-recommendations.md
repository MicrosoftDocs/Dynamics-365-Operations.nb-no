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
ms.openlocfilehash: ecda571a356c6968196d09cc19923105cf4544ab
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770145"
---
# <a name="enable-product-recommendations"></a>Aktiver produktanbefalinger

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du kan bruke produktanbefalinger som er basert på kunstig intelligens-maskinopplæring (AI-ML), tilgjengelig for Microsoft Dynamics 365 Commerce-kunder. Hvis du vil ha mer informasjon om produktanbefalingslister, kan du se [Oversikt over produktanbefalinger](product-recommendations.md).

## <a name="recommendations-pre-check"></a>Anbefalinger, forhåndssjekk
Før du aktiverer bør du være oppmerksom på at produktanbefalinger bare støttes for økonomi/drift-kunder som støtter bygg 10.0.6 og har migrert lagringsplassen til BDL. 

Kontroller også at RetailSale-mål er aktivert. Hvis du vil lære mer om denne konfigureringsprosessen, går du [hit.](https://docs.microsoft.com/en-us/dynamics365/ai/customer-insights/pm-measures)


## <a name="turn-on-recommendations"></a>Aktivere anbefalinger

Gjør følgende for å aktivere produktanbefalinger.

1. Gå til **Retail** &gt; **Produktanbefalinger** &gt; **Anbefalingsparametere**.
1. Velg **Anbefalingslister** i listen over delte parametere for detaljhandel.
1. Sett alternativet **Aktiver anbefalinger** til **Ja**.

![aktivere produktanbefalinger](./media/enableproductrecommendations.png)

> [!NOTE]
> Denne fremgangsmåten starter prosessen med å generere produktanbefalingslister. Opptil flere timer kan være nødvendig før listene er tilgjengelige og kan sees ved salgsstedet (POS) eller i Dynamics 365 for Commerce.

## <a name="configure-recommendation-list-parameters"></a>Konfigurere parametere for anbefalingsliste
Den AI-ML-baserte produktanbefalingslisten gir som standard foreslåtte verdier. Du kan endre standardverdiene som foreslås, slik at de passer til forretningsflyten. Hvis du vil ha mer informasjon om hvordan du endrer standardparametere, kan du gå til [Behandle resultater for AI-ML-basert produktanbefaling](modify-product-recommendation-results.md).

## <a name="show-recommendations-on-pos-devices"></a>Vis anbefalinger på salgsstedsenheter
Når du har aktivert anbefalinger i backoffice, må anbefalingspanelet legges til i skjermbildet for kontroll av POS-skjermen via oppsettverktøyet. Hvis du vil lære mer om denne prosessen, går du [hit.](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Legge til produktanbefalingslisten på sider](add-reco-list-to-page.md)

[Legge til anbefalingspanel til POS-enheter](https://docs.microsoft.com/en-us/dynamics365/unified-operations/retail/add-recommendations-control-pos-screen)


