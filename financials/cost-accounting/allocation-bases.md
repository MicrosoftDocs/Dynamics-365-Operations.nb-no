---
title: Tildelingsgrunnlag
description: "Dette emnet gir informasjon om tildelingsgrunnlag. Tildelingsgrunnlag er nøkkelkomponenter i kostnadsregnskap og brukes for det meste til å tildele indirekte kostnader."
author: YuyuScheller
manager: AnnBe
ms.date: 05/24/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMDimensionMember
audience: Application User
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 223174
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: Human Translation
ms.sourcegitcommit: 63160b9473c7f45b0eb0ca7139f9ed47c8e1446f
ms.openlocfilehash: 74a3033ffbdba2efc6c5ecd6c55019898751a146
ms.contentlocale: nb-no
ms.lasthandoff: 06/20/2017


---

# Tildelingsgrunnlag
<a id="allocation-bases" class="xliff"></a> 

[!include[banner](../includes/banner.md)]

Et tildelingsgrunnlag er grunnlaget som kostnadsregnskap tildeler indirekte kostnader på. Et tildelingsgrunnlag kan være et antall, for eksempel maskindriftstid som brukes, kilowattimer (kWh) som brukes, eller antall kvadratmeter som er opptatt. Tildelingsgrunnlag brukes hovedsakelig til å tilordne indirekte kostnader til beholdning som produseres. En IT-avdeling tildeler for eksempel utgiftene etter antallet datamaskiner som hver avdeling bruker.

Det er tre typer tildelingsgrunnlag i kostnadsregnskap:

- Forhåndsdefinerte tildelingsgrunnlag for dimensjonsmedlem
- Hierarkitildelingsgrunnlag
- Formeltildelingsgrunnlag

## Forhåndsdefinerte tildelingsgrunnlag for dimensjonsmedlem
<a id="predefined-dimension-member-allocation-bases" class="xliff"></a>

De forhåndsdefinerte tildelingsgrunnlagene for dimensjonsmedlem opprettes automatisk når et dimensjonsmedlem av en av følgende typer opprettes:

- Statistiske medlemmer av dimensjon
- Medlemmer av dimensjon for kostnadselement

> [!NOTE]
> De forhåndsdefinerte tildelingsgrunnlagene for dimensjonsmedlem som er basert på et dimensjonsmedlem for kostnadselement, vurderer bare verdiene fra datakildeleverandøren, for eksempel økonomimodulen eller budsjettet.

### Eksempel 1: Bruke et dimensjonsmedlem for kostnadselement som tildelingsgrunnlag
<a id="example-1-use-a-cost-element-dimension-member-as-the-allocation-base" class="xliff"></a>
Dette eksemplet viser hvordan du oppretter en kostnadsfordelingsregel for å tildele kostnadselement 10002 (Personalforsikring) til saldoen som er registrert for kostnadselement 10001 (Lønn). Fordelingsregelen defineres basert på forholdet mellom lønn for hver avdeling og samlet lønn. (Må gjennomgås!)

I økonomimodulen er kontoplanen definert som følger.

| Kontoplan | Hovedkonto | beskrivelse        | Hovedkontotype |
|------------------|--------------|--------------------|-------------------|
| Delt           | 10001        | Lønn           | Utgift           |
| Delt           | 10002        | Personalforsikring | Utgift           |

Definer en dimensjon for kostnadselement, og konfigurerer datakoblingen. Etter at dataene er importert, opprettes følgende oppføringer i kostnadsregnskap.

**Medlemmer av dimensjon for kostnadselement**

| Navn på kostnadselementdimensjon | Kostnadselement |  beskrivelse       | Type    |
|-----------------------------|--------------|--------------------|---------|
| Kostnadselementer               | 10001        | Lønn           | Primær |
| Kostnadselementer               | 10002        | Personalforsikring | Primær |

**Forhåndsdefinerte tildelingsgrunnlag for dimensjonsmedlem** 

