---
title: Forbedre ytelsen for ER-løsninger ved å legge til datakilder med parameterisert BEREGNET FELT
description: Denne artikkelen beskriver hvordan du kan forbedre ytelsen til ER-løsninger (Electronic Reporting) ved å legge til datakilder med parameterisert BEREGNET FELT.
author: NickSelin
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8c2c0499ac3d41c9bb6026cc05f971087799c28f
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8850121"
---
# <a name="improve-the-performance-of-er-solutions-by-adding-parameterized-calculated-field-data-sources"></a>Forbedre ytelsen for ER-løsninger ved å legge til datakilder med parameterisert BEREGNET FELT

[!include [banner](../includes/banner.md)]

I denne artikkelen finner du informasjon om hvordan du kan utføre [ytelsessporinger](trace-execution-er-troubleshoot-perf.md) av [Elektronisk rapportering (ER)](general-electronic-reporting.md) som kjøres, og deretter bruke informasjonen fra disse sporingene til å forbedre ytelsen ved å konfigurere en datakilde med parameterisert **beregnet felt**.

Som en del av prosessen med å utforme ER-konfigurasjoner for å generere forretningsdokumenter, definerer du metoden som brukes til å hente data fra appen og registrere den i de genererte utdataene. Ved å utforme en parameterisert ER-datakilde for typen **Beregnet felt**, kan du redusere antallet databasekall, og du kan redusere tiden og kostnadene betydelig slik at du får mer detaljert informasjon om ER-formatutføringen.

## <a name="prerequisites"></a>Forutsetninger

- Hvis du vil fullføre eksemplene i denne artikkelen, må du ha tilgang til følgende [roller](../sysadmin/tasks/assign-users-security-roles.md):

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

