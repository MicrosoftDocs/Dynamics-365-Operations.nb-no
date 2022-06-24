---
title: Definere kildeskattmyndigheter for TDS-avgiftstypen
description: Denne artikkelen forklarer hvordan du konfigurerer myndigheter for TDS-funksjonen (Tax Deducted at Source).
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
ms.openlocfilehash: 43562381bab93d2f143788b8dc61f2b13d05db3b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8864220"
---
# <a name="set-up-withholding-tax-authorities-for-the-tds-tax-type"></a>Definere kildeskattmyndigheter for TDS-avgiftstypen

[!include [banner](../includes/banner.md)]

Denne artikkelen forklarer hvordan du konfigurerer myndigheter for TDS-funksjonen (Tax Deducted at Source).

1. Gå til **Avgift \> Indirekte avgifter \> Myndigheter for kildeskatt**.

    [![Siden Myndigheter for kildeskatt.](./media/apac-ind-TDS-12.png)](./media/apac-ind-TDS-12.png)

2. Velg **TDS** i **Avgiftstype**-feltet for å definere myndigheter for kildeskatt for TDS-avgiftstypen.
3. I handlingsruten velger du **Ny** for å opprette en linje.
4. Angi et navn for TDS-myndigheten i feltet **Kildeskattemyndighet**.
5. Angi en beskrivelse i **Beskrivelse**-feltet.
6. I hurtifanene **Generelt** i feltet **Leverandørkonto** velger du leverandørkontoen for TDS-myndigheten.

    > [!NOTE]
    > Du må definere navnet på banken der det blir satt inn penger som skyldes til TDS-myndighetsleverandøren. Bankens navn er definert på siden **Bankkontoer** (**Leverandører \> Alle leverandører \> Leverandør \> Konfigurer \> Bankkontoer**).

7. Lukk siden.
