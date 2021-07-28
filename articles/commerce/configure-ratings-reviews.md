---
title: Konfigurere vurderinger og anmeldelser
description: Dette emnet beskriver hvordan du konfigurerer e-handelområdet til å vise kundevurderinger og -omtaler i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
ms.date: 02/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 09930af8b6ce78a2a88382772a44de173875856a
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6352548"
---
# <a name="configure-ratings-and-reviews"></a>Konfigurere vurderinger og anmeldelser

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer e-handelområdet til å vise kundevurderinger og -omtaler i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Vurderinger og evalueringer på e-handelswebområder hjelper kunder med å lære om produkter før de tar en avgjørelse, ved å vise dem hva andre kunder mener om disse produktene. For webområder for e-handel er også vurderinger og gjennomganger en mekanisme for å samle kundetilbakemeldinger om produkter. 

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Konfigurere et område for å vise vurderinger og omtaler

Konfigurasjonsverdier for vurderinger og omtaler, for eksempel leie-ID, kontroll av tekstlengde og kontroll av tittellengde, konfigureres på områdenivå. 

Følg denne fremgangsmåten for å konfigurere et område for å vise vurderinger og omtaler. 

1. Gå til **Hjem \> Områder**.
1. Velg navnet på området ditt. 
1. Gå til **Områdeinnstillinger \> Tillegg**. 
1. I feltet for **Maksimal lengde for vurderingstekst** angir du maksimalt antall tegn som vurderingsteksten kan ha (for eksempel **1000**). 
1. I feltet for **Maksimal lengde for vurderingstittel** angir du maksimalt antall tegn som vurderingstittelen kan ha (for eksempel **55**). 
1. Velg **Lagre og publiser**. 

Illustrasjonen nedenfor viser hvordan denne konfigurasjonen ser ut i Dynamics 365 Commerce.

![Konfigurere et område for å vise vurderinger og omtaler.](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Koble en produktvurdering til omtaledelen i en PDP

En produktvurdering vises under produkttittelen øverst i PDP. Produktvurderingen kan konfigureres slik at den er koblet til **Vurderinger**-delen av samme PDP. 

Følg denne fremgangsmåten for å koble en produktomtale til **Vurderinger**-delen i PDPen:

1. Åpne PDP-malen. 
1. Gå til **Innstillinger for kjøpsboks-containermodul**.
1. Under **Kjøpsboks** velger du **Produktvurderinger**, og deretter merker du av for **Koble klikket til modul med full vurdering**.

Illustrasjonen nedenfor viser hvordan denne konfigurasjonen ser ut i Dynamics 365 Commerce.

![Koble en produktvurdering til omtaledelen i en PDP.](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Konfigurere koblingen for siden for personvern og policy

Følg disse trinnene for å konfigurere koblingen for siden for personvern og policy.

1. Gå til **Hjem \> Områder**.
1. Velg navnet på området ditt. 
1. Gå til **Områdeinnstillinger \> Tillegg**.
1. I kategorien **Ruter**, under **Personvernpolicy for vurderinger og omtaler**, velger du **Legg til kobling**. Hvis det allerede er angitt en kobling, og du vil erstatte den, velger du koblingen. 
1. Velg koblingen for siden for personvern og policy i dialogboksen **Legg til en kobling**, og velg deretter **OK**. 
1. Velg **Lagre og publiser**. 

Illustrasjonen nedenfor viser hvordan denne konfigurasjonen ser ut i Dynamics 365 Commerce.

![Konfigurere koblingen for siden for personvern og policy.](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="configure-ratings-and-reviews-modules-on-product-details-pages"></a>Konfigurere vurderings- og omtalemoduler på sider med produktdetaljer

Hvis du vil ha informasjon om hvordan du konfigurerer vurderings- og omtalemoduler på sider med produktdetaljer, kan du se [Vurderings- og omtalemoduler](ratings-reviews-modules.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Velge å bruke vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Konfigurere vurderings- og omtalemoduler på sider med produktdetaljer](ratings-reviews-modules.md)

[Synkronisere produktvurderinger i Dynamics 365 Retail](sync-product-ratings.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]