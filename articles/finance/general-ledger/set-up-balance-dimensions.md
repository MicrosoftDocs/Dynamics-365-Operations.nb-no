---
title: Hvordan konfigurerer jeg balansering av finansdimensjoner?
description: Dette emnet beskriver alternativene for å konfigurere og bruke funksjonen for balansering av finansdimensjon.
author: kweekley
ms.date: 08/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: DimensionDetails
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2021-08-17
ms.dyn365.ops.version: 10.0.210
ms.openlocfilehash: cb3033a615200a358c1b28b0991bae4b84470ae0
ms.sourcegitcommit: e09f5c6d78d7942af950ae3f6407df2fedceeba4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/06/2022
ms.locfileid: "8720118"
---
# <a name="how-do-i-set-up-balancing-financial-dimensions"></a>Hvordan konfigurerer jeg balansering av finansdimensjoner?

[!include [banner](../includes/banner.md)]

Dette emnet beskriver alternativene for å konfigurere og bruke funksjonen for balansering av finansdimensjon.

## <a name="symptom"></a>Symptom

Det finnes to alternativer for å konfigurere balansering av finansdimensjoner. Det første alternativet er å bruke feltet **Saldofinansdimensjon** på **Finans**-oppsett-siden (**Økonomimodul \> Finansoppsett \> Finans**). Det andre alternativet er å bruke feltet **Krev at dimensjonen balanseres** på siden **Finansdimensjoner** (**Økonomimodul > Kontoplan \> Dimensjoner \> Finansdimensjoner**). Dette emnet forklarer forskjellen mellom disse to alternativene.

## <a name="resolution"></a>Løsning

Organisasjoner bruker vanligvis balansedimensjoner til å generere en balanse som er i balanse på finansdimensjonsnivå. Hvis du aktiverer en av disse funksjonene, blir ikke posterte, ubalanserte dimensjoner balansert. Du må først angi justeringsoppføringer manuelt for å sette balansen i balanse før du aktiverer noen av funksjonene.

De to alternativene er gjensidig utelukkende. Alternativet som organisasjonen bruker, bør baseres på forretningsbehovene. Vi hører ofte om kunder som definerer balansedimensjonen i både finansoppsettet og finansdimensjonsoppsettet, og deretter fullfører vi noe av eller hele tilleggsoppsettet som kreves. De kan imidlertid fremdeles ikke posteres på grunn av ubalanse på finansdimensjonsnivået.

Delene nedenfor beskriver de to alternativene, og forklarer hvordan du konfigurerer dem.

### <a name="ledger--balancing-financial-dimension"></a>Finans – Saldofinansdimensjon

Saldofinansdimensjon på **Finans**-oppsettsiden brukes til å aktivere interenhetsregnskap. Følg denne fremgangsmåten for å aktivere funksjonen.

1. Avgjør hvilken finansdimensjon som skal være balansedimensjonen.

    - Ved hjelp av denne funksjonaliteten kan du bare velge én finansdimensjon som balansedimensjon.
    - Ikke velg dimensjonen på **Finans**-oppsettsiden ennå.
    - Kontroller at balansen allerede er balansert for den valgte finansdimensjonen.

2. Oppdater kontostrukturen for saldofinansdimensjonen.

    - Saldofinansdimensjon må inkluderes i alle kontostrukturer som er tilordnet finans.
    - Finansdimensjonen kan ikke tillate tomme verdier i kontostrukturen. Denne begrensningen sikrer at hver regnskapsoppføring som posteres i økonomimodulen, inneholder en finansdimensjonsverdi. En tom dimensjonsfordeling er ikke gyldig når det brukes balanseringsdimensjoner.

3. Definer hovedkontoene for enhetsintern debet og kredit på siden **Kontoer for automatiske transaksjoner** (**Økonomimodul \> Posteringsoppsett \> Kontoer for automatiske transaksjoner**).
4. Velg en finansdimensjon som skal brukes for balansering, på **Finans**-oppsettsiden (**Økonomimodul \> Finansoppsett \> Finans**), i feltet **Saldofinansdimensjon**.

Hvis den valgte finansdimensjonen ikke er balansert etter hvert som transaksjoner registreres og posteres, vil systemet automatisk legge til debet- eller kreditoppføringene som er nødvendige for å balansere regnskapsoppføringen under postering. Finanskontoene for debet og kredit for interenhetstransaksjon vises på det posterte bilaget i økonomimodulen. De vil imidlertid ikke vises i journalene eller kildedokumentene som regnskapsoppføringene ble postert for.

