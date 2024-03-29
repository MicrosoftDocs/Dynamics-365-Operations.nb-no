---
title: Opprette serviceordrer automatisk
description: Du kan opprette serviceordrer for én serviceavtale eller for flere serviceavtaler.
author: sorenva
ms.date: 05/01/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SMAServiceOrderTable
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: sorenand
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: db9d337166f05f80cfdb9d4b82533117daa871e9
ms.sourcegitcommit: cfe8fbc202c3eb05d894076fdf99e46704f17365
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/15/2022
ms.locfileid: "9014727"
---
# <a name="create-service-orders-automatically"></a>Opprette serviceordrer automatisk    

[!include [banner](../includes/banner.md)]


Du kan opprette serviceordrer for én serviceavtale eller for flere serviceavtaler. Når de er opprettet, kan du vise serviceordrene i **Serviceordrer**-skjemaet.

Serviceordrer opprettes bare for serviceavtalens gyldighetsperiode. Hvis intervallet du angir i skjemaet **Opprett serviceordrer**, er før startdatoen eller etter sluttdatoen for serviceavtalen, opprettes det bare serviceordrer for den delen av intervallet som er innenfor serviceavtalens gyldighetsperiode.

Når du oppretter serviceordrer manuelt eller automatisk fra serviceavtalelinjen, må serviceordren falle innenfor tidsintervallet som er definert av start- og sluttdatoen for linjen, med mindre du ikke angir en sluttdato på linjen.

## <a name="create-service-orders-automatically-for-a-service-agreement"></a>Opprette serviceordrer for en serviceavtale automatisk

1.  Klikk på **Servicestyring** \> **Serviceavtaler** \> **Serviceavtaler**.

2.  Velg en serviceavtale.

3.  Klikk på fanen **Lever**, og klikk deretter **Planlagte serviceordrer**.

4.  Angi datoer i feltene **Fra dato** og **Til dato** for å definere serviceavtalens gyldighetsperiode.

5.  Merk av for **Vis infologg** for å vise en liste over serviceordrene som opprettes.

6.  Velg transaksjonstypene i feltgruppen **Inkluder transaksjonstyper**. Transaksjonstypene representerer linjene som opprettes i serviceavtalen, og hver transaksjonstype du velger, genererer flere serviceordrer, avhengig av serviceintervallet som er angitt for serviceavtalelinjen.

7.  Merk av for **Kontinuerlig** hvis du vil opprette eventuelle serviceordrer som mangler i en kontinuerlig serie av serviceordrer.

8.  Klikk på **OK**.

## <a name="create-service-orders-automatically-for-several-service-agreements"></a>Opprette serviceordrer for flere serviceavtaler automatisk

1.  Klikk på **Servicestyring** \> **Periodisk** \> **Serviceordrer** \> **Opprett serviceordrer**.

2.  Klikk på **Velg** for å angi valg for å legge til eller fjerne kriterier som skal brukes til å opprette serviceordrer.

3.  Klikk på **OK**.

## <a name="see-also"></a>Se også

[Serviceordrer](service-orders.md)

[Automatisk opprette serviceordrer](auto-create-service-orders.md)

  




[!INCLUDE[footer-include](../../includes/footer-banner.md)]