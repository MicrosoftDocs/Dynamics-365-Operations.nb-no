---
title: Funksjonen for deling av faktura
description: Dette emnet beskriver oppsettet og funksjonen for deling av fakturaer etter leveringsadresse og TAN-nummer (Tax Account Number).
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
ms.openlocfilehash: 7dddbb9f69a9735c2a03d2b23928f5cb92d4e0fd
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6023483"
---
# <a name="split-invoice-functionality"></a>Funksjonen for deling av faktura

[!include [banner](../includes/banner.md)]

Dette emnet beskriver oppsettet og funksjonen for deling av fakturaer etter leveringsadresse og TAN-nummer (Tax Account Number).

Merk av for **Produktkvittering** eller **Faktura** i **Generelt**-fanen på siden **Leverandørparametere** for å postere og dele en produktkvittering eller faktura som har ulike leveringsadresser eller TAN-numre på siden **Bestilling**. Den posterte fakturaen blir deretter delt etter leveringsadresse og TAN-nummer.

Sett alternativet **Bekreftelse**, **Plukkliste**, **Følgeseddel** eller **Faktura** til **Ja** i raden **Leveringsinformasjon** i hurtigfanen **Del basert på** i fanen **Samleoppdatering** for å postere og dele en bekreftelse, plukkliste, følgeseddel eller faktura der ulike leveringsadresser og TAN-numre er definert for ulike fakturalinjer på siden **Salgsordre**. Fakturaen blir først delt etter leveringsadresse og deretter etter TAN-nummer.

> [!IMPORTANT]
> - Hvis ingen alternativer for **Leveringsinformasjon** er satt til **Ja**, blir fakturaen postert som én faktura. Fakturaen blir ikke delt.
> - Hvis du vil dele og postere en følgeseddel der fakturalinjene har ulike leveringsadresser og TAN-numre, må du sette alternativet **Følgeseddel** for **Leveringsinformasjon** til **Ja**.
> - Hvis du vil dele og postere en faktura der fakturalinjene har ulike leveringsadresser og TAN-numre, må du sette alternativet **Faktura** for **Leveringsinformasjon** til **Ja**.
> - Hvis du vil postere en faktura der fakturalinjene har ulike leveringsadresser, men samme TAN-nummer, setter du alternativet **Faktura** for **Leveringsinformasjon** til **Nei**. Fakturaen blir delt etter leveringsadresse.

## <a name="example"></a>Eksempel

I dette eksemplet er alternativet **Faktura** for **Leveringsinformasjon** satt til **Ja** i fanen **Samleoppdatering** på siden **Leverandørparametere**. Det posteres en innkjøpsfaktura som har følgende oppsett for leveringsadresser og TAN-numre på linjene:

- **Varelinje 1:** Leveringsadresse 1, TAN-ABCD12345A
- **Varelinje 2:** Leveringsadresse 1, TAN-ABCD12345A
- **Varelinje 3:** Leveringsadresse 2, TAN-ABCE12345B
- **Varelinje 4:** Leveringsadresse 3, TAN-ABCD12345A

Den opprinnelige fakturaen blir i dette tilfellet delt i to fakturaer og postert på følgende måte:

- Faktura 1 posteres for varelinje 1 og varelinje 2 fordi begge linjene har samme leveringsadresse og TAN-nummer.
- Faktura 2 posteres for varelinje 3.
- Faktura 3 posteres for varelinje 4.
