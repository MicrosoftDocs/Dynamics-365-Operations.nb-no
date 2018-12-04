---
title: Definere en foretrukket tekniker
description: Du kan velge en hvilken som helst arbeider som en foretrukket tekniker for en serviceavtale eller serviceordre.
author: ShylaThompson
manager: AnnBe
ms.date: 05/01/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: Global
ms.author: ShylaThompson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 390e436b63fdfe82e0b743e7f286cae3bb29be55
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---


# <a name="set-up-a-preferred-technician"></a>Definere en foretrukket tekniker 

[!include [banner](../includes/banner.md)]


Du kan velge en hvilken som helst arbeider som en foretrukket tekniker for en serviceavtale eller serviceordre. Det er imidlertid lurt å legge til arbeideren i det aktuelle fordelingsteamet, slik at arbeideren er inkludert i **Tjenestefordeling**.

## <a name="assign-employee-to-a-dispatch-team"></a>Tilordne en ansatt til en fordelingsgruppe

1.  Klikk på **Personale** \> **Felles** \> **Arbeidere** \> **Arbeidere**. Dobbeltklikk en arbeider for å åpne siden med arbeiderdetaljer. I **handlingsruten** klikker du **Oppsett** \>**Fordelingsteam** for å åpne skjemaet **Fordel arbeidere**.

2.  I **Fordelingsteam**-feltet velger du teamet du vil tilordne arbeideren til.

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>Tilordne en foretrukket tekniker til en serviceavtale

1.  Klikk **Servicestyring** \> **Felles** \> **Serviceavtaler** \> **Serviceavtaler**. Dobbeltklikk en serviceavtale for å åpne detaljskjemaet.

2.  I kategorien **Generelt** velger du feltet **Foretrukket tekniker**, og deretter velger du et medlem i det aktuelle fordelingsteamet som den foretrukne teknikeren for serviceavtalen.

## <a name="assign-a-preferred-technician-to-a-service-order"></a>Tilordne en foretrukket tekniker til en serviceordre

1.  Klikk **Servicestyring** \> **Periodisk** \> **Tjenestefordeling**.
    

    > [!NOTE]
    > <P>I skjemaet <STRONG>Tjenestefordeling</STRONG> angir du et datointervall for fordelingsaktiviteter du vil vise. Velg også om lukkede aktiviteter skal vises og om fordelingsaktivitetslisten skal begrenses til grupper du tilhører eller har tillatelse til å overvåke. Klikk <STRONG>OK</STRONG> for å åpne skjemaet <STRONG>Tjenestefordeling</STRONG>.</P>



2.  Velg serviceaktivitetslinjen du vil endre.

3.  I kategorien **Relatert** bruker du **Arbeider**-listen til å tilordne et medlem av korrekt fordelingsgruppe til foretrukket tekniker for serviceutkallingen.

## <a name="see-also"></a>Se også

[Serviceavtaler](service-agreements.md)

[Opprette serviceordrer manuelt](create-service-orders-manually.md)

[Serviceavtaler (skjema)](https://technet.microsoft.com/en-us/library/aa617823\(v=ax.60\))
  



