---
title: Legg til en opphavsrettserklæring
description: Denne artikkelen beskriver hvordan du legger til opphavsrettserklæring på e-handelsområdet.
author: psimolin
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: a1e394b9a582b48c44bbec26ef42a90d50918f87
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8851223"
---
# <a name="add-a-copyright-notice"></a>Legg til en opphavsrettserklæring

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du legger til opphavsrettserklæring på e-handelsområdet.

## <a name="prerequisites"></a>Forutsetninger

Før du kan legge til en opphavsrettserklæring på området, må du ha følgende elementer:

- En mal som inneholder et delt bunntekstfragment.
- En side som bruker denne malen.

## <a name="add-a-copyright-notice"></a>Legge til en opphavsrettserklæring

Hvis du vil legge til en opphavsrettserklæring nederst på hver side som bruker en bestemt mal, følger du disse trinnene.

1. Gå til **Fragmenter**, og velg deretter **Nytt**.
1. I dialogboksen **Nytt fragment** velger du **Bunntekst**-modulen, og gir fragmentet et navn. Skriv for eksempel inn **Bunntekst-opphavsrettserklæring**.
1. Velg **OK**.
1. I navigasjonsruten velger du ellipseknappen (**...**) ved siden av **Bunntekst**, og deretter velger du **Legg til modul**.
1. I dialogboksen velger du **Bunntekstkategori**, og deretter velger du **OK**.
1. I navigasjonsruten velger du ellipseknappen ved siden av **Bunntekstkategori**, og deretter velger du **Legg til modul**.
1. I dialogboksen velger du **Tekstblokk**, og deretter velger du **OK**.
1. I navigasjonsruten velger du **Tekstblokk**.
1. Legg til melding om opphavsrett i feltet **Avsnitt** i egenskapsruten til høyre. Skriv for eksempel inn **(C) Fabrikam 2019**.
1. Velg **Lagre**, velg **Fullfør redigering**, og velg deretter **Publiser**.
1. Gå til **Maler**, velg malen, og velg deretter **Rediger**.
1. Under **Sideoppsett** utvider du **Brødtekst**, og deretter utvider du **Standardside**.
1. Velg ellipseknappen ved siden av **Bunntekstspor**, og velg deretter **Legg til fragment**.
1. Velg fragmentet du opprettet tidligere, og velg deretter **Velg**.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.

Bunnteksten som inneholder opphavsrettserklæringen, vises automatisk nederst på alle sider som bruker den valgte malen.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en logo](add-logo.md)

[Velge et områdetema](select-site-theme.md)

[Arbeide med CSS-overstyringsfiler](css-override-files.md)

[Legge til et favorittikon](add-favicon.md)

[Legge til språk på området](add-languages-to-site.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
