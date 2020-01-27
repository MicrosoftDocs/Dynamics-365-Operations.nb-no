---
title: Administere attributter og attributtgrupper
description: Dette emnet beskriver hvordan du bruker attributter til å beskrive et produkt og egenskapene ved hjelp av brukerdefinerte felt.
author: ashishmsft
manager: AnnBe
ms.date: 04/28/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: asharchw
ms.search.validFrom: 2018-03-30
ms.dyn365.ops.version: Application pdate 5, AX 8.0
ms.openlocfilehash: 5ba273265b677f71762c8beae3561712efb92645
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915278"
---
# <a name="manage-attributes-and-attribute-groups"></a>Administere attributter og attributtgrupper

[!include [banner](includes/banner.md)]

*Attributter* gir en metode for å beskrive et produkt og dets egenskaper ved hjelp av brukerdefinerte felt (som **Minnestørrelse**, **Harddiskkapasitet**, **Is Energy star-kompatibel** og så videre). Attributter kan knyttes til forskjellige Retail-enheter, for eksempel produktkategorier og kanaler for detaljhandel, og du kan angi standardverdier for dem. Produkter arver attributtene og standardverdiene når de blir knyttet til produktkategoriene eller detaljhandelskanaler. Standardverdiene kan overstyres på nivået for det individuelle produktet, på nivået for detaljhandelskanalen, eller i en detaljhandelskatalog.


Et vanlig TV-produkt kan for eksempel ha følgende attributter.

| Kategori   | Attributt                | Tillatte verdier          | Standardverdi |
|------------|--------------------------|-----------------------------|---------------|
| TV og video | Merke                    | En gyldig merkeverdi       | None          |
| TV         | Skjermstørrelse              | 20–80 tommer                | None          |
|            | Loddrett oppløsning      | 480i, 720p, 1080i eller 1080p | 1080p         |
|            | Oppdateringsfrekvens for skjerm      | 60 Hz, 120 Hz eller 240 Hz       | 60 Hz          |
|            | HDMI-innganger              | 0–10                        | 3             |
|            | DVI-innganger               | 0–10                        | 1             |
|            | Komposittinnganger         | 0–10                        | 2             |
|            | Komponentinnganger         | 0–10                        | 1             |
| LCD-SKJERM        | 3D Ready                 | Ja eller No                   | Ja           |
|            | 3D Enabled               | Ja eller No                   | Antall            |
| Plasma     | Driftstemperatur fra      | 0–43 grader              | 32            |
|            | Driftstemperatur til        | 0–43 grader              | 100           |
| Projektor | Garanti for projiseringsrør | 6, 12 eller 18 måneder         | 12            |
|            | \# Antall projiseringsrør   | 1–5                         | 3             |

## <a name="attributes-and-attribute-types"></a>Attributter og attributtyper

Attributter er basert på *attributtyper*. Attributtypen identifiserer datatypen som kan angis for et bestemt attributt. Følgende attributtyper støttes:

- **Valuta** – Denne typen støtter en valutaverdi. Den kan være bundet (det vil si den kan støtte et verdiområde), eller den kan være være tom.
- **Dato og klokkeslett** – Denne attributtypen støtter en dato- og klokkeslettverdi. Den kan være bundet eller åpen.
- **Desimal** – Denne attributtypen støtter en numerisk verdi som inneholder desimaler. Den støtter også en måleenhet. Den kan være bundet eller åpen.
- **Heltall** – Denne attributtypen støtter en numerisk verdi. Den støtter også en måleenhet. Den kan være bundet eller åpen.
- **Tekst** – Denne attributtypen støtter en tekstverdi. Den støtter også et forhåndsdefinert sett med mulige verdier (altså en *opplisting*).
- **Boolsk** – Denne attributtypen støtter en binær verdi (**sann** eller **usann**).
- **Referanse** – Denne typen refererer til andre attributter.

### <a name="set-up-attribute-types"></a>Definer attributtyper

1. Logge på Back Office-klienten som en varehandelsleder for detaljhandel.
2. Gå til **Behandling av produktinformasjon** &gt; **Oppsett** &gt; **Kategorier og attributter** &gt; **Attributtyper**.
3. Opprett to attributtyper av typen **Tekst**, sett valget **Fast liste** til **Ja**, og legg til en liste over verdier:

    - Gi navn til en attributtype **form**, og legg til følgende verdier: **oval**, **firkantet**, og **rektangulært**.
    - Gi navn til den andre attributtypen **solbrillemerke**, og legg til følgende verdier: **Ray ban**, **Aviator**, og **Oakley**.

