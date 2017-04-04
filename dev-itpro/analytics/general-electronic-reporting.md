---
title: Oversikt over elektronisk rapportering
description: "Denne artikkelen gir en oversikt over verktøyet for elektronisk rapportering (ER). Den inneholder informasjon om viktige konsepter, hvilke scenarioer ER støtter, samt en liste over formater som er utviklet og lansert som en del av ER-løsningen."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: ERWorkspace
audience: Application User, Developer, IT Pro
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.region: global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 388b6398488e6f316c1ec07a00182e81c1dc8d08
ms.openlocfilehash: b3e8174d07c9b9fd4210486c369c640fe07c49eb
ms.lasthandoff: 03/31/2017


---

# <a name="electronic-reporting-overview"></a>Oversikt over elektronisk rapportering

Denne artikkelen gir en oversikt over verktøyet for elektronisk rapportering (ER). Den inneholder informasjon om viktige konsepter, hvilke scenarioer ER støtter, samt en liste over formater som er utviklet og lansert som en del av ER-løsningen.

Elektronisk rapportering (ER) er et verktøy du kan bruke til å konfigurere formater for elektroniske dokumenter i overensstemmelse med de juridiske kravene i ulike land/områder. ER lar deg administrere disse formatene i deres livssyklus. Du kan for eksempel innføre nye lovbestemte krav, og kan generere forretningsdokumenter i det riktige formatet for elektronisk utveksling av informasjon med statlige instanser, banker og andre parter. ER-motoren er rettet mot bedriftsbrukere i stedet for utviklere. Siden du konfigurere formater, ikke kode, er prosessen med å opprette og justere formater for elektroniske dokumenter raskere og enklere. ER støtter regnearkformatene TEKST, XML og OPENXML. Et filtypegrensesnitt gir imidlertid støtte for flere formater.

## <a name="capabilities"></a>Muligheter
ER-motoren har følgende funksjoner:

-   Det representerer et enkelt vanlige verktøy for elektronisk rapportering i forskjellige domener, og erstatter mer enn 20 ulike motorer som gjør noen type elektronisk rapportering for Microsoft Dynamics-365 for operasjoner.
-   Det er en rapport format isolert fra den gjeldende Dynamics 365 for implementering av operasjoner. (Med andre ord, formatet kan brukes for ulike versjoner av Dynamics 365 for operasjoner.)
-   Den støtter oppretting av et tilpasset format som er basert på et opprinnelig format. Den inkluderer funksjoner for å automatisk oppgradere det egendefinerte formatet når det gjøres endringer til det opprinnelige formatet fordi krav til lokalisering/tilpassing er innført.
-   Den blir det primære standardverktøyet for å støtte for lokaliseringskrav i elektronisk rapportering, både for Microsoft og Microsoft-partnere.
-   Den støtter muligheten til å distribuerte formater til partnere og kunder via Microsoft Dynamics Lifecycle Services (LCS).

## <a name="concepts"></a>Begreper
### <a name="components"></a>Komponenter

ER støtter de to komponenttypene **Datamodell** og **Format **.

#### <a name="data-model-components"></a>Datamodellkomponenter

En datamodellkomponent er en abstrakt representasjon av en datastruktur, og den brukes for å beskrive et bestemt forretningsområde med nok detaljer til å oppfylle rapporteringskravene for dette området. En datamodellkomponent består av følgende deler:

-   en datamodell som et sett med områdespesifikke forretningsenheter, og hierarkisk strukturert definisjon av relasjoner mellom disse enhetene.
-   En modell tilordning at koblinger valgt Dynamics 365 for operasjoner datakilder til individuelle elementer i en datamodell som angir, i kjøretid for dataflyt og reglene for datapopulasjon for bedrifter på en data-modell komponent.