| Navn  | beskrivelse        | Kostnadselementdimensjon |
|-------|--------------------|------------------------|
| 10001 | Lønn           | Kostnadselementer          |
| 10002 | Personalforsikring | Kostnadselementer          |

Følgende oppføringer er postert i økonomimodulen:

- Oppføringene som viser hovedkontoen for lønn, kommer fra lønningssystemet og posteres i kostsentre.
- Utgiften for personalforsikring posteres manuelt i et standard kostsenter.

| Regnskapsdato | Kostsenter |  beskrivelse        | Hovedkonto |  beskrivelse       | Beløp i regnskapsvaluta |
|-----------------|-------------|---------------------|--------------|--------------------|-------------------------------|
| 03.01.2017      | CC001       | Personale                  | 10001        | Lønn           | 2 000,00                      |
| 03.01.2017      | CC002       | FI                  | 10001        | Lønn           | 5 000,00                      |
| 03.01.2017      | CC003       | LO                  | 10001        | Lønn           | 3 000,00                      |
| 03.01.2017      | CC099       | Standard kostsenter | 10002        | Personalforsikring | 1 000,00                      |

Etter at kildedataene for økonomimodulen er behandlet, opprettes følgende oppføringer i kostnadsregnskap.

**Kostnadsoppføringer**

| Kostnadsobjekt |  beskrivelse        | Kostnadselement  |  beskrivelse       | Kostnadsatferd   |Beløp|Regnskapsdato|
|-------------|---------------------|---------------|--------------------|-----------------|------|---------------|
| CC001       | Personale                  | 10001         | Lønn           | Uklassifisert    |2 000,00|  03.01.2017    |
| CC002       | FI                  | 10001         | Lønn           | Uklassifisert    |5 000,00|     03.01.2017         |
| CC003       | LO                  | 10001         | Lønn           | Uklassifisert    |3 000,00|      03.01.2017        |
| CC099       | Standard kostsenter | 10002         | Personalforsikring | Uklassifisert    |1 000,00|      03.01.2017       |

I dette forenklede eksemplet opprettes en kostnadsfordelingsregel for å tildele kostnadselement 10002 (Personalforsikring) i forhold til saldoen som er registrert for kostnadselement 10001 (Lønn).

**Kostnadsdistribusjonsregel**

| Dimensjonshierarkihode for kostnadsobjekt | Dimensjonshierarkihode for kostnadselement | Kostnadsatferd | Tildelingsgrunnlag |
|--------------------------------------|---------------------------------------|---------------|-----------------|
| CC099                                | 10002                                 | Uklassifisert  | 10001           |

**Beregn indirekte kostnader**

Etter at kostnadselement 10001 (Lønn) er brukt som tildelingsgrunnlaget, er resultatet av beregningen av indirekte kostnader som følger.

| Kostnadsobjekt | beskrivelse | Størrelse |   Tildelingsfaktor         | Beløp |
|-------------|-------------|-----------|-----------------------------|--------|
| CC001       | Personale          | 2 000     | (2 000 ÷ 10 000) × 1 000,00 | 200,00 |
| CC002       | FI          | 5 000     | (5 000 ÷ 10 000) × 1 000,00 | 500,00 |
| CC003       | LO          | 3 000     | (3 000 ÷ 10 000) × 1 000,00 | 300,00 |

**Journalen**

| Journalen | Journaltype                          | Økonomisk kalenderperiode | År | Periode   | Versjon                                                                 |
|---------|---------------------------------------|------------------------|------|----------|-------------------------------------------------------------------------|
| 00001   | Beregningsjournal for kostnadsdistribusjon | Skattemessig                 | 2017 | Periode 1 | Beregning av indirekte kostnader / 02.01.2017 23.51.00 / Finans /2017 / Periode 1 |

**Journaloppføringer for kostnadsobjektsaldo**

