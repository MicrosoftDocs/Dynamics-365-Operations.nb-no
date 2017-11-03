---
title: "Statistiske dimensjonsmedlemmer og maler for leverandør av statistisk måling"
description: "Dette emnet gir informasjon om statistiske dimensjonsmedlemmer og maler for leverandør av statistisk måling. Statistiske dimensjonsmedlemmere kan brukes som tildelingsgrunnlag i policyer som kostnadsdistribusjon og kostnadstildeling. De kan også brukes til å rapportere ikke-monetært kostnadsforbruk."
author: AndersGirke
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CAMCostAccountingLedgerSourceEntryProvider, CAMStatisticalDimension, CAMAXStatisticalMeasureProviderTemplate
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations, Core
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: YuyuScheller
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: a59d9768161e0f456873b939c89b6e89b2fa0f67
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---

# <a name="statistical-dimension-members-and-statistical-measure-provider-templates"></a>Statistiske dimensjonsmedlemmer og maler for leverandør av statistisk måling

[!include[banner](../includes/banner.md)]

En statistisk dimensjon og medlemmene av denne brukes til å registrere og kontrollere ikke-monetære oppføringer i kostnadsregnskap. Statistiske dimensjonsmedlemmer kan brukes til to formål:

- Som tildelingsgrunnlag i policyer som kostnadsdistribusjon eller kostnadstildeling
- For rapportering av ikke-monetært forbruk

## <a name="statistical-dimension"></a>Statistisk dimensjon

En statistisk dimensjon har et unikt navn og en rekke unike dimensjonsmedlemmer. Den statistisk dimensjonen som er tilordnet en finans-ID for kostnadsregnskap. Dette forholdet knytter alle tilsvarende statistiske dimensjonsmedlemmer til Finans for kostnadsregnskap. Derfor opprettes alle statistiske poster i sammenheng med Finans for kostnadsregnskap.

> [!NOTE]
> En statistisk dimensjon kan tilordnes til mer enn én kostnadsregnskapsfinans.

Her er et eksempel på en statistisk dimensjon.

| Navn                        | Datakobling for dimensjonsmedlemmer |
|-----------------------------|--------------------------------------|
| Delte statistiske elementer | Importerte medlemmer av dimensjon           |

Her er et eksempel på en statistisk dimensjonen som er knyttet til en finanskonto for kostnadsregnskap.

| Navn                  | Regnskapsvaluta | Type valutakurs | Økonomisk kalender | Kostnadselementdimensjon | Statistisk dimensjon       |
|-----------------------|---------------------|--------------------|-----------------|------------------------|-----------------------------|
| Økonomistyring | USD                 | Konstant valuta  | Regnskapsperiode   | Delte kostnadselementer   | Delte statistiske elementer |

## <a name="statistical-dimension-members"></a>Statistiske medlemmer av dimensjon

Et statistisk dimensjonsmedlem representerer en enhet som du vil registrere ikke-monetære mål for. Disse målene kan enten brukes som enten tildelingsgrunnlag eller eller bare til å rapportere ikke-monetære verdier.

Statistiske dimensjonsmedlemmer kan opprettes manuelt. De kan også importeres fra en fil ved hjelp av databehandlingsverktøyet for import/eksport.

Et statistisk dimensjonsmedlem blir automatisk et forhåndsdefinert tildelingsgrunnlag. Den kan brukes som tildelingsgrunnlag i policyer for eller som inndata i andre typer tildelingsgrunnlag.

Her er noen eksempler på vanlige statistiske dimensjonsmedlemmer.

| Navn på statistisk dimensjon  | Statistiske elementer | beskrivelse             | Enhet |
|-----------------------------|----------------------|-------------------------|------|
| Delte statistiske elementer | Heltidsansatt                  | Heltidsansatte     | Hver  |
| Delte statistiske elementer | Elektrisitet          | Strømforbruk | kWh  |
| Delte statistiske elementer | Emb.-kostsenter              | Emballasjekostsenter   | Tmr |