En forretningsenhet for en datamodell representeres som en beholder (post). Egenskaper for forretningsenhet representeres som dataelementer (felt). Hvert dataelement har unik navn, etikett, beskrivelse og verdi. Verdien for hvert dataelement kan være utformet slik at det blir gjenkjent som streng, heltall, desimaltall, dato, opplistingstype, boolsk og så videre. I tillegg kan det være en annen post eller postliste. Én enkelt datamodellkomponent kan inneholde flere hierarkier for områdespesifikke forretningsenheter, i tillegg til modelltilordninger som støtter en bestemt rapportspesifikk dataflyt under kjøring. Hierarkiene skilles med én enkelt post som er valgt som roten for modelltilordning. Datamodellen for betalingsområdet kan for eksempel støtte følgende tilordninger:

-   Firma -&gt; leverandør -&gt; betalingstransaksjoner for AP-domene
-   Kunde -&gt; firma -&gt; betalingstransaksjoner for AR-domene

Vær oppmerksom på at forretningsenheter (for eksempel firma og betalingstransaksjoner) utformes én gang. Forskjellige tilordninger kan deretter bruke dem på nytt. En modelltilordning har følgende funksjoner:

-   Den kan bruke forskjellige Dynamics 365 for datatyper for operasjoner som datakilder for en datamodell. Den kan for eksempel bruke tabeller, dataenheter, metoder eller opplistinger.
-   Den støtter parametere for inndata som kan defineres som datakilder for en datamodell når noen data må angis under kjøring.
-   Den støtter transformeringen av Dynamics 365 for operasjoner data i nødvendige gruppene, filtrere, sortere og summere data, og føyer også med logiske beregnede felt som er utviklet gjennom Microsoft Excel-lignende formler (Hvis du vil ha mer informasjon, se [formel designer i elektronisk rapportering](general-electronic-reporting-formula-designer.md)).

[![Excel-lignende formelredigeringen](./media/pic-formula-1024x615.png)](./media/pic-formula.png) en komponent for data-modellen er utformet for hvert firma domene som skal brukes som en felles datakilde for rapportering som isolerer rapportering fra fysisk implementering av Dynamics 365 for datakilder for operasjoner, og representerer begreper i domene-spesifikke business og funksjonaliteten i et skjema som gjør et rapportering format innledende utforming og ytterligere Vedlikehold mer effektivt.

#### <a name="format-components"></a>Formatkomponenter

En formatkomponent er oppsettet for rapporteringsutdataene som genereres under kjøring. Et utvalg består av følgende elementer:

-   Et format som definerer strukturen og innholdet i det elektroniske rapporteringsdokumentet som genereres under kjøring.
-   Datakilder som et sett med inndataparametre og en områdespesifikk datamodell som bruker modelltilordning
-   En formattilordning som et sett av bindingene for formatdatakilder som har enkelte elementene i et format som under kjøring angir dataflyt og regler for generering av utdataformat
-   Formatvalidering som et sett med konfigurerbare regler som styrer rapportgenerering ved kjøretid, avhengig av kjørekonteksten (for eksempel en regel som stopper utdatagenerering av en leverandørs betaling, og genererer et unntak når bestemte attributter for den valgte leverandøren mangler, for eksempel bankkontonummer).

En formatkomponent støtter følgende funksjoner:

-   Oppretting av rapporteringsutdata som individuelle filer i forskjellige formater: tekst, XML eller regneark
-   Oppretting av flere filer separat, og også innkapsling av filene i ZIP-filer

En formatkomponent gjør det mulig å vedlegge bestemte filer, som kan brukes i rapporteringsutdataene:

-   Excel-arbeidsbøker som inneholder et regneark som kan brukes som en mal for utdata i OPENXML-regnearkformatet
-   Andre filer som kan inkluderes i formatutdataene som forhåndsdefinerte filer

#### <a name="component-versioning"></a>Versjonskontroll av komponenter

Versjonskontroll støttes for ER-komponenter. Følgende arbeidsflyt leveres for å behandle endringer i ER-komponenter:

-   Versjonen som opprinnelig opprettes, er merket som en **UTKAST**-versjon. Denne versjonen kan redigeres og er tilgjengelig for testkjøringer.
-   **UTKAST**-versjonen kan konverteres til en **FULLFØRT**-versjon. Denne versjonen kan brukes i lokale rapporteringsprosesser.
-   Den **fullført** versjon kan konverteres til en **DELTE** versjon. Denne versjonen er publisert på LCS og kan brukes i global reporting prosesser.
-   **DELT**-versjonen kan konverteres til en **AVSLUTTET**-versjon. Denne versjonen kan deretter slettes.

