---
title: GS1-strekkoder og QR-koder
description: Dette emnet beskriver hvordan du definerer GS1-strekkoder og QR-koder slik at etiketter kan skannes på et lager.
author: Mirzaab
ms.date: 08/02/2021
ms.topic: article
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-08-02
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: ef28fcaf308225a78bcbac42f591e6b24b21b1b1
ms.sourcegitcommit: 2b04b5a5c883d216072bb91123f9c7709a41f69a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2021
ms.locfileid: "7384543"
---
# <a name="gs1-bar-codes-and-qr-codes"></a>GS1-strekkoder og QR-koder

[!include [banner](../includes/banner.md)]
[!INCLUDE [preview-banner](../includes/preview-banner.md)]

Lagerarbeidere må ofte utføre flere oppgaver når de bruker en mobilenhetskanner for å registrere bevegelser av en vare, palett eller container. Disse oppgavene kan omfatte både å skanne strekkoder og legge inn informasjon manuelt på mobilenheten. Strekkodene bruker et firmaspesifikt format som du definerer og administrerer ved hjelp av Microsoft Dynamics 365 Supply Chain Management.

GS1-strekkode- og QR-kodeformater for fraktetiketter ble utviklet for å gi en global standard for utveksling av data mellom firmaer. GS1-formater koder ikke bare dataene, men lar deg også bruke en forhåndsdefinert liste over *app-ID-er* for å definere betydningen av dataene. GS1-standarden definerer dataformatet og de forskjellige datatypene som den kan brukes til å kode. I motsetning til eldre strekkoder kan GS1-strekkoder ha flere dataelementer. Derfor kan ett enkelt strekkodesøk registrere flere typer produktinformasjon, for eksempel bunken og utløpsdatoen.

GS1-støtten i Supply Chain Management forenkler skanneprosessen i lagre der paller og containere merkes ved hjelp av koder i GS1-format. Lagerarbeidere kan hente ut all nødvendig informasjon ved hjelp av en enkelt skanning av en GS1-strekkode. Ved å eliminere behovet for å utføre flere søk og/eller angi informasjon manuelt, bidrar GS1-strekkoder til å redusere tiden som er knyttet til oppgavene. Samtidig kan de også øke nøyaktigheten.

Logistikksjefer må definere den nødvendige listen over applikasjons-IDer og knytte hver av dem til de aktuelle menyelementene for mobilenheter. Applikasjons-IDene kan deretter brukes på tvers av lagre som en global innstilling for flyttings- og emballasjeformål. Derfor tar alle fraktetikettene et felles skjema.

Med mindre annet er angitt, bruker dette emnet begrepet *strekkode* for å referere til både strekkoder og QR-koder.

## <a name="turn-on-the-gs1-feature"></a>Aktivere GS1-funksjonen

