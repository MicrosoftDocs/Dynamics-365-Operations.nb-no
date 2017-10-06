--- 
title: Behandle og spore kildedata
description: "All databehandling kjøres av jobber."
author: YuyuScheller
manager: AnnBe
ms.date: 06/27/2017
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
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 9de7d5d241a65add894e0c6ae4840cd05753a419
ms.contentlocale: nb-no
ms.lasthandoff: 07/27/2017

---
# <a name="process-and-trace-source-data"></a>Behandle og spore kildedata

[!include[task guide banner](../../includes/task-guide-banner.md)]

All databehandling kjøres av jobber. For hver enkelt leverandør for jobb og data opprettes en journal til dokumentet som prosessen har blitt kjørt, og som oppføringene som ble behandlet i den gjeldende jobben. Bruk denne fremgangsmåten til å definere en datakilde, og deretter spore opprinnelsen til en bestemt kostpost. Denne registreringen bruker USP2-demodatafirmaet. Før du fullfører denne oppgaven, må du se gjennom følgende oppgaveveiledninger: "Opprette kostnadsregnskapsfinans", "Definere kostnadskontrollenheter" og "Administrere datakilde for kostnadsregnskapsfinans".

1. Gå til Kostnadsregnskap > Finansoppsett > Kostnadsregnskapsfinans.
2. Finn og velg ønsket post i listen.
    * Velg kostnadsregnskapsfinans som du opprettet tidligere.  
3. Klikk Faktiske versjoner.
4. I handlingsruten, klikker du kilden for databehandling.
5. Klikk Overføringsjournaler for økonomimoduloppføring.
6. Finn og velg ønsket post i listen.
7. Klikk Journaloppføringer.
8. Merk den valgte raden i listen.
9. Klikk Kostnadsoppføringer.
10. Klikk Kildeoppføring.
11. I handlingsruten, klikker du kilden for databehandling.
12. Klikk Økonomimodul.
13. Angi eller velg en verdi i feltet Regnskapskalenderperiode.
    * I dette eksemplet, velg regnskapsår 2017, periode 9.  
14. Klikk OK.

