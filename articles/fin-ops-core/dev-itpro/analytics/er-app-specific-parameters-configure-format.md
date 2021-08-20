---
title: Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet
description: Dette emnet forklarer hvordan du kan konfigurere elektroniske rapporter (ER)-formater til å bruke parametere som angis per juridisk enhet.
author: NickSelin
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERSolutionTable, EROperationDesigner, ERLookupDesigner, ERComponentLookupStructureEditing
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2019-01-01
ms.dyn365.ops.version: Release 8.1.3
ms.openlocfilehash: 2bf4d1ecad3e25299df7c87ffa2236736ddcac300a5ded779616b25920745d7e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765838"
---
# <a name="configure-er-formats-to-use-parameters-that-are-specified-per-legal-entity"></a>Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet

[!include[banner](../includes/banner.md)]

## <a name="overview"></a>Oversikt

I mange av formatene for elektronisk rapportering (ER) som du vil utforme, må du filtrere data ved hjelp av et verdisett som er spesifikke for hver juridiske enhet for forekomsten (for eksempel et sett med mva-koder for å filtrere mva-transaksjoner). Når filtrering av denne typen er konfigurert i et ER-format, brukes verdier som er avhengige av den juridiske enheten (for eksempel skattekoder) i uttrykk med ER-formatet for å angi datafiltreringsregler. Derfor er formatet opprettet juridisk enhet-spesifikt, og hvis du vil generere de nødvendige rapportene, må du opprette avledede kopier av det opprinnelige ER-formatet for hver juridiske enhet der du må kjøre ER-formatet. Hvert avledede ER-format må redigeres for å hente juridisk enhet-spesifikke verdier til den, basert på nytt når den opprinnelige versjonen (basis) er oppdatert, eksportert fra et testmiljø og importeres til et produksjonsmiljø når det må distribueres for produksjonsbruk, og så videre. Derfor er vedlikehold av denne typen konfigurert ER-løsning kompleks og tidkrevende av flere årsaker:

-   Jo flere juridiske enheter det er, jo flere ER-formatkonfigurasjoner må vedlikeholdes.
-   Vedlikehold av ER-konfigurasjoner krever at bedriftsbrukere har kjennskap til ER.

De ER-programspesifikke parameterne gjør det mulig for privilegerte brukere å konfigurere datafiltrering i et ER-format slik at det er basert på et sett med abstrakte regler. Dette settet med regler kan konfigureres til å bruke datakildene som er tilgjengelige i et ER-format. Forretningsbrukere kan deretter angi reelle regler utenfor ER-rammeverket ved hjelp av brukergrensesnittet som automatisk genereres basert på innstillingene i det tilsvarende ER-formatet, og de gjeldende dataene for juridisk enhet blir åpnet av datakildene for ER-formatet. Regelsettet som er angitt for et ER-format, kan eksporteres fra den gjeldende juridiske enheten for Dynamics 365 Finance (Finance)-forekomsten. Det kan deretter importeres til en annen juridisk enhet av enten samme Finance-forekomst eller en annen forekomst som et sett med regler for samme ER-format.

## <a name="prerequisites"></a>Forutsetninger

For å fullføre eksemplene i dette emnet må du har tilgang til forekomsten av Regulatory Configuration Service (RCS) som er klargjort for samme leietaker som Finance and Operations, for én av følgende roller:

- Utvikler av elektronisk rapportering
- Funksjonell konsulent for elektronisk rapportering
- Systemansvarlig

Vi anbefaler at du fullfører trinnene i emnet [Støtte for parametriserte kall av ER-datakilder av felttypen Beregnet](er-calculated-field-type.md). Hvis du allerede har fullført disse trinnene, kan du hoppe over trinnene i **Importere ER-konfigurasjoner til RCS**.

## <a name="import-er-configurations-into-rcs"></a>Importere ER-konfigurasjoner til RCS

Last ned og lagre følgende ER-konfigurasjoner lokalt:

