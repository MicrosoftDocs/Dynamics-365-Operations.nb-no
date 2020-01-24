---
title: Arbeide med moduler
description: Dette emnet beskriver hvordan og når du bruker moduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/12/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: ''
ms.author: phinneyridge
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3c4161e7a40cdbbb40292a6ce9acab58347460bd
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914800"
---
# <a name="work-with-modules"></a>Arbeide med moduler

Dette emnet beskriver hvordan og når du bruker moduler i Microsoft Dynamics 365 Commerce.

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

## <a name="overview"></a>Oversikt

Moduler er logiske byggeblokker som utgjør sidestrukturen, og de har forskjellige formål og omfang. Noen moduler er containere på høyt nivå, og det eneste formålet er å oppbevare og organisere andre moduler (underordnede moduler). Andre moduler, for eksempel en enkel bildeplasseringsmodul, har et svært bestemt formål. Andre moduler, for eksempel en karusellmodul, faller et sted mellom disse to kategoriene.

Som standard inneholder Dynamics 365 Commerce-området et startpakkemodulbibliotek som lar deg utføre de mest grunnleggende e-handelsscenarioene. Du skal kunne konstruere et ende-til-ende-område for e-handel bare ved å bruke disse modulene. Det kan imidlertid hende at du også vil tilpasse disse modulene eller bygge nye, tilpassede moduler for bestemte behov. Hvis du vil bygge egendefinerte moduler, er en modul-SDK (Software Development Kit) tilgjengelig slik at du kan opprette et egendefinert modulbibliotek.

## <a name="container-modules-and-slots"></a>Containermoduler og -spor

Som nevnt tidligere er noen moduler utformet for å inneholde underordnede moduler. Disse modulene kalles *containere* og tillater hierarkier av nestede moduler. Containermoduler inneholder *spor*. Spor brukes til å håndtere oppsettet og formålet med underordnede moduler i containeren. Et eksempel er en grunnleggende sidecontainermodul (en modul på øverste nivå for alle sider) som definerer flere viktige spor:

- Et overskriftsspor
- Et brødtekstspor
- Et bunntekstspor

Utvikleren av modulen definerer disse sporene og bestemmer hvilke underordnede moduler og hvor mange underordnede moduler som kan plasseres direkte i den. Overskriftssporet kan for eksempel støtte bare én modul av typen **Topptekst**, mens brødtekstsporet kan støtte et ubegrenset antall moduler av alle typer (bortsett fra andre sidecontainermoduler).

I redigeringsverktøyene trenger ikke sideforfattere å vite på forhånd hvilke moduler som kan og ikke kan legges i hvert spor. Når sideforfattere velger et spor, og deretter prøver å velge en modul som skal legges til, vil de se en filtrert visning av modultyper som støttes for dette sporet.

## <a name="content-modules"></a>Innholdsmoduler

Innholdsmoduler inneholder innholds- og medieelementer, for eksempel tekst (f.eks. overskrifter, avsnitt og koblinger) eller aktivareferanser (for eksempel bilder, videoer og PDF-filer). Eksempler på typiske innholdsmodultyper er **Hovedbanner**, **Funksjon** og **Banner**. Moduler av disse tre typene kan inneholde tekst eller medier, og de krever ingen underordnede moduler for å gjøre noe synlig på en side.

De fleste av de typiske, daglige side- og innholdsredigeringsaktivitetene omfatter innholdsmoduler, først og fremst siden disse modulene definerer det faktiske innholdet som gjengis i de overordnede containermodulene. Mange innholdsmoduler er tilgjengelige, og disse modulene er vanligvis de siste brikkene du legger til i sidehierarkiet for nestede moduler.

Illustrasjonen nedenfor viser hvordan moduler er nestet i overordnede containermodulspor.

