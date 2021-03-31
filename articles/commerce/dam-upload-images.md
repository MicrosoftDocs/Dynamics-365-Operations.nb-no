---
title: Laste opp bilder
description: Dette emnet beskriver hvordan du laster opp bilder i områdebyggeren for Microsoft Dynamics 365 Commerce.
author: psimolin
manager: annbe
ms.date: 03/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 51571ce221714598b2e2d39c76cb69dcb57cc52b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5213800"
---
# <a name="upload-images"></a>Laste opp bilder

[!include [banner](includes/banner.md)]

Dette emnet beskriver hvordan du laster opp bilder i områdebyggeren for Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Med mediebiblioteket for Commerce-områdebygger kan du laste opp bilder, enten enkeltvis eller flere samtidig ved hjelp av mapper. Du bør alltid laste opp den versjonen av bildet med høyest oppløsning og kvalitet, fordi bildeskaleringskomponenten automatisk vil optimalisere bildet for forskjellige visningsporter og deres stoppunkter.

### <a name="image-information-specified-during-upload"></a>Bildeinformasjon som angis under opplasting

Når du laster opp et bilde, kan følgende informasjon angis.

- **Tittel, alt-tekst, beskrivelse, nøkkelord**: metadata for bildet eller bildene. Tittel og alt-tekst er obligatoriske verdier.
- **Velg kategori**:
    - **Ingen**: brukes for beskrivelse av bilde eller bilder i e-handel.
    - **Produkt, kategori, kunde, ansatt, katalog**: brukes for Dynamics 365 Commerce omni-kanalbilde eller -bilder.
- **Publiser aktiva etter opplasting**: Når det er merket av i denne avmerkingsboksen, publiseres bildet eller bildene umiddelbart etter opplastingen.

> [!NOTE]
> Bilderessurser med en kategori som er tilordnet, blir også automatisk merket med kategorien som et nøkkelord for å hjelpe å søke etter anleggsmidler for en bestemt kategori.

### <a name="naming-conventions-for-omni-channel-images"></a>Navnekonvensjoner for omni-kanals bilder 

Hvis du har konfigurert mediebiblioteket som omnikanal-bildeserver, kan du bruke bildekategorier til å angi hvilken kategori den opplastede bildet tilhører. Det finnes også en navngivningskonvensjon som bør følges for å sikre at bilder hentes riktig av andre kanaler, for eksempel salgssted.

Standard navnekonvensjon varierer avhengig av kategorien:
- Katalogbilder må ha navnet "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"
- Kategori bilder bør ha navnet "**/Categories/\{CategoryName\}.png**"
- Kundebilder bør gis navnet "**/Customers/\{CustomerNumber\}.jpg**"
- Bilde for ansatte bør ha navnet "**/Workers/\{WorkerNumber\}.jpg**"
- Produktbilder bør ha navnet "**/Products/\{ProductNumber\}_000_001.png**"
    - 001 er bildesekvensen, og det kan være 001, 002, 003, 004 eller 005
- Produktvariantbilder bør ha navnet "**/Products/\{ProductNumber\}\_\{Size\}\_\{Color\}\_\{Style\}\_000_001.png**"

## <a name="upload-an-image"></a>Laste opp et bilde

Hvis du vil laste opp et bilde i områdebygger, følger du disse trinnene.

1. Velg **Mediebibliotek** i navigasjonsruten til venstre.
1. Velg **Last opp \> Last opp medieelementer** på kommandolinjen.
1. I Filutforsker-vinduet går du til og velger én eller flere bildefiler du vil laste opp, og velger deretter **Åpne**.
1. I dialogboksen **Last opp medieelement** angir du nødvendig tittel og alt-tekst.
1. Angi en valgfri beskrivelse og nøkkelord, og velg en kategori hvis ønskelig. 
1. Hvis du vil publisere bilder like etter opplastingen, merker du av for **Publiser medieelementer etter opplasting**.
1. Velg **OK**.

## <a name="upload-a-folder-of-images"></a>Laste opp en mappe med bilder

Hvis du vil masseopplaste en mappe med bilde i områdebygger, følger du disse trinnene.

1. Velg **Mediebibliotek** i navigasjonsruten til venstre.
1. Velg **Last opp \> Last opp mappe** på kommandolinjen.
1. I Filutforsker-vinduet går du til og velger en mappe du vil laste opp, og velger deretter **Åpne**.
1. I dialogboksen **Last opp medieelementer** angir du valgfrie nøkkelord og velger en kategori hvis du ønsker det. 
1. Hvis du vil publisere bildene i mappen like etter opplastingen, merker du av for **Publiser medieelementer etter opplasting**.
1. Velg **OK**.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over digital anleggsmiddelbehandling](dam-overview.md)

[Laste opp video](dam-upload-video.md)

[Laste opp filer](dam-upload-files.md)

[Beskjære bilder](dam-crop-images.md)

[Tilpasse bildefokuspunkter](dam-custom-focal-point.md)

[Last opp og betjen statiske filer](upload-serve-static-files.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]