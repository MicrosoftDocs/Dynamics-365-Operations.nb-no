---
title: Beregne kapasitetsbelastning på planlagte arbeidsordrer
description: Dette emnet forklarer hvordan du beregner kapasitetsbelastning på planlagte arbeidsordrer i Aktivastyring.
author: johanhoffmann
ms.date: 08/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: ff244e51151a1cc0485cae25873566fa97253171516d48449fed75f070146431
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/05/2021
ms.locfileid: "6766224"
---
# <a name="calculate-capacity-load-on-scheduled-work-orders"></a>Beregne kapasitetsbelastning på planlagte arbeidsordrer

[!include [banner](../../includes/banner.md)]

 

Du kan beregne kapasitetsbelastning på planlagte arbeidsordrer for å få en oversikt over arbeidsbelastningen på ressurser for en bestemt periode. Beregninger kan gjøres for følgende ressurser: vedlikeholdspersoner, arbeidsgrupper, verktøy og aktiva.

1. Klikk på **Aktivastyring** > **Forespørsel** > **Planlegg** > **Kapasitetsbelastning**.

2. I dialogboksen **Beregn kapasitetsbelastning** > **Vis**-feltet velger du hvilken belastningstype du vi vil beregne: **Kapasitet**, **Reservert** eller **Rest**.

3. Velg **Ja** på veksleknappen **Hopp over null** hvis du ikke vil vise resultater med null timer.

4. Velg ressurstypene du vil beregne kapasitetsbelastningen for, ved å velge **Ja** på de aktuelle veksleknappene: **Arbeider**, **Vedlikeholdspersongruppe**, **Verktøy** og **Aktivum**.

5. Velg startdatoen for beregningen i **Fra dato**-feltet.

6. I **Intervalltype**-feltet velger du intervallet for beregningen: **Dag**, **Uke**, **Måned** eller **Kvartal**.

7. I **Periodefrekvens**-feltet setter du inn antall intervaller du vil beregne. Hvis du for eksempel har valgt **Dag** som intervalltype, og du setter inn tallet "5" i dette feltet, vil det bli opprettet en beregning på fem dager fra startdatoen.

8. Klikk på **OK** for å starte beregningen.

Figuren nedenfor viser resultatet av en beregning som dekker tre uker for belastningstypen **Reservert**.

![Figur 1.](media/08-work-order-scheduling.png)

[!NOTE]
Hvis du velger belastningstypene **Kapasitet** eller **Rest** for beregningen, vil det samme resultatet vises hvis det ikke er gjort reservasjoner for ressursene i den valgte perioden.

Se [Beregne kapasitetsbelastning](../capacity-planning/calculate-capacity-load.md) for informasjon om hvordan du beregner kapasitetsbelastning på vedlikeholdsplanlinjer og ikke planlagte arbeidsordrer.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]