---
title: Navigasjonsmenymodul
description: Denne artikkelen dekker navigasjonsmenymoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 10/27/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d58d3957749fa961b7be164a0a474ac90a23321f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9281515"
---
# <a name="navigation-menu-module"></a>Navigasjonsmenymodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker navigasjonsmenymoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

Hovedformålet med navigasjonsmenymoduler er å gjøre det mulig for områdebrukere å bla gjennom produkter og områdesider i henhold til kanalnavigeringshierarkiet som er definert i Dynamics 365 Commerce-hovedkvarteret. Elementer som er konfigurert i en navigasjonsmenymodul, vises som navigasjon i områdehodet. Navigasjonsmenymoduler støtter også statiske menyelementer som kobles til andre sider på et e-handelsområde.

Navigasjonsmenymodulen kan legges til i topptekstmodulen på en side. I Fabrikam-temaet viser navigasjonsmenyen to nivåer som standard. I Starter-temaet viser navigasjonsmenyen tre nivåer som standard. Hvis du vil endre antall nivåer, kreves det en visningsutvidelse i temaet.

Følgende illustrasjon viser et eksempel på en navigasjonsmeny for området Fabrikam med to nivåer med kategorihierarki og enkelte statiske menyelementer.
![Eksempel på en navigasjonsmenymodul.](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Egenskaper for navigasjonsmenymodul

| Egenskapsnavn             | Verdi                 | beskrivelse |
|---------------------------|-----------------------|-------------|
| Kilde                  | **Detaljhandel**, **Manuell redigering**, **Detaljhandel og manuell redigering** | Verdien for **Detaljhandel** gjør at kanalnavigasjonshierarkiet fra Commerce-hovedkontoret vises på navigasjonsmenyen. Veridn for **Manuell redigering** tillater at statiske menyelementer blir kuratert. Verdien for **Detaljhandel og manuell redigering** tilbyr en kombinasjon av begge. |
| Vise kategoribilder | **Sann** eller **Usann**    | Når denne egenskapen er aktivert, vises kategoribilder på navigasjonsmenyen, som definert i Commerce Headquarters for hver kategori. Lagt til i Commerce-versjon 10.0.14. |
| Vis kampanjebilder | **Sann** eller **Usann** | Når denne egenskapen er aktivert, kan kampanjer konfigureres ved hjelp av bilder, koblinger og tekst. Denne egenskapen ble lagt til i Commerce versjon 10.0.17-versjonen. |
|Legge til kampanjeinnhold for kategori | Tekst, bilde eller kobling | Når egenskapen **Vis kampanjebilder** er aktivert, kan du legge til tekst, et bilde eller en kobling som kampanjeinnhold på navigasjonsmenyen. |
| Aktiver navigasjonsmeny med flere nivåer | **Sann** eller **Usann** | Når denne egenskapen er aktivert, kan navigasjonsmenyen vise flere nivåer i navigasjonshierarkiet. Denne funksjonen er tilgjengelig i Commerce versjon 10.0.15-versjonen. |
| Antall nivåer | heltall | Denne egenskapen definerer antall nivåer som skal vises hvis egenskapen **Aktiver navigasjonsmeny med flere nivåer** er satt til **sann**. |
| Statisk menyelement| Matrise med verdier| Statiske menyelementer som knytter et menyelementnavn til en kobling til en statisk områdeside. Du kan opprette menyelementer under andre menyelementer. Som standard vises statiske menyer på rotnivå, og de blir lagt ved kanalnavigasjonshierarkiet hvis det finnes. |
| Vis rotmeny | **Sann** eller **Usann** | Når denne egenskapen er aktivert, kan navigasjonsmenyen defineres under en egendefinert rot (for eksempel **Handle nå**). Denne funksjonen er tilgjengelig i Dynamics 365 Commerce versjon 10.0.15. |
| Rotmeny | streng | Denne egenskapen kan brukes til å definere tekst for en egendefinert rot hvis egenskapen **Vis rotmeny** er satt til **sann**. |

Følgende illustrasjon viser et eksempel på et kategoribilde som vises på navigasjonsmenyen for Fabrikam-området.
![Eksempel på en navigasjonsmenymodul med kategoribilder.](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Legge til en navigasjonsmenymodul i en topptekstmodul

Hvis du vil ha mer informasjon om hvordan du legger til en navigasjonsmenymodul i en topptekstmodul, kan du se [Topptekstmodul](author-header-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Søkebanemodul](add-breadcrumb.md)

[Områdevelgermodul](site-selector.md)

[Kjøpsboksmodul](add-buy-box.md)

[Informasjonskapselsamsvar](cookie-compliance.md)

[Topptekstmodul](author-header-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
