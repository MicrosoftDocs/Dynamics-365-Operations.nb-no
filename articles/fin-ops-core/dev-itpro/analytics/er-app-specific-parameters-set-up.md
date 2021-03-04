---
title: Definere parameterne for et ER-format per juridisk enhet
description: Dette emnet forklarer hvordan du kan konfigurere parametere for et ER-format per juridisk enhet.
author: NickSelin
manager: AnnBe
ms.date: 10/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: b51a7ae8587a3cbb65efc4af574929efcbc8fbf8
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681478"
---
# <a name="set-up-the-parameters-of-an-er-format-per-legal-entity"></a>Definere parameterne for et ER-format per juridisk enhet

[!include[banner](../includes/banner.md)]

## <a name="prerequisites"></a>Forutsetninger

Hvis du vil fullføre disse trinnene, må du først fullføre trinnene i emnet [Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet](er-app-specific-parameters-configure-format.md).

Hvis du vil fullføre eksemplene i dette emnet, må du ha tilgang til Microsoft Dynamics 365 Finance (Finance) for en av de følgende rollene:

- Utvikler av elektronisk rapportering
- Funksjonell konsulent for elektronisk rapportering
- Systemansvarlig

## <a name="import-er-configurations"></a>Importere ER-konfigurasjoner

1.  Logg på miljøet.
2.  Velg **Elektronisk rapportering** på standard instrumentbord.
3.  Velg **Rapporteringskonfigurasjoner**.
4.  Importerer, til den gjeldende forekomsten av Finance, konfigurasjonene du eksporterte fra Regulatory Configuration Services (RCS) mens du fullfører trinnene i emnet [Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet](er-app-specific-parameters-configure-format.md). Følg denne fremgangsmåten for hver ER-konfigurasjon i følgende rekkefølge: datamodell, modelltilordning og formater.

    1. Velg **Exchange \> Last inn fra XML-fil**.
    2. Velg **Bla gjennom** for å velge den riktige filen for den nødvendige ER-konfigurasjonen i XML-format.
    3. Velg **OK**.
    
    Følgende illustrasjon viser konfigurasjonene du trenger når du er ferdig.

    ![Siden ER-konfigurasjoner](./media/GER-AppSpecParms-ImportedConfigurations.PNG)

## <a name="set-up-parameters-for-the-demf-company"></a>Definer parametere for DEMF-selskapet

Du kan bruke ER-rammeverket til å definere programspesifikke parametere for et ER-format.

1.  Velg den juridiske enheten **DEMF**.
2.  I konfigurasjonstreet velger du formatet **Format for å lære hvordan du slår opp LE-data**.
3.  På Handling-panelet, i kategorien **Konfigurasjoner**, i gruppen **Programspesifikke parametere**, velg **Oppsett**.

    ![Siden ER-programspesifikke parametere](./media/GER-AppSpecParms-LookupForm.PNG)
    
    På siden **Programspesifikke parametere** kan du konfigurere reglene for **Velger**-datakilden for **Format for å lære hvordan du slår opp LE-data**.
    
    Hvis det grunnleggende ER-formatet vil inneholde flere datakilder for **Oppslag**-typen, må du velge ønsket datakilde i **Oppslag**-hurtigfanen før du kan begynne med å konfigurere regelsettet for datakilden.
    
    For hver datakilde kan du konfigurere egne regler for hver versjon av det valgte ER-formatet.
    
    Hele settet med regler for alle oppslagsdatakilder som er tilgjengelige i den valgte versjonen av det grunnleggende ER-formatet, utgjør programspesifikke parametere for ER-formatet.

4.  Velg versjon **1.1.1** av ER-formatet.
5.  Velg **Legg til** på hurtigfanen **Betingelser**.
6.  Klikk på rullegardinpilen i **Kode**-feltet for den nye posten for å åpne oppslaget.

    Oppslaget viser listen over avgiftskoder for valg. Denne listen er returnert av **Model.Data.Tax**-datakilden som er konfigurert i det grunnleggende ER-formatet. Siden denne datakilden inneholder **navn** -feltet, vises navnet på hver avgiftskode i oppslaget.

    ![Siden ER-programspesifikke parametere](./media/GER-AppSpecParms-LookupForm-CodeFldPicker.PNG)
    
