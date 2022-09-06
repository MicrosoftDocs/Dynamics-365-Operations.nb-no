---
title: Administere attributter og attributtgrupper
description: Denne artikkelen beskriver hvordan du kan administrere attributter og attributtgrupper for å beskrive produkter og egenskapene deres i Microsoft Dynamics 365 Commerce.
author: ashishmsft
ms.date: 08/31/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: josaw
ms.search.region: Global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.openlocfilehash: aad448ea733aabdff3dc4438dcb682d49e0665c0
ms.sourcegitcommit: 09d4805aea6d148de47c8ca38d8244bbce9786ce
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/31/2022
ms.locfileid: "9386979"
---
# <a name="manage-attributes-and-attribute-groups"></a>Administere attributter og attributtgrupper

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du kan administrere attributter og attributtgrupper for å beskrive produkter og egenskapene deres i Microsoft Dynamics 365 Commerce.

Du kan bruke *attributter* til å beskrive produkter og egenskapene deres ved hjelp av brukerdefinerte felter. Eksempler omfatter minnestørrelse, harddiskkapasitet og samsvar med Energy Star-merkeordningen.

Attributter kan knyttes til forskjellige Commerce-enheter, for eksempel produktkategorier og kanaler, og du kan angi standardverdier for dem. Produkter arver disse attributtene og standardverdiene når de blir knyttet til produktkategorier eller kanaler. Standard attributtverdier kan overstyres på nivået for det individuelle produktet, på kanalnivået, eller i en katalog.

Et vanlig TV-produkt kan for eksempel ha følgende attributter.

| Kategori   | Attributt           | Tillatte verdier                        | Standardverdi |
|------------|---------------------|-------------------------------------------|---------------|
| TV og video | Merke               | En gyldig merkeverdi                     | Ingen          |
| TV         | Skjermstørrelse         | 20–85 tommer                              | 55 tommer     |
|            | Loddrett oppløsning | 4K (2160p), full HD (1080p) eller HD (720p) | 4K (2160p)    |
|            | Oppdateringsfrekvens for skjerm | 60 Hz, 120 Hz eller 240 Hz                     | 60 Hz          |
|            | HDMI-innganger         | 0–10                                      | 3             |

## <a name="attributes-and-attribute-types"></a>Attributter og attributtyper

Attributter er basert på *attributtyper*. En attributtype identifiserer datatypen som kan angis for et bestemt attributt. Følgende attributtyper støttes i Commerce:

- **Valuta** – Denne typen støtter en valutaverdi. Den kan være bundet (det vil si den kan støtte et verdiområde), eller den kan være være tom.
- **Dato og klokkeslett** – Denne attributtypen støtter en dato- og klokkeslettverdi. Den kan være bundet eller åpen.
- **Desimal** – Denne attributtypen støtter en numerisk verdi som inneholder desimaler. Den støtter også en måleenhet. Den kan være bundet eller åpen.
- **Heltall** – Denne attributtypen støtter en numerisk verdi. Den støtter også en måleenhet. Den kan være bundet eller åpen.
- **Tekst** – Denne attributtypen støtter en tekstverdi. Den støtter også et forhåndsdefinert sett med mulige verdier når innstillingen **Fast liste** er aktivert.
- **Boolsk** – Denne attributtypen støtter en binær verdi (**sann** eller **usann**).
- **Referanse** – Denne typen refererer til andre attributter.

> [!NOTE]
> Attributtypen **Desimal** støttes ikke for skybasert søkefunksjonalitet på grunn av [begrensninger ved søkeindeksen for Azure](/rest/api/searchservice/data-type-map-for-indexers-in-azure-search). Azure Cognitive Search støtter ikke konvertering av attributtypen **Desimal** til feltindeksmåltypen **Edm.Double**, fordi denne konverteringen hadde redusert presisjonen.

### <a name="set-up-attribute-types"></a>Definer attributtyper

Følg trinnene i denne eksempelprosedyren for å definere attributtyper.