Versjoner som har enten ** fullført ** eller **DELTE** status er tilgjengelige for andre datautveksling. En komponent som har disse statusene, kan ha disse handlingene utført:

-   De kan være serialisert i XML-format og eksportert fra Dynamics 365 for operasjoner som en fil i XML-format.
-   De kan være reserialized fra en XML-fil og importeres til Dynamics 365 for operasjoner som en ny versjon av en komponent ER.

#### <a name="component-date-effectivity"></a>Datogyldighet for komponent

ER-komponentversjoner har datogyldighet. **Gyldig fra**-datoen kan defineres for en ER-komponent for å angi startdatoen som komponenten er gyldig fra for rapporteringsprosesser. Dynamics-365 for operasjoner øktdatoen brukes til å definere om en komponent er gyldig for kjøring. Hvis flere enn én versjon er gyldig for en bestemt dato, brukes den nyeste versjonen for rapporteringsprosessen.

#### <a name="component-access"></a>Komponenttilgang

Tilgang til ER-formatkomponenter avhenger av innstillingen for ISO-kode for land/område. Når denne innstillingen er tomt for en valgt versjon av en konfigurasjon for format, er en komponent i format tilgjengelig fra alle Dynamics 365 for operasjoner selskap ved kjøretid. Når denne innstillingen inneholder ISO-landskoder, er en komponent i formatet bare tilgjengelig fra Dynamics 365 for operasjoner selskaper som har en primær adresse som er definert for en av ISO-landskoder for en format-komponent. Forskjellige versjoner av en dataformatkomponent kan ha ulike innstillinger for ISO-koder for land/område.

#### <a name="configuration"></a>Konfigurasjon

En ER-konfigurasjon er wrapper for en bestemt ER-komponent: **Datamodell** eller **Format**. En konfigurasjon kan inneholde forskjellige versjoner av en bestemt ER-komponent. Hver konfigurasjon er merket som eid av en bestemt konfigurasjonsleverandør. Den **DRAFT** versjon av en komponent i en konfigurasjon som kan redigeres når eieren av konfigurasjonen som er valgt som en aktiv leverandør i innstillinger ER i Dynamics 365 for operasjoner. Hver modellkonfigurasjon inneholder en **Datamodell**-komponent. En ny formatkonfigurasjon kan komme fra (utledes) en bestemt datamodellkonfigurasjon. Formatkonfigurasjonen som opprettes, presenteres i konfigurasjonstreet som en underordnet av den opprinnelige datamodellkonfigurasjonen. Formatkonfigurasjonen som opprettes, inneholder en **Format **-komponent. **Datamodell**-komponenten for den opprinnelige modellkonfigurasjonen settes automatisk inn i **Format**-komponenten for den underordnede formatkonfigurasjonen som standard datakilde. En konfigurasjon ER er delt for Dynamics 365 for operasjoner selskaper.

#### <a name="provider"></a>Leverandør

ER-leverandør er parts-ID-en som brukes til å angi forfatteren (eier) av hver ER-konfigurasjon. ER lar deg administrere listen over konfigurasjonsleverandører. Formatere konfigurasjoner som er utgitt for elektroniske dokumenter som en del av Dynamics-365 for operasjoner løsning er merket som eies av den **Microsoft** konfigurasjon av leverandøren.

#### <a name="repository"></a>Repositorium

