---
title: Opprette en malstykkliste
description: Du kan opprette en malstykkliste ved å bruke flere metoder.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMATemplateBOMTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 89c5d45ac27a8678c51fb63c0326c2802a094596
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1566601"
---
# <a name="create-a-template-bom"></a>Opprette en malstykkliste   

[!include [banner](../includes/banner.md)]


Du kan opprette en malstykkliste ved å bruke en av følgende metoder. For alle metodene er feltene **Fra dato** og **Til dato** valgfrie og bare til informasjon.

## <a name="create-a-template-bom-manually"></a>Opprette en malstykkliste manuelt

1.  Klikk **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.

2.  Trykk CTRL+N for å åpne skjemaet **Opprett malstykkliste**.

3.  Under **Kopier stykklistelinjer fra referanse** velger du **Manuell**.

4.  I **Varenummer**-feltet angir du en vare av typen **Stykkliste**.

5.  I **Navn**-feltet angir du et navn på malen.

6.  I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.

7.  Klikk **OK**.

Det opprettes en ny, tom malstykkliste.

## <a name="create-a-template-bom-based-on-another-template-bom"></a>Opprette en malstykkliste basert på en annen malstykkliste

1.  Klikk **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.

2.  Trykk CTRL+N for å åpne skjemaet **Opprett malstykkliste**.

3.  Under **Kopier stykklistelinjer fra referanse** velger du **Malstykkliste**.

4.  I **Referansenummer**-feltet velger du en eksisterende malstykkliste som skal kopieres til den nye malstykklisten.

5.  I **Navn**-feltet angir du et navn på malen.

6.  I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.

7.  Klikk **OK**.

En ny malstykkliste opprettes ved hjelp av linjer som svarer til linjene i den opprinnelige malstykklisten.

## <a name="create-a-template-bom-based-on-an-item-bom"></a>Opprette en malstykkliste basert på en varestykkliste

1.  Klikk **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.

2.  Trykk CTRL+N for å åpne skjemaet **Opprett malstykkliste**.

3.  Under **Kopier stykklistelinjer fra referanse** velger du **Stykkliste**.

4.  I **Referansenummer**-feltet velger du en stykklisteversjon. En vare av typen stykkliste kopieres til **Varenummer**.

5.  I **Navn**-feltet angir du et navn på malen.

6.  I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.

7.  Klikk **OK**.

Det opprettes en ny malstykkliste ved å bruke linjer som tilsvarer linjene i stykklisten som er angitt i **Stykklister**.

## <a name="create-a-template-bom-based-on-a-production-bom"></a>Opprette en malstykkliste basert på en produksjonsstykkliste

1.  Klikk **Servicestyring** \> **Oppsett** \> **Serviceobjekter** \> **Malstykklister**.

2.  Trykk CTRL+N for å åpne skjemaet **Opprett malstykkliste**.

3.  Under **Kopier stykklistelinjer fra referanse** velger du **Produksjon**.

4.  I **Referansenummer**-feltet velger du en produksjonsstykkliste.

5.  I **Navn**-feltet angir du et navn på malen.

6.  I feltene **Fra dato** og **Til dato** angir du et datointervall der malstykklisten er aktiv.

7.  Klikk **OK**.

Det opprettes en ny malstykkliste ved å bruke linjer som tilsvarer linjene i stykklisten som er angitt i **Stykkliste**.

## <a name="see-also"></a>Se også

[Stykklistemaler ](template-boms.md)

  