| Regnskapsdato | Kostnadsobjekt | beskrivelse         | Kostnadselement | beskrivelse        | Kostnadsatferd |  Beløp  |
|-----------------|-------------|---------------------|--------------|--------------------|---------------|----------|
| 31.01.2017      | CC099       | Standard kostsenter | 10002        | Personalforsikring | Uklassifisert  | 1 000,00 |

**Kostnadsoppføringer**

| Kostnadsobjekt |  beskrivelse        | Kostnadselement |    beskrivelse     | Kostnadsatferd | Beløp    | Regnskapsdato |
|-------------|---------------------|--------------|--------------------|---------------|-----------|-----------------|
| CC099       | Standard kostsenter | 10002        | Personalforsikring | Uklassifisert  | -1 000,00 | 31.01.2017      |
| CC001       | Personale                  | 10002        | Personalforsikring | Uklassifisert  | 200,00    | 31.01.2017      |
| CC002       | FI                  | 10002        | Personalforsikring | Uklassifisert  | 500,00    | 31.01.2017      |
| CC099       | LO                  | 10002        | Personalforsikring | Uklassifisert  | 300,00    | 31.01.2017      |

### Eksempel 2: Bruke et medlem av statistisk dimensjon som tildelingsgrunnlag
<a id="example-2-use-a-statistical-dimension-member-as-the-allocation-base" class="xliff"></a>

Medlemmer av statistisk dimensjon kan brukes som tildelingsgrunnlag for å definere policyer eller rapportere ikke-monetært forbruk etter kostnadsobjekter. Du kan opprette medlemmer av statistisk dimensjon manuelt eller importere dem fra en fil ved hjelp av databehandlingsverktøyet for import/eksport.

**Statistiske medlemmer av dimensjon**

| Navn på statistisk dimensjon | Statistisk element | beskrivelse               | Enhet |
|----------------------------|---------------------|---------------------------|------|
| Statistiske elementer       | FTE                 | Heltidsansatte       | Hver   |
| Statistiske elementer       | Strøm         | Strømforbruk   | kWh  |

Når et medlem av statistisk dimensjon er lagret, opprettes en tilsvarende post i de forhåndsdefinerte tildelingsgrunnlagene for dimensjonsmedlem.

**Forhåndsdefinerte tildelingsgrunnlag for dimensjonsmedlem**

| Navn        | beskrivelse             | Dimensjon for statistisk element |
|-------------|-------------------------|-------------------------------|
| FTE         | Heltidsansatte     | Statistiske elementer          |
| Strøm | Strømforbruk | Statistiske elementer          |

Statistiske målinger kan komme fra ulike kilder:

- Strømforbruk kan måles av målere som er montert på ulike områder i firmaet.
- Tabeller inneholder statistiske målinger. Tabellen HcmEmployment inneholder for eksempel en liste over alle ansatte og kostsentrene de arbeider for.

| Navn       | Kostsenter |  beskrivelse  | Arbeidertype |
|------------|-------------|----|-------------|
| Ansatt A | CC001       | Personale | Ansatt    |
| Ansatt B | CC002       | FI | Ansatt    |
| Ansatt C | CC002       | FI | Ansatt    |
| Ansatt D | CC003       | LO | Ansatt    |
| Ansatt F | CC003       | LO | Ansatt    |

> [!NOTE]
> Alle tabellene som inneholder finansdimensjoner, kan brukes som kilder for statistiske målinger.

Kostnadsregnskap støtter en rekke statistiske målinger ved hjelp av følgende datatilkoblinger:

- Databehandlingsverktøyet for import/eksport
- Statistiske målinger

Hvis du vil hente statistiske målinger fra systemet, må du ha en mal for leverandør av statistisk måling. Hvis du vil ha mer informasjon, kan du se Mal for leverandør av statistisk måling. (Legger til en kobling når dette emnet er skrevet.)

**Maler for leverandør av statistisk måling**

| Navn  | Funksjon | Kildetabell  | Summer-felt      | Dato-felt     |
|-------|----------|---------------|----------------|----------------|
| FTE | Antall    | HcmEmployment | Gjelder ikke her | Gjelder ikke her |