1. Logg deg på Commerce headquarters som varehandelsleder.
1. Gå til **Behandling av produktinformasjon \> Oppsett \> Kategorier og attributter \> Attributtyper**.
1. Velg **Ny** i handlingsruten.
1. Angi **Bag type** i feltet **Navn på attributtype**.
1. I feltet **Type** velger du **Tekst**.
1. Sett alternativet **Fast liste** til **Ja**.
1. Velg **Legg til** i hurtigfanen **Verdier**.
1. I den nye raden i **Verdi**-feltet angir du **Satchel**.
1. Legg til fem rader til. Angi en annen verdi i **Verdi**-feltet i hver rad: **Clutch**, **Purse**, **Backpack**, **Messenger** eller **Wallet**.
1. Velg **Lagre** i handlingsruten.
1. Velg **Ny** i handlingsruten.
1. Angi **Sunglass brand** i feltet **Navn på attributtype**.
1. I feltet **Type** velger du **Tekst**.
1. Sett alternativet **Fast liste** til **Ja**.
1. Velg **Legg til** i hurtigfanen **Verdier**.
1. I den nye raden i **Verdi**-feltet angir du **Ray ban**.
1. Legg til to rader til. Angi en annen verdi i **Verdi**-feltet i hver rad: **Aviator** eller **Oakley**.
1. Velg **Lagre** i handlingsruten.

![Siden Attributtyper.](media/AttributeType_2022Series.png)

### <a name="set-up-an-attribute"></a>Definer attributter

Følg trinnene i denne eksempelprosedyren for å definere et attributt.

1. Logg deg på Commerce headquarters som varehandelsleder.
1. Gå til **Behandling av produktinformasjon \> Oppsett \> Kategorier og attributter \> Attributter**.
1. Velg **Ny** i handlingsruten.
1. Angi **Bag type** i **Navn**-feltet.
1. Velg **Bag type** i **Attributtype**-feltet.
1. Velg **Lagre** i handlingsruten.

![Siden Attributter.](media/Attribute_2022Series.png)

## <a name="attribute-metadata"></a>Attributtmetadata

Med *Attributtmetadata* kan du velge alternativer for å angi hvordan attributtene for hvert produkt skal fungere. Du kan for eksempel angi om attributter skal være obligatoriske, om de skal brukes til søk, og om de kan brukes som et filter.

Innstillingene for attributtet kan overstyres på kanalnivå for produkter.

**Attributter**-siden for et attributt inneholder flere alternativer som er knyttet til attributtmetadata. Hvis du for eksempel velger **Ja** for alternativet **Kan justeres** under **Attributtmetadata for Commerce-kanaler**, vises attributtet for justering eller filtrering av produkter i søkeresultater og sider for kategorilesing. For å kunne konfigurere et attributt som justerbart må du først velge **Filterinnstillinger** i handlingsruten og bekrefte filterinnstillingene for attributtet.

## <a name="filter-settings-for-attributes"></a>Filterinnstillinger for attributtfilter.

Med filterinnstillingene for attributter kan du definere hvordan attributtfiltre skal vises på salgsstedet. For å få tilgang til filterinnstillingene for et attributt velger du **Filterinnstillinger** i handlingsruten på **Attributter**-siden.

Siden **Filterinnstillinger** inneholder følgende felter:

- **Navn** – som standard er dette feltet satt til navnet på attributtet. Du kan imidlertid endre verdien.
- **Visningsalternativ**- følgende alternativer er tilgjengelige:

    - **Enkeltverdi** – dette alternativet er tilgjengelig for følgende attributter: **Boolsk**, **Valuta**, **Desimal**, **Heltall** og **Tekst**. Det gjør at bare én verdi kan velges for presiseringer på produktlistesider, for eksempel sider for kategorilesing og produktsøkeresultater.
    - **Flerverdi** – dette alternativet er tilgjengelig for følgende attributtyper: **Valuta**, **Desimal**, **Integer** og **Tekst**. Det gjør at du kan velge flere verdier for attributtet i klienten, for å finjustere det.

- **Visningskontroll**- følgende alternativer er tilgjengelige:

    - **Liste** – dette alternativet er tilgjengelig for alle attributtyper.
    - **Område** – denne muligheten er tilgjengelig for følgende attributtyper: **Valuta**, **Desimal** og **Integer**.
    - **Glidebryter** – denne muligheten er tilgjengelig for følgende attributtyper: **Valuta**, **Desimal** og **Integer**.
    - **Glidebryter med linjer** – denne muligheten er tilgjengelig for følgende attributtyper: **Valuta**, **Desimal** og **Integer**.

