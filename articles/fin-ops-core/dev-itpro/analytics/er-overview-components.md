---
title: Komponenter i elektronisk rapportering
description: Denne artikkelen beskriver ER-komponentene (elektronisk rapportering).
author: kfend
ms.date: 09/28/2021
ms.topic: overview
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58941
ms.assetid: 5d51b6a6-ad12-4af9-a66d-a1eb820ae57f
ms.search.form: ERWorkspace
ms.openlocfilehash: 4851374ca4943a84d35f063e0ee65b537ec3b6cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285039"
---
# <a name="electronic-reporting-components"></a>Komponenter i elektronisk rapportering

[!include [banner](../includes/banner.md)]

Elektronisk rapportering (ER) støtter følgende typer komponenter:

- Datamodell
- Modelltilordning
- Format
- Metadata

## <a name="data-model-component"></a>Datamodellkomponent

En datamodellkomponent er en abstrakt representasjon av en datastruktur. Den beskriver et bestemt bedriftsdomeneområde med nok detaljer for å oppfylle kravene til rapportering for dette domenet. En datamodellkomponent består av følgende deler:

- **Datamodell** – Et sett med områdespesifikke forretningsenheter, og hierarkisk strukturert definisjon av relasjoner mellom disse enhetene.
- **Modelltilordning** – Valgte programdatakilder kobles til enkeltelementer i en datamodell, som under kjøring angir dataflyten og reglene for utfylling av forretningsdata i en datamodellkomponent.

Forretningsenhetet for en datamodell representeres som en container, eller post. Egenskaper for forretningsenhet representeres som dataelementer, eller felt. Hvert dataelement har unik(t) navn, etikett, beskrivelse og verdi. Verdien for hvert dataelement kan være utformet slik at det blir gjenkjent som streng, heltall, desimaltall, dato, opplisting eller boolsk verdi. I tillegg kan dataelementet være en annen post eller postliste.

En enkelt datamodellkomponent kan inneholde flere hierarkier for domenespesifikke forretningsenheter. Det kan også inneholde modelltilordninger som støtter en rapportspesifikk dataflyt ved kjøring. Hierarkiene skilles med én enkelt post som er valgt som roten for modelltilordning. Datamodellen for betalingsområdet kan for eksempel støtte følgende tilordninger:


- Firma \> Leverandør \> Betalingstransaksjoner for AP-område
- Kunde \> Firma \> Betalingstransaksjoner for AR-område

Forretningsenheter, for eksempel firma og betalingstransaksjoner, utformes bare én gang. Ulike tilordninger kan bruke dem på nytt etter behov.

## <a name="model-mapping-component"></a>Modelltilordningskomponent

Modelltilordning kobler valgte programdatakilder kobles til enkeltelementer i en datamodell, som under kjøring angir dataflyten og reglene for utfylling av forretningsdata i en datamodellkomponent.

En modelltilordning som støtter utgående elektroniske dokumenter har følgende funksjoner:

- Den kan bruke forskjellige datatyper som datakilder for en datamodell. Disse datatypene inkluderer tabeller, dataenheter, metoder og opplistinger.
- Den støtter parametere for inndata som kan defineres som datakilder for en datamodell når noen data må angis under kjøring.
- Det støtter transformasjon av data i nødvendige grupper. Du kan også kan du filtrere, sortere og summere data og legge til logiske beregnede felt som er laget ved hjelp av formler som ligner på Microsoft Excel-formler. Hvis du vil ha mer informasjon, se [Formeldesigner i Elektronisk rapportering (ER)](general-electronic-reporting-formula-designer.md).

En modelltilordning som støtter innkommende elektroniske dokumenter har følgende funksjoner:

- Den kan bruke forskjellige oppdaterbare dataelementer som mål. Disse dataelementene inkluderer tabeller, visninger og data-enheter. Dataene kan oppdateres av innkommende data fra elektroniske dokumenter. Flere mål kan brukes i en enkelt modell-tilordning.
- Den støtter parametere for inndata som kan defineres som datakilder for en datamodell når noen data må angis under kjøring.

En datamodellkomponent er utviklet for hvert forretningsdomene som brukes som en felles datakilde for rapportering. Den felles datakilden isolerte rapportering fra den fysiske implementeringen av datakilder. Komponenten representerer domenespesifikke forretningsbegreper og funksjoner i et skjema som gjør et rapporteringsformats opprinnelige utforming og ytterligere vedlikehold mer effektivt.

## <a name="format-component"></a>Formatkomponent

### <a name="format-components-for-outgoing-electronic-documents"></a>Formatkomponenter for utgående elektroniske dokumenter

