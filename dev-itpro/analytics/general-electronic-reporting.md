---
title: Oversikt over elektronisk rapportering
description: "Denne artikkelen gir en oversikt over verktøyet for elektronisk rapportering (ER). Den inneholder informasjon om viktige konsepter, hvilke scenarioer ER støtter, samt en liste over formater som er utviklet og lansert som en del av ER-løsningen."
author: kfend
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
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
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: caa9f4c73f4c6b5b7637b5b012bd9ed3b7dd6392
ms.contentlocale: nb-no
ms.lasthandoff: 05/25/2017


---

# <a name="electronic-reporting-overview"></a>Oversikt over elektronisk rapportering

[!include[banner](../includes/banner.md)]


Denne artikkelen gir en oversikt over verktøyet for elektronisk rapportering (ER). Den inneholder informasjon om viktige konsepter, hvilke scenarioer ER støtter, samt en liste over formater som er utviklet og lansert som en del av ER-løsningen.

Elektronisk rapportering (ER) er et verktøy du kan bruke til å konfigurere formater for elektroniske dokumenter i overensstemmelse med de juridiske kravene i ulike land/områder. ER lar deg administrere disse formatene i deres livssyklus. Du kan for eksempel innføre nye lovbestemte krav, og kan generere forretningsdokumenter i det riktige formatet for elektronisk utveksling av informasjon med statlige instanser, banker og andre parter. ER-motoren er rettet mot bedriftsbrukere i stedet for utviklere. Siden du konfigurere formater, ikke kode, er prosessen med å opprette og justere formater for elektroniske dokumenter raskere og enklere. ER støtter regnearkformatene TEKST, XML og OPENXML. Et filtypegrensesnitt gir imidlertid støtte for flere formater.

## <a name="capabilities"></a>Muligheter
ER-motoren har følgende funksjoner:

-   Den representerer ett felles verktøy for elektronisk rapportering i forskjellige områder, og erstatter mer enn 20 forskjellige motorer som utfører en slags elektronisk rapportering i Microsoft Dynamics 365 for Operations.
-   Den isolerer rapportformatet fra gjeldende Dynamics 365 for Operations-implementering. (Med andre ord, formatet kan brukes for ulike versjoner av Microsoft Dynamics 365 for Operations.)
-   Den støtter oppretting av et tilpasset format som er basert på et opprinnelig format. Den inkluderer funksjoner for å automatisk oppgradere det egendefinerte formatet når det gjøres endringer til det opprinnelige formatet fordi krav til lokalisering/tilpassing er innført.
-   Den blir det primære standardverktøyet for å støtte for lokaliseringskrav i elektronisk rapportering, både for Microsoft og Microsoft-partnere.
-   Den støtter muligheten til å distribuerte formater til partnere og kunder via Microsoft Dynamics Lifecycle Services (LCS).

## <a name="concepts"></a>Begreper
### <a name="components"></a>Komponenter

ER støtter de to komponenttypene **Datamodell** og **Format**.

#### <a name="data-model-components"></a>Datamodellkomponenter

En datamodellkomponent er en abstrakt representasjon av en datastruktur, og den brukes for å beskrive et bestemt forretningsområde med nok detaljer til å oppfylle rapporteringskravene for dette området. En datamodellkomponent består av følgende deler:

-   en datamodell som et sett med områdespesifikke forretningsenheter, og hierarkisk strukturert definisjon av relasjoner mellom disse enhetene.
-   En modelltilordning som kobler valgte Microsoft Dynamics 365 for Operations-datakilder til enkeltelementer i en datamodell, som under kjøring angir dataflyten og reglene for utfylling av forretningsdata for en datamodellkomponent.

En forretningsenhet for en datamodell representeres som en beholder (post). Egenskaper for forretningsenhet representeres som dataelementer (felt). Hvert dataelement har unik navn, etikett, beskrivelse og verdi. Verdien for hvert dataelement kan være utformet slik at det blir gjenkjent som streng, heltall, desimaltall, dato, opplistingstype, boolsk og så videre. I tillegg kan det være en annen post eller postliste. Én enkelt datamodellkomponent kan inneholde flere hierarkier for områdespesifikke forretningsenheter, i tillegg til modelltilordninger som støtter en bestemt rapportspesifikk dataflyt under kjøring. Hierarkiene skilles med én enkelt post som er valgt som roten for modelltilordning. Datamodellen for betalingsområdet kan for eksempel støtte følgende tilordninger:

-   Firma -&gt; Leverandør -&gt; Betalingstransaksjoner for AP-område
-   Kunde -&gt; Firma -&gt; betalingstransaksjoner for AR-område

Vær oppmerksom på at forretningsenheter (for eksempel firma og betalingstransaksjoner) utformes én gang. Forskjellige tilordninger kan deretter bruke dem på nytt. En modelltilordning har følgende funksjoner:

-   Den kan bruke forskjellige datatyper for Dynamics 365 for Operations som datakilder for en datamodell. Den kan for eksempel bruke tabeller, dataenheter, metoder eller opplistinger.
-   Den støtter parametere for inndata som kan defineres som datakilder for en datamodell når noen data må angis under kjøring.
-   Den støtter transformeringen av Dynamics 365 for Operations-data til nødvendige grupper, filtre, sortering og summeringsdata, og føyes også til logisk beregnede felt som er utviklet gjennom Microsoft Excel-lignende formler (Hvis du vil ha mer informasjon, kan du se [Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)).

[![Excel-lignende formelredigering](./media/pic-formula-1024x615.png)](./media/pic-formula.png)En datamodellkomponent er utformet for hvert forretningsområde som skal brukes som felles datakilde for rapportering som isolerer rapportering fra den fysiske implementeringen av Dynamics 365 for Operations -datakilder, og representere områdespesifikke forretningsbegreper og -funksjoner i et format som gjør at rapporteringsformatets innledende utforming og ytterligere vedlikehold mer effektivt.

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
-   **AVSLUTTET**-versjonen kan konverteres til en **DELT**-versjon. Denne versjonen er publisert på LCS og kan brukes i globale rapporteringsprosesser.
-   **DELT**-versjonen kan konverteres til en **AVSLUTTET**-versjon. Denne versjonen kan deretter slettes.

Versjoner som har statusen** FULLFØRT eller **DELT**, er tilgjengelig for annen datautveksling. En komponent som har disse statusene, kan ha disse handlingene utført:

-   De kan serialiseres i XML-format og eksporteres fra Dynamics 365 for Operations som en fil i XML-format.
-   De kan serialiseres på nytt fra en XML-fil og importeres til Dynamics 365 for Operations som en ny versjon av en ER-komponent.

#### <a name="component-date-effectivity"></a>Datogyldighet for komponent

ER-komponentversjoner har datogyldighet. **Gyldig fra**-datoen kan defineres for en ER-komponent for å angi startdatoen som komponenten er gyldig fra for rapporteringsprosesser. Dynamics 365 for Operations-øktdatoen brukes for å definere om en komponent er gyldig for kjøring. Hvis flere enn én versjon er gyldig for en bestemt dato, brukes den nyeste versjonen for rapporteringsprosessen.

#### <a name="component-access"></a>Komponenttilgang

Tilgang til ER-formatkomponenter avhenger av innstillingen for ISO-kode for land/område. Når denne innstillingen er tom for en valgt versjon av en formatkonfigurasjon, er en formatkomponent tilgjengelig fra et Dynamics 365 for Operations-firma ved kjøretid. Når denne innstillingen inneholder ISO-koder for land/område, er en formatkomponent bare tilgjengelig fra Dynamics 365 for Operations-firmaene som har en primæradresse som er definert for én av ISO-kodene for land/område for formatkomponenten. Forskjellige versjoner av en dataformatkomponent kan ha ulike innstillinger for ISO-koder for land/område.

#### <a name="configuration"></a>Konfigurasjon

