---
title: Definere lagre for overføringsordrer
description: Dette emnet beskriver hvordan du kan definere lagre for overføringsordrer.
author: Mirzaab
manager: AnnBe
ms.date: 01/18/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2018-4-30
ms.dyn365.ops.version: 8
ms.openlocfilehash: 91db6e8f921bd674211f6d478b6d0f0a832c983c
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1847021"
---
# <a name="set-up-warehouses-for-transfer-orders"></a>Definere lagre for overføringsordrer 

[!include [banner](../includes/banner.md)]

Du kan bruke lagernivåer for å opprette et hierarki som støtter overføringsordrer mellom lagre. På grunnlag av dette oppsettet blir hovedplanlegging brukt til å beregne varebehov på det enkelte lagernivå og generere planlagte overføringsordrer fra et tilordnet kildelager for å dekke behovet.

1.  Klikk **Lagerstyring > Oppsett > Lageroppdeling > Lagre**.

2.  Velg lageret du vil fylle på.

3.  På **Hovedplanlegging**-hurtigkategorien merker du av for **Påfylling**.

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
