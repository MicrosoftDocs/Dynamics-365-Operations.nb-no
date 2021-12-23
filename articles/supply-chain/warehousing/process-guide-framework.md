---
title: Rammeverk for prosessveiledning
description: Dette emnet gir informasjon om rammeverket for prosessveiledning for utviklere som utvider lagerets mobilprosesser i X++.
author: Mirzaab
ms.date: 11/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 6882c979ad9b37eb4f95a04259b6ac0f0a0edcdc
ms.sourcegitcommit: fd6270dc7f49f93a8155d2b827153b13edb7be8a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/09/2021
ms.locfileid: "7902052"
---
# <a name="process-guide-framework"></a>Rammeverk for prosessveiledning

[!include [banner](../includes/banner.md)]

Dette emnet gir informasjon om rammeverket for prosessveiledning for utviklere som utvider lagerets mobilprosesser i X++. Lagerets mobilprosesser er utvidbare som et resultat av at prosessene brytes inn i små trinn. Forretningslogikken og brukergrensesnittbyggingen for hvert trinn er hentet inn i individuelle klasser, som gir utviding.

## <a name="overview-of-the-existing-design"></a>Oversikt over eksisterende utforming

Lagerets mobilutførelsesflyt vises via et enkelt egendefinert endepunkt for tjeneste. Forespørselen ankommer fra mobilappen i form av en XML-streng, som inneholder metadataene fra brukergrensesnittet som presenteres i mobilappen, i tillegg til verdiene som angis av brukeren.

Når forespørselen mottas, er det første trinnet å deserialisere denne XMLen. **WHSMobileAppServiceXMLTranslator**-klassen konverterer XMLen til en container som inneholder både kontrollinformasjon og øktinformasjon.

Etter dette brukes informasjonen i containeren til å utlede hvilken lagerprosess brukeren arbeider med, eller er i ferd med å starte (representert av **WHSWorkExecuteMode**-opplistingen), og tilsvarende instansiere en avledet klasse for **WHSWorkExecuteDisplay**. Metoden **displayform()** startes, som deretter gjør følgende:

-   Behandler data fra brukeren (delegert til **WHSRFControlData**-klassen, men noen prosesser implementerer spesifikk logikk ved å overstyre **processControl()**-metoden).

-   Utfører forretningslogikk.

-   Øker trinnet.

-   Bygger containeren som representerer det nye brukergrensesnittet (vanligvis i en **build…()**-metode).

Containeren returneres deretter til oversetteren, som deretter serialiserer XMLen, og sender den tilbake som svar på mobilenheten.

Sekvensdiagrammet nedenfor viser en oversikt over kjøringsflyten. Legg merke til at diagrammet er mer en skjematisk oversikt, og er ikke en 1:1-representasjon av den faktiske koden.

![Skjematisk oversikt over prosessen.](media/schematic-overview.png) 

### <a name="reason-for-the-redesign"></a>Årsak til den nye utformingen

Utformingen ovenfor gir et svært enkelt rammeverk for byggeprosesser som brukes i mobilflyt. Det er imidlertid, som vist ovenfor, **displayform()**-metodene som tar over flere ansvarsområder. Det delegerer dem ikke til andre metoder og klasser, men hvis det ikke finnes klasseansvar, gjøres det på en inkonsekvent måte på tvers av klasser. Dessuten vil noen av disse klassene bli ganske komplekse etter hvert som antallet scenarier som støttes vokser kraftig. For å gjøre det mer interessant overstyres noen av klassene/metodene, og de brukes på nytt i flere moduser. Resultatet er svært lange metoder med høy sammensatt kompleksitet. Det har tidligere vært vedlikeholdsproblemer. Det har vært risikofylt å løse problemer med disse metodene.
For eksempel refereres **processWorkLine()**-metoden i **WhsWorkExecuteDisplay**-klassen fra flere prosesser (vanligvis hvor arbeidsutførelsen utføres).

Hvis du vil gjøre disse utvidbare, kan ett av alternativene være å dele **displayForm**-metodene i mindre metoder og introdusere utvidbarhetspunkt. På grunn av scenariomatrisen vil det imidlertid være utfordrende for partnere å skrive utvidelser og validere mot regresjoner. Ikke bare det, på grunn av mangel på strukturert ansvarsfordeling som er nevnt ovenfor, vil koden fortsette å vokse på uforutsigbare måter over tid, og gi utfordringer ved bygging av kvalitetsforlengelser.

Den nye utformingen er derfor det bærekraftige alternativet, med et mål om å ha en klar definisjon av klasser som har uavhengige ansvarsområder. En klasse bør ha ett ansvarsområde, én årsak til endring og én årsak til utvidelsen.

## <a name="design-overview"></a>Oversikt over utforming

I det nye rammeverket er kjernestrategien avhengig av to prinsipper: Del utførelsesflyten inn i individuelle komponenter med veldefinerte ansvarsområder, og ha veldefinerte utvidelsespunkt i hver av komponentene.

