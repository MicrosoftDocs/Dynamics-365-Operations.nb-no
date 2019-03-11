---
title: Rapporteringstredefinisjoner finansrapporter
description: Denne artikkelen gir informasjon om rapporteringstredefinisjoner. En rapporteringstredefinisjon er en rapportkomponent eller byggeblokk, som bidrar til å definere strukturen og hierarkiet i organisasjonen.
author: ShylaThompson
manager: AnnBe
ms.date: 01/11/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: FinancialReports
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 57592
ms.assetid: 747faa47-9a23-4277-bc11-8d0a1267c3a4
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-05-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 00219f21076af60f8e2f16ca365b1138bb279400
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "316953"
---
# <a name="reporting-tree-definitions-in-financial-reports"></a>Rapporteringstredefinisjoner finansrapporter

[!include [banner](../includes/banner.md)]

Denne artikkelen gir informasjon om rapporteringstredefinisjoner. En rapporteringstredefinisjon er en rapportkomponent eller byggeblokk, som bidrar til å definere strukturen og hierarkiet i organisasjonen.

Finansrapporter støtter fleksibel rapportering, slik at du enkelt kan gjøre endringer når forretningsstrukturen endres. Rapporter bygges opp av ulike komponenter eller byggeblokker. Én av disse byggeblokkene er en rapporteringstredefinisjon. En rapporteringstredefinisjon bidrar til å definere strukturen og hierarkiet i organisasjonen. Den er en hierarkisk struktur på tvers av dimensjoner som basert på dimensjonsrelasjonene i de økonomiske dataen. Den inneholder informasjon på rapporteringsenhetsnivå og et sammendragsnivå for alle enheter i treet. Rapporteringstredefinisjonene kan kombineres med kolonnedefinisjoner og rapportdefinisjoner for å opprette en blokkgruppe som kan brukes av flere firmaer. En rapporteringsenhet brukes for hver boks i et organisasjonskart. En rapporteringsenhet kan være en enkeltstående avdeling fra finansdataene, eller en summeringsenhet på et høyere nivå, som kombinerer informasjon fra andre rapporteringsenheter. For en rapportdefinisjon som inkluderer et rapporteringstre genereres en rapport for hver rapporteringsenhet og for sammendragsnivået. Alle disse rapportene bruke rad- og kolonnedefinisjoner som er angitt i rapportdefinisjonen, med mindre rapportdefinisjonen angir at rapporteringstreet fra raddefinisjonen skal brukes. Rad- og kolonnedefinisjoner er viktige komponenter i utformingen og funksjonaliteten til økonomiske rapporter. Rapporteringtrær øke funksjonaliteten til komponenter og støtter fleksibel rapportering etter hvert som forretningsstrukturen endres. Finansrapporter som ikke er basert på et rapporteringstre bruker bare noen av funksjonene i finansrapportering. Du kan bruke flere rapporteringstredefinisjoner sammen med samme rad og kolonnedefinisjoner til å vise organisasjonens data på forskjellige måter.

## <a name="reporting-tree-best-practices"></a>Anbefalte fremgangsmåter for rapporteringstre
Før du oppretter et rapporteringstre bør du vurdere følgende anbefalte fremgangsmåter:

- Fastslå først hvilke rapporteringsdimensjoner den juridiske enheten eller firmaet trenger.
- Vurdere hvordan du har definert strukturen, og tegn deretter et organisasjonskart for firmaet ditt. Organisasjonsdiagrammet er til hjelp når du skal se for deg hvordan du grupperer rapporteringsenhetene i ett eller flere rapporteringstrær.
- Start med det lavest tilgjengelige detaljnivået, for eksempel avdelinger og prosjekter som er definert i de økonomiske dataen. Legg til bokser etter behov på detaljnivået, for å vise overordnede avdelinger eller områder. Hver boks representerer en potensiell rapporteringsenhet i et rapporteringstreet som du oppretter.
- Du må også vurdere den beste metoden for å bygge trær. Du kan bruke en automatisert byggeprosessen for å generere et rapporteringstre, eller du kan opprette et rapporteringstre manuelt. Det er viktig at du forstår begge metodene før du utformer trærne.
- Du kan bruke rapporteringsenhetene som er definert i systemet for økonomiske data, for å legge til rapportenheter i rapporteringstredefinisjonen.

