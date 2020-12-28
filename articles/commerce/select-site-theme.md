---
title: Velge et områdetema
description: Dette emnet beskriver hvordan du angir eller endrer områdets tema i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: c54a3e9471fdeb56f27fe7c567c7cd7f0b7fd218
ms.sourcegitcommit: 2ef23dcd4e42362186b9951e675010d97d55c6bd
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4556435"
---
# <a name="select-a-site-theme"></a>Velge et områdetema

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du angir eller endrer områdets tema i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

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

[Legge til en velkomstmelding](add-welcome-message.md)

[Legge til en opphavsrettserklæring](add-copyright-notice.md)

[Legge til språk på området](add-languages-to-site.md)

[Legge til skript kode i områdes ID-er for å støtte telemetri](add-telemetry.md)

[Temaoversikt](e-commerce-extensibility/theming.md)

[Opprett et nytt tema](e-commerce-extensibility/create-theme.md)