Navnet på det nye rammeverket er "ProcessGuide". Dette er fordi målet med disse klassene er å veilede en bruker gjennom en forretningsprosess (i motsetning til den rike klienten, som er en skjemabasert erfaring der brukeren har mer fleksibilitet når det gjelder hvordan de samhandler med dataene eller i hvilken rekkefølge de utfører oppgaver).

> [!NOTE]
> En viktig detalj er med hensikt å utelate prefikset "WHS". Mens de mobile prosessene først ble lansert for lageraktiviteter, har de senere gått over til å støtte forskjellige produksjons- og lagerstyringsprosesser. Lagerreferansen ble da utelukket i navnet på rammeverket.

Når du skal identifisere komponentene, er det første trinnet å se på produksjonsstartprosessen (**WhsWorkExecuteDisplayProdStart**-klassen). Her er en skjematisk oversikt over prosessen.

![Bilde av skjemaprosessen.](media/production-start-process-schematic.png)

Hvis du ser på kontrollflyten, trenger du følgende komponenter:

-   Kontroller som går gjennom hele forretningsprosessen.
-   Trinn som er ansvarlig for utføring av et trinn i prosessen.
-   Databehandler for behandling av dataene i et trinn.
-   Sidebygger som er ansvarlig for å bygge opp brukergrensesnittet for et trinn.
-   En navigasjonsagent som er ansvarlig for trinnovergangen.
-   Klasse som er ansvarlig for utføring av forretningsprosessen.

I prosessflytdiagrammet ovenfor, hvis du begynner på trinn 1 og begynner å behandle dataene fra forrige trinn, og deretter slutter med å bygge et grensesnitt, vil dataene fortsette å bli behandlet i det neste trinnet. Dette introduserer en fast kobling mellom fortløpende trinn, slik at den nye skjematiske oversikten på høyt nivå vil se ut som følgende:

![Bilde av skjemaprosess på høynivå.](media/high-level-schematic.png)

Nedenfor finner du nøkkelkomponentene i prosessen med ny utforming:

-   **ProcessGuideController** - Denne klassen lager den helhetlige utførelsen av forretningsprosessen. Den definerer faktorer som starter trinnet og navigasjonsagenten, som deretter utgjør prosessutførelsen, i tillegg til oppryddingslogikken for annullering eller avslutning av prosessen.

-   **ProcessGuideStep** - Denne klassen representerer ett enkelt trinn i forretningsprosessen. Denne klassen inneholder en definisjon av faktorene som starter en sidebygger, handlinger og databehandlere, og er ansvarlig for å starte dem i riktig rekkefølge.

-   **ProcessGuideNavigationAgent** - Denne klassen er ansvarlig for navigasjon mellom trinnene. Når et trinn er fullført, er navigasjonsagenten ansvarlig for å definere neste trinn og sender eventuelle parametere som det forrige trinnet må kommunisere med det neste.

-   **ProcessGuidePageBuilder** - Denne klassen er ansvarlig for å starte brukergrensesnittet.

-   **ProcessGuideAction** - Denne klassen representerer en handling, som vises som en knapp for brukeren.

-   **ProcessGuideDataProcessor** - Denne klassen er ansvarlig for behandling av brukerens angitte data i et felt.

## <a name="execution-flow"></a>Utførelsesflyt

Utgangspunktet for utførelsesflyten forblir uendret. Forespørselen ankommer fortsatt gjennom de samme sluttpunktene, etterfulgt av deserialisering av XMLen i containeren. Denne containeren sendes deretter til **getNextFormState()**.

Det er tre viktige klasser du kan merke deg:

-  **ProcessGuideSessionState** – Dette inneholder informasjon om øktstatusen – modus, overføring, kontroller og trinn som utføres, og så videre.

-  **ProcessGuidePage** - Dette inneholder en sterkt skrevet representasjon av metadataene for brukergrensesnittet.

-  **ProcessGuideRequest** - Dette inneholder de to ovenfor som medlemmer, og er en representasjon av forespørselen du mottok fra mobilenheten.

Disse klassene opprettes ved hjelp av containerinformasjonen (både status- og brukerdefinerte kontrolldata). Dette gir en typesikker måte å få tilgang til og manipulere verdiene på. Sammenlignet med gjentagende tilgang av containeren under prosessen, gir dette fordeler både når det gjelder lesbarhet og ytelse.

Informasjonen om øktstatusen brukes til å starte den riktige **ProcessGuideController**-klassen. Når **createResponse()**-metoden i **ProcessGuideController**-klassen startes. Denne metoden er oppføringspunktet til prosessveiledningslogikken, og etter utføringen kommer tilbake med svaret (representert i **ProcessGuideResponse**-klassen). Svaret konverteres deretter tilbake til containeren og sendes tilbake til den eldre logikken, som deretter serialiserer den til XML, og sender svar tilbake til mobilenheten.

