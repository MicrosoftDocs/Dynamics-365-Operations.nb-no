---
title: Velge å bruke vurderinger og anmeldelser
description: Dette emnet forklarer hvordan du velger å bruke vurderinger og omtaler på Microsoft Dynamics 365 Commerce-området.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697986"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Velge å bruke vurderinger og anmeldelser

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du velger å bruke vurderinger og omtaler på Microsoft Dynamics 365 Commerce-området.

## <a name="overview"></a>Oversikt

Løsningen for vurderinger og omtaler er en omnikanalløsning som du kan gjøre tilgjengelig i Dynamics 365 Commerce ved å bruke Microsoft Dynamics Lifecycle Services (LCS). LCS er en administrasjonsportal som forhandlere bruker for å administrere sine miljøer fra klargjøring til avvikling.

Hvis du vil bruke løsningen for vurderinger og omtaler på webområdet for Commerce, må du først velge å bruke løsningen.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Velge å bruke vurderinger og anmeldelser

Følg denne fremgangsmåten for å velge å bruke vurderinger og omtaler på området ditt.

1. Følg fremgangsmåten i [Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md).
1. Mens du fortsatt er i LCS, kan du gå til **Konfigurasjon av distribusjon av Retail \> Andre innstillinger**.
1. Sett alternativet **Aktiver tjenesten for vurderinger og omtale** til **Ja**.
1. I **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler (sikkerhetsgruppeobjekt-ID)** angir du IDen til Microsoft Azure Active Directory (Azure AD)-sikkerhetsgruppen som inkluderer moderatorene for vurderinger og omtaler.

    ![Velge å bruke vurderinger og anmeldelser](media/LCS_RnR_Preference.png)

1. Fullfør initialiseringsprosessen for e-handel.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)

[Synkronisere produktvurderinger i Dynamics 365 Retail](sync-product-ratings.md)