## <a name="create-multiple-reporting-trees"></a> Opprette flere rapporteringstrær
Du kan opprette et ubegrenset antall rapporteringstrær for å vise organisasjonens data på forskjellige måter. Hvert rapporteringstre kan inneholde en kombinasjon av avdelinger og summeringsenheter. En rapportdefinisjon kan inneholde en kobling til bare ett rapporteringstre om gangen. Ved å omorganisere strukturen for rapporteringsenhetene, kan du opprette forskjellige rapporteringstrær. Du kan deretter bruke samme rad- og kolonnedefinisjoner for hvert rapporteringstreet. På denne måten kan du raskt opprette ulike finansrapportoppsett. Hvis du oppretter flere rapporteringstrær, kan du skrive ut en serie med regnskapsoppgjør hver måned som analyserer og presentere firmaets operasjoner på en rekke måter. Hvis du vil ha mer informasjon, kan du se eksemplene på strukturer for rapporteringsenhet på slutten av denne artikkelen.

## <a name="create-a-reporting-tree-definition"></a> Opprette rapporteringstredefinisjon
En rapporteringstredefinisjonen inneholder kolonnene som er beskrevet i tabellen nedenfor.

| Rapporteringstrekolonne | Beskrivelse |
|-----------------------|-------------|
| Firma               | Firmanavnet for rapporteringsenheten. Verdien **@ANY**, som vanligvis tilordnes bare til sammendragsnivået, aktiverer rapporteringstreet slik at det kan brukes for alle firmaer. Alle underordnede avdelinger er tilordnet til et firma. |
| Enhetsnavn             | Koden som identifiserer rapporteringsenheten i det grafiske rapporteringstreet. Pass på å opprette et unik fargekodingssystem som er konsekvent, og som skal være enkelt for brukerne å forstå. |
| Enhetsbeskrivelse      | Tittelen for rapporteringsenheten vises i topp- eller bunnteksten på rapporten hvis du angir **UnitDesc** som kode i kategorien **Topptekst og bunntekst** i rapportdefinisjonen. Tittelen vises i radbeskrivelsen for rapporten hvis du angir **UnitDesc** i **Beskrivelse**-cellen for raddefinisjonen. |
| Dimensjoner            | En rapporteringsenhet som henter informasjon direkte fra de økonomiske dataen. Den definerer den logisk plassering og lengdene for kontoen og tilknyttede segmenter. Hver rad for rapporteringsenhet må ha en dimensjon i denne kolonnen. Du kan også legge en dimensjon i en rad for sammendragsenhet (for eksempel for utgifter som er direkte relatert til denne enheten). Hvis du angir en dimensjon i en rad for sammendragsenhet, må kontoer som brukes i overordnede enheter ikke brukes i underordnede enheter. Hvis ikke, kan det hende beløpene blir duplisert. |
| Raddefinisjoner       | Navnet på raddefinisjonen for rapporteringsenheten. Den samme raddefinisjonen brukes for hver enhet i rapporteringstreet. Når du genererer en rapport, brukes denne raddefinisjonen for hver rapporteringsenhet. Raddefinisjonen kan inneholde flere koblinger til finansdimensjoner. Hvis en raddefinisjon er angitt i rapporteringstreet, merker du av for **Bruk raddefinisjon fra rapporteringstre** i kategorien **Rapport** i rapportdefinisjonen. |
| Radkobling              | Radkoblingen som skal brukes for rapporteringsenheten. Radkoblinger defineres for raddefinisjonen for å identifisere finansdimensjonene det skal kobles til. |
| Ekstern kobling         | Radkoblingen som skal brukes for denne rapporteringsenheten. Radkoblinger er definert for raddefinisjonen for å identifisere rapporten som skal kobles til. |
| Ekstern fil         | Filbanen til regnearket for finansrapportering som det skal hentes data fra. |
| Sidealternativer          | Denne kolonnen angir om detaljene for rapporteringsenhet undertrykkes når rapporten vises eller skrives ut. |
| Opprulling i %              | Prosentdelen av rapporteringsenheten som skal tilordnes til den overordnede enheten. Prosentdelen du angir i denne kolonnen, gjelder for hver rad i raddefinisjonen før verdien i raden legges til den overordnede rapporten. Hvis en underordnet enhet for eksempel skal deles likt mellom to avdelinger, blir beløpene i hver rad multiplisert med 50 prosent før verdien legges til i avdelingsrapporten. Én rapporteringsenhet kan ikke ha to overordnede enheter. Hvis du vil tilordne beløpene fra en rapportering til to overordnede enheter, kan du opprette en annen rapporteringsenhet som har samme dimensjon for å rulle opp de ekstra 50 prosentene. Skriv inn hele prosentdeler uten desimaltegn. **25** representerer for eksempel 25 prosent allokering til overordnet. Hvis du tar med et desimaltegn (**,25**), vil 0,25 prosent allokeres til overordnet. Hvis du vil bruke en prosentdel som er mindre enn én prosent, kan du bruke alternativet **Tillat opprulling &lt;1%** i rapportdefinisjonen. Dette alternativet er i kategorien **Tilleggsalternativer** i dialogboksen **Rapportinnstillinger**. Du kan åpne denne dialogboksen fra **Annet**-knappen i kategorien **Innstillinger** i rapportdefinisjonen. |
| Enhetssikkerhet         | Begrensninger for brukere og grupper som har tilgang til informasjon for rapporteringsenheten. |
| Tilleggstekst       | Tekst som er inkludert i rapporten. |

