---
title: Konfigurerer TDS-finanskontoer
description: Denne artikkelen forklarer hvordan du konfigurerer finanskontoer for TDS-funksjonen (Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 227ed304c23f96cdbf4dbb4a07d028cd1e2758a6
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8904477"
---
# <a name="set-up-tds-ledger-accounts"></a>Konfigurerer TDS-finanskontoer

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer finanskontoer for TDS-funksjonen (Tax Deducted at Source). Du bruker **Kontoplan**-siden til å konfigurere finanskontoer for TDS.

1. Gå til **Økonomimodul \> Kontoplan \> Kontoer \> Hovedkontoer**.
2. Trykk på **ALT+N** i **Oversikt**-fanen for å opprette en TDS-finanskonto, og angi de nødvendige detaljene.
3. Velg **Kildeskatt** i **Posteringstype**-feltet i **Oppsett**-fanen.     

    > [!NOTE]
    > Finanskontoer som har posteringstypen **Kildeskatt**, kan bare defineres som kundereskontroer som brukes til å postere TDS-tilgodebeløpet for en TDS-avgiftskode.

4. Lukk siden.
