---
title: Utform en ny ER-løsning for å skrive ut ZPL-etiketter
description: Denne artikkelen forklarer hvordan du utformer en ny ER-løsning (elektronisk rapportering) for å skrive ut ZPL-etiketter (Zebra Programming Language).
author: kfend
ms.date: 02/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-02-01
ms.dyn365.ops.version: 10.0.26
ms.custom: 97423
ms.assetid: f3055a27-717a-4c94-a912-f269a1288be6
ms.search.form: ERSolutionTable, ERFormatDestinationTable
ms.openlocfilehash: 7ef83cf4822ca129af3ca01fa6ddd05219fee0d7
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9271771"
---
# <a name="design-a-new-er-solution-to-print-zpl-labels"></a>Utform en ny ER-løsning for å skrive ut ZPL-etiketter

[!include [banner](../includes/banner.md)]


Denne artikkelen forklarer hvordan en bruker med en rolle som systemansvarlig, utvikler av elektronisk rapportering eller funksjonell konsulent for elektronisk rapportering kan konfigurere parametere for rammeverket for [elektronisk rapportering (ER)](general-electronic-reporting.md), utforme nødvendige ER-[konfigurasjoner](general-electronic-reporting.md#Configuration) for en ny ER-løsning for å få tilgang til dataene i lagerstyringssystemet og generere egendefinerte lagerlokasjonsetiketter i ZPL II-format (Zebra Programming Language). Denne fremgangsmåten kan gjennomføres i firmaet **USRT**.

## <a name="business-scenario"></a>Forretningsscenario

Du representerer et firma som implementerte lagerstyring i Microsoft Dynamics 365 Finance. Hver lagerlokasjon må merkes med en selvklebende etikett som omfatter en strekkode. Lagerarbeidere bruker håndholdte strekkodelesere til å skanne strekkodene.

Alle lagerlokasjoner er merket innenfor området for aktiviteter før aktivering. Du må imidlertid også kunne skrive ut lagerlokasjonsetiketter ved behov hvis eksisterende etiketter blir skadet eller lagerhyllene blir omkonfigurert. Når du bruker nylig utgitt ER-funksjonalitet, kan du konfigurere en ny ER-løsning som gjør at en lagersjef kan skrive ut etiketter direkte på en termisk etikettskriver.

## <a name="configure-the-er-framework"></a>Konfigurere ER-rammeverket

Følg trinnene i [Konfigurere ER-rammeverket](er-quick-start2-customize-report.md#ConfigureFramework) for å konfigurere minimumssettet med ER-parametere. Du må fullføre denne konfigurasjonen før du begynner å bruke ER-rammeverket til å utforme en ny ER-løsning.

## <a name="design-a-domain-specific-data-model"></a>Utforme en domenespesifikk datamodell

Opprett en ny ER-konfigurasjon som inneholder en [datamodell](er-overview-components.md#data-model-component) komponent for lagerstyringsdomenet. Denne datamodellen vil senere bli brukt som datakilde når du utformer et ER-format for å generere lagerlokasjonsetiketter.

### <a name="import-a-data-model-configuration"></a>Importere en datamodellkonfigurasjon

Følg denne fremgangsmåten for å importere den nødvendige datamodellen fra en XML-fil fra Microsoft. Du kan alternativt opprette din egen datamodell som beskrevet i neste del.

1. Last ned filen [Warehouse model.version.1.xml](https://download.microsoft.com/download/9/f/1/9f136e9b-bf5f-403a-b089-a2b2ed1da2ba/Warehouse-model.version.1.xml), og lagre den på den lokale datamaskinen.
2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.
4. På siden **Konfigurasjoner** velger du **Exchange** \> **Last fra XML-fil** i handlingsruten.
5. Velg **Bla gjennom**, og finn og velg deretter filen **Warehouse model.version.1.xml**.
6. Velg **OK** for å importere konfigurasjonen.

![Importert ER-datamodellkonfigurasjon på konfigurasjonssiden.](./media/er-design-zpl-labels-imported-model.png)

### <a name="create-a-data-model-configuration"></a>Opprette en datamodellkonfigurasjon

Du kan opprette en datamodell fra grunnen av i stedet for å importere datamodellfilen fra Microsoft. Hvis du vil se et eksempel som viser hvordan du fullfører denne oppgaven, kan du se [Opprett en ny datamodellkonfigurasjon](er-quick-start1-new-solution.md#DesignDataModel).

### <a name="review-the-data-model"></a>Se gjennom datamodellen

Du kan vise en redigerbar versjon av den konfigurerte datamodellen på siden **Datamodellutforming**.

![Strukturen til ER-datamodellen på siden Datamodellutforming.](./media/er-design-zpl-labels-model.png)

## <a name="design-a-model-mapping-for-the-configured-data-model"></a>Utforme en modelltilordning for den konfigurerte datamodellen

Som en bruker med rollen som utvikler av elektronisk rapportering må du opprette en ny ER-konfigurasjon som inneholder en komponent for [modelltilordning](er-overview-components.md#model-mapping-component) for lagerdatamodellen. Denne komponenten implementerer den konfigurerte datamodellen for Dynamics 365 Finance og gjelder spesifikt for denne appen. Du må konfigurere den for å angi programobjektene som skal brukes til å fylle ut den konfigurerte datamodellen med programdata ved kjøring. For å kunne fullføre denne oppgaven må du forstå hvordan datastrukturen i bedriftsdomenet for lagerstyring er implementert i Finance.

### <a name="import-a-model-mapping-configuration"></a>Importere en modelltilordningskonfigurasjon

Følg denne fremgangsmåten for å importere den nødvendige modelltilordningen fra en XML-fil fra Microsoft. Du kan alternativt opprette din egen modelltilordning som beskrevet i neste del.

1. Last ned filen [Warehouse model mapping.version.1.1.xml](https://download.microsoft.com/download/1/c/c/1cc94d28-3d90-4ffd-a118-77d6c322904f/Warehouse-model-mapping.version.1.1.xml), og lagre den på den lokale datamaskinen.
2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.
4. På siden **Konfigurasjoner** velger du **Exchange** \> **Last fra XML-fil** i handlingsruten.
5. Velg **Bla gjennom**, og finn og velg filen **Warehouse model mapping.version.1.1.xml**.
6. Velg **OK** for å importere konfigurasjonen.

![Importert ER-modelltilordningskonfigurasjon på konfigurasjonssiden.](./media/er-design-zpl-labels-imported-mapping.png)

### <a name="create-a-model-mapping-configuration"></a>Opprette en modelltilordningskonfigurasjon

Du kan opprette en modelltilordning fra grunnen av i stedet for å importere modelltilordningsfilen fra Microsoft. Hvis du vil se et eksempel som viser hvordan du fullfører denne oppgaven, kan du se [Opprette en ny modelltilordningskonfigurasjon](er-quick-start1-new-solution.md#CreateModelMapping).

### <a name="review-the-model-mapping"></a>Se gjennom modelltilordningen

Du kan vise en redigerbar versjon av den konfigurerte modelltilordningen på siden **Modelltilordningsutforming**.

![Strukturen til ER-modelltilordningen på siden Modelltilordningsutforming.](./media/er-design-zpl-labels-mapping.png)

## <a name="design-a-format"></a>Utforme et format

Som en bruker med rollen som funksjonsrådgiver for elektronisk rapportering må du opprette en ny ER-konfigurasjon som inneholder en komponent av typen [format](er-overview-components.md#format-component). Du konfigurerer denne komponenten ved å bruke ZPL II-kode til å angi oppsettet for lagerlokasjonsetiketten.

### <a name="import-a-format-configuration"></a>Importere en formatkonfigurasjon

Følg denne fremgangsmåten for å importere det nødvendige formatet fra en XML-fil fra Microsoft. Du kan alternativt opprette ditt eget format som beskrevet i neste del.

1. Last ned filen [Warehouse location labels.version.1.1.xml](https://download.microsoft.com/download/5/7/5/5758b551-69a5-45bd-a2b2-21c3db73a6fc/Warehouse-location-labels.version.1.1.xml), og lagre den på den lokale datamaskinen.
2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.
4. På siden **Konfigurasjoner** velger du **Exchange** \> **Last fra XML-fil** i handlingsruten.
5. Velg **Bla gjennom**, og finn og velg filen **Warehouse location labels.version.1.1.xml**.
6. Velg **OK** for å importere konfigurasjonen.

![Importert ER-formatkonfigurasjon på konfigurasjonssiden.](./media/er-design-zpl-labels-imported-format.png)

### <a name="create-a-format-configuration"></a>Opprette en formatkonfigurasjon

Du kan opprette et format fra grunnen av i stedet for å importere formatfilen fra Microsoft. Hvis du vil se et eksempel som viser hvordan du fullfører denne oppgaven, kan du se [Opprette en ny formatkonfigurasjon](er-quick-start1-new-solution.md#FormatCreate).

### <a name="review-the-format"></a>Se gjennom format

Du kan vise en redigerbar versjon av det konfigurerte formatet på siden **Formatutforming**.

![Strukturen til ER-formatet på siden Formatutforming.](./media/er-design-zpl-labels-format.png)

Datakilden `model.Location.Label` for dette formatet er konfigurert slik at den genererer etiketter som inneholder følgende informasjon:

- Lagertittelen som tekst
- Lagertittelen som en strekkode
- Lokasjonstittelen
- Kontrollsifre

På **Formeldesigner**-siden for datakilden inneholder ER-formelen som brukes til å generere etiketter, en `CONCATENATE`-funksjon som kombinerer informasjonen i det ønskede oppsettet.

![Formel for datakilden på siden Formeldesigner.](./media/er-design-zpl-labels-review-formula.png)

> [!TIP]
> Etikettoppsettet er utformet slik at lokasjonstittelen og kontrollsifrene er på midten av etiketten. ZPL II støtter imidlertid ikke midtjustering for strekkoder. Formelen for datakilden `model.Location.Warehouse.Alignment` brukes derfor til å plassere strekkoden på midten av etiketten. Denne formelen beregner venstre forskyvning av strekkoden basert på antall tegn i lagertittelen.

## <a name="prepare-your-environment-for-previewing-generated-labels"></a>Klargjøre miljøet for forhåndsvisning av genererte etiketter

Eksemplet nedenfor bruker et skriveremulatorprogram for ZPL-etiketter til å vise en forhåndsvisning av genererte etiketter på skjermen. Følg disse trinnene for å aktivere dette alternativet.

1. Legg til ER-målet [Skriver](er-destination-type-print.md) for ER-formatet **Lagerlokasjonsetikett**, og konfigurer det slik at det sender genererte etiketter fra Finance til [dokumentrutingsagenten](install-document-routing-agent.md).
2. Installer og konfigurer dokumentrutingsagenten slik at den ruter genererte etiketter fra Finance til en lokal skriver som er tilgjengelig fra gjeldende arbeidsstasjon.
3. Legg til en lokal skriver for den gjeldende arbeidsstasjonen, og konfigurer den slik at den sender genererte etiketter fra dokumentrutingsagenten til et skriveremulatorprogram.
4. Installer et skriveremulatorprogram som en utvidelse i nettleseren Chrome, og konfigurer det slik at det sender genererte etiketter fra en lokal skriver til en nettjeneste som gjengir genererte etiketter og returnerer dem til skriveremulatoren for å forhåndsvises.

<table>
<tbody>
<tr align="center">
<td>
<p>Finance</p>
<p>ER-rapport</p>
<p>Skrivermål</p>
</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from Finance to the DRA."></td>
<td>Dokumentrutingsagent</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from the DRA to a local printer."></td>
<td>Lokal skriver</td>
<td><img src="./media/er-design-zpl-labels-flow1.png" alt="Data flow direction: from a local printer to a printer emulator."></td>
<td>Skriveremulator</td>
<td><img src="./media/er-design-zpl-labels-flow2.png" alt="Data flow direction: from a printer emulator to a rendering web service and then back to the printer emulator."></td>
<td>Gjengivelse av nettjeneste</td>
</td>
</tr>
</tbody>
</table>

### <a name="install-and-configure-a-printer-emulator-application"></a>Installere og konfigurere et skriveremulatorprogram

Legg til et skriveremulatorprogram for ZPL-gjengivelsesmotoren i nettleseren Chrome. I dette eksemplet brukes emulatoren [Zpl Printer](https://chrome.google.com/webstore/detail/zpl-printer/phoidlklenidapnijkabnfdgmadlcmjo) som er basert på [ZPL Web Service fra Labelary](http://labelary.com/service.html). Skriveremulatorprogrammet sender genererte etiketter i ZPL-format fra en lokal skriver til nettjenesten, og returnerer deretter etiketter som PDF- eller PNG-filer for forhåndsvisning.

1. Du kan finne og velge skriveremulatorprogrammet du vil bruke, i nettbutikken for Chrome. Velg deretter **Legg til i Chrome** for å legge det til i nettleseren Chrome.

    ![Tilføying av skriveremulatorprogrammet i nettleseren Chrome fra nettbutikken for Chrome.](./media/er-design-zpl-labels-add-app.png)

2. Velg **Start app** for å kjøre skriveremulatorprogrammet fra nettleseren Chrome.

    ![Kjøring av skriveremulatorprogrammet fra nettleseren Chrome.](./media/er-design-zpl-labels-run-app.png)

3. Konfigurere programmet som kjører:

    1. Deaktiver programmet.
    2. Angi **127.0.0.1** for verten i skriverinnstillingene.
    3. Angi **9100** for porten.

        ![Konfigurasjon av skriveremulatorprogrammet.](./media/er-design-zpl-labels-configure-app.png)

    4. Aktiver programmet på nytt. Du skal få en melding om at skriveren ble startet på verten og i porten som er angitt.

        ![Skriveremulatorprogrammet er aktivert på nytt.](./media/er-design-zpl-labels-turn-on-app.png)

> [!NOTE]
> Siden skriveremulatorprogrammet som brukes i dette eksemplet, er avhengig av en nettjeneste for å gjengi etiketter, må du sørge for at sikkerhetsinnstillingene lar deg kommunisere med tjenesten. Ellers kan ikke programmet motta de gjengitte etikettene, og ingen forhåndsvisning av disse etikettene blir tilgjengelig.

### <a name="add-and-configure-a-local-printer"></a>Legge til og konfigurere en lokal skriver

[Legg til en ny lokal skriver](https://support.microsoft.com/windows/install-a-printer-in-windows-10-cc0724cf-793e-3542-d1ff-727e4978638b) som gjeldende enhet kan bruke til å sende genererte etiketter fra dokumentrutingsagenten til skriveremulatorprogrammet.

1. Velg **Start** \> **Innstillinger** \> **Enheter** \> **Skrivere \& skannere** i Windows.
2. Velg **Innstillinger for skrivere \& skannere**.
3. Velg **Legg til enhet** for **Legg til en skriver eller skanner**.
4. Velg **Legg til manuelt** for **Skriveren jeg vil ha, er ikke i listen**.
5. Velg **Legg til en lokal skriver eller nettverksskriver med manuelle innstillinger** i feltet **Søk etter en skriver på andre måter**.
6. I feltet **Velg en skriverport** velger du **Opprett en ny port**, og følg deretter denne fremgangsmåten:

    1. Velg **Standard TCP/IP-port** i **Porttype**-feltet.
    2. Angi **127.0.0.1** i feltet **Vertsnavn eller IP-adresse**.
    3. Angi **ZPL** i **Portnavn**-feltet.
    4. Vent til operasjonen **Oppdager TCP/IP-port** er fullført.
    5. Velg **Egendefinert** i **Enhetstype**-feltet, og velg deretter **Innstillinger**.
    6. Kontroller at følgende portinnstillinger er angitt:

        - **Portnavn:** ZPL
        - **Skrivernavn eller IP-adresse:** 127.0.0.1
        - **Protokoll:** Rå
        - **Portnummer:** 9100

7. Velg **Generisk / Bare tekst** i feltet **Installer skriverdriver**.
8. I feltet **Skrivernavn** angir du **ZebraPrinter**.

![Tilføying av en lokal skriver for gjeldende enhet.](./media/er-design-zpl-labels-configure-printer.png)

### <a name="install-and-configure-the-dra"></a>Installere og konfigurere dokumentrutingsagenten

Klargjør dokumentrutingsagenten slik at den kan sende genererte etiketter fra Finance til den konfigurerte lokale skriveren.

1. [Installer dokumentrutingsagenten](install-document-routing-agent.md#install-the-document-routing-agent).
2. [Konfigurer dokumentrutingsagenten](install-document-routing-agent.md#configure-the-document-routing-agent).
3. [Registrer den lokale skriveren](install-document-routing-agent.md#register-network-printers) i dokumentrutingsagenten.
4. [Aktiver den lokale skriveren](install-document-routing-agent.md#administer-network-printers) i Finance-miljøet.

![Klargjøring av dokumentrutingsagenten slik at den skriver ut genererte etiketter.](./media/er-design-zpl-labels-configure-dra.png)

### <a name="configure-the-er-destination"></a>Konfigurere ER-målet

Klargjør ER-målet slik at det kan sende genererte etiketter fra Finance til dokumentrutingsagenten.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Mål for elektronisk rapportering**.
2. På siden **Mål for elektronisk rapportering** velger du **Ny** i handlingsruten.
3. Velg **Lagerlokasjonsetiketter** i **Referanse**-feltet.
4. På **Filmål**-hurtigfanen velger du **Ny**.
5. Angi **Etiketter** i **Navn**-feltet.
6. I feltet **Navn på filkomponent** velger du **Rapport**.
7. Velg **Innstillinger**.
8. I **Skriver**-fanen i dialogboksen **Innstillinger for mål** setter du alternativet **Aktivert** til **Ja**.
9. I feltet **Skrivernavn** velger du **ZebraPrinter**.
10. Velg **ZPL** i feltet **Dokumentrutingstype**.
11. Velg **OK**.

![Konfigurasjon av ER-målet for formatet Lagerlokasjonsetiketter på målsiden for elektronisk rapportering.](./media/er-design-zpl-labels-configure-destination.png)

## <a name="review-warehouse-locations"></a>Se gjennom lagerlokasjoner

1. Gå til **Lagerstyring** \> **Oppsett** \> **Lager** \> **Lokasjoner**.
2. Filtrer på **Lokasjoner**-siden for å vise bare lokasjoner som har en verdi i feltet **Kontrollsifre**.

![Se gjennom lagerlokasjoner på Lokasjoner-siden.](./media/er-design-zpl-labels-review-locations.png)

## <a name="print-warehouse-location-labels"></a>Skrive ut lagerlokasjonsetiketter

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. I konfigurasjonstreet på siden **Konfigurasjoner** utvider du **Lagermodell** og velger **Lagerlokasjonsetiketter**.
3. Velg **Kjør** i handlingsruten.
4. I fanen **Poster som skal inkluderes** i dialogboksen **Parametere for elektronisk rapport** velger du **Filter**.
5. Finn raden der **Tabell**-feltet i **Område**-fanen er satt til **Lokasjoner** og **Felt**-feltet er satt til **Lokasjon**. Angi **LPEnabled** i **Kriterier**-feltet.
6. Velg **OK**.
7. Velg **OK**. En etikett genereres og vises på forhåndsvisningssiden i skriveremulatorprogrammet.

![Se gjennom en generert etikett på forhåndsvisningssiden i emulatorprogrammet Zpl Printer.](./media/er-design-zpl-labels-preview-label.png)

## <a name="modify-the-layout-of-a-label"></a>Endre oppsettet for en etikett

Du kan endre det gjeldende oppsettet for lagerlokasjonsetikettene. Eksemplet nedenfor viser hvordan du endrer oppsettet slik at genererte etiketter inneholder en lokasjonsprofil-ID.

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. Angi **Ja** for [ER-brukerparameteren](electronic-reporting-destinations.md#applicability) **Bruk mål for utkaststatus**.
3. I konfigurasjonstreet på siden **Konfigurasjoner** utvider du **Lagermodell** og velger **Lagerlokasjonsetiketter**.
4. Velg **Utforming**.
5. Velg datakilden `model.Location.Label` i **Tilordning**-fanen på siden **Formatutforming**.
6. Velg **Rediger** \> **Rediger formel** i dialogboksen **Datakildeegenskaper**.
7. Gå gjennom ER-formelen som brukes til å generere etiketter, i **Formel**-feltet på siden **Formelutforming**.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^XZ")
    ```

8. Oppdater formelen for å legge til en lokasjonsprofil-ID på genererte etiketter.

    ```vb
    CONCATENATE(
    "^XA",CrLf,
    "^CF0,30,30^FO0,30^FB800,1,0,C,0^FD",Warehouse,"\&^FS",CrLf,
    "^BY2,2,50^FT",@.Warehouse.Alignment,",126^BCN,,N,N,N,A^FD",Warehouse,"\&^FS",CrLf,
    "^FO0,150^FB800,1,0,C,0^FD",@.Name,"\&^FS",CrLf,
    "^CF0,20,20^FO0,200^FB800,1,0,C,0^FD",@.CheckDigits,"\&^FS",CrLf,
    "^CF0,40,40^FO0,240^FB800,1,0,C,0^FD",@.ProfileID,"\&^FS",CrLf,
    "^XZ")
    ```

9. Velg **Lagre**.
10. Velg **OK**.
11. Velg **Kjør** i handlingsruten.
12. I fanen **Poster som skal inkluderes** i dialogboksen **Parametere for elektronisk rapport** velger du **Filter**.
13. Finn raden der **Tabell**-feltet i **Område**-fanen er satt til **Lokasjoner** og **Felt**-feltet er satt til **Lokasjon**. I **Kriterier**-feltet angir du **Rampe**.
14. Velg **OK**.
15. Velg **OK**. En etikett genereres og vises på forhåndsvisningssiden i skriveremulatorprogrammet.

![Ser gjennom en generert etikett som inneholder en lokasjonsprofil-ID, på forhåndsvisningssiden i emulatorprogrammet Zpl Printer.](./media/er-design-zpl-labels-preview-label2.png)

## <a name="encoding"></a>Koding

> [!NOTE]
> Du må synkronisere kodingsinnstillingen for komponenten **Common\\File** i det redigerbare ER-formatet og den riktige innstillingen for den utformede etiketten. Verdien i **[Koding](er-suppress-bom-characters.md)**-feltet for komponenten **Common\\File** skal ikke motsi en ZPL-kommando som brukes til å styre etikettens koding (for eksempel kommandoen `^CI`). ER validerer ikke at disse innstillingene er synkronisert.

## <a name="additional-resources"></a>Tilleggsressurser

[Skrivermål](er-destination-type-print.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
