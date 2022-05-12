---
title: Tilpasse konfigurasjoner for elektronisk rapportering for å generere et elektronisk dokument
description: Dette emnet beskriver hvordan du tilpasser det Microsoft-leverte formatet for elektronisk rapportering (ER) som brukes til å generere et egendefinert elektronisk dokument.
author: NickSelin
ms.date: 10/21/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERParameters, ERDataModelDesigner, ERModelMappingTable, ERModelMappingDesigner, EROperationDesigner, ERVendorTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom:
- "220314"
- intro-internal
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a7353d7d8149ff1316fbc0adc55b7e1050f443a8
ms.sourcegitcommit: 5f7177b9ab192b5a6554bfc2f285f7cf0b046264
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/30/2022
ms.locfileid: "8661665"
---
# <a name="customize-electronic-reporting-configurations-to-generate-an-electronic-document"></a>Tilpasse konfigurasjoner for elektronisk rapportering for å generere et elektronisk dokument

[!include[banner](../includes/banner.md)]

Med det [elektroniske rapporteringsrammeverket (ER)](general-electronic-reporting.md) kan du laste opp ER- [konfigurasjonene](general-electronic-reporting.md#Configuration) som Microsoft leverer i Microsoft Dynamics 365 Finance-forekomsten. På denne måten kan de Microsoft-leverte konfigurasjonene fungere som en ER-løsningen som brukes til å generere elektroniske kundefakturaer (e-fakturaer). Du kan bruke denne ER-løsningen til å konfigurere din egendefinerte ER-løsning for å få tilgang til egendefinerte databasefelt og generere e-fakturaer som er kompatible med dine spesifikke behov, uten å måtte redigere kildekoden.

## <a name="overview"></a>Oversikt

I dette emnet må du for eksempel angi et føderalt skattenummer som et nytt egendefinert attributt for hver kunde du fakturerer elektronisk. Derfor må du tilpasse strukturen til fakturaen som brukes, ved å legge til en ny vare som må fylles ut av mva-koden i hver e-faktura som genereres.

Fremgangsmåtene i dette emnet forklarer hvordan en bruker i rollen systemansvarlig, utvikler av elektronisk rapportering eller funksjonsrådgiver for elektronisk rapportering kan utføre disse oppgavene i Finance-forekomsten:

- [Konfigurer minimumssettet med ER-parametere som kreves for å begynne å bruke ER-rammeverket](#ConfigureER).
- [Importer de opprinnelige versjonene av standard ER-konfigurasjonene som leveres for å generere e-fakturaer](#ImportERConfigurations1).
- [Konfigurer kundeparameterne for å starte å bruke standard ER-konfigurasjonene](#ConfigureAR1).
- [Konfigurer parameterne for juridisk enhet for å fakturere kunder](#ConfigureLE).
- [Forbered en kundepost for elektronisk fakturering](#ConfigureCustomer1).
- [Legg til, poster og send en kundefaktura ved hjelp av standard ER-konfigurasjonene](#ProcessInvoice1).
- [Legg til et egendefinert databasefelt for å administrere et føderalt skattenummer for kunder](#AddCustomField).
- [Oppdater metadataene for ER å aktivere databaseendringer for ER-utforming av modelltilordning](#RefreshERMetadata).
- [Utform egendefinerte ER-konfigurasjoner for å generere e-fakturaer som inneholder den nye avgiftskoden](#DesignCustomERConfigurations).
- [Konfigurer kundeparameterne for å starte å bruke de egendefinerte ER-konfigurasjonene](#ConfigureAR2).
- [Oppdater en kundepost for elektronisk fakturering](#ConfigureCustomer2).
- [Legg til, poster og send en kundefaktura ved hjelp av de egendefinerte ER-konfigurasjonene](#ProcessInvoice2).
- [Importer de nye versjonene av standard ER-konfigurasjonene som leveres for å generere e-faktura](#ImportERConfigurations2).
- [Ta i bruk endringene i de nye versjonene av standard ER-konfigurasjonene i dine tilpassede ER-konfigurasjoner](#RebaseCustomERConfigurations).
- [Legg til, poster og send en kundefaktura ved hjelp av de nye versjonene av egendefinerte ER-konfigurasjoner](#ProcessInvoice3).

Alle disse prosedyrene kan gjennomføres i firmaet **DEMF**.

## <a name="configure-the-er-framework"></a><a name="ConfigureER"></a>Konfigurere ER-rammeverket

Som en en bruker med rollen funksjonsrådgiver for elektronisk rapportering eller utvikler av elektronisk rapportering, må du konfigurere minimumssettet med ER-parametere. Du kan deretter begynne å bruke ER-rammeverket til å utforme egendefinerte versjoner av standardkonfigurasjonene i ER-løsningen som brukes til å generere e-fakturaer.

### <a name="configure-er-parameters"></a>Konfigurere ER-parametere

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskursplan**, i delen **Relaterte koblinger**, velger du flisen **Parametere for elektronisk rapportering**.
3. På **Parametere for elektronisk rapportering**-siden, i **Generelt**-fanen angi **Aktiver utformingsmodus** til **Ja**.
4. I kategorien **Vedlegg** i **Konfigurasjoner**-feltet velger du **Fil**.
5. I feltene **Jobbarkiv**, **Midlertidig**, **Grunnlinje** og **Annet** velger du **Fil**-typen.

Hvis du vil ha mer informasjon om ER-parametere, kan du se [Konfigurere ER-rammeverket](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a>Aktivere en ER-konfigurasjonsleverandør

Hver ER-konfigurasjon som legges til, er merket som eid av en ER-konfigurasjonsleverandør. ER-konfigurasjonsleverandøren som aktiveres i **Elektronisk rapportering**-arbeidsområdet, brukes til dette formålet. Derfor må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet før du begynner å legge til eller redigere ER-konfigurasjoner.

> [!NOTE]
> Bare eieren av en ER-konfigurasjon kan redigere den. Derfor, før en ER-konfigurasjon kan redigeres, må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet.

#### <a name="review-the-list-of-er-configuration-providers"></a>Se gjennom listen over ER-konfigurasjonsleverandører

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskursplan**, i delen **Relaterte koblinger**, velger du flisen **Konfigurasjonsleverandører**.
3. På **Konfigurasjonsleverandørtabell**-siden har hver leverandørpost et unikt navn og en unik URL-adresse. Se gjennom innholdet på denne siden. Hvis det allerede finnes en post for **Litware, Inc.** (`https://www.litware.com`), hopper du over den neste fremgangsmåten og [legger til en ny ER-konfigurasjonsleverandør](#AddProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="AddProvider"></a>Legg til en ny ER-konfigurasjonsleverandør

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskursplan**, i delen **Relaterte koblinger**, velger du flisen **Konfigurasjonsleverandører**.
3. Velg **Ny** på siden **Konfigurasjonsleverandører**.
4. I **Navn**-feltet angir du **Litware, Inc.**
5. I **Internett-adresse**-feltet angir du `https://www.litware.com`.
6. Velg **Lagre**.

#### <a name="activate-an-er-configuration-provider"></a>Aktivere en ER-konfigurasjonsleverandør

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På **Lokaliseringskursplan**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Litware, Inc.**-flisen og deretter **Angi aktiv**.

Hvis du ha mer informasjon om ER-konfigurasjonsleverandører, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="import-the-initial-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations1"></a>Importer de opprinnelige versjonene av standard ER-konfigurasjoner

Hvis du vil legge til standard ER-konfigurasjoner i den gjeldende Finance-forekomsten, må du importere dem fra ER- [repositoriet](general-electronic-reporting.md#Repository) som ble konfigurert for den forekomsten.

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På **Lokaliseringskursplan**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Microsoft**-flisen og deretter **Repositorier** for å vise listen over repositorier for Microsoft-leverandøren.
3. På **Konfigurasjonsrepositorier**-siden velger du repositoriet for **Global**-typen, og deretter velger du **Åpne**. Hvis du blir spurt om godkjenning for å koble til Regulatory Configuration Service, følger du godkjenningsinstruksjonene.
4. På **Konfigurasjonsrepositorier**-siden går du til konfigurasjonstreet i venstre rute og velger **Peppol-salgsfakura**-formatkonfigurasjonen.
5. Velg versjon **11.2.2** på hurtigfanen **Versjoner**.
6. Velg **Importer** for å laste ned den valgte versjonen fra det globale repositoriet.

![Konfigurasjonsrepositorium-side.](./media/er-quick-start3-import-solution1.png)

> [!TIP]
> Hvis du har problemer med å få tilgang til det [globale repositoriet](er-download-configurations-global-repo.md), kan du [laste ned konfigurasjoner](download-electronic-reporting-configuration-lcs.md) fra Microsoft Dynamics Lifecycle Services (LCS) i stedet.

### <a name="review-the-imported-er-configurations"></a>Se gjennom importerte ER-konfigurasjoner

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskursplan**, i delen **Konfigurasjoner**, velger du flisen **Rapporteringskonfigurasjoner**.
3. På **Konfigurasjoner**-siden utvider du hurtigfanen **Konfigurasjonskomponenter**.
4. Utvid **Fakturamodell** i konfigurasjonstreet i venstre rute, og utvid deretter **UBL-salgsfaktura**.

Legg merke til at i tillegg til det valgte ER-formatet for **Peppol-salgsfaktura**, ble andre ER-konfigurasjoner importert. Fordi nye versjoner av ER-konfigurasjoner stadig publiseres til det globale repositoriet og LCS, for å holde de tilsvarende løsningene kompatible med nye krav, ble de nyeste versjonene av den nødvendige datamodell-konfigurasjonen og de tilhørende modelltilordning-konfigurasjonene importert.

![Siden Konfigurasjoner.](./media/er-quick-start3-imported-solution1a.png)

Følg fremgangsmåten nedenfor for å simulere tilstanden som ER-konfigurasjoner i gjeldende Finance-forekomst vil være hvis du har importert versjon **11.2.2** til ER-formatet **Peppol-salgsfaktura** tidligere (for eksempel 7. august 2019).

- Velg **Slett** i handlingsruten for å slette alle ER-konfigurasjonene som ble publisert etter 7. august 2019. Den eneste konfigurasjonene **Fakturamodell**, **Fakturamodelltilordning** (først kalt **Modelltilordning for kundefaktura**), **UBL-salgsfaktura** og **Peppol-salgsfaktura** må beholdes.
- I hurtigfanen **Versjoner** velger du **Slett** for de gjenstående ER-konfigurasjonene for å slette alle versjoner av ER-konfigurasjoner som ble publisert etter 7. august, 2019.

Kontroller deretter at følgende konfigurasjoner er tilgjengelige i konfigurasjonstreet:

- **Fakturamodell**-ER-datamodellkonfigurasjon (opprinnelig kalt **Kundefakturamodell**):

    - Versjon 11 inneholder versjon 10 av datamodell ER-komponenten som representerer datastrukturen i fakturaens forretningsdomene. Denne ER-konfigurasjonen er importert som en overordnet til **Peppol salgsfaktura** ER-formatet som ble valgt for import.
    - Versjon 50 inneholder versjon 31 av datamodell ER-komponenten. Denne ER-konfigurasjonen er importert som en overordnet av 7. august 2019-versjonen av **Fakturamodelltilordning** ER- modelltilordingskonfigurasjonen.

    ![ER-modelltilordningskonfigurasjon på konfigurasjonssiden.](./media/er-quick-start3-imported-solution1b1.png)

    > [!TIP]
    > Hvis du ikke ser versjon 50 av denne datamodellen, åpner du det globale repositoriet og importerer versjon 50.19 av ER-konfigurasjonen **Fakturamodelltilordning**.

- **Fakturamodelltilordning** ER-modelltilordningskonfigurasjon (opprinnelig kalt **Modelltilordning for kundefaktura**):

    - Versjon 50.19 er importert som siste implementering av versjon 50 av ER-datamodellkonfigurasjonen **Fakturamodell**. Den inneholder to modelltilordning ER-komponenter som beskriver hvordan datamodellen fylles ut med programdata ved kjøring.

    ![ER-modelltilordningskonfigurasjon Fakturamodelltilordning på konfigurasjonssiden.](./media/er-quick-start3-imported-solution1b2.png)

    > [!TIP]
    > Hvis du ikke ser versjon 50.19 av denne modelltilordningen, åpner du det globale repositoriet og importerer versjon 50.19 av ER-konfigurasjonen **Fakturamodelltilordning**.

- **UBL-salgsfaktura** ER-formatkonfigurasjon:

    - Versjon 11.2 inneholder format og formattilordning ER-komponenter. Formatkomponenten angir rapportoppsettet. Formattilordningskomponenten inneholder modelldatakilden og angir hvordan denne datakilden brukes til å rapportoppsettet fylles ut under kjøring. Dette ER-formatet ble konfigurert til å generere e-fakturaer i Universal Business Language (UBL)-format. Den er importert som en overordnet til **Peppol salgsfaktura** ER-formatet som ble valgt for import.

- **Peppol-salgsfaktura** ER-formatkonfigurasjon:

    - Versjon 11.2.2 inneholder format- og formattilordnings ER-komponenter som ble konfigurert til å generere e-fakturaer i Pan-European Public Procurement OnLine (PEPPOL)-format.

    ![ER-formatkonfigurasjon for Peppol-salgsmodell på konfigurasjonssiden.](./media/er-quick-start3-imported-solution1b3.png)

## <a name="configure-the-accounts-receivable-parameters"></a><a name="ConfigureAR1"></a>Konfigurere kundeparameterne

1. Gå til **Kunder** \> **Oppsett** \> **Kundeparametere**.
2. I kategorien **Elektroniske dokumenter** i hurtigfanen **Elektronisk rapportering** i feltet **Salgs- og fritekstfaktura** velger du **Peppol-salgsfaktura**.
3. Velg **Lagre**.

![Kategorien Elektroniske dokumenter på kundeparametere-siden.](./media/er-quick-start3-configure-ar1.png)

## <a name="configure-the-legal-entity-parameters"></a><a name="ConfigureLE"></a>Konfigurere parameterne for juridisk enhet

1. Gå til **Organisasjonsstyring** \> **Organisasjoner** \> **Juridiske enheter**.
2. For det velgte **DEMF**-selskapet, i hurtigfanen **Bankkontoinformasjon** i feltet **Rutingsnummer**, angir du **1234**.
3. Velg **Lagre**.
4. Lukk skjemaet **Juridiske enheter**.

## <a name="prepare-a-customer-record"></a><a name="ConfigureCustomer1"></a>Opprett en kundepost

1. Gå til **Kunder** \> **Kunder** \> **Alle kunder**.
2. På **Alle kunder**-siden velger du kundekontokoblingen **DE-014**.

### <a name="add-a-customer-contact"></a>Legg til en kundekontakt

1. Gå til **Kunder** \> **Kunder** \> **Alle kunder**.
2. I handlingsruten i kategorien **Kunde** i gruppen **Kontoer** velger du **Kontakter**.
3. Velg **Legg til kontakter**.
4. På **Kontakter**-siden i **Fornavn**-feltet åpner du oppslaget, velger **Adam Carter**, og deretter **Velg** for å lukke oppslaget.
5. Velg **Lagre**.
6. Lukk **Kontakter**-siden.

### <a name="define-a-primary-contact"></a>Definere en primær kontakt

1. Gå til **Kunder** \> **Kunder** \> **Alle kunder**.
2. I hurtigfanen **Salgsdemografi** i feltet **Hovedkontakt** velger du **Adam Carter**.

### <a name="set-the-e-invoicing-option"></a>Angi alternativet for e-fakturering

1. Gå til **Kunder** \> **Kunder** \> **Alle kunder**.
2. I hurtigfanen **Faktura og levering** setter du **eFaktura**-alternativet til **Ja**.
3. Velg **Lagre**.
4. Lukk siden **Alle kunder**.

## <a name="process-a-customer-invoice-by-using-the-standard-er-configurations"></a><a name="ProcessInvoice1"></a>Behandle en kundefaktura ved hjelp av standard ER-konfigurasjonene

Du kan nå bruke standard ER-konfigurasjonene du importerte, til å sende en fritekstfaktura til en kunde elektronisk.

### <a name="add-a-new-invoice"></a>Legg til ny faktura

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. Velg **Ny** på siden **Fritekstfaktura**.
3. I hurtigfanen **Fakturahode i fritekst** i feltet **Kundekonto** velger du **DE-014**.
4. På hurtigfanen **Fakturalinjer** legges det automatisk til en fakturalinje. På denne linjen angir du følgende felt:

    - I **Beskrivelse**-feltet angir du **Notatblokk**.
    - Velg **401100** i feltet **Hovedkonto**.
    - Angi **1000** i **Enhetspris**-feltet.

5. Velg **Lagre**.

![Siden Fritekstfaktura.](./media/er-quick-start3-add-invoice.png)

Hvis du vil ha mer informasjon, kan du se [Opprette en fritekstfaktura](../../../finance/accounts-receivable/create-free-text-invoice-new.md).

### <a name="post-a-new-invoice"></a>Postere ny faktura

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. På siden **Fritekstfaktura** i handlingsruten velger du **Poster**.
3. I dialogboksen **Poster fritekstfaktura** velger du **OK**.

![Siden Detaljer for fritekstfaktura.](./media/er-quick-start3-post-invoice.png)

### <a name="send-a-posted-invoice"></a>Sende en postert faktura

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. På siden **Fritekstfaktura** i handlingsruten i **Dokument**-gruppen velger du **Send** \> **Opprinnelig**.

    ![Forhåndsvisning av den opprinnelige fakturaen.](./media/er-quick-start3-send-invoice.png)

3. Lukk siden **Fritekstfaktura**.

### <a name="analyze-a-generated-e-invoice"></a>Analysere en generert e-faktura

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Elektroniske rapporteringsjobber**.
2. På siden **Elektroniske rapporteringsjobber** velger du den opprinnelige posten som har oppgavebeskrivelsen **Send eFaktura-XML**.
3. Velg **Vis filer** for å få tilgang til listen over genererte filer.

    ![Siden Elektroniske rapporteringsjobber.](./media/er-quick-start3-jobs-list.png)

4. Velg **Åpne** for å laste ned e-faktura-XML-filen som genereres.
5. Analyser XML-filen for e-faktura. Legg merke til at kundeavgiftsskjemaet for øyeblikket er representert av **schemeID** og **schemeAgencyID**-XML-attributtene. Legg også merke til at **cbc:CustomizationID** XML-elementet inneholder følgende tekst: `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0`.

    ![Forhåndsvisning av den genererte XML-filen for e-faktura.](./media/er-quick-start3-e-invoice1.png)

## <a name="add-a-custom-database-field"></a><a name="AddCustomField"></a>Legge til et egendefinert databasefelt

Du kan bruke funksjonen [Egendefinert felt](../../fin-ops/get-started/user-defined-fields.md) til å gjøre følgende tilpasning i gjeldende Finance-forekomst:

- Tilpass databasestrukturen ved å legge til et nytt egendefinert databasefelt som lagrer et føderalt skattenummer for hver kunde.
- Tilpass **Kunde**-siden ved å legge til et nytt dataregistreringsfelt som kan brukes til å angi en mva-kode i det nye egendefinerte databasefeltet.

Følg denne fremgangsmåten for å utføre tilpassingen.

1. Gå til **Kunder** \> **Kunder** \> **Alle kunder**.
2. På **Alle kunder**-siden velger du kundekontokoblingen **DE-014**.
3. I hurtigfanen **Generelt** høyreklikker du i et tomt område i **Språk**-feltet, og deretter velger du **Tilpass: UpperGroup**.

    Innholdet i hurtigfanen **Generelt** utheves, og en **Tilpass**-meny vises.

4. Velg **Legg til et felt** på **Tilpass**-menyen.
5. Velg **Opprett nytt felt** i dialogboksen **Legg til kolonner**.
6. I dialogboksen **Opprett nytt felt** i feltet **Tabellnavn** velger du **Kunder**.
7. I **Navneprefiks**-feltet angir du **FederalTaxID**.

    > [!NOTE]
    > Hele feltnavnet er automatisk definert som **FederalTaxID\_Custom**.

8. I feltet **Etikett** angir du **Federal Tax ID**.
9. I feltet **Type** velger du **Tekst**.
10. Angi **20** i feltet **Lengde**.
11. Velg **Lagre**.
12. I meldingsboksen som vises, velger du **Ja** for å bekrefte at du vil opprette en ny **FederalTaxID**-feltoppføring for **Kunder**-tabellen.
13. Velg **Sett inn** for å <a name="insert_custom_field"></a>legge til feltet **FederalTaxID\_Custom** på gjeldende side.

    ![Alle kunder-siden.](./media/er-quick-start3-create-new-field.gif)

14. Lukk siden **Alle kunder**.

## <a name="refresh-the-er-metadata"></a><a name="RefreshERMetadata"></a>Oppdatere ER-metadata

Du må oppdatere metadataene for ER for å gjøre det egendefinerte feltet som du la til, [synlig](electronic-reporting-er-configure-parameters.md#frequently-asked-questions) i ER-modelltilordningsutformingen.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Bygg tabellreferanser på nytt**.
2. Velg **OK** i dialogboksen **Oppdater datamodell**.

## <a name="design-the-custom-er-configurations"></a><a name="DesignCustomERConfigurations"></a>Utforme de tilpassede ER-konfigurasjonene

Du kan bruke de Microsoft-oppgitte ER-konfigurasjonene til å utforme dine egendefinerte ER-konfigurasjoner, slik at de genererer e-fakturaer som inneholder den nye avgiftskoden.

### <a name="customize-the-data-model-configuration"></a>Tilpasse datamodellkonfigurasjonen

Som en bruker i rollen som funksjonsrådgiver for elektronisk rapportering, kan du utforme din egen ER-datamodell.

#### <a name="add-a-custom-data-model-configuration"></a>Legg til en tilpasset datamodellkonfigurasjon

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, velger du **Kundefakturamodell**.
3. Velg **Opprett konfigurasjon** i handlingsruten.
4. I rullegardinboksen i **Ny**-feltet velger du **Avled fra navnet: Kundefakturamodell, Microsoft** for å angi at den nye egendefinerte ER-datamodellkonfigurasjonen skal være basert på ER-datamodellkonfigurasjonen.
5. I feltet **Navn** angir du **Fakturamodell (Litware)**.
6. Velg **Opprett konfigurasjon** for å legge til den nye ER-konfigurasjonen.

Nå kan du bruke ER-datamodellutformingen til å redigere versjon 50.1 av ER-konfigurasjonen **Fakturamodell (Litware)** i **Utkast** [status](general-electronic-reporting.md#component-versioning).

![Versjon 50.1 av ER-konfigurasjonen på Konfigurasjoner-siden.](./media/er-quick-start3-added-custom-model.png)

#### <a name="configure-a-custom-data-model"></a>Konfigurere en tilpasset datamodell

Du må endre den egendefinerte datamodellen ved å legge til et nytt felt for å angi verdien til et føderalt skattenummer. Denne koden er en del av kundedataene for alle ER-formater som vil bruke denne datamodellen som en datakilde.

1. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, velger du **Fakturamodell (Litware)**.
2. I **Versjoner**-hurtigkategorien velger du versjon **50.1** for den valgte ER-datamodellkonfigurasjonen i **Utkast** status.
3. Velg **Utforming** for den valgte konfigurasjonsversjonen i handlingsruten.
4. På siden **Datamodellutforming** i datamodelltreet velger du **Kundeinformasjon (kunde)**.
5. Velg **Ny**.
6. I rullegardinboksen i feltet **Ny node som en** godtar du standardverdien, **Underordnet for en aktiv node**.
7. I **Navn**-feltet angir du **FederalTaxID\_Litware**.
8. I **Varetype**-feltet godtar du standardverdien, **Streng**.
9. Velg **Legg til**, og velg deretter **Lagre**.

    ![Siden Datamodellutforming.](./media/er-quick-start3-add-data-model-field.png)

    > [!NOTE]
    > Feltene **Etikett** og **Beskrivelse** beskriver formålet med det nye feltet. Du kan fylle ut disse feltene på flere språk. Hvis du vil ha mer informasjon, se [Utforme flerspråklige rapporter i elektronisk rapportering](er-design-multilingual-reports.md).

10. Lukk siden **Datamodellutforming**.

#### <a name="complete-a-custom-data-model-configuration"></a>Fullføre en tilpasset datamodellkonfigurasjon

Du må [fullføre](general-electronic-reporting.md#component-versioning) arbeidet med versjon 50.1 av din tilpassede ER-datamodellkonfigurasjon for å gjøre den tilgjengelig, slik at andre tilpassede ER-konfigurasjoner kan legges til.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Fakturamodell** og velger **Fakturamodell (Litware)**.
3. I **Versjon**-hurtigfanen velger du **Endre status** \> **Fullført**, og deretter velger du **OK**.

Statusen for versjon 50.1 endres fra **Utkast** til **Fullført**, og versjonen blir skrivebeskyttet. En ny redigerbar versjon, 50.2, har blitt lagt til og har statusen **Utkast**. Du kan bruke denne versjonen til å gjøre ytterligere endringer i ER-datamodellkonfigurasjonen.

![Versjon 50.1 fullført på konfigurasjonssiden.](./media/er-quick-start3-completed-custom-model1.png)

### <a name="customize-the-model-mapping-configuration"></a>Tilpasse modelltilordningskonfigurasjonen

Som en bruker i rollen som utvikler av elektronisk rapportering, kan du utforme din egen ER-modelltilordning.

#### <a name="add-a-custom-model-mapping-configuration"></a>Legg til en tilpasset modelltilordningskonfigurasjon

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Kundefakturamodell** og velger **Modelltilordning for kundefaktura**.
3. Velg **Opprett konfigurasjon** i handlingsruten.
4. I rullegardinboksen i **Ny**-feltet velger du **Avled fra navnet: Modelltilordning for kundefaktura, Microsoft** for å angi at den nye egendefinerte ER-modelltilordningskonfigurasjonen skal være basert på ER-modelltilordningskonfigurasjonen.
5. I feltet **Navn** angir du **Fakturamodelltilordning (Litware)**.
6. I **Målmodell**-feltet velger du **Fakturamodell (Litware)**.

    > [!IMPORTANT]
    > Dette trinnet er svært viktig. Hvis du utelater det, kan du ikke bruke den egendefinerte datamodellen i den konfigurerte modelltilordningen.

7. Velg **Opprett konfigurasjon** for å legge til den nye ER-konfigurasjonen.

![Legge til en tilpasset modelltilordningskonfigurasjon på konfigurasjonssiden.](./media/er-quick-start3-adding-custom-mapping.png)

#### <a name="configure-a-custom-model-mapping"></a>Konfigurere en tilpasset modelltilordning

Du må endre den egendefinerte modelltilordningen og angi hvordan det egendefinerte **FederalTaxID\_Litware**-feltet for den egendefinerte datamodellen skal fylles ut med programdata ved kjøring.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Kundefakturamodell** \> **Modelltilordning for kundefaktura**, og velger **Fakturamodelltilordning (Litware)**.
3. Velg **Utforming** i handlingsruten.
4. På siden **Tilordning av modell til datakilde** velger du **Kundefaktura**-tilordningen.

    ![Siden Tilordning av modell til datakilde.](./media/er-quick-start3-select-customer-mapping.png)

5. Velg **Utforming**.
6. På siden **Modelltilordningsutforming** i **Datakilder**-ruten utvider du **CustInvoiceJour**-datakilden som representerer **CustInvoiceJour**-programtabellen.
7. Under **CustInvoiceJour** utvider du **Relasjoner** for å se gjennom listen over relasjoner mellom mange-til-én-typen (N:1) for **CustInvoiceJour**-tabellen.
8. Under **CustInvoiceJour** \> **Relasjoner** utvider du **Kunder (CustTable)** for å få tilgang til feltene og relasjonene i tabellen **Kunder (CustTable)**.
9. Velg datakildefeltet **FederalTaxID\_Custom** som du implementerte [tidligere](#insert_custom_field).
10. I **Datamodell**-ruten utvider du **Kundeinformasjon (kunde)**, og velger **FederalTaxID\_Litware**-datamodellfeltet.
11. Velg **Bind**.

    ![Modellkartleggingsutforming-siden.](./media/er-quick-start3-customize-model-mapping.gif)

12. Velg **Lagre**.
13. Lukk siden **Modelltilordningsutforming**.
14. Lukk siden **Tilordning av modell til datakilde**.

#### <a name="complete-a-custom-model-mapping-configuration"></a>Fullføre en tilpasset modelltilordningskonfigurasjon

Du må [fullføre](general-electronic-reporting.md#component-versioning) arbeidet med versjon 50.19.1 av den tilpassede ER-modelltilordningskonfigurasjon for å gjøre den tilgjengelig for bruk.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Kundefakturamodell** \> **Modelltilordning for kundefaktura**, og velger **Fakturamodelltilordning (Litware)**.
3. I **Versjon**-hurtigfanen velger du **Endre status** \> **Fullført**, og deretter velger du **OK**.

Statusen for versjon 50.19.1 endres fra **Utkast** til **Fullført**, og versjonen blir skrivebeskyttet. En ny redigerbar versjon, 50.19.2, har blitt lagt til og har statusen **Utkast**. Du kan bruke denne versjonen til å gjøre ytterligere endringer i ER-modelltilordningskonfigurasjonen.

![Versjon 50.19.1 fullført på konfigurasjonssiden.](./media/er-quick-start3-completed-custom-mapping1.png)

> [!NOTE]
> Den støttede [livssyklus](general-electronic-reporting-manage-configuration-lifecycle.md) for konfigurasjon dekker ikke livssyklusen for databaseendringer. Hvis du eksporterer versjon 50.19.1 av konfigurasjonen **Fakturamodelltilordning (Litware)** fra gjeldende Finance-forekomst og prøver å importere den til en annen forekomst som ikke inneholder det egendefinerte **FederalTaxID\_Custom**-feltet i **CustTable**-tabellen, vil det oppstå et unntak. Unntaket vil føre til at den importerte ER-konfigurasjonen ikke er kompatibel med metadataene for mål-Finance-forekomsten.

### <a name="customize-the-format-configuration"></a>Tilpasse formatkonfigurasjonen

Som en bruker i rollen som funksjonsrådgiver for elektronisk rapportering, kan du utforme det tilpassede ER-formatet.

#### <a name="add-a-custom-format-configuration"></a>Legge til en tilpasset formatkonfigurasjon

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Kundefakturamodell** \> **UBL-salgsfaktura**, og velger **Peppol-salgsfaktura**.
3. Velg **Opprett konfigurasjon** i handlingsruten.
4. I rullegardinboksen i **Ny**-feltet velger du **Avled fra navnet: Peppol-salgsfaktura, Microsoft** for å angi at den nye egendefinerte ER-formatfigurasjonen skal være basert på ER-formatfigurasjonen.
5. I feltet **Navn** angir du **Peppol-salgsfaktura (Litware)**.
6. I **Datamodell**-feltet velger du **Fakturamodell (Litware)** for å bruke de tilpassede datamodell- og modelltilordningskomponentene.

    > [!NOTE]
    > Dette trinnet er svært viktig. Hvis du utelater det, kan du ikke bruke den egendefinerte datamodellen i det konfigurerte formatet.

7. I feltet **Datamodell** velger du **InvoiceCustomer**-rotdefinisjonen.
8. Velg **Opprett konfigurasjon** for å legge til den nye ER-konfigurasjonen.

![Legge til en tilpasset formatkonfigurasjon på konfigurasjonssiden.](./media/er-quick-start3-adding-custom-format.png)

Nå kan du bruke ER-operasjonsutformingen til å redigere versjon 11.2.2.1 av ER-konfigurasjonen **Peppol-salgsfaktura (Litware)** i **Utkast** [status](general-electronic-reporting.md#component-versioning).

![Versjon 11.2.2.1 av ER-konfigurasjonen på Konfigurasjoner-siden.](./media/er-quick-start3-added-custom-format.png)

#### <a name="configure-a-custom-format"></a>Konfigurere et tilpasset format

Du må endre det egendefinerte formatet ved å legge til et nytt format-element for å fylle ut verdien til en fakturert kundes føderale skattenummer.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Kundefakturamodell** \> **UBL-salgsfaktura** \> **Peppol-salgsfaktura**, og velger **Peppol-salgsfaktura (Litware)**.
3. Velg **Utforming** i handlingsruten.
4. I formattreet utvider du **XMLHeader** \> **Faktura** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme**, og velger **cbc:ID**.
5. Velg **Legg til,**, og velg deretter **XML** \> **Attributt**.
6. I dialogboksen **Komponentegenskap** i **Navn**-feltet skriver du inn **FederalTaxID**.
7. Velg **OK** for å legge til et nytt formatelement for å opprette et nytt **FederalTaxID** XML-attributt i en generert XML-fil.
8. I formattreet under **XMLHeader** \> **Faktura** \> **cac:AccountingCustomerParty** \> **cac:Party** \> **cac:PartyTaxScheme** \> **cac:TaxScheme** \> **cbc:ID** velger du **FederalTaxID**.
9. Velg **Flytt opp**.

![Nytt formatelement på Formatutforming-siden.](./media/er-quick-start3-customized-format.png)

#### <a name="configure-a-custom-format-mapping"></a>Konfigurere en tilpasset formattilordning

1. På siden **Formatutforming** i kategorien **Tilordning** utvider du **Faktura**-datakilden for **Modell**-typen.
2. Under **Faktura** utvider du **Kundeinformasjon (kunde)**, og velger **FederalTaxID\_Litware**.
3. Velg **Bind**.

    ![Formatutformingsside.](./media/er-quick-start3-customized-format-mapping.png)

4. Velg **Faktura**-datakilden for **Modell**-typen, og velg deretter **Rediger**.
5. I **Versjon**-feltet velger du versjon **1** av den egen definerte datamodellen, og deretter velger du **OK**.
6. Velg **Lagre**.
7. Lukk **Formatutforming**-siden.

#### <a name="complete-a-custom-format-configuration"></a>Fullføre en tilpasset formatkonfigurasjon

Du må [fullføre](general-electronic-reporting.md#component-versioning) arbeidet med versjon 11.2.2.1 av den tilpassede ER-formatkonfigurasjon for å gjøre den tilgjengelig for bruk.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Kundefakturamodell** \> **UBL-salgsfaktura** \> **Peppol-salgsfaktura**, og velger **Peppol-salgsfaktura (Litware)**.
3. I **Versjon**-hurtigfanen velger du **Endre status** \> **Fullført**, og deretter velger du **OK**.

Statusen for versjon 11.2.2.1 endres fra **Utkast** til **Fullført**, og versjonen blir skrivebeskyttet. En ny redigerbar versjon, 11.2.2.2, har blitt lagt til og har statusen **Utkast**. Du kan bruke denne versjonen til å gjøre ytterligere endringer i den egendefinerte ER-formatkonfigurasjonen.

![Versjon 11.2.2.1 fullført på konfigurasjonssiden.](./media/er-quick-start3-completed-custom-format1.png)

## <a name="configure-the-accounts-receivable-parameters-to-start-to-use-custom-er-configurations"></a><a name="ConfigureAR2"></a>Konfigurere kundeparameterne for å starte å bruke de egendefinerte ER-konfigurasjonene

1. Gå til **Kunder** \> **Oppsett** \> **Kundeparametere**.
2. I kategorien **Elektroniske dokumenter** i hurtigfanen **Elektronisk rapportering** i feltet **Salgs- og fritekstfaktura** velger du **Peppol-salgsfaktura (Litware)**.
3. Velg **Lagre**.

![Siden Kundeparametere, kategorien Elektroniske dokumenter, hurtigfanen Elektronisk rapportering.](./media/er-quick-start3-configure-ar2.png)

## <a name="update-a-customer-record-by-adding-a-federal-tax-identification-code"></a><a name="ConfigureCustomer2"></a>Oppdatere en kundepost ved å legge til et føderalt skattenummer

1. Gå til **Kunder** \> **Kunder** \> **Alle kunder**.
2. På **Alle kunder**-siden velger du kundekontokoblingen **DE-014**.
3. I **Generelt**-hurtigfanen i feltet **Federal Tax ID** angir du **LITWARE-6789**.
4. Velg **Lagre**.

    ![DE-014-kundedetaljerside.](./media/er-quick-start3-added-tax-id-value.png)

5. Lukk siden **Alle kunder**.

## <a name="process-a-customer-invoice-by-using-custom-er-configurations"></a><a name="ProcessInvoice2"></a>Behandle en kundefaktura ved hjelp av tilpassede ER-konfigurasjoner

### <a name="select-and-send-a-posted-invoice"></a>Velge og sende en postert faktura

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. På siden **Fritekstfaktura** velger du fakturaen du har lagt til og postert tidligere.
3. I handlingsruten i **Dokument**-gruppen velger du **Send** \> **Opprinnelig**.
4. Lukk siden **Fritekstfaktura**.

### <a name="analyze-a-generated-e-invoice"></a>Analysere en generert e-faktura

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Elektroniske rapporteringsjobber**.
2. På siden **Elektroniske rapporteringsjobber** velger du den siste posten som har oppgavebeskrivelsen **Send eFaktura-XML**.
3. Velg **Vis filer** for å få tilgang til listen over genererte filer.
4. Velg **Åpne** for å laste ned e-faktura-XML-filen som genereres.
5. Analyser XML-filen for e-faktura. Legg merke til at i samsvar med tilpassingen, inkluderer kundeavgiftsskjemaet det egendefinerte **FederalTaxID** XML-attributtet i tillegg til **schemeID** og **schemeAgencyID** XML-attributtene. Verdien til dette nye XML-attributtet angis av **LITWARE-6789** ID for føderal skatt som ble angitt for en fakturert kunde.

    ![Forhåndsvisning av den genererte XML-filen med tilpassingene.](./media/er-quick-start3-e-invoice2.png)

## <a name="import-the-latest-versions-of-standard-er-configurations"></a><a name="ImportERConfigurations2"></a>Importer de siste versjonene av standard ER-konfigurasjoner

Hvis du vil beholde settet med standard ER-konfigurasjoner i Finance-forekomsten din [oppdatert](general-electronic-reporting-manage-configuration-lifecycle.md), må du importere nye versjoner av dem hver gang de blir tilgjengelige i ER- [repositoriet](general-electronic-reporting.md#Repository) som ble konfigurert for den forekomsten.

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På **Lokaliseringskonfigurasjoner**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Microsoft**-flisen og deretter **Repositorier** for å vise listen over repositorier for Microsoft-leverandøren.
3. På **Konfigurasjonsrepositorier**-siden velger du repositoriet for **Global**-typen, og deretter velger du **Åpne**. Hvis du blir spurt om godkjenning for å koble til Regulatory Configuration Service, følger du godkjenningsinstruksjonene.
4. På **Konfigurasjonsrepositorier**-siden går du til konfigurasjonstreet i venstre rute og velger **Peppol-salgsfakura**-formatkonfigurasjonen.
5. I hurtigfanen **Versjoner** velger du versjon **32.6.7** av den valgte ER-formatkonfigurasjonen som er utgitt for å støtte elektroniske fakturaer for kunder i PEPPOL BIS 3-format. Hvis du vil ha mer informasjon, kan du se [KB4490320](https://support.microsoft.com/help/4490320/an-update-for-european-union-to-support-export-of-customers-electronic).
6. Velg **Importer** for å laste ned den valgte versjonen fra det globale repositoriet til den gjeldende forekomsten av Finance.

![Versjon 32.6.7 valgt på siden Konfigurasjonsrepositorium.](./media/er-quick-start3-import-solution2.png)

Hvis du vil ha informasjon om hvordan denne prosessen kan automatiseres, se [Importere oppdaterte versjoner av ER-konfigurasjoner](er-download-updated-versions-global-repo.md).

### <a name="review-the-imported-er-configurations"></a>Se gjennom importerte ER-konfigurasjoner

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Konfigurasjoner**, velger du flisen **Rapporteringskonfigurasjoner**.
3. Utvid hurtigfanen **Konfigurasjonskomponenter**.
4. I konfigurasjonstreet i venstre rute utvider du **Fakturamodell**. Legg merke til at navnet på **Kundefakturamodell** er endret til **Fakturamodell** i en av de importerte ER-datamodellkonfigurasjonene.
5. I konfigurasjonstreet i venstre rute utvider du **Fakturamodelltilordning**. Legg merke til at navnet på **Modelltilordning for kundefaktura** er endret til **Fakturamodelltilordning** i en av de importerte ER-modelltilordningskonfigurasjonene.
6. Utvid **UBL-salgsfaktura** \> **Peppol-salgsfaktura**.

Legg merke til at i tillegg til det valgte ER-formatet for **Peppol-salgsfaktura**, ble de siste versjonene av andre nødvendige ER-konfigurasjoner importert. Fordi nye versjoner av ER-konfigurasjoner stadig publiseres til det globale repositoriet og LCS, for å holde de tilsvarende ER-løsningene kompatible med nye krav, ble de nyeste versjonene av den nødvendige datamodell-konfigurasjonen og de tilhørende modelltilordning-konfigurasjonene importert.

Kontroller at følgende ER-konfigurasjoner til slutt er tilgjengelige i konfigurasjonstreet:

- **Fakturamodell** ER-datamodellkonfigurasjon:

    - Versjon 206 (eller senere) inneholder versjon 24 (eller senere) av datamodell ER-komponenten som representerer datastrukturen i fakturaens forretningsdomene. Denne ER-konfigurasjonen er importert som en overordnet av den sist tilgjengelige ER-modelltilordningsversjonen av **Fakturamodelltilordning**.

    ![Versjon 206 på konfigurasjonssiden.](./media/er-quick-start3-imported-solution2b1.png)

- **Fakturamodelltilordning** ER-modelltilordningskonfigurasjon:

    - Versjon 206.132 (eller senere) er importert som siste implementering av versjon 206 av ER-datamodellkonfigurasjonen **Fakturamodell**. Den inneholder flere modelltilordning ER-komponenter som beskriver hvordan datamodellen fylles ut med programdata ved kjøring.

    ![Versjon 206.132 på konfigurasjonssiden.](./media/er-quick-start3-imported-solution2b2.png)

- **UBL-salgsfaktura** ER-formatkonfigurasjon:

    - Versjon 32.6 inneholder format og formattilordning ER-komponenter. Formatkomponenten angir rapportoppsettet. Formattilordningskomponenten inneholder modelldatakilden og angir hvordan denne datakilden brukes til å rapportoppsettet fylles ut under kjøring. Dette ER-formatet ble konfigurert til å generere e-fakturaer i UBL-format. Den er importert som en overordnet til **Peppol salgsfaktura** ER-formatet som ble valgt for import.

- **Peppol-salgsfaktura** ER-formatkonfigurasjon:

    - Versjon 32.6.7 inneholder format- og formattilordnings ER-komponenter som ble konfigurert til å generere e-fakturaer i PEPPOL-format.

    ![Versjon 32.6.7 på konfigurasjonssiden.](./media/er-quick-start3-imported-solution2b3.png)

## <a name="adopt-the-changes-to-the-new-standard-er-configurations-in-your-custom-er-configurations"></a><a name="RebaseCustomERConfigurations"></a>Ta i bruk endringene i de nye versjonene av standard ER-konfigurasjonene i dine tilpassede ER-konfigurasjoner

### <a name="adopt-your-custom-er-data-model"></a>Ta i bruk den tilpassede datamodellen

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Fakturamodell** og velger **Fakturamodell (Litware)**.
3. I **Versjoner**-hurtigkategorien for utkastversjon **50.2** av den valgte datamodellkonfigurasjonen velger du **Rebaser**.
4. I **Målversjon**-feltet bekrefter du valget av versjon **206** av den grunnleggende ER-datamodellkonfigurasjonen, og deretter velger du **OK**.

    Utkastversjonen av den tilpassede ER-datamodellkonfigurasjonen er omnummerert fra **50.2** til **206.2** for å angi at den nå inneholder tilpassingen som ble slått sammen med endringene i den siste versjonen (206) av den grunnleggende ER-datamodellkonfigurasjon.

    > [!NOTE]
    > Rebaseringshandlingen er reversibel. Hvis du vil avbryte denne rebaseringen, velger du **50.1** av **Fakturamodell (Litware)**-modellen i **Versjoner**-hurtigfanen, og deretter velger du **Hent denne versjonen**. Versjon 206.2 blir deretter omnummerert tilbake til **50.2**, og innholdet i utkastversjon 50.2 vil samsvare med innholdet i versjon 50.1.

5. I **Versjon**-hurtigfanen velger du **Endre status** \> **Fullført**, og deretter velger du **OK**.

Statusen for versjon 206.2 endres fra **Utkast** til **Fullført**, og versjonen blir skrivebeskyttet. En ny redigerbar versjon, 206.3, har blitt lagt til og har statusen **Utkast**. Du kan bruke denne versjonen til å gjøre ytterligere endringer i ER-datamodellkonfigurasjonen.

![Versjon 206.2 fullført på konfigurasjonssiden.](./media/er-quick-start3-completed-custom-model2.png)

### <a name="adopt-your-custom-er-model-mapping"></a>Ta i bruk den tilpassede ER-modelltilordningen

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Fakturamodell** \> **Fakturamodelltilordning**, og velger **Fakturamodelltilordning (Litware)**.
3. I **Versjoner**-hurtigkategorien for utkastversjon **50.19.2** av den valgte modelltilordningskonfigurasjonen velger du **Rebaser**.
4. I **Målversjon**-feltet bekrefter du valget av versjon **206.132** av den grunnleggende ER-modelltilordningskonfigurasjonen, og deretter velger du **OK**.

    Utkastversjonen av den tilpassede ER-modelltilordningskonfigurasjonen er omnummerert fra **50.19.2** til **206.132.2** for å angi at den nå inneholder tilpassingen som ble slått sammen med endringene i den siste versjonen (206.132) av den grunnleggende ER-modelltilordningskonfigurasjonen.

    Legg merke til at noen rebaseringskonflikter ble oppdaget. Du må nå løse disse konfliktene manuelt.

    ![Melding om rebaseringskonflikt på konfigurasjonssiden.](./media/er-quick-start3-rebase-conflicts-model-mapping1.png)

5. Velg **Utforming** i handlingsruten, og velg deretter **Kundefaktura** i listen over tilordninger.
6. For hver rebaseringskonflikt velger **Behold egen verdi**, fordi du må beholde versjonsnummeret for den egendefinerte datamodellen for hver komponent som er nevnt.

    ![Rebaseringskonflikter på siden Modelltilordningsutforming.](./media/er-quick-start3-rebase-conflicts-model-mapping2.png)

7. Velg **Lagre**, og lukk deretter siden **Modelltilordningsutforming**.
8. I listen over tilordninger velger du **Prosjektfaktura**.
9. For hver rebaseringskonflikt velger **Behold egen verdi**, fordi du må beholde versjonsnummeret for den egendefinerte datamodellen for hver komponent som er nevnt.
10. Velg **Lagre**, og lukk deretter siden **Modelltilordninger**.

    > [!NOTE]
    > Rebaseringshandlingen er reversibel. Hvis du vil avbryte denne rebaseringen, velger du **50.19.1** av modelltilordningen **Fakturamodelltilordning (Litware)** i **Versjoner**-hurtigfanen, og deretter velger du **Hent denne versjonen**. Versjon 206.132.2 blir deretter omnummerert tilbake til **50.19.2**, og innholdet i utkastversjon 50.19.2 vil samsvare med innholdet i versjon 50.19.1.

11. I **Versjon**-hurtigfanen velger du **Endre status** \> **Fullført**, og deretter velger du **OK**.

Statusen for versjon 206.132.2 endres fra **Utkast** til **Fullført**, og versjonen blir skrivebeskyttet. En ny redigerbar versjon, 206.132.3, har blitt lagt til og har statusen **Utkast**. Du kan bruke denne versjonen til å gjøre ytterligere endringer i ER-modelltilordningskonfigurasjonen.

![Versjon 206.132.2 fullført på konfigurasjonssiden.](./media/er-quick-start3-completed-custom-mapping2.png)

### <a name="adopt-your-custom-er-format"></a>Ta i bruk det egendefinert ER-formatet

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Fakturamodell** \> **UBL-salgsfaktura** \> **Peppol-salgsfaktura**, og velger **Peppol-salgsfaktura (Litware)**.
3. I **Versjoner**-hurtigkategorien for utkastversjon **11.2.2.2** av den valgte formatkonfigurasjonen velger du **Rebaser**.
4. I **Mål**-versjonsfeltet bekrefter du valget av versjon **32.6.7** av den grunnleggende ER-formatkonfigurasjonen, og deretter velger du **OK**.

    Utkastversjonen av den tilpassede ER-formatkonfigurasjonen er omnummerert fra **11.2.2.2** til **32.6.7.2** for å angi at den nå inneholder tilpassingen som ble slått sammen med endringene i den siste versjonen (32.6.7) av den grunnleggende ER-formatkonfigurasjonen.

    Legg merke til at noen rebaseringskonflikter ble oppdaget. Du må nå løse disse konfliktene manuelt.

5. Velg **Utforming** i handlingsruten.
6. For hver rebaseringskonflikt velger **Behold egen verdi**, fordi du må beholde versjonsnummeret for den egendefinerte datamodellen for hver komponent som er nevnt.
7. Velg **Lagre**.
8. I **Tilordning**-kategorien velger du **Faktura**-datakilden for **Modell**-typen, og velger deretter **Rediger**.
9. I **Versjon**-feltet velger du versjon **2** av den egen definerte datamodellen, og deretter velger du **OK**.
10. Velg **Lagre**.

    > [!NOTE]
    > Rebaseringshandlingen er reversibel. Hvis du vil avbryte denne rebaseringen, velger du **11.2.2.1** av formatet **Peppol-salgsfaktura (Litware)** i **Versjoner**-hurtigfanen, og deretter velger du **Hent denne versjonen**. Versjon 32.6.7.2 blir deretter omnummerert tilbake til **11.2.2.2**, og innholdet i utkastversjon 11.2.2.2 vil samsvare med innholdet i versjon 11.2.2.1.

11. Lukk **Formatutforming**-siden.
12. I **Versjon**-hurtigfanen velger du **Endre status** \> **Fullført**, og deretter velger du **OK**.

Statusen for versjon 32.6.7.2 endres fra **Utkast** til **Fullført**, og versjonen blir skrivebeskyttet. En ny redigerbar versjon, 32.6.7.3, har blitt lagt til og har statusen **Utkast**. Du kan bruke denne versjonen til å gjøre ytterligere endringer i den egendefinerte ER-formatkonfigurasjonen.

![Versjon 32.6.7.2 fullført på konfigurasjonssiden.](./media/er-quick-start3-completed-custom-format2.png)

## <a name="process-a-customer-invoice-by-using-new-versions-of-the-custom-er-configurations"></a><a name="ProcessInvoice3"></a>Behandle en kundefaktura ved hjelp av nye versjoner av tilpassede ER-konfigurasjoner

### <a name="select-and-send-a-posted-invoice"></a>Velge og sende en postert faktura

1. Gå til **Kunder** \> **Fakturaer** \> **Alle fritekstfakturaer**.
2. På siden **Fritekstfaktura** velger du fakturaen du har lagt til og postert tidligere.
3. I handlingsruten i **Dokument**-gruppen velger du **Send** \> **Opprinnelig**.

    > [!NOTE] 
    > Fordi du nå har to versjoner av ER-formatkonfigurasjonen **Peppol-salgsfaktura (Litware)**, og ingen av versjonene har en [ikrafttredelsesdato](general-electronic-reporting.md#component-date-effectivity)-verdi, brukes den nyeste versjonen til å generere en e-faktura.

4. Lukk siden **Fritekstfaktura**.

### <a name="analyze-a-generated-e-invoice"></a>Analysere en generert e-faktura

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Elektroniske rapporteringsjobber**.
2. På siden **Elektroniske rapporteringsjobber** velger du den nyeste posten som har oppgavebeskrivelsen **Send eFaktura-XML**.
3. Velg **Vis filer** for å få tilgang til listen over genererte filer.
4. Velg **Åpne** for å laste ned e-faktura-XML-filen som genereres.
5. Analyser XML-filen for e-faktura. Legg merke til at i samsvar med tilpassingen, inkluderer kundeavgiftsskjemaet fremdeles det egendefinerte **FederalTaxID** XML-attributtet i tillegg til **schemeID** og **schemeAgencyID** XML-attributtene. I tillegg, fordi endringene i den nye versjonen av det grunnleggende **UBL-salgsfaktura**-formatet ble flettet med tilpassingen, er teksten i **cbc:CustomizationID** XML-elementet endret fra `urn:www.cenbii.eu:transaction:biicoretrdm010:ver1.0:# urn:www.peppol.eu:bis:peppol5a:ver1.0` til `urn:cen.eu:en16931:2017#compliant#urn:fdc:peppol.eu:2017:poacc:billing:3.0`.

    ![Forhåndsvisning av den genererte XML-filen med tilpassingene.](./media/er-quick-start3-e-invoice3.png)

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering](general-electronic-reporting.md)
- [Laste ned ER-konfigurasjoner fra Lifecycle Services](download-electronic-reporting-configuration-lcs.md)
- [Last ned ER-konfigurasjoner fra det globale repositoriet for konfigurasjonstjenesten](er-download-configurations-global-repo.md)
- [Opprett en fritekstfaktura](../../../finance/accounts-receivable/create-free-text-invoice-new.md)
- [Opprette og arbeide med egendefinerte felt](../../fin-ops/get-started/user-defined-fields.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
