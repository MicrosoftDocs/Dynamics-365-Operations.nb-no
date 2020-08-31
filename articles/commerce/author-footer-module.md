---
title: Bunntekstmodul
description: Dette emnet dekker bunntekstmoduler og hvordan du redigerer dem i Dynamics 365 Commerce.
author: anupamar
manager: annbe
ms.date: 05/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar-ms
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: e81617979a945274500c9f4ceaa8078d8dfd79e8
ms.sourcegitcommit: 81f162f2d50557d7afe292c8d326618ba0bc3259
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/11/2020
ms.locfileid: "3686724"
---
# <a name="footer-module"></a>Bunntekstmodul  

[!include [banner](includes/banner.md)]

Dette emnet dekker bunntekstmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Bunntekstmodulen er en spesialcontainer som brukes til å være vert for modulene som vises i bunnteksten på siden. Den kan for eksempel inneholde koblinger til ulike sider på området, for eksempel sider for **Kontakt oss** og **Butikkpolicyer**.

Bildet nedenfor viser et eksempel på en bunntekstmodul på en områdeside.

![Eksempel på en bunntekstmodul](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Egenskaper for bunntekstmodul 

I likhet med de fleste containere støtter en bunntekstmodul egenskaper for overskriften og bredden. Den støtter også tillegging av flere bunntekstkategorimoduler. Hver bunntekstkategorimodul som legges til, gjengis som en kolonne i bunntekstmodulen.

## <a name="modules-available-in-a-footer-module"></a>Moduler som er tilgjengelige i en bunntekstmodul

**Bunntekstelementer** – En modul for bunntekstelementer kan inneholde en overskrift, et bilde og en kobling. Overskriften kan enten brukes alene eller sammen med et bilde og en kobling. Hver kobling i bunnteksten kan konfigureres slik at den har bare tekst (for eksempel "Kontakt oss"- og "Personvern"-koblinger), eller slik at den har både tekst og et bilde (for eksempel koblinger til sosiale medier).

**Til toppen** – En Til toppen-modul gir en kobling for rask navigering til toppen av siden. Et mål kreves. Standard målverdi er \#, som fører brukeren til toppen av siden.

## <a name="create-a-footer-module"></a>Opprette en bunntekstmodul

1. Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.
1. I dialogboksen **Nytt sidefragment** velger du **Beholder**-modulen, skriver inn et navn på sidefragmentet og velger **OK**.
1. I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Bunntekstkategori**-modulen, og deretter velger du **OK**.
1. I **Bunntekstkategori**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Bunntekstelement**-modulen, og deretter velger du **OK**.
1. Velg **Bunntekstelement**-sporet. Deretter, i egenskapsruten til høyre, konfigurerer du overskriften, koblingen, koblingsteksten og bildet etter behov.
1. Gjenta trinn 5 til og med 7 for hvert element for å legge til flere bunntekstelementer.
1. For å legge til "Til toppen"-kobling i bunnteksten velger du ellipsen (**…**) i **Bunntekstkategori**-sporet, og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Til toppen**-modulen, og deretter velger du **OK**.
1. Velg **Til toppen**-sporet. Deretter, i egenskapsruten til høyre, konfigurerer du teksten og andre modulegenskaper etter behov.
1. Velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere den.

For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.

1. I **Bunntekst**-sporet på **Standardside**-modulen legger du til bunntekstfragmentet du opprettet.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.

Ved å legge til sidefragmentet i sidemaler garanteres det at bunnteksten gjengis på hver side.

## <a name="additional-resources"></a>Tilleggsressurser

[Startpakke, oversikt](starter-kit-overview.md)

[Containermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)
