---
title: Aktiv bildemodul
description: Dette emnet dekker aktive bildemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 07/08/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 36b7d6dea87c7f309c07608794d443a0ae19be211847d2cddcad95f2d933a8db
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6716914"
---
# <a name="active-image-module"></a>Aktiv bildemodul

[!include [banner](includes/banner.md)]

Dette emnet dekker aktive bildemoduler og beskriver hvordan du legger dem til områdesider i Microsoft Dynamics 365 Commerce.

En aktiv bildemodul kan brukes til å bygge inn produktkoder i et bilde. Brukere av e-handelsområder kan deretter holde markøren over kodene for å forhåndsvise produkter som vises i bildet. Forhåndsvisningene vises i popup-vinduer. Ved å velge et popup-vindu for forhåndsvisning kan brukerne gå direkte til produktdetaljersiden (PDP) for det tilsvarende produktet.

Kodene defineres ved hjelp av X- og Y-koordinatene i bildet. Hvert kodet punkt bør konfigureres med produkt-IDen for produktet som vises i bildet.

Illustrasjonen nedenfor viser et eksempel på et popup-vindu for forhåndsvisning av et bilde av en helt på hjemmesiden for Adventure Works.

![Eksempel på et popup-vindu for forhåndsvisning i en aktiv bildemodul](./media/Active_image.PNG)

> [!IMPORTANT]
> - Den aktive bildemodulen er tilgjengelig fra Dynamics 365 Commerce-10.0.20-versjonen.
> - Den aktive bildemodulen presenteres i Adventure Works-emnet.

## <a name="active-image-module-properties"></a>Egenskaper for Aktiv bildemodul

| Egenskapsnavn      | Verdier | beskrivelse |
|--------------------|--------|-------------|
| Bilde              | Bildefil | Et bilde kan brukes til å vise ett eller flere produkter. Bildet kan lastes opp til mediebiblioteket i Commerce-områdebyggeren, eller du kan bruke et eksisterende bilde. |
| Bredde              | Antall piksler | Denne egenskapen definerer bredden på bildet. De aktive koordinatene beregnes på grunnlag av bildebredden.|
| Aktive koordinater | X- og Y-koordinater og et produkt-ID-nummer | Hver aktive bildetabell består av X- og Y-koordinater, og et produkt-ID-nummer.|
| Overskrift            | Overskriftstekst og overskriftskode (**H1**, **H2**, **H3**, **H4**, **H5** eller **H6**) | Som standard brukes **H2**-overskriftskoden, men koden kan endres for å imøtekomme tilgjengelighetskrav. |
| Avsnitt          | Avsnittstekst | Modulen støtter avsnittstekst i rikt tekstformat. Noen grunnleggende funksjoner for rik tekst støttes, for eksempel hyperkoblinger og fet, understreket og kursivert tekst. Noen av disse funksjonene kan overstyres av sidetemaet som brukes på modulen. |
| Sammenkobling               | Koblingstekst, URL for kobling, ARIA (Accessible Rich Internet Applications) og **Åpne kobling i ny kategori**-velger | Modulen støtter én eller flere "handlingsoppfordring"-koblinger. Hvis en kobling er lagt til, er det nødvendig med en koblingstekst, en URL-adresse og en ARIA-etikett. ARIA-etiketter bør være beskrivende for å oppfylle tilgjengelighetskravene. Koblinger kan konfigureres slik at de åpnes i en ny fane. |
| Undertekst           | Overskrift, tekst og koblinger | Du kan legge til mer kontekst for bildet, for eksempel en forfatter eller et designernavn, eller koblinger til personlige blogger.|
| Teksttema         | **Lys** eller **Mørk** | Ved hjelp av denne egenskapen kan en bruker angi teksten til lys eller mørk, basert på bakgrunnsbildet. Den er tilgjengelig som emneutvidelse i Adventure Works-emnet. |

## <a name="add-an-active-image-module-to-a-new-page"></a>Legge til en aktiv bildemodul på en ny side

Hvis du vil legge til en aktiv bildemodul på en ny side og angi de nødvendige egenskapene, følger du disse trinnene.

1. Gå til **Maler**, og åpne markedsføringsmalen for områdets hjemmeside (eller opprett en ny markedsføringsmal).
1. I **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Aktiv bilde**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og åpne områdets hjemmeside (eller opprett en ny hjemmeside ved hjelp av markedsføringsmalen).
1. På **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg til modul** velger du **Aktiv bilde**-modulen, og deretter velger du **OK**.
1. Legg til et bilde i egenskapsruten for den aktive bildemodulen, og angi lerretsstørrelsen etter størrelsen på bildet.
1. Angi X- og Y-koordinatene, og legg til det riktige produkt-ID-nummeret.
1. Legg til og konfigurer flere aktive bildemoduler etter behov.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden.
1. Velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Adventure Works-tema](adventure-works-theme.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
