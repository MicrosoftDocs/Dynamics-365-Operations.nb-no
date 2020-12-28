---
title: Vurderings- og omtalemoduler
description: Dette emnet dekker vurderings- og omtalemoduler som brukes på sider med produktdetaljer i Microsoft Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 09/15/2020
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
ms.author: gmohanv
ms.search.validFrom: 2020-10-31
ms.dyn365.ops.version: Release 10.0.6
ms.openlocfilehash: 85fb1272103eed7d6e44635b7c20438471d96b34
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414745"
---
# <a name="ratings-and-reviews-modules"></a>Vurderings- og omtalemoduler

[!include [banner](includes/banner.md)]

Dette emnet dekker vurderings- og omtalemoduler som brukes på sider med produktdetaljer i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Vurderinger og evalueringer på e-handelswebområder hjelper kunder med å lære om produkter før de tar en avgjørelse, og det er også en metode for å samle inn tilbakemeldinger fra kunder om produkter. 

Vurderingene vises på produktlistesider, kategorilistesider, sider for søkeresultater og andre områdesider. 

Vurderingshistogrammer og produktgjennomganger vises på sider for produktdetaljer. En **Skriv en vurdering**-knapp gir kundene muligheten til å sende inn rangeringer og omtaler for et produkt. Disse PDP-funksjonene kontrolleres av vurderings- og omtalemoduler.

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
![Dialogboksen Skriv en vurdering](media/rnr-eCommerce-write-review-module.png) Tabellen nedenfor viser egenskapen for Skriv en vurdering-modulen som må konfigureres i redigeringsverktøyet.
| Egenskapsnavn | Verdi        | Egenskapsbeskrivelse                 |
|---------------|--------------|--------------------------------------|
| Navn          | Skriv vurdering | Navnet på Skriv en vurdering-modulen |

### <a name="ratings-histogram-module"></a>Modul for vurderingshistogrammer

Modul for vurderingshistogrammer viser vurderingshistogrammet. Denne modulen vises vanligvis mellom Skriv vurdering-modulen og listemodulen for produktvurderinger på en PDP.
Histogrammodulen for vurderinger krever ingen konfigurasjon. Du trenger bare å legge til modulen i PDP-malen. Illustrasjonene nedenfor viser hvordan en PDP-mal ser ut i Dynamics 365 Commerce når modulene for vurderinger og gjennomgang er konfigurert for visning på PDPer.
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

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Beholdermodul](add-container-module.md)

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
