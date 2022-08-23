---
title: Grupper poster og slå sammen beregninger ved hjelp av GROUPBY-datakilder
description: Denne artikkelen forklarer hvordan du kan bruke datakilder av GROUPBY-typen i elektronisk rapportering (ER).
author: kfend
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: ''
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: 0e520705d2441ead5a68ec3284db74999b3d90b5
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9277609"
---
# <a name="group-records-and-aggregate-calculations-by-using-groupby-data-sources"></a>Grupper poster og slå sammen beregninger ved hjelp av GROUPBY-datakilder

[!include[banner](../includes/banner.md)]

Når du konfigurerer modelltilordninger eller formater for [elektronisk rapportering (ER)](general-electronic-reporting.md), kan du [legge til](#AddMmDataSource2) nødvendige datakilder av **GroupBy**-typen.

Ved utformingstidspunktet konfigureres en **GroupBy**-datakilde til å identifisere følgende elementer:

- En [basisdatakilde](#BaseDataSource) som inneholder poster som skal grupperes ved kjøretid
- [Grupperingsfelter](#GroupingFields) for basisdatakilden, som skal brukes til postgruppering ved kjøretid
- [Aggregatfunksjoner](#AggregateFunctions) som angir aggregatberegningene som vil bli utført for hver oppdagede gruppe ved kjøretid

Ved kjøretid grupperer en konfigurert **GroupBy**-datakilde poster som har de samme verdiene i grupperingsfeltene, og returnerer deretter en liste med poster. Hver post representerer en enkelt gruppe. For hver gruppe eksponerer datakilden feltverdiene som de første postene ble gruppert etter, verdiene til de beregnede mengdefunksjonene og listen over poster for basisdatakilden som tilhører gruppen.

## <a name="aggregate-functions"></a><a name="AggregateFunctions"></a>Aggregatfunksjoner

Ved kjøretid utføres hver aggregatberegning for hver gruppe med poster. Denne beregningen utføres ved å bruke verdien til ett enkelt felt eller et uttrykk i postene til en datakilde som ble valgt for gruppering i den redigerbare datakilden for **GroupBy**-typen. Følgende aggregatfunksjoner støttes for øyeblikket:

- **AVG** – Denne funksjonen returnerer gjennomsnittet av verdiene i en gruppe. Den kan bare brukes med numeriske felt.
- **COUNT** – Denne funksjonen returnerer antallet elementer som ble funnet i en gruppe.
- **Min** – Denne funksjonen returnerer minimumsverdien blant verdiene i en gruppe.
- **Max** – Denne funksjonen returnerer maksimumsverdien blant verdiene i en gruppe.
- **SUM** – Denne funksjonen returnerer summen av alle verdiene i en gruppe. Den kan bare brukes med numeriske felt.

## <a name="execution-location"></a><a name="ExecutionLocation"></a>Kjøringssted

Når du redigerer en **GroupBy**-datakilde og angir basisdatakilden som inneholder postene som må grupperes, oppdager systemet automatisk den mest effektive [plasseringen](#ExecutionLocation) for utføring av denne **GroupBy**-datakilden. Hvis basisdatakilden er [spørringsbar](er-functions-list-filter.md#usage-notes) (det vil si om den kan kjøres på databasenivå), angis også appdatabasen som utførelsesplasseringen til den redigerbare **GroupBy**-datakilden. Ellers angis appserverminnet som utførelsesplasseringen.

Du kan manuelt endre den automatisk registrerte utførelsesplasseringen ved å velge plasseringen som gjelder for den konfigurerte datakilden. Hvis utførelsesplasseringen som er valgt, ikke er aktuell, utløses en [valideringsfeil](er-components-inspections.md#i5) ved utformingstidspunktet.

> [!TIP]
> Vi anbefaler at du bruker databaseplasseringen til å gruppere datakilder som viser et stort antall poster.

## <a name="memory-consumption"></a><a name="MemoryConsumption"></a>Minneforbruk

Hvis en **GroupBy**-datakilde kjøres i minnet, brukes som standard appserverminnet til å lagre poster for basisdatakilden som tilhører hver oppdagede gruppe, som poster for en enkelt gruppe. For å redusere minneforbruket kan du redusere postlagring for **GroupBy**-datakilder hvis de ble konfigurert til å bare beregne aggregerte funksjoner, og hvis gruppens poster ikke brukes ved kjøretid. Hvis du vil redusere minneforbruket på denne måten, kan du aktivere funksjonen **Reduser minnebruk i ER når postergruppering bare brukes til å beregne aggregeringer** i arbeidsområdet **Funksjonsbehandling**.

## <a name="alternatives"></a><a name="Alternatives"></a>Alternativer

Lignende aggregeringer kan beregnes ved hjelp av [ulike](er-data-collection-data-sources.md#if-i-have-to-calculate-running-totals-and-collect-data-what-is-the-difference-between-using-a-data-collection-data-source-and-using-the-built-in-data-collection-functions) typer datakilder eller innebygde ER-funksjoner.

Hvis du vil vite mer om denne funksjonen, kan du fullføre eksemplet nedenfor.

## <a name="example-use-a-groupby-data-source-for-aggregate-calculations-and-record-grouping"></a><a name="Example"></a>Eksempel: Bruk en GROUPBY-datakilde for å aggregere beregninger og gruppere poster

Dette eksemplet viser hvordan en bruker med rollen som systemadministrator eller funksjonell konsulent for elektronisk rapportering kan konfigurere en ER-modelltilordning som har en **GROUPBY**-datakilde som brukes til å beregne aggregeringsfunksjoner og gruppere poster. Denne modelltilordningen brukes til å skrive ut kontrollrapporten når Intrastat-deklareringen genereres. Med denne rapporten kan du gå gjennom rapporterte Intrastat-transaksjoner.

Prosedyrene i dette eksemplet kan fullføres i **DEMF**-firmaet i Microsoft Dynamics 365 Finance. 

### <a name="prepare-sample-data"></a>Klargjør eksempeldata

Kontroller at du har Intrastat-transaksjoner for rapportering på **Intrastat**-siden. Du må ha transaksjoner for forskjellige transportkoder, siden du skal gruppere transaksjoner etter **Transport**-feltet i dette eksemplet.

![Klargjør Intrastat-transaksjoner på Intrastat-siden.](./media/er-groupby-data-sources-prepare-transactions.png)

### <a name="configure-the-er-framework"></a>Konfigurere ER-rammeverket

Følg trinnene i [Konfigurere ER-rammeverket](er-quick-start2-customize-report.md#ConfigureFramework) for å konfigurere minimumssettet med ER-parametere. Du må fullføre dette oppsettet før du begynner å bruke ER-rammeverket til å utforme en ER-modelltilordning.

### <a name="import-the-standard-er-format-configuration"></a>Importere standard ER-formatkonfigurasjon

Følg trinnene i [Importere standard ER-formatkonfigurasjon](er-quick-start2-customize-report.md#ImportERSolution1) for å legge til standard ER-konfigurasjoner i gjeldende forekomst av Dynamics 365 Finance. Importer versjon 1 av konfigurasjonen av **Intrastat-modellen** fra repositoriet.

### <a name="create-a-custom-data-model-configuration"></a>Opprett en egendefinert datamodellkonfigurasjon

Følg trinnene i [Legg til en tilpasset datamodellkonfigurasjon](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) for å manuelt legge til en ny konfigurasjon av en ER-datamodell for **Intrastat-modell (Litware)** som du utleder fra den importerte konfigurasjonen av **Intrastat-modell**.

### <a name="configure-a-custom-data-model-component"></a>Konfigurer en tilpasset datamodellkomponent

Følg denne fremgangsmåten for å gjøre de nødvendige endringene i den avledede **Intrastat-modellens (Litware)** datamodell, slik at den kan brukes til å vise transportkoder med de nødvendige detaljene.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På siden **Konfigurasjoner** i konfigurasjonstreet velger du **Intrastat-modell (Litware)**.
3. Velg **Utforming**.
4. På siden **Datamodellutforming**, i modelltreet, velger du **Intrastat**.
5. Velg **Ny** for å legge til en ny nestet node for den valgte **Intrastat**-noden. I dialogboksen for å legge til en datamodellnode gjør du følgende:

    1. Angi **Transport** i **Navn**-feltet.
    2. Velg **Postliste** i **Varetype**-feltet.
    3. Velg **Legg til** for å legge til den nye noden.

6. Velg **Ny** for å legge til en ny nestet node for **Transport**-noden du nettopp la til. I dialogboksen for å legge til en datamodellnode gjør du følgende:

    1. Angi **Kode** i **Navn**-feltet.
    2. Velg **Streng** i **Varetype**-feltet.
    3. Velg **Legg til** for å legge til den nye noden.

7. Velg **Ny** for å legge til en annen ny nestet node for **Transport**-noden. I dialogboksen for å legge til en datamodellnode gjør du følgende:

    1. I **Navn**-feltet angir du **TotalInvoicedAmount**.
    2. Velg **Faktisk** i **Varetype**-feltet.
    3. Velg **Legg til** for å legge til den nye noden.

8. Velg **Ny** for å legge til en annen ny nestet node for **Transport**-noden. I dialogboksen for å legge til en datamodellnode gjør du følgende:

    1. I **Navn**-feltet angir du **NumberOfTransactions**.
    2. Velg **Heltall** i feltet **Varetype**.
    3. Velg **Legg til** for å legge til den nye noden.

9. Velg **Ny** for å legge til en annen ny nestet node for **Transport**-noden. I dialogboksen for å legge til en datamodellnode gjør du følgende:

    1. Skriv inn **Transaksjon** i **Navn**-feltet.
    2. Velg **Postliste** i **Varetype**-feltet.
    3. Velg **Legg til** for å legge til den nye noden.

10. For **Transaksjon**-noden du akkurat la til, på hurtigfanen **Node**, velger du **Bytt varereferanse**.
11. I dialogboksen **Bytt varereferanse**, i datamodelltreet, velger du **CommodityRecord**. Velg deretter **OK**.

![Konfigurert datamodell i ER-datamodellutforming.](./media/er-groupby-data-sources-configure-data-model.png)

### <a name="complete-the-design-of-a-custom-data-model"></a>Fullfør utformingen av en egendefinert datamodell

Følg trinnene i [Fullføre utformingen av datamodellen](er-quick-start3-customize-report.md#add-a-custom-data-model-configuration) for å fullføre utformingen av den utledede datamodellen **Intrastat-modell (Litware)**.

### <a name="create-a-new-model-mapping-configuration"></a>Opprette en ny modelltilordningskonfigurasjon

Følg trinnene i [Opprette en ny modelltilordningskonfigurasjon](er-quick-start1-new-solution.md#CreateModelMapping) for å manuelt legge til en ny ER-modelltilordningsfunksjon for **Intrastat-eksempeltilordning** for den utledede konfigurasjonen av **Intrastat-modell (Litware)**.

### <a name="add-a-new-model-mapping-component"></a>Legg til en ny modelltilordningskomponent

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. I konfigurasjonstreet på **Konfigurasjoner**-siden utvider du konfigurasjonen av **Intrastat-modell**.
3. Velg konfigurasjonen **Eksempeltilordning for Intrastat**.
4. Velg **Utforming** for å åpne listen over tilordninger.
5. Velg **Slett** for å fjerne den eksisterende tilordningskomponenten.
6. Velg **Ny** for å legge til en ny tilordningskomponent.
7. Velg **Intrastat** i **Definisjon**-feltet.
8. I **Navn**-feltet angir du **Intrastat-tilordning**.
9. Velg **Utforming** for å konfigurere den nye tilordningen.

### <a name="design-the-added-model-mapping-component"></a>Utforme tilordningskomponent for modellen som er lagt til

#### <a name="add-a-data-source-to-access-an-application-table"></a><a name="AddMmDataSource1"></a>Legg til en datakilde for å få tilgang til en apptabell

Konfigurer en datakilde for å få tilgang til apptabellene som inneholder detaljene for Intrastat-transaksjoner.

1. På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Dynamics 365 for Operations\\Tabellposter**.
2. I **Datakilder**-ruten velger du **Legg til rot** for å legge til en ny datakilde som skal brukes til å få tilgang til **Intrastat**-tabellen. Hver post i **Intrastat**-tabellen representerer en enkelt Intrastat-transaksjon.
3. I dialogboksen **Datakildeegenskaper**, i feltet **Navn**, angir du **Transaksjon**.
4. I **Tabell**-feltet angir du **Intrastat**.
5. Velg **OK** for å legge til den nye datakilden.

#### <a name="add-a-data-source-to-group-intrastat-transactions"></a><a name="AddMmDataSource2"></a>Legg til en datakilde for å gruppere Intrastat-transaksjoner

Konfigurer en **GroupBy**-datakilde for å gruppere Intrastat-transaksjoner og beregne aggregatfunksjoner.

1. På siden **Modelltilordningsutforming**, i ruten **Datakildetyper**, velger du **Funksjoner\\Grupper etter**.
2. I **Datakilder**-ruten velger du **Legg til rot** for å legge til en ny datakilde som skal brukes til å gruppere Intrastat-transaksjoner og beregne aggregatfunksjoner.
3. I dialogboksen **Datakildeegenskaper**, i feltet **Navn**, angir du **TransportRecord**.
4. Velg **Rediger gruppe etter** for å konfigurere grupperingsbetingelser.
5. På sisden **Rediger parametersiden Grupper etter**, i listen over datakilder i den høyre ruten, velger du **Transaksjon**-datakilden og utvider den.
6. Velg **Legg til felt i \> Hva skal grupperes** for å indikere at **Transaksjon**-datakilden er valgt som <a name="BaseDataSource">basisdatakilden</a> for den konfigurert **GroupBy**-datakilden. Postene i **Transaksjon**-datakildenblir gruppert, og feltverdiene for denne datakilden blir brukt til beregninger i aggragatfunksjoner.
7. Velg feltet **Transaksjon\Transport**, og velg deretter **Legg til felt i \> Gruppert felt** for å indikere at **Transport**-feltet for basisdatakilden er valgt som <a name="GroupingFields">grupperingsvilkår</a> for den konfigurert **GroupBy**-datakilden. Med andre ord blir postene for **Transaksjon**-datakilden gruppert basert på verdien i **Transport**-feltet. Hver post for den konfigurerte **GroupBy**-datakilden vil representere en enkelt transportkode som blir funnet i poster for basisdatakilden.
8. Velg feltet **Transaction\AmountMST**, og følg deretter denne fremgangsmåten:

    1. Velg **Legg til felt i \> Aggreger felter** for å angi at en <a name="AggregateFunctions">aggregatfunksjon</a> vil bli beregnet for dette feltet.
    2. I **Aggregeringer**-ruten, i posten som har blitt lagt til for det valgte **Transaction\AmountMST**-feltet, i **Metode**-feltet, velger du **Sum**-funksjonen.
    3. I det valgfrie **Navn**-feltet angir du **TotalInvoicedAmount**.

    Disse innstillingene angir at totalbeløpet i feltet **Transaction\AmountMST** skal beregnes for hver transportgruppe.

9. Velg feltet **Transaction\RecId**, og følg deretter denne fremgangsmåten:

    1. Velg **Legg til felt i \> Aggreger felter** for å angi at en aggregatfunksjon vil bli beregnet for dette feltet.
    2. I **Aggregeringer**-ruten, i posten som har blitt lagt til for det valgte **Transaction\RecId**-feltet, i **Metode**-feltet, velger du **Count**-funksjonen.
    3. I det valgfrie **Navn**-feltet angir du **NumberOfTransactions**.

    Disse innstillingene angir at antallet transaksjoner i gruppen blir beregnet for hver transportgruppe.

10. Velg **Lagre**.
11. Se gjennom parametrene for <a name="ExecutionLocation">kjøring</a> i den redigerbare datakilden. Legg merke til at **Registrer automatisk** har blitt valgt automatisk i feltet **Utførelseslokasjon**, og at feltet **Utførelse på** inneholder verdien **SQL**. Disse innstillingene angir at den valgte **Transaksjon**-basisdatakilden for øyeblikket kan spørres, og du kan kjøre den redigerbare **GroupBy**-datakilden på databasenivå.
12. Åpne oppslaget for feltet **Utførelseslokasjon** for å se gjennom listen med tilgjengelige verdier. Legg merke til at du kan velge **Spørring** eller **I minnet** for å tvinge denne **GroupBy**-datakilden til å kjøres på databasenivået eller i appserverminnet.
13. Velg **Lagre**, og lukk **Rediger parametersiden Grupper etter**.
14. Velg **OK** for å fullføre innstillingene for **GroupBy**-datakilden.

#### <a name="bind-the-groupby-data-source-to-data-model-fields"></a><a name="AddMmBindings"></a>Bind GroupBy-datakilden til datamodellfelt

Du kan binde den konfigurerte datakilden til feltene i datamodellen for å angi hvordan datamodellen skal fylles ut med appdata ved kjøring.

1. På siden **Modelltilordningsutforming**, i ruten **Datamodell**, utvider du **Transport**-noden.
2. I **Datakilder**-ruten utvider du **TransportRecord**-datakilden.
3. Legg til en binding for å vise listen over oppdagede transportgrupper:

    1. I **Datamodell**-ruten velger du **Transport**-elementet.
    2. I **Datakilder**-ruten velger du **TransportRecord**-datakilden.
    3. Velg **Bind**.

4. Legg til en binding for å vise transportkoden for hver oppdagede transportgruppe:

    1. Velg datamodellelementet **Transport.Code**.
    2. Velg det grupperte feltet **TransportRecord.grouped.TransportMode**.
    3. Velg **Bind**.

5. Legg til en binding for å vise verdiene for de beregnede aggregatfunksjonene for hver oppdagede transportgruppe:

    1. Velg datamodellelementet **Transport.NumberOfTransactions**.
    2. Velg det aggregerte feltet **TransportRecord.aggregated.NumberOfTransactions**.
    3. Velg **Bind**.
    4. Velg datamodellelementet **Transport.TotalInvoicedAmount**.
    5. Velg det aggregerte feltet **TransportRecord.aggregated.TotalInvoicedAmount**.
    6. Velg **Bind**.

6. Legg til en binding for å vise transaksjonsposter som tilhører hver oppdagede transportgruppe:

    1. Velg datamodellelementet **Transport.Transaction**.
    2. Velg feltet **TransportRecord.lines**.
    3. Velg **Bind**.

    Du kan fortsette å konfigurere bindinger for de nestede elementene i datamodellelementet **Transport.Transaction** og datakildefeltet **TransportRecord.lines** for å vise, ved kjøretid, detaljer for Intrastat-transaksjonene som tilhører hver oppdagede transportgruppe.

![Konfigurert modelltilordning i ER-modelltilordningsutforming.](./media/er-groupby-data-sources-configure-model-mapping.png)

### <a name="debug-the-added-model-mapping-component"></a>Feilsøk tilordningskomponent for modellen som er lagt til

Bruk [ER-feilsøkingsprogrammet for datakilde](er-debug-data-sources.md) til å teste den konfigurerte modelltilordningen.

1. På siden **Modellkartleggingsutforming** velger du **Start feilsøking**.
2. På siden **Feilsøk datakilder**, i den venstre ruten, velger du **TransportRecord**-datakilden og velger deretter **Les alle poster**.
3. Utvid **TransportRecord**-datakilden, og gjør deretter følgende:

    1. Velg datakilden **TransportRecord.grouped.TransportMode**.
    2. Velg **Hent verdi**.
    3. Velg datakilden **TransportRecord.grouped.NumberOfTransactions**.
    4. Velg **Hent verdi**.
    5. Velg datakilden **TransportRecord.grouped.TotalInvoicedAmount**.
    6. Velg **Hent verdi**.

4. Velg **Vis alle** i høyre rute.

Datakilden **TransportRecord** viser to poster og presenterer to transportkoder. For hver transportkode beregnes antall transaksjoner og totalt fakturert beløp.

> [!NOTE]
> Tilnærmingen"rolig avlesning" brukes når en **GroupBy**-datakilde kalles for å optimalisere databasekall. Derfor blir noen av feltverdiene i en **GroupBy**-datakilde bare beregnet i feilsøkingen av ER-datakilden når de er knyttet til datamodellfelt.

![Resultater av feilsøking av datakilde på siden Feilsøk datakilder.](./media/er-groupby-data-sources-debug-datasource.png)

## <a name="frequently-asked-questions"></a>Vanlige spørsmål

### <a name="is-there-any-way-to-calculate-grand-totals-when-the-group-totals-are-calculated"></a>Finnes det en metode for å beregne hovedsummer når gruppetotalene er beregnet?

Ja. Du kan beregne hovedsummer ved å konfigurere en annen **GroupBy**-datakilde der **GroupBy**-datakilden som du konfigurerte tidligere, brukes som basisdatakilde. Illustrasjonen nedenfor viser **Totaler**-datakilden av **GroupBy**-typen som brukes til å beregne **SUM**-aggregeringsfunksjonen, basert på **SUM**-aggregeringen av **TransportRecord**-datakilden av **GroupBy**-typen.

![Totaler-datakilde i ER-modelltilordningsutformingen.](./media/er-groupby-data-sources-configure-model-mapping2.png)

Illustrasjonen nedenfor viser resultatene av feilsøkingen av **Totaler**-datakilden.

![Resultater av feilsøking av Totaler-datakilde på siden Feilsøk datakilder.](./media/er-groupby-data-sources-debug-datasource2.png)

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over elektronisk rapportering](general-electronic-reporting.md)
- [Feilsøke datakilder for et utført ER-format for å analysere dataflyt og transformasjon](er-debug-data-sources.md)
- [Bruk datakilder for DATAINNSAMLING i formater for elektronisk rapportering](er-data-collection-data-sources.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
