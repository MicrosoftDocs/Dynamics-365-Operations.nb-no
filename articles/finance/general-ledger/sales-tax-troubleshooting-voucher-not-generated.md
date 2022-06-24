---
title: Bilag genereres ikke
description: Denne artikkelen gir feilsøkingsinformasjon som kan være til hjelp når et bilag ikke genereres som det skal.
author: qire
ms.date: 04/13/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: kfend
ms.search.region: Global
ms.author: wangchen
ms.search.validFrom: 2021-04-01
ms.dyn365.ops.version: 10.0.1
ms.openlocfilehash: 1200fe50bf9be4c6d1ca809ad9a86da2ff3e0ced
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8909018"
---
# <a name="voucher-isnt-generated"></a>Bilag genereres ikke

[!include [banner](../includes/banner.md)]

Hvis et bilag skal genereres, men **bilagstransaksjonssiden** ikke viser noen bilag, følger du trinnene i de følgende delene etter behov for å feilsøke dette problemet.

[![Bilagstransaksjonsside som ikke har noen bilag.](./media/voucher-not-generated-Picture1.png)](./media/voucher-not-generated-Picture1.png)

## <a name="check-the-tax-applicability"></a>Kontrollere mva-relevansen

1. Gå til **Avgift** \> **Periodiske oppgaver** \> **Underfinansjournaloppføringer som ennå ikke er overført**.
2. Hvis det finnes en journalpost, velger du den, og deretter velger du **Overfør nå**.

    [![Overfør nå-knappen på siden Underfinansjournaloppføringer som ennå ikke er overført.](./media/voucher-not-generated-Picture2.png)](./media/voucher-not-generated-Picture2.png)

3. Åpne **bilagstransaksjonssiden** på nytt for å se om bilaget ble generert.

## <a name="determine-whether-customization-exists"></a>Fastslå om det finnes tilpasning

Hvis du har fullført trinnene i den forrige delen, men ikke har funnet problemet, må du avgjøre om det finnes tilpasning. Hvis det ikke finnes noen tilpasning, oppretter du en Microsoft-tjenesteforespørsel for mer støtte.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
