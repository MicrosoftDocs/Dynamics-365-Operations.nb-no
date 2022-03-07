---
title: Definere rapporteringskoder for kildeskatt for TDS-avgiftstypen
description: Kildeskattrapporteringskoder brukes til å generere From 26Q- og Form 27Q-oppgavene for avgift fratrukket i kilde (TDS). Dette emnet beskriver hvordan du konfigurerer rapporteringskodetrinn for kildeskatt, slik at du kan definere TDS-rapporteringskoder.
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
ms.openlocfilehash: 1f9325d182f89b98e8b943ae047c55e7e1aeb02f
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023488"
---
# <a name="set-up-withholding-tax-reporting-codes-for-the-tds-tax-type"></a>Definere rapporteringskoder for kildeskatt for TDS-avgiftstypen

[!include [banner](../includes/banner.md)]

Kildeskattrapporteringskoder brukes til å generere From 26Q- og Form 27Q-oppgavene for avgift fratrukket i kilde (TDS). Dette emnet beskriver hvordan du konfigurerer rapporteringskodetrinn for kildeskatt, slik at du kan definere TDS-rapporteringskoder.

1. Gå til **Avgift \> > Oppsett \> > Kildeskatt \> >Rapporteringskoder for kildeskatt**.

    [![Siden for rapporteringskoder for kildeskatt](./media/apac-ind-TDS-16.png)](./media/apac-ind-TDS-16.png)

2. Velg **TDS** i **Avgiftstype**-feltet for å definere rapporteringskoder for kildeskatt for TDS-avgiftstypen.
3. I feltet **Komponent for kildeskatt** velger du TDS-komponenten som du definerer rapporteringskoden for kildeskatt for. Feltet **Komponentgruppe for kildeskatt** viser TDS-komponentgruppen som ble definert for TDS-komponenten du definerer.

    Feltet **Paragrafkode** på hurtigfanen **Generelt** viser delkoden som er knyttet til TDS-komponentgruppen.

4. Velg TDS-rapporteringskoden i feltet **Rapporteringskode** i hurtigfanen **Generelt**:

    - TDS
    - TCS
    - Tillegg
    - PE\_Cess
    - SHE\_Cess

5. Lukk siden.