### <a name="financial-dimensions--require-the-dimension-to-be-balanced"></a>Finansdimensjoner – Krever at dimensjonen er balansert

Selv om balansedimensjonen på **Finansdimensjoner**-siden vanligvis brukes av firmaer i offentlig sektor, er funksjonaliteten ikke knyttet til en konfigurasjonsnøkkel for offentlig sektor. Fordi det ikke er noen begrensning i systemet, kan du bruke denne funksjonaliteten selv om organisasjonen ikke er en enhet i offentlig sektor.

Denne funksjonaliteten brukes vanligvis i kundegrunnlaget i offentlig sektor, fordi det krever at posteringsdefinisjoner brukes til å balansere hver transaksjon automatisk. De konserninterne debet- og kreditkontoene som er definert på siden **Kontoer for automatiske transaksjoner**, brukes ikke automatisk til å balansere regnskapsoppføringene automatisk. Hvis regnskapsoppføringer ikke er balansert på dimensjonsnivå etter at posteringsdefinisjonene er brukt, vil ikke transaksjonen posteres, selv om de konserninterne debet- og kreditkontoene er definert.

Vi hører ofte om kunder som definerer balansedimensjonen i både finansoppsettet og finansdimensjonsoppsettet. I dette tilfellet bruker systemet funksjonaliteten for finansdimensjoner. Oppsettet for balansering av dimensjoner på finansdimensjonsnivå har prioritet under postering. Posteringen vil mislykkes hvis posteringsdefinisjonen ikke oppretter en balansert regnskapsoppføring på finansdimensjonsnivå.

Følg denne fremgangsmåten for å aktivere bruken av en balansedimensjon på finansdimensjonsnivå.

1. Avgjør hvilke finansdimensjoner som skal være balansedimensjoner.

    - Du kan angi mer enn én finansdimensjon som en balansedimensjon.
    - Ikke angi finansdimensjonene som er nødvendige for å balansere en transaksjon på **Finansdimensjoner**-siden, ennå.

2. Definer posteringsdefinisjonene for hver type journal- eller kildedokument som brukes av organisasjonen. Posteringsdefinisjoner bruker finanskontoene fra en upostert journal eller kildedokument som samsvarskriterier. Posteringsdefinisjonen returnerer deretter de genererte oppføringene som blir regnskapsoppføringen. Hvis posteringsdefinisjonen er satt opp riktig, inkluderer den genererte oppføringen finanskontoene med samsvarskriterier, pluss flere kontoer for å balansere regnskapsoppføringen på dimensjonsnivå. Hvis du vil ha mer informasjon, kan du se [Posteringsdefinisjoner](posting-definitions.md). 
   
   Posteringsdefinisjoner støttes ikke på alle typer transaksjoner. Posteringsdefinisjoner kan for eksempel ikke defineres for noen transaksjoner som er registrert via økonomijournalen eller anleggsmiddeljournalen. Hvis en posteringsdefinisjon ikke kan defineres for et journal- eller kildedokument, må transaksjonen balanseres manuelt til finansdimensjonsverdien. Hvis det for eksempel opprettes en generell journaloppføring og avdelingsdimensjonen er balansedimensjonen, må du sikre at hver avdelingsverdi er i balanse.  Hvis dimensjonen ikke er balansert for hver avdelingsverdi, posteres ikke bilaget før ubalansen er rettet opp ved å legge til en konsernintern debet eller kredit i bilaget manuelt. 

    > [!IMPORTANT]
    > Hvis et stort antall transaksjoner må balanseres manuelt, bør du **ikke** bruke balansedimensjonsfunksjonaliteten på **Finansdimensjoner**-siden. Bruk i stedet balansedimensjonsfunksjonaliteten på **Finans**-oppsettsiden.

3. Når posteringsdefinisjonene er definert, kan finansdimensjonene merkes som nødvendige for balansering.

Etter hvert som du angir og posterer transaksjoner, kalles posteringsdefinisjonene under postering for å bestemme regnskapsoppføringene. Hvis finansdimensjonene er balansert, skjer valideringen etter at regnskapsoppføringene er bestemt. Hvis finansdimensjonene ikke er balansert, posteres ikke transaksjonen, og du får en melding som angir at debetbeløpet ikke er lik kreditten for en bestemt dimensjon.