Deretter må kontrolløren finne neste trinn som skal utføres. Hvis dette er begynnelsen på en ny prosess, vil kontrolløren kalle **initialStep()** for å få det første trinnet i prosessen. Etter det vil det kalle **execute()**-metoden i **ProcessGuideStep**. Denne metoden vil deretter instansiere en **ProcessGuidePageBuilder**-klasse og kalle **buildPage()**, som ville returnere med et **ProcessGuidePage**-objekt, som er en virtuell representasjon av brukergrensesnittet som skal presenteres for brukeren. Trinnet ville da sende resultatet tilbake til kontrolleren, som deretter ville lagre gjeldende øktstatus og deretter returnere resultatet tilbake til **getNextFormState()** i form av **ProcessGuideResponse**-klassen. Etter det blir svaret konvertert tilbake til containeren, og deretter serialiseres til XML, og sender tilbake svaret til mobilenheten.

Diagrammet nedenfor forklarer denne kontrollflyten. Legg merke til at dette er den vanligste kontrollflyten, forenklet for forklaring av utformingen.

![Kontrollflyt forenklet.](media/control-flow.png)

Når brukeren gjør en handling på mobilenheten ved å klikke en knapp (eller skanne en verdi – som vanligvis utløser standardhandlingen) – ankommer forespørselen **createResponse()**-metoden i **ProcessGuideController**-klassen gjennom den samme ruten. Denne tiden vet imidlertid kontrolløren fra øktstatusen hvilket trinn brukeren er i. I henhold til dette instansierer den den aktuelle **ProcessGuideStep**-klassen og starter utføringsmetoden. **ProcessGuideStep** leser deretter handlingsnavnet som startes av brukeren, og instansierer deretter den aktuelle **ProcessGuideAction**-klassen og kaller **execute()**.

**ProcessGuideAction**-klassen er ansvarlig for å utføre den bestemte handlingen, men det er to viktige unntak.

Den første er **ProcessGuideOKAction-**-klassen. Denne handlingen innebærer at brukeren ønsker å bekrefte og gå fremover i prosessen. I henhold til det - denne metoden gjør faktisk et tilbakekall til ProcessGuideStep-klassen, som betyr at trinnet starter **processData()** i **ProcessGuideDataProcessor**. Dette behandler dataene brukeren har angitt, og oppdaterer deretter statusen for trinnet og sender resultatet tilbake til kontrolløren. Trinnet starter sidebyggeren for å bygge opp det riktige brukergrensesnittet eller angir status for trinnet som fullført, avhengig av resultatet av behandleren. Dette gjenspeiles i den øvre halvdelen av sekvensdiagrammet nedenfor.

Det andre unntaket er annulleringshandlingen, implementert i klassene **ProcessGuideCancelResetProcessAction** og **ProcessGuideCancelExitProcessAction**. Disse handlingene representerer en hensikt om å avbryte prosessen og gå tilbake til enten begynnelsen av prosessen eller avslutte prosessen helt. På samme måte som **OK**-handlingen, utfører disse handlingene også et tilbakekall på trinnet, som signaliserer hensikten til **ProcessGuideController**. Kontrolleren utfører deretter den nødvendige oppryddingen av tilstandsvariabler, og enten flytter kontroll til det innledende trinnet i prosessen eller avslutter prosessen helt.

Når trinnet er fullført, hvis statusen for trinnet er satt til **Fullført**, instansierer kontrolløren øyeblikkelig **ProcessGuideNavigationAgent**, som returnerer navnet på neste trinn. Kontrolleren instansierer deretter dette trinnet og starter **execute()**-metoden, og syklusen fortsetter. Det nye trinnet starter vanligvis tilsvarende **ProcessGuidePageBuilder** for å bygge opp brukergrensesnittet for det neste skjermbildet som skal presenteres for brukeren, som deretter sendes tilbake. Flyten vises i den nedre halvdelen av sekvensdiagrammet nedenfor.

![sekvensdiagram.](media/sequence-diagram.png)

## <a name="building-a-new-process-using-the-processguide-framework"></a>Bygge en ny prosess ved hjelp av ProcessGuide-rammeverket

Den beste måten å forklare kontrollflyten på, er ved hjelp av et eksempel som finnes i programmet – produksjonstartsprosessen.

## <a name="overview-of-the-production-start-process"></a>Oversikt over produksjonsstartprosessen

La oss starte med å forstå prosessflyten. I det første trinnet blir brukeren bedt om å bruke produksjonsordre-ID.

![Ledetekst for produksjons-ID.](media/production-id-prompt.png)

Når brukeren angir produksjonsordre-IDen, valideres ordrenummeret. Noen av valideringene som kjøres, er basert på om ordren er i det samme lageret som brukeren er logget på, og statusen for ordren. Hvis valideringen mislykkes, vises brukeren en feilmelding. Hvis valideringen lykkes, vises brukeren detaljer om produksjonsordren og varen.

Brukeren kan enten avbryte og gå tilbake til begynnelsen av prosessen, eller klikke **OK** for å bekrefte. I det siste tilfellet settes produksjonsordren til **Startet**-status, tilsvarende journaler posteres, kontrollen flyttes tilbake til det første trinnet og meldingen "Arbeid fullført" vises til brukeren.


