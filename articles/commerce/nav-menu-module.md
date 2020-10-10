---
title: Navigasjonsmenymodul
description: Dette emnet dekker navigasjonsmenymoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 08/31/2020
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
ms.openlocfilehash: 9f66bbe7bf436ab6360dda7d92d6d51e47eedf16
ms.sourcegitcommit: 420b9e538f706178f8e1f2786e02f4f400bf2336
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/02/2020
ms.locfileid: "3761412"
---
# <a name="navigation-menu-module"></a>Navigasjonsmenymodul

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet dekker navigasjonsmenymoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Hovedformålet med navigasjonsmenymoduler er å gjøre det mulig for områdebrukere å bla gjennom produkter og områdesider i henhold til kanalnavigeringshierarkiet som er definert i Dynamics 365 Commerce-hovedkvarteret. Elementer som er konfigurert i en navigasjonsmenymodul, vises som navigasjon i områdehodet. Navigasjonsmenymoduler støtter også statiske menyelementer som kobles til andre sider på et e-handelsområde.

Navigasjonsmenymodulen kan legges til i topptekstmodulen på en side. I Fabrikam-temaet viser navigasjonsmenyen to nivåer som standard. I Starter-temaet viser navigasjonsmenyen tre nivåer som standard. Hvis du vil endre antall nivåer, kreves det en visningsutvidelse i temaet.

Følgende illustrasjon viser et eksempel på en navigasjonsmeny for området Fabrikam med to nivåer med kategorihierarki og enkelte statiske menyelementer.
![Eksempel på en navigasjonsmenymodul](./media/ecommerce-header.png)

## <a name="navigation-menu-module-properties"></a>Egenskaper for navigasjonsmenymodul

| Egenskapsnavn             | Verdi                 | beskrivelse |
|---------------------------|-----------------------|-------------|
| Kilde                  | **Detaljhandel**, **Manuell redigering**, **Detaljhandel og manuell redigering** | Verdien for **Detaljhandel** gjør at kanalnavigasjonshierarkiet fra Commerce-hovedkontoret vises på navigasjonsmenyen. Veridn for **Manuell redigering** tillater at statiske menyelementer blir kuratert. Verdien for **Detaljhandel og manuell redigering** tilbyr en kombinasjon av begge. |
| Vise kategoribilder | **Sann** eller **Usann**    | Når denne egenskapen er aktivert, vises kategoribilder på navigasjonsmenyen, som definert i Commerce Headquarters for hver kategori. Lagt til i Commerce-versjon 10.0.14. |
| Statisk menyelement| Matrise med verdier| Statiske menyelementer som knytter et menyelementnavn til en kobling til en statisk områdeside. Du kan opprette menyelementer under andre menyelementer. Som standard vises statiske menyer på rotnivå, og de blir lagt ved kanalnavigasjonshierarkiet hvis det finnes. |

Følgende illustrasjon viser et eksempel på et kategoribilde som vises på navigasjonsmenyen for Fabrikam-området.
![Eksempel på en navigasjonsmenymodul med kategoribilder](./media/ecommerce-categoryimages.PNG)

## <a name="add-a-navigation-menu-module-to-a-header-module"></a>Legge til en navigasjonsmenymodul i en topptekstmodul

Hvis du vil ha mer informasjon om hvordan du legger til en navigasjonsmenymodul i en topptekstmodul, kan du se [Topptekstmodul](author-header-module.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Kjøpsboksmodul](add-buy-box.md)

[Informasjonskapselsamsvar](cookie-compliance.md)

[Topptekstmodul](author-header-module.md)