Etter at kildedataene for statistisk måling er behandlet, opprettes følgende oppføringer i kostnadsregnskap.

**Statistiske oppføringer**

| Kostnadsobjekt | beskrivelse      | Regnskapsdato | Statistisk medlem av dimensjon | beskrivelse         | Størrelse |
|-------------|------------------|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personale               | 31.01.2017      | FTE                        | Heltidsansatte | 1,00      |
| CC002       | FI               | 31.01.2017      | FTE                        | Heltidsansatte | 2,00      |
| CC003       | LO               | 31.01.2017      | FTE                        | Heltidsansatte | 2,00      |

Her er et eksempel på en kostnadsdistribusjonsregel hvis de heltidsansattes forhåndsdefinerte tildelingsgrunnlag for dimensjonsmedlem er tilordnet som tildelingsgrunnlaget i den.

| Kostnadsobjekt | beskrivelse  | Størrelse | Tildelingsfaktor |
|-------------|------|-----------|-------------------|
| CC001       | Personale   | 1,00      | (1/5) × beløp    |
| CC002       | FI   | 2,00      | (2/5) × beløp    |
| CC003       | LO   | 2,00      | (2/5) × beløp    |

Du kan bruke dataenheten Importerte statistiske målinger til å importere statistiske målinger til kostnadsregnskap. Du kan også bruke databehandlingsverktøyet for import/eksport. Strømforbruket registreres som følger i Excel.

| Regnskapsdato | Dimensjonsmedlem | Størrelse | Kildeidentifikator |
|-----------------|------------------|-----------|-------------------|
| 31.01.2017      | CC001            | 2 450,00  | Strøm       |
| 31.01.2017      | CC002            | 4 100,00  | Strøm       |
| 31.01.2017      | CC003            | 15 000,00 | Strøm       |

Etter at kildedataene for statistisk måling er behandlet, opprettes følgende oppføringer i kostnadsregnskap.

**Statistiske oppføringer**

| Kostnadsobjekt |    | Regnskapsdato | Statistisk medlem av dimensjon |    beskrivelse          | Størrelse |
|-------------|----|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Personale | 31.01.2017      | Strøm                  | Strømforbruk | 2 450,00  |
| CC002       | FI | 31.01.2017      | Strøm                  | Strømforbruk | 4 100,00  |
| CC003       | LO | 31.01.2017      | Strøm                  | Strømforbruk | 15 000,00 |

Her er et eksempel på en kostnadsdistribusjonsregel hvis det forhåndsdefinerte tildelingsgrunnlaget for dimensjonsmedlem for Strøm er tilordnet som tildelingsgrunnlaget i den.

| Kostnadsobjekt | beskrivelse  | Størrelse | Tildelingsfaktor          |
|-------------|------|-----------|----------------------------|
| CC001       | Personale   | 2 450,00  | (2 450 ÷ 21 550) × beløp  |
| CC002       | FI   | 4 100,00  | (4 100 ÷ 21 550) × beløp  |
| CC003       | LO   | 15 000,00 | (15 000 ÷ 21 550) × beløp |

## Hierarkitildelingsgrunnlag
<a id="hierarchy-allocation-bases" class="xliff"></a>

Regnskapsførere kan opprette hierarkitildelingsgrunnlagene manuelt ved å bruke en dimensjonshierarkinode for kostnadsobjekt på et eksisterende tildelingsgrunnlag. På denne måten kan du begrense området til det opprinnelige forhåndsdefinerte tildelingsgrunnlaget for dimensjonsmedlem. Ett forhåndsdefinert tildelingsgrunnlag for dimensjonsmedlem kan brukes til å opprette flere hierarkitildelingsgrunnlag. Områder kan vedlikeholdes i dimensjonshierarkiet for kostnadsobjekt som er knyttet til hierarkitildelingsgrunnlagene.

