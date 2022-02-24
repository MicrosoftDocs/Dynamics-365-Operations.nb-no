---
title: Tilgjengelighetsfunksjoner og egenskaper
description: Dette emnet gir informasjon om tilgjengelighetsfunksjonene og egenskapene i Microsoft Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 04/14/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6f6bca3589da4055eef000fc3b2c88b93eabb4d5
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414565"
---
# <a name="accessibility-features-and-capabilities"></a>Tilgjengelighetsfunksjoner og egenskaper


[!include [banner](includes/banner.md)]

Dette emnet gir informasjon om tilgjengelighetsfunksjonene og egenskapene i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Tilgjengelighetsfunksjoner og -egenskaper gir alle brukere de funksjonelle midlene til å få tilgang til og utføre handlinger slik at de kan oppnå målene sine. Dette brede utvalget av brukere kan kreve hjelpeverktøy for brukere med ulike nedsatte funksjoner.

Ulike funksjoner i Dynamics 365 Commerce lar deg bygge nettstedet ditt slik at det inneholder hjelpefunksjoner. Når du utformer området, bør du vurdere områdene med tilgjengelighetsfunksjonalitet som er nevnt i [Microsoft Accessibility Center](https://www.microsoft.com/accessibility). 

Dette emnet beskriver noen flere områder med tilgjengelighetsfunksjonalitet som du bør vurdere når du bruker Dynamics 365 Commerce.

## <a name="image-alt-text"></a>Bildealternativ tekst

Dynamics 365 Commerce har et innebygd digitalt system for anleggsmiddelbehandling for å spore bilde- og videoressurser som brukes på nettstedet ditt. Bildetekster, beskrivelser og alt-tekst kan legges til i egenskapsruten for et bilde når det er valgt eller lastet opp.

## <a name="video-accessibility"></a>Videotilgjengelighet

Det Dynamics 365 Commerce digitale systemet for anleggsmiddelbehandling støtter flere tilgjengelighetsfunksjoner for videoinnhold. Noen eksempler er oppført i tabellen nedenfor.

| Videofunksjon               | Beskrivelse |
|-----------------------------|-------------|
| Teksting for hørselshemmede      | Tekst som kan vises for lyd og lydbeskrivende elementer i en video, for å hjelpe brukere som er døve eller hørselshemmede |
| Undertekster                   | Undertekstfiler som viser teksten i kontekstledetråder eller dialog på skjermen |
| Lydtranskripsjoner           | En tekstutskrift av talte ord som er generert fra lyden av en videoressurs |
| Beskrivende lyd           | En ikke-primær lydkanal som beskriver innholdet eller konteksten som skjer på skjermen |
| Minimumsalder            | Et attributt som kan lagre minstealderen som en seer må ha for å vise en video (bare metadata) |

### <a name="configure-video-accessibility-elements"></a>Konfigurere tilgjengelighetselementer for video

I **Mediebibliotek**-delen for for Commerce for nettstedet ditt, kan du laste opp videoressurser som har separate filer for teksting for hørselshemmede, vanlig lyd og beskrivende lyd. Teksting for hørselshemmede kan også genereres automatisk når en videoressurs lastes opp.

#### <a name="generate-or-upload-closed-caption-files-during-video-asset-upload"></a>Generer eller last opp undertekstfiler under opplasting av videoressurser

Hvis du vil at en undertekstfil automatisk skal genereres når du laster opp en video, følger du denne fremgangsmåten.

- I dialogboksen **Opplasting av aktivum** velger du **Generer undertekster automatisk**. Hvis du genererer en undertekstfil, vil ikke filvelgeren for undertekstfiler være tilgjengelig i dialogboksen.

Hvis du vil laste opp en undertekstfil manuelt når du laster opp en video, følger du denne fremgangsmåten.

- I dialogboksen **Opplasting av aktivum** fjerner du merket for **Generer undertekster automatisk**.

Hvis du vil laste opp vanlig lyd eller beskrivende lydfiler for videoen, bruker du filvelgeren i dialogboksen **Opplasting av aktivum**.

> [!NOTE]
> Teksting for hørselshemmede, vanlig lyd og beskrivende lydinnhold kan også legges til etter at en videoressurs er lastet opp. Gå til **Mediebibliotek**, velg videoressursen, og velg **Rediger** for å sjekke den ut. Last deretter opp tilleggsressursene i egenskapsruten for videoressursen.

#### <a name="edit-cc-and-audio-transcript-files"></a>Redigere undertekst- og lydtranskripsjonsfiler

Undertekst- og lydtranskripsjonfiler kan redigeres direkte i redigeringsverktøyet. Videoavspilling er tilgjengelig under redigering.

Følg denne fremgangsmåten for å redigere undertekst- og lydtranskripsjonsfiler.

1. Gå til **Mediebibliotek**, og velg filnavnet for videoressursen. Redigeringsprogrammet for undetekst og transkripsjon vises.
1. Velg **Rediger**.
1. Rediger underteksten eller transkripsjonsteksten.
1. Når du er ferdig, velger du **Lagre** og deretter **Fullfør redigering**.
1. Når du er klar til å publisere, velger du **Publiser**.

#### <a name="set-the-minimum-age-attribute"></a>Angi Minimumsalder-attributtet

Et **Minimumsalder**-metadataattributt kan knyttes til videoressurser.

Hvis du vil angi **Minimumsalder**-attributtet for en videoressurs, følger du denne fremgangsmåten.

1. Gå til **Mediebibliotek**, og velg videoressursen.
1. Velg **Rediger**.
1. Angi **Minimumsalder**-attributtet i egenskapsruten for videoressursen.

> [!NOTE]
> Egenskapsruten brukes bare til å angi og lagre verdien for metadata-attributtet. Tilpassede moduler må opprettes for å bruke dette attributtet for avspillingsporting.

## <a name="additional-resources"></a>Tilleggsressurser

[Tilgjengelighet i skjemaer, produkter og kontroller](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/user-interface/enable-accessibility)

[Microsoft Accessibility Center](https://www.microsoft.com/accessibility)

[Dynamics 365 Accessibility Center](https://docs.microsoft.com/dynamics365/get-started/accessibility/index)

[Samsvarsoversikt](compliance-overview.md)

[Informasjonskapselsamsvar](cookie-compliance.md)

[Legge til en side for personvernpolicy](add-privacy-page.md)

[Erstatte bruker-IDer knyttet til sporede innholdsendringer](replace-IDs-tracked-changes.md)
