---
title: Arbeide med moduler
description: Dette emnet beskriver hvordan og når du bruker moduler i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/31/2020
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
ms.openlocfilehash: da430857801d8007244c04aadd325e99c0b882c5
ms.sourcegitcommit: 078befcd7f3531073ab2c08b365bcf132d6477b0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/31/2020
ms.locfileid: "3646021"
---
# <a name="work-with-modules"></a>Arbeide med moduler

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

Dette emnet beskriver hvordan og når du bruker moduler i Microsoft Dynamics 365 Commerce.

## <a name="overview"></a>Oversikt

Moduler er logiske byggeblokker som utgjør sidestrukturen, og de har forskjellige formål og omfang. Noen moduler er containere på høyt nivå, og det eneste formålet er å oppbevare og organisere andre moduler (underordnede moduler). Andre moduler, for eksempel en enkel bildeplasseringsmodul, har et svært bestemt formål. Andre moduler, for eksempel en karusellmodul, faller et sted mellom disse to kategoriene.

Som standard inneholder Dynamics 365 Commerce-området et startpakkemodulbibliotek som lar deg utføre de mest grunnleggende e-handelsscenarioene. Du skal kunne konstruere et ende-til-ende-område for e-handel bare ved å bruke disse modulene. Det kan imidlertid hende at du også vil tilpasse disse modulene eller bygge nye, tilpassede moduler for bestemte behov. Hvis du vil bygge egendefinerte moduler, er en modul-SDK (Software Development Kit) tilgjengelig slik at du kan opprette et egendefinert modulbibliotek.

## <a name="container-modules-and-slots"></a>Containermoduler og -spor

Som nevnt tidligere er noen moduler utformet for å inneholde underordnede moduler. Disse modulene kalles *containere* og tillater hierarkier av nestede moduler. Containermoduler inneholder *spor*. Spor brukes til å håndtere oppsettet og formålet med underordnede moduler i containeren. Et eksempel er en grunnleggende sidecontainermodul (en modul på øverste nivå for alle sider) som definerer flere viktige spor:

- Et overskriftsspor
- Et underoverskriftsspor
- Et hovedspor
- Et bunntekstspor
- Et underbunntekstsspor

Utvikleren av modulen definerer disse sporene og bestemmer hvilke underordnede moduler og hvor mange underordnede moduler som kan plasseres direkte i den. Overskriftssporet kan for eksempel støtte bare én modul av typen **Topptekst**, mens brødtekstsporet kan støtte et ubegrenset antall moduler av alle typer (bortsett fra andre sidecontainermoduler).

I redigeringsverktøyene trenger ikke sideforfattere å vite på forhånd hvilke moduler som kan og ikke kan legges i hvert spor. Når sideforfattere velger et spor, og deretter prøver å velge en modul som skal legges til, vil de se en filtrert visning av modultyper som støttes for dette sporet.

## <a name="content-modules"></a>Innholdsmoduler

Innholdsmoduler inneholder innholds- og medieelementer, for eksempel tekst (f.eks. overskrifter, avsnitt og koblinger) eller aktivareferanser (for eksempel bilder, videoer og PDF-filer). Vanlige innholdsmodultyper inkluderer moduler for innholdsblokk, tekstblokk og promobanner. Moduler av disse tre typene kan inneholde tekst eller medier, og de krever ingen underordnede moduler for å gjøre noe synlig på en side.

De fleste av de typiske, daglige side- og innholdsredigeringsaktivitetene omfatter innholdsmoduler, først og fremst siden disse modulene definerer det faktiske innholdet som gjengis i de overordnede containermodulene. Mange innholdsmoduler er tilgjengelige, og disse modulene er vanligvis de siste brikkene du legger til i sidehierarkiet for nestede moduler.

Illustrasjonen nedenfor viser hvordan moduler er nestet i overordnede containermodulspor.

![Neste moduler](../commerce/media/basic-module-nesting.png)

## <a name="add-or-remove-modules"></a>Legge til eller fjerne moduler

Følgende prosedyrer beskriver hvordan du legger til og fjerner moduler.

### <a name="add-a-module"></a>Legge til en modul

Følg disse trinnene for å legge til en modul i et spor eller en container på en side.

1. I disposisjonsruten til venstre eller direkte på hovedlerretet velger du en container eller et spor der en underordnet modul kan legges til.

    > [!NOTE]
    > Modulutforming definerer listen over modultyper som kan legges til i et bestemt modulspor. Malredigerere kan deretter forbedre de tillatte modulalternativene for å sikre konsekvent søkemotoroptimalisering (SEO) og administrasjonseffektivitet for alle sidene som er bygget fra en bestemt mal. Når du legger til en modul for et spor, blir dialogboksen **Legg til modul** automatisk filtrert, slik at den bare viser moduler som støttes i valgt container eller spor. Denne listen over tillatte moduler bestemmes av sidens mal eller containermoduldefinisjonen.

1. Hvis du bruker disposisjonsruten, velger du ellipsen (**...**) ved siden av modulnavnet, og deretter velger du **Legg til modul**. Hvis du bruker kontrollene direkte i lerretet, velger du plusstegnet (**+**) i et tomt spor eller ved siden av den valgte modulen, og deretter velger du **Legg til modul**.

    > [!NOTE]
    > Hvis en container eller et spor ikke støtter nye underordnede moduler, er alternativet **Legg til modul** ikke tilgjengelig.

1. Velg en modul du vil legge til på siden, i dialogboksen **Legg til modul**.

    > [!TIP]
    > **Innholdsblokk** er en god modultype for nybegynnere til å arbeide med.

