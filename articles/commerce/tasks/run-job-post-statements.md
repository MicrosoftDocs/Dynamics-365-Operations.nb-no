---
title: Konfigurere og kjøre jobben for å postere utdrag
description: Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å postere utdrag for en valgt butikk eller en gruppe med butikker.
author: josaw1
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: RetailChannelOperationsWorkspace, RetailOperatingUnitPicker, SysRecurrence
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f89203850b302b769b22920fa5c42d2b0b877684
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/13/2020
ms.locfileid: "4414676"
---
# <a name="configure-and-run-job-to-post-statements"></a>Konfigurere og kjøre jobben for å postere utdrag

[!include [banner](../includes/banner.md)]

Denne prosedyren hjelper med å konfigurere og kjøre en gjentakende satsvis jobb for å postere utdrag for en valgt butikk eller en gruppe med butikker. Denne prosedyren bruker firmaet USRT i demonstrasjonsdataene.

1. Gå til Alle arbeidsområder > .. > Finans for butikk.
2. Klikk på Poster utdrag satsvis.
    * Velg et organisasjonshierarki, og velg deretter en enkelt butikk eller node i organisasjonsnodetreet. Velg en node hvis du vil opprette den satsvise jobben for en gruppe med butikker.  
    * Klikk pilen for å legge til valget.  
3. Klikk på kategorien Kjør i bakgrunnen. ![Kjør i bakgrunnen](../dev-itpro/media/runbackground.png "Kjør i bakgrunnen") 
4. Merk av eller fjern merket for Satsvis behandling.
![Satsvis behandling](../dev-itpro/media/batchprocessing.png "Satsvis behandling og gjentakelse") 
5. Klikk Regelmessighet.
6. Angi en dato i Startdato-feltet.
7. Angi et tidspunkt i Starttidspunkt-feltet.
    * Velg om du vil avslutte gjentakelsen etter et bestemt antall kjøringer, på en bestemt dato eller aldri. Velg deretter de ulike alternativene for å definere hvor ofte du vil at jobben skal kjøres.  
8. Klikk OK.
9. Klikk OK.



[!INCLUDE[footer-include](../../includes/footer-banner.md)]