## <a name="statistical-measure-provider-template"></a>Mal for leverandør av statistisk måling

Statistiske målinger kan hentes fra mange typer datakilder. Microsoft Dynamics 365 for Finance and Operations, Enterprise edition er en god kilde til å hente statistiske målinger fra. Du kan bruke en mal for leverandør av statistiske mål for enkelt å konfigurere de statistiske målinger som du vil hente ut.

Definisjonen av en mal for leverandør av statistiske mål er generisk og kan brukes på nytt i flere statistiske dimensjonsmedlemmer.

> [!NOTE]
> Alle tabeller som inneholder finansdimensjoner, kan brukes som kilder for statistiske målinger.

**Eksempel: Antall ansatte per kostsenter**

Antall ansatte per kostsenter er en statistisk måling som kan brukes for ulike formål som gir leder innsikt:

- En statistisk rapporteringsmåling etter kostsenter
- Et tiltelingsgrunnlag for ulike typer uttgifter
- Interne kostnadssatser etter kostsenter:

    - Kostnad etter ansatt
    - Inntekt etter ansatt

Tabellen HcmEmployment inneholder en liste over alle ansatte i forekomsten. Dette er en global tabell. Derfor ikke er postene relatert til en bestemt dataområde-ID.

Her er et eksempel på ansatte i tabellen HcmEmployment.

| Navn       | Kostsenter | beskrivelse   | Arbeidertype |
|------------|-------------|----|-------------|
| Ansatt 1 | CC001       | Personale | Ansatt    |
| Ansatt 2 | CC002       | FI | Ansatt    |
| Ansatt 3 | CC002       | FI | Ansatt    |
| Ansatt 4 | CC003       | LO | Ansatt    |
| Ansatt 5 | CC003       | LO | Ansatt    |
| Ansatt 6 | CC002       | FI | Oppdragstaker  |

Når du oppretter en **Mal for leverandør av statistisk måling**-post, må du bestemme hvilken funksjon som skal brukes:

- **Antall** – antall poster per kostobjekt overføres.
- **Sum** – sum for poster per kostobjekt overføres. (**Sum**-feltet og **Dato**-feltet er obligatorisk.)

## <a name="using-the-count-function"></a>Bruke Antall-funksjonen

En mal for leverandør av statistisk måling kan for eksempel defineres på følgende måte.

| Navn  | Funksjon | Kildetabell  | Summer-felt      | Dato-felt     |
|-------|----------|---------------|----------------|----------------|
| Heltidsansatte  | Antall    | HcmEmployment | Gjelder ikke her | Gjelder ikke her |

Du kan også legge til ett eller flere områder for å begrense målinger fra kildetabellen.

I dette eksemplet, hvis du bare ønsker en oversikt over alle fulltidsansatte (heltidsansatte), kan de legge til et område i den **Arbeiderype**-feltet. I **vilkår**-felte velger du **ansatt** for å begrense utdata på følgende måte.

**Områder**

| Kildetabell  | Felt       | Vilkår |
|---------------|-------------|----------|
| HcmEmployment | Arbeidertype | Ansatt |

Før du kan få statistiske målinger i kostnadsregnskap, må du opprette relasjonen mellom malen for leverandør av statistisk måling og det statistiske dimensjonsmedlemmet. Denne relasjonen opprettes per kostnadsregnskapsfinans- og versjon. Relasjonen består av en datakobling og en dataleverandør. Du kan ha flere datakoblinger og dataleverandører per statistisk dimensjonsmedlem.

> [!NOTE]
> I dette eksemplet skal vi opprette en relasjon for **faktisk versjon**.

Gå til **kostnadsregnskapsfinans** \> **faktisk versjon** \> **behandle** \> **statistiske målinger** for å opprette relasjonen. I dette scenariet velger du datakoblingen **Dynamics 365 for Finance and Operations, Enterprise edition – statistisk målinger**, fordi vi vil trekke ut data fra Finance and Operations.

