---
title: Støtte for parameterkall fra ER-datakilder for Beregnet felt-typen
description: Dette emnet inneholder informasjon om hvordan du bruker Beregnet felt-typen for ER-datakilder.
author: NickSelin
ms.date: 08/06/2020
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
ms.openlocfilehash: fb09e1ccd4b2be08e43784330adf4092ca25f5a6
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349166"
---
# <a name="support-parameterized-calls-of-er-data-sources-of-the-calculated-field-type"></a>Støtte for parameterkall fra ER-datakilder for Beregnet felt-typen

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du kan utforme en datakilde for elektronisk rapportering (ER) ved hjelp **Beregnet felt**-typen. Denne datakilden kan inneholde et ER-uttrykk som, når det kjøres, kan kontrolleres av verdiene til parameterargumentene som er konfigurert i en binding som kaller opp denne datakilden. Ved å konfigurere parametriske kall for en slik datakilde, kan du gjenbruke én enkelt datakilde i mange bindinger, noe som reduserer det totale antallet datakilder som må konfigureres i ER-modelltilordninger eller ER-formater. Den forenkler også den konfigurerte ER-komponenten, noe som reduserer vedlikeholdskostnadene og kostnadene for bruk av andre forbrukere.

## <a name="prerequisites"></a>Forutsetninger
Hvis du vil fullføre eksemplene i dette emnet, må du ha følgende tilgang:

- Tilgang til én av disse rollene:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

- Tilgang til Regulatory Configuration Services (RCS) som er klargjort for samme leietaker som Finance and Operations, for én av følgende roller:

    - Utvikler av elektronisk rapportering
    - Funksjonell konsulent for elektronisk rapportering
    - Systemansvarlig

Du må også laste ned og lagre følgende filer lokalt.