### Eksempel: Hierarkitildelingsgrunnlag som er basert på heltidsansatte i organisasjonen
<a id="example-hierarchy-allocation-bases-that-are-based-on-full-time-employees-in-the-organization" class="xliff"></a>
Her er et eksempel på et dimensjonshierarki for kostnadsobjekt som kan opprettes for å beskrive en forenklet organisasjon.

| Navn på hierarki | Nodenivå 0 | Nodenivå 1 | Nodenivå 2 | Dimensjonsmedlemmer |
|----------------|--------------|--------------|--------------|-------------------|
| Organisasjon   | Adm. dir.          | CFO          | FICO         | CC001             |
| Organisasjon   | Adm. dir.          | CFO          | Personale           | CC002             |
| Organisasjon   | Adm. dir.          | CIO          | LO           | CC003             |

De heltidsansattes forhåndsdefinerte tildelingsgrunnlag for dimensjonsmedlem som ble opprettet i forrige del, inneholder følgende oppføringer.

**Statistiske oppføringer**

| Kostnadsobjekt | beskrivelse  | Regnskapsdato | Statistisk medlem av dimensjon | beskrivelse | Størrelse |
|-------------|------|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personale   | 31.01.2017      | FTE                        | Heltidsansatte | 1,00      |
| CC002       | FI   | 31.01.2017      | FTE                        | Heltidsansatte | 2,00      |
| CC003       | LO   | 31.01.2017      | FTE                        | Heltidsansatte | 2,00      |

En kostnad må distribueres mellom kostsentre som rapporterer til organisasjonens økonomidirektør (CFO). Det bekreftes at det riktige fordelingsforholdet er antall heltidsansatte (FTE) etter kostsenter.

**Hierarkitildelingsgrunnlag**

| Navn                  | Tildelingsgrunnlag | Dimensjonsobjekt for kostnadselement | Dimensjonshierarkihode for kostnadsobjekt |
|-----------------------|-----------------|---------------------------------|--------------------------------------|
| Antall heltidsansatte i CFO | FTE           | Organisasjon                    | CFO                                  |

En forhåndsvisningsfunksjon lar deg validere hierarkitildelingsgrunnlaget som er opprettet, basert på statistisk oppføringer i systemet.

**Detaljer om tildelingsgrunnlag**

| Kostnadsobjekt | beskrivelse  |  Størrelse |
|-------------|------|------------|
| CC001       | Personale   | 1,00       |
| CC002       | FI   | 2,00       |

Her er et eksempel på en kostnadsdistribusjonsregel hvis antall heltidsansatte i hierarkitildelingsgrunnlag for CFO er tilordnet som tildelingsgrunnlaget i den.

| Kostnadsobjekt | beskrivelse  | Størrelse | Tildelingsfaktor |
|-------------|------|-----------|-------------------|
| CC001       | Personale   | 1,00      | (1/3) × beløp    |
| CC002       | FI   | 2,00      | (2/3) × beløp    |

## Formeltildelingsgrunnlag
<a id="formula-allocation-bases" class="xliff"></a>

Formeltildelingsgrunnlag lar deg definere avanserte formler for å oppnå det riktige tildelingsgrunnlaget. Du kan opprette formeltildelingsgrunnlag manuelt.

Når du oppretter et formeltildelingsgrunnlag, velger du hvilken statistisk dimensjon og dimensjon for kostnadselement som skal være grunnlaget for formelen. Alle tildelingsgrunnlag som kommer fra de tidligere valgte dimensjonene kan brukes i et formeltildelingsgrunnlag.

> [!NOTE]
> Tidligere definerte formeltildelingsgrunnlag kan brukes til å definere et nytt formeltildelingsgrunnlag.

I faktorer for formeltildelingsgrunnlag oppretter du et alias og knytter det til et tildelingsgrunnlag eller en konstant. Aliasene kan deretter brukes til å definere formelen.

Du kan bruke følgende operatorer til å definere formelen.

| Symboler | Tekst           |
|---------|----------------|
| ( )     | Parenteser    |
| \<      | Mindre enn   |
| \>      | Større enn    |
| +       | Tillegg       |
| –       | Subtraksjon    |
| \*      | Multiplikasjon |

