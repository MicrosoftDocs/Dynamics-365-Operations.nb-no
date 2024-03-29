---
title: Kartmodul
description: Denne artikkelen dekker kartmoduler og beskriver hvordan du konfigurerer dem i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2020-02-10
ms.dyn365.ops.version: Release 10.0.13
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d72091baf2f216bfbe33950950f8917c3ba1ba5c
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283353"
---
# <a name="map-module"></a>Kartmodul

[!include [banner](includes/banner.md)]


Denne artikkelen dekker kartmoduler og beskriver hvordan du konfigurerer dem i Microsoft Dynamics 365 Commerce.

En kartmodul viser plasseringen av butikker på et interaktivt kart som gjengis ved hjelp av [Bing Maps V8-webkontrollen](/bingmaps/v8-web-control/). En API-nøkkel for Bing-kart kreves, og den må legges til på siden Delte parametere for Commerce Headquarters. Kartmoduler gir forskjellige visninger, for eksempel veier, fra luften og på gatenivå, som brukerne kan velge for å vise kartstedene. De tillater også samhandlinger, som å zoome og bruke brukerens plassering.

En kartmodul fungerer sammen med butikkvelgermodulen for å bestemme de geografiske lokasjonene til butikkene som må gjengis på et kart. Butikkvelgeren og kartmodulene fungerer sammen når en bruker velger en butikk i en av disse modulene på en områdeside. Kartmoduler kan utvides for andre scenarier, utover samhandling med butikkvelgermoduler. Modultilpassing er imidlertid nødvendig.

> [!NOTE]
> Kartmodulen er tilgjengelig i Dynamics 365 Commerce 10.0.13-versjonen.

Bildet nedenfor viser et eksempel på en kartmodul som brukes på en side med butikkplasseringer.

![Eksempel på en butikkvelgermodul.](./media/ecommerce-Storelocator.PNG)

## <a name="module-properties"></a>Modulegenskaper

| Egenskapsnavn             | Verdi                 | beskrivelse |
|---------------------------|-----------------------|-------------|
| Overskrift | Tekst | Overskriften for modulen. |
| Alternativer for stift: standardikon | Bilde | Bildet for stiftsymbolen som skal brukes for butikker som vises på et kart. |
| Alternativer for stift: aktivt ikon | Bilde | Bildet for stiftsymbolen som skal brukes for en butikk som er valgt på et kart. |
| Alternativer for stift: standard ikonfarge | Tegnstreng | Teksten eller den heksadesimale verdien for stiftsymboler på et kart. |
| Alternativer for stift: farge for aktivt ikon | Tegnstreng | Teksten eller den heksadesimale verdien for valgte stiftsymboler på et kart. |
| Vis indeks | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann**, vil hvert stiftsymbol som angir en butikk, vise en indeks. Denne indeksen samsvarer med indeksen i listevisningen som butikkvelgermodulen viser. |

## <a name="add-allowed-mapping-urls-to-a-sites-content-security-policy-directives"></a>Legge til tillatte URL-adresser for tilordning til et områdes sikkerhetspolicy for innhold

For at kartmodulen skal kunne kommunisere med Bing Maps, må du kontrollere at følgende URL-adresser for tilordning er tillatt i henhold til områdets sikkerhetspolicy for innhold (CSP). Dette oppsettet gjøres i Commerce-områdebygger ved å legge til tillatte URL-adresser i CSP-direktiver for ulike områder (for eksempel **img-src**). Hvis du vil ha mer informasjon, se [Innholdssikkerhetspolicy](manage-csp.md). 

- For direktivet **connect-src** legger du til **&#42;.bing.com**.
- For direktivet **img-src** legger du til **&#42;.virtualearth.net**.
- For direktivet **script-src** legger du til **&#42;.bing.com, &#42;.virtualearth.net**.
- For direktivet **script style-src** legger du til **&#42;.bing.com**.

## <a name="add-a-map-module-to-a-page"></a>Legge til en kartmodul på en side

Hvis du vil ha detaljert informasjon om hvordan du konfigurerer en kartmodul på en side, kan du se [Butikkvelgermodul](store-selector.md). 
 
## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Butikkvelgermodul](store-selector.md)

[Behandle Bing-kart for organisasjonen](./dev-itpro/manage-bing-maps.md)

[Bing Maps V8-webkontrollen](/bingmaps/v8-web-control/)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