- **Terskelverdi** – denne innstillingen kreves hvis du har valgt **Område** som kontrolltype for visningen. Du kan definere verdier med et semikolon (;) som skilletegn.

    Terskelverdien for et **Bag Volume**-attributt som har attributtypen **Heltall**, kan for eksempel være **10; 20; 50; 100; 200; 500; 1000; 5000**. Salgsstedet viser i så fall følgende områder. Områder som ikke har noen produkter i resultatsettet, vises nedtonet.

    - Under 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 eller mer

Filterinnstillinger for attributter gjelder bare for produktattributter og kan brukes til å filtrere resultatene av produktsøk og kategorilesing. De gjelder ikke for kundesøk eller ordresøk, selv om de samme attributtene kan brukes til å supplere kunde- eller ordreinformasjon.

I standard Commerce-moduler er det ingen bruksklar støtte for filterinnstillinger for **Visningskontroll**, for eksempel **Område**, **Glidebryter** og **Glidebryter med linjer**. Innstillingene for **Område** og **Glidebryter** støttes fortsatt for salgsstedsløsninger, mens innstillingen for **Glidebryter med linjer** gjelder for eldre SharePoint-nettbutikker og er fortsatt tilgjengelig for tredjepartsintegrering og egendefinerte scenarioer.

Vi anbefaler at attributter som kan justeres, har et attributt av typen **Tekst** der alternativet **Fast liste** er aktivert, og at du holder listen håndterlig (opptil 100–200 unike verdier). Hvis en presisering skal ha 1000 eller flere unike verdier, er det mer hensiktsmessig å bruke et attributt av typen **Tekst** der alternativet **Fast liste** er deaktivert.

Oversettelser er avgjørende for attributtnavn og verdiene deres. Når det gjelder attributter av typen **Tekst** der alternativet **Fast liste** er aktivert, kan du definere oversettelser for attributtverdiene under **Attributtype**. For alle andre attributtyper kan du definere oversettelser på siden der du definerer attributtverdiene. Når det gjelder et attributt av typen **Tekst**, kan du for eksempel definere oversettelser for standardverdien på **Attributter**-siden for attributtet. Hvis du imidlertid overstyrer standardverdien på produktnivået, kan du definere oversettelser for attributtet på siden **Produktattributter** for produktet.

Når det er angitt at et attributt kan justeres for en kanal, bør du ikke oppdatere attributtypen. Hvis du gjør det, kommer du til å påvirke publiseringen av produktdata i søkeindeksen. I stedet anbefaler vi at du oppretter et nytt attributt for en ny type presisering, og trekker tilbake det forrige attributtet ved å fjerne det fra andre attributtgrupper.

Søk etter attributter støttes, men henter bare resultater for nøyaktige treff på søkeord. Attributtet **Fabric** har for eksempel verdien **Cashmere cotton**. Hvis en kunde søker etter «Cash», hentes ingen produkter laget av **Cashmere cotton**. Hvis en kunde imidlertid søker etter «Cashmere», «Cotton» eller «Cashmere Cotton», hentes produkter laget av **Cashmere cotton**.

### <a name="additional-attribute-metadata-options"></a>Ytterligere alternativer for attributtmetadata

> [!NOTE]
> Disse alternativene for attributtmetadata gjelder bare for eldre SharePoint-nettbutikker og eksterne integreringer. Hvis du vil ha mer informasjon om disse alternativene for attributtmetadata, kan du se [Oversikt over søkeskjemaet i SharePoint Server 2013](/SharePoint/search/search-schema-overview).

De følgende tilleggsalternativene for attributtmetadata er også tilgjengelige på **Attributter**-siden:

- Søkbar
- Kan hentes
- Kan spørres
- Sorterbar
- Ignorer bokstavtype og format
- Fullt samsvar