![Neste moduler](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Legge til eller fjerne moduler

Følgende prosedyrer beskriver hvordan du legger til og fjerner moduler.

### <a name="add-a-module"></a>Legge til en modul

Følg disse trinnene for å legge til en modul i et spor eller en container på en side.

1. I disposisjonsruten til venstre velger du en container eller et spor som en underordnet modul kan legges til i.

    > [!NOTE]
    > Modulutforming definerer listen over modultyper som kan legges til i et bestemt modulspor. Malredigerere kan deretter forbedre de tillatte modulalternativene for å sikre konsekvent søkemotoroptimalisering (SEO) og administrasjonseffektivitet for alle sidene som er bygget fra en bestemt mal.

1. Velg ellipseknappen (**...**) for modulen, og velg deretter **Legg til modul**. Dialogboksen **Legg til modul** vises. Denne dialogboksen blir automatisk filtrert, slik at den bare viser moduler som støttes i valgt container eller spor. Listen over moduler bestemmes av sidens mal eller containermoduldefinisjonen.

    > [!NOTE]
    > Hvis en container eller et spor ikke støtter nye underordnede moduler, er alternativet **Legg til modul** ikke tilgjengelig.

1. Søk etter og velg en modul du vil legge til på siden, i dialogboksen.

    > [!TIP]
    > **Funksjon** og **Hovedbanner** er gode modultyper som nybegynnere kan jobbe med.

1. Velg **OK** for å legge den valgte modulen til valgt container eller spor på siden.

### <a name="remove-a-module"></a>Fjerne en modul

Følg disse trinnene for å fjerne en modul fra sporet eller containeren på en side.

1. I disposisjonsruten til venstre velger du ellipseknappen ved siden av navnet på modulen som skal fjernes, og deretter velger du papirkurvknappen.
1. Når du blir bedt om å bekrefte at du vil fjerne modulen, velger du **OK**.

## <a name="configure-modules"></a>Konfigurere moduler

Følgende prosedyrer beskriver hvordan du konfigurerer innhold og innholdsmoduler.

### <a name="configure-a-content-module"></a>Konfigurere en innholdsmodul

Hvis du vil konfigurere en innholdsmodul på en side, følger du disse trinnene.

1. I disposisjonsruten til venstre velger du en innholdsmodultype (for eksempel **Funksjon**, **Hovedbanner** eller **Banner**).
1. I egenskapsruten til høyre utvider du de nestede kontrollene ved å velge overskriftene og angi eventuelle nødvendige kontrollverdier.
1. Hvis egenskapsruten har en **Datakonfigurasjon**-del, merker du den for å utvide den. Hvis ikke går du til trinn 5.
1. Hvis det finnes en **Legg til datakilde**-knapp, velger du den, og deretter velger du innholdselementene for å legge til.
1. Angi innstillinger for eventuelle nødvendige eller ønskede modulkontroller.
1. Velg **Lagre**.

### <a name="configure-a-container-module"></a>Konfigurere en containermodul

Hvis du vil konfigurere en containermodul på en side, følger du disse trinnene.

1. Velg en containermodul på siden (for eksempel en karusell eller en modul for flytende container).
1. I egenskapsruten til høyre utvider du de nestede kontrollene ved å velge overskriftene og angi eventuelle nødvendige kontrollverdier.
1. I disposisjonsruten til venstre velger du ellipseknappen ved siden av navnet på enten containeren eller eventuelle spor i containeren, og deretter velger du **Legg til modul**. Deretter legger du til underordnede moduler i den valgte containeren. Hvis du ha mer informasjon, kan du se prosedyren [Legge til en modul](#add-a-module) tidligere i dette emnet.
1. Hvis det finnes flere underordnede moduler som sideordnede i en overordnet container, kan du endre visningsrekkefølgen i den overordnede containeren. Velg ellipseknappen for en modul, og bruk deretter tastene for pil opp og pil ned.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over maler og oppsett](templates-layouts-overview.md)

[Arbeide med maler](work-with-templates.md)

[Arbeide med forhåndsinnstilte oppsett](work-with-layouts.md)

[Arbeide med fragmenter](work-with-fragments.md)

[Legge til en containermodul på en side](add-container-module.md)

[Legge til moduler for innholdsplassering på en side](add-content-placement-modules.md)

[Arbeide med publiseringsgrupper](publish-groups.md)