Et ER-repositorium lagrer ER-konfigurasjoner. Følgende typer ER repositorier støttes: **operasjonsressurser** og **LCS project**. En ** operasjoner ressurser ** repositoriet gir tilgang til listen over konfigurasjoner som er gitt ut som en del av Dynamics-365 for operasjoner løsning av Microsoft som en leverandør av ER konfigurasjon. Disse konfigurasjonene kan importeres til den gjeldende Dynamics 365 for forekomsten av operasjoner og brukes for elektronisk rapportering. De kan også brukes til tilleggslokaliseringer/-tilpassinger. **LCS-prosjekt**-repositoriet gir tilgang til listen over konfigurasjoner for et bestemt LCS-prosjekt (aktivabibliotek for LCS-prosjekt), som ble valgt under registrering av repositoriet. ER det mulig å laste opp delte konfigurasjoner fra gjeldende Dynamics-365 for operasjoner-forekomst til en bestemt **LCS project** repositoriet. Du kan også importere konfigurasjoner fra en bestemt **LCS project** databasen til den gjeldende Dynamics 365 for forekomsten av operasjoner. Nødvendig **LCS project** repositorier kan registreres individuelt for hver konfigurasjon av leverandøren av den gjeldende Dynamics 365 for forekomsten av operasjoner. Hvert repositorium kan reserveres for en bestemt konfigurasjonsleverandør.

## <a name="supported-scenarios"></a>Scenarier som støttes
### <a name="building-a-data-model"></a>Bygge en datamodell

