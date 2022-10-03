---
title: Aktivere valutakurstype for forskuddsskatt og oppsett for dato
description: Denne artikkelen beskriver hvordan du aktiverer det globale oppsettet for valutakurstypen og datotypen for kildeskatt.
author: kailiang
ms.date: 08/02/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 13131
ms.assetid: 08fd46ef-2eb8-4942-985d-40fd757b74a8
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2022-08-01
ms.dyn365.ops.version: 10.0.29
ms.openlocfilehash: 9db9cf41381b8b4de7dffe1c755a7df805a003ea
ms.sourcegitcommit: adadbc6e355e2ad68a1f6af26a1be1f89dc8eec6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/22/2022
ms.locfileid: "9573231"
---
# <a name="enable-the-global-withholding-tax-currency-exchange-rate-type-and-date-type-setup"></a>Aktivere valutakurstype for forskuddsskatt og oppsett for dato

[!include[banner](../includes/banner.md)]

Denne artikkelen beskriver hvordan du aktiverer det globale oppsettet for valutakurstypen og datotypen for kildeskatt. Du kan nå velge en egen valutakurstype og beregningsdatotype for valutakurser for kildeskattvalutaen. Disse valgene bestemmer den utenlandske valutakursen som brukes til å beregne kildeskattbeløpet i betalingstransaksjonene i kildeskattvalutaen.

Denne funksjonen er tilgjengelig i Microsoft Dynamics 365 Finance versjon 10.0.29 og nyere.

1. Gå til **Avgift** \> **Oppsett** \> **Parametere** \> **Parametere for økonomimodul**.
2. Sett alternativet **Aktiver avansert kildeskattvaluta** til **Ja** i fanen **Kildeskattvaluta**.
3. Velg en valutakurstype for kildeskattvalutaen i **Valutakurstype**-feltet.
4. I feltet **Beregningsdatotype** velger du en beregningsdatotype som bestemmer valutakursen for kildeskatt:

    - **Betalingsdato** – Fastgjør valutakursen basert på posteringsdatoen til betalingsjournalen.
    - **Fakturadato** – Fastgjør valutakursen basert på faktureringsdatoen til fakturasjournalen. Hvis fakturadatoen på bilaget er tomt, brukes fakturaposteringsdatoen. 
    - **Dokumentdato** – Fastgjør valutakursen basert på dokumentdatoen til betalingsjournalen. Hvis dokumentdatoen på bilaget er tomt, brukes betalingsdatoen.

5. Velg **Lagre**.

Hvis transaksjonsvalutaen er forskjellig fra kildeskattvalutaen som er definert i kildeskattkoden, blir beløpet i kildeskattvalutaen beregnet fra transaksjonsvalutaen, basert på de foregående innstillingene, og blir registrert i de posterte kildeskatttransaksjonene.
