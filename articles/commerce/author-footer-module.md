---
title: Bunntekstmodul
description: Denne artikkelen dekker bunntekstmoduler og hvordan du redigerer dem i Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 4e7796d9700eabc923f2bb45187832d5993ae56e
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8876618"
---
# <a name="footer-module"></a>Bunntekstmodul  

[!include [banner](includes/banner.md)]

Denne artikkelen dekker bunntekstmoduler og beskriver hvordan du oppretter dem i Microsoft Dynamics 365 Commerce.

Bunntekstmodulen er en spesialcontainer som brukes til å være vert for modulene som vises i bunnteksten på siden. Den kan for eksempel inneholde koblinger til ulike sider på området, for eksempel sider for **Kontakt oss** og **Butikkpolicyer**.

Bildet nedenfor viser et eksempel på en bunntekstmodul på en områdeside.

![Eksempel på en bunntekstmodul.](./media/ecommerce-footer.PNG)

## <a name="footer-module-properties"></a>Egenskaper for bunntekstmodul 

I likhet med de fleste containere støtter en bunntekstmodul egenskaper for overskriften og bredden. Den støtter også tillegging av flere bunntekstkategorimoduler. Hver bunntekstkategorimodul som legges til, gjengis som en kolonne i bunntekstmodulen.

## <a name="modules-available-in-a-footer-module"></a>Moduler som er tilgjengelige i en bunntekstmodul

**Bunntekstelement** – En modul for bunntekstelement kan inneholde en overskrift eller en kobling. Overskriften brukes vanligvis som en tittel på bunntekstdelen.  Hver kobling i bunnteksten kan konfigureres slik at den har bare tekst (for eksempel "Kontakt oss"- og "Personvern"-koblinger), eller slik at den har både tekst og et bilde (for eksempel koblinger til sosiale medier). Hvis det finnes både en overskrift og en kobling, har overskriftsegenskapen prioritet over koblingen. 

**Til toppen** – En Til toppen-modul gir en kobling for rask navigering til toppen av siden. Et mål kreves. Standard målverdi er \#, som fører brukeren til toppen av siden.

## <a name="create-a-footer-module"></a>Opprette en bunntekstmodul

1. Gå til **Fragmenter**, og velg **Nytt** for å opprette et nytt sidefragment.
1. I dialogboksen **Velg et fragment** velger du **Beholder**-modulen, skriver inn et navn på fragmentet og velger **OK**.
1. I **Standard beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Bunntekstkategori**-modulen, og deretter velger du **OK**.
1. I **Bunntekstkategori**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Bunntekstelement**-modulen, og deretter velger du **OK**.
1. Velg **Bunntekstelement**-sporet. Deretter, i egenskapsruten til høyre, konfigurerer du overskriften, koblingen, koblingsteksten og bildet etter behov.
1. Gjenta trinn 5 til og med 7 for hvert element for å legge til flere bunntekstelementer.
1. For å legge til "Til toppen"-kobling i bunnteksten velger du ellipsen (**…**) i **Bunntekstkategori**-sporet, og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Til toppen**-modulen, og deretter velger du **OK**.
1. Velg **Til toppen**-sporet. Deretter, i egenskapsruten til høyre, konfigurerer du teksten og andre modulegenskaper etter behov.
1. Velg **Fullfør redigering** for å sjekke inn fragmentet, og velg deretter **Publiser** for å publisere den.

For å sikre at det vises en topptekst på hver side, kan du følge denne fremgangsmåten på hver sidemal som opprettes for området.

1. I **Bunntekst**-sporet på **Standardside**-modulen legger du til bunntekstfragmentet du opprettet.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.

Ved å legge til fragmentet i sidemaler garanteres det at bunnteksten gjengis på hver side.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Beholdermodul](add-container-module.md)

[Kjøpsboksmodul](add-buy-box.md)

[Handlekurvmodul](add-cart-module.md)

[Kassemodul](add-checkout-module.md)

[Ordrebekreftelsesmodul](order-confirmation-module.md)

[Topptekstmodul](author-header-module.md)

[Bunntekstmodul](author-footer-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