**Datakilde**

| Navn        | Datakobling                                                                     | Statistisk medlem av dimensjon |
|-------------|------------------------------------------------------------------------------------|------------------------------|
| Heltidsansatte D365FO | Dynamics 365 for Finance and Operations, Enterprise edition – statistiske målinger | Heltidsansatte                         |

**Konfigurasjon av dataleverandør**

| Navn på statistisk mal |
|---------------------------|
| Heltidsansatte                      |

Etter at kildedataene for statistisk måling er behandlet, opprettes følgende statistiske oppføringer i kostnadsregnskap.

**Journal**

| Journalen | Journaltype                       | Økonomisk kalenderperiode | År   |  Periode  |  Versjon | Kildeoppføringer for datakobling|
|---------|------------------------------------|------------------------|--------|----------|----------|------------------------------|
| 00001   | Journal for overføring av statistisk oppføring | Skattemessig                 | 2017   | Periode 1 | Kontoplan USMF | Heltidsansatte                   |

**Journaloppføringer for overføring av statistisk oppføring**

| Regnskapsdato | Størrelse | Statistisk element |   beskrivelse       | Kostsenter |
|-----------------|-----------|---------------------|---------------------|-------------|
| 31.01.2017      | 1,00      | Heltidsansatte                | Heltidsansatte | CC001       |
| 31.01.2017      | 2.00      | Heltidsansatte                | Heltidsansatte | CC002       |
| 31.01.2017      | 2.00      | Heltidsansatte                | Heltidsansatte | CC003       |

**Statistiske oppføringer**

| Kostnadsobjekt |    | Regnskapsdato | Statistisk medlem av dimensjon |  beskrivelse        | Størrelse |
|-------------|----|-----------------|------------------------------|---------------------|-----------|
| CC001       | Personale | 31.01.2017      | Heltidsansatte                         | Heltidsansatte | 1,00      |
| CC002       | FI | 31.01.2017      | Heltidsansatte                         | Heltidsansatte | 2.00      |
| CC003       | LO | 31.01.2017      | Heltidsansatte                         | Heltidsansatte | 2.00      |

Hvis tildelingsgrunnlaget for det forhåndsdefinerte dimensjonsmedlemmet Heltidsansatte, tildeles som et tildelingsgrunnlag i en kostnadsdistribusjonsregel, blir kostnaden distribuert ved hjelp av følgende tildelingsfaktor.

| Kostnadsobjekt | beskrivelse    | Størrelse | Tildelingsfaktor |
|-------------|----|-----------|-------------------|
| CC001       | Personale | 1,00      | (1/5) × beløp    |
| CC002       | FI | 2.00      | (2/5) × beløp    |
| CC003       | LO | 2.00      | (2/5) × beløp    |

## <a name="using-the-sum-function"></a>Bruke summeringsfunksjonen

Et kostsenter for produksjon, CC010 (innpakning), er ansvarlig for å pakke produktene før de sendes til kunder. Den direkte arbeidskostnaden blir lagt til produktene via stykklisten (BOM) og ruten. Den indirekte kostnaden ved å drive kostsenteret må også tilordnes de produserte varene. Det beste statistiske målet for en slik tildeling er ofte antall registrerte produksjonstimer per produkt i en gitt periode.

Tabellen ProdRouteTrans inneholder alle arbeidstransaksjoner i produksjonen per juridisk enhet DataAreadID.

Her er et eksempel på ansatte i tabellen ProdRouteTrans.

