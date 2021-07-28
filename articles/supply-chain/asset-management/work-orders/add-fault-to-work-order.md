---
title: Legge til feil i arbeidsordre
description: Dette emnet beskriver hvordan du legger til feilregistreringer i arbeidsordrer i Aktivastyring.
author: johanhoffmann
ms.date: 10/15/2019
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
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 30cd077402928bc33949b821b9b114fbf8a632f2
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/06/2021
ms.locfileid: "6359155"
---
# <a name="add-fault-to-work-order"></a>Legge til feil i arbeidsordre

[!include [banner](../../includes/banner.md)]



Du kan legge til feil som er definert i feilutformingen, i en arbeidsordre. Én eller flere feilposter må knyttes til aktivatyper som brukes for aktivumet som velges i arbeidsordren. Hvis du vil ha mer informasjon om det generelle oppsettet for vurdering, kan du se [Feilstyring](../setup-for-work-orders/fault-management.md).

1. Velg **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. Velg arbeidsordren det skal utføres en feilregistrering på, og deretter går du til handlingsruten, fanen **Arbeidsordre**, gruppen **Aktiva** og velger **Aktivumfeil**.

3. Velg **Legg til linje** på hurtigfanen **Symptomer**. Et sekvensielt feilnummer settes automatisk inn i **Feil**-feltet.

4. Velg det relevante symptomet i **Feilsymptom**-feltet.

5. Velg de aktuelle verdiene i feltene **Feilområde** og **Feiltype**.

6. Den gjeldende datoen settes automatisk inn i **Feildato**-feltet. Du kan velge en annen dato etter behov.

7. I hurtigfanen **Årsaker til valgte symptom** legger du til en linje som beskriver årsaken til problemet.

8. I hurtigfanen **Løsninger på valgte symptom** legger du til en linje som beskriver en mulig løsning på problemet.

9. Velg **Lagre**.

Illustrasjonen nedenfor viser et eksempel på en feilregistrering.

![Figur 1.](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Vis aktivafeil

I listen **Aktivumfeil** kan du få en oversikt over alle feilene som er registrert på aktiva.

På listesiden **Aktivumfeil** kan du få en oversikt over alle feilene som er registrert på aktiva. Velg **Aktivastyring** > **Forespørsler** > **Aktivafeil** > **Aktivafeil** for å åpne listen.


## <a name="print-asset-fault-report"></a>Skriv ut rapport for aktivumfeil

Fra listesiden **Alle aktiva** kan du skrive ut en rapport om aktivumfeil som viser alle feilregistreringer, i tillegg til en grafisk oversikt over feilstatistikk.

1. Velg **Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva**.

2. Velg aktivumet det skal skrives ut en rapport for.

3. I handlingsruten velger du fanen **Generelt** i gruppen **Rapporter** og deretter **Aktivafeil**.

4. Sett inn en bestemt periode, eller velg en feiltype.

5. Velg **OK** for å skrive ut rapporten.

>[!NOTE]
>For å skrive ut en feilrapport for flere aktiva eller aktivatyper, velg **Aktivastyring** > **Rapporter** > **Aktiva** > **Aktivafeil**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]