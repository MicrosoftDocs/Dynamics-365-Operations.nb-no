---
title: Navigasjonsmenymodul
description: Dette emnet dekker navigasjonsmenymoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/01/2020
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
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: b0e8168ca9ec9ca68011650a73cc09983deca645
ms.sourcegitcommit: 765056b5dc1d0a8c27e56ff2cbd310ad3349ff09
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/20/2020
ms.locfileid: "4055743"
---
# <a name="navigation-menu-module"></a>Navigasjonsmenymodul

[!include [banner](includes/banner.md)]

Dette emnet dekker navigasjonsmenymoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Hovedformålet med navigasjonsmenymoduler er å gjøre det mulig for områdebrukere å bla gjennom produkter og områdesider i henhold til kanalnavigeringshierarkiet som er definert i Dynamics 365 Commerce-hovedkvarteret. Elementer som er konfigurert i en navigasjonsmenymodul, vises som navigasjon i områdehodet. Navigasjonsmenymoduler støtter også statiske menyelementer som kobles til andre sider på et e-handelsområde.

Navigasjonsmenymodulen kan legges til i topptekstmodulen på en side. I Fabrikam-temaet viser navigasjonsmenyen to nivåer som standard. I Starter-temaet viser navigasjonsmenyen tre nivåer som standard. Hvis du vil endre antall nivåer, kreves det en visningsutvidelse i temaet.

Følgende illustrasjon viser et eksempel på en navigasjonsmeny for området Fabrikam med to nivåer med kategorihierarki og enkelte statiske menyelementer.
![Eksempel på en navigasjonsmenymodul](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Egenskaper for navigasjonsmenymodul

| Egenskapsnavn             | Verdi                 | beskrivelse |
|---------------------------|-----------------------|-------------|
| Kilde                  | **Detaljhandel** , **Manuell redigering** , **Detaljhandel og manuell redigering** | Verdien for **Detaljhandel** gjør at kanalnavigasjonshierarkiet fra Commerce-hovedkontoret vises på navigasjonsmenyen. Veridn for **Manuell redigering** tillater at statiske menyelementer blir kuratert. Verdien for **Detaljhandel og manuell redigering** tilbyr en kombinasjon av begge. |
| Vise kategoribilder | **Sann** eller **Usann**    | Når denne egenskapen er aktivert, vises kategoribilder på navigasjonsmenyen, som definert i Commerce Headquarters for hver kategori. Lagt til i Commerce-versjon 10.0.14. |
| Aktiver navigasjonsmeny med flere nivåer | **Sann** eller **Usann** | Når denne egenskapen er aktivert, kan navigasjonsmenyen vise flere nivåer i navigasjonshierarkiet. Denne funksjonen er tilgjengelig i Dynamics 365 Commerce versjon 10.0.15. |
| Antall nivåer | heltall | Denne egenskapen definerer antall nivåer som skal vises hvis egenskapen **Aktiver navigasjonsmeny med flere nivåer** er satt til **sann**. |
| Statisk menyelement| Matrise med verdier| Statiske menyelementer som knytter et menyelementnavn til en kobling til en statisk områdeside. Du kan opprette menyelementer under andre menyelementer. Som standard vises statiske menyer på rotnivå, og de blir lagt ved kanalnavigasjonshierarkiet hvis det finnes. |
| Vis rotmeny | **Sann** eller **Usann** | Når denne egenskapen er aktivert, kan navigasjonsmenyen defineres under en egendefinert rot (for eksempel **Handle nå** ). Denne funksjonen er tilgjengelig i Dynamics 365 Commerce versjon 10.0.15. |
| Rotmeny | streng | Denne egenskapen kan brukes til å definere tekst for en egendefinert rot hvis egenskapen **Vis rotmeny** er satt til **sann**. |

Følgende illustrasjon viser et eksempel på et kategoribilde som vises på navigasjonsmenyen for Fabrikam-området.
![Eksempel på en navigasjonsmenymodul med kategoribilder](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Legge til en navigasjonsmenymodul i en topptekstmodul

Hvis du vil ha mer informasjon om hvordan du legger til en navigasjonsmenymodul i en topptekstmodul, kan du se [Topptekstmodul](author-header-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Søkebanemodul](add-breadcrumb.md)

[Områdevelgermodul](site-selector.md)

[Kjøpsboksmodul](add-buy-box.md)

[Informasjonskapselsamsvar](cookie-compliance.md)

[Topptekstmodul](author-header-module.md)
