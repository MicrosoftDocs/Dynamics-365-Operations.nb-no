---
title: "Eksempel på leverandørsjekker ved elektronisk rapportering"
description: Dette emnet gir generell informasjon om hvordan du bruker eksempelsjekkformatene i elektronisk rapportering.
author: twheeloc
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: twheeloc
ms.dyn365.intro: 2017-06-30T00:00:00.000Z
ms.dyn365.version: Enterprise edition, July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: a8ba439ff643fce4811be9224a3edf96b2b9025c
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---

[!include[banner](../includes/banner.md)]

# <a name="electronic-reporting-sample-check-formats"></a>Eksempel på sjekkformater ved elektronisk rapportering

Du kan bruke elektronisk rapportering (ER) til å formatere leverandørsjekker. Mange bank-spesifikke og sjekkleverandør-spesifikke sjekkformater er tilgjengelig på markedet. Eksempler på sjekkformater er tatt med i sjekkbetalingsmodellen i repositoriet til ER-verktøyet. Disse eksempelsjekkene er kalt **Sjekk i midten (USA)** og **Sjekk øverst stub under (USA)**.

## <a name="what-check-formats-are-currently-supported"></a>Hvilke sjekkformater støttes for tiden?

Du bør alltid gå til det delte ativabiblioteket i Microsoft Dynamics Lifecycle Services (LCS) og viser den gjeldende listen over tilgjengelige filer som har aktivatypen **TYSK konfigurasjon**. Den neste delen, "Hva må jeg konfigurere?", inneholder en kobling til et emne som forklarer hvordan du oppretter et LCS-repositorium, slik at du kan se gjennom tilgjengelige konfigurasjoner og importere valgte konfigurasjoner.

Microsoft Dynamics 365 for Finance and Operations, Enterprise edition inneholder et eksempelformat der sjekken er øverst, etterfulgt av to deler for remittering. Det inneholder også et eksempelformat hvor sjekken er i midten, mellom to remitteringsdeler. Disse eksempelformatene tilsvarer formatet for Deluxe-forretningssjekker.

## <a name="what-do-i-have-to-set-up"></a>Hva må jeg konfigurere?

- Før du kan skrive ut sjekker ved hjelp av ER må minst én aktiv sjekk-konfigurasjon importeres til dine ER-konfigurasjoner. hvis du vil ha mer informasjon, kan du se [Laste ned elektroniske rapporteringskonfigurasjoner fra Lifecycle Services](/dynamics365/unified-operations/dev-itpro/analytics/download-electronic-reporting-configuration-lcs).
- Når du konfigurerer kontant- og bankbehandlingssjekker for bankkontoen, merker du av for **Generisk elektronisk eksportformat**, og velger deretter riktig sjekkformat som en eksportformatkonfigurasjon.
- Du må også angi hvor mange seddellinjer som skal skrives ut på remitteringen. Husk å inkludere radoverskrifter når du beregner dette antallet. For de to eksempelsjekkformatene er anbefalt antall følgeseddellinjer 17. Dette nummeret vil imidlertid variere, avhengig av sjekkpapiret og skriverdriverne.
- Vi anbefaler at du skriver ut en testsjekk for å validere sjekkoppsettet. Hvis du vil skrive ut en testsjekk, velg  **Skriv ut test**-alternativet. Eksempelsjekkformatene fungerer best når **Marginer** er satt til **Ingen** i de avanserte skriveregenskapene for Microsoft Excel. Etter at testsjekken er generert, aktiverer du redigering av Excel-utdataene, og konfigurerer sideoppsettet slik at alle margene er satt til **0** (null). Sammenlign testeksemplaret av sjekkene med sjekkpapiret, og juster innstillingene til du er fornøyd med justeringen.
- Når du genererer betalinger for den konfigurerte bankkontoen i betalingsjournalen, må sjekkene skrives ut ved hjelp av det angitte formatet.

Hvis du vil ha mer informasjon, se [Endre et format for elektronisk rapportering](/dynamics365/unified-operations/dev-itpro/analytics/modify-electronic-reporting-format-reapply-excel-template).

