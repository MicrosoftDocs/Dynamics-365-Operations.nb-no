---
title: Skriv ut Mva-betaling etter kode-rapporten
description: Dette emnet inneholder informasjon om innstillingene og handlingene som kreves for å skrive ut mva-betaling etter kode-rapporten i regnskaps- eller avgiftskodevalutaen.
author: anasyash
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: anasyash
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: dad1cad6dcda1c7768f9be8bd7bd4426be7fbcbb
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358863"
---
# <a name="print-the-sales-tax-payment-by-code-report"></a>Skriv ut Mva-betaling etter kode-rapporten 

[!include [banner](../includes/banner.md)]

For å skrive ut **Mva-betaling etter kode**-rapporten går du til **Avgift** \> **Forespørsler og rapporter** \> **Merverdiavgiftsrapporter** \> **Mva-betaling etter kode**. Som standard genereres rapportbeløp i regnskapsvalutaen til den juridiske enheten for alle rapporteringskoder som er definert på siden **Mva-rapporteringskoder**.

Du kan også generere denne rapporten slik at den viser betalingsbeløp for merverdiavgift i valutaene til mva-kodene for alle rapporteringskoder som er tilordnet mva-koder på siden **Mva-koder**.

## <a name="turn-on-the-feature"></a>Aktivere funksjonen

I arbeidsområdet **Funksjonsbehandling** aktiverer du følgende funksjon: **Generate Mva-betaling etter kode-rapporten i valutaen for mva-koden**.

## <a name="run-the-report"></a>Kjøre rapporten

1. Gå til **Avgift** \> **Forespørsler og rapporter** \> **Merverdiavgiftsrapporter** \> **Mva-betaling etter rapporteringskode**.
2. I feltet **Rapportvaluta** velger du en av følgende verdier:

    - **Regnskapsvaluta** – Skriv ut rapportbeløpene i regnskapsvalutaen.
    - **Valuta for mva-kode** – Skriv ut rapportbeløpene i valutaene for mva-kodene.

    ![Dialogboksen Mva-betaling etter kode.](media/Sales-tax-payment-by-code.png)

Illustrasjonen nedenfor viser et eksempel på rapporten som genereres. Rapporten viser at rapporteringskoden **101** har **EUR**-valutaen hvis feltet **Mva-valuta** er satt til **EUR** for mva-koden som rapporteringskoden er tilordnet til.

![Eksempel på Mva-betaling etter kode-rapporten.](media/Sales-tax-payment-by-code-2.png)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]