1. Velg **OK** for å legge den valgte modulen til valgt container eller spor på siden.

### <a name="remove-a-module"></a>Fjerne en modul

Følg disse trinnene for å fjerne en modul fra sporet eller containeren på en side.

1. I disposisjonsruten til venstre velger du ellipsen (**...**) ved siden av navnet på modulen som skal fjernes, og deretter velger du papirkurvsymbolet. På hovedlerretet kan du også velge papirkurvsymbolet på verktøylinjen i en valgt modul.
1. Når du blir bedt om å bekrefte at du vil fjerne modulen, velger du **OK**.

## <a name="move-a-module-to-a-new-position"></a>Flytte en modul til en ny posisjon

Hvis du vil flytte en modul til en ny plassering på siden, kan du bruke en av følgende metoder.

### <a name="move-a-module-using-the-outline-pane"></a>Flytte en modul ved hjelp av disposisjonsruten

Følg denne fremgangsmåten for å flytte en modul ved hjelp av disposisjonsruten.

1. Velg og hold modulen du vil flytte, i disposisjonsruten, og dra deretter modulen til en ny posisjon i disposisjonen. Den blå linjen i disposisjonen og på lerretet viser hvor modulen kan plasseres.
1. Frigi modulen for å slippe den i den nye stillingen.

### <a name="move-a-module-directly-within-the-canvas"></a>Flytte en modul direkte på lerretet

Følg denne fremgangsmåten for å flytte en modul direkte ved hjelp av lerretet.

1. Velg modulen du vil flytte, på lerretet. 
1. Velg et pilsymbol som peker oppover eller nedover på verktøylinjen for modulen, og dra deretter pilen til en ny plassering på siden. Den blå linjen på lerretet og i disposisjonen viser hvor modulen kan plasseres. Hvis en modul ikke kan flyttes opp eller ned, vil dette pilsymbolet være nedtonet. 
1. Frigi modulen for å slippe den i den nye stillingen.

### <a name="move-a-module-using-the-ellipsis-menu"></a>Flytte en modul ved hjelp av ellipsemenyen

Følg denne fremgangsmåten for å flytte en modul ved hjelp av ellipsemenyen.

1. Velg en modul enten i disposisjonen eller på lerretet.
1. Velg ellipsen (**...**) ved siden av modulens navn i disposisjonsruten eller modulens verktøylinje i lerretet.
1. Hvis modulen kan flyttes opp eller ned i containeren eller sporet, vil du se alternativer for **Flytt opp** eller **Flytt ned**. Velg ønsket flyttealternativ for å flytte modulen opp eller ned i forhold dens sideordnede elementer.

## <a name="configure-modules"></a>Konfigurere moduler

Følgende prosedyrer beskriver hvordan du konfigurerer innhold og innholdsmoduler.

### <a name="configure-a-content-module"></a>Konfigurere en innholdsmodul

Hvis du vil konfigurere en innholdsmodul på en side, følger du disse trinnene.

1. I disposisjonsruten til venstre utvider du treet og velger en innholdsmodul (for eksempel **Innholdsblokk**). Du kan også velge modulen på hovedlerretet.
1. Angi egenskaper for eventuelle modulkontroller i modulegenskapsruten til høyre.
1. Velg **Lagre** på kommandolinjen. Dette vil også oppdatere forhåndsvisningslerretet.

### <a name="edit-module-text-properties"></a>Redigere tekstegenskaper for modul

Tekstegenskaper for modul som ikke er skrivebeskyttet, kan redigeres direkte på lerretet.

Følg denne fremgangs måten for å redigere tekstegenskaper for modul.

1. Merk tekstkontrollen på lerretet, og plasser deretter markøren der du vil redigere tekst.
1. Skriv inn tekstinnholdet.
1. Merk hvor som helst utenfor tekstinnholdet for å fortsette å redigere annet innhold.

### <a name="inline-image-selection"></a>Valg av innebygd bilde

Modulbilder som ikke er skrivebeskyttet, kan endres direkte fra lerretet.

Hvis du vil velge et nytt bilde for en innholdsmodul, følger du disse trinnene.

1. Dobbeltklikk bildet på lerretet. Dette henter frem medievelgervinduet.
1. Finn og velg et nytt bilde som du vil bruke, og velg deretter **OK**. Det nye bildet vises nå på lerretet.

### <a name="configure-a-container-module"></a>Konfigurere en containermodul

Hvis du vil konfigurere en containermodul på en side, følger du disse trinnene.

1. Velg en containermodul på siden (for eksempel en karusell eller en modul for flytende container).
1. I egenskapsruten til høyre utvider du de nestede kontrollene ved å velge overskriftene og angi eventuelle nødvendige kontrollverdier.
1. I disposisjonsruten til venstre velger du ellipseknappen ved siden av navnet på enten containeren eller eventuelle spor i containeren, og deretter velger du **Legg til modul**. Deretter legger du til underordnede moduler i den valgte containeren. Hvis du ha mer informasjon, kan du se delen [Arbeide med moduler](#add-a-module) tidligere i dette emnet.
1. Hvis det finnes flere underordnede moduler som sideordnede i en overordnet container, kan du endre visningsrekkefølgen i den overordnede containeren. Velg ellipseknappen for en modul, og bruk deretter tastene for pil opp og pil ned.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over maler og oppsett](templates-layouts-overview.md)

[Arbeide med maler](work-with-templates.md)

[Arbeide med forhåndsinnstilte oppsett](work-with-layouts.md)

[Arbeide med fragmenter](work-with-fragments.md)

[Legge til en containermodul på en side](add-container-module.md)

[Arbeide med publiseringsgrupper](publish-groups.md)

