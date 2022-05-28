---
title: Kontoer for automatiske transaksjoner
description: Dette emnet beskriver hvordan kontoer for automatiske transaksjoner brukes til postering gjennom Microsoft Dynamics 365, og gir eksempler for nøkkelkontoer for automatiske transaksjoner.
author: rachel-profitt
ms.date: 12/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerSystemAccounts
audience: Application User
ms.reviewer: twheeloc
ms.custom: ''
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2022-01-03
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 275c74d673d1ba2468e23c5fa443c9272d13a184
ms.sourcegitcommit: 5d1772bdeb21a9bec6dc49e64550aaf34127a4e2
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/10/2022
ms.locfileid: "8735267"
---
# <a name="accounts-for-automatic-transactions"></a>Kontoer for automatiske transaksjoner

Siden **Kontoer for automatiske transaksjoner** (**Økonomimodul &gt; Posteringsoppsett &gt; Kontoer for automatiske transaksjoner**) brukes til å definere standard hovedkonto som brukes for hver posteringstype i systemet. Selv om de fleste posteringstyper kan konfigureres på en modulspesifikk eller funksjonsspesifikk side, kan noen posteringstyper bare konfigureres på siden **Kontoer for automatiske transaksjoner**.

Du kan for eksempel angi hovedkontoen som skal brukes for posteringstypen **Kundesaldo** i **Sammendrag**-feltet på siden **Kundeposteringsprofil**, og bruke en forskjellig hovedkonto for hver kundeprofil. På denne måten har du mer detaljert kontroll over posteringene. På den annen side kan du angi kontoene med feil bare på siden **Kontoer for automatiske transaksjoner**.

Når du åpner siden **Kontoer for automatiske transaksjoner** i en ny juridisk enhet, er kontolisten tom. Du kan legge til de vanligste posteringstypene som skal konfigureres på siden, ved å velge knappen **Opprett standardtyper**. For hver rad kan du deretter velge hovedkontoen i **Hovedkonto**-feltet. Hvis du lar **Hovedkonto**-feltet stå tomt for en posteringstype, og du ikke har konfigurert en hovedkonto på en modulspesifikk eller funksjonsspesifikk side, får du en feilmelding når du posterer en transaksjon som bruker den posteringstypen. Vanligvis vil meldingen være «Finner ikke kontoen for \[posteringstype\]».

## <a name="default-posting-types"></a>Standard posteringstyper

Følgende tabell viser eksempler på standard posteringstyper som opprettes når du velger **Opprett standardtyper** på siden **Kontoer for automatiske transaksjoner**. Den viser eksempelkontoer og beskrivelser. Kolonnen «Debet/kredit?» angir om transaksjonen vanligvis posterer et debet- eller et kreditbeløp. I noen tilfeller kan en transaksjon postere enten et debet- eller en kreditbeløp. «Avregningskonto»-kolonnen angir om posteringstypen er en avregningskonto. Hvis posteringstypen er en avregningskonto, blir beløpet som er postert i denne kontoen, automatisk tilbakeført når en senere transaksjon posteres.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Øredifferanse i rapporteringsvaluta | 618160 | Diverse utgifter | Utgift | Begge | Nei | Denne posteringstypen brukes når det forekommer en øredifferanse når et transaksjonsbeløp i en utenlandsk valuta omregnes til rapporteringsvalutaen. |
| Øredifferanse i regnskapsvaluta | 618160 | Diverse utgifter | Utgift | Begge | Nei | Denne posteringstypen brukes når det forekommer en øredifferanse når et transaksjonsbeløp i en utenlandsk valuta omregnes til regnskapsvalutaen. |
| Feilkonto | 999999 | Feilkonto | Utgift | Begge | Nei | Denne posteringstypen brukes når det oppstår en feil i systemet. Kontoen bør valideres hver periode, og eventuelle feil må løses. |
| Årets resultat | 300160 | Tilbakeholdt overskudd | Egenkapital | Begge | Nei | Denne posteringstypen brukes når årsavsluttingsprosessen kjøres for å flytte balansen for kontoer av typen **Resultat** til hovedkontoen som er valgt for årsavslutningsresultatet. |
| Kundekontantrabatt | Gjelder ikke | Gjelder ikke | Gjelder ikke | Gjelder ikke | Nei | Posteringstypen som er definert på siden **Kontoer for automatiske transaksjoner**, brukes ikke. En hovedkonto er nødvendig når kontantrabatter konfigureres i Kunder.|
| Leverandørkontantrabatt | Gjelder ikke | Gjelder ikke | Gjelder ikke | Gjelder ikke | Nei | Posteringstypen som er definert på siden **Kontoer for automatiske transaksjoner**, brukes ikke. En hovedkonto er nødvendig når kontantrabatter konfigureres i Leverandører. |

## <a name="additional-posting-types"></a>Ekstra posteringstyper

Tabellen nedenfor viser eksempler på ekstra posteringstyper som må konfigureres hvis du planlegger å bruke de relaterte funksjonene. For disse posteringstypene er ingen posteringsprofilkonfigurasjoner tilgjengelige i en annen modul. Kolonnen «Debet/kredit?» angir om transaksjonen vanligvis posterer et debet- eller et kreditbeløp. I noen tilfeller kan en transaksjon postere enten et debet- eller en kreditbeløp. «Avregningskonto»-kolonnen angir om posteringstypen er en avregningskonto. Hvis posteringstypen er en avregningskonto, blir beløpet som er postert i denne kontoen, automatisk tilbakeført når en senere transaksjon posteres.

| Posteringstype | Eksempel på hovedkonto | Eksempel på hovedkontonavn | Kontotype | Debet/kredit? | Avregningskonto | Beskrivelse |
|--------------|----------------------|---------------------------|--------------|---------------|------------------|-------------|
| Balansekonto for konsolideringsdifferanse | 801200 | Fortjeneste og tap – Revaluering | Utgift | Begge | Nei | Denne posteringstypen brukes når du utfører en konsolidering som omfatter en valutarevaluering, og det oppstår øredifferanser under revalueringen. |
| Resultatkonto for konsolideringsdifferanser | 801200 | Fortjeneste og tap – Revaluering | Utgift | Begge | Nei | Denne posteringstypen brukes når du utfører en konsolidering som omfatter en valutarevaluering, og det oppstår øredifferanser under revalueringen. |
| Enhetsintern – debet | 133500 | Enhetsintern innkommende | Objekt | Debet | Nei | Denne posteringstypen brukes når du velger en balanseringsdimensjon på **Hovedbok**-siden, og dimensjonen ikke er i balanse i en transaksjon som er postert. |
| Enhetsintern - kredit | 233500 | Enhetsintern utgående | Gjeld | Kredit | Nei | Denne posteringstypen brukes når du velger en balanseringsdimensjon på **Hovedbok**-siden, og dimensjonen ikke er i balanse i en transaksjon som er postert. |