## <a name="creating-the-controller"></a>Opprette kontrolleren

Det første trinnet i forretningsprosessen er å opprette kontrollerklassen, og går fra abstraktklassen **ProcessGuideController**, som implementerer standardvirkemåten til en kontroller. Det nye klassenavnet er **ProdProcessGuideProductionStartController** og kommer med **WHSWorkExecuteMode**-verdien til **StartProdOrder**. Den samme **SysExtension**-baserte forekomsten som ble brukt i **WHSWorkExecuteDisplay**-klassene brukes, noe som gjør det enklere å starte kontrolleren når brukeren utfører et menyelement for denne modusen.

```xpp
[WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
public class ProdProcessGuideProductionStartController extends ProcessGuideController
```

> [!NOTE]
> Navnemønsteret til klassen er **\<FunctionalArea\>ProcessGuide\<Businessprocessname\>Controller**. Dette er mønsteret som brukes for kontrollklassene og for å forlenge til andre klasser.


## <a name="building-the-first-step"></a>Bygge opp det første trinnet

Deretter definerer du det første trinnet du oppretter **ProdProcessGuidePromptProductionIdStep**-klassen, som går fra **ProcessGuideStep**.

Oppgaven med å starte klassen delegeres til en trinnfabrikk, som startes av basisklassen **ProcessGuideController**. Standardimplementeringen av fabrikken instansierer trinnet basert på navn. Derfor må du gjøre to ting for å instansiere **ProdProcessGuidePromptProductionIdStep** som det første trinnet i kontrolleren:

-   Dekorer **ProdProcessGuidePromptProductionIdStep**-klassen med attributtet **ProcessGuideStepName**.

    ```xpp
    [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))] public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
    ```