7.  Velg mva-koden **VAT19**.
8.  Klikk på rullegardinpilen i **Oppslagsresultat**-feltet for den nye posten for å åpne oppslaget. Oppslaget presenterer listen med verdier for formatopplistingen for TaxationLevel for utvalg.

    Legg merke til at hvis tysk er valgt som foretrukket språk for brukeren du er logget på som, vil etikettene for verdiene i oppslaget være på tysk, forutsatt at de er oversatt i grunnleggende ER-format. Hvis etiketten til en oppslagsdatakilde for eksempel er oversatt, vil denne etiketten vises på brukerens foretrukne språk i **Oppslag**-kategorien.

    ![Siden ER-programspesifikke parametere](./media/GER-AppSpecParms-LookupForm-LookupFldPicker.PNG)

9.  Velg **Vanlig avgift**-verdien.

    Når du legger til denne posten, definerer du følgende regel: Hver gang **Velger**-oppslagsdatakilden blir forespurt, og **VAT19** mva-koden sendes som et argument, returneres **vanlig avgift** som forespurt avgiftsnivå.

10. Velg **Legg til**, og følg deretter denne fremgangsmåten:

    1. I **Kode**-feltet velger du avgiftskoden **InVAT19**.
    2. Velg **Vanlig avgift**-verdien i **Oppslagsresultat**-feltet.
    
11. Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:

    1. I **Kode**-feltet velger du avgiftskoden **VAT7**.
    2. Velg **Redusert avgift**-verdien i **Oppslagsresultat**-feltet.
    
12. Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:

    1. I **Kode**-feltet velger du avgiftskoden **InVAT7**.
    2. Velg **Redusert avgift**-verdien i **Oppslagsresultat**-feltet.
    
13. Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:

    1. I **Kode**-feltet velger du avgiftskoden **THIRD**.
    2. Velg **Ingen avgift**-verdien i **Oppslagsresultat**-feltet.
    
14. Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:

    1. I **Kode**-feltet velger du avgiftskoden **InVAT0**.
    2. Velg **Ingen avgift**-verdien i **Oppslagsresultat**-feltet.
    
15. Velg **Legg til** på nytt, og følg deretter denne fremgangsmåten:

    1. I **Kode**-feltet velger du **\*Ikke tom\***-alternativet.
    2. Velg **Annet**-verdien i **Oppslagsresultat**-feltet.
    
    Ved å legge til den siste posten definerer du følgnde regel: Her gang avgiftskoden som sendes som et argument, ikke oppfyller noen av de tidligere reglene, returnerer oppslagsdatakilden **Annet** som forespurt avgiftsnivå.

    ![Siden ER-programspesifikke parametere](./media/GER-AppSpecParms-LookupForm-RulesSet.PNG)
    
16. Velg **Fullført** i **Status**-feltet.

    Når du kjører en ER-formatversjon som har statusen **fullført** eller **delt**, må dette settet med regler være i **fullført**-tilstand. Hvis ikke vil utføringen av det grunnleggende ER-formatet bli avbrutt når formatet prøver å laste inn data fra dette regelsettet mens data **Velger**-oppslagsdatakilden kjøres.
    
    Når du kjører en ER-formatversjon som har statusen **utkast**, kan det grunnleggende ER-formatet få tilgang til dette regelsettet, uavhengig av tilstanden.
    
17. Velg **Lagre**.
18. Lukk siden **Programspesifikke parametere**.

## <a name="run-the-er-format-in-the-demf-company"></a>Kjør ER-formatet i DEMF firmaet

1.  I konfigurasjonstreet velger du formatet **Format for å lære hvordan du slår opp LE-data**.
2.  Velg **Kjør** i handlingsruten.
3.  I dialogboksen som vises, velger du **OK**.
4.  Last ned utdraget som er generert, og lagre det lokalt.

    I det genererte utdraget legger du merke til at sammendraget av **InVAT7**-avgiftskoden er lagt på **Redusert**-nivået, og sammendragene av **VAT19** og **InVA19**-avgiftskodene er lagt på **vanlig** nivå. Denne virkemåten bestemmes av konfigurasjonen i det juridisk enhetensavhengige regelsettet.
    
