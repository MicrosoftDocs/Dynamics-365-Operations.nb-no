---
title: Velge å bruke vurderinger og anmeldelser
description: Dette emnet forklarer hvordan du velger å bruke vurderinger og omtaler på Microsoft Dynamics 365 Commerce-området.
author: gvrmohanreddy
manager: annbe
ms.date: 01/30/2020
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
ms.openlocfilehash: eda7fbaeea8d3c1a07f7b43cafe44886d149a211
ms.sourcegitcommit: 1e6c8163da5818196769eb278afb3a2335d0cbe3
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2020
ms.locfileid: "3027271"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a>Velge å bruke vurderinger og anmeldelser

[!include [banner](includes/banner.md)]

Dette emnet forklarer hvordan du velger å bruke vurderinger og omtaler på Microsoft Dynamics 365 Commerce-området.

## <a name="overview"></a>Oversikt

Løsningen for vurderinger og omtaler er en omnikanalløsning som du kan gjøre tilgjengelig i Dynamics 365 Commerce ved å bruke Microsoft Dynamics Lifecycle Services (LCS). LCS er en administrasjonsportal som forhandlere bruker for å administrere sine miljøer fra klargjøring til avvikling.

Hvis du vil bruke for vurderinger og omtaler på handelsområdet ditt, må du velge vurdering og omtaler under distribusjon av e-handelsområdet ditt på Dynamics 365 Commerce.

## <a name="opt-in-to-use-ratings-and-reviews"></a>Velge å bruke vurderinger og anmeldelser

Følg denne fremgangsmåten for å velge å bruke vurderinger og omtaler på området ditt.

1. Følg fremgangsmåten i [Distribuere et nytt e-handelsområde](deploy-ecommerce-site.md).
1. Mens du fortsatt er i LCS, kan du gå til **Konfigurasjon av distribusjon av Retail \> Andre innstillinger**.
1. Sett alternativet **Aktiver tjenesten for vurderinger og omtale** til **Ja**.
1. I **Moderator for AAD-sikkerhetsgruppe for vurderinger og omtaler (sikkerhetsgruppeobjekt-ID)** angir du IDen til Microsoft Azure Active Directory (Azure AD)-sikkerhetsgruppen som inkluderer moderatorene for vurderinger og omtaler.

    ![Velge å bruke vurderinger og anmeldelser](media/LCS_RnR_Preference.png)

1. Fullfør initialiseringsprosessen for e-handel.

> [!NOTE] 
> Hvis du er en eksisterende Dynamics 365 Commerce-kunde som allerede har distribuert et e-handelsområde uten å ha valgt vurderinger og omtaler, og som nå ønsker å bruke for vurderinger og omtaler fra Dynamics 365 Commerce-pakken, kan du sende en tjenesteforespørsel. Hvis du vil ha informasjon om hvordan du sender en tjenesteforespørsel, kan du se [Prosess for å sende inn tjenesteforespørsler](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json). 

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderinger og anmeldelser](configure-ratings-reviews.md)

[Synkronisere produktvurderinger i Dynamics 365 Retail](sync-product-ratings.md)


