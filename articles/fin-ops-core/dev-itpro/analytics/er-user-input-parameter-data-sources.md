---
title: Bruke datakildene for BRUKERINNDATAPARAMETER til å angi parametere for en rapport
description: Denne artikkelen beskriver hvordan du bruker datakildene for BRUKERINNDATAPARAMETER til å angi parametere for rapporter du genererer.
author: kfend
ms.date: 04/20/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-05-01
ms.dyn365.ops.version: Version 10.0.27
ms.custom: 220314
ms.assetid: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner
ms.openlocfilehash: c6d0f1a0d9c5eb70a9812459a25d5b14407cce7a
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278715"
---
# <a name="use-user-input-parameter-data-sources-to-specify-parameters-for-a-report"></a>Bruke datakildene for BRUKERINNDATAPARAMETER til å angi parametere for en rapport

[!include[banner](../includes/banner.md)]

Når du utformer [Elektronisk rapportering](general-electronic-reporting.md) (ER) som [modelltilordning](er-overview-components.md#model-mapping-component) og komponenter i ER-[format](er-overview-components.md#format-component), kan du bruke datakildene til en *BRUKERINNDATAPARAMETER* til å hente de nødvendige verdiene som kan angis i dataoppføringsfelt i dialogboksen ved kjøretid, før utføringen av et ER-format starter. Denne artikkelen beskriver datakildene *BRUKERINNDATAPARAMETER* som for øyeblikket støttes.

## <a name="mandatory-properties"></a><a name="mandatory-properties"></a>Obligatoriske egenskaper

Du må angi følgende egenskaper for datakilder for hver *BRUKERINNDATAPARAMETER*-type:

- I **Navn**-feltet angir du det interne navnet på datakilden. Du kan bruke dette navnet i andre [uttrykk](er-formula-language.md) og bindinger for den konfigurerte modelltilordningen eller formatkomponenten.

## <a name="optional-properties"></a><a name="optional-properties"></a>Andre egenskaper

Du må eventuelt angi følgende egenskaper for datakilder for en *BRUKERINNDATAPARAMETER*-type:

- I **Etikett**-feltet angir du etiketten som skal brukes for det relaterte dataoppføringsfeltet i dialogboksen ved kjøringstid. Du kan legge til en annen etiketttekst for forskjellige språkkoder ved å aktivere **Etikett**-feltet og deretter velge **Oversett**.
- I **Hjelp**-feltet angir du hjelpeteksten som vises på utformingstidspunktet nederst på siden **Formatutforming** eller **Modelltilordningsutforming** når en redigerbar datakilde for en *BRUKERINNDATAPARAMETER* er valgt. Denne teksten kan gi tilleggsinformasjon om datakilden for å hjelpe brukerne når de konfigurerer det redigerbare formatet eller modelltilordningskomponenten. Du kan legge til en annen hjelpetekst for forskjellige språkkoder ved å velge **Oversett**.

    > [!NOTE]
    > **Oversett**-knappen du kan bruke til å legge til [språkspesifikke etiketter og tekst](er-design-multilingual-reports.md#format-component) blir bare tilgjengelig når du har lagt til datakilden, lagret endringene og deretter åpnet datakilden for redigering på nytt.

- I **Skrivebeskyttet**-feltet konfigurerer du et uttrykk som returnerer en *[boolsk](er-formula-supported-data-types-primitive.md#boolean)* verdi.

    - Hvis det konfigurerte uttrykket returnerer verdien **Sann** ved kjøretid, er det relaterte dataoppføringsfeltet nedtonet i dialogboksen, og du kan ikke endre verdien.
    - Hvis det konfigurerte uttrykket returnerer verdien **Usann** ved kjøretid, eller hvis ingen uttrykk er konfigurert, er det relaterte dataoppføringsfeltet tilgjengelig i dialogboksen, og du kan endre verdien.

- I **Standardverdi**-feltet konfigurerer du et uttrykk som returnerer verdien til den refererte parametertypen. Denne verdien kan brukes til å fylle ut en standardverdi for det relaterte dataoppføringsfeltet i dialogboksen ved kjøringstid.

    Når du kjører et ER-format, lagres verdien du angir i det relaterte dataoppføringsfeltet, i dialogboksen ved kjøretid, i minnet som den tidligere brukte verdien. Tidligere brukte verdier lagres enkeltvis for hvert felt, og kjører ER-format, gjeldende bruker og gjeldende organisasjon (firma).

    - Sett alternativet **Tilbakestill alltid til standardverdi** til **Ja** hvis verdien som returneres av **Standardverdi**-uttrykket, alltid skal brukes som standardverdi, uavhengig av den tidligere brukte verdien.
    - Sett alternativet **Tilbakestill alltid til standardverdi** til **Nei** hvis verdien som returneres av **Standardverdi**-uttrykkverdien, skal brukes som standardverdi bare når den tidligere brukte verdien mangler.

    > [!NOTE]
    > Hvis du setter alternativet **Alltid tilbakestilt til standardverdi** til **Ja**, må det konfigureres et uttrykk i **Standardverdi**-feltet.

- Hvis du setter alternativet **Tillat flere valg** til **Ja**, kan du velge flere verdier for den konfigurerte parameteren ved kjøretid. Hvis du setter den til **Nei**, kan du bare velge en enkelt verdi.

    > [!NOTE]
    > Dette alternativet gjelder ikke for alle *BRUKERINNDATAPARAMETER*. På utformingstidspunktet opprettes det et unntak for å informere brukeren om at den konfigurerte brukerinndataparameteren ikke støtter flere valg, og at bare en enkelt verdi kan velges eller angis.
    >
    > Hvis du setter alternativet **Tillat flerevalg** til **Ja**, og du angav et uttrykk i feltet **Standardverdi**, kan dette uttrykket bare brukes til å angi en enkelt standardverdi.

- Velg alternativet **Rediger synlighet** for å angi om den konfigurerte parameteren skal vises i dialogboksen ved kjøretid.

    > [!NOTE]
    > Standard synlighet for datakilder av typen *BRUKERINNDATAPARAMETER* er avhengig av ER-komponenten som inneholder dem.
    >
    > - Hvis en datakilde er konfigurert i formatkomponenten, er den synlig som standard.
    > - Hvis en datakilde er konfigurert i modelltilordningskomponenten, er den bare synlig hvis verdien til datakilden påvirker resultatet når en ER-komponent kjøres. Du la for eksempel til en datakilde, men brukte den ikke i uttrykk og bindinger for den gjeldende modelltilordningskomponenten. I dette tilfellet vises ikke det relevante dataoppføringsfeltet som standard i dialogboksen ved kjøring. 

    Konfigurer et uttrykk som returnerer en **boolsk** verdi på siden **Formeldesigner** i *Formel*-feltet.

    - Hvis det konfigurerte uttrykket returnerer verdien **Sann** ved kjøretid, eller hvis ingen uttrykk er konfigurert, er det relaterte dataoppføringsfeltet synlig i dialogboksen ved kjøretid.
    - Hvis det konfigurerte uttrykket returnerer verdien **Usann**, er det relaterte dataoppføringsfeltet skjult i dialogboksen ved kjøring. Når det kalles av andre uttrykk ved kjøretid, returneres standardverdien, den tidligere brukte verdien eller standardverdien for gjeldende datatypeverdi, avhengig av andre innstillinger.

## <a name="type-specific-properties"></a>Typespesifikke egenskaper

### <a name="application-dependent-user-input-parameter"></a>Programavhengig brukerinndataparameter

Bruk en datakilde for **Generelt**\> **Brukerinndataparameter**-typen for å hente den nødvendige verdien eller verdiene av en datatype som er angitt for den gjeldende forekomsten av Microsoft Dynamics 365 Finance-programmet. Når du legger til en datakilde av denne typen i en ER-komponent, angir du følgende egenskaper:

- I feltet **Navn på Operations-datatype (EDT, enum)** velger du et program [utvidet datatype (EDT)](../extensibility/extensible-edts.md) eller en programopplisting.

> [!NOTE]
> Vi anbefaler at du går gjennom uttrykkene som er konfigurert i feltene **Skrivebeskyttet** og **Standardverdi** når du endrer referansen for **Navn på Operations-datatype (EDT, enum)** i en redigerbar datakilde av denne *BRUKERINNDATAPARAMETER*-typen.

Illustrasjonen nedenfor viser egenskaper til datakilden `$TaxRegNum` som ble konfigurert i ER-formatkonfigurasjonen **Instat XML (DE)**. Denne datakilden er konfigurert til å bruke *Beskrivelse*-EDT til å tilby dataregistreringsfeltet **Avgiftsregistreringsnummer** i dialogboksen ved kjøringstid.

![Egenskaper til en datakilde av BRUKERINNDATAPARAMETER-typen i dialogboksen på Formatutforming-siden.](./media/er-user-input-parameter-data-sources-01.png)

Illustrasjonen nedenfor viser dialogboksen som vises ved kjøretid når ER-formatkonfigurasjonen **Instat XML (DE)** kjøres for å [generere](../../../finance/localizations/tasks/eur-00002-eu-intrastat-declaration.md) Intrastat-deklareringen. Legg merke til at det konfigurerte feltet **Avgiftsregistreringsnummer** er tilgjengelig for dataregistrering.

![Dialogboksen Intrastat-rapport for det kjørende ER-formatet på Intrastat-siden.](./media/er-user-input-parameter-data-sources-02.png)

### <a name="data-model-enumeration-user-input-parameter"></a>Brukerinndataparameter  for datamodellopplisting

Bruk en datakilde av typen **Datamodell** \> **Brukerinndataparameter for opplisting** for å hente den nødvendige verdien eller verdiene for én enkelt datamodell [opplisting](er-formula-supported-data-types-primitive.md#enumeration). Når du legger til en datakilde av denne typen i en ER-komponent, angir du følgende egenskaper:

- I **Modell**-feltet angir du en referanse til stamdatamodellen.
- Angi en referanse til en opplisting av den refererte datamodellen, i **Modellopplisting**-feltet.
- I **Versjon**-feltet velger du endringsnummeret for ER-datamodellkomponenten som inneholder den refererte modellopplistingen.

    > [!TIP]
    > På utformingstidsprogrammet kan du la **Versjon**-feltet stå tomt for å få tilgang til listen med opplistinger for den refererte datamodellkomponenten som ligger i utkastversjonen av den tilsvarende ER-datamodellkonfigurasjonen. På denne måten kan du redigere utkastversjonen av modelltilordnings- eller formatkomponenten og utkastversjonen til stamdatamodellkomponenten samtidig.
    >
    > Legg imidlertid merke til at **Versjon**-feltet bare kan stå tomt i utkastversjonen til en modelltilordnings- eller formatkomponent. Når du endrer statusen til en ER-modelltilordning eller formatkonfigurasjon fra **Utkast** til **Fullført**, fylles dette feltet automatisk ut med det høyeste modellendringsnummeret som er tilgjengelig i gjeldende Finance-forekomst. Hvis du introduserer en ny opplisting eller en ny opplistingsverdi i utkastversjonen av basisdatamodellen og refererer til den i den redigerbare modelltilordnings- eller formatkomponenten, fullfører du utkastversjonen av basisdatamodellenkonfigurasjonen før utkastversjonen av ER-modelltilordningen eller -formatkonfigurasjonen er fullført. Hvis ikke skjer det et unntak om at banen ikke finnes når du endrer status for modelltilordnings- eller formatkonfigurasjonen fra **Utkast** til **Fullført**. Meldingen informerer deg om at den refererte opplistings- eller opplistingsverdien mangler i stamdatamodellen.

Illustrasjonen nedenfor viser egenskaper til datakilden `$ReportDirection` som ble konfigurert i ER-formatkonfigurasjonen **Instat XML (DE) Contoso**. Konfigurasjonen **Instat XML (DE) Contoso** er [avledet](general-electronic-reporting.md#Configuration) fra **Instat XML-konfigurasjonen (DE)**-konfigurasjonen. Denne datakilden er konfigurert til å bruke *ReportDirection*-modellopplistingen for å tilby riktig oppslagsfelt i dialogboksen ved kjøretid.

![Egenskaper til datakilden for BRUKERINNDATAPARAMETER-typen i dialogboksen på Formatutforming-siden.](./media/er-user-input-parameter-data-sources-03.png)

### <a name="format-enumeration-user-input-parameter"></a>Brukerinndataparameter  for formatopplisting

Bruk en datakilde av typen **Formatopplisting** \> **Brukerinndataparameter for opplisting** for å hente den nødvendige verdien eller verdiene for én enkelt formatopplisting. Når du legger til en datakilde av denne typen i en ER-komponent, angir du følgende egenskaper:

- Angi en opplisting av det redigerbare formatet i **Formatopplisting**-feltet.

> [!NOTE]
> Datakilder av denne typen kan bare konfigureres i området av den redigerbare formatkomponenten.

## <a name="additional-resources"></a>Tilleggsressurser

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Initialisere datakildeverdier av typen USER INPUT PARAMETER fra kildekoden](er-initiate-uip-data-source-value-from-source-code.md)