5.  Gå til **Avgift \> Indirekte avgifter \> Merverdiavgift \> Mva-koder**.
6.  Velg mva-koden **InVAT7**.
7.  I handlingsruten i kategorien **Mva-kode** i **Forespørsler**-gruppen velger du **Postert merverdiavgift** for å vise informasjon om avgiftsverdien og brukt avgiftssats per avgiftskode.

    ![Siden Postert merverdiavgift](./media/GER-AppSpecParms-Statement.PNG)

8.  Lukk siden Postert merverdiavgift.

## <a name="set-up-parameters-for-the-usmf-company"></a>Definer parametere for USMF-selskapet

1.  Velg den juridiske enheten **USMF**.
2.  Gå til **Organisasjonsstyring \> Elektronisk rapportering \> Konfigurasjoner**.
3.  I konfigurasjonstreet utvider du elementet **Modell for å lære om parameterkall**, utvid elementet **Format for å lære om parameterkall**, og velg formatet **Format for å lære hvordan du slår opp LE-data**.
4.  På Handling-panelet, i kategorien **Konfigurasjoner**, i gruppen **Programspesifikke parametere**, velg **Oppsett**.
5.  Velg versjon **1.1.1** av det valgte ER-formatet.
6.  Velg **Legg til** på hurtigfanen **Betingelser**.
7.  Klikk på rullegardinpilen i **Kode**-feltet for den nye posten for å åpne oppslaget.

    Oppslaget viser nå en liste over mva-koder for **USMF** selskapsavgiften for valg.

    ![Siden ER-programspesifikke parametere](./media/GER-AppSpecParms-LookupForm-CodeFldPicker2.PNG)
    
8.  Velg mva-koden **EXEMPT**.
9.  Velg **Ingen avgift**-verdien i **Oppslagsresultat**-feltet for den nye posten.
10. Velg **Legg til** på nytt.
11. I **Kode**-feltet for den nye posten velger du **\*Ikke tom\***-alternativet.
12. Velg **Vanlig avgift**-verdien i **Oppslagsresultat**-feltet for den nye posten.
13. Velg **Fullført** i **Status**-feltet.
14. Velg **Lagre**.

    ![Siden ER-programspesifikke parametere](./media/GER-AppSpecParms-LookupForm-RulesSet2.PNG)
    
15. Lukk siden **Programspesifikke parametere**.

## <a name="run-the-er-format-in-the-usmf-company"></a>Kjør ER-formatet i USMF firmaet

1.  I konfigurasjonstreet velger du formatet **Format for å lære hvordan du slår opp LE-data**.
2.  Velg **Kjør** i handlingsruten.
3.  I dialogboksen som vises, velger du **OK**.
4.  Last ned utdraget som er generert, og lagre det lokalt.

    Legg merke til at du nå har brukt det samme ER-formatet på nytt for en annen juridisk enhet i det genererte uttrykket, men uten å gjøre noen justeringer i ER-formatet.

## <a name="reuse-legal-entitydependent-parameters"></a>Bruk juridisk enhetsavhengige parametere på nytt

### <a name="export-parameters"></a>Eksportere parametere

1.  Gå til **Organisasjonsstyring \> Arbeidsområder \> Elektronisk rapportering**.
2.  Velg **Rapporteringskonfigurasjoner**.
3.  I konfigurasjonstreet velger du formatet **Format for å lære hvordan du slår opp LE-data**.
4.  På Handling-panelet, i kategorien **Konfigurasjoner**, i gruppen **Programspesifikke parametere**, velg **Oppsett**.
5.  Velg versjon **1.1.1** av ER-formatet.
6.  Velg **Eksporter** på handlingsruten.
7.  Last ned filen som er generert, og lagre det lokalt.

    Det konfigurerte settet med programspesifikke parametere er nå eksportert som en XML-fil.

### <a name="import-parameters"></a>Importere parametere

