---
title: Oversikt over avansert bankavstemming
description: Avansert bankavstemming lar deg importere og avstemme elektroniske bankkontoutdrag og automatisk avstemme med banktransaksjoner i Microsoft Dynamics 365 for Operations.  Denne artikkelen beskriver prosessen for definisjon av avstemming.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 98303
ms.assetid: ae071f04-f038-4b17-812d-0a241ed15521
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 6c6b171fbba90b02b80c70783ecfd9ab57beb96d
ms.contentlocale: nb-no
ms.lasthandoff: 04/25/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Oversikt over avansert bankavstemming

[!include[banner](../includes/banner.md)]


Avansert bankavstemming lar deg importere og avstemme elektroniske bankkontoutdrag og automatisk avstemme med banktransaksjoner i Microsoft Dynamics 365 for Operations.  Denne artikkelen beskriver prosessen for definisjon av avstemming.  

Det finnes en rekke deler som må defineres før du kan bruke den avanserte funksjonen for bankavstemming. Hvis du vil ha mer informasjon om hvordan du konfigurerer import for bankkontoutdrag, se [Definere prosessen for import av bankkontoutdrag](set-up-advanced-bank-reconciliation-import-process.md).  Krav til oppsett av avstemmingsprosessen er beskrevet nedenfor.

## <a name="transaction-codes"></a>Transaksjonskoder
Transaksjonskoder kan brukes som en del av samsvarsregler for bankavstemmingen.  Transaksjonskoder bidrar til å samsvare med bare de samme typene transaksjoner mellom Dynamics 365 for Operations og bankkontoutdraget.  Hvis du vil utføre denne typen samsvar, må du først definere transaksjonstypene som brukes for banktransaksjoner fra Dynamics 365 for Operations, og deretter tilordne disse typene til utdragstransaksjonskoder som brukes av banken.  Transaksjonstypene for banktransaksjoner i Dynamics 365 for Operations er definert på siden **Banktransaksjonstype**.  Det er også her du definerer hovedkontoen som skal brukes for posteringer som er tilknyttet denne transaksjonstypen. 

Når transaksjonskoder i Dynamics 365 for Operations er definert, tilordner du dem til transaksjonskoder som brukes i dine elektroniske bankkontoutdrag.  Denne tilordningsprosessen gjøres ved hjelp av siden **Transaksjonskodetilordning**.  Transaksjonskodetilordning fullføres separat for hver bankkonto.

## <a name="matching-rules-and-matching-rule-sets"></a>Samsvarsregler og samsvarsregelsett
Med samsvarsregler kan du definere vilkår for automatisk avstemming mellom Dynamics 365 for Operations -banktransaksjoner og bankkontoutdragstransaksjoner.  Oppsett av samsvarsregler utføres på siden **Samsvarsregler for avstemming**.  Hvis du vil ha mer informasjon, kan du se [Definere samsvarsregler for bankavstemming](set-up-bank-reconciliation-matching-rules.md). 

Samsvarsregelsett brukes til å definere en gruppe med samsvarsregler som kjøres i rekkefølge under avstemmingen av bankkontoutdrag.  Samsvarsregelsett konfigureres på siden **Samsvarsregelsett for avstemming**.

## <a name="cash-and-bank-management-parameters"></a>Parametere for kontant- og bankbehandling
Det er flere parametere som er spesifikke for den avanserte bankavstemmingsprosessen på siden **Parametere for kontant- og bankbehandling**.  **Vis utdragslinjebeløp i debet/kredit** endrer visningen av beløpene på siden **Bankkontoutdrag**.  Hvis dette alternativet er valgt, vises transaksjonsbeløpene fra bankkontoutdrag i separate debet og kreditkolonner.  Hvis det ikke er valgt, vises transaksjonsbeløpene fra bankkontoutdrag i én enkelt beløpskolonne med riktig fortegn. 

Valideringsalternativene som er angitt på parametersiden, overstyrer valgene som er angitt i samsvarsregler.  Du kan for eksempel ikke manuelt eller automatisk samsvare dokumenter utenfor datoforskjellen som er angitt på parametersiden.  Hvis alternativet **Valider tilordning av transaksjonstype** er valgt, må transaksjonstypene tilordnes mellom Dynamics 365 for Operations-banktransaksjonen og bankkontoutdragstransaksjonen for at transaksjonene kan samsvares manuelt eller automatisk. 

Du må også konfigurere de nødvendige nummerseriene på siden **Parametere for kontant- og bankbehandling**.  I kategorien **Nummerserier** angir du nummerseriekoder for referansene **nedlastings-ID, Utdrags-ID, avstemmings-ID og bankavstemming**.

## <a name="bank-account-reconciliation-options"></a>Alternativer for bankkontoavstemming
Du må først aktivere avansert bankavstemming for bankkontoen.  Mange flere alternativer er tilgjengelige på siden **Bankkonto** når funksjonalitet for avanserte bankavstemming er aktivert. 

Funksjonen **Bruk bankkontoutdrag som bekreftelse av elektroniske betalinger** integrerer funksjonaliteten for bankavstemming med statusene for elektroniske betalinger.  Når dette er aktivert, opprettes et bankdokument automatisk for den elektroniske betalingen der statusen er satt til **Sendt**.  I tillegg vil statusen for elektronisk betaling bli oppdatert fra **Sendt** til **Mottatt** etter at betalingen er samsvart, avstemt og postert. 

Feltet **Banknavn i bankkontoutdrag** er navnet som brukes for bankkontoen på de elektroniske bankkontoutdragene.  Dette navnet brukes når du bestemmer hvilke transaksjoner som skal importeres for en bankkonto fra et utdrag som kan inneholde informasjon om flere bankkontoer. 

Alternativet **Avstem etter import** vil automatisk validere bankkontoutdraget, opprette en ny bankavstemmingen og regneark, og kjør Standard samsvarsregelsett.  Denne funksjonen automatiserer prosessen frem til transaksjonene som må kontrolleres manuelt.  Innstillingen på bankkontoen brukes som standard når du importerer.




