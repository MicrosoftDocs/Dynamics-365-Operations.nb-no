---
title: Korrigere en fritekstfaktura
description: "Denne artikkelen forklarer hvordan du kan rette en fritekstfaktura som er postert og sende den på nytt som en rettet faktura."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: mfalkner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: ab16c517abfd3fa2b59625fff04b7427ee3471bb
ms.lasthandoff: 03/31/2017


---

# <a name="correct-a-free-text-invoice"></a>Korrigere en fritekstfaktura

[!include[banner](../includes/banner.md)]


Denne artikkelen forklarer hvordan du kan rette en fritekstfaktura som er postert og sende den på nytt som en rettet faktura.

Hvis du vil rette en fritekstfaktura som allerede er postert, kan du åpne den posterte fritekstfakturaen. På **Faktura**-siden velger du **Avbryt**, og velger deretter **Rett faktura**. Velg en årsakskode, legg til kommentarer, og velg datoen for ny, korrigert faktura. Du kan endre den rettede fakturaen og postere den. 

Når du posterer den rettede fakturaen, opprettes en annulleringsfaktura for et kreditbeløp som er lik det opprinnelige fakturabeløpet. Den kombinerte saldoen mellom den opprinnelige fakturaen og annulleringsfakturaen er derfor 0 (null). Annulleringsfakturaen utlignes mot den opprinnelige fakturaen. 

Når du posterer den rettede fakturaen, får du tre fakturaer:

-   **Opprinnelig faktura** – Fakturaen som inneholder informasjonen du retter.
-   **Annulleringsfaktura** – Den systemgenererte kreditfakturaen som ble opprettet for å annullere fakturaen som sist ble rettet.
-   **Rettet faktura** – Fakturaen som inneholder den rettede fakturainformasjonen.

Du kan identifisere annullerings- og korrigeringsfakturaer på to måter:

-   Siden **Alle fritekstfakturaer** inneholder en **Korrigering**-kolonne der du kan se hvilke fakturaer som er annulleringsfakturaer, og hvilke som er korrigeringsfakturaer.
-   Toppteksten i fritekstfakturaen viser statusen **Annulleringsfaktura \[fakturanummeret\]** eller **Rettet faktura\[ fakturanummer\]**.

> [!NOTE]
> Denne funksjonen er bare tilgjengelig hvis konfigurasjonsnøkkelen **Korreksjon av fritekstfaktura** er valgt.




