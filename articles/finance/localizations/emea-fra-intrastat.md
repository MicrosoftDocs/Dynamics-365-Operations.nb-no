---
title: Fransk Intrastat
description: Dette emnet inneholder informasjon om Intrastat-deklarering i Frankrike.
author: andosip
ms.date: 07/9/2021
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: v-aosipov
ms.search.validFrom: ''
ms.openlocfilehash: a0f418aa18db99088db0b75df41f950e67160e3f
ms.sourcegitcommit: 8fb79920bea14746a71551a4456236a6386bfcea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/12/2021
ms.locfileid: "6538884"
---
# <a name="french-intrastat"></a>Fransk Intrastat

[!include[banner](../includes/banner.md)]

Firmaer i Frankrike som er registrert for merverdiavgift, og som handler med andre EU-land, må deklarere utveksling av varer og tjenester til og fra Frankrike. The Declaration d'exchanges de biens (erklæring om handel med varer, eller DEB) er en kombinasjon av EU-salgslisten og Intrastat-rapporten. Du må sende inn denne rapporten månedlig for alt salg av varer innenfor EU.

Du kan generere DEB-rapporten i ett av to elektroniske tekstfilformater: SAISUNIC 330- eller INTRACOM-formatet.

Følgende tabell viser feltene som er inkludert i den franske Intrastat-deklareringen i SAISUNIC 330-format.

| **Felt**                   | **Rapportnivå**   |              |
|-----------------------------|--------------------|--------------|
|                             | **4 (forenklet)** | **1 (fullstendig)** |
| Referanseperiode         | X                  | X            |
| Antall deklarasjoner       | X                  | X            |
| Linjenummer                 | X                  | X            |
| ISO-kode for land (FR)       | X                  | X            |
| Tilleggskode          | X                  | X            |
| Siren-nummer                | X                  | X            |
| Mva-kode for kunde        | X                  | X            |
| Retningskode              | X                  | X            |
| Transaksjonstype            | X                  | X            |
| Forpliktelsesnivå            | X                  | X            |
| Artikkelkode              |                    | X            |
| Nasjonal NGP                |                    | X            |
| Kommune (avdeling)         |                    | X            |
| Transaksjonstype       |                    | X            |
| Opprinnelsesland      |                    | X            |
| Opprinnelsesland - import |                    | X            |
| Endelig mål - eksport |                    | X            |
| Fakturaverdi               | X                  | X            |
| Statistisk verdi           |                    | X            |
| Nettovekt                  |                    | X            |
| Tilleggsenheter            |                    | X            |
| Transportkode              |                    | X            |

Følgende tabell viser feltene som er inkludert i den franske Intrastat-deklareringen i INTRACOM-format.

| **Felt**                   | **Rapportnivå**   |              |
|-----------------------------|--------------------|--------------|
|                             | **4 (forenklet)** | **1 (fullstendig)** |
| Kode                        | X                  | X            |
| Antall deklarasjoner       | X                  | X            |
| Linjenummer              | X                  | X            |
| Siren                       | X                  | X            |
| Kommune (avdeling)         |                    | X            |
| Transportkode              |                    | X            |
| Opprinnelsesland           |                    | X            |
| Transaksjonstype       |                    | X            |
| Fakturaverdi               | X                  | X            |
| Leveringsmåter           |                    | X            |
| Transaksjonstype            | X                  | X            |
| Forpliktelsesnivå            | X                  | X            |
| Artikkelkode              |                    | X            |
| Nasjonal NGP                |                    | X            |
| Nettovekt                  |                    | X            |
| Statistisk verdi           |                    | X            |
| Tilleggsenheter            |                    | X            |
| Opprinnelsesland - import |                    | X            |
| Endelig mål - eksport |                    | X            |
| Mva-kode for kunde        | X                  | X            |
| Tilleggskode          | X                  | X            |
| Referanseperiode         | X                  | X            |

### <a name="set-up-intrastat"></a>Definere Intrastat

1.  I [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index), i biblioteket over delt aktiva, laster du ned de nyeste versjonene av følgende ER-konfigurasjoner for Intrastat-erklæringen:

-   Intrastat modell

-   Intrastat-rapport

-   Intrastat-INTRACOM (FR)

-   Intrastat-SAISUNIC (FR)

Hvis du vil ha mer informasjon, kan du se [Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services](../../fin-ops-core/dev-itpro/analytics/download-electronic-reporting-configuration-lcs.md).

