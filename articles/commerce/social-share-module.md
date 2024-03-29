---
title: Modul for sosial deling
description: Denne artikkelen dekker moduler for sosial deling for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
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
ms.openlocfilehash: 88bc5469e3072b625836cc942efbd2206f6dd6ba
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9284691"
---
# <a name="social-share-module"></a>Modul for sosial deling

[!include [banner](includes/banner.md)]

Denne artikkelen dekker moduler for sosial deling for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

Med moduler for sosial deling kan brukere dele URL-adresser på områdesidene for e-handel på sosiale medier, for eksempel Facebook Twitter, Pinterest og LinkedIn. URL-adresser til områdesider kan også deles via e-post. Moduler for sosial deling brukes vanligvis på sider for produktdetaljer (PDP-er) for å hjelpe brukere med å dele produktinformasjon.

Hver modul for sosialdeling er en beholder for varemoduler for sosial deling. Hver varemodul for sosial deling kan konfigureres slik at den peker til et bestemt område for sosiale medier. Integrering med Facebook, Twitter, Pinterest, LinkedIn og e-post støttes som standard. Når en områdebruker velger et symbol for sosiale medier, startes en forekomst av HTML iFrame for det respektive området for sosialt medium. I iFrame kan brukeren logge på og legge inn sideinnholdet de studerte.

Hver sosiale medieplattform kan spore informasjonskapsler, så denne modulen krever at områdebrukere godtar varslingen om samtykke for informasjonskapsel. Når samtykke for informasjonskapsel ikke godkjennes, vil modulen være skjult på siden. Hvis du vil ha mer informasjon, kan du se [Samsvar for informasjonskapsel](cookie-compliance.md).

Illustrasjonen nedenfor viser et eksempel på en modul for sosial deling som brukes på en produktdetaljside.

![Eksempel på en modul for sosial deling.](./media/ecommerce-socialshare.png)

## <a name="social-share-module-properties"></a>Egenskaper for modul for sosial deling

| Egenskapsnavn             | Verdi                 | beskrivelse |
|---------------------------|-----------------------|-------------|
| Overskrift                  | Tekst | Denne egenskapen angir en tittel for modulen. |
| Retning | **Vannrett** eller **Loddrett**  | Denne egenskapen definerer oppsettsretningen for elementene for sosiale medier. |

## <a name="social-share-item-module-properties"></a>Egenskaper for varemodul for sosial deling
| Egenskapsnavn             | Verdi                 | beskrivelse |
|---------------------------|-----------------------|-------------|
| Sosiale medier              | **Facebook**, **Twitter**, **Pinterest**, **LinkedIn**, **Mail** | En rullegardinmeny med en liste over plattformer for sosiale medier. |
| Ikon |Bilde    | Dette vil være bildet som vil vises for de respektive sosiale mediene. Den beste fremgangsmåten får du ved å se SDK for plattform for sosiale medier for det anbefalte bildet som skal brukes for hver plattform. |

## <a name="add-a-social-share-module-to-a-buy-box-module"></a>Legg til en modul for sosial deling i en kjøpsboksmodul

Hvis du vil legge til en modul for sosial deling i en kjøpsboksmodul, gjør du følgende:

1. Velg **Sider** på Fabrikam-området, og velg deretter siden **DefaultPDP** for å åpne siden med produktdetaljer. 
1. I sporet **Kjøpsboks (obligatorisk)** velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du modulen **Sosial deling**, og deretter velger du **OK**.
1. I sporet **Sosial deling** velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du modulen **SocialShare**, og deretter velger du **OK**.
1. I egenskapsruten for modulen **Sosial deling** velger du **Vannrett** under **Retning**. Legg til en bildetekst etter behov.
1. I sporet **SocialShare** velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **SocialShareItem**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for modulen **SocialShareItem** velger du **Facebook** under **Sosiale medier**.
1. I egenskapsruten for modulen **SocialShareItem** velger du **+ Legg til et bilde** under **Ikon**.
1. I dialogboksen **Medievelger** velger du logobildet Facebook, og deretter velger du **OK**. Hvis et logobilde for Facebook ikke finnes, velger du **Last opp nytt medieelement** for å laste opp et bilde.
1. Legg til og konfigurer flere forekomster av modulen **SocialShareItem** etter behov.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden. Siden vil vise modulen for sodial deling.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Kjøpsboksmodul](add-buy-box.md)

[Informasjonskapselsamsvar](cookie-compliance.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
