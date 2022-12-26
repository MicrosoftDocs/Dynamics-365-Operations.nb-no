---
title: Fransk Intrastat
description: Denne artikkelen inneholder informasjon om Intrastat-deklarering i Frankrike.
author: anasyash
ms.date: 11/30/2022
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: ''
ms.openlocfilehash: 2076649c7fff9f47b9c1fda62a103168b19bb973
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831812"
---
# <a name="french-intrastat"></a>Fransk Intrastat

[!include[banner](../includes/banner.md)]

Firmaer i Frankrike som er registrert for merverdiavgift, og som handler med andre EU-land, må deklarere utveksling av varer og tjenester til og fra Frankrike. The Declaration d'exchanges de biens (erklæring om handel med varer, eller DEB) er en kombinasjon av EU-salgslisten og Intrastat-rapporten. Du må sende inn denne rapporten månedlig for alt salg av varer innenfor EU.

Du kan generere DEB-rapporten i ett av to elektroniske tekstfilformater: SAISUNIC 330- eller INTRACOM-formatet.

Følgende tabell viser feltene som er inkludert i den franske Intrastat-deklareringen i SAISUNIC 330-format. Tabellen angir også rapportnivåene for hvert felt. Et felt kan ha følgende rapportnivåer:

- **4** – Avgiftsdeklarering.
- **1** – Statistisk svar.
- **5** – Statistisk svar på forsendelse og avgiftsdeklarering og samlet utfylling.

| Felt                       | Rapportnivåer |
|-----------------------------|---------------|
| Referanseperiode         | 4, 1, 5       |
| Antall deklarasjoner       | 4, 1, 5       |
| Linjenummer                 | 4, 1, 5       |
| ISO-kode for land (FR)       | 4, 1, 5       |
| Tilleggskode          | 4, 1, 5       |
| Siren-nummer                | 4, 1, 5       |
| Mva-kode for kunde        | 4, 1, 5       |
| Retningskode              | 4, 1, 5       |
| Transaksjonstype            | 4, 1, 5       |
| Forpliktelsesnivå            | 4, 1, 5       |
| Artikkelkode              | 1, 5          |
| Nasjonal NGP                | 1, 5          |
| Kommune (avdeling)         | 1, 5          |
| Transaksjonstype       | 1, 5          |
| Opprinnelsesland      | 1, 5          |
| Opprinnelsesland - import | 1, 5          |
| Endelig mål - eksport | 1, 5          |
| Fakturaverdi               | 4, 1, 5       |
| Statistisk verdi           | 1, 5          |
| Nettovekt                  | 1, 5          |
| Tilleggsenheter            | 1, 5          |
| Transportkode              | 1, 5          |

Følgende tabell viser feltene som er inkludert i den franske Intrastat-deklareringen i INTRACOM-format. Tabellen angir også rapportnivåene for hvert felt. Et felt kan ha følgende rapportnivåer:

- **4** – Avgiftsdeklarering.
- **1** – Statistisk svar.
- **5** – Statistisk svar på forsendelse og avgiftsdeklarering og samlet utfylling.

| Felt                       | Rapportnivåer |
|-----------------------------|---------------|
| Retningskode              | 4, 1, 5       |
| Antall deklarasjoner       | 4, 1, 5       |
| Linjenummer              | 4, 1, 5       |
| Siren                       | 4, 1, 5       |
| Kommune (avdeling)         | 1, 5          |
| Transportkode              | 1, 5          |
| Opprinnelsesland           | 1, 5          |
| Transaksjonstype       | 1, 5          |
| Fakturaverdi               | 4, 1, 5       |
| Leveringsmåter           | 1, 5          |
| Transaksjonstype            | 4, 1, 5       |
| Forpliktelsesnivå            | 4, 1, 5       |
| Artikkelkode              | 1, 5          |
| Nasjonal NGP                | 1, 5          |
| Nettovekt                  | 1, 5          |
| Statistisk verdi           | 1, 5          |
| Tilleggsenheter            | 1, 5          |
| Opprinnelsesland - import | 1, 5          |
| Endelig mål - eksport | 1, 5          |
| Mva-kode for kunde        | 4, 1, 5       |
| Tilleggskode          | 4, 1, 5       |
| Referanseperiode         | 4, 1, 5       |