Før du kan bruke denne funksjonen, må den være aktivert i systemet. Administratorer kan bruke innstillingene for [funksjonsbehandling](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til å kontrollere funksjonsstatusen og aktivere den. I **Funksjonsadministrering**-arbeidsområdet er denne funksjonen oppført på følgende måte:

- **Modul:** *Lagerstyring*
- **Funksjonsnavn:** *Skann GS1-strekkoder*

## <a name="set-up-global-gs1-options"></a>Definer globale GS1-alternativer

Siden **Warehouse Management-parametere** har noen innstillinger som etablerer globale GS1-alternativer.

Gjør følgende for å konfigurere globale GS1-alternativer:

1. Gå til **Lagerstyring \> Oppsett \> Lagerstyringsparametere**.
1. Angi følgende felter på hurtigfanen **Strekkoder**:

    - **FNC1-tegn** – Angi tegn som skal tolkes som et prefiks når en strekkode analyseres.
    - **Datamatrisetegn** – Angi tegn som skal tolkes som et prefiks når en datamatrise analyseres.
    - **QR-kodetegn** – Angi tegn som skal tolkes som et prefiks når en QR-kode analyseres.
    - **Gruppeskilletegn** – Angi tegnet som identifiserer separate deler av en strekkode eller QR-kode.
    - **Maksimumslengde for ID** – Angi maksimalt antall tegn som er tillatt for app-ID-en.

> [!NOTE]
> Prefikser forteller systemet at en strekkode er kryptert i henhold til GS1-standarden. Opptil tre prefikser (**FNC1-tegn**, **Datamatrisetegn** og **QR-kodetegn**) kan brukes samtidig og til forskjellige formål.

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

    - **App-ID** – Angi identifikasjonskoden for app-ID-en. Denne koden er vanligvis et tosifret heltall, men den kan være lengre. For desimalverdier angir det siste sifferet antallet desimaler. Hvis du vil ha mer informasjon, kan du se beskrivelsen av avmerkingsboksen **Desimal** senere i denne listen.
    - **Beskrivelse** – Angi en kort beskrivelse av ID-en.
    - **Fast lengde** – Merk av i denne avmerkingsboksen hvis verdier som skannes ved hjelp av denne app-ID-en, har et fast antall tegn. Fjern merket i denne boksen hvis verdilengden er variabel. I dette tilfellet må du angi slutten på verdien ved å bruke gruppeskilletegnet som du angav på siden **Warehouse Management-parametere**.
    - **Lengde** – Angi maksimalt antall tegn som kan vises i verdiene som skannes ved hjelp av denne app-ID-en. Hvis det er merket av for **Fast lengde**, forventes nøyaktig dette antallet tegn.
    - **Type** – Velg verditypen som skannes ved hjelp av denne app-ID-en (*numerisk*, *alfanumerisk* eller *dato*). For datoer er det forventede formatet ÅÅMMDD (uten mellomrom eller bindestreker).
    - **Desimal** – Merk av i denne avmerkingsboksen hvis verdien inneholder et underforstått desimalpunkt. Hvis det er merket av i denne boksen, bruker systemet det siste sifferet i app-IDen til å bestemme antallet desimalplasser. Hvis app-ID-en for eksempel er *3205*, tolkes de høyre fem sifrene i verdien for å komme etter desimaltegnet.

> [!NOTE]
> Gruppeskilletegnet som er angitt på siden **Warehouse Management-parameter**, er valgfritt hvis en verdi som er etterfulgt av en app-ID, har en fast lengde, eller hvis lengden er maksimert (det vil si hvis lengden er lik **Lengde**-verdien som er angitt for app-ID-en).

## <a name="establish-the-generic-gs1-setup"></a>Opprett det generelle GS1-oppsettet

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

## <a name="set-up-gs1-policies-that-you-can-assign-to-mobile-device-menu-items"></a>Definer GS1-policyer som du kan tilordne til menyelementer for mobilenheter

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
1. Velg **Vare**-feltet, og skann følgende strekkode: *\]C10100000012345678\~3030\~10b1\~17220215*.

På grunn av innstillingene som er fastsatt for dette eksemplet, analyserer systemet den skannede strekkoden på følgende måte.

| Feltnøkkel | App-ID | Verdi | Merk |
|---|---|---|---|
| ItemId | 01 | 00000012345678 | Fordi arbeideren skannet til **Vare**-feltet, tilordnes den første verdien i strekkoden til dette feltet. Tilordningen tas fra det generelle oppsettet for GS1. |
| Antall | 30 | 30 | Fordi flere feltverdier registreres i en enkelt skanning, hentes denne tilordningen og alle gjenværende tilordninger fra GS1-policyen som er tilordnet menyelementet **Innkjøpsmottak**. Denne verdien er antallet som ble mottatt. |
| InventBatchId | 10 | b1 | Denne verdien er parti-ID-en. |
| ExpDate | 17 | 220215 | Datoformatet er ÅÅMMDD. Utløpsdatoen er derfor 15. februar 2022. |

Mottaket registreres deretter, og de relevante databaseverdiene angis etter enkeltskanningen.