| Referanse        | Tall | Operasjon | Type | Tidspunkt  | Fysisk dato | Produkt (finansdimensjon) | Juridisk enhet |
|------------------|--------|-----------|------|-------|---------------|-------------------------------------|--------------|
| Produksjonsordre | P0001  | Innpakning | Tidspunkt | 8,00  | 01.01.2017    | Appelsinjus B2B                    | USMF         |
| Produksjonsordre | P0001  | Innpakning | Tidspunkt | 8,00  | 02.01.2017    | Appelsinjus B2B                    | USMF         |
| Produksjonsordre | P0002  | Innpakning | Tidspunkt | 4,00  | 03.01.2017    | Forbruker av appelsinjus               | USMF         |
| Produksjonsordre | P0003  | Innpakning | Tidspunkt | 4,00  | 03.01.2017    | Forbruker av appelsinjus               | USMF         |
| Produksjonsordre | P0004  | Rekonst.  | Tidspunkt | 10,00 | 03.01.2017    | Forbruker av appelsinjus               | USMF         |

Når du oppretter en **Mal for leverandør av statistisk måling**-post, må du bestemme hvilken funksjon som skal brukes:

- **Antall** – antall poster per kostobjekt overføres.
- **Sum** – sum for poster per kostobjekt overføres. (**Sum**-feltet og **Dato**-feltet er obligatorisk.)

En mal for leverandør av statistisk måling kan for eksempel defineres på følgende måte.

| Navn    | Funksjon | Kildetabell   | Summer-felt | Dato-felt    |
|---------|----------|----------------|-----------|---------------|
| Emb.-kostsenter | Sum      | ProdRouteTrans | Timeantall     | Fysisk dato |

Du kan også legge til områder for å begrense målinger fra kildetabellen.

I dette eksemplet, hvis du bare vil ha summen av timer som er knyttet til Emballasjekostsenteret CC010, kan du du legge til et område i **Operasjon**-feltet. I **vilkår**-feltet velger du **innpakning** for å begrense utdataområdet.

**Områder**

| Kildetabell   | Felt     | Vilkår  |
|----------------|-----------|-----------|
| ProdRouteTrans | Operasjon | Innpakning |

Før du kan få statistiske målinger i kostnadsregnskap, må du opprette relasjonen mellom malen for leverandør av statistisk måling og det statistiske dimensjonsmedlemmet. Denne relasjonen opprettes per kostnadsregnskapsfinans- og versjon. Relasjonen består av en datakobling og en dataleverandør. Du kan ha flere datakoblinger og dataleverandører per statistisk dimensjonsmedlem.

> [!NOTE]
> I dette eksemplet skal vi opprette en relasjon for **faktisk versjon**.

Gå til **kostnadsregnskapsfinans** \> **faktisk versjon** \> **behandle** \> **statistiske målinger** for å opprette relasjonen. I dette scenariet velger du datakoblingen **Dynamics 365 for Finance and Operations, Enterprise edition – statistisk målinger**, fordi vi vil trekke ut data fra Finance and Operations.

**Datakilde**

| Navn           | Datakobling                                                                     | Statistisk medlem av dimensjon |
|----------------|------------------------------------------------------------------------------------|------------------------------|
| Emb.-kostsenter D365FO | Dynamics 365 for Finance and Operations, Enterprise edition – statistiske målinger | Emb.-kostsenter                      |

Systemet gjenkjenner at ProdRouteTrans er en tabell der hver post tilhører en separat juridisk enhet. Derfor får du spørsmål om å velge den juridiske enheten som transaksjonene skal importeres fra.

**Konfigurasjon av dataleverandør**

| Navn på statistisk mal | Juridisk enhet |
|---------------------------|--------------|
| Emb.-kostsenter                   | USMF         |

Etter at kildedataene for statistisk måling er behandlet, opprettes følgende statistiske oppføringer i kostnadsregnskap.

**Journal**

| Journalen | Journaltype                     | Økonomisk kalenderperiode | År   | Periode | Versjon   |   Kildeoppføringer for datakobling  |
|---------|----------------------------------|------------------------|--------|---------|----------------|---------|
| 00002   | Journal for overføring av statistisk oppføring | Skattemessig               | 2017    | Periode 1  | Kontoplan USMF | Emb.-kostsenter |

