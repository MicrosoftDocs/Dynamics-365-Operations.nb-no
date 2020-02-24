---
title: Konfigurere vurderinger og anmeldelser
description: Dette emnet beskriver hvordan du konfigurerer e-handelområdet til å vise kundevurderinger og -omtaler i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0aac4b680590a95f465d33950f2933c4a4582e54
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002203"
---
# <a name="configure-ratings-and-reviews"></a>Konfigurere vurderinger og anmeldelser


[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du konfigurerer e-handelområdet til å vise kundevurderinger og -omtaler i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Vurderinger og evalueringer på e-handelswebområder hjelper kunder med å lære om produkter før de tar en avgjørelse, ved å vise dem hva andre kunder mener om disse produktene. For webområder for e-handel er også vurderinger og gjennomganger en mekanisme for å samle kundetilbakemeldinger om produkter. 

Vurderingene vises på produktlistesider, kategorilistesider, sider for søkeresultater og andre områdesider. Vurderingshistogrammer og produktgjennomganger vises på sider for produktdetaljer (PDPer). En **Skriv en vurdering**-knapp gir kundene muligheten til å sende inn rangeringer og omtaler for et produkt.

## <a name="ratings-and-reviews-modules-on-pdps"></a>Vurderings- og omtalemoduler på PDPer 

Tre moduler viser vurderings- og omtalesammendraget på PDPer:

- Modul for skriving av vurdering
- Listemodul for produktvurderinger
- Modul for vurderingshistogrammer
 
Illustrasjonen nedenfor viser hvordan vurderings- og evalueringsmodulene ser ut på en PDP.

![Vurderings- og omtalemoduler på en PDP](media/rnr-eCommerce-pdp-reviews-modules_design.png)

> [!TIP] 
> Hvis du vil ha informasjon om hvordan du optimaliserer PDP-maler og -oppsett slik at du kan dele konfigurasjonene for vurderings- og omtalemoduler mellom flere PDPer på e-handelsområdet, se [Oversikt over maler og oppsett](templates-layouts-overview.md).

Illustrasjonen nedenfor viser hvordan dialogboksen **Legg til modul** viser rangerings- og omtalemoduler i Dynamics 365 Commerce.

![Dialogboksen Legg til modul](media/rnr-eCommerce-pdp-adding-rnr-modules.png)

### <a name="write-review-module"></a>Modul for omtaleskriving

Modulen for omtaleskriving inkluderer en **Skriv en vurdering**-knapp som lar brukere logge på, tilordne en vurdering og skrive en omtale av et produkt. Denne modulen lar også brukere redigere en vurdering eller omtale som de tidligere har sendt. Denne modulen vises vanligvis over listemodulene for vurderingshistogram og produktevalueringer på en PDP.

Følgende illustrasjon viser dialogboksen **Skriv en gjennomgang** som vises når en kunde velger **Skriv en vurdering**. Kunden kan bruke denne dialogboksen til å sende inn en vurdering og en omtale.

![Dialogboksen Skriv en vurdering](media/rnr-eCommerce-write-review-module.png)

Tabellen nedenfor viser egenskapen for Skriv en vurdering-modulen som må konfigureres i redigeringsverktøyet.

| Egenskapsnavn | Verdi        | Egenskapsbeskrivelse                 |
|---------------|--------------|--------------------------------------|
| Navn          | Skriv vurdering | Navnet på Skriv en vurdering-modulen |

### <a name="ratings-histogram-module"></a>Modul for vurderingshistogrammer

Modul for vurderingshistogrammer viser vurderingshistogrammet. Denne modulen vises vanligvis mellom Skriv vurdering-modulen og listemodulen for produktvurderinger på en PDP.

Histogrammodulen for vurderinger krever ingen konfigurasjon. Du trenger bare å legge til modulen i PDP-malen. 

Illustrasjonene nedenfor viser hvordan en PDP-mal ser ut i Dynamics 365 Commerce når modulene for vurderinger og gjennomgang er konfigurert for visning på PDPer.

![PDP-mal når vurderinger og omtaler er konfigurert for visning på PDPer](media/rnr-eCommerce-pdp-reviews-modules.png)

### <a name="product-reviews-list-module"></a>Listemodul for produktvurderinger

Listemodulen for produktvurderinger viser en liste over produktvurderinger sammen med alternativer for sortering, filtrering og paginering. Denne modulen vises vanligvis etter vurderingshistogrammodulen på en PDP.

Tabellen nedenfor viser egenskapene for listemodulen for produktvurderinger som må konfigureres i redigeringsverktøyet.

| Egenskapsnavn              | Verdi | Egenskapsbeskrivelse |
|----------------------------|-------| ---------------------|
| Omtaler som vises på hver side | 10    | Antall omtaler som skal vises om gangen på en PDP. Knappene **Neste** og **Forrige** er inkludert, slik at brukerne kan bla gjennom sidene med gjennomganger. |

#### <a name="ratings-histogram--summary-view"></a>Vurderingshistogram – sammendragsvisning

Listemodulen for produktvurderinger inneholder et spor der du kan legge til en vurderingshistogrammodul. Illustrasjonen nedenfor viser hvordan du kan legge til et vurderingshistogram i listemodulen for produktvurderinger i Dynamics 365 Commerce.

![Legge til en histogrammodul i en listemodulen for produktvurderinger](media/rnr-eCommerce-pdp-rating-histogram-summary.png)

## <a name="configure-a-site-to-show-ratings-and-reviews"></a>Konfigurere et område for å vise vurderinger og omtaler

Konfigurasjonsverdier for vurderinger og omtaler, for eksempel leie-ID, kontroll av tekstlengde og kontroll av tittellengde, konfigureres på områdenivå. 

Følg denne fremgangsmåten for å konfigurere et område for å vise vurderinger og omtaler. 

1. Gå til **Hjem \> Områder**.
1. Velg navnet på området ditt. 
1. Gå til **Områdebehandling \> Utvidelsesmulighet**. 
1. I feltet for **Maksimal lengde for vurderingstekst** angir du maksimalt antall tegn som vurderingsteksten kan ha (for eksempel **1000**). 
1. I feltet for **Maksimal lengde for vurderingstittel** angir du maksimalt antall tegn som vurderingstittelen kan ha (for eksempel **55**). 
1. Velg **Lagre og publiser**. 

Illustrasjonen nedenfor viser hvordan denne konfigurasjonen ser ut i Dynamics 365 Commerce.

![Konfigurere et område for å vise vurderinger og omtaler](media/rnr-eCommerce-site-appsettings.png)

## <a name="link-a-product-rating-to-the-reviews-section-of-a-pdp"></a>Koble en produktvurdering til omtaledelen i en PDP

En produktvurdering vises under produkttittelen øverst i PDP. Produktvurderingen kan konfigureres slik at den er koblet til **Vurderinger**-delen av samme PDP. 

Følg denne fremgangsmåten for å koble en produktomtale til **Vurderinger**-delen i PDPen:

1. Åpne PDP-malen. 
1. Gå til **Innstillinger for kjøpsboks-containermodul**.
1. Under **Kjøpsboks** velger du **Produktvurderinger**, og deretter merker du av for **Koble klikket til modul med full vurdering**.

Illustrasjonen nedenfor viser hvordan denne konfigurasjonen ser ut i Dynamics 365 Commerce.

![Koble en produktvurdering til omtaledelen i en PDP](media/rnr-eCommerce-buy-box-rating-summary.png)

## <a name="configure-the-link-for-the-privacy-and-policy-page"></a>Konfigurere koblingen for siden for personvern og policy

Følg disse trinnene for å konfigurere koblingen for siden for personvern og policy.

1. Gå til **Hjem \> Områder**.
1. Velg navnet på området ditt. 
1. Gå til **Områdebehandling \> Utvidelsesmulighet**
1. I kategorien **Ruter**, under **Personvernpolicy for vurderinger og omtaler**, velger du **Legg til kobling**. Hvis det allerede er angitt en kobling, og du vil erstatte den, velger du koblingen. 
1. Velg koblingen for siden for personvern og policy i dialogboksen **Legg til en kobling**, og velg deretter **OK**. 
1. Velg **Lagre og publiser**. 

Illustrasjonen nedenfor viser hvordan denne konfigurasjonen ser ut i Dynamics 365 Commerce.

![Konfigurere koblingen for siden for personvern og policy](media/rnr-eCommerce-rnr-privacy-policy-link.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over vurderinger og anmeldelser](ratings-reviews-overview.md)

[Velge å bruke vurderinger og anmeldelser](opt-in-ratings-reviews.md)

[Administrere vurderinger og anmeldelser](manage-reviews.md)

[Synkronisere produktvurderinger i Dynamics 365 Retail](sync-product-ratings.md)