En formatkomponent er oppsettet for rapporteringsutdataene som genereres under kjøring. Et utvalg består av følgende elementer:

- Et format som definerer strukturen og innholdet i det utgående elektroniske dokumentet som genereres under kjøring.
- Datakilder, som et sett med inndataparametre og en områdespesifikk datamodell som bruker modelltilordning.
- En formattilordning, som et sett av bindingene for formatdatakilder som har enkelte elementene i et format som under kjøring angir dataflyt og regler for generering av utdataformat.
- En formatvalidering, som et sett med konfigurerbar regler som styrer rapportgenerering under kjøring avhengig av kjørekontekst. Det kan for eksempel være en regel som stopper utdatagenerering av en leverandørs betalinger og genererer et unntak når bestemte attributter for den valgte leverandøren mangler, for eksempel bankkontonummeret.

En formatkomponent støtter følgende funksjoner:

- Oppretting av rapporteringsutdata som individuelle filer i forskjellige formater, som tekst, XML, Microsoft Word-dokument eller regneark
- Oppretting av flere filer separat, og innkapsling av filene i ZIP-filer

En formatkomponent gjør det mulig å vedlegge bestemte filer, som kan brukes i rapporteringsutdataene:

- Excel-arbeidsbøker som inneholder et regneark som kan brukes som en mal for utdata i OPENXML-regnearkformatet
- Word-filer som inneholder et dokument som kan brukes som en mal for utdata i Microsoft Word-dokumentformatet
- Andre filer som kan inkluderes i formatutdataene som forhåndsdefinerte filer

Illustrasjonen nedenfor viser hvordan dataene flyter for disse formatene.

[![Dataflyt for utgående formatkomponenter](./media/ER-overview-02.png)](./media/ER-overview-02.png)

Hvis du vil kjøre en enkelt ER-formatkonfigurasjonen og generere et utgående elektroniske dokument, må du identifisere tilordningen til formatkonfigurasjonen.

#### <a name="format-components-for-incoming-electronic-documents"></a>Formatkomponenter for innkommende elektroniske dokumenter
En formatkomponent er oppsettet for det innkommende dokumentet som importeres under kjøring. Et utvalg består av følgende elementer:

- Et format som definerer strukturen og innholdet i det innkommende elektroniske rapporteringsdokumentet som inneholder data som importeres under kjøring. En formatkomponent brukes til å analysere et innkommende dokument i forskjellige formater, for eksempel tekst og XML.
- En formattilordning som binder individuelle formaterelementer til elementer i en domenespesifikk datamodell. Ved kjøreti angir elementene i datamodellen dataflyten og reglene for å importere data fra et innkommende dokument, og lagrer deretter dataene i en datamodell.
- En formatvalidering, som et sett med konfigurerbar regler som styrer dataimport under kjøring avhengig av kjørekontekst. Det kan for eksempel være en regel som stopper datamimport av et bankkontoutdrag som har en leverandørs betalinger, og genererer et unntak når en bestemt leverandørs attributter mangler, for eksempel leverandøridentifikasjonskode.

Illustrasjonen nedenfor viser hvordan dataene flyter for disse formatene.

[![Dataflyt for innkommende formatkomponenter](./media/ER-overview-03.png)](./media/ER-overview-03.png)

Hvis du vil kjøre en enkelt ER-formatkonfigurasjon for å importere data fra et innkommende elektronisk dokument, må du identifisere ønsket tilordning til en formatkonfigurasjonen samt integreringspunktet til en modelltilordning. Du kan bruke samme modelltilordning og mål med ulike formater for ulike typer innkommende dokumenter.


## <a name="component-versioning"></a>Versjonskontroll av komponenter

Versjonskontroll støttes for ER-komponenter. Følgende arbeidsflyt leveres for å behandle endringer i ER-komponenter:

1. Versjonen som opprinnelig opprettes, er merket som en **Utkast**-versjon. Denne versjonen kan redigeres og er tilgjengelig for testkjøringer.
2. **Utkast**-versjonen kan konverteres til en **Fullført**-versjon. Denne versjonen kan brukes i lokale rapporteringsprosesser.
3. **Fullført**-versjonen kan konverteres til en **Delt**-versjon. Denne versjonen er publisert i Microsoft Dynamics Lifecycle Services (LCS) og kan brukes i globale rapporteringsprosesser.
4. **Delt**-versjonen kan konverteres til en **Avsluttet**-versjon. Denne versjonen kan slettes.

Versjoner som har statusen **Fullført** eller **Delt**, er tilgjengelig for annen datautveksling. Følgende handlinger kan utføres på en komponent som har disse statusene:

