---
title: Definer samsvarsregler for bankavstemming
description: Denne artikkelen beskriver hvordan du konfigurerer samsvarsregler og samsvarsregelsett for å assistere bankavstemmingsprosessen. Samsvarsregler er et sett kriterier som brukes for å filtrere bankkontoutdragslinjer og bankdokumentlinjer under avstemmingsprosessen.
author: angelad116
ms.date: 11/22/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: kfend
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ac5ab5e2bcb9a63bb52d5a74bd5e4b5db51ba603
ms.sourcegitcommit: 81bb8e51951395be3f18f45212e47e6c41656f6a
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/23/2022
ms.locfileid: "9803944"
---
# <a name="set-up-bank-reconciliation-matching-rules"></a>Definer samsvarsregler for bankavstemming

[!include [banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du konfigurerer samsvarsregler og samsvarsregelsett for å assistere bankavstemmingsprosessen. Samsvarsregler er et sett kriterier som brukes for å filtrere bankkontoutdragslinjer og bankdokumentlinjer under avstemmingsprosessen.

Du kan definere samsvarsregler og samsvarsregelsett for å assistere bankavstemmingsprosessen. En samsvarsregel for avstemming er et sett kriterier som brukes for å filtrere bankkontoutdragslinjer og Dynamics 365 Finance-banktransaksjonslinjer under avstemmingsprosessen. Bruk siden **Samsvarsregler for avstemming** for å definere samsvarsregler for avstemming. Du kan definere flere samsvarsregler og deretter opprette et samsvarsregelsett for avstemming på siden **Samsvarsregelsett for avstemming**. 

> [!NOTE] 
> Samsvarsregler for bankavstemming brukes hvis du avstemmer et elektronisk bankkontoutdrag ved hjelp av avansert bankavstemming. 

På siden **Samsvarsregler for avstemming** kan du velge hvilke handlinger og valgkriterier som brukes når samsvarsregelen kjøres. I **Handlinger**-feltgruppen velger du handlingen som skal utføres når samsvarsregelen kjøres under avstemmingsprosessen.  

Som standard vil samsvarsregler samsvare med det første bankdokumentet som oppfyller kriteriene for samsvarsregelen. Hvis flere bankdokumenter oppfyller regelkriteriene, vil parameteren som krever manuelt samsvar, aktiveres ved å gå til **Kontant- og bankbehandling > Oppsett > Parametere for kontant- og bankbehandling > Bankavstemming > Krev manuelt samsvar når avanserte bankavstemmingsregler finner flere dokumenter som samsvarer på beløp**.

> [!NOTE] 
> Alternativet du velger, bestemmer feltene som vises.

| Handling | beskrivelse   | Utvalgskriterier som er tilgjengelige når handlingen er valgt     |
|--------|---------------|----------------------------------------------------------|
| **Samsvar med bankdokument**       | Opprett kriterier for å angi hvordan bankdokumenter og bankkontoutdragslinjer sammenlignes når samsvarsregelen kjøres fra siden **Bankavstemmingsregneark**. Transaksjonslinjene velges i henhold til tilleggskriteriene som er definert i hurtigfanene. | <ul><li>**Trinn 1: Definere samsvarsregelen** – Velg kriterier for å angi hvilke bankkontoutdrag som skal samsvares med Finance-banktransaksjoner.</li><li> **Trinn 2 (valgfritt): Velg utdragslinjene å kjøre samsvarsregler mot:** Bruk et filter på hvilke utdragslinje å kjøre regler mot.</li></ul>                                       |
| **Nullstill tilbakeføringsutdragslinjer** | Opprett kriterier for å angi hvordan tilbakeføringsutdragslinjer skal fjernes fra skjemaet **Bankavstemmingsregneark** når samsvarsregelen kjøres. Dette alternativet brukes når en bankfeil fører til at det føres opp to bankkontoutdragslinjer i det importerte bankkontoutdraget, og linjene må avstemmes. |<ul><li> **Trinn 1**:**Søk etter tilbakeføringsutdragslinjer**– Legg til utvalgskriterier for å velge bankkontoutdragslinjer for tilbakeføring. Hvis du for eksempel vil velge bare sjekker, velger du **Banktransaksjonskode** i **Felt**-feltet, velger plusstegnet (+) i **Operator**-feltet, og deretter angir du **Sjekker** i **Verdi**-feltet. </li><li>**Trinn 2: Søk etter opprinnelige kontoutdragslinjer** – Du kan legge til utvalgskriterier for å sammenligne bankdokumentlinjer med bankkontoutdragslinjer. </li><li>**Trinn 3: Søk etter Finance-banktransaksjoner** – Du kan legge til utvalgskriterier for å samsvare Finance-banktransaksjoner med bankkontoutdragslinjer.</li></ul>  |
| **Merk nye transaksjoner**          | Opprett kriterier for å angi hvordan nye transaksjoner skal merkes på siden **Bankavstemmingsregneark** når samsvarsregelen kjøres.                                                                                                                                                                 | <ul><li>**Trinn 1: Søk etter kontoutdragslinjer**– Legg til utvalgsvalgfelt for å angi hvilke bankkontoutdragslinjer som skal velges fra siden **Bankavstemmingsregneark**.</li><li> **Trinn 2: Søk etter Finance and Operations** – Du kan legge til utvalgskriterier for å søke etter bankdokumentlinjer. Hvis ingen bankdokument blir funnet, merkes en utdragslinje som en ny transaksjon. </li></ul>         |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]

