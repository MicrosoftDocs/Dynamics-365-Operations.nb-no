---
title: Last opp bilder
description: Denne artikkelen beskriver hvordan du laster opp bilder i områdebyggeren for Microsoft Dynamics 365 Commerce.
author: josaw1
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: josaw
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.custom: ''
ms.assetid: ''
ms.search.industry: ''
ms.openlocfilehash: d937e8c0e00ce28b0e4a4c2feab3ac1c8f075916
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9283386"
---
# <a name="upload-images"></a>Last opp bilder

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du laster opp bilder i områdebyggeren for Microsoft Dynamics 365 Commerce.

Med mediebiblioteket for Commerce-områdebygger kan du laste opp bilder, enten enkeltvis eller flere samtidig ved hjelp av mapper. Du bør alltid laste opp den versjonen av bildet med høyest oppløsning og kvalitet, fordi bildeskaleringskomponenten automatisk vil optimalisere bildet for forskjellige visningsporter og deres stoppunkter.

### <a name="image-information-specified-during-upload"></a>Bildeinformasjon som angis under opplasting

Når du laster opp et bilde, kan følgende informasjon angis.

- **Tittel, alt-tekst, beskrivelse, nøkkelord**: metadata for bildet eller bildene. Tittel og alt-tekst er obligatoriske verdier.
- **Velg kategori**:
    - **Ingen**: brukes for beskrivelse av bilde eller bilder i e-handel.
    - **Produkt, kategori, kunde, ansatt, katalog**: brukes for Dynamics 365 Commerce omni-kanalbilde eller -bilder.
- **Publiser aktiva etter opplasting**: Når det er merket av i denne avmerkingsboksen, publiseres bildet eller bildene umiddelbart etter opplastingen.

> [!NOTE]
> - Bilderessurser med en kategori som er tilordnet, blir også automatisk merket med kategorien som et nøkkelord for å hjelpe å søke etter anleggsmidler for en bestemt kategori.
> - Produktdetaljsider genererer **alt-tekst** dynamisk ved hjelp av produktnavnet, slik at endring av **alt-tekst** for et produktbilde ikke har noen innvirkning på det gjengitte bildet.

### <a name="naming-conventions-for-omni-channel-images"></a>Navnekonvensjoner for omni-kanals bilder 

Hvis du har konfigurert mediebiblioteket som omnikanal-bildeserver, kan du bruke bildekategorier til å angi hvilken kategori den opplastede bildet tilhører. Det finnes også en navngivningskonvensjon som bør følges for å sikre at bilder hentes riktig av andre kanaler, for eksempel salgssted.

Standard navnekonvensjon varierer avhengig av kategorien:
- Katalogbilder må ha navnet "**/Catalogs/\{LanguageId\}/\{CatalogName\}.jpg**"
- Kategori bilder bør ha navnet "**/Categories/\{CategoryName\}.png**"
- Kundebilder bør gis navnet "**/Customers/\{CustomerNumber\}.jpg**"
- Bilde for ansatte bør ha navnet "**/Workers/\{WorkerNumber\}.jpg**"
- Produktbilder bør ha navnet "**/Products/\{ProductNumber\}\_000_001.png**"
    - 001 er bildesekvensen, og det kan være 001, 002, 003, 004 eller 005
- Produktvariantbilder bør ha navnet "**/Produkter/\{Produktnummer\} \^ \{Stil\} \^ \{Størrelse\} \^ \{Farge\} \^\_000_001.png**"
    - For eksempel: 93039 \^ &nbsp;\^ 2 \^ Black \^\_000_001.png
- Produktvariantbilder med konfigurasjonsdimensjon bør ha navnet "**/Products/\{ProductNumber\} \^ \{Configuration\}\_000_001.png**"
    - For eksempel: 93039 \^ LB8017_000_001.png

> [!NOTE]
> For produktvariantbilder må det være to mellomrom mellom karetene i filnavnet hvis dimensjonsverdien er tom.

I eksemplene ovenfor brukes standardkonfigurasjonen. Skilletegnet og dimensjonene kan konfigureres, og den nøyaktige navngivningen som kreves, kan variere mellom distribusjonene. En metode som kan brukes til å identifisere den nøyaktige navngivningskonvensjonen som kreves, er å bruke utviklerkonsollen i webleseren til å kontrollere bildeforespørsler for produktvariantene mens du endrer produktdimensjonene på siden med produktdetaljer (PDP) for produktmodeller.

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
