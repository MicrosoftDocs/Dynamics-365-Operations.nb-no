---
title: Korrigere en fritekstfaktura
description: Denne artikkelen forklarer hvordan du kan rette en fritekstfaktura som er postert og sende den på nytt som en rettet faktura.
author: abruer
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: twheeloc
ms.custom: 13991
ms.assetid: 2a0a4789-8619-4974-bef9-0923cc848420
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b3cc07a1f0ba444250eddcf892681e2ca63e9c1a
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780516"
---
# <a name="correct-a-free-text-invoice"></a>Korrigere en fritekstfaktura

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du kan rette en fritekstfaktura som er postert og sende den på nytt som en rettet faktura.

Til å rette en fritekstfaktura som allerede er postert: 
1. Åpne den posterte fritekstfakturaen. 
2. På **Faktura**-siden velger du **Avbryt**, og velger deretter **Rett faktura**. 
3. Velg en årsakskode, legg til kommentarer, og velg datoen for ny, korrigert faktura.
4. Du kan endre den rettede fakturaen og postere den. 

Når du posterer den rettede fakturaen, opprettes en annulleringsfaktura for et kreditbeløp som er lik det opprinnelige fakturabeløpet. Den kombinerte saldoen mellom den opprinnelige fakturaen og annulleringsfakturaen er derfor 0 (null). Annulleringsfakturaen utlignes mot den opprinnelige fakturaen. 

Når du posterer den rettede fakturaen, får du tre fakturaer:

-   **Opprinnelig faktura** – Fakturaen som inneholder informasjonen du retter.
-   **Annulleringsfaktura** – Den systemgenererte kreditfakturaen som ble opprettet for å annullere fakturaen som sist ble rettet.
-   **Rettet faktura** – Fakturaen som inneholder den rettede fakturainformasjonen.

Du kan identifisere annullerings- og korrigeringsfakturaer på to måter:

-   Siden **Alle fritekstfakturaer** inneholder en **Korrigering**-kolonne der du kan se hvilke fakturaer som er annulleringsfakturaer, og hvilke som er korrigeringsfakturaer.
-   Toppteksten i fritekstfakturaen viser statusen **Annulleringsfaktura \[fakturanummeret\]** eller **Rettet faktura\[ fakturanummer\]**.

> [!NOTE]
> Denne funksjonen er bare tilgjengelig hvis konfigurasjonsnøkkelen **Korreksjon av fritekstfaktura** er valgt. Hvis du vil ha mer informasjon om hvordan du aktiverer konfigurasjonsnøkler, kan du se i delen om aktivering (eller deaktivering) av konfigurasjonsnøkler i artikkelen [Vedlikeholdsmodus](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md). 





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
