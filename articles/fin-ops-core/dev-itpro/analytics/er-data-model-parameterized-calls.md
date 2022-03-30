---
title: Støtte for parameteriserte kall av ER-datamodeller
description: Dette emnet beskriver hvordan du implementerer parameteriserte kall av datamodeller for elektronisk rapportering (ER).
author: NickSelin
ms.date: 03/14/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERModelMappingDesigner, EROperationDesigner, ERExpressionDesignerFormula, ERDataModelDesigner
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2020-10-01
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 968b0769607e9fdbed57c25b727ed44988a92913
ms.sourcegitcommit: 399d0d3f8e2ebb81b6b9d640365ebe182690bab2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/15/2022
ms.locfileid: "8419473"
---
# <a name="support-parameterized-calls-of-er-data-models"></a>Støtte for parameteriserte kall av ER-datamodeller

[!include [banner](../includes/banner.md)]

Hvis du vil generere forretningsdokumenter, konfigurerer du en [ER-løsning (elektronisk rapportering)](general-electronic-reporting.md) som inneholder følgende ER-komponenter:

- **[Format](er-overview-components.md#format-component)** – Denne komponenten angir strukturen til et forretningsdokument.
- **Formattilordning** – Denne komponenten styrer hvordan et forretningsdokument fylles ut ved kjøretid.
- **[Modelltilordning](er-overview-components.md#model-mapping-component)** – Denne komponenten angir hva dataene henter fra appen til en formattilordning.
- **[Datamodell](er-overview-components.md#data-model-component)** – Denne komponenten sender informasjon mellom individuelle komponenter.

Når du kjører et ER-format, kjøres hvert formatelement fra rotformatelementet. Hver gang et formatelement som kjøres, inneholder en binding til en [datakilde](general-electronic-reporting.md#configuring-data-model-mappings-for-outgoing-documents), kjøres datakilden for å levere de forventede dataene og bruker dem til å fylle ut formatelementet. Når en datakilde av *Modell*-typen kalles opp, kalles den egnede modelltilordningen for å trekke data ut av appen, basert på innstillingene for modelltilordning.

Tidligere kunne ikke disse modelltilordningskallene parameteriseres for å gjøre dem avhengige av logikken i formatet som kjøres. Bare følgende dataflyt ble støttet.

<table>
<tbody>
<tr align="center">
<td>
<b>Format</b><br>
Format&nbsp;element<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;forespørsel&nbsp;&gt;<br>
&lt;&nbsp;verdi&nbsp;&lt;
</td>
<td><b>Format&nbsp;tilordning</b><br>
Datakilde<br>
&nbsp;
</td>
<td>
<i>Data&nbsp;modell</i><br>
&gt;&nbsp;forespørsel&nbsp;&gt;<br>
&lt;&nbsp;verdi&nbsp;&lt;
</td>
<td>
<b>Modell&nbsp;tilordning</b><br>
Data&nbsp;kilde<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;forespørsel&nbsp;&gt;<br>
&lt;&nbsp;verdi&nbsp;&lt;
</td>
<td>
<b>Tabell</b><br>
Ta opp<br>
Felt
</td>
</tr>
</tbody>
</table>

I versjon 10.0.15 og senere kan du imidlertid konfigurere datamodellfelter som bare kan kalles når verdiene til de konfigurerte parameterne er angitt. Når et slikt felt konfigureres og kalles fra en formatkomponent, må de obligatoriske parameterne angis i et format som er bindende som argumenter for samtalen. I slike tilfeller kan verdiene til argumenterene angis basert på formatspesifikke verdier. Derfor kan du bruke **dynamisk parametrisering av kjøretid** for datamodellkall for å støtte følgende dataflyt.

<table>
<tbody>
<tr align="center">
<td>
<b>Format</b><br>
Format&nbsp;element&nbsp;1<br>
<br>
Format&nbsp;element&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;forespørsel&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;verdi&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;forespørsel&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;verdi&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Format&nbsp;tilordning</b><br>
Data&nbsp;kilde&nbsp;1<br>
&nbsp;<br>
<b>value2=Func(value1)</b><br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Data&nbsp;modell</i><br>
&gt;&nbsp;felt1&nbsp;&gt;<br>
&lt;&nbsp;verdi&nbsp;1&nbsp;&lt;<br>
<b>&gt;&nbsp;field2(value2)&nbsp;&gt;</b><br>
&lt;&nbsp;verdi&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Modell&nbsp;tilordning</b><br>
Data&nbsp;kilde&nbsp;1<br>
<br>
Data&nbsp;kilde&nbsp;2<br>
&nbsp;<br>
&nbsp;
</td>
<td>
<i>Binding</i><br>
&gt;&nbsp;forespørsel&nbsp;1&nbsp;&gt;<br>
&lt;&nbsp;verdi&nbsp;1&nbsp;&lt;<br>
&gt;&nbsp;forespørsel&nbsp;2&nbsp;&gt;<br>
&lt;&nbsp;verdi&nbsp;3&nbsp;&lt;<br>
&nbsp;
</td>
<td>
<b>Tabell&nbsp;1</b><br>
Oppføring&nbsp;1<br>
Felt&nbsp;1<br>
<b>Tabell&nbsp;2</b><br>
Oppføring&nbsp;2<br>
Felt&nbsp;2
</td>
</tr>
</tbody>
</table>

Ved hjelp av den nye funksjonen kan du parametrisere kallet til et hvilket som helst datamodellfelt av typen [*Oppføring*](er-formula-supported-data-types-composite.md#record) eller [*Oppføringsliste*](er-formula-supported-data-types-composite.md#record-list). Følgende datatyper støttes for parameterne i et datamodellfelt:

- [Boolsk](er-formula-supported-data-types-primitive.md#boolean)
- [Beholder](er-formula-supported-data-types-composite.md#container)
- [Dato](er-formula-supported-data-types-primitive.md#date)
- [dato/klokkeslett](er-formula-supported-data-types-primitive.md#datetime)
- [GUID](er-formula-supported-data-types-primitive.md#guid)
- [Int64](er-formula-supported-data-types-primitive.md#int64)
- [Heltall](er-formula-supported-data-types-primitive.md#integer)
- [Kommatall](er-formula-supported-data-types-primitive.md#real)
- [Streng](er-formula-supported-data-types-primitive.md#string)

Du kan angi hver parameter for et datamodellfelt der argumentet kan angis som en enkeltverdi av den definerte datatypen og [*listen*](er-formula-supported-data-types-composite.md#record-list) over slike verdier.

> [!NOTE]
> Standardverdien for parameteren til et datamodellfelt støttes ikke. Hvis du legger til en parameter i et felt i en datamodell, og versjonen av denne datamodellen allerede er frigitt og publisert, må du [rebasere](general-electronic-reporting.md#upgrading-a-format-selecting-a-new-version-of-base-format-rebase) alle tilsvarende modelltilordninger og -formater til den nye versjonen av denne modellen, fordi denne datamodellen ikke er bakoverkompatibel.

Du kan konfigurere parametriserte datamodellfelter for å gjøre modelltilordningskall formatspesifikke. Denne fremgangsmåten kan hjelpe deg med å redusere antall modelltilordninger som må konfigureres for mange formater for en enkelt datamodell. Du kan også bruke denne fremgangsmåten til å forbedre kjøringsytelsen for formatene og redusere tiden det tar å generere forretningsdokumenter. Hvis du vil vite mer om denne funksjonen, kan du fullføre eksemplet i dette emnet.

## <a name="example-use-parameterized-calls-of-er-data-models"></a>Eksempel: Bruk parameteriserte kall av ER-datamodeller

Trinnene nedenfor forklarer hvordan en bruker i rollen som systemadministrator eller utvikler av elektronisk rapportering kan utforme en ER-løsning som inneholder en datamodell, en modelltilordning og en format-ER-komponent som er konfigurert til å kalle en modelltilordning fra et format ved å angi et argument for kallet, og verdien av dette er beregnet ved kjøretid ved å bruke formelen for det kjørende formatet. 

Denne fremgangsmåten kan gjennomføres i firmaet **DEMF**. Ingen kodeendringer er nødvendig. 

I dette eksemplet skal du opprette de nødvendige ER-[konfigurasjonene](general-electronic-reporting.md#Configuration) for eksempelfirmaet **Litware, Inc**. Kontroller at konfigurasjonsleverandøren for eksempelfirmaet **Litware, Inc.** (`http://www.litware.com`) er oppført for ER-rammeverket og at det er merket som **Aktiv**. Hvis denne konfigurasjonsleverandøren ikke er oppført, eller hvis den ikke er merket som **Aktiv**, følger du trinnene i emnet [Opprette en konfigurasjonsleverandør og merke den som aktiv](tasks/er-configuration-provider-mark-it-active-2016-11.md).

### <a name="business-scenario"></a>Forretningsscenario

Du har en ER-løsning som inneholder et format du kan kjøre for å generere et elektronisk dokument til revisjonsformål. Dette formatet inneholder avgiftstransaksjoner som er knyttet til salgsordrer og bestillinger, og som har de nødvendige detaljene, for eksempel transaksjonsdato og avgiftsverdi. Strukturen i dette dokumentet er endret per det nye regnskapsåret. Du må nå sende inn et utvidet dokument som inneholder flere detaljer (navn) for alle parter (kunder og leverandører) som har transaksjoner presentert i genererte rapporter. Derfor må du endre ER-løsningen slik at den genererer dokumenter som samsvarer med dette nye kravet.

### <a name="configure-the-er-framework"></a>Konfigurere ER-rammeverket

Følg trinnene i [Konfigurere ER-rammeverket](er-quick-start2-customize-report.md#ConfigureFramework) for å konfigurere minimumssettet med ER-parametere. Du må fullføre denne konfigurasjonen før du begynner å bruke ER-rammeverket til å utforme en ny ER-løsning.

### <a name="design-a-domain-specific-data-model"></a>Utforme en domenespesifikk datamodell

Du må opprette en ny ER-konfigurasjon som inneholder den påkrevde datamodellkomponenten. Denne datamodellen vil senere bli brukt som datakilde når du utformer et ER-format for å generere en revisjonsrapport.

Følg denne fremgangsmåten for å importere den nødvendige datamodellen fra en XML-fil fra Microsoft.

1. Last ned filen [Sample audit model.version.1.xml](https://download.microsoft.com/download/7/1/9/719b0132-fed7-4c73-8afa-90cac29c2fee/Sample-audit-model.version.1.xml), og lagre den på den lokale datamaskinen.
2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.
4. På siden **Konfigurasjoner** velger du **Exchange** \> **Last fra XML-fil** i handlingsruten.
5. Velg **Bla gjennom**, og finn og velg filen **Sample audit model.version.1.xml**.
6. Velg **OK** for å importere konfigurasjonen.

    ![Importert ER-datamodellkonfigurasjon på konfigurasjonssiden.](./media/er-data-model-parameterized-calls-imported-model.png)

Følgende illustrasjon viser den redigerbare versjonen av den konfigurerte datamodellen på siden **Datamodellutforming**.

![Strukturen til ER-datamodellen på siden Datamodellutforming.](./media/er-data-model-parameterized-calls-model1.png)

For øyeblikket er modellen utformet for å vise bare avgiftstransaksjoner som har de nødvendige detaljene.

### <a name="design-a-model-mapping-for-the-configured-data-model"></a>Utforme en modelltilordning for den konfigurerte datamodellen

Som en bruker med rollen som utvikler av elektronisk rapportering må du opprette en ny ER-konfigurasjon som inneholder en tilordningskomponent for datamodellen for eksempelrevisjon. Denne komponenten implementerer den konfigurerte datamodellen for Microsoft Dynamics 365 Finance og gjelder spesifikt for denne appen. Du må konfigurere komponenten for modelltilordning for å angi appobjektene som må brukes til å fylle ut den konfigurerte datamodellen med appdata ved kjøring. For å kunne fullføre denne oppgaven må du forstå hvordan datastrukturen i bedriftsdomenet for avgift er implementert i Finance.

Følg denne fremgangsmåten for å importere den nødvendige modelltilordningen fra en XML-fil fra Microsoft.

1. Last ned filen [Sample audit mapping.version.1.1.xml](https://download.microsoft.com/download/c/0/3/c03a4673-b1b1-4ef8-96d0-bf96518be6e0/Sample-audit-model-mapping.version.1.1.xml), og lagre den på den lokale datamaskinen.
2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.
4. På siden **Konfigurasjoner** velger du **Exchange** \> **Last fra XML-fil** i handlingsruten.
5. Velg **Bla gjennom**, og finn og velg filen **Sample audit model mapping.version.1.1.xml**.
6. Velg **OK** for å importere konfigurasjonen.

    ![Importert ER-modelltilordningskonfigurasjon på konfigurasjonssiden.](./media/er-data-model-parameterized-calls-imported-mapping.png)

Den følgende illustrasjonen viser den redigerbare versjonen av den konfigurerte modelltilordningen på siden **Modelltilordningsutforming**.

![Strukturen til ER-modelltilordningen på siden Modelltilordningsutforming.](./media/er-data-model-parameterized-calls-mapping1.png)

For øyeblikket er modelltilordningen utformet for å vise avgiftstransaksjoner som har de nødvendige detaljene. Den henter denne informasjonen `TaxTrans`-apptabellen hjelp av den konfigurerte `TaxTrans`-datakilden og `TaxTransFiltered` ER-datakildene.

### <a name="design-a-new-format"></a>Utforming av et nytt format

Som en bruker med rollen som funksjonsrådgiver for elektronisk rapportering må du opprette en ny ER-konfigurasjon som inneholder en komponent av typen format. Du må konfigurere formatkomponenten for å fylle ut genererte rapporter med avgiftstransaksjoner som har alle de nødvendige detaljene.

Følg denne fremgangsmåten for å importere det nødvendige formatet fra en XML-fil fra Microsoft.

1. Last ned filen [Sample audit format.version.1.1.xml](https://download.microsoft.com/download/e/b/7/eb7e126e-2bb3-4bbb-a735-ffd4c48920b1/Sample-audit-format.version.1.1.xml), og lagre den på den lokale datamaskinen.
2. Gå til **Organisasjonsstyring** \> **Arbeidsområder** \> **Elektronisk rapportering**.
3. I arbeidsområdet **Elektronisk rapportering** velger du **Rapporteringskonfigurasjoner**.
4. På siden **Konfigurasjoner** velger du **Exchange** \> **Last fra XML-fil** i handlingsruten.
5. Velg **Bla gjennom**, og finn og velg filen **Sample audit format.version.1.1.xml**.
6. Velg **OK** for å importere konfigurasjonen.

    ![Importert ER-formatkonfigurasjon på konfigurasjonssiden.](./media/er-data-model-parameterized-calls-imported-format.png)

Den følgende illustrasjonen viser den redigerbare versjonen av det konfigurerte formatet på siden **Formatutforming**.

![Strukturen til ER-formatet på siden Formatutforming.](./media/er-data-model-parameterized-calls-format1.png)

ER-formatet er konfigurert til å generere en rapport som en tekstfil i kommaseparerte verdier (CSV-format).

### <a name="run-the-imported-format"></a>Kjør det importerte formatet

1. På **Konfigurasjoner**-siden velger du konfigurasjonen **Eksempelrevisjonsformat**, og deretter velger du **Kjør** i handlingsruten.
2. I fanen **Poster som skal inkluderes** i dialogboksen **Parametere for elektronisk rapport** velger du **Filter**.
3. Angi betingelsene for å velge avgiftstransaksjonene for bilagene **PIV-110000004** og **INV-10000001**.
4. Velg **OK**.
5. Velg **OK**.
6. Gå gjennom det genererte dokumentet som inneholder avgiftstransaksjoner for de valgte bilagene.

    ![Forhåndsvisning av det genererte dokumentet med avgiftstransaksjoner.](./media/er-data-model-parameterized-calls-output1.png)

### <a name="adjust-the-imported-er-solution"></a>Juster den importerte ER-løsningen

I henhold til det nye kravet må dokumentet du må sender, inneholde navnene til kunder og leverandører som har transaksjoner som er inkludert. Derfor må du endre den importerte ER-løsningen slik at den genererer et dokument som overholder dette nye kravet.

Bestem hvordan du vil implementere de nødvendige endringene av de importerte ER-komponentene.

Den opplagte tilnærmingen er å implementere følgende endringer:

- I datamodellen legger du til det nye `Transaction.Party.Name`-datamodellfeltet for *Streng*-typen.
- Konfigurer bindingen for det nye datamodellfeltet i modelltilordningen ved å bruke tilgjengelige tabellrelasjoner til å få tilgang til den relevante posten i `DirPartyTable`-apptabellen, og hent verdien til `Name`-feltet fra den.

Selv om denne fremgangsmåten vil fungere, kan den forårsake ytelsesproblemer i SQL-databasen fordi `TaxTrans` er transaksjonstabellen og kan derfor inneholde et stort antall poster. I dette tilfellet må antall kall til `DirPartyTable` være likt antall poster i `TaxTrans`-tabellen som kan forårsake ytelsesproblemer.

Du kan også implementere følgende endringer:

- I datamodellen legger du til den nye `Party`-roten og det nye `Party.Name`-feltet.
- I modelltilordningen legger du til en ny datakilde som skal slå sammen alle postene med tabeller som brukes i tabellrelasjoner for å få tilgang til den relevante posten i `DirPartyTable`-apptabellen, med start fra `TaxTrans`-tabellen.

Selv om denne fremgangsmåten vil fungere, kan den forårsake noen problemer med minneforbruk. Selv når en ny [JOIN](er-join-data-sources.md)-datakilde kjøres som én enkelt SQL-forespørsel til appdatabasen for å unngå problemer med databaseytelsen, må resultatet hentes til minnet på appserveren. Fordi antall poster og antall felt i disse postene vil være ganske stort, kan denne fremgangsmåten forårsake svært tungt minneforbruk. Et kjøretidsunntak for tomt minne kan til og med kastes.

Du kan implementere endringene når et format som kjøres, samler inn de unike identifikasjonskodene til kunder og leverandører for alle mva-transaksjoner som vil bli presentert på en generert rapport. Fordi bare unike koder skal beholdes, er ikke det endelige kodesettet stort nok til å påvirke minneforbruket. Kodesettet vil deretter sendes til modelltilordningen som argumentet for et annet kall fra datakilden av *Modell*-typen. Basert på dette kallet vil modelltilordningen kjøre en ny ER-datakilde som lager en enkelt SQL-forespørsel til appdatabasen for å hente poster fra `DirPartyTable`-tabellen, bare for partene som har koder som presenteres i det angitte kodesettet.

### <a name="adjust-the-imported-data-model"></a>Juster den importerte datamodellen

1. Gå til **Organisasjonsstyring** \> **Elektronisk rapportering** \> **Konfigurasjoner**.
2. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, velger du **Eksempelrevisjonsmodell**.
3. På hurtigfanen **Versjoner** velger du versjon **2** med statusen **[Utkast](general-electronic-reporting.md#component-versioning)**.
4. Velg hurtigfanen **Konfigurasjonskomponenter**.
5. Velg **Utforming** for å åpne datamodellen for redigering.
6. På **Datamodell**-siden kontrollerer du at feltet `Root` er valgt, og deretter velger du **Ny**.
7. Følg disse trinnene i rullegardinboksen:

    1. I feltgruppen **Ny node som** velger du **Underordnet for en aktiv node**.
    2. Angi **Part** i **Navn**-feltet.
    3. Velg **Postliste** i **Varetype**-feltet.
    4. Velg **Legg til** for å fullføre tilføyelsen av det nye feltet.

8. Kontroller at `Root.Party`-feltet er valgt, gå til **Node**-fanen og velg **Parametere**.
9. Følg disse trinnene i dialogboksen **Parametere**:

    1. Velg **Ny** på fanen **Parametere**.
    2. Angi **PartyRefRecId** i **Navn**-feltet.
    3. Velg **Int64** i **Type**-feltet.
    4. Merk av for **Liste**.
    5. Velg **OK** for å fullføre angivelsen av parameterne.

    > [!NOTE]
    > Du har nettopp konfigurert `Root.Party`-datamodellfeltet som et felt som kalles når det angis en verdi i parameteren **PartyRefRecId**. Denne verdien må finnes i listen over poster som inneholder et `Value`-felt av datatypen *Int64*.

    ![Dialogboksen Parametere.](./media/er-data-model-parameterized-calls-model2a.png)

10. Kontroller at `Root.Party`-feltet fremdeles er valgt, og velg deretter **Ny**.
11. Følg disse trinnene i rullegardinboksen:

    1. I feltgruppen **Ny node som** velger du **Underordnet for en aktiv node**.
    2. Angi **Navn** i **Navn**-feltet.
    3. Velg **Streng** i **Varetype**-feltet.
    4. Velg **Legg til** for å fullføre tilføyelsen av det nye feltet.

12. Velg **Lagre**, og lukk siden **Datamodell**.

    ![Strukturen til den justerte ER-datamodellen på siden Datamodellutforming.](./media/er-data-model-parameterized-calls-model2b.png)

13. På hurtigfanen **Versjoner** for versjon **2** velger du **Endre status** \> **Fullført**. Velg deretter **OK**.

    > [!NOTE]
    > Endringene i datamodeller lagres i den andre revisjonen av **Eksempelrevisjonsmodell**-datamodellkomponenten som finnes i den andre versjonen av ER-konfigurasjonen **Eksempelrevisjonsmodell**.

![Oppdatert ER-datamodellkonfigurasjon på konfigurasjonssiden.](./media/er-data-model-parameterized-calls-updated-model.png)

### <a name="adjust-the-imported-model-mapping"></a>Juster den importerte modelltilordningen

1. På **Konfigurasjoner**-siden, i konfigurasjonstreet i venstre rute, utvider du **Eksempelrevisjonsmodell**.
2. Velg tilordningen **Eksempelrevisjonsmodell**, og på hurtigfanen **Versjoner** velger du deretter den andre tilordningsversjonen som er basert på den første datamodellversjonen (versjon **1.2**), og som har statusen **Utkast**.
3. Velg **Rebaser**.
4. I feltet **Målversjon** lar du versjon **2** av basismodellen **Eksempelrevisjonsmodell** stå.
5. Velg **OK** for å rebasere og samkjøre modelltilordningen med nylige datamodellendringer.

    Legg merke til at versjonsnummeret til den redigerbare modelltilordningen er endret fra **1.2** til **2.2** for å angi at den andre modellversjonen for øyeblikket brukes som grunnlag.

6. Velg **Utforming**.
7. På siden **Tilordning av modell til datakilde** velger du **Utforming** for den gjeldende modelltilordningen.
8. Følg denne fremgangsmåten for å legge til en ny datakilde for å få tilgang til `DirPartyTable`-apptabellen:

    1. I ruten **Datakildetype** velger du **Dynamics 365 for Operations \> Tabellposter**.
    2. I **Datakilder**-ruten velger du **Legg til rot**.
    3. Angi **PartyTable** i **Navn**-feltet.
    4. I **Tabell**-feltet angir du **DirPartyTable**.
    5. Velg **OK** for å fullføre tilføyelsen av den nye datakilden.

9. Følg denne fremgangsmåten for å legge til en ny datakilde for å be om `DirPartyTable`-poster, basert på listen over postidentifikasjonskoder som er angitt:

    1. I ruten **Datakildetype** velger du **Generelt \> Tom beholder**.
    2. I **Datakilder**-ruten velger du **Legg til rot**.
    3. Angi **Data** i **Navn**-feltet.
    4. Velg **OK** for å fullføre tilføyelsen av den nye datakilden.
    5. I **Datakilder**-ruten velger du **Data**-datakilden.
    6. I ruten **Datakildetype** velger du **Funksjoner \> Beregnet felt**.
    7. I ruten **Datakilder** velger du **Legg til**.
    8. Angi **DirParty** i **Navn**-feltet.
    9. Velg **Rediger formel**.
    10. På siden **Formeldesigner** velger du **Parametere**.
    11. Følg disse trinnene i dialogboksen **Parametere**:

        1. Velg **Ny** på fanen **Parametere**.
        2. Angi **DirPartyId** i **Navn**-feltet.
        3. Velg **Int64** i **Type**-feltet.
        4. Merk av for **Liste**.
        5. Velg **OK**.

        > [!NOTE]
        > Du har nettopp konfigurert dette beregnede feltet, slik at det ved kjøretid vil godta argumentet for en enkelt parameter som er konfigurert som en postliste som har ett enkelt `Value`-felt av typen *Int64*.

    12. I **Formel**-feltet angir du følgende uttrykk:

        `FILTER(PartyTable, VALUEINLARGE(PartyTable.RecId, DirPartyId, DirPartyId.Value))`

        > [!NOTE]
        > Du har nettopp konfigurert det beregnede `DirParty`-feltet til å hente kun `DirPartyTable`-poster der postidentifikasjonskodene er inkludert i `DirPartyId`-listen som vises som et argument når `DirParty`-feltet kalles.

        ![Formel for å hente partsnavn fra apptabellen på Formeldesigner-siden.](./media/er-data-model-parameterized-calls-formula1.png)

    13. Velg **Lagre**, og lukk siden **Formeldesigner**.
    14. Velg **Lagre**, og velg deretter **OK** for å fullføre tilføyelsen av den nye datakilden.

10. Følg denne fremgangsmåten for å binde den nye datakilden til det nye datamodellfeltet, slik at datamodellen brukes til å vise partnavn:

    1. I **Datamodell**-ruten velger du `Root.Party`-datamodellfeltet.
    2. I **Datamodell**-ruten velger du **Rediger**.
    3. På siden **Formeldesigner** i feltet **Formel** angir du uttrykket `Data.DirParty(PartyRefRecId)`.
    4. Velg **Lagre**, og lukk siden **Formeldesigner**.

        > [!NOTE]
        > Du har nettopp konfigurert bindingen til å kalle den konfigurerte `Data.DirParty`-datakilden og angi listen over post-ID-koder som skal angis i formatet når `Root.Party`-datamodellfeltet kalles.

    5. I **Datamodell**-ruten velger du `Root.Party.Name`-datamodellfeltet.
    6. I **Datamodell**-ruten velger du **Rediger**.
    7. På siden **Formeldesigner** i **Datakilde**-ruten utvider du **Data \> DirParty** og velger **Navn**.
    8. Velg **Legg til datakilde**.
    9. Velg **Lagre**, og lukk siden **Formeldesigner**.

    ![Strukturen til den justerte ER-modelltilordningen på siden Modelltilordningsutforming.](./media/er-data-model-parameterized-calls-mapping2.png)

11. Velg **Lagre**, og lukk siden **Modelltilordningsutforming**.
12. Lukk siden **Tilordning av modell til datakilde**.
13. På hurtigfanen **Versjoner** for versjon **2.2** velger du **Endre status \> Fullført**. Velg deretter **OK**.

### <a name="adjust-the-imported-format"></a>Juster det importerte formatet

1. Velg **Eksempelrevisjonsformat** på siden **Konfigurasjoner**.
2. På hurtigfanen **Versjoner** velger du versjon **1.2** med statusen **Utkast**.
3. Velg **Rebaser**.
4. I feltet **Målversjon** lar du versjon **2** av basismodellen **Eksempelrevisjonsmodell** stå.
5. Velg **OK** for å rebasere og samkjøre formatet med de nylige datamodellendringene.
6. Velg **Utforming**.
7. På siden **Formatutforming** i formatstrukturtreet i venstre rute velger du **Utvid/Skjul**.
8. Følg denne fremgangsmåten for å legge til et nytt formatelement for å samle inn postidentifikasjonskoder til parter som har transaksjoner presentert i genererte rapporter.

    1. I formatstrukturtreet velger du sekvenselementet **Report.Row.Trans**.
    2. Velg **Legg til**.
    3. I dialogboksen **Legg til** velger du **Datakilde \> Element**.
    4. I dialogboksen **Komponentegenskaper** i feltet **Navn** angir du **ID**.
    5. I **Datatype**-feltet velger du **Int64**.
    6. Velg **OK**.

    > [!NOTE]
    > Et element av typen **Datakilde \> Element** kan bare brukes til å utføre interne beregninger og datatransformasjon i omfanget til formatet som kjøres. Hvis du legger til dette formatelementet, endrer du derfor ikke innholdet i et generert dokument.

9. Følg denne fremgangsmåten for å legge til nye formatelementer for å angi partsnavn i genererte rapporter:

    1. Velg sekvenselementet **Report.Row**.
    2. Velg **Legg til**.
    3. I dialogboksen **Legg til** velger du **Tekst \> Sekvens**.
    4. I dialogboksen **Komponentegenskaper** i feltet **Navn** angir du **Part**.
    5. Velg **OK**.
    6. Velg sekvenselementet **Report.Row.Party**.
    7. Velg **Legg til**.
    8. I dialogboksen **Legg til** velger du **Tekst \> Streng**.
    9. I dialogboksen **Komponentegenskaper** i feltet **Navn** angir du **Navn**.
    10. Velg **OK**.

10. Følg denne fremgangsmåten for å legge til en ny datakilde for å samle inn postidentifikasjonskoder til parter som har transaksjoner presentert i genererte rapporter.

    1. Velg **Legg til rot** på **Tilordning**-fanen.
    2. I dialogboksen **Legg til datakilde** velger du **Funksjoner \> Datainnsamling**.
    3. I dialogboksen **Datakildeegenskaper for datainnsamling** i feltet **Navn** angir du **PartyIds**.
    4. I **Varetype**-feltet velger du **Int64**.
    5. Velg **OK**.

11. Følg denne fremgangsmåten for å legge til en ny binding for å samle inn postidentifikasjonskoder til parter som har transaksjoner presentert i genererte rapporter.

    1. I formatstrukturtreet velger du datavareelementet **Report.Row.Trans.Id**.
    2. Velg **Rediger formel**.
    3. På siden **Formeldesigner** skriver du inn uttrykket `PartyIds.Collect(model.Transaction.Party.RecId)`.
    4. Velg **Lagre**, og lukk siden **Formeldesigner**.

12. Følg denne fremgangsmåten for å legge til nye bindinger for å angi partsnavn i genererte rapporter:

    1. I formatstrukturtreet velger du sekvenselementet **Report.Party**.
    2. Velg **Rediger formel**.
    3. På siden **Formeldesigner** skriver du inn uttrykket `model.Party(PartyIds.Result)`.
    4. Velg **Lagre**, og lukk siden **Formeldesigner**.
    5. I formatstrukturtreet velger du sekvenselementet **Report.Party.Name**.
    6. På **Tilordning**-fanen velger du datamodellfeltet `model.Party.Name`.
    7. Velg **Bind**.

    ![Strukturen til det justerte ER-formatet på siden Formatutforming.](./media/er-data-model-parameterized-calls-format2.png)

13. Velg **Lagre**, og lukk siden **Formatutforming**.
14. Lukk siden **Tilordning av modell til datakilde**.
15. På hurtigfanen **Versjoner** for versjon **2.2** velger du **Endre status** \> **Fullført**. Velg deretter **OK**.

### <a name="run-the-adjusted-format"></a>Kjør det justerte formatet

1. På **Konfigurasjoner**-siden velger du **Eksempelrevisjonsformat**, og deretter velger du **Kjør** i handlingsruten.
2. I fanen **Poster som skal inkluderes** i dialogboksen **Parametere for elektronisk rapport** velger du **Filter**.
3. Angi betingelsene for å velge avgiftstransaksjoner for bilagene **PIV-110000004** og **INV-10000001**.
4. Velg **OK**.
5. Velg **OK**.
6. Gå gjennom det genererte dokumentet som inneholder avgiftstransaksjoner for de valgte bilagene og navnene til den tilsvarende kunden og leverandøren.

    ![Forhåndsvisning av det genererte dokumentet med avgiftstransaksjoner og partsnavn.](./media/er-data-model-parameterized-calls-output2.png)

7. Gå til **Leverandør** \> **Leverandører** \> **Alle leverandører**, og gå gjennom detaljene i det valgte bilaget **PIV-110000004**, inkludert leverandørnavnet.

    ![Gå gjennom innkjøpsbilagsdetaljene på sidene Alle leverandører og Fakturajournal.](./media/er-data-model-parameterized-calls-review1.gif)

8. Gå til **Kunde** \> **Kunder** \> **Alle kunder**, og gå gjennom detaljene i det valgte bilaget **INV-10000001**, inkludert kundenavnet.

    ![Gå gjennom salgsbilagsdetaljene på sidene Alle kunder og Postert merverdiavgift.](./media/er-data-model-parameterized-calls-review2.gif)

Hvis du vil ha mer informasjon om denne kjøringen av ER-løsningen, kan du bruke den innebygde analysen for [ER-ytelsessporing](trace-execution-er-troubleshoot-perf.md).

## <a name="additional-resources"></a>Tilleggsressurser

- [Støtte for parameterkall fra ER-datakilder for Beregnet felt-typen](er-calculated-field-type.md)
- [Spore kjøringen av ER-formater for å feilsøke ytelsesproblemer](trace-execution-er-troubleshoot-perf.md)
- [Bruk datakilder for DATAINNSAMLING i formater for elektronisk rapportering](er-data-collection-data-sources.md)
- [ValueInLarge ER-funksjonen](er-functions-logical-valueinlarge.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
