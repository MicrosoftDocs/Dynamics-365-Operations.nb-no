--- 
title: 'Opprette kostnadselementer  '
description: "Det finnes flere måter å opprette kostnadselementer på i kostnadsregnskap."
author: YuyuScheller
manager: AnnBe
ms.date: 10/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 0b1045610881bc272798f1176fbca58731e5d43b
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="create-cost-elements"></a>Opprette kostnadselementer   

[!include[task guide banner](../../includes/task-guide-banner.md)]

Det finnes flere måter å opprette kostnadselementer på i kostnadsregnskap. Denne fremgangsmåten viser hvordan du oppretter kostnadselementer ved å importere -hovedkontoer via en datakobling. Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren. Denne fremgangsmåten gjelder for en kostnadsregnskapsfunksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="create-new-cost-elements"></a>Opprette nye kostnadselementer
1. Gå til Kostnadsregnskap > Dimensjoner > Kostnadselementdimensjoner.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Klikk Lagre.

## <a name="configure-the-data-connector"></a>Konfigurere datakoblingen
1. Klikk Konfigurer dimensjonsmedlemsleverandør.
2. Skriv inn eller velg en verdi Kontoplan-feltet.
    * Velg Delt for å bruke den delte kontoplanen.  
3. Klikk Ny.
4. Merk den valgte raden i listen.
    * Du kan bruke filtre på kontoer som oppfyller kriteriene dine.  
5. Angi eller velg en verdi i feltet Fra hovedkonto.
6. Angi eller velg en verdi i feltet Til hovedkonto.
7. Klikk OK.

## <a name="import-main-accounts"></a>Importer hovedkontoer
1. Klikk Importer dimensjonsmedlemmer.
    * Hovedkontoer blir importert til kostnadsregnskap og brukt som kostnadselementer.  
2. Klikk OK.

## <a name="view-the-imported-accounts-as-cost-elements"></a>Vise de importerte kontoene som kostnadselementer
1. Klikk Vis dimensjonsmedlemmer.
    * Vis de importerte finanskontoene som kostnadselementer i bedriften som kostnader kan flyte til.  

