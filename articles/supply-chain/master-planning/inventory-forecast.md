---
title: Lagerprognoser
description: Dette emnet beskriver funksjonaliteten for forsynings- og behovsprognose som kan brukes til å opprette lagerprognoser i Microsoft Dynamics 365 Supply Chain Management.
author: crytt
ms.date: 06/08/2021
ms.topic: article
ms.search.form: EcoResProductDetailsExtended, ForecastSales, ForecastPurch, ForecastInvent
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-08
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7901bcfc239885aa53863729e573d1f37ba67f81
ms.sourcegitcommit: f21659f1c23bc2cd65bbe7fb7210910d5a8e1cb9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/24/2021
ms.locfileid: "6306421"
---
# <a name="inventory-forecasts"></a>Lagerprognoser

[!include [banner](../includes/banner.md)]

Dette emnet beskriver hvordan du kan vise og opprette lagerprognoser. Du kan opprette og vise forsynings- og behovsprognoselinjer for varer, varegrupper, varefordelingsnøkler, kundekontoer, kundegrupper, leverandørkontoer og leverandørgrupper.

Du kan velge prognosemodellen som skal brukes, for hver prognoselinje. Du kan deretter angi varen eller varegruppen pluss antallet eller transaksjonsbeløpet. Du kan også konfigurere en tidsplan for fordeling av prognoseantallet.

Forsynings- og behovsprognoselinjene produserer en lagerprognose for den samme kombinasjonen av en vare og en modell. Denne lagerprognosen representerer en balanse mellom forsyningen og behovet som ble angitt for den samme varen. Den kan ikke redigeres. Lagerprognosen hjelper lagerstyringsteamet å gå gjennom forventede endringer i lagerbeholdningen for en vare i løpet av den kommende perioden som er prognoseberegnet.

Etter at du har angitt behovet og/eller forsyningen, kan du kjøre prognoseplanlegging for å beregne bruttobehov for materialer og kapasitet og generere planlagte bestillinger.

## <a name="view-and-manually-enter-forecast-lines"></a><a name="manual-entry"></a>Vise og angi prognoselinjer manuelt

Bruk denne fremgangsmåten til å opprette prognoselinjer manuelt for produkter.

Det finnes også andre måter å opprette prognoselinjer på:

- [Generere en statistisk basislinjeprognose](generate-statistical-baseline-forecast.md)
- [Importere historiske data for behovsprognoser](import-historical-data.md)
- [Generere prognosen ved å bruke en Microsoft Azure Machine Learning-nettjeneste](demand-forecasting-setup.md)
- [Importere behovs- eller forsyningsprognoselinjer ved hjelp av rammeverket for databehandling (dataenhetene ForecastDemandForecastEntryStaging og ForecastSupplyForecastEntryStaging)](../../dev-itpro/data-entities/data-entities-data-packages.md)

Som du kan se i tabellen i trinn 1, kan du få tilgang til sidene som brukes, på ulike måter.

1. Åpne en forsynings-, behovs- eller lagerprognoseside som beskrevet i tabellen nedenfor, avhengig av enhetstypen du vil opprette en prognose for, og prognosetypen du vil opprette.

    | Entity | Instruksjoner |
    |---|---|
    | Frigitte produkter | <ol><li>Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produkter**.</li><li>Velg produktet du vil opprette en prognose for.</li><li>Velg **Behovsprognose**, **Forsyningsprognose** eller **Lagerprognose** i **Prognose**-gruppen i **Plan**-fanen i handlingsruten, avhengig av hvilken type prognose du vil arbeide med.</li></ol> |
    | Frigitte produktvarianter | <ol><li>Gå til **Behandling av produktinformasjon \> Produkter \> Frigitte produktvarianter**.</li><li>Velg varianten du vil opprette en prognose for.</li><li>Velg **Behovsprognose**, **Forsyningsprognose** eller **Lagerprognose** i **Prognose**-gruppen i **Plan**-fanen i handlingsruten, avhengig av hvilken type prognose du vil arbeide med.</li></ol> |
    | Varegrupper | <ol><li>Gå til **Lagerstyring \> Oppsett \> Beholdning \> Varegrupper**.</li><li>Velg varegruppen du vil opprette en prognose for.</li><li>Velg **Prognose \> Behov**, **Prognose \> Forsyning** eller **Prognose \> Lagerprognose** i handlingsruten, avhengig av hvilken type prognose du vil arbeide med.</li></ol> |
    | Varefordelingsnøkler | <ol><li>Gå til **Lagerstyring \> Oppsett \> Prognose**.</li><li>Velg varefordelingsnøkkelen du vil opprette en prognose for.</li><li>Velg **Behovsprognose** i handlingsruten.</li></ol> |
    | Kunder | <ol><li>Gå til **Hovedplanlegging \> Prognose \> Manuell prognoseregistrering \> Kunder**.</li><li>Velg kunden du vil opprette en prognose for.</li><li>Velg **Definer behovsprognose** i handlingsruten.</li></ol> |
    | Kundegrupper | <ol><li>Gå til **Hovedplanlegging \> Prognose \> Manuell prognoseregistrering \> Kundegrupper**.</li><li>Velg kundegruppen du vil opprette en prognose for.</li><li>Velg **Definer behovsprognose** i handlingsruten.</li></ol> |
    | Leverandører | <ol><li>Gå til **Hovedplanlegging \> Prognose \> Manuell prognoseregistrering \> Leverandører**.</li><li>Velg leverandøren du vil opprette en prognose for.</li><li>Velg **Oppføring** for å åpne siden **Forsyningsprognose** i handlingsruten.</li></ol> |
    | Leverandørgrupper | <ol><li>Gå til **Hovedplanlegging \> Prognose \> Manuell prognoseregistrering \> Leverandørgrupper**.</li><li>Velg leverandørgruppen du vil opprette en prognose for.</li><li>Velg **Oppføring** for å åpne siden **Forsyningsprognose** i handlingsruten.</li></ol> | 
    | Alle linjer | <ul><li>Gå til **Hovedplanlegging \> Prognose \> Behovsprognoselinjer** eller **Hovedplanlegging \> Prognose \> Forsyningsprognoselinjer**, avhengig av hvilken type prognose du vil arbeide med.</li></ul> |

    Siden **Forsyningsprognose** eller **Behovsprognose** vises, avhengig av hva du valgte. Den viser eventuelle eksisterende prognoselinjer for posten du valgte før du åpnet siden.

