---
title: Oversikt over Adventure Works-tema
description: Dette emnet gir en oversikt over Adventure Works-emnet, og beskriver hvordan det brukes på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/21/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 5bade39b1b327a0784272669ce074d9762a318c2cad6d4105f0d186c91d2593f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6733234"
---
# <a name="adventure-works-theme-overview"></a>Oversikt over Adventure Works-tema

[!include [banner](includes/banner.md)]

Dette emnet gir en oversikt over Adventure Works-emnet, og beskriver hvordan det brukes på områdesider i Microsoft Dynamics 365 Commerce.

Dynamics 365 Commerce har et tema for e-handel som kalles Adventure Works. Adventure Works-temaet handler om sport og fritidsprodukter, og er optimalisert for en omfattende og utvidet fortellingserfaring. Det gir et moderne utseende, nytt oppsett og animasjonseffekter som skaper en oppslukende, engasjernde handleopplevelse for e-handelskunder.

## <a name="trial-environments-in-commerce"></a>Prøvemiljøer i Commerce

Hvis du vil se hvordan Adventure Works-emnet ser ut når det distribueres for bedrift-til-kunde- (B2C) og bedrift-til-bedrift-områder (B2B), kan du gå til følgende prøveområder:

- [B2C-området Adventure Works](https://www.adventure-works.com/)
- [B2B-området Adventure Works](https://www.adventure-works.com/business)

## <a name="theme-capabilities"></a>Temafunksjoner

Adventure Works-emnet inneholder følgende nye funksjoner:

- Videospillermodulen støtter nå overskrift, avsnitt og koblingsfunksjonalitet for ytterligere fortelling.
- Det er bedre overganger for innhold gjennom animasjon.
- Handlingen "Legg til handlekurv" starter minikurven i stedet for å gi en melding.
- Modulen for hurtigvisning er en rute som vises både på skrivebordet og i mobilvisninger.
- Det finnes nye oppsett for områdesidene. 
- Markedsføringsinnhold kan konfigureres for kurven og minikurven når de er tomme.
- Minikurven kan vise kampanjemeldinger, for eksempel "Gratis levering ved bestilling over 500 kroner."
- Beskrivelseskort gjengis på søke- og kategorisider.

Adventure Works-temaet inneholder nå følgende fortellingsmoduler i Commerce-modulbiblioteket:

- [Flislistemodul](tile-list-module.md)
- [Interaktiv funksjonsmodul](interactive-feature-module.md)
- [Aktiv bildemodul](active-image-module.md)
- [Abonnementsmodul](subscribe-module.md)
- [Bildelistemodul](image-list-module.md)

Adventure Works-emnet svarer fullstendig og gir en optimalisert erfaring for visning på skrivebord, mobil og nettbrett.

> [!IMPORTANT]
> Adventure Works-temaet og de nye modulene er tilgjengelige fra Dynamics 365 Commerce 10.0.20-versjonen.

Illustrasjonen nedenfor viser et eksempel på en hjemmeside som bruker Adventure Works-emnet.

![Eksempel på en hjemmeside som bruker Adventure Works-emnet](./media/aw_b2c.PNG)

Illustrasjonen nedenfor viser et eksempel på en listeside som bruker Adventure Works-emnet.

![Eksempel på en listeside som bruker Adventure Works-emnet](./media/Aw_list.PNG)

Illustrasjonen nedenfor viser et eksempel på en produktdetaljside som bruker Adventure Works-emnet.

![Eksempel på en produktdetaljside som bruker Adventure Works-emnet](./media/aw_pdp.PNG)

## <a name="use-the-adventure-works-theme-for-b2b-sites"></a>Bruke Adventure Works-emnet for B2B-områder

Adventure Works-emnet er også et referansetema for B2B-områder (business-to-business). Alle B2B-moduler og arbeidsflyter vises i Adventure Works-emnet. Hvis du vil ha mer informasjon om hvordan du konfigurerer et B2B-område, kan du se [Oppsett av B2B-område](./b2b/set-up-b2b-site.md).

Illustrasjonen nedenfor viser et eksempel på en B2B-hjemmeside som bruker Adventure Works-emnet.

![Eksempel på en B2B-hjemmeside som bruker Adventure Works-emnet](./media/aw_b2b.PNG)

## <a name="theme-extensions"></a>Emnetillegg

Adventure Works-emnet inneholder flere emneutvidelser, for eksempel **Visningstillegg** og **Moduldefinisjonstillegg**. Adventure Works-emnet kan brukes som referansetema for å bygge like utvidelser. Listesiden i Adventure Works-emnet implementeres for eksempel som en visningsutvidelse som har en vannrett presisering. (I kontrast til dette brukes en venstre rute-presisering i Fabrikam-emnet.)

På samme måte omfatter andre moduler moduldefinisjonstillegg. For eksempel inneholder [kurvikonmodulen](cart-icon-module.md) to ekstra **Tom kurv**- og **Kampanjeinnhold**-spor som implementeres ved hjelp av moduldefinisjonstillegg. I tillegg er det lagt til en ny **Mobillogo**-egenskap i hodemodulen for å støtte en logo på mobilvisninger. Denne egenskapen implementeres som filtypen for definisjon av hodemodulen.

Hvis du vil ha mer informasjon om emneutvidelser, kan du se [Emnetillegg](e-commerce-extensibility/theme-module-extensions.md).

## <a name="install-the-adventure-works-theme"></a>Installere Adventure Works-temaet

Hvis du vil ha mer informasjon om hvordan du installerer Adventure Works-temaet, kan du se [Installere Adventure Works-temaet](install-adventure-works.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Flislistemodul](tile-list-module.md)

[Interaktiv funksjonsmodul](interactive-feature-module.md)

[Aktiv bildemodul](active-image-module.md)

[Abonner-modul](subscribe-module.md)

[Bildelistemodul](image-list-module.md)

[Emnetillegg](e-commerce-extensibility/theme-module-extensions.md)

[Handlekurvikonmodul](cart-icon-module.md)

[Definere et e-handelsområde for B2B](./b2b/set-up-b2b-site.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
