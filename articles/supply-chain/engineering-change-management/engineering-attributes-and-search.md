---
title: Tekniske attributter og søk i tekniske attributter
description: I denne artikkelen finner du informasjon om hvordan du kan bruke tekniske attributter til å angi alle ikke-standardegenskaper, for å sikre at alle produkthoveddataene kan registreres i systemet. Det forklarer også hvordan du kan bruke søk i tekniske attributter til å finne produkter på en enkel måte, basert på de registrerte egenskapene.
author: t-benebo
ms.date: 09/28/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: EngChgProductAttributeSearch, EngChgMaintainAttributeInheritance, EngChgAttribute
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 4b25ab0bfda08b7aa091de8c6833007c586b9c87
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8852570"
---
# <a name="engineering-attributes-and-engineering-attribute-search"></a>Tekniske attributter og søk i tekniske attributter

[!include [banner](../includes/banner.md)]

Bruke tekniske attributter til å angi alle ikke-standardegenskaper for å sikre at alle produktstandarder kan registreres i systemet. Du kan deretter bruke søk i tekniske attributter til å finne produkter på en enkel måte, basert på de registrerte egenskapene.

## <a name="create-engineering-attributes-and-attribute-types"></a>Opprett tekniske attributter og attributtyper

Tekniske produkter har vanligvis mange egenskaper du må ta opp. Selv om du kan registrere noen av egenskapene ved å bruke standard produktfelter, kan du også opprette nye tekniske egenskaper etter behov. Du kan definere dine egne *tekniske attributter* og gjøre dem til en del av produktdefinisjonen.

Hvert tekniske attributt må tilhøre en *attributtype*. Dette kravet finnes fordi hvert tekniske attributt må ha en *datatype* som definerer verditypene det kan inneholde. En teknisk attributttype kan være en standardtype (for eksempel fritekst, heltall eller desimal) eller en egendefinert type (for eksempel tekst med et bestemt sett med verdier du kan velge fra). Du kan bruke hver attributtype på nytt med en rekke tekniske attributter.

### <a name="set-up-engineering-attribute-types"></a>Definer tekniske attributtyper

Følg denne fremgangsmåten for å vise, opprette eller redigere en teknisk attributtype.

1. Gå til **Behandling av teknisk endring \> Oppsett \> Attributter \> Attributtyper**.
1. Velg en eksisterende attributtype i listeruten, eller velg **Ny** i handlingsruten for å opprette en ny attributtype.
1. Angi følgende felt:

    - **Attributtypenavn** – Angi et navn på attributtypen.
    - **Type** – Velg en standard datatype (*valuta*, *datetime*, *desimal*, *heltall*, *tekst*, *boolsk* eller *referanse*).
    - **Fast liste** – Dette alternativet er bare tilgjengelig hvis du angir feltet **Type** til *Tekst*. Sett det til *Ja* for å definere bestemte verdier for attributter av denne typen. I dette tilfellet vil det bli opprettet en rullegardinliste. Du bruker **Verdi**-hurtigfanen til å opprette verdiene som er tilgjengelige for denne attributtypen. Sett dette alternativet til *Nei* for å la brukerne angi en verdi. I dette tilfellet vil et inndatafelt bli opprettet.
    - **Verdiområde** – Dette alternativet er bare tilgjengelig hvis du setter **Type**-feltet til *Heltall*, *Desimal* eller *Valuta*. Sett det til *Ja* for å etablere minimums- og maksimumsverdier som blir godtatt for attributter av denne typen. Du bruker **Område**-hurtigfanen til å fastsette minimums- og maksimumsverdiene, og (for valuta) valutaen som gjelder for de angitte grensene. Sett dette alternativet til *Nei* for å godta alle verdier. 
    - **Måleenhet** – Dette feltet er bare tilgjengelig hvis du setter **Type**-feltet til *Heltall* eller *Desimal*. Velg måleenheten som gjelder for denne attributtypen. Hvis ingen enhet er nødvendig, lar du dette feltet stå tomt.

### <a name="set-up-engineering-attributes"></a>Definer tekniske attributter

Følg denne fremgangsmåten for å vise, opprette eller redigere et teknisk attributt.

1. Gå til **Behandling av teknisk endring \> Oppsett \> Attributter \> Tekniske attributter**.
1. Velg et eksisterende attributt i listeruten, eller velg **Ny** i handlingsruten for å opprette et nytt attributt.
1. Angi følgende felt:

    - **Navn** – Angi et navn for attributtet. Dette navnet vises bare på siden **Tekniske attributter**. Andre steder i systemet vises verdien for feltet **Egendefinert navn** vanligvis for å identifisere attributtet.
    - **Attributtype** – Velg en attributtype du definerte i den forrige delen.
    - **Egendefinert navn** – Angi et navn som identifiserer attributtet i systemet (bortsett fra på siden **Tekniske attributter**). 
    - **Beskrivelse** – Angi en beskrivelse av attributtet.
    - **Hjelpetekst** – Angi hjelpetekst som forteller andre brukere hva attributtet gjelder for.
    - **Standardverdi** – Angi en standardverdi for attributtet. Alternativene som vises, er avhengig av attributtypen du har valgt.
    - **Valuta** – Hvis attributtypen du valgte er en valuta, velger du valutaen som attributtet skal godta og vise verdier i.

1. Hvis attributtypen du valgte er et heltall eller en desimal, vises **Område**-hurtigfanen. Angi følgende felter i denne hurtigfanen:

    - **Toleransehandling** – Velg hvordan systemet skal svare hvis en bruker angir en verdi utenfor det angitte området. Hvis du velger *Advarsel*, vises en advarsel, men brukeren kan lagre verdien. Hvis du velger *Ikke tillatt*, vises en advarsel, og verdien kan ikke lagres før brukeren retter den opp.
    - **Minimum** – Angi minste anbefalte eller godkjente verdi.
    - **Maksimum** – Angi høyeste anbefalte eller godkjente verdi.

### <a name="engineering-attribute-inheritance"></a>Teknisk attributt-arv

For produktstrukturer, for eksempel stykklister eller formler, kan valgte attributter sendes fra de underordnede elementene opp til de overordnede elementene. Du kan se på denne prosessen som "tilbakefør arv."

#### <a name="turn-engineering-attribute-inheritance-on-or-off"></a>Aktivere eller deaktivere teknisk attributt-arv

Denne funksjonen krever at funksjonene *Behandling av teknisk endring* og *Forbedret attributtarv for behandling av teknisk endring* er aktivert for systemet. Hvis du vil ha mer informasjon om hvordan du aktiverer eller deaktiverer disse funksjonene, kan du se [Oversikt over behandling av teknisk endring](product-engineering-overview.md).

#### <a name="attribute-inheritance-example"></a>Eksempel på attributtarv

For et matprodukt som en gulrotkake, må systemet registrere hvert allergen som produktet inneholder. Gulrotkaken kan modelleres i systemet som et teknisk produkt som har en formel. Denne formelen inneholder ingrediensene til gulrotkaken, for eksempel mel, melk, gulrot og nøtter. I dette eksemplet tilbyr firmaet to modeller for gulrotkake: en som inneholder laktose, og en som ikke gjør det.

Kaken som inneholder laktose, har følgende attributter på ingrediensnivået:

- Ingrediens "mel": attributt "gluten" = ja
- Ingrediens "melk": attributt "laktose" = ja
- Ingrediens "nøtter": attributt "nøtter" = ja

Kaken som ikke inneholder laktose, bruker laktosefri melk og har følgende attributter på ingrediensnivået:

- Ingrediens "mel": attributt "gluten" = ja
- Ingrediens "melk": attributt "laktose" = nei
- Ingrediens "nøtter": attributt "nøtter" = ja

Fordi disse produktene er stort sett like, kan det være nyttig å sende disse attributtene fra de underordnede attributtene (de to variasjonene) til det overordnede produktet (den grunnleggende gulrotkaken). Når du skal implementere denne "tilbakeføringsarven", kan du bruke funksjonaliteten for *attributtarv*. Denne funksjonaliteten er definert for hver [teknisk versjon](engineering-versions-product-category.md).

## <a name="connect-engineering-attributes-to-an-engineering-product-category"></a>Koble sammen tekniske attributter til en kategori for teknisk produkt

Noen tekniske attributter gjelder for alle produkter, mens andre er spesifikke for individuelle produkter eller produktkategorier. Elektriske attributter kreves for eksempel ikke for mekaniske produkter. Derfor kan du definere *kategorier for teknisk produkt*. En kategori for teknisk produkt etablerer samlingen av tekniske attributter som må være del av definisjonen for produkter som tilhører denne kategorien. Du kan også angi hvilke tekniske attributter som er obligatoriske, og om det finnes en standardverdi.

Hvis du vil ha mer informasjon om hvordan du arbeider med kategorier for teknisk produkt, deriblant informasjon om hvordan du kobler attributter til kategorier, kan du se [Tekniske versjoner og kategorier for teknisk produkt](engineering-versions-product-category.md).

## <a name="set-attribute-values-for-engineering-attributes"></a>Angi attributtverdier for tekniske attributter

Tekniske attributter som er koblet til en kategori for teknisk produkt, presenteres når du oppretter et nytt teknisk produkt som er basert på denne kategorien. Du kan når som helst angi verdier for attributtene. Senere kan disse verdiene endres på siden **Teknisk versjon** eller som en del av behandling av teknisk endring i en ordre om teknisk endring. Hvis du vil ha mer informasjon, kan du se [Behandle endringer i tekniske produkter](engineering-change-management.md).

## <a name="create-an-engineering-product"></a>Opprett et teknisk produkt

Åpne siden **Frigitte produkter** for å opprette et teknisk produkt. I handlingsruten, i **Produkt**-fanen og **Ny**-gruppen velger du **Teknisk produkt**.

Du må angi den tekniske kategorien som produktet tilhører. Kategorien angir alle standardverdier og -egenskaper for produktet. Den vil også angi attributtene som gjelder for produktet. Når kategorien er valgt, vil det bli angitt verdier for attributtene. Deretter kan du endre disse verdiene.

## <a name="search-for-products-by-using-engineering-attribute-values"></a>Søk etter produkter ved hjelp av verdier for tekniske attributter

Du kan bruke søk i tekniske attributter til å finne produkter ved å søke etter verdier for tekniske attributter. Derfor er det enkelt å finne tekniske produkter basert på deres egenskaper. Du kan søke i produktene som hører til en utviklingsproduktkategori, eller du kan søke på tvers av alle tekniske produkter.

Søket er tilgjengelig på sider for produkthoveddata og fra transaksjonelle elementer i systemet, for eksempel salgsordrer. For et transaksjonselement kan du bruke siden **Søk i teknisk attributt** til å søke etter et produkt. Du kan deretter bruke knappen **Legg til som ny linje** til å legge til produktet i salgsordrelinjene. Produkter i søkeresultatene kan også legges til direkte i ordren.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