![Attributtyper](media/AttributeType.png)

### <a name="set-up-an-attribute"></a>Definer attributter

1. Logge på Back Office-klienten som en varehandelsleder for detaljhandel.
2. Gå til **Behandling av produktinformasjon** &gt; **Oppsett** &gt; **Kategorier og attributter** &gt; **Attributter**.
3. Opprett et attributt som heter **Glass**.
4. Angi **Attributtype** til **Form**.

![Attributter](media/Attribute.png)

## <a name="attribute-metadata"></a>Attributtmetadata

Med *Attributtmetadata* kan du velge alternativer for å angi hvordan attributtene for hvert produkt skal fungere. Du kan for eksempel angi om attributter skal være obligatoriske, om de skal brukes til søk, og om de kan brukes som et filter.

Innstillingene for attributtet kan overstyres på kanalnivå for detaljhandelsprodukter. Denne funksjonen diskuteres senere i dette emnet.

Som du kanskje har merket deg, inneholder **Attributter**-siden alternativer som er knyttet til Attributtmetadata. Under **Attributtmetadata for POS**, påvirker et alternativ som heter **Kan justeres** atferden til attributtverdier i POS, eller måten systemet behandler disse attributtverdiene. Bare attributtene der du kan angi **Kan justeres** til **Ja**, vises for finjustering eller filtrering av produkter i Retail POS.

Her er de gjenværende alternativene for attributtet metadata på siden **Attributter**:

- Søkbar
- Kan hentes
- Kan spørres
- Sorterbar
- Tillat flere verdier
- Ignorer bokstavtype og format
- Fullt samsvar

Disse alternativene er egentlig beregnet for å forbedre søkefunksjonen for nettbutikkfasaden. Selv om Retail ikke inneholder nettbutikkfasade, er eCommerce Publishing Software Development Kit (SDK) inkludert. Kunder kan bruke denne SDK for å plassere varer i en søkeindeks etter eget valg. Selv om den unike produktinformasjonen blir importert, skal kunder fortsatt kunne skille mellom søkbare data, data som kan inngå i spørringen, og så videre. På den måten kan de bygge en optimal indeks for å være sikker på at de bare indeksere attributter som *etter deres synspunktt*, skal indekseres.

