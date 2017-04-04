---
title: Oversikt over avansert bankavstemming
description: Avanserte bankavstemmingen, kan du importere elektroniske bankkontoutdrag og avstemme automatisk med banktransaksjoner i Microsoft Dynamics 365 for operasjoner.  Denne artikkelen beskriver prosessen for definisjon av avstemming.
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
translationtype: Human Translation
ms.sourcegitcommit: 3b16ef53f9fb57a6663db0be1f7e0a57471db2fb
ms.openlocfilehash: c2fc9e858f61d7d0122393bbf306ba64ac3659b8
ms.lasthandoff: 03/31/2017


---

# <a name="advanced-bank-reconciliation-overview"></a>Oversikt over avansert bankavstemming

Avanserte bankavstemmingen, kan du importere elektroniske bankkontoutdrag og avstemme automatisk med banktransaksjoner i Microsoft Dynamics 365 for operasjoner.  Denne artikkelen beskriver prosessen for definisjon av avstemming.  

Det finnes en rekke deler må defineres før du kan bruke funksjonen Avansert bankavstemming. Hvis du vil ha mer informasjon om hvordan du konfigurerer bank utdrag import, se [definert importprosessen bank setningen](set-up-advanced-bank-reconciliation-import-process.md).  Krav til oppsett av avstemmingsprosessen er beskrevet nedenfor.

## <a name="transaction-codes"></a>Transaksjonskoder
Transaksjonskoder kan brukes som en del av avstemmingen av samsvarende regler.  Transaksjonskoder bidrar til å samsvare med bare de samme typene transaksjoner mellom Dynamics 365 for operasjoner og kontoutskriften.  Hvis du vil utføre denne typen samsvarer, må du først definere brukes til banktransaksjoner fra Dynamics 365 for operasjoner deretter tilordne disse typene til setningen transaksjonskoder som brukes av banken.  Transaksjonstypene for Dynamics 365 for transaksjoner for operasjoner som er definert i den **Banktransaksjonstype** siden.  Dette er også her du definerer hovedkontoen som skal brukes for posteringer som er tilknyttet denne transaksjonstypen. 

Når din Dynamics 365 for transaksjonskoder for operasjoner bank er definert, tilordne du deretter dem til transaksjonskoder som brukes i din elektroniske bankkontoutdrag.  Denne tilordningen er gjort ved hjelp av den **Transaksjonskodetilordning** siden.  Tilordning av transaksjonen fullføres separat for hver bankkonto.

## <a name="matching-rules-and-matching-rule-sets"></a>Samsvarsregler og samsvarsregelsett
Samsvarende regler kan du definere vilkår for automatisk avstemming mellom Dynamics 365 for operasjoner banktransaksjoner og bankkontoutdragstransaksjonene.  Oppsett av søkeregler utføres på **regler for avstemming** siden.  Hvis du vil ha mer informasjon, se [Sett opp regler for bankavstemming](set-up-bank-reconciliation-matching-rules.md). 

Samsvarsregelsett brukes til å definere en gruppe med samsvarende regler som kjøres i rekkefølge under avstemming av banken.  Samsvarende regelsett er konfigurert på den **regelsett for avstemming** siden.

## <a name="cash-and-bank-management-parameters"></a>Parametere for kontant- og bankbehandling
Antall parametere er spesifikke for avanserte bankavstemming prosessen på den **parametere for kontant- og** siden.  Den **Vis setningen linjebeløpet i debet/kredit** endrer visningen av beløpene på de **bankkontoutdrag** siden.  Hvis dette alternativet er valgt, vises bank setningen transaksjonsbeløpene i separate debet og kredit-kolonnene.  Hvis det ikke er merket, vises transaksjonsbeløpene bank-setning i en enkelt beløp-kolonne med det riktige tegnet. 

Validering-alternativene som er angitt på siden parametere overstyrer valgene som er angitt i samsvarende regler.  For eksempel du kan manuelt eller med automatisk dokumenter utenfor forskjellen datoen angitt på parametere-siden.  Også, hvis muligheten til å **bekrefte transaksjonen typetilordning** er valgt, må transaksjonstypene tilordnes mellom Dynamics-365 for banktransaksjonen for operasjoner og bankkontoutdragstransaksjonen for at transaksjonene manuelt eller automatisk samkjøres. 

Du må også konfigurere de nødvendige nummerseriene i den **parametere for kontant- og** siden.  På den **nummerserier** kategorien, Angi nummerseriekoder for nedlastingen **-ID, ID-setningen, avstemme ID og Bank avstemming** referanser.

## <a name="bank-account-reconciliation-options"></a>Alternativer for bankkontoavstemming
Du må først aktivere avanserte bankavstemmingen for bankkontoen.  Mange flere alternativer er tilgjengelige på den **bankkonto** side når Avansert bankavstemming-funksjonalitet er aktivert. 

**Bruk bankkontoutdrag som bekreftelse av elektronisk betaling** funksjonalitet som integrerer funksjonaliteten for bank-avstemming med statusene for elektronisk betaling.  Når dette er aktivert, et bankdokument opprettes automatisk for elektronisk betaling-statusen er satt til **sendt**.  I tillegg til statusen for elektronisk betaling vil bli oppdatert fra **sendt** til **mottatt** etter at betalingen er avstemt, avstemmes og posteres. 

Den **bankkonto navnet i setninger** -feltet er navnet som brukes for bankkontoen på de elektroniske bankkontoutdrag.  Dette navnet brukes når du bestemmer hvilke transaksjoner som skal importeres for en bankkonto fra en setning som kan inneholde informasjon om flere bankkontoer. 

Muligheten til å **Avstem etter import** automatisk validere bankkontoutdraget, opprette en ny bankavstemmingen og regneark, og Kjør samsvarende regelsettet som standard.  Denne funksjonen automatiserer prosessen frem til transaksjonene manuelt må kontrolleres.  Innstillingen på bankkontoen som standard når du importerer.