1. Velg **Ny** i handlingsruten for å legge til en prognoselinje i rutenettet i øvre del av siden.
1. Velg prognosemodellen som skal brukes, i **Modell**-feltet på den nye linjen. Angi deretter andre detaljer etter behov, for eksempel vare, varegruppe, kunde- eller leverandørkonto eller kunde- eller leverandørgruppe, vareantall eller totalt transaksjonsbeløp. Hvis du vil ha fullstendige detaljer om feltene som er tilgjengelige på sidene **Forsyningsprognose** og **Behovsprognose**, kan du se de senere delene i dette emnet.
1. Hvis du vil distribuere prognosen over perioden, velger du **Fordel prognose** på verktøylinjen i **Oversikt**-fanen.
1. Gå gjennom tidshorisonten og tidsintervallene som brukes til fordeling av prognoseantallet, i rutenettet **Fordeling**.

## <a name="supply-forecast-lines"></a>Forsyningsprognoselinjer

Forsyningsprognosen lar deg opprette en plan for varer som må kjøpes. Den viser innkjøpsassistenter hva de forventes å bestille.

Du kan angi en forsyningsprognose etter vare, varegruppe, varefordelingsnøkkel, leverandør og leverandørgruppe. Hvis du vil ha informasjon om alle måtene du kan åpne **Forsyningsprognose**-siden for forskjellige enheter og poster på, kan du se delen [Vise og angi prognoselinjer manuelt](#manual-entry) tidligere i dette emnet.

Den øvre delen av siden **Forsyningsprognose** har et rutenett med forsyningsprognoselinjer og et sett med faner du kan bruke til å vise og angi mer informasjon om en valgt prognoselinje. Den nedre delen av siden inneholder rutenettet **Tildeling**.

De følgende underdelene beskriver alle feltene som er tilgjengelige i hver fane, og alle kommandoene som er tilgjengelige i handlingsruten på siden og på verktøylinjen i **Oversikt**-fanen.

### <a name="action-pane-commands-on-the-supply-forecast-page"></a>Kommandoer i handlingsruten på Forsyningsprognose-siden

Tabellen nedenfor beskriver kommandoene som er tilgjengelige i handlingsruten på **Forsyningsprognose**-siden.

| Kommando | beskrivelse |
|---|---|
| Lagre | Lagre de gjeldende innstillingene. |
| Rediger | Aktiver innstillingene på siden som skal redigeres. |
| Nye | Legg til en prognoselinje i det øvre rutenettet. |
| Delete | Fjern den valgte prognoselinjen fra det øvre rutenettet. |
| Prognosesaldoer | Vis prognosesaldoer som er beregnet for den valgte linjens modell-ID for det gjeldende regnskapsåret. Saldoene deles etter periode (måned). |
| Kontantstrømprognoser | Vis prognosetransaksjoner som er fordelt til økonomimodulen. Hvis du vil ha mer informasjon, kan du se [Kontantstrømprognose](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Lager \> Visningsdimensjoner | Velg lagerdimensjonene som skal vises i rutenettet i **Oversikt**-fanen. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-supply-forecast-page"></a>Verktøylinjekommandoer i Oversikt-fanen på Forsyningsprognose-siden

Tabellen nedenfor beskriver kommandoene som er tilgjengelige på verktøylinjen i **Oversikt**-fanen på **Forsyningsprognose**-siden.

| Kommando | beskrivelse |
|---|---|
| Fordel prognose | Hvis du bruker en tildelingsmetode, genererer du de individuelle tidsplanlinjene for prognosetransaksjonen. Linjeantallet distribueres deretter etter dato (i samsvar med de valgte tidsintervallene), antall og beløp for hele tidshorisonten. |
| Masseoppdatering | Åpne siden **Rediger prognosetransaksjoner**. (Se delen [Masseoppdatere prognosetransaksjoner](#bulk-update) senere i dette emnet.) |
| Lagerprognose | Åpne en visning av **Lagerprognose**-siden som er filtrert for den valgte vare-/modellkombinasjonen. (Se delen [Lagerprognose](#inventory-forecast) senere i dette emnet.) |
| Opprett varebehov | Åpne en dialogboks der du kan opprette varebehov og salgsordre- eller varejournallinjer for prosjektrelaterte prognosetransaksjoner. Selv om denne kommandoen er tilgjengelig for både forsynings- og behovsprognoselinjer, kan den ikke brukes på **Forsyningsprognose**-siden. |

### <a name="the-overview-tab-on-the-supply-forecast-page"></a>Oversikt-fanen på Forsyningsprognose-siden

Tabellen nedenfor beskriver feltene i **Oversikt**-fanen på **Forsyningsprognose**-siden.

| Felt | beskrivelse |
|---|---|
| **Modell** | Prognosemodellen som transaksjonen er knyttet til. |
| **Dato** | Startdatoen for transaksjonen. |
| **Leverandørnummer** | Leverandørkontoen som transaksjonen er knyttet til. |
| **Leverandørgruppe** | Leverandørgruppen som transaksjonen er knyttet til. |
| **Varenummer** | Identifikatoren for varen. |
| **Varegruppe** | Varegruppen som transaksjonen er knyttet til. |
| **Varefordelingsnøkkel** | varefordelingsnøkkelen som er tilknyttet prognosen. |
| **Faktisk vekt-antall** | Prognoseantallet i den angitte faktisk vekt-enheten. |
| **Faktisk vekt-enhet** | Faktisk vekt-enheten som varen kjøpes i. Verdien hentes automatisk fra vareoppsettet. |
| **Antall** | Prognoseantallet i den angitte innkjøpsenheten. |
| **Enhet** | Enheten som varen kjøpes i. Verdien hentes automatisk fra vareoppsettet. Du kan imidlertid endre den hvis enhetsomregninger er konfigurert. |
| **Beløp** | Bruttobeløpet, minus rabatter, som prognosetransaksjonen bidrar med i prognosen. |
| **Valuta.** | Valutaen som brukes for prognosetransaksjonen. Standardvalutaen angis automatisk, men du kan velge en annen valuta. |
| (Andre dimensjoner) | Ytterligere dimensjoner kan vises som kolonner i rutenettet. Hvis du vil velge de ytterligere dimensjonene som vises, velger du **Vis dimensjoner** i handlingsruten. |

### <a name="the-general-tab-on-the-supply-forecast-page"></a>Generelt-fanen på Forsyningsprognose-siden

**Generelt**-fanen viser mer informasjon om linjen som for øyeblikket er valgt i **Oversikt**-fanen. Deler av denne informasjonen gjentas fra **Oversikt**-fanen. I tabellen nedenfor beskrives feltene som er unike for **Generelt**-fanen.

| Felt | beskrivelse |
|---|---|
| Rapport | Sett dette alternativet til *Ja* hvis du vil ta med transaksjonen i rapporter. |
| Kommentarer | Angi eventuelle kommentarer om prognosetransaksjonen. |
| Aktivt | Merk av for dette hvis du vil ta med transaksjonen i budsjettrapporter. |
| Inkluder i kontantstrømprognoser | Merk av for dette alternativet hvis du vil fordele prognosetransaksjonen til økonomimodulen. Innstillingen for denne avmerkingsboksen kan ikke endres for rapporteringstransaksjoner. |
| Merverdiavgiftsgruppe | Avgiftsgruppen som brukes til å angi avgifter for prognosetransaksjonen. |
| Varens mva-gruppe | Vareavgiftsgruppen som brukes til å angi avgifter for prognosetransaksjonen. |
| Metode | <p>Velg metoden du vil bruke til å tildele prognosetransaksjonen:</p><ul><li>**Ingen** – Ingen tildeling finner sted.</li><li>**Periode** – Prognoseberegn det samme antallet for hver periode. Hvis du velger denne verdien, angir du et antall i **Per**-feltet og en tidsenhet i **Enhet**-feltet.</li><li>**Nøkkel** – Tildel prognosen i samsvar med periodetildelingsnøkkelen du angir i **Periodenøkkel**-feltet. Du kan bruke denne metoden når du vil ta hensyn til sesongvariasjoner.</li></ol>|
| Per | <p>Angi hvor mange fremtidige tidsintervaller prognosen skal gjelde for. Dette feltet er bare tilgjengelig hvis du velger *Periode* i **Metode**-feltet.</p><p>La oss si at du velger *Periode* i **Metode**-feltet, angir *1* i **Per**-feltet og velger *Måneder* i **Enhet**-feltet. Du angir en sluttdato i **Slutt**-feltet som er ett år frem i tid. I dette tilfellet blir én prognoselinje opprettet for hver måned i det kommende året, basert på varen og antallet som er angitt i hodelinjen.</p> |
| Enhet | Velg enheten for tidsintervallet: *Dager*, *Måneder* eller *År*. Tildeling tilsvarer da antallet dager, måneder eller år du angir i **Per**-feltet.|
| Periodenøkkel | Angi periodetildelingsnøkkelen. |
| Slutt | Angi sluttdatoen når du bruker feltene **Per** og **Enhet**. |

### <a name="the-item-tab-on-the-supply-forecast-page"></a>Vare-fanen på Forsyningsprognose-siden

**Vare**-fanen viser mer vareinformasjon om linjen som for øyeblikket er valgt i **Oversikt**-fanen.

Rutenettet øverst i **Vare**-fanen gjentar vareinformasjon som også vises i **Oversikt**-fanen. Det omfatter i tillegg **Enhetspris**-feltet, som viser innkjøpsprisen for antallet enheter som er angitt i **Enhet**-feltet. Enhetsprisen hentes automatisk fra vareoppsettet, men du kan endre den.

Feltene nedenfor rutenettet inneholder flere varedetaljer. Deler av denne informasjonen gjentas fra **Oversikt**-fanen. I tabellen nedenfor beskrives feltene som er unike for **Vare**-fanen.

| Felt | beskrivelse |
|---|---|
| Prisenhet | Antall enheter som innkjøpsprisen gjelder for. Verdien hentes automatisk fra Varer-tabellen, men du kan endre den. |
| Innkjøpstillegg | Faste tillegg til innkjøpsprisen. Tilleggene er uavhengig av antallet. |
| Rabattprosent | Rabatten som en prosent. |
| Rabattbeløp | Rabatten som et beløp per salgsenhet. |
| Bruttobeløp | Beløpet når ingen rabatter blir brukt. |
| Antall | Transaksjonsantallet i varens lagerenhet. |
| Understykkliste | Stykklistenummeret til en bestemt understykkliste. |
| Underrute | Rutenummeret til en bestemt underrute. |

### <a name="the-financial-dimensions-tab-on-the-supply-forecast-page"></a>Finansdimensjoner-fanen på Forsyningsprognose-siden

**Finansdimensjoner**-fanen viser alle finansdimensjonsverdiene for linjen som for øyeblikket er valgt i **Oversikt**-fanen.

### <a name="the-inventory-dimensions-tab-on-the-supply-forecast-page"></a>Lagerdimensjoner-fanen på Forsyningsprognose-siden

**Lagerdimensjoner**-fanen viser alle lagerdimensjonsverdiene for linjen som for øyeblikket er valgt i **Oversikt**-fanen.

### <a name="the-allocation-grid-on-the-supply-forecast-page"></a>Rutenettet Tildeling på Forsyningsprognose-siden

Hvis du bruker en varefordelingsnøkkel eller har angitt en vareprognose for én eller flere fremtidige perioder, kan du tildele prognosen ved å velge **Fordel prognose** på verktøylinjen i **Oversikt**-fanen. Antallet distribueres deretter på måten som angis av linjene i rutenettet **Tildeling**.

## <a name="demand-forecast-lines"></a>Behovsprognoselinjer

Behovsprognosen lar deg angi eller generere behov etter en kunde. Den hjelper salgs- og markedsføringsassistenter å informere hovedplanleggingsassistenter om forventet behov i den kommende prognoseperioden.

Du kan angi en behovsprognose etter vare, varegruppe, varefordelingsnøkkel, kunde og kundegruppe. Hvis du vil ha informasjon om alle måtene du kan åpne **Behovsprognose**-siden for forskjellige enheter og poster på, kan du se delen [Vise og angi prognoselinjer manuelt](#manual-entry) tidligere i dette emnet.

Den øvre delen av **Behovsprognose**-siden har et rutenett med behovsprognoselinjer og et sett med faner du kan bruke til å vise og angi mer informasjon om en valgt prognoselinje. Den nedre delen av siden inneholder rutenettet **Tildeling**.

De følgende underdelene beskriver alle feltene som er tilgjengelige i hver fane, og alle kommandoene som er tilgjengelige i handlingsruten på siden og på verktøylinjen i **Oversikt**-fanen.

### <a name="action-pane-commands-on-the-demand-forecast-page"></a>Kommandoer i handlingsruten på Behovsprognose-siden

Tabellen nedenfor beskriver kommandoene som er tilgjengelige i handlingsruten på **Behovsprognose**-siden.

| Kommando | beskrivelse |
|---|---|
| Lagre | Lagre de gjeldende innstillingene. |
| Rediger | Aktiver innstillingene på siden som skal redigeres. |
| Nye | Legg til en prognoselinje i det øvre rutenettet. |
| Delete | Fjern den valgte prognoselinjen fra det øvre rutenettet. |
| Prognosesaldoer | Vis prognosesaldoer som er beregnet for den valgte linjens modell-ID for det gjeldende regnskapsåret. Saldoene deles etter periode (måned). |
| Kontantstrømprognose | Vis prognosetransaksjoner som må er fordeles til økonomimodulen. Hvis du vil ha mer informasjon, kan du se [Kontantstrømprognose](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Visningsdimensjoner | Velg produkt-, lager- og sporingsdimensjonene som skal vises i rutenettet, i **Oversikt**-fanen. |
| Forhåndsvisning av økonomimodul | Vis økonomimoduloppføringene for den valgte transaksjonen. |
| Overfør tilbudslinjer | Overfør tilbudslinjer til det valgte prosjektet. |

### <a name="toolbar-commands-on-the-overview-tab-of-the-demand-forecast-page"></a>Verktøylinjekommandoer i Oversikt-fanen på Behovsprognose-siden

Tabellen nedenfor beskriver kommandoene som er tilgjengelige på verktøylinjen i **Oversikt**-fanen på **Behovsprognose**-siden.

| Kommando | beskrivelse |
|---|---|
| Fordel prognose | Hvis du bruker en tildelingsmetode, genererer du de individuelle tidsplanlinjene for prognosetransaksjonen. Linjeantallet distribueres deretter etter dato (i samsvar med de valgte tidsintervallene), antall og beløp for hele tidshorisonten. |
| Masseoppdatering | Åpne siden **Rediger prognosetransaksjoner**. (Se delen [Masseoppdatere prognosetransaksjoner](#bulk-update) senere i dette emnet.) |
| Lagerprognose | Åpne en visning av **Lagerprognose**-siden som er filtrert for den valgte vare-/modellkombinasjonen. (Se delen [Lagerprognose](#inventory-forecast) senere i dette emnet.) |
| Opprett varebehov | Åpne en dialogboks der du kan opprette varebehov og salgsordre- eller varejournallinjer for prosjektrelaterte prognosetransaksjoner. |

### <a name="the-overview-tab-on-the-demand-forecast-page"></a>Oversikt-fanen på Behovsprognose-siden

Tabellen nedenfor beskriver feltene i **Oversikt**-fanen på **Behovsprognose**-siden.

| Felt | beskrivelse |
|---|---|
| **Oppgavenavn** | Navnet på den satsvise oppgaven som ble brukt til å opprette prognoselinjen. |
| **Modell** | Prognosemodellen som transaksjonen er knyttet til. |
| **Dato** | Startdatoen for transaksjonen. |
| **Kundekonto** | Kundekontoen som transaksjonen er knyttet til. |
| **Kundegruppe** | Kundegruppen som transaksjonen er knyttet til. |
| **Varenummer** | Identifikatoren for varen. |
| **Produktnavn** | Beskrivelsen av varen. |
| **Varefordelingsnøkkel** | Varefordelingsnøkkel som brukes under lagerprognosetildeling. |
| **Salgsantall** | Transaksjonsantallet i den angitte salgsenheten. |
| **Enhet** | Enheten som varen selges i. |
| **Beløp** | Bruttobeløpet, uten rabatter, som prognosetransaksjonen bidrar med i prognosen. |
| **Salgspris** | Salgsprisen for antallet enheter som er angitt i **Prisenhet**-feltet. Verdien hentes fra vareoppsettet, men du kan endre den. |
| **Salgsvaluta** | Valutaen som brukes for prognosetransaksjonen. Standardvalutaen angis automatisk, men du kan velge en annen valuta. |
| **Faktisk vekt-antall** | Prognoseantallet i den angitte faktisk vekt-enheten. |
| **Faktisk vekt-enhet** | Faktisk vekt-enheten som varen selges i. Verdien hentes automatisk fra vareoppsettet. |
| (Andre dimensjoner) | Ytterligere produkt-, lager- og sporingsdimensjoner kan vises som kolonner i rutenettet. Hvis du vil velge de ytterligere dimensjonene som vises, velger du **Vis dimensjoner** i handlingsruten. |

### <a name="the-general-tab-on-the-demand-forecast-page"></a>Generelt-fanen på Behovsprognose-siden

**Generelt**-fanen viser mer informasjon om linjen som for øyeblikket er valgt i **Oversikt**-fanen. Deler av denne informasjonen gjentas fra **Oversikt**-fanen. I tabellen nedenfor beskrives feltene som er unike for **Generelt**-fanen.

| Felt | beskrivelse |
|---|---|
| Serienummer for behovsprognose | Det unike nummeret på behovsprognoselinjen. Dette nummeret genereres ved å bruke nummerserien som er valgt for behovsprognoser på siden **Parametere for hovedplanlegging**. |
| Varegruppe | Varegruppen som transaksjonen er knyttet til. |
| Rapport | Sett dette alternativet til *Ja* hvis du vil ta med transaksjonen i rapporter. |
| Kommentarer | Angi eventuelle kommentarer om prognosetransaksjonen. |
| Aktivt | Merk av for dette hvis du vil ta med transaksjonen i budsjettrapporter. Innstillingen for denne avmerkingsboksen kan ikke endres for rapporteringstransaksjoner. |
| Inkluder i kontantstrømprognoser | Merk av for dette alternativet hvis du vil fordele prognosetransaksjonen til økonomimodulen. Innstillingen for denne avmerkingsboksen kan ikke endres for rapporteringstransaksjoner. Hvis du vil ha mer informasjon, kan du se [Kontantstrømprognose](../../finance/cash-bank-management/cash-flow-forecasting.md). |
| Merverdiavgiftsgruppe | Avgiftsgruppen som brukes til å angi avgifter for prognosetransaksjonen. |
| Varens mva-gruppe | Vareavgiftsgruppen som brukes til å angi avgifter for prognosetransaksjonen. |
| Metode | <p>Velg metoden du vil bruke til å tildele prognosetransaksjonen:</p><ul><li>**Ingen** – Ingen tildeling finner sted.</li><li>**Periode** – Prognoseberegn det samme antallet for hver periode. Hvis du velger denne verdien, angir du et antall i **Per**-feltet og en tidsenhet i **Enhet**-feltet.</li><li>**Nøkkel** – Tildel prognosen i samsvar med periodetildelingsnøkkelen du angir i **Periodenøkkel**-feltet. Du kan bruke denne metoden når du vil ta hensyn til sesongvariasjoner.</li><ul>|
| Per | <p>Angi hvor mange fremtidige tidsintervaller prognosen skal gjelde for. Dette feltet er bare tilgjengelig hvis du velger *Periode* i **Metode**-feltet.</p><p>La oss si at du velger *Periode* i **Metode**-feltet, angir *1* i **Per**-feltet og velger *Måneder* i **Enhet**-feltet. Du angir en sluttdato i **Slutt**-feltet som er ett år frem i tid. I dette tilfellet blir én prognoselinje opprettet for hver måned i det kommende året, basert på varen og antallet som er angitt i hodelinjen. |
| Enhet | Velg enheten for tidsintervallet: *Dager*, *Måneder* eller *År*. Tildeling tilsvarer da antallet dager, måneder eller år du angir i **Per**-feltet.|
| Periodenøkkel | Angi periodetilordningsnøkkelen som skal brukes til å tilordne prognosen. Hvis du vil ha mer informasjon, kan du se [Tildeling av data for budsjettplanlegging](../../finance/budgeting/budget-planning-data-allocation.md). |
| Slutt | Angi sluttdatoen når du bruker feltene **Per** og **Enhet**. |

### <a name="the-item-tab-on-the-demand-forecast-page"></a>Vare-fanen på Behovsprognose-siden

**Vare**-fanen viser mer vareinformasjon om linjen som for øyeblikket er valgt i **Oversikt**-fanen. Deler av denne informasjonen gjentas fra **Oversikt**-fanen. I tabellen nedenfor beskrives feltene som er unike for **Vare**-fanen.

| Felt | beskrivelse |
|---|---|
| Prisenhet | Antallet salgsenheter som salgsprisen gjelder for. Verdien hentes automatisk fra Varer-tabellen, men du kan endre den. |
| Salgstillegg | Faste tillegg til salgsprisen. Tilleggene er uavhengig av antallet. |
| Kostpris | Kostnaden for den gjeldende prognosetransaksjonen per lagerenhet. Verdien hentes fra Varer-tabellen, men du kan endre den. |
| Rabattprosent | Rabatten som en prosent. |
| Rabattbeløp | Rabatten som et beløp per salgsenhet. |
| Bruttobeløp | Beløpet når ingen rabatter blir brukt. |
| Lagerantall | Transaksjonsantallet i varens lagerenhet. |
| Bruk spesifikk stykkliste | Stykklistenummeret til en bestemt stykkliste. |
| Bruk spesifikk rute | Rutenummeret til en bestemt underrute. |

### <a name="the-project-tab-on-the-demand-forecast-page"></a>Prosjekt-fanen på Behovsprognose-siden

**Prosjekt**-fanen viser mer prosjektinformasjon om linjen som for øyeblikket er valgt i **Oversikt**-fanen. Noe av denne informasjonen gjentas fra fanen **Oversikt**, **Generelt** eller **Vare**. I tabellen nedenfor beskrives feltene som er unike for **Prosjekt**-fanen.

| Felt | beskrivelse |
|---|---|
| Prosjektdato | Datoen for behovsprognosetransaksjonen. |
| Prosjekt-ID | Identifikatoren for prosjektet som den gjeldende transaksjonen henviser til. |
| Finansieringskilde | Finansieringskilden som behovsprognosen er knyttet til. |
| Aktivitetsnummer | Aktiviteten som er knyttet til behovsprognosetransaksjonen. |
| Kategori | Kostnadskategorien for den gjeldende transaksjonen. |
| Linjeegenskap | Status som transaksjonen er knyttet til. |
| Transaksjons-ID | Systemidentifikatoren for behovsprognosetransaksjonen. |
| Kostnadsbeløp | Beløpet for behovsprognosetransaksjonen. |
| Enhetspris | Prisen per enhet. |
| Endret av | Identifikatoren til arbeideren som sist endret den valgte transaksjonen. |
| Fakturadato | Angi den forventede fakturadatoen. |
| Elimineringsdato | Vis eller endre elimineringsdatoen. Når prognosen opprettes, blir elimineringsdatoen satt til sluttdatoen for prosjektet. Hvis prosjektet ikke har en sluttdato, blir prosjektdatoen brukt. Dette feltet gjelder fastpris- og investeringsprosjekter. |
| Kostnadsbetalingsdato | Angi forventet dato for bestillingsbetalingen. |
| Salgsbetalingsdato | Angi forventet dato for salgsbetalingen. |

### <a name="the-financial-dimensions-tab-on-the-demand-forecast-page"></a>Finansdimensjoner-fanen på Behovsprognose-siden

**Finansdimensjoner**-fanen viser alle finansdimensjonsverdiene for linjen som for øyeblikket er valgt i **Oversikt**-fanen.

### <a name="the-inventory-dimensions-tab-on-the-demand-forecast-page"></a>Lagerdimensjoner-fanen på Behovsprognose-siden

**Lagerdimensjoner**-fanen viser alle lagerdimensjonsverdiene for linjen som for øyeblikket er valgt i **Oversikt**-fanen.

### <a name="the-allocation-grid-on-the-demand-forecast-page"></a>Rutenettet Tildeling på Behovsprognose-siden

Hvis du bruker en varefordelingsnøkkel eller har angitt en vareprognose for én eller flere fremtidige perioder, kan du tildele prognosen ved å velge **Fordel prognose** på verktøylinjen i **Oversikt**-fanen. Antallet distribueres deretter på måten som angis av linjene i rutenettet **Tildeling**.

## <a name="inventory-forecast"></a><a name="inventory-forecast"></a>Lagerprognose

Sidene for forsynings- og behovsprognoselinjer har en **Lagerprognose**-knapp som åpner en visning av **Lagerprognose**-siden som er filtrert for samme kombinasjon av vare og modell. Lagerprognosen representerer en balanse mellom forsyningen og behovet som ble angitt for den samme varen. Den kan ikke redigeres. Lagerprognosen hjelper lagerstyringsteamet å gå gjennom forventede endringer i lagerbeholdningen for en vare i løpet av den kommende perioden som er prognoseberegnet.

### <a name="the-action-pane-on-the-inventory-forecast-page"></a>Handlingsruten på Lagerprognose-siden

Tabellen nedenfor beskriver kommandoene som er tilgjengelige i handlingsruten på **Lagerprognose**-siden.

| Handling | beskrivelse |
|---|---|
| Forsyningsprognose | Åpne en visning av **Forsyningsprognose**-siden som er filtrert for den samme kombinasjonen av vare, modell og dato. |
| Behovsprognose | Åpne en visning av **Behovsprognose**-siden som er filtrert for den samme kombinasjonen av vare, modell og dato. |
| Lager \> Visningsdimensjoner | Velg produkt-, lager- og sporingsdimensjonene som skal vises, i rutenettet **Oversikt**. |

### <a name="the-grid-on-the-inventory-forecast-page"></a>Rutenettet på Lagerprognose-siden

I tabellen nedenfor beskrives feltene i rutenettet på **Lagerprognose**-siden.

| Felt | beskrivelse |
|---|---|
| **Modell** | Prognosemodellen som transaksjonen er knyttet til. |
| **Varenummer** | Identifikatoren for varen. |
| **Budsjettdato** | Datoen for prognosetransaksjonen. |
| **Prognosetype** | Kilden til transaksjonen (*Behovsprognose* eller *Forsyningsprognose*). |
| **Faktisk vekt-antall** | Prognoseantallet i faktisk vekt-enheten. |
| **Antall** | Prognoseantallet i lagerenheten. |
| **Akkumulert faktisk vekt** | Det akkumulerte prognoseantallet i faktisk vekt-enheten når flere prognoselinjer er akkumulert for den samme varen. |
| **Understykkliste** | Stykklistenummeret til en bestemt understykkliste. |
| **Underrute** | Rutenummeret til en bestemt underrute. |
| (Andre dimensjoner) | Ytterligere dimensjoner kan vises som kolonner i rutenettet. Hvis du vil velge de ytterligere dimensjonene som vises, velger du **Lager \> Vis dimensjoner** i handlingsruten. |

## <a name="bulk-update-forecast-transactions"></a><a name="bulk-update"></a>Masseoppdatere prognosetransaksjoner

Bruk denne fremgangsmåten til å behandle eksisterende prognosetransaksjonslinjer. Du kan kopiere, redigere og slette prognosetransaksjonslinjer.

1. Velg **Masseoppdatering** på siden for forsynings- eller behovsprognoselinjer.
1. Velg **Filter** i dialogboksen.
1. I **Område**-fanen velger du kriteriene som identifiserer kildeprognosedataene du vil kopiere, redigere eller slette. Disse dataene kan omfatte prognosemodellen, varenummeret og kundekontoen.
1. Velg **OK** for å bekrefte valget.

    Etter at dataene er valgt, kan du bruke dialogboksen **Rediger prognosetransaksjoner** til å definere hvordan du vil kopiere, redigere eller slette dem.

    > [!NOTE]
    > Filtreringstrinnet er en forutsetning for bruk av funksjonen **Masseredigering**. Hvis du hopper over det, velger og oppdaterer programmet **alle** prognoselinjene. Du kan dermed utilsiktet forårsake duplisering eller fjerning av transaksjoner.

1. Velg om du vil kopiere, oppdatere eller slette de valgte prognosetransaksjonene, i **Administrasjon**-delen.
1. Bruk delen **Endringer i felt** til å endre parameterne for prognosen. Velg avmerkingsboksen for en parameter, og velg deretter blant de tilgjengelige alternativene. Du kan for eksempel merke av for **Modell** og deretter velge et prognosemodellnummer. Eksisterende prognoselinjer blir kopiert til den valgte prognosemodellen.
1. Bruk delen **Endring av periode** til å flytte start- og sluttdatoene for prognosen fremover eller bakover. Velg avmerkingsboksen, og bruk deretter antalls- og periodefeltet til å definere hvordan prognosedatoene skal flyttes. Du kan angi et negativt antall for å flytte startdatoen fremover (det vil si gjøre den tidligere).

    Hvis du for eksempel vil forsinke startdatoen for prognosetransaksjonen med seks måneder, merker du av i avmerkingsboksen, angir *6* som antall og velger *Måneder* som periode.

1. Bruk delen **Rettelse av felt** til å oppdatere de faktiske prognosedataene. Velg kriteriet du ønsker å endre, i **Felt**-feltet. Angi en multipliseringsfaktor som skal brukes for det valgte kriteriet, i **Faktor**-feltet, eller angi en konstant for å addere eller subtrahere. Du kan for eksempel velge *Antall* som kriterium og angi en faktor på *1,5* for å multiplisere vareantallet med 1,5. Du kan alternativt angi en konstant på *–25* for å redusere vareantallet med 25 enheter.
1. Bruk delen **Finansdimensjoner** til å oppdatere finansdimensjonene til prognoselinjer. Velg finansdimensjonene du vil endre, og angi deretter en verdi som skal brukes på de valgte dimensjonene.
1. Velg **OK** for å bruke endringene.

## <a name="use-forecasts-with-master-planning"></a>Bruke prognoser med hovedplanlegging

Når du har angitt behovsprognosen og/eller forsyningsprognosen, kan du inkludere prognosene under hovedplanlegging for å ta hensyn til forventet behov og/eller forsyning i kjøringen av hovedplanlegging. Når prognoser inkluderes i hovedplanleggingen, beregnes det bruttobehov for materialer og kapasitet, og planlagte bestillinger genereres.

### <a name="set-up-a-master-plan-to-include-an-inventory-forecast"></a>Definere en hovedplan for å inkludere en lagerprognose

Følg denne fremgangsmåten for å konfigurere en hovedplan, slik at den inneholder en lagerprognose.

1. Gå til **Hovedplanlegging \> Oppsett \> Planer \> Hovedplaner**.
1. Velg en eksisterende plan, eller opprett en ny plan.
1. Angi følgende felt i hurtigfanen **Generelt**:

    - **Prognosemodell** – Velg prognosemodellen som skal brukes. Denne modellen blir tatt hensyn til når det genereres et forsyningsforslag for den gjeldende hovedplanen.
    - **Inkluder forsyningsprognose** – Sett dette alternativet til *Ja* for å inkludere forsyningsprognosen i gjeldende hovedplan. Hvis du setter det til *Nei*, blir ikke transaksjoner for forsyningsprognose inkludert i hovedplanen.
    - **Inkluder behovsprognose** – Sett dette alternativet til *Ja* for å inkludere behovsprognose i gjeldende hovedplan. Hvis du setter det til *Nei*, blir ikke transaksjoner for behovsprognose inkludert i hovedplanen.
    - **Metode som brukes til å redusere behovskrav** – Velg metoden som skal brukes til å redusere prognosebehovene. Hvis du vil ha mer informasjon, kan du se [Prognosereduksjonsnøkler](planning-optimization/demand-forecast.md#reduction-keys).

1. I **Horisonter i dager** kan du angi følgende felter for å angi perioden som prognosen skal tas med i:

    - **Prognoseplan** – Sett dette alternativet til *Ja* for å overstyre prognoseplanen som kommer fra de individuelle dekningsgruppene. Sett det til *Nei* for å bruke verdiene fra de individuelle dekningsgruppene for den gjeldende hovedplanen.
    - **Tidsperiode for prognose** – Hvis du angir **Prognoseplan** til *Ja*, angir du antall dager (fra dagens dato) som behovsprognose skal brukes på.

    > [!IMPORTANT]
    > Alternativet **Prognoseplan** støttes ikke med Planleggingsoptimalisering ennå.

### <a name="run-a-master-plan-that-includes-an-inventory-forecast"></a>Kjøre en hovedplan som inkluderer en lagerprognose

Følg denne fremgangsmåten for å kjøre en hovedplan som inneholder en lagerprognose.

1. Gå til **Hovedplanlegging \> Arbeidsområder \> Hovedplanlegging**.
1. I **Hovedplan**-feltet angir eller velger du hovedplanen som du definerte i den forrige fremgangsmåten.
1. Velg **Kjør** i **Hovedplanlegging**.
1. I dialogboksen **Hovedplanlegging** angir du alternativet **Spor behandlingstid** til *Ja*.
1. Angi et tall i feltet **Antall tråder**.
1. Velg **Filtrer** i hurtigfanen **Poster som skal inkluderes** .
1. En standard dialogboks for Power Query-redigering vises. I fanen **Område** velger du raden der **Felt**-feltet er satt til *Varenummer*.
1. Velg varenummeret som skal tas med i planen, i **Kriterier**-feltet.
1. Velg **OK**.

Hvis du vil vise behovene som beregnes, åpner du **Bruttobehov**-siden. Velg for eksempel **Bruttobehov** i **Behov**-gruppen i **Plan**-fanen på siden **Frigitte produkter** i handlingsruten.

Hvis du vil vise de planlagte bestillingene som genereres, kan du gå til **Hovedplanlegging \> Felles \> Planlagte bestillinger** og velge den aktuelle prognoseplanen.

## <a name="additional-resources"></a>Tilleggsressurser

- [Oversikt over behovsprognose](introduction-demand-forecasting.md)
- [Oppsett av behovsprognose](demand-forecasting-setup.md)
- [Generer en statistisk basislinjeprognose](generate-statistical-baseline-forecast.md)
- [Foreta manuelle justeringer i basislinjeprognosen](manual-adjustments-baseline-forecast.md)
- [Hovedplanlegging med behovsprognoser](planning-optimization/demand-forecast.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
