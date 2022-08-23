---
title: Velge et områdetema
description: Denne artikkelen beskriver hvordan du angir eller endrer områdets tema i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.custom: ''
ms.assetid: ''
ms.openlocfilehash: 3b7b3e8d6fd75a31bf9830c50b5c641ab3e62ab3
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286790"
---
# <a name="select-a-site-theme"></a>Velge et områdetema

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du angir eller endrer områdets tema i Microsoft Dynamics 365 Commerce.

Området og stilen for et oppsett (for eksempel skrifter, størrelser og farger) defineres av temaet du velger, og gjelder for området. Et tema opprettes og distribueres av en utvikler i firmaet. Hvis du vil ha en oversikt over temaer, se [Temaoversikt](e-commerce-extensibility/theming.md). Hvis du vil ha mer informasjon om hvordan du oppretter og distribuerer temaer, kan du se [Opprette et nytt tema](e-commerce-extensibility/create-theme.md).

Når du oppretter et område for første gang, bruker det som standard et tema kalt **Fabrikam**. Dette standardtemaet leveres som en del av Commerce-modulbiblioteket. Når du har distribuert flere temaer for området, kan du konfigurere området slik at det bruker en av dem i stedet.

## <a name="select-the-site-theme"></a>Velge områdetema

Følg denne fremgangsmåten for å velge temaet som skal brukes på området.

1. Gå til området i redigeringsmiljøet for området.
1. Gå til **Områdebehandling** \> **Utvidelsesmulighet**.
1. Under **Tema** velger du et tema på rullegardinmenyen.
1. Hvis du vil bruke det valgte temaet på området, velger du **Lagre og publiser**.

> [!NOTE]
> Temaet du velger, publiseres på området så snart du velger **Lagre og publiser** på siden **Utvidelse**. Hvis du vil forhåndsvise et tema på området før du bruker det, kan du bruke utviklings- eller sandkassemiljøet.

## <a name="additional-resources"></a>Tilleggsressurser

[Legge til en logo](add-logo.md)

[Arbeide med CSS-overstyringsfiler](css-override-files.md)

[Legge til et favorittikon](add-favicon.md)

[Legge til en opphavsrettserklæring](add-copyright-notice.md)

[Legge til språk på området](add-languages-to-site.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)

[Temaoversikt](e-commerce-extensibility/theming.md)

[Opprett et nytt tema](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
