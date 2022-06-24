---
title: Definere lagre for overføringsordrer
description: Denne artikkelen beskriver hvordan du kan definere lagre for overføringsordrer.
author: Mirzaab
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventLocation,CustVendTransportPoint2Point
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 984f90343805d35833b7ddd1a175af5833c23dd5
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/03/2022
ms.locfileid: "8905522"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Definere lagre for overføringsordrer 

[!include [banner](../includes/banner.md)]

Du kan bruke lagernivåer for å opprette et hierarki som støtter overføringsordrer mellom lagre. På grunnlag av dette oppsettet blir hovedplanlegging brukt til å beregne varebehov på det enkelte lagernivå og generere planlagte overføringsordrer fra et tilordnet kildelager for å dekke behovet.

1.  Klikk på **Lagerstyring > Oppsett > Lageroppdeling > Lagre**.

2.  Velg lageret du vil fylle på.

3.  På **Hovedplanlegging**-hurtigfanen merker du av for **Påfylling**.

4.  I **Hovedlager**-feltet velger du lageret du vil tilordne som påfyllingslager. Hovedplanleggingen beregner et overføringsbehov for det valgte lager og genererer en planlagt overføringsordre fra tilordnet **Hovedlager**.
   
    > [!NOTE]
    > <P>Hvis du fjerner merket for <STRONG>Påfylling</STRONG>, blir det valgte lageret tilordnet et lagernivå i forhold til <STRONG>Hovedlager</STRONG>, men <STRONG>Hovedlager</STRONG> blir ikke definert som et påfyllingslager.</P>

5.  Velg siden for å bruke det nye oppsettet.


> [!TIP]
> <P>Hvis du vil tilordne et lager for påfylling, må du først definere lagret som en lagringsdimensjon på siden <STRONG>Lagringsdimensjonsgrupper</STRONG>. På denne siden velger du feltet <STRONG>Aktiv</STRONG> og feltet <STRONG>Dekningsplanlegg etter dimensjon</STRONG> for lageret.</P>

## <a name="set-up-transport-lead-time"></a>Angi leveringstid for transporten

Du må også definere leveringstiden for transport mellom lagrene på siden **Transportdager**. 
1. Gå til **Lagerstyring > Oppsett > Distribusjon > Transportdager**.
2. I **Mottakspunkt**-feltet velger du **lager**.
3. Velg **Leverende lager**, **Mottakende lager** og **Transportdager**. 
4. (Valgfritt) Du kan også angi transporttiden, avhengig av leveringsmåten, under **Transportdager per leveringsmåte**-fanen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]