Disse alternativene var opprinnelig ment å forbedre søkefunksjonen for eldre SharePoint-baserte nettbutikker. De gjelder ikke nødvendigvis for Commerce-e-handelsnettsteder eller salgsstedsterminaler. Siden hodeløs integrering fortsatt støttes, er disse alternativene tilgjengelige for å eksportere attributtmetadata ved hjelp av SDK (Software Development Kit) for Commerce. Du kan bruke SDK for Commerce til å legge produkter i en egendefinert, optimalisert ekstern søkeindeks. På denne måten kan du sikre at bare attributter som skal indekseres, blir indeksert.

## <a name="attribute-groups"></a>Attributtgrupper

En *attributtgruppe* brukes til å gruppere de individuelle attributtene for en komponent eller delkomponent i en produktkonfigurasjonsmodell. Et attributt kan inkluderes i én eller flere attributtgrupper. Attributtgrupper kan hjelpe brukere med å konfigurere produkter, fordi de forskjellige valgene er ordnet i en bestemt kontekst. Attributtgrupper kan tilordnes til kategorier eller kanaler. Du kan også angi standardverdier for attributter i en attributtgruppe.

![Siden Attributtgrupper.](media/AttributeGroup_2022Series.png)

### <a name="create-an-attribute-group"></a>Opprette en attributtgruppe

Følg trinnene i denne eksempelprosedyren for å opprette en attributtgruppe.

1. Logg deg på Commerce headquarters som varehandelsleder.
1. Gå til **Behandling av produktinformasjon \> Oppsett \> Kategorier og attributter \> Attributtgrupper**.
1. Opprette en attributtgruppe med navnet **Dress Shirts**.
1. Legg til følgende attributter: **CleaningMethod**, **CollarType**, **Collection** og **Design**.

> [!NOTE]
> Visningsrekkefølgeverdiene til attributter i attributtgruppen verken påvirker eller gjelder for rekkefølgen på presiseringene i søke- eller kategorilesingsresultatene. De gjelder bare for scenarioet med ordreattributter.

### <a name="assign-attribute-groups-to-categories"></a>Tilordne attributtgrupper til kategorier

Én eller flere attributtgrupper kan knyttes til kategorinoder i følgende typer kategorihierarkier:

- Hierarki for handelsprodukt
- Kategorihierarki for kanalnavigasjon
- Ekstra produktkategorihierarki

Når produkter kategoriseres i kategorier som er knyttet til attributtgrupper, arver de attributtene som er inkludert i disse attributtgruppene.

![Hurtigfane for produktattributtgrupper på produkthierarkisiden for Commerce.](media/AGRetailProdHierarchy_2022Series.png)

Følg fremgangsmåten i denne eksempelprosedyren for å tilordne attributtgrupper til kategorier i Commerce-produkthierarkiet.

1. Logg deg på Commerce headquarters som varehandelsleder.
1. Gå til **Detaljhandel og handel \> Produkter og kategorier \> Handelsprodukthierarki**.
1. Velg navigasjonshierarkiet **Mote**.
1. Under **Herreklær** velger du kategorien **Bukser**, og i hurtigfanen **Produktattributtgrupper** legger du til en attributtgruppe kalt **Herrebelter**.
1. Velg kategorien **Moteriktige solbriller**, og kontroller de nye attributtene i attributtgruppen **Moteriktige solbriller** ved å velge **Vis attributter**. Attributtgruppen skal vise de nye attributtene **form** og **solbrillemerke**.
1. Velg kategorien **Bukser**, og kontroller attributtene for attributtgruppen **Herrebelter** ved å velge **Vis attributter**. Attributtgruppen skal vise attributtene **merke herrebelte**, **beltemateriale**, og **beltestørrelse** .

Den samme grunnleggende fremgangsmåten kan også brukes til å tilordne attributtgrupper til kategorier i navigasjonskategorihierarkiet for kanal og det ekstra produktkategorihierarkiet. I trinn 2 bruker du imidlertid en av følgende baner, avhengig av hierarkiet du vil tilordne attributtgrupper til:

- **Navigasjonskategorihierarki for kanal:** Gå til **Detaljhandel og handel \> Kategori- og produktstyring \> Navigasjonskategorier for kanal**.
- **Ekstra produktkategorihierarki:** Gå til **Detaljhandel og handel \> Kategori- og produktstyring \> Ekstra produktkategorier**.