Tradisjonelle **IF**-setninger støttes ikke. Du kan imidlertid lage setninger og validere om de er sanne.

| Kontoutdrag | Validering | Resultat |
|-----------|------------|--------|
| a \> b    | Sann       | 1      |
| a \> b    | Usann      | 0      |

### Eksempel 1: En enkel formel
<a id="example-1-a-simple-formula" class="xliff"></a>

Strømregninger består ofte av to deler:

- Et fast gebyr for nettleie
- En kostnad som er knyttet til forbruk per kWh

Forhåndsdefinerte tildelingsgrunnlag for dimensjonsmedlem for Strøm er allerede definert og har disse verdiene.

**Statistiske oppføringer**

| Kostnadsobjekt | Navn | Regnskapsdato | Statistisk medlem av dimensjon | beskrivelse             | Størrelse |
|-------------|------|-----------------|------------------------------|-------------------------|-----------|
| CC001       | Personale   | 31.01.2017      | Strøm                  | Strømforbruk | 2 450,00  |
| CC002       | FI   | 31.01.2017      | Strøm                  | Strømforbruk | 4 100,00  |
| CC003       | LO   | 31.01.2017      | Strøm                  | Strømforbruk | 15 000,00 |

Hvis det faste gebyret nå må fordeles likt på kostnadsobjekter som bruker strøm, har du to alternativer for kostnadsfordeling:

- Opprett et nytt forhåndsdefinert tildelingsgrunnlag, Fast strøm, og bruk deretter en statistisk måling på 1,00 for hvert kostnadsobjekt som brukte strøm.
- Opprett et formeltildelingsgrunnlag, Fast strøm, som drar nytte av det forhåndsdefinerte tildelingsgrunnlaget for Strøm som allerede er definert i systemet. Fordelen med dette alternativet er at dataene må lastes inn i kostnadsregnskap for bare ett medlem av statistisk dimensjon for Strøm.

**Formeltildelingsgrunnlag** 

| Navn              | Kostnadselementdimensjon | Statistisk dimensjon | Formel |
|-------------------|------------------------|-----------------------|---------|
| Fast strøm |                        | Statistiske elementer  |         |

Før du kan fylle ut **Formel**-feltet, må du angi aliaset som skal brukes i formelen.

**Faktorer for formeltildelingsgrunnlag**

| Alias | Konstant | Tildelingsgrunnlag |
|-------|----------|-----------------|
| a     |          | Strøm     |
| b     | 0,01     |                 |

Vær oppmerksom på at du ikke kan bruke 0 (null) som konstant.

**Formeltildelingsgrunnlag**

| Navn              | Kostnadselementdimensjon | Statistisk dimensjon | Formel |
|-------------------|------------------------|-----------------------|---------|
| Fast strøm |                        | Statistiske elementer  | a \> b  |

En forhåndsvisningsfunksjon lar deg validere formeltildelingsgrunnlaget som er opprettet, basert på statistisk oppføringer i systemet.

**Detaljer om tildelingsgrunnlag**

| Kostnadsobjekt | beskrivelse  | Formel           | Størrelse |
|-------------|------|-------------------|-----------|
| CC001       | Personale   | 2.450,00 \> 0,01  | 1,00      |
| CC002       | FI   | 4 100,00 \> 0,01  | 1,00      |
| CC003       | LO   | 15 000,00 \> 0,01 | 1,00      |

Her er et eksempel på en kostnadsdistribusjonsregel hvis formeltildelingsgrunnlaget for Strøm er tilordnet som tildelingsgrunnlaget i den.

**Tildelingsfaktor for kostnadsobjektsstørrelse**

| Kostnadsobjekt | Navn | Størrelse |  Tildelingsfaktor |
|-------------|------|-----------|--------------------|
| CC001       | Personale   | 1,00      | (1/3) × beløp     |
| CC002       | FI   | 1,00      | (1/3) × beløp     |
| CC003       | LO   | 1,00      | (1/3) × beløp     |

