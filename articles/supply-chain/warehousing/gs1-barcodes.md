---
title: GS1-strekkoder
description: Dette emnet beskriver hvordan du definerer GS1-strekkoder og QR-koder slik at etiketter kan skannes på et lager.
author: Mirzaab
ms.date: 03/21/2022
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.25
ms.openlocfilehash: 083748d4aecf551fd326b6c3cbf6d92cf3daf717
ms.sourcegitcommit: d475dea4cf13eae2f0ce517542c5173bb9d52c1c
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/05/2022
ms.locfileid: "8547823"
---
# <a name="gs1-bar-codes"></a>GS1-strekkoder

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]
<!-- Preview until 10.0.25 GA -->

Lagerarbeidere må ofte utføre flere oppgaver når de bruker en mobilenhetskanner for å registrere bevegelser av en vare, palett eller container. Disse oppgavene kan omfatte både å skanne strekkoder og legge inn informasjon manuelt på mobilenheten. Strekkodene bruker et firmaspesifikt format som du definerer og administrerer ved hjelp av Microsoft Dynamics 365 Supply Chain Management.

GS1-strekkoder for fraktetiketter ble utviklet for å gi en global standard for utveksling av data mellom firmaer. De er tilgjengelige i både lineære symbologier, som 1D (strekkodeformater), for eksempel GS1-128, og 2D-symbologier, for eksempel GS1 DataMatrix og GS1 QR-koder. GS1-strekkoder koder ikke bare data, men lar deg også bruke en forhåndsdefinert liste over *app-ID-er* for å definere betydningen av disse dataene. GS1-standarden definerer dataformatet og de forskjellige datatypene som den kan brukes til å kode. I motsetning til eldre strekkodestandarder kan GS1-strekkoder ha flere dataelementer. Derfor kan ett enkelt strekkodesøk registrere flere typer produktinformasjon, for eksempel bunken og utløpsdatoen.

GS1-støtten i Supply Chain Management forenkler skanneprosessen i lagre der paller og containere merkes ved hjelp av strekkoder i GS1-format. Lagerarbeidere kan hente ut all nødvendig informasjon ved hjelp av en enkelt skanning av en GS1-strekkode. Ved å eliminere behovet for å utføre flere søk og/eller angi informasjon manuelt, bidrar GS1-strekkoder til å redusere tiden som er knyttet til oppgavene. Samtidig kan de også øke nøyaktigheten.

Logistikksjefer må definere den nødvendige listen over applikasjons-IDer og knytte hver av dem til de aktuelle menyelementene for mobilenheter. Applikasjons-IDene kan deretter brukes på tvers av lagre som en global innstilling for flyttings- og emballasjeformål. Derfor tar alle fraktetikettene et felles skjema.

Med mindre annet er angitt, bruker dette emnet begrepet *strekkode* for å referere til både lineære strekkoder (1D) og 2D-strekkoder.

## <a name="the-gs1-bar-code-format"></a>GS1-strekkodeformatet

