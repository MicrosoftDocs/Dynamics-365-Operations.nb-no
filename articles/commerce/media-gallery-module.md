---
title: Mediegallerimodul
description: Dette emnet dekker mediegallerimoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
ms.date: 05/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.13
ms.openlocfilehash: 0d05129145c5d6c3967b243cb0855a1c4fd3e84e
ms.sourcegitcommit: ccb39767bd3430c24f4653c26560bba2cd66553c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/19/2022
ms.locfileid: "8780874"
---
# <a name="media-gallery-module"></a>Mediegallerimodul

[!include [banner](includes/banner.md)]

Dette emnet dekker mediegallerimoduler og beskriver hvordan du legger dem til på områdesider i Microsoft Dynamics 365 Commerce.

Mediegallerimoduler viser ett eller flere bilder i en gallerivisning. Mediegallerimoduler støtter miniatyrbilder, som kan ordnes enten vannrett (som en rad under bildet) eller loddrett (som en kolonne ved siden av bildet). Mediegallerimoduler inneholder også funksjoner som gjør at bilder kan zoomes (forstørres) eller vises i fullskjermmodus. For å bli gjengitt i en mediegallerimodul må et bilde være tilgjengelig i mediebiblioteket i Commerce-områdebygger. Mediegallerimoduler støtter for øyeblikket bare bilder.

I standardmodus bruker en mediegallerimodul produkt-ID-en som er tilgjengelig fra sidekonteksten til en produktdetaljside (PDP) for å gjengi de tilsvarende produktbildene. I Commerce Headquarters må det defineres en mediefilbane for alle produkter. Bilder bør deretter lastes opp til mediebiblioteket i områdebyggeren i henhold til filbanen som ble definert for produktene i Commerce Headquarters. Disse bildene inneholder bilder for produkter og alle produktvarianter. Hvis du vil ha mer informasjon om hvordan du laster opp bilder til mediebiblioteket i områdebyggeren, kan du se [Laste opp bilder](dam-upload-images.md).

En mediegallerimodul kan eventuelt være vert for et fullstendig kuratert sett med bilder på en side i et bildegalleri, der det ikke er noen avhengigheter på produkt-ID-en eller sidekonteksten. I dette tilfellet må bilder lastes opp til mediebiblioteket i områdebygger og angis i områdebygger.

Her er noen brukseksempler for mediegallerimoduler:

- Gjengi produktbilder på en PDP
- Gjengi produktbilder på en produktmarkedsføringsside
- Presentere et kuratert sett med bilder på en markedsføringsside, for eksempel en galleriside

I eksemplet i følgende illustrasjon er en kjøpeboks på en PDP som er vert for produkt bilder, ved hjelp av en mediegallerimodul.

![Eksempel på en kjøpeboks på en produktdetaljside som er vert for produktavbildninger ved hjelp av en mediegallerimodul.](./media/ecommerce-pdp-buybox.PNG)

## <a name="media-gallery-properties"></a>Egenskaper for mediegalleri

| Egenskapsnavn | Verdier | beskrivelse |
|---------------|--------|-------------|
| Bildekilde | **Sidekontekst** eller **Produkt-ID** | Standardverdien er **Sidekontekst**. Hvis **Sidekontekst** er valgt, forventer modulen at siden oppgir produkt-ID-informasjon. Hvis **Produkt-ID** er valgt, må produkt-ID-en for et bilde angis som verdien for egenskapen **Produkt-ID**. Denne funksjonen er tilgjengelig i Commerce versjon 10.0.12. |
| Produkt-ID | En produkt-ID | Denne egenskapen gjelder bare hvis verdien for egenskapen **Bildekilde**-egenskapen er **Produkt-ID**. |
| Bildezoom | **Innebygd** eller **Container** | Denne egenskapen lar brukeren zoome bilder i mediagallerimodulen. Et bilde kan zoomes enten innebygd eller i en separat container ved siden av bildet. Denne funksjonen er tilgjengelig i 10.0.12. |
| Zoomfaktor | Et desimaltall | Denne egenskapen angir skaleringsfaktoren for zooming av bilder. Hvis for eksempel verdien er satt til **2,5**, forstørres bildene 2,5 ganger. |
| Fullskjerm | **Sann** eller **Usann** | Denne egenskapen angir om bilder kan vises i fullskjermmodus. I fullskjermmodus kan bilder også bli ytterligere forstørret hvis zoomefunksjonen er slått på. Denne funksjonen er tilgjengelig i Commerce versjon 10.0.13-versjonen. |
| Kvalitet for zoomet bilde | Et tall fra 1 til og med 100 som representerer en prosent, og som velges ved hjelp av en trackbar-kontroll | Denne egenskapen definerer bildekvaliteten for bilder som zoomes inn. Du kan angi en oppløsning på 100 prosent for å sikre at et zoomet bilde alltid bruker høyest mulig oppløsning. Denne egenskapen gjelder ikke PNG-filer fordi de bruker format uten datatap. Denne funksjonen er tilgjengelig fra og med Commerce versjon 10.0.19-versjonen. |
| Bilder | Bilder som er valgt fra mediebiblioteket i områdebygger | I tillegg til å bli gjengitt fra et produkt kan bilder kurateres for en mediegallerimodul. Disse bildene blir føyd til alle tilgjengelige produktavbildninger. Denne funksjonen er tilgjengelig i Commerce versjon 10.0.12. |
| Miniatyrbilderetning | **Loddrett** eller **Vannrett** | Denne egenskapen angir om miniatyrbilder skal vises i en loddrett stripe eller en vannrett stripe. |
| Skjul hovedproduktbilder for variant | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann** når en variant er valgt, skjules bilder av hovedproduktet hvis varianten ikke har noen bilder. Denne egenskapen påvirker ikke produkter som ikke har noen varianter. |
| Oppdater medier ved dimensjonsvalg | **Sann** eller **Usann** | Hvis denne egenskapen er satt til **Sann**, oppdateres bilder i mediebiblioteket når en dimensjon (for eksempel farge, stil eller størrelse) er valgt, og hvis et bilde er tilgjengelig. Denne egenskapen bidrar til å forenkle nettleseropplevelsen, fordi ikke alle produktvariantdimensjoner må velges for det tilsvarende bildet som skal oppdateres. Denne egenskapen er tilgjengelig i fanen **Avansert**. |