> [!NOTE]
> Pass på at du bare tilknytter attributtgrupper i et kategorihierarki i hurtigfanen **Produktattributtgrupper**, ikke i hurtigfanen **Kategoriattributtverdier**. Hvis attributter vises i hurtigfanen **Kategoriattributtverdier**, velger du **Rediger kategorihierarki** i handlingsruten. Deretter velger du kategorinodene i hurtigfanen **Kategoriattributtgrupper** og velger **Fjern**. Det er ikke støtte for å hente attributter etter kategori via Commerce Scale Unit.

## <a name="identify-viewable-and-refinable-attributes-for-commerce-channels-for-the-default-product-collection"></a>Identifiser attributter som kan vises og justeres, for Commerce-kanaler for standard produktsamling

Etter at du har knyttet forskjellige attributtgrupper til kategorier i ulike hierarkier (Commerce-produkthierarki eller kanalnavigasjonskategorier) og definert attributtverdier for hvert produkt basert på kategoritilknytningen, må du aktivere flagget **Vis attributter i kanal** for å gjøre disse attributtene tilgjengelige i en bestemt kanal.

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Kanalkategorier og produktattributter**.
1. Velg **Angi attributtmetadata**, og velg deretter et attributt i venstre navigasjonsrute.
1. I hurtigfanen **Kanalproduktattributter** (ikke hurtigfanen **Kategoriattributter**) angir du **Ja** for alternativet **Vis attributter i kanal** for å gjøre attributtet synlig.
1. Hvis du også vil at attributtet skal kunne justeres, angir du **Ja** for alternativet **Kan justeres**.

### <a name="control-visibility-of-dimension-based-refiners-such-as-size-style-and-color"></a>Kontroller synligheten til dimensjonsbaserte presiseringer, for eksempel størrelse, stil og farge

Produktdimensjoner, for eksempel størrelse, stil og farge, er de mest brukte presiseringene. Hvis du vil gjøre disse produktdimensjonene tilgjengelige som presiseringer, må du tilknytte en attributtgruppe på kanalnivå som inneholder en referanse til en attributtype som automatisk arver verdier fra produktdimensjonsverdier.

Du kan angi at produktdimensjoner skal kunne vises og justeres, ved å oppdatere flagg på siden **Kanalkategorier og produktattributter**. Velg rotnoden i navigasjonsruten, og angi deretter **Ja** for alternativet **Vis attributter i kanal** for attributtene **Størrelse**, **Stil** og **Farge** i hurtigfanen **Kanalproduktattributter**. Hvis du også vil at disse attributtene skal kunne justeres, angir du **Ja** for alternativet **Kan justeres** for hvert attributt.

![Angi attributtmetadata for dimensjonspresiseringer.](./media/ProductDimensionRefinersMetadataSetup_2022Series.png)

For å aktivere attributtene slik at de er tilgjengelige i den demodatabaserte Houston-kanalen, følger du trinnene i denne eksempelprosedyren.

1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Kanalkategorier og produktattributter**.
1. Velg **Houston**-kanalen.
1. I handlingsruten velger du **Angi attributtmetadata**.
1. Velg kategorinoden **Klær** og på hurtigfanen **Kanalproduktattributter** hurtigkategorien, velger du **Inkluder attributt** for hvert attributt.
1. Velg kategorinoden **Tilbehør** velg kategorien **Moteriktige solbriller** og på hurtigfanen **Kanalproduktattributter** Velger du **Inkluder attributt** for hvert attributt.
1. Velg kategorinoden **Herreklær**, så kategorien **Bokser**, og på hurtigfanen **Kanalproduktattributter** Velger du **Inkluder attributt** for hvert attributt.
1. Etter at du har oppdatert attributtmetadataene for de tiltenkte attributtene og presiseringene, passer du på at du lagrer endringene og kjører jobben **Publiser kanaloppdateringer**. Etter at oppdateringene er publisert, må du kjøre følgende jobber: **1070** (**Kanalkonfigurasjon**), **1040** (**Produkter**) og **1150** (**Katalog**).

