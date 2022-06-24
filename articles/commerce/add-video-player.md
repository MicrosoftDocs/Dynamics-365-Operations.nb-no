---
title: Videospillermodul
description: Denne artikkelen dekker videospillermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
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
ms.openlocfilehash: 20d516c58bf619065d57b27bc5a614eb7bd4cea9
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8873442"
---
# <a name="video-player-module"></a>Videospillermodul

[!include [banner](includes/banner.md)]

Denne artikkelen dekker videospillermoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

Videospillermodulen brukes til å støtte videoavspilling. Den kan legges til på en hvilken som helst side, forutsatt at videoinnhold lastes opp til og er tilgjengelig i innholdsbehandlingssystemet (CMS). Videospillermodulen støtter MP4-medietypen.

## <a name="video-player-module"></a>Videospillermodul

Videospillermodulen kan brukes til å vise videoer på et e-handelsområde. Den støtter alle avspillingsfunksjoner, for eksempel spill av, pause, fullstørrelsesmodus, lydbeskrivelser og teksting for hørselshemmede. Videospillermodulen støtter også tilpassing av teksting for hørselshemmede for å oppfylle Microsofts tilgjengelighetsstandarder. Du kan for eksempel tilpasse skriftstørrelsen og bakgrunnsfargen.

Videospiller-modulen støtter også sekundære lydspor. Når en video er lastet opp til CMS, kan du også laste opp et sekundært lydspor. Videospiller-modulen kan deretter spille av det sekundære lydsporet hvis en bruker velger det.

### <a name="examples-of-video-player-modules-in-e-commerce"></a>Eksempler på omgivelsesvideospillermoduler i e-handel

- Instruksjonsvideoer på produktdetaljsider eller markedsføringssider
- Kampanjevideoer eller videoer om policyer på en hvilken som helst markedsføringsside
- Markedsføringsvideoer som fremhever produktfunksjoner på sider med produktdetaljer eller markedsføringssider

Bildet nedenfor viser et eksempel på en videospillermodul på en hjemmeside.

![Eksempel på en videospillermodul.](./media/ecommerce-videoplayer.PNG)

### <a name="video-player-module-properties"></a>Egenskaper for videospillermodul

| Egenskapsnavn         | Verdi                               | beskrivelse |
|-----------------------|-------------------------------------|-------------|
| Overskrift               | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Som standard brukes **H2**-overskriftskoden, men koden kan endres for å imøtekomme tilgjengelighetskrav. |
| Rik tekst             | Avsnittstekst | Modulen støtter avsnittstekst i rikt tekstformat. Noen grunnleggende funksjoner for rik tekst støttes, for eksempel hyperkoblinger og fet, understreket og kursivert tekst. Noen av disse funksjonene kan overstyres av sidetemaet som brukes på modulen. |
| Sammenkobling                  | Koblingstekst, URL for kobling, ARIA (Accessible Rich Internet Applications) og **Åpne kobling i ny kategori**-velger | Modulen støtter én eller flere "handlingsoppfordring"-koblinger. Hvis en kobling er lagt til, er det nødvendig med en koblingstekst, en URL-adresse og en ARIA-etikett. ARIA-etiketter bør være beskrivende for å oppfylle tilgjengelighetskravene. Koblinger kan konfigureres slik at de åpnes i en ny fane. |
| Undertekst              | Overskrift, tekst eller koblinger | Du kan legge til mer kontekst for videospillermodulen, for eksempel en forfatter eller et designernavn, eller koblinger til personlige blogger. |
| Automatisk avspilling             | **Sann** eller **Usann**               | Når verdien settes til **Sann**, spilles videoen automatisk. |
| Demp                  | **Sann** eller **Usann**               | Når verdien settes til **Sann**, dempes lyden. For denne spilleren er standardverdien **Usann**. I Chrome-leseren dempes autokjørvideoer som standard, og lyden spilles av bare hvis brukeren spiller av videoen manuelt. |
| Løkke                  | **Sann** eller **Usann**               | Når verdien settes til **Sann**, gjentas videoen i en løkke. |
| Medier                 | Filbane og -navn for video. | Videofilen som spilles av i videospilleren. |
| Spille av fullskjerm       | **Sann** eller **Usann**               | Når verdien settes til **Sann**, spilles videoen automatisk i fullskjermmodus. |
| Utløser for avspilling/pause    | **Sann** eller **Usann**               | Når verdien er satt til **Sann**, vises en spill av / pause-knapp på videoen. |
| Kontroller for videospiller | **Sann** eller **Usann**               | Når verdien settes til **Sann**, vises alle videospillerkontroller. Disse kontrollene inkluderer knapper for spill av og pause, en fremdriftsindikator og alternativer for teksting for hørselshemmede. |
| Skjul plakatbilde     | **Sann** eller **Usann**               | En video kan ha en plakatramme. Når verdien for denne egenskapen er satt til **Sann**, er plakatrammen skjult. |
| Maskenivå            | Et tall fra **0** til **100** | Masken som brukes på videoen for styling. |

> [!IMPORTANT]
> Egenskapene **Overskrift**, **Rik tekst**, **Kobling** og **Undertekst** er tilgjengelig fra Dynamics 365 Commerce 10.0.20-versjonen.

## <a name="add-a-video-player-module-to-a-page"></a>Legge til en videospillermodul på en side

> [!NOTE] 
> Før du oppretter en videospillermodul, må du først laste opp en video til mediebiblioteket.

Hvis du vil legge til en videospillermodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du **Videospillermal**, og velger deretter **OK**.
1. I **Tekst**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg moduler** velger du **Standardside**-modulen, og deretter velger du **OK**.
1. På **Hoved**-sporet på **Standardside**-modulen velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Videospiller**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den. 
1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I dialogboksen **Opprett ny side**, under **Sidenavn**, angir du en **Videospillerside**, og velger deretter **Neste**.
1. Velg **Videospillermal**-malen du opprettet,under **Velg en mal**, og velg deretter **Neste**.
1. Under **Velg et oppsett** velger du et sideoppsett (for eksempel **Fleksibelt oppsett**), og deretter velger du **Neste**.
1. Gå gjennom sidekonfigurasjonen under **Gjennomgang og fullfør**. Hvis du har behov for å redigere sideinformasjonen, velger du **Tilbake**. Hvis sideinformasjonen er riktig, velger du **Opprett side**.
1. På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Videospiller**-modulen, og deretter velger du **OK**.
1. Velg **Legg til en video** i egenskapsruten for videospillermodulen.
1. Velg en video i dialogboksen **Medievelger**, og velg deretter **Last opp nytt medieelement** .
1. I Filutforsker velger du en videofil, og deretter velger du **Åpne**.
1. I **Last opp medieelement**-dialogboksen skriver du inn en tittel og annen informasjon etter behov, og velger deretter **OK**.
1. I **Medievelger**-dialogboksen velger du **Lukk**.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden. Du skal se videomodulen på siden. Du kan endre flere innstillinger for å tilpasse virkemåten til modulen.
1. Velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den. 

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Promobannermodul](add-alert.md)

[Karusellmodul](add-carousel.md)

[Tekstblokkmodul](add-content-rich-block.md)

[Innholdsblokkmodul](add-hero-module.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
