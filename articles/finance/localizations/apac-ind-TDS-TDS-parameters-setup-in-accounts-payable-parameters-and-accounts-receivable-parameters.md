---
title: Konfigurere TDS-parametere i Leverandører og Kunder
description: Dette emnet forklarer hvordan du angir parametere i Leverandører og Kunder for å støtte TDS-fradrag (Tax Deducted at Source).
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
ms.openlocfilehash: ccf1557d3c95829421b26d5f84750e3d4236c9e0
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6358224"
---
# <a name="set-tds-parameters-in-accounts-payable-and-accounts-receivable"></a>Konfigurere TDS-parametere i Leverandører og Kunder

[!include [banner](../includes/banner.md)]

Dette emnet forklarer hvordan du angir parametere i Leverandører og Kunder for å støtte TDS-fradrag (Tax Deducted at Source).

1. Gå til **Avgift \> Oppsett \> Parametere \> Kundeparametere**.
2. Velg **Oppdater ordrelinjer** i **Oppdateringer**-fanen for å åpne dialogboksen **Oppdater ordrelinjer**.
3. Angi metoden du vil bruke til å oppdatere TDS-gruppen på linjenivået, i feltet **Oppdatering av TDS-gruppe** i delen **TDS-gruppe**. Denne innstillingen brukes når TDS-gruppen oppdateres i et ordrehode. Følgende alternativer er tilgjengelige:

    - **Aldri** – TDS-gruppen oppdateres ikke på ordrelinjene når den oppdateres i ordrehodet.
    - **Alltid** – TDS-gruppen oppdateres automatisk på ordrelinjene når den oppdateres i ordrehodet.
    - **Be om** – Brukere får en melding der de blir bedt om å oppdatere TDS-gruppen på ordrelinjene.
4. Velg **OK**.

    [![Dialogboksen Oppdater ordrelinjer.](./media/apac-ind-TDS-26.PNG)](./media/apac-ind-TDS-26.PNG)

5. Gå til **Avgift \> Oppsett \> Parametere \> Leverandørparametere**.
6. Sett alternativet **Produktkvittering** til **Ja** i hurtigfanen **Del basert på leveringsinformasjon** i **Generelt**-fanen hvis du vil postere og dele en produktkvittering som har ulike leveringsadresser og TAN-numre. Hvis du setter dette alternativet til **Nei**, kan du ikke postere en bestillingsfølgeseddel som har ulike leveringsadresser og TAN-numre.
7. Sett alternativet **Faktura** til **Ja** for å postere og dele en innkjøpsfaktura som har ulike leveringsadresser og TAN-numre.

    [![Hurtigfanen Del basert på leveringsinformasjon.](./media/apac-ind-TDS-25.png)](./media/apac-ind-TDS-25.png)

8. Lukk siden.
