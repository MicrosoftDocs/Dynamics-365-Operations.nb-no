---
title: Opprette kuraterte anbefalinger manuelt
description: Dette emnet beskriver hvordan selgere kan opprette og administrere manuelle produktlister for Microsoft Dynamics 365 Commerce-kunder.
author: bebeale
manager: AnnBe
ms.date: 05/26/2020
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
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 0b866704b419fb07dcf1ddd386af2f7d6cfa02e2
ms.sourcegitcommit: fdc5dd9eb784c7d8e75692c8cdba083fe0dd87ce
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/26/2020
ms.locfileid: "3404122"
---
# <a name="manually-create-curated-recommendations"></a>Opprette kuraterte anbefalinger manuelt

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan selgere kan opprette og administrere manuelle lister over produktanbefalinger for Microsoft Dynamics 365 Commerce-kunder.

Kuraterte lister er samlinger av individuelt innhold som opprettes og kurateres av personer.  

## <a name="create-a-new-list"></a>Opprette en ny liste

Hvis du vil opprette en kuratert produktanbefalingsliste, gjør du følgende.

1. Gå til **Detaljhandel og handel &gt; Produktanbefalinger &gt; Anbefalingslister**.
1. Velg **Ny**.
1. Angi en verdi i **Liste-ID**-feltet.
1. Angi en verdi i **Listenavn**-feltet.
    - **Listenavn** er tittelen på listen som vil vises i delen med kuraterte lister i modulen **Produktsamling** .
1. Hvis du vil legge til produkter i listen, velger du **Legg til produkter**.
1. Hvis du vil endre rekkefølgen på produktene i listen, angir du en verdi i **Vis rekkefølge**-kolonnen.
    - Hvis to produkter har samme verdi for visningsrekkefølge, kan den endelige rekkefølgen for disse to resultatene avvike fra back office.
1. Velg **Lagre** for å lagre listen.

## <a name="example-list"></a>Eksempelliste

![Eksempel på kuratert liste i backoffice](./media/examplecuratedrecolist.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over produktanbefalinger](product-recommendations.md)

[Aktivere Azure Data Lake Storage i et Dynamics 365 Commerce-miljø](enable-adls-environment.md)

[Aktiver produktanbefalinger](enable-product-recommendations.md)

[Aktivere personlige anbefalinger](personalized-recommendations.md)

[Velge bort personlige anbefalinger](personalization-gdpr.md)

[Legge til produktanbefalinger i POS](product.md)

[Legge til anbefalinger i transaksjonsskjermbildet](add-recommendations-control-pos-screen.md)

[Justere anbefalingsresultater for AI-ML](modify-product-recommendation-results.md)

[Opprette anbefalinger med demonstrasjonsdata](product-recommendations-demo-data.md)

[Vanlige spørsmål om produktanbefalinger](faq-recommendations.md)
