---
title: Serviceintervaller
description: Serviceintervallet viser hvor ofte serviceordrelinjene skal opprettes for serviceavtalelinjene når du oppretter serviceordrer.
author: ShylaThompson
manager: tfehr
ms.date: 02/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SMAAgreementTable
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1027a6a1ddb1057ba039382d394522d6f9538a90
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4434496"
---
# <a name="service-intervals"></a>Serviceintervaller

[!include [banner](../includes/banner.md)]

Serviceavtaleintervallet viser hvor ofte serviceordrelinjene skal opprettes for serviceavtalelinjene når du oppretter serviceordrer automatisk.

Når du oppretter serviceordrer automatisk, opprettes serviceordrelinjer i samsvar med det intervallet du har angitt for serviceavtalelinjen fra startdatoen for avtalelinjen.

Hvis **Intervall**-feltet for en serviceavtalelinje på **Serviceavtaler**-siden er tomt, gjelder linjen et engangstilfelle, og brukes ikke til å opprette gjentatte serviceordrer.

## <a name="example"></a>Eksempel

Dette eksemplet viser hvordan et serviceintervall påvirker serviceavtalelinjer og serviceordrelinjer i en serviceordre.

### <a name="create-a-service-agreement"></a>Opprette en serviceavtale

Først oppretter du en serviceavtale og setter **Kombiner serviceordrer** til **Etter serviceavtale**.

1. Klikk på **Serviceavtaler**.
2. I **Handlingsruten** i **Serviceavtale**-kategorien i **Ny**-gruppen klikker du **Serviceavtale** for å opprette en ny serviceavtale.
3. Angi en beskrivelse, velg et prosjekt i **Prosjekt-ID**-feltet, og angi en dato i **Startdato**-feltet.
4. I **Kombiner serviceordrer**-feltet velger du **Etter serviceavtale**.

Du har nå opprettet følgende serviceavtale:

| Project      | Startdato                                                                         |
|--------------|------------------------------------------------------------------------------------|
| Ditt prosjekt | Datoen du angav for prosjektet. I dette eksemplet brukes gjeldende dato. |

### <a name="create-a-service-agreement-line"></a>Opprette en serviceavtalelinje

Deretter oppretter du en serviceavtalelinje som har transaksjonstypen **Time**.

For å fullføre denne delen, må du opprette et serviceintervall på 10 dager på **Serviceintervaller**-siden. 

1. Velg serviceavtalen du nettopp opprettet. 
2. På **Linjer**-hurtigkategorien, klikk **Legg til** for å opprette en ny linje i den nedre ruten på **Serviceavtaler**-siden.
3. Velg **Time** i **Transaksjonstype**-feltet.
4. I **Arbeider**-feltet velger du arbeideren som skal levere servicen.
5. Velg 10-dagersintervallet i feltet **Serviceintervall**.

Du har nå opprettet en serviceavtalelinje med følgende informasjon:

| transaksjonstype | Startdato                               | Serviceintervall |
|------------------|------------------------------------------|------------------|
| Time             | Den gjeldende datoen.                        | Hver 10. dag    |
| Arbeider           | Arbeideren som skal utføre servicen. |                  |

Det er ikke angitt noe tidsvindu for linjen. 

### <a name="create-planned-service-orders"></a>Opprette planlagte serviceordrer

Du kan nå opprette planlagte serviceordrer og serviceordrelinjer for kommende måned.

1. På **Serviceavtaler**-siden i **handlingsruten** i **Lever**-fanen, klikker du **Planlagte serviceordrer**.
2. På **Opprett serviceordrer**-siden skriver du inn gjeldende dato i **Fra dato**-feltet og en dato som er én måned fra gjeldende dato i **Til dato**-feltet.
3. Sett **Time**-glidebryteren til **Ja**. 
4. Klikk **OK**.

Fordi det ikke finnes noen grupperinger i serviceordren (definert med alternativet **Etter serviceavtale** i feltet **Kombiner serviceordrer**), blir det opprettet én serviceordrelinje per serviceordre.

### <a name="service-orders-created"></a>Opprettede serviceordrer

Tre serviceordrelinjer er opprettet innenfor tidsrammen du angav i dialogboksen **Opprett serviceordrer**. Du kan vise serviceordrelinjene på **Serviceavtaler**-siden (**Handlingsrute** \> **Lever**-kategorien \> **Vis**-knappen).

## <a name="related-topics"></a>Relaterte emner

[Definere serviceintervaller](set-up-service-intervals.md)  



[!INCLUDE[footer-include](../../includes/footer-banner.md)]