> [!IMPORTANT]
> Egenskapen **Oppdater medier ved dimensjonsvalg** er tilgjengelig fra og med Commerce, versjon 10.0.21. Den krever at Commerce-modulbibliotekpakken versjon 9.31 er installert.

Illustrasjonen nedenfor viser et eksempel på en mediegallerimodul der alternativene for fullskjerm og zoom er tilgjengelige.

![Eksempel på en mediegallerimodul der alternativene for fullskjerm og zoom er tilgjengelige.](./media/ecommerce-media-zoom.png)

Illustrasjonen nedenfor viser et eksempel på en mediegallerimodul med kuraterte bilder (det vil si at de angitte bildene ikke er avhengige av produkt-ID-en eller sidekonteksten).

![Eksempel på en mediegallerymodul med kuraterte bilder.](./media/ecommerce-media-curated.PNG)

## <a name="commerce-scale-unit-interaction"></a>Samhandling med Commerce Scale Unit

Når bildekilden er avledet fra sidekonteksten, brukes produkt-ID-en fra PDP til å hente bildene. Mediegallerimodulen henter bildefilbanen for produkter ved hjelp av API-er for Commerce Scale Unit. Bildene hentes deretter fra mediebiblioteket slik at de kan gjengis i modulen.

## <a name="add-a-media-gallery-module-to-a-page"></a>Legge til en mediegallerimodul på en side

Følg disse trinnene for å legge til en mediegallerimodul på en markedsføringsside.

1. Gå til **Maler**, og velg **Ny** for å opprette en ny mal.
1. I dialogboksen **Ny mal**, under **Malnavn**, angir du **Markedsføringsmal**, og velger deretter **OK**.
1. I **Tekst**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Legg moduler** velger du **Standardside**-modulen, og deretter velger du **OK**.
1. I **Hoved**-sporet på standardsiden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. Velg **Lagre**, velg **Fullfør redigering** for å sjekke inn malen, og velg deretter **Publiser** for å publisere den.
1. Gå til **Sider**, og velg **Ny** for å opprette en ny side.
1. I dialogboksen **Opprett ny side**, under **Sidenavn**, angir du en **Mediegalleriside**, og velger deretter **Neste**.
1. Velg **Markedsføringsmal**-malen du opprettet, under **Velg en mal**, og velg deretter **Neste**.
1. Under **Velg et oppsett** velger du et sideoppsett (for eksempel **Fleksibelt oppsett**), og deretter velger du **Neste**.
1. Gå gjennom sidekonfigurasjonen under **Gjennomgang og fullfør**. Hvis du har behov for å redigere sideinformasjonen, velger du **Tilbake**. Hvis sideinformasjonen er riktig, velger du **Opprett side**. 
1. På **Hoved**-sporet på den nye siden velger du ellipseknappen (**...**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Beholder**-modulen, og deretter velger du **OK**.
1. I **Beholder**-sporet velger du ellipsen (**…**), og deretter velger du **Legg til modul**.
1. I dialogboksen **Velg moduler** velger du **Mediegalleri**-modulen, og deretter velger du **OK**.
1. I egenskapsruten for mediegallerimodulen, under **Bildekilde**, velger du **Productid**. I feltet **Product id** angir du deretter en produkt-ID.
1. Velg **Lagre**, og velg deretter **Forhåndsvisning** for å forhåndsvise siden. Du skal kunne se bildene for produktet i en gallerivisning.
1. Hvis du bare vil bruke kuraterte bilder, går du til egenskapsruten under **Bildekilde** og velger **Productid**. Under **Bilder** velger du deretter **Legg til et bilde** så mange ganger som nødvendig for å legge til bilder fra mediebiblioteket.
1. Angi eventuelle tilleggsegenskaper du vil angi, for eksempel **Bildezoom**, **Zoomfaktor** og **Miniatyrbilderetning**.
1. Når du er ferdig, velger du **Lagre**, velg **Fullfør redigering** for å sjekke inn siden, og velg deretter **Publiser** for å publisere den.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over modulbibliotek](starter-kit-overview.md)

[Kjøpsboksmodul](add-buy-box.md)

[Beholdermodul](add-container-module.md)

[Laste opp bilder](dam-upload-images.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