Følg fremgangsmåten nedenfor for å opprette en rapporteringstredefinisjon.

1. Åpne Rapportutforming.
2. Klikk **Fil** &gt; **Ny** &gt; **Rapporteringstredefinisjon**.
3. Klikk **Rediger** &gt; **Sett inn rapporteringsenheter fra dimensjoner**.
4. I dialogboksen **Sett inn rapporteringsenheter fra dimensjoner** merker du av for hver dimensjon som skal tas med i rapporteringstreet. Dialogboksen **Sett inn rapporteringsenheter fra dimensjoner** inneholder delene nedenfor.

    | Seksjon                          | Beskrivelse |
    |----------------------------------|-------------|
    | Segmentering av rapporteringsdimensjon | Bruk knappene **Del segmenter** og **Kombiner segmenter** til å endre antallet av og lengden på segmenter.<blockquote>[!NOTE] Du kan bare kombinere segmenter som du har delt. Hvis du vil kombinere flere dimensjoner, kan du bruke jokertegn i dimensjonsverdiene.</blockquote> |
    | Inkluder/tegnposisjon       | Dette avsnittet viser dimensjonene som er definert i de økonomiske dataene, og viser antall tegn i den lengste verdien som er definert for hver dimensjon. Merk av for en dimensjon for å inkludere denne dimensjonen i hierarkiet for rapporteringstreet. |
    | Segmenter hierarki og områder     | Dette avsnittet viser dimensjonshierarkiet. Du kan flytte dimensjonene i listen for å endre rapporteringsrekkefølgen. Du kan angi en rekke verdier i hver dimensjon i feltene **Fra dimensjon** og **Til dimensjon**. Hvis du ikke angir et område, settes alle dimensjonsverdier inn i rapporteringstreet.<blockquote>[!NOTE] Hvis du bruker flere dimensjoner, blir bare dimensjonskombinasjoner det er postert til, returnert i resultatene.</blockquote> |

    Hvis du vil vise et skjermbilde som viser et eksempel på dialogboksen **Sette inn rapporteringsenheter fra dimensjoner**, kan du se avsnittet "Eksempel på Sett inn rapporteringsenheter fra dialogboksen Dimensjoner" senere i denne artikkelen.

5. Hvis du vil opprette flere segmenter (for eksempel ved å dele opp ett segment i to kortere segmenter), klikker du den aktuelle posisjonen i feltet **Tegnposisjon**, og deretter klikker du **Del segmenter**.
6. Hvis du vil slå sammen to segmenter til ett segment, klikker du en av segmentboksene for å slå sammen, og deretter klikker du **Kombiner segmenter**.
7. Hierarkiet definerer hvordan dimensjonene rapporterer til hverandre og området for hver dimensjon. Hvis du vil endre hierarki for dimensjonene i området **Segmenter hierarki og områder**, velger du dimensjonen du vil flytte, og deretter klikker du **Flytt opp** eller **Flytt ned**.
8. Hvis du vil angi en rekke dimensjonsverdier å legge til i det nye rapporteringstreet, følger du følgende fremgangsmåte i området **Segmenter hierark og områder**:

    1. I feltet **Fra dimensjon** for denne dimensjonen, angir du den første verdien i området.
    2. Angi den siste verdien i området i feltet **Til dimension**.

9. Gjenta trinn 7 til 8 for hver dimensjon i området **Segmenter hierarki og områder**.
10. Når du er ferdig med å definere hvordan rapportenhetene skal hentes inn i det nye rapporteringstreet, klikker du **OK**.
11. Klikk **Fil** &gt; **Lagre** for å lagre rapporteringstreet. Skriv inn et unikt navn og beskrivelse for rapporteringstreet, og klikk deretter **OK**.

### <a name="open-an-existing-reporting-tree-definition"></a>Åpne en eksisterende rapporteringstredefinisjon

1. Klikk **Rapporteringstredefinisjoner** i navigasjonsruten i Rapportutforming.
2. Dobbeltklikk et navn i rapporteringstrelisten for å åpne det.
3. Hvis du vil vise alle byggeblokker som er knyttet til rapporteringstreet, høyreklikker du rapporteringstredefinisjonen og velger deretter **Tilknytninger**.

### <a name="roll-up-data-in-a-reporting-tree"></a>Rulle opp data i er rapporteringstre

Når du bruker et rapporteringstre, kan du samle beløp fra underordnede rapporteringsenheter på det nivået for den overordnede rapporteringsenheten. Dette aggregeringen kalles å rulle opp dataene. Følgende regler brukes til å rulle opp beløp til overordnede enheter i et rapporteringstre:

- I et rapporterings må underordnede enheter inneholde dimensjoner, med mindre det er et rapporteringstre med ett nivå. Overordnede enheter inneholder vanligvis ikke dimensjoner i et rapporteringstre.

    > [!NOTE]
    > Hvis du angir dimensjoner for både underordnede enheter og overordnede enheter, kan det føre til duplisering av data i rapporten.

- Rapportenheter som inneholder dimensjoner i rapporteringstreet tilsvarer dimensjonene som brukes i rad- og kolonnedefinisjonene. Kombinasjonen av dimensjonene bestemmer beløpene som returneres for denne enheten. I eksempel 2 senere i denne artikkelen, returnerer linje 6 og 7 verdier bare for henholdsvis avdeling 00 og 01.
- Beløpene for overordnede rapporteringsenheter som ikke inneholder dimensjoner i rapporteringstreet, bestemmes fra rapporten for den underordnede enheten, og beløpet rulles opp til den angitte overordnede enheten. Hvis den overordnede enheten (se Contoso USA i eksempel 2 for eksempler på opprulling) for eksempel har to underordnede enheter (022 og 023) og ikke inneholder dimensjoner, genereres en rapport for hver underordnet og overordnet enhet. Den overordnede totalen er summen av de to underordnede beløpene.

### <a name="manage-reporting-units"></a>Administrere rapporteringsenheter

Hver rapporteringstredefinisjon vises i unike visninger. Det finnes en grafisk visning som viser det overordnede/underordnede hierarkiet, og en regnearkvisning som viser den spesifikke informasjon om hver rapporteringsenhet. Den grafiske visningen og regnearkvisningen er koblet. Når du velger en rapporteringsenhet i én visning, velges den også i den andre visningen. Du kan bygge hierarkier på tvers av dimensjoner som er basert på dimensjonsrelasjonene i de økonomiske dataen. Når du oppretter en rapporteringstredefinisjon, kan du bruke de samme raddefinisjonene flere ganger, uavhengig av om du genererer resultatregnskap for en avdeling eller resultatregnskapet for et konsolidert sammendrag. Dimensjonene som er definert i raddefinisjonen kan kombineres med dimensjonene rapporteringstredefinisjonen for å gi en rekke forskjellige visninger av organisasjonens ytelse.

### <a name="reporting-unit-structure"></a> Struktur for rapporteringsenhet

Følgende typer rapporteringsenheter brukes i finansrapportering:

- En detaljenhet henter informasjon direkte fra de økonomiske dataene, fra en Excel-regneark eller fra et annet regneark for finansrapportering.
- En sammendragsenhet summerer data fra enheter på lavere nivå.

En overordnet rapporteringsenhet er en sammendragsenhet som samler sammendragsinformasjonen fra en detaljenhet. En sammendragsenhet kan være både en detaljenhet og en sammendragsenhet. Derfor kan en sammendragsenhet hente informasjon fra en enhet på lavere nivå, økonomiske data eller et Excel-regneark. En overordnet enhet kan være en underordnet enhet for en overordnet enhet på høyere nivå. En underordnet rapporteringsenhet kan være en detaljenhet som henter informasjon direkte fra de økonomiske dataene eller et Excel-regneark. En underordnet rapporteringsenhet kan også være en mellomliggende sammendragsenhet. Den kan med andre ord være den overordnede enheten for en enhet på et lavere nivå, og også den underordnede enheten for en sammendragsenhet på høyere nivå. I det vanligste scenariet for rapporteringsenheter har overordnede enheter en tom celle i kolonnen **Dimensjoner**, og underordnede enheter har koblinger til bestemte dimensjoner eller jokertegnkombinasjoner for dimensjoner.

