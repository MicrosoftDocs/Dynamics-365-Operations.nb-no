---
title: Definere en foretrukket tekniker
description: Du kan velge en hvilken som helst arbeider som en foretrukket tekniker for en serviceavtale eller serviceordre.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAAgreementTable, SMADispatchBoard
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4c9495bbc8e5f7cb603c027a125887feba1f0e2d
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9017210"
---
# <a name="set-up-a-preferred-technician"></a>Definere en foretrukket tekniker 

[!include [banner](../includes/banner.md)]


Du kan velge en hvilken som helst arbeider som en foretrukket tekniker for en serviceavtale eller serviceordre. Det er imidlertid lurt å legge til arbeideren i det aktuelle fordelingsteamet, slik at arbeideren er inkludert i **Tjenestefordeling**.

## <a name="assign-employee-to-a-dispatch-team"></a>Tilordne en ansatt til en fordelingsgruppe

1.  Klikk på **Personale** \> **Arbeidere** \> **Arbeidere**. Dobbeltklikk en arbeider for å åpne siden med arbeiderdetaljer. I **handlingsruten** klikker du **Oppsett** \>**Fordelingsteam** for å åpne skjemaet **Fordel arbeidere**.

2.  I **Fordelingsteam**-feltet velger du teamet du vil tilordne arbeideren til.

## <a name="assign-a-preferred-technician-to-a-service-agreement"></a>Tilordne en foretrukket tekniker til en serviceavtale

1.  Klikk på **Servicestyring** \> **Serviceavtaler** \> **Serviceavtaler**. Dobbeltklikk en serviceavtale for å åpne detaljskjemaet.

2.  I fanen **Generelt** velger du feltet **Foretrukket tekniker**, og deretter velger du et medlem i det aktuelle fordelingsteamet som den foretrukne teknikeren for serviceavtalen.

## <a name="assign-a-preferred-technician-to-a-service-order"></a>Tilordne en foretrukket tekniker til en serviceordre

1.  Klikk på **Servicestyring** \> **Periodisk** \> **Tjenestefordeling**.
    

    > [!NOTE]
    > <P>I skjemaet <STRONG>Tjenestefordeling</STRONG> angir du et datointervall for fordelingsaktiviteter du vil vise. Velg også om lukkede aktiviteter skal vises og om fordelingsaktivitetslisten skal begrenses til grupper du tilhører eller har tillatelse til å overvåke. Klikk på <STRONG>OK</STRONG> for å åpne skjemaet <STRONG>Tjenestefordeling</STRONG>.</P>



2.  Velg serviceaktivitetslinjen du vil endre.

3.  I fanen **Relatert** bruker du **Arbeider**-listen til å tilordne et medlem av korrekt fordelingsgruppe til foretrukket tekniker for serviceutkallingen.

## <a name="see-also"></a>Se også

[Oversikt over å utvikle og etablere serviceavtaler](service-agreements.md)

[Opprette serviceordrer manuelt](create-service-orders-manually.md)

[Serviceavtaler (skjema)](https://technet.microsoft.com/library/aa617823\(v=ax.60\))
  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]