> [!NOTE]
> - Hvis virksomheten din krever at du ofte legger til eller fjerner produkter i navigasjonshierarkiet, eller at du foretar endringer, for eksempel oppdaterer visningsrekkefølgeverdier, legger til nye kategorier og legger til nye attributtgrupper i kategorier, anbefaler vi at du konfigurerer jobben **Publiser kanaloppdateringer** slik at den kjører som en hyppig satsvis jobb. Du kan alternativt utløse jobben **Publiser kanaloppdateringer** manuelt og deretter følgende CDX-jobber (Commerce Data Exchange): **1070** (**Kanalkonfigurasjon**), **1040** (**Produkter**) og **1150** (**Katalog**).
> - Alternativet **Arv** lar deg angi at en kanal skal arve attributtgruppene fra den overordnede kanalen i hierarkiet. Hvis du setter valget **Arv** til **Ja**, arver den underordnede kanalnoden alle attributtgrupper og alle attributtene i disse attributtetgruppene.
> - Hvis knappen **Angi attributtmetadata** i handlingsruten ikke er tilgjengelig, må du kontrollere at **Navigasjonshierarki** er knyttet til kanalen din i hurtigfanen **Generelt**.
> - Du må la være å tilknytte andre attributtgrupper enn dimensjonsbaserte attributtgrupper på et kanalnivå (for eksempel under **Attributtgrupper** på siden **Kanalkategorier og produktattributter**).
> - Etter innføringen av støtte for kundespesifikke B2B-kataloger (bedrift-til-bedrift) i Commerce versjon 10.0.27 forventes det at du identifiserer presiserings- og attributtoppsettene for hver B2B-katalog på samme måte som er beskrevet i denne artikkelen.

## <a name="override-attribute-values"></a>Overstyr attributtverdier

Standardverdiene for attributter kan overstyres for enkeltprodukter på produktnivå. De kan også overstyres for individuelle produkter i bestemte kataloger som er rettet mot bestemte kanaler.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Overstyre attributtverdier for et enkelt produkt

Følg trinnene i denne eksempelprosedyren for å overstyre attributtverdiene for et enkeltprodukt.

1. Logg deg på Commerce headquarters som varehandelsleder.
1. Gå til **Detaljhandel og handel \> Kategori- og produktstyring \> Utgitte produkter etter kategori**.
1. Velg **Klær \> Tilbehør \> Moteriktige solbriller**.
1. Velg det nødvendige produktet i rutenettet. I handlingsruten, i **Produkt**-kategorien og **Oppsett**-gruppen, velger du **Produktattributter**.
1. Marker et attributt i venstre rute, og oppdater deretter verdien i den høyre ruten.

![Siden Produktattributtverdier.](media/ProdDetailsProdAttrValues_2022Series.png)

### <a name="override-the-attribute-values-of-all-products-in-a-catalog"></a>Overstyr attributtverdiene for alle produkter i en katalog

Følg trinnene i denne eksempelprosedyren for å overstyre attributtverdiene for alle produkter i en katalog.

1. Logg deg på Commerce headquarters som varehandelsleder.
1. Gå til **Detaljhandel og handel \> Katalogadministrasjon \> Alle kataloger**.
1. Velg katalogen **Fabrikam basiskatalog**.
1. Velg **Klær \> Tilbehør \> Moteriktige solbriller**.
1. På hurtigfanen **Produkter** velger du det aktuelle produktet og så **Attributter** over produktrutenettet.
1. Oppdater verdiene for de obligatoriske attributtene på følgende hurtigfaner:

    - Delte produktmedier
    - Delte produktattributter
    - Kanalmedier
    - Kanalproduktattributter

### <a name="override-the-attribute-values-of-all-products-in-a-channel"></a>Overstyr attributtverdier for alle produkter i en kanal

Følg trinnene i denne eksempelprosedyren for å overstyre attributtverdiene for alle produkter i en kanal.

1. Logg deg på Commerce headquarters som varehandelsleder.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Kanalkategorier og produktattributter**.
1. Velg **Houston**-kanalen.
1. På hurtigfanen **Produkter** velger du det aktuelle produktet og så **Attributter** over produktrutenettet.
1. Hvis det ikke finnes produkter, velger du **Legg til** i hurtigfanen **Produkter**. Velg deretter de aktuelle produktene i dialogboksen **Legg til produkter**.
1. Oppdater verdiene for de obligatoriske attributtene på følgende hurtigfaner:

    - Delte produktmedier
    - Delte produktattributter
    - Kanalmedier
    - Kanalproduktattributter

