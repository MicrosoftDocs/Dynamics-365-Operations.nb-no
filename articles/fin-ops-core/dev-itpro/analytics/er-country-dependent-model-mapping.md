---
title: Konfigurere landkontekstsavhengige ER-modelltilordninger
description: Dette emnet beskriver hvordan du kan definere ER-modelltilordninger slik at de avhenger av land/område-konteksten til den juridiske enheten som styrer bruken.
author: NickSelin
manager: AnnBe
ms.date: 11/11/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERSolutionTable
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.2
ms.openlocfilehash: a9035f128a1db4bcd126f09c0fe30c1857fa884a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680883"
---
# <a name="configure-country-context-dependent-er-model-mappings"></a>Konfigurere landkontekstsavhengige ER-modelltilordninger

[!include[banner](../includes/banner.md)]

Du kan konfigurere ER-modelltilordninger slik at de implementerer en generisk ER-datamodell, men som er spesifikke for Dynamics 365 Finance. Dette emnet forklarer hvordan du utformer flere ER-modelltilordninger for en ER-datamodell for å kontrollere hvordan de brukes ved hjelp av de tilsvarende ER-formatene som kjøres fra firmaer som har forskjellige land-/område kontekster.

## <a name="prerequisites"></a>Forutsetninger

Hvis du vil fullføre eksemplene i dette emnet, må du ha følgende tilgang:

- Tilgang til Finance for én av følgende roller:
    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

- Tilgang til forekomsten av Regulatory Configuration Service (RCS) som er klargjort for samme leietaker som Finance, for én av følgende roller:
    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

Noen trinn i dette emnet krever at du kjører et ER-format. I noen tilfeller påvirkes utføringen av et ER-format av land/område-konteksten til det firmaet du er logget på. Du kan kjøre et ER-format i gjeldende RCS-forekomst hvis firmaet som har den nødvendige land/område-konteksten, er tilgjengelig i RCS. Hvis ikke må du laste opp en fullført versjon av ER-modelltilordningen og ER-formatkonfigurasjonene som bruker ER-datamodellen til Finance-forekomsten, og deretter kjøre ER-formatet i den Finance-forekomsten. Hvis du vil ha informasjon om hvordan du importerer konfigurasjoner som ligger i RCS til en Finance-forekomst, kan du se [Importere konfigurasjoner fra RCS](rcs-download-configurations.md).

## <a name="single-model-mapping-case"></a>Sak for tilordning av én modell

