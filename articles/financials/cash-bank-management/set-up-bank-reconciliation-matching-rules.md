---
title: Definere samsvarsregler for bankavstemming
description: "Dette emnet beskriver hvordan du konfigurerer samsvarsregler og samsvarsregelsett for å assistere bankavstemmingsprosessen. Samsvarsregler er et sett kriterier som brukes for å filtrere bankkontoutdragslinjer og bankdokumentlinjer under avstemmingsprosessen."
author: twheeloc
manager: AnnBe
ms.date: 10/27/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BankReconciliationMatchRule, BankReconciliationMatchRuleSet
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 12971
ms.assetid: b5073f83-31dc-404f-af42-3fd84a02a7c6
ms.search.region: Global
ms.author: leguo
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 93438840123f02dd36927e044ff5ddbe60a76176
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-bank-reconciliation-matching-rules"></a>Definere samsvarsregler for bankavstemming

[!include[banner](../includes/banner.md)]


Dette emnet beskriver hvordan du konfigurerer samsvarsregler og samsvarsregelsett for å assistere bankavstemmingsprosessen. Samsvarsregler er et sett kriterier som brukes for å filtrere bankkontoutdragslinjer og bankdokumentlinjer under avstemmingsprosessen.

Du kan definere samsvarsregler og samsvarsregelsett for å assistere bankavstemmingsprosessen. En samsvarsregel for avstemming er et sett kriterier som brukes til å filtrere bankkontoutdragslinjer og Microsoft Dynamics 365 for Finance and Operations, Enterprise edition-banktransaksjonslinjer under avstemmingsprosessen. Bruk siden **Samsvarsregler for avstemming** for å definere samsvarsregler for avstemming. Du kan definere flere samsvarsregler og deretter opprette et samsvarsregelsett for avstemming på siden **Samsvarsregelsett for avstemming**. 

> [!NOTE] 
> Samsvarsregler for bankavstemming brukes hvis du avstemmer et elektronisk bankkontoutdrag ved hjelp av avansert bankavstemming. 

På siden **Samsvarsregler for avstemming** kan du velge hvilke handlinger og valgkriterier som brukes når samsvarsregelen kjøres. I **Handlinger**-feltgruppen velger du handlingen som skal utføres når samsvarsregelen kjøres under avstemmingsprosessen.  

> [!NOTE] 
> Alternativet du velger, bestemmer feltene som vises.

|                                    |                                                                                                                                                                                                                                                                                                               |                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| **Handling**                         |                                                                                                                                                                                                                                                                                                               | **Utvalgskriterier som er tilgjengelige når handlingen er valgt**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                         |
| **Samsvar med bankdokument**       | Opprett kriterier for å angi hvordan bankdokumenter og bankkontoutdragslinjer sammenlignes når samsvarsregelen kjøres fra siden **Bankavstemmingsregneark**. Transaksjonslinjene velges i henhold til tilleggskriteriene som er definert i hurtigfanene.                                | **Trinn 1: Definere samsvarsregelen** – Velg kriterier for å angi hvilke bankkontoutdrag som skal samsvares med Finance and Operations-banktransaksjoner. **Trinn 2 (valgfritt): Velg utdragslinjene å kjøre samsvarsregler mot:** Bruk et filter på hvilke utdragslinje å kjøre regler mot.                                                                                                                                                                                                                                                                                                               |
| **Nullstill tilbakeføringsutdragslinjer** | Opprett kriterier for å angi hvordan tilbakeføringsutdragslinjer skal fjernes fra skjemaet **Bankavstemmingsregneark** når samsvarsregelen kjøres. Dette alternativet brukes når en bankfeil fører til at det føres opp to bankkontoutdragslinjer i det importerte bankkontoutdraget, og linjene må avstemmes. | **Trinn 1**:**Søk etter tilbakeføringsutdragslinjer**– Legg til utvalgskriterier for å velge bankkontoutdragslinjer for tilbakeføring. Hvis du for eksempel vil velge bare sjekker, velger du **Banktransaksjonskode** i Felt-feltet, velger plusstegnet (+) i **Operator**-feltet, og deretter angir du **Sjekker** i Verdi-feltet. **Trinn 2: Søk etter opprinnelige kontoutdragslinjer** – Du kan legge til utvalgskriterier for å sammenligne bankdokumentlinjer med bankkontoutdragslinjer. **Trinn 3: Søk etter Finance and Operations -banktransaksjoner** – Du kan legge til utvalgskriterier for å samsvare Finance and Operations-banktransaksjoner med bankkontoutdragslinjer. |
| **Merk nye transaksjoner**          | Opprett kriterier for å angi hvordan nye transaksjoner skal merkes på siden **Bankavstemmingsregneark** når samsvarsregelen kjøres.                                                                                                                                                                 | **Trinn 1: Søk etter kontoutdragslinjer**– Legg til utvalgsvalgfelt for å angi hvilke bankkontoutdragslinjer som skal velges fra siden **Bankavstemmingsregneark**. **Trinn 2: Søk etter Finance and Operations-banktransaksjoner **– Du kan legge til utvalgskriterier for å søke etter bankdokumentlinjer. Hvis ingen bankdokument blir funnet, merkes en utdragslinje som en ny transaksjon.                                                                                                                                                                                                                                             |

 