- Komponenten kan serialiseres i XML-format og eksporteres som en fil i XML-format.
- Komponenten kan serialiseres på nytt fra en XML-fil og importeres til programmet som en ny versjon av en ER-komponent.

Hvis du vil ha mer informasjon, kan du se [Importer en ny datamodellkonfigurasjon](er-quick-start1-new-solution.md#ImportDataModel) og [Eksporter fullført versjon av et avledet format](er-calculated-field-type.md#export-completed-version-of-a-derived-format).

### <a name="draft-versions-at-runtime"></a>Utkastversjoner ved kjøretid

I dine personlige brukerparametere for ER-rammeverket kan du aktivere alternativet som lar deg angi om utkastversjonen av en ER-konfigurasjon må brukes ved kjøretid. Hvis du vil ha informasjon om hvordan du gjør alternativet **Kjør utkast** tilgjengelig for ER-konfigurasjonene, kan du se [Merk et egendefinert format som kjørbart](er-quick-start2-customize-report.md#MarkFormatRunnable).

> [!NOTE]
> ER-brukerparametere er firmaspesifikke og brukerspesifikke.

### <a name="draft-format-versions-at-runtime"></a>Utkastformatversjoner ved kjøretid

Som standard blir kladdversjonene av formatkomponentene ignorert når du kjører en ER-løsning. I stedet brukes bare den relevante versjonen som har en annen status enn **Utkast**. Noen ganger kan det hende at du vil tvinge ER til å bruke kladdversjonen av ER-formatkonfigurasjonen ved kjøretid. Når du for eksempel innfører nødvendige endringer i kladdeversjonen, kan du bruke utkastversjonen til å kjøre testen. På denne måten kan du validere riktigheten av endringene. [Sett](er-quick-start2-customize-report.md#MarkFormatRunnable) **Kjør utkast**-alternativet for den relevante ER-konfigurasjonen til **Ja**.

### <a name="draft-model-mapping-versions-at-runtime"></a>Utkast til modelltildelingsversjoner ved kjøretid

Som standard blir kladdversjonene av modelltildelingskomponentene alltid brukt når du kjører en ER-løsning. Noen ganger kan det hende at du vil tvinge ER til å ignorere kladdversjonen av ER-modelltildelingskonfigurasjonen ved kjøretid. I **versjon 10.0.29 og nyere** kan du aktivere funksjonen **Ta alltid i betraktning alternativet Kjør utkast for ER-modelltildelinger** for å styre modelltildelingsversjonen som brukes ved kjøretid. Når denne funksjonen er aktivert, skjer følgende:

- Når alternativet **Kjør utkast** er satt til **Nei** for en modelltildelingskonfigurasjon, brukes den høyeste ikke-utkastversjonen av denne konfigurasjonen ved kjøretid. Et unntak opprettes hvis konfigurasjonen ikke er tilgjengelig i nåværende Finance-forekomst.
- Når alternativet **Kjør utkast** er satt til **Ja** for en modelltildelingskonfigurasjon, brukes utkastversjonen av denne konfigurasjonen ved kjøretid.

## <a name="component-date-effectivity"></a>Datogyldighet for komponent

ER-formatkomponentversjoner har datogyldighet. Du kan angi "Gyldig fra"-datoen for en ER-formatkomponent for å angi startdatoen som komponenten er gyldig fra for rapporteringsprosesser. Øktdatoen for programmet brukes for å definere om en komponent er gyldig for kjøring. Hvis flere enn én versjon er gyldig for en bestemt dato, brukes den nyeste versjonen for rapporteringsprosessen.

## <a name="component-access"></a>Komponenttilgang

Tilgang til ER-format- og -modelltildelingskomponenter ved kjøretid avhenger av innstillingen for International Organization for Standardization (ISO)-kode for land/område. Hvis denne innstillingen er tom for en valgt versjon av en format- eller modelltildelingskonfigurasjon, er en format- eller modelltildelingskomponent tilgjengelig fra et firma ved kjøretid. Hvis innstillingen inneholder ISO-koder for land/område, er en format- eller modelltildelingskomponent bare tilgjengelig fra firmaene som har en primæradresse som er definert for én av ISO-kodene for land/område for formatkomponenten.

Forskjellige versjoner av en format- eller modelltildelingskomponent kan ha ulike innstillinger for ISO-koder for land/område.

Hvis du vil ha mer informasjon, kan du se, [Konfigurer modelltildelinger for landkontekstavhengig ER](er-country-dependent-model-mapping.md).

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]