Følg trinnene i [Tillegg 1](#appendix1) i dette emnet for å utforme de nødvendige ER-komponentene. Du har nå modelltilordningskonfigurasjonen **Tilordning (generelt)** som inneholder modelltilordningen for definisjonen **Inngangspunkt 1**.

![Siden ER-konfigurasjoner](./media/RCS-Context-specific-mapping-Tree.PNG)

### <a name="run-the-configured-format"></a>Kjøre det konfigurerte formatet

1.  Velg **Kjør** i hurtigfanen **Versjoner** på **Konfigurasjoner-siden**.
2.  Velg **OK**.

Legg merke til at webleseren tilbyr å laste ned tekstfilen som ble generert av det utførte ER-formatet. Fordi dette formatet ble konfigurert til å bruke **Inngangspunkt 1**-definisjonen, og bare én enkelt modelltilordning for øyeblikket er tilgjengelig for grunnmodellen som inneholder en tilordning for denne definisjonen, brukte det utførte ER-formatet **Tilordning (generelt)**-modelltilordningen for **Tilordning (generelt)**-konfigurasjonen som en datakilde. Derfor inneholder den nedlastede filen **Generisk funksjonalitet 1**-teksten.

## <a name="multiple-shared-model-mappings-case"></a>Sak for tilordninger av flere delte modeller

Følg trinnene i [Tillegg 2](#appendix2) i dette emnet for å utforme de nødvendige ER-komponentene. Du har nå modelltilordningskonfigurasjonene **Tilordning (generelt)** og **Tilordning (generelt) egendefinert** som hver inneholder modelltilordningen for definisjonen **Inngangspunkt 1**.

![Siden ER-konfigurasjoner](./media/RCS-Context-specific-mapping-TreeCustom.PNG)

### <a name="run-the-configured-format"></a>Kjøre det konfigurerte formatet

1.  På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Format for å lære om tilordninger**.
2.  Velg **Kjør** i hurtigfanen **Versjoner**.
3.  Velg **OK**.

Varsel om at utføringen av det valgte ER-formatet er mislykket. En feilmelding informerer deg om at det finnes mer enn én modelltilordning for modellen **Modell for å lære om tilordninger** og **Inngangspunkt 1**-definisjon i modelltilordningskonfigurasjonene **Tilordning (generelt)** og **Tilordning (generelt) egendefinert**. Meldingen anbefaler også at du velger en av disse konfigurasjonene som standardkonfigurasjon.

![Siden ER-konfigurasjoner](./media/RCS-Context-specific-mapping-FormatRunCustomFailed.PNG)

### <a name="define-a-default-mapping-configuration"></a>Definere en konfigurasjon for standardtilordning

Følg denne fremgangsmåten for å definere modelltilordningskonfigurasjonen **Tilordning (generelt) egendefinert** som standardkonfigurasjon, slik at tilordninger kan brukes som datakilder for ER-formatet **Format for å lære om tilordninger**.

1.  På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Tilordning (generelt) egendefinert**.
2.  Velg om nødvendig **Rediger** for å klargjøre gjeldende side for redigering.
3.  Sett alternativet **Standard for modelltilordning** til **Ja**.
4.  Velg **Lagre**.

![Siden ER-konfigurasjoner](./media/RCS-Context-specific-mapping-MappingsCustomDefault.PNG)

### <a name="run-the-configured-format"></a>Kjøre det konfigurerte formatet

1.  På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Format for å lære om tilordninger**.
2.  Velg **Kjør** i hurtigfanen **Versjoner**.
3.  Velg **OK**.

Varsel om at utføringen av det valgte ER-formatet lyktes. Webleseren tilbyr å laste ned tekstfilen som ble generert av det utførte ER-formatet. Fordi dette formatet ble konfigurert til å bruke **Inngangspunkt 1**-definisjonen, og modelltilordningskonfigurasjonen **Tilordning (generelt) egendefinert** ble valgt som standardkonfigurasjon, brukte det utførte ER-formatet modelltilordningen **Tilordning (generelt) kopi** for konfigurasjonen **Tilordning (generelt) egendefinert** som en datakilde. Derfor inneholder den nedlastede filen **Generisk funksjonalitet 1 egendefinert**-teksten.

> [!NOTE]
> Hvis du endrer firmaet du er logget på og kjører dette ER-formatet på nytt, får du samme innhold i den genererte filen, fordi standardkonfigurasjonen for ER-modelltilordning ikke inneholder firmaavhengige begrensninger.

## <a name="multiple-mixed-model-mappings-case"></a>Sak for tilordninger av flere blandede modeller

Følg trinnene i [Tillegg 3](#appendix3) i dette emnet for å utforme de nødvendige ER-komponentene. Du har nå konfigurasjonene **Tilordning (generelt)**, **Tilordning (generelt) egendefinert** og **Tilordning (FR) modelltilordning** som inneholder modelltilordningen for definisjonen **Inngangspunkt 1**.

Legg merke til at versjon 1 av **Tilordning (FR)**-modelltilordningskonfigurasjonen er konfigurert slik at den bare gjelder for ER-formater for modellen **Modell for å lære om tilordninger** som kjøres i økonomifirmaer som har fransk land/område-kontekst.

![Siden ER-konfigurasjoner](./media/RCS-Context-specific-mapping-TreeFR.PNG)

### <a name="run-the-configured-format"></a>Kjøre det konfigurerte formatet

1.  Endre firma til **FRSI**.
2.  På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Format for å lære om tilordninger**.
3.  Velg **Kjør** i hurtigfanen **Versjoner**.
4.  Velg **OK**.

Varsel om at utføringen av det valgte ER-formatet lyktes. Webleseren tilbyr å laste ned tekstfilen som ble generert av det utførte ER-formatet. Fordi dette formatet ble konfigurert til å bruke **Inngangspunkt 1**-definisjonen, og modelltilordningskonfigurasjonen **Tilordning (generelt) egendefinert** ble valgt som standardkonfigurasjon, brukte det utførte ER-formatet modelltilordningen **Tilordning (generelt) kopi** for konfigurasjonen **Tilordning (generelt) egendefinert** som en datakilde. Derfor inneholder den nedlastede filen **Generisk funksjonalitet 1 egendefinert**-teksten.

### <a name="define-the-france-specific-mapping-configuration-as-the-default-configuration"></a>Definere den Frankrike-spesifikke tilordningskonfigurasjonen som standardkonfigurasjon

Følg denne fremgangsmåten for definere den egendefinerte modelltilordningskonfigurasjonen **Tilordning (FR)** som standardkonfigurasjon. Vær oppmerksom på at siden denne tilordningen er spesifikk for Frankrike, regnes den som standardtilknytningen mellom alle modelltilordningskonfigurasjoner som har **FR**-landskoden spesifisert i feltet **ISO-koder for land/område**.

1.  På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Tilordning (FR)**.
2.  Velg om nødvendig **Rediger** for å klargjøre gjeldende side for redigering.
3.  Sett alternativet **Standard for modelltilordning** til **Ja**.
4.  Velg **Lagre**.

![Siden ER-konfigurasjoner](./media/RCS-Context-specific-mapping-TreeFRDefault.PNG)

### <a name="run-the-configured-format"></a>Kjøre det konfigurerte formatet

1.  På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Format for å lære om tilordninger**.
2.  Velg **Kjør** i hurtigfanen **Versjoner**.
3.  Velg **OK**.

Varsel om at utføringen av det valgte ER-formatet lyktes. Webleseren tilbyr å laste ned tekstfilen som ble generert av det utførte ER-formatet. Fordi dette formatet ble konfigurert til å bruke **Inngangspunkt 1**-definisjonen, og modelltilordningskonfigurasjonen **Tilordning (FR)** ble valgt som standardkonfigurasjon, brukte det utførte ER-formatet modelltilordningen **Tilordning (FR)** for konfigurasjonen **Tilordning (FR)** som en datakilde. Derfor inneholder den nedlastede filen **FR-funksjonalitet 1**-teksten.

> [!NOTE]
> Hvis du endrer firmaet som du for øyeblikket er logget på og kjører dette ER-formatet på nytt, vil utdataene være avhengig av land/område-konteksten for det valgte firmaet.

## <a name="other-model-mapping-cases"></a>Andre saker for tilordning av modell

Som du har sett, kan du velge en modelltilordning for å kjøre et ER-format på følgende måte:

- Modelltilordningsdefinisjonen som brukes av ER-formatet, er angitt (**Inngangspunkt 1** i eksemplene i dette emnet).
- Alle tilordningskonfigurasjoner som inneholder en tilordning som har den angitte definisjonen, og som oppfyller alle kontekstbegrensninger for land/område som er konfigurert, kan potensielt brukes til å kjøre ER-formatet (**Tilordning (generelt)**, **Tilordning (generelt) egendefinert** og **Tilordning (FR)** i eksemplene i dette emnet).
- Alle standard modelltilordninger som har kontekstbegrensninger for land/område, har høyest prioritet for valg (**Tilordning (FR)** i eksemplene i dette emnet).
- Alle standard modelltilordninger som ikke har kontekstbegrensninger for land/område, har nest høyest prioritet for valg (**Tilordning (genrelt) egendefinert** i eksemplene i dette emnet).
- Alle modelltilordninger som har kontekstbegrensninger for land/område har høyere prioritet for valg enn modelltilordninger som ikke har kontekstbegrensninger for land/område.

Følgende tabell gir informasjon om resultatene av modelltilordningsvalget for alle mulige tilfeller for modelltilordningsinnstillinger:

- Kolonne 1 angir om den første modelltilordningen som ikke har kontekstbegrensninger for land/område (for eksempel den delte tilordningen **Tilordning (generelt)**) blir presentert, og hvis den blir det, om alternativet **Standard for modelltilordning** er angitt til **Ja** for den.
- Kolonne 2 angir om den andre modelltilordningen som ikke har kontekstbegrensninger for land/område (for eksempel den delte tilordningen **Tilordning (generelt) egendefinert**), blir presentert, og hvis den blir det, om alternativet **Standard for modelltilordning** er angitt til **Ja** for den.
- Kolonne 3 angir om den første modelltilordningen som har kontekstbegrensninger for land/område A (for eksempel den Frankrike-spesifikke tilordningen **Tilordning (FR)**), blir presentert, og hvis den blir det, om alternativet **Standard for modelltilordning** er angitt til **Ja** for den.
- Kolonne 4 angir om den andre modelltilordningen som har kontekstbegrensninger for land/område A, blir presentert, og hvis den blir det, om alternativet **Standard for modelltilordning** er angitt til **Ja** for den.
- Kolonne 5 viser resultatet av et modelltilordningsvalg for utførelse av et ER-format under kontroll av et firma som har en kontekst for land/område A.
- Kolonne 6 viser resultatet av et modelltilordningsvalg for utførelse av et ER-format under kontroll av et firma som har en kontekst for land/område B.

I tabellen angir et plusstegn (+) tilstedeværelsen av en modelltilordningskonfigurasjon i den gjeldende forekomsten av Microsoft Azure-tjenesten som brukes til å kjøre et ER-format (enten Finance eller RCS).

| Sak | Modelltilordning 1 uten land/område-kontekst (MM1) | Modelltilordning 2 uten land/område-kontekst (MM2) | Modelltilordning 1 med land/område A-kontekst (MM1A) | Modelltilordning 2 med land/område A-kontekst (MM2A) | Kjør under kontroll av et firma som har en kontekst for land/område A | Kjør under kontroll av et firma som har en kontekst for land/område B |
|---------|---------|---------|---------|---------|---------------------------|----------------------------|
|         |     1   |     2   |    3    |    4    |           5               |            6               |
|     1   |         |         |         |         | Feil (mangler tilordning)   | Feil (mangler tilordning)    |
|     2   |     +   |         |         |         | MM1                       | MM1                        |
|     3   |     +   |     +   |         |         | Feil (flere tilordninger) | Feil (flere tilordninger)  |
|     4   |     +   |         |    +    |         | MM1A                      | MM1                        |
|     5   |     +   |         |    +    |    +    | Feil (flere tilordninger) | MM1                        |
|     6   |     +   | standard |    +    |    +    | MM2                       | MM2                        |
|     7   |     +   |         | standard |         | MM1A                      | MM1                        |
|     8   |     +   |         | standard |    +    | MM1A                      | MM1                        |
|     9   |     +   |         | standard | standard | Feil (flere tilordninger) | MM1                        |
|    10   | standard |         |         |         | MM1                       | MM1                        |
|    11   | standard |    +    |         |         | MM1                       | MM1                        |
|    12   | standard |         |    +    |         | MM1                       | MM1                        |
|    13   | standard | standard |         |         | Feil (flere tilordninger) | Feil (flere tilordninger)  |
|    14   | standard |         | standard |         | MM1A                      | MM1                        |
|    15   | standard |         | standard | standard | MM1A                      | MM2A                       |
|    16   |         |         |    +    |    +    | MM1A                      | MM2A                       |
|    17   |         |         | standard | standard | MM1A                      | MM2A                       |

## <a name="learn-what-mapping-was-used-in-the-execution-of-an-er-format"></a>Lær hvilken tilordning som ble brukt ved utførelsen av et ER-format

### <a name="configure-er-user-parameters"></a>Konfigurere ER-brukerparametere

1.  Velg **Brukerparametere** i **KONFIGURASJON**-fanen i handlingsruten på **Konfigurasjoner**-siden.
2.  Sett alternativet **Kjør i feilsøkingsmodus** til **Ja**.
4.  Velg **OK**.

### <a name="run-the-configured-format"></a>Kjøre det konfigurerte formatet

1.  På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Format for å lære om tilordninger**.
2.  Velg **Kjør** i hurtigfanen **Versjoner**.
3.  Velg **OK**.

### <a name="review-the-er-debug-log"></a>Se gjennom feilsøkingsloggen for ER

1.  I navigasjonsruten går du til **Moduler \> Organisasjonsstyring \> Elektronisk rapportering \> Feilsøkingslogger for konfigurasjon**.
2.  Velg knappen **Last inn denne siden på nytt**.

![Siden ER-kjøringslogger](./media/RCS-Context-specific-mapping-DebugLog.PNG)

Legg merke til at en ny post er lagt til i ER-feilsøkingsloggen for det utførte ER-formatet. Siden **Nivå**-feltet for denne posten er satt til **Informasjon**, er posten veiledende. Siden Formatkomponent-feltet er satt **Tilordningskonfigurasjon**, informerer posten deg om en modelltilordning som ble brukt under utførelsen av ER-formatet **Format for å lære om tilordninger** (valgt i feltet **Konfigurasjonsnavn**). Innholdet i feltet **Generert tekst** informerer deg om at tilordningskomponenten **Tilordning (FR)** som befinner seg i konfigurasjonen **Tilordning (FR)**, er brukt til å kjøre denne rapporten.

## <a name="appendix-1"></a><a name="appendix1"></a> Tillegg 1

### <a name="configure-a-sample-data-model"></a>Konfigurere en eksempeldatamodell

Logg på RCS-forekomsten.

I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet, Litware, Inc. Først må du fullføre disse trinnene i RCS i fremgangsmåten [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

#### <a name="create-an-er-data-model-configuration"></a>Opprette en ER-datamodellkonfigurasjon

1.  Velg **Elektronisk rapportering** på standard instrumentbord.
2.  Velg flisen **Rapporteringskonfigurasjoner**.
3.  Velg **Opprett konfigurasjon** på siden **Konfigurasjoner**.
4.  Skriv inn **Modell for å lære om tilordninger** i **Navn**-feltet i rullegardinboksen.
5.  Velg **Opprett konfigurasjon**.
6.  Velg hurtigfanen **Konfigurasjonskomponenter**.

Legg merke til at utkastversjon 1 av denne ER-konfigurasjonen er klar til redigering. Denne versjonen inneholder datamodellkomponenten.

#### <a name="design-a-sample-data-model"></a>Utforme en eksempeldatamodell

1.  Velg **Utforming** på **Konfigurasjoner-siden**.
2.  Velg **Ny**.
3.  Skriv inn **Inngangspunkt 1** i **Navn**-feltet i rullegardinboksen.
4.  Velg **Legg til**.
5.  Velg **Ny**.
6.  Skriv inn **Funksjonsbeskrivelse** i **Navn**-feltet i rullegardinboksen.
7.  Velg **Legg til**.
8.  Velg **Ny**.
9.  Skriv inn **Modellrot** i **Ny node**-feltgruppen i rullegardinboksen.
10. I **Navn**-feltet angir du **Inngangspunkt 2**.
11. Velg **Inngangspunkt 2**.
12. Velg **Legg til**.
13. Velg **Ny**.
14. Skriv inn **Funksjonsbeskrivelse** i **Navn**-feltet i rullegardinboksen.
15. Velg **Legg til**.

    ![Siden ER-datamodellutforming](./media/RCS-Context-specific-mapping-Model.PNG)

16. Velg **Lagre**.
17. Lukk siden.

#### <a name="complete-the-modified-version-of-the-model-configuration"></a>Fullføre den endrede versjonen av modellkonfigurasjonen

1.  Velg **Endre status** i hurtigfanen **Versjoner** på siden **Konfigurasjoner**.

    > Endre statusen for utformet modellkonfigurasjon fra **Kladd** til **Fullført**, slik at den kan brukes til å utforme de nødvendige modelltilordningene og formatene.

2.  Velg **Fullfør**.
3.  Velg **OK**.

Legg merke til at den opprettede konfigurasjonen er lagret som fullført versjon 1.

### <a name="configure-a-sample-model-mapping"></a>Konfigurere en eksempelmodelltilordning

#### <a name="create-an-er-model-mapping-configuration"></a>Opprette en ER-modelltilordningskonfigurasjon

1.  Velg **Opprett konfigurasjon** på siden **Konfigurasjoner**.
2.  I feltgruppen **Ny** i rullegardinboksen velger du alternativet **Modelltilordning basert på datamodellen Modell for å lære om tilordninger**.
3.  I **Navn**-feltet angir du **Tilordning (generelt)**.
4.  Velg **Inngangspunkt 1** i **Definisjon av datamodell**-feltet.
5.  Velg **Opprett konfigurasjon**.

Legg merke til at utkastversjon 1 av denne ER-konfigurasjonen er klar til redigering. Denne versjonen inneholder modelltilordningskomponenten.

#### <a name="design-a-sample-model-mapping"></a>Utforme en eksempelmodelltilordning

1.  Velg **Utforming** på siden **Konfigurasjoner**.

    Legg merke til at modelltilordningen for **Til modell**-retningstypen er automatisk lagt til i denne komponenten for definisjonen **Inngangspunkt 1**.
    
2.  Velg **Utforming** for å begynne å redigere den tillagte modelltilordningen.
3.  Velg **Rediger** i delen **Datamodell**.
4.  I feltet **Formel** angir du **"Generisk funksjonalitet 1"**.
5.  Velg **Lagre**.
6.  Lukk siden **Formelutforming**.

    ![Siden ER-utforming av modelltilordning](./media/RCS-Context-specific-mapping-Mapping1.PNG)

7.  Velg **Lagre**.
8.  Lukk siden **Modelltilordningsutforming**.
9.  Velg **Ny**.
10. Velg **Inngangspunkt 2** i **Definisjon**-feltet.
11. I **Navn**-feltet angir du **Tilordning (generelt) 2**.
12. Velg **Utforming**.
13. Velg **Rediger** i delen **Datamodell**.
14. I feltet **Formel** angir du **"Generisk funksjonalitet 2"**.
15. Velg **Lagre**.
16. Lukk siden **Formelutforming**.

    ![Siden ER-utforming av modelltilordning](./media/RCS-Context-specific-mapping-Mapping2.PNG)

17. Velg **Lagre**.
18. Lukk siden **Modelltilordningsutforming**.

    ![Siden ER-modelltilordninger](./media/RCS-Context-specific-mapping-Mappings.PNG)

19. Lukk siden **Modelltilordninger**.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Fullføre den endrede versjonen av modelltilordningskonfigurasjonen

1.  Velg **Endre status** i hurtigfanen **Versjoner** på **Konfigurasjoner-siden**.

    > Endre statusen for utformet modelltilordningskonfigurasjon fra **Kladd** til **Fullført**, slik at den kan brukes av ER-formater.

2.  Velg **Fullfør**.
3.  Velg **OK**.

Legg merke til at den opprettede konfigurasjonen er lagret som fullført versjon 1.

### <a name="configure-a-sample-format"></a>Konfigurere et eksempelformat

#### <a name="create-an-er-format-configuration"></a>Opprette en ER-formatkonfigurasjon

1.  På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Modell for å lære om tilordninger**.
2.  Velg **Opprett konfigurasjon**.
3.  I feltgruppen **Ny** i rullegardinboksen velger du alternativet **Format basert på datamodellen Modell for å lære om tilordninger**.
4.  I **Navn**-feltet angir du **Format for å lære om tilordninger**.
5.  Velg **Inngangspunkt 1** i **Definisjon av datamodell**-feltet.
6.  Velg **Opprett konfigurasjon**.

Legg merke til at utkastversjon 1 av denne ER-konfigurasjonen er klar til redigering. Denne versjonen inneholder formatkomponenten.

#### <a name="design-a-sample-format"></a>Utforme et eksempelformat

1.  Velg **Utforming** på siden **Konfigurasjoner**.
2.  Velg **Legg til rot**.
3.  I **Tekst**-gruppen velger du **Streng**-elementet.
4.  Velg **OK**.

#### <a name="bind-format-elements-to-a-data-source"></a>Binde formatelementer til en datakilde

1.  Utvid modelldatakilden på **Formatutforming**-siden i kategorien **Tilordning**.
2.  Velg **Funksjonsbeskrivelse**-feltet.
3.  Velg **Bind**.

    ![Side med ER-formatutforming](./media/RCS-Context-specific-mapping-Format.PNG)

4.  Velg **Lagre**.
5.  Lukk siden.

## <a name="appendix-2"></a><a name="appendix2"></a> Tillegg 2

### <a name="configure-a-sample-model-mapping-for-general-customization"></a>Konfigurere en eksempelmodelltilordning for generell tilpasning

Du vil kanskje tilpasse en modelltilordning som en konfigurasjonsleverandør (partner) har gitt deg, og deretter bruke den tilpassede versjonen som en datakilde for ER-formatene. I dette tilfellet må du opprette en egendefinert ER-modelltilordningskonfigurasjon for å utføre de nødvendige endringene i eksisterende modelltilordninger. Fremgangsmåtene i dette tillegget bruker modelltilordningen **Tilordning (generelt)** som et eksempel.

#### <a name="create-an-er-model-mapping-configuration"></a>Opprette en ER-modelltilordningskonfigurasjon

1.  På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Tilordning (generelt)**.
2.  Velg **Opprett konfigurasjon**.
3.  Velg **Avled fra navnet: Tilordning (generelt), Litware, Inc.** i rullegardinlisten i **Ny**-feltgruppen.
4.  I **Navn**-feltet angir du **Tilordning (generelt) egendefinert**.
5.  Velg **Opprett konfigurasjon**.

Legg merke til at utkastversjon 1 av denne ER-konfigurasjonen er klar til redigering.

#### <a name="design-a-sample-model-mapping"></a>Utforme en eksempelmodelltilordning

1.  Velg **Utforming** på siden **Konfigurasjoner**.

    > Legg merke til at modelltilordninger for grunnkonfigurasjonen er kopiert til denne konfigurasjonen automatisk.

2.  Velg tilordningen **Tilordning (generelt)**.
3.  Velg **Utforming**.
4.  Velg **Rediger** i delen **Datamodell**.
5.  I feltet **Formel** angir du **"Generisk funksjonalitet 1 egendefinert"**.
6.  Velg **Lagre**.
7.  Lukk siden.

    ![Siden ER-utforming av modelltilordning](./media/RCS-Context-specific-mapping-Mapping1Custom.PNG)

8.  Velg **Lagre**.
9.  Lukk siden.
10. Velg tilordningen **Tilordning (generelt) 2 kopi**.
11. Velg **Utforming**.
12. Velg **Rediger** i delen **Datamodell**.
13. I feltet **Formel** angir du **"Generisk funksjonalitet 2 egendefinert"**.
14. Velg **Lagre**.
15. Lukk siden.

    ![Siden ER-utforming av modelltilordning](./media/RCS-Context-specific-mapping-Mapping2Custom.PNG)

16. Velg **Lagre**.
17. Lukk siden.

    ![Siden ER-modelltilordninger](./media/RCS-Context-specific-mapping-MappingsCustom.PNG)

18. Lukk siden.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Fullføre den endrede versjonen av modelltilordningskonfigurasjonen

1.  Velg **Endre status** i hurtigfanen **Versjoner** på siden **Konfigurasjoner**.

    > Endre statusen for utformet modelltilordningskonfigurasjon fra **Kladd** til **Fullført**, slik at den kan brukes av ER-formater.

2.  Velg **Fullfør**.
3.  Velg **OK**.

Legg merke til at den opprettede konfigurasjonen er lagret som fullført versjon 1.

## <a name="appendix-3"></a><a name="appendix3"></a> Tillegg 3

### <a name="configure-a-sample-model-mapping-for-countryregion-specific-customization"></a>Konfigurere en eksempelmodelltilordning for land/områdespesifikk tilpasning

For noen ER-formater kan det være land-/områdespesifikke krav til klargjøring av data. I dette tilfellet kan du behandle en separat ER-modelltilordningskonfigurasjon og isolere implementeringen av disse land-/områdespesifikke kravene fra generell implementering. Fremgangsmåtene i dette tillegget bruker ER-formatet **Format for å lære om tilordninger** og franske spesifikke krav som et eksempel.

#### <a name="create-an-er-model-mapping-configuration"></a>Opprette en ER-modelltilordningskonfigurasjon

Først oppretter du en ny ER-modelltilordningskonfigurasjon for å implementere lands-/områdespesifikke krav. Bruk din egen tilpassede ER-modelltilordningskonfigurasjon som basis.

1.  På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Tilordning (generelt) egendefinert**.
2.  Velg **Opprett konfigurasjon**.
3.  Velg **Avled fra navnet: Tilordning (generelt) egendefinert, Litware, Inc.** i rullegardinlisten i **Ny**-feltgruppen.
4.  I **Navn**-feltet angir du **Tilordning (FR)**.
5.  Velg **Opprett konfigurasjon**.

Legg merke til at utkastversjon 1 av denne ER-konfigurasjonen er klar til redigering.

#### <a name="design-a-sample-model-mapping"></a>Utforme en eksempelmodelltilordning

1.  Velg **Utforming** på siden **Konfigurasjoner**.

    > Legg merke til at modelltilordninger for grunnkonfigurasjonen er kopiert til denne konfigurasjonen automatisk.

2.  Velg tilordningen **Tilordning (generelt) kopi**.
3.  Gi den det nye navnet **Tilordning (FR)**.
4.  Velg **Utforming**.
5.  Velg **Rediger** i delen **Datamodell**.
6.  I feltet **Formel** angir du **"FR-funksjonalitet 1"**.
7.  Velg **Lagre**.
8.  Lukk siden.

    ![Siden ER-utforming av modelltilordning](./media/RCS-Context-specific-mapping-Mapping1FR.PNG)

9.  Velg **Lagre**.
10. Lukk siden.
11. Velg tilordningen **Tilordning (generelt) 2 kopi**.
12. Gi den det nye navnet **Tilordning (FR) 2**.
13. Velg **Utforming**.
14. Velg **Rediger** i delen **Datamodell**.
15. I feltet **Formel** angir du **"FR-funksjonalitet 2"**.
16. Velg **Lagre**.
17. Lukk siden.

    ![Siden ER-utforming av modelltilordning](./media/RCS-Context-specific-mapping-Mapping2FR.PNG)

18. Velg **Lagre**.
19. Lukk siden.

    ![Siden ER-modelltilordninger](./media/RCS-Context-specific-mapping-MappingsFR.PNG)

20. Lukk siden.

#### <a name="specify-countryregion-context-restrictions-for-use"></a>Angi kontekstbegrensninger for land/område for bruk

1.  Velg **Ny** i hurtigfanen **ISO-land-/områdekoder** på **Konfigurasjoner**-siden.
2.  Velg **FR** i **ISO**-feltet.
3.  Velg **Lagre**.

Legg merke til at du må logge på et bestemt firma i Finance for å kjøre et ER-format. Derfor kan dette firmaet anses som en part som kontrollerer både ER-formatutførelse og valget av den riktige ER-modelltilordningen av den grunnleggende ER-datamodellen. Ved å legge til **FR**-landskoden angir du at denne modelltilordningen bare kan velges med et ER-format på basisdatamodellen når dette formatet kjøres under kontrollen av et firma som har fransk land/område-kontekst.

Du kan legge til flere lands-/områdekoder for en enkelt versjon av en ER-modelltilordningskonfigurasjon. På denne måten kan modelltilordninger som ligger i denne modelltilordningskonfigurasjonen, brukes for et ER-format som kjøres under kontroll over firmaer som har forskjellig land/område-kontekst.

Legg merke til at listen over land-/områdekoder er angitt for hver enkelt versjon av en ER-modelltilordningskonfigurasjon, og kan variere fra versjon til versjon.

#### <a name="complete-the-modified-version-of-the-model-mapping-configuration"></a>Fullføre den endrede versjonen av modelltilordningskonfigurasjonen

1.  Velg **Endre status** i hurtigfanen **Versjoner** på siden **Konfigurasjoner**.

    > Endre statusen for utformet modelltilordningskonfigurasjon fra **Kladd** til **Fullført**, slik at den kan brukes av ER-formater.

2.  Velg **Fullfør**.
3.  Velg **OK**.

Legg merke til at den opprettede konfigurasjonen er lagret som fullført versjon 1.

## <a name="additional-resources"></a>Tilleggsressurser

[Oversikt over elektronisk rapportering (ER)](general-electronic-reporting.md)

[Administrere ER-modelltilordning i separate ER-konfigurasjoner](./tasks/er-manage-model-mapping-configurations-july-2017.md)

[Bruke lands-/områdekontekst](../lcs-solutions/apply-country-context.md)

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

#### <a name="i-configured-two-shared-er-model-mapping-configurations-in-rcs-and-marked-one-of-them-as-the-default-model-mapping-configuration-i-successfully-ran-an-er-format-that-was-created-for-the-same-base-er-data-model-configuration-to-test-model-mappings-i-then-imported-the-whole-er-solution-er-data-model-two-er-model-mapping-configurations-and-er-format-configuration-into-finance-why-do-i-receive-an-error-message-when-i-try-to-run-the-same-er-format-in-finance"></a>Jeg konfigurerte to delte ER-modelltilordningskonfigurasjoner i RCS, og merket en av dem som standard modelltilordningskonfigurasjon. Jeg kjørte et ER-format som ble opprettet for den samme grunnleggende ER-datamodellkonfigurasjonen, for testing av modelltilordninger. Jeg importerte deretter hele ER-løsningen (ER-datamodell, to ER-modelltilordningskonfigurasjoner og ER-formatkonfigurasjon) til Finance. Hvorfor får jeg en feilmelding når jeg prøver å kjøre samme ER-format i Finance?
Standardinnstillingen for modelltilordning er miljøspesifikk. Den konfigureres i RCS, men eksporteres ikke til Finance. Hvis du skal kunne kjøre dette ER-formatet, må du merke én av ER-modelltilordningskonfigurasjonene som standardkonfigurasjon for modelltilordning i Finance.

#### <a name="i-configured-one-model-mapping-as-a-shared-model-mapping-and-completed-the-draft-version-of-it-i-then-added-a-new-model-mapping-configuration-for-same-data-model-and-configured-it-as-french-specific-why-is-the-shared-model-mapping-selected-when-i-run-an-er-format-even-though-this-er-format-uses-the-correct-root-definition-and-execution-is-done-under-the-control-of-the-company-that-has-french-countryregion-context"></a>Jeg konfigurerte én modelltilordning som en delt modelltilordning og fullførte utkastversjonen av den. Jeg la deretter til en ny modelltilordningskonfigurasjon for samme datamodell og konfigurerte den som fransk-spesifikk. Hvorfor blir den delte modelltilordningen valgt når jeg kjører et ER-format, selv om dette ER-formatet bruker riktig rotdefinisjon og kjøringen utføres under kontroll av firmaet som har fransk land/område-kontekst?
Kontroller at den delte modelltilordningskonfigurasjonen ikke er merket som standard modelltilordningskonfigurasjon. Hvis ikke vil den ha høyere prioritet under tilordningsvalg. Kontroller også at den fransk-spesifikke modelltilordningskonfigurasjon vurderes når det velges en tilordning under kjøring av ER-format. En ER-modelltilordningskonfigurasjon er bare tilgjengelig for valg hvis minst én av følgende betingelser er oppfylt:
- Minst én versjon av ER-modellkonfigureringskonfigurasjonen har enten **Fullført** eller **Delt** status. I dette tilfellet vil versjonen med det høyeste versjonsnummeret bli brukt til ER-format-utførelse.
- Alternativet **Kjøringsutkast** for ER-modelltilordningskonfigurasjonen er aktivert. I dette tilfellet vil versjonen som har **Utkast**-status, bli brukt til ER-format-utførelse.
> Alternativet **Kjøringsutkast** blir tilgjengelig på **Konfigurasjoner**-siden for hver ER-modelltilordningskonfigurasjon når ER-brukerparameteren **Kjøringsinnstilling** er aktivert.