Hvis du vil ha informasjon om hensikten med resten av alternativene, se [oversikt over søkeskjemaet i SharePoint Server 2013](https://technet.microsoft.com/library/jj219669.aspx).

## <a name="filter-settings-for-attributes"></a>Filterinnstillinger for attributtfilter.

Med filterinnstillingene for attributter kan du definere hvordan filtrene for attributter skal vises i Retail POS. For å få tilgang til filterinnstillingene for et attributt på **Attributter**-siden, merker du attributtet, og i handlingsruten velger du **Filterinnstillinger**.

Siden **Innstillinger for filtervisning** inneholder følgende felt:

- **Navn** – som standard er dette feltet satt til navnet på attributtet. Du kan imidlertid endre verdien.
- **Visningsalternativ**- følgende alternativer er tilgjengelige:

    - **Enkeltverdi** – dette alternativet er tilgjengelig for følgende attributter: **Boolsk**, **Valuta**, **Desimal**, **Heltall** og **Tekst**. Dette alternativet gir enkeltverdivalg for disse attributtene i klienten for finjustering.
    - **Flerverdi** – denne muligheten er tilgjengelig for følgende atributtyper: **Valuta**, **Desimal**, **Integer** og **Tekst**. Dette alternativet gir valg av flerverdi for dette attributtet i klienten for finjustering.

- **Visningskontroll**- følgende alternativer er tilgjengelige:

    - **Liste** - dette alternativet er tilgjengelig for alle atributtyper.
    - **Område** – denne muligheten er tilgjengelig for følgende atributtyper: **Valuta**, **Desimal** og **Integer**.
    - **Glidebryter** – denne muligheten er tilgjengelig for følgende atributtyper: **Valuta**, **Desimal** og **Integer**.
    - **Glidebryter med linjer** – denne muligheten er tilgjengelig for følgende atributtyper: **Valuta**, **Desimal** og **Integer**.

- **Terskelverdi** – denne innstillingen kreves hvis du har valgt **Område** som kontrolltype for visningen. Du kan definere verdier med et semikolon (;) som skilletegn.

    For **posevolume**, for eksempel, kan terskelverdien være **10. 20, 50; 100; 200; 500; 1000. 5000**. Retail-POS viser i så fall følgende områder. Alle områder som ikke har noen produkter i resultatsettet vises nedtonet.

    - Under 10
    - 10 – 20
    - 20 – 50
    - 50 – 100
    - 100 – 200
    - 200 – 500
    - 500 eller mer

![Innstillinger for attributtfilter](media/AttributeFilterSettings.PNG)

## <a name="attribute-groups"></a>Attributtgrupper

Etter at attributtene er definert, kan de tilordnes attributtgrupper. En *attributtgruppe* brukes til å gruppere de individuelle attributtene for en komponent eller delkomponent i en produktkonfigurasjonsmodell. Et attributt kan inkluderes i én eller flere attributtgrupper. Attributtgrupper kan hjelpe brukere med å konfigurere produkter, fordi de forskjellige valgene er ordnet i en bestemt kontekst. Attributtgrupper kan tilordnes til detaljhandelkategorier eller detaljhandelkanaler.

Du kan også angi standardverdier for attributter som er inkludert i en attributtgruppe. Du kan for eksempel legge til et attributt for farge i en attributtgruppe, og velge **blå** som standard attributtverdi. I så fall, når attributtgruppen legges til et handelsprodukt som inkluderer farge som ett av attributtene, vises **blå** som standardfarge for produktet.

![Attributtgrupper](media/AttributeGroup.png)

### <a name="create-an-attribute-group"></a>Opprette en attributtgruppe

1. Logge på Back Office-klienten som en varehandelsleder for detaljhandel.
2. Gå til **Behandling av produktinformasjon** &gt; **Oppsett** &gt; **Kategorier og attributter** &gt; **Attribugrupper**.
3. Opprette en attributtgruppe med navnet **Moteriktige solbriller**.
4. Legge til følgende attributter: **form** og **solbrillemerke**.

### <a name="assign-attribute-groups-to-retail-categories"></a>Tilordne attributtgrupper til detaljhandelskategorier

Én eller flere attributtgrupper kan knyttes til kategorinoder i følgende typer detaljhandelshierarkier: hierarki for detaljhandelprodukt, kanalnavigasjonshierarkiet for kategorier og ekstra hierarki for leverandørproduktkategori. Etter at varer er kategorisert, arver de attributtene som er inkludert i attributtgruppene.

![Hierarki for detaljhandelprodukt – Produktattributtgrupper](media/AGRetailProdHierarchy.PNG)

Følg denne fremgangsmåten for å tilordne attributtgrupper til kategorier i hierarki for detaljhandelprodukt.

1. Logge på Back Office-klienten som en varehandelsleder for detaljhandel.
2. Gå til **Retail** &gt; **Kategori- og produktstyring** &gt; **Hierarki for detaljhandelprodukt**.
3. Velg **Navigasjonshierarkiet for klær**.
4. Under **Herreklær**, velger du kategorien **Bukser** og på hurtigfane **Produktattributtgrupper** er attributtgruppen **Herrebelter** lagt til.
5. Velg kategorien **Moteriktige solbriller**, og kontroller de nye attributtene i attributtgruppen **Moteriktige solbriller** ved å velge **Vis attributter**.

    Attributtgruppen skal vise de nye attributtene **form** og **solbrillemerke**.

6. Under **Herreklær**, velger kategorien **Bukser**, og kontroller attributtene for attributtgruppen **Herrebelte** ved å velge **Vis attributter**.

    Attributtgruppen skal vise attributtene **merke herrebelte**, **beltemateriale**, og **beltestørrelse** .

> [!NOTE]
> Denne fremgangsmåten kan også brukes til å tilordne attributtgrupper til kategorier i navigasjonskategorihierarkiet for kanalen og Ekstra produktkategorihierarkiet. Bruk følgende navigasjonsbane i trinn 2:
>
> - Detaljhandel &gt; Kategori- og produktstyring &gt; Navigasjonskategorier for kanal
> - Detaljhandel &gt; Kategori- og produktstyring &gt; Ekstra produktkategorier

### <a name="assign-attribute-groups-to-retail-stores"></a>Tilordne attributtgrupper til detaljhandelsbutikker

Én eller flere attributtgrupper kan knyttes til én eller flere detaljhandelsbutikker i hierarkiet for detaljhandelsbutikker. Når varene er supplert for spesifikke detaljhandelsbutikker, arver de attributtene som er inkludert i attributtgruppene.

1. Logge på Back Office-klienten som en varehandelsleder for detaljhandel.
2. Gå til **Detaljhandel** &gt; **Kanaloppsett** &gt; **Kanalkategorier og produktattributter**.
3. Tilordne attributter til Houston-kanalen:

    1. Velg **Houston**-kanalen.
    2. På hurtigfanen **Attributtgruppe** velger du **Legg til**, og i feltet **Navn** velger du **SharePointProvisionedProductAttributeGroup**.
    3. Velg **Legg til** på nytt, og i feltet **Navn** velger du **Herrebelte**.
    4. Velg **Legg til** på nytt, og i feltet **Navn** velger du **Moteriktige solbriller**.

        > [!NOTE]
        > Et alternativ som lar deg angi at denne kanalen skal arve attributtgruppene fra den overordnede kanalen i hierarkiet. Hvis du setter valget **Arv** til **Ja**, arver den underordnede kanalnoden alle attributtgrupper og alle attributtene i disse attributtetgruppene.

4. Aktiver attributtene slik at de er tilgjengelige i Houston-kanalen:

    1. I handlingsruten velger du **Angi attributtmetadata**.
    2. Velg kategorinoden **Klær** og på hurtigfanen **Kanalproduktattributter** hurtigkategorien, velger du **Inkluder attributt** for hvert attributt.
    3. Velg kategorinoden **Tilbehør** velg kategorien **Moteriktige solbriller** og på hurtigfanen **Kanalproduktattributter** Velger du **Inkluder attributt** for hvert attributt.
    4. Velg kategorinoden **Herreklær**, så kategorien **Bokser**, og på hurtigfanen **Kanalproduktattributter** Velger du **Inkluder attributt** for hvert attributt.

![Kanalkategorier og produktattributter - Attributtgrupper](media/CCPAttrGrp.png)

## <a name="overriding-attribute-values"></a>Overstyre attributtverdier

Standardverdiene for attributter kan overstyres for enkeltprodukter på produktnivå. Standardverdiene kan også overstyres for individuelle produkter i bestemte kataloger som er rettet mot bestemte detaljhandelkanaler.

### <a name="override-the-attribute-values-of-an-individual-product"></a>Overstyre attributtverdier for et enkelt produkt

1. Logge på Back Office-klienten som en varehandelsleder for detaljhandel.
2. Gå til **Detaljhandel** &gt; **Kategori- og produktstyring** &gt; **Utgitte produkter etter kategori**.
3. Velg kategorinoden **Klær** &gt; **Tilbehør** &gt; **Moteriktige solbriller**.
4. Velg det nødvendige produktet i rutenettet. I handlingsruten, i **Produkt**-kategorien og **Oppsett**-gruppen, velger du **Produktattributter**.
5. Marker et attributt i venstre rute, og oppdater deretter verdien i den høyre ruten.

![Siden med produktdetaljert – Produktattributtgrupper](media/ProdDetailsProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-catalog"></a>Overstyre attributtverdier for produkter i en katalog

1. Logge på Back Office-klienten som en varehandelsleder for detaljhandel.
2. Gå til **Detaljhandel** &gt; **Katalogadministrasjon** &gt; **Alle kataloger**.
3. Velg katalogen **Fabrikam basiskatalog**.
4. Velg kategorinoden **Klær** &gt; **Tilbehør** &gt; **Moteriktige solbriller**.
5. På hurtigfanen **Produkter** velger du det aktuelle produktet og så **Attributter** over produktrutenettet.
6. Oppdater verdiene for de obligatoriske attributtene på følgende hurtigfaner:

    - Delte produktmedier
    - Delte produktattributter
    - Kanalmedier
    - Kanalproduktattributter

    > [!NOTE]
    > Hvis delte produktmedier og delte produktattributter opprettes, gjelder de for alle detaljhandelsprodukter.

![Produktattributtverdi for grupper](media/CatalogProdAttrValues.png)

### <a name="override-the-attribute-values-of-products-in-a-channel"></a>Overstyre attributtverdier for produkter i en kanal

1. Logge på Back Office-klienten som en varehandelsleder for detaljhandel.
2. Gå til **Detaljhandel** &gt; **Kanaloppsett** &gt; **Kanalkategorier og produktattributter**.
3. Velg **Houston**-kanalen.
4. På hurtigfanen **Produkter** velger du det aktuelle produktet og så **Attributter** over produktrutenettet.

    > [!NOTE]
    > Hvis det ikke finnes produkter, legger du til produkter ved å velge **Legg til** på hurtigfanen **Produkter**. Velg deretter aktuelle produktene i **Legg til produkter**-dialogboksen.

5. Oppdater verdiene for de obligatoriske attributtene på følgende hurtigfaner:

    - Delte produktmedier
    - Delte produktattributter
    - Kanalmedier
    - Kanalproduktattributter

    > [!NOTE]
    > Hvis delte produktmedier og delte produktattributter opprettes, gjelder de for alle detaljhandelsprodukter.