-   I kontrollklassen implementerer du abstraktmetoden **initialStepName()** for å returnere trinnnavnet.

    ```xpp
    protected final ProcessGuideStepName initialStepName()
    {
        return classStr(ProdProcessGuidePromptProductionIdStep);
    }
    ````   
    
> [!NOTE]
> Verdien i **ProcessGuideStepName**-attributtet trenger ikke å samsvare nøyaktig med klassenavnet, som vist ovenfor. Implementering av dette gir imidlertid en enhetlig og typesikkerhet rundt kryssreferanser ved bruk av klassen. Bruk av denne navngivningskonvensjonen anbefales.
>
> **ProcessGuideStepName**-basert forekomst av trinnet implementeres i **ProcessGuideStepDefaultFactory**-klassen. I det sjeldne tilfellet du vil ha en annen strategi for å starte trinnet, må du gjøre følgende:
> -   Opprett en ny fabrikkklasse som arver fra **ProcessGuidStepAbstractFactory**.
> -   Du kan også opprette en ny parameterklasse som implementerer **ProcessGuideIStepCreationParameters**-grensesnittet, som inneholder parameterne som fabrikken trenger.
> -   I kontrollerklassen overstyrer du **stepFactory()** og **stepCreationParameters()**-metodene for å returnere fabrikken og parameterne ovenfor.

Det neste trinnet er å implementere funksjonaliteten til **ProdProcessGuidePromptProductionIdStep**-klassen. Du må implementere logikken for å bygge opp brukergrensesnittet, behandle data som angis av brukeren og finne ut når trinnet er fullført.

### <a name="building-the-user-interface-for-the-first-step"></a>Bygge brukergrensesnittet for første trinn

Brukergrensesnittet bygges ved hjelp av en klasse som arver fra **ProcessGuidePageBuilder**-abstraktklassen. For dette trinnet bør du gi klassen navn som representerer hva den gjør – **ProdProcessGuidePromptProductionIdPageBuilder**.

Forekomstmekanismen til klassen ligner på måten trinnet ble iniisert på fra kontrolleren. 

-   Dekorer **ProdProcessGuidePromptProductionIdPageBuilder**-klassen med attributtet **ProcessGuidePageBuilderName**.

    ```xpp
    [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))] public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
    ```

-   I **ProdProcessGuidePromptProductionIdStep**-klassen implementerer abstraktmetoden **pageBuilderName()** for å returnere dette navnet.

    ```xpp
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
    }
    ```    

> [!TIP]
> Ligner på trinnfabrikken, det er også et abstrakt fabrikkmønster implementert for sidebyggerfabrikken. Så i det sjeldne tilfellet at du vil ha en annen strategi for å starte sidebygeren, kan du gjøre følgende:
> - Opprett en ny fabrikkklasse som arver fra **ProcessGuidePageBuilderAbstractFactory**.
> - Du kan også opprette en ny parameterklasse som implementerer **ProcessGuideIPageBuilderCreationParameters**-grensesnittet, som inneholder parameterne som fabrikken trenger.
> - I trinnklassen overstyrer du **pageBuilderFactory()** og **pageBuilderCreationParameters()**-metodene for å returnere fabrikken og parameterne ovenfor.

For å implementere brukergrensesnittet trenger du en side med én tekstboks for å angi produksjonsordre-IDen, i tillegg til en **OK**-knapp og en **Avbryt**-knapp. **Avbryt**-knappen bør avslutte prosessen.

Hvis du vil implementere dette, må du overstyre to metoder i **ProdProcessGuidePromptProductionIdPageBuilder**-klassen:

-   Bruk **addDataControls()**-metoden til å legge til tekstboksen.

    ```xpp
    protected final void addDataControls(ProcessGuidePage _page)
    {
        _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
    }
    ```   

-   Bruk **addActionControls()**-metoden for å legge til **OK**- og **Avbryt**-knappene.

    ```xpp
    protected final void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelExitProcess));
    }
    ``` 

Nå legges datakontrollene til, etterfulgt av knappene. Hvis du imidlertid vil bygge en skjerm med fordelte datakontroller og -knapper, kan du overstyre **addControls()**-metoden i stedet for fleksibilitet.

Et tilleggsscenario som bør vurderes, er hvordan man gjenoppbygger siden ved valideringsfeil, for eksempel hvis brukeren angir feil produksjonsordre-ID. **ProcessGuidePageBuilder**-basisklassen implementerer standardvalget, som bygger brukergrensesnittet på nytt, fjerner den skannede verdien og legger til feilkontroll med feilmeldingen. Fordi dette er standardvalget du vil bruke, behøver du ikke å legge til noen koder for å håndtere feil.

> [!TIP]
> Hvis du vil implementere egendefinert grensesnittatferd for feilsituasjoner, kan du overstyre én eller flere av metodene **rebuildFromRequestPage()**, **isErrorState()** og **reuseRequestPageOnError**.

### <a name="processing-the-user-entered-data-in-the-first-step"></a>Behandle de brukeangitte dataene i første trinn

Behandlingen av dataene utføres i **ProcessGuideDataProcessorDefault**-klassen, som igjen starter den eldre **WhsRfControlData-**-klassen. Det er ingen endringer i denne standardvirkemåten, og **WhsRfControlData** har allerede logikk for validering av **ProdId**-feltet, så du trenger ikke å skrive noen logikk for å håndtere dette. I tilfelle nødvendige utvidelser for valideringslogikken, kan du vurdere å bruke **WhsControl**-basert utvidelsesmekanisme.

### <a name="determine-if-the-first-step-is-complete"></a>Finne ut om det første trinnet er fullført

Når valideringen er vellykket, er det på tide å merke trinnet som fullført. Dette gjøres i basisklassen, men du må implementere betingelsen for å bestemme fullføringstrinnet. Følgende overstyrte metode gjør det.

```xpp
protected final boolean isComplete()
{
    WhsrfPassthrough pass = controller.parmSessionState().parmPass();
    ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);
        return (prodId != '');
}
```   

### <a name="step-two-view-order-details-and-confirm"></a>Trinn to: Vis ordredetaljer og bekreft

I det andre trinnet i prosessen vises en skjerm med detaljer om ordren. Brukeren kan enten klikke **OK**-knappen for å bekrefte starten på produksjonsordren, eller klikke **Avbryt** for å gå tilbake til begynnelsen av prosessen. For dette eksemplet kan du gi navn til trinnet **ProdProcessGuideConfirmProductionOrderStep** og sidebyggerklassen **ProdProcessGuideConfirmProductionOrderPageBuilder**.

Klassen ProdProcessGuideConfirmProductionOrderStep ser ut som følgende.

```xpp
[ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
{
    protected final ProcessGuidePageBuilderName pageBuilderName()
    {
        return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
     }
}
```     

Siden brukeren ikke angir noen verdier her, trenger du ikke å overstyre **isComplete()**-metoden. Trinnet er fullført når brukeren klikker **OK**.

Sidebyggerklassen overstyrer **addDataControls()**-metoden hvis du vil legge til tre etiketter. Den første etiketten viser produksjonsordre-IDen, den andre inneholder vareinformasjon (for eksempel vare-ID, dimensjoner eller beskrivelse), og den tredje inneholder mengde og måleenhet.

**addActionControls()** overstyres deretter hvis du vil legge til 2 knapper – **OK**-knappen og **Avbryt**-knappen for å avbryte prosessen og gå tilbake til begynnelsen av prosessen.

```xpp
/// <summary>
/// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
/// and then confirm.
/// </summary>
[ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
{
    protected void addDataControls(ProcessGuidePage _page)
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;
        
        _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
        _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
        _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

        if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
        {
            _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
        }
    }

    protected void addActionControls(ProcessGuidePage _page)
    {
        #ProcessGuideActionNames
        _page.addButton(step.createAction(#ActionOK), true);
        _page.addButton(step.createAction(#ActionCancelResetProcess));
    }
```

> [!NOTE]
> I dette emnet finner du samme kildekode for X++-metodene ved hjelp av Programutforsker. Filtrer på klassenavnet, høyreklikk klassenavnet og velg **Vis kode**.

### <a name="step-3-start-the-production-order"></a>Trinn 3: Starte produksjonsordren

Det tredje trinnet er hvor forretningslogikken for å starte produksjonsordren utføres. Dette trinnet er noe forskjellig fra de forrige trinnene, der dette trinnet ikke har et brukergrensesnitt. Dette trinnet blir utført stille når brukeren klikker **OK** i det forrige trinnet.

Abstraktklassen **ProcessGuideStepWithoutPrompt** implementerer standardvirkemåten for slike trinn. Det gjeldende trinnet bør derfor utvide **ProcessGuideStepWithoutPrompt**-klassen og overstyre **doExecute()**-metoden.

Følgende kodeeksempel viser klassen og **doExecute**-metodeimplementeringen. Metoden henter ganske enkelt ordre-IDen og bruker-IDen fra øktstatusen, og starter metoden for å starte denne produksjonsordren.

```xpp
/// <summary>
/// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
/// </summary>
[ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
{
    protected final void doExecute()
    {
        WhsrfPassthrough pass = controller.parmSessionState().parmPass();
        WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
        ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
        WhsWorkExecute workExecute = WhsWorkExecute::construct();
        workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

        this.addProcessCompletionMessage();

        super();
    }

}
```

Hvis det er et unntak, sikrer rammeverkets unntakshåndteringslogikk at prosessen tilbakerulles til forrige trinn.

> [!NOTE]
> Starten til **addProcessCompletionMessage()** legger til meldingen "Arbeid fullført" i navigasjonsparameterne. Neste trinn (hvis det har et brukergrensesnitt) vil vise denne meldingen. Basisklassene håndterer denne logikken, og ingen bestemt kode må legges til i prosessklassene for å oppnå denne virkemåten.


### <a name="building-the-navigation-through-the-steps"></a>Bygge opp navigeringen gjennom trinnene

Basisklassen **ProcessGuideController** instansierer klassen **ProcessGuideNavigationAgentDefault**, som er avhengig av en forhåndsdefinert navigasjonsrute, som er et enkelt kart over kilde- og måltrinn. For produksjonsstartscenariet, fordi det ikke finnes noen betingede grener, vil denne implementeringen være tilstrekkelig. Derfor trenger du bare å overstyre **initializeNavigationRoute()**-metoden for å definere navigasjonsruten.

```xpp
    protected ProcessGuideNavigationRoute initializeNavigationRoute()
    {
        ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
        navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
        navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

        return navigationRoute;
    }
```

Det finnes prosesser der det vil være betingede grener (basert på brukerhandlinger eller andre betingelser). Slike prosesser må gjøre følgende:

-   Implementere bestemte navigasjonsagenter som er arvet fra **ProcessGuideNavigationAgent**-klassen.

-   Implementere den bestemte navigasjonsagenten som er arvet fra **ProcessGuideNavigationAgentAbstractFactory**-klassen, som inneholder logikk for å instansiere riktig navigasjonsagent basert på gjeldende trinn, øktstatus, brukerhandling eller annen logikk.

-   Du kan også overstyre **navigationAgentCreationParameters()** i kontrollklassen for å sende passende parametere.

-   Overstyr **navigationAgentFactory()** i kontrolleren for å instansiere navigasjonsagentens fabrikk opprettet ovenfor.

### <a name="action-classes"></a>Handlingsklasser

Handlingsklasser representerer brukerhandlinger, så dette eksemplet bruker **OK**-handlingen til å vise hvordan handlingene opprettes.

```xpp
[ProcessGuideActionName(#ActionOK)]
public class ProcessGuideOKAction extends ProcessGuideAction
{
    public final str label()
    {
        return "@SYS5473";
     }
     protected final void doExecute()
     {
        step.executeOKAction();
      }
}
```    

Klassen må implementere to abstrakte metoder:

-   **label()**, som returnerer etiketten som skal vises i en knappekontroll som er knyttet til denne handlingen.

-   **doExecute()**, som utfører handlingen. Som nevnt tidligere, utfører **OK**-knappen ganske enkelt et tilbakekall til trinnet. Andre handlinger kan imidlertid ha mer kompleks logikk her.

Handlingene startes ved hjelp av **SysExtension**-rammeverket basert på **ProcessGuideActionName**-attributtet. I likhet med forekomsten av sidebyggere implementerer trinnklassen den standard handlingsfabrikken, og det er mulig å overstyre dette. Sidebyggeren legger til en knappekontroll som dette.

```xpp
_page.addButton(step.createAction(#ActionOK), true);
```

Når dette skjer, blir trinnet bedt om å opprette en handlingsklasse for det sendte navnet, og knytter denne handlingen til knappen.

### <a name="summary"></a>Sammendrag

Hvis du vil oppsummere alt som er forklart i dette emnet, finner du et omfattende sammendrag av koden som kreves for prosessen:

1.  **ProdProcessGuideProductionStartController**

    1.  Overstyr **initialStepName()** for å angi navnet på det første trinnet.
    2.  Overstyr **initializeNavigationRoute()** for å konstruere navigasjonstilordningen.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideProductionStartController</c> class is the controller class for the production order start process guide.
        /// </summary>
        [WHSWorkExecuteMode(WHSWorkExecuteMode::StartProdOrder)]
        public class ProdProcessGuideProductionStartController extends ProcessGuideController
        {
            protected ProcessGuideStepName initialStepName()
            {
                return classStr(ProdProcessGuidePromptProductionIdStep);
            }

            protected ProcessGuideNavigationRoute initializeNavigationRoute()
            {
                ProcessGuideNavigationRoute navigationRoute = new ProcessGuideNavigationRoute();
                navigationRoute.addFollowingStep(classStr(ProdProcessGuidePromptProductionIdStep), classStr(ProdProcessGuideConfirmProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideConfirmProductionOrderStep), classStr(ProdProcessGuideStartProductionOrderStep));
                navigationRoute.addFollowingStep(classStr(ProdProcessGuideStartProductionOrderStep), classStr(ProdProcessGuidePromptProductionIdStep));

                return navigationRoute;
            }

        }
        ```

2.  **ProdProcessGuidePromptProductionIdStep**

    1.  Overstyr **isComplete()** for å angi når trinnet regnes som fullført.
    2.  Overstyr **pageBuilderName()** for å angi sidebyggeren som skal brukes.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdStep</c> represents a step that 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuidePromptProductionIdStep))]
        public class ProdProcessGuidePromptProductionIdStep extends ProcessGuideStep
        {
            protected boolean isComplete()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdId prodId = pass.lookup(ProcessGuideDataTypeNames::ProdId);

                return (prodId != '');
            }

            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuidePromptProductionIdPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuidePromptProductionIdPageBuilder**

    1.  Overstyr **addDataControls()** for å legge til **Produkt-ID**-tekstboksen.
    2.  Overstyr **addActionControls()** for å legge til **OK**- og **Avbryt**-knappene.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuidePromptProductionIdPageBuilder</c> class builds a page 
        /// that prompts the user for a production order id.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuidePromptProductionIdPageBuilder))]
        public class ProdProcessGuidePromptProductionIdPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                _page.addTextBox(ProcessGuideDataTypeNames::ProdId, "@SYS4398", extendedTypeNum(ProdId));
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelExitProcess));
            }

        }
        ```

4.  **ProdProcessGuideConfirmProductionOrderStep**

    1.  Overstyr **pageBuilderName()** for å angi sidebyggeren som skal brukes.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderStep</c> class represents the step for viewing production order
        /// details and confirming the same.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideConfirmProductionOrderStep))]
        public class ProdProcessGuideConfirmProductionOrderStep extends ProcessGuideStep
        {    
            protected ProcessGuidePageBuilderName pageBuilderName()
            {
                return classStr(ProdProcessGuideConfirmProductionOrderPageBuilder);
            }

        }
        ```

3.  **ProdProcessGuideConfirmProductionOrderPageBuilder**

    1.  Overstyr **addDataControls()** for å legge til ordre-, vare- og antallsinformasjonsetiketter.

    2.  Overstyr **addActionControls()** for å legge til **OK**- og **Avbryt**-knappene.
        
        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideConfirmProductionOrderPageBuilder</c> builds a page that allows the user to see details of a production order
        /// and then confirm.
        /// </summary>
        [ProcessGuidePageBuilderName(classStr(ProdProcessGuideConfirmProductionOrderPageBuilder))]
        public class ProdProcessGuideConfirmProductionOrderPageBuilder extends ProcessGuidePageBuilder
        {
            protected void addDataControls(ProcessGuidePage _page)
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                UnitOfMeasureSymbol inventUOM = InventTableModule::find(prodTable.ItemId, ModuleInventPurchSales::Invent).UnitId;

                _page.addLabel(ProcessGuideDataTypeNames::ProdIdLabelName, strFmt("@WAX1684", prodTable.ProdId), extendedTypeNum(ProdId));
                _page.addLabel(ProcessGuideDataTypeNames::ItemInfo, this.generateItemInfoForProdId(pass.lookup(ProcessGuideDataTypeNames::ProdId)), extendedTypeNum(WHSRFUndefinedDataType));
                _page.addLabel(ProcessGuideDataTypeNames::QtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId)), inventUOM), extendedTypeNum(WHSRFQuantityAndUOM));

                if (PdsGlobal::pdsIsCWItem(prodTable.ItemId))
                {
                    _page.addLabel(ProcessGuideDataTypeNames::InventQtyLabelName, strFmt("@WAX1685", WHSWorkExecuteDisplay::num2StrDisplay(ProdUpdStartUp::pdsCWProposalStartupQty(prodTable.ProdId)), PdsCatchWeightItem::pdsCWUnitId(prodTable.ItemId)), extendedTypeNum(WHSRFQuantityAndUOM));
                }
            }

            protected void addActionControls(ProcessGuidePage _page)
            {
                #ProcessGuideActionNames
                _page.addButton(step.createAction(#ActionOK), true);
                _page.addButton(step.createAction(#ActionCancelResetProcess));
            }

        ```

        > [!NOTE]
        > Metoden **generateItemInfoForProdId()**, som brukes til å generere vareinformasjonsetiketter, utelates fra dette emnet. Denne metoden spør et par tabeller for å få vare-ID, beskrivelse og dimensjoner. Hvis du vil ha en bedre forståelse av **generateItemInfoForProdId()**, kan du se på kildekoden.

4.  **ProdProcessGuideStartProductionOrderStep**

    1.  Overstyr **doExecute()** for å utføre startprosessen for produksjon og legge til fullføringsmeldingen for prosessen.

        ```xpp
        /// <summary>
        /// The <c>ProdProcessGuideStartProductionOrderStep</c> represents a step that starts a production order.
        /// </summary>
        [ProcessGuideStepName(classStr(ProdProcessGuideStartProductionOrderStep))]
        public class ProdProcessGuideStartProductionOrderStep extends ProcessGuideStepWithoutPrompt
        {
            protected final void doExecute()
            {
                WhsrfPassthrough pass = controller.parmSessionState().parmPass();
                WHSUserId userId = pass.lookup(ProcessGuideDataTypeNames::UserId);
                ProdTable prodTable = ProdTable::find(pass.lookup(ProcessGuideDataTypeNames::ProdId));
                WhsWorkExecute workExecute = WhsWorkExecute::construct();
                workExecute.prodStartUp(prodTable.ProdId, ProdUpdStartUp::proposalStartUpQty(prodTable.ProdId), userId);

                this.addProcessCompletionMessage();

                super();
            }

        }
        ```

> [!NOTE]
> Legg merke til at en rekke av de vanlige mønstrene (regenerering av grensesnitt ved feil, innstilling av fullføringsmelding for prosess, **OK** og **Avbryt**-virkemåte) er flyttet til rammeverket – og dermed slipper programutvikleren å skrive standardkode som både er utsatt for feil og har en risiko for inkonsekvent virkemåte på tvers av prosesser. Der scenariet må avvike fra den vanlige banen, får imidlertid programutvikleren muligheten til å overstyre passende metoder – men da er det et tilsiktet avvik som både er eksplisitt og sporbart.


### <a name="extending-a-business-process"></a>Utvide en forretningsprosess

Hittil har dette emnet uthevet hvordan du bygger en ny prosess ved hjelp av **ProcessGuide**-rammeverket. I denne siste delen finner du noen eksempler på hvordan denne forretningsprosessen kan utvides.

### <a name="add-a-step-in-a-flow-using-processguidenavigationagentdefault"></a>Legge til et trinn i en flyt (ved hjelp av ProcessGuideNavigationAgentDefault)

Hvor du skal utvide:

-   Underordnet **ProcessGuideController**-klassen for prosessen.

Slik utvider du:

-   Utvid **initializeNavigationRoute()**-metoden i kontrollklassen, og start **addFollowingStep()** i **ProcessGuideNavigationRoute**-klassen.

### <a name="add-a-step-in-a-flow-using-custom-navigation-agent"></a>Legge til et trinn i en flyt (ved hjelp av en egendefinert navigasjonsagent)

Hvor du skal utvide:

-   Underordnet **ProdProcessGuideNavigationAgentFactory/ProdProcessGuideNavigationAgent**.

Slik utvider du:

-   Opprett en ny underordnet klasse av **ProcessGuideNavigationAgent** som returnerer det ønskede trinnnavnet.

-   Opprett en ny klasse som er avledet fra **ProcessGuideNavigationAgentFactory**, som returnerer navigasjonsagenten som er opprettet ovenfor.

-   Utvid **navigationAgentFactory()**-metoden i kontrollerklassen for å returnere fabrikken opprettet ovenfor.

### <a name="add-a-new-control-in-the-ui-of-an-existing-step"></a>Legge til en ny kontroll i grensesnittet til et eksisterende trinn 

Hvor du skal utvide:

-   Underordnet **ProdProcessGuidePageBuilder** for trinnet.

Slik utvider du:

-   Utvid **addDataControls()**-metoden og legg til tilleggskontrollen.

### <a name="complete-overhaul-of-the-user-interface-in-an-existing-step"></a>Fullføre overhaling av brukergrensesnittet i et eksisterende trinn

Hvor du skal utvide:

-   Underordnet **ProdProcessGuideStep**.

Slik utvider du:

-   Opprett en ny underordnet klasse av **ProdProcessGuidePageBuilder**-klassen, og implementer det ønskede brukergrensesnittet.

-   Utvid **pageBuildeName()**-metoden i trinnklassen for å returnere **ProcessGuidePageBuilderNameAttribute** for klassen som ble opprettet ovenfor.

### <a name="alter-logic-when-a-step-is-considered-complete"></a>Endre logikk når et trinn regnes som fullført

Hvor du skal utvide:

-   Underordnet **ProdProcessGuideStep**.

Slik utvider du:

-   Utvid **isComplete()**-metoden for å bygge tilleggslogikken.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]