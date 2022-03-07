---
title: Klargjøre miljøet for samarbeid med nettjenestene ID-porten og Altinn
description: Dette emnet forklarer hvordan du klargjør miljøet for samarbeid med nettjenestene ID-porten og Altinn.
author: liza-golub
ms.date: 12/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Norway
ms.author: elgolu
ms.search.validFrom: 2021-11-18
ms.dyn365.ops.version: AX 10.0.22
ms.openlocfilehash: 1a40666261e7908430fba254f8375ece7ea68e46
ms.sourcegitcommit: b1c758ec4abfcf3bf9e50f18c1102d4a9c1316d0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/15/2021
ms.locfileid: "7922376"
---
# <a name="prepare-your-environment-to-interoperate-with-id-porten-and-altinn-web-services"></a>Klargjøre miljøet for samarbeid med nettjenestene ID-porten og Altinn

[!include [banner](../includes/banner.md)]

Når firmaet har [registrert et integreringspunkt](emea-nor-vat-return-integration-point.md) i nettportalen ID-porten. Disse oppgavene forbereder Microsoft Dynamics 365 Finance-miljøet for samarbeid med ID-porten- og Altinn-webtjenester for å sende mva-returer.

- [Importere og sette opp ER-konfigurasjoner](#er-setup)
- [Definere programspesifikke parametere for mva-deklareringsformat](#application-specific-parameters)
- [Importere en pakke med dataenheter som inkluderer et forhåndsdefinert oppsett for elektroniske meldinger (EM)](#em-setup)
- [Angi mva-registreringsnummeret til firmaet som rapporterer en mva-retur](#vat-registration-number)
- [Definere et papirformat for å forhåndsvise mva-returer](#preview-format)
- [Aktiver mva-returrapportering for firmaer som rapporterer som en mva-gruppe i den samme systemdatabasen](#vat-group)
- [Definer en mva-utligningsperiode](#settlement-period)
- [Definere nummerserier for funksjonen Elektroniske meldinger](#number-sequences)
- [Definere dokumentstyringsparametere](#document-management-parameters)
- [Definere et transformasjonsskjema for valideringsresultater](#transformation-schema)
- [Definere sikkerhetsroller for behandling av elektroniske meldinger](#em-security-roles)
- [Definere sikkerhetsroller for samarbeid med webtjenestene ID-porten og Altinn](#web-security-roles)
- [Definere klient-IDen og klienthemmelighet for integreringspunktet for ID-porten i Finance](#client-credentials)
- [Definere internettadressen til webtjenestene ID-porten og Altinn](#internet-address)

Webtjenestene ID-porten og Altinn krever at du bruker TLS (Transport Layer Security) 1.2. Hvis du vil ha mer informasjon om hvordan du aktiverer TLS 1.2, kan du se [Aktivere TLS 1.2](/mem/configmgr/core/plan-design/security/enable-tls-1-2).

## <a name="import-and-set-up-er-configurations"></a><a id="er-setup"></a>Importere og konfigurere ER-konfigurasjoner

Importer følgende ER-konfigurasjoner for å klargjøre Finance til å generere mva-returformater som er gyldige for perioder som starter 1. januar 2022 i Norge, og til å forberede det sammen med webtjenestene ID-porten og Altinn.

| Tall | ER-konfigurasjonsnavn | Type | Beskrivelse |
|---|---|---|---|
| **1** |**Mva-deklareringsmodell** | **Modell** | **En generisk modell for ulike mva-deklareringer.** |
| 2 | Tilordning av mva-deklareringsmodell | Modelltilordning | En generisk modelltilordning for mva-deklareringer. |
| 3 | Mva-deklarasjon XML (NO) | Format (eksport) | En mva-retur i XML-format for innsending til Altinn. |
| 4 | Mva-deklarasjon Excel (NO) | Format (eksport) | En mva-retur i Microsoft Excel-format for forhåndsvisning. |
| 5 | Altinn mva-samhandling (NO) | Format (eksport) | Et format som brukes til å opprette en URL-bane for webtjenestesluttpunktene ID-porten og Altinn. |
| **6** | **Rammeverkmodellen for elektroniske meldinger** | **Modell** |**Modellen for rammeverk for elektroniske meldinger.** |
| 7 | Altinn mva-modelltilordning | Modelltilordning (eksport, import) | Modelltilordning som støtter samarbeid med ID-porten/ og Altinn-webtjenester for Norge. |
| 8 | Altinn mva-autorisasjonsformat (NO) | Format (eksport) | Forespørselsparameterne for autorisasjonskoden, tilgangstoken og bygging av URLene der forespørselen vil bli sendt. |
| 9 | Altinn-mva-import Altinn-tokenformat (NO) | Format (import) | ER-formatet som brukes til å importere tilgangstokenet som mottas fra Altinn-webtjenesten, til databasen. |
| 10 | Format for tilbakemelding om Altinn mva-import (NO) | Format (import) | ER-formatet som brukes til å importere tilbakemeldingsstatusen som mottas fra Altinn-webtjenesten, til databasen. |
| 11 | Altinn-mva-import ID-porten-tokenformat (NO) | Format (import) | ER-formatet som brukes til å importere tilgangstokenet som mottas fra ID-porten-webtjenesten, til databasen. |
| 12 | Altinn mva-importforekomstformat (NO) | Format (import) | ER-formatet som brukes til å importere parameterne for forekomsten som mottas fra Altinn-webtjenesten til databasen. |
| 13 | Resultatformat for Altinn-importvalidering (NO) | Format (import) | ER-formatet som brukes til å importere resultatene for mva-returvalidering som mottas fra Altinn-webtjenesten til databasen. |
| 14 | Format for webforespørselshoder for Altinn mva (NO) | Format (eksport) | Format som brukes til å opprette hoder for HTTPS-forespørselen (Hypertext Transfer Protocol over Secure Sockets Layer). |

Importer de nyeste versjonene av disse konfigurasjonene. Versjonsbeskrivelsen inneholder vanligvis nummeret til Microsoft Knowledge Base-artikkelen (KB) som forklarer endringene som ble introdusert i konfigurasjonsversjonen. Bruk nummeret på KB-artikkelen i [Problemsøkportalen i Microsoft Dynamics Lifecycle Service (LCS)](https://lcs.dynamics.com/v2) for å få mer informasjon om endringene som er innført. Hvis den siste konfigurasjonsversjonen inneholder referanser til objekter som ikke er tilgjengelige i Finance-versjonen, vil importprosessen være låst for denne konfigurasjonsversjonen. I så fall må du importere den nyeste versjonen av konfigurasjonen som er tilgjengelig for Finance-versjonen.

> [!NOTE]
> Når du har importert alle ER-konfigurasjoner fra tabellen ovenfor, kan du angi alternativet **Standard for modelltilordning** til **Ja** for følgende konfigurasjoner:
>
> - **Tilordning av mva-deklareringsmodell** under **Mva-deklareringsmodell**
> - **Altinn mva-modelltilordning** under **Rammeverkmodellen for elektroniske meldinger**

Hvis du vil ha mer informasjon om hvordan du laster ned ER-konfigurasjoner fra det globale Microsoft-repositoriet, kan du se [Laste ned ER-konfigurasjoner fra det Globale repositoriet](../../fin-ops-core/dev-itpro/analytics/er-download-configurations-global-repo.md).

## <a name="set-up-application-specific-parameters-for-the-vat-declaration-format"></a><a id="application-specific-parameters"></a>Definere programspesifikke parametere for mva-deklareringsformat

Formatet som brukes til å rapportere mva-returer til norske skattemyndigheter, krever bestemte verdier fra opplistede lister for enkelte elementer (for eksempel standard avgiftskoder). For å sikre at de obligatoriske verdiene er angitt for disse elementene, må du definere programspesifikke parametere for ER-formatene **Mva-deklarasjon XML (NO)** og **Mva-deklarasjon Excel (NO)** før du begynner å bruke dem. Programspesifikke parametere gjør det enklere å knytte hoveddata fra Finance-miljøet til de opplistede listene med elementer som de norske skattemyndighetene krever for rapporten.

> [!NOTE]
> Vi anbefaler at du aktiverer funksjonen **Bruk programspesifikke parametere fra tidligere versjoner av ER-formater** i arbeidsområdet **Funksjonsbehandling**. Når denne funksjonen er aktivert, blir parametere som er konfigurert for en tidligere versjon av et ER-format, automatisk gjeldende for en senere versjonen av samme format. Hvis denne funksjonen ikke er aktivert, må du uttrykkelig konfigurere programspesifikke parametere for hver formatversjon. Funksjonen **Bruk programspesifikke parametere fra tidligere versjoner av ER-formater** er tilgjangelig i arbeidsområdet **Funksjonsbehandling** fra og med Finance-versjon 10.0.23. Hvis du vil ha mer informasjon om hvordan du definerer parameterne for et ER-format for hver juridiske enhet, kan du se [Definere parameterne for et ER-format per juridisk enhet](../../fin-ops-core/dev-itpro/analytics/er-app-specific-parameters-set-up.md).

Programspesifikke parametere for ER-formatene **Mva-deklarasjon XML (NO)** og **Mva-deklarasjon Excel (NO)** omfatter følgende oppslagsfelt for oppsett.

| Navn på oppslagsfelt | Beskrivelse | Konsekvens |
|---|---|---|
| [NoteForTaxCode_Lookup](#note-for-tax-code) | Kodelisten som brukes til å vise forbindelsen mellom strukturerte merknader og mva-koder i mva-meldingen. | Under kjøringen av rapporten brukes dette oppslagsfeltet til å finne verdien fra den opplistede listen over verdier som den norske skatteetaten krever, basert på hoveddata fra Finance, og til å rapportere den under `<merknad/utvalgtMerknad>` i noden `<mvaSpesifikasjonslinje>`. |
| [VATSpecification_Lookup](#vat-specification) | Kodelisten for ytterligere spesifikasjon av mva. | Under kjøringen av rapporten brukes dette oppslagsfeltet til å finne verdien fra den opplistede listen over verdier som den norske skatteetaten krever, basert på hoveddata fra Finance, og til å rapportere den under `<spesifikasjon>` i noden `<mvaSpesifikasjonslinje>`. |
| [StandardTaxCodes_Lookup](#standard-tax-code) | Mva-koden som er angitt av den norske skatteetaten. | Under kjøringen av rapporten brukes dette oppslagsfeltet til å finne standard mva-kode for mva-koden som brukes i mva-postering i Finance, og til å rapportere den i under `<mvaKode>` i rapporten. |

Følg disse trinnene for å opprette programspesifikke parametere for ER-formatene **Mva-deklarasjon XML (NO)** og **Mva-deklarasjon Excel (NO)**.

1. I arbeidsområdet **Elektronisk rapportering** velger du flisen **Rapporteringskonfigurasjoner**.
2. På siden **Konfigurasjoner** utvider du **Mva-deklareringsmodell** og velger **Mva-deklarasjon (NO)**.
3. På Handling-panelet, i kategorien **Konfigurasjoner**, i gruppen **Programspesifikke parametere**, velg **Oppsett**.
4. På siden **Programspesifikke parametere** velger du den siste versjonen av formatet du vil definere betingelser for.
5. Velg hvert oppslag i hurtigfanen **Oppslag**, og definer passende betingelser for det.
6. I hurtigfanen **Betingelser** definerer du hvilke avgiftskoder eller andre tilgjengelige kriterier som må samsvare med et bestemt oppslagsresultat.

    Hvis betingelser defineres på én linje, bruker systemet vanligvis dem til en kildeavgiftstransaksjon ved hjelp av **AND**-operatoren. Hvis betingelser må brukes ved hjelp av **OR**-operatoren, definerer du dem på separate linjer. Når en avgiftstransaksjon fra rapporteringsperioden oppfyller en betingelse i listen, blir verdien som er angitt i den tilknyttede **Resultat**-kolonnen, rapportert for det relaterte dokumentet. Mer informasjon om oppsettet av hvert oppslagsfelt er angitt senere i dette emnet.

7. Når du er ferdig med å definere betingelser, velger du **Fullført** i **Tilstand**-feltet. Deretter lagrer du konfigurasjonen.

    Du kan enkelt eksportere oppsettet av applikasjonsspesifikke parametere fra én versjon av en rapport og importere det til en annen versjon. Du kan også eksportere oppsettet fra **Mva-deklarasjon XML (NO)** og importere det til **Mva-deklarasjon Excel (NO)**, forutsatt at begge rapportene har samme struktur for oppslagsfelt.

### <a name="note-for-tax-code-notefortaxcode_lookup"></a><a id="note-for-tax-code"></a>Merknad for mva-kode (NoteForTaxCode_Lookup)

`<merknad>`-merket er et valgfritt merke under `<mvaSpesifikasjonslinje>`-noden. I enkelte scenarier kan imidlertid norske skattemyndigheter kreve rapportering av dette merket. Hvis du vil rapportere dette merke fra Finance-miljøet, aktiverer du funksjonen [Aktiver utvidet støtte for finansårsakskoder](emea-financial-reason.md) i arbeidsområdet for **Funksjonsbehandling**. 

1. Gå til **Arbeidsområder** \> **Funksjonsbehandling**.
2. I kategorien **Alle** finner du og velger du funksjonen **Aktiver utvidet støtte for finansårsakskode** i listen.
3. Velg **Aktiver nå**.

![Aktiver funksjonen Aktiver utvidet støtte for finansårsakskode i arbeidsområdet for Funksjonsbehandling.](media/emea-nor-vat-return-fin-reason.png)

Når funksjonen er aktivert i Finance-miljøet, vil avgiftstransaksjoner som posteres i systemet, inneholde en økonomisk årsakskode og en kommentar fra de opprinnelige dokumentene. Du kan deretter rapportere `<merknad>`-merket under `<mvaSpesifikasjonslinje>`-noden i mva-returen. Bruk **NoteForTaxCode_Lookup** til å knytte hoveddata fra Finance-miljøet til den opplistede listen over verdier som norske skattemyndigheter krever. For dette oppslagsfeltet er følgende hoveddatakilder tilgjengelige for oppsett:

- **Mva-kode** – Mva-koden.
- **Avgiftsklasse** – En nummerert liste med verdier som representerer ulike kombinasjoner av mva-transaksjonsretninger og kreditnotakriterier i Finans. Hvis du vil ha mer informasjon om hvordan mva-klassifikatoren beregnes for en avgiftstransaksjon, kan du se [Detaljert beskrivelse av klassifikatoren for mva-transaksjoner](#tax-transaction-classifier).
- **Årsak** – Årsaken består av finansielle årsakskoder som er definert i Finance-miljøet, og brukes i avgiftstransaksjoner som posteres i systemet. Hvis du vil definere finansielle årsakskoder, kan du gå til **Organisasjonsstyring** > **Oppsett** > **Finansårsaker**.

Definer betingelser fra det gjeldende firmaets hoveddatakilder for å finne ut hvilken verdi fra den opplistede listen med verdier som norske skattemyndigheter krever, som må rapporteres for den tilhørende kombinasjonen av hoveddata fra Finance-miljøet.

Tabellen nedenfor viser oppslagsresultatene for **NoteForTaxCode_Lookup**.

| Oppslagsresultat (Norsk) | Oppslagsresultat (Engelsk) |
|---|---|
| periodisering | Avsetning |
| feil mva-kode brukt tidligere | Feil mva-kode som tidligere er brukt |
| feil i regnskapsprogram | Feil i regnskapsprogramvaren |
| omsetning før registrering | Omsetning før registrering |
| omberegning/retur | Omberegning/retur | 
| midlertidig innførsel | Midlertidig import |
| gjeninnførsel | Ny import |
| tolldeklarasjon på feil organisasjonsnummer | Tolldeklarering på feil organisasjonsnummer |
| gjenutførsel | Eksporter på nytt |
| gjenutførsel eller retur | Gjenutførsel eller retur |
| midlertidig utførsel | Midlertidig eksport |
| tjenesteeksport | Tjenesteeksporter |
| butikkanskaffelser| Store innkjøp |
| anskaffelser foretatt før mva-plikt | Innkjøp foretatt før mva-plikt |
| forsikringsoppgjør| Forsikringsoppgjør |
| sesongvariasjon | Sesongvariasjon |
| kreditnota | Kreditnota |
| Annet | Annet |

> [!IMPORTANT]
> Det er viktig at du legger til **Annet** (**Annet**), som må samle inn data fra andre tilfeller som den siste varen i listen. **Linjeverdien** må være den siste verdien i tabellen. I alle de andre kolonnene velger du **\*Ikke tom\***. Siden **Årsak** ikke er et obligatorisk felt i avgiftstransaksjoner, legger du til en linje med oppslagsresultatverdien **Annet** (**Annet**), **\*Tom\*** i **Årsak**-kolonnen, og **\*Ikke tom\*** i alle de andre kolonnene.

Hvis du velger en økonomisk årsakskode for et dokument som ikke er tilknyttet et oppslagsresultat fra den forrige tabellen (dette betyr at **Annet**-verdi vil bli brukt), kan ikke systemet rapportere denne årsaken som én av verdiene fra listen som er listet opp, som den norske skatteetaten krever. I dette tilfellet rapporteres årsakskoden og kommentaren i `<merknad/beskrivelse>`-koden under `<mvaSpesifikasjonslinje>`-noden, og kommentaren rapporteres \"som den er\" i det relaterte **Årsakskommentar**-feltet i det opprinnelige dokumentet

#### <a name="detailed-description-of-the-tax-transaction-classifier"></a><a id="tax-transaction-classifier"></a>Detaljert beskrivelse av klassifikatoren for mva-transaksjoner

Klassifikatoren for avgiftstransaksjonen knyttes til retningen for avgiftstransaksjonen og kreditnota-IDen. Følgende tabell gir en definisjon av denne klassifikatoren.

| Klassifikatorverdi | Betingelse |
|---|---|
| PurchaseCreditNote | <ul><li>Kreditnota</li><li>Mva-retning = Innkommende merverdiavgift</li></ul> |
| Kjøp | <ul><li>Ikke kreditnota</li><li>Mva-retning = Innkommende merverdiavgift</li></ul> |
| SalesCreditNote | <ul><li>Kreditnota</li><li>Mva-retning = Konto, utgående mva</li></ul> |
| Salg | <ul><li>Ikke kreditnota</li><li>Mva-retning = Konto, utgående mva</li></ul> |
| PurchaseExemptCreditNote | <ul><li>Kreditnota</li><li>Avgiftsretning = Avgiftsfritt kjøp</li></ul> |
| PurchaseExempt | <ul><li>Ikke kreditnota</li><li>Avgiftsretning = Avgiftsfritt kjøp</li></ul> |
| SalesExemptCreditNote | <ul><li>Kreditnota</li><li>Avgiftsretning = Avgiftsfritt salg</li></ul> |
| SaleExempt | <ul><li>Ikke kreditnota</li><li>Avgiftsretning = Avgiftsfritt salg</li></ul> |
| UseTaxCreditNote | <ul><li>Kreditnota</li><li>Mva-retning = Bruk avgift</li></ul> |
| UseTax | <ul><li>Ikke kreditnota</li><li>Mva-retning = Bruk avgift</li></ul> |
| PurchaseReverseChargeCreditNote | <ul><li>Kreditnota</li><li>Mva-retning = Innkommende merverdiavgift</li><li>ReverseCharge\_W = Ja</li></ul> |
| PurchaseReverseCharge | <ul><li>Ikke kreditnota</li><li>Mva-retning = Innkommende merverdiavgift</li><li>ReverseCharge\_W = Ja</li></ul> |
| SalesReverseChargeCreditNote | <ul><li>Kreditnota</li><li>Mva-retning = Konto, utgående mva</li><li>ReverseCharge\_W = Ja</li></ul> |
| SalesReverseCharge | <ul><li>Ikke kreditnota</li><li>Mva-retning = Konto, utgående mva</li><li>ReverseCharge\_W = Ja</li></ul> |

### <a name="vat-specification-vatspecification_lookup"></a><a id="vat-specification"></a>Mva-spesifikasjon (VATSpecification_Lookup)

For dette oppslagsfeltet er følgende hoveddatakilder tilgjengelige for oppsett:

- **Mva-kode** – Mva-koden.
- **Avgiftsklasse** – En nummerert liste med verdier som representerer ulike kombinasjoner av mva-transaksjonsretninger og kreditnotakriterier i Finans. Hvis du vil ha mer informasjon om hvordan mva-klassifikatoren beregnes for en avgiftstransaksjon, kan du se [Detaljert beskrivelse av klassifikatoren for mva-transaksjoner](#tax-transaction-classifier).
- **Varens mva-gruppe** – Varens mva-gruppe.
- **Mva-gruppe** – Mva-gruppen.

Definer betingelsene fra det gjeldende firmaets hoveddatakilder for å finne ut hvilken verdi fra den opplistede listen med verdier som norske skattemyndigheter krever, som må rapporteres i `<spesifikasjon>`-koden under `<mvaSpesifikasjonslinje>`-noden for den tilhørende kombinasjonen av hoveddata fra Finance-miljøet.

Tabellen nedenfor viser oppslagsresultatene for **VATSpecification_Lookup**.

| Oppslagsresultat (Norsk) | Oppslagsresultat (Engelsk) |
|---|---|
| justering | Justering |
| trykk på krav | Tap på krav |
| tilbakeføringAvInngåendeMerverdiavgift | Tilbakeføring av inngående mva |
| uttak | Uttak |
| varer | Varer |
| tjenester | Tjeneste |
| Annet | Annet |

> [!IMPORTANT]
> Det er viktig at du legger til **Annet** (**Annet**), som må samle inn data fra andre tilfeller som den siste varen i listen. **Linjeverdien** må være den siste verdien i tabellen. I alle de andre kolonnene velger du **\*Ikke tom\***. Fordi i noen tilfeller kan feltene for **varens mva-gruppe** og **merverdiavgiftsgruppe** være tomme i avgiftstransaksjoner, legg til en linje til med oppslagsresultatverdien **Annet** (**Annet**), **\*Tomt\*** i kolonnene **Varens mva-gruppe** og **Merverdiavgiftsgruppe** og **\*Ikke tomt\*** i alle de andre kolonnene.

> [!IMPORTANT]
> Verdier fra opplistingsliste *Spesifikasjon* av verdier må bare brukes med bestemte *Standard avgiftskoder*. Sørg for at **VATSpecification_Lookup** er kompatibelt med gjeldende regler som defineres av norske skattemyndigheter som følger med i dokumentasjonen til [Informasjonsmodeller, XSD og koding](https://skatteetaten.github.io/mva-meldingen/english/informasjonsmodell/#encoding).

### <a name="standard-tax-codes-standardtaxcodes_lookup"></a><a id="standard-tax-code"></a>Standard mva-koder (StandardTaxCodes_Lookup)

For dette oppslagsfeltet er følgende hoveddatakilder tilgjengelige for oppsett:

- **Mva-kode** – Mva-koden.
- **Avgiftsklasse** – En nummerert liste med verdier som representerer ulike kombinasjoner av mva-transaksjonsretninger og kreditnotakriterier i Finans. Hvis du vil ha mer informasjon om hvordan mva-klassifikatoren beregnes for en avgiftstransaksjon, kan du se [Detaljert beskrivelse av klassifikatoren for mva-transaksjoner](#tax-transaction-classifier).

Definer betingelsene fra det gjeldende firmaets hoveddatakilder for å finne ut hvilken verdi fra den opplistede listen med verdier som norske skattemyndigheter krever, som må rapporteres i `mvaKode`-koden under `mvaSpesifikasjonslinje`-noden for de tilhørende kombinasjonene av hoveddata fra Finance-miljøet.

Tabellen nedenfor viser oppslagsresultatene for **StandardTaxCodes_Lookup**.

| Oppslagsresultater | Beskrivelse (norsk) | Beskrivelse (engelsk) |
|---|---|---|
| 1 | Fradragsberettiget innenlands inngående merverdiavgift, 25% | Fradragsberettiget innenlands inngående mva, 25 % |
| 11 | Fradragsberettiget innenlands inngående merverdiavgift, 15 % | Fradragsberettiget innenlands inngående mva, 15 % |
| 12 | Fradragsberettiget innenlands inngående merverdiavgift, 11,11% | Fradragsberettiget innenlands inngående mva, 11.11 % |
| 13 | Fradragsberettiget innenlands inngående merverdiavgift, 12% | Fradragsberettiget innenlands inngående mva, 12 % |
| 14 | Fradragsberettiget innførselsmerverdiavgift, 25% | Fradragsberettiget inngående mva (betalt ved import), 25 % |
| sept. | Fradragsberettiget innførselsmerverdiavgift, 15% | Fradragsberettiget inngående mva (betalt ved import), 15 % |
| 3 | Utgående merverdiavgift, 25 % | Utgående mva, 25 % |
| 31 | Utgående merverdiavgift, 15 % | Utgående mva, 15 % |
| 32 | Utgående merverdiavgift, 11,11 % | Utgående mva, 11.11 % |
| 33 | Utgående merverdiavgift, 12 % | Utgående mva, 12 % |
| 5 | Innenlands omsetning og uttak fritatt for merverdiavgift | Innenlands salg og uttak fritatt mva |
| 51 | Innenlandsk omsetning med omvendt avgiftplikt | Innenlands omsetning med snudd avregning |
| 52 | Utførsel av varer og tjenester | Eksport av varer og tjenester |
| 6 | Omsetning utenfor merverdiavgiftsloven | Omsetning utenfor mva-loven |
| 81 | Grunnlag innførsel av varer med fradragsrett for innførselsmerverdiavgift, 25% | Basis for import av varer med rett til fradrag av innførselsavgift, 25% |
| 82 | Grunnlag innførsel av varer uten fradragsrett for innførselsmerverdiavgift, 25% | Basis for import av varer uten rett til fradrag av innførselsavgift, 25% |
| 83 | Grunnlag innførsel av varer med fradragsrett for innførselsmerverdiavgift, 15% | Basis for import av varer med rett til fradrag av innførselsavgift, 15% |
| 84 | Grunnlag innførsel av varer uten fradragsrett for innførselsmerverdiavgift, 15% | Basis for import av varer uten rett til fradrag av innførselsavgift, 15% |
| 85 | Grunnlag innførsel av varer som det ikke skal beregnes merverdiavgift av | Grunnlag for import av varer som merverdiavgift ikke skal beregnes fra |
| 86 | Tjenester kjøpt fra utlandet med fradragsrett for merverdiavgift, 25 % | Tjenester kjøpt fra utlandet med rett til fradrag av mva, 25 % |
| 87 | Tjenester kjøpt fra utlandet uten fradragsrett for merverdiavgift, 25 % | Tjenester kjøpt fra utenlandet uten rett til å trekke fra merverdiavgift, 25 % |
| 88 | Tjenester kjøpt fra utlandet med fradragsrett for merverdiavgift, 12 % | Tjenester kjøpt fra utlandet med rett til fradrag av mva, 12 % |
| 89 | Tjenester kjøpt fra utlandet uten fradragsrett for merverdiavgift, 12 % | Tjenester kjøpt fra utenlandet uten rett til å trekke fra merverdiavgift, 12 % |
| 91 | Kjøp av klimakvoter eller gull med fradragsrett for merverdiavgift, 25 % | Kjøp av handelsvirksomhet eller gull med rett til å trekke fra merverdiavgift, 25 % 
| 92 | Kjøp av klimakvoter eller gull uten fradragsrett for merverdiavgift, 25 % | Kjøp av handelsvirksomhet eller gull uten rett til å trekke fra merverdiavgift, 25 % |

> [!IMPORTANT]
> Det er viktig at du definerer betingelser for alle mva-koder som brukes i avgiftstransaksjoner i løpet av rapporteringsperioden. Hvis det ikke er definert et passende oppslagsresultat for en mva-kode som brukes i transaksjoner i løpet av rapporteringsperioden, stoppes genereringen av en mva-retur. 

## <a name="import-a-package-of-data-entities-that-includes-a-predefined-em-setup"></a><a id="em-setup"></a>Importere en pakke med dataenheter som inkluderer et forhåndsdefinert EM-oppsett

Prosessen med å konfigurere EM-funksjonaliteten for mva-returer med direkte innsending til Altinn har mange trinn. Fordi navnene på noen forhåndsdefinerte enheter brukes i ER-konfigurasjonene, er det viktig at du bruker et sett med forhåndsdefinerte verdier som leveres i en pakke med dataenheter for de relaterte tabellene. Noen poster i dataenhetene inneholder en kobling til ER-konfigurasjoner. Før du begynner å importere dataenhetene, importerer du ER-konfigurasjoner til Finance.

1. I [LCS](https://lcs.dynamics.com/v2) går du til **Delt aktivabibliotek** og velger **Datapakke** som aktivatype. 
2. I listen over datapakkefiler finner du **NO mva-tilbakebetaling – Altinn**, og laster den ned til datamaskinen.
3. I Finance velger du firmaet du vil samhandle med Altinn fra, og deretter går du til **Arbeidsområder** \> **Databehandling**.
4. Før du importerer oppsettdata fra dataenhetene, må du kontrollere at dataenhetene i programmet oppdateres og synkroniseres. I **Databehandling**-arbeidsområdet går du til **Rammeverkparametere** \> **Enhetsinnstillinger**, og deretter velger du **Oppdater enhetsliste**. Vent på bekreftelse på at oppdateringen er fullført. Hvis du vil ha mer informasjon om hvordan du oppdaterer enhetslisten, kan du se [Oppdatering av enhetsliste](../../fin-ops-core/dev-itpro/data-entities/data-entities.md#entity-list-refresh).
5. Bekreft at kildedataene og måldataene er riktig tilordnet. For mer informasjon, se [Bekreft at kildedataene og måldataene er kartlagt riktig](../../fin-ops-core/dev-itpro/data-entities/data-import-export-job.md#validate-that-the-source-data-and-target-data-are-mapped-correctly).
6. I arbeidsområdet **Databehandling** velger du **Importer**, og deretter, på hurtigfanen **Importer** angir du feltet **Gruppenavn**.
7. På **Valgte enheter**-hurtigfanen velger du **Legg til fil**.
8. Velg **Pakke** i feltet **Kildedataformat**, og velg deretter **Last opp og legg til**. 
9. Finn og velg **NO mva-retur – Altinn**-oppsettfilen du tidligere lastet ned.
10. Vent til dataenhetene fra filen vises i rutenettet i hurtigfanen **Valgte enheter**, og velg deretter **Lukk**.
11. Før dataenhetene brukes for første gang til å importere data fra pakken, må du synkronisere tilordningen av kildedataene og måldataene. Velg en dataenhet i listen for pakken, og velg deretter **Endre måltilordning** i handlingsruten. 
12. Over rutenettet for pakken velger du **Generer tilordning** for å opprette en tilordning fra begynnelsen. Deretter lagrer du tilordningen.
13. Gjenta trinn 11 og 12 for hver dataenhet i pakken før du starter importen.
14. Nå kan du importere data fra **NO mva-tilbakebetaling – Altinn**-oppsettfilen til det valgte firmaet. Velg **Importer** i handlingsruten for å starte importen.

    ![Importer en pakke med dataenheter som inkluderer et forhåndsdefinert EM-oppsett.](media/emea-nor-vat-return-importem-setup.png)

    Hvis du vil ha mer informasjon, kan du se [Oversikt over databehandling](../../fin-ops-core/dev-itpro/data-entities/data-entities-data-packages.md).

    Hvis du vil ha mer informasjon om det forhåndsdefinerte oppsettet som er inkludert i dataenhetene i pakken for **NO mva-retur med direkte innsending til Altinn**-funksjonen, kan du se [Kontrolliste for oppsett av elektroniske meldinger for mva-returer med direkte innsending til Altinn](emea-nor-vat-return-checklist.md).

## <a name="set-up-the-vat-registration-number-of-the-company-that-is-reporting-a-vat-return"></a><a id="vat-registration-number"></a>Angi mva-registreringsnummeret til firmaet som rapporterer en mva-retur

**NO mva-tilbakebetaling – Altinn**-oppsettfilen angir tilleggsfeltet **Avgiftsregistreringsnummer** for **NO mva-tilbakebetaling** EM-behandling. Dette feltet aktiverer et mva-registreringsnummer som er uavhengig av den juridiske enhetens hovedadresse og registrerings-ID som defineres for firmaet som må rapportere mva-returer ved å bruke funksjonen for **NO mva-tilbakebetaling med direkte innsending til Altinn** i Finance. Juridiske enheter som har flere mva-registreringer, kan derfor enkelt sende inn mva-returene som er spesifikke for mva-registreringen i Norge. Hvis du vil ha mer informasjon om om hvordan du støtter arkivering for flere mva-registreringer, kan du se [Flere mva-registreringsnumre](emea-multiple-vat-registration-numbers.md).

Følg denne fremgangsmåten for å definere mva-registreringsnummeret som funksjonen for **NO mva-tilbakebetaling med direkte innsending til Altinn**-funksjonen i Finance må bruke til å sende mva-returer.

1. Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Behandling av elektronisk melding**, og velg **NO mva-tilbakebetaling**-behandling.
2. Definer mva-registreringsnummeret som skal brukes til å sende mva-retur til Altinn, i hurtigfanen **Tilleggsfelt for melding** i feltet **Avgiftsregistreringsnummer**.
3. Lagre endringene.

    ![Angi mva-registreringsnummeret til firmaet som rapporterer en mva-retur.](media/emea-nor-vat-return-tax-registration-number.png)

Hvis mva-registreringsnummeret ikke er angitt i tilleggsfeltet **Avgiftsregistreringsnummer** i behandlingen **NO mva-retur**, henter systemet det fra registrerings-IDen som er definert i egenskapene til den juridiske enheten som er knyttet til registreringskategorien for **mva-ID**. Hvis du vil ha mer informasjon, kan du se [Registreringstype](emea-registration-ids.md#registration-type-creation) og [Registreringskategori](emea-registration-ids.md#supported-registration-categories).

## <a name="set-up-a-paper-format-to-preview-vat-returns"></a><a id="preview-format"></a>Definere et papirformat for å forhåndsvise mva-returer

Du kan generere en mva-retur i Excel-format for å forhåndsvise mva-beløp i løpet av perioden. Følg disse trinnene for å aktivere denne muligheten.

1. Gå til **Arbeidsområder** \> **Funksjonsbehandling**.
2. I kategorien **Alle** finner du og velger du funksjonen **Rapporter i mva-oppgaveformat** i listen.
3. Velg **Aktiver nå**.
4. Gå til **Avgift** \> **Oppsett** \> **Parametere for økonomimodul**.
5. Velg **Mva-deklarering Excel (NO)** i feltet **Tilordning av format for mva-oppgave** i delen **Mva-alternativer** i fanen **Mva**.
6. Gå til **Avgift** \> **Indirekte avgifter** \> **Merverdiavgift** \> **Skattemyndigheter**. 
7. Velg skattemyndigheten som er knyttet til utligningsperioden for merverdiavgift som du rapporterer mva-returer for Norge.
8. Velg **Standard** i feltet **Rapportoppsett**.
9. Lagre endringene.

Hvis du vil generere en mva-retur i Excel-format, kan du gå til **Mva** \> **Deklareringer** \> **Utgående merverdiavgift** \> **Rapporter merverdiavgift for utligningsperioden**. Hvis du vil generere en mva-retur for å forhåndsvise mva-beløp for en valgt betalingstransaksjon for mva, kan du gå til **Mva** \> **Forespørsler og rapporter** \> **Merverdiavgiftforespørsler** \> **Mva-betalinger** og deretter velge **Skriv ut rapport** i handlingsruten.

## <a name="enable-vat-return-reporting-for-companies-that-report-as-a-vat-group-in-the-same-system-database"></a><a id="vat-group"></a>Aktiver mva-returrapportering for firmaer som rapporterer som en mva-gruppe i den samme systemdatabasen

> [!NOTE]
> Denne delen av oppsettet for **NO mva-tilbakebetaling med direkte innsending til Altinn**-funksjonen kreves bare for firmaer som rapporterer som mva-gruppe i den samme systemdatabasen.

Hvis du vil klargjøre Finance for å rapportere en mva-retur for en mva-gruppe, må du kontrollere at forretningsprosessene og systemoppsettet oppfyller følgende betingelser:

- Skatteinformasjon fra alle datterselskapene registreres i samme system (i dette tilfellet Finance).
- Systemet gjenspeiler alle avgiftstransaksjonene riktig i henhold til reglene og prinsippene for Norge.
- Utligningsperioder for alle juridiske enheter som er involvert i mva-gruppen, er identisk definert.
- Jobben **Utlign og poster merverdiavgift** fullføres i hver juridiske enhet for datterselskap.
- Programspesifikke parametere for mva-returformat defineres for hver juridiske enhet for datterselskapet. Oppsettkonfigurasjonene fullføres for både **Mva-deklarasjon XML (NO)**-formatet og **Mva-deklarasjon Excel (NO)**-formatet.
- En mva-retur i Excel-format genereres riktig i hver juridiske enhet for datterselskap.
- Én juridisk enhet er definert for samarbeid med Altinn i henhold til informasjonen i dette emnet.
- Mva-utligningsperioder for handlingen **NO MVA Samle inn mva-betaling** er definert for hver juridiske enhet for datterselskap.

Hvis du vil aktivere Finance til å rapportere mva-retur fra flere juridiske enheter i den samme systemdatabasen, må du aktivere funksjonen **Spørringer på tvers av firmaer for Handlinger for fyll ut poster** i arbeidsområdet **Funksjonsbehandling**. 

1. Gå til **Arbeidsområder** \> **Funksjonsbehandling**.
2. I fanen **Alle** søk etter og velg funksjonen **Spørringer på tvers av firmaer for Handlinger for Fyll ut poster i listen** i listen.
3. Velg **Aktiver nå**. 

## <a name="define-a-sales-tax-settlement-period"></a><a id="settlement-period"></a>Definere en mva-utligningsperiode

Elektronisk meldingsbehandling som er definert for **NO mva-tilbakebetaling - Altinn**-oppsettpakken, har ingen avhengigheter fra primæradressen til den juridiske enheten. Derfor kan pakken implementeres i en hvilken som helst juridisk enhet i Finance.

Ved **NO mva-tilbakebetaling** kan du samle inn betalingstransaksjoner for merverdiavgift i den juridiske enheten. Du kan deretter generere en mva-retur i XML- eller Excel-format. Innsamlingen av mva-betalingstransaksjoner implementeres ved hjelp av handlingen **NO MVA Samle inn mva-betalinger** av typen **Fyll ut poster**. Hvis du vil hente inn betalingstransaksjoner for mva på riktig måte, må du definere en utligningsperiode for handlingen **NO MVA Samle inn mva-betalinger**.

1. Gå til **Avgift** \> **Oppsett** \> **Elektroniske meldinger** \> **Fyller ut poster**, og velg **NO MVA Samle inn mva-betaling**.
2. I hurtigfanen **Oppsett av datakilder** velger du **NO mva-tilbakebetaling**, og deretter velger du **Rediger spørring**.
3. I raden for tabellen **Mva-betalinger** i feltet **Utligningsperiode** definerer du mva-utligningsperiode som er knyttet til mva-transaksjonene fra den valgte juridiske enheten som må rapporteres til Altinn.

    ![Definer en mva-utligningsperiode.](media/emea-nor-vat-return-settlement-period.png)

    Hvis du ikke angir **Utligningsperiode**, blir alle mva-transaksjoner fra den valgte juridiske enheten tatt hensyn til ved rapportering.

Hvis firmaet må rapportere en mva-innbetaling som en mva-gruppe, må du kontrollere at alle betingelsene som er beskrevet i [Aktiver mva-returrapportering for firmaer som rapporterer som en mva-gruppe i den samme systemdatabasen](#vat-group), er oppfylt. Følg deretter denne fremgangsmåten for å definere utligningsperioden for merverdiavgift for alle juridiske enheter som er inkludert i mva-gruppen.

1. Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Fyll ut poster**.

    På siden **Fyll ut poster** inkluderer rutenettet på hurtigfanen **Oppsett av datakilder** et **Firma**-felt. For eksisterende poster som ble opprettet under det generelle oppsettet for **NO mva-tilbakebetaling med direkte innsending til Altinn**, viser dette feltet IDen til den gjeldende juridiske enheten. Det forutsettes at utligningsperioden for den gjeldende juridiske enheten ble satt opp under det generelle oppsettet for funksjonen **NO mva-tilbakebetaling med direkte innsending til Altinn**.

2. I hurtigfanen **Oppsett av datakilder** i rutenettet legger du til en linje for hver juridiske enhet for datterselskap som må inkluderes i rapportering for mva-gruppen. For hver nye linje angir du feltene nedenfor.

    | Feltnavn | Verdi |
    |---|---|
    | Navn | Angi en tekstverdi som vil hjelpe deg med å forstå hvor denne posten kommer fra. Du kan for eksempel angi **NO Mva-betaling for datterselskap 1**. |
    | Type meldingselement | Velg **Mva-retur**. Denne verdien er den eneste verdien som er tilgjengelig for alle postene. |
    | Kontotype | Velg **Alle**. |
    | Navn på hovedtabell | Angi **TaxReportVoucher** for alle postene. |
    | Feltet Dokumentnummer | Angi **Bilag** for alle postene. |
    | Feltet Dokumentdato | Angi **TransDate** for alle postene. |
    | Feltet Dokumentkonto | Angi **TaxPeriod** for alle postene. |
    | Selskap | Velg IDen for den juridiske enheten for datterselskap. |
    | Brukerspørring | Denne boksen blir automatisk merket når du definerer kriterier ved å velge **Rediger spørring**. |

3. For hver nye linje velger du **Rediger spørring** og angir en tilknyttet utligningsperiode for den juridiske enheten som er angitt i **Firma**-feltet i linjen.

![Definere en mva-utligningsperiode for en mva-gruppe.](media/emea-nor-vat-return-settlement-period-vat-group.png)

Hvis du vil ha mer informasjon om hvordan du fyller ut poster fra flere firmaer i EM, kan du se [Fylle ut poster fra flere firmaer](../general-ledger/electronic-messaging-setup.md#multiple-companies-populate).

## <a name="set-up-number-sequences-for-electronic-messages-functionality"></a><a id="number-sequences"></a>Definere nummerserier for funksjonen Elektroniske meldinger

Hvis du vil arbeide med funksjonaliteten for elektroniske meldinger, må du definere de relaterte nummerseriene.

1. Gå til **Avgift** \> **Oppsett** \> **Parametere for økonomimodul**.
2. På **Nummerserier**-fanen oppretter du to nye nummerserier:

    - Melding
    - Meldingselement

## <a name="set-up-document-management-parameters"></a><a id="document-management-parameters"></a>Definere dokumentstyringsparametere

Før du sender en mva-innbetaling til Altinn, må du kontrollere at følgende filtyper er definert i kategorien **Filtyper** på siden **Dokumentbehandlingsparametere** (**Organisasjonsadministrasjon** \> **Dokumentbehandling** \> **dokumentbehandlingsparametere**):

- **XML** – eXtensible Markup Language
- **XLS** – Microsoft Excel-regneark
- **XLSX** – Microsoft Office Excel 2007-regneark
- **XSLT** – eXtensible Stylesheet Language Transformations
- **JSON** – JavaScript Object Notation
 
Hvis noen av disse filtypene er definert i kategorien **Filtyper**, legger du dem til.

## <a name="set-up-a-validation-results-transformation-schema"></a><a id="transformation-schema"></a>Definere et transformasjonsskjema for valideringsresultater

Webtjenesten for skatteadministrasjon validerer mva-innbetalinger. Denne webtjenesten sender deretter valideringsresultatene i XML-format. For å gjøre det enklere for brukere å lese og analysere valideringsresultatene, kan du laste ned og bruke en XSLT-transformasjon (Extensible Stylesheet Language Transformations).

1. I [LCS](https://lcs.dynamics.com/v2) går du til **Delt aktivabibliotek** og velger **Datapakke** som aktivatype. 
2. I listen over datapakkefiler finner du **NO MVA-valideringsresutatkonverterer** og laster den ned til datamaskinen. Filnavnet er **NO MVA-valideringsresultatkonverterer.zip**.
3. Ikke arkiver filen `NO VAT validation result converter.zip` for å hente `NO VAT validation result converter.xslt`-filen.
4. Gå til **Avgift** \> **Oppsett** \> **Elektroniske meldinger** \> **Handlinger for meldingsbehandling**, og velg **NO VAT Importer valideringssvarhandling**.
5. Velg **Vedlegg**.
6. På siden **Vedlegg for handlingsmelding - Handling: NO VAT Importer valideringssvar**, i handlingsruten, velger du **Ny** \> **Fil**.
7. Velg filen `NO VAT validation result converter.xslt` som du fjernet fra arkivet i trinn 3.
8. Gjenta trinn 3 til 6 for handlingen **NO MVA Importer endelig valideringsresultat**.

Systemet bruker automatisk den tilknyttede XSLT-filen til valideringsresultater fra ID-porten. Deretter kan du se gjennom resultatene i HTML-format i en webleser.

## <a name="set-up-security-roles-for-electronic-message-processing"></a><a id="em-security-roles"></a>Definere sikkerhetsroller for behandling av elektroniske meldinger

Forskjellige grupper av brukere kan kreve tilgang til forskjellig elektronisk meldingsbehandling. Du kan begrense tilgangen til hver type behandling basert på sikkerhetsgrupper som er definert i systemet.

Følg denne fremgangsmåten for å definere hvilke sikkerhetsroller som har tilgang til **NO mva-tilbakebetaling**.

1. Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Behandling av elektronisk melding**.
2. Velg **NO mva-tilbakebetaling**, og legg til sikkerhetsgruppene som må arbeide med denne behandlingen. 

Hvis sikkerhetsroller ikke er definert for elektronisk meldingsbehandling, kan bare en systemadministrator vise den elektroniske meldingsbehandlingen ved å gå til **Avgift** \> **Forespørsler og rapporter** \> **Elektroniske meldinger** \> **Elektroniske meldinger**.

## <a name="set-up-security-roles-for-interoperation-with-id-porten-and-altinn-web-services"></a><a id="web-security-roles"></a>Definere sikkerhetsroller for samhandling med webtjenestene ID-porten og Altinn

Når et tilgangstoken for ID-porten og Altinn hentes, lagres den i systemdatabasen i kryptert format. Tilgangstokenet må brukes hver gang en forespørsel av en hvilken som helst type blir sendt til ID-porten eller Altinn. Av sikkerhetsårsaker må tilgang til tilgangstokenet begrenses til sikkerhetsgruppene som sender forespørsler. Hvis en bruker som ikke er i noen av disse sikkerhetsgruppene, prøver å sende en forespørsel til Altinn, varsler en melding dem om at de ikke har tillatelse til å bruke det valgte webprogrammet for samarbeid.

Følg denne fremgangsmåten for å definere sikkerhetsgrupper som må ha tilgang til tilgangstokener for ID-porten eller Altinn.

1. Gå til **Mva** \> **Oppsett** \> **Elektroniske meldinger** \> **Webprogrammer**.
2. Velg webprogrammet (**ID-porten** eller **Altinn**) du vil definere sikkerhetsgrupper for.
3. I hurtigfanen **Sikkerhetsroller** legger du til sikkerhetsgruppene som må kunne sende forespørsler til enten ID-porten eller Altinn (avhengig av webprogrammet du valgte i trinn 2).

Hvis sikkerhetsroller ikke er definert for et webprogram, kan bare en systemansvarlig samhandle via dette webprogrammet.

## <a name="set-up-the-client-id-and-client-secret-of-your-id-porten-integration-point-in-finance"></a><a id="client-credentials"></a>Definere klient-IDen og klienthemmelighet for integreringspunktet for ID-porten i Finance

Når du [registrerer et integreringspunkt i webportalen ID-porten](emea-nor-vat-return-integration-point.md), bør du trygt lagre klient-IDen og klienthemmeligheten som vil bli brukt til direkte innsending til Altinn fra Finance. I fremgangsmåten nedenfor kopierer du klient-IDen og klienthemmeligheten for integreringspunktet i ID-porten og limer dem inn i Finance.

1. Gå til **Avgift** \> **Oppsett** \> **Elektroniske meldinger** \> **Webprogrammer**, og velg webprogrammet **NO ID-Porten** i listen til venstre.
2. I **Klient-ID**-feltet limer du inn klient-IDen og integreringspunktet for ID-porten.
3. I **Klienthemmelighet**-feltet limer du inn klienthemmeligheten for integreringspunktet i ID-porten.
4. Lagre endringene.

## <a name="set-up-the-internet-address-of-id-porten-and-altinn-web-services"></a><a id="internet-address"></a>Definere internettadressen til webtjenestene for ID-porten og Altinn

Internett-adresser (URL) kan endres av norske skattemyndigheter. Vi anbefaler at du ser etter faktiske URL-adresser på det offisielle Altinn- og ID-porten-webområdet. 

Følg denne fremgangsmåten for å konfigurere URL som brukes i ID-porten.

1. Gå til **Avgift** \> **Oppsett** \> **Parametere** \> **Elektroniske meldinger** \> **Webprogrammer**, og velg webprogrammet **NO ID-Porten** i listen til venstre.
2. I feltet **Base-URL** angir du en av følgende nettadresser:

    - `https://oidc-ver2.difi.no/idporten-oidc-provider` for å fungere sammen med *sandkasseendepunktet* for ID-porten
    - `https://oidc.difi.no/idporten-oidc-provider/` å interoperatisere med *produksjonsendepunktet* for ID-porten

    > [!IMPORTANT]
    > For faktiske Internett-adresser går du til <https://docs.digdir.no/oidc_func_wellknown.html>.

3. I feltet **URL-bane til autorisasjon** angir du **/authorize**.
4. I feltet **URL-bane til token** angir du **/token**.
5. Kopier den fullstendige URL-adressen til den gjeldende siden fra webleserens adresselinje, og lim den inn i feltet **URL-adresse for omadressering**.

    ![Kopier den fullstendige URL-adressen til den gjeldende siden fra webleserens adresselinje, og lim den inn i feltet URL-adresse for omadressering.](media/emea-nor-vat-return-redirect-url.png)

Følg denne fremgangsmåten for å definere en Internett-adresse som brukes av Altinn-webtjenester.

1. Gå til **Avgift** \> **Oppsett** \> **Parametere** \> **Elektroniske meldinger** \> **Webprogrammer**, og velg webprogrammet **NO Altinn** i listen til venstre.
2. I feltet **Primær URL-adresse** angir du `https://platform.tt02.altinn.no/authentication/api/v1/exchange/id-porten`.
3. Gå til **Avgift** \> **Oppsett** \> **Parametere** \> **Elektroniske meldinger** \> **Nettjenesteinnstillinger**, og angi følgende informasjon for å definere nettadressen for nettjenestene som skal fungere sammen med *API-ene for sandkasse* som norske skattemyndigheter tilbyr.

    | Webtjenestenavn | Internett-adresse |
    |---|---|
    | NO Altinn GET JSON | `https://skd.apps.tt02.altinn.no/skd/mva-melding-innsending-etm2/instances` |
    | NO Altinn POST JSON | `https://skd.apps.tt02.altinn.no/skd/mva-melding-innsending-etm2/instances` |
    | NO Altinn POST XML | `https://skd.apps.tt02.altinn.no/skd/mva-melding-innsending-etm2/instances` |
    | NO Altinn PUT JSON | `https://skd.apps.tt02.altinn.no/skd/mva-melding-innsending-etm2/instances` |
    | NO Altinn PUT XML | `https://skd.apps.tt02.altinn.no/skd/mva-melding-innsending-etm2/instances` |
    | NO Altinn GET-vedlegg | La dette feltet stå tomt. |
    | NO Valider mva-retur | `https://mp-test.sits.no/api/mva/grensesnittstoette/mva-melding/valider` |

For *produksjonssamsvar* med nettjenester som norske skattemyndigheter tilbyr bruker du følgende nettadresser.

| Webtjenestenavn | Internett-adresse |
|---|---|
| NO Altinn GET JSON        | `https://skd.apps.altinn.no/skd/mva-melding-innsending-v1/instances` |
| NO Altinn POST JSON       | `https://skd.apps.altinn.no/skd/mva-melding-innsending-v1/instances` |
| NO Altinn POST XML        | `https://skd.apps.altinn.no/skd/mva-melding-innsending-v1/instances` |
| NO Altinn PUT JSON        | `https://skd.apps.altinn.no/skd/mva-melding-innsending-v1/instances` |
| NO Altinn PUT XML         | `https://skd.apps.altinn.no/skd/mva-melding-innsending-v1/instances` |
| NO Altinn GET-vedlegg | La dette feltet stå tomt. |
| NO Valider mva-retur    | `https://idporten.api.skatteetaten.no/api/mva/grensesnittstoette/mva-melding/valider` |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
