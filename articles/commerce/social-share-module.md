---
title: Sosial deling-modul
description: Dette emnet dekker moduler for sosial deling for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
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
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.14
ms.openlocfilehash: 82a8795360f453cdee19fa6e9e376a42e8276849
ms.sourcegitcommit: 510ca8b14d8b5334e50aca1b15d636c65fcc9888
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/16/2020
ms.locfileid: "4414774"
---
# <a name="social-share-module"></a>Sosial deling-modul

[!include [banner](includes/banner.md)]

Dette emnet dekker moduler for sosial deling for informasjonskapsel og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Med moduler for sosial deling kan brukere dele URL-adresser på områdesidene for e-handel på sosiale medier, for eksempel Facebook Twitter, Pinterest og LinkedIn. URL-adresser til områdesider kan også deles via e-post. Moduler for sosial deling brukes vanligvis på sider for produktdetaljer (PDP-er) for å hjelpe brukere med å dele produktinformasjon.

Hver modul for sosialdeling er en beholder for varemoduler for sosial deling. Hver varemodul for sosial deling kan konfigureres slik at den peker til et bestemt område for sosiale medier. Integrering med Facebook, Twitter, Pinterest, LinkedIn og e-post støttes som standard. Når en områdebruker velger et symbol for sosiale medier, startes en forekomst av HTML iFrame for det respektive området for sosialt medium. I iFrame kan brukeren logge på og legge inn sideinnholdet de studerte.

Hver sosiale medieplattform kan spore informasjonskapsler, så denne modulen krever at områdebrukere godtar varslingen om samtykke for informasjonskapsel. Når samtykke for informasjonskapsel ikke godkjennes, vil modulen være skjult på siden. Hvis du vil ha mer informasjon, kan du se [Samsvar for informasjonskapsel](cookie-compliance.md).

Illustrasjonen nedenfor viser et eksempel på en modul for sosial deling som brukes på en produktdetaljside.

![Eksempel på en modul for sosial deling](./media/ecommerce-socialshare.png)

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
1. I dialogboksen **Legg til modul** velger du modulen **Sosial deling**, og deretter velger du **OK**.
1. I sporet **Sosial deling** velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du modulen **Sosial deling**, og deretter velger du **OK**.
1. I egenskapsruten for modulen **Sosial deling** velger du **Vannrett** under **Retning**. Legg til en bildetekst etter behov.
1. I sporet **Sosial deling** velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du modulen **SocialShareItem**, og deretter velger du **OK**.
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