**Journaloppføringer for overføring av statistisk oppføring**

| Regnskapsdato | Størrelse | Statistisk element |  beskrivelse          | Produktgruppe         |
|-----------------|-----------|---------------------|-----------------------|-----------------------|
| 31.01.2017      | 16,00     | Emb.-kostsenter             | Emballasjekostsenter | Appelsinjus B2B      |
| 31.01.2017      | 8,00      | Emb.-kostsenter             | Emballasjekostsenter | Forbruker av appelsinjus |

**Statistiske oppføringer**

| Kostnadsobjekt           | Regnskapsdato | Statistisk medlem av dimensjon |    beskrivelse        | Størrelse |
|-----------------------|-----------------|------------------------------|-----------------------|-----------|
| Appelsinjus B2B      | 31.01.2017      | Emb.-kostsenter                      | Emballasjekostsenter | 16,00     |
| Forbruker av appelsinjus | 31.01.2017      | Emb.-kostsenter                      | Emballasjekostsenter | 8,00      |

Hvis tildelingsgrunnlaget for det forhåndsdefinerte dimensjonsmedlemmet Emb.-kostsenter, tildeles som et tildelingsgrunnlag i en kostnadsdistribusjonsregel, blir kostnaden distribuert ved hjelp av følgende tildelingsfaktor.

| Kostnadsobjekt           | Størrelse | Tildelingsfaktor  |
|-----------------------|-----------|--------------------|
| Appelsinjus B2B      | 16,00     | (16 ÷ 24) × beløp |
| Forbruker av appelsinjus | 8,00      | (8 ÷ 24) × beløp  |

## <a name="imported-statistical-measures"></a>Importerte statistiske målinger

Du kan importere statistiske målinger til kostnadsregnskap ved hjelp av databehandlingsverktøyet for import/eksport.

Dataenheten som skal brukes for import kalles importerte statistiske målinger.

> [!NOTE]
> Denne dataenheten er utformet for å tillate maksimalt fem unike dimensjonsverdier per post.

Strømforbruket registreres i Microsoft Excel ved å bruke dataenhetens forhåndsdefinerte format. Her er et eksempel:

| Regnskapsdato | Navn1 på dimensjonsmedlem | Navn2 på dimensjonsmedlem | Navn5 på dimensjonsmedlem | Størrelse  | Kildeidentifikator |
|-----------------|------------------------|------------------------|------------------------|------------|-------------------|
| 31.01.2017      | CC001                  |                        |                        | 2,450.00   | Elektrisitet       |
| 31.01.2017      | CC002                  |                        |                        | 4,100.00   | Elektrisitet       |
| 31.01.2017      | CC003                  |                        |                        | 15,000.00  | Elektrisitet       |

Når du har importert dataene via databehandling, blir dataene lagret i en oppsamlingstabell for kostnadsregnskap. Derfor kan de importerte dataene brukes i flere kontoer i kostnadsregnskap. Det er ikke nødvendig å lasste inn data på nytt.

Hvis du vil importere dataene, kan du gå til **Importerte data** \> **Dataenhet** \> **Importerte statistiske målinger**.

| Kildeidentifikator | Regnskapsdato | Størrelse  | Navn1 på dimensjonsmedlem | Navn2 på dimensjonsmedlem | Navn5 på dimensjonsmedlem |
|-------------------|-----------------|------------|------------------------|------------------------|------------------------|
| Elektrisitet       | 31.01.2017      | 2,450.00   | CC001                  |                        |                        |
| Elektrisitet       | 31.01.2017      | 4,100.00   | CC002                  |                        |                        |
| Elektrisitet       | 31.01.2017      | 15,000.00  | CC003                  |                        |                        |