### Eksempel 2: En avansert formel
<a id="example-2-an-advanced-formula" class="xliff"></a>
I dette eksemplet skal ikke strømkostnaden følge det faktiske strømforbruket i kWh. Ledelsen ønsker å innføre insentiv for å redusere strømforbruket. 

| Regel              | Sats | 
|-------------------|------|
| a <= 10000,00 kWh | 0,75 |
| a > 10000,00 kWh  | 1,15 |

Et nytt formeltildelingsgrunnlag, Strømforbruk, opprettes.

**Formeltildelingsgrunnlag**

| Navn              | Kostnadselementdimensjon | Statistisk dimensjon | Formel |
|-------------------|------------------------|-----------------------|---------|
| Strømforbruk |                        | Statistiske elementer  |         |

Før du kan fylle ut **Formel**-feltet, må du angi aliaset som skal brukes i formelen.

**Faktorer for formeltildelingsgrunnlag**

| Alias | Konstant  | Tildelingsgrunnlag |
|-------|-----------|-----------------|
| a     |           | Strøm     |
| b     | 10 000,00 |                 |
| c     | 0,75      |                 |
| d     | 1,15      |                 |

**Formeltildelingsgrunnlag**

| Navn              | Kostnadselementdimensjon | Statistisk dimensjon | Formel                                                    |
|-------------------|------------------------|-----------------------|------------------------------------------------------------|
| Fast strøm |                        | Statistiske elementer  | ((a \> b) × ((b × c) + (a – b) × d)) + ((a \<= b] × a × c) |

En forhåndsvisningsfunksjon lar deg validere formeltildelingsgrunnlaget som er opprettet, basert på statistisk oppføringer i systemet.

**Detaljer om tildelingsgrunnlag**

| Kostnadsobjekt |    | Formel                                                                                                                             | Størrelse |
|-------------|----|-------------------------------------------------------------------------------------------------------------------------------------|-----------|
| CC001       | Personale | ((2 450,00 \> 10 000,00) × ((10 000,00 × 0,75) + (2 450,00 – 10 000,00) × 1,15)) + ((2 450,00 \<= 10 000,00) × 2 450,00 × 0,75)     | 1 837,50  |
| CC002       | FI | ((4100,00 \> 10 000,00) × ((10 000,00 × 0,75) + (4 100,00 – 10 000,00) × 1,15)) + ((4 100,00 \<= 10 000,00) × 4 100,00 × 0,75)     | 3 075,00  |
| CC003       | LO | ((15 000,00 \> 10 000,00) × ((10 000,00 × 0,75) + (15 000,00 – 10 000,00) × 1,15)) + ((15 000,00 \<= 10 000,00) × 15 000,00 × 0,75) | 13 250,00 |

Her er et nærmere blikk på formelen for CC003 (IT):

((15 000,00 \> 10 000,00) × ((10 000,00 × 0,75) + (15 000,00 – 10 000,00) × 1,15)) + ((15 000,00 \<= 10 000,00) × 15 000,00 × 0,75) = 13 250,00

(1 × (7 500,00 + 5 000,00 × 1,15)) + (0 × 15 000.00 × 0,75)            

1 × 7 500,00 + 5 750,00 + 0 

Her er et eksempel på en kostnadsdistribusjonsregel hvis formeltildelingsgrunnlaget for Fast strøm er tilordnet som tildelingsgrunnlaget i den.

| Kostnadsobjekt |  beskrivelse  | Størrelse | Tildelingsfaktor                |
|-------------|----|-----------|----------------------------------|
| CC001       | Personale | 1 837,50  | (1 837,50 ÷ 18 162,50) × beløp  |
| CC002       | FI | 3 075,00  | (3 075,00 ÷ 18 162,50) × beløp  |
| CC003       | LO | 13 250,00 | (13 250,00 ÷ 18 162,50) × beløp |