- Firmaet må settes til **DEMF**.
- Følg trinnene i [Tillegg 1](#appendix1) i denne artikkelen for å laste ned komponentene i Microsoft ER-eksempelløsningen som kreves for å fullføre eksemplene i denne artikkelen.
- Følg trinnene i [Tillegg 2](#appendix2) i denne artikkelen for å konfigurere minimumssettet med ER-parametere som kreves for å bruke ER-rammeverket til å forbedre ytelsen i Microsoft ER-eksempelløsningen.

## <a name="import-the-sample-er-solution"></a>Importere ER-eksempelløsningen

Anta at du må utforme en ER-løsning for å generere en ny rapport som viser leverandørtransaksjoner. For øyeblikket finner du transaksjonene for en valgt leverandør på siden **Leverandørtransaksjoner** (gå til **Leverandører** \> **Leverandører** \> **Alle leverandører**, velg en leverandør, og deretter velger du **Transaksjoner** i gruppen **Transaksjoner** i kategorien **Leverandør** i handlingsruten). Du vil imidlertid ha alle leverandørtransaksjoner sammen i ett elektronisk dokument i XML-format. Denne løsningen vil bestå av flere ER-konfigurasjoner som inneholder den nødvendige datamodellen, modelltilordningen og formatkomponentene.

Det første trinnet er å importere ER-eksempelløsningen for å generere en leverandørtransaksjonsrapport.

1. Logg på forekomsten av Microsoft Dynamics 365 Finance som er klargjort for firmaet ditt.
2. I denne artikkelen skal du opprette og endre konfigurasjoner for eksempelfirmaet **Litware, Inc.** Kontroller at denne konfigurasjonsleverandøren er lagt til i Finance-forekomsten og er merket som aktiv. Hvis du ha mer informasjon, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).
3. I arbeidsområdet **Elektronisk rapportering** velger du flisen **Rapporteringskonfigurasjoner**.
4. På siden **Konfigurasjoner** importerer du ER-konfigurasjoner som du lastet ned som en forutsetning til Finance, i denne rekkefølgen: datamodell, modelltilordning, format. For hver konfigurasjon følger du disse trinnene:

    1. I handlingsruten velger du **Kurs** \> **Last fra XML-fil**.
    2. Velg **Bla gjennom**, og velg den riktige filen for ER-konfigurasjonen i XML-format.
    3. Velg **OK**.

![Importerte konfigurasjoner på siden Konfigurasjoner.](./media/er-calculated-field-ds-performance-imported-configurations.png)

## <a name="review-the-sample-er-solution"></a>Gå gjennom ER-eksempelløsningen

### <a name="review-the-model-mapping"></a>Se gjennom modelltilordningen

1. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **modellen Ytelsesforbedring** og velger **tilordningen Ytelsesforbedring**.
2. Velg **Utforming** i handlingsruten.
3. På siden **Tilordning av modell til datakilde** velger du **Utforming** i handlingsruten.

    Denne ER-modelltilordningen er utformet for å utføre følgende handlinger:

    - Hent listen over leverandørtransaksjoner som er lagret i VendTrans-tabellen (**Ttrans**-datakilde).
    - For hver transaksjon må du hente posten for en leverandør som transaksjonen er postert for (**\#Vend**-datakilde), fra tabellen VendTable.

    > [!NOTE]
    > Datakilden **\#Vend** er konfigurert til å hente den tilsvarende leverandørposten ved hjelp av den eksisterende mange-til-én-relasjonen **\@.'\>Relations'.VendTable\_AccountNum**.

    Modelltilordningen i denne konfigurasjonen implementerer basisdatamodellen for ER-formater som opprettes for denne modellen og som kjøres i Finance. Derfor vil inneholdet i datakilden **Trans** bli eksponert for ER-formater, for eksempel abstrakte datakilder av typen **model**.

    ![Trans-datakilde på siden Modelltilordningsutforming.](media/er-calculated-field-ds-performance-mapping-1.png)

4. Lukk siden **Modelltilordningsutforming**.
5. Lukk siden **Tilordning av modell til datakilde**.

### <a name="review-format"></a>Gjennomgangsformat

1. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **modellen Ytelsesforbedring** og velger **formatet Ytelsesforbedring**.
2. Velg **Utforming** i handlingsruten.
3. På siden **Formatutforming** i kategorien **Tilordning** velger du **Vis/skjul**.
4. Vis elementene **Modell**, **Data** og **Transaksjon**.

    Dette ER-formatet er utformet for å generere en leverandørtransaksjonsrapport i XML-format.

    ![Formatdatakilder og konfigurerte bindinger for formatelementer på siden Formatutforming.](media/er-calculated-field-ds-performance-format.png)

5. Lukk **Formatutforming**-siden.

## <a name="run-the-sample-er-solution-to-trace-execution"></a>Kjøre ER-eksempelløsningen for å spore kjøring

Anta at du er ferdig med å utforme den første versjonen av ER-løsningen. Nå skal du teste løsningen i Finance-forekomsten og analysere kjøringsytelsen.

### <a name="turn-on-the-er-performance-trace"></a>Aktivere ER-ytelsessporing

1. Velg **DEMF**-firmaet.
2. Følg fremgangsmåten il [Aktivere ER-ytelsessporing](trace-execution-er-troubleshoot-perf.md#turn-on-the-er-performance-trace) for å generere en ytelsessporing mens et ER-format kjøres.

    ![Dialogboksen Brukerparametere.](media/er-calculated-field-ds-performance-format-user-parameters.png)

### <a name="run-the-er-format"></a><a id="run-format"></a>Kjør ER-formatet

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På siden **Konfigurasjoner** i konfigurasjonstreet, velger du **Format for ytelsesforbedring**.
3. Velg **Kjør** i handlingsruten.

## <a name="use-the-performance-trace-to-analyze-model-mapping-performance"></a>Bruke ytelsessporing til å analysere ytelse for modelltilordning

1. På siden **Konfigurasjoner** i konfigurasjonstreet, velger du **Tilordning for ytelsesforbedring**.
2. Velg **Utforming** i handlingsruten.
3. På siden **Modelltilordninger** velger du **Utforming** i handlingsruten.
4. På siden **Modelltilordningsutforming**, i handlingsruten, velger du **Ytelsessporing**.
5. Velg den siste sporingen som ble generert, og velg deretter **OK**.

Ny informasjon er nå tilgjengelig for noen datakildeelementer av gjeldende modelltilordning:

- Den faktiske tiden som ble brukt til å hente data ved hjelp av datakilden
- Den samme tiden som prosent av den totale tiden som ble brukt til å kjøre hele modelltilordningen

![Informasjon om utføringstid på siden Modelltilordningsutforming.](./media/er-calculated-field-ds-performance-mapping-2.png)

Rutenettet **Ytelsesstatistikk** viser at datakilden **Trans** kaller VendTrans-tabellen én gang. Verdien **\[265\]\[Q:265\]** for datakilden **Trans** angir at 265 leverandørtransaksjoner er hentet fra apptabellen og returneres til datamodellen.

Rutenettet **Ytelsesstatistikk** viser også at gjeldende modelltilordning dupliserer databaseforespørsler når datakilden **\#Vend** kjøres. Dupliseringen skjer av følgende årsaker:

- Leverandørtabellen kalles to ganger for hver av de 265 omsluttede leverandørtransaksjonene, totalt 530 kall:

    - Det blir opprettet ett kall for å angi leverandørkontonummeret.
    - Det blir opprettet ett kall for å angi leverandørnavnet.

- Leverandørtabellen kalles for hver repeterende leverandørtransaksjon, selv om de hentede transaksjonene bare er postert for fem leverandører. Av de 530 kallene er 525 duplikater. Følgende illustrasjon viser meldingen du mottar om duplikatoppringinger (databaseforespørsler).

![Melding om dupliserte databaseforespørsler på siden Modelltilordningsutforming.](./media/er-calculated-field-ds-performance-mapping-2a.png)

Av den samlede utføringstiden for modelltilordning (ca. åtte sekunder), må du legge merke til at mer enn 80 prosent (omtrent seks sekunder) har blitt brukt til å hente verdier fra apptabellen VendTable. Denne prosentandelen er for stor for to attributter av fem leverandører, sammenlignet med informasjonsvolumet i apptabellen VendTrans.

Hvis du vil redusere antallet kall som gjøres for å få leverandørdetaljene for hver transaksjon, og for å forbedre ytelsen til modelltilordningen, kan du bruke hurtigbufring for datakilden **\#Vend**.

> [!NOTE]
> Datakilden **Trans\\\#Vend** blir bufret i området til gjeldende transaksjon for datakilden **Trans** ved kjøring.

Ved å bufre datakilden **\#Vend**, reduserer du antallet dupliserte kall fra 525 til 260, men eliminerer ikke dupliseringen fullstendig. Hvis du vil eliminere duplisering fullstendig, kan du konfigurere en ny parameterdatakilde av typen **Beregnet felt**.

## <a name="improve-the-model-mapping-based-on-information-from-the-execution-trace"></a>Forbedre modelltilordningen basert på informasjon fra kjøringssporingen

### <a name="change-the-logic-of-the-model-mapping"></a>Endre logikken til modelltilordningen

Følg denne fremgangsmåten for å bruke bufring og en datakilde av typen **Beregnet felt** for å hindre dupliserte kall til databasen.

1. På siden **Konfigurasjoner** i konfigurasjonstreet, velger du **Tilordning for ytelsesforbedring**.
2. Velg **Utforming** i handlingsruten.
3. På siden **Modelltilordninger** velger du **Utforming** i handlingsruten.
4. På siden **Modelltilordningsutforming** følger du denne fremgangsmåten for å legge til en datakilde av typen **Tabellposter** for å få tilgang til poster i apptabellen VendTable:

    1. I ruten **Datakildetyper** utvider du **Dynamics 365 for Operations** og velger **Tabellposter**.
    2. Velg **Legg til rot**.
    3. Skriv inn **Vend** i **Navn**-feltet i dialogboksen.
    4. I **Tabell**-feltet angir du **VendTable**.
    5. Velg **OK**.

5. Du kan parameterisere kall til datakilder av typen **Beregnet felt** bare hvis disse datakildene befinner seg i en beholder. Du bør derfor følge denne fremgangsmåten for å legge til en datakilde av typen **Tom beholder** for å oppbevare en ny parameterdatakilde av typen **Beregnet felt**:

    1. I ruten **Datakildetyper** utvider du **Generelt** og velger **Tom beholder**.
    2. Velg **Legg til rot**.
    3. Skriv inn **Box** i **Navn**-feltet i dialogboksen.
    3. Velg **OK**.

    ![Box-datakilde på siden Modelltilordningsutforming.](./media/er-calculated-field-ds-performance-mapping-3.png)

6. Følg disse trinnene for å legge til en parameterdatakilde av typen **Beregnet felt**:

    1. I ruten **Datakilder** velger du **Box**.
    2. I ruten **Datakildetyper** utvider du **Funksjoner** og velger **Beregnet felt**.
    3. Velg **Legg til**.
    4. Skriv inn **Vend** i **Navn**-feltet i dialogboksen.
    5. Velg **Rediger formel**.
    6. På siden **Formeldesigner** velger du **Parametere** for å angi parameterne som må oppgis når datakilden kalles.
    7. I dialogboksen **Parametere** velger du **Ny**.
    8. I **Navn**-feltet angir du **parmVendAccNumber**.
    9. Velg **Streng** i **Type**-feltet.
    10. Velg **OK**.
    11. I **Formel**-feltet angir du **FIRSTORNULL(FILTER(Vend, Vend.AccountNum=parmVendAccNumber))**.
    12. Velg **Lagre**, og lukk siden **Formeldesigner**.
    13. Velg **OK** for å legge til den nye datakilden.

7. Følg denne fremgangsmåten for å merke den tillagte datakilden som hurtigbufret under kjøringen:

    1. I ruten **Datakilder** velger du **Box\\Vend**.
    2. Velg **Hurtigbuffer**.

    > [!NOTE]
    > Datakilden **Box\\Vend** vil bli bufret i omfanget for alle leverandørtransaksjoner for datakilden **Trans** under kjøring.

8. Følg denne fremgangsmåten for å oppdatere den nestede datakilden **Trans\\\#Vend** slik at den bruker datakilden **Box\\Vend**:

    1. I **Datakilder**-ruten utvider du **Trans**.
    2. Velg datakilden **Trans\\\#Vend**, og velg deretter **Rediger** \> **Rediger formel**.
    3. På siden **Formeldesigner** i feltet **Formel** angir du **Box.Vend(\@.AccountNum)**.
    4. Velg **Lagre**, og lukk deretter siden **Formeldesigner**.
    5. Velg **OK** for å fullføre endringene i den valgte datakilden.

9. Velg **Lagre**.

    ![Vend-datakilde på siden Modelltilordningsutforming.](./media/er-calculated-field-ds-performance-mapping-4.png)

10. Lukk siden **Modelltilordningsutforming**.
11. Lukk siden **Modelltilordninger**.

### <a name="complete-the-modified-version-of-the-er-model-mapping"></a>Fullføre den endrede versjonen av ER-modelltilordningen

1. På siden **Konfigurasjoner** i hurtigkategorien **Versjoner**, velger du versjon **1.2** av konfigurasjonen **Tilordning for ytelsesforbedring**.
2. Velg **Endre status** \> **Fullfør**, og velg deretter **OK**.

## <a name="run-the-modified-er-solution-to-trace-execution"></a>Kjøre den endrede ER-løsningen for å spore kjøring

Gjenta trinnene i delen [Kjør ER-formatet](#run-format) tidligere i denne artikkelen for å generere en ny ytelsessporing.

## <a name="use-the-performance-trace-to-analyze-adjustments-to-the-model-mapping"></a>Bruke ytelsessporing til å analysere justerniger for modelltilordningen 

1. På siden **Konfigurasjoner** i konfigurasjonstreet, velger du **Tilordning for ytelsesforbedring**.
2. Velg **Utforming** i handlingsruten.
3. På siden **Modelltilordninger** velger du **Utforming** i handlingsruten.
4. På siden **Modelltilordningsutforming**, i handlingsruten, velger du **Ytelsessporing**.
5. Velg den siste sporingen som ble generert, og velg deretter **OK**.

Legg merke til at justeringene du har gjort i modelltilordningen, har eliminert duplikate spørringer til databasen. Antall kall til databasetabeller og datakilder for denne modelltilordningen er også redusert.

![Sporingsinformasjon på siden Modelltilordningsutforming 1.](./media/er-calculated-field-ds-performance-mapping-5.png)

Den totale utføringstiden er redusert omtrent 20 ganger (fra omtrent 8 sekunder til omtrent 400 millisekunder). Derfor har ytelsen til hele ER-løsningen blitt forbedret.

![Sporingsinformasjon på siden Modelltilordningsutforming 2.](./media/er-calculated-field-ds-performance-mapping-5a.png)

## <a name="appendix-1-download-the-components-of-the-sample-microsoft-er-solution"></a><a name="appendix1"></a>Tillegg 1: Last ned komponentene i Microsoft ER-eksempelløsningen

Du må laste ned følgende filer og lagre dem lokalt.

| Fil                                        | Innhold |
|---------------------------------------------|---------|
| Ytelsesforbedringsmodell, versjon 1     | [Eksempel ER-datamodellkonfigurasjon](https://download.microsoft.com/download/4/6/f/46f0f3fa-782b-414a-8f7b-b6c64a388661/Performance_improvement_model.version.1.xml) |
| Tilordning for ytelsesforbedring, versjon.1.1 | [Eksempel ER-modelltilordningskonfigurasjon](https://download.microsoft.com/download/8/9/1/8913a763-afb8-4bf4-aaf1-95ad793ffc5a/Performance_improvement_mapping.version.1.1.xml) |
| Format for ytelsesforbedring, versjon.1.1  | [Eksempel ER-formatkonfigurasjon](https://download.microsoft.com/download/9/0/c/90c75963-bc78-4edc-9096-556bbe281f10/Performance_improvement_format.version.1.1.xml) |

## <a name="appendix-2-configure-the-er-framework"></a><a name="appendix2"></a>Tillegg 2: Konfigurere ER-rammeverket

Før du kan begynne å bruke ER-rammeverket til å forbedre ytelsen til Microsoft ER-eksempelløsningen, må du konfigurere minimumssettet med ER-parametere.

### <a name="configure-er-parameters"></a><a id="ConfigureParameters"></a>Konfigurere ER-parametere

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Parametere for elektronisk rapportering**.
3. På **Parametere for elektronisk rapportering**-siden, i **Generelt**-fanen angi **Aktiver utformingsmodus** til **Ja**.
4. Angi følgende parametere i fanen **Vedlegg**:

    - I **Konfigurasjoner**-feltet velger du **Fil**-typen for **DEMF**-firmaet.
    - I feltene **Jobbarkiv**, **Midlertidig**, **Grunnlinje** og **Annet** velger du **Fil**-typen.

Hvis du vil ha mer informasjon om ER-parametere, kan du se [Konfigurere ER-rammeverket](electronic-reporting-er-configure-parameters.md).

### <a name="activate-an-er-configuration-provider"></a><a id="ActivateProvider"></a>Aktivere en ER-konfigurasjonsleverandør

Hver ER-konfigurasjon som legges til, er merket som eid av en ER-konfigurasjonsleverandør. ER-konfigurasjonsleverandøren som aktiveres i **Elektronisk rapportering**-arbeidsområdet, brukes til dette formålet. Derfor må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet før du begynner å legge til eller redigere ER-konfigurasjoner.

> [!NOTE]
> Bare eieren av en ER-konfigurasjon kan redigere den. Derfor, før en ER-konfigurasjon kan redigeres, må du aktivere en ER-konfigurasjonsleverandør i **Elektronisk rapportering**-arbeidsområdet.

#### <a name="review-the-list-of-er-configuration-providers"></a><a id="ReviewProvidersList"></a>Se gjennom listen over ER-konfigurasjonsleverandører

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Konfigurasjonsleverandører**.
3. På **Konfigurasjonsleverandørtabell**-siden har hver leverandørpost et unikt navn og en unik URL-adresse. Se gjennom innholdet på denne siden. Hvis en post for **Litware, Inc.** allerede finnes, hopper du over netste prosedyre, kalt [Legg til en ny ER-konfigurasjonsleverandør](#ActivateProvider).

#### <a name="add-a-new-er-configuration-provider"></a><a id="ActivateProvider"></a>Legg til en ny ER-konfigurasjonsleverandør

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På siden **Lokaliseringskonfigurasjoner**, i delen **Relaterte koblinger**, velger du flisen **Konfigurasjonsleverandører**.
3. Velg **Ny** på siden **Konfigurasjonsleverandører**.
4. I **Navn**-feltet angir du **Litware, Inc.**
5. I **Internett-adresse**-feltet angir du `https://www.litware.com`.
6. Velg **Lagre**.

#### <a name="activate-an-er-configuration-provider"></a><a id="ActivateAddedProvider"></a>Aktivere en ER-konfigurasjonsleverandør

1. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
2. På **Lokaliseringskonfigurasjoner**-siden, i **Konfigurasjonsleverandører**-delen, velger du **Litware, Inc.**-flisen og deretter **Angi aktiv**.

Hvis du ha mer informasjon om ER-konfigurasjonsleverandører, kan du se [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md).

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering](general-electronic-reporting.md)
- [Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md)
- [Støtte for parameterkall fra ER-datakilder for Beregnet felt-typen](er-calculated-field-type.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