2.  I Dynamics 365 Finance går du til **Avgift** &gt; **Oppsett** &gt; **Utenrikshandel** &gt; **Utenrikshandelsparametere**, og følger disse trinnene:

    1.  I kategorien **Intrastat**, i hurtigfanen **Elektronisk rapportering** i feltet **Rapportformatkartlegging** velger du **Intrastat INTRACOM (FR)** eller **Intrastat SAISUNIC (FR)**.

    2.  I feltet **Rapportformatkartlegging** velger du **Intrastat-rapport**.

    3.  I hurtigfanen **Artikkelkodehierarki** i feltet **Kategorihierarki** velger du **Intrastat**.

    4.  Velg koden som brukes til overføringer av varer, i **Transaksjonskode**-feltet i kategorien **Generelt**.

    5.  Velg koden som brukes til retur av varer, i **Kreditnota**-feltet.

    6.  I feltet **Forpliktelsesnivå for eksport** angir du detaljnivået for eksportrapporten. Nivået du velger, påvirker linjene som vises i rapporten. Hvis du vil ha mer informasjon, kan du se tabellene i begynnelsen av dette emnet.

3.  Gå til **Organisasjonsstyring** &gt; **Organisasjoner** &gt; **Juridiske enheter**, velg firmaet, og følg denne fremgangsmåten:

    1.  Angi NAF-koden i hurtigfanen **Registreringsnumre** i **NAF-kode**-feltet. Hvis du vil ha mer informasjon, kan du se [FR-00003 NAF-koder og Siret-numre](tasks/fr-00003-naf-codes-siret-numbers.md).

    2.  I hurtigfanen **Utenrikshandel og logistikk**, i **Intrastat**-delen, angir du feltene **Eksport av VAT exempt number** og **Import av VAT exempt number**.

    3.  I feltet **Mva-nummer** i hurtigfanen **Avgiftsregistrering** angir du mva-nummeret for firmaet ditt.

4.  Hvis du vil angi NAF-koder og mva-organisasjonsnumre for kunder, kan du gå til **Kunder** &gt; **Kunder** &gt; **Alle kunder**, og følge disse trinnene:

    1.  Velg en kunde.

    2.  Angi kundens avgiftsfritaksnummer i hurtigfanen **Faktura og levering**, i **Merverdiavgift**-delen i feltet **Avgiftsfritaksnummer**.

    3.  Angi firmaets Siret-nummer i hurtigfanen **Salgsdemografi** i feltet **Fransk Siret**.

    4.  Angi firmaets NAF-kode i **NAF-kode**-feltet.

    5.  Gjenta denne fremgangsmåten for andre kunder.

5.  Hvis du vil angi NAF-koder og mva-organisasjonsnumre for leverandører, kan du gå til **Leverandører** &gt; **Leverandører** &gt; **Alle leverandører**, og følge disse trinnene:

    1.  Velg en leverandør.

    2.  Angi leverandørens avgiftsfritaksnummer i hurtigfanen **Faktura og levering**, i **Merverdiavgift**-delen i feltet **Avgiftsfritaksnummer**.

    3.  Angi firmaets Siret-nummer i hurtigfanen **Innkjøpsdemografi** i feltet **Fransk Siret**.

    4.  Angi firmaets NAF-kode i **NAF-kode**-feltet.

    5.  Gjenta denne fremgangsmåten for andre leverandører.

6.  Gå til **Avgift** &gt; **Oppsett** &gt; **Utenrikshandel** &gt; **Komprimering av Intrastat**, og velg feltene som skal sammenlignes når Intrastat-informasjon summeres. For fransk Intrastat velger du **Statistikkprosedyre**, **Opprinnelsesstat**, **Opprinnelsesland/-område**, **Leveringsbetingelser**, **Transport**, **Korrigering**, **Land/område**, **Opprinnelsesregion/-mål**, **Retning**, **Land/område til avsender**, **Delstat til avsender**, **Delstat**, **Transaksjonskode** og **Artikkel**.

7.  Gå til **Lagerstyring** &gt; **Oppsett** &gt; **Lager** &gt; **Lagre**, velg et lager, og følg denne fremgangsmåten:

    1.  På hurtigfanen **Adresser** velger du **Legg til** eller **Rediger**.

    2.  I **Poststed**-feltet dialogboksen velger du poststed for lageret. Delstaten til byen brukes som en region i DEB-rapporten.

### <a name="ngp-codes"></a>NGP-koder

I DEB-rapporten består kodingen av produkter av følgende elementer:

1.  Den åttesifrede CN8-koden som representerer tariffen og den statistiske nomenklaturen til EU.

2.  Hvis det er aktuelt, skal den ettsifrede nasjonale artikkelkoden Nomenclature Générale des Produits (NGP) brukes.

I 2021 gjelder NGP bare tre typer produkter:

-   Noen produkter fra kuer, får og geiter

-   Militært utstyr

-   Franske viner

Du må definere NGP-kodene og tilordne dem til relaterte produkter. **NGP-feltet** angis deretter automatisk på siden **Intrastat-journal**.

#### <a name="set-up-an-ngp-code"></a>Definere en NGP-kode

1.  Gå til **Avgift** &gt; **Oppsett** &gt; **Utenrikshandel** &gt; **NGP-koder**.

2.  I handlingsruten velger du **Ny** for å opprette en NGP-kode.

3.  I **NGP**-feltet skriver du inn en ensifret kode.

4.  Skriv inn en beskrivelse for koden i feltet **Beskrivelse**.

#### <a name="assign-an-ngp-code-to-a-product"></a>Tilordne en NGP-kode til et produkt

1.  Gå til **Administrering av produktinformasjon** &gt; **Produkter** &gt; **Frigitte produkter**.

2.  Velg et produkt i rutenettet.

3.  Velg riktig NGP-kode i hurtigfanen **Utenrikshandel** i **Intrastat**-delen i **NGP**-feltet.

## <a name="intrastat-journal"></a>Intrastat-journal

Gå til **Avgift** &gt; **Deklareringer** &gt; **Utenriks** **handel** &gt; **Intrastat** for å administrere transaksjonene som gjelder utenrikshandel med EU-land. Hvis du vil ha mer informasjon, kan du se [Intrastat-oversikt](emea-intrastat.md).

**NGP**-kolonnen er spesifikk for Frankrike. Den viser NGP-koden for produktet. Hvis NGP-en ikke gjelder et produkt, vises **0** (null). Du kan justere NGP-koden. Velg transaksjonen, og velg deretter den nødvendige NGP-koden i **Generelt**-fanen i **Koder**-delen i **NGP**-feltet.

### <a name="intrastat-transfer"></a>Intrastat-overføring

I handlingsruten på **Intrastat**-siden kan du velge **Overfør** for å overføre informasjonen om fellesskapshandel automatisk fra salgsordrene, fritekstfakturaer, bestillinger, leverandørfakturaer, leverandørproduktmottak, prosjektfakturaer og overføringsordrer. Bare dokumenter som har et EU-land som destinasjonsland eller målområde (for fordelinger) eller forsendelse (for ankomster) blir overført.

Fordi DEB-rapporten er en kombinasjon av EU-salgslisten og Intrastat-rapporten, omfatter den også *triangulære* transaksjoner, der direkte levering gjøres fra ett EU-land (part A) til et annet EU-land (parti C), og en fransk juridisk enhet (parti B) står midt i den triangulære avtalen.

### <a name="generate-a-deb-intrastat-report"></a>Generere en DEB-rapport (Intrastat)

1.  Gå til **Avgift** &gt; **Deklareringer** &gt; **Utenrikshandel** &gt; **Intrastat**.

2.  Velg **Utlevering** &gt; **Rapport** i handlingsruten.

3.  I **Intrastat-rapport**-dialogboksen angir du følgende felt.

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

## <a name="example"></a>Eksempel

Følgende eksempel viser hvordan du definerer og arbeider med NGP-koder. Den bruker den juridiske enheten **DEMF**.

