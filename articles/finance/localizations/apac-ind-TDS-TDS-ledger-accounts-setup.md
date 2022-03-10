---
title: Konfigurerer TDS-finanskontoer
description: Dette emnet forklarer hvordan du konfigurerer finanskontoer for TDS-funksjonen (Tax Deducted at Source).
author: kailiang
ms.date: 02/12/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 15721
ms.assetid: b4b406fa-b772-44ec-8dd8-8eb818a921ef
ms.search.region: Global
ms.author: kailiang
ms.search.validFrom: 2021-02-12
ms.dyn365.ops.version: AX 10.0.17
ms.openlocfilehash: 45c8d08ebca6ce1479baf975bfd661c6d100cac869b706fdb30ea64e9550ef6c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6715027"
---
# <a name="set-up-tds-ledger-accounts"></a>Konfigurerer TDS-finanskontoer

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer finanskontoer for TDS-funksjonen (Tax Deducted at Source). Du bruker **Kontoplan**-siden til å konfigurere finanskontoer for TDS.

1. Gå til **Økonomimodul \> Kontoplan \> Kontoer \> Hovedkontoer**.
2. Trykk på **ALT+N** i **Oversikt**-fanen for å opprette en TDS-finanskonto, og angi de nødvendige detaljene.
3. Velg **Kildeskatt** i **Posteringstype**-feltet i **Oppsett**-fanen.     

    > [!NOTE]
    > Finanskontoer som har posteringstypen **Kildeskatt**, kan bare defineres som kundereskontroer som brukes til å postere TDS-tilgodebeløpet for en TDS-avgiftskode.

4. Lukk siden.
