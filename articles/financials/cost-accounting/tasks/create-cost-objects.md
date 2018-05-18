--- 
title: 'Opprette kostnadsobjekter  '
description: "Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for Dynamics 365 for Finance and Operations-kostsenter til kostnadsregnskap via en datakobling."
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a0739304723d19b910388893d08e8c36a1f49d13
ms.openlocfilehash: 21fa90557b665e0777935cc6bae8cd9f1c29cb60
ms.contentlocale: nb-no
ms.lasthandoff: 03/26/2018

---
# <a name="create-cost-objects"></a>Opprette kostnadsobjekter   

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåten viser hvordan du oppretter kostnadsobjekter ved å importere finansdimensjonen for Dynamics 365 for Finance and Operations-kostsenter til kostnadsregnskap via en datakobling. Demonstrasjonsdatafirmaet USMF ble brukt til å opprette denne prosedyren. Denne fremgangsmåten gjelder for en kostnadsregnskapsfunksjon som ble lagt til i Dynamics 365 for Operations, versjon 1611.


## <a name="create-new-cost-objects"></a>Opprette nye kostnadsobjekter
1. Gå til Kostnadsregnskap > Dimensjoner > Kostnadsobjektdimensjoner.
2. Klikk Ny.
3. Skriv inn en verdi i Navn-feltet.
4. Angi eller velg en verdi i feltet Datakobling for dimensjonsmedlemmer.
5. Skriv inn en verdi i feltet Beskrivelse.
6. Klikk Lagre.

## <a name="configure-the-data-connector"></a>Konfigurere datakoblingen
1. Klikk Konfigurer dimensjonsmedlemsleverandør.
    * Velg CostCenter for å importere CostCenter-dimensjonen i kostnadsregnskap.  
2. Velg Kostsenter i feltet Dimensjonsnavn.
3. Klikk OK.

## <a name="import-cost-centers"></a>Importere kostsentre
1. Klikk Importer dimensjonsmedlemmer.
2. Klikk OK.

## <a name="view-the-imported-cost-centers"></a>Vise de importerte kostsentrene
1. Klikk Vis dimensjonsmedlemmer.


