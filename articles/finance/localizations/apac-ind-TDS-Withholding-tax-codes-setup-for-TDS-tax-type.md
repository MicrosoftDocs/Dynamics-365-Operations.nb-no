---
title: Definere kildeskattkoder for TDS-avgiftstypen
description: Dette emnet forklarer hvordan du konfigurerer avgiftskoder for TDS-funksjonen (Tax Deducted at Source).
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
ms.openlocfilehash: 57de382c6d363a6c1d87cf734e9aedb32d6009a9
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6349934"
---
# <a name="set-up-withholding-tax-codes-for-the-tds-tax-type"></a>Definere kildeskattkoder for TDS-avgiftstypen

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du konfigurerer avgiftskoder for TDS-funksjonen (Tax Deducted at Source).

1. Gå til **Avgift \> > Indirekte avgifter \> > Kildeskatt \> > Kildeskattkoder**.

    [![Siden Kildeskattkoder.](./media/apac-ind-TDS-17.png)](./media/apac-ind-TDS-17.png)

2. Velg **Ny** i handlingsruten for å opprette en kildeskattkode for TDS, og angi de nødvendige detaljene.
3. Velg **TDS** i **Mva-type**-feltet i kategorien **Generelt** for å kategorisere avgiftskoden som en TDS-avgiftskode.
4. I feltet **Utligningsperiode** velger du TDS-utligningsperioden for TDS-avgiftskoden.
5. I feltet **Hovedkonto** velger du finanskontoen som TDS-beløpet skal posteres til.
6. I feltet for **kundekonto** velger du kundekontoen som TDS-beløpet som er trukket fra i salgstransaksjoner, skal posteres til.

    Feltet **Opprinnelse** settes automatisk til **Prosent av bruttobeløp**, og verdien kan ikke endres.

    > [!NOTE]
    > Du kan ikke angi opprinnelsen til **Prosent av nettobeløp** for avgiftskoder av TDS-avgiftstypen.

7. I feltet **Komponenter for kildeskatt** velger du TDS-komponentgruppen for TDS-kildekode.
8. Velg **Verdier** i handlingsruten for å åpne siden **Withholding tax-verdier**.
9. I **Fra dato**-feltet angir du startdatoen for TDS-verdien. I **Til dato**-feltet angir du sluttdatoen.

    > [!NOTE]
    > Feltene **Minimumsgrense**, **Øvre grense** og **Ekskluder %** er ikke tilgjengelige for avgiftskoder av TDS-avgiftstypen.

10. Angi prosenten for TDS for TDS-avgiftskoden i **Verdi**-feltet.
11. Lukk siden **Kildeskattverdier** for å gå tilbake til siden **Kildeskattkoder**.

    > [!NOTE]
    > **Grenser**-knappen på siden **Kildeskattkoder** er ikke tilgjengelig for avgiftskoder av TDS-avgiftstypen.

12. Lukk siden.