1.  I [Microsoft Dynamics Lifecycle Services (LCS)](https://lcs.dynamics.com/Logon/Index), i biblioteket over delt aktiva, laster du ned de nyeste versjonene av følgende ER-konfigurasjoner for formatet i Intrastat-erklæringen:

-   Intrastat modell

-   Intrastat-rapport

-   Intrastat-INTRACOM (FR)

2.  Definer en transaksjonskode i Finance:

    1.  Gå til **Avgift** &gt; **Oppsett** &gt; **Utenrikshandel** &gt; **Transaksjonskoder**.

    2.  Velg **Ny** i handlingsruten.

    3.  I **Transaksjonskode**-feltet skriver du inn **11**.

    4.  I **Navn**-feltet angir du **Kjøp eller salg**.

    5.  Velg **Lagre** i handlingsruten.

3.  Definer et produkthierarki:

    1.  Gå til **Behandling av produktinformasjon** &gt; **Oppsett** &gt; **Kategorier og attributter** &gt; **Kategorihierarkier**.

    2.  Velg **Intrastat** i rutenettet. I handlingsruten, i kategorien **Kategorihierarki**, i **Oppretthold**-gruppen, velger du **Rediger**.

    3.  I handlingsruten velger du **Ny kategorinode**.

    4.  I **Navn**-feltet angir du **Autres Libournais**.

    5.  I **Kode**-feltet skriver du inn **2204 21 42**.

    6.  Velg **Lagre** i handlingsruten.

4.  Gå til **Avgift** &gt; **Oppsett** &gt; **Utenrikshandel** &gt; **Utenrikshandelsparametere**, og følg disse trinnene:

    1.  I **Intrastat**-fanen i hurtigfanen **Generelt** i **Transaksjonskode**-feltet velger du **11**.

    2.  I hurtigfanen **Elektronisk rapportering** i feltet **Rapportformatkartlegging** velger du **Intrastat INTRACOM (FR)**.

    3.  I feltet **Rapportformatkartlegging** velger du **Intrastat-rapport**.

    4.  I hurtigfanen **Artikkelkodehierarki** i feltet **Kategorihierarki** velger du **Intrastat**.

5.  Definere en NGP-kode:

    1.  Gå til **Avgift** &gt; **Oppsett** &gt; **Utenrikshandel** &gt; **NGP-koder**.

    2.  Velg **Ny** i handlingsruten.

    3.  I feltet **NGP** angir du **8**.

    4.  If eltet **Beskrivelsesnavn** angir du **NGP 8**.

    5.  Velg **Lagre** i handlingsruten.

6.  Tilordne NGP-koden til et produkt:

    1.  Gå til **Administrering av produktinformasjon** &gt; **Produkter** &gt; **Frigitte produkter**.

    2.  Velg **0001** i rutenettet.

    3.  På hurtigfanen **Utenrikshandel**, i **NGP**-feltet, velger du **8**.

    4.  I **Artikkel**-feltet velger du **2204 21 42**.

    5.  Velg **Lagre** i handlingsruten.

7.  Opprett en salgsordre som inneholder det nye produktet:

    1.  Gå til **Kunder** &gt; **Ordrer** &gt; **Alle salgsordrer**.

    2.  Velg **Ny** i handlingsruten.

    3.  I dialogboksen **Opprett** **salgs** **ordre**, i **Kunde**-delen i feltet **Kunde** **konto** velger du **100001**.

    4.  I **Adresse**-delen i **Leveringsadresse**-feltet velger du plusstegnet (**+**) for å opprette en adresse

    5.  I dialogboksen **Ny adresse** i feltet **Navn på beskrivelse** angir du **Tyskland**.

    6.  I feltet **Land/område** velger du **DEU**.

    7.  Velg **OK**.

    8.  I dialogboksen **Opprett salgsordre** velger du **OK**.

    9.  I hurtigfanen **Salgs** **ordrelinjer** i **Varenummer**-feltet velger du **0001**.

    10. Velg **Lagre** i handlingsruten.

    11. I handlingsruten, på **Faktura**-fanen i **Generer**-gruppen, velger du **Faktura**.

    12. I dialogboksen **Postering av faktura** i hurtigfanen **Parametere** i **Parameter**-delen i **Antall**-feltet velger du **Alle**. Velg deretter **OK** for å publisere fakturaen.

8.  Opprette DEB-rapporten:

    1.  Gå til **Avgift** &gt; **Deklareringer** &gt; **Utenrikshandel** &gt; **Intrastat**:

    2.  I handlingsruten velger du **Overfør**.

    3.  I dialogboksen **Intrastat (overføring)** i **Parametere**-delen angir du **Kundefaktura**-alternativet til **Ja**. Velg deretter **OK**.

    4.  Sorter transaksjoner etter **Dato**-feltet. Den øverste transaksjonen er resultattransaksjonen. **NGP**-feltet angis automatisk.

    5.  Velg **Utlevering** &gt; **Rapport** i handlingsruten.

    6.  I dialogboksen **Intrastat-rapport** velger du måneden for salgsordren du opprettet, i hurtigfanen **Parametere** i **Dato**-delen.

    7.  I delen **Eksportalternativer** angir du alternativet **Generer fil** til **Ja**.

    8.  I **Filnavn**-feltet angir du det obligatoriske navnet.

    9.  Velg **OK**, og se gjennom rapporten.
