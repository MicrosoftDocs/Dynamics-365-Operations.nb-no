---
title: Legge til en opphavsrettserklæring
description: Dette emnet beskriver hvordan du legger til opphavsrettserklæring på e-handelsområdet.
author: psimolin
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 39135a2eca25336097ee9eddf06dc6709c102571
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696951"
---
# <a name="add-a-copyright-notice"></a>Legge til en opphavsrettserklæring

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du legger til opphavsrettserklæring på e-handelsområdet.

## <a name="prerequisites"></a>Forutsetninger

Før du kan legge til en opphavsrettserklæring på området, må du ha følgende elementer:

- En mal som inneholder et delt bunntekstfragment.
- En side som bruker denne malen.

## <a name="add-a-copyright-notice"></a>Legge til en opphavsrettserklæring

Hvis du vil legge til en opphavsrettserklæring nederst på hver side som bruker en bestemt mal, følger du disse trinnene.

1. Gå til **Fragmenter**, og velg **Nytt sidefragment**.
1. I dialogboksen velger du **Bunntekst**-modulen, og deretter gir du navn til fragmentet. Skriv for eksempel inn **Bunntekst-opphavsrettserklæring**.
1. Velg **OK**.
1. I navigasjonsruten velger du ellipseknappen (**...**) ved siden av **Bunntekst**, og deretter velger du **Legg til modul**.
1. I dialogboksen velger du **Bunntekstkategori**, og deretter velger du **OK**.
1. I navigasjonsruten velger du ellipseknappen ved siden av **Bunntekstkategori**, og deretter velger du **Legg til modul**.
1. I dialoigboksen velger du **Innholdsrikt blokkelement**, og velg deretter **OK**.
1. I navigasjonsruten velger du **Innholdsrikt blokkelement**.
1. Legg til melding om opphavsrett i feltet **Avsnitt** i egenskapsruten til høyre. Skriv for eksempel inn **(C) Fabrikam 2019**.
1. Velg **Lagre**, velg **Sjekk inn**, og velg deretter **Publiser**.
1. Gå til **Maler**, velg malen, og velg deretter **Sjekk ut**.
1. Under **Sideoppsett** utvider du **Brødtekst**, og deretter utvider du **Standardside**.
1. Velg ellipseknappen ved siden av **Bunntekstspor**, og velg deretter **Legg til fragment**.
1. Velg fragmentet du opprettet tidligere, og velg deretter **Velg**.
1. Sjekk inn malen, og publiser den.

Bunnteksten som inneholder opphavsrettserklæringen, vises automatisk nederst på alle sider som bruker den valgte malen.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en logo](add-logo.md)

[Velge et områdetema](select-site-theme.md)

[Legge til et favorittikon](add-favicon.md)

[Legge til en velkomstmelding](add-welcome-message.md)

[Legge til språk på området](add-languages-to-site.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)

