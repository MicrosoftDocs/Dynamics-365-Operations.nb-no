---
title: Legge til feil i arbeidsordre
description: Dette emnet beskriver hvordan du legger til feilregistreringer i arbeidsordrer i Aktivastyring.
author: josaw1
manager: AnnBe
ms.date: 08/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2019-08-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 7c86973ca44d9113d14e180e27cc51343da5d2c0
ms.sourcegitcommit: f5bfa3212bc3ef7d944a358ef08fe8863fd93b91
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/16/2019
ms.locfileid: "1875824"
---
# <a name="add-fault-to-work-order"></a>Legge til feil i arbeidsordre

[!include [banner](../../includes/banner.md)]

[!include [banner](../../includes/preview-banner.md)]


Du kan legge til feil som er definert i feilutformingen, i en arbeidsordre. Anleggsmiddelet som er valgt i arbeidsordren, må inneholde anleggsmiddeltyper som har én eller flere feilposter tilknyttet. Les mer om oppsett i delen [Feilstyring](../setup-for-work-orders/fault-management.md).

1. Klikk på **Aktivastyring** > **Felles** > **Arbeidsordrer** > **Alle arbeidsordrer** eller **Aktive arbeidsordrer**.

2. I listen velger du arbeidsordren du vil utføre en feilregistrering for, og klikker på **Aktivumfeil**.

3. Klikk på **Legg til linje** på hurtigfanen **Symptomer**. Et sekvensielt feilnummer settes automatisk inn i **Feil**-feltet.

4. Velg det relevante symptomet i **Feilsymptom**-feltet.

5. Velg **Feilområde** og **Feiltype**.

6. Den gjeldende datoen settes automatisk inn i **Feildato**-feltet. Hvis det er nødvendig, kan du velge en annen dato.

7. I hurtigfanen **Årsaker til valgte symptom** legger du til en linje som beskriver årsaken til problemet.

8. I hurtigfanen **Løsninger på valgte symptom** legger du til en linje som beskriver en mulig løsning problemet.

9. Klikk **Lagre**.

![Figur 1](media/19-work-orders.png)


## <a name="view-asset-faults"></a>Vis aktivafeil

I listen **Aktivumfeil** kan du få en oversikt over alle feilene som er registrert på aktiva.

Klikk **Aktivastyring** > **Forespørsler** > **Aktivumfeil** > **Aktivafeil** for å åpne listen.


## <a name="print-asset-fault-report"></a>Skriv ut rapport for aktivumfeil

Fra listesiden **Alle aktiva** kan du skrive ut en rapport om aktivumfeil som viser alle feilregistreringer, i tillegg til en grafisk oversikt over feilstatistikk.

1. Klikk på **Aktivastyring** > **Felles** > **Aktiva** > **Alle aktiva**.

2. I listen **Aktiva** velger du aktivumet du vil skrive ut en feilrapport for.

3. I fanen **Generelt** > **delen Rapporter** klikker du **Aktivumfeil**.

4. Sett inn en bestemt periode, eller velg en feiltype.

5. Velg **OK** for å skrive ut rapporten.

>[!NOTE]
>Du kan også skrive ut en feilrapport for flere aktiva eller aktivatyper ved å klikke **Aktivastyring** > **Rapporter** > **Aktiva** > **Aktivafeil**.