Før du kan få statistiske målinger i kostnadsregnskap, må du opprette relasjonen mellom malen for leverandør av statistisk måling og det statistiske dimensjonsmedlemmet. Denne relasjonen opprettes per kostnadsregnskapsfinans- og versjon. Relasjonen består av en datakobling og en dataleverandør. Du kan ha flere datakoblinger og dataleverandører per statistisk dimensjonsmedlem.

> [!NOTE]
> I dette eksemplet skal vi opprette en relasjon for **faktisk versjon**.

Gå til **kostnadsregnskapsfinans** \> **faktisk versjon** \> **behandle** \> **statistiske målinger** for å opprette relasjonen. I dette scenariet kan du velge datakoblingen **Importerte statistiske målinger**, fordi dataene er importert fra et tredjepartssystem i kostnadsregnskap via Excel.

**Datakilde**

| Navn        | Datakobling                | Statistisk medlem av dimensjon |
|-------------|-------------------------------|------------------------------|
| Elektrisitet | Importerte statistiske målinger | Elektrisitet                  |

**Konfigurasjon av dataleverandør**

| Importer kildeidentifikator | Funksjon | Dimensjon1   | Dimensjon2 | Dimensjon5 |
|--------------------------|----------|--------------|------------|------------|
| Elektrisitet              | Sum      | Kostsentre |            |            |

> [!NOTE]
> Når du definerer dataleverandørkonfigurasjon, må du angi hvilke kostnadsobjektdimensjoner som skal samsvare med transaksjoner som er importert. Etter at kildedataene for statistisk måling er behandlet, opprettes følgende statistiske oppføringer i kostnadsregnskap.

**Journal**

| Journalen | Journaltype                       | Økonomisk kalenderperiode | År  | Periode  |Versjon      |Kildeoppføringer for datakobling |
|---------|------------------------------------|------------------------|-------|--------|---------------|-------------|
| 00002   | Journal for overføring av statistisk oppføring | Skattemessig                 | 2017  | Periode 1 | Kontoplan USMF | Elektrisitet |

**Journaloppføringer for overføring av statistisk oppføring**

| Regnskapsdato | Størrelse  | Kostnadselement |   beskrivelse           | Kostsenter |
|-----------------|------------|--------------|-------------------------|-------------|
| 31.01.2017      | 2,450.00   | Elektrisitet  | Strømforbruk | CC001       |
| 31.01.2017      | 4,100.00   | Elektrisitet  | Strømforbruk | CC002       |
| 31.01.2017      | 15,000.00  | Elektrisitet  | Strømforbruk | CC003       |

**Statistiske oppføringer**

| Kostnadsobjekt |    | Regnskapsdato | Statistisk medlem av dimensjon |      beskrivelse                   | Størrelse  |
|-------------|----|-----------------|------------------------------|-------------------------|------------|
| CC001       | Personale | 31.01.2017      | Elektrisitet                  | Strømforbruk | 2,450.00   |
| CC002       | FI | 31.01.2017      | Elektrisitet                  | Strømforbruk | 4,100.00   |
| CC003       | LO | 31.01.2017      | Elektrisitet                  | Strømforbruk | 15,000.00  |

Hvis tildelingsgrunnlaget for det forhåndsdefinerte dimensjonsmedlemmet Strøm, tildeles som et tildelingsgrunnlag i en kostnadsdistribusjonsregel, blir kostnaden distribuert ved hjelp av følgende tildelingsfaktor.

| Kostnadsobjekt |    | Størrelse | Tildelingsfaktor          |
|-------------|----|-----------|----------------------------|
| CC001       | Personale | 2,450.00  | (2 450 ÷ 21 550) × beløp  |
| CC002       | FI | 4,100.00  | (4 100 ÷ 21 550) × beløp  |
| CC003       | LO | 15,000.00 | (15 000 ÷ 21 550) × beløp |

## <a name="see-also"></a>Se også

[Tildelingsgrunnlag](allocation-bases.md)