1.  Velg versjon **1.1.2** av ER-formatet.
2.  Velg **Importer** på handlingsruten.
3.  Velg **Ja** for å bekrefte at du vil overstyre de eksisterende programspesifikke parameterne for denne formatversjonen.
4.  Velg **Bla gjennom** for å finne filen som inneholder de eksporterte programspesifikke parameterne for versjon **1.1.1.**.
5.  Velg **OK**.

    Versjon **1.1.2** av ER-formatet har nå samme programspesifikke parametere som du opprinnelig konfigurerte for versjon **1.1.1.**.
    
    Legg merke til at de programspesifikke parameterne for et ER-format er juridisk enhetsavhengig. Hvis du vil bruke de programspesifikke parameterne som ble konfigurert for én juridisk enhet på nytt i en annen juridisk enhet, må du eksportere dem mens du er logget på den første juridiske enheten, og deretter importere dem etter at du har logget på den andre juridiske enheten.

    Du kan også bruke denne fremgangsmåten til å overføre ER-formatrelaterte programspesifikke parametere som opprinnelig ble konfigurert i én forekomst av Finance til en annen forekomst av Finance.

    Vær oppmerksom på at hvis du konfigurerer programspesifikke parametere for én versjon av et ER-format og importerer en høyere versjon av samme format til gjeldende Finance-forekomst, vil ikke de eksisterende programspesifikke parameterne brukes for den importerte versjonen.
    
    Vær også oppmerksom på at når du velger en fil for import, sammenlignes strukturen til programspesifikke parametere i den aktuelle filen med strukturen til den tilsvarende datakilden for **Oppslag**-typen i ER-formatet som er valgt for import. Importen utføres når strukturen til hver programspesifikk parameter samsvarer med strukturen til den tilsvarende datakilden i ER-formatet som er valgt for import. Hvis strukturene ikke samsvarer, får du en advarsel som sier at importen ikke kan utføres. Hvis du fremtvinger importen som skal utføres, ryddes det opp i de eksisterende programspesifikke parameterne for det valgte ER-formatet, og du må definere dem fra begynnelsen.

## <a name="relationship-between-application-specific-parameters-and-an-er-format"></a>Relasjon mellom programspesifikke parametere og et ER-format

Forholdet mellom et ER-format og de programspesifikke parameterne etableres av ER-formatets forekomstuavhengige unike identifikasjonskode. Når du fjerner et ER-format fra Finance, beholdes derfor de programspesifikke parameterne som er konfigurert for ER-formatet, i den gjeldende forekomsten av Finance. Du kan få tilgang til dem når det grunnleggende ER-formatet blir importert på nytt til denne forekomsten av Finance.

## <a name="access-application-specific-parameters-by-using-the-er-framework"></a>Få tilgang til programspesifikke parametere ved hjelp av ER-rammeverket

I det forrige eksemplet har du fått tilgang til programspesifikke parametere i et ER-format ved hjelp av ER-rammeverket. Denne fremgangsmåten gir deg ikke muligheten til å begrense tilgangen til programspesifikke parametere i et spesielt ER-format. Hvis du må bruke slike restriksjoner, følger du disse trinnene. 

1.  Bruk et eksisterende **ERSolutionAppSpecificParametersDesigner**-menyelement, eller implementer ditt eget **ERSolutionAppSpecificParametersDesigner**-menyelement.

    ![Visual studio-side](./media/GER-AppSpecParms-LookupForm-Access1.PNG)
    
2.  Følg ett av disse trinnene:

    1.  Opprett en ny menyelementknapp, og koble den til den tilsvarende posten fra **ERSolutionTable**-tabellen ved å sette **Datakilde**-egenskapen til **ERSolutionTable**.
    
        ![Visual studio-side](./media/GER-AppSpecParms-LookupForm-Access2.PNG)
        
    2.  Opprett en enkel knapp, og overstyr **Klikket**-metoden, som vist i følgende eksempel.
    
        Ved å bruke denne fremgangsmåten kan du angi en unik løsnings-ID (definert via **GUID**-verdien) for å gi tilgang til de programspesifikke parameterne for bare et spesifikt ER-format og underordnede kopier som er avledet fra det.
        
        ```xpp
        public void clicked()
            {
                super();

                ERSolutionTable solutionTableRecord = ERSolutionTable::findByGUID(str2Guid('ADACCB2F-EFD1-4C90-877D-7E1E5D1AEE92'));

                Args args = new Args();
                args.record(solutionTableRecord);
                args.caller(this);

                new MenuFunction(menuItemDisplayStr(ERSolutionAppSpecificParametersDesigner), MenuItemType::Display)
                    .run(args);
            }
        ```

## <a name="additional-resources"></a>Tilleggsressurser

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Konfigurere ER-formater til å bruke parametere som angis per juridisk enhet](er-app-specific-parameters-configure-format.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]