En ER-konfigurasjon er wrapper for en bestemt ER-komponent: **Datamodell** eller **Format**. En konfigurasjon kan inneholde forskjellige versjoner av en bestemt ER-komponent. Hver konfigurasjon er merket som eid av en bestemt konfigurasjonsleverandør. **UTKAST**-versjonen av en komponent i en konfigurasjon kan redigeres når eieren av konfigurasjonen er valgt som en aktive leverandør i ER-innstillingene i Dynamics 365 for Operations. Hver modellkonfigurasjon inneholder en **Datamodell**-komponent. En ny formatkonfigurasjon kan komme fra (utledes) en bestemt datamodellkonfigurasjon. Formatkonfigurasjonen som opprettes, presenteres i konfigurasjonstreet som en underordnet av den opprinnelige datamodellkonfigurasjonen. Formatkonfigurasjonen som opprettes, inneholder en **Format**-komponent. **Datamodell**-komponenten for den opprinnelige modellkonfigurasjonen settes automatisk inn i **Format**-komponenten for den underordnede formatkonfigurasjonen som standard datakilde. En ER-konfigurasjon er delt for Dynamics 365 for Operations-firmaer.

#### <a name="provider"></a>Leverandør

ER-leverandør er parts-ID-en som brukes til å angi forfatteren (eier) av hver ER-konfigurasjon. ER lar deg administrere listen over konfigurasjonsleverandører. Formatkonfigurasjoner som leveres for elektroniske dokumenter som en del av Dynamics 365 for Operations-løsningen, er merket som eid av konfigurasjonsleverandøren **Microsoft**.

#### <a name="repository"></a>Repositorium

Et ER-repositorium lagrer ER-konfigurasjoner. Følgende typer ER-repositorier støttes: **Operasjonsressurser** og **LCS-prosjekt**. Et ** Operasjonsressurser**-repositorium gir tilgang til listen over konfigurasjoner som leveres som en ER-konfigurasjonsleverandør, som en del av Dynamics 365 for Operations-løsningen fra Microsoft. Disse konfigurasjonene kan importeres til den gjeldende forekomst av Dynamics 365 for Operations og brukes til elektronisk rapportering. De kan også brukes til tilleggslokaliseringer/-tilpassinger. **LCS-prosjekt**-repositoriet gir tilgang til listen over konfigurasjoner for et bestemt LCS-prosjekt (aktivabibliotek for LCS-prosjekt), som ble valgt under registrering av repositoriet. ER lar deg laste opp delte konfigurasjoner fra gjeldende Dynamics 365 for Operations-forekomst til et bestemt **LCS-prosjekt**-repositorium. Du kan også importere konfigurasjoner fra et bestemt **LCS-prosjekt**-repositorium til gjeldende Dynamics 365 for Operations-forekomst. Nødvendige **LCS-prosjekt**-repositorier kan registreres individuelt for hver enkelt konfigurasjonsleverandør for gjeldende Dynamics 365 for Operations-forekomst. Hvert repositorium kan reserveres for en bestemt konfigurasjonsleverandør.

## <a name="supported-scenarios"></a>Scenarier som støttes
### <a name="building-a-data-model"></a>Bygge en datamodell

ER tilbyr en modellutforming som du kan bruke for å bygge en datamodell for et bestemt forretningsområde. Alle områdespesifikke forretningsenheter og relasjoner mellom dem, kan være representert i en datamodell som en hierarkisk struktur. Illustrasjonen nedenfor viser et eksempel på denne typen datamodell (datamodellen for betalingsområde). [![Eksempel på en datamodell](./media/pic-data-model-1024x550.png)](./media/pic-data-model.png) Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Utforme domenespesifikk datamodell** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="translating-data-model-content"></a>Oversette datamodellinnhold

Datamodellinnhold (etiketter og beskrivelser) kan oversettes til andre språk som Dynamics 365 for Operations støtter. Du vil kanskje oversette datamodellinnhold av følgende årsaker:

-   Gjøre innholdet tydeligere under utformingen for formatutviklere som snakker et annet språk, som skal bruke en datamodell for datatilordning av formatkomponenter.
-   Gjøre innholdet mer brukervennlig ved kjøretid ved å presentere spørsmål og hjelp for kjøretidsparameterne, og også konfigurerte valideringsmeldinger (feil og advarsler) på foretrukket språk for pålogget Dynamics 365 for Operations-bruker.

Illustrasjonen nedenfor viser et eksempel på hvordan datamodellinnhold kan oversettes fra engelsk til japansk. [![Datamodellinnhold i engelsk](./media/pic-translate-en-1024x495.png)](./media/pic-translate-en.png)[![Datamodellinnhold som er oversatt til japansk](./media/pic-translate-ja-1024x495.png)](./media/pic-translate-ja.png)

