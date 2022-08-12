---
title: Opprett Commerce-kataloger for B2B-områder
description: Denne artikkelen beskriver hvordan du oppretter handelskataloger for Microsoft Dynamics 365 Commerce-bedrift-til-bedrift-områder (B2B).
author: ashishmsft
ms.date: 07/11/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: Global
ms.author: asharchw
ms.search.validFrom: 2022-02-28
ms.openlocfilehash: 7d4ed3e2a76924c2c3c0ba55e21ba648e8da7b76
ms.sourcegitcommit: d1491362421bf2fcf72a81dc2dc2d13d3b98122b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/11/2022
ms.locfileid: "9136833"
---
# <a name="create-commerce-catalogs-for-b2b-sites"></a>Opprett Commerce-kataloger for B2B-områder

[!include [banner](includes/banner.md)]

Denne artikkelen beskriver hvordan du oppretter handelsproduktkataloger for Microsoft Dynamics 365 Commerce-bedrift-til-bedrift-områder (B2B). Hvis du vil ha svar på vanlige spørsmål om handelskataloger for B2B-områder, kan du se [Vanlige spørsmål om handelskataloger for B2B](catalogs-b2b-sites-FAQ.md).

> [!NOTE]
> Denne artikkelen gjelder for Dynamics 365 Commerce, versjon 10.0.27 og nyere utgivelser.

Du kan bruke handelskataloger til å identifisere produktene du vil tilby i B2B-nettbutikkene. Når du oppretter en katalog, identifiserer du nettbutikkene som produktene tilbys i, legger til produktene du vil ta med, og forbedrer produkttilbudene ved å legge til handelsinformasjon om varer. Du kan opprette flere kataloger for hver B2B-nettbutikk, som vist i illustrasjonen nedenfor.

![Forhåndsvisning av Commerce-produktkataloger.](./media/Commerce_Catalogs.png)

Med handelsproduktkataloger kan du definere følgende informasjon:

- **Katalogtype** – Konfigurer verdien som **B2B**. Du kan definere B2B-katalogspesifikke egenskaper, for eksempel et navigasjonshierarki, et kundehierarki og attributtmetadata for katalogen. 
- **Katalogspesifikk navigasjonshierarki** – Organisasjoner kan opprette en atskilt kategoristruktur for den bestemte katalogen.
- **Katalogspesifikke attributtmetadata** – Attributter inneholder detaljer om et produkt. Ved å tildele attributter til en kategori i navigasjonshierarkiet, kan du definere verdier for de attributtene på nivå med produkter som er tildelt den kategorien. Organisasjoner kan deretter utføre disse oppgavene:

    - Definer katalogspesifikke attributtverdier.
    - Kontroller oversikten for attributter på katalognivå.
    - Velg begrensningene som er spesifikke for en enkeltkatalog.

- **Kanaler** – Organisasjoner kan knytte mer enn én B2B-nettkanal til en katalog. Slutt-til-slutt-støtte for kataloger er for øyeblikket bare tilgjengelig for B2B-nettbutikker.
- **Kundehierarkier** – Organisasjoner kan gjøre en bestemt katalog tilgjengelig for valgte B2B-partnere ved å knytte kundehierarkier til denne katalogen.
- **Prisgrupper** – Du kan konfigurere priser og kampanjer som er spesifikke for en angitt katalog. Denne funksjonen er en hovedårsak til å definere en katalog for en B2B-kanal. Ved hjelp av prisgrupper for kataloger kan organisasjoner gjøre produkter tilgjengelige for de tiltenkte B2B-organisasjonene og bruke foretrukne priser og rabatter. B2B-kunder som bestiller fra en konfigurert katalog, kan dra nytte av spesialpriser og kampanjer etter at de har logget seg på et B2B-handelsområde. Du kan konfigurere katalogspesifikke priser ved å velge **Prisgrupper** på fanen **Kataloger** for å koble én eller flere prisgrupper til katalogen. Alle handelsavtaler, prisjusteringsjournaler og avanserte rabatter som er koblet til samme prisgruppe, vil bli brukt når kunder bestiller fra denne katalogen. (Avanserte rabatter omfatter terskelrabatter, kvantumsrabatter og samlerabatter.) Hvis du vil ha mer informasjon om prisgrupper, kan du se [Prisgrupper](price-management.md#price-groups).

> [!NOTE]
> Denne funksjonen er tilgjengelig fra og med Dynamics 365 Commerce-versjon 10.0.27. Hvis du vil konfigurere katalogspesifikke konfigurasjoner, for eksempel navigasjonshierarkiet og kundehierarkiet i Commerce headquarters, går du til arbeidsområdet **Funksjonsstyring** (**Systemadministrasjon \> Arbeidsområder \> Funksjonsstyring**), aktiverer du funksjonen **Aktiver bruk av flere kataloger på detaljhandelskanaler** og deretter kjører du **1110 CDX**-jobben. Når du aktiverer denne funksjonen, blir alle eksisterende kataloger som brukes for salgsstedsbutikker eller et telefonsenter, merket som **Katalogtype = B2C** på **Kataloger**-siden. Bare eksisterende og nye kataloger som er merket som **Katalogtype = B2C**, gjelder for salgsstedsbutikker og et telefonsenter. 

## <a name="b2b-catalog-process-flow"></a>B2B-katalogprosessflyt

Prosessen med å opprette og behandle en katalog har fire generelle trinn. Hvert trinn forklares i detalj i den neste delen.

> [!NOTE]
> Før du fortsetter, må du kontrollere at katalogen er merket som **Katalogtype = B2B**.

1. **[Konfigurasjon](#configure-the-catalog)**

    - Tilknytt navigasjonshierarkiet.
    - Angi tidseffektive datoer og utløpsdatoer hvis de er aktuelle.
    - Legg til og kategoriser produkter.
    - Tilknytt prisgrupper.
    - Tilknytt et kundehierarki som er spesifikk for B2B-organisasjonene. 
    - Tilknytt standard dimensjonsattributtgruppe for presiseringer som størrelse, stil og farge.
    - Angi attributtmetadata.

1. **[Validering](#validate-the-catalog)** – I dette trinnet kjører du valideringsregler som fremtvinger bestemt virkemåte. Her er noen eksempler:

    - Kontroller at det ikke finnes noen uspesifiserte produkter.
    - Pass på at alle varene som er assortert til hver kanal, er tilknyttet en katalog.

1. **[Godkjenning](#approve-the-catalog)**
1. **[Publisering](#publish-the-catalog)**

## <a name="set-up-the-catalog"></a>Definer katalogen

Bruk informasjonen i denne delen til å definere katalogen.

### <a name="configure-the-catalog"></a>Konfigurer katalogen

I Commerce Headquarters går du til **Retail og Commerce \> Kataloger og sortimenter \> Alle kataloger** for å konfigurere katalogen.

Når du oppretter en ny katalog, må du først knytt den til en eller flere kanaler. Bare varer som er knyttet til den valgte kanalen [sortimenter](/dynamics365/unified-operations/retail/assortments), kan brukes når katalogen opprettes. Hvis du vil knytte katalogen til en eller flere kanaler, velger du **Legg til** i hurtigfanen **Handelskanaler** på **Katalogoppsett**-siden. Kontroller at katalogen er merket som **Katalogtype = B2B**.

#### <a name="associate-the-navigation-hierarchy"></a>Tilknytt navigasjonshierarkiet

Hvis du vil legge til produkter i en katalog, må du velge et navigasjonshierarki. Navigasjonshierarkiet støtter kategoristrukturen for katalogen. Du må velge blant navigasjonshierarkier som er tilknyttet kanalene valgt i hurtigfanen **Handelskanaler** på **Katalogoppsett**-siden. Hvis du vil knytte et standard navigasjonshierarki til hver av kanalene, kan du gå til **Retail og Commerce \> Kanaloppsett \> Kanalkategorier og produktattributter**.

#### <a name="specify-time-effective-and-expiration-dates"></a>Angi tidseffektive datoer og utløpsdatoer

Hvis du vil angi tidseffektive datoer og utløpsdatoer for en katalog, velger du toppnoden i kataloghierarkiet for å gå tilbake til hovedkataloghodevisningen. Konfigurer effektive datoer og utløpsdatoer etter behov i hurtigfanen **Generelt**.

#### <a name="add-and-categorize-products"></a>Legg til og kategoriser produkter

For å konfigurere produkter du vil legge til i katalogen går du til **Retail og Commerce \> Kataloger og sortimenter \> Alle kataloger** i Commerce Headquarters. Velg deretter **Legg til produkter** i **Kataloger**-fanen.

Du kan også velge en node i navigasjonshierarkiet. Deretter kan du legge til produkter direkte i en kategori i katalogen.

#### <a name="associate-price-groups"></a>Tilknytt prisgrupper

For å konfigurere produkter du vil legge til i katalogen går du til **Retail og Commerce \> Kataloger og sortimenter \> Alle kataloger** i Commerce Headquarters. Velg deretter **Legg til produkter** i **Kataloger**-fanen. 

Produkter som ble lagt til i en katalog fra rotnoden i navigasjonshierarkiet ved å velge **Legg til produkter** i handlingsruten, arver kategoriene hvis kildenavigasjonshierarkiet også er tilknyttet katalogen. Endringer i kategorier som foretas i kildenavigasjonshierarkiet, gjenspeiles umiddelbart i katalogene. Du må publisere katalogene på nytt for å oppdatere kanalene.

Du kan også velge en node i navigasjonshierarkiet og legge til produkter direkte i en valgt kategori i katalogen. 

Når du legger til produkter, blir alternativet **Inkluder alle varianter automatisk når bare produktstandard er valgt** tilgjengelig. Hvis du vil hindre inkludering av alle varianter, velger du minst én variant for hovedproduktet. 

> [!NOTE]
> Hvis du velger å ta med alle varianter i et stort hovedvalg for produkter, kan du oppleve lengre behandlingstider. Hvis du ønsker store valg, anbefaler vi at du velger **Inkluder alle varianter** i handlingsruten på katalogsiden for å kjøre operasjonen i satsvis modus. Hvis du bare har tatt med hovedproduktet i katalogen, og ikke inkluderte noen varianter, kan det hende at variantvelgeren ikke er tilgjengelig når du navigerer til en produktdetaljerside. 

Hvis du vil konfigurere katalogspesifikke priser, må du koble en eller flere prisgrupper til katalogen. For å knytte prisgrupper til en katalog går du til **Retail og Commerce \> Kataloger og sortimenter \> Alle kataloger** i Commerce Headquarters. Deretter velger du **Prisgrupper** under **Prissetting** i fanen **Kataloger**. Alle handelsavtaler, prisjusteringsjournaler og avanserte rabatter for detaljhandel (terskelrabatter, kvantumsrabatter og samlerabatter) som er koblet til samme prisgruppe, vil bli brukt når kunder bestiller fra katalogen.

Du finner mer informasjon om prisgrupper under [Prisgrupper](price-management.md#price-groups).

> [!NOTE]
> Du kan ikke opprette en ny prisgruppe fra siden **Alle kataloger**. I stedet må du opprette den fra siden **Alle prisgrupper**. Deretter må du knytte den til katalogen på siden **Alle kataloger**.

#### <a name="associate-a-customer-hierarchy"></a>Tilknytt et kundehierarki

For å tilknytte kundehierarkier i Commerce Headquarters går du til **Retail og Commerce \> Kataloger og sortimenter \> Alle kataloger**. Velg deretter **Tilordne hierarkier** under **Kundehierarki** i fanen **Kataloger** for å koble et eller flere kundehierarkier til katalogen.

> [!NOTE]
> Du kan ikke opprette et nytt kundehierarki fra siden **Alle kataloger**. I stedet må du opprette den fra siden **Kundehierarkier**. Deretter må du knytte den til katalogen på siden **Alle kataloger**.

#### <a name="associate-default-dimension-attribute-group-for-refiners-such-as-size-style-and-color"></a>Tilknytt standard dimensjonsattributtgruppe for presiseringer som størrelse, stil og farge

Hvis du vil tilknytte en standard attributtgruppe for dimensjonsattributter, for eksempel størrelse, stil og farge, går du til **Retail og Commerce \> Kataloger og sortimenter \> Alle kataloger**. Deretter velger du **Attributtgrupper** under **Attributter** i fanen **Kataloger**.

#### <a name="set-attribute-metadata"></a>Angi attributtmetadata

For å konfigurere attributtmetadata i Commerce Headquarters går du til **Retail og Commerce \> Kataloger og sortimenter \> Alle kataloger**. Deretter velger du **Angi attributtmetadata** under **Attributter** i fanen **Kataloger**. Hvis du vil velge attributtene som skal vises og kan defineres på nytt, velger du en kategori i det tilknyttede katalogspesifikke navigasjonshierarkiet og velger et attributt under **Katalogproduktattributter**. Velg **Vis attributter i kanal**. Alle attributter som kan vises, er som standard også søkbare. Hvis du vil gjøre at attributtene kan justeres, kan du velge **Kan justeres**.

### <a name="validate-the-catalog"></a>Valider katalogen

Før en ny katalog er tilgjengelig for bruk, må den valideres og publiseres.

Hvis du vil validere en katalog, følger du fremgangsmåten nedenfor.

1. Velg **Valider katalog** for å kjøre en validering under **Valider katalog** i fanen **Kataloger** på **Alle kataloger**-siden. Dette trinnet er obligatorisk. Dette validerer at den nødvendige konfigurasjonen er riktig.
1. Velg **Vis resultater** for å se detaljene for valideringen. Hvis det oppdages feil, må du rette dataene og deretter kjøre validering på nytt helt til den er bestått.

> [!NOTE]
> Hvis **Katalogtype = B2B**, vil valideringen mislykkes hvis du har lagt til salgsstedsbutikker eller et telefonsenter i katalogen. B2B-kataloger kan bare ha B2B-nettbaserte kanaler tilknyttet. Validering vil også mislykkes hvis intet kundehierarki er knyttet til en B2B-katalog. 

### <a name="approve-the-catalog"></a>Godkjenn katalogen

Etter at en katalog valideres, må den godkjennes.

For å starte arbeidsflyten for kataloggodkjenning følger du denne fremgangsmåten.

1. I handlingsruten på siden **Alle kataloger** velger du **Arbeidsflyt \> Send inn**.
1. Gå til **Retail og Commerce \> Headquarters-oppsett \> Handelsarbeidsflyter** for å konfigurere trinnene og godkjente brukere for arbeidsflyten. Arbeidsflyten definerer trinnene som kreves for å få katalogen til en **Godkjent**-status.

### <a name="publish-the-catalog"></a>Publiser katalogen

Når en katalog har statusen **Godkjent**, kan du publisere den ved å velge **Publiser** på **Kataloger**-menyen. Etter at katalogen er i en **Publisert**-tilstand, den kan brukes i ordreregistrering i telefonsenteret og send katalog-prosesser. Du kan publisere en katalog manuelt eller ved hjelp av en satsvis prosess. Gyldighetsdatoen du definerte for katalogen, avgjør når produktene er tilgjengelige i nettbutikken. Utløpsdatoen du definerte, bestemmer når produktene fjernes fra nettbutikken.

> [!NOTE]
> Du kan publisere en katalog som inneholder produkter som har advarsler. Disse produktene vises imidlertid ikke i nettbutikken.

## <a name="additional-resources"></a>Tilleggsressurser

[Påvirkning av handelskataloger for B2B-tilpasninger](catalogs-b2b-sites-dev.md)

[Vanlige spørsmål om handelskataloger for B2B](catalogs-b2b-sites-FAQ.md)

[Katalogvelgermodul](catalog-picker.md)