### <a name="organize-reporting-units"></a> Ordne rapporteringsenheter

Du kan ordne organisasjonsstrukturen i en rapporteringstredefinisjon ved å flytte rapporteringsenheter i den grafiske visningen. Du kan også forfremme rapporteringsenheter til et høyere nivå i rapporteringstreet eller senke dem til et lavere nivå.

1. Åpne rapporteringstreet som skal endres i Rapportutforming.
2. Velg en rapporteringsenhet i den grafiske visningen av rapporteringstredefinisjonen.
3. Dra enheten til en ny plassering. Du kan også høyreklikke enheten og deretter velge **Forfremme rapporteringsenhet** eller **Senk rapporteringsenhet**.
4. Klikk **Fil** &gt; **Lagre** for å lagre endringene.

### <a name="add-text-about-a-reporting-unit"></a> Legge til tekst om en rapporteringsenhet

En oppføring for tilleggstekst er en statisk tekststreng med opptil 255 tegn, som legger til informasjon i rapporteringstredefinisjonen. Tilleggsteksten kan for eksempel være en kort beskrivelse av firmaet. Du kan opprette opptil ti oppføringer for tilleggstekst for hver rapporteringsenhet i en rapporteringstredefinisjon. Tilleggsteksten vises i rapporten for rapporteringsenheten som teksten er tilordnet. Du kan legge til tekstoppføringer fra **Beskrivelse**-kolonnen i raddefinisjonen, og fra kategorien **Topptekst og bunntekst** i rapportdefinisjonen.

1. Åpne rapporteringstreet som skal endres i Rapportutforming.
2. Dobbeltklikk **Tilleggstekst**-cellen for raden for rapporteringsenheten.
3. Skriv inn teksten i den første tomme raden i dialogboksen **Tilleggstekst**. Den første raden som inneholder tekst, kalles Enhetstekst1, uavhengig av posisjonen i dialogboksen **Tilleggstekst**.
4. Hvis du vil legge til flere tekstoppføringer for rapporteringsenheten, skriver du inn teksten i en tom rad.
5. Klikk **OK**.

### <a name="remove-additional-text-from-a-reporting-unit"></a>Fjerne tilleggstekst fra en rapporteringsenhet

1. Åpne rapporteringstredefinisjonen som skal endres, i Rapportutforming.
2. Dobbeltklikk **Tilleggstekst**-cellen for raden til rapporteringsenheten.
3. I dialogboksen **Tilleggstekst** velger du oppføringen som skal fjernes, og deretter klikker du **Fjern**. Du kan også høyreklikke oppføringen og deretter velge **Klipp ut**.
4. Klikk **OK**.

### <a name="restrict-access-to-a-reporting-unit"></a>Begrense tilgang til en rapporteringsenhet

Du kan hindre at bestemte brukere eller grupper får tilgang til en rapporteringsenhet. Du kan også definere begrensninger, slik at de gjelder for underordnede rapporteringsenheter for rapporteringsenheten.

1. Åpne rapporteringstreet som skal endres i Rapportutforming.
2. Dobbeltklikk **Enhetssikkerhet**-cellen for raden i rapporteringsenheten det skal begrenses tilgang til.
3. I dialogboksen **Enhetssikkerhet** klikker du **Brukere og grupper**.
4. Velg brukerne eller gruppene som skal ha tilgang til rapporteringsenheten, og klikk deretter **OK**.
5. Hvis du vil begrense tilgang til underordnede rapportenheter, merker du av for **Legg til sikkerhet for underordnede rapporteringsenheter**.
6. Klikk **OK**.

### <a name="remove-access-to-a-reporting-unit"></a>Fjerne tilgang til en rapporteringsenhet

1. Åpne rapporteringstreet som skal endres i Rapportutforming.
2. Dobbeltklikk **Enhetssikkerhet**-cellen for raden for rapporteringsenheten som tilgang skal fjernes for.
3. Velg et navn, og klikk deretter **Fjern** i dialogboksen **Enhetssikkerhet**.
4. Klikk **OK**.

### <a name="link-toreports"></a>Koble til rapporter

Når du har opprettet en  **rapportkolonne** i raddefinisjonen, og har angitt rapporten som skal tas med i rapporten, må du oppdatere rapporteringstreet med den koblede kolonnen og informasjonen om rapporten. En rapport kan importeres til enheter i rapporteringstreet.