### <a name="configuring-data-model-mappings"></a>Konfigurere datamodelltilordninger

ER inneholder en modelltilordningsutforming som lar brukere tilordne datamodeller som de har utformet, til bestemte Dynamics 365 for Operations-datakilder. Illustrasjonen nedenfor viser et eksempel på denne typen datamodelltilordning (modelltilordning for **SEPA-kredittoverføring** for datamodell for betalingsområde). [![Eksempel på en datamodelltilordning ](./media/pic-model-mapping-1024x551.png)](./media/pic-model-mapping.png) Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Definere modelltilordning og velge datakilder** og **ER Tilordningen datamodell til valgte datakilder** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**).

### <a name="storing-a-designed-model-component-as-a-model-configuration"></a>Lagre en utformet modellkomponent som en modellkonfigurasjon

ER kan lagre en utformet datamodell sammen med tilknyttede datatilordninger som en modellkonfigurasjon for gjeldende Dynamics 365 for Operations-forekomst. Illustrasjonen nedenfor viser et eksempel på denne typen datamodellkonfigurasjon (konfigurasjon for betalingsmodell). [![Eksempel på en datamodellkonfigurasjon](./media/pic-model-configuration-1024x585.png)](./media/pic-model-configuration.png) Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Tilordningen datamodell til valgte datakilder** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="building-a-format-that-uses-a-data-model-as-a-base"></a>Bygge et format som bruker en datamodell som basis

ER støtter at en formatutforming som du kan bruke til å bygge formatet for et bestemt elektronisk dokument for et valgt forretningsområde ved å velge modellkomponenten som basis. Samme ER-formatutforming lar deg tilordne et format som du oppretter for en valgt datamodelltilordning for området som en datakilde. Illustrasjonen nedenfor viser et eksempel på denne typen format (formatkonfigurasjon som støtter **BBS**-betalingsformatet for Storbritannia). [![Eksempel på et format som har en datamodell som basis](./media/pic-format-1024x690.png)](./media/pic-format.png) Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Utforme domenespesifikt format** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="building-a-configuration-to-generate-electronic-documents-in-openxml-worksheet-format"></a>Bygge en konfigurasjon for å generere elektroniske dokumenter i OPENXML-regnearkformat

ER-formatutformingen kan brukes til å bygge et bestemt elektronisk dokument i OPENXML-regnearkformat. Illustrasjonen nedenfor viser et eksempel på denne typen format (en formatkonfigurasjon for å generere OPENXML-regneark med opplysninger om en valgt betalingsjournal):[![Bilde ER-format-Excel](./media/pic-er-format-excel.jpg)](./media/pic-er-format-excel.jpg) For å bli kjent med detaljene i dette scenariet, kan du spille oppgaveveiledningen **ER Opprette en konfigurasjon for rapporter i OPENXML-format** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**). Bruk det refererte Excel-filen under som en mal for utforming av ER-formatet til å fullføre trinnet i en formatmalimport av denne oppgaveveiledningen: [Mal for betalingsrapport (SampleVendPaymWsReport.xlsx)](https://go.microsoft.com/fwlink/?linkid=845202)

### <a name="storing-a-designed-format-component-in-a-format-configuration"></a>Lagre en utformet formatkomponent i en formatkonfigurasjon

ER kan lagre et utformet format sammen med de konfigurerte datatilordningene som en formatkonfigurasjon for gjeldende Dynamics 365 for Operations-forekomst. Den forrige illustrasjonen viser et eksempel på denne typen formatkonfigurasjon (**BBS (Storbritannia)**, som er underordnet av **Betalingsmodell**-konfigurasjonen). Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Utforme områdespesifikt format** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="configuring-dynamics-365-for-operations-to-start-to-use-a-created-format-internally"></a>Konfigurere Dynamics 365 for Operations til å begynne å bruke opprettet format internt

Dynamics 365 for Operations kan konfigureres til å begynne å bruke et opprettet format til å generere elektroniske rapporter. Referansen til den opprettede formatkonfigurasjonen må defineres i innstillingene for et bestemte område. Hvis du for eksempel vil begynne å bruke en ER-formatkonfigurasjon for elektroniske leverandørbetalinger i BBS-format, må formatkonfigurasjonen refereres i bestemte betalingsmåter, som vist i illustrasjonene nedenfor: 

[![Formatkonfigurasjon for BSS (Storbritannia)](media/ger-bacs-uk-format-configuration.png) 

[![Referanse til BBS-format (Storbritannia) i en betalingsmåte](media/ger-bacs-uk-format-method.png) 

Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Bruk format for å generere elektronisk dokument for betaling** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

## <a name="handling-er-components"></a>Behandle ER-komponenter
### <a name="publishing-an-er-component-in-lcs-to-offer-it-externally-localization"></a>Publisere ER-komponent i LCS for å tilby den eksternt (lokalisering)

Eieren av en komponent (modell eller format) som er opprettet, kan bruke ER for å publisere den fullførte versjonen komponenten til LCS. Et repositorium av typen **LCS-prosjekt** for gjeldende ER-konfigurasjonsleverandør er nødvendig. Når statusen for den fullførte versjonen av en komponent endres fra **FULLFØRT** til **DELT**, publiseres denne versjonen i LCS. Når en komponent er publisert til LCS, blir eieren av denne komponenten en leverandør av tjenesten for å støtte komponenten. Hvis formatkomponenten for eksempel er utformet for å generere et juridisk påkrevd elektronisk dokument (for eksempel i henhold til lokaliseringsscenario), antas det at formatet holdes i samsvar med juridiske endringer, og at leverandøren vil utstede nye versjoner av komponenten hver gang nye juridisk krav oppstår. Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Laste opp en konfigurasjon til Lifecycle Services** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="importing-an-er-component-from-lcs-to-use-it-internally"></a>Importere en ER-komponent fra LCS til bruk internt

ER lar deg importere ER-komponenter fra LCS til gjeldende Dynamics 365 for Operations-forekomst. Et repositorium av typen **LCS-prosjekt** kreves. Når en ER-komponent er importert fra LCS til gjeldende Dynamics 365 for Operations-forekomst, blir eieren av forekomsten forbruker av tjenesten, som tilbys av eieren (forfatter) av den importerte komponenten. Hvis en formatkomponent for eksempel er utformet for å generere et bestemt elektronisk dokument fra Dynamics 365 for Operations, som har et spesifikt format for land/områder (lokaliseringsscenario), antas det at tjenesteforbrukeren kan hente eventuelle oppdateringer som gjøres for formatet, slik at det overholder juridisk krav. Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Importere en konfigurasjon fra Lifecycle Services** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**) .

### <a name="building-a-format-selecting-another-format-as-a-base-customization"></a>Bygge et format ved å velge et annet format som basis (tilpasning)

ER lar deg opprette (avlede) en ny komponent fra gjeldende versjon av en komponent (basis) som ble importert fra LCS. En bruker vil for eksempel avlede et nytt format for å implementere noen spesielle krav til et elektronisk dokument (for eksempel et tilleggsfelt eller en omfattende beskrivelse) for å støtte et tilpassingsscenario. Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Oppgrader format ved innføring av ny basisversjon av det** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**).

### <a name="upgrading-a-format-selecting-a-new-version-of-base-format-rebase"></a>Oppgradere et format ved å velge en ny versjon av basisformat (rebasere)

ER lar deg automatisk innføre endringer av den nyeste versjonen av basiskomponenten i gjeldende utkastversjon av den avledede komponenten. Denne prosessen kalles *rebasering*. En ny forskriftsmessig endringer som ble introdusert i den nyeste versjonen av formatet som ble importert fra LCS), kan for eksempel slå sammen automatisk i den tilpassede versjon av dette formatet av det elektroniske dokumentet. Endringer som ikke kan slås sammen automatisk anses som konflikter. Disse konfliktene presenteres for manuell løsing i utformingsverktøyet for den aktuelle komponenten. Hvis du vil gjøre deg kjent med dette scenariet i detalj, spiller du av oppgaveveiledningen **ER Oppgrader format ved innføring av ny basisversjon av det** (en del av forretningsprosessen **7.5.4.3 Anskaffe/utvikle komponenter for IT-tjeneste/-løsning (10677)**).

## <a name="list-of-er-configurations-that-are-delivered-in-the-dynamics-365-for-operations-solution"></a>Oversikt over ER-konfigurasjoner som er avledet i Dynamics 365 for Operations-løsningen
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