## <a name="set-up-intrastat"></a>Definere Intrastat

- I [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/Logon/Index), i biblioteket over delt aktiva, laster du ned de nyeste versjonene av følgende ER-konfigurasjoner for Intrastat-erklæringen:

    - Intrastat modell
    - Intrastat-rapport
    - Intrastat-INTRACOM (FR)
    - Intrastat-SAISUNIC (FR)

    Hvis du vil ha mer informasjon, kan du se [Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

### <a name="set-up-vat-ids"></a>Definer mva-ID-er

#### <a name="set-up-vat-codes-for-your-company"></a>Definer mva-koder for selskapet

1. Gå til **Avgift** \> **Oppsett** \> **Merverdiavgift** \> **Numre for avgiftsfritak**.
2. Velg **Ny** i handlingsruten.
3. I feltet **Land/område** velger du **FRA**.
4. I feltet **Avgiftsfritaksnummer** skriver du inn firmaets mva-nummernøkkel.
5. Gå til **Organisasjonsstyring** \> **Organisasjoner** \> **Juridiske enheter**, og velg firmaet ditt.
6. I hurtigfanen **Utenrikshandel og logistikk**, i **Intrastat**-delen, angir du feltene **Eksport av VAT exempt number** og **Import av VAT exempt number** til koden du opprettet i trinn 4..
7. I feltet **Mva-nummer** i hurtigfanen **Avgiftsregistrering** angir du mva-nummeret for firmaet ditt.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>Definer mva-ID-er for handelspartnere

##### <a name="create-a-registration-type-for-the-company-code"></a>Opprett en registreringstype for firmakoden

Du må opprette mva-registreringstyper for alle land eller områder som firmaet gjør forretninger med.

1. Gå til **Organisasjonsstyring** \> **Global adressebok** \> **Registreringstyper** \> **Registreringstyper**.
2. Velg **Ny** i handlingsruten for å opprette en registreringstype for MVA-ID-en.
3. I dialogboksen **Angi detaljer for registreringstypen** skriver du inn et navn på den nye registreringstypen i **Navn**-feltet. Skriv for eksempel inn **mva-ID**.
4. I feltet **Land/område** velger du handelspartnerens land eller område.
5. Velg **Opprett**.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Samsvar registreringstypen med en registreringskategori

1. Gå til **Organisasjonsstyring** \> **Global adressebok** \> **Registreringstyper** \> **Registreringskategorier**.
2. Velg **Ny** i handlingsruten for å opprette en kobling mellom en registreringstype og en registreringskategori.
3. For registreringstypen for mva-ID-en velger du registreringskategorien **Mva-ID**.
4. Gjenta trinn 2 og 3 for de andre registreringstypene du opprettet for landene eller områdene som firmaet gjør forretninger med.

##### <a name="set-up-the-vat-number-of-a-trading-partner"></a>Definer mva-nummeret til en handelspartner

1. Gå til **Kunder** \> **Kunder** \> **Alle kunder**.
2. Velg en kunde i rutenettet.
3. I gruppen **Registrering** i fanen **Kunde** i handlingsruten velger du **Registrerings-ID-er**.
4. Velg **Legg til** for å opprette en registrerings-ID i hurtigfanen **Registrerings-ID**.
5. I feltet **Registreringstype** velger du registreringstypen du opprettet for firmakoden.
6. Angi firmaets mva-nummer i **Registreringsnummer**-feltet.
7. Velg **Lagre** i handlingsruten og lukk siden.

Hvis du vil ha mer informasjon, kan du se [Registrerings-ID-er](emea-registration-ids.md).

### <a name="set-up-foreign-trade-parameters"></a>Angi utenrikshandelsparametere

1. Gå til **Avgift** \> **Oppsett** \> **Utenrikshandel** \> **Utenrikshandelsparametere**.
2. I kategorien **Intrastat**, i hurtigfanen **Elektronisk rapportering** i feltet **Rapportformatkartlegging** velger du **Intrastat INTRACOM (FR)** eller **Intrastat SAISUNIC (FR)**.
3. I feltet **Rapportformatkartlegging** velger du **Intrastat-rapport**.
4. I hurtigfanen **Artikkelkodehierarki** i feltet **Kategorihierarki** velger du **Intrastat**.
5. Velg koden som brukes til overføringer av varer, i **Transaksjonskode**-feltet i kategorien **Generelt**.
6. Velg koden som brukes til retur av varer, i **Kreditnota**-feltet.
7. I **Arbeider**-feltet velger du navnet på kontaktpersonen.
8. I fanen **Kontakt** legger du til informasjon om kontaktpersonen:

    - I **Telefon**-feltet angir du telefonnummeret til kontaktpersonen.
    - I **Faks**-feltet angir du faksnummeret til kontaktpersonen.

9. I fanen **Land-/områdeegenskaper** i feltet **Land/område** viser du alle landene eller områdene som firmaet gjør forretninger med. For hvert land som er en del av EU, velger du **EU** i feltet **Type land/område**, slik at landet vises i Intrastat-rapporten. For Frankrike velger du **Innenlands** i feltet **Land-/områdetype**.

### <a name="set-up-compression-of-intrastat"></a>Definer komprimering av Intrastat

- Gå til **Avgift** \> **Oppsett** \> **Utenrikshandel** \> **Komprimering av Intrastat**, og velg feltene som skal sammenlignes når Intrastat-informasjon summeres. For fransk Intrastat velger du følgende felter:
 
    - Statistikkprosedyre
    - Opprinnelsesland/-område
    - Transport
    - Korrigert melding
    - Land/område
    - Opprinnelsesregion/-mål
    - Retning
    - Land/område for avsender
    - Transaksjonskode
    - Artikkelkode

### <a name="set-up-product-parameters-for-the-intrastat-declaration"></a>Definer produktparametere for Intrastat-deklarering

1. Gå til **Administrering av produktinformasjon** \> **Produkter** \> **Frigitte produkter**.
2. Velg et produkt i rutenettet.
3. Velg artikkelkoden på hurtigfanen **Utenrikshandel** i **Intrastat**-delen i **Artikkel**-feltet. Navnet på artikkelen blir skrevet ut i feltet **Beskrivelse av artikler** i Intrastat-rapporten.
4. I **Opprinnelse**-delen, i feltet **Lang/område**, velger du produktets opprinnelsesland eller -område.
5. Angi produktets vekt i kilogram i **Nettovekt**-feltet på hurtigfanen **Behandle lager**.

### <a name="ngp-codes"></a>NGP-koder

I DEB-rapporten består kodingen av produkter av følgende elementer:

- Den åttesifrede CN8-koden som representerer tariffen og den statistiske nomenklaturen til EU.
- Hvis det er aktuelt, skal den ettsifrede nasjonale artikkelkoden Nomenclature Générale des Produits (NGP) brukes.

I 2022 gjelder NGP bare tre typer produkter:

- Noen produkter fra kuer, får og geiter
- Militært utstyr
- Franske viner

Du må definere NGP-kodene og tilordne dem til relaterte produkter. **NGP-feltet** angis deretter automatisk på siden **Intrastat-journal**.

#### <a name="set-up-an-ngp-code"></a>Definere en NGP-kode

1. Gå til **Avgift** \> **Oppsett** \> **Utenrikshandel** \> **NGP-koder**.
2. Velg **Ny** i handlingsruten.
3. I **NGP**-feltet skriver du inn en ensifret kode.
4. Skriv inn en beskrivelse for koden i feltet **Beskrivelse**.

#### <a name="assign-an-ngp-code-to-a-product"></a>Tilordne en NGP-kode til et produkt

1. Gå til **Administrering av produktinformasjon** \> **Produkter** \> **Frigitte produkter**.
2. Velg et produkt i rutenettet.
3. Velg riktig NGP-kode i hurtigfanen **Utenrikshandel** i **Intrastat**-delen i **NGP**-feltet.

### <a name="set-up-warehouse-parameters-for-the-intrastat-declaration"></a>Definer lagerparametere for Intrastat-deklarering

1. Gå til **Lagerstyring** \> **Oppsett** \> **Lager** \> **Lagre**.
2. Velg et lager, og i hurtigfanen **Adresser** velger du **Legg til** eller **Rediger**.
3. I **Poststed**-feltet dialogboksen velger du poststed for lageret. Delstaten til byen eller provinsen brukes som en region i DEB-rapporten.

### <a name="set-up-the-transport-method"></a>Definer transportmetoden

1. Gå til **Avgift** \> **Oppsett** \> **Utenrikshandel** \> **Transportmetode**.
2. Velg **Ny** i handlingsruten.
3. Angi en unik kode i **Transport**-feltet. Firmaer i Frankrike bruker ensifrede transportkoder.

### <a name="intrastat-journal"></a>Intrastat-journal

Gå til **Avgift** \> **Deklareringer** \> **Utenriks handel** \> **Intrastat** for å administrere transaksjonene som gjelder utenrikshandel med EU-land. Hvis du vil ha mer informasjon, kan du se [Intrastat-oversikt](emea-intrastat.md).

**NGP**-kolonnen er spesifikk for Frankrike og viser NGP-koden for produktet. Hvis NGP-en ikke gjelder et produkt, vises **0** (null). Hvis du vil justere NGP-koden, velger du transaksjonen og deretter den nødvendige NGP-koden i **Generelt**-fanen i **Koder**-delen i **NGP**-feltet.

#### <a name="intrastat-transfer"></a>Intrastat-overføring

I handlingsruten på **Intrastat**-siden kan du velge **Overfør** for å overføre informasjonen om fellesskapshandel automatisk fra salgsordrene, fritekstfakturaer, bestillinger, leverandørfakturaer, leverandørproduktmottak, prosjektfakturaer og overføringsordrer. Bare dokumenter som har et EU-land som destinasjonsland eller målområde (for fordelinger) eller forsendelse (for ankomster) blir overført.

Fordi DEB-rapporten er en kombinasjon av EU-salgslisten og Intrastat-rapporten, omfatter den også *triangulære* transaksjoner, der direkte levering gjøres fra ett EU-land (part A) til et annet EU-land (parti C), og en fransk juridisk enhet (parti B) står midt i den triangulære avtalen.

#### <a name="generate-a-deb-intrastat-report"></a>Generere en DEB-rapport (Intrastat)

1. Gå til **Avgift** \> **Deklareringer** \> **Utenrikshandel** \> **Intrastat**.
2. Velg **Utlevering** \> **Rapport** i handlingsruten.
3. I **Intrastat-rapport**-dialogboksen angir du følgende felt.

    | Felt            | beskrivelse                                                                                                                         |
    |------------------|-------------------------------------------------------------------------------------------------------------------------------------|
    | Fra dato        | Velg startdatoen for rapporten.                                                                                               |
    | Til dags dato          | Velg sluttdatoen for rapporten.                                                                                                 |
    | Generer fil    | Sett dette alternativet til **Ja** for å generere en TXT-fil.                                                                                 |
    | Filnavn        | Angi navnet på TXT-filen for Intrastat-rapporten.                                                                          |
    | Generer rapport  | Sett dette alternativet til **Ja** for å generere en XML-fil.                                                                                |
    | Navn på rapportfil | Angi det obligatoriske navnet.                                                                                                            |
    | Bare rettelser | Sett dette alternativet til **Ja** for bare å rapportere korrigeringer. Sett den til **Nei** for å rapportere både vanlige transaksjoner og rettelser.         |
    | Retning        | Velg **Ankomster** for en rapport om fellesskapsankomster. Velg **Fordelinger** for en rapport om fellesskapsfordelinger. |

4. Velg **OK** for å lukke dialogboksen **Intrastat-rapport**.
5. Velg rapportnivået i **Rapportnivå**-feltet i dialogboksen **Parametere for elektronisk rapportering** på hurtigfanen **Parametere**. Rapportnivået kan være **1 – statistisk svar**, **4 – avgiftsdeklarering** eller **5 – statistisk svar på forsendelse og avgiftsdeklarering**.

## <a name="example"></a>Eksempel

Følgende eksempel viser hvordan du definerer fransk Intrastat og oppretter DEB-rapporten. Den bruker den juridiske enheten **DEMF**.

### <a name="preliminary-setup"></a>Foreløpig oppsett

1. I [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com/Logon/Index), i biblioteket over delt aktiva, laster du ned de nyeste versjonene av følgende ER-konfigurasjoner for formatet i Intrastat-erklæringen:

    - Intrastat modell
    - Intrastat-rapport
    - Intrastat-INTRACOM (FR)

2. Definer et produkthierarki:

    1. Gå til **Behandling av produktinformasjon** \> **Oppsett** \> **Kategorier og attributter** \> **Kategorihierarkier**.
    2. Velg **Intrastat** i rutenettet.
    3. I handlingsruten, i fanen **Kategorihierarki**, i **Oppretthold**-gruppen, velger du **Rediger**.
    4. I handlingsruten velger du **Ny kategorinode**.
    5. I **Navn**-feltet angir du **Autres Libournais**.
    6. I **Kode**-feltet skriver du inn **2204 21 42**.
    7. Velg **Lagre** i handlingsruten.

### <a name="set-up-vat-ids"></a>Definer mva-ID-er

#### <a name="set-up-vat-codes-for-your-company"></a>Definer mva-koder for selskapet

1. Gå til **Avgift** \> **Oppsett** \> **Merverdiavgift** \> **Numre for avgiftsfritak**.
2. Velg **Ny** i handlingsruten.
3. I feltet **Land/område** velger du **FRA**.
4. Velg **MS123456** i feltet **Avgiftsfritaksnummer**.
5. Gå til **Organisasjonsstyring** \> **Organisasjoner** \> **Juridiske enheter** og velg **DEMF**.
6. I hurtigfanen **Utenrikshandel og logistikk**, i **Intrastat**-delen, angir du feltene **Eksport av VAT exempt number** og **Import av VAT exempt number** til koden du opprettet i trinn 4..
7. Angi **123456789** i feltet **Avgiftsregistreringsnummer** i hurtigfanen **Avgiftsregistrering**.

#### <a name="set-up-the-vat-ids-for-trading-partners"></a>Definer mva-ID-er for handelspartnere

##### <a name="create-a-registration-type-for-the-company-code"></a>Opprett en registreringstype for firmakoden

1. Gå til **Organisasjonsstyring** \> **Global adressebok** \> **Registreringstyper** \> **Registreringstyper**.
2. Velg **Ny** i handlingsruten for å opprette en registreringstype for MVA-ID-en.
3. I dialogboksen **Angi detaljer for registreringstypen**, **Navn**-feltet, angir du **Mva-ID**.
4. I feltet **Land/område** velger du **DEU**.
5. Velg **Opprett**.

##### <a name="match-the-registration-type-with-a-registration-category"></a>Samsvar registreringstypen med en registreringskategori

1. Gå til **Organisasjonsstyring** \> **Global adressebok** \> **Registreringstyper** \> **Registreringskategorier**.
2. Velg **Ny** i handlingsruten for å opprette en kobling mellom registreringstypen og registreringskategorien.
3. For registreringstypen **Mva-ID** for **DEU**-landet velger du registreringskategorien **Mva-ID**.

##### <a name="set-up-the-customers-vat-registration-number"></a>Definer kundens mva-registreringsnummer

1. Gå til **Kunder** \> **Kunder** \> **Alle kunder**.
2. Velg **DE-016** i rutenettet.
3. I gruppen **Registrering** i fanen **Kunde** i handlingsruten velger du **Registrerings-ID-er**.
4. Velg **Legg til** for å opprette en registrerings-ID i hurtigfanen **Registrerings-ID**.
5. Velg **Mva-ID** i **Registreringstype**-feltet.
6. Angi **DE9012** i feltet **Registreringsnummer**.
7. Velg **Lagre** i handlingsruten og lukk siden.
8. I hurtigfanen **Faktura og levering**, i **Merverdiavgift**-delen i feltet **Avgiftsfritaksnummer**, velger du **DE9012**.

### <a name="set-up-foreign-trade-parameters"></a>Angi utenrikshandelsparametere

1. Gå til **Avgift** \> **Oppsett** \> **Utenrikshandel** \> **Utenrikshandelsparametere**.
2. I **Intrastat**-fanen i hurtigfanen **Generelt** i **Transaksjonskode**-feltet velger du **11**.
3. I hurtigfanen **Elektronisk rapportering** i feltet **Rapportformatkartlegging** velger du **Intrastat INTRACOM (FR)**.
4. I feltet **Rapportformatkartlegging** velger du **Intrastat-rapport**.
5. I hurtigfanen **Artikkelkodehierarki** i feltet **Kategorihierarki** velger du **Intrastat**.
6. Velg en post i **Arbeider**-feltet.
7. I fanen **Kontakt** i **Telefon**-feltet angir du kontaktens telefonnummer
8. I **Faks**-feltet angir du kontaktens faksnummer.

### <a name="create-ngp-code"></a>Opprett NGP-kode

1. Gå til **Avgift** \> **Oppsett** \> **Utenrikshandel** \> **NGP-koder**.
2. Velg **Ny** i handlingsruten.
3. I feltet **NGP** angir du **8**.
4. If eltet **Beskrivelsesnavn** angir du **NGP 8**.
5. Velg **Lagre** i handlingsruten.

### <a name="set-up-product-information"></a>Definer produktinformasjon

1. Gå til **Administrering av produktinformasjon** \> **Produkter** \> **Frigitte produkter**.
2. Velg **D0001** i rutenettet.
3. På hurtigfanen **Utenrikshandel**, i **Intrastat**-delen, i **NGP**-feltet velger du **8**.
4. I **Artikkel**-feltet velger du **2204 21 42**.
5. I delen **Opprinnelse** i feltet **Land/område**-felt velger du **FRA**.
6. Angi **2** i **Nettovekt**-feltet i hurtigfanen **Behandle lager** i delen **Vektmålinger**.
7. Velg **Lagre** i handlingsruten og lukk siden.
8. Velg **D0003** i rutenettet.
9. Velg **100 200 30** i hurtigfanen **Utenrikshandel** i **Intrastat**-delen i feltet **Artikkel**.
10. I delen **Opprinnelse** i feltet **Land/område**-felt velger du **DEU**.
11. Angi **5** i **Nettovekt**-feltet i hurtigfanen **Behandle lager** i delen **Vektmålinger**.
12. Velg **Lagre** i handlingsruten.

### <a name="set-up-regime-codes"></a>Definer regimekoder

1. Gå til **Avgift** \> **Oppsett** \> **Utenrikshandel** \> **Statstikkprosedyre**.
2. Velg **Ny** i handlingsruten.
3. Angi **21** i **Statistikkprosedyre**-feltet.
4. I **Tekst 1**-feltet angir du **Regimekode 21**.

### <a name="change-the-site-address"></a>Endre områdeadressen

1. Gå til **Lagerstyring** \> **Oppsett** \> **Lager** \> **Steder**.
2. Velg **1** i rutenettet.
3. Velg **Rediger** på hurtigfanen **Adresser**.
4. I dialogboksen **Rediger adresse**, i feltet **Land/område**, velger du **FRA**.
5. Velg **OK**.
6. Gå til **Lagerstyring** \> **Oppsett** \> **Lager** \> **Lagre**, velg et lager, og velg et lager.
7. Velg **Legg til** på hurtigfanen **Adresser**.
8. I dialogboksen **Ny adresse**, i feltet **Land/område**, velger du **FRA**.
9. I feltet **By** velger du **Bordeaux**.
10. Velg **OK** for å lukke dialogboksen.

### <a name="set-up-a-transport-method"></a>Definer en transportmetode

1. Gå til **Avgift** \> **Oppsett** \> **Utenrikshandel** \> **Transportmetode**.
2. Velg **Ny** i handlingsruten.
3. Angi **3** i **Transport**-feltet.
4. I **Beskrivelse**-feltet angir du **Veitransport**.

### <a name="assign-a-transport-mode-to-a-mode-of-delivery"></a>Tildel en transportmodus til en leveringsmåte

1. Gå til **Innkjøp og leverandører** \> **Oppsett** \> **Distribusjon** \> **Leveringsmåter**.
2. Velg **50** i rutenettet.
3. På hurtigfanen **Utenrikshandel**, i **Transport**-feltet, velger du **3**.

### <a name="create-a-sales-order-with-an-eu-customer-that-includes-the-new-product"></a>Opprett en salgsordre med en EU-kunde som inneholder det nye produktet

1. Gå til **Kunder** \> **Ordrer** \> **Alle salgsordrer**.
2. Velg **Ny** i handlingsruten.
3. I dialogboksen **Opprett salgs ordre**, i **Kunde**-delen i feltet **Kundekonto** velger du **DE-016**.
4. I **Adresse**-delen i **Leveringsadresse**-feltet velger du plusstegnet (**+**) for å opprette en adresse
5. I dialogboksen **Ny adresse** i feltet **Navn på beskrivelse** angir du **Tyskland**.
6. I feltet **Land/område** velger du **DEU**.
7. Velg **OK**.
8. I dialogboksen **Opprett salgsordre** velger du **OK**.
9. I hurtigfanen **Salgsordrelinjer** i **Varenummer**-feltet velger du **0001**.
10. I **Utenlandshandel**-fanen i hurtigfanen **Linjedetaljer** i **Statstikkprosedyre**-feltet velger du **21**.
11. I feltet **Opprinnelsesdelstat** velger du **AL**.
12. Velg **Lagre** i handlingsruten.
13. Kontroller at **50** er valgt i fanen **Hode** på hurtigfanen **Levering**, i feltet **Leveringsmåte**.
14. I handlingsruten, på **Faktura**-fanen i **Generer**-gruppen, velger du **Faktura**.
15. I dialogboksen **Postering av faktura** i hurtigfanen **Parametere** i **Parameter**-delen i **Antall**-feltet velger du **Alle**. Velg deretter **OK** for å publisere fakturaen.

### <a name="transfer-the-transaction-to-the-intrastat-journal-and-review-the-result"></a>Overfør transaksjonen til Intrastat-journalen, og gå gjennom resultatet

1. Gå til **Avgift** \> **Deklareringer** \> **Utenrikshandel** \> **Intrastat**.
2. I handlingsruten velger du **Overfør**.
3. I dialogboksen **Intrastat (overføring)** i **Parametere**-delen angir du **Kundefaktura**-alternativet til **Ja**. Velg deretter **OK**.
4. Sorter transaksjoner etter **Dato**-feltet. Den øverste transaksjonen er resultattransaksjonen.

    ![Linjen som representerer salgsordre på Intrastat-siden.](media/intrastat_fr_1.png)

5. Velg transaksjonslinjen, og velg deretter fanen **Generelt** for å vise flere detaljer.

    ![Salgsordredetaljer i fanen Generelt på Intrastat-siden.](media/intrastat_fr_2.png)

6. Velg **Utlevering** \> **Rapport** i handlingsruten.
7. I dialogboksen **Intrastat-rapport** velger du måneden for salgsordren du opprettet, i hurtigfanen **Parametere** i **Dato**-delen.
8. I delen **Eksportalternativer** angir du alternativet **Generer fil** til **Ja**.
9. I **Filnavn**-feltet angir du det obligatoriske navnet.
10. Velg **OK** for å lukke dialogboksen **Intrastat-rapport**.
11. I dialogboksen **Parametere for elektronisk rapport**, på hurtigfanen **Parametere**, i feltet **Rapportnivå** velger du elektronisk rapportparametere velger du **5 – statistisk svar på forsendelse og avgiftsdeklarering** og går gjennom rapporten.

    ![Intrastat Intracom-rapport ved fordelinger.](media/intrastat_fr_3.png)

12. Gå gjennom den genererte Excel-rapporten.

    ![Intrastat-rapport ved fordelinger.](media/intrastat_fr_4.png)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