### <a name="identify-the-report-in-a-reporting-tree"></a>Identifisere rapporten i rapporteringstreet

1. Åpne rapporteringstreet som skal endres i Rapportutforming.
2. Informasjonscellene i **Raddefinisjoner**-kolonnen er basert på informasjonen for den valgte raden, fordi samme raddefinisjon må brukes i alle enheter i rapporteringstreet. Dobbeltklikk **Raddefinisjoner**-cellen, og velg deretter raddefinisjonen som inneholder informasjon om rapporten.
3. I **Regnearkkobling**-cellen for rapporteringsenhet velger du koblingsnavnet som samsvarer med rapporten.
4. I cellen **Bane til arbeidsbok eller rapport** for en rapporteringsenhet, skriver du inn navnet på rapporten eller går til den valgte rapporten.
5. Hvis du vil angi et regneark i en rapport, skriver du inn navnet på regnearket i cellen **Regnearknavn**.
6. Gjenta trinn 3 til 5 for alle rapporteringsenheter som skal motta data fra en rapport. Hvis du vil hindre at feil data vises i rapporten, må du passe på at de riktige rapportnavnene vises i den tilsvarende enheten i rapporteringstreet

## <a name="examples"></a>Eksempler
### <a name="reporting-unit-structure--example-1"></a>Struktur for rapporteringsenhet – Eksempel 1

Her er strukturen for rapporteringsenhetene i følgende rapporteringstre:

- Rapporteringsenheten Contoso Japan en overordnet enhet for de underordnede enhetene Contoso Japan Sales og Contoso Japan Consulting.
- Avdelingsenheten Contoso Japan Sales er både en underordnet enhet for Contoso Japan-enheten og en overordnet enhet for enhetene Home Sales og Auto Sales.
- Rapporteringsenhetene på det laveste nivået (Home Sales, Auto Sales, Client Services, and Operations) representerer avdelinger i de økonomiske dataen. Disse rapporteringsenhetene er i det skyggelagte området i diagrammet.
- Sammendragsenhetene på høyere nivå summerer informasjon fra detaljenhetene.

[![ContosoEntertainmentSummaryReportStructure](./media/contosoentertainmentsummaryreportstructure.png)](./media/contosoentertainmentsummaryreportstructure.png)

### <a name="reporting-unit-structure--example-2"></a>Struktur for rapporteringsenhet – Eksempel 2

I diagrammet nedenfor har rapporteringstre en organisasjonsstruktur som er delt inn etter forretningsfunksjon.

[![summaryofallunitscontoso](./media/summaryofallunitscontoso.png)](./media/summaryofallunitscontoso.png)

### <a name="example-of-the-insert-reporting-units-from-dimensions-dialog-box"></a>Eksempel på dialogboksen Sett inn rapporteringsenheter fra dimensjoner

Illustrasjonen nedenfor viser et eksempel på dialogboksen **Sett inn rapporteringsenheter fra dimensjoner**. I dette eksemplet returnerer resultatene kombinasjonen av forretningsenheter, kostsentre og avdelinger.

[![InsertReportingUnits](./media/insertreportingunits.png)](./media/insertreportingunits.png)

Den resulterende rapporteringstredefinisjonen er sortert etter forretningsenhet, deretter etter kostsenter og til slutt etter avdeling. Dimensjonen for den femte rapporteringsenheten er **Forretningsenhet = \[001\], Kostsenter =\[\], Avdeling = \[022\]**, og identifiserer en rapporteringsenhet for kontoer som er spesifikke for forretningsenhet 001 og avdeling 022.

[![Rapporteringstre](./media/reportingtree-1024x646.png)](./media/reportingtree.png)

### <a name="examples-of-data-roll-up"></a>Eksempler på opprulling av data

Eksemplene nedenfor viser mulig informasjon som brukes i en rapporteringstredefinisjon for data som rulles opp.

#### <a name="example-1"></a>Eksempel 1

[![MutliCompanyRollUp](./media/mutlicompanyrollup.png)](./media/mutlicompanyrollup.png)

#### <a name="example-2"></a>Eksempel 2

[![CrossCompanyDepartmentRollUp](./media/crosscompanydepartmentrollup.png)](./media/crosscompanydepartmentrollup.png)

## <a name="additional-resources"></a>Tilleggsressurser

[Finansrapportering](financial-reporting-intro.md)
