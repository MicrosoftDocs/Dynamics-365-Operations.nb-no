---
title: Skriv ut Mva-betaling etter kode-rapporten
description: Denne artikkelen inneholder informasjon om innstillingene og handlingene som kreves for å skrive ut mva-betaling etter kode-rapporten i regnskaps- eller avgiftskodevalutaen.
author: AdamTrukawka
ms.date: 05/27/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: atrukawk
ms.search.validFrom: 2020-04-08
ms.dyn365.ops.version: 10.0.11
ms.search.form: ''
ms.openlocfilehash: ea11826d21b66e6283abf24b3f7b0945e6eb9192
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/12/2022
ms.locfileid: "9272376"
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