| **Innhold**                           | **Filnavn**                                        |
|---------------------------------------|------------------------------------------------------|
| Eksempel ER-datamodellkonfigurasjon    | [Modell for å lære om parameterkall.versjon.1.XML](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)     |
| Eksempel ER-metadatakonfigurasjon      | [Metadata for å lære om parameterkall.versjon.1.XML](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |
| Eksempel ER-modelltilordningskonfigurasjon | [Tilordning for å lære om parameterkall.versjon.1.1.XML](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg) |
| Eksempel ER-formatkonfigurasjon        | [Format for å lære om parameterkall.versjon.1.1.XML](https://mbs.microsoft.com/customersource/global/AX/downloads/hot-fixes/365optelecrepeg)  |

## <a name="sign-in-to-your-rcs-instance"></a>Logge på RCS-forekomsten
I dette eksemplet skal du opprette en konfigurasjon for eksempelfirmaet, Litware, Inc. Først må du fullføre disse trinnene i RCS i fremgangsmåten [Opprette konfigurasjonsleverandører og merke dem som aktive](tasks/er-configuration-provider-mark-it-active-2016-11.md):

1. Velg **Elektronisk rapportering** på standard instrumentbord.
2. Velg **Rapporteringskonfigurasjoner**.
3. Importer de nedlastede konfigurasjonene til RCS i følgende rekkefølge: datamodell, metadata, modelltilordning, format. Fullfør trinnene nedenfor for hver ER-konfigurasjon:

    1. Velg **Veksle**.
    2. Velg **Last fra XML-fil**.
    3. Velg **Bla gjennom**, og velg deretter den nødvendige ER-konfigurasjonen i XML-format.
    4. Velg **OK**

## <a name="review-the-provided-er-solution"></a>Se gjennom den angitte ER-løsningen

### <a name="review-model-mapping"></a>Se gjennom modelltilordning

1. I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.
2. Velg **Tilordning for å lære om parameterkall**.
3. Velg **Utforming**.
4. Velg **Utforming**.  
   
    Denne ER-modelltilordningen er utformet for å gjøre følgende:

    - Hent listen over avgiftskoder (datakilden **Avgift**) som finnes i **TaxTable**-tabellen.
    - Hent listen over avgiftstransaksjoner (datakilden **Trans**) som finnes i **TaxTrans**-tabellen:
    
        - Grupper listen over hentede transaksjoner (datakilden **Gr**) etter avgiftskode.
        - Beregn for grupperte transaksjoner etter aggregerte verdier per avgiftskode:

            - Summen av basisverdier for avgift.
            - Summen av verdier for avgift.
            - Minimumsverdi for brukt avgiftssats.

    Modelltilordningen i denne konfigurasjonen implementerer basisdatamodellen for alle ER-formatene som opprettes for denne modellen og som kjøres i Finance and Operations. Derfor vil inneholder i datakildene **Avgift** og **Gr** bli eksponert for ER-formater, for eksempel abstrakte datakilder.

    ![Siden Modelltilordningsutforming viser datakildene Avgift og Gr.](media/er-calculated-field-type-01.png)

5.  Lukk siden **Modelltilordningsutforming**.
6.  Lukk siden **Modelltilordning**.

### <a name="review-format"></a>Gjennomgangsformat

1. I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.
2. Velg **Format for å lære om parameterkall**.
3. Velg **Utforming**. Dette ER-formatet er utformet for å gjøre følgende:

    - Generer en avgiftsoppgave i XML-format.
    - Presenter følgende nivåer for avgifter i avgiftsoppgaven: vanlig, redusert og ingen.
    - Presenter flere detaljer for hvert avgiftsnivå med ulikt antall detaljer på hvert nivå.

    ![Formatutformingsside.](media/er-calculated-field-type-02.png)

4. Velg **Tilordning**.
5. Vis elementene **Model**, **Data,** og **Summary**. 

    Det beregnede feltet **Model.Data.Summary.Level** inneholder uttrykket som returnerer koden for avgiftsnivået (**Vanlig**, **Redusert**, **Ingen** eller **Annet**) som en tekstverdi for avgiftskoder som kan hentes fra datamodellen **Model.Data.Summary** ved kjøretid.

    ![Siden Formatutforming som viser detaljer for datamodellen Modell for å lære om parameterkall.](media/er-calculated-field-type-03.png)

6. Vis elementet **Model**.**Data2**.
7. Vis elementet **Model**.**Data2.Summary2**.
   
    Datakilden **Model**.**Data2.Summary2** konfigureres til å gruppere transaksjonsdetaljene for datakilden **Model.Data.Summary** etter avgiftsnivå (returneres av det beregnede feltet **Model.Data.Summary.Level**) og beregne aggregeringene.

    ![Siden Formatutforming som viser detaljer om datakilden Model.Data2.Summary2.](media/er-calculated-field-type-04.png)

8. Gå gjennom de beregnede feltene **Model**.**Data2.Level1**, **Model**.**Data2.Level2** og **Model**.**Data2.Level3.** Disse beregnede feltene brukes til å filtrere postlistene **Model**.**Data2. Summary2** og bare returnere poster som representerer et bestemt avgiftsnivå.
9. Lukk **Formatutforming**-siden.

## <a name="create-a-derived-format"></a>Opprette et avledet format
Du kan forbedre det angitte formatet ved å legge til ett beregnet felt for å filtrere det nødvendige avgiftsnivået i stedet for å bruke de eksisterende tre feltene: **Model**.**Data2.Level1**, **Model**.**Data2.Level2** og **Model**.**Data2.Level3**. Nødvendig avgiftsnivå kan angis der dette nye beregnede feltet vil bli kalt.

1. I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.
2. Velg **Format for å lære om parameterkall**.
3. Velg **Opprett konfigurasjon**.
4. Velg **Avled fra navn: Format for å lære om parameterkall, Microsoft**.
5. I **Navn**-feltet angir du **Format for å lære om parameterkall (tilpasset)**.
6. Velg **Opprett konfigurasjon**

## <a name="configure-a-parameterized-calculated-field-that-returns-a-list-of-records"></a>Konfigurere et parameterberegnet felt som returnerer en liste med poster

### <a name="start-adding-a-new-calculated-field"></a>Begynne å legge til et nytt beregnet felt

1. Velg **Utforming**.
2. Velg **Vis/skjul** for å vise alle formatelementer.
3. Velg **Tilordning**.
4. Vis elementet **Model**.
5. Velg elementet **Model.Data2**.
6. Velg **Legg til**.
7. Velg **Funksjoner\\Beregnet felt**.
8. Angi **Nivåer** i **Navn**-feltet.
9. Velg **Rediger formel**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Definere en parameter for å legge til et beregnet felt

1. Velg **Parametre**.
2. Velg **Ny**.
3. I **Navn**-feltet angir du **Avgiftsnivå**.
4. Velg **Streng** i **Type**-feltet.

    Bare primitive datatyper kan brukes til å angi typen for parameterens argument. Derfor kan ikke typene **Postliste**, **Post** og **Opplisting** brukes til dette formålet.

    Det maksimale antallet parametere som kan angis for ett enkelt beregnet felt er 8.

    ![Kildeliste for parameterdata.](media/er-calculated-field-type-05.png)

5. Velg **OK**.

Ved å legge til denne parameteren angir du betingelsen som må være tilstede for å kalle dette beregnede feltet. Når du kaller dette beregnede feltet, må du sette argumentet for parameteren **Avgiftsnivå** til en verdi i **Streng**-format.

   Pass på at du bare definerer parametere for de beregnede feltene som finnes seg i en container (enten **Postliste**, **Post** eller **Container**).

   Den konfigurerte parameteren er tilgjengelig i listen over datakilder for dette beregnede feltet. Du kan legge til parameteren i det konfigurerte uttrykket ved å velge **Legg til datakilde**.

   ![Datakildefelt.](media/er-calculated-field-type-06.png)

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Definere et uttrykk for å legge til et beregnet felt

1. I **Formel**-feltet angir du: 

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level =**
    
2. Velg parameteren **Avgiftsnivå** i listen over datakilder.
3. Velg **Legg til datakilde**.
4. I **Formel**-feltet fullfører du uttrykket slik:  

    **WHERE(\@.Summary2, \@.Summary2.grouped.Level = 'Avgiftsnivå')**

5. Velg **Lagre**.

    ![Informasjon for datakildefelt.](media/er-calculated-field-type-07.png)

6. Lukk siden **Formelutforming**.

### <a name="finish-adding-a-new-calculated-field"></a>Fullfør å legge til et nytt beregnet felt

- Velg **OK**.

På siden **Formatutforming** krever det konfigurerte parameterberegnede feltet **Nivåer** et **Streng**-argument.

![Vist liste over nivåer for beregnede felt.](media/er-calculated-field-type-08.png)

### <a name="use-the-configured-calculated-field-for-binding-format-elements"></a>Bruke det konfigurerte beregnede feltet til binding av formatelementer

1. Velg **Model.Data2.Levels** for å velge det konfigurerte beregnede feltet.
2. Velg formatelementet **Statement.Taxation.Regular**.
3. Velg **Bind**.
4. Velg **Ja** for å bekrefte veksling av gjeldende brukerdatakilde, **Level1**, til den nye datakilden, **Levels**, i alle kjedede formatelementer i det valgte formatelementet.

    Brukt binding er bygget som et kall til det parameterberegnede feltet. Som standard brukes navnet på det bundne formatelementet som et argument for parameterberegnede felt under følgende betingelser:

      - Det beregnede feltet er konfigurert til å bruke én enkelt parameter.
      - Datatypen for denne parameteren er definert som **Streng**.

    Når navnet på det bundne formatelementet er tomt, brukes datakildenavnet for dette elementet i den brukte bindingen.

5. Velg formatelementet **Statement.Taxation.Reduced**.
6. Velg **Bind**.
7. Velg **Ja** for å bekrefte veksling av gjeldende brukerdatakilde, **Level2**, til den nye datakilden, **Levels**, i alle kjedede formatelementer under det valgte formatelementet.
8. Velg formatelementet **Statement.Taxation.None**.
9. Velg **Bind**.
10. Velg **Ja** for å bekrefte veksling av gjeldende brukerdatakilde, **Level3**, til den nye datakilden, **Levels**, i alle kjedede formatelementer under det valgte formatelementet.

   Når du angir argumentet for det parameterberegnede feltet for XML-elementet som representerer et avgiftsnivå (for eksempel **Model.Data2.Levels("Redusert")** som en tekstverdi), trenger du ikke gjøre det samme for kjedede XML-attributter. Bindingene deres arver automatisk verdien til argumentet som er definert på overordnet nivå (**Model.Data2.Levels.aggregated.Base**, ikke **Model.Data2.Levels("Redusert").aggregated.Base**).

Gjentakende kall til parameterberegnede felt støttes ikke.

Du kan velge **Rediger formel** og endre argumentet som brukes om standard for det parameterberegnede feltet i den valgte bindingen. Hvis dette argumentet mangler, kan det føre til feil ved kjøretid – brukerne får beskjed om en slik situasjon når gjeldende format blir validert.

![Varsling om valideringsadvarsel.](media/er-calculated-field-type-10.png)

## <a name="configure-a-parameterized-calculated-field-to-return-a-record"></a>Konfigurere et parameterberegnede felt til å returnere en post
Når et parameterberegnet felt returnerer en post, må du støtte binding av enkeltfelt til formatelementer i denne posten. I slike tilfeller er det ingen overordnet binding som inneholder verdien til et argument for å kalle et parameterberegnet felt. Denne verdien må være definert i bindingen til feltet for en enkeltpost.

### <a name="start-adding-a-new-calculated-field"></a>Begynne å legge til et nytt beregnet felt

1. Velg elementet **Model.Data2**.
2. Velg **Legg til**.
3. Velg **Funksjoner\\Beregnet felt**.
4. Angi **LevelRecord** i **Navn**-feltet.
5. Velg **Rediger formel**.

### <a name="define-a-parameter-for-adding-a-calculated-field"></a>Definere en parameter for å legge til et beregnet felt

1. Velg **Parametre**.
2. Velg **Ny**.
3. I **Navn**-feltet angir du **Avgiftsnivå**.
4. Velg **Streng** i **Type**-feltet.
5. Velg **OK**.

### <a name="define-an-expression-for-adding-a-calculated-field"></a>Definere et uttrykk for å legge til et beregnet felt

1. I **Formel**-feltet angir du følgende:  
    
    **FIRSTORNULL(\@.Levels(**

2. Velg parameteren **Avgiftsnivå**.
3. Velg **Legg til datakilde**.
4. I **Formel**-feltet legger du til **Avgiftsnivå))** i det du skrev inn i trinn 1, for å fullføre uttrykket slik:  
    
    **FIRSTORNULL(\@.Levels('Avgiftsnivå'))**

5. Velg **Lagre**.
6. Lukk siden **Formelutforming**.

### <a name="finish-adding-a-new-calculated-field"></a>Fullfør å legge til et nytt beregnet felt

-   Velg **OK**.

### <a name="use-the-configured-calculated-field-to-bind-format-elements"></a>Bruke det konfigurerte beregnede feltet til å binde formatelementer

1. Vis **Model.Data2.LevelRecord** for å velge det konfigurerte beregnede feltet.
2. Vid **Model.Data2.LevelRecord.aggregated**-container for det konfigurerte beregnede feltet.
3. Velg feltet **Model.Data2.LevelRecord.aggregated.Base**.
4. Velg formatelementet **Statement.Taxation.None**.
5. Velg **Opphev binding**.
6. Velg formatelementet **Statement.Taxation.None.Base**.
7. Velg **Bind**.
8. Velg **Rediger formel**.
9. Endre uttrykket til **Model.Data2.LevelRecord("None").aggregated.Base**.

![Oppdatert uttrykk.](media/er-calculated-field-type-11.png)

## <a name="remove-calculated-fields-that-are-not-used"></a>Fjerne beregnede felt som ikke brukes

1. Velg **Model.Data2.Level1**.
2. Velg **Slett**.
3. Velg **Model.Data2.Level2**.
4. Velg **Slett**.
5. Velg **Model.Data2.Level3**.
6. Velg **Slett**.
7. Velg **Lagre**.

  > [!NOTE]
  > Du brukte det samme beregnede feltet, **Model.Data2.Levels**, flere ganger i formatbindinger. Det er mye enklere å bruke og vedlikeholde ett enkelt beregnet felt i stedet for å gjøre dette for flere lignende felt.

8. Lukk **Formatutforming**-siden.

## <a name="complete-adjusted-version-of-a-derived-format"></a>Fullstendig justert versjon av et avledet format

1. I hurtigfanen **Versjoner** velger du **Endre status**.
2. Velg **Fullfør**.

## <a name="export-completed-version-of-a-derived-format"></a>Eksporter fullført versjon av et avledet format

1. Velg formatet **Format for å lære om parameterkall (tilpasset)** i konfigurasjonstreet.
2. I hurtigfanen **Versjoner** velger du den fullførte versjon 1.1.1.
3. Velg **Veksle**.
4. Velg **Eksporter som XML-fil**.
5. Lagre den nedlastede konfigurasjonen lokalt i XML-format.

## <a name="test-er-formats"></a>Teste ER-formater 
Du kan kjøre de opprinnelige og forbedrede ER-formatene for å sikre at konfigurerte parameterberegnede felt fungerer slik de skal.

### <a name="import-er-configurations"></a>Importere ER-konfigurasjoner
Du kan importere gjennomgåtte konfigurasjoner fra RCS ved å bruke ER-repositoriet til **RCS**-typen. Hvis du allerede har gått gjennom trinnene gjort i emnet [Importere konfigurasjoner for elektronisk rapportering (ER) fra Regulatory Configuration Services](rcs-download-configurations.md), bruker du det konfigurerte ER-repositoriet til å importere konfigurasjoner som er beskrevet tidligere i dette emnet, til miljøet. Hvis ikke følger du denne fremgangsmåten:

1. Velg firmaet **DEMF**, og velg **Elektronisk rapportering** på standard instrumentbord.
2. Velg **Rapporteringskonfigurasjoner**.
3. Importer konfigurasjonene fra Microsoft Download Center i følgende rekkefølge: datamodell, modelltilordning, format. Fullfør trinnene nedenfor for hver ER-konfigurasjon:

    1. Velg **Veksle**.
    2. Velg **Last fra XML-fil**.
    3. Velg **Bla gjennom** for å velge den nødvendige ER-konfigurasjonen i XML-format.
    4. Velg **OK**.

4. Importer den eksporterte fra RCS-fullført versjon 1.1.1 i formatet **Format for å lære om parameterkall (tilpasset)**:

    1. Velg **Veksle**.
    2. Velg **Last fra XML-fil**.
    3. Velg **Bla gjennom** for å velge filen i **Format for å lære om parameterkall (tilpasset)** i XML-format.
    4. Velg **OK**.

### <a name="run-er-formats"></a>Kjøre ER-formater

1. I konfigurasjonstreet viser du innholdet for elementet **Modell for å lære om parameterkall**.
2. Velg **Format for å lære om parameterkall**.
3. Velg **Kjør** på det øverste båndet.
4. Lagre de lokalt genererte utdataene.
5. Velg elementet **Format for å lære om parameterkall (tilpasset)**.
6. Velg **Kjør** på det øverste båndet.
7. Lagre de genererte utdataene lokalt. 
8. Sammenlign innholdet i de genererte utdataene.

## <a name="additional-resources"></a>Tilleggsressurser

- [Formeldesigner i elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md)
- [Forbedre ytelse for ER-løsninger ved å legge til datakilder med parameterisert BEREGNET FELT](er-calculated-field-ds-performance.md)



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]