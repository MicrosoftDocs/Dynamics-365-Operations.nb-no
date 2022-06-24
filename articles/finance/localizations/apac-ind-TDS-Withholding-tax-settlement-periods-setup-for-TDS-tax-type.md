---
title: Definere utligningsperioder for kildeskatt for TCS-avgiftstypen
description: Denne artikkelen forklarer hvordan du konfigurerer utligningsperioder for TDS-utligningsperioder (Tax Deducted at Source).
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
ms.openlocfilehash: 855bda71f0967c53166cf0a7f5e7e465146f34a7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8846562"
---
# <a name="set-up-withholding-tax-settlement-periods-for-the-tds-tax-type"></a>Definere utligningsperioder for kildeskatt for TCS-avgiftstypen

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer utligningsperioder for TDS-utligningsperioder (Tax Deducted at Source).

1. Gå til **Avgift \> Indirekte avgifter \> Kildeskatt \> Utligningsperioder for kildeskatt**.

    [![Siden Utligningsperioder for kildeskatt.](./media/apac-ind-TDS-13.png)](./media/apac-ind-TDS-13.png)

2. Velg **TDS** i **Avgiftstype**-feltet for å definere utligningsperioder for kildeskatt for TDS-avgiftstypen.
3. Velg **Ny** for å opprette en linje.
4. I **Utligningsperiode**-feltet angir du et navn for TDS-utligningsperioden.
5. Angi en beskrivelse i **Beskrivelse**-feltet.
6. I feltet for **kildeskattemyndighet** velger du TDS-myndigheten som du definerer TDS-utligningsperioden for.
7. I feltet **Periodeintervall** i hurtigfanen **Generelt** velger du typen periodeintervall for TDS-utligningsperioden.
8. I feltet **Antall enheter** angir du antall enheter for periodeintervalltypen.
9. I hurtigfanen **Perioder** i feltet **Fra dato** velger du startdatoen for TDS-utligningsperioden. I **Til dato**-feltet velger du sluttdatoen.
10. Hvis du vil opprette en etterfølgende TDS-utligningsperiode for en eksisterende periode, velger du **Ny periode** basert på periodeintervallet og periodeenhetene.
11. Hvis du vil vise detaljene for den periodiske TDS-utligningen som kjøres for en bestemt utligningsperiode, velger du **Kildeskattbetalinger** for å åpne **Kildeskattbetaling**-siden.

    > [!NOTE]
    > Hvis du vil kjøre den periodiske TDS-utligningsprosessen, går du til **Økonomimodul \> Periodisk \> Kildeskatt \> Kildeskattbetaling**.

    [![Siden Kildeskattbetaling.](./media/apac-ind-TDS-15.png)](./media/apac-ind-TDS-15.png)

12. Lukk siden.