ER tilbyr en modellutforming som du kan bruke for å bygge en datamodell for et bestemt forretningsområde. Alle områdespesifikke forretningsenheter og relasjoner mellom dem, kan være representert i en datamodell som en hierarkisk struktur. Illustrasjonen nedenfor viser et eksempel på denne typen datamodell (datamodellen for betalingsområde). [![Eksempel på en datamodell](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) for å bli kjent med detaljene i dette scenariet, kan du spille den **ER utformingen domenemodell bestemte data** aktivitet guide (en del av den **7.5.4.3 komponenter for henting/utvikle IT Services-løsning (10677)** forretningsprosessen).

### <a name="translating-data-model-content"></a>Oversette datamodellinnhold

Modellen innholdsdata (etiketter og beskrivelser) kan oversettes til andre språk som støtter Dynamics 365 for operasjoner. Du vil kanskje oversette datamodellinnhold av følgende årsaker:

-   Gjøre innholdet tydeligere under utformingen for formatutviklere som snakker et annet språk, som skal bruke en datamodell for datatilordning av formatkomponenter.
-   Ved kjøretid, at innholdet mer brukervennlig ved å vise spørsmål og hjelp for parametere for kjøring, og også er konfigurert med valideringsmeldinger (feil og advarsler), på språket som du logget på Dynamics 365 for operasjoner bruker foretrekker

Illustrasjonen nedenfor viser et eksempel på hvordan datamodellinnhold kan oversettes fra engelsk til japansk. [![Data modell innhold i engelsk](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png)[![Data modell innhold som er oversatt til japansk](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Konfigurere datamodelltilordninger

ER gir en modell tilordning designer som lar brukere er tilordnet datamodeller som de er utformet for bestemte Dynamics 365 for operasjoner datakilder. Illustrasjonen nedenfor viser et eksempel på denne typen datamodelltilordning (modelltilordning for **SEPA-kredittoverføring** for datamodell for betalingsområde). [![Eksempel på en datatilordning for modellen ](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png)for å bli kjent med detaljene i dette scenariet, kan du spille den **modell ER definere datakilder for tilordning og velger** og **ER kartet datamodellen til valgte datakilder** oppgave støttelinjer (en del av den **7.5.4.3 komponenter for henting/utvikle IT Services-løsning (10677)** forretningsprosess).

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Lagre en utformet modellkomponent som en modellkonfigurasjon

ER kan lagre en utformet datamodell sammen med tilknyttede datatilordninger som en konfigurasjon for den gjeldende Dynamics 365 for forekomsten av operasjoner. Illustrasjonen nedenfor viser et eksempel på denne typen datamodellkonfigurasjon (konfigurasjon for betalingsmodell). [![Eksempel på en konfigurasjon for data ](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png)for å bli kjent med detaljene i dette scenariet, kan du spille den **ER kartet datamodellen til valgte datakilder** aktivitet guide (en del av den **7.5.4.3 komponenter for henting/utvikle IT Services-løsning (10677)** forretningsprosess).

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Bygge et format som bruker en datamodell som basis

ER støtter at en formatutforming som du kan bruke til å bygge formatet for et bestemt elektronisk dokument for et valgt forretningsområde ved å velge modellkomponenten som basis. Samme ER-formatutforming lar deg tilordne et format som du oppretter for en valgt datamodelltilordning for området som en datakilde. Illustrasjonen nedenfor viser et eksempel på denne typen format (formatkonfigurasjon som støtter **BBS**-betalingsformatet for Storbritannia). [![Eksempel på et format som har en datamodell som basis](./media/pic-format-1024x690.png)](./media/pic-format.png) for å bli kjent med detaljene i dette scenariet, kan du spille den **ER Design domene bestemt format** aktivitet guide (en del av den **7.5.4.3 komponenter for henting/utvikle IT Services-løsning (10677)** forretningsprosessen).

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Bygge en konfigurasjon for å generere elektroniske dokumenter i OPENXML-regnearkformat

ER-formatutformingen kan brukes til å bygge et bestemt elektronisk dokument i OPENXML-regnearkformat. Illustrasjonen nedenfor viser et eksempel på denne typen format (et formatkonfigurasjonen til å generere OPENXML regneark med opplysninger om valgte betalingsjournalen):[![Pic-ER-format-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) for å bli kjent med detaljene i dette scenariet, kan du spille den **ER opprette en konfigurasjon for rapporter i formatet for OPENXML** aktivitet guide (en del av den **7.5.4.3 henting/utvikle IT Services-løsningen komponenter (10677)** forretningsprosessen). Bruk det refereres under Excel-fil som en mal for utforming ER formatet til å fullføre trinn i et format mal import av veiledningen oppgave: [mal for betalingen (SampleVendPaymWsReport.xlsx) rapport](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Lagre en utformet formatkomponent i en formatkonfigurasjon

ER kan lagre et format som er utformet med de konfigurerte datatilordninger som en format-konfigurasjon for den gjeldende Dynamics 365 for forekomsten av operasjoner. Den forrige illustrasjonen viser et eksempel på denne typen formatkonfigurasjon (**BBS (Storbritannia)**, som er underordnet av **Betalingsmodell**-konfigurasjonen). Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Utforme områdespesifikt format** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Konfigurere Dynamics 365 for operasjoner for å begynne å bruke et format som opprettet internt

Dynamics 365 for operasjoner kan konfigureres til å begynne å bruke et format som er opprettet til å generere elektroniske rapporter. Referansen til den opprettede formatkonfigurasjonen må defineres i innstillingene for et bestemte område. For eksempel for å begynne å bruke en Gjenopprettingsdiskett format konfigurasjon for elektronisk leverandørbetalinger i BBS-format, skal formatkonfigurasjonen refereres til i bestemte betalingsmåter, som vist i illustrasjonene nedenfor: 

[![Konfigurasjon av formatet BBS (Storbritannia)](media/ger-bacs-uk-format-configuration.png) 

[![Refererer til BBS (Storbritannia)-format i en betalingsmåte](media/ger-bacs-uk-format-method.png) 

Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Bruk format for å generere elektronisk dokument for betaling** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

## <a name="handling-er-components"></a>Behandle ER-komponenter
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Publisere ER-komponent i LCS for å tilby den eksternt (lokalisering)

Eieren av en komponent (modell eller format) som er opprettet, kan bruke ER for å publisere den fullførte versjonen komponenten til LCS. Et repositorium av typen **LCS-prosjekt** for gjeldende ER-konfigurasjonsleverandør er nødvendig. Når statusen for den fullførte versjonen av en komponent endres fra **FULLFØRT** til **DELT**, publiseres denne versjonen i LCS. Når en komponent er publisert til LCS, blir eieren av denne komponenten en leverandør av tjenesten for å støtte komponenten. Hvis formatkomponenten for eksempel er utformet for å generere et juridisk påkrevd elektronisk dokument (for eksempel i henhold til lokaliseringsscenario), antas det at formatet holdes i samsvar med juridiske endringer, og at leverandøren vil utstede nye versjoner av komponenten hver gang nye juridisk krav oppstår. Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Laste opp en konfigurasjon til Lifecycle Services** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Importere en ER-komponent fra LCS til bruk internt

ER kan du importere ER komponenter fra LCS til den gjeldende Dynamics 365 for forekomsten av operasjoner. Et repositorium av typen **LCS-prosjekt ** kreves. Når en komponent ER er importert fra LCS til den gjeldende Dynamics 365 for forekomsten av operasjoner, blir eieren av forekomsten av en forbruker av tjenesten som leveres av eieren av den importerte komponenten (forfatter). For eksempel hvis en komponent i formatet er utformet til å generere et bestemt dokument elektronisk fra Dynamics 365 for operasjoner i et land-/ områdespesifikke format (scenario for lokalisering), antas det at tjenesteforbrukeren vil kunne få tak i alle oppdateringer som er gjort i dette formatet, slik at den er kompatibel med juridisk krav. Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Importere en konfigurasjon fra Lifecycle Services** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Bygge et format ved å velge et annet format som basis (tilpasning)

ER lar deg opprette (avlede) en ny komponent fra gjeldende versjon av en komponent (basis) som ble importert fra LCS. En bruker vil for eksempel avlede et nytt format for å implementere noen spesielle krav til et elektronisk dokument (for eksempel et tilleggsfelt eller en omfattende beskrivelse) for å støtte et tilpassingsscenario. Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Oppgrader format ved innføring av ny basisversjon av det** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Oppgradere et format ved å velge en ny versjon av basisformat (rebasere)

ER lar deg automatisk innføre endringer av den nyeste versjonen av basiskomponenten i gjeldende utkastversjon av den avledede komponenten. Denne prosessen kalles *rebasering*. En ny forskriftsmessig endringer som ble introdusert i den nyeste versjonen av formatet som ble importert fra LCS), kan for eksempel slå sammen automatisk i den tilpassede versjon av dette formatet av det elektroniske dokumentet. Endringer som ikke kan slås sammen automatisk anses som konflikter. Disse konfliktene presenteres for manuell løsing i utformingsverktøyet for den aktuelle komponenten. Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Oppgrader format ved innføring av ny basisversjon av det** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**).

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>Oversikt over ER konfigurasjoner som er levert i Dynamics-365 for operasjoner løsning
| Områdespesifikke datamodellkonfigurasjoner: tittel | Domene                | Datamodellavhengige formatkonfigurasjoner: tittel | Beskrivelse                                                        |
|--------------------------------------------------|-----------------------|---------------------------------------------------|--------------------------------------------------------------------|
| Revisjonsfilmodell                                 | Økonomiske revisjon       |                                                   |                                                                    |
|                                                  |                       | Revisjonsfil (NL)                                   | Revisjonsfilformat for Nederland                                  |
| BAS-modell                                        | Avgiftsrapportering         |                                                   |                                                                    |
|                                                  |                       | BAS (AU)                                          | BAS-format for Australia                                           |
| Skjemamodell for byggebransjen               | Avgiftsrapportering         |                                                   |                                                                    |
|                                                  |                       | CIS Månedlige Retur (Storbritannia)                           | CIS Månedlige returformat for Storbritannia                   |
| Purremodell                          | Elektronisk fakturering  |                                                   |                                                                    |
|                                                  |                       | OIOUBL Purring Letter (DK)                     | OIOUBL Purreformat for Danmark                        |
| Elektronisk finansmodell (MX)          | Avgiftsrapportering         |                                                   |                                                                    |
|                                                  |                       | XML for hjelpefinans (MX)                         | Rapportformat for hjelpefinanstransaksjoner per konto for Mexico |
|                                                  |                       | XML for kontoplan (MX)                         | Rapportformat for kontoplan for Mexico                          |
|                                                  |                       | XML for journaler (MX)                                 | Rapportformat for journaltransaksjoner for Mexico                      |
|                                                  |                       | XML for råbalanse (MX)                            | Rapportformat for råbalanse for Mexico                             |
| Elster-modell                                     | Avgiftsrapportering         |                                                   |                                                                    |
|                                                  |                       | Elster (DE)                                       | Elster-format for Tyskland                                          |
| Modell for EU-salgsliste                              | Handelsrapportering       |                                                   |                                                                    |
|                                                  |                       | EU-salgsliste (DE)                                | TXT-format for EU-salgsliste for Tyskland                               |
|                                                  |                       | EU-salgsliste (DK)                                | TXT-format for EU-salgsliste for Danmark                               |
|                                                  |                       | EU-salgsliste (FR)                                | XML-format for EU-salgsliste for Frankrike                                |
|                                                  |                       | EU-salgsliste (NL)                                | XML-format for EU-salgsliste for Nederland                           |
|                                                  |                       | TXT for EU-salgsliste (Storbritannia)                            | TXT-format for EU-salgsliste for Storbritannia                    |
|                                                  |                       | XML for EU-salgsliste (Storbritannia)                            | XML-format for EU-salgsliste for Storbritannia                    |
|                                                  |                       | Rapport for EU-salgsliste etter kolonner                   | Rapport for EU-salgsliste etter kolonner                                    |
|                                                  |                       | Rapport for EU-salgsliste etter rader                      | Rapport for EU-salgsliste etter rader                                       |
| FEC-regnskapsmodell (FR)                        | Avgiftsrapportering         |                                                   |                                                                    |
|                                                  |                       | XML for FEC-regnskapsdata (FR)                      | XML-format for eksport av FEC-regnskapsdata for Frankrike                   |
| Tysk revisjonsfil                                | Økonomiske revisjon       |                                                   |                                                                    |
|                                                  |                       | Tysk revisjonsfilutdata                          | Revisjonsfilutdata for Tyskland og Østerrike                          |
| Intrastat modell                                  | Handelsrapportering       |                                                   |                                                                    |
|                                                  |                       | Intrastat (DE)                                    | Intrastat-format for Tyskland                                       |
|                                                  |                       | Intrastat (DK)                                    | Intrastat-format for Danmark                                       |
|                                                  |                       | Intrastat-INTRACOM (FR)                           | Intrastat-INTRACOM-format for Frankrike                               |
|                                                  |                       | Intrastat-SAISUNIC (FR)                           | Intrastat SAISUNIC-format for Frankrike                               |
|                                                  |                       | Intrastat (NL)                                    | Intrastat-format for Nederland                               |
|                                                  |                       | Intrastat (Storbritannia)                                    | Intrastat-format for Storbritannia                            |
|                                                  |                       | Intrastat-rapport                                  | Intrastat-kontrollrapport for Excel                                     |
| Kundefakturamodell                           | Elektronisk fakturering  |                                                   |                                                                    |
|                                                  |                       | OIOUBL Prosjektkreditnota (DK)                   | OIOUBL Format for prosjektkreditnota for Danmark                      |
|                                                  |                       | OIOUBL Prosjektfaktura (DK)                       | OIOUBL Format for prosjektfaktura for Danmark                          |
|                                                  |                       | OIOUBL Salgskreditnota (DK)                     | OIOUBL Format for salgskreditnota for Danmark                        |
|                                                  |                       | OIOUBL Salgsfaktura (DK)                         | OIOUBL Salgsfakturaformat for Danmark                            |
| OB-deklareringsmodell                             | Avgiftsrapportering         |                                                   |                                                                    |
|                                                  |                       | OB-deklarering (NL)                               | OB-deklareringsformat for Nederland                          |
| Betalingsmodell                                    | Betalinger              |                                                   |                                                                    |
|                                                  |                       | Betalingsservice (DK)                             | Betalingsservice-betalingsformatet for Danmark                        |
|                                                  |                       | vekselremittering (FR)                  | Vekselremitteringsformat for Frankrike                      |
|                                                  |                       | BTL91 (NL)                                        | BTL91-leverandørbetalingsformat for Nederland                    |
|                                                  |                       | CFONB Prelevements (FR)                           | CFONB-betalingsformat for avtalegiro for Frankrike                       |
|                                                  |                       | CFONB Virements (FR)                              | CFONB-betalingsformat for innenlandsk leverandør for Frankrike                    |
|                                                  |                       | Nordea Leverandør (DK)                                | Betalingsformat leverandørbetaling for Nordea Corporate Netbank for Danmark         |
|                                                  |                       | Tjenesteformat for ANZ-direkteinnbetaling (AU)                    | Tjenesteformatet for ANZ-direkteinnbetaling for Australia                 |
|                                                  |                       | Tjenesteformat for CBA-direkteinnbetaling (AU)                    | Tjenesteformatet for CBA-direkteinnbetaling for Australia                 |
|                                                  |                       | Tjenesteformat for NAB-direkteinnbetaling (AU)                    | Tjenesteformatet for NAB-direkteinnbetaling for Australia                 |
|                                                  |                       | Tjenesteformat for STG-direkteinnbetaling (AU)                    | Tjenesteformatet for STG-direkteinnbetaling for Australia                 |
|                                                  |                       | System for WBC-direkteoppføring (AU)                      | Systemformat for WBC-direkteoppføring for Australia                   |
|                                                  |                       | DirectLink (NZ)                                   | Format for DirectLink for New Zealand                              |
|                                                  |                       | JBA-betalingsfil (JP)                             | JBA-betalingsformat for Japan                                       |
|                                                  |                       | ISO20022-kredittoverføring                          | SEPA-kredittoverføringsformat for Europa                             |
|                                                  |                       | ISO20022-kredittoverføring (FR)                     | SEPA-kredittoverføringsformat for Frankrike                             |
|                                                  |                       | ISO20022-kredittoverføring (DE)                     | SEPA-kredittoverføringsformat for Tyskland                            |
|                                                  |                       | ISO20022-kredittoverføring (NL)                     | SEPA-kredittoverføringsformat for Nederland                    |
|                                                  |                       | ISO20022-avtalegiro                             | SEPA-avtalegiroformat for Europa                                |
|                                                  |                       | ISO20022-avtalegiro (FR)                        | SEPA-avtalegiroformat for Frankrike                                |
|                                                  |                       | ISO20022-avtalegiro (DE)                        | SEPA-avtalegiroformat for Tyskland                               |
|                                                  |                       | ISO20022-avtalegiro (NL)                        | SEPA-avtalegiroformat for Nederland                       |
|                                                  |                       | BBS (Storbritannia)                                         | Format for BACS-leverandørbetalings for Storbritannia                  |
| Snudd avregning                                   | Avgiftsrapportering         |                                                   |                                                                    |
|                                                  |                       | Salgsliste for snudd avregning                         | Format for salgsliste for snudd avregning                                   |
| Nederlandsk XBRL-integreringsmodell                     | XBRL-rapportering        |                                                   |                                                                    |
|                                                  |                       | Semansys XBRL (NL)                                | Semansys XBRL-eksportformat for Nederland                    |
| GAF-modell (MY)                                   | Økonomiske revisjon       |                                                   |                                                                    |
|                                                  |                       | GAF-fil (MY)                                     | Format for GAF for Malaysia                                         |
| Rapport for aldersfordeling for leverandører (CN)                         | Dataanalyse for leverandører |                                                   |                                                                    |
|                                                  |                       | Format for aldersfordeling for leverandører (CN)                   | Format for aldersfordeling for leverandører for Kina                               |
| Modell for deklarering av leverandørfaktura                 | Dataanalyse for leverandører |                                                   |                                                                    |
|                                                  |                       | Deklarering av leverandørfaktura (IS)                   | Format for deklarering av leverandørfaktura for Island                      |
|                                                  |                       | Rapport for deklarering av leverandørfaktura (IS)            | Rapport for deklarering av leverandørfaktura for Island                      |



<a name="see-also"></a>Se også
--------

[Lokaliseringskrav – Opprette en elektronisk rapporteringskonfigurasjon](electronic-reporting-configuration.md)

[Administrere livssyklus til konfigurasjoner for elektronisk rapportering](general-electronic-reporting-manage-configuration-lifecycle.md)