### <a name="define-variant-specific-attribute-values-and-define-multiple-values-for-product-attributes"></a>Definer variantspesifikke attributtverdier og definer flere verdier for produktattributter

Følg trinnene i denne eksempelprosedyren for å definere variantspesifikke attributtverdier og definere flere verdier for produktattributter.

1. Logg deg på Commerce headquarters som varehandelsleder.
1. Gå til **Detaljhandel og handel \> Kanaloppsett \> Kanalkategorier og produktattributter**.
1. Velg **Houston**-kanalen.
1. I hurtigfanen **Produkter** velger du den aktuelle produktvarianten og deretter **Attributter** over produktrutenettet.
1. Hvis det ikke finnes produkter, velger du **Legg til** i hurtigfanen **Produkter**. Velg deretter de aktuelle produktvariantene i dialogboksen **Legg til produkter**.
1. Oppdater verdiene for de obligatoriske attributtene på følgende hurtigfaner:

    - Delte produktmedier
    - Delte produktattributter
    - Kanalmedier
    - Kanalproduktattributter

#### <a name="example-of-variant-specific-attribute-configuration"></a>Eksempel på variantspesifikk attributtkonfigurasjon
        
I dette eksemplet er produktet **P001-Master** en sko for flere aktiviteter i tre varianter: **Running**, **Walking** og **Trekking**. Du ønsker å definere verdien unikt for attributtet **Activity** for hver variant. I hurtigfanen **Produkter** på siden **Kanalkategorier og produktattributter** for kanalen definerer du attributtverdien **Activity** for variantene som vist i tabellen nedenfor.

| Variant     | Attributtverdien Activity |
|-------------|--------------------------|
| P001-Master | Sports                   |
| P001-1      | Running                  |
| P001-2      | Walking                  |
| P001-3      | Trekking                 |

Hvis en bruker søker etter «shoe», vises produktet **P001-Master** i søkeresultatene. Hvis du konfigurerte attributtet **Activity** slik at det kan justeres, viser **Activity**-presiseringen bare **Sports** som en verdi som kan justeres, fordi denne verdien ble definert for attributtet **Activity** på nivået for produktet **P001-Master**.

Attributter på variantnivå er som standard bare ment å brukes på produktdetaljsider (PDP-er). Når du velger en bestemt produktvariant på en PDP, oppdateres produktspesifikasjonene på PDP-en for den bestemte varianten.

For at presiseringer skal kunne hente attributtverdier som er definert på produktvariantnivået, må du definere et attributt på produktstandardnivået, merke av for **Tillat flere verdier** og angi **Tekst** for attributtypen.

Du må deretter fastsette alle mulige verdier for produktvariantene. For attributtet **Activity** som brukes i dette eksemplet, kan mulige verdier omfatte **Running**, **Walking**, **Hiking**, **Trekking**, **Camping**, **Watersports** og **Snowsports**.

Når du har fastsatt hva variantattributtverdiene skal være, kan du definere dem på produktstandardnivået ved hjelp av verdier atskilt med loddrette streker. For attributtet **Activity** kan du definere attributtverdien i produktstandarden som **Running|Walking|Hiking|Trekking|Camping|Watersports|Snowsports**.

For hver variant kan du deretter definere attributtverdier ved å angi enten enkeltverdier eller verdier atskilt med loddrette streker. For attributtet **Activity** kan du konfigurere en individuell produktvariant som **Running|Walking|Hiking**, **Running**, **Running|Hiking|Watersports** og så videre.

Etter at du har definert verdiene for variantattributt, velger du **Publiser kanaloppdateringer** i handlingsruten på siden **Kanalkategorier og produktattributter**, og kjører deretter jobbene **1150**, **1040** og **1070**.

Etter at jobbene er fullført og søkeindeksen oppdatert, skal alle forventede verdier vises i søkeresultater og kategorilesingsresultater.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