De generelle spesifikasjonene for GS1angir hvilke symbologier som kan brukes for GS1-strekkoder, og hvordan dataene i strekkoden skal kodes. Denne delen gir en kort innledning til emnet. Hvis du vil ha fullstendig informasjon, kan du se de [generelle spesifikasjonene for GS1](https://www.gs1.org/docs/barcodes/GS1_General_Specifications.pdf) som er publisert av GS1. GS1-spesifikasjonene oppdateres regelmessig, og informasjonen er oppdatert med de genrelle spesifikasjonene for GS1, versjon 22.0.

GS1-strekkoder bruker følgende symbologier:

- **Lineære eller 1D-strekkoder** – GS1-128 og GS1 DataBar
- **2D-strekkoder** – GS1 DataMatrix, GS1 QR-kode og GS1 Dotcode

Legg merke til at det er spesielle benevnelser av GS1 i GS1-128, som er et spesielt tilfelle av den vanlige lineære strekkoden Code-128, GS1 DataMatrix og GS1 QR-kode. Forskjellen mellom GS1-versjonen og ikke-GS1-versjonen er tilstedeværelsen av et spesialtegn (FNC1) som det første tegnet i strekkodedataene. Tilstedeværelsen av et FNC1-tegn betyr at dataene i strekkoden skal tolkes i henhold til GS1-spesifikasjonen.

Dataene i selve strekkoden består av flere dataelementer, som hver for seg identifiseres av en app-ID ved starten av feltet. Vanligvis presenteres dataene også under strekkoden i et lesbart format, der app-ID-en vises i parentes. Her er et eksempel: `(01) 09521101530001 (17) 210119 (10) AB-123`. Denne strekkoden inneholder tre elementer:

- **App-ID 01** – Det globale GS1-handelsvarenummeret (GTIN) for varen.
- **App-ID 17** – Utløpsdatoen.
- **App-ID 10** – Partinummeret.

For hvert element kan dataene enten ha en forhåndsdefinert lengde eller en variabel lengde. Det finnes en fast liste over app-ID-er med forhåndsdefinert lengde. Alle andre app-ID-er har variabel lengde, og listen over GS1-app-ID-er angir maksimal lengde og dataformatet. App-ID 01 har for eksempel en forhåndsdefinert lengde på 16 tegn (to for selve app-ID-en og deretter 14 for GTIN), og app-ID 17 har en forhåndsdefinert lengde på åtte tegn (to for selve app-ID-en og deretter seks for datoen). App-ID 10 har imidlertid to tall for selve app-ID-en og deretter opptil 20 alfanumeriske tegn.

Hvis et element følger et element med variabel lengde, må det brukes et skilletegn når de settes sammen. Dette skilletegnet kan enten være det spesielle FNC1-tegnet eller gruppeskilletegnet (et tegn som ikke kan skrives ut, som har ASCII-kode 29 og heksadesimal kode 1D). Skilletegnet bør ikke brukes etter det siste elementet. Selv om skilletegnet heller ikke bør brukes etter elementer som har forhåndsdefinert lengde, er ikke tilstedeværelsen en kritisk feil.

I strekkodedataene fra det forrige eksemplet på en strekkode som inneholder app-ID 01, 17 og 10, kodes dataene i en Code-128, QR-kode eller et DataMatrix-symbol som `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` (app-ID-er vises i fet skrift). Det er en god fremgangsmåte å plassere alle elementer som har variabel lengde på slutten, for å eliminere behovet for et ekstra gruppeskilletegn. Strekkoden kan imidlertid også ha en forskjellig rekkefølge på elementene, der skilletegnet er obligatorisk. Her er et eksempel: `<FNC1>`**`01`**`09521101530001`**`10`**`AB-123<GS>`**`17`**`210119`.

### <a name="dates-and-decimal-numbers"></a>Datoer og desimaltall

Datoer representeres alltid i *ÅÅMMDD*-format, og århundret til året bestemmes av GS1-spesifikasjoner. Bare datoer fra 49 år i fortiden til 50 år i fremtiden (i forhold til gjeldende år) kan representeres.

Enkelte dataelementer inneholder desimaltall. For eksempel representerer app-ID-ene 3100, 3101, ... 3105 representerer en nettovekt i kilogram. Fordi disse app-ID-ene har en forhåndsdefinert lengde på 10, er seks tall tilgjengelige for antallet. Posisjonen til desimalpunktet angis av det siste tallet i app-ID-en. Derfor kan denne serien med app-ID-er også representeres som *310n*. Ettersom GS1-standarden angir at det alltid må være minst ett tall til venstre for desimalpunktet, er maksimalt fem desimaler tillatt.

Her er noen eksempler som viser hvordan tallet *123456* tolkes av ulike app-ID-er (vist med fet skrift):

- **`3100`**`123456` &rarr; 123456 (heltall)
- **`3101`**`123456` &rarr; 12345.6 (én desimal)
- **`3102`**`123456` &rarr; 1234.56 (to desimaler)
- **`3103`**`123456` &rarr; 123.456 (tre desimaler)
- **`3104`**`123456` &rarr; 12.3456 (fire desimaler)
- **`3105`**`123456` &rarr; 1.23456 (fem desimaler)

## <a name="scanning-gs1-bar-codes-in-supply-chain-management"></a>Skanning av GS1-strekkoder i Supply Chain Management

Når lagerarbeidere skal skanne GS1-strekkoder, bruker de en skanner som er innebygd i eller koblet til en mobilenhet. Skanneren overfører deretter den skannede strekkoden til Warehouse Management-mobilappen som en serie med tastaturhendelser. Denne operasjonsmåten er også kjent som en *tastaturkortleser* eller en *kortleser*. Mobilappen sender deretter den mottatte teksten som den er til Supply Chain Management. Når systemet mottar inndata, bestemmer det først om dataene begynner med et av de konfigurerte prefiksene som angir at dataene faktisk er en GS1-strekkode (se delen [Definer globale GS1-alternativer](#set-gs1-options)). Hvis de skannede dataene ikke starter med ett av disse prefiksene, bruker systemet en GS1-parser til å dele opp dataene og hente individuelle dataelementer i henhold til app-ID-ene. Når dataene er delt opp, blir enten gjeldende inndatafelt eller flere felter fylt ut med de skannede dataene.

### <a name="configuration-of-bar-code-scanner-hardware-and-software"></a>Konfigurasjon av maskinvare og programvare for strekkodeskanner

For at Supply Chain Management skal kunne gjenkjenne og dekode GS1-strekkoder korrekt, må maskinvareskanneren eller støtteprogramvaren konfigureres til å utføre følgende handlinger:

- Legg til et prefiks i de skannede strekkodene, slik at systemet kan gjenkjenne en GS1-strekkode.
- Konverter ASCII-gruppeskilletegnet som ikke kan skrives ut (ASCII-kode 29 eller heksadesimal kode 1D) til et tegn som kan skrives ut, for eksempel en tilde (~).

Selv om du kan legge til et hvilket som helst prefiks i den skannede strekkoden, er det et alternativ å legge til en ID for ISO/IEC 15424-symbologien, også kalt en *AIM-ID*. Denne ID-en på tre tegn starter med `]`, og deretter med ett tegn som identifiserer symbologien som brukes, og deretter et tall som brukes som en ytterligere modifikator. AIM-ID-en `]C1` angir for eksempel en Code 128-strekkode (på grunn av tegnet `C`), og modifikatoren `1` angir at det er et FNC1-tegn i den første posisjonen i dataene. På den annen side er `]C0` en Code 128-strekkode som har ethvert annet tegn som det første tegnet i dataene.

Følgende fem symbologi-ID-er tilsvarer GS1-strekkoder som har app-ID-elementer:

- `]C1` – Code 128 (`C`) med FNC1-tegn i første posisjon (`1`), også kjent som GS1-128.
- `]e0` – GS1 DataBar.
- `]d2` – DataMatrix (`d`) med ECC 200 og FNC1 i første posisjon (`2`), også kjent som GS1 DataMatrix.
- `]Q3` – QR-kode (`Q`) Model 2-symbol med FNC1 i første posisjon (`3`), også kjent som GS1 QR-kode.
- `]J1` – GS1 DotCode.

Hvis du bruker disse ID-ene, krever kompatibilitet med ikke-GS1-strekkoder at skannerne eller skanneprogramvaren er konfigurert til å fjerne ID-er som ikke samsvarer med GS1-ID-ene. Hvis du for eksempel skanner en normal Code 39-strekkode, blir prefikset `]A0` lagt til. Fordi systemet ikke vil forstå dette prefikset som et av GS1-prefiksene, vil det tolke det som data og gi uventede resultater.

> [!NOTE]
> Av praktiske årsaker vil versjon 2.0.17.0 og senere av Warehouse Management-mobilappen fjerne alle AIM-prefikser som ikke er inkludert i den forrige listen. Denne virkemåten støtter tilfeller der du kan konfigurere skanneren til å legge til AIM-prefikset, men ikke fjerne de uønskede prefiksene.

### <a name="single-and-multiple-field-scanning"></a>Skanning av ett felt og flere felter

Når dataene er analysert fra strekkoden, blir de matet inn i flytkontrollene for mobilenheten. Det finnes to metoder som vil bli behandlet hver for seg:

- **Enkeltfeltskanning** – Denne metoden fyller bare ut feltet som strekkoden ble skannet inn i. Hvis du for eksempel skanner strekkoden `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123` mens markøren er i **Vare**-feltet, blir GTIN `09521101530001` fra strekkoden angitt i dette feltet. Hvis du skanner den samme strekkoden mens markøren er i feltet **Parti-ID**, angis partinummeret `AB-123` fra strekkoden. Denne modusen fungerer for alle felter i alle flyter og krever bare at det generelle GS1-oppsettet er konfigurert. Hvis en strekkode inneholder flere elementer, må den skannes flere ganger, fordi bare én del av strekkoden om gangen vil bli angitt i flyten på mobilenheten. Denne virkemåten styres av det generelle GS1-oppsettet, som beskrevet i delen [Opprett det generelle GS1-oppsettet](#generic-gs1-setup).
- **Flerfeltsskanning** – Denne metoden fyller ut flere felter når én strekkode skannes, ved å videresende tilleggsdata til flyttilstanden for mobilenheten. Policyen konfigureres for eksempel til å videresende app-ID 01 inn i `ItemId`-kontrollen og app-ID 10 inn i `InventBatchId`-feltet. Hvis du i dette tilfellet skanner strekkoden `<FNC1>`**`01`**`09521101530001`**`17`**`210119`**`10`**`AB-123`, blir data for begge variablene videresendt samtidig. Derfor vil ikke systemet be deg om vare- og/eller partinummeret i flyten. Denne virkemåten styres av GS1-policyer som er koblet til menyelementer, som beskrevet i delen [Definer GS1-policyer til å være menyelementer for mobilenheter](#policies-for-menus).

> [!WARNING]
> Standard GS1-policyer er testet til å fungere uten uventet atferd. Tilpasning av GS1-policyer som er koblet til menyelementer, kan imidlertid forårsake uventet atferd, fordi flyten kanskje ikke forventer at enkelte data er tilgjengelige på et bestemt tidspunkt.

## <a name="turn-on-the-gs1-feature"></a>Aktivere GS1-funksjonen

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Skann GS1-strekkoder*

### <a name="turn-on-the-enhanced-parser-for-gs1-barcodes-feature"></a>Aktiver funksjonen Forbedret analyse for GS1-strekkoder

Hvis du bruker GS1-strekkoder, anbefaler vi at du også aktiverer funksjonen *Forbedret analyse for GS1-strekkoder*. Denne funksjonen gir en forbedret implementering av GS1-strekkodeanalyseringen. Den legger til følgende forbedringer:

- Den følger GSGS1-algoritmen for generell spesifikasjon for symboldataanalyse og validerer at dataene i symbolet er gyldige i henhold til spesifikasjonen.
- Den krever ikke at du definerer en verdi for **Maksimumslengde for ID**, og den bruker lengste prefikssamsvar fra konfigurerte app-ID-er.
- Den gjør det enklere å konfigurere app-ID-er med desimaler ved å bruke bokstaven *n* til å samsvare med et hvilket som helst tall. Du kan for eksempel konfigurere bare én app-ID (*310n*) i stedet for separate app-ID-er (*3101*, *3102*, *3103* og så videre).
- Den løser et problem der feilkodede data tolkes som feltdata.
- Den leveres som en separat klasse som kan brukes på nytt i andre sammenhenger, og gjør det mulig å bruke et utvidbarhetspunkt til å manipulere skannede data før flytfeltene fylles ut.

## <a name="set-up-global-gs1-options"></a><a name="set-gs1-options"></a>Definer globale GS1-alternativer

Siden **Warehouse Management-parametere** har noen innstillinger som etablerer globale GS1-alternativer.

Gjør følgende for å konfigurere globale GS1-alternativer:

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. Angi følgende felter på hurtigfanen **Strekkoder**:

    - **FNC1-tegn**, **Datamatrix-tegn** og **QR-kodetegn** – Angi tegn som skal tolkes som et prefiks for hver type GS1-strekkode.
    - **Gruppeskilletegn** – Angi tegnet som erstatter ASCII-gruppeskilletegnet.
    - **Maksimumslengde for ID** – Angi maksimalt antall tegn som er tillatt for app-ID-en. Dette feltet kreves ikke hvis funksjonen *Forbedret GS1-analyse* er aktivert i systemet.

> [!NOTE]
> Prefikser forteller systemet at en strekkode er kodet i henhold til GS1-standarden. Opptil tre prefikser (**FNC1-tegn**, **Datamatrisetegn** og **QR-kodetegn**) kan brukes samtidig og til forskjellige formål.

## <a name="gs1-application-identifiers"></a>GS1-programidentifikatorer

GS1-formater koder ikke bare dataene, men lar deg også bruke en forhåndsdefinert liste over app-ID-er for å definere betydningen av dataene. Logistikksjefer må definere den nødvendige listen over applikasjons-IDer og knytte hver av dem til de aktuelle menyelementene for mobilenheter. ID-ene kan deretter brukes på tvers av lagre som en global innstilling for flyttings- og emballasjeformål. Derfor tar alle fraktetikettene et felles skjema.

Systemet bruker dataene, spesielt de forhåndsdefinerte app-ID-ene, til å fastsette reglene som skal brukes på den relevante delen av skannede informasjon.

Hver app-ID signaliserer til systemet at etterfølgende tegn i den skannede strekkoden bør betraktes som en blokk med kryptert informasjon. Oppsettet for app-ID-ene definerer hvordan systemet skal tolke en strekkode og lagre den som en verdi i systemet.

Logistikksjefer kan bruke standard internasjonale app-ID-er og/eller opprette sine egne.

### <a name="load-the-standard-application-identifiers"></a>Last inn standard app-ID-er

Du kan komme raskt i gang ved å laste inn en liste over vanlige internasjonale app-ID-er. Du kan deretter utvide eller redigere listen senere, etter behov.

Følg denne fremgangsmåten for å laste inn standard app-ID-er.

1. Gå til **Warehouse Management \> Oppsett \> GS1 \> GS1-app-ID-er**.
1. Velg **Opprett standardoppsett** i handlingsruten.

> [!WARNING]
> Kommandoen **Opprett standardoppsett** sletter alle app-ID-ene som er definert, og erstatter dem med standardlisten. Når du har lastet inn standardoppsettet, kan du imidlertid tilpasse listen etter behov.

### <a name="set-up-custom-application-identifiers"></a>Sett opp egendefinerte app-ID-er

Hvis noen eller alle app-ID-ene som firmaet bruker, er forskjellige fra standardsettet, kan du opprette dine egne koder fra begynnelsen eller tilpasse standardsettet etter behov.

Følg denne fremgangsmåten for å konfigurere og tilpasse dine egne GS1-app-ID-er.

1. Gå til **Warehouse Management \> Oppsett \> GS1 \> GS1-app-ID-er**.
1. Følg ett av disse trinnene:

    - For å opprette en ny ID velger du **Ny** i handlingsruten.
    - Hvis du vil redigere en eksisterende ID: Velg ID-en, og velg deretter **Rediger** i handlingsruten.

1. Angi følgende felter for den nye eller valgte ID-en:

    - **App-ID** – Angi identifikasjonskoden for app-ID-en. Denne koden er vanligvis et tosifret heltall, men den kan være lengre. For desimalverdier angir det siste sifferet antallet desimaler. Hvis du vil ha mer informasjon, kan du se beskrivelsen av avmerkingsboksen **Desimal** senere i denne listen. Hvis funksjonen *Forbedret analyse for GS1-strekkoder* er aktivert, kan du opprette én enkelt app-ID for alle desimalplassvarianter ved å bruke bokstaven *n* som det siste tegnet i app-ID-en. Du kan for eksempel konfigurere bare én app-ID (*310n*) i stedet for en separat app-ID for hvert antall desimaler (*3101*, *3102*, *3103* og så videre).
    - **Beskrivelse** – Angi en kort beskrivelse av ID-en.
    - **Fast lengde** – Merk av i denne avmerkingsboksen hvis verdier som skannes ved hjelp av denne app-ID-en, har et fast antall tegn. Fjern merket i denne boksen hvis verdilengden er variabel. I dette tilfellet må du angi slutten på verdien ved å bruke gruppeskilletegnet som du angav på siden **Warehouse Management-parametere**.
    - **Lengde** – Angi maksimalt antall tegn som kan vises i verdiene som skannes ved hjelp av denne app-ID-en. Hvis det er merket av for **Fast lengde**, forventes nøyaktig dette antallet tegn.
    - **Type** – Velg verditypen som skannes ved hjelp av denne app-ID-en (*numerisk*, *alfanumerisk* eller *dato*). Hvis du vil ha mer informasjon om hvordan datoer og tall representeres i strekkodedata, kan du se delen [Datoer og desimaltall](#dates-and-decimal-numbers).
    - **Desimal** – Merk av i denne avmerkingsboksen hvis verdien inneholder et underforstått desimalpunkt. Hvis det er merket av i denne boksen, bruker systemet det siste sifferet i app-IDen til å bestemme antallet desimalplasser. Hvis du vil ha mer informasjon om hvordan datoer og tall representeres i strekkodedata, kan du se delen [Datoer og desimaltall](#dates-and-decimal-numbers).

> [!WARNING]
> Selv om systemet vil tillate at du merker av for **Fast lengde** for enhver app-ID, bør dette bare brukes for delsettet med app-ID-er som har en forhåndsdefinert lengde per de generelle GS1-spesifikasjonene. Den forbedrede GS1-analysen inneholder allerede listen over alle app-ID-er som har forhåndsdefinert lengde.

> [!NOTE]
> Verdien for **Gruppeskilletegn** som er angitt på siden **Warehouse management-parametere**, er valgfri hvis en verdi som er etterfulgt av en app-ID, har en fast lengde.

## <a name="establish-the-generic-gs1-setup"></a><a name="generic-gs1-setup"></a>Opprett det generelle GS1-oppsettet

Det generelle GS1-oppsettet fastsetter en samling vanlige tilordninger. Disse tilordningene samsvarer med hvert relevante inndatafelt i mobilappen med app-ID-en som kontrollerer hvordan verdier fra skannede strekkoder tolkes og lagres i dette feltet. Som standard gjelder disse innstillingene for alle søk for alle menyelementer på mobilenheter. De kan imidlertid overskrives for ett eller flere bestemte felter av en GS1-policy som er tilordnet til et bestemt menyelement.

Det generelle GS1-oppsettet tillater bare én verdi å skannes om gangen. Hvis du vil laste inn flere feltverdier fra ett enkelt søk, må du derfor definere en GS1-policy for de relevante menyelementene.

Se neste del for mer informasjon om GS1-policyer.

### <a name="load-the-standard-generic-gs1-setup"></a>Laste inn det standard generelle GS1-oppsettet

På siden **Generelt GS1-oppsett** kan du laste inn et standardsett med tilordninger mellom felter på mobilenheter og standard app-ID-er som opprettes av standardoppsettet.

Hvis du vil opprette det generelle GS1-oppsettet, kan du gå til **Warehouse Management \> Oppsett \> GS1 \> Generelt GS-oppsett**. Deretter velger du **Opprett standardoppsett** for å automatisk tilordne en passende app-ID til hvert felt som vanligvis brukes av menyelementer på mobilenheter.

> [!WARNING]
> Hvis det allerede finnes et generelt GS1-oppsett, vil kommandoen **Opprett standardoppsett** slette det fullstendig og laste inn standardoppsettet.

### <a name="customize-the-standard-generic-gs1-setup"></a>Tilpass det standard generelle GS1-oppsettet

Følg denne fremgangsmåten for å tilpasse det generelle GS1-oppsettet.

1. Gå til **Warehouse Management \> Oppsett \> GS1 \> Generelt GS1-oppsett**.
1. Følg ett av disse trinnene:

    - I handlingsruten velger du **Ny** for å opprette en ny tilordning.
    - Hvis du vil redigere en eksisterende tilordning: Velg tilordningen, og velg deretter **Rediger** i handlingsruten.

1. Angi følgende felter for den nye eller valgte tilordningen:

    - **Felt** – Velg eller angi inndatafeltet for mobilappen som den innkommende verdien skal tilordnes til. Verdien er ikke visningsnavnet som arbeiderne ser. Den er i stedet nøkkelnavnet som er tilordnet til feltet i den underliggende koden. Standardoppsettet inneholder en samling felt som sannsynligvis vil være nyttige, og inkluderer intuitive nøkkelnavn for hvert felt og hver samsvarende programmerte funksjonalitet. Det kan imidlertid hende at du må kontakte utviklingspartnerne dine for å finne de riktige valgene for implementeringen.
    - **App-ID** – Velg den aktuelle app-ID-en, som er definert på siden **GS1-app-ID-er**. ID-en fastsetter hvordan strekkoden tolkes og lagres som en verdi for det navngitte feltet. Når du har valgt en app-ID, vises beskrivelsen av den i **Beskrivelse**-feltet.

## <a name="set-up-gs1-policies-to-be-to-mobile-device-menu-items"></a><a name="policies-for-menus"></a>Definer GS1-policyer til å være menyelementer for mobilenheter

Formålet med GS1-standarden er å gjøre det mulig for ansatte å laste inn flere verdier når de skanner en enkelt strekkode én gang. For å oppnå dette formålet må logistikksjefer definere GS1-policyer som forteller systemet hvordan de tolker strekkoder med flere verdier. Senere kan du tilordne policyer til menyelementer for mobilenheter for å styre hvordan en strekkode tolkes når arbeidere skanner den mens de bruker et bestemt menyelement.

Hvis ingen GS1-policy er tilordnet et menyelement, kan systemet bare registrere en enkelt verdi. Denne verdien brukes for inndataene i mobilappen som velges når arbeideren tar søket, som angitt av det generelle GS1-oppsettet. Hvis en GS1-policy er tilordnet menyelementet, bruker systemet det generelle GS1-oppsettet til å tilordne den første strekkodeverdien til det valgte feltet. Deretter kan det imidlertid registrere flere feltverdier, som angitt i den aktuelle policyen.

### <a name="load-the-standard-specific-gs1-policies"></a>Last inn de spesifikke GS1-standardpolicyene

Du kan komme raskt i gang ved å laste inn et sett med GS1-policyer. Du kan deretter utvide eller redigere policyene senere, etter behov.

Følg denne fremgangsmåten for å laste inn standard app-ID-er.

1. Gå til **Warehouse Management \> Oppsett \> GS1 \> GS1-policy**.
1. Velg **Opprett standardoppsett** i handlingsruten.

> [!WARNING]
> Kommandoen **Opprett standardoppsett** sletter alle policyene som er definert, og erstatter dem med standardsettet med policyer. Når standardoppsettet er lastet inn, kan du imidlertid tilpasse policyene etter behov.

### <a name="set-up-custom-specific-gs1-policies"></a>Sett opp egendefinerte GS1-policyer

> [!WARNING]
> Det kan hende at enkelte GS1-policyer ikke fungerer med enhver mobilflyt du bruker. Når du konfigurerer egendefinerte GS1-policyer, må du teste flyten for mobilenheten ved å bruke ulike deler med informasjon som skannes på forskjellige tidspunkt i flyten. På denne måten kan du finne ut om flyten fungerer som forventet.

Følg denne fremgangsmåten for å sette opp og tilpasse GS1-policyene:

1. Gå til **Warehouse Management \> Oppsett \> GS1 \> GS1-policy**.
1. Følg ett av disse trinnene:

    - I handlingsruten velger du **Ny** for å opprette en ny policy.
    - Hvis du vil redigere en eksisterende policy, velger du policyen i listeruten.

1. I toppteksten i den nye eller valgte policyen angir du følgende felter:

    - **Policynavn** – Angi et navn for policyen.
    - **Beskrivelse** – Angi en kort beskrivelse av policyen.

1. På hurtigfanen under hodet tilordner du feltnavn til app-ID-er etter behov for den gjeldende policyen. Bruk knappene på verktøylinjen for å legge til og rader regler etter behov. For hver rad angir du feltene nedenfor:

    - **Felt** – Velg eller angi inndatafeltet for mobilappen som den innkommende verdien skal tilordnes til. Verdien er ikke visningsnavnet som arbeiderne ser. Den er i stedet nøkkelnavnet som er tilordnet til feltet i den underliggende koden. Standardoppsettet inneholder en samling felt som sannsynligvis vil være nyttige, og inkluderer intuitive nøkkelnavn for hvert felt og hver samsvarende programmerte funksjonalitet. Det kan imidlertid hende at du må kontakte utviklingspartnerne dine for å finne de riktige valgene for implementeringen.
    - **App-ID** – Velg den aktuelle app-ID-en, som er definert på siden **GS1-app-ID-er**. ID-en fastsetter hvordan strekkoden tolkes og lagres som en verdi for det navngitte feltet. Når du har valgt en app-ID, vises beskrivelsen av den i **Beskrivelse**-feltet.
    - **Sortering** – Hver flerverdistrekkode inkluderer en serie med app-ID-er, der hver ID er etterfulgt av en verdi. Den aktuelle GS1-policyen identifiserer hvilken app-ID som er tilordnet hvert databasefelt. Hvis en strekkode imidlertid bruker samme app-ID mer enn én gang, bruker systemet rekkefølgen som app-ID-ene vises i, for å tilordne dem til felt. For rader som deler en app-ID med én eller flere andre rader, bruker du dette feltet til å fastsette rekkefølgen som de samsvarende radene behandles i. Raden som har den laveste sorteringsverdien, behandles først.

> [!NOTE]
> For strekkoder som inneholder mer enn én identisk app-ID, *må* du bruke **Sortering**-feltet til å fastsette rekkefølgen på feltene.

## <a name="assign-gs1-policies-to-mobile-device-menu-items"></a>Tilordne GS1-policyer til enyelementer på mobilenheten

Som standard har alle menyelementer for mobilenheter inndatafelter der arbeidere kan skanne en enkelt verdi i henhold til det generelle GS1-oppsettet. Hvis du vil at arbeidere skal kunne skanne mer enn én feltverdi i ett enkelt søk etter et menyelement på en mobilenhet, må du tilordne en GS1-policy ved å følge disse trinnene.

1. Gå til **Lagerstyring \> Oppsett \> Mobilenhet \> Menyelementer på mobilenheten**.
1. Opprett eller åpne et menyelement.
1. På hurtigfanen **Generelt** angir du feltet **GS1-policy** til policyen som gjelder for menyelementet.

## <a name="gs1-setup-example"></a>Eksempel på GS1-oppsett

Dette eksemplet gjelder for et system der GS1-alternativene konfigureres på følgende måte:

- På siden **Warehouse Management-parametere** er følgende globale innstillinger opprettet:

    - **FNC1-tegn:** *\]C1*
    - **Skilletegn for gruppe:** *\~*

- På siden **GS1-app-ID-er** er følgende app-ID-er relevante for dette eksemplet.

    | Programidentifikator | beskrivelse | Fast lengde | Lengde | Type | Desimal |
    |---|---|---|---|---|---|
    | 01 | GTIN | Valgt | 14 | Numerisk | Avstem |
    | 10 | Partinummer | Avstem | 20 | Alfanumerisk | Avstem |
    | 17 | Utløpsdato | Valgt | 6 | Dato | Avstem |
    | 30 | Mottaksantall | Avstem | 8 | Numerisk | Avstem |

- På siden **Generelt GS1-oppsett** er følgende innstillinger for den generelle GS1-policyen relevante for dette eksemplet.

    | Felt | Programidentifikator | beskrivelse |
    |---|---|---|
    | ItemId | 01 | GTIN |

- På siden **GS1-policy** finnes det en policy der feltet **Policynavn** er satt til *Innkjøpsmottak*. Denne policyen omfatter følgende linjer.

    | Felt | Programidentifikator | beskrivelse | Sortering |
    |---|---|---|---|
    | ExpDate | 17 | Utløpsdato | 0 |
    | InventBatchId | 10 | Partinummer | 0 |
    | Antall | 30 | Mottaksantall | 0 |

- På siden **Menyelementer på mobilenheten** finnes det et menyelement kalt *Innkjøpsmottak*. Feltet **GS1-policy** er angitt til *Innkjøpsmottak*.

Når varer for en bestilling ankommer lageret, følger arbeideren disse trinnene.

1. Velg menyelementet **Innkjøpsmottak** på mobilenheten.
1. Angi bestillingsnummeret.
1. Velg **Vare**-feltet, og skann følgende strekkode: `]C10100000012345678~3030~10b1~17220215`.

På grunn av innstillingene som er fastsatt for dette eksemplet, analyserer systemet den skannede strekkoden på følgende måte.

| Feltnøkkel | App-ID | Verdi | Merk |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Fordi arbeideren skannet til **Vare**-feltet, tilordnes den første verdien i strekkoden til dette feltet. Tilordningen tas fra det generelle oppsettet for GS1. |
| Antall | 30 | 30 | Fordi flere feltverdier registreres i en enkelt skanning, hentes denne tilordningen og alle gjenværende tilordninger fra GS1-policyen som er tilordnet menyelementet **Innkjøpsmottak**. Denne verdien er antallet som ble mottatt. |
| InventBatchId | 10 | b1 | Denne verdien er parti-ID-en. |
| ExpDate | 17 | 220215 | Datoformatet er ÅÅMMDD. Utløpsdatoen er derfor 15. februar 2022. |

Mottaket registreres deretter, og de relevante databaseverdiene angis etter enkeltskanningen.