| **Innholdsbeskrivelse**                        | **Filnavn**                                        |
|------------------------------------------------|------------------------------------------------------|
| Eksempel på konfigurasjonsfilen **ER-datamodell**    | [Modell for å lære om parameterkall.versjon.1.XML](https://download.microsoft.com/download/2/d/b/2db913a0-3622-494e-91a2-97fc494af9b9/Modeltolearnparameterizedcalls.version.1.xml)     |
| Eksempel på konfigurasjonsfilen **ER-metadata**      | [Metadata for å lære om parameterkall.versjon.1.XML](https://download.microsoft.com/download/1/b/3/1b343968-5a47-4000-b5a8-6487698ef4c0/Metadatatolearnparameterizedcalls.version.1.xml)  |
| Eksempel på konfigurasjonsfilen **ER-modelltilordning** | [Tilordning for å lære om parameterkall.versjon.1.1.XML](https://download.microsoft.com/download/8/6/6/866e0ab6-2e05-4d98-9d52-d2da2038f6e4/Mappingtolearnparameterizedcalls.version.1.1.xml) |
| Eksempel på **ER-format**-konfigurasjon             | [Format for å lære om parameterkall.versjon.1.1.XML](https://download.microsoft.com/download/e/3/9/e392eadc-b9b4-4834-95c3-b8066dd00b9c/Formattolearnparameterizedcalls.version.1.1.xml)  |

Logg deretter på RCS-forekomsten.

I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet Litware, Inc. Før du kan fullføre trinnene i denne prosedyren må du fullføre prosedyren i emnet [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md) i RCS.

1.  Velg **Elektronisk rapportering** på standard instrumentbord.
2.  Velg **Rapporteringskonfigurasjoner**.
3.  Importer de nedlastede ER-konfigurasjonene til RCS i følgende rekkefølge: datamodell, metadata, modelltilordning, format. For hver ER-konfigurasjon følger du disse trinnene:

    1.  Velg **Veksle**.
    2.  Velg **Last fra XML-fil**.
    3.  Velg **Bla gjennom** for å velge den riktige filen for den nødvendige ER-konfigurasjonen i XML-format.
    4.  Velg **OK**.

## <a name="review-the-er-solution-that-is-provided"></a>Se gjennom den angitte ER-løsningen

1.  I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.
2.  Velg elementet **Format for å lære om parameterkall**.
3.  Velg **Utforming**.
4.  Velg **Vis/skjul**.

    ER-formatet **Format for å lære om parameterkall** er utformet for å generere en skatteoppgave i XML-format som viser flere nivåer med avgifter (vanlig, redusert og ingen). Hvert nivå har et ulikt antall detaljer.

    ![Flere nivåer av ER-format. Format for å lære parameteriserte samtaler.](./media/RCS-AppSpecParms-ReviewFormat.PNG)

5.  Utvid elementene **Modell**, **Data** og **Sammendrag** i kategorien **Tilordning**.

    Datakilden **Model.Data.Summary** returnerer listen over mva-transaksjoner. Disse transaksjonene er oppført etter mva-kode. For denne datakilden er det beregnede **Model.Data.Summary.Level**-feltet konfigurert til å returnere koden for avgiftsnivået for hver summerte post. For alle avgiftskoder som kan hentes fra **Model.Data.Summary**-datakilden ved kjøretid, returnerer det beregnede feltet avgiftsnivåkode (**Vanlig**, **Redusert**, **Ingen** eller **Annet**) som en tekstverdi. Det beregnede **Model.Data.Summary.Level**-feltet brukes til å filtrere poster for **Model.Data.Summary**-datakilden og angi de filtrerte dataene i hvert XML-element som representerer et avgiftsnivå ved hjelp av feltene **Model.Data2.Level1**, **Model.Data2.Level2** og **Model.Data2.Level3**.

    ![Datakildelisten Model.Data.Summary over mva-transaksjoner.](./media/RCS-AppSpecParms-ReviewFormat-Data2Fld.PNG)

    Det beregnede **Model.Data.Summary.Level**-feltet er konfigurert slik at det inneholder et ER-uttrykk. Avgiftskoder (**VAT19**, **InVAT19**, **VAT7**, **InVAT7**, **THIRD** og **InVAT0**) er hardkodet til denne konfigurasjonen. Derfor er dette ER-formatet avhengig av den juridiske enheten der disse avgiftskodene ble konfigurert.

    ![Det beregnede feltet Model.Data.Summary.Level med hardkodede avgiftskoder.](./media/RCS-AppSpecParms-ReviewFormat-LevelFld.PNG)

    Hvis du vil støtte et annet sett med mva-koder for hver juridiske enhet, må du følge denne fremgangsmåten:

    - Opprett en avledet versjon av ER-formatet for hver juridiske enhet.
    - Oppdater avgiftskodene i det beregnede **Model.Data.Summary.Level**-feltet, basert på innstillingen for juridisk enhet.

6.  Lukk **Formatutforming**-siden.

## <a name="create-a-derived-format"></a>Opprette et avledet format

Deretter skal du bruke funksjonen for ER-programspesifikke parametere til å støtte et annet sett med mva-koder for hver juridiske enhet i ett enkelt ER-format.

1.  I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.
2.  Velg elementet **Format for å lære om parameterkall**.
3.  Velg **Opprett konfigurasjon**.
4.  Velg alternativet **Avled fra navn: Format for å lære om parameterkall, Microsoft**.
5.  I **Navn**-feltet angir du **Format for å lære hvordan du slår opp LE-data**.
6.  Velg **Opprett konfigurasjon**.

## <a name="configure-a-derived-format"></a>Konfigurere et avledet format

### <a name="add-a-format-enumeration"></a>Legge til en formatopplisting

Deretter legger du til en ny ER-formatopplisting. Verdiene for denne formatopplistingen vil bli presentert for forretningsbrukere, som vil angi juridisk enhetsavhengige sett med mva-koder for de ulike avgiftsnivåene som brukes i ER-formatet.

1.  Velg **Utforming**.
2.  Velg **Formatopplistinger**.
3.  Velg **Legg til**.
4.  I **Navn**-feltet angir du **Liste over avgiftsnivåer**.
5.  Velg **Lagre**.
6.  Velg **Legg til** i kategorien **Verdier for formatopplisning**.
7.  I **Navn**-feltet angir du **Vanlig avgift**.
8.  Velg **Legg til** på nytt.
9.  I **Navn**-feltet angir du **Redusert avgift**.
10. Velg **Legg til** på nytt.
11. I **Navn**-feltet angir du **Ingen avgift**.
12. Velg **Legg til** på nytt.
13. Angi **Annet** i **Navn**-feltet.

    ![Ny post på Format-opplistingssiden.](./media/RCS-AppSpecParms-ConfigureFormat-Enum.PNG)

    Siden forretningsbrukerne kan bruke forskjellige språk til å angi juridisk enhetsavhengige sett med avgiftskoder, anbefaler vi at du oversetter verdiene for denne opplistingen til språkene som er konfigurert som foretrukne språk for disse brukerne i Økonomimodulen.

14. Velg posten **Ingen avgift**.
15. Klikk i **Etikett**-feltet.
16. Velg **Oversett**.
17. Angi **LBL_LEVELENUM_NO** i **Tekstoversettelse**-ruten i **Etikett-ID**-feltet.
18. I feltet **Tekst på standardspråk** angir du **Ingen avgift**.
19. I **Språk**-feltet velger du **DE**.
20. I **Oversatt tekst**-feltet angir du **keine Besteuerung**.
21. Velg **Oversett**.

    ![Lysbilde ut for tekstoversetting.](./media/RCS-AppSpecParms-ConfigureFormat-EnumTranslate.PNG)

22. Velg **Lagre**.
23. Lukk **Formatopplistinger**-siden.

### <a name="add-a-new-lookup-data-source"></a>Legg til en ny datakilde for oppslag

Deretter legger du til en ny datakilde for å angi hvordan forretningsbrukere skal angi juridisk enhetsavhengige relger for å gjenkjenne det riktige avgiftsnivået for hver summerte transaksjonsoppføring.

1.  Velg **Legg til** i **Tilordning**-fanen.
2.  Velg **Formatopplisting\Oppslag**.

    Du har nettopp identifisert at hver regel som forretningsbrukere angir for avgiftsnivågjenkjenning vil returnere en verdi for en ER-formatopplisting. Legg merke til at du får tilgang til **Oppslag**-datakildetypen under **Datamodell** og **Dynamics 365 for Operations**-blokker i tillegg til **Formatopplisning**-blokken. Derfor kan det brukes ER-datamodellopplistinger og programopplisninger til å angi typen verdier som returneres for datakilder av denne typen. Hvis du vil lære mer om **Oppslag**-datakildene, kan du se [Konfigurer Oppslag-datakilder for å bruke funksjonen for ER-programspesifikke parametere](er-lookup-data-sources.md).
    
3.  Angi **Velger** i **Navn**-feltet.
4.  I **Formatopplisning**-feltet velger du **Liste over avgiftsnivåer**.

    Du har angitt at en forretningsbruker må velge en av verdiene i formatopplisningen **Liste over avgiftsnivåer** som en retur verdi for hver regel som er angitt i denne datakilden.
    
5.  Velg **Rediger oppslag**.
6.  Velg **Kolonner**.
7.  Vis elementet **Model**.
8.  Vis elementet **Data**.
9.  Vis elementet **Avgift**.
10. Velg elementet **Model.Data.Tax.Code**.
11. Velg **Legg til**-knappen (høyre pilen).

    ![Kolonner lysbilde ut.](./media/RCS-AppSpecParms-ConfigureFormat-Lookup1.PNG)

    Du har akkurat angitt at en forretningsbruker må velge en av avgiftskodene som en betingelse for hver regel som er angitt i denne datakilden for avgiftsnivågjenkjenning. Listen over avgiftskoder som firmabrukeren kan velge, vil bli returnert av **Model.Data.Tax**-datakilden. Siden denne datakilden inneholder **Navn**-feltet, vises navnet på mva-koden for hver mva-kodeverdi i oppslaget som presenteres for forretningsbrukeren.
    
12. Velg **OK**.

    ![Oppslagsutformingsside.](./media/RCS-AppSpecParms-ConfigureFormat-Lookup2.PNG)

    Forretningsbrukere kan legge til flere regler som poster i denne datakilden. Hver post vil bli nummerert med en linjekode. Regler vil bli evaluert i stigende linjenummer.

    Fordi du valgte **Mva-kode**-feltet som en betingelse for regler i denne oppslagsdatakilden, og fordi **Mva-kode** er definert som et felt av **Streng**-datatypen, evalueres hver regel ved kjøring ved å sammenligne avgiftskoden som sendes til datakilden med mva-koden som er definert i denne posten for datakilden.

    Når en regel som er i samsvar med den konfigurerte betingelsen, blir funnet, returnerer denne datakilden oppslagsverdien for regelen som er definert i **Oppslagsresultat**-feltet. Hvis ingen regel blir funnet, oppstår det et unntak for å varsle brukeren om at den gjeldende datakilden ikke kan returnere en riktig verdi.

13. Velg **Lagre**.
14. Lukk **Oppslagsutforming**-siden.
15. Velg **OK**.

    Legg merke til at du har lagt til en ny datakilde som returnerer avgiftsnivået som verdien for formatopplistingen **Liste over avgiftsnivåer** for en mva-kode som sendes til datakilden som argument for **kode**-parameteren til datatypen **streng**.
    
    ![Formatutformingsside med en ny datakilde.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld.PNG)

    Evalueringen av konfigurerte regler avhenger av datatypen til feltene som er valgt for å definere betingelsene for disse reglene. Når du velger et felt som er konfigurert som et felt enten for datatypen **numerisk** eller **dato**, vil vilkårene være forskjellige fra vilkårene som ble beskrevet tidligere for datatypen **streng**. For **numerisk**- og **data**-felt må regelen angis som et verdiområde. Betingelsen for regelen vil da anses som oppfylt når en verdi som sendes til datakilden, er i det konfigurerte området.
    
    Illustrasjonen nedenfor viser et eksempel på denne typen oppsett. I tillegg til **Model.Data.Tax.Code**-feltet i **streng**-datatypen brukes **Model.Tax.Summary.Base**-feltet for **Real**-datatypen til å angi betingelser for en oppslagsdatakilde.
    
    ![Oppslagsutformingsside med tilleggskolonner.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFld2.PNG)

    Fordi feltene **Model.Data.Tax.Code** og **Model.Tax.Summary.Base** er valgt for denne oppslagsdatakilden, konfigureres hver regel for denne datakilden på følgende måte:
    
    -   I listen som vises, må verdien i formatopplistingen **Liste over avgiftsnivåer** velges som en returnert verdi.
    -   Mva-koden må angis som en betingelse for denne regelen. Bare avgiftskoder som tilbys av modellen **Model.Data.Tax**-datakilden, er gjeldende.
    -   Minimums- og maksimumsverdiene for avgiftsgrunnlagsbeløpet må angis som betingelser for denne regelen.

    Slik blir hver regel i denne datakilden evaluert ved kjøretid:
    -   Er koden for **streng**-datatypen som ble sendt til denne datakilden, lik mva-koden for en regel?
    -   Faller verdien av **Real**-datatypen som ble sendt til denne datakilden, mellom bestemte minimums- og maksimumsverdier?

    En regel blir ansett som gjeldende når begge betingelser er oppfylt.

### <a name="translate-the-label-of-the-lookup-data-source-that-was-added"></a>Oversett etiketten til oppslagsdatakilden som ble lagt til

Siden forretningsbrukerne kan bruke forskjellige språk til å angi juridisk enhetsavhengige sett med avgiftskoder, anbefaler vi at du oversetter etiketten for alle oppslagsdatakilder du legger til, slik at den presenteres på hver brukes foretrukne språk på den tilsvarende siden.

1.  Velg **Model.Data.Selector**-datakilden.
2.  Velg **Rediger**.
3.  Klikk i **Etikett**-feltet.
4.  Velg **Oversett**.
5.  Angi **LBL_SELECTOR_DS** i **Tekstoversettelse**-ruten i **Etikett-ID**-feltet.
6.  I feltet **Tekst på standardspråk** angir du **Velg skattenivå etter mva-kode**.
7.  I **Språk**-feltet velger du **DE**.
8.  I **Oversatt tekst**-feltet angir du **Steuerebene für Steuerkennzeichen auswählen**.
9.  Velg **Oversett**.
10. Velg **OK**.

    ![Datakildeegenskaper dras ut.](./media/RCS-AppSpecParms-ConfigureFormat-SelectorFldTranslate.PNG)

### <a name="add-a-new-field-to-consume-the-configured-lookup"></a>Legg til et nytt felt for å bruke det konfigurerte oppslaget

1.  Vis elementet **Model.Data**.
2.  Velg elementet **Model.Data.Tax.Summary**.
3.  Velg **Legg til**.
4.  Velg **Funksjoner/Beregnet felt**.
5.  I **Navn**-feltet angir du **LevelByLookup**.
6.  Velg **Rediger formel**.
7.  I **Formel**-feltet angir du **Model.Selector(Model.Data.Summary.Code)**.
8.  Velg **Lagre**.

    ![Legg til Model.Selector(Model.Data.Summary.Code) på Formeldesigner-siden.](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld.PNG)

9.  Lukk siden **Formelredigering**.
10. Velg **OK**.

    ![Formatutformingsside med ny formel lagt til.](./media/RCS-AppSpecParms-ConfigureFormat-AddLevelByLookupFld2.PNG)

    Legg merke til at det beregnede **LevelByLookup**-feltet som du la til, returnerer avgiftsnivået som verdien for formatopplistingen **Liste over avgiftsnivåer** for hver summerte avgiftstransaksjonsoppføring. Mva-koden for posten vil bli sendt til **Model.Selector**-oppslagsdatakilden, og settet med regler for denne datakilden blir brukt til å velge riktig avgiftsnivå.

### <a name="add-a-new-format-enumeration-based-data-source&quot;></a>Legg til en ny formatopplistingsbasert datakilde

Deretter legger du til en ny datakilde som refererer til formatopplistingen du la til tidligere. Verdier i denne datakilden vil bli brukt i et ER-formatuttrykk senere.

1.  Velg **Legg til rot**.
2.  Velg **Formatopplistinger\Opplisting**.
3.  I **Navn**-feltet angir du **Avgiftsnivå**.
4.  I **Formatopplisning**-feltet velger du **Liste over avgiftsnivåer**.
5.  Velg **Lagre**.

### <a name=&quot;modify-an-existing-field-to-start-to-use-the-lookup&quot;></a>Endre et eksisterende felt for å begynne å bruke oppslaget

Deretter skal du endre det eksisterende beregnede feltet slik at det bruker den konfigurerte oppslagsdatakilden til å returnere den riktige avgiftsnivåverdien, avhengig av mva-koden.

1.  Velg elementet **Model.Data.Summary.Level**.
2.  Velg **Rediger**.
3.  Velg **Rediger formel**.

    Legg merke til at gjeldende uttrykk for **Model.Data.Summary.Level**-feltet inkluderer følgende hardkodede mva-koder:
    
    CASE (@.Code, &quot;VAT19&quot;, &quot;Vanlig&quot;, &quot;InVAT19&quot;, &quot;Vanlig&quot;, &quot;VAT7&quot;, &quot;Reduced&quot;, &quot;InVAT7&quot;, &quot;Redusert&quot;, &quot;THIRD&quot;, &quot;Ingen&quot;, &quot;InVAT0&quot;, &quot;Ingen&quot;, &quot;Annet")

4.  I **Formel**-feltet angir du **CASE(@.LevelByLookup, TaxationLevel.'Regular taxation', "Vanlig", TaxationLevel.'Reduced taxation', "Redusert", TaxationLevel.'No taxation', "Ingen", "Annet")**.

    ![Side med ER-operasjonsutforming.](./media/RCS-AppSpecParms-ConfigureFormat-ChangeLookupFld.PNG)
    
    Legg merke til at uttrykket for **Model.Data.Summary.Level**-feltet nå returnerer avgiftsnivået, basert på mva-koden for den gjeldende posten og regelsettet som en forretningsbruker konfigurerer, i oppslagsdatakilden **Model.Data.Selector**.
    
5.  Velg **Lagre**.
6.  Lukk siden **Formelutforming**.
7.  Velg **OK**.
8.  Velg **Lagre**.
9.  Lukk siden **Formatutforming**.

## <a name="complete-the-draft-version-of-a-derived-format"></a>Fullfør utkastversjonen av et avledet format

1.  På hurtigfanen **Versjoner** velger du **Endre status**.
2.  Velg **Fullfør**.
3.  Velg **OK**.

## <a name="export-completed-version-of-modified-format"></a>Eksporter fullført versjon av et endret format

1.  I konfigurasjonstreet velger du elementet **Format for å lære hvordan du slår opp LE-data**.
2.  På hurtigfanen **Versjoner** velger du posten med statusen **Fullført**.
3.  Velg **Veksle**.
4.  Velg **Eksporter som XML-fil**.
5.  Velg **OK**.
6.  Nettleseren laster ned filen **Format for å lære hvordan du slår opp LE-data.xml**. Lagre denne filen lokalt.

Gjenta trinn i denne delen for overordnede elementer i formatet **Format for å lære hvordan du slår opp LE-data**, og lagre følgende filer lokalt:

-   Format for å lære om parameterkall.xml
-   Tilordning for å lære om parameterkall.xml
-   Modell for å lære om parameterkall.xml

Hvis du vil lære hvordan du bruker det konfigurerte ER-formatet **Format for å lære hvordan du slår opp LE-data** til å definere juridisk enhetsavhengige sett med mva-koder for å filtrere mva-transaksjoner etter ulike avgiftsnivåer, må du fullføre trinnene i emnet [Definere parameterne for et ER-format per juridisk enhetdataenhet](er-app-specific-parameters-set-up.md).

## <a name="additional-resources"></a>Tilleggsressurser

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Definere parameterne for et ER-format per juridisk enhet](er-app-specific-parameters-set-up.md)

[Konfigurer Oppslag-datakilder for å bruke funksjonen for ER-programspesifikke parametere](er-lookup-